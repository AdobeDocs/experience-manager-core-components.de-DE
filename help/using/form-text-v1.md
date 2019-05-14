---
title: Formulartextkomponente (v 1)
seo-title: Formulartextkomponente (v 1)
description: 'null'
seo-description: Die Komponente "Core-Komponenten-Formulartext" ermöglicht die Einsendung von Formulartext.
uuid: 30123 aba -57 a 8-4 ed 4-93 cb -6 a 3 d 2 edff 9 a 7
content-type: Referenz
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-new
discoiquuid: bd 4 e 9930-4 d 81-49 ae-a 3 d 1-9 a 8740418 dae
index: n
translation-type: tm+mt
source-git-commit: 4e74f10e2a4119484a597178dc4577b399833dbf

---


# Formulartextkomponente (v 1){#form-text-component-v}

Die Komponente &quot;Core-Komponenten-Formulartext&quot; ermöglicht die Einsendung von Formulartext.

## Nutzung {#usage}

Die Formulartextkomponente ermöglicht die Übermittlung verschiedener Texttypen und soll zusammen mit der [Formularcontainerkomponente verwendet](form-container.md)werden.

Der Typ der Textvalidierung, Beschriftung und Hilfemeldungen kann vom Content Editor im Dialogfeld [&quot;Konfigurieren&quot; definiert](form-text-v1.md#main-pars_title)werden.

## Version und Kompatibilität {#version-and-compatibility}

In diesem Dokument wird die Version 1 der Komponente &quot;Formulartext&quot; beschrieben, die ursprünglich mit Version 1.0.0 der Kernkomponenten mit AEM 6.3 eingeführt wurde.

In der folgenden Tabelle ist die Kompatibilität von v 1 der Formulartextkomponente aufgeführt.

| AEM-Version | Formulartextkomponente v 1 |
|--- |--- |
| 6.3 | Kompatibel |
| 6.4 | Kompatibel |

>[!CAUTION]
>
>In diesem Dokument wird Version 1 der Komponente &quot;Formulartext&quot; beschrieben.
>
>Weitere Informationen zur aktuellen Version der Formulartextkomponente finden Sie im [Dokument &quot;Formulartext-Komponente](form-text.md) &quot; .

## Musterkomponentenausgabe {#sample-component-output}

Nachfolgend finden Sie ein Beispiel aus [We. Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

### Screenshot {#screenshot}

![](assets/chlimage_1-22.png)

### HTML {#html}

```
<div class="cmp cmp-form aem-GridColumn aem-GridColumn--default--12">
 <form method="POST" action="/content/we-retail/us/en/experience.html" id="new_form" name="new_form" enctype="multipart/form-data" class="aem-Grid aem-Grid--12 aem-Grid--default--12 ">
     <input type="hidden" name=":formstart" value="/content/we-retail/us/en/experience/jcr:content/root/responsivegrid/container">
     <div class="cmp cmp-form-field aem-GridColumn aem-GridColumn--default--12">
   <div class="form-group">
       <label for="form-text-978484744">How many pieces of toast would you like?</label>
          <input type="number" id="form-text-978484744" name="pieces">
   </div>
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
                "text": {
                  "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
                  ":type": "weretail/components/form/text",
                  "name": "piecesOfToast",
                  "jcr:title": "How many pieces of toast would you like?",
                  "type": "number",
                  "rows": "2"
                }
              },
              ":itemsOrder": [
                "text"
              ],
              ":type": "weretail/components/form/container"
            }
```

>[!NOTE]
>
>Für JSON-Exporte aus den Core-Komponenten ist Version 1.1.0 der Kernkomponenten erforderlich. Weitere Informationen finden Sie in den [Kompatibilitätsinformationen für Kernkomponenten v 1](versions.md#main-pars_title_236368006) .

## Dialogfeld konfigurieren {#configure-dialog}

Das Dialogfeld &quot;Konfigurieren&quot; ermöglicht es dem Inhaltsautor, den Texttyp sowie Standardwerte und Beschriftungen zu definieren.

### Haupt {#main}

![](assets/chlimage_1-23.png)

* **Constraint** - Der Typ des einzustellenden Texts und wird mit

   * **Text**
   * **Textbereich**
   * **E-Mail**
   * **Tel**
   * **Datum**
   * **Nummer**
   * **Kennwort**

* **Textzeilen** : Anzahl der im Textbereich anzuzeigenden Zeilen (nur angezeigt, wenn **&quot;Constraint&quot;** auf **&quot; Textbereich&quot; festgelegt** ist)

* **Beschriftung** - Die Beschriftung, die für das Feld angezeigt wird
* **Blenden Sie die Beschriftung aus** - Erforderlich, wenn die Beschriftung nur für Ein-/Ausgabehilfe erforderlich ist und keine zusätzlichen visuellen Informationen über das Feld enthält.
* **Elementname** - Der Name des mit den Formulardaten gesendeten Felds
* **Wert** - Standardwert, der im Feld vorausgefüllt wird

### Info {#about}

![](assets/chlimage_1-24.png)

* **Hilfe-Meldung** : Ein Hinweis für den Benutzer, der in das Feld eingegeben werden kann
* **Hilfe-Meldung als Platzhalter anzeigen** - Zur Anzeige der Hilfenachricht in der Formulareingabe, wenn diese leer und nicht fokussiert ist

### Einschränkungen {#constraints}

![](assets/chlimage_1-25.png)

* **Beschränkungsmeldung**

   * Meldung wird beim Senden des Formulars als QuickInfo angezeigt, wenn der Wert den ausgewählten Typ nicht validiert
   * Nicht für **Text-** und **Textbereichstypen** angezeigt

* **Erforderlich** : Wenn ausgewählt, muss der Benutzer einen Wert ausfüllen, bevor er das Formular sendet.
* **Schreibgeschützt:** Wenn ausgewählt, kann der Benutzer den Wert des Felds nicht ändern.

## Design-Dialogfeld {#design-dialog}

Es gibt kein Dialogfeld für die Formulartext-Komponente.

## Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur Formulartextkomponente [finden Sie unter github](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/text/v1/text).

Das gesamte Kernkomponentenprojekt kann von github heruntergeladen werden.

Weitere Informationen zur Entwicklung Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Komponenten](developing.md).
