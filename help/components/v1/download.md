---
title: Download-Komponente (v1)
description: Die Kernkomponente „Download-Komponente“ ermöglicht die Erstellung einer Download-Option auf einer Seite.
role: Architect, Developer, Admin, User
exl-id: ebd63522-218d-4784-bea0-1627c64f5230
index: n
source-git-commit: 92a3ec273a5be6751c1503835b9c2e5cbd61bb9e
workflow-type: ht
source-wordcount: '0'
ht-degree: 100%

---


# Download-Komponente (v1) {#download-component}

Die Kernkomponente „Download-Komponente“ ermöglicht die Erstellung einer Download-Option auf einer Seite.

## Nutzung {#usage}

Die Kernkomponente „Download-Komponente“ ermöglicht die Erstellung einer Download-Option und zugehöriger Elemente auf einer Seite.

* Die Eigenschaften der Download-Komponente können im [Dialogfeld „Konfigurieren“](#configure-dialog) ausgewählt werden.
* Standardwerte für die Download-Komponente können im [Dialogfeld „Design“](#design-dialog) definiert werden.

## Version und Kompatibilität {#version-and-compatibility}

In diesem Dokument wird die v1 der Download-Komponente beschrieben, die mit Version 2.5.0 der Kernkomponenten im Juni 2019 eingeführt wurde.

>[!CAUTION]
>
>In diesem Dokument wird die v1 der Download-Komponente beschrieben.
>
>Weitere Informationen zur aktuellen Version der Download-Komponente finden Sie im Dokument [Download-Komponente](/help/components/download.md).

## Musterkomponentenausgabe {#sample-component-output}

Um die Download-Komponente sowie Beispiele für die Konfigurationsoptionen sowie HTML- und JSON-Ausgaben zu erhalten, besuchen Sie die [Komponentenbibliothek](https://adobe.com/go/aem_cmp_library_download_de).

## Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur Download-Komponente [finden Sie auf GitHub](https://adobe.com/go/aem_cmp_tech_download_v1_de).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Mit dem Dialogfeld „Konfigurieren“ kann der Inhaltsautor das Download-Element und sein Verhalten und Aussehen für einen Besucher der Seite definieren.

![Registerkarte „Asset“ auf dem Dialogfeld „Bearbeiten“ der Download-Komponente](/help/assets/download-edit-asset.png)

### Registerkarte „Asset“ {#asset-tab}

Die Auswahl eines Download-Assets ähnelt der Funktionalität der [Bildkomponente](image-v1.md) und nutzt gleichermaßen das AEM-DAM.

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
