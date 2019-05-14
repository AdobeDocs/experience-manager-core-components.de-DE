---
title: Komponente "Formularoptionen «
seo-title: Komponente "Formularoptionen «
description: Die Komponente "Core-Komponenten-Formularformulare" ermöglicht die Auswahl aus vordefinierten Optionen in verschiedenen Formaten.
seo-description: Die Komponente "Core-Komponenten-Formularformulare" ermöglicht die Auswahl aus vordefinierten Optionen in verschiedenen Formaten.
uuid: 7 e 8714 df -75 d 1-4 bb 0-b 1 ee-b 7 c 7450 d 806 a
contentOwner: Benutzer
content-type: Referenz
topic-tags: authoring
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-new
discoiquuid: 42289 c 2 b -1671-463 a-ac 1 d -457 aa 9 aefa 2 a
translation-type: tm+mt
source-git-commit: 1243d6cc1b0b015ee2f37ae89d0e2e42d366cc02

---


# Komponente &quot;Formularoptionen «{#form-options-component}

Die Komponente &quot;Core-Komponenten-Formularoptionen&quot; ermöglicht die Auswahl aus vordefinierten Optionen in verschiedenen Formaten.

## Nutzung {#usage}

Die Komponente &quot;Core-Komponenten-Formularoptionen&quot; ermöglicht die Übermittlung verschiedener Arten von Optionen, die auf vielerlei Arten präsentiert werden und sollen zusammen mit der [Formularcontainer-Komponente verwendet](form-container.md)werden.

Die Darstellung der Optionen, Beschriftungen und einzelnen Optionen kann vom Content Editor im Dialogfeld [&quot;Konfigurieren&quot; definiert](#configure-dialog)werden.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Formularoptionskomponente ist v 2, die mit Version 2.0.0 der Kernkomponenten im Januar 2018 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v2 | Kompatibel | Kompatibel | Kompatibel |
| [v1](form-options-v1.md) | Kompatibel | Kompatibel | Kompatibel |

Weitere Informationen zu Core-Komponentenversionen und -versionen finden Sie in den Core [-Komponentenversionen](versions.md).

## Musterkomponentenausgabe {#sample-component-output}

Nachfolgend finden Sie ein Beispiel aus [We. Retail](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html).

### Screenshot {#screenshot}

![](assets/screen_shot_2018-01-12at113648.png)

### HTML {#html}

```
<form method="POST" action="/content/we-retail/us/en/experience.html" id="new_form" name="new_form" enctype="multipart/form-data" class="cmp-form aem-Grid aem-Grid--12 aem-Grid--default--12">
    <input type="hidden" name=":formstart" value="/content/we-retail/us/en/experience/jcr:content/root/responsivegrid/container">
    
    <div class="hidden aem-GridColumn aem-GridColumn--default--12">
<input type="hidden" id="form-hidden-66464844" name="hidden">

</div>
<div class="hidden aem-GridColumn aem-GridColumn--default--12">
<input type="hidden" id="form-hidden-858231075" name="hidden">

</div>
<div class="hidden aem-GridColumn aem-GridColumn--default--12">
<input type="hidden" id="form-hidden-862566768" name="hidden">

</div>
<div class="container responsivegrid aem-GridColumn aem-GridColumn--default--12">

    <input type="hidden" name=":formstart" value="/content/we-retail/us/en/experience/jcr:content/root/responsivegrid/container/container">
    
    <div class="options aem-GridColumn aem-GridColumn--default--12">

    <fieldset class="cmp-form-options">
        
            <legend class="cmp-form-options__legend">What is your favorite type of toast?</legend>
            <label class="cmp-form-options__field-label">
                <input class="cmp-form-options__field cmp-form-options__field--radio" type="radio" name="favToast" value="dryToast">
                Plain dry toast
            </label>
<label class="cmp-form-options__field-label">
                <input class="cmp-form-options__field cmp-form-options__field--radio" type="radio" name="favToast" value="frenchToast">
                French Toast
            </label>
<label class="cmp-form-options__field-label">
                <input class="cmp-form-options__field cmp-form-options__field--radio" type="radio" name="favToast" value="texasToast">
                Texas Toast
            </label>

    </fieldset>

</div>

</div></form>
```

### JSON {#json}

```
"container":{  
                           "columnClassNames":"aem-GridColumn aem-GridColumn--default--12",
                           "columnCount":12,
                           "gridClassNames":"aem-Grid aem-Grid--12 aem-Grid--default--12",
                           ":items":{  
                              "options_816658469":{  
                                 "columnClassNames":"aem-GridColumn aem-GridColumn--default--12",
                                 "id":"form-options-269951232",
                                 "title":"What is your favorite type of toast?",
                                 "name":"favToast",
                                 "type":"RADIO",
                                 "items":[  
                                    {  
                                       "value":"dryToast",
                                       "text":"Plain dry toast",
                                       "selected":false,
                                       "disabled":false
                                    },
                                    {  
                                       "value":"frenchToast",
                                       "text":"French Toast",
                                       "selected":false,
                                       "disabled":false
                                    },
                                    {  
                                       "value":"texasToast",
                                       "text":"Texas Toast",
                                       "selected":false,
                                       "disabled":false
                                    }
                                 ],
                                 ":type":"core/wcm/sandbox/components/form/options/v2/options"
                              }
                           },
                           ":itemsOrder":[  
                              "options_816658469"
                           ],
                           ":type":"core/wcm/sandbox/components/form/container/v2/container"
                        }
```

### Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur Formularoptionskomponente [finden Sie unter github](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/form/options/v2/options).

Weitere Informationen zur Entwicklung Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Komponenten](developing.md).

