---
title: Breadcrumb-Komponente (v2)
description: Die Kernkomponente „Breadcrumb-Komponente“ ist eine Navigationskomponente, die einen Breadcrumb von Links basierend auf der Position der Seite in der Inhaltshierarchie erstellt.
role: Architect, Developer, Admin, User
exl-id: 5f2e6fef-e2f6-48e2-8dac-008db3131044
index: n
source-git-commit: 92a3ec273a5be6751c1503835b9c2e5cbd61bb9e
workflow-type: ht
source-wordcount: '0'
ht-degree: 100%

---


# Breadcrumb-Komponente (v2) {#breadcrumb-component}

Die Kernkomponente „Breadcrumb-Komponente“ ist eine Navigationskomponente, die einen Breadcrumb von Links basierend auf der Position der Seite in der Inhaltshierarchie erstellt.

## Nutzung {#usage}

Die Breadcrumb-Komponente zeigt die Position der aktuellen Seite innerhalb der Site-Hierarchie an, wodurch Seitenbesucher von ihrer aktuellen Position aus durch die Seitenhierarchie navigieren können. Dies ist oft in Kopf- oder Fußzeilen von Seiten integriert.

Verfügbare Optionen wie die Standardnavigationsstufe und die Möglichkeit, die aktuelle Seite oder ausgeblendete Seiten anzuzeigen, können vom Vorlagenautor im [Dialogfeld „Design“](#design-dialog) definiert werden. Der Inhaltseditor kann dann festlegen, ob ausgeblendete Seiten angezeigt werden sollen oder nicht, und er kann die tatsächliche Navigationsstufe für die Komponente im [Dialogfeld „Bearbeiten“](#edit-dialog) wählen.

## Version und Kompatibilität {#version-and-compatibility}

In diesem Dokument wird die v2 der Breadcrumb-Komponente beschrieben, die ursprünglich mit Version 2.0.0 der Kernkomponenten im Januar 2018 eingeführt wurde.

>[!CAUTION]
>
>In diesem Dokument wird die v2 der Breadcrumb-Komponente beschrieben.
>
>Weitere Informationen zur aktuellen Version der Breadcrumb-Komponente finden Sie im Dokument [Breadcrumb-Komponente](/help/components/breadcrumb.md).

## Musterkomponentenausgabe {#sample-component-output}

Um die Breadcrumb-Komponente und Beispiele für die Konfigurationsoptionen sowie HTML- und JSON-Ausgaben zu erhalten, besuchen Sie die [Komponentenbibliothek](https://adobe.com/go/aem_cmp_library_breadcrumb_de).

>[!NOTE]
>
>Ab Version 2.1.0 der Kernkomponenten unterstützt die Breadcrumb-Komponente [schema.org-Mikrodaten](https://schema.org/BreadcrumbList).

## Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur Breadcrumb-Komponente [finden Sie auf GitHub](https://adobe.com/go/aem_cmp_tech_breadcrumb_v2_de).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Dialogfeld „Bearbeiten“ {#edit-dialog}

Das Dialogfeld „Bearbeiten“ ermöglicht es dem Inhaltsautor, ausgeblendete und aktive Seiten in den Breadcrumbs zu unterdrücken sowie die Tiefe der anzuzeigenden Hierarchie zu wählen.

![Dialogfeld „Bearbeiten“ der Breadcrumb-Komponente](/help/assets/breadcrumb-edit.png)

* **Startebene für die Navigation** - Wo in der Hierarchie die Breadcrumb-Komponente beginnen soll, um zur aktuellen Seite zu gelangen. Beispiel:

   * 0 beginnt bei `/content`
   * 1 beginnt bei `/content/<yourSite>`
   * 2 beginnt bei `/content/<yourSite>/<country>`

* **Verborgene Navigationselemente anzeigen** - Zeigt Seiten an, die im Breadcrumb als ausgeblendet markiert sind (standardmäßig werden sie nicht angezeigt)
* **Aktuelle Seite ausblenden** - Unterdrücken der aktuellen Seite im Breadcrumb (standardmäßig wird sie angezeigt)
* **Schatten deaktivieren** - Wenn es sich bei der Seite in der Hierarchie um einen Redirect handelt, wird anstelle der Zielseite der Name der umleitenden (Redirect)-Seite angezeigt. Weitere Informationen finden Sie unter [Unterstützung für Shadow Site-Struktur](../v1/navigation.md#shadow-structure) der Navigationskomponente.
* **ID** - Diese Option dient zur Kontrolle der eindeutigen Kennung der Komponente in der HTML-Datei und auf der [Datenschicht](/help/developing/data-layer/overview.md).
   * Wenn Sie das Feld leer lassen, wird automatisch eine eindeutige ID generiert, die Sie über die resultierende Seite finden.
   * Sofern eine ID angegeben wird, ist vom Autor bzw. der Autorin sicherzustellen, dass diese eindeutig ist.
   * Änderungen der ID können sich auf das CSS-, JS- und Datenschicht-Tracking auswirken.

## Dialogfeld „Design“ {#design-dialog}

Das Dialogfeld „Design“ ermöglicht es dem Vorlagenautor, die Standardwerte für die Optionen festzulegen, um ausgeblendete und aktive Seiten in den Breadcrumbs zu unterdrücken, sowie die Tiefe der anzuzeigenden Hierarchie zu definieren.

### Registerkarte „Allgemein“ {#main-tab}

![](/help/assets/breadcrumb-design.png)

* **Startebene für die Navigation** - Definiert den Standardwert, für den in der Hierarchie die Breadcrumb-Komponente aufgerufen werden soll, wenn die Breadcrumb-Komponente zu einer Seite hinzugefügt wird.
* **Verborgene Navigationselemente anzeigen** - Definiert den Standardwert der Option **Verborgene Navigationselemente anzeigen**, wenn der Seite die Breadcrumb-Komponente hinzugefügt wird.

   * Die Option für den Autor wird dadurch nicht aktiviert oder deaktiviert. Es wird nur der Standardwert festgelegt.

* **Aktuelle Seite ausblenden** - Definiert den Standardwert der Option **Aktuelle Seite ausblenden**, wenn die Breadcrumb-Komponente einer Seite hinzugefügt wird.

   * Die Option für den Autor wird dadurch nicht aktiviert oder deaktiviert. Es wird nur der Standardwert festgelegt.

* **Schatten deaktivieren** - Definiert den Standardwert der Option **Schatten deaktivieren**, wenn die Breadcrumb-Komponente einer Seite hinzugefügt wird.

### Registerkarte „Arten“ {#styles-tab}

Die Breadcrumb-Komponente unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).

## Adobe Client-Datenschicht {#data-layer}

Die Breadcrumb-Komponente unterstützt die [Adobe Client-Datenschicht](/help/developing/data-layer/overview.md).
