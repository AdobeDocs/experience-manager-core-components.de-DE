---
title: Bearbeiten mit Kernkomponenten
seo-title: Bearbeiten mit Kernkomponenten
description: In AEM sind Komponenten die Strukturelemente, die den Inhalt der erstellten Seiten darstellen. Kernkomponenten bieten flexible und funktionsreiche Authoring-Funktionen.
seo-description: In AEM sind Komponenten die Strukturelemente, die den Inhalt der erstellten Seiten darstellen. Kernkomponenten bieten flexible und funktionsreiche Authoring-Funktionen.
uuid: 4 a 54 cd 4 c -3 d 89-4683-8301-bf 1 e 344736 e 3
content-type: Referenz
topic-tags: authoring
discoiquuid: 8751 e 490-d 427-44 f 2-b 767-51935 afda 988
translation-type: tm+mt
source-git-commit: 600aefa49d6247c290b8fb9f6acf5548126b3f61

---


# Autor mit Kernkomponenten

In Adobe Experience Manager sind Komponenten die strukturellen Elemente, aus denen der Inhalt von bearbeiteten Seiten besteht. Dieser Abschnitt enthält die Kernkomponenten, die wichtige Inhaltstypen zur Erstellung vonseiten bereitstellen.

Die Kernkomponenten bieten flexible und funktionale Authoring-Funktionen. Die Referenz-Website [für wir](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html) zeigt an, wie die Kernkomponenten verwendet werden können.

>[!NOTE]
>
>Kernkomponenten sind für Autoren nicht sofort verfügbar, das [Entwicklungsteam muss sie zunächst in Ihre Umgebung integrieren](using.md). Nach der Integration können sie über den [Vorlageneditor](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html) oder im [Designmodus bereitgestellt und vorkonfiguriert](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/default-components-designmode.html)werden.

>[!CAUTION]
>
>Core-Komponenten [benötigen AEM 6.3 oder höher](versions.md) und funktionieren nicht mit der klassischen Benutzeroberfläche.

## Bearbeiten mit Kernkomponenten {#authoring-with-core-components}

