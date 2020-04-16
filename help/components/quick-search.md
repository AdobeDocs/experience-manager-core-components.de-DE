---
title: Schnellsuch-Komponente
description: Die Schnellsuch-Komponente bietet Suchfunktionen für eine Website und zeigt Suchergebnisse an, damit Besucher die Site durchsuchen und die Ergebnisse filtern können.
translation-type: ht
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# Schnellsuch-Komponente {#quick-search-component}

Die Schnellsuch-Komponente bietet Suchfunktionen für eine Website und zeigt Suchergebnisse an, damit Besucher mühelos übereinstimmende Inhalte finden und Ergebnisse anzeigen können.

## Nutzung {#usage}

Die Schnellsuch-Komponente bietet Site-Besuchern die Möglichkeit, nach Inhalten zu suchen, die Ergebnisse unmittelbar anzuzeigen und leicht zu den passenden Seiten zu navigieren. Neue Ergebnisse werden dynamisch abgerufen, wenn der Benutzer die Suchergebnisse durchblättert.

Im [Dialogfeld „Bearbeiten“](#edit-dialog) kann der Verfasser des Inhalts festlegen, wo die Suche in der Inhaltsstruktur beginnen soll. Im [Dialogfeld „Design“](#design-dialog) kann der Vorlagenautor den Standardwert festlegen, an dem die Suche in der Inhaltsstruktur beginnen soll, sowie eine maximale Ergebnissatzgröße und minimale Suchbegriffslänge festlegen.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Schnellsuch-Komponente ist v1, die mit Version 2.0.0 der Kernkomponenten im Januar 2018 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.3 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |--- |---|
| v1 | Kompatibel | Kompatibel | Kompatibel | Kompatibel |

Weitere Informationen zu Kernkomponentenversionen und -freigaben finden Sie in den [Kernkomponentenversionen](/help/versions.md).

## Musterkomponentenausgabe {#sample-component-output}

Im Folgenden finden Sie ein Beispiel von [We.Retail](https://docs.adobe.com/content/help/en/experience-manager-65/developing/bestpractices/we-retail/we-retail.html).

### Screenshot {#screenshot}

![](/help/assets/screen_shot_2018-01-19at094248.png)

### HTML {#html}

```
<section class="cmp-search" role="search" data-cmp-is="search" data-cmp-min-length="3" data-cmp-results-size="10">
    <form class="cmp-search__form" data-cmp-hook-search="form" method="get" action="/content/we-retail/us/en/equipment.searchresults.json/_jcr_content/root/responsivegrid/search" autocomplete="off">
        <div class="cmp-search__field">
            <i class="cmp-search__icon" data-cmp-hook-search="icon"></i>
            <span class="cmp-search__loading-indicator" data-cmp-hook-search="loadingIndicator"></span>
            <input class="cmp-search__input" data-cmp-hook-search="input" type="text" name="fulltext" placeholder="Search" role="combobox" aria-autocomplete="list" aria-haspopup="true" aria-invalid="false">
            <button class="cmp-search__clear" data-cmp-hook-search="clear">
                <i class="cmp-search__clear-icon"></i>
            </button>
        </div>
    </form>
    <div class="cmp-search__results" data-cmp-hook-search="results" role="listbox" aria-multiselectable="false"></div>
    
<script data-cmp-hook-search="itemTemplate" type="x-template">
    <a class="cmp-search__item" data-cmp-hook-search="item">
        <span class="cmp-search__item-title" data-cmp-hook-search="itemTitle"></span>
    </a>
</script>
</section>
```

### JSON {#json}

```
"search":{  
                     "columnClassNames":"aem-GridColumn aem-GridColumn--default--12",
                     "relativePath":"/jcr:content/root/responsivegrid/search",
                     "resultsSize":10,
                     "searchTermMinimumLength":3,
                     ":type":"core/wcm/components/search/v1/search"
                  }
```

### Technische Details {#technical-details}

>[!NOTE]
>
>Der Schutz der Suchkomponente oder einer beliebigen AEM-basierten Anwendung gegen DOS-Angriffe sollte auf höherer Ebene implementiert werden, z. B. durch Verwendung von `mod_security` auf dem Dispatcher.

Die neueste technische Dokumentation zur Schnellsuch-Komponente [finden Sie auf GitHub](https://adobe.com/go/aem_cmp_tech_search_v1).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Dialogfeld „Bearbeiten“ {#edit-dialog}

Im Dialogfeld „Bearbeiten“ kann der Verfasser des Inhalts festlegen, wo die Suche in der Inhaltsstruktur beginnen soll.

![](/help/assets/screen_shot_2018-04-03at120132.png)

**Suchstamm** - Die Stammseite, von der aus die Suche gestartet werden soll. Der Suchstamm kann ein Blueprint-Master, ein Sprachen-Master oder eine normale Seite sein.

## Dialogfeld „Design“ {#design-dialog}

Im Dialogfeld „Design“ kann der Vorlagenautor den Standardwert festlegen, an dem die Suche in der Inhaltsstruktur beginnen soll, sowie eine maximale Ergebnissatzgröße und minimale Suchbegriffslänge. Das Dialogfeld „Design“ ermöglicht dem Vorlagenautor, die für die Inhaltsautoren verfügbaren Textformatierungsoptionen zu definieren.

### Registerkarte „Eigenschaften“ {#properties-tab}

![](/help/assets/screen_shot_2018-04-03at120028.png)

* **Suchstamm**
Der Standardwert des Suchstamms, wenn ein Inhaltsautor die Komponente „Schnellsuche“ auf einer Inhaltsseite platziert
* **Ergebnisgröße**
Die maximale Anzahl von Ergebnissen, die durch eine Suchanfrage abgerufen werden
* **Mindestlänge des Suchbegriffs**
Mindestlänge des Suchbegriffs, um die Suche zu starten

>[!NOTE]
>
>**Die Größe der Ergebnisse** und **die Mindestlänge des Suchbegriffs** können nur im Designmodus festgelegt werden und daher nur auf Vorlagenebene, d. h. Inhaltsautoren können diese Werte nicht ändern.

>[!CAUTION]
>
>**Die Größe der Ergebnisse** und **die Mindestlänge des Suchbegriffs** können Auswirkungen auf die Leistung haben, wenn sie zu hoch oder zu niedrig eingestellt sind.

### Registerkarte „Stile“ {#styles-tab}

Die Komponente „Schnellsuche“ unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).
