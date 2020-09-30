---
title: Komponentenrichtlinien
description: Die Kernkomponenten folgen modernen Implementierungsmustern, die sich stark von den Foundation-Komponenten unterscheiden.
translation-type: tm+mt
source-git-commit: 2926c51c2ab97b50b9ec4942cd5415c15a1411b6
workflow-type: tm+mt
source-wordcount: '1259'
ht-degree: 99%

---


# Komponentenrichtlinien {#component-guidelines}

Die [Kernkomponenten](overview.md) folgen modernen Implementierungsmustern, die sich stark von den Foundation-Komponenten unterscheiden.

Diese Seite erklärt diese Muster und wann Sie sie verwenden müssen, um Ihre eigenen autorenfähigen Komponenten zu erstellen. Der erste Abschnitt [Allgemeine Komponentenmuster](#general-component-patterns)gilt für jede beliebige Komponente, während der zweite Abschnitt [Wiederverwendbare Komponentenmuster](#reusable-component-patterns) für Komponenten gilt, die für alle Sites oder Projekte wiederverwendet werden sollen, wie z. B. die Kernkomponenten.

## Allgemeine Komponentenmuster {#general-component-patterns}

Die Richtlinien in diesem Abschnitt werden für jede Art von Komponente empfohlen, unabhängig davon, ob die Komponente spezifisch für ein einzelnes Projekt ist oder ob die Komponente für eine breite Wiederverwendung in Sites oder Projekten bestimmt ist.

### Konfigurierbare Komponenten {#configurable-components}

Komponenten können Dialogfelder mit einer Vielzahl von Optionen haben. Dies sollte genutzt werden, um Komponenten flexibel und konfigurierbar zu machen und die Implementierung mehrerer Komponenten, die hauptsächlich Variationen voneinander darstellen, zu vermeiden.

Wenn ein Kabelgitter oder ein Design Variationen ähnlicher Elemente enthält, sollten diese Variationen typischerweise nicht als verschiedene Komponenten implementiert werden, sondern als eine Komponente mit Optionen zur Auswahl zwischen den Variationen.

Wenn Sie diesen Schritt weiter durchführen möchten, wenn Komponenten über mehrere Sites oder Projekte hinweg wiederverwendet werden, lesen Sie den Abschnitt [Vorkonfigurierbare Funktionen](#pre-configurable-capabilities).

### Problemtrennung {#separation-of-concerns}

Es empfiehlt sich, die Logik (oder das Modell) einer Komponente getrennt von der Markup-Vorlage (oder der Ansicht) zu halten. Es gibt verschiedene Möglichkeiten, dies zu erreichen. Es wird jedoch empfohlen, [ Sling-Modelle ](https://sling.apache.org/documentation/bundles/models.html) für die Logik und [ HTML-Vorlagensprache ](https://docs.adobe.com/content/help/de-DE/experience-manager-htl/using/overview.html) (HTL) für das Markup zu verwenden, wie dies auch die Kernkomponenten tun.

Sling-Modelle sind eine Reihe von Java-Anmerkungen, um schnell auf benötigte Variablen von POJOs zuzugreifen und daher eine einfache, leistungsstarke und effiziente Möglichkeit, Java-Logik für Komponenten zu implementieren.

HTL wurde als sichere und einfache Vorlagensprache entwickelt, die auf AEM zugeschnitten ist. Es kann viele Formen der Logik aufrufen, was es sehr flexibel macht.

## Wiederverwendbare Komponentenmuster {#reusable-component-patterns}

Die Richtlinien in diesem Abschnitt können für jede Art von Komponente ebenfalls verwendet werden. Für Komponenten, die über mehrere Sites oder Projekte hinweg wiederverwendet werden sollen, wie z. B. Kernkomponenten, sind sie jedoch am sinnvollsten. Diese Richtlinien können daher für Komponenten ignoriert werden, die nur auf einer einzelnen Site oder einem einzelnen Projekt verwendet werden.

### Vorkonfigurierbare Funktionen {#pre-configurable-capabilities}

Neben dem Bearbeitungsdialogfeld, das von den Seitenautoren verwendet wird, können Komponenten auch ein Dialogfeld „Design“ für Vorlagenautoren haben, um diese vorkonfigurieren zu können. Der [Vorlageneditor](https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/sites/authoring/features/templates.translate.html) ermöglicht das Einrichten aller Vorkonfigurationen, die als &quot;Richtlinien&quot; bezeichnet werden.

Um Komponenten so wiederverwendbar wie möglich zu machen, sollten sie mit aussagekräftigen Optionen zur Vorkonfiguration bereitgestellt werden. Dies ermöglicht das Aktivieren oder Deaktivieren von Funktionen der Komponenten, die den spezifischen Anforderungen verschiedener Sites entsprechen.

### Proxy-Komponentenmuster {#proxy-component-pattern}

Da jede Inhalts-Ressource eine `sling:resourceType` Eigenschaft aufweist, die auf die Komponente verweist, um sie zu rendern, empfiehlt es sich in der Regel, diese Eigenschaften auf Site-spezifische Komponenten zu verweisen, anstatt auf Komponenten zu verweisen, die von mehreren Sites gemeinsam genutzt werden. Dies bietet mehr Flexibilität und verhindert eine Refaktorierung von Inhalten, wenn eine Site ein anderes Verhalten für eine Komponente benötigt, da diese Anpassung dann auf der Site-spezifischen Komponente vorgenommen werden kann und sich nicht auf die anderen Sites auswirkt.

Damit die projektspezifischen Komponenten jedoch keinen Code duplizieren, sollten sie jeweils auf die freigegebene übergeordnete Komponente mit der `sling:resourceSuperType`-Eigenschaft verweisen. Diese projektspezifischen Komponenten, die überwiegend einfach auf die übergeordneten Komponenten verweisen, werden als „Proxy-Komponenten“ bezeichnet. Proxy-Komponenten können vollständig leer sein, wenn sie die Funktionalität vollständig übernehmen, oder sie können einige Aspekte der Komponente neu definieren.

### Komponentenversionierung {#component-versioning}

Komponenten sollten im Laufe der Zeit vollständig kompatibel bleiben. Doch manchmal sind Änderungen, die nicht kompatibel bleiben können, erforderlich. Eine Lösung für diese gegensätzlichen Anforderungen ist die Einführung der Komponentenversionierung durch Hinzufügen einer Nummer in ihrem Ressourcentyppfad und in den voll qualifizierten Java-Klassennamen ihrer Implementierungen. Diese Versionsnummer stellt eine Hauptversion im Sinne der [Richtlinien für die semantische Versionierung](https://semver.org/) dar, die nur für Änderungen erhöht wird, die nicht abwärtskompatibel sind.

Inkompatible Änderungen an den folgenden Aspekten von Komponenten führen zu einer neuen Version der Komponenten:

* Sling-Modelle (entsprechend den semantischen Versionierungsrichtlinien)
* HTL-Skripte und -Vorlagen
* HTML-Markup und CSS-Selektoren
* JSON-Darstellung
* Dialogfelder

Weitere Informationen finden Sie im Dokument [Versionsrichtlinien](https://github.com/adobe/aem-core-wcm-components/wiki/Versioning-Policies) in GitHub.

Die Komponentenversionierung schafft eine Art Vertrag, der für Upgrades wichtig ist, da sie klärt, wann etwas möglicherweise refaktoriert werden muss. Siehe auch den Abschnitt [Upgrade-Kompatibilität von Anpassungen](customizing.md#upgrade-compatibility-of-customizations), der erklärt, welche Überlegungen verschiedene Formen von Anpassungen für ein Upgrade erfordern.

Um schmerzhafte Inhaltsmigrationen zu vermeiden, sollten Sie niemals direkt auf versionierte Komponenten aus Inhalts-Ressourcen verweisen. Als Faustregel gilt, dass ein `sling:resourceType` des Inhalts nie eine Versionsnummer enthalten darf, oder dass bei der Aktualisierung von Komponenten auch der Inhalt refaktoriert werden muss. Am besten lässt sich dies vermeiden, indem Sie dem oben beschriebenen [Proxy-Komponentenmuster](#proxy-component-pattern) folgen.

### Modellschnittstellen {#model-interfaces}

Dieses Muster bezieht sich auf die Anweisung `data-sly-use` von HTL, auf eine Java-Schnittstelle zu verweisen, während die Sling-Modell-Implementierung sich selbst auch zum Ressourcentyp der Komponente registriert.

In Kombination mit dem oben beschriebenen [Proxy-Komponentenmuster](#proxy-component-pattern) bietet diese Form der doppelten Bindung die folgenden erfreulichen Erweiterungspunkte:

1. Eine Site kann die Implementierung eines Sling-Modells neu definieren, indem sie sie zum Ressourcentyp der Proxy-Komponente registriert, ohne sich über die HTL-Datei Gedanken machen zu müssen, die weiter auf die Schnittstelle verweisen kann.
1. Eine Site kann das HTL-Markup einer Komponente neu definieren, ohne darauf achten zu müssen, auf welche Implementierungslogik sie verweisen sollte.

## Alles zusammenbringen {#putting-it-all-together}

Im Folgenden finden Sie eine Übersicht über die gesamte Ressourcentyp-Bindungsstruktur, die sich auf die Titel-Kernkomponente bezieht. Es zeigt, wie eine Site-spezifische Proxy-Komponente die Versionierung der Komponenten auflösen lässt, um zu vermeiden, dass die Inhaltsressource eine Versionsnummer enthält. Anschließend wird gezeigt, wie die Datei `title.html` [HTL](https://docs.adobe.com/content/help/de-DE/experience-manager-htl/using/overview.html) der Komponente für die Modellschnittstelle verwendet wird, während die Implementierung über [Sling Model ](https://sling.apache.org/documentation/bundles/models.html)-Anmerkungen an die bestimmte Version der Komponente gebunden wird.

![Überblick über die Ressourcenbindung](/help/assets/chlimage_1-32.png)

Im Folgenden finden Sie eine weitere Übersicht, in der keine Details zur Implementierung von POJO angezeigt werden, jedoch die Referenzierung der zugehörigen [Vorlagen und Richtlinien](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/components-templates/templates.html).

Die `cq:allowedTemplates`-Eigenschaft gibt an, welche Vorlagen für eine Site verwendet werden können, und die `cq:template` informiert für jede Seite, was die zugehörige Vorlage ist. Jede Vorlage besteht aus den folgenden drei Teilen:

* **structure** – Enthält die Ressourcen, die auf jeder Seite erzwungen werden sollen und die der Seitenautor nicht löschen kann, z. B. die Kopf- und Fußzeilenkomponenten der Seite.
* **Initial** – Enthält den anfänglichen Inhalt, der beim Erstellen der Seite auf sie dupliziert wird.
* **Richtlinien** – Enthält für jede Komponente die Zuordnung zu einer Richtlinie, die die Vorkonfiguration der Komponente ist. Diese Zuordnung ermöglicht die Wiederverwendung von Richtlinien über Vorlagen hinweg, sodass sie zentral verwaltet werden können.

![Vorlagen und Richtlinien - Übersicht](/help/assets/screen_shot_2018-12-07at093102.png)

## AEM-Projektarchetyp {#aem-project-archetype}

[Der AEM-Projektarchetyp](/help/developing/archetype/overview.md) erstellt ein Adobe Experience Manager-Minimalprojekt als Ausgangspunkt für Ihre eigenen Projekte, einschließlich eines Beispiels für benutzerdefinierte HTML-Komponenten mit SlingModels, um die Logik und ordnungsgemäße Implementierung der Kernkomponenten mit dem empfohlenen Proxy-Muster zu gewährleisten.

**Lesen Sie als Nächstes:**

* [Verwenden von Kernkomponenten](/help/get-started/using.md) - Starten Sie mit Kernkomponenten in Ihrem eigenen Projekt.
* [Anpassen der Kernkomponenten](customizing.md) - Erfahren Sie, wie Sie die Kernkomponenten gestalten und anpassen können.
