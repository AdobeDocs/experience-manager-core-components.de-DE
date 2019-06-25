---
title: Container-Komponente
seo-title: Container-Komponente
description: 'null'
seo-description: Die Komponente Component Component Container ermöglicht die Erstellung eines Containers für mehrere zusätzliche Komponenten auf einer Seite.
uuid: ec 807 de 9-f 76 c -4850-9 ece-c 3 e 339 a 1 d 626
contentOwner: Benutzer
content-type: Referenz
topic-tags: authoring
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-new
discoiquuid: f 093 f 58 e -9755-4 a 4 f -803 a-ab 93 a 50 e 6870
translation-type: tm+mt
source-git-commit: 3e2e7a297c6ee1d6c8d092c619df8febdc900e25

---


# Container Component{#container-component}

Die Komponente Component Component Container ermöglicht die Erstellung eines Containers für mehrere zusätzliche Komponenten auf einer Seite.

## Nutzung {#usage}

Die Komponente Component Component Container ermöglicht die Erstellung eines Containers für mehrere zusätzliche Komponenten auf einer Seite und kann verwendet werden, um andere Komponenten zu gruppieren und einen allgemeinen Stil oder ein gemeinsames Layout anzuwenden.

* The container&#39;s properties can be selected in the [configure dialog](#configure-dialog).
* Defaults for the Container Component when adding it to a page can be defined in the [design dialog](#design-dialog).

## Version and Compatibility {#version-and-compatibility}

Die aktuelle Version der Container-Komponente ist v 1, die mit Version 2.5.0 der Kernkomponenten im Juni 2019 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |---|
| v1 | Kompatibel | Kompatibel | Kompatibel |

For more information about Core Component versions and releases, see the document [Core Components Versions](versions.md).

## Sample Component Output {#sample-component-output}

To experience the Container Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](http://opensource.adobe.com/aem-core-wcm-components/library/container.html).

## Technical Details {#technical-details}

The latest technical documentation about the Container Component [can be found on GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/container/v1/container).

Further details about developing Core Components can be found in the [Core Components developer documentation](developing.md).

## Configure Dialog {#configure-dialog}

Das Dialogfeld &quot;Konfigurieren&quot; ermöglicht dem Inhaltsautor das Definieren des Behälterelements und die Art und Weise, wie er sich für einen Besucher der Seite verhalten wird.

![](assets/screen-shot-2019-06-21-13.59.26.png)

* **Layout** - Diese Option definiert das Verhalten oder das Layout-Verhalten der Container-Komponente.
   * **Einfach** - Definiert einen Container als einfache Sammlung von Komponenten
   * **Responsives Raster** : Definiert einen Container als interaktives [AEM-Raster](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/responsive-layout.html)
* **ID** - Verwenden Sie diese Option, um das HTML-ID-Attribut zu definieren, das auf die Komponente angewendet werden soll.
* **Hintergrundfarbe** - Definieren Sie entweder als freie RGB-Werte oder mithilfe der Farbauswahl [, je nach Konfiguration.](#background-tab)
* **Hintergrundbild** - Definiert [eine Hintergrundfarbe für den Container, je nach Konfiguration](#background-tab)

## Design Dialog {#design-dialog}

Das Design-Dialogfeld ermöglicht es dem Vorlagenautor, die verfügbaren Optionen für den Inhaltsautor zu definieren, der die Container-Komponente verwendet.

### Allowed Components Tab {#allowed-components-tab}

The **Allowed Components** tab is used to define which components can be added as items to the Container Component by the content author.

The Allowed Components tab functions in the same way as the tab of the same name when [defining the policy and properties of a Layout Container in the Template Editor.](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html)

### Default Components Tab {#default-components-tab}

The Default Components tab is used to define which component is added to the component when a particular asset type is dropped on the container, similar to [how default components are defined on the page template](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html#EditingTemplatesTemplateAuthors).

### Responsive Settings Tab {#responsive-settings-tab}

![](assets/screen-shot-2019-06-21-09.33.03.png)

* **Spalten** : Definiert die Anzahl der Spalten im Raster des resultierenden Containers.

### Background Tab {#background-tab}

![](assets/screen-shot-2019-06-21-09.42.42.png)

* **Hintergrundbild**
   * **Hintergrundbild** aktivieren: Wählen Sie diese Option, damit der Inhaltsautor ein Hintergrundbild für den Container definieren kann.
* **Hintergrundfarbe**
   * **Hintergrundfarbe** aktivieren: Wählen Sie diese Option, um dem Inhaltsautor die Definition einer Hintergrundfarbe für den Container zu ermöglichen.
   * **Nur Farbfelder** : Wählen Sie diese Option aus, damit der Inhaltsautor nur aus vordefinierten Farbfeldern für die Containerhintergrundfarbe auswählen kann.
      * Only available when **Enable background color** is selected
* **Zulässige Farbfelder** : Definieren vordefinierter Farben, aus denen der Inhaltsautor die Hintergrundfarbe des Containers auswählen kann
   * Use the **Add** button to add a pre-defined color swatch. Nach dem Hinzufügen wird der Liste ein Eintrag hinzugefügt, der die folgenden Spalten enthält:
   * **Wert** : Definieren Sie die Farbe manuell über RGB-Werte.
      * Tippen oder klicken Sie auf die Farbauswahl, um eine Farbe leichter auszuwählen, indem Sie einzelne RGB-Werte anpassen oder einen hexadezimalen Wert definieren.
   * **Löschen** - Tippen oder klicken Sie, um ein Muster zu löschen.
   * **Neu anordnen** - Tippen oder klicken Sie auf, um die Reihenfolge der Farbfelder neu anzuordnen.

### Styles Tab {#styles-tab}

The Container Component supports the AEM [Style System](authoring.md#component-styling).
