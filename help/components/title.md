---
title: Titelkomponente
description: Die Kernkomponente „Titelkomponente“ ist eine Komponente für Abschnittsüberschriften, die eine Bearbeitung im Kontext ermöglicht.
role: Architect, Developer, Admin, User
exl-id: 393af72c-549f-4609-afb0-2712f827b549
source-git-commit: 327c239b02e0aecee878784c918bfa98d960530e
workflow-type: tm+mt
source-wordcount: '619'
ht-degree: 100%

---

# Titelkomponente{#title-component}

Die Kernkomponente „Titelkomponente“ ist eine Komponente für Abschnittsüberschriften, die eine Bearbeitung im Kontext ermöglicht.

## Nutzung {#usage}

Die Titelkomponente soll als Titel oder Überschrift eines Inhaltsabschnitts verwendet werden. Die verfügbaren Überschriftenebenen können vom Vorlagenautor im [Dialogfeld „Design“](#design-dialog) definiert werden. Der Inhaltseditor kann aus verfügbaren Überschriftenebenen im [Dialogfeld „Bearbeiten“](#edit-dialog) auswählen. Für zusätzlichen Komfort steht auch eine einfache direkte Bearbeitung des Überschriftentexts zur Verfügung.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Titelkomponente ist v3, die mit Version 2.18.0 der Kernkomponenten im Februar 2022 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|---|
| v3 | - | Kompatibel | Kompatibel |
| [v2](v2/title.md) | Kompatibel | Kompatibel | Kompatibel |
| [v1](v1/title-v1.md) | Kompatibel | Kompatibel | Kompatibel |

Weitere Informationen zu Kernkomponentenversionen und -freigaben finden Sie im Dokument [Kernkomponentenversionen](/help/versions.md).

## Musterkomponentenausgabe {#sample-component-output}

Um die Titelkomponente sowie Beispiele für die Konfigurationsoptionen sowie HTML- und JSON-Ausgaben zu erhalten, besuchen Sie die [Komponentenbibliothek](https://adobe.com/go/aem_cmp_library_title_de).

### Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur Titelkomponente [finden Sie auf GitHub](https://adobe.com/go/aem_cmp_tech_title_v3_de).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Dialogfeld „Bearbeiten“ {#edit-dialog}

Im Dialogfeld „Bearbeiten“ kann der Inhaltsautor den Titeltext definieren sowie die Überschriftenebene auswählen.

* **Titel** - Wenn leer, wird der Seitentitel verwendet
* **Typ/Größe** - Definiert die Überschriftenebene des Titels
* **Verknüpfung** - Definiert den Inhalt, auf den der Titel verweist. Dies kann ein Pfad zu einer Inhaltsseite, eine externe URL oder ein Seitenanker sein.
* **Link auf neuer Registerkarte öffnen** – Wenn diese Option aktiviert ist, wird der Link auf einer neuen Browser-Registerkarte geöffnet.
* **ID** - Diese Option dient zur Kontrolle der eindeutigen Kennung der Komponente in der HTML-Datei und auf der [Datenschicht](/help/developing/data-layer/overview.md).
   * Wenn Sie das Feld leer lassen, wird automatisch eine eindeutige ID generiert, die Sie über die resultierende Seite finden.
   * Sofern eine ID angegeben wird, ist vom Autor bzw. der Autorin sicherzustellen, dass diese eindeutig ist.
   * Änderungen der ID können sich auf das CSS-, JS- und Datenschicht-Tracking auswirken.

![Dialogfeld „Bearbeiten“ der Titelkomponente](/help/assets/title-edit.png)

Der Editor für die Bearbeitung im Kontext kann auch verwendet werden, um den Text der Titelkomponente zu bearbeiten.

![In-Kontext-Bearbeitung der Titelkomponente](/help/assets/title-edit-inline.png)

### Registerkarte „Arten“ {#styles-tab-edit}

Die Titelkomponente unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).

Verwenden Sie das Dropdown-Menü, um die Stile auszuwählen, die Sie auf die Komponente anwenden möchten. Die im Dialogfeld „Bearbeiten“ vorgenommenen Auswahlen haben denselben Effekt wie die in der Komponenten-Symbolleiste ausgewählten.

Stile müssen für diese Komponente im [Dialogfeld „Design“](#design-dialog) konfiguriert werden, damit das Dropdown-Menü verfügbar ist.

![Registerkarte „Arten“ im Dialogfeld „Bearbeiten“ der Titelkomponente](/help/assets/title-edit-styles.png)

## Dialogfeld „Design“ {#design-dialog}

Das Dialogfeld „Design“ ermöglicht es dem Vorlagenautor, die standardmäßige Überschriftenebene zu definieren, die Titelkomponenten bei der Erstellung durch Inhaltsautoren haben.

### Registerkarte „Größen“ {#sizes-tab}

![Dialogfeld „Design“ der Titelkomponente](/help/assets/title-design.png)

* **Zulässige Typen/Größen für Autoren** - Aktiviert oder deaktiviert die Überschrifttypen, die für Inhaltsautoren verfügbar sind, wenn sie die Titelkomponente verwenden.
* **Standardtyp/Größe** - Definieren Sie den Überschrifttyp, der automatisch zugewiesen wird, wenn ein Inhaltsautor die Titelkomponente zu einer Seite hinzufügt.
* **Link deaktivieren** - Deaktiviert die Unterstützung für Links in der Titelkomponente, um Inhaltsautoren zu verbieten, von Titeln zu verlinken.

### Registerkarte „Arten“ {#styles-tab}

Die Titelkomponente unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).

## Adobe Client-Datenschicht {#data-layer}

Die Titelkomponente unterstützt die [Adobe Client-Datenschicht](/help/developing/data-layer/overview.md).
