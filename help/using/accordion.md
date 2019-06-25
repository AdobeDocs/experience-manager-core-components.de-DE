---
title: Akkordeon-Komponente
seo-title: Akkordeon-Komponente
description: 'null'
seo-description: Die Komponente "Core-Komponente Akkordeon" ermöglicht die Erstellung einer Sammlung von Feldern, die in einem Akkordeon auf einer Seite angeordnet sind.
uuid: ec 807 de 9-f 76 c -4850-9 ece-c 3 e 339 a 1 d 626
contentOwner: Benutzer
content-type: Referenz
topic-tags: authoring
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-new
discoiquuid: f 093 f 58 e -9755-4 a 4 f -803 a-ab 93 a 50 e 6870
translation-type: tm+mt
source-git-commit: bbd54d433cbeee5395dc8b90bc47f9b44747e25b

---


# Accordion Component{#accordion-component}

Die Komponente &quot;Core-Komponente Akkordeon&quot; ermöglicht die Erstellung einer Sammlung von Feldern, die in einem Akkordeon auf einer Seite angeordnet sind.

## Nutzung {#usage}

The Core Component Accordion component allows for the creation of a collection of components, composed as panels, and arranged in an accordion on a page, similar to the [Tabs Component](tabs.md), but allows for expanding and collapsing of the panels.

* The accordion&#39;s properties can be defined in the [configure dialog](#configure-dialog).
* The order of the panels of the accordion can be defined in the configure dialog as well as the [select panel popover](#select-planel.md).
* Defaults for the Accordion Component when adding it to a page can be defined in the [design dialog](#design-dialog).

## Version and Compatibility {#version-and-compatibility}

Die aktuelle Version der Akkordeon-Komponente ist v 1, die mit Version 2.5.0 der Kernkomponenten im Juni 2019 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |---|
| v1 | Kompatibel | Kompatibel | Kompatibel |

For more information about Core Component versions and releases, see the document [Core Components Versions](versions.md).

## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](http://opensource.adobe.com/aem-core-wcm-components/library/accordion.html).

## Technical Details {#technical-details}

The latest technical documentation about the Accordion Component [can be found on GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/accordion/v1/accordion).

Further details about developing Core Components can be found in the [Core Components developer documentation](developing.md).

## Configure Dialog {#configure-dialog}

Das Dialogfeld &quot;Konfigurieren&quot; ermöglicht es dem Inhaltsautor, das Akkordeon-Element, seine Bedienfelder und dessen Verhalten zu definieren und für einen Besucher der Seite zu erscheinen.

### Items Tab {#items-tab}

![](assets/screen-shot-2019-06-21-08.26.38.png)

Use the **Add** button to open the component selector to choose which component to add as a panel. Nach dem Hinzufügen wird der Liste ein Eintrag hinzugefügt, der die folgenden Spalten enthält:

* **Symbol** - Das Symbol des Komponententyps zur einfachen Identifizierung in der Liste. Bewegen Sie den Mauszeiger über den vollständigen Komponentennamen als quickinfo.
* **Beschreibung** : Die Beschreibung, die als Text des Bedienfelds verwendet wird und standardmäßig den Namen der für das Bedienfeld ausgewählten Komponente angibt.
* **Löschen** - Tippen oder klicken Sie auf, um das Bedienfeld aus der Akkordeon-Komponente zu löschen.
* **Neu anordnen** - Tippen oder klicken Sie auf, um die Reihenfolge der Bedienfelder neu anzuordnen.

### Properties Tab {#properties-tab}

![](assets/screen-shot-2019-06-21-08.26.53.png)

* **Einzelne Elementerweiterung** : Wenn diese Option aktiviert ist, wird ein einzelnes Akkordeon-Element gleichzeitig erweitert. Wenn Sie ein Element erweitern, reduzieren Sie dann alle anderen.
* **Erweiterte Elemente** - Diese Option definiert die Elemente, die standardmäßig beim Laden der Seite erweitert werden.
   * When **Single item expansion** is selected, one panel must be selected. Standardmäßig wird das erste Bedienfeld ausgewählt.
   * When **Single item expansion** is not selected, this option is a multi-select and is optional.

## Select Panel Popover {#seelct-panel-popover}

The content author can use the **Select Panel** option on the component toolbar to change to a different panel for editing as well as to easily rearrange the order of the panels within the accordion.

![](assets/screen-shot-2019-06-21-08.49.36.png)

Once selecting the **Select Panel** option in the component toolbar, the configured accordion panels are displayed as a drop-down.

![](assets/screen-shot-2019-06-21-08.52.14.png)

* Die Liste wird durch die zugewiesene Anordnung der Bedienfelder angeordnet und wird in der Nummerierung angezeigt.
* Der Komponententyp des Bedienfelds wird zuerst angezeigt, gefolgt von der Beschreibung des Bedienfelds in der helleren Schriftart.
* Durch Tippen oder Klicken auf einen Eintrag in der Dropdown-Liste wird die Ansicht im Editor in dieses Bedienfeld verschoben.
* Die Bedienfelder können mithilfe der Ziehpunkte neu angeordnet werden.

## Design Dialog {#design-dialog}

Das Design-Dialogfeld ermöglicht es dem Vorlagenautor, die Optionen für den Inhaltsautor zu definieren, der die Akkordeon-Komponente verwendet, und die Standardeinstellungen, die beim Platzieren der Akkordeon-Komponente festgelegt werden.

### Properties Tab {#properties-tab-design}

![](assets/screen-shot-2019-06-21-08.58.11.png)

* **Zulässige Überschriften-Elemente** - Diese Dropdownliste Mehrfachauswahl definiert die HTML-Elemente für das Akkordeon-Element, die von einem Autor ausgewählt werden dürfen.
* **Element** &quot;Standardüberschrift&quot; : Diese Dropdown-Liste definiert das Standardmäßige HTML-Element für das Akkordeon-Element.

### Allowed Components Tab {#allowed-components-tab}

The **Allowed Components** tab is used to define which components can be added as items to panels in the Accordion Component by the content author.

The Allowed Components tab functions in the same way as the tab of the same name when [defining the policy and properties of a Layout Container in the Template Editor.](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html)

### Styles Tab {#styles-tab}

The Accordion Component supports the AEM [Style System](authoring.md#component-styling).
