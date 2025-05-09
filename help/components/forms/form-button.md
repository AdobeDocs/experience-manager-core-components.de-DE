---
title: Formularschaltflächen-Komponente
description: Die Kernkomponente „Komponente für ausgeblendetes Formular“ ermöglicht die Einbeziehung eines ausgeblendeten Felds in ein Formular.
role: Architect, Developer, Admin, User
exl-id: 1e5cff43-57db-4bfc-b2d2-23307eaf5eb3
source-git-commit: 6fbc781db555bc6abaed1d122a9a8756e3d53222
workflow-type: ht
source-wordcount: '413'
ht-degree: 100%

---

# Formularschaltflächen-Komponente {#form-button-component}

Die Kernkomponente „Formularschaltflächen-Komponente“ ermöglicht die Einbeziehung einer Schaltfläche zum Auslösen einer Aktion auf einer Seite.

## Nutzung {#usage}

Die Kernkomponente „Formularschaltflächen-Komponente“ ermöglicht die Erstellung von Schaltflächenfeldern, die häufig dazu dienen, die Übermittlung des Formulars auszulösen, und zusammen mit der [Formular-Container-Komponente](form-container.md). verwendet werden sollen

Die Schaltflächeneigenschaften können vom Inhaltseditor im [Dialogfeld „Konfigurieren“](#configure-dialog) definiert werden.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Formularschaltflächenkomponente ist v2, die mit Version 2.0.0 der Kernkomponenten im Januar 2018 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |--- |---|---|
| v2 | Kompatibel mit<br>[Version 2.17.4](/help/versions.md) und vorherigen | Kompatibel | Kompatibel | Kompatibel |
| [v1](/help/components/v1/form-button-v1.md) | Kompatibel | Kompatibel | – | Kompatibel |

Weitere Informationen zu Kernkomponentenversionen und -freigaben finden Sie im Dokument [Kernkomponentenversionen](/help/versions.md).

## Musterkomponentenausgabe {#sample-component-output}

Um die Formularschaltflächen-Komponente kennenzulernen und Beispiele für die Konfigurationsoptionen sowie HTML- und JSON-Ausgaben anzuzeigen, besuchen Sie die [Komponentenbibliothek](https://adobe.com/go/aem_cmp_library_form_button_de).

### Technische Details {#technical-details}

Die neueste technische Dokumentation zur Formularschaltflächen-Komponente [finden Sie auf GitHub](https://adobe.com/go/aem_cmp_tech_form_button_v2_de).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Über das Dialogfeld „Konfigurieren“ kann der Inhaltsautor die Parameter der Schaltfläche definieren.

### Registerkarte „Eigenschaften“ {#properties-tab}

![Dialogfeld „Bearbeiten“ der Formularschaltflächen-Komponente](/help/assets/form-button-edit.png)

* **Typ**

   * **Schaltfläche**
   * **Absenden**

* **Titel** - Der auf der Schaltfläche angezeigte Text

   * Wenn kein Wert angegeben ist, erscheint standardmäßig der Schaltflächentyp

* **Name** - Der Name der Schaltfläche, der mit den Formulardaten übermittelt wird.
* **Wert** - Der Wert der Schaltfläche, der mit den Formulardaten übermittelt wird.

* **ID** – Diese Option dient zur Kontrolle der eindeutigen Kennung der Komponente in der HTML-Datei und auf der [Datenschicht](/help/developing/data-layer/overview.md).
   * Wenn Sie das Feld leer lassen, wird automatisch eine eindeutige ID generiert, die Sie über die resultierende Seite finden.
   * Sofern eine ID angegeben wird, ist vom Autor bzw. der Autorin sicherzustellen, dass diese eindeutig ist.
   * Änderungen der ID können sich auf das CSS-, JS- und Datenschicht-Tracking auswirken.

## Dialogfeld „Design“ {#design-dialog}

### Registerkarte „Arten“ {#styles-tab}

Die Formularschaltflächen-Komponente unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).
