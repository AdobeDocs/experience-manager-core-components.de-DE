---
title: Listenkomponente (v 1)
seo-title: Listenkomponente (v 1)
description: 'null'
seo-description: Die Komponente Component Component List ermöglicht die einfache Erstellung dynamischer sowie statischer Listen.
uuid: 06658 c 9 d-cbf 2-4 bfe-b 425-d 980 d 1181908
content-type: Referenz
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-new
discoiquuid: 7 c 130 ccc -83 ff -464 d-b 58 f-d 581 f 4365 dbd
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
translation-type: tm+mt
source-git-commit: 1bbec9b1f109df88964dce051a58d111bf6cafaa

---


# Listenkomponente (v 1){#list-component-v}

Die Komponente Component Component List ermöglicht die einfache Erstellung dynamischer sowie statischer Listen.

## Nutzung {#usage}

Die Listenkomponente kann zum Erstellen einer dynamischen Liste von untergeordneten Seiten oder einer statischen Liste von willkürlich definierten Elementen verwendet werden.

Der Typ der verfügbaren Listen und Formatierungsoptionen kann vom Vorlagenautor im [Designdialogfeld definiert](list-v1.md#main-pars_title_1995166862)werden. Der Content-Editor kann aus verfügbaren Listentypen und dem Formatieren der Listenelemente im [Bearbeitungsdialogfeld auswählen](list-v1.md#main-pars_title).

## Version und Kompatibilität {#version-and-compatibility}

In diesem Dokument wird die Version 1 der List Component beschrieben, die ursprünglich mit Version 1.0.0 der Kernkomponenten mit AEM 6.3 eingeführt wurde.

In der folgenden Tabelle ist die Kompatibilität von v 1 der Listenkomponente aufgeführt.

| AEM-Version | Listenkomponente v 1 |
|--- |--- |
| 6.3 | Kompatibel |
| 6.4 | Kompatibel |

>[!CAUTION]
>
>In diesem Dokument wird v 1 der Listenkomponente beschrieben.
>
>Weitere Informationen zur aktuellen Version der Listenkomponente finden Sie im [Dokument List Component](list.md) .

## Musterkomponentenausgabe {#sample-component-output}

Nachfolgend finden Sie ein Beispiel aus [We. Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

### Screenshot {#screenshot}

![](assets/chlimage_1-47.png)

### HTML {#html}

```
<div class="cmp cmp-list aem-GridColumn aem-GridColumn--default--12">

<ul>
    <li>
    <article>
        <a href="/content/we-retail/us/en/experience/arctic-surfing-in-lofoten.html">
            <span class="cmp-list--item-title">Arctic Surfing In Lofoten</span>
            
        </a>
        
    </article>
</li>

    <li>
    <article>
        <a href="/content/we-retail/us/en/experience/summit-success-in-the-himalayas.html">
            <span class="cmp-list--item-title">Summit Success in the Himalayas</span>
            
        </a>
        
    </article>
</li>

    <li>
    <article>
        <a href="/content/we-retail/us/en/experience/climbing-on-kalymnos-island--greece.html">
            <span class="cmp-list--item-title">Climbing on Kalymnos Island, Greece</span>
            
        </a>
        
    </article>
</li>

    <li>
    <article>
        <a href="/content/we-retail/us/en/experience/running-at-the-great-wall-marathon.html">
            <span class="cmp-list--item-title">Running at the Great Wall Marathon</span>
            
        </a>
        
    </article>
</li>

    <li>
    <article>
        <a href="/content/we-retail/us/en/experience/skiing-deep-powder-in-siberia.html">
            <span class="cmp-list--item-title">Skiing deep powder in Siberia</span>
            
        </a>
        
    </article>
</li>

    <li>
    <article>
        <a href="/content/we-retail/us/en/experience/climbing-in-the-massif-du-mont-blanc.html">
            <span class="cmp-list--item-title">Climbing in the Massif du Mont Blanc</span>
            
        </a>
        
    </article>
</li>
</ul>

</div>
```

### JSON {#json}

```
"articles_list": {
              "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
              ":type": "weretail/components/content/articleslist",
              "tagsMatch": "any",
              "displayAs": "teaser",
              "feedEnabled": "true",
              "listFrom": "children",
              "limit": "0",
              "orderBy": "cq:lastModified",
              "pageMax": "0"
            }
```

>[!NOTE]
>
>Für JSON-Exporte aus den Core-Komponenten ist Version 1.1.0 der Kernkomponenten erforderlich. Weitere Informationen finden Sie in den [Kompatibilitätsinformationen für Kernkomponenten v 1](versions.md#main-pars_title_236368006) .

## Dialogfeld bearbeiten {#edit-dialog}

Das Dialogfeld &quot;Bearbeiten&quot; ermöglicht dem Inhaltsautor die Konfiguration der Liste und der Listenelemente.

### Listen-Einstellungen {#list-settings}

Die Liste kann auf verschiedene Weise erstellt werden.

* [Untergeordnete Seiten](list-v1.md#main-pars_title_1861279796)
* [Liste fester Werte](list-v1.md#main-pars_title_1227896889)
* [Suchen](list-v1.md#main-pars_title_1224003560)
* [Tags](list-v1.md#main-pars_title_700759533)

Unabhängig davon, wie die Liste erstellt wurde, gibt es [Sortieroptionen](list-v1.md#main-pars_title_1568376452) , die immer konfiguriert werden können.

![](assets/chlimage_1-38.png)

Je nachdem, wie der Inhaltsautor die Liste erstellt, werden die zusätzlichen Konfigurationsoptionen geändert.

#### Untergeordnete Seiten {#child-pages}

Die Liste kann aus den untergeordneten Seiten der aktuellen Seite oder einer anderen Seite bestehen.

![](assets/chlimage_1-39.png)

* **Übergeordnete Seite**
   * Die Seite, deren untergeordnete Seiten die Liste bereitstellen sollten
   * Leer lassen, um die aktuelle Seite zu verwenden
* **Untergeordnete Tiefe** - Wie viele Ebenen in der Hierarchie verwendet werden sollten

#### Feste Liste {#fixed-list}

Die Liste kann mit einer festen Liste von Elementen erstellt werden.

![](assets/chlimage_1-40.png)

Tippen oder klicken Sie auf **die Schaltfläche &quot;Hinzufügen** &quot; , um ein neues Element auf die Liste einzufügen.

* Geben Sie Text für das Element in der Liste ein oder wählen Sie im **Auswahldialogfeld** ein Element aus AEM aus.
* Mit dem Ziehpunkt können Sie die Elemente in der Liste neu anordnen.
* Verwenden Sie das Papierkorbsymbol, um Elemente in der Liste zu löschen.

#### search (Suche){#search}

Die Liste kann mithilfe der Ergebnisse einer Suche aus AEM-Inhalten erstellt werden.

![](assets/chlimage_1-41.png)

* **Suchabfrage** - Die Zeichenfolge, für die eine Volltextsuche ausgeführt wird, um die Listenelemente zu generieren
* **Suchen in** - Wo die Suche ausgeführt werden soll
   * Wählen Sie im **Dialogfeld &quot;Auswahl&quot;** den Speicherort in AEM aus.
   * Aktuelle Seite verwenden, wenn leer

#### Tags {#tags}

Die Liste kann mithilfe vonseiten erstellt werden, die bestimmten Tags unter einem bestimmten Ort entsprechen.

![](assets/chlimage_1-42.png)

* **Übergeordnete Seite** - Wo die Tag-Übereinstimmung beginnen sollte
   * Wählen Sie im **Dialogfeld &quot;Auswahl&quot;** den Speicherort in AEM aus.
   * Aktuelle Seite verwenden, wenn leer
* **Tags** - Welche Tags sollten erfüllt werden
   * Verwenden Sie das **Dialogfeld &quot;Durchsuchen&quot;** , um die Tags auszuwählen.
* **Übereinstimmung** - Definieren Sie, welche Art von Übereinstimmung eine Seite qualifizieren soll, damit sie in die Liste aufgenommen wird.
   * **beliebiges Tag**
   * **alle Tags**

#### Sortieroptionen {#sort-options}

Unabhängig davon, wie Sie die Liste erstellen, gibt es bestimmte Sortieroptionen, die immer definiert werden können.

![](assets/chlimage_1-43.png)

* **Reihenfolge nach** - Reihenfolge der Elemente
   * **Titel**
   * **Datum der letzten Änderung**
* **Sortierreihenfolge** - Reihenfolge, in der die Elemente angeordnet werden sollen
   * **Aufsteigend**
   * **Absteigend**
* **Max. Elemente** - Maximale Anzahl der in der Liste angezeigten Elemente.
   * Leer lassen, um alle Elemente zurückzugeben.

### Element-Einstellungen {#item-settings}

Auf der Registerkarte **&quot;Elementeinstellungen** &quot; kann die Formatierung der Listenelemente konfiguriert werden.

![](assets/chlimage_1-44.png)

* **** Linkelemente verknüpfen Elemente mit der entsprechenden Seite
* **Beschreibung**
anzeigen Beschreibung des Link-Elements
* **Datum**des Änderungsdatums
des Links anzeigen

## Design-Dialogfeld {#design-dialog}

Über das Design-Dialogfeld können Sie festlegen, welche Listentypen den Autoren-Autoren sowie den verfügbaren Elementeinstellungen erlaubt werden sollen.

### Listen-Einstellungen {#list-settings-1}

Auf der Registerkarte **&quot;Listeneinstellungen** &quot; kann das Datumsformat sowie der Listentyp definiert werden, der in der Komponente den Autoren des Inhalts zur Verfügung stehen soll.

![](assets/chlimage_1-45.png)

* **Datumsformat** - Format für die Anzeige des Änderungsdatum der letzten Änderung
* **Untergeordnete Elemente** deaktivieren: Deaktivieren Sie den Listentyp der untergeordneten Liste in der Komponente.
* **Statisch** deaktivieren: Deaktivieren Sie den statischen Listentyp in der Komponente.
* **Suche** deaktivieren - Deaktivieren Sie den Suchlistentyp in der Komponente.
* **Tags deaktivieren** - Tag-Listentyp in der Komponente deaktivieren

### Element-Einstellungen {#item-settings-1}

Auf der **Registerkarte &quot;Elementeinstellungen** &quot; können die Formatierungsoptionen für die einzelnen Listenelemente definiert werden, die in der Komponente für die Autoren verfügbar sein sollten.

![](assets/chlimage_1-46.png)

* **Verknüpfungselemente** - Option &quot;Verknüpfungselemente aktivieren&quot; im [Dialogfeld&quot; Bearbeiten&quot; aktivieren](list-v1.md#main-pars_title_550499279)
* **Beschreibungen anzeigen** - Option &quot;Beschreibungen anzeigen&quot; im [Dialogfeld&quot; Bearbeiten&quot; aktivieren](list-v1.md#main-pars_title_550499279)
* **Datum anzeigen** - Option Datum anzeigen im [Dialogfeld Bearbeiten](list-v1.md#main-pars_title_550499279)

## Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur Listenkomponente [finden Sie unter github](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/list/v1/list).

Das gesamte Kernkomponentenprojekt kann von github heruntergeladen werden.

Weitere Informationen zur Entwicklung Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Komponenten](developing.md).
