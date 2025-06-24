---
title: Listenkomponente (v1)
description: Die Kernkomponente „Listenkomponente“ ermöglicht die einfache Erstellung dynamischer sowie statischer Listen.
index: n
role: Architect, Developer, Admin, User
exl-id: 510d059c-e60a-40aa-9032-66a901109f6e
source-git-commit: 92a3ec273a5be6751c1503835b9c2e5cbd61bb9e
workflow-type: tm+mt
source-wordcount: '836'
ht-degree: 100%

---


# Listenkomponente (v1) {#list-component-v}

Die Kernkomponente „Listenkomponente“ ermöglicht die einfache Erstellung dynamischer sowie statischer Listen.

## Nutzung {#usage}

Die Listenkomponente kann beispielsweise zum Erstellen einer dynamischen Liste von untergeordneten Seiten oder einer statischen Liste von willkürlich definierten Elementen verwendet werden.

Der Typ der verfügbaren Listen und Formatierungsoptionen kann vom Vorlagenautor im [Dialogfeld „Design“](#design-dialog) definiert werden. Der Inhaltseditor kann aus verfügbaren Listentypen und Elementen zum Formatieren der Listen im [Dialogfeld „Bearbeiten“](#edit-dialog) auswählen.

## Version und Kompatibilität {#version-and-compatibility}

In diesem Dokument wird die v1 der Listenkomponente beschrieben, die ursprünglich mit Version 1.0.0 der Kernkomponenten mit AEM 6.3 eingeführt wurde.

In der folgenden Tabelle ist die Kompatibilität von v1 der Listenkomponente aufgeführt.

| AEM-Version | Listenkomponente v1 |
|--- |--- |
| 6.3 | Kompatibel |
| 6.4 | Kompatibel |

>[!CAUTION]
>
>In diesem Dokument wird v1 der Listenkomponente beschrieben.
>
>Weitere Informationen zur aktuellen Version der Listenkomponente finden Sie im Dokument [Listenkomponente](/help/components/list.md).

## Musterkomponentenausgabe {#sample-component-output}

Im Folgenden finden Sie ein Beispiel von [We.Retail](https://helpx.adobe.com/de/experience-manager/6-4/sites/developing/using/we-retail.html).

### Screenshot {#screenshot}

![](/help/assets/chlimage_1-47.png)

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
>Für JSON-Exporte aus den Kernkomponenten ist Version 1.1.0 der Kernkomponenten erforderlich. Weitere Informationen finden Sie in den [Kompatibilitätsinformationen für Kernkomponenten v1](/help/versions.md).

## Dialogfeld „Bearbeiten“ {#edit-dialog}

Das Dialogfeld „Bearbeiten“ ermöglicht dem Inhaltsautor die Konfiguration der Liste und der Listenelemente.

### Listen-Einstellungen {#list-settings}

Die Liste kann auf verschiedene Weise erstellt werden.

* [Untergeordnete Seiten](#child-pages)
* [Liste fester Werte](#fixed-list)
* [Suche](#search-list)
* [Tags](#tags)

Unabhängig davon, wie die Liste erstellt wurde, gibt es [Sortieroptionen](#sort-options), die immer konfiguriert werden können.

![](/help/assets/chlimage_1-38.png)

Je nachdem, wie der Inhaltsautor die Liste erstellt, werden die zusätzlichen Konfigurationsoptionen geändert.

#### Untergeordnete Seiten {#child-pages}

Die Liste kann aus den untergeordneten Seiten der aktuellen Seite oder einer anderen Seite bestehen.

![](/help/assets/chlimage_1-39.png)

* **Übergeordnete Seite**
   * Die Seite, deren untergeordnete Seiten in die Liste aufgenommen werden sollen
   * Frei lassen, um aktuelle Seite zu verwenden
* **Untergeordnete Tiefe** – Wie viele Ebenen in der Hierarchie verwendet werden sollten

#### Liste fester Werte {#fixed-list}

Die Liste kann mit einer Liste mit festen Elementen erstellt werden.

![](/help/assets/chlimage_1-40.png)

Tippen oder klicken Sie auf die Schaltfläche **Hinzufügen**, um ein neues Element in die Liste einzufügen.

* Geben Sie Text für das Element in der Liste ein oder wählen Sie im **Dialogfeld „Auswahl“** ein Element aus AEM aus.
* Mit dem Ziehpunkt können Sie die Elemente in der Liste neu anordnen.
* Verwenden Sie das Papierkorbsymbol, um Elemente in der Liste zu löschen.

#### Suche {#search-list}

Die Liste kann mithilfe der Ergebnisse einer Suche aus AEM-Inhalten erstellt werden.

![](/help/assets/chlimage_1-41.png)

* **Suchabfrage** – Die Zeichenfolge, für die eine Volltextsuche ausgeführt wird, um die Listenelemente zu generieren
* **Suchen in** – Wo die Suche ausgeführt werden soll
   * Wählen Sie im **Dialogfeld „Auswahl“** den Speicherort in AEM aus
   * Aktuelle Seite verwenden, wenn leer

#### Tags {#tags}

Die Liste kann mithilfe von Seiten erstellt werden, die bestimmten Tags unter einem bestimmten Ort entsprechen.

![](/help/assets/chlimage_1-42.png)

* **Übergeordnete Seite** – Wo das Tag-Matching beginnen sollte
   * Wählen Sie im **Dialogfeld „Auswahl“** den Speicherort in AEM aus
   * Aktuelle Seite verwenden, wenn leer
* **Tags** – Welche Tags sollten abgestimmt werden
   * Verwenden Sie das Dialogfeld **Durchsuchen**, um die Tags auszuwählen.
* **Übereinstimmung** – Definieren Sie, welche Art von Übereinstimmung eine Seite dazu qualifizieren soll, damit sie in die Liste aufgenommen wird.
   * **beliebiges Tag**
   * **alle Tags**

#### Sortieroptionen {#sort-options}

Unabhängig davon, wie Sie die Liste erstellen, gibt es bestimmte Sortieroptionen, die immer definiert werden können.

![](/help/assets/chlimage_1-43.png)

* **Sortieren nach** – Gewünschte Reihenfolge der Elemente
   * **Titel**
   * **Datum der letzten Änderung**
* **Sortierreihenfolge** – Reihenfolge, in der die Elemente angeordnet werden sollen
   * **Aufsteigend**
   * **Absteigend**
* **Maximale Elemente** – die maximale Anzahl der in der Liste angezeigten Elementen.
   * Leer lassen, um alle Elemente zurückzugeben.

### Elementeinstellungen {#item-settings}

Auf der Registerkarte **Elementeinstellungen** kann die Formatierung der Listenelemente konfiguriert werden.

![](/help/assets/chlimage_1-44.png)

* **Elemente verknüpfen**
Elemente mit der entsprechenden Seite verknüpfen
* **Beschreibung anzeigen**
Beschreibung des Link-Elements anzeigen
* **Datum anzeigen**
Änderungsdatum des Link-Elements anzeigen

## Dialogfeld „Design“ {#design-dialog}

Über das Dialogfeld „Design“ kann der Vorlagenautor festlegen, welche Listentypen für Inhaltsautoren erlaubt und welche Elementeinstellungen verfügbar sind.

### Listen-Einstellungen {#list-settings-1}

Auf der Registerkarte **Listen-Einstellungen** kann das Datumsformat sowie der Listentyp definiert werden, der in der Komponente den Inhaltsautoren zur Verfügung stehen soll.

![](/help/assets/chlimage_1-45.png)

* **Datumsformat** – Format für die Anzeige des letzten Bearbeitungsdatums
* **Untergeordnete deaktivieren** – Deaktiviert den untergeordneten Listentyp in der Komponente.
* **Statisch deaktivieren** – Deaktiviert den statischen Listentyp in der Komponente
* **Suche deaktivieren** – Deaktiviert den Suchlistentyp in der Komponente.
* **Tags deaktivieren** – Deaktiviert den Tag-Listentyp in der Komponente

### Elementeinstellungen {#item-settings-1}

Auf der Registerkarte **Element-Einstellungen** können die Formatierungsoptionen für die einzelnen Listenelemente definiert werden, die in der Komponente für die Inhaltsautoren verfügbar sein sollten.

![](/help/assets/chlimage_1-46.png)

* **Elemente verknüpfen** – Aktivieren Sie die Option Verknüpfungselemente im [Dialogfeld „Bearbeiten“](#edit-dialog)
* **Beschreibungen anzeigen** – Aktivieren Sie die Option „Beschreibungen anzeigen“ im [Dialogfeld „Bearbeiten“](#edit-dialog)
* **Datum anzeigen** – Aktivieren Sie die Option „Datum anzeigen“ im [Dialogfeld „Bearbeiten“](#edit-dialog)

## Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur Listenkomponente [finden Sie auf GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/list/v1/list).

Das gesamte Kernkomponentenprojekt kann von GitHub heruntergeladen werden.

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).
