---
title: Authoring mit Kernkomponenten
seo-title: Authoring mit Kernkomponenten
description: In AEM sind Komponenten die Strukturelemente, die den Inhalt der zu erstellenden Seiten ausmachen. Kernkomponenten bieten flexible und funktionsreiche Authoring-Funktionalität.
seo-description: In AEM sind Komponenten die Strukturelemente, die den Inhalt der zu erstellenden Seiten ausmachen. Kernkomponenten bieten flexible und funktionsreiche Authoring-Funktionalität.
uuid: 4a54cd4c-3d89-4683-8301-bf1e634736e3
content-type: Referenz
topic-tags: Authoring
discoiquuid: 8751e490-d427-44f2-b767-51935afda988
translation-type: ht
source-git-commit: 632d6abb1f13667cc0457152268d50af3bfabfc4

---


# Authoring mit Kernkomponenten

In Adobe Experience Manager sind Komponenten die strukturellen Elemente, aus denen der Inhalt von bearbeiteten Seiten besteht. In diesem Abschnitt werden die Kernkomponenten behandelt, die die grundlegenden Arten von Inhalten zum Erstellen von Seiten bereitstellen.

Die Kernkomponenten bieten eine flexible und funktionsreiche Authoring-Funktionalität. Die [Referenz-Site „We.Retail“](https://helpx.adobe.com/de/experience-manager/6-5/sites/developing/using/we-retail.html) illustriert, wie die Kernkomponenten verwendet werden können.

Um die Kernkomponenten zu erleben und Beispiele für ihre Konfigurationsoptionen sowie die HTML- und JSON-Ausgabe zu sehen, besuchen Sie die [Komponentenbibliothek](http://opensource.adobe.com/de/aem-core-wcm-components/library/content-fragment.html).

>[!NOTE]
>
>Kernkomponenten sind für Autoren nicht sofort verfügbar. Das [Entwicklerteam muss sie zuerst in Ihre Umgebung integrieren](using.md). Nach der Integration können sie über den [Vorlageneditor](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html) bereitgestellt und vorkonfiguriert werden.

>[!CAUTION]
>
>Kernkomponenten [erfordern AEM 6.3 oder höher](versions.md) und die Verwendung von [bearbeitbaren Vorlagen](https://helpx.adobe.com/de/experience-manager/6-5/sites/authoring/using/templates.html). Sie funktionieren weder mit der klassischen Benutzeroberfläche noch mit statischen Vorlagen.

## Authoring mit Kernkomponenten {#authoring-with-core-components}

Als Autor werden Sie einige Vorteile der Kernkomponenten bemerken, wie beispielsweise:

* Einfach zu verwenden und gut mit dem [Seiteneditor](https://helpx.adobe.com/de/experience-manager/6-5/sites/authoring/using/editing-content.html) integriert

* Vielfältige Funktionen zur Anpassung an viele Anwendungsfälle, wie in [We.Retail](https://helpx.adobe.com/de/experience-manager/6-5/sites/developing/using/we-retail.html) sowie in der [Komponentenbibliothek](http://opensource.adobe.com/de/aem-core-wcm-components/library/content-fragment.html) gezeigt

* [Vorkonfigurierbar](#pre-configuring-core-components), um zu definieren, welche Funktionen für Seitenautoren über den [Vorlageneditor](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html) verfügbar sind

* Basierend auf [Zugänglichkeitsrichtlinien](https://helpx.adobe.com/de/experience-manager/6-5/managing/using/web-accessibility.html)

* Entwickelt, um [responsives Layout](https://helpx.adobe.com/de/experience-manager/6-5/sites/authoring/using/responsive-layout.html) zu unterstützen

Komponenten sind auf der Registerkarte **Komponenten** im seitlichen Bedienfeld des Seiteneditors beim [Bearbeiten einer Seite](https://helpx.adobe.com/de/experience-manager/6-5/sites/authoring/using/editing-content.html) verfügbar.

Komponenten werden nach Kategorien gruppiert, die Komponentengruppen genannt werden, um die Komponenten mühelos zu organisieren und zu filtern. Der Name der Komponentengruppe wird mit der Komponente im [Komponenten-Browser](https://helpx.adobe.com/de/experience-manager/6-5/sites/authoring/using/editing-content.html) angezeigt, und es ist auch möglich, nach Gruppen zu filtern, um mühelos die richtige Komponente zu finden.

>[!NOTE]
>
>Die Kernkomponenten sind standardmäßig Teil einer ausgeblendeten Gruppe und sind im Komponenten-Browser nicht sichtbar.
>
>Fügen Sie die erforderlichen Komponenten einer sichtbaren Gruppe hinzu oder passen Sie sie an, damit sie für Autoren verfügbar sind.

## Vorkonfigurieren der Kernkomponenten {#pre-configuring-core-components}

Die Konfiguration von Foundation-Komponenten war Auftrag eines Entwicklers. Mit Kernkomponenten kann ein Vorlagenautor jedoch jetzt eine Reihe von Funktionen über den Vorlageneditor konfigurieren.

Wenn beispielsweise eine Bild-Komponente keine Bilduploads vom Dateisystem zulassen soll oder wenn eine Textkomponente nur bestimmte Absatzformatierungen zulassen soll, können diese Funktionen mit einem einfachen Klick aktiviert oder deaktiviert werden.

Weitere Informationen finden Sie unter [Erstellen von Seitenvorlagen](https://helpx.adobe.com/de/experience-manager/6-5/sites/authoring/using/templates.html).

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

Weitere Informationen finden Sie in der Dokumentation zum [Stilsystem](https://helpx.adobe.com/de/experience-manager/6-5/sites/authoring/using/style-system.html).

>[!NOTE]
>
>In AEM 6.3 ist Service Pack 2 (6.3.2.0) oder neuer erforderlich, um die Stilsystemfunktion zu aktivieren.

## Liste der verfügbaren Kernkomponenten {#list-of-core-components-available}

Im Folgenden finden Sie eine Liste der verfügbaren Kernkomponenten und Links zu Seiten, auf denen ihre Dialogfelder zum Bearbeiten und Design im Detail beschrieben werden.

Die aktuelle Version der Kernkomponenten enthält die folgenden Komponenten.

* [Breadcrumb](breadcrumb.md)
* [Formularschaltfläche](form-button.md)
* [Karussell](carousel.md)
* [Formular-Container](form-container.md)
* [Inhaltsfragment](content-fragment-component.md)
* [Inhaltsfragmentliste](content-fragment-list.md)
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
* [Teaser](teaser.md)
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
