---
title: 'Download-Komponente '
description: Die Kernkomponente „Download-Komponente“ ermöglicht die Erstellung einer Download-Option auf einer Seite.
role: Architect, Developer, Admin, User
exl-id: 48e7ade0-b849-4d1f-b836-51196e5ac507
source-git-commit: dd30def59a8f037864da875ef4c831b11f766e57
workflow-type: ht
source-wordcount: '741'
ht-degree: 100%

---


# Download-Komponente {#download-component}

Die Kernkomponente „Download-Komponente“ ermöglicht die Erstellung einer Download-Option auf einer Seite.

{{traditional-aem}}

## Nutzung {#usage}

Die Kernkomponente „Download-Komponente“ ermöglicht die Erstellung einer Download-Option und zugehöriger Elemente auf einer Seite.

* Die Eigenschaften der Download-Komponente können im [Dialogfeld „Konfigurieren“](#configure-dialog) ausgewählt werden.
* Standardwerte für die Download-Komponente können im [Dialogfeld „Design“](#design-dialog) definiert werden.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Download-Komponente ist v2, die mit Version 2.18.0 der Kernkomponenten im Februar 2022 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |---|---|---|
| v2 | – | Kompatibel | Kompatibel | Kompatibel |
| [v1](v1/download.md) | Kompatibel | Kompatibel | – | Kompatibel |

Weitere Informationen zu Kernkomponentenversionen und -freigaben finden Sie im Dokument [Kernkomponentenversionen](/help/versions.md).

## Musterkomponentenausgabe {#sample-component-output}

Um die Download-Komponente sowie Beispiele für die Konfigurationsoptionen sowie HTML- und JSON-Ausgaben zu erhalten, besuchen Sie die [Komponentenbibliothek](https://adobe.com/go/aem_cmp_library_download_de).

## Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur Download-Komponente [finden Sie auf GitHub](https://adobe.com/go/aem_cmp_tech_download_v2_de).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Mit dem Dialogfeld „Konfigurieren“ kann der Inhaltsautor das Download-Element und sein Verhalten und Aussehen für einen Besucher der Seite definieren.

![Registerkarte „Asset“ auf dem Dialogfeld „Bearbeiten“ der Download-Komponente](/help/assets/download-edit-asset.png)

### Registerkarte „Asset“ {#asset-tab}

Die Auswahl eines Download-Assets ähnelt der Funktionalität der [Bildkomponente](image.md) und nutzt gleichermaßen das AEM-DAM.

* **Asset herunterladen**
   * Ziehen Sie ein Asset aus dem [Asset-Browser](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html?lang=de) oder tippen Sie auf die Option **Durchsuchen**, um es von einem lokalen Dateisystem hochzuladen.
   * Tippen oder klicken Sie auf **Löschen**, um das aktuell ausgewählte Bild zu deaktivieren.
   * Tippen oder klicken Sie auf **Bearbeiten**, um die [Ausgabedarstellungen des Assets](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/manage-digital-assets.html?lang=de) im Asset-Editor zu verwalten.

### Registerkarte „Eigenschaften“ {#properties-tab}

![Registerkarte „Eigenschaften“ auf dem Dialogfeld „Bearbeiten“ der Download-Komponente](/help/assets/download-edit-properties.png)

* **Titel** - Wird als Überschrift für das Download-Element angezeigt
   * **Titel von DAM-Asset abrufen** - Wenn ausgewählt, wird der Titel automatisch mit dem Titel des DAM-Assets ausgefüllt.
* **Beschreibung** - Zeigt eine beschreibende Unterüberschrift des Download-Elements an
   * **Beschreibung von DAM-Asset abrufen** - Wenn ausgewählt, wird die Beschreibung automatisch mit der Beschreibung des DAM-Assets ausgefüllt.
* **Aktionstext** - Zeigt Aktionstext für das Download-Element an
   * Dieses Feld ist beim Hochladen eines Assets aus dem Dateisystem erforderlich.
   * **Inline anzeigen** - Wenn ausgewählt, wird der angegebene **Aktionstext** inline angezeigt.
* **ID** – Diese Option dient zur Kontrolle der eindeutigen Kennung der Komponente in der HTML-Datei und auf der [Datenschicht](/help/developing/data-layer/overview.md).
   * Wenn Sie das Feld leer lassen, wird automatisch eine eindeutige ID generiert, die Sie über die resultierende Seite finden.
   * Sofern eine ID angegeben wird, ist vom Autor bzw. der Autorin sicherzustellen, dass diese eindeutig ist.
   * Änderungen der ID können sich auf das CSS-, JS- und Datenschicht-Tracking auswirken.

### Registerkarte „Arten“ {#styles-tab-edit}

![Registerkarte „Arten“ im Dialogfeld „Bearbeiten“ der Download-Komponente](/help/assets/download-edit-styles.png)

Die Download-Komponente unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).

Verwenden Sie das Dropdown-Menü, um die Stile auszuwählen, die Sie auf die Komponente anwenden möchten. Die im Dialogfeld „Bearbeiten“ vorgenommenen Auswahlen haben denselben Effekt wie die in der Komponenten-Symbolleiste ausgewählten.

Stile müssen für diese Komponente im [Dialogfeld „Design“](#design-dialog) konfiguriert werden, damit das Dropdown-Menü verfügbar ist.

## Dialogfeld „Design“ {#design-dialog}

Das Dialogfeld „Design“ ermöglicht es dem Vorlagenautor, die Optionen für den Inhaltsautor zu definieren, der die Download-Komponente verwendet.

### Registerkarte „Eigenschaften“ {#properties-tab-design}

![Dialogfeld „Design“ der Download-Komponente](/help/assets/download-design.png)

* **Uploads aus Dateisystem zulassen** - Ermöglicht dem Inhaltsautor das Hochladen eines Assets aus seinem lokalen Dateisystem als Download-Asset.
   * Der Standardwert ist nicht ausgewählt.
* **Titeltyp** - Das HTML-Element, das für den Titel der Download-Komponente verwendet wird.
   * Wenn kein Wert ausgewählt ist, lautet der Standardwert H3.
* **Dateigröße anzeigen** - Wenn ausgewählt, wird die Dateigröße des Assets in der Download-Komponente angezeigt.
   * Der Standardwert ist ausgewählt.
* **Dateiformat anzeigen** - Wenn ausgewählt, wird das Dateiformat des Assets in der Download-Komponente angezeigt.
   * Der Standardwert ist ausgewählt.
* **Dateiname anzeigen** - Wenn ausgewählt, wird der Dateiname des Assets in der Download-Komponente angezeigt.
   * Der Standardwert ist ausgewählt.

### Registerkarte „Arten“ {#styles-tab}

Die Bildkomponente unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).
