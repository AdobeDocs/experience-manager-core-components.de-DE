---
title: Formulartextkomponente
seo-title: Formulartextkomponente
description: 'null'
seo-description: Die Komponente "Core-Komponenten-Formulartext" ermöglicht die Einsendung von Formulartext.
uuid: f 2418 d 55-0 b 59-4 c 7 c-a 541-d 12 dda 4 db 4 cf
contentOwner: Benutzer
content-type: Referenz
topic-tags: authoring
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-new
discoiquuid: 3 a 970 c 4 b -806 b -4 a 0 a-b 6 b 8-b 3 dca 4 e 9 f 136
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


# Formulartextkomponente{#form-text-component}

Die Komponente &quot;Core-Komponenten-Formulartext&quot; ermöglicht die Einsendung von Formulartext.

## Nutzung {#usage}

Die Komponente &quot;Formulartext&quot; ermöglicht die Übermittlung verschiedener Texttypen und soll zusammen mit der [Formularcontainerkomponente verwendet](form-container.md)werden. Der Typ der Textvalidierung, Beschriftung und Hilfemeldungen kann vom Content Editor im Dialogfeld [&quot;Konfigurieren&quot; definiert](#configure-dialog)werden.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Formulartext-Komponente ist v 2, die mit Version 2.0.0 der Kernkomponenten im Januar 2018 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v2 | Kompatibel | Kompatibel | Kompatibel |
| [v1](form-text-v1.md) | Kompatibel | Kompatibel | Kompatibel |

Weitere Informationen zu Core-Komponentenversionen und -versionen finden Sie in den Core [-Komponentenversionen](versions.md).

## Musterkomponentenausgabe {#sample-component-output}

Nachfolgend finden Sie ein Beispiel aus [We. Retail](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html).

### Screenshot {#screenshot}

![](assets/chlimage_1-22.png)

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

Die aktuelle technische Dokumentation zur Formulartextkomponente [finden Sie unter github](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/text/v2/text).

Weitere Informationen zur Entwicklung Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Komponenten](developing.md).

## Dialogfeld konfigurieren {#configure-dialog}

Das Dialogfeld &quot;Konfigurieren&quot; ermöglicht es dem Inhaltsautor, den Texttyp sowie Standardwerte und Beschriftungen zu definieren.

### Hauptregisterkarte {#main-tab}

![](assets/chlimage_1-23.png)

* **Constraint**
The Type of text to be input and will be validation against
   * **Text**
   * **Textbereich**
   * **E-Mail**
   * **Tel**
   * **Datum**
   * **Nummer**
   * **Kennwort**
* **Textzeilenanzahl**
der Zeilen, die im Textbereich angezeigt werden sollen (nur angezeigt, wenn **&quot;Constraint** «auf **&quot; Textbereich&quot; festgelegt** ist)
* **Beschriftung für** das Feld beschriften
* **Blenden Sie die Beschriftung von**&quot;Erforderlich&quot; aus, wenn die Beschriftung nur für Ein-/Ausgabehilfe-Zwecke erforderlich ist und keine weiteren visuellen Informationen über das Feld eingibt.
* **Elementname**
Der Name des Feldes, das mit den Formulardaten gesendet wird
* **Standardwert,**
der im Feld vorbelegt wird

### Registerkarte &quot;Info « {#about-tab}

![](assets/chlimage_1-24.png)

* **Hilfe-Meldung**
an den Benutzer senden, was in das Feld eingegeben werden kann
* **Hilfe-Meldung als Platzhalter**
anzeigen, um die Hilfemeldung in der Formulareingabe anzuzeigen, wenn diese leer und nicht fokussiert ist

### Registerkarte „Beschränkungen“{#constraints-tab}

![](assets/chlimage_1-25.png)

* **Beschränkungsmeldung**
   * Meldung wird beim Senden des Formulars als QuickInfo angezeigt, wenn der Wert den ausgewählten Typ nicht validiert
   * Nicht für **Text-** und **Textbereichstypen** angezeigt
* **Wenn**
ausgewählt, muss der Benutzer einen Wert ausfüllen, bevor er das Formular sendet.
* **Schreibgeschützt** Wenn ausgewählt, kann der Benutzer den Wert des Felds nicht ändern

## Design-Dialogfeld {#design-dialog}

Es gibt kein Dialogfeld für die Formulartext-Komponente.