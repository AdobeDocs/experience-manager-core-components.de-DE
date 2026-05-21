---
title: Schaltflächenkomponente (v1)
description: Die Kernkomponente „Schaltflächenkomponente“ ermöglicht die Erstellung und Anzeige einer Schaltfläche.
role: Developer, Admin, User
exl-id: 63af16e4-dd4d-426d-88ef-769ecd1b3175
index: false
TQID: https://experienceleague.adobe.com/te1330KgXtcUKnZTKKvYr4Uf48z9RYRKcY76tZ1oenE
product_v2: id: c45915cf-e157-4af7-a80d-97b905bcb3a5id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: e2c1b6d3-bb7e-4fe8-8c72-f7b403298e91
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: cc72dcf1-72e1-48cc-b434-e7c27d62d67c
source-git-commit: 73aa5234ac63fa3be99feebce448bb6722513838
workflow-type: tm+mt
source-wordcount: 408
ht-degree: 100%

---

# Schaltflächenkomponente (v1) {#button-component}

Die Kernkomponente „Schaltflächenkomponente“ ermöglicht die Erstellung und Anzeige eines Schaltflächen-Elements auf einer Seite.

## Nutzung {#usage}

Die Kernkomponente „Schaltflächenkomponente“ ermöglicht die Integration einer Schaltfläche in eine Seite.

* Die Eigenschaften der Schaltfläche können im [Dialogfeld „Konfigurieren“](#configure-dialog) ausgewählt werden.
* Stile für die Schaltflächenkomponente können im [Dialogfeld „Design“](#design-dialog) definiert werden.

## Version und Kompatibilität {#version-and-compatibility}

In diesem Dokument wird die v1 der Schaltflächenkomponente beschrieben, die mit Version 2.5.0 der Kernkomponenten im Juni 2019 eingeführt wurde.

>[!CAUTION]
>
>In diesem Dokument wird die v1 der Schaltflächenkomponente beschrieben.
>
>Weitere Informationen zur aktuellen Version der Schaltflächenkomponente finden Sie im Dokument [Schaltflächenkomponente](/help/components/button.md).

## Musterkomponentenausgabe {#sample-component-output}

Um die Schaltflächen-Komponente sowie Beispiele für die Konfigurationsoptionen sowie HTML- und JSON-Ausgaben zu erhalten, besuchen Sie die [Komponentenbibliothek](https://adobe.com/go/aem_cmp_library_button).

## Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur Schaltflächenkomponente [finden Sie auf GitHub](https://adobe.com/go/aem_cmp_tech_button_v1).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Mit dem Dialogfeld „Konfigurieren“ kann der Inhaltsautor die Schaltfläche und ihr Verhalten und Aussehen für einen Besucher der Seite definieren.

### Registerkarte „Eigenschaften“ {#properties-tab}

![Registerkarte „Eigenschaften“ im Dialogfeld „Design“ der Schaltflächenkomponente](/help/assets/button-edit-properties.png)

* **Text** – Der Text, der auf der Schaltfläche angezeigt werden soll
* **Verknüpfung** - Link zu einer Inhaltsseite in AEM, einer externen Ressource oder einem Anker
   * Wählen Sie im Dialogfeld **Auswahl** einen Pfad in AEM aus.
* **Symbol** – Bezeichner für die Anzeige eines Symbols auf der Schaltfläche
* **ID** – Diese Option dient zur Kontrolle der eindeutigen Kennung der Komponente in der HTML-Datei und auf der [Datenschicht](/help/developing/data-layer/overview.md).
   * Wenn Sie das Feld leer lassen, wird automatisch eine eindeutige ID generiert, die Sie über die resultierende Seite finden.
   * Sofern eine ID angegeben wird, ist vom Autor bzw. der Autorin sicherzustellen, dass diese eindeutig ist.
   * Änderungen der ID können sich auf das CSS-, JS- und Datenschicht-Tracking auswirken.

### Registerkarte „Erreichbarkeit“ {#accessibility-tab}

![Registerkarte „Erreichbarkeit“ im Dialogfeld „Bearbeiten“ der Schaltflächenkomponente](/help/assets/button-edit-accessibility.png)

Auf der Registerkarte **Erreichbarkeit** können Werte für die [ARIA-Barrierefreiheits-Beschriftungen](https://www.w3.org/WAI/standards-guidelines/aria/) für die Komponente festgelegt werden.

* **Beschriftung** - Wert eines ARIA-Beschriftungs-Attributs für die Komponente

## Dialogfeld „Design“ {#design-dialog}

### Registerkarte „Arten“ {#styles-tab}

Die Schaltflächenkomponente unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).

## Adobe Client-Datenschicht {#data-layer}

Die Schaltflächenkomponente unterstützt die [Adobe Client-Datenschicht](/help/developing/data-layer/overview.md).
