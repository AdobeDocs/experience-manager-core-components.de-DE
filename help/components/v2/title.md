---
title: Titelkomponente (v2)
description: Die Kernkomponente „Titelkomponente“ ist eine Komponente für Abschnittsüberschriften, die eine Bearbeitung im Kontext ermöglicht.
role: Architect, Developer, Admin, User
exl-id: f853ec46-19fd-4569-a9d3-5c376d2a2101
source-git-commit: e291d4c1bfd37292d68c236178f9681c4e5ee741
workflow-type: tm+mt
source-wordcount: '521'
ht-degree: 100%

---

# Titelkomponente (v2) {#title-component}

Die Kernkomponente „Titelkomponente“ ist eine Komponente für Abschnittsüberschriften, die eine Bearbeitung im Kontext ermöglicht.

## Nutzung {#usage}

Die Titelkomponente soll als Titel oder Überschrift eines Inhaltsabschnitts verwendet werden. Die verfügbaren Überschriftenebenen können vom Vorlagenautor im [Dialogfeld „Design“](#design-dialog) definiert werden. Der Inhaltseditor kann aus verfügbaren Überschriftenebenen im [Dialogfeld „Bearbeiten“](#edit-dialog) auswählen. Für zusätzlichen Komfort steht auch eine einfache direkte Bearbeitung des Überschriftentexts zur Verfügung.

## Version und Kompatibilität {#version-and-compatibility}

In diesem Dokument wird die v2 der Titelkomponente beschrieben, die ursprünglich mit Version 2.0.0 der Kernkomponenten im Januar 2018 eingeführt wurde.

>[!CAUTION]
>
>In diesem Dokument wird die v2 der Titelkomponente beschrieben.
>
>Weitere Informationen zur aktuellen Version der Titelkomponente finden Sie im Dokument [Titelkomponente](/help/components/title.md).

## Musterkomponentenausgabe {#sample-component-output}

Um die Titelkomponente sowie Beispiele für die Konfigurationsoptionen sowie HTML- und JSON-Ausgaben zu erhalten, besuchen Sie die [Komponentenbibliothek](https://adobe.com/go/aem_cmp_library_title_de).

### Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur Titelkomponente [finden Sie auf GitHub](https://adobe.com/go/aem_cmp_tech_title_v2_de).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Dialogfeld „Bearbeiten“ {#edit-dialog}

Im Dialogfeld „Bearbeiten“ kann der Inhaltsautor den Titeltext definieren sowie die Überschriftenebene auswählen.

* **Titel** - Wenn leer, wird der Seitentitel verwendet
* **Typ/Größe** - Definiert die Überschriftenebene des Titels
* **Verknüpfung** - Definiert den Inhalt, auf den der Titel verweist. Dies kann ein Pfad zu einer Inhaltsseite, eine externe URL oder ein Seitenanker sein.
* **ID** - Diese Option dient zur Kontrolle der eindeutigen Kennung der Komponente in der HTML-Datei und auf der [Datenschicht](/help/developing/data-layer/overview.md).
   * Wenn Sie das Feld leer lassen, wird automatisch eine eindeutige ID generiert, die Sie über die resultierende Seite finden.
   * Sofern eine ID angegeben wird, ist vom Autor bzw. der Autorin sicherzustellen, dass diese eindeutig ist.
   * Änderungen der ID können sich auf das CSS-, JS- und Datenschicht-Tracking auswirken.

![Dialogfeld „Bearbeiten“ der Titelkomponente](/help/assets/title-edit.png)

>[!NOTE]
>
>Die Möglichkeit, einen Link für den Titel zu definieren, wurde mit Version 2.2.0 der Kernkomponenten eingeführt.

Der Editor für die Bearbeitung im Kontext kann auch verwendet werden, um den Text der Titelkomponente zu bearbeiten.

![In-Kontext-Bearbeitung der Titelkomponente](/help/assets/title-edit-inline.png)

## Dialogfeld „Design“ {#design-dialog}

Das Dialogfeld „Design“ ermöglicht es dem Vorlagenautor, die standardmäßige Überschriftenebene zu definieren, die Titelkomponenten bei der Erstellung durch Inhaltsautoren haben.

### Registerkarte „Größen“ {#sizes-tab}

![Dialogfeld „Design“ der Titelkomponente](/help/assets/title-design.png)

* **Zulässige Typen/Größen für Autoren** - Aktiviert oder deaktiviert die Überschrifttypen, die für Inhaltsautoren verfügbar sind, wenn sie die Titelkomponente verwenden.
* **Standardtyp/Größe** - Definieren Sie den Überschrifttyp, der automatisch zugewiesen wird, wenn ein Inhaltsautor die Titelkomponente zu einer Seite hinzufügt.
* **Link deaktivieren** - Deaktiviert die Unterstützung für Links in der Titelkomponente, um Inhaltsautoren zu verbieten, von Titeln zu verlinken.

>[!NOTE]
>
>Die Möglichkeit, einen Link für den Titel zu definieren, wurde mit Version 2.2.0 der Kernkomponenten eingeführt.

### Registerkarte „Arten“ {#styles-tab}

Die Titelkomponente unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).

## Adobe Client-Datenschicht {#data-layer}

Die Titelkomponente unterstützt die [Adobe Client-Datenschicht](/help/developing/data-layer/overview.md).
