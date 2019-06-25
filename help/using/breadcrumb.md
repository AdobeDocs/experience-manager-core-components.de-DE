---
title: Breadcrumb-Komponente
seo-title: Breadcrumb-Komponente
description: 'null'
seo-description: Die Core Component Breadcrumb-Komponente ist eine Navigationskomponente, die eine Breadcrumb von Links basierend auf der Position der Seite in der Inhaltshierarchie erstellt.
uuid: 13 e 858 d 5-24 ad -4144-adc 4-0 fa 1 ffd 257 c 1
contentOwner: Benutzer
content-type: Referenz
topic-tags: authoring
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-new
discoiquuid: ecd 237 df -08 b 8-4 deb -9881-66 a 1 f 0 d 65 ef 3
modalsize: 426x240
translation-type: tm+mt
source-git-commit: c58826c133eb112b305fa4facbe2a81e577eb896

---


# Breadcrumb Component{#breadcrumb-component}

Die Core Component Breadcrumb-Komponente ist eine Navigationskomponente, die eine Breadcrumb von Links basierend auf der Position der Seite in der Inhaltshierarchie erstellt.

## Nutzung {#usage}

Die Breadcrumb-Komponente zeigt die Position der aktuellen Seite innerhalb der Site-Hierarchie an, wodurch Seitenbesucher von ihrer aktuellen Position aus über die Seitenhierarchie navigieren können. Dies ist oft in Seitenkopf- oder -fußzeilen integriert.

Available options, such as the default navigation level and the ability to show the current page or hidden pages, can be defined by the template author in the [design dialog](#design-dialog). The content editor can then choose if hidden pages should be shown or not and the actual navigation level for the component in the [edit dialog](#edit-dialog).

## Version and Compatibility {#version-and-compatibility}

Die aktuelle Version der Breadcrumb-Komponente ist v 2, die mit Version 2.0.0 der Kernkomponenten im Januar 2018 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v2 | Kompatibel | Kompatibel | Kompatibel |
| [v1](breadcrumb-v1.md) | Kompatibel | Kompatibel | Kompatibel |

For more information about Core Component versions and releases, see the document [Core Components Versions](versions.md).

## Sample Component Output {#sample-component-output}

To experience the Breadcrumb Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](http://opensource.adobe.com/aem-core-wcm-components/library/breadcrumb.html).

>[!NOTE]
>
>As of Core Components release 2.1.0, the Breadcrumb Component supports [schema.org microdata](https://schema.org/BreadcrumbList).

## Technical Details {#technical-details}

The latest technical documentation about the Breadcrumb Component [can be found on GitHub](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/breadcrumb/v2/breadcrumb).

Further details about developing Core Components can be found in the [Core Components developer documentation](developing.md).

## Edit Dialog {#edit-dialog}

Das Dialogfeld &quot;Bearbeiten&quot; ermöglicht dem Inhaltsautor, ausgeblendete und aktive Seiten in den Breadcrumbs sowie die Tiefe der anzuzeigenden Hierarchie zu unterdrücken.

![](assets/screen_shot_2018-01-12at124250.png)

* **Navigations-Startebene** - Wo in der Hierarchie die Breadcrumb-Komponente beginnen soll, um zur aktuellen Seite zu gelangen. Beispiel: In We. Retail:

   * 0 starts at `/content`

   * 1 starts at `/content/we-retail`
   * 2 starts at `/content/we-retail/<country>`

* **Ausgeblendete Navigationselemente** anzeigen: Zeigt Seiten an, die im Breadcrumb als ausgeblendet markiert markiert sind (standardmäßig werden sie nicht angezeigt)
* **Aktuelle Seite** ausblenden - Unterdrücken Sie die aktuelle Seite im Breadcrumb (standardmäßig wird sie angezeigt)

## Design Dialog {#design-dialog}

Das Entwurfsdialogfeld ermöglicht es dem Vorlagenautor, die Standardwerte für die Optionen festzulegen, um ausgeblendete und aktive Seiten in den Breadcrumbs sowie die Tiefe der anzuzeigenden Hierarchie zu unterdrücken.

### Main Tab {#main-tab}

![](assets/screen_shot_2018-01-12at124437.png)

* **Navigations-Startebene** : Definiert den Standardwert, für den in der Hierarchie die Breadcrumb-Komponente aufgerufen werden soll, wenn die Breadcrumb-Komponente zu einer Seite hinzugefügt wird.
* **Ausgeblendete Navigationselemente** anzeigen: Definiert den Standardwert der **Option Verborgene Navigationselemente** anzeigen, wenn der Seite die Breadcrumb-Komponente hinzugefügt wird.

   * Die Option für den Autor wird nicht aktiviert oder deaktiviert. Es wird nur der Standardwert festgelegt.

* **Aktuelle Seite** ausblenden: Definiert den Standardwert der Option **Aktuelle Seite** ausblenden, wenn die Breadcrumb-Komponente einer Seite hinzugefügt wird.

   * Die Option für den Autor wird nicht aktiviert oder deaktiviert. Es wird nur der Standardwert festgelegt.

### Styles Tab {#styles-tab}

The Breadcrumb Component supports the AEM [Style System](authoring.md#component-styling).