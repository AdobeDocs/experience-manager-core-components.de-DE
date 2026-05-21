---
title: PDF-Viewer-Komponente
description: Die PDF-Viewer-Komponente ermöglicht die Anzeige eines PDF-Dokuments.
role: Developer, Admin, User
exl-id: deb635f5-2b73-4e7a-9838-3a941e39e898
TQID: https://experienceleague.adobe.com/dCn7o5IjD1PIHN1M6K1btrnLkXk5bKPr8w3DutA1Vbk
product_v2: id: c45915cf-e157-4af7-a80d-97b905bcb3a5id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 73aa5234ac63fa3be99feebce448bb6722513838
workflow-type: tm+mt
source-wordcount: 716
ht-degree: 100%

---

# PDF-Viewer-Komponente {#pdf-viewer-component}

Die Kernkomponente „PDF-Viewer-Komponente“ ermöglicht die Integration eines PDF-Dokuments in eine Seite.

{{traditional-aem}}

## Nutzung {#usage}

Die Kernkomponente „PDF-Viewer-Komponente“ bettet einen Viewer zur Anzeige von PDF-Dateien ein, die als Assets auf der Seite gespeichert werden.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der PDF-Viewer-Komponente ist v1, die mit Version 2.10.0 der Kernkomponenten im Juni 2020 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |---|---|---|
| v1 | Kompatibel mit<br>[Version 2.17.4](/help/versions.md) und vorherigen | Kompatibel | Kompatibel | Kompatibel |

Weitere Informationen zu Kernkomponentenversionen und -freigaben finden Sie im Dokument [Kernkomponentenversionen](/help/versions.md).

## Musterkomponentenausgabe {#sample-component-output}

Näheres zur PDF-Viewer-Komponente und Beispiele für zugehörige Konfigurationsoptionen sowie HTML- und JSON-Ausgaben finden Sie in der [Komponentenbibliothek](https://adobe.com/go/aem_cmp_library_pdfviewer_de).

## Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur PDF-Viewer-Komponente finden Sie auf [GitHub](https://adobe.com/go/aem_cmp_tech_pdfviewer_v1_de).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

>[!NOTE]
>
>Die PDF Viewer-Komponente nutzt die [Document Services-APIs von Adobe](https://www.adobe.io/apis/documentcloud/dcsdk.html). Ihr Administrator muss für die Verwendung dieser Services eine [kontextbezogene Konfiguration](/help/developing/context-aware-configs.md) einrichten. In der technischen Dokumentation zu der Komponente finden Sie [Einzelheiten zu dieser Konfiguration](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/pdfviewer/v1/pdfviewer#context-aware-config).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Mit dem Dialogfeld „Konfigurieren“ kann der Inhaltsautor den Viewer und sein Verhalten und Aussehen für einen Besucher der Seite definieren.

### Registerkarte „Konfiguration“ {#configuration-tab}

Auf der Registerkarte „Konfiguration“ kann der Autor festlegen, welche PDF-Datei angezeigt werden soll. Der Pfad kann als Asset in AEM oder als absoluter Pfad zu einer anderen Ressource definiert werden.

![Registerkarte „Konfiguration“ im Dialogfeld „Bearbeiten“ der PDF-Viewer-Komponente](/help/assets/pdf-viewer-edit-configuration.png)

### Registerkarte „Anpassen“ {#customize-tab}

Auf der Registerkarte „Anpassen“ kann der Autor festlegen, welche Optionen im Viewer für den Leser verfügbar sind und wie der Viewer angezeigt wird.

![Registerkarte „Anpassen“ im Dialogfeld „Bearbeiten“ der PDF-Viewer-Komponente](/help/assets/pdf-viewer-edit-customize.png)

Die Anzahl der verfügbaren Optionen hängt vom ausgewählten **Typ** ab.

* [Vollbild](#full-window) - Der Anzeigebereich wird im vollständigen Browser gerendert. Dies eignet sich am besten für Speicher- und Produktivitätsprogramme.
* [Größenangepasster Container](#sized-container) - Der Anzeigebereich wird im vollständigen Browser gerendert. Dies eignet sich am besten für Speicher- und Produktivitätsprogramme.
* [In Zeilen](#in-line) - Alle PDF-Seiten werden auf einer Web-Seite in Zeilen gerendert. Dies eignet sich am besten für Leseprogramme.

#### Vollbild {#full-window}

Der Anzeigebereich wird im vollständigen Browser gerendert. Dies eignet sich am besten für Speicher- und Produktivitätsprogramme.

![Registerkarte „Anpassen“ für die Vollbildoption im Dialogfeld „Bearbeiten“ der PDF-Viewer-Komponente](/help/assets/pdf-viewer-edit-customize-full.png)

* **Standardanzeigemodus** – Wie der Viewer in die Seite eingepasst wird, auf der er angezeigt wird
   * Seite anpassen
   * Breite anpassen
* **Vollbild** – Wenn diese Option aktiviert ist, nutzt der Viewer die volle Höhe/Breite des Viewports.
* **Anmerkungs-Tools** – Wenn diese Option aktiviert ist, stehen die Anmerkungs-Tools zur Verfügung.
* **Linkes Bedienfeld** – Wenn diese Option aktiviert ist, wird das linke Bedienfeld angezeigt.
* **PDF herunterladen** – Wenn diese Option aktiviert ist, wird die Download-Schaltfläche angezeigt.
* **PDF drucken** – Wenn diese Option aktiviert ist, wird die Druck-Schaltfläche angezeigt.
* **Seitensteuerungen** – Schaltet das Verhalten der Seitensteuerungen um.
   * Andocken
   * Abdocken

#### Größenangepasster Container {#sized-container}

Der Anzeigebereich wird im vollständigen Browser gerendert. Dies eignet sich am besten für Speicher- und Produktivitätsprogramme.

![Registerkarte „Anpassen“ für den größenangepassten Container im Dialogfeld „Bearbeiten“ der PDF-Viewer-Komponente](/help/assets/pdf-viewer-edit-customize-sized-container.png)

* **Vollbild** – Wenn diese Option aktiviert ist, nutzt der Viewer die volle Höhe/Breite des Viewports.
* **PDF herunterladen** – Wenn diese Option aktiviert ist, wird die Download-Schaltfläche angezeigt.
* **PDF drucken** – Wenn diese Option aktiviert ist, wird die Druck-Schaltfläche angezeigt.
* **Seitensteuerungen** – Schaltet das Verhalten der Seitensteuerungen um.
   * Andocken
   * Abdocken

#### Inline {#in-line}

Alle PDF-Seiten werden auf einer Web-Seite in Zeilen gerendert. Dies eignet sich am besten für Leseprogramme.

![Registerkarte „Anpassen“ für den größenangepassten Container im Dialogfeld „Bearbeiten“ der PDF-Viewer-Komponente](/help/assets/pdf-viewer-edit-customize-inline.png)

* **PDF herunterladen** – Wenn diese Option aktiviert ist, wird die Download-Schaltfläche angezeigt.
* **PDF drucken** – Wenn diese Option aktiviert ist, wird die Druck-Schaltfläche angezeigt.

## Dialogfeld „Design“ {#design-dialog}

Es gibt kein Dialogfeld „Design“ für die PDF-Viewer-Komponente.
