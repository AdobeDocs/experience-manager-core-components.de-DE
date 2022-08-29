---
title: Listenkomponente (v2)
description: Die Kernkomponente „Listenkomponente“ ermöglicht die einfache Erstellung dynamischer sowie statischer Listen.
role: Architect, Developer, Admin, User
exl-id: fa34be64-b345-45cd-baf3-571973414852
source-git-commit: 241c86240377858a73f4a022368d428da9c11100
workflow-type: tm+mt
source-wordcount: '1022'
ht-degree: 100%

---

# Listenkomponente (v2) {#list-component}

Die Kernkomponente „Listenkomponente“ ermöglicht die einfache Erstellung dynamischer sowie statischer Listen.

## Nutzung {#usage}

Die Listenkomponente kann beispielsweise zum Erstellen einer dynamischen Liste von untergeordneten Seiten oder einer statischen Liste von willkürlich definierten Elementen verwendet werden. Der Typ der verfügbaren Listen und Formatierungsoptionen kann vom Vorlagenautor im [Dialogfeld „Design“](#design-dialog) definiert werden. Der Inhaltseditor kann aus verfügbaren Listentypen und Elementen zum Formatieren der Listen im [Dialogfeld „Bearbeiten“](#edit-dialog) auswählen.

## Version und Kompatibilität {#version-and-compatibility}

In diesem Dokument wird die v1 der Listenkomponente beschrieben, die ursprünglich mit Version 2.0.0 der Kernkomponenten im Januar 2018 eingeführt wurde.

>[!CAUTION]
>
>In diesem Dokument wird die v2 der Listenkomponente beschrieben.
>
>Weitere Informationen zur aktuellen Version der Listenkomponente finden Sie im Dokument [Listenkomponente](/help/components/list.md).

## Redirects in Listen {#redirects}

Wenn eine Seite ein Redirect-Ziel hat (unabhängig davon, ob sie auf eine externe URL oder eine andere AEM verweist), dann verweist eine Liste mit Links darauf direkt auf die URL des Redirect-Ziels.

### Beispiel {#redirect-example}

* Erstellen Sie eine Seite A, die zu Seite B umleitet.
* Erstellen Sie eine Seite C, die zu `https://aemcomponents.dev` umleitet.
* Fügen Sie auf einer Seite D eine Listenkomponente ein, die die Seiten A und C enthält.
* Die entsprechenden generierten Links verweisen dann direkt auf Seite B und `https://aemcomponents.dev`

## Musterkomponentenausgabe {#sample-component-output}

Um die Listenkomponente und Beispiele für die Konfigurationsoptionen sowie HTML- und JSON-Ausgaben zu erhalten, besuchen Sie die [Komponentenbibliothek](https://adobe.com/go/aem_cmp_library_list_de).

### Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur Listenkomponente [finden Sie auf GitHub](https://adobe.com/go/aem_cmp_tech_list_v2_de).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Dialogfeld „Bearbeiten“ {#edit-dialog}

Im Dialogfeld „Bearbeiten“ kann der Inhaltsautor die Liste und die Listenelemente konfigurieren.

### Registerkarte „Listen-Einstellungen“ {#list-settings-tab}

Die Liste kann auf verschiedene Weise erstellt werden.

* [Untergeordnete Seiten](#child-pages)
* [Liste fester Werte](#fixed-list)
* [Suche](#search-options)
* [Tags](#tags)

Unabhängig davon, wie die Liste erstellt wurde, stehen Optionen für [Sortieren und ID](#sort-options) zur Verfügung, die immer konfiguriert werden können.

![Dialogfeld „Bearbeiten“ der Listenkomponente](/help/assets/v2/list-edit.png)

Je nachdem, wie der Inhaltsautor die Liste erstellt, werden die zusätzlichen Konfigurationsoptionen geändert.

#### Untergeordnete Seiten {#child-pages}

Die Liste kann aus den untergeordneten Seiten der aktuellen Seite oder einer anderen Seite bestehen.

![Optionen für untergeordnete Seiten](/help/assets/v2/list-edit-child-pages.png)

* **Übergeordnete Seite**
   * Die Seite, deren untergeordnete Seiten in die Liste aufgenommen werden sollen
   * Frei lassen, um aktuelle Seite zu verwenden

* **Untergeordnete Tiefe**,
Wie viele Ebenen in der Hierarchie angelegt werden sollten

#### Liste fester Werte {#fixed-list}

Die Liste kann mit einer Liste mit festen Elementen erstellt werden.

![Optionen für Listen fester Werte](/help/assets/v2/list-edit-fixed-list.png)

Tippen oder klicken Sie auf die Schaltfläche **Hinzufügen**, um ein neues Element in die Liste einzufügen.

* Geben Sie Text für das Element in der Liste ein oder wählen Sie im **Dialogfeld „Auswahl“** ein Element aus AEM aus.
* Mit dem Ziehpunkt können Sie die Elemente in der Liste neu anordnen.
* Verwenden Sie das Papierkorbsymbol, um Elemente in der Liste zu löschen.

#### Suche {#search-options}

Die Liste kann mithilfe der Ergebnisse einer Suche aus AEM-Inhalten erstellt werden.

![Optionen für die Suchliste](/help/assets/v2/list-edit-search.png)

* **Suchanfrage**
Die Zeichenfolge, für die eine Volltextsuche ausgeführt wird, um die Listenelemente zu generieren
* **Suche in**
Wo die Suche ausgeführt werden soll
   * Wählen Sie im **Dialogfeld „Auswahl“** den Speicherort in AEM aus
   * Aktuelle Seite verwenden, wenn leer

#### Tags {#tags}

Die Liste kann mithilfe von Seiten erstellt werden, die bestimmten Tags unter einem bestimmten Ort entsprechen.

![Optionen für die Tag-Liste](/help/assets/v2/list-edit-tags.png)

* **Übergeordnete Seite**
Wo die Tag-Übereinstimmung beginnen sollte
   * Wählen Sie im **Dialogfeld „Auswahl“** den Speicherort in AEM aus
   * Aktuelle Seite verwenden, wenn leer
* **Tags**
Welche Tags sollten abgeglichen werden
   * Verwenden Sie das Dialogfeld **Durchsuchen**, um die Tags auszuwählen.
* **Übereinstimmung**
Definieren, welche Art von Übereinstimmung eine Seite qualifizieren soll, damit sie in die Liste aufgenommen wird
   * **beliebiges Tag**
   * **alle Tags**

#### Sortieroptionen {#sort-options}

Unabhängig davon, wie Sie die Liste erstellen, gibt es bestimmte Sortieroptionen, die immer definiert werden können.

![Sortieroptionen](/help/assets/v2/list-edit-sort-options.png)

* **Sortieren nach**
Anordnung der Elemente
   * **Titel**
   * **Datum der letzten Änderung**
* **Sortierreihenfolge**
Die Reihenfolge, in der die Elemente angeordnet werden sollen
   * **Aufsteigend**
   * **Absteigend**
* **Maximale Elemente**
Maximale Anzahl der in der Liste angezeigten Elemente.
   * Leer lassen, um alle Elemente zurückzugeben.
* **ID** - Diese Option dient zur Kontrolle der eindeutigen Kennung der Komponente in der HTML-Datei und auf der [Datenschicht](/help/developing/data-layer/overview.md).
   * Wenn Sie das Feld leer lassen, wird automatisch eine eindeutige ID generiert, die Sie über die resultierende Seite finden.
   * Sofern eine ID angegeben wird, ist vom Autor sicherzustellen, dass diese eindeutig ist.
   * Änderungen der ID können sich auf das CSS-, JS- und Datenschicht-Tracking auswirken.

### Registerkarte „Element-Einstellungen“ {#item-settings-tab}

Auf der Registerkarte „Element-Einstellungen“ kann die Formatierung der Listenelemente konfiguriert werden.

![Elementeinstellungen](/help/assets/v2/list-edit-item-settings.png)

* **Elemente verknüpfen**
Elemente mit der entsprechenden Seite verknüpfen
* **Beschreibung anzeigen**
Beschreibung des Link-Elements anzeigen
* **Datum anzeigen**
Änderungsdatum des Link-Elements anzeigen

## Dialogfeld „Design“ {#design-dialog}

Über das Dialogfeld „Design“ kann der Vorlagenautor festlegen, welche Listentypen für Inhaltsautoren erlaubt und welche Elementeinstellungen verfügbar sind.

### Listen-Einstellungen {#list-settings}

Auf der Registerkarte **Listen-Einstellungen** kann das Datumsformat sowie der Listentyp definiert werden, der in der Komponente den Inhaltsautoren zur Verfügung stehen soll.

![Listeneinstellung im Dialogfeld „Design“ der Listenkomponente](/help/assets/v2/list-design-list-settings.png)

* **Datumsformat**
Format für die Anzeige des letzten Änderungsdatums
* **Untergeordnete Elemente deaktivieren**
Deaktiviert den Listentyp „untergeordnete Elemente“ in der Komponente
* **Statische Anzeige deaktivieren**
Deaktiviert den Listentyp „Statisch“ in der Komponente
* **Suche deaktivieren**
Deaktiviert den Listentyp „Suche“ in der Komponente
* **Tags deaktivieren**
Deaktiviert den Listentyp „Tags“ in der Komponente

### Elementeinstellungen {#item-settings}

Auf der Registerkarte **Element-Einstellungen** können die Formatierungsoptionen für die einzelnen Listenelemente definiert werden, die in der Komponente für die Inhaltsautoren verfügbar sein sollten.

![Elementeinstellungen im Dialogfeld „Design“ der Listenkomponente](/help/assets/v2/list-design-item-settings.png)

* **Elemente verknüpfen**
Aktiviert die Option „Elemente verknüpfen“ im [Dialogfeld „Bearbeiten“](#edit-dialog)
* **Beschreibungen anzeigen**
Aktiviert die Option „Beschreibungen anzeigen“ im [Dialogfeld „Bearbeiten“](#edit-dialog)
* **Datum anzeigen**
Aktiviert die Option „Datum anzeigen“ im [Dialogfeld „Bearbeiten“](#edit-dialog)

### Registerkarte „Arten“ {#styles-tab}

Die Bildkomponente unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).

## Adobe Client-Datenschicht {#data-layer}

Die Listenkomponente unterstützt die [Adobe Client-Datenschicht](/help/developing/data-layer/overview.md).
