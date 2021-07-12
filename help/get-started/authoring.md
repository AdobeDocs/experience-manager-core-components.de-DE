---
title: Authoring mit Kernkomponenten
description: In AEM sind Komponenten die Strukturelemente, die den Inhalt der zu erstellenden Seiten ausmachen. Kernkomponenten bieten flexible und funktionsreiche Authoring-Funktionalität.
role: Architect, Developer, Admin, User
exl-id: 56e58303-a178-45ab-b59d-e374c9cf90cf
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '764'
ht-degree: 100%

---

# Authoring mit Kernkomponenten

In Adobe Experience Manager sind Komponenten die strukturellen Elemente, aus denen der Inhalt von bearbeiteten Seiten besteht.

Die Kernkomponenten bieten eine flexible und funktionsreiche Authoring-Funktionalität. Die [Referenz-Site „WKND“](https://wknd.site) zeigt, wie die Kernkomponenten zur Implementierung eines umfassenden Website-Erlebnisses verwendet werden können.

Um die Kernkomponenten auszuprobieren und Beispiele für ihre Konfigurationsoptionen sowie die HTML- und JSON-Ausgabe zu sehen, besuchen Sie die [Komponentenbibliothek](https://adobe.com/go/aem_cmp_library_de).

Um eine tiefergehende und entwicklerorientierte Einführung in die Implementierung der Kernkomponenten in einem AEM-Projekt zu erhalten, sehen Sie sich den [AEM-Projektarchetyp](/help/developing/archetype/overview.md) im [WKND-Tutorial](https://docs.adobe.com/content/help/de-DE/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html) an.

>[!NOTE]
>
>Kernkomponenten sind für Autoren nicht sofort verfügbar. Das [Entwicklerteam muss sie zuerst in Ihre Umgebung integrieren](/help/get-started/using.md). Nach der Integration können sie über den [Vorlageneditor](https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/sites/authoring/features/templates.translate.html) bereitgestellt und vorkonfiguriert werden.

>[!CAUTION]
>
>Kernkomponenten [erfordern AEM 6.4 oder höher](/help/versions.md) und setzen [bearbeitbare Vorlagen](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html) voraus. Sie funktionieren weder mit der klassischen Benutzeroberfläche noch mit statischen Vorlagen.

## Authoring mit Kernkomponenten {#authoring-with-core-components}

Als Autor werden Sie einige Vorteile der Kernkomponenten bemerken, wie beispielsweise:

* Einfach zu verwenden und gut in den [Seiteneditor](https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.translate.html) integriert

* Breit gefächerte Funktionen zur Unterstützung vieler Anwendungsfälle, wie auf der [Referenz-Site „WKND“](https://wknd.site) sowie der [Komponentenbibliothek](https://adobe.com/go/aem_cmp_library) dargestellt

* [Vorkonfigurierbar](#pre-configuring-core-components), um zu definieren, welche Funktionen für Seitenautoren über den [Vorlageneditor](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html) verfügbar sind

* Erstellt entsprechend den [Richtlinien für Eingabehilfen](https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.translate.html)

* Entwickelt zur Unterstützung von [responsivem Layout](https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/sites/authoring/features/responsive-layout.translate.html)

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

### Dialogfelder „Bearbeiten“ und „Design“  {#edit-and-design-dialogs}

Da die Kernkomponenten von Vorlagenautoren vorkonfiguriert werden können, um zu definieren, welche Optionen als Teil einer Vorlage zulässig sind, und dann weiter vom Seitenautor konfiguriert werden können, um tatsächliche Seiteninhalte zu definieren, kann jede Komponente über Optionen in zwei verschiedenen Dialogfeldern verfügen.

|  | Beschreibung | Funktion | Beispiele |
|--- |--- |--- |--- |
| **Dialogfeld „Bearbeiten“** | Optionen, die ein **Seitenautor** während der normalen Seitenbearbeitung für die platzierten Komponenten ändern kann | Der von der Komponente angezeigte Inhalt und die Art und Weise, wie er letztendlich auf der Seite angezeigt wird. | Formatieren von Inhaltstext und Drehen eines Bildes auf einer Seite |
| **Dialogfeld „Design“** | Optionen, die ein **Vorlagenautor** ändern kann, wenn er eine Seitenvorlage konfiguriert. | Welche Optionen für den Seitenautor beim Bearbeiten der Komponente verfügbar sind | Welche Textformatierungsoptionen verfügbar sind, welche ersetzenden Optionen für Bilder verfügbar sind |

### Komponentenstil {#component-styling}

Die Stile der meisten Kernkomponenten können mithilfe des AEM-Stilsystems definiert werden.

* Ein Vorlagenautor kann festlegen, welche Stile für eine bestimmte Komponente im Dialogfeld „Design“ dieser Komponente verfügbar sind.
* Der Inhaltsautor kann dann festlegen, welche Stile angewendet werden sollen, wenn er die Komponente hinzufügt und Inhalte erstellt.

Weitere Informationen finden Sie in der Dokumentation zum [Stilsystem](https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/sites/authoring/features/style-system.translate.html).

## Entwicklungsressourcen {#developer-resources}

Technische Informationen zu Kernkomponenten finden Sie in der Entwicklerdokumentation [Entwickeln von Kernkomponenten](/help/developing/overview.md).
