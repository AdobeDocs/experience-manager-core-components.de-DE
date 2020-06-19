---
title: PDF Viewer-Komponente
description: Die PDF-Viewer-Komponente ermöglicht die Anzeige eines PDF-Dokuments.
translation-type: tm+mt
source-git-commit: b08fc5ec49126f7be19b7433a3d71de877d9e442
workflow-type: tm+mt
source-wordcount: '644'
ht-degree: 13%

---


# PDF Viewer-Komponente {#pdf-viewer-component}


Die Komponente &quot;PDF Viewer für die Hauptkomponente&quot;ermöglicht die Einbindung eines PDF-Dokuments in eine Seite.

## Verwendung {#usage}

Die Komponente &quot;PDF Viewer für die Hauptkomponente&quot;bettet einen Viewer ein, um PDF-Dateien anzuzeigen, die als Assets auf der Seite gespeichert wurden.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der PDF Viewer-Komponente ist Version 1, die mit Version 2.10.0 der Core-Komponenten im Juni 2020 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Kompatibel | Kompatibel | Kompatibel |

Weitere Informationen zu Kernkomponentenversionen und -freigaben finden Sie in den [Kernkomponentenversionen](/help/versions.md).

## Musterkomponentenausgabe {#sample-component-output}

To experience the PDF Viewer Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_pdfviewer).

## Technische Details {#technical-details}

The latest technical documentation about the PDF Viewer Component [can be found on GitHub](https://adobe.com/go/aem_cmp_tech_pdfviewer_v1).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Im Dialogfeld &quot;Konfigurieren&quot;kann der Inhaltsersteller den Viewer definieren und festlegen, wie er sich verhalten und für einen Besucher zur Seite angezeigt werden soll.

### Configuration Tab {#configuration-tab}

Auf der Registerkarte &quot;Konfiguration&quot;kann der Autor festlegen, welche PDF-Datei angezeigt werden soll. Der Pfad kann als Asset in AEM oder als absoluter Pfad zu einer anderen Ressource definiert werden.

![Registerkarte &quot;Konfiguration&quot;des Dialogfelds &quot;Bearbeiten&quot;der PDF Viewer-Komponente](/help/assets/pdf-viewer-edit-configuration.png)

### Registerkarte anpassen {#customize-tab}

Auf der Registerkarte &quot;Anpassen&quot;kann der Autor festlegen, welche Optionen im Viewer für den Leser verfügbar sind und wie der Viewer angezeigt werden soll.

![Registerkarte &quot;Bearbeiten&quot;des Dialogfelds &quot;PDF Viewer-Komponente&quot;anpassen](/help/assets/pdf-viewer-edit-customize.png)

Die Anzahl der verfügbaren Optionen hängt vom ausgewählten **Typ** ab.

* [Volles Fenster](#full-window) - Der Anzeigebereich wird im gesamten Browser gerendert. Dies eignet sich am besten für Datenspeicherung- und Produktivitätsanwendungen.
* [Größter Container](#sized-container) - Der Anzeigebereich wird im gesamten Browser gerendert. Dies eignet sich am besten für Datenspeicherung- und Produktivitätsanwendungen.
* [Inline](#in-line) - Alle PDF-Seiten, die in einer Webseite in einer Zeile wiedergegeben werden. Dies eignet sich am besten zum Lesen von Anwendungen.

#### Vollständiges Fenster {#full-window}

Der Anzeigebereich wird im vollständigen Browser gerendert. Dies eignet sich am besten für Datenspeicherung- und Produktivitätsanwendungen.

![Option für das vollständige Fenster der Registerkarte im Bearbeitungsdialogfeld der PDF Viewer-Komponente anpassen](/help/assets/pdf-viewer-edit-customize-full.png)

* **Standardmodus** der Ansicht: Wie der Viewer auf die Seite passt, auf der er angezeigt wird
   * Fenstergröße
   * Fensterbreite
* **Vollbild** - Bei Aktivierung nimmt der Viewer die volle Höhe/Breite des Viewports ein.
* **Anmerkungswerkzeuge** - Wenn diese Option aktiviert ist, stehen die Anmerkungswerkzeuge zur Verfügung.
* **Linke Hand - Wenn diese Option aktiviert ist, wird der linke Bereich angezeigt** .
* **PDF** herunterladen: Wenn diese Option aktiviert ist, wird die Schaltfläche zum Herunterladen angezeigt.
* **PDF** drucken: Wenn diese Option aktiviert ist, wird die Drucken-Schaltfläche angezeigt.
* **Seitensteuerelemente** : Schaltet das Verhalten der Seitensteuerelemente um.
   * Dock
   * Dock

#### Größter Container {#sized-container}

Der Anzeigebereich wird im vollständigen Browser gerendert. Dies eignet sich am besten für Datenspeicherung- und Produktivitätsanwendungen.

![Option &quot;Container in Registerkartengröße&quot;im Dialogfeld &quot;Bearbeiten&quot;der PDF Viewer-Komponente anpassen](/help/assets/pdf-viewer-edit-customize-sized-container.png)

* **Vollbild** - Bei Aktivierung nimmt der Viewer die volle Höhe/Breite des Viewports ein.
* **PDF** herunterladen: Wenn diese Option aktiviert ist, wird die Schaltfläche zum Herunterladen angezeigt.
* **PDF** drucken: Wenn diese Option aktiviert ist, wird die Drucken-Schaltfläche angezeigt.
* **Seitensteuerelemente** : Schaltet das Verhalten der Seitensteuerelemente um.
   * Dock
   * Dock

#### Inline {#in-line}

Alle PDF-Seiten, die innerhalb einer Webseite in Linie gerendert werden. Dies eignet sich am besten zum Lesen von Anwendungen.

![Option &quot;Container in Registerkartengröße&quot;im Dialogfeld &quot;Bearbeiten&quot;der PDF Viewer-Komponente anpassen](/help/assets/pdf-viewer-edit-customize-inline.png)

* **PDF** herunterladen: Wenn diese Option aktiviert ist, wird die Schaltfläche zum Herunterladen angezeigt.
* **PDF** drucken: Wenn diese Option aktiviert ist, wird die Drucken-Schaltfläche angezeigt.

## Dialogfeld „Design“ {#design-dialog}

Für die PDF-Viewer-Komponente gibt es kein Dialogfeld &quot;Design&quot;.
