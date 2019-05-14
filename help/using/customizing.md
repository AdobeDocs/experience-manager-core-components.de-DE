---
title: Anpassen der Kernkomponenten
seo-title: Anpassen der Kernkomponenten
description: Die Kernkomponenten implementieren verschiedene Muster, die eine einfache Anpassung ermöglichen, von einfachen Stilen bis zur Wiederverwendung erweiterter Funktionen.
seo-description: Die AEM Core-Komponenten implementieren verschiedene Muster, die eine einfache Anpassung ermöglichen, von einfachen Stilen bis zur Wiederverwendung erweiterter Funktionen.
uuid: 38 d 22 b 5-4867-4716-817 a -10 ee 2 f 8 de 6 f 5 f 5
contentOwner: Benutzer
content-type: Referenz
topic-tags: wird entwickelt
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-new
discoiquuid: 3 c 9 e 0 ade -1 ce 0-4 e 34-ae 04-8 da 63 f 9 b 6 c 4 f
translation-type: tm+mt
source-git-commit: 62643e5bd49ab006230f65004bb9374822dcc017

---


# Anpassen der Kernkomponenten{#customizing-core-components}

Die [Kernkomponenten](developing.md) implementieren verschiedene Muster, die eine einfache Anpassung ermöglichen, von einfachen Stilen bis zur Wiederverwendung erweiterter Funktionen.

## Flexible Architektur {#flexible-architecture}

Die Kernkomponenten wurden von Anfang an so entworfen, dass sie flexibel und erweiterbar sind. Ein Überblick über ihre Architektur zeigt an, wo Anpassungen vorgenommen werden können.

![Core Components Architecture](assets/screen_shot_2018-12-07at093742.png)

