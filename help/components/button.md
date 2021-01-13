---
title: Schaltflächenkomponente
description: Die Kernkomponente „Schaltflächenkomponente“ ermöglicht die Erstellung und Anzeige einer Schaltfläche.
translation-type: ht
source-git-commit: df42f9e3fa26cbb26aa44688e26e5c9a7de4752e
workflow-type: ht
source-wordcount: '438'
ht-degree: 100%

---


# Schaltflächenkomponente {#button-component}

Die Kernkomponente „Schaltflächenkomponente“ ermöglicht die Erstellung und Anzeige eines Schaltflächen-Elements auf einer Seite.

## Verwendung {#usage}

Die Kernkomponente „Schaltflächenkomponente“ ermöglicht die Integration einer Schaltfläche in eine Seite.

* Die Eigenschaften der Schaltfläche können im [Dialogfeld „Konfigurieren“](#configure-dialog) ausgewählt werden.
* Stile für die Schaltflächenkomponente können im [Dialogfeld „Design“](#design-dialog) definiert werden.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Schaltflächenkomponente ist v1, die mit Version 2.5.0 der Kernkomponenten im Juni 2019 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Kompatibel | Kompatibel | Kompatibel |

Weitere Informationen zu Kernkomponentenversionen und -freigaben finden Sie in den [Kernkomponentenversionen](/help/versions.md).

## Musterkomponentenausgabe {#sample-component-output}

Um die Schaltflächen-Komponente sowie Beispiele für die Konfigurationsoptionen sowie HTML- und JSON-Ausgaben zu erhalten, besuchen Sie die [Komponentenbibliothek](https://adobe.com/go/aem_cmp_library_button).

## Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur Schaltflächenkomponente [finden Sie auf GitHub](https://adobe.com/go/aem_cmp_tech_button_v1).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Mit dem Dialogfeld „Konfigurieren“ kann der Inhaltsautor die Schaltfläche und ihr Verhalten und Aussehen für einen Besucher der Seite definieren.

### Registerkarte „Eigenschaften“ {#properties-tab}

![Registerkarte „Eigenschaften“ im Dialogfeld „Design“ der Schaltflächenkomponente](/help/assets/button-edit-properties.png)

* **Text** - Der Text, der auf der Schaltfläche angezeigt werden soll
* **Link** - Link zu einer Inhaltsseite in AEM, einer externen Ressource oder einem Anker
   * Wählen Sie im Dialogfeld **Auswahl** einen Pfad in AEM aus.
* **Symbol** - Bezeichner für die Anzeige eines Symbols auf der Schaltfläche
* **ID** – Diese Option dient zur Kontrolle der eindeutigen Kennung der Komponente in der HTML-Datei und auf der [Datenschicht](/help/developing/data-layer/overview.md).
   * Wenn Sie das Feld leer lassen, wird automatisch eine eindeutige ID generiert, die Sie über die resultierende Seite finden.
   * Sofern eine ID angegeben wird, ist vom Autor sicherzustellen, dass diese eindeutig ist.
   * Änderungen der ID können sich auf das CSS-, JS- und Datenschicht-Tracking auswirken.

### Registerkarte „Erreichbarkeit“ {#accessibility-tab}

![Registerkarte „Erreichbarkeit“ im Dialogfeld „Bearbeiten“ der Schaltflächenkomponente](/help/assets/button-edit-accessibility.png)

Auf der Registerkarte **Erreichbarkeit** können Werte für die [ARIA-Erreichbarkeits-Beschriftungen](https://www.w3.org/WAI/standards-guidelines/aria/) für die Komponente festgelegt werden.

* **Beschriftung** - Wert eines ARIA-Beschriftungs-Attributs für die Komponente

## Dialogfeld „Design“ {#design-dialog}

### Registerkarte „Stile“ {#styles-tab}

Die Schaltflächenkomponente unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).
