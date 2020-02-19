---
title: Akkordeon-Komponente
description: Dier Kernkomponente „Akkordeon“ ermöglicht die Erstellung einer Sammlung von Bedienfeldern, die auf der Seite in einem Akkordeon angeordnet sind.
translation-type: tm+mt
source-git-commit: fe8a121520000ffd56ae3347469590e89121eaf0

---


# Akkordeon-Komponente{#accordion-component}

Dier Kernkomponente „Akkordeon“ ermöglicht die Erstellung einer Sammlung von Bedienfeldern, die auf der Seite in einem Akkordeon angeordnet sind.

## Nutzung {#usage}

Die Kernkomponente „Akkordeon“ ermöglicht die Erstellung einer Sammlung von Komponenten in Form von Bedienfeldern, die auf einer Seite in einem Akkordeon angeordnet sind, ähnlich der [Registerkarten-Komponente](tabs.md), jedoch mit der Möglichkeit, die Bedienfelder ein- und auszublenden.

* Die Eigenschaften des Akkordeons können im [Dialogfeld „Konfigurieren“](#configure-dialog) definiert werden.
* Die Reihenfolge der Bedienfelder im Akkordeon kann im Dialogfeld „Konfigurieren“ und im [Popover zur Bedienfeldauswahl](#select-panel-popover) definiert werden.
* Standardwerte für die Akkordeon-Komponente können beim Hinzufügen zu einer Seite im [Dialogfeld „Design“](#design-dialog) konfiguriert werden.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Akkordeon-Komponente ist v1, die mit Version 2.5.0 der Kernkomponenten im Juni 2019 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.3 | AEM 6.4 | AEM 6.5 | AEM als Cloud Service |
|--- |--- |--- |---|---|
| v1 | Kompatibel | Kompatibel | Kompatibel | Kompatibel |

Weitere Informationen zu Kernkomponentenversionen und -freigaben finden Sie in den [Kernkomponentenversionen](/help/versions.md).

## Musterkomponentenausgabe {#sample-component-output}

Um die Akkordeon-Komponente sowie Beispiele für die Konfigurationsoptionen sowie HTML- und JSON-Ausgaben zu erhalten, besuchen Sie die [Komponentenbibliothek](https://adobe.com/go/aem_cmp_library_accordion).

## Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur Akkordeon-Komponente [finden Sie auf GitHub](https://adobe.com/go/aem_cmp_tech_accordion_v1).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Mit dem Dialogfeld „Konfigurieren“ kann die Akkordeon-Elemente, die Bedienfelder und sein Verhalten und Aussehen für einen Besucher der Seite definieren.

### Registerkarte „Elemente“ {#items-tab}

![](/help/assets/screen-shot-2019-06-21-08.26.38.png)

Verwenden Sie die Schaltfläche **Hinzufügen**, um die Komponentenauswahl zu öffnen und dort auszuwählen, welche Komponente als Bedienfeld hinzugefügt werden soll. Nach dem Hinzufügen wird der Liste ein Eintrag hinzugefügt, der die folgenden Spalten enthält:

* **Symbol** - Das Symbol des Komponententyps des Bedienfelds zur einfachen Identifizierung in der Liste. Bewegen Sie den Mauszeiger darüber, um den vollständigen Komponentennamen als QuickInfo zu sehen.
* **Beschreibung** - Die Beschreibung, die als Text des Bedienfelds verwendet wird und standardmäßig den Namen der für das Bedienfeld ausgewählten Komponente enthält.
* **Entfernen** - Tippen oder klicken Sie, um das Bedienfeld aus der Akkordeon-Komponente zu löschen.
* **Neu anordnen** - Tippen oder klicken und ziehen Sie, um die Reihenfolge der Bedienfelder neu anzuordnen.

>[!TIP]
>
>Wenn der Viewport der Seite so reduziert wird, dass das Bearbeitungsdialogfeld im Vollbildmodus angezeigt wird, ist die Schaltfläche **Hinzufügen** ausgeblendet. Sie können der Akkordeon-Komponente weiterhin Komponenten hinzufügen, indem Sie sie [per Drag-and-Drop aus dem Komponenten-Browser ziehen und im Seiteneditor auf der Akkordeon-Komponente ablegen](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/editing-content.html#InsertingaComponent).

### Registerkarte „Eigenschaften“{#properties-tab}

![](/help/assets/screen-shot-2019-06-21-08.26.53.png)

* **Einzelelement-Erweiterung** - Wenn diese Option ausgewählt ist, wird jeweils ein einzelnes Akkordeon-Element eingeblendet. Wenn Sie ein Element einblenden, werden alle anderen ausgeblendet.
* **Erweiterte Elemente** - Diese Option definiert die Elemente, die standardmäßig beim Laden der Seite eingeblendet werden.
   * Wenn **Einzelelement-Erweiterung** ausgewählt ist, muss ein Bedienfeld ausgewählt werden. Standardmäßig wird das erste Bedienfeld ausgewählt.
   * Wenn **Einzelelement-Erweiterung** nicht ausgewählt ist, ist diese Option eine Mehrfachauswahl und optional.

## Popover zur Bedienfeldauswahl{#select-panel-popover}

Der Inhaltsautor kann in der Komponenten-Symbolleiste die Option **Bedienfeld auswählen** verwenden, um zu einem anderes Bedienfeld zu wechseln, um es zu bearbeiten, und auch um die Reihenfolge der Registerkarten innerhalb des Akkordeons einfach zu ändern.

![](/help/assets/screen-shot-2019-06-21-08.49.36.png)

Nach Auswahl der Option **Bedienfeld auswählen** in der Komponentensymbolleiste werden die konfigurierten Akkordeon-Bedienfelder als Dropdown-Liste angezeigt.

![](/help/assets/screen-shot-2019-06-21-08.52.14.png)

* Die Liste wird im Sinne der zugewiesenen Anordnung der Bedienfelder geordnet, was sich auch in der Nummerierung zeigt.
* Der Komponententyp des Bedienfelds wird zuerst angezeigt, gefolgt von der Beschreibung des Bedienfelds in hellerer Schriftart.
* Durch Tippen oder Klicken auf einen Eintrag in der Dropdown-Liste wird die Ansicht im Editor auf dieses Bedienfeld umgestellt.
* Die Bedienfelder können direkt mithilfe der Ziehgriffe neu angeordnet werden.

## Dialogfeld „Design“ {#design-dialog}

Das Dialogfeld „Design“ ermöglicht es dem Vorlagenautor, die Optionen zu definieren, die für den Inhaltsautor bei Verwendung der Akkordeon-Komponente verfügbar sind, sowie die Standardeinstellungen bei Platzierung der Akkordeon-Komponente.

### Registerkarte „Eigenschaften“{#properties-tab-design}

![](/help/assets/screen-shot-2019-06-21-08.58.11.png)

* **Zulässige Überschriftenelemente** - Diese Mehrfachauswahl-Dropdown-Liste definiert die HTML-Elemente für die Überschrift des Akkordeon-Elements, die von einem Autor ausgewählt werden können.
* **Standard-Überschriftenelement** - Diese Dropdown-Liste definiert das Standard-HTML-Überschriftenelement für das Akkordeon-Element.

### Registerkarte „Zugelassene Komponenten“{#allowed-components-tab}

Über die Registerkarte **Zugelassene Komponenten** können Sie definieren, welche Komponenten der Akkordeon-Komponente vom Inhaltsautor als Elemente in Bedienfeldern hinzugefügt werden können.

Die Registerkarte „Zugelassene Komponenten“ funktioniert auf die gleiche Weise wie die Registerkarte desselben Namens beim [Definieren der Richtlinie und Eigenschaften eines Layoutcontainers im Vorlageneditor.](https://docs.adobe.com/content/help/en/experience-manager-65/authoring/siteandpage/templates.html)

### Registerkarte „Stile“ {#styles-tab}

Die Akkordeon-Komponente unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).
