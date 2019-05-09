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
source-git-commit: 1bbec9b1f109df88964dce051a58d111bf6cafaa

---


# Breadcrumb-Komponente{#breadcrumb-component}

Die Core Component Breadcrumb-Komponente ist eine Navigationskomponente, die eine Breadcrumb von Links basierend auf der Position der Seite in der Inhaltshierarchie erstellt.

## Nutzung {#usage}

Die Breadcrumb-Komponente zeigt die Position der aktuellen Seite innerhalb der Site-Hierarchie an, wodurch Seitenbesucher von ihrer aktuellen Position aus über die Seitenhierarchie navigieren können. Dies ist oft in Seitenkopf- oder -fußzeilen integriert.

Verfügbare Optionen wie die standardnavigationsstufe und die Möglichkeit, die aktuelle Seite oder ausgeblendete Seiten anzuzeigen, können vom Vorlagenautor im [Designdialogfeld definiert](#design-dialog)werden. Der Content-Editor kann dann festlegen, ob ausgeblendete Seiten angezeigt werden sollen oder nicht, und die tatsächliche Navigationsstufe für die Komponente im [Dialogfeld &quot;Bearbeiten](#edit-dialog)«wird angezeigt.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Breadcrumb-Komponente ist v 2, die mit Version 2.0.0 der Kernkomponenten im Januar 2018 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v2 | Kompatibel | Kompatibel | Kompatibel |
| [v1](breadcrumb-v1.md) | Kompatibel | Kompatibel | Kompatibel |

Weitere Informationen zu Core-Komponentenversionen und -versionen finden Sie in den Core [-Komponentenversionen](versions.md).

## Musterkomponentenausgabe {#sample-component-output}

Nachfolgend finden Sie ein Beispiel aus [We. Retail](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html).

### Screenshot {#screenshot}

![](assets/chlimage_1.png)

### HTML {#html}

```
<nav class="cmp-breadcrumb">
    <ol class="cmp-breadcrumb__list">
        <li class="cmp-breadcrumb__item">
            <a href="/content/we-retail/us.html" class="cmp-breadcrumb__item-link">
                United States
            </a>
        </li>
    
        <li class="cmp-breadcrumb__item">
            <a href="/content/we-retail/us/en.html" class="cmp-breadcrumb__item-link">
                English
            </a>
        </li>
    
        <li class="cmp-breadcrumb__item cmp-breadcrumb__item--active">
            
                Experience
            
        </li>
    </ol>
</nav>
```

### JSON {#json}

```
"breadcrumb":{  
                     "columnClassNames":"aem-GridColumn aem-GridColumn--default--12",
                     "items":[  
                        {  
                           "page":{  
                              "path":"/content/we-retail/us",
                              "pageTitle":null,
                              "name":"us",
                              "description":null,
                              "title":"United States"
                           },
                           "active":false
                        },
                        {  
                           "page":{  
                              "path":"/content/we-retail/us/en",
                              "pageTitle":null,
                              "name":"en",
                              "description":null,
                              "title":"English"
                           },
                           "active":false
                        },
                        {  
                           "page":{  
                              "path":"/content/we-retail/us/en/experience",
                              "pageTitle":null,
                              "name":"experience",
                              "description":null,
                              "title":"Experience"
                           },
                           "active":true
                        }
                     ],
                     ":type":"weretail/components/content/breadcrumb"
                  }
```

>[!NOTE]
>
>Ab Version 2.1.0 von Core Components unterstützt die Breadcrumb-Komponente [schema.org Microdata](https://schema.org/BreadcrumbList).

### Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur Breadcrumb-Komponente [finden Sie unter github](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/breadcrumb/v2/breadcrumb).

Weitere Informationen zur Entwicklung Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Komponenten](developing.md).

## Dialogfeld bearbeiten {#edit-dialog}

Das Dialogfeld &quot;Bearbeiten&quot; ermöglicht dem Inhaltsautor, ausgeblendete und aktive Seiten in den Breadcrumbs sowie die Tiefe der anzuzeigenden Hierarchie zu unterdrücken.

![](assets/screen_shot_2018-01-12at124250.png)

* **Navigations-Startebene** - Wo in der Hierarchie die Breadcrumb-Komponente beginnen soll, um zur aktuellen Seite zu gelangen. Beispiel: In We. Retail:

   * 0 beginnt bei `/content`

   * 1 beginnt bei `/content/we-retail`
   * 2 beginnt bei `/content/we-retail/<country>`

* **Ausgeblendete Navigationselemente** anzeigen: Zeigt Seiten an, die im Breadcrumb als ausgeblendet markiert markiert sind (standardmäßig werden sie nicht angezeigt)
* **Aktuelle Seite** ausblenden - Unterdrücken Sie die aktuelle Seite im Breadcrumb (standardmäßig wird sie angezeigt)

## Design-Dialogfeld {#design-dialog}

Das Entwurfsdialogfeld ermöglicht es dem Vorlagenautor, die Standardwerte für die Optionen festzulegen, um ausgeblendete und aktive Seiten in den Breadcrumbs sowie die Tiefe der anzuzeigenden Hierarchie zu unterdrücken.

### Hauptregisterkarte {#main-tab}

![](assets/screen_shot_2018-01-12at124437.png)

* **Navigations-Startebene** : Definiert den Standardwert, für den in der Hierarchie die Breadcrumb-Komponente aufgerufen werden soll, wenn die Breadcrumb-Komponente zu einer Seite hinzugefügt wird.
* **Ausgeblendete Navigationselemente** anzeigen: Definiert den Standardwert der **Option Verborgene Navigationselemente** anzeigen, wenn der Seite die Breadcrumb-Komponente hinzugefügt wird.

   * Die Option für den Autor wird nicht aktiviert oder deaktiviert. Es wird nur der Standardwert festgelegt.

* **Aktuelle Seite** ausblenden: Definiert den Standardwert der Option **Aktuelle Seite** ausblenden, wenn die Breadcrumb-Komponente einer Seite hinzugefügt wird.

   * Die Option für den Autor wird nicht aktiviert oder deaktiviert. Es wird nur der Standardwert festgelegt.

### Stile Registerkarte {#styles-tab}

Die Breadcrumb-Komponente unterstützt das AEM [-Stilsystem](authoring.md#component-styling).