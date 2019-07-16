---
title: Formularoptionen-Komponente (v1)
seo-title: Formularoptionen-Komponente (v1)
description: 'null'
seo-description: Die Kernkomponente „Formularoptionen“ ermöglicht die Auswahl aus vordefinierten Optionen in verschiedenen Formaten.
uuid: a22ed77c-c9f3-46f4-8afe-e478383c1251
content-type: Referenz
products: SG_EXPERIENCEMANAGER/CORECOMPONENTS-new
discoiquuid: e1975bfe-2bda-409a-998e-1ff4f9f23b94
disttype: dist5
gnavtheme: light
groupsectionnavitems: keine
hidemerchandisingbar: inherit
hidepromocomponent: inherit
modalsize: 426x240
noindex: 'true'
index: n
internal: n
snippet: y
translation-type: ht
source-git-commit: 632d6abb1f13667cc0457152268d50af3bfabfc4

---


# Formularoptionen (v1){#form-options-component-v}

Die Kernkomponente „Formularoptionen“ ermöglicht die Auswahl aus vordefinierten Optionen in verschiedenen Formaten.

## Nutzung {#usage}

Die Kernkomponente „Formularoptionen-Komponente“ ermöglicht die Übermittlung verschiedener Arten von Optionen, die auf vielerlei Arten präsentiert werden und die zusammen mit der [Formularcontainer-Komponente](form-container.md) verwendet werden sollten.

Die Darstellung der Optionen, Beschriftungen und individuellen Optionen kann vom Inhaltseditor im Dialogfeld [Konfigurieren](form-options-v1.md#main-pars_title) definiert werden.

## Version und Kompatibilität {#version-and-compatibility}

In diesem Dokument wird die v1 der Formularoptionen-Komponente beschrieben, die ursprünglich mit Version 1.0.0 der Kernkomponenten mit AEM 6.3 eingeführt wurde.

In der folgenden Tabelle ist die Kompatibilität von v1 der Formularoptionen-Komponente aufgeführt.

| Komponentenversion | AEM 6.3 | AEM 6.4 |
|--- |--- |--- |
| v2 | Kompatibel | Kompatibel |
| v1 | Kompatibel | Kompatibel |

>[!CAUTION]
>
>In diesem Dokument wird die v1 der Formularoptionen-Komponente beschrieben.
>
>Weitere Informationen zur aktuellen Version der Formularoptionen-Komponente finden Sie im Dokument [Formularoptionen-Komponente](form-options.md).

## Musterkomponentenausgabe {#sample-component-output}

Folgendes Beispiel wurde von [We.Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html) übernommen.

### Screenshot {#screenshot}

![](assets/chlimage_1-89.png)

### HTML {#html}

```
<div class="cmp cmp-form aem-GridColumn aem-GridColumn--default--12">
<form method="POST" action="/content/we-retail/us/en/experience.html" id="new_form" name="new_form" enctype="multipart/form-data" class="aem-Grid aem-Grid--12 aem-Grid--default--12 ">
    <input type="hidden" name=":formstart" value="/content/we-retail/us/en/experience/jcr:content/root/responsivegrid/container">
    
    <div class="cmp cmp-options aem-GridColumn aem-GridColumn--default--12">

    <fieldset class="form-group checkbox">
        <legend>What is your favorite type of toast?</legend>
        
        <div class="checkbox-item">
            <label>
              <input type="checkbox" name="toasttypes" value="dry">
              Plain dry toast
            </label>
        </div>
<div class="checkbox-item">
            <label>
              <input type="checkbox" name="toasttypes" value="french">
              French toast
            </label>
        </div>
<div class="checkbox-item">
            <label>
              <input type="checkbox" name="toasttypes" value="texas">
              Texas toast
            </label>
        </div>

    </fieldset>
    
</div>
    
</form></div>
```

### JSON {#json}

```
"container": {
              "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
              "columnCount": 12,
              "gridClassNames": "aem-Grid aem-Grid--12 aem-Grid--default--12",
              ":items": {
                "options": {
                  "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
                  ":type": "weretail/components/form/options",
                  "name": "toastTypes",
                  "jcr:title": "What is your favorite type of toast?",
                  "source": "local",
                  "type": "checkbox"
                }
              },
              ":itemsOrder": [
                "options"
              ],
              ":type": "weretail/components/form/container"
            }
```

>[!NOTE]
>
>Für JSON-Exporte aus den Kernkomponenten ist Version 1.1.0 der Kernkomponenten erforderlich. Weitere Informationen finden Sie in den [Kompatibilitätsinformationen für Kernkomponenten v1](versions.md#main-pars_title_236368006).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Im Dialogfeld „Konfigurieren“ kann der Inhaltsautor den Typ der Optionen festlegen, die angezeigt werden sollen, Beschriftungen definieren und festlegen, welche Optionen verfügbar sind.

![](assets/chlimage_1-90.png)

* **Arten**
Wie die Optionen angezeigt werden

   * **Kontrollkästchen**
   * **Optionsfelder**
   * **Dropdown**
   * **Dropdown für mehrere Auswahlen**

* **Titel** - Der Titel, der als Beschriftung für die Optionen angezeigt wird
* **Name** - Der Name des mit den Formulardaten gesendeten Felds
* **Quelle** - Wo die Optionen definiert sind

   * **Lokal** - Definiert in der Komponente
      * Tippen oder klicken Sie auf die Schaltfläche **Hinzufügen**, um einen Wert hinzuzufügen, und auf **Entfernen**, um einen Wert zu entfernen.
      * **Wert** - Der Wert, der gespeichert wird, wenn diese Option beim Senden des Formulars ausgewählt wird.
      * **Text** - Die Bezeichnung für die Option, die im Formular angezeigt wird
      * **Aktiv** - Die Option wird als ausgewählt markiert, wenn das Formular geladen wird
      * **Deaktiviert** - Die Option ist nicht auswählbar, wird aber trotzdem angezeigt
      * **Liste** - Eine an anderer Stelle in AEM definierte statische Liste wird für die Option verwendet
         * **Liste** - Der Pfad der statischen Liste in AEM
            * Verwenden Sie die Schaltfläche „Durchsuchen“, um die Listenressource zu finden.
      * **Datenquelle** - Eine Datenquelle wird für die Optionen verwendet
         * **Datenquelle** - Ressourcentyp der Datenquelle
* **Hilfenachricht** - Ein Hinweis für den Benutzer dahingehend, was im Feld eingegeben werden kann

## Dialogfeld „Design“ {#design-dialog}

Es gibt kein Dialogfeld „Design“ für die Formularoptionen-Komponente.

## Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur Formularoptionen-Komponente [finden Sie auf GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/options/v1/options).

Das gesamte Kernkomponentenprojekt kann von GitHub heruntergeladen werden.

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation von Kernkomponenten für Entwickler](developing.md).
