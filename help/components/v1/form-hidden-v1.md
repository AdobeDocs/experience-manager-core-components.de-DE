---
title: Komponente für ausgeblendetes Formular (v1)
description: Die Kernkomponente „Komponente für ausgeblendetes Formular“ ermöglicht die Anzeige eines ausgeblendeten Felds.
index: false
role: Developer, Admin, User
exl-id: 8e30dac0-5b4b-4fc7-af99-5791c98c90bf
TQID: https://experienceleague.adobe.com/rMf4285S77F8hsmwcgo24Bd39eDl13nozM6KZFCuPqY
product_v2: id: c45915cf-e157-4af7-a80d-97b905bcb3a5id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 73aa5234ac63fa3be99feebce448bb6722513838
workflow-type: tm+mt
source-wordcount: 344
ht-degree: 100%

---

# Komponente für ausgeblendetes Formular (v1) {#form-hidden-component-v}

Die Kernkomponente „Komponente für ausgeblendetes Formular“ ermöglicht die Anzeige eines ausgeblendeten Felds.

## Nutzung {#usage}

Die Kernkomponente „Komponente für ausgeblendetes Formular“ ermöglicht die Erstellung ausgeblendeter Felder, um Informationen über die aktuelle Seite zurück an AEM zu senden. Sie soll zusammen mit der [Formular-Container-Komponente](form-container-v1.md) verwendet werden.

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

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Über das Dialogfeld „Konfigurieren“ kann der Inhaltsautor die Parameter des ausgeblendeten Felds definieren.

![](/help/assets/chlimage_1-26.png)

* **Name** - Der Name des mit den Formulardaten gesendeten Felds
* **Wert** - Der Wert des mit den Formulardaten gesendeten Felds
* **Kennung** - Die Kennung muss auf der Seite eindeutig sein und kann genutzt werden, um Skripte in dieses Formularfeld einzubinden.

## Dialogfeld „Design“ {#design-dialog}

Es gibt kein Dialogfeld „Design“ für die Komponente für ausgeblendetes Formular.

## Technische Details {#technical-details}

Die neueste technische Dokumentation zur Komponente für ausgeblendetes Formular [finden Sie auf GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/hidden/v1/hidden).

Das gesamte Kernkomponentenprojekt kann von GitHub heruntergeladen werden.

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).
