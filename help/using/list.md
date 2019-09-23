---
title: Listenkomponente
seo-title: Listenkomponente
description: 'null'
seo-description: Die Kernkomponente „Listenkomponente“ ermöglicht die einfache Erstellung dynamischer sowie statischer Listen.
uuid: 50a572e8-b444-4f7d-82bc-5a93ebb4be95
contentOwner: Benutzer
content-type: Referenz
topic-tags: Authoring
products: SG_EXPERIENCEMANAGER/CORECOMPONENTS-new
discoiquuid: 89053323-6221-46ed-896a-31a42c55282e
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
source-git-commit: eef608fb06001485aa2c2c0b574af412ed7f15a4

---


# Listenkomponente{#list-component}

Die Kernkomponente „Listenkomponente“ ermöglicht die einfache Erstellung dynamischer sowie statischer Listen.

## Nutzung {#usage}

Die Listenkomponente kann beispielsweise zum Erstellen einer dynamischen Liste von untergeordneten Seiten oder einer statischen Liste von willkürlich definierten Elementen verwendet werden. Der Typ der verfügbaren Listen und Formatierungsoptionen kann vom Vorlagenautor im [Dialogfeld „Design“](#design-dialog) definiert werden. Der Inhaltseditor kann aus verfügbaren Listentypen und Elementen zum Formatieren der Listen im [Dialogfeld „Bearbeiten“](#edit-dialog) auswählen.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Listen-Komponente ist v2, die mit Version 2.0.0 der Kernkomponenten im Januar 2018 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v2 | Kompatibel | Kompatibel | Kompatibel |
| [v1](list-v1.md) | Kompatibel | Kompatibel | Kompatibel |

Weitere Informationen zu Kernkomponentenversionen und -freigaben finden Sie in den [Kernkomponentenversionen](versions.md).

## Musterkomponentenausgabe {#sample-component-output}

Um die Listenkomponente sowie Beispiele für die Konfigurationsoptionen sowie HTML- und JSON-Ausgaben zu erhalten, besuchen Sie die [Komponentenbibliothek](http://opensource.adobe.com/aem-core-wcm-components/library/list.html).

### Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur List Component [finden Sie auf GitHub](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/list/v2/list).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](developing.md).

## Dialogfeld „Bearbeiten“ {#edit-dialog}

Im Dialogfeld „Bearbeiten“ kann der Inhaltsautor die Liste und die Listenelemente konfigurieren.

### Registerkarte „Listeneinstellungen“ {#list-settings-tab}

Die Liste kann auf verschiedene Weise erstellt werden.

* [Untergeordnete Seiten](#child-pages)
* [Liste fester Werte](#fixed-list)
* [Suchen](#search-options)
* [Tags](#tags)

Unabhängig davon, wie die Liste erstellt wurde, gibt es [Sortieroptionen](#sort-options), die immer konfiguriert werden können.

![](assets/chlimage_1-38.png)

Je nachdem, wie der Inhaltsautor die Liste erstellt, werden die zusätzlichen Konfigurationsoptionen geändert.

#### Untergeordnete Seiten {#child-pages}

Die Liste kann aus den untergeordneten Seiten der aktuellen Seite oder einer anderen Seite bestehen.

![](assets/chlimage_1-39.png)

* **Übergeordnete Seite**
   * Die Seite, deren untergeordnete Seiten in die Liste aufgenommen werden sollen
   * Frei lassen, um aktuelle Seite zu verwenden

* **Untergeordnete Tiefe**,
Wie viele Ebenen in der Hierarchie angelegt werden sollten

#### Liste fester Werte {#fixed-list}

Die Liste kann mit einer Liste mit festen Elementen erstellt werden.

![](assets/chlimage_1-40.png)

Tippen oder klicken Sie auf die Schaltfläche **Hinzufügen**, um ein neues Element in die Liste einzufügen.

* Geben Sie Text für das Element in der Liste ein oder wählen Sie im **Dialogfeld „Auswahl“** ein Element aus AEM aus.
* Mit dem Ziehpunkt können Sie die Elemente in der Liste neu anordnen.
* Verwenden Sie das Papierkorbsymbol, um Elemente in der Liste zu löschen.

#### Suche{#search-options}

Die Liste kann mithilfe der Ergebnisse einer Suche aus AEM-Inhalten erstellt werden.

![](assets/chlimage_1-41.png)

* **Suchabfrage**
Die Zeichenfolge, für die eine Volltextsuche ausgeführt wird, um die Listenelemente zu generieren
* **Suchen in**,
Wo die Suche ausgeführt werden soll
   * Wählen Sie im **Dialogfeld „Auswahl“** den Speicherort in AEM aus
   * Aktuelle Seite verwenden, wenn leer

#### Tags {#tags}

Die Liste kann mithilfe von Seiten erstellt werden, die bestimmten Tags unter einem bestimmten Ort entsprechen.

![](assets/chlimage_1-42.png)

* **Übergeordnete Seite**
Where the tag matching should startWo die Tag-Übereinstimmung beginnen sollte
   * Wählen Sie im **Dialogfeld „Auswahl“** den Speicherort in AEM aus
   * Aktuelle Seite verwenden, wenn leer
* **Tags**,
Welche Tags sollten abgeglichen werden
   * Verwenden Sie das Dialogfeld **Durchsuchen**, um die Tags auszuwählen.
* **Übereinstimmung**
Definieren, welche Art von Übereinstimmung eine Seite qualifizieren soll, damit sie in die Liste aufgenommen wird
   * **beliebiges Tag**
   * **alle Tags**

#### Sortieroptionen {#sort-options}

Unabhängig davon, wie Sie die Liste erstellen, gibt es bestimmte Sortieroptionen, die immer definiert werden können.

![](assets/chlimage_1-43.png)

* **Reihenfolge**
Anordnung der Elemente
   * **Titel**
   * **Datum der letzten Änderung**
* **Sortierreihenfolge**
Die Reihenfolge, in der die Elemente angeordnet werden sollen
   * **Aufsteigend**
   * **Absteigend**
* **Maximale Elementanzahl**
Maximale Anzahl der in der Liste angezeigten Elemente
   * Leer lassen, um alle Elemente zurückzugeben.

### Registerkarte „Elementeinstellungen“ {#item-settings-tab}

Auf der Registerkarte „Elementeinstellungen“ kann die Formatierung der Listenelemente konfiguriert werden.

![](assets/chlimage_1-44.png)

* **Elemente verknüpfen**
Elemente mit der entsprechenden Seite verknüpfen
* **Beschreibung anzeigen**
Beschreibung des Link-Elements anzeigen
* **Datum anzeigen**
Änderungsdatum des Link-Elements anzeigen

## Dialogfeld „Design“ {#design-dialog}

Über das Dialogfeld „Design“ kann der Vorlagenautor festlegen, welche Listentypen für Inhaltsautoren erlaubt und welche Elementeinstellungen verfügbar sind.

### Listen-Einstellungen {#list-settings}

Auf der Registerkarte **Listeneinstellungen** kann das Datumsformat sowie der Listentyp definiert werden, der in der Komponente den Inhaltsautoren zur Verfügung stehen soll.

![](assets/chlimage_1-45.png)

* **Datumsformat**
Format für die Anzeige des letzten Änderungsdatums
* **Deaktivierung der untergeordneten Liste**
Untergeordnete Listentypen in der Komponente deaktivieren
* **Statischen Listentyp deaktivieren**
Deaktivierung des statischen Listentyps in der Komponente
* **Suche deaktivieren**
Deaktivieren des Suchlistentyps in der Komponente
* **Deaktivierung von Tags**
Deaktivieren des Tags-Listentyps in der Komponente

### Element-Einstellungen {#item-settings}

Auf der Registerkarte **Elementeinstellungen** können die Formatierungsoptionen für die einzelnen Listenelemente definiert werden, die in der Komponente für die Inhaltsautoren verfügbar sein sollten.

![](assets/chlimage_1-46.png)

* **Link-Elemente**
Option „Link-Elemente“ im [Dialogfeld „Bearbeiten“ aktivieren](#edit-dialog)
* **Beschreibungen anzeigen**
Option „Beschreibungen anzeigen“ im Dialogfeld [ „Bearbeiten“ aktivieren](#edit-dialog)
* **Datum anzeigen**
Option „Datum anzeigen“ im [Dialogfeld „Bearbeiten“ aktivieren](#edit-dialog)

### Registerkarte „Stile“ {#styles-tab}

Die Bildkomponente unterstützt das AEM-[Stilsystem](authoring.md#component-styling).