---
title: Karussellkomponente
description: Mit der Karussellkomponente kann der Inhaltsautor Inhalte in einem drehbaren Karussell präsentieren.
translation-type: tm+mt
source-git-commit: c186e9ec3944d785ab0376769cf7f2307049a809
workflow-type: tm+mt
source-wordcount: '1112'
ht-degree: 89%

---


# Karussellkomponente{#carousel-component}

Mit der Kernkomponente „Karussellkomponente“ kann der Inhaltsautor Inhalte in einem navigierbaren Karussell präsentieren.

## Nutzung {#usage}

Mit der Karussellkomponente organisiert der Inhaltsautor Inhalte in einem drehbaren Karussell aus Folien.

Das [Dialogfeld „Bearbeiten“](#edit-dialog) ermöglicht dem Inhaltsautor das Erstellen, Benennen und Anordnen mehrerer Folien sowie die Aktivierung des automatischen Übergangs mit Verzögerung. Über das [Dialogfeld „Design“](#design-dialog) kann der Vorlagenautor definieren, welche Komponenten dem Karussell hinzugefügt werden können, automatische Übergänge aktivieren oder deaktivieren und die Stile anpassen.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Karussellkomponente ist v1, die mit Version 2.2.0 der Kernkomponenten im Oktober 2018 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v1 | Kompatibel | Kompatibel | Kompatibel |

Weitere Informationen zu Kernkomponentenversionen und -freigaben finden Sie in den [Kernkomponentenversionen](/help/versions.md).

## Musterkomponentenausgabe {#sample-component-output}

Um die Karussellkomponente zu erleben und Beispiele für ihre Konfigurationsoptionen sowie die HTML- und JSON-Ausgabe zu sehen, besuchen Sie die [Komponentenbibliothek](https://adobe.com/go/aem_cmp_library_carousel).

### Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur Karussellkomponente [finden Sie auf GitHub](https://adobe.com/go/aem_cmp_tech_carousel_v1).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Dialogfeld „Bearbeiten“ {#edit-dialog}

Im Dialogfeld „Bearbeiten“ kann der Inhaltsautor Folien hinzufügen, umbenennen und neu anordnen sowie die Einstellungen für den automatischen Übergang definieren.

### Registerkarte „Elemente“ {#items-tab}

![Registerkarte &quot;Elemente&quot;des Dialogfelds &quot;Bearbeiten&quot;der Karussell-Komponente](/help/assets/carousel-edit-items.png)

Verwenden Sie die Schaltfläche **Hinzufügen**, um die Komponentenauswahl zu öffnen und dort auszuwählen, welche Komponente als Registerkarte hinzugefügt werden soll. Nach dem Hinzufügen wird der Liste ein Eintrag hinzugefügt, der die folgenden Spalten enthält:

* **Symbol** - Das Symbol des Komponententyps der Registerkarte zur einfachen Identifizierung in der Liste. Bewegen Sie den Mauszeiger darüber, um den vollständigen Komponentennamen als QuickInfo zu sehen.
* **Beschreibung** - Die Beschreibung, die als Text der Registerkarte verwendet wird und standardmäßig den Namen der für die Registerkarte ausgewählten Komponente enthält.
* **Entfernen** - Tippen oder klicken Sie, um die Registerkarte aus der Registerkartenkomponente zu löschen.
* **Neu sortieren** - Tippen oder klicken und ziehen Sie, um die Registerkarten anzuordnen.

>[!TIP]
>
>Wenn der Viewport der Seite so reduziert wird, dass das Bearbeitungsdialogfeld im Vollbildmodus angezeigt wird, ist die Schaltfläche **Hinzufügen** ausgeblendet. Sie können der Karussellkomponente weiterhin Komponenten hinzufügen, indem Sie sie [per Drag-and-Drop aus dem Komponenten-Browser ziehen und im Seiteneditor auf der Karussellkomponente ablegen](https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.translate.html#inserting-a-component-from-the-components-browser).

### Registerkarte „Eigenschaften“ {#properties-tab}

![Registerkarte &quot;Eigenschaften&quot;des Dialogfelds &quot;Bearbeiten&quot;der Karussell-Komponente](/help/assets/carousel-edit-properties.png)

Auf der Registerkarte **Eigenschaften** kann der Inhaltsautor die Folien auf automatische Übergänge einstellen.

* **Automatische Folienübergänge** – Wenn diese Option aktiviert ist, wechselt die Komponente nach einer festgelegten Verzögerungszeit automatisch zur nächsten Folie.
* **Übergangsverzögerung** – Wenn die Option „Automatische Folienübergänge“ ausgewählt wird, wird dieser Wert verwendet, um die Verzögerung zwischen Übergängen (in Millisekunden) zu definieren.
* **Automatische Pause beim Bewegen der Maus deaktivieren** - Wenn die Option **Automatische Folienübergänge** ausgewählt ist, wird der Karussell-Übergang automatisch angehalten, sobald die Maus über das Karussell bewegt wird; Wählen Sie diese Option, damit der Übergang nicht angehalten wird.
* **ID** - Diese Option ermöglicht die Steuerung des eindeutigen Bezeichners der Komponente im HTML und in der [Datenschicht](/help/developing/data-layer/overview.md).
   * Wenn Sie das Feld leer lassen, wird automatisch eine eindeutige ID generiert und Sie können die resultierende Seite überprüfen.
   * Wenn eine ID angegeben wird, muss der Autor sicherstellen, dass sie eindeutig ist.
   * Eine Änderung der ID kann sich auf die Verfolgung von CSS, JS und Datenschichten auswirken.

>[!NOTE]
>
>Die Steuerelemente für die Abfolge der Folien werden im Modus **Bearbeiten** nicht aktiviert. Verwenden Sie den [**Vorschaumodus **](https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.translate.html#preview-mode)oder die Option **[Als veröffentlicht anzeigen](https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.translate.html#view-as-published)**, um so mit dem Karussell zu interagieren, wie es ein Leser des veröffentlichten Inhalts tun würde.
>
>Die Funktion des automatischen Übergangs ist im Modus **Bearbeiten** nicht aktiviert. Verwenden Sie die Option **[Als veröffentlicht anzeigen](https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.translate.html#view-as-published)**, um die Funktion des automatischen Übergangs so anzuzeigen, wie es ein Leser der veröffentlichten Inhalte tun würde.

### Registerkarte „Barrierefreiheit“ {#accessibility-tab}

![Registerkarte &quot;Ein-/Ausgabehilfe&quot;des Dialogfelds &quot;Bearbeiten&quot;der Karussell-Komponente](/help/assets/carousel-edit-accessibility.png)

Auf der Registerkarte **Barrierefreiheit** können Werte für die [ARIA-Barrierefreiheits-Bezeichungen](https://www.w3.org/WAI/standards-guidelines/aria/) für die Komponente festgelegt werden.

* **Bezeichnung** - Wert eines ARIA-Bezeichnungs-Attributs für die Komponente

## Bedienfeld auswählen {#select-panel}

Der Inhaltsautor kann die Option **Bedienfeld auswählen** in der Komponentensymbolleiste verwenden, um zu einer anderen Folie zu wechseln und die Reihenfolge der Folien einfach neu zu ordnen.

![Bedienfeldsymbol auswählen](/help/assets/select-panel-icon.png)

Nach Auswahl der Option **Bedienfeld auswählen** in der Komponentensymbolleiste werden die konfigurierten Folien als Dropdown-Liste angezeigt.

* Die Liste wird durch die zugewiesene Anordnung der Folien angeordnet und entsprechend nummeriert.
* Der Komponententyp der Folie wird zuerst angezeigt, gefolgt von der Beschreibung der Folie in heller Schrift.

![Bedienfeld auswählen](/help/assets/select-panel-popover.png)

* Durch Tippen oder Klicken auf einen Eintrag in der Dropdown-Liste wird die Ansicht im Editor auf diese Folie umgestellt.
* Die Folie kann mithilfe der Ziehpunkte neu angeordnet werden.

## Dialogfeld „Design“ {#design-dialog}

Im Dialogfeld „Design“ kann der Vorlagenautor definieren, welche Komponenten der Karussellkomponente als Folien hinzugefügt werden können, sowie Standardübergänge benutzerdefinierte Stile definieren, die dem Inhaltsautor zur Verfügung stehen.

### Registerkarte „Eigenschaften“ {#properties-tab-1}

Über die Registerkarte **Eigenschaften** werden die Standardeinstellungen für die Folienübergänge definiert, wenn ein Inhaltsautor die Karussellkomponente einer Seite hinzufügt.

![Design-Dialogfeld der Karussell-Komponente](/help/assets/carousel-design.png)

* **Automatische Folienübergänge** – Definiert, ob die Option, automatisch das Karussell auf die nächste Folie zu verschieben, aktiviert ist, wenn der Inhaltsautor die Karussellkomponente einer Seite hinzufügt.
* **Übergangsverzögerung** – Definiert den Standardwert der Übergangsverzögerung zwischen Folien (in Millisekunden), wenn ein Inhaltsautor die Karussellkomponente einer Seite hinzufügt.
* **Automatische Pause beim Bewegen der Maus deaktivieren** – Definiert, ob standardmäßig die Option zum Deaktivieren der automatischen Pause der Folie aktiviert ist, wenn **Automatische Folienübergänge** vom Inhaltsautor ausgewählt wird.

### Registerkarte „Zugelassene Komponenten“{#allowed-components-tab}

Über die Registerkarte **Zugelassene Komponenten** können Sie definieren, welche Komponenten der Karussellkomponente vom Inhaltsautor als Folien hinzugefügt werden können.

Die Registerkarte „Zugelassene Komponenten“ funktioniert auf die gleiche Weise wie die Registerkarte desselben Namens beim [Definieren der Richtlinie und Eigenschaften eines Layoutcontainers im Vorlageneditor.](https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/sites/authoring/features/templates.translate.html)

### Registerkarte „Stile“ {#styles-tab}

Die Karussellkomponente unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).
