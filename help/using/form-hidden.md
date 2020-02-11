---
title: Komponente für ausgeblendetes Formular
description: Die Kernkomponente „Komponente für ausgeblendetes Formular“ ermöglicht die Anzeige eines ausgeblendeten Felds.
translation-type: tm+mt
source-git-commit: 60df01ca9efe59b67bad57610d04496a2cdded9e

---


# Komponente für ausgeblendetes Formular{#form-hidden-component}

Die Kernkomponente „Komponente für ausgeblendetes Formular“ ermöglicht die Anzeige eines ausgeblendeten Felds.

## Nutzung {#usage}

Die Kernkomponente „Komponente für ausgeblendetes Formular“ ermöglicht die Erstellung ausgeblendeter Felder, um Informationen über die aktuelle Seite zurück an AEM zu senden. Sie soll zusammen mit der [Formularcontainer-Komponente](form-container.md) verwendet werden.

Die Feldeigenschaften können vom Inhaltseditor im [Dialogfeld „Konfigurieren“](form-hidden.md) definiert werden.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Komponente für ausgeblendetes Formular ist v2, die mit Version 2.0.0 der Kernkomponenten im Januar 2018 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.3 | AEM 6.4 | AEM 6.5 | AEM als Cloud-Dienst |
|--- |--- |--- |--- |---|
| v2 | Kompatibel | Kompatibel | Kompatibel | Kompatibel |
| [v1](form-hidden-v1.md) | Kompatibel | Kompatibel | Kompatibel | - |

Weitere Informationen zu Kernkomponentenversionen und -freigaben finden Sie in den [Kernkomponentenversionen](versions.md).

## Musterkomponentenausgabe {#sample-component-output}

Im Folgenden finden Sie ein Beispiel von [We.Retail](https://docs.adobe.com/content/help/en/experience-manager-65/developing/bestpractices/we-retail/we-retail.html).

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

### Technische Details {#technical-details}

The latest technical documentation about the Form Hidden Component [can be found on GitHub](https://adobe.com/go/aem_cmp_tech_form_hidden_v2).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](developing.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Über das Dialogfeld „Konfigurieren“ kann der Inhaltsautor die Parameter des ausgeblendeten Felds definieren.

![](assets/chlimage_1-26.png)

* **Name**
Der Name des mit den Formulardaten gesendeten Felds
* **Wert**
Der Wert des mit den Formulardaten gesendeten Felds
* **Kennung**
Die Kennung muss auf der Seite eindeutig sein und kann genutzt werden, um Skripte in dieses Formularfeld einzubinden.

Da die Komponente für ausgeblendetes Formular normalerweise keine sichtbaren Attribute aufweist, zeigt der Platzhalter der Komponente im Editor die Feldwerte **Name** und **Wert** an, wenn sie zugewiesen werden, um dem Autor zu helfen, die passende Komponente für ausgeblendetes Formular zu identifizieren.

![](assets/screenshot_2018-10-19at094927.png)

## Dialogfeld „Design“ {#design-dialog}

Es gibt kein Dialogfeld „Design“ für die Komponente für ausgeblendetes Formular.
