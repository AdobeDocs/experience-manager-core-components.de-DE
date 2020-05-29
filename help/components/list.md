---
title: Listenkomponente
description: Die Kernkomponente „Listenkomponente“ ermöglicht die einfache Erstellung dynamischer sowie statischer Listen.
translation-type: tm+mt
source-git-commit: c186e9ec3944d785ab0376769cf7f2307049a809
workflow-type: tm+mt
source-wordcount: '968'
ht-degree: 80%

---


# Listenkomponente{#list-component}

Die Kernkomponente „Listenkomponente“ ermöglicht die einfache Erstellung dynamischer sowie statischer Listen.

## Nutzung {#usage}

Die Listenkomponente kann beispielsweise zum Erstellen einer dynamischen Liste von untergeordneten Seiten oder einer statischen Liste von willkürlich definierten Elementen verwendet werden. Der Typ der verfügbaren Listen und Formatierungsoptionen kann vom Vorlagenautor im [Dialogfeld „Design“](#design-dialog) definiert werden. Der Inhaltseditor kann aus verfügbaren Listentypen und Elementen zum Formatieren der Listen im [Dialogfeld „Bearbeiten“](#edit-dialog) auswählen.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Listen-Komponente ist v2, die mit Version 2.0.0 der Kernkomponenten im Januar 2018 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.3 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |--- |---|
| v2 | - | Kompatibel | Kompatibel | Kompatibel |
| [v1](v1/list-v1.md) | Kompatibel | Kompatibel | Kompatibel | - |

Weitere Informationen zu Kernkomponentenversionen und -freigaben finden Sie in den [Kernkomponentenversionen](/help/versions.md).

## Musterkomponentenausgabe {#sample-component-output}

Um die Listenkomponente und Beispiele für die Konfigurationsoptionen sowie HTML- und JSON-Ausgaben zu erhalten, besuchen Sie die [Komponentenbibliothek](https://adobe.com/go/aem_cmp_library_list).

### Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur Listenkomponente [finden Sie auf GitHub](https://adobe.com/go/aem_cmp_tech_list_v2).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Dialogfeld „Bearbeiten“ {#edit-dialog}

Im Dialogfeld „Bearbeiten“ kann der Inhaltsautor die Liste und die Listenelemente konfigurieren.

### Registerkarte „Listeneinstellungen“ {#list-settings-tab}

Die Liste kann auf verschiedene Weise erstellt werden.

* [Untergeordnete Seiten](#child-pages)
* [Liste fester Werte](#fixed-list)
* [Suchen](#search-options)
* [Tags](#tags)

Regardless of how the list is built, there are [Sort and ID Options](#sort-options) that can always be configured.

![Dialogfeld &quot;Bearbeiten&quot;der Liste](/help/assets/list-edit.png)

Je nachdem, wie der Inhaltsautor die Liste erstellt, werden die zusätzlichen Konfigurationsoptionen geändert.

#### Untergeordnete Seiten {#child-pages}

Die Liste kann aus den untergeordneten Seiten der aktuellen Seite oder einer anderen Seite bestehen.

![Untergeordnete Seitenoptionen](/help/assets/list-edit-child-pages.png)

* **Übergeordnete Seite**
   * Die Seite, deren untergeordnete Seiten in die Liste aufgenommen werden sollen
   * Frei lassen, um aktuelle Seite zu verwenden

* **Untergeordnete Tiefe**,
Wie viele Ebenen in der Hierarchie angelegt werden sollten

#### Liste fester Werte {#fixed-list}

Die Liste kann mit einer Liste mit festen Elementen erstellt werden.

![Optionen für behobene Liste](/help/assets/list-edit-fixed.png)

Tippen oder klicken Sie auf die Schaltfläche **Hinzufügen**, um ein neues Element in die Liste einzufügen.

* Geben Sie Text für das Element in der Liste ein oder wählen Sie im **Dialogfeld „Auswahl“** ein Element aus AEM aus.
* Mit dem Ziehpunkt können Sie die Elemente in der Liste neu anordnen.
* Verwenden Sie das Papierkorbsymbol, um Elemente in der Liste zu löschen.

#### Suche{#search-options}

Die Liste kann mithilfe der Ergebnisse einer Suche aus AEM-Inhalten erstellt werden.

![Suchoptionen für Listen](/help/assets/list-edit-search.png)

* **Suchabfrage**
Die Zeichenfolge, für die eine Volltextsuche ausgeführt wird, um die Listenelemente zu generieren
* **Suchen in**,
Wo die Suche ausgeführt werden soll
   * Wählen Sie im **Dialogfeld „Auswahl“** den Speicherort in AEM aus
   * Aktuelle Seite verwenden, wenn leer

#### Tags {#tags}

Die Liste kann mithilfe von Seiten erstellt werden, die bestimmten Tags unter einem bestimmten Ort entsprechen.

![Optionen zur Liste von Tags](/help/assets/list-edit-tags.png)

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

![Sortieroptionen](/help/assets/list-edit-sort-options.png)

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
* **ID** - Diese Option ermöglicht die Steuerung des eindeutigen Bezeichners der Komponente im HTML und in der [Datenschicht](/help/developing/data-layer/overview.md).
   * Wenn Sie das Feld leer lassen, wird automatisch eine eindeutige ID generiert und Sie können die resultierende Seite überprüfen.
   * Wenn eine ID angegeben wird, muss der Autor sicherstellen, dass sie eindeutig ist.
   * Eine Änderung der ID kann sich auf die Verfolgung von CSS, JS und Datenschichten auswirken.

### Registerkarte „Elementeinstellungen“ {#item-settings-tab}

Auf der Registerkarte „Elementeinstellungen“ kann die Formatierung der Listenelemente konfiguriert werden.

![Elementeinstellungen](/help/assets/list-edit-items.png)

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

![Einstellung der Liste des Designdialogs der Liste-Komponente](/help/assets/list-design-list-settings.png)

* **Datumsformat**
Format für die Anzeige des letzten Änderungsdatums
* **Untergeordnete Elemente** deaktivieren Der Typ der untergeordneten Liste in der Komponente
* **Deaktivieren Sie static** Deaktivieren Sie den Typ der statischen Liste in der Komponente
* **Suche** deaktivierenDeaktivieren Sie den Liste-Typ der Suche in der Komponente
* **Tags** deaktivieren Sie den Listen-Typ der Tags in der Komponente

### Element-Einstellungen {#item-settings}

Auf der Registerkarte **Elementeinstellungen** können die Formatierungsoptionen für die einzelnen Listenelemente definiert werden, die in der Komponente für die Inhaltsautoren verfügbar sein sollten.

![Einstellungen des Designdialogfelds der Liste-Komponente](/help/assets/list-design-item-settings.png)

* **Verknüpfungselemente** Option &quot;Verknüpfungselemente aktivieren&quot;im Dialogfeld &quot; [Bearbeiten&quot;](#edit-dialog)
* **Beschreibungen** anzeigenOption &quot;Beschreibungen anzeigen&quot;im Dialogfeld &quot; [Bearbeiten&quot;anzeigen](#edit-dialog)
* **Datum** anzeigenOption Datum anzeigen im Dialogfeld [bearbeiten](#edit-dialog)

### Registerkarte „Stile“ {#styles-tab}

Die Bildkomponente unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).
