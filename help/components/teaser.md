---
title: Teaser-Komponente
description: Die Teaser-Komponente kann ein Bild, einen Titel, Rich-Text und optional einen Link zu weiteren Inhalten anzeigen.
role: Architect, Developer, Admin, User
exl-id: ec75e168-6f3b-4dff-8df6-06ca7dc18688
source-git-commit: 6fbc781db555bc6abaed1d122a9a8756e3d53222
workflow-type: ht
source-wordcount: '1046'
ht-degree: 100%

---

# Teaser-Komponente {#teaser-component}

Die Kernkomponente „Teaser-Komponente“ kann ein Bild, einen Titel, Rich-Text und optional einen Link zu weiteren Inhalten anzeigen.

## Nutzung {#usage}

Mit der Teaser-Komponente kann der Inhaltsautor problemlos einen Teaser für weitere Inhalte erstellen, indem er ein Bild, einen Titel oder einen Rich Text verwendet und Links zu weiteren Inhalten oder anderen Aktionen erstellt.

Der Vorlagenautor kann das [Dialogfeld „Design“](#design-dialog) verwenden, um zu definieren, ob die Optionen zum Erstellen von Aktionsaufrufen und zum Hinzufügen von Links verfügbar sind sowie verschiedene Anzeigeoptionen deaktivieren. Der Inhaltsautor kann das [Dialogfeld „Konfigurieren“](#configure-dialog) verwenden, um ein Bild festzulegen, CTAs zu definieren, Titel und Beschreibungen festzulegen und Links zum jeweiligen Teaser zu konfigurieren. Es kann auf das [Dialogfeld „Bearbeiten“](image.md#edit-dialog) der [Bild-Komponente](image.md) zugegriffen werden, um das Bild des Teasers zu ändern.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Teaser-Komponente ist v2, die mit Version 2.18.0 der Kernkomponenten im Februar 2022 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|---|---|---|---|---|
| v2 | – | Kompatibel | Kompatibel | Kompatibel |
| [v1](v1/teaser.md) | Kompatibel | Kompatibel | – | Kompatibel |

## Unterstützung für Remote Assets {#remote-assets}

Die Teaser-Komponente (ab [Version 2.23.2](/help/versions.md)) unterstützt Remote-Assets. [Sobald konfiguriert,](/help/developing/remote-assets.md) können Sie Assets aus einem Remote-Dienst für Ihre Teaser-Komponente auswählen.

## Musterkomponentenausgabe {#sample-component-output}

Um die Teaser-Komponente sowie Beispiele für die Konfigurationsoptionen sowie HTML- und JSON-Ausgaben zu erhalten, besuchen Sie die [Komponentenbibliothek](https://adobe.com/go/aem_cmp_library_teaser_de).

### Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur Teaser-Komponente [finden Sie auf GitHub](https://adobe.com/go/aem_cmp_tech_teaser_v1_de).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Der Inhaltsautor kann das Dialogfeld „Konfigurieren“ verwenden, um die Eigenschaften des einzelnen Teasers zu definieren. Es gibt auch ein [Dialogfeld „Bearbeiten“](#edit-dialog) zum Bearbeiten des Teaserbilds, wenn eines ausgewählt ist.

### Registerkarte „Links“ {#links-tab}

![Registerkarte „Links“ im Dialogfeld „Bearbeiten“ der Teaser-Komponente](/help/assets/teaser-edit-links.png)

Der Teaser-Titel, die Beschreibung und das Bild können von der verknüpften Seite oder von der Seite übernommen werden, die im ersten Aktionsaufruf verknüpft ist. Wenn weder ein Link noch ein Aktionsaufruf angegeben ist, werden Titel, Beschreibung und Bild von der aktuellen Seite übernommen.

* **Link** – Diese Datei verweist auf eine Inhaltsseite, eine externe URL oder einen Seitenanker.
* **Link in neuer Registerkarte öffnen** – Wenn diese Option aktiviert ist, wird der Link in einer neuen Browser-Registerkarte geöffnet.
* **Aktionsaufrufe** – Diese Option ermöglicht Links mit mehreren Zielen.
   * Die im ersten Aktionsaufruf verknüpfte Seite wird beim Vererben des Teaser-Titels, der Beschreibung oder des Bildes verwendet.

### Registerkarte „Text“ {#text-tab}

![Registerkarte „Text“ im Dialogfeld „Bearbeiten“ der Teaser-Komponente](/help/assets/teaser-edit-text.png)

* **Vortitel** - Der Vortitel wird vor dem Titel des Teasers angezeigt.
* **Titel** - Definiert einen Titel, der als Überschrift für den Teaser angezeigt wird.
   * **Titel von verknüpfter Seite übernehmen** - Bei Aktivierung dieser Option wird der Titel mit dem Titel der verknüpften Seite ausgefüllt.
* **Beschreibung** - Definiert eine Beschreibung, die als Unter-Überschrift für den Teaser angezeigt wird.
   * **Beschreibung von verknüpfter Seite übernehmen** - Bei Aktivierung dieser Option wird die Beschreibung mit der Beschreibung der verknüpften Seite ausgefüllt.
* **ID** – Diese Option dient zur Kontrolle der eindeutigen Kennung der Komponente in der HTML-Datei und auf der [Datenschicht](/help/developing/data-layer/overview.md).
   * Wenn Sie das Feld leer lassen, wird automatisch eine eindeutige ID generiert, die Sie über die resultierende Seite finden.
   * Sofern eine ID angegeben wird, ist vom Autor bzw. der Autorin sicherzustellen, dass diese eindeutig ist.
   * Änderungen der ID können sich auf das CSS-, JS- und Datenschicht-Tracking auswirken.

### Registerkarte „Asset“ {#asset-tab}

![Registerkarte „Bild“ im Dialogfeld „Bearbeiten“ der Teaser-Komponente](/help/assets/teaser-edit-image.png)

* **Vorgestelltes Bild von Seite übernehmen** – Verwendet das in den Seiteneigenschaften der verknüpften Seite definierte Bild oder das der aktuellen Seite, wenn keines gefunden wird.
* **Bild-Asset** – Ziehen Sie ein Asset aus dem [Asset-Browser](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html?lang=de) oder tippen Sie auf die Option **Durchsuchen**, um es aus einem lokalen Dateisystem hochzuladen.
   * Tippen oder klicken Sie auf **Löschen**, um die Auswahl des aktuell ausgewählten Bilds aufzuheben.
   * Tippen oder klicken Sie auf **Auswählen**, um zum Auswählen eines Bildes den [Asset-Browser](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html?lang=de) zu öffnen.
      * Wenn die [Remote-Assets-Unterstützung](#remote-assets) aktiviert ist, haben Sie mehrere Optionen zum Auswählen eines Assets:
         * Mit der Option **Lokal** wird ein Asset aus der lokalen AEM-Asset-Bibliothek ausgewählt.
         * Mit **Remote** wird aus einer Dynamic Media-Bibliothek außerhalb Ihrer AEM-Instanz ausgewählt.
   * Tippen oder klicken Sie auf **Bearbeiten**, um die [Ausgabedarstellungen des Assets](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/manage-digital-assets.html?lang=de) im Asset-Editor zu verwalten.
* **Alternativtext für Barrierefreiheit** – In diesem Feld können Sie eine Beschreibung des Bildes für sehbehinderte Benutzer definieren.
   * **Alternativtext von Seite übernehmen** – Diese Option verwendet die alternative Beschreibung des verknüpften Asset-Werts der `dc:description`-Metadaten in DAM oder der aktuellen Seite, wenn kein Asset verknüpft ist.
* **Keinen Alternativtext angeben** – Mit dieser Option wird das Bild so markiert, dass es von unterstützenden Technologien wie Bildschirmlesegeräten ignoriert wird, wenn das Bild rein dekorativ ist oder sonst keine zusätzlichen Informationen für die Seite liefert.

### Registerkarte „Arten“ {#styles-tab-edit}

![Registerkarte „Arten“ im Dialogfeld „Bearbeiten“ der Teaser-Listenkomponente](/help/assets/teaser-edit-styles.png)

Die Teaser-Komponente unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).

Verwenden Sie das Dropdown-Menü, um die Stile auszuwählen, die Sie auf die Komponente anwenden möchten. Die im Dialogfeld „Bearbeiten“ vorgenommenen Auswahlen haben denselben Effekt wie die in der Komponenten-Symbolleiste ausgewählten.

Stile müssen für diese Komponente im [Dialogfeld „Design“](#design-dialog) konfiguriert werden, damit das Dropdown-Menü verfügbar ist.

## Dialogfeld „Bearbeiten“ {#edit-dialog}

Die Teaser-Komponente delegiert das Rendern von Bildern an die [Bild-Komponente](image.md). Daher wird das [Dialogfeld „Bearbeiten“]&#x200B;(image.md#edit-dialog) dem Inhaltsautor zur Bearbeitung des Teaserbilds zur Verfügung gestellt.

## Dialogfeld „Design“ {#design-dialog}

Das Dialogfeld „Design“ ermöglicht es dem Vorlagenautor, die Teaser-Optionen zu definieren, die der Inhaltsautor bei Verwendung dieser Komponente hat.

### Registerkarte „Teaser“ {#teaser-tab}

![Dialogfeld „Design“ der Teaser-Komponente](/help/assets/teaser-design.png)

* **Aktionsaufrufe**
   * **Aktionsaufrufe deaktivieren** - Blendet die Option **Aktionsaufrufe** für Inhaltsautoren aus
* **Elemente**
   * **Vortitel ausblenden** - Blendet die Option **Vortitel** für Inhaltsautoren aus
   * **Titel ausblenden** - Blendet die Option **Titel** für Inhaltsautoren aus
      * Bei Auswahl der Option wird der **Titeltyp** ausgeblendet.
   * **Beschreibung ausblenden** - Blendet die Option **Beschreibung** für Inhaltsautoren aus
* **Standardtiteltyp** – Definiert das H-Tag, das vom Titel des Teasers verwendet werden soll.
* **Bilddelegat** – Informationen, die anzeigen, an welche Komponente der Teaser die Bildverarbeitung delegiert.

### Registerkarte „Arten“ {#styles-tab}

Die Teaser-Komponente unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).

## Adobe Client-Datenschicht {#data-layer}

Die Teaser-Komponente unterstützt die [Adobe Client-Datenschicht](/help/developing/data-layer/overview.md).
