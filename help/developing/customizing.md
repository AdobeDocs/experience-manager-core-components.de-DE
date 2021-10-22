---
title: Anpassen der Kernkomponenten
description: Die Kernkomponenten implementieren verschiedene Muster, die eine einfache Anpassung ermöglichen, von einfachen Stilen bis hin zur Wiederverwendung erweiterter Funktionen.
role: Architect, Developer, Admin
exl-id: ec4b918b-bc70-4d72-ba84-a24556aedb41
source-git-commit: 2ac16b15718128feefbe903e92f276b16fe96f69
workflow-type: ht
source-wordcount: '1100'
ht-degree: 100%

---

# Anpassen der Kernkomponenten {#customizing-core-components}

Die [Kernkomponenten](overview.md) implementieren verschiedene Muster, die eine einfache Anpassung ermöglichen, von einfachen Stilen bis hin zur Wiederverwendung erweiterter Funktionen.

## Flexible Architektur {#flexible-architecture}

Die Kernkomponenten wurden von Anfang an so entworfen, dass sie flexibel und erweiterbar sind. Ein Überblick über ihre Architektur zeigt an, wo Anpassungen vorgenommen werden können.

![Architektur der Kernkomponenten](/help/assets/screen_shot_2018-12-07at093742.png)

* Im [Dialogfeld „Design“](/help/get-started/authoring.md#edit-and-design-dialogs) wird definiert, was Autoren im Dialogfeld „Bearbeiten“ tun können und was nicht.
* Das [Dialogfeld „Bearbeiten“](/help/get-started/authoring.md#edit-and-design-dialogs) zeigt Autoren nur die Optionen an, die sie verwenden dürfen.
* [Das Sling-Modell](#customizing-the-logic-of-a-core-component) überprüft und bereitet den Inhalt für die Ansicht (Vorlage) vor.
* [Das Ergebnis des Sling-Modells](#customizing-the-logic-of-a-core-component) kann für die SPA-Anwendungsfälle in JSON serialisiert werden.
* [Das HTL rendert die HTML](#customizing-the-markup) Server-seitig für die herkömmliche Server-seitige Wiedergabe.
* [Die HTML-Ausgabe](#customizing-the-markup) ist semantisch, barrierefrei, suchmaschinenoptimiert und leicht zu gestalten.

Und alle Kernkomponenten implementieren das [Stilsystem](#styling-the-components).

## AEM-Projektarchetyp {#aem-project-archetype}

[Der AEM-Projektarchetyp](/help/developing/archetype/overview.md) erstellt ein Adobe Experience Manager-Minimalprojekt als Ausgangspunkt für Ihre eigenen Projekte, einschließlich eines Beispiels für eine benutzerdefinierte HTL-Komponente mit SlingModels, um die Logik und ordnungsgemäße Implementierung der Kernkomponenten mit dem empfohlenen Proxy-Muster zu gewährleisten.

## Anpassungsmuster {#customization-patterns}

### Anpassen von Dialogen {#customizing-dialogs}

Es ist möglicherweise sinnvoll, die in einem Kernkomponentendialogfeld verfügbaren Konfigurationsoptionen anzupassen, entweder [im Dialogfeld „Design“ oder im Dialogfeld „Bearbeiten“](/help/get-started/authoring.md).

Jedes Dialogfeld hat eine einheitliche Knotenstruktur. Es wird empfohlen, dass diese Struktur in einer inhärenten Komponente repliziert wird, sodass [Sling Ressource Merger](https://helpx.adobe.com/de/experience-manager/6-4/sites/developing/using/sling-resource-merger.html) und [Ausblende-Bedingungen](https://helpx.adobe.com/de/experience-manager/6-5/sites/developing/using/hide-conditions.html) genutzt werden können, um Bereiche des Originaldialogs auszublenden, zu ersetzen oder neu anzuordnen. Die zu replizierende Struktur ist als beliebiger Wert bis zur Registerkartenelement-Knotenebene definiert.

Damit alle Änderungen an einem Dialogfeld in seiner aktuellen Version vollständig kompatibel sind, ist es äußerst wichtig, dass Strukturen unterhalb der Registerkartenelementebene nicht angerührt werden (ausgeblendet, hinzugefügt, ersetzt, neu angeordnet usw.). Stattdessen sollte ein übergeordnetes Tab-Element über die Eigenschaft `sling:hideResource` ausgeblendet werden (siehe [ Eigenschaften der Zusammenführung von Sling-Ressourcen ](https://helpx.adobe.com/de/experience-manager/6-5/sites/developing/using/sling-resource-merger.html)) und neue Tab-Elemente hinzugefügt werden, die die maßgeschneiderten Konfigurationsfelder enthalten. `sling:orderBefore` kann verwendet werden, um die Registerkartenelemente bei Bedarf neu anzuordnen.

Das folgende Dialogfeld zeigt die empfohlene Dialogfeldstruktur sowie das Ausblenden und Ersetzen einer vererbten Registerkarte wie oben beschrieben:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<jcr:root xmlns:sling="https://sling.apache.org/jcr/sling/1.0"
          xmlns:jcr="https://www.jcp.org/jcr/1.0"
          xmlns:nt="https://www.jcp.org/jcr/nt/1.0"
          xmlns:granite="https://www.adobe.com/jcr/granite/1.0"
          jcr:primaryType="nt:unstructured">
    <content jcr:primaryType="nt:unstructured">
        <items jcr:primaryType="nt:unstructured">
            <tabs jcr:primaryType="nt:unstructured">
                <items jcr:primaryType="nt:unstructured">
                        <originalTab
                                jcr:primaryType="nt:unstructured"
                                sling:hideResource="true"/>
                        </originalTab>
                        <myTab
                               jcr:primaryType="nt:unstructured"
                               jcr:title="My Tab"
                               sling:resourceType="granite/ui/components/coral/foundation/container"/>
                               <!-- myTab content -->
                        </myTab>
                </items>
            </basic>
        </items>
    </content>
</jcr:root>
```

### Anpassen der Logik einer Kernkomponente {#customizing-the-logic-of-a-core-component}

Die Geschäftslogik für die Kernkomponenten ist in Sling-Modellen implementiert. Diese Logik kann mithilfe eines Sling-Delegationsmusters erweitert werden.

Beispielsweise verwendet die Titel-Kernkomponente die `jcr:title`-Eigenschaft der angeforderten Ressource, um den Titeltext zu liefern. Wenn keine `jcr:title`-Eigenschaft definiert ist, ist eine Ausweichmöglichkeit zum aktuellen Seitentitel implementiert. Wir möchten das Verhalten so ändern, dass der Titel der aktuellen Seite immer angezeigt wird.

Da die Implementierung der Modelle der Kernkomponenten privat ist, müssen sie mit einem Delegationsmuster erweitert werden.

```java
@Model(adaptables = SlingHttpServletRequest.class,
       adapters = Title.class,
       resourceType = "myproject/components/pageHeadline")
public class PageHeadline implements Title {
    @ScriptVariable private Page currentPage;
    @Self @Via(type = ResourceSuperType.class)
    private Title title;
    @Override public String getText() {
        return currentPage.getTitle();
    }
    @Override public String getType() {
        return title.getType();
    }
}
```

Weitere Informationen zum Delegierungsmuster finden Sie im GitHub Wiki-Artikel [Delegierungsmuster für Sling-Modelle](https://github.com/adobe/aem-core-wcm-components/wiki/Delegation-Pattern-for-Sling-Models).

### Anpassen des Markup {#customizing-the-markup}

Manchmal erfordert erweitertes Formatieren eine andere Markup-Struktur der Komponente.

Hierfür können Sie ganz einfach die zu ändernden HTL-Dateien aus der Kernkomponente in die [Proxy-Komponente](guidelines.md#proxy-component-pattern) kopieren.

Wenn Sie das Beispiel der Breadcrumb-Kernkomponente erneut aufrufen, um die Markup-Ausgabe anzupassen, muss die `breadcrumb.html`-Datei in die Site-spezifische Komponente kopiert werden, die über ein `sling:resourceSuperTypes` verfügt, das auf die Breadcrumb-Kernkomponente zeigt.

### Formatieren der Komponenten {#styling-the-components}

Die erste Art der Anpassung besteht darin, CSS-Stile anzuwenden.

Um dies zu vereinfachen, rendern die Kernkomponenten das Semantik-Markup und folgen einer standardisierten Benennungskonvention, die von [Bootstrap](https://getbootstrap.com/) / inspiriert wurde. Um die Stile für die einzelnen Komponenten einfach zu erreichen und zu benennen, wird jede Kernkomponente in ein DIV-Element mit den Klassen `cmp` und `cmp-<name>` eingeschlossen.

Betrachtet man beispielsweise die HTL-Datei der v1-Kern-Breadcrumb-Komponente: [ breadcrumb.html](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/breadcrumb/v2/breadcrumb/breadcrumb.html), so ergibt sich eine Hierarchie der ausgegebenen Elemente von `ol.breadcrumb > li.breadcrumb-item > a`. Um sicherzustellen, dass eine CSS-Regel nur die Breadcrumb-Klasse dieser Komponente betrifft, sollten alle Regeln in einem Namensbereich angeordnet werden, wie unten dargestellt:

```shell
.cmp-breadcrumb .breadcrumb {}  
.cmp-breadcrumb .breadcrumb-item {}  
.cmp-breadcrumb a {}
```

Darüber hinaus nutzt jede der Kernkomponenten die AEM-Funktion [Style System](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/style-system.html?lang=de), mit der Vorlagenautoren zusätzliche CSS-Klassennamen definieren können, die von den Seitenautoren auf die Komponente angewendet werden können. Auf diese Weise können Sie für jede Vorlage eine Liste der zulässigen Komponentenstile definieren und festlegen, ob eine dieser Komponenten standardmäßig auf alle Komponenten dieser Art angewendet werden soll.

## Upgrade-Kompatibilität von Anpassungen {#upgrade-compatibility-of-customizations}

Es gibt drei verschiedene Arten von Upgrades:

* Upgrade der AEM-Version
* Upgrade der Kernkomponenten auf eine neue Unterversion
* Upgrade der Kernkomponenten auf eine Hauptversion

Im Allgemeinen wirkt sich ein Upgrade von AEM auf eine neue Version nicht auf die Kernkomponenten oder die vorgenommenen Anpassungen aus, vorausgesetzt, die Komponentenversionen unterstützen auch die neue AEM-Version, auf die migriert wird, und Anpassungen verwenden keine APIs, die [veraltet oder entfernt](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/deprecated-removed-features.html?lang=de).

Das Aktualisieren der Kernkomponenten ohne Wechseln zu einer neueren Hauptversion sollte sich nicht auf Anpassungen auswirken, solange die auf dieser Seite beschriebenen Anpassungsmuster verwendet werden.

Wechseln zu einer neueren Hauptversion der Kernkomponenten ist nur für die Inhaltsstruktur kompatibel, Anpassungen müssen jedoch möglicherweise überarbeitet werden. Klare Änderungsprotokolle werden für jede Komponentenversion veröffentlicht, um die Änderungen hervorzuheben, die Auswirkungen auf die auf dieser Seite beschriebenen Anpassungen haben.

## Unterstützung von Anpassungen {#support-of-customizations}

Wie bei jeder AEM-Komponente gibt es einige Aspekte hinsichtlich der Anpassungen zu beachten:

1. **Ändern Sie den Code der Kernkomponenten nie direkt.**

   Dies würde dazu führen, dass sie nicht vollständig unterstützt werden und künftige Updates der Komponenten zu einem schmerzhaften Prozess machen. Verwenden Sie stattdessen die auf dieser Seite beschriebenen Anpassungsmethoden.

1. **Für benutzerdefinierten Code sind Sie selbst verantwortlich.**

   Unser Support-Programm deckt keinen benutzerdefinierten Code ab und gemeldete Probleme, die nicht mit Vanilla-Kernkomponenten reproduziert werden können, die [wie dokumentiert](/help/get-started/using.md) verwendet werden, werden nicht anerkannt.

1. **Achten Sie auf veraltete und entfernte Funktionen.**

   Stellen Sie bei jedem Upgrade jeder neuen AEM-Version sicher, dass alle verwendeten APIs immer aktuell sind, indem Sie die Seite [Veraltete und entfernte Funktionen](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/deprecated-removed-features.html?lang=de) im Auge behalten.

Siehe auch Abschnitt zur [Kernkomponentenunterstützung](overview.md#core-component-support).

**Lesen Sie als Nächstes:**

* [Verwenden von Kernkomponenten](/help/get-started/using.md) - Starten Sie mit Kernkomponenten in Ihrem eigenen Projekt.
* [Komponentenrichtlinien](guidelines.md) - Lernen Sie die Implementierungsmuster der Kernkomponenten kennen.
