---
title: Authoring mit Kernkomponenten
description: In AEM sind Komponenten die Strukturelemente, die den Inhalt der zu erstellenden Seiten ausmachen. Kernkomponenten bieten flexible und funktionsreiche Authoring-Funktionalität.
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# Authoring mit Kernkomponenten

In Adobe Experience Manager sind Komponenten die strukturellen Elemente, aus denen der Inhalt von bearbeiteten Seiten besteht.

Die Kernkomponenten bieten eine flexible und funktionsreiche Authoring-Funktionalität. Die [WKND-Referenz-Website](https://wknd.site) und deren stellt dar, wie die Kernkomponenten zur Implementierung eines umfassenden Website-Erlebnisses verwendet werden können.

Um die Kernkomponenten auszuprobieren und Beispiele für ihre Konfigurationsoptionen sowie die HTML- und JSON-Ausgabe zu sehen, besuchen Sie die [Komponentenbibliothek](https://adobe.com/go/aem_cmp_library).

For a more in-depth, developer-oriented introduction to implementing the Core Components on an AEM project by using the [AEM Project Archetype](/help/developing/archetype/overview.md) check out [the WKND tutorial.](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)

>[!NOTE]
>
>Kernkomponenten sind für Autoren nicht sofort verfügbar. Das [Entwicklerteam muss sie zuerst in Ihre Umgebung integrieren](/help/get-started/using.md). Nach der Integration können sie über den [Vorlageneditor](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html) bereitgestellt und vorkonfiguriert werden.

>[!CAUTION]
>
>Kernkomponenten [erfordern AEM 6.3 oder höher](/help/versions.md) und setzen [bearbeitbare Vorlagen](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html) voraus. Sie funktionieren weder mit der klassischen Benutzeroberfläche noch mit statischen Vorlagen.

## Authoring mit Kernkomponenten {#authoring-with-core-components}

Als Autor werden Sie einige Vorteile der Kernkomponenten bemerken, wie beispielsweise:

* Einfach zu verwenden und gut in den [Seiteneditor](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html) integriert

* Feature-rich capabilities to accommodate many use cases as illustrated by the [WKND reference site](https://wknd.site) as well as in the [Component Library](https://adobe.com/go/aem_cmp_library)

* [Vorkonfigurierbar](#pre-configuring-core-components), um zu definieren, welche Funktionen für Seitenautoren über den [Vorlageneditor](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html) verfügbar sind

* Erstellt entsprechend den [Richtlinien für Eingabehilfen](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html)

* Entwickelt zur Unterstützung von [responsivem Layout](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/responsive-layout.html)

* Entwickelt als Hilfe für die [einfache Lokalisierung](localization.md)

Komponenten sind beim [Bearbeiten einer Seite](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html) auf der Registerkarte **Komponenten** im seitlichen Bedienfeld des Seiteneditors verfügbar.

Komponenten werden nach Kategorien gruppiert, die Komponentengruppen genannt werden, um die Komponenten mühelos zu organisieren und zu filtern. Der Name der Komponentengruppe wird mit der Komponente im [Komponenten-Browser](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html) angezeigt; außerdem ist es möglich, nach Gruppen zu filtern, um mühelos die richtige Komponente zu finden.

>[!NOTE]
>
>Die Kernkomponenten sind standardmäßig Teil einer ausgeblendeten Gruppe und sind im Komponenten-Browser nicht sichtbar.
>
>Fügen Sie die erforderlichen Komponenten einer sichtbaren Gruppe hinzu oder passen Sie sie an, damit sie für Autoren verfügbar sind.

## Vorkonfigurieren der Kernkomponenten {#pre-configuring-core-components}

Die Konfiguration von Foundation-Komponenten war Auftrag eines Entwicklers. Mit Kernkomponenten kann ein Vorlagenautor jedoch jetzt eine Reihe von Funktionen über den Vorlageneditor konfigurieren.

Wenn beispielsweise eine Bild-Komponente keine Bilduploads vom Dateisystem zulassen soll oder wenn eine Textkomponente nur bestimmte Absatzformatierungen zulassen soll, können diese Funktionen mit einem einfachen Klick aktiviert oder deaktiviert werden.

Weitere Informationen finden Sie unter [Entwickeln von Seitenvorlagen](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html).

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

Weitere Informationen finden Sie in der Dokumentation zum [Stilsystem](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/style-system.html).

>[!NOTE]
>
>In AEM 6.3 ist Service Pack 2 (6.3.2.0) oder neuer erforderlich, um die Stilsystemfunktion zu aktivieren.

## Liste der verfügbaren Kernkomponenten {#list-of-core-components-available}

Im Folgenden finden Sie eine Liste der verfügbaren Kernkomponenten und Links zu Seiten, auf denen ihre Dialogfelder zum Bearbeiten und Design im Detail beschrieben werden.

Die aktuelle Version der Kernkomponenten enthält die folgenden Komponenten.

* [Akkordeon](/help/components/accordion.md)
* [Breadcrumb](/help/components/breadcrumb.md)
* [Schaltfläche](/help/components/button.md)
* [Container](/help/components/container.md)
* [Karussell](/help/components/carousel.md)
* [Inhaltsfragment](/help/components/content-fragment-component.md)
* [Inhaltsfragmentliste](/help/components/content-fragment-list.md)
* [Download](/help/components/download.md)
* [Einbetten](/help/components/embed.md)
* [Experience Fragment](/help/components/experience-fragment.md)
* [Formularschaltfläche](/help/components/forms/form-button.md)
* [Formular-Container](/help/components/forms/form-container.md)
* [Ausgeblendetes Formular](/help/components/forms/form-hidden.md)
* [Formularoptionen](/help/components/forms/form-options.md)
* [Formulartext](/help/components/forms/form-text.md)
* [Bild](/help/components/image.md)
* [Sprachnavigation](/help/components/language-navigation.md)
* [Liste](/help/components/list.md)
* [Navigation](/help/components/navigation.md)
* [Seite](/help/components/page.md)
* [Schnellsuche](/help/components/quick-search.md)
* [Trennzeichen](/help/components/separator.md)
* [Freigabe in Social Media](/help/components/sharing.md)
* [Registerkarten](/help/components/tabs.md)
* [Text](/help/components/text.md)
* [Titel](/help/components/title.md)

>[!CAUTION]
>
>Einige Versionen einzelner Kernkomponenten sind möglicherweise nur mit bestimmten Versionen von AEM kompatibel.
>
>Weitere Informationen zu Kompatibilitätsinformationen finden Sie auf der Hilfeseite für die jeweilige Komponente (Links in der vorherigen Liste) oder im Dokument [Kernkomponentenversionen](/help/versions.md).

>[!NOTE]
>
>Abhängig von Ihrer Instanz besitzen Sie möglicherweise benutzerdefinierte Komponenten, die speziell für Ihre Anforderungen entwickelt wurden. Möglicherweise haben diese sogar denselben Namen wie die hier behandelten Komponenten.
>Die Formular-Kernkomponenten hängen nicht mit AEM Forms zusammen.

## Entwicklungsressourcen {#developer-resources}

Technische Informationen zu Kernkomponenten finden Sie in der Entwicklerdokumentation [Entwickeln von Kernkomponenten](/help/developing/overview.md).