* [Im Design-Dialogfeld](authoring.md#edit-and-design-dialogs) wird definiert, was Autoren im Bearbeitungsdialogfeld tun können oder nicht.
* [Das Dialogfeld](authoring.md#edit-and-design-dialogs) &quot;Bearbeiten&quot; zeigt Autoren nur die Optionen an, die sie verwenden dürfen.
* [Das Sling-Modell](#customizing-the-logic-of-a-core-component) überprüft und bereitet den Inhalt für die Ansicht (Vorlage) vor.
* [Das Ergebnis des Sling-Modells](#customizing-the-logic-of-a-core-component) kann für die Anwendungsfälle in JSON serialisiert werden.
* [Das HTL rendert die HTML](#customizing-the-markup) -Serverseite für die herkömmliche serverseitige Wiedergabe.
* [Die HTML-Ausgabe](#customizing-the-markup) ist semantisch, barrierefrei, suchmaschinenoptimiert und leicht zu gestalten.

Alle Hauptkomponenten implementieren das [Stilsystem](customizing.md).

## Anpassungsmuster {#customization-patterns}

### Anpassen von Dialogen {#customizing-dialogs}

Es ist möglicherweise sinnvoll, die in einem Kernkomponentendialogfeld verfügbaren Konfigurationsoptionen anzupassen, entweder [im Design-Dialogfeld oder im Dialogfeld &quot;Bearbeiten](authoring.md)«.

Jedes Dialogfeld hat eine einheitliche Knotenstruktur. Es wird empfohlen, dass diese Struktur in einer vererbenden Komponente repliziert wird, sodass [Sling Resource Fusion](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/sling-resource-merger.html) und [Bedingungen](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/hide-conditions.html) zum Ausblenden, Ersetzen oder Neuordnen von Abschnitten des ursprünglichen Dialogfelds verwendet werden können. Die zu replizierende Struktur ist als beliebiger Wert bis zur Node-Elementebene definiert.

Damit alle Änderungen an einem Dialogfeld in der aktuellen Version vollständig kompatibel sind, ist es äußerst wichtig, dass Strukturen unterhalb der Registerelementebene nicht weitergeleitet werden (ausgeblendet, hinzugefügt, ersetzt, neu angeordnet usw.). Stattdessen sollte ein Tabulatorelement aus der übergeordneten Eigenschaft über die `sling:hideResource` Eigenschaft ausgeblendet werden (siehe [Sling Resource Fusion-Eigenschaften](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/sling-resource-merger.html)) und neue Tabulatorelemente hinzugefügt, die die bespoke-Konfigurationsfelder enthalten. `sling:orderBefore` kann verwendet werden, um die Tab-Elemente bei Bedarf neu anzuordnen.

Das folgende Dialogfeld zeigt die empfohlene Dialogfeldstruktur sowie das Ausblenden und Ersetzen einer vererbten Registerkarte wie oben beschrieben:

<!-- 

Comment Type: annotation
Last Modified By: ims-author-CE1E2CE451D1F0680A490D45@AdobeID
Last Modified Date: 2017-04-17T17:43:20.265-0400

Should we provide guidance on how to name their CSS classes, etc. to align to component re-usability best-practices? We tout that we follow bootstrap css naming, should we be counseling customers to align similarly? .cmp- 
<component name="">
  -- 
 <element>
   - 
  <element descriptor="">
    ? 
  </element> 
 </element> 
</component>

 -->

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

### Anpassen der Logik einer Core-Komponente {#customizing-the-logic-of-a-core-component}

Die Geschäftslogik für die Kernkomponenten ist in Sling-Modellen implementiert. Diese Logik kann mithilfe eines Sling-Delegationsmusters erweitert werden.

Beispielsweise verwendet die title-Core-Komponente die `jcr:title` Eigenschaft der angeforderten Ressource, um den Titeltext anzugeben. Wenn keine `jcr:title` Eigenschaft definiert ist, wird eine Ausweichmöglichkeit zum aktuellen Seitentitel implementiert. Wir möchten das Verhalten so ändern, dass der Titel der aktuellen Seite immer angezeigt wird.

Da die Implementierung der Modelle Kernkomponenten privat ist, müssen sie mit einem Delegationsmuster erweitert werden.

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

Weitere Informationen zum Delegationsmuster finden Sie im Artikel &quot;Delegationsmuster für Kernkomponenten&quot; des github Wiki-Artikels [für Sling-Modelle](https://github.com/adobe/aem-core-wcm-components/wiki/Delegation-Pattern-for-Sling-Models).

### Anpassen der Markierung {#customizing-the-markup}

Manchmal erfordert erweiterte Formatierung eine andere Markierungsstruktur der Komponente.

Dies kann einfach erfolgen, indem Sie die HTL-Dateien kopieren, die aus der Core-Komponente in die Proxy-Komponente geändert werden müssen.

Wenn Sie das Beispiel der Core-Breadcrumb-Komponente erneut aufrufen, um die Markup-Ausgabe anzupassen, muss die `breadcrumb.html` Datei in die sitespezifische Komponente kopiert werden, die über einen `sling:resourceSuperTypes` Punkt auf die Core-Breadcrumb-Komponente verfügt.

<!-- 

Comment Type: annotation
Last Modified By: ims-author-CE1E2CE451D1F0680A490D45@AdobeID
Last Modified Date: 2017-04-17T17:43:20.265-0400

Should we provide guidance on how to name their CSS classes, etc. to align to component re-usability best-practices? We tout that we follow bootstrap css naming, should we be counseling customers to align similarly? .cmp- 
<component name="">
  -- 
 <element>
   - 
  <element descriptor="">
    ? 
  </element> 
 </element> 
</component>

 -->

### Formatieren der Komponenten {#styling-the-components}

Die erste Art der Anpassung besteht darin, CSS-Stile anzuwenden.

Um dies zu vereinfachen, rendert die Kernkomponenten das Semantic-Markup und folgen einer standardisierten Benennungskonvention, die vom [Bootstrap inspiriert](https://getbootstrap.com/)wurde. Um die Stile für die einzelnen Komponenten einfach zu erreichen und zu benennen, wird jede Core-Komponente in ein DIV-Element mit den &quot; `cmp`und&quot; `cmp-<name>`-Klassen eingeschlossen.

Beispielsweise die HTL-Datei der Core-Breadcrumb-Komponente von v 1: [breadcrumb.html](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/breadcrumb/v2/breadcrumb/breadcrumb.html). Wir sehen, dass die Hierarchie der Elemente `ol.breadcrumb > li.breadcrumb-item > a`ausgeblendet ist. Um sicherzustellen, dass eine CSS-Regel nur die Breadcrumb-Klasse dieser Komponente betrifft, sollten alle Regeln wie unten dargestellt benannt werden:

```shell
.cmp-breadcrumb .breadcrumb {}  
.cmp-breadcrumb .breadcrumb-item {}  
.cmp-breadcrumb a {}
```

Darüber hinaus nutzen alle Kernkomponenten die AEM [-Stilsystemfunktion](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/style-system.html) , mit der Vorlagenautoren zusätzliche CSS-Klassennamen definieren können, die von den Seitenverfassern auf die Komponente angewendet werden können. Auf diese Weise können Sie für jede Vorlage eine Liste der zulässigen Komponentenstile definieren und ob eine dieser Komponenten standardmäßig auf alle Komponenten dieser Art angewendet werden soll.

## Upgrade-Kompatibilität von Anpassungen {#upgrade-compatibility-of-customizations}

Es gibt drei verschiedene Arten von Aktualisierungen:

* Aktualisieren der Version von AEM
* Aktualisieren der Kernkomponenten auf eine neue Version
* Aktualisieren der Kernkomponenten auf eine Hauptversion

Im Allgemeinen wirkt sich das Aktualisieren von AEM auf eine neue Version nicht auf die Kernkomponenten oder die vorgenommenen Anpassungen aus, sofern die Versionen der Komponenten auch die neue AEM-Version unterstützen, die migriert wird, und dass diese Anpassungen keine apis verwenden, die [nicht mehr unterstützt oder entfernt](https://helpx.adobe.com/experience-manager/6-5/release-notes/deprecated-removed-features.html)wurden.

Das Aktualisieren der Core-Komponenten ohne Wechsel zu einer neueren Hauptversion sollte sich nicht auf Anpassungen auswirken, solange die auf dieser Seite beschriebenen Anpassungsmuster verwendet werden.

Wechsel zu einer neueren Hauptversion der Kernkomponenten ist nur für die Inhaltsstruktur kompatibel, Anpassungen müssen jedoch möglicherweise refaktoriert werden. Klare Änderungsprotokolle werden für jede Komponentenversion veröffentlicht, um die Änderungen hervorzuheben, die Auswirkungen auf die auf dieser Seite beschriebenen Anpassungen haben.

## Unterstützung von Anpassungen {#support-of-customizations}

Wie bei jeder AEM-Komponente gibt es einige Aspekte hinsichtlich der Anpassungen:

1. **Ändern Sie den Code der Kernkomponenten nie direkt.**

   Dies würde dazu führen, dass sie nicht vollständig unterstützt werden und künftige Updates der Komponenten einen schmerzhaften Prozess vornehmen. Verwenden Sie stattdessen die auf dieser Seite beschriebenen Anpassungsmethoden.

1. **Benutzerdefinierter Code ist Ihre eigene Verantwortung.**

   Unser Support-Programm deckt keine benutzerspezifischen Code ab und meldet Probleme, die nicht mit Vanilla Core Components reproduziert werden können, die [wie dokumentiert](using.md) verwendet werden.

1. **Beobachten Sie die veraltete und entfernte Funktion.**

   Achten Sie bei jeder neuen AEM-Version darauf, dass alle verwendeten API noch aktuell sind, indem Sie die Seite [&quot;Veraltete und entfernte Funktionen](https://helpx.adobe.com/experience-manager/6-5/release-notes/deprecated-removed-features.html) &quot; verwenden.

Siehe auch Abschnitt zur [Core-Komponentenunterstützung](developing.md#core-component-support) .

**Lesen Sie als Nächstes:**

* [Verwenden Kernkomponenten](using.md) - rufen Sie die Kernkomponenten in Ihrem eigenen Projekt auf.
* [Komponentenrichtlinien](guidelines.md) - um die Implementierungsmuster der Kernkomponenten zu erfahren.
