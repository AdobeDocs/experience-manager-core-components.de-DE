---
title: Formularschaltflächen-Komponente
description: Die Kernkomponente „Komponente für ausgeblendetes Formular“ ermöglicht die Einbeziehung eines ausgeblendeten Felds in ein Formular.
translation-type: tm+mt
source-git-commit: 95c0621f5423bfa515fe5e8b693e127ea56b4ae0

---


# Formularschaltflächen-Komponente {#form-button-component}

Die Kernkomponente „Formularschaltflächen-Komponente“ ermöglicht die Einbeziehung einer Schaltfläche zum Auslösen einer Aktion auf einer Seite.

## Nutzung {#usage}

Die Kernkomponente „Formularschaltflächen-Komponente“ ermöglicht die Erstellung von Schaltflächenfeldern, die häufig dazu dienen, die Übermittlung des Formulars auszulösen, und zusammen mit der [Formularcontainer-Komponente](form-container.md). verwendet werden sollen

Die Schaltflächeneigenschaften können vom Inhaltseditor im [Dialogfeld „Konfigurieren“](#configure-dialog) definiert werden.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Formularschaltflächenkomponente ist v2, die mit Version 2.0.0 der Kernkomponenten im Januar 2018 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.3 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |--- |---|
| v2 | Kompatibel | Kompatibel | Kompatibel | Kompatibel |
| [v1](/help/components/v1/form-button-v1.md) | Kompatibel | Kompatibel | Kompatibel | - |

Weitere Informationen zu Kernkomponentenversionen und -freigaben finden Sie in den [Kernkomponentenversionen](/help/versions.md).

## Musterkomponentenausgabe {#sample-component-output}

To experience the Form Button Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_form_button).

### Technische Details {#technical-details}

Die neueste technische Dokumentation zur Formularschaltflächen-Komponente [finden Sie auf GitHub](https://adobe.com/go/aem_cmp_tech_form_button_v2).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Über das Dialogfeld „Konfigurieren“ kann der Inhaltsautor die Parameter der Schaltfläche definieren.

### Registerkarte „Eigenschaften“{#properties-tab}

![](/help/assets/screen_shot_2018-01-12at120433.png)

* **Typ**

   * **Schaltfläche**
   * **Absenden**

* **Titel** - Der auf der Schaltfläche angezeigte Text

   * Wenn kein Wert angegeben ist, erscheint standardmäßig der Schaltflächentyp

* **Name** - Der Name der Schaltfläche, der mit den Formulardaten übermittelt wird.
* **Wert** - Der Wert der Schaltfläche, der mit den Formulardaten übermittelt wird.

## Dialogfeld „Design“ {#design-dialog}

### Registerkarte „Stile“ {#styles-tab}

Die Formularschaltflächen-Komponente unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).
