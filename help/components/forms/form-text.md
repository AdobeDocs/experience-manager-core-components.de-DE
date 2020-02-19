---
title: Formulartext-Komponente
description: Die Kernkomponente „Formulartext-Komponente“ ermöglicht die Eingabe von Formulartext zur Übermittlung.
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# Formulartext-Komponente{#form-text-component}

Die Kernkomponente „Formulartext-Komponente“ ermöglicht die Eingabe von Formulartext zur Übermittlung.

## Nutzung {#usage}

Die Formulartext-Komponente ermöglicht die Übermittlung verschiedener Texttypen und sollte zusammen mit der [Formularcontainer-Komponente](form-container.md) verwendet werden. Der Typ der Textvalidierung, Beschriftung und Hilfemeldungen kann vom Inhaltseditor im [Dialogfeld „Konfigurieren“](#configure-dialog) definiert werden.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Formulartext-Komponente ist v2, die mit Version 2.0.0 der Kernkomponenten im Januar 2018 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.3 | AEM 6.4 | AEM 6.5 | AEM als Cloud Service |
|--- |--- |--- |--- |---|
| v2 | Kompatibel | Kompatibel | Kompatibel | Kompatibel |
| [v1](/help/components/v1/form-text-v1.md) | Kompatibel | Kompatibel | Kompatibel | - |

Weitere Informationen zu Kernkomponentenversionen und -freigaben finden Sie in den [Kernkomponentenversionen](/help/versions.md).

## Musterkomponentenausgabe {#sample-component-output}

Im Folgenden finden Sie ein Beispiel von [We.Retail](https://docs.adobe.com/content/help/en/experience-manager-65/developing/bestpractices/we-retail/we-retail.html).

### Screenshot {#screenshot}

![](/help/assets/chlimage_1-22.png)

### HTML {#html}

```
<div class="text aem-GridColumn aem-GridColumn--default--12">
   <div class="cmp-form-text">
      <label for="form-text-2146967">How many pieces of toast would you like?
      </label>
   <input class="cmp-form-text__text" type="number" id="form-text-2146967" name="pieces">
   </div>
</div>
```

### JSON {#json}

```
"text":{  
                     "columnClassNames":"aem-GridColumn aem-GridColumn--default--12",
                     "id":"form-text-2146967",
                     "title":"How many pieces of toast would you like?",
                     "name":"pieces",
                     "value":"",
                     "helpMessage":"",
                     "type":"number",
                     "readOnly":false,
                     "required":false,
                     "requiredMessage":"",
                     "constraintMessage":"",
                     "rows":2,
                     "defaultValue":"",
                     ":type":"core/wcm/components/form/text/v2/text"
                  }
```

### Technische Details {#technical-details}

The latest technical documentation about the Form Text Component [can be found on GitHub](https://adobe.com/go/aem_cmp_tech_form_text_v2).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Das Dialogfeld „Konfigurieren“ ermöglicht es dem Inhaltsautor, den Texttyp sowie Standardwerte und Beschriftungen zu definieren.

### Hauptregisterkarte {#main-tab}

![](/help/assets/chlimage_1-23.png)

* **Einschränkung**
Die Art des Textes, der eingegeben und anhand dem validiert wird
   * **Text**
   * **Textbereich**
   * **E-Mail**
   * **Tel**
   * **Datum**
   * **Nummer**
   * **Kennwort**
* **Textzeile**
Anzahl der Zeilen, die im Textbereich angezeigt werden sollen (nur angezeigt, wenn **Beschränkung** auf **Textbereich** festgelegt ist)
* **Beschriftung**
Die Beschriftung, die für das Feld angezeigt wird
* **Beschriftung ausblenden**
Erforderlich, wenn die Beschriftung nur für Zugangszwecke erforderlich ist und keine weiteren visuellen Informationen über das Feld vermittelt
* **Element Name**
Der Name des mit den Formulardaten gesendeten Felds
* **Wert,**
Der im Feld vorbelegte Standardwert

### Registerkarte „Info“ {#about-tab}

![](/help/assets/chlimage_1-24.png)

* **Hilfemeldung**
: Sie weist den Benutzer darauf hin, was im Feld eingegeben werden kann
* **Bestimmt, ob die Hilfemeldung in der Formulareingabe angezeigt wird, wenn sie leer ist und sich nicht im Fokus befindet**


### Registerkarte „Beschränkungen“{#constraints-tab}

![](/help/assets/chlimage_1-25.png)

* **Beschränkungsmeldung**
   * Meldung wird beim Senden des Formulars als QuickInfo angezeigt, wenn der Wert den ausgewählten Typ nicht validiert
   * Wird nicht für Beschränkungstypen **Text** und **Textbereich** angezeigt
* **Erforderlich**
Wenn ausgewält, muss der Benutzer einen Wert ausfüllen, bevor das Formular gesendet werden kann
* **Schreibgeschützt**
Wenn ausgewählt, kann der Benutzer den Wert des Felds nicht ändern

## Dialogfeld „Design“ {#design-dialog}

Es gibt kein Dialogfeld „Design“ für die Formulartext-Komponente.
