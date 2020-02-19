---
title: Schaltflächenkomponente
description: Die Kernkomponente „Schaltflächenkomponente“ ermöglicht die Erstellung und Anzeige einer Schaltfläche.
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# Schaltflächenkomponente{#button-component}

Die Kernkomponente „Schaltflächenkomponente“ ermöglicht die Erstellung und Anzeige eines Schaltflächen-Elements auf einer Seite.

## Nutzung {#usage}

Die Kernkomponente „Schaltflächenkomponente“ ermöglicht die Integration einer Schaltfläche in eine Seite.

* Die Eigenschaften der Schaltfläche können im [Dialogfeld „Konfigurieren“](#configure-dialog) ausgewählt werden.
* Stile für die Schaltflächenkomponente können im [Dialogfeld „Design“](#design-dialog) definiert werden.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Schaltflächenkomponente ist v1, die mit Version 2.5.0 der Kernkomponenten im Juni 2019 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.3 | AEM 6.4 | AEM 6.5 | AEM als Cloud Service |
|--- |--- |--- |---|---|
| v1 | Kompatibel | Kompatibel | Kompatibel | Kompatibel |

Weitere Informationen zu Kernkomponentenversionen und -freigaben finden Sie in den [Kernkomponentenversionen](/help/versions.md).

## Musterkomponentenausgabe {#sample-component-output}

Um die Schaltflächen-Komponente sowie Beispiele für die Konfigurationsoptionen sowie HTML- und JSON-Ausgaben zu erhalten, besuchen Sie die [Komponentenbibliothek](https://adobe.com/go/aem_cmp_library_button).

## Technische Details {#technical-details}

The latest technical documentation about the Button Component [can be found on GitHub](https://adobe.com/go/aem_cmp_tech_button_v1).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Mit dem Dialogfeld „Konfigurieren“ kann der Inhaltsautor die Schaltfläche und ihr Verhalten und Aussehen für einen Besucher der Seite definieren.

### Registerkarte „Eigenschaften“ {#properties-tab}

![](/help/assets/screen-shot-2019-08-29-12.19.32.png)

* **Text** - Der Text, der auf der Schaltfläche angezeigt werden soll
* **Link** - Link zu einer Inhaltsseite in AEM, einer externen Ressource oder einem Anker
   * Wählen Sie im Dialogfeld **Auswahl** einen Pfad in AEM aus.
* **Symbol** - Bezeichner für die Anzeige eines Symbols auf der Schaltfläche

### Registerkarte „Barrierefreiheit“ {#accessibility-tab}

![](/help/assets/screen-shot-2019-08-29-12.19.43.png)

Auf der Registerkarte **Barrierefreiheit** können Werte für die [ARIA-Barrierefreiheits-Bezeichungen](https://www.w3.org/WAI/standards-guidelines/aria/) für die Komponente festgelegt werden.

* **Bezeichnung** - Wert eines ARIA-Bezeichnungs-Attributs für die Komponente

## Dialogfeld „Design“ {#design-dialog}

### Registerkarte „Stile“ {#styles-tab}

Die Bildkomponente unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).
