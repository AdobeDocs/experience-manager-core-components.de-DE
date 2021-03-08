---
title: Teaser-Komponente
description: Die Teaser-Komponente kann ein Bild, einen Titel, Rich-Text und optional einen Link zu weiteren Inhalten anzeigen.
translation-type: ht
source-git-commit: d3ebcea5fa1523c1a986841cd3d1a64e16e85f6d
workflow-type: ht
source-wordcount: '775'
ht-degree: 100%

---


# Teaser-Komponente {#teaser-component}

Die Kernkomponente Teaser-Komponente kann ein Bild, einen Titel, Rich-Text und optional einen Link zu weiteren Inhalten anzeigen.

## Verwendung {#usage}

Mit der Teaser-Komponente kann der Inhaltsautor problemlos einen Teaser für weitere Inhalte erstellen, indem er ein Bild, einen Titel oder einen Rich Text verwendet und Links zu weiteren Inhalten oder anderen Aktionen erstellt.

Der Vorlagenautor kann das [Dialogfeld „Design“](#design-dialog) verwenden, um zu definieren, ob die Optionen zum Erstellen von Aktionsaufrufen und zum Hinzufügen von Links verfügbar sind sowie verschiedene Anzeigeoptionen deaktivieren. Der Inhaltsautor kann das [Dialogfeld „Konfigurieren“](#configure-dialog) verwenden, um ein Bild festzulegen, CTAs zu definieren, Titel und Beschreibungen festzulegen und Links zum jeweiligen Teaser zu konfigurieren. Es kann auf das [Dialogfeld „Bearbeiten“](image.md#edit-dialog) der [Bild-Komponente](image.md) zugegriffen werden, um das Bild des Teasers zu ändern.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Teaser-Komponente ist v1, die mit Version 2.1.0 der Kernkomponenten im Juli 2018 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|---|
| v1 | Kompatibel | Kompatibel | Kompatibel |

## Musterkomponentenausgabe {#sample-component-output}

Um die Teaser-Komponente sowie Beispiele für die Konfigurationsoptionen sowie HTML- und JSON-Ausgaben zu erhalten, besuchen Sie die [Komponentenbibliothek](https://adobe.com/go/aem_cmp_library_teaser_de).

### Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur Teaser-Komponente [finden Sie auf GitHub](https://adobe.com/go/aem_cmp_tech_teaser_v1).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Der Inhaltsautor kann das Dialogfeld „Konfigurieren“ verwenden, um die Eigenschaften des einzelnen Teasers zu definieren. Es gibt auch ein [Dialogfeld „Bearbeiten“](#edit-dialog) zum Bearbeiten des Teaserbilds, wenn eines ausgewählt ist.

### Bild {#image}

![Registerkarte „Bild“ im Dialogfeld „Bearbeiten“ der Teaser-Komponente](/help/assets/teaser-edit-image.png)

* **Bild-Asset**
   * Ziehen Sie ein Asset aus dem [Asset-Browser](https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.translate.html) oder tippen Sie auf die Option **Durchsuchen**, um es von einem lokalen Dateisystem hochzuladen.
   * Tippen oder klicken Sie auf **Löschen**, um das aktuell ausgewählte Bild zu deaktivieren.
   * Tippen oder klicken Sie auf **Bearbeiten**, um die [Ausgabedarstellungen des Assets](https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/assets/manage/manage-digital-assets.translate.html) im Asset-Editor zu verwalten.

>[!NOTE]
>
>[Dynamic Media-Funktionen](image.md#dynamic-media) sind derzeit nicht in der Teaser-Komponente verfügbar.

### Text {#text}

![Registerkarte „Text“ im Dialogfeld „Bearbeiten“ der Teaser-Komponente](/help/assets/teaser-edit-text.png)

* **Vortitel** - Der Vortitel wird vor dem Titel des Teasers angezeigt.
* **Titel** - Definiert einen Titel, der als Überschrift für den Teaser angezeigt wird.
   * **Titel von verknüpfter Seite übernehmen** - Bei Aktivierung dieser Option wird der Titel mit dem Titel der verknüpften Seite ausgefüllt.
* **Beschreibung** - Definiert eine Beschreibung, die als Unter-Überschrift für den Teaser angezeigt wird.
   * **Beschreibung von verknüpfter Seite übernehmen** - Bei Aktivierung dieser Option wird die Beschreibung mit der Beschreibung der verknüpften Seite ausgefüllt.
* **ID** - Diese Option dient zur Kontrolle der eindeutigen Kennung der Komponente in der HTML-Datei und auf der [Datenschicht](/help/developing/data-layer/overview.md).
   * Wenn Sie das Feld leer lassen, wird automatisch eine eindeutige ID generiert, die Sie über die resultierende Seite finden.
   * Sofern eine ID angegeben wird, ist vom Autor sicherzustellen, dass diese eindeutig ist.
   * Änderungen der ID können sich auf das CSS-, JS- und Datenschicht-Tracking auswirken.

### Verknüpfung und Aktionen {#links-actions}

![Registerkarte „Link“ im Dialogfeld „Bearbeiten“ der Teaser-Komponente](/help/assets/teaser-edit-link.png)

* **Verknüpfung** - Link, der auf den Teaser angewendet wird. Verwenden Sie den Pfad-Browser, um das Link-Ziel auszuwählen.
* **Aktionsaufrufe ermöglichen** - Bei Aktivierung dieser Option können Aktionsaufrufe definiert werden. Der erste Link zu Aktionsaufrufen in der Liste wird als Link für andere Teaser-Elemente verwendet.

## Dialogfeld „Bearbeiten“ {#edit-dialog}

Die Teaser-Komponente delegiert das Rendern von Bildern an die [Bild-Komponente](image.md). Daher wird das [Dialogfeld „Bearbeiten“] dem Inhaltsautor zur Bearbeitung des Teaserbilds zur Verfügung gestellt.

## Dialogfeld „Design“ {#design-dialog}

Das Dialogfeld „Design“ ermöglicht es dem Vorlagenautor, die Teaser-Optionen zu definieren, die der Inhaltsautor bei Verwendung dieser Komponente hat.

### Registerkarte „Teaser“ {#teaser-tab}

![Dialogfeld „Design“ der Teaser-Komponente](/help/assets/teaser-design.png)

* **Aktionsaufrufe**
   * **Aktionsaufrufe deaktivieren** - Blendet die Option **Aktionsaufrufe** für Inhaltsautoren aus.
* **Elemente**
   * **Vortitel ausblenden** - Blendet die Option **Vortitel** für Inhaltsautoren aus.
   * **Titel ausblenden** - Blendet die Option **Titel** für Inhaltsautoren aus.
      * Bei Auswahl der Option wird der **Titeltyp** ausgeblendet.
   * **Beschreibung ausblenden** - Blendet die Option **Beschreibung** für Inhaltsautoren aus.
* **Titeltyp** - Definiert das H-Tag, das vom Titel des Teasers verwendet werden soll.
* **Links**
   * **Bild nicht verknüpfen** - Bei Auswahl dieser Option wird das Teaser-Bild nicht verknüpft.
   * **Titel nicht verknüpfen** - Bei Auswahl dieser Option wird der Teaser-Titel nicht verknüpft.
* **Bilddelegat** - Information, die anzeigt, an welche Komponente der Teaser die Bildverarbeitung delegiert.

### Registerkarte „Stile“ {#styles-tab}

Die Teaser-Komponente unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).

## Adobe Client-Datenschicht {#data-layer}

Die Teaser-Komponente unterstützt die [Adobe Client-Datenschicht](/help/developing/data-layer/overview.md).
