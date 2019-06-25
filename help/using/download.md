---
title: Komponente herunterladen
seo-title: Komponente herunterladen
description: 'null'
seo-description: Die Komponente "Core-Komponente-Download" ermöglicht die Erstellung einer Download-Option auf einer Seite.
uuid: ec 807 de 9-f 76 c -4850-9 ece-c 3 e 339 a 1 d 626
contentOwner: Benutzer
content-type: Referenz
topic-tags: authoring
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-new
discoiquuid: f 093 f 58 e -9755-4 a 4 f -803 a-ab 93 a 50 e 6870
translation-type: tm+mt
source-git-commit: 88bc68b60e5de247fe800ac041ffefdf9238cce1

---


# Download Component{#download-component}

Die Komponente &quot;Core-Komponente-Download&quot; ermöglicht die Erstellung einer Download-Option auf einer Seite.

## Nutzung {#usage}

Die Komponente &quot;Core-Komponente-Download&quot; ermöglicht die Einbeziehung einer Download-Option und des zugehörigen Assets auf einer Seite.

* The download option&#39;s properties can be selected in the [configure dialog](#configure-dialog).
* Defaults for the download component can be defined in the [design dialog](#design-dialog).

## Version and Compatibility {#version-and-compatibility}

Die aktuelle Version der Download-Komponente ist v 1, die mit Version 2.5.0 der Kernkomponenten im Juni 2019 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |---|
| v1 | Kompatibel | Kompatibel | Kompatibel |

For more information about Core Component versions and releases, see the document [Core Components Versions](versions.md).

## Sample Component Output {#sample-component-output}

To experience the Download Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](http://opensource.adobe.com/aem-core-wcm-components/library/download.html).

## Technical Details {#technical-details}

The latest technical documentation about the Download Component [can be found on GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/download/v1/download).

Further details about developing Core Components can be found in the [Core Components developer documentation](developing.md).

## Configure Dialog {#configure-dialog}

Das Dialogfeld &quot;Konfigurieren&quot; ermöglicht dem Inhaltsautor das Herunterladen des Downloadelements und die Art und Weise, wie er sich für einen Besucher der Seite verhalten wird.

![](assets/screen-shot-2019-06-17-09.49.14.png)

### Asset Tab {#asset-tab}

The selection of a download asset is very similar to the functionality of the [Image Component](image.md) and likewise leverages AEM&#39;s DAM.

* **Asset herunterladen**
   * Drop an asset from the [asset browser](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/author-environment-tools.html) or tap the **browse** option to upload from a local file system.
   * Tap or click **Clear** to de-select the currently selected image.
   * Tap or click **Edit** to [mange the renditions of the asset](https://helpx.adobe.com/experience-manager/6-5/assets/using/managing-assets-touch-ui.html) in the asset editor.

### Properties Tab {#properties-tab}

![](assets/screen-shot-2019-06-17-09.49.51.png)

* **Titel** - Wird als Überschrift für das Downloadelement angezeigt
   * **Titel vom DAM-Asset abrufen** - Wenn ausgewählt, wird der Titel automatisch mit dem DAM-Asset-Titel ausgefüllt.
* **Beschreibung** - Wird als beschreibendes Unterüberschrift des Downloadelements angezeigt
   * **Beschreibung vom DAM-Asset abrufen** - Wenn ausgewählt, wird die Beschreibung automatisch mit der Beschreibung des DAM-Assets ausgefüllt.
* **Action Text** - Wird als Action Text for the Download Item angezeigt
   * Dieses Feld ist beim Hochladen eines Assets aus dem Dateisystem erforderlich.
   * **Inline-Anzeige** : Wenn ausgewählt wird, wird der angegebene **Aktionstext** inline angezeigt.

## Design Dialog {#design-dialog}

Im Entwurfsdialogfeld kann der Vorlagenautor die verfügbaren Optionen für den Inhaltsautor definieren, der die Downloadkomponente verwendet.

### Properties Tab {#properties-tab-design}

![](assets/screen-shot-2019-06-17-10.04.31.png)

* **Standardaktionstext** : Definiert den **Standardmäßigen Aktionstext,** der angegeben wird, wenn ein Autor die Download-Komponente einer Seite hinzufügt.
* **Upload von Dateisystem** zulassen: Ermöglicht dem Inhaltsautor das Hochladen eines Assets aus seinem lokalen Filesystem als Download-Asset.
   * Der Standardwert ist nicht ausgewählt.
* **Titeltyp** - Das HTML-Element, das für den Titel der Downloadkomponente verwendet wird.
   * Wenn kein Wert ausgewählt ist, lautet der Standardwert H 3.
* **Dateigröße anzeigen** : Wenn ausgewählt, wird die Dateigröße des Assets in der Downloadkomponente angezeigt.
   * Der Standardwert ist ausgewählt.
* **Dateiformat anzeigen** : Wenn ausgewählt, wird das Dateiformat des Assets in der Downloadkomponente angezeigt.
   * Der Standardwert ist ausgewählt.
* **Dateiname anzeigen** : Wenn ausgewählt, wird der Dateiname des Assets in der Downloadkomponente angezeigt.
   * Der Standardwert ist ausgewählt.

### Styles Tab {#styles-tab}

The Image Component supports the AEM [Style System](authoring.md#component-styling).
