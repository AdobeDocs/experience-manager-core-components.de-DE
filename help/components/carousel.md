---
title: Karussellkomponente
description: Mit der Karussellkomponente kann der Inhaltsautor Inhalte in einem drehbaren Karussell präsentieren.
role: Architect, Developer, Admin, User
exl-id: 3331214c-a05c-47e1-b54c-fbfd1045bd60
source-git-commit: d39fe0084522f67664203a026340b23d325c1883
workflow-type: ht
source-wordcount: '1313'
ht-degree: 100%

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
| v1 | Kompatibel mit<br>[Version 2.17.4](/help/versions.md) und vorherigen | Kompatibel | Kompatibel |

Weitere Informationen zu Kernkomponentenversionen und -freigaben finden Sie im Dokument [Kernkomponentenversionen](/help/versions.md).

## Musterkomponentenausgabe {#sample-component-output}

Um die Karussellkomponente zu erleben und Beispiele für ihre Konfigurationsoptionen sowie die HTML- und JSON-Ausgabe zu sehen, besuchen Sie die [Komponentenbibliothek](https://adobe.com/go/aem_cmp_library_carousel_de).

### Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur Karussellkomponente [finden Sie auf GitHub](https://adobe.com/go/aem_cmp_tech_carousel_v1_de).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Tiefe Verknüpfung mit einem Bedienfeld {#deep-linking}

Die Karussell-, [Registerkarten](tabs.md)- und [Akkordeon-Komponenten](accordion.md) unterstützen direkte Links zu einem Bedienfeld innerhalb der Komponente.

Gehen Sie hierfür wie folgt vor:

1. Zeigen Sie die Seite mit der Komponente über die Option **[Als veröffentlicht anzeigen](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html?lang=de#view-as-published)** im Seiteneditor an.
1. Überprüfen Sie den Inhalt der Seite und halten Sie die ID des Bedienfeldes fest.
   * Beispiel `id="carousel-bfe4fa6647-item-47f1a7ca67-tabpanel"`
1. Die ID wird der Anker, den Sie über einen Hash (`#`) an die URL anhängen können.
   * Beispiel `https://wknd.site/content/wknd/language-masters/en/magazine/western-australia.html#carousel-bfe4fa6647-item-47f1a7ca67-tabpanel`

Wird zu der URL mit der Bereichs-ID navigiert, scrollt der Browser direkt zur jeweiligen Komponente und zeigt das angegebene Bedienfeld an. Wenn das Bedienfeld so konfiguriert ist, dass es nicht standardmäßig angezeigt wird, wird automatisch dorthin gescrollt.

## Karussell und responsives Design {#responsive-design}

Alle Kernkomponenten sind so konzipiert, dass sie vollständig responsiv sind und auf allen Geräten ein nahtloses Erlebnis bieten.

Einige erweiterte Komponenten wie die Karussellkomponente erfordern möglicherweise besondere Überlegungen im Kontext des Implementierungsprojekts, um unter allen Bedingungen die Reaktionsfähigkeit zu bewahren. Weitere Informationen finden Sie im Dokument [Responsives Design der Kernkomponenten](/help/responsive.md).

## Dialogfeld „Bearbeiten“ {#edit-dialog}

Im Dialogfeld „Bearbeiten“ kann der Inhaltsautor Folien hinzufügen, umbenennen und neu anordnen sowie die Einstellungen für den automatischen Übergang definieren.

### Registerkarte „Elemente“ {#items-tab}

![Registerkarte „Elemente“ im Dialogfeld „Bearbeiten“ der Karussellkomponente](/help/assets/carousel-edit-items.png)

Verwenden Sie die Schaltfläche **Hinzufügen**, um die Komponentenauswahl zu öffnen und dort auszuwählen, welche Komponente als Registerkarte hinzugefügt werden soll. Nach dem Hinzufügen wird der Liste ein Eintrag hinzugefügt, der die folgenden Spalten enthält:

* **Symbol** - Das Symbol des Komponententyps der Registerkarte zur einfachen Identifizierung in der Liste. Bewegen Sie den Mauszeiger darüber, um den vollständigen Komponentennamen als QuickInfo zu sehen.
* **Beschreibung** - Die Beschreibung, die als Text der Registerkarte verwendet wird und standardmäßig den Namen der für die Registerkarte ausgewählten Komponente enthält.
* **Entfernen** - Tippen oder klicken Sie, um die Registerkarte aus der Registerkartenkomponente zu löschen.
* **Neu sortieren** - Tippen oder klicken und ziehen Sie, um die Registerkarten anzuordnen.

>[!TIP]
>
>Wenn der Viewport der Seite so reduziert wird, dass das Bearbeitungsdialogfeld im Vollbildmodus angezeigt wird, ist die Schaltfläche **Hinzufügen** ausgeblendet. Sie können der Karussellkomponente weiterhin Komponenten hinzufügen, indem Sie sie [per Drag-and-Drop aus dem Komponenten-Browser ziehen und im Seiteneditor auf der Karussellkomponente ablegen](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html?lang=de#inserting-a-component-from-the-components-browser).

### Registerkarte „Eigenschaften“ {#properties-tab}

![Registerkarte „Eigenschaften“ im Dialogfeld „Bearbeiten“ der Karussellkomponente](/help/assets/carousel-edit-properties.png)

Auf der Registerkarte **Eigenschaften** können Inhaltsautorinnen und -autoren die Folien auf automatische Übergänge einstellen.

* **Aktives Element**: Inhaltsautorinnen und -autoren können definieren, welche Registerkarte beim Laden der Seite aktiv ist.
* **Automatisch zwischen Folien wechseln** - Wenn diese Option aktiviert ist, wechselt die Komponente nach einer festgelegten Verzögerungszeit automatisch zur nächsten Folie.
* **Übertragungsverzögerung** - Wenn die Option „Automatisch zwischen Folien wechseln“ ausgewählt wird, wird dieser Wert verwendet, um die Verzögerung zwischen Übergängen (in Millisekunden) zu definieren.
* **Automatisches Pausieren beim Bewegen des Mauszeigers deaktivieren** - Wenn die Option **Automatisch zwischen Folien wechseln** ausgewählt ist, wird der Karussell-Übergang automatisch angehalten, sobald die Maus über das Karussell bewegt wird; Wählen Sie diese Option, damit der Übergang nicht angehalten wird.
* **ID** – Diese Option dient zur Kontrolle der eindeutigen Kennung der Komponente in der HTML-Datei und auf der [Datenschicht](/help/developing/data-layer/overview.md).
   * Wenn Sie das Feld leer lassen, wird automatisch eine eindeutige ID generiert, die Sie über die resultierende Seite finden.
   * Sofern eine ID angegeben wird, ist vom Autor bzw. der Autorin sicherzustellen, dass diese eindeutig ist.
   * Änderungen der ID können sich auf das CSS-, JS- und Datenschicht-Tracking auswirken.

>[!NOTE]
>
>Die Steuerelemente für die Abfolge der Folien werden im Modus **Bearbeiten** nicht aktiviert. Verwenden Sie den [**Vorschaumodus**](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html?lang=de#preview-mode) oder die Option **[Als veröffentlicht anzeigen](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html?lang=de#view-as-published)**, um so mit dem Karussell zu interagieren, wie es ein Leser des veröffentlichten Inhalts tun würde.
>
>Die Funktion des automatischen Übergangs ist im Modus **Bearbeiten** nicht aktiviert. Verwenden Sie die Option **[Als veröffentlicht anzeigen](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html?lang=de#view-as-published)**, um die Funktion des automatischen Übergangs so anzuzeigen, wie es ein Leser der veröffentlichten Inhalte tun würde.

### Registerkarte „Erreichbarkeit“ {#accessibility-tab}

![Registerkarte „Erreichbarkeit“ im Dialogfeld „Bearbeiten“ der Karussellkomponente](/help/assets/carousel-edit-accessibility.png)

Auf der Registerkarte **Erreichbarkeit** können Werte für die [ARIA-Barrierefreiheits-Beschriftungen](https://www.w3.org/WAI/standards-guidelines/aria/) für die Komponente festgelegt werden.

* **Beschriftung**: Wert eines aria-label-Attributs für das Karussell, das den Karussellinhalt beschreibt.
* **Zurück**: Wert eines aria-label-Attributs für die Beschriftung der Zurück-Schaltfläche bei der Karussellnavigation.
* **Weiter**: Wert eines aria-label-Attributs für die Beschriftung der Weiter-Schaltfläche bei der Karussellnavigation.
* **Wiedergabe**: Wert eines aria-label-Attributs für die Beschriftung der Wiedergabe-Schaltfläche bei der Karussellnavigation.
* **Pause**: Wert eines aria-label-Attributs für die Beschriftung der Pause-Schaltfläche bei der Karussellnavigation.
* **Registerkartenliste**: Wert eines aria-label-Attributs für die Beschriftung der Elementliste bei der Karussellnavigation.
* **Beschriftung des Karussellelements auf seinen Titel festlegen**: Wenn diese Option aktiviert ist, wird der Titel der Karussellelemente automatisch auf die aria-label-Beschreibung festgelegt.

## Bedienfeld auswählen {#select-panel}

Der Inhaltsautor kann die Option **Bedienfeld auswählen** in der Komponentensymbolleiste verwenden, um zu einer anderen Folie zu wechseln und die Reihenfolge der Folien einfach neu zu ordnen.

![Symbol „Bedienfeld auswählen“](/help/assets/select-panel-icon.png)

Nach Auswahl der Option **Bedienfeld auswählen** in der Komponentensymbolleiste werden die konfigurierten Folien als Dropdown-Liste angezeigt.

* Die Liste wird durch die zugewiesene Anordnung der Folien angeordnet und entsprechend nummeriert.
* Der Komponententyp der Folie wird zuerst angezeigt, gefolgt von der Beschreibung der Folie in heller Schrift.

![Bedienfeld auswählen](/help/assets/select-panel-popover.png)

* Durch Tippen oder Klicken auf einen Eintrag in der Dropdown-Liste wird die Ansicht im Editor auf diese Folie umgestellt.
* Die Folie kann mithilfe der Ziehpunkte neu angeordnet werden.

## Dialogfeld „Design“ {#design-dialog}

Im Dialogfeld „Design“ kann der Vorlagenautor definieren, welche Komponenten der Karussellkomponente als Folien hinzugefügt werden können, sowie Standardübergänge und benutzerdefinierte Stile definieren, die dem Inhaltsautor zur Verfügung stehen.

### Registerkarte „Eigenschaften“ {#properties-tab-1}

Über die Registerkarte **Eigenschaften** werden die Standardeinstellungen für die Folienübergänge definiert, wenn ein Inhaltsautor die Karussellkomponente einer Seite hinzufügt.

![Dialogfeld „Design“ der Karussellkomponente](/help/assets/carousel-design.png)

* **Automatisch zwischen Folien wechseln** - Definiert, ob die Option, automatisch das Karussell auf die nächste Folie zu verschieben, aktiviert ist, wenn der Inhaltsautor die Karussellkomponente einer Seite hinzufügt.
* **Steuerelemente voranstellen**: Wenn diese Option aktiviert ist, werden die Steuerelemente vor den Karussellelementen platziert, um die Barrierefreiheit zu verbessern.

### Registerkarte „Zugelassene Komponenten“ {#allowed-components-tab}

Über die Registerkarte **Zugelassene Komponenten** können Sie definieren, welche Komponenten der Karussellkomponente von Inhaltsautorinnen und Inhaltsautoren als Folien hinzugefügt werden können.

Die Registerkarte „Zugelassene Komponenten“ funktioniert auf die gleiche Weise wie die Registerkarte desselben Namens beim [Definieren der Richtlinie und Eigenschaften eines Layout-Containers im Vorlageneditor.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=de)

### Registerkarte „Arten“ {#styles-tab}

Die Karussellkomponente unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).

## Adobe Client-Datenschicht {#data-layer}

Die Karussellkomponente unterstützt die [Adobe Client-Datenschicht](/help/developing/data-layer/overview.md).
