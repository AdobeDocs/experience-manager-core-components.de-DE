---
title: Komponente ausgeblendeter Formulare
seo-title: Komponente ausgeblendeter Formulare
description: 'null'
seo-description: Die Komponente "Core-Komponente-Formular ausgeblendet" ermöglicht die Anzeige eines unsichtbaren Felds.
uuid: 63 a 1 b 381-f 45 c -4241-b 743-dea 8 abd 45 e 11
contentOwner: Benutzer
content-type: Referenz
topic-tags: Kernkomponenten
discoiquuid: 36 e 49035-7641-4 unangemessen -8 a 61-723060032903
disttype: dist5
gnavtheme: light
groupsectionnavitems: keine
hidemerchandisingbar: inherit
hidepromocomponent: inherit
modalsize: 426x240
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 1bbec9b1f109df88964dce051a58d111bf6cafaa

---


# Komponente ausgeblendeter Formulare{#form-hidden-component}

Die Komponente &quot;Core-Komponente-Formular ausgeblendet&quot; ermöglicht die Anzeige eines unsichtbaren Felds.

## Nutzung {#usage}

Die Komponente &quot;Core Component Form Hidden&quot; (Ausgeblendete Komponenten) ermöglicht die Erstellung ausgeblendeter Felder, um Informationen über die aktuelle Seite zurück an AEM zurückzusenden. Sie soll zusammen mit der [Formularcontainerkomponente verwendet](form-container.md)werden.

Die Feldeigenschaften können vom Content-Editor im Dialogfeld [&quot;Konfigurieren&quot; definiert](form-hidden.md)werden.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der ausgeblendeten Komponente ist v 2, die mit Version 2.0.0 der Kernkomponenten im Januar 2018 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v2 | Kompatibel | Kompatibel | Kompatibel |
| [v1](form-hidden-v1.md) | Kompatibel | Kompatibel | Kompatibel |

Weitere Informationen zu Core-Komponentenversionen und -versionen finden Sie in den Core [-Komponentenversionen](versions.md).

## Musterkomponentenausgabe {#sample-component-output}

Nachfolgend finden Sie ein Beispiel aus [We. Retail](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html).

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

Die aktuelle technische Dokumentation zur Formular-ausgeblendeten Komponente [finden Sie unter github](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/form/hidden/v2/hidden).

Weitere Informationen zur Entwicklung Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Komponenten](developing.md).

## Dialogfeld konfigurieren {#configure-dialog}

Das Dialogfeld &quot;Konfigurieren&quot; ermöglicht dem Inhaltsautor die Definition der Parameter des ausgeblendeten Felds.

![](assets/chlimage_1-26.png)

* **Name**des Feldes,
das mit den Formulardaten gesendet wird
* **Wert**
des Felds, das mit den Formulardaten gesendet wird
* **Bezeichner**
Der Bezeichner muss eindeutig auf der Seite sein und kann verwendet werden, um Skripten an dieses Formularfeld zu binden.

Da die Komponente &quot;Ausgeblendete Formulare&quot; normalerweise keine sichtbaren Attribute aufweist, zeigt der Platzhalter der Komponente im Editor die **Feldwerte&quot; Name** «und **&quot;Wert&quot;** an, wenn sie zugewiesen werden, damit der Autor die entsprechende Form ausgeblendet wird.

![](assets/screenshot_2018-10-19at094927.png)

## Design-Dialogfeld {#design-dialog}

Es gibt kein Design-Dialogfeld für die Komponente &quot;Formular ausgeblendet&quot; .