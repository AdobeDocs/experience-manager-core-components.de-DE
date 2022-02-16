---
title: Teaser-Komponente
description: Die Teaser-Komponente kann ein Bild, einen Titel, Rich-Text und optional einen Link zu weiteren Inhalten anzeigen.
role: Architect, Developer, Admin, User
exl-id: ec75e168-6f3b-4dff-8df6-06ca7dc18688
source-git-commit: 395a1669cf3e17f649c23852addc37316b923bfd
workflow-type: tm+mt
source-wordcount: '999'
ht-degree: 69%

---

# Teaser-Komponente {#teaser-component}

Die Kernkomponente „Teaser-Komponente“ kann ein Bild, einen Titel, Rich-Text und optional einen Link zu weiteren Inhalten anzeigen.

## Nutzung {#usage}

Mit der Teaser-Komponente kann der Inhaltsautor problemlos einen Teaser für weitere Inhalte erstellen, indem er ein Bild, einen Titel oder einen Rich Text verwendet und Links zu weiteren Inhalten oder anderen Aktionen erstellt.

Der Vorlagenautor kann das [Dialogfeld „Design“](#design-dialog) verwenden, um zu definieren, ob die Optionen zum Erstellen von Aktionsaufrufen und zum Hinzufügen von Links verfügbar sind sowie verschiedene Anzeigeoptionen deaktivieren. Der Inhaltsautor kann das [Dialogfeld „Konfigurieren“](#configure-dialog) verwenden, um ein Bild festzulegen, CTAs zu definieren, Titel und Beschreibungen festzulegen und Links zum jeweiligen Teaser zu konfigurieren. Es kann auf das [Dialogfeld „Bearbeiten“](image.md#edit-dialog) der [Bild-Komponente](image.md) zugegriffen werden, um das Bild des Teasers zu ändern.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Teaser-Komponente ist v2, die mit Version 2.18.0 der Kernkomponenten im Februar 2022 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|---|
| v2 | - | Kompatibel | Kompatibel |
| [v1](v1/teaser.md) | Kompatibel | Kompatibel | Kompatibel |

## Musterkomponentenausgabe {#sample-component-output}

Um die Teaser-Komponente sowie Beispiele für die Konfigurationsoptionen sowie HTML- und JSON-Ausgaben zu erhalten, besuchen Sie die [Komponentenbibliothek](https://adobe.com/go/aem_cmp_library_teaser_de).

### Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur Teaser-Komponente [finden Sie auf GitHub](https://adobe.com/go/aem_cmp_tech_teaser_v1_de).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Der Inhaltsautor kann das Dialogfeld „Konfigurieren“ verwenden, um die Eigenschaften des einzelnen Teasers zu definieren. Es gibt auch ein [Dialogfeld „Bearbeiten“](#edit-dialog) zum Bearbeiten des Teaserbilds, wenn eines ausgewählt ist.

### Registerkarte &quot;Links&quot; {#links-tab}

![Registerkarte &quot;Links&quot;im Dialogfeld &quot;Bearbeiten&quot;der Teaser-Komponente](/help/assets/teaser-edit-links.png)

Der Teaser-Titel, die Beschreibung und das Bild können von der verknüpften Seite oder von der Seite übernommen werden, die im ersten Aktionsaufruf verknüpft ist. Wenn weder ein Link noch ein Aktionsaufruf angegeben ist, werden Titel, Beschreibung und Bild von der aktuellen Seite übernommen.

* **Link** - Diese Datei verlinkt zu einer Inhaltsseite, einer externen URL oder einem Seitenanker.
* **Link in neuer Registerkarte öffnen** - Wenn diese Option aktiviert ist, wird der Link in einer neuen Browser-Registerkarte geöffnet.
* **Aktionsaufrufe** - Diese Option ermöglicht die Verknüpfung mit mehreren Zielen.
   * Die im ersten Aktionsaufruf verknüpfte Seite wird beim Vererben des Teaser-Titels, der Beschreibung oder des Bildes verwendet.

### Registerkarte &quot;Text&quot; {#text-tab}

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

### Registerkarte „Asset“ {#asset-tab}

![Registerkarte „Bild“ im Dialogfeld „Bearbeiten“ der Teaser-Komponente](/help/assets/teaser-edit-image.png)

* **Eigenes Bild von Seite übernehmen** - Verwenden Sie das in den Seiteneigenschaften der verknüpften Seite definierte Bild oder die aktuelle Seite, wenn keines gefunden wird.
* **Bild-Asset** - Ziehen Sie ein Asset aus dem [Asset-Browser](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html?lang=de) oder tippen Sie auf **durchsuchen** Option zum Hochladen aus einem lokalen Dateisystem.
   * Tippen oder klicken Sie auf **Löschen**, um das aktuell ausgewählte Bild zu deaktivieren.
   * Tippen oder klicken Sie auf **Bearbeiten**, um die [Ausgabedarstellungen des Assets](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/manage-digital-assets.html?lang=de) im Asset-Editor zu verwalten.
* **Alternativtext für Barrierefreiheit** - In diesem Feld können Sie eine Beschreibung des Bildes für sehbehinderte Benutzer definieren.
   * **Alternativtext von Seite übernehmen** - Diese Option verwendet die alternative Beschreibung des verknüpften Asset-Werts des `dc:description` Metadaten in DAM oder der aktuellen Seite, wenn kein Asset verknüpft ist.
* **Geben Sie keinen alternativen Text an** - Diese Option markiert das Bild, das von Hilfstechnologien wie Bildschirmlesehilfen ignoriert werden soll, wenn das Bild rein dekorativ ist oder anderweitig keine zusätzlichen Informationen zur Seite vermittelt.

>[!NOTE]
>
>[Dynamic Media-Funktionen](image.md#dynamic-media) sind derzeit nicht in der Teaser-Komponente verfügbar.

### Registerkarte „Stile“ {#styles-tab-edit}

![Registerkarte &quot;Stile&quot;im Dialogfeld &quot;Bearbeiten&quot;der Teaser-Listenkomponente](/help/assets/teaser-edit-styles.png)

Die Teaser-Komponente unterstützt das AEM-[Stilsystem.](/help/get-started/authoring.md#component-styling).

Verwenden Sie das Dropdown-Menü, um die Stile auszuwählen, die Sie auf die Komponente anwenden möchten. Die im Dialogfeld &quot;Bearbeiten&quot;vorgenommenen Auswahlen haben denselben Effekt wie die in der Komponenten-Symbolleiste ausgewählten.

Stile müssen für diese Komponente im [Dialogfeld &quot;Design&quot;](#design-dialog) , damit das Dropdown-Menü verfügbar ist.

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
* **Standardtitel** - Definiert das H-Tag, das vom Titel des Teasers verwendet werden soll.
* **Bilddelegat** - Information, die anzeigt, an welche Komponente der Teaser die Bildverarbeitung delegiert.

### Registerkarte „Stile“ {#styles-tab}

Die Teaser-Komponente unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).

## Adobe Client-Datenschicht {#data-layer}

Die Teaser-Komponente unterstützt die [Adobe Client-Datenschicht](/help/developing/data-layer/overview.md).