## Dialogfeld konfigurieren {#configure-dialog}

Im Dialogfeld &quot;Konfigurieren&quot; kann der Inhaltsautor den Typ der Optionen festlegen, die angezeigt werden sollen, Beschriftungen und welche Optionen verfügbar sind.

![](assets/screen_shot_2018-01-12at113153.png)

* **Typen** - Wie die Optionen angezeigt werden
   * **Kontrollkästchen**
   * **Optionsfelder**
   * **Dropdown**
   * **Dropdown für mehrere Auswahlen**
* **Titel**
Der Titel, der als Beschriftung für die Optionen angezeigt wird
* **Name**
des mit den Formulardaten gesendeten Felds
* **Quelle**, an
der die Optionen definiert sind
   * **Lokal**
definiert in der Komponente
      * Tippen oder klicken Sie auf **die Schaltfläche Hinzufügen** , um einen Wert hinzuzufügen, **Löschen** , um einen Wert zu entfernen.
      * **Wert wird**
gespeichert, wenn diese Option beim Senden des Formulars ausgewählt wird
      * **Text**
Der Beschriftung der im Formular angezeigten Option
      * **Aktiv**
Diese Option wird als ausgewählt markiert, wenn das Formular geladen wird.
      * **Deaktiviert**
Die Option ist nicht auswählbar, aber trotzdem angezeigt
      * **Liste**Eine statische Liste,
die anderswo in AEM definiert ist, wird für die Optionen verwendet
         * **Den** Pfad der statischen Liste in AEM auflisten
            * Suchen Sie mithilfe der Schaltfläche &quot;Durchsuchen&quot; die Listenressource.
      * **Datenquelle**
Eine Datenquelle wird für die Optionen verwendet.
         * **Datenquellen**-Ressourcentyp
der Datenquelle
* **Hilfe-Meldung**
Ein Hinweis für den Benutzer, der in das Feld eingegeben werden kann

## Design-Dialogfeld {#design-dialog}

### Stile Registerkarte {#styles-tab}

Die Komponente &quot;Formularoptionen&quot; unterstützt das AEM [-Stilsystem](authoring.md#component-styling).