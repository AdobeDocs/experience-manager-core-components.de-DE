---
title: Komponente für ausgeblendetes Formular
seo-title: Komponente für ausgeblendetes Formular
description: 'null'
seo-description: Die Kernkomponente „Komponente für ausgeblendetes Formular“ ermöglicht die Anzeige eines ausgeblendeten Felds.
uuid: 63a1b381-f45c-4241-b743-dea8abd45e11
contentOwner: Benutzer
content-type: Referenz
topic-tags: Kernkomponenten
discoiquuid: 36e49035-7641-4bad-8a61-723060032903
disttype: dist5
gnavtheme: light
groupsectionnavitems: keine
hidemerchandisingbar: inherit
hidepromocomponent: inherit
modalsize: 426x240
index: y
internal: n
snippet: y
translation-type: ht
source-git-commit: 632d6abb1f13667cc0457152268d50af3bfabfc4

---


# Komponente für ausgeblendetes Formular{#form-hidden-component}

Die Kernkomponente „Komponente für ausgeblendetes Formular“ ermöglicht die Anzeige eines ausgeblendeten Felds.

## Nutzung {#usage}

Die Kernkomponente „Komponente für ausgeblendetes Formular“ ermöglicht die Erstellung ausgeblendeter Felder, um Informationen über die aktuelle Seite zurück an AEM zu senden. Sie soll zusammen mit der [Formularcontainer-Komponente](form-container.md) verwendet werden.

Die Feldeigenschaften können vom Inhaltseditor im [Dialogfeld „Konfigurieren“](form-hidden.md) definiert werden.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Komponente für ausgeblendetes Formular ist v2, die mit Version 2.0.0 der Kernkomponenten im Januar 2018 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v2 | Kompatibel | Kompatibel | Kompatibel |
| [v1](form-hidden-v1.md) | Kompatibel | Kompatibel | Kompatibel |

Weitere Informationen zu Kernkomponentenversionen und -freigaben finden Sie in den [Kernkomponentenversionen](versions.md).

## Musterkomponentenausgabe {#sample-component-output}

Folgendes Beispiel wurde von [We.Retail](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html) übernommen.

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

Die aktuelle technische Dokumentation zur Komponente für ausgeblendetes Formular [finden Sie auf GitHub](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/form/hidden/v2/hidden).

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