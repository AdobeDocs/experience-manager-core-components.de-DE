---
title: Authoring mit Kernkomponenten
seo-title: Authoring mit Kernkomponenten
description: In AEM sind Komponenten die Strukturelemente, die den Inhalt der zu erstellenden Seiten ausmachen. Kernkomponenten bieten flexible und funktionsreiche Authoring-Funktionalität.
seo-description: In AEM sind Komponenten die Strukturelemente, die den Inhalt der zu erstellenden Seiten ausmachen. Kernkomponenten bieten flexible und funktionsreiche Authoring-Funktionalität.
uuid: 4a54cd4c-3d89-4683-8301-bf1e634736e3
content-type: Referenz
topic-tags: Authoring
discoiquuid: 8751e490-d427-44f2-b767-51935afda988
translation-type: tm+mt
source-git-commit: b6fbef1cff2908533df6573cd3a92266857ba93f

---


# Authoring mit Kernkomponenten

In Adobe Experience Manager sind Komponenten die strukturellen Elemente, aus denen der Inhalt von bearbeiteten Seiten besteht.

Die Kernkomponenten bieten eine flexible und funktionsreiche Authoring-Funktionalität. The [We.Retail reference site](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html) illustrates how the core components can be used.

To experience the Core Components and see examples of their configuration options as well as HTML and JSON output, visit the [Component Library](http://opensource.adobe.com/aem-core-wcm-components/library/content-fragment.html).

Für eine tiefer gehende, entwicklungsorientierte Einführung in die Implementierung der Kernkomponenten in einem AEM-Projekt lesen Sie [das WKND-Lernprogramm.](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/getting-started.html)

>[!NOTE]
>
>Kernkomponenten sind für Autoren nicht sofort verfügbar. Das [Entwicklerteam muss sie zuerst in Ihre Umgebung integrieren](using.md). Once integrated, they may be made available and pre-configured via the [template editor](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html).

>[!CAUTION]
>
>Hauptkomponenten [erfordern AEM 6.3 oder höher](versions.md) und müssen [bearbeitbare Vorlagen](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html)verwenden. Sie funktionieren weder mit der klassischen Benutzeroberfläche noch mit statischen Vorlagen.

## Authoring mit Kernkomponenten {#authoring-with-core-components}

Als Autor werden Sie einige Vorteile der Kernkomponenten bemerken, wie beispielsweise:

* Simple to use and well-integrated with the [page editor](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/editing-content.html)

* Funktionsreiche Funktionen zur Unterstützung vieler Anwendungsfälle, wie [in We.Retail](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html) sowie in der [Komponentenbibliothek dargestellt](http://opensource.adobe.com/aem-core-wcm-components/library/content-fragment.html)

* [Vorkonfigurierbar](#pre-configuring-core-components) zur Definition der Funktionen, die Seitenautoren über den [Vorlageneditor zur Verfügung stehen](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html)

* Built around [accessibility guidelines](https://helpx.adobe.com/experience-manager/6-5/managing/using/web-accessibility.html)

* Built to support [responsive layout](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/responsive-layout.html)

* Die [einfache Lokalisierung wird unterstützt](localization.md)

Components are available on the **Components** tab of the side panel of the page editor when [editing a page](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/editing-content.html).

Komponenten werden nach Kategorien gruppiert, die Komponentengruppen genannt werden, um die Komponenten mühelos zu organisieren und zu filtern. The component group name is displayed with the component in the [component browser](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/editing-content.html) and it is also possible to filter by group to easily find the right component.

>[!NOTE]
>
>Die Kernkomponenten sind standardmäßig Teil einer ausgeblendeten Gruppe und sind im Komponenten-Browser nicht sichtbar.
>
>Fügen Sie die erforderlichen Komponenten einer sichtbaren Gruppe hinzu oder passen Sie sie an, damit sie für Autoren verfügbar sind.

## Vorkonfigurieren der Kernkomponenten {#pre-configuring-core-components}

Die Konfiguration von Foundation-Komponenten war Auftrag eines Entwicklers. Mit Kernkomponenten kann ein Vorlagenautor jedoch jetzt eine Reihe von Funktionen über den Vorlageneditor konfigurieren.

Wenn beispielsweise eine Bild-Komponente keine Bilduploads vom Dateisystem zulassen soll oder wenn eine Textkomponente nur bestimmte Absatzformatierungen zulassen soll, können diese Funktionen mit einem einfachen Klick aktiviert oder deaktiviert werden.

See [Creating Page Templates](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html) for more information.

### Dialogfelder „Bearbeiten“ und „Design“ {#edit-and-design-dialogs}

Da die Kernkomponenten von Vorlagenautoren vorkonfiguriert werden können, um zu definieren, welche Optionen als Teil einer Vorlage zulässig sind, und dann weiter vom Seitenautor konfiguriert werden können, um tatsächliche Seiteninhalte zu definieren, kann jede Komponente über Optionen in zwei verschiedenen Dialogfeldern verfügen.

|  | Beschreibung | Funktion | Beispiele |
|--- |--- |--- |--- |
| **Dialogfeld „Bearbeiten“** | Optionen, die ein **Seitenautor** während der normalen Seitenbearbeitung für die platzierten Komponenten ändern kann | Der von der Komponente angezeigte Inhalt und die Art und Weise, wie er letztendlich auf der Seite angezeigt wird. | Formatieren von Inhaltstext und Drehen eines Bildes auf einer Seite |
| **Dialogfeld „Design“** | Optionen, die ein **Vorlagenautor** ändern kann, wenn er eine Seitenvorlage konfiguriert. | Welche Optionen für den Seitenautor beim Bearbeiten der Komponente verfügbar sind | Welche Textformatierungsoptionen verfügbar sind, welche ersetzenden Optionen für Bilder verfügbar sind |

### Komponentenstil {#component-styling}

Die Stile der meisten Kernkomponenten können mithilfe des AEM-Stilsystems definiert werden.

* Ein Vorlagenautor kann festlegen, welche Stile für eine bestimmte Komponente im Dialogfeld „Design“ dieser Komponente verfügbar sind.
* Der Inhaltsautor kann dann festlegen, welche Stile angewendet werden sollen, wenn er die Komponente hinzufügt und Inhalte erstellt.

Weitere Informationen finden Sie in der Dokumentation zum [Stilsystem](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/style-system.html) .

>[!NOTE]
>
>In AEM 6.3 ist Service Pack 2 (6.3.2.0) oder neuer erforderlich, um die Stilsystemfunktion zu aktivieren.

## Liste der verfügbaren Kernkomponenten {#list-of-core-components-available}

Im Folgenden finden Sie eine Liste der verfügbaren Kernkomponenten und Links zu Seiten, auf denen ihre Dialogfelder zum Bearbeiten und Design im Detail beschrieben werden.

Die aktuelle Version der Kernkomponenten enthält die folgenden Komponenten.

* [Akkordeon](accordion.md)
* [Breadcrumb](breadcrumb.md)
* [Schaltfläche](button.md)
* [Container](container.md)
* [Karussell](carousel.md)
* [Inhaltsfragment](content-fragment-component.md)
* [Inhaltsfragmentliste](content-fragment-list.md)
* [Download](download.md)
* [Experience Fragment](experience-fragment.md)
* [Formularschaltfläche](form-button.md)
* [Formular-Container](form-container.md)
* [Ausgeblendetes Formular](form-hidden.md)
* [Formularoptionen](form-options.md)
* [Formulartext](form-text.md)
* [Bild](image.md)
* [Sprachnavigation](language-navigation.md)
* [Liste](list.md)
* [Navigation](navigation.md)
* [Seite](page.md)
* [Schnellsuche](quick-search.md)
* [Trennzeichen](separator.md)
* [Freigabe in Social Media](sharing.md)
* [Registerkarten](tabs.md)
* [Text](text.md)
* [Titel](title.md)

>[!CAUTION]
>
>Einige Versionen einzelner Kernkomponenten sind möglicherweise nur mit bestimmten Versionen von AEM kompatibel.
>
>Weitere Informationen zu Kompatibilitätsinformationen finden Sie auf der Hilfeseite für die jeweilige Komponente (Links in der vorherigen Liste) oder im Dokument [Kernkomponentenversionen](versions.md).

>[!NOTE]
>
>Abhängig von Ihrer Instanz besitzen Sie möglicherweise benutzerdefinierte Komponenten, die speziell für Ihre Anforderungen entwickelt wurden. Möglicherweise haben diese sogar denselben Namen wie die hier behandelten Komponenten.
>Die Formular-Kernkomponenten hängen nicht mit AEM Forms zusammen.

## Entwicklungsressourcen {#developer-resources}

Technische Informationen zu Kernkomponenten finden Sie in der Entwicklerdokumentation [Entwickeln von Kernkomponenten](developing.md).
