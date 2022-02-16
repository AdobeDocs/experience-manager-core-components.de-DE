---
title: Teaser-Komponente (v1)
description: Die Teaser-Komponente kann ein Bild, einen Titel, Rich-Text und optional einen Link zu weiteren Inhalten anzeigen.
role: Architect, Developer, Admin, User
source-git-commit: f8aa86d58ba71ede3c3cd867c45aafff06923325
workflow-type: tm+mt
source-wordcount: '748'
ht-degree: 91%

---


# Teaser-Komponente (v1) {#teaser-component}

Die Kernkomponente „Teaser-Komponente“ kann ein Bild, einen Titel, Rich-Text und optional einen Link zu weiteren Inhalten anzeigen.

## Nutzung {#usage}

Mit der Teaser-Komponente kann der Inhaltsautor problemlos einen Teaser für weitere Inhalte erstellen, indem er ein Bild, einen Titel oder einen Rich Text verwendet und Links zu weiteren Inhalten oder anderen Aktionen erstellt.

Der Vorlagenautor kann das [Dialogfeld „Design“](#design-dialog) verwenden, um zu definieren, ob die Optionen zum Erstellen von Aktionsaufrufen und zum Hinzufügen von Links verfügbar sind sowie verschiedene Anzeigeoptionen deaktivieren. Der Inhaltsautor kann das [Dialogfeld „Konfigurieren“](#configure-dialog) verwenden, um ein Bild festzulegen, CTAs zu definieren, Titel und Beschreibungen festzulegen und Links zum jeweiligen Teaser zu konfigurieren. Es kann auf das [Dialogfeld „Bearbeiten“](image-v1.md#edit-dialog) der [Bild-Komponente](image-v1.md) zugegriffen werden, um das Bild des Teasers zu ändern.

## Version und Kompatibilität {#version-and-compatibility}

In diesem Dokument wird die Version 1 der Teaser-Komponente beschrieben, die mit Version 2.1.0 der Kernkomponenten im Juli 2018 eingeführt wurde.

>[!CAUTION]
>
>In diesem Dokument wird v1 der Teaser-Komponente beschrieben.
>
>Weitere Informationen zur aktuellen Version der Teaser-Komponente finden Sie unter [Teaser-Komponente](/help/components/teaser.md) Dokument.

## Musterkomponentenausgabe {#sample-component-output}

Um die Teaser-Komponente sowie Beispiele für die Konfigurationsoptionen sowie HTML- und JSON-Ausgaben zu erhalten, besuchen Sie die [Komponentenbibliothek](https://adobe.com/go/aem_cmp_library_teaser_de).

### Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur Teaser-Komponente [finden Sie auf GitHub](https://adobe.com/go/aem_cmp_tech_teaser_v1_de).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Der Inhaltsautor kann das Dialogfeld „Konfigurieren“ verwenden, um die Eigenschaften des einzelnen Teasers zu definieren. Es gibt auch ein [Dialogfeld „Bearbeiten“](#edit-dialog) zum Bearbeiten des Teaserbilds, wenn eines ausgewählt ist.

### Bild {#image}

![Registerkarte „Bild“ im Dialogfeld „Bearbeiten“ der Teaser-Komponente](/help/assets/teaser-edit-image.png)

* **Bild-Asset**
   * Ziehen Sie ein Asset aus dem [Asset-Browser](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html?lang=de) oder tippen Sie auf die Option **Durchsuchen**, um es von einem lokalen Dateisystem hochzuladen.
   * Tippen oder klicken Sie auf **Löschen**, um das aktuell ausgewählte Bild zu deaktivieren.
   * Tippen oder klicken Sie auf **Bearbeiten**, um die [Ausgabedarstellungen des Assets](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/manage-digital-assets.html?lang=de) im Asset-Editor zu verwalten.

>[!NOTE]
>
>[Dynamic Media-Funktionen](image-v1.md#dynamic-media) sind derzeit nicht in der Teaser-Komponente verfügbar.

### Text {#text}

![Registerkarte „Text“ im Dialogfeld „Bearbeiten“ der Teaser-Komponente](/help/assets/teaser-edit-text.png)

* **Vortitel** - Der Vortitel wird vor dem Titel des Teasers angezeigt.
* **Titel** - Definiert einen Titel, der als Überschrift für den Teaser angezeigt wird.
   * **Titel von verknüpfter Seite übernehmen** - Bei Aktivierung dieser Option wird der Titel mit dem Titel der verknüpften Seite ausgefüllt.
* **Beschreibung** - Definiert eine Beschreibung, die als Unter-Überschrift für den Teaser angezeigt wird.
   * **Beschreibung von verknüpfter Seite übernehmen** - Bei Aktivierung dieser Option wird die Beschreibung mit der Beschreibung der verknüpften Seite ausgefüllt.
* **ID** – Diese Option dient zur Kontrolle der eindeutigen Kennung der Komponente in der HTML-Datei und auf der [Datenschicht](/help/developing/data-layer/overview.md).
   * Wenn Sie das Feld leer lassen, wird automatisch eine eindeutige ID generiert, die Sie über die resultierende Seite finden.
   * Sofern eine ID angegeben wird, ist vom Autor sicherzustellen, dass diese eindeutig ist.
   * Änderungen der ID können sich auf das CSS-, JS- und Datenschicht-Tracking auswirken.

### Verknüpfung und Aktionen {#links-actions}

![Registerkarte „Link“ im Dialogfeld „Bearbeiten“ der Teaser-Komponente](/help/assets/teaser-edit-link.png)

* **Verknüpfung** - Link, der auf den Teaser angewendet wird. Verwenden Sie den Pfad-Browser, um das Link-Ziel auszuwählen.
* **Aktionsaufrufe ermöglichen** - Bei Aktivierung dieser Option können Aktionsaufrufe definiert werden. Der erste Link zu Aktionsaufrufen in der Liste wird als Link für andere Teaser-Elemente verwendet.

## Dialogfeld „Bearbeiten“ {#edit-dialog}

Die Teaser-Komponente delegiert das Rendern von Bildern an die [Bild-Komponente](image-v1.md). Daher [Dialogfeld &quot;Bearbeiten&quot;](image-v1.md#edit-dialog der Bildkomponente ist für den Inhaltsautor verfügbar, um das Teaser-Bild zu bearbeiten.

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
