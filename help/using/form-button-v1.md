---
title: Formular-Schaltflächenkomponente (v 1)
seo-title: Formular-Schaltflächenkomponente (v 1)
description: 'null'
seo-description: Die Komponente "Core Component Form" (Ausgeblendete Komponente) ermöglicht die Einbeziehung eines unsichtbaren Felds in ein Formular.
uuid: 0525 e 70 f -294 f -4 d 35-bf 96-fc 0 e 4 ec 225 e 9
content-type: Referenz
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-new
discoiquuid: ea 06 acc 0-38 e 2-4252-ac 29-07332835 b 7 c 4
disttype: dist5
gnavtheme: light
groupsectionnavitems: keine
hidemerchandisingbar: inherit
hidepromocomponent: inherit
modalsize: 426x240
index: n
translation-type: tm+mt
source-git-commit: 4e74f10e2a4119484a597178dc4577b399833dbf

---


# Formular-Schaltflächenkomponente (v 1){#form-button-component-v}

Die Komponente &quot;Core-Komponenten-Formular&quot; ermöglicht die Einbeziehung eines Schaltflächenfelds in ein Formular, um eine Aktion auszulösen.

## Nutzung {#usage}

Die Komponente &quot;Core-Komponenten-Formular&quot; ermöglicht die Erstellung von Schaltflächenfeldern, die häufig die Übermittlung des Formulars auslösen und zusammen mit der [Formularcontainerkomponente verwendet werden sollen](form-container.md).

Die Schaltflächeneigenschaften können vom Content-Editor im Dialogfeld [&quot;Konfigurieren&quot; definiert](form-button-v1.md#main-pars_title)werden.

## Version und Kompatibilität {#version-and-compatibility}

In diesem Dokument wird die Version 1 der Komponente &quot;Formular-Schaltfläche&quot; beschrieben, die ursprünglich mit Version 1.0.0 der Kernkomponenten mit AEM 6.3 eingeführt wurde.

In der folgenden Tabelle ist die Kompatibilität von v 1 der Formular-Schaltflächenkomponente aufgeführt.

| AEM-Version | Formular-Schaltflächenkomponente v 1 |
|--- |--- |
| 6.3 | Kompatibel |
| 6.4 | Kompatibel |

>[!CAUTION]
>
>In diesem Dokument wird die Version 1 der Komponente &quot;Formular-Schaltfläche&quot; beschrieben.
>
>Weitere Informationen zur aktuellen Version der Formular-Schaltflächenkomponente finden Sie im [Dokument &quot;Formularschaltflächenkomponente](form-button.md) &quot; .

## Musterkomponentenausgabe {#sample-component-output}

Nachfolgend finden Sie ein Beispiel aus [We. Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

### Screenshot {#screenshot}

![](assets/chlimage_1-48.png)

### HTML {#html}

```
<div class="cmp cmp-button aem-GridColumn aem-GridColumn--default--12">
    <div class="cmp cmp-button">
        <button type="BUTTON" class="btn btn-action btn-primary" name="loveToast" value="ILoveToast">
            Click here if you love toast!
        </button>
    </div>
</div>
```

### JSON {#json}

```
"container": {
              "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
              "columnCount": 12,
              "gridClassNames": "aem-Grid aem-Grid--12 aem-Grid--default--12",
              ":items": {
                "button": {
                  "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
                  ":type": "weretail/components/form/button",
                  "name": "loveToast",
                  "jcr:title": "Click here if you love toast!",
                  "type": "submit",
                  "value": "ILoveToast"
                }
              },
              ":itemsOrder": [
                "button"
              ],
              ":type": "weretail/components/form/container"
            }
```

>[!NOTE]
>
>Für JSON-Exporte aus den Core-Komponenten ist Version 1.1.0 der Kernkomponenten erforderlich. Weitere Informationen finden Sie in den [Kompatibilitätsinformationen für Kernkomponenten v 1](versions.md#main-pars_title_236368006) .

## Dialogfeld konfigurieren {#configure-dialog}

Über das Dialogfeld &quot;Konfigurieren&quot; kann der Inhaltsautor die Parameter der Schaltfläche definieren.

![](assets/chlimage_1-49.png)

* **Typ**
   * **Schaltfläche**
   * **Absenden**

* **Titel** - Der auf der Schaltfläche angezeigte Text
   * Wenn kein Wert angegeben ist, wird standardmäßig der Schaltflächentyp

* **Name** - Der Name der Schaltfläche, die mit den Formulardaten gesendet wird
* **Wert** - Der Wert der Schaltfläche, der mit den Formulardaten gesendet wird

## Design-Dialogfeld {#design-dialog}

Es gibt kein Dialogfeld für die Formularschaltfläche.

## Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur Formularschaltfläche-Komponente [finden Sie unter github](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/button/v1/button).

Das gesamte Kernkomponentenprojekt kann von github heruntergeladen werden.

Weitere Informationen zur Entwicklung Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Komponenten](developing.md).
