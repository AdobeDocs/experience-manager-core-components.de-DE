---
title: Teaser-Komponente
seo-title: Teaser-Komponente
description: Die Teaser-Komponente kann ein Bild, einen Titel, Rich-Text und optional einen Link zu weiteren Inhalten anzeigen.
seo-description: Die Teaser-Komponente kann ein Bild, einen Titel, Rich-Text und optional einen Link zu weiteren Inhalten anzeigen.
uuid: 46989314-df 37-448 b -8562-c 707043 f 2160
contentOwner: Bohnert
content-type: Referenz
topic-tags: Kernkomponenten
discoiquuid: e 597 c 18 e -3643-41 be -9878-4 a 7872 f 1 ab 90
translation-type: tm+mt
source-git-commit: 1243d6cc1b0b015ee2f37ae89d0e2e42d366cc02

---


# Teaser-Komponente{#teaser-component}

Die Core Component Teaser-Komponente kann ein Bild, einen Titel, Rich-Text und optional einen Link zu weiteren Inhalten anzeigen.

## Nutzung {#usage}

Mit der Teaser-Komponente kann der Inhaltsautor problemlos einen Teaser für weitere Inhalte erstellen, indem Sie ein Bild, einen Titel oder einen Rich Text verwenden und Links zu weiteren Inhalten oder anderen Aktionen erstellen.

Der Vorlagenautor kann das [Design-Dialogfeld](#design-dialog) verwenden, um zu definieren, ob die Optionen zum Erstellen von Aktionsaufrufen und zum Hinzufügen von Links sowie zum Deaktivieren verschiedener Anzeigeoptionen verfügbar sind. Der Inhaltsautor kann das [Konfigurationsdialogfeld](#configure-dialog) verwenden, um ein Bild festzulegen, ctas festzulegen, Titel und Beschreibungen festzulegen und Links zum jeweiligen Teaser zu konfigurieren. Auf das Dialogfeld [&quot;Bearbeiten&quot;](image.md#edit-dialog) der [Image-Komponente](image.md) kann zugegriffen werden, um den Teaser-Image zu ändern.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Teaser-Komponente ist v 1, die mit Version 2.1.0 der Kernkomponenten im Juli 2018 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|---|---|---|---|
| v1 | Kompatibel | Kompatibel | Kompatibel |

## Musterkomponentenausgabe {#sample-component-output}

Im Folgenden finden Sie ein Beispiel aus [We. Retail](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html).

### Screenshot {#screenshot}

![](assets/screen_shot_2018-07-04at145042.png)

### Komponentenbibliothek

Rufen Sie die [Komponentenbibliothek auf, um die Teaser-Komponente sowie Beispiele für die Konfigurationsoptionen sowie HTML- und JSON-Ausgaben zu erhalten](http://opensource.adobe.com/aem-core-wcm-components/library/teaser.html).

### Technische Details {#technical-details}

Die aktuellste technische Dokumentation zur Teaser-Komponente [finden Sie unter github](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/teaser/v1/teaser).

Weitere Informationen zur Entwicklung Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Komponenten](developing.md).

## Dialogfeld konfigurieren {#configure-dialog}

Der Inhaltsautor kann das Konfigurationsdialogfeld verwenden, um die Eigenschaften des einzelnen Teasers zu definieren. Es gibt auch [ein Dialogfeld zum Bearbeiten](#edit-dialog) des Teaserbilds, wenn eine ausgewählt ist.

### image (Bild){#image}

![](assets/screen_shot_2018-07-03at104125.png)

* **Bild-Asset**
   * Legen Sie ein Asset aus dem [Asset-Browser ab](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/author-environment-tools.html) oder tippen Sie auf die **Durchsuchen** -Option, um es aus einem lokalen Dateisystem hochzuladen.
   * Tippen oder klicken **Sie auf Leeren** , um das aktuell ausgewählte Bild zu deaktivieren.
   * Tippen oder klicken **Sie auf Bearbeiten** , um [die Darstellungen des Assets](https://helpx.adobe.com/experience-manager/6-5/assets/using/managing-assets-touch-ui.html) im Asset Editor zu mange.

### Text {#text}

![](assets/screen_shot_2018-07-03at104138.png)

* **Title**
Definiert einen Titel, der als Überschrift für den Teaser angezeigt wird.
* **Titel von verknüpfte Seite**
abrufen Wenn aktiviert, wird der Titel mit dem Titel der verknüpften Seite ausgefüllt.
* **Beschreibung**
Definiert eine Beschreibung, die als Überschrift des Teasers angezeigt wird.
* **Beschreibung von verknüpfte Seite**
erhalten, Wenn aktiviert, wird die Beschreibung mit der Beschreibung der verknüpften Seite ausgefüllt.

### Links und Aktionen {#links-actions}

![](assets/screen_shot_2018-07-03at104146.png)

* **Link Link**
auf den Teaser angewendet. Verwenden Sie den Pfad-Browser, um das Link-Ziel auszuwählen.
* **Aktivieren von Aktionsaufrufen**, wenn aktiviert, ermöglicht die Definition von Aktionsaufrufen. Der erste Link-zu-Action-Link in der Liste wird als Link für andere Teaser-Elemente verwendet.

## Dialogfeld bearbeiten {#edit-dialog}

Die Teaser-Komponente überträgt das Bild-Rendern an die [Image-Komponente](image.md). Daher wird das [Dialogfeld &quot;Bearbeiten]&quot; (image. md # edit-dialog der Image-Komponente verfügbar) dem Inhaltsautor zur Bearbeitung des Teaserbilds zur Verfügung gestellt.

## Design-Dialogfeld {#design-dialog}

Das Design-Dialogfeld ermöglicht es dem Vorlagenautor, die Teaser-Optionen zu definieren, die der Inhaltsautor bei Verwendung dieser Komponente hat.

### Teaser-Registerkarte {#teaser-tab}

![](assets/screen_shot_2018-07-03at105958.png)

* **Aktionsaufrufe**
   * **Aufrufen von Aktionsaufrufen** ausblenden der Option **&quot;Aktionsaufruf** ausblenden&quot; für Inhaltsautoren
* **Elemente**
   * **Titel ausblenden**
      * Blendet **die Option &quot;Titel&quot;** für Autoren von Inhalten aus.
      * Wenn ausgewählt, wird der **Titeltyp** ausgeblendet.
   * **Beschreibung**
ausblenden Option Die Option **Beschreibung** ausblenden für Autoren ausblenden
* **Titeltyp**
Definiert das H-Tag, das vom Titel des Teasers verwendet werden soll.
* **Links**
   * **Verknüpfen Sie das Bild**
nicht, wenn ausgewählt, wird das Teaser-Bild nicht verknüpft.
   * **Verknüpfen Sie den Titel**
nicht, wenn ausgewählt, der Teaser-Titel ist nicht verknüpft.

### Stile Registerkarte {#styles-tab}

Die Teaser-Komponente unterstützt das AEM [-Stilsystem](authoring.md#component-styling).
