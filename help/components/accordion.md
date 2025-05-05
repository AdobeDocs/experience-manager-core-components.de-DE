---
title: Akkordeon-Komponente
description: Die Kernkomponente „Akkordeon“ ermöglicht die Erstellung einer Sammlung von Bedienfeldern, die auf der Seite in einem Akkordeon angeordnet sind.
role: Architect, Developer, Admin, User
exl-id: 1deb570a-3d8d-409e-805f-8460c49cf9bb
source-git-commit: 6fbc781db555bc6abaed1d122a9a8756e3d53222
workflow-type: ht
source-wordcount: '1102'
ht-degree: 100%

---


# Akkordeon-Komponente{#accordion-component}

Die Kernkomponente „Akkordeon“ ermöglicht die Erstellung einer Sammlung von Bedienfeldern, die auf der Seite in einem Akkordeon angeordnet sind.

## Nutzung {#usage}

Die Kernkomponente „Akkordeon“ ermöglicht die Erstellung einer Sammlung von Komponenten in Form von Bedienfeldern, die auf einer Seite in einem Akkordeon angeordnet sind, ähnlich der [Registerkarten-Komponente](tabs.md), jedoch mit der Möglichkeit, die Bedienfelder ein- und auszublenden.

* Die Eigenschaften des Akkordeons können im [Dialogfeld „Konfigurieren“](#configure-dialog) definiert werden.
* Die Reihenfolge der Bedienfelder im Akkordeon kann im Dialogfeld „Konfigurieren“ und im [Popover zur Bedienfeldauswahl](#select-panel-popover) definiert werden.
* Standardwerte für die Akkordeon-Komponente können beim Hinzufügen zu einer Seite im [Dialogfeld „Design“](#design-dialog) konfiguriert werden.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Akkordeon-Komponente ist v1, die mit Version 2.5.0 der Kernkomponenten im Juni 2019 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |---|---|---|
| v1 | Kompatibel mit<br>[Version 2.17.4](/help/versions.md) und vorherigen | Kompatibel | Kompatibel | Kompatibel |

Weitere Informationen zu Kernkomponentenversionen und -freigaben finden Sie im Dokument [Kernkomponentenversionen](/help/versions.md).

## Musterkomponentenausgabe {#sample-component-output}

Um die Akkordeon-Komponente sowie Beispiele für die Konfigurationsoptionen sowie HTML- und JSON-Ausgaben zu erhalten, besuchen Sie die [Komponentenbibliothek](https://adobe.com/go/aem_cmp_library_accordion_de).

## Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur Akkordeon-Komponente [finden Sie auf GitHub](https://adobe.com/go/aem_cmp_tech_accordion_v1_de).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Tiefe Verknüpfung mit einem Bedienfeld {#deep-linking}

Die Akkordeon-, [Karussell](carousel.md)- und [Registerkarten-Komponenten](tabs.md) unterstützen direkte Links zu einem Bedienfeld innerhalb der Komponente.

Gehen Sie hierfür wie folgt vor:

1. Zeigen Sie die Seite mit der Komponente über die Option **[Als veröffentlicht anzeigen](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html?lang=de#view-as-published)** im Seiteneditor an.
1. Überprüfen Sie den Inhalt der Seite und halten Sie die ID des Bedienfeldes fest.
   * Beispiel `id="accordion-86196c94d3-item-ca319dbb0b"`
1. Die ID wird der Anker, den Sie über einen Hash (`#`) an die URL anhängen können.
   * Beispiel `https://wknd.site/content/wknd/language-masters/en/magazine/western-australia.html#accordion-86196c94d3-item-ca319dbb0b`

Wird zu der URL mit der Bereichs-ID navigiert, scrollt der Browser direkt zur jeweiligen Komponente und zeigt das angegebene Bedienfeld an. Wenn das Bedienfeld so konfiguriert ist, dass es nicht standardmäßig eingeblendet wird, wird es automatisch eingeblendet.

## Akkordeon und responsives Design {#responsive-design}

Alle Kernkomponenten sind so konzipiert, dass sie vollständig responsiv sind und auf allen Geräten ein nahtloses Erlebnis bieten.

Einige erweiterte Komponenten wie die Akkordeon-Komponente erfordern möglicherweise besondere Überlegungen im Kontext des Implementierungsprojekts, um unter allen Bedingungen die Reaktionsfähigkeit zu bewahren. Weitere Informationen finden Sie im Dokument [Responsives Design der Kernkomponenten](/help/responsive.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Mit dem Dialogfeld „Konfigurieren“ können Sie die Akkordeon-Elemente, die Bedienfelder und sein Verhalten und Aussehen für einen Besucher der Seite definieren.

### Registerkarte „Elemente“ {#items-tab}

![Registerkarte „Elemente“ im Dialogfeld „Bearbeiten“ der Akkordeon-Komponente](/help/assets/accordion-edit-items.png)

Verwenden Sie die Schaltfläche **Hinzufügen**, um die Komponentenauswahl zu öffnen und dort auszuwählen, welche Komponente als Bedienfeld hinzugefügt werden soll. Nach dem Hinzufügen wird der Liste ein Eintrag hinzugefügt, der die folgenden Spalten enthält:

* **Symbol** - Das Symbol des Komponententyps des Bedienfelds zur einfachen Identifizierung in der Liste. Bewegen Sie den Mauszeiger darüber, um den vollständigen Komponentennamen als QuickInfo zu sehen.
* **Beschreibung** - Die Beschreibung, die als Text des Bedienfelds verwendet wird und standardmäßig den Namen der für das Bedienfeld ausgewählten Komponente enthält.
* **Entfernen** - Tippen oder klicken Sie, um das Bedienfeld aus der Akkordeon-Komponente zu löschen.
* **Neu anordnen** - Tippen oder klicken und ziehen Sie, um die Reihenfolge der Bedienfelder neu anzuordnen.

>[!TIP]
>
>Wenn der Viewport der Seite so reduziert wird, dass das Bearbeitungsdialogfeld im Vollbildmodus angezeigt wird, ist die Schaltfläche **Hinzufügen** ausgeblendet. Sie können der Akkordeon-Komponente weiterhin Komponenten hinzufügen, indem Sie sie [per Drag-and-Drop aus dem Komponenten-Browser ziehen und im Seiteneditor auf der Akkordeon-Komponente ablegen](https://helpx.adobe.com/de/experience-manager/6-5/sites/authoring/using/editing-content.html#InsertingaComponent).

### Registerkarte „Eigenschaften“ {#properties-tab}

![Registerkarte „Hintergrund“ im Dialogfeld „Design“ der Akkordeon-Komponente](/help/assets/accordion-edit-properties.png)

* **Einzelne Elementerweiterung** - Wenn diese Option ausgewählt ist, wird jeweils ein einzelnes Akkordeon-Element eingeblendet. Wenn Sie ein Element einblenden, werden alle anderen ausgeblendet.
* **Erweiterte Elemente** - Diese Option definiert die Elemente, die standardmäßig beim Laden der Seite eingeblendet werden.
   * Wenn **Einzelne Elementerweiterung** ausgewählt ist, muss ein Bedienfeld ausgewählt werden. Standardmäßig wird das erste Bedienfeld ausgewählt.
   * Wenn **Einzelne Elementerweiterung** nicht ausgewählt ist, ist diese Option eine Mehrfachauswahl und optional.
* **ID** – Diese Option dient zur Kontrolle der eindeutigen Kennung der Komponente in der HTML-Datei und auf der [Datenschicht](/help/developing/data-layer/overview.md).
   * Wenn Sie das Feld leer lassen, wird automatisch eine eindeutige ID generiert, die Sie über die resultierende Seite finden.
   * Sofern eine ID angegeben wird, ist vom Autor bzw. der Autorin sicherzustellen, dass diese eindeutig ist.
   * Änderungen der ID können sich auf das CSS-, JS- und Datenschicht-Tracking auswirken.

## Popover „Bedienfeld auswählen“ {#select-panel-popover}

Der Inhaltsautor kann in der Komponenten-Symbolleiste die Option **Bedienfeld auswählen** verwenden, um zu einem anderes Bedienfeld zu wechseln, um es zu bearbeiten, und auch um die Reihenfolge der Registerkarten innerhalb des Akkordeons einfach zu ändern.

![Symbol „Bedienfeld auswählen“](/help/assets/select-panel-icon.png)

Nach Auswahl der Option **Bedienfeld auswählen** in der Komponentensymbolleiste werden die konfigurierten Akkordeon-Bedienfelder als Dropdown-Liste angezeigt.

![Popover „Bedienfeld auswählen“](/help/assets/select-panel-popover.png)

* Die Liste wird im Sinne der zugewiesenen Anordnung der Bedienfelder geordnet, was sich auch in der Nummerierung zeigt.
* Der Komponententyp des Bedienfelds wird zuerst angezeigt, gefolgt von der Beschreibung des Bedienfelds in hellerer Schriftart.
* Durch Tippen oder Klicken auf einen Eintrag in der Dropdown-Liste wird die Ansicht im Editor auf dieses Bedienfeld umgestellt.
* Die Bedienfelder können direkt mithilfe der Ziehgriffe neu angeordnet werden.

## Dialogfeld „Design“ {#design-dialog}

Das Dialogfeld „Design“ ermöglicht es dem Vorlagenautor, die Optionen zu definieren, die für den Inhaltsautor bei Verwendung der Akkordeon-Komponente verfügbar sind, sowie die Standardeinstellungen bei Platzierung der Akkordeon-Komponente.

### Registerkarte „Eigenschaften“ {#properties-tab-design}

![Registerkarte „Eigenschaften“ im Dialogfeld „Design“](/help/assets/accordion-design-properties.png)

* **Zulässige Überschriftenelemente** - Diese Mehrfachauswahl-Dropdown-Liste definiert die HTML-Elemente für die Überschrift des Akkordeon-Elements, die von einem Autor ausgewählt werden können.
* **Standardmäßiges Überschriftenelement** - Diese Dropdown-Liste definiert das Standard-HTML-Überschriftenelement für das Akkordeon-Element.

### Registerkarte „Zugelassene Komponenten“ {#allowed-components-tab}

Über die Registerkarte **Zugelassene Komponenten** können Sie definieren, welche Komponenten der Akkordeon-Komponente vom Inhaltsautor als Elemente in Bedienfeldern hinzugefügt werden können.

Die Registerkarte „Zugelassene Komponenten“ funktioniert auf die gleiche Weise wie die Registerkarte desselben Namens beim [Definieren der Richtlinie und Eigenschaften eines Layout-Containers im Vorlageneditor.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=de#editing-a-template-layout-template-author)

### Registerkarte „Arten“ {#styles-tab}

Die Akkordeon-Komponente unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).

## Adobe Client-Datenschicht {#data-layer}

Die Akkordeon-Komponente unterstützt die [Adobe Client-Datenschicht](/help/developing/data-layer/overview.md).