Um die Kernkomponenten zu verstehen, sehen Sie sich die [Komponentenbibliothek an](http://opensource.adobe.com/aem-core-wcm-components/library.html), in der die Kernkomponenten vorgestellt werden und Beispiele für deren Nutzung präsentiert werden.

Als Autor werden Sie verschiedene Vorteile der Kernkomponenten bemerken, darunter:

* Einfach zu verwenden und mit [dem Seiteneditor gut integriert](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/editing-content.html)
* Funktionsreiche Funktionen für zahlreiche Anwendungsfälle, [wie in &quot;We. Retail&quot; gezeigt](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html)
* [Vorkonfigurierbar](#pre-configuring-core-components) , um zu definieren, welche Funktionen für Seitenautoren verfügbar sind
   * Über den [Vorlageneditor](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html) für [bearbeitbare Vorlagen](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/page-templates-editable.html)
   * Im [Designmodus](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/default-components-designmode.html) für [statische Vorlagen](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/page-templates-static.html)

* Richtlinien [für Barrierefreiheit](https://helpx.adobe.com/experience-manager/6-5/managing/using/web-accessibility.html)

* Erstellen, um [responsive Layout zu unterstützen](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/responsive-layout.html)

Komponenten sind auf der Registerkarte **Komponenten** des Seiteneditors beim [Bearbeiten einer Seite auf der Registerkarte &quot;Komponenten&quot; verfügbar](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/editing-content.html).

Komponenten werden nach Kategorien gruppiert, die Komponentengruppen genannt werden, um die Komponenten mühelos zu organisieren und zu filtern. Der Komponentengruppenname wird mit der Komponente im [Komponentenbrowser angezeigt,](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/editing-content.html) und es ist auch möglich, nach Gruppe zu filtern, um die richtige Komponente zu finden.

>[!NOTE]
>
>Die Kernkomponenten sind standardmäßig Teil einer ausgeblendeten Gruppe und sind im Komponentenbrowser nicht sichtbar.
>
>Fügen Sie die erforderlichen Komponenten einer sichtbaren Gruppe hinzu oder passen Sie sie an, damit sie für Autoren verfügbar sind.

## Vorkonfigurieren der Kernkomponenten {#pre-configuring-core-components}

Die Konfiguration von Foundation-Komponenten war der Auftrag eines Entwicklers. Mit Core-Komponenten kann ein Vorlagenautor jetzt eine Reihe von Funktionen über den Vorlageneditor oder im Designmodus konfigurieren.

Wenn beispielsweise eine Image-Komponente keine Bilduploads vom Dateisystem zulassen darf oder wenn eine Textkomponente nur bestimmte Absatzformatierungen zulassen soll, können diese Funktionen mit einem einfachen Klick aktiviert oder deaktiviert werden.

Weitere Informationen finden Sie unter [Erstellen von Seitenvorlagen](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html) .

### Dialogfelder bearbeiten und entwerfen {#edit-and-design-dialogs}

Da die Kernkomponenten von Vorlagenautoren vorkonfiguriert werden können, um zu definieren, welche Optionen als Teil einer Vorlage zulässig sind und dann weiter vom Seitenautor konfiguriert werden, um tatsächliche Seiteninhalte zu definieren, kann jede Komponente über zwei verschiedene Dialogfelder verfügen.

|  | Beschreibung | Steuerelemente | Beispiele |
|--- |--- |--- |--- |
| **Dialogfeld bearbeiten** | Optionen, die ein **Seitenautor** während der normalen Seitenbearbeitung für die platzierten Komponenten ändern kann | Der von der Komponente angezeigte Inhalt und die Art und Weise, wie er letztendlich auf der Seite angezeigt wird. | Formatieren von Inhalten, Drehen eines Bildes auf einer Seite |
| **Design-Dialogfeld** | Optionen, die ein **Vorlagenautor ändern** kann, wenn eine Seitenvorlage konfiguriert wird. | Welche Optionen der Seitenautor beim Bearbeiten der Komponente verfügbar hat | Welche Textformatierungsoptionen verfügbar sind, sind die ersetzenden Optionen verfügbar. |

### Komponentenstil {#component-styling}

Die Stile der meisten Kernkomponenten können mithilfe des AEM-Stilsystems definiert werden.

* Ein Vorlagenautor kann festlegen, welche Stile für eine bestimmte Komponente im Design-Dialogfeld dieser Komponente verfügbar sind.
* Der Inhaltsautor kann dann festlegen, welche Stile angewendet werden sollen, wenn die Komponente hinzugefügt und Inhalte erstellt werden.

Weitere Informationen finden Sie in der [Dokumentation zum Stilsystem](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/style-system.html) .

>[!NOTE]
>
>In AEM 6.3 ist Service Pack 2 (6.3.2.0) oder neuer erforderlich, um die Stilsystemfunktion zu aktivieren.

## Liste der verfügbaren Kernkomponenten {#list-of-core-components-available}

Im Folgenden finden Sie eine Liste der verfügbaren Kernkomponenten, die mit den Seiten verknüpft sind, die ihre Dialogfelder zum Bearbeiten und Design im Detail beschreiben.

Die aktuelle Version der Kernkomponenten enthält die folgenden Komponenten.

* [Breadcrumb](breadcrumb.md)
* [Formularschaltfläche](form-button.md)
* [Karussell](carousel.md)
* [Formular-Container](form-container.md)
* [Inhaltsfragmente](content-fragment-component.md)
* [Inhaltsfragmentliste](content-fragment-list.md)
* [Ausgeblendetes Formular](form-hidden.md)
* [Formularoptionen](form-options.md)
* [Formulartext](form-text.md)
* [Bild](image.md)
* [Sprachnavigation](language-navigation.md)
* [Liste](list.md)
* [Navigation](navigation.md)
* [Page](page.md)
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
>Weitere Informationen finden Sie auf der einzelnen Hilfeseite (Links in der vorherigen Liste) für die jeweilige Komponente oder auf das Dokument [Hauptkomponenten Versionsversionen](versions.md) .

>[!NOTE]
>
>Abhängig von Ihrer Instanz besitzen Sie möglicherweise benutzerdefinierte Komponenten, die speziell für Ihre Anforderungen entwickelt wurden. Möglicherweise haben diese sogar denselben Namen wie die hier behandelten Komponenten.
>Die Core-Komponenten des Formulars sind nicht mit AEM Forms verknüpft.

## Entwicklungsressourcen {#developer-resources}

Technische [Informationen zu Kernkomponenten finden Sie in der](developing.md) Entwicklerdokumentation zu Kernkomponenten entwickeln.
