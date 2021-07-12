---
title: Komponente für ausgeblendetes Formular (v1)
description: Die Kernkomponente „Komponente für ausgeblendetes Formular“ ermöglicht die Anzeige eines ausgeblendeten Felds.
index: n
role: Architect, Developer, Admin, User
exl-id: 8e30dac0-5b4b-4fc7-af99-5791c98c90bf
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 100%

---

# Komponente für ausgeblendetes Formular (v1) {#form-hidden-component-v}

Die Kernkomponente „Komponente für ausgeblendetes Formular“ ermöglicht die Anzeige eines ausgeblendeten Felds.

## Nutzung {#usage}

Die Kernkomponente „Komponente für ausgeblendetes Formular“ ermöglicht die Erstellung ausgeblendeter Felder, um Informationen über die aktuelle Seite zurück an AEM zu senden. Sie soll zusammen mit der [Formularcontainer-Komponente](form-container-v1.md) verwendet werden.

Die Feldeigenschaften können vom Inhaltseditor im [Dialogfeld „Konfigurieren“](#configure-dialog) definiert werden.

## Version und Kompatibilität {#version-and-compatibility}

Dieses Dokument beschreibt die v1 der Komponente für ausgeblendetes Formular, die ursprünglich mit Version 1.0.0 der Kernkomponenten mit AEM 6.3 eingeführt wurde.

In der folgenden Tabelle ist die Kompatibilität von v1 der Komponente für ausgeblendetes Formular aufgeführt.

| AEM-Version | Komponente für ausgeblendetes Formular v1 |
|--- |--- |
| 6.3 | Kompatibel |
| 6.4 | Kompatibel |

>[!CAUTION]
>
>Dieses Dokument beschreibt v1 der Komponente für ausgeblendetes Formular.
>
>Weitere Informationen zur aktuellen Version der Komponente für ausgeblendetes Formular finden Sie im Dokument [Komponente für ausgeblendetes Formular](/help/components/forms/form-hidden.md)

## Musterkomponentenausgabe {#sample-component-output}

Im Folgenden finden Sie ein Beispiel von [We.Retail](https://helpx.adobe.com/de/experience-manager/6-4/sites/developing/using/we-retail.html).

### HTML {#html}

```
<div class="cmp cmp-form aem-GridColumn aem-GridColumn--default--12">
 <form method="POST" action="/content/we-retail/us/en/experience.html" id="new_form" name="new_form" enctype="multipart/form-data" class="aem-Grid aem-Grid--12 aem-Grid--default--12 ">
  <input type="hidden" name=":formstart" value="/content/we-retail/us/en/experience/jcr:content/root/responsivegrid/container">
   <div class="visible aem-GridColumn aem-GridColumn--default--12">
    <input type="hidden" id="ghostToast" name="Invisible Toast" value="ghostToast">
   </div>
 </form>
</div>
```

### JSON {#json}

```
"container": {
              "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
              "columnCount": 12,
              "gridClassNames": "aem-Grid aem-Grid--12 aem-Grid--default--12",
              ":items": {
                "hidden": {
                  "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
                  ":type": "weretail/components/form/hidden",
                  "name": "Invisible Toast",
                  "id": "ghostToast",
                  "value": "ghostToast"
                }
              },
              ":itemsOrder": [
                "hidden"
              ],
              ":type": "weretail/components/form/container"
            }
```

>[!NOTE]
>
>Für JSON-Exporte aus den Kernkomponenten ist Version 1.1.0 der Kernkomponenten erforderlich. Weitere Informationen finden Sie in den [Kompatibilitätsinformationen für Kernkomponenten v1](/help/versions.md#release-history-and-compatibility).

## Dialogfeld „Konfigurieren“  {#configure-dialog}

Über das Dialogfeld „Konfigurieren“ kann der Inhaltsautor die Parameter des ausgeblendeten Felds definieren.

![](/help/assets/chlimage_1-26.png)

* **Name** - Der Name des mit den Formulardaten gesendeten Felds
* **Wert** - Der Wert des mit den Formulardaten gesendeten Felds
* **Kennung** - Die Kennung muss auf der Seite eindeutig sein und kann genutzt werden, um Skripte in dieses Formularfeld einzubinden.

## Dialogfeld „Design“  {#design-dialog}

Es gibt kein Dialogfeld „Design“ für die Komponente für ausgeblendetes Formular.

## Technische Details {#technical-details}

Die neueste technische Dokumentation zur Komponente für ausgeblendetes Formular [finden Sie auf GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/hidden/v1/hidden).

Das gesamte Kernkomponentenprojekt kann von GitHub heruntergeladen werden.

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).
