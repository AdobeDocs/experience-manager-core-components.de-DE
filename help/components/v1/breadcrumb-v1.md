---
title: Breadcrumb-Komponente (v1)
description: Die Kernkomponente „Breadcrumb-Komponente“ ist eine Navigationskomponente, die einen Breadcrumb von Links basierend auf der Position der Seite in der Inhaltshierarchie erstellt.
index: n
role: Architekt, Entwickler, Administrator, Geschäftspraktiker
translation-type: ht
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: ht
source-wordcount: '551'
ht-degree: 100%

---


# Breadcrumb-Komponente (v1) {#breadcrumb-component-v}

Die Kernkomponente „Breadcrumb-Komponente“ ist eine Navigationskomponente, die einen Breadcrumb von Links basierend auf der Position der Seite in der Inhaltshierarchie erstellt.

## Verwendung {#usage}

Die Breadcrumb-Komponente zeigt die Position der aktuellen Seite innerhalb der Site-Hierarchie an, wodurch Seitenbesucher von ihrer aktuellen Position aus durch die Seitenhierarchie navigieren können. Dies ist oft in Kopf- oder Fußzeilen von Seiten integriert.

Verfügbare Optionen wie die Standardnavigationsstufe und die Möglichkeit, die aktuelle Seite oder ausgeblendete Seiten anzuzeigen, können vom Vorlagenautor im [Dialogfeld „Design“](#design-dialog) definiert werden. Der Inhaltseditor kann dann festlegen, ob ausgeblendete Seiten angezeigt werden sollen oder nicht, und er kann die tatsächliche Navigationsstufe für die Komponente im [Dialogfeld „Bearbeiten“](#edit-dialog) wählen.

## Version und Kompatibilität {#version-and-compatibility}

In diesem Dokument wird die v1 der Breadcrumb-Komponente beschrieben, die ursprünglich mit Version 1.0.0 der Kernkomponenten mit AEM 6.3 eingeführt wurde.

In der folgenden Tabelle ist die Kompatibilität von v1 der Breadcrumb-Komponente aufgeführt.

| AEM-Version | Breadcrumb-Komponente v1 |
|--- |--- |
| 6.3 | Kompatibel |
| 6.4 | Kompatibel |

>[!CAUTION]
>
>In diesem Dokument wird v1 der Breadcrumb-Komponente beschrieben.
>Weitere Informationen zur aktuellen Version der Breadcrumb-Komponente finden Sie im Dokument [Breadcrumb-Komponente](/help/components/breadcrumb.md).

## Musterkomponentenausgabe {#sample-component-output}

Im Folgenden finden Sie ein Beispiel von [We.Retail](https://helpx.adobe.com/de/experience-manager/6-4/sites/developing/using/we-retail.html).

### Screenshot {#screenshot}

![](/help/assets/chlimage_1-33.png)

### HTML {#html}

```
<div class="cmp cmp-breadcrumb aem-GridColumn aem-GridColumn--default--12">

<ol class="breadcrumb">
    <li class="breadcrumb-item ">
        <a href="/content/we-retail/us.html">
            United States
        </a>
    </li>

    <li class="breadcrumb-item ">
        <a href="/content/we-retail/us/en.html">
            English
        </a>
    </li>

    <li class="breadcrumb-item active">
        
            Experience
        
    </li>
</ol>
 
</div>
```

### JSON {#json}

```
"breadcrumb": {
              "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
              ":type": "weretail/components/content/breadcrumb"
            }
```

>[!NOTE]
>
>Für JSON-Exporte aus den Kernkomponenten ist Version 1.1.0 der Kernkomponenten erforderlich. Weitere Informationen finden Sie in den [Kompatibilitätsinformationen für Kernkomponenten v1](/help/versions.md).

## Dialogfeld „Bearbeiten“ {#edit-dialog}

Das Dialogfeld „Bearbeiten“ ermöglicht es dem Inhaltsautor, ausgeblendete und aktive Seiten in den Breadcrumbs zu unterdrücken sowie die Tiefe der anzuzeigenden Hierarchie zu wählen.

![](/help/assets/chlimage_1-34.png)

* **Start-Level für die Navigation** - Wo in der Hierarchie die Breadcrumb-Komponente beginnen soll, um zur aktuellen Seite zu gelangen. Beispiel in We.Retail:

   * 1 beginnt bei `/content/we-retail`
   * 2 beginnt bei `/content/we-retail/<country>`

* **Ausgeblendete anzeigen** - Zeigt Seiten, die im Breadcrumb als ausgeblendet markiert sind (standardmäßig werden sie nicht angezeigt)
* **Aktuelles ausblenden** - Unterdrücken der aktuellen Seite im Breadcrumb (standardmäßig wird sie angezeigt)

## Dialogfeld „Design“ {#design-dialog}

Das Dialogfeld „Design“ ermöglicht es dem Vorlagenautor, die Standardwerte für die Optionen festzulegen, um ausgeblendete und aktive Seiten in den Breadcrumbs zu unterdrücken, sowie die Tiefe der anzuzeigenden Hierarchie zu definieren.

![](/help/assets/chlimage_1-35.png)

* **Navigations-Level für Anfang** – Definiert den Standardwert, für den in der Hierarchie die Breadcrumb-Komponente aufgerufen werden soll, wenn die Breadcrumb-Komponente zu einer Seite hinzugefügt wird.
* **Ausgeblendete anzeigen** - Definiert den Standardwert der Option **Ausgeblendete anzeigen**, wenn die Breadcrumb-Komponente zu einer Seite hinzugefügt wird.

   * Die Option für den Autor wird dadurch nicht aktiviert oder deaktiviert. Es wird nur der Standardwert festgelegt.

* **Aktuelles ausblenden** – Definiert den Standardwert der Option **Aktuelle Seite ausblenden**, wenn die Breadcrumb-Komponente zu einer Seite hinzugefügt wird.

   * Die Option für den Autor wird dadurch nicht aktiviert oder deaktiviert. Es wird nur der Standardwert festgelegt.

## Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur Breadcrumb-Komponente [finden Sie auf GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/breadcrumb/v1/breadcrumb).

Das gesamte Kernkomponentenprojekt kann von GitHub heruntergeladen werden.

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).
