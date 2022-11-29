---
title: E-Mail-Teaser-Komponente
description: Die E-Mail-Teaser-Komponente kann ein Bild, einen Titel, Rich-Text und optional einen Link zu weiteren Inhalten anzeigen.
role: Architect, Developer, Admin, User
exl-id: d6123b22-7cba-406c-986d-b6f00322d135
source-git-commit: 33976c0e745ad091a142109f70541f01a31edc5b
workflow-type: tm+mt
source-wordcount: '1056'
ht-degree: 53%

---


# E-Mail-Teaser-Komponente {#email-teaser-component}

Die E-Mail-Teaser-Komponente kann ein Bild, einen Titel, Rich-Text und optional einen Link zu weiteren Inhalten anzeigen.

## Nutzung {#usage}

Mit der E-Mail-Teaser-Komponente kann der Inhaltsautor einen Teaser einfach mithilfe eines Bildes, Titels oder Rich-Text erstellen und Links zu weiteren Inhalten oder anderen Aktionen erstellen.

* Der Vorlagenautor kann das [Dialogfeld „Design“](#design-dialog) verwenden, um zu definieren, ob die Optionen zum Erstellen von Aktionsaufrufen und zum Hinzufügen von Links verfügbar sind sowie verschiedene Anzeigeoptionen deaktivieren.
* Der Inhaltsautor kann das [Dialogfeld „Konfigurieren“](#configure-dialog) verwenden, um ein Bild festzulegen, CTAs zu definieren, Titel und Beschreibungen festzulegen und Links zum jeweiligen Teaser zu konfigurieren.
* Die [Dialogfeld &quot;Bearbeiten&quot;](image.md#edit-dialog) des [E-Mail-Bildkomponente](image.md) kann aufgerufen werden, um das Teaser-Bild zu ändern.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der E-Mail-Teaser-Komponente ist v1, die mit Version x der E-Mail-Kernkomponenten im Oktober 2022 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|
| v1 | Kompatibel | Kompatibel |

## Musterkomponentenausgabe {#sample-component-output}

Um die E-Mail-Teaser-Komponente zu erleben und Beispiele für ihre Konfigurationsoptionen sowie HTML- und JSON-Ausgaben zu sehen, besuchen Sie die [Komponentenbibliothek.](https://adobe.com/go/aem_cmp_library_email_teaser)

### Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur E-Mail-Teaser-Komponente [finden Sie auf GitHub.](https://adobe.com/go/aem_cmp_tech_email_teaser_v1)

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler.](/help/developing/overview.md)

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Der Inhaltsautor kann das Dialogfeld „Konfigurieren“ verwenden, um die Eigenschaften des einzelnen Teasers zu definieren. Es gibt auch ein [Dialogfeld „Bearbeiten“](#edit-dialog) zum Bearbeiten des Teaserbilds, wenn eines ausgewählt ist.

### Registerkarte „Links“ {#links-tab}

![Registerkarte &quot;Links&quot;im Dialogfeld &quot;Bearbeiten&quot;der E-Mail-Teaser-Komponente](/help/email/assets/email-teaser-edit-links.png)

Der Teaser-Titel, die Beschreibung und das Bild können aus dem verknüpften Inhalt oder aus dem Inhalt übernommen werden, der im ersten Aktionsaufruf verknüpft ist. Wenn weder ein Link noch ein Aktionsaufruf angegeben ist, werden der Titel, die Beschreibung und das Bild vom aktuellen Inhalt übernommen.

* **Link** - Diese Datei verlinkt zu Inhalt, externer URL oder Anker.
   * Klicken Sie auf das Kampagnensymbol , um die [Adobe Campaign-Variable auswählen](/help/email/campaign-variables.md) zum Einfügen von dynamischen Inhalten aus Adobe Campaign.
* **Aktionsaufrufe** – Diese Option ermöglicht Links mit mehreren Zielen.
   * Die im ersten Aktionsaufruf verknüpfte Seite wird beim Vererben des Teaser-Titels, der Beschreibung oder des Bildes verwendet.
   * Klicken Sie auf das Kampagnensymbol , um die [Adobe Campaign-Variable auswählen](/help/email/campaign-variables.md) zum Einfügen von dynamischen Inhalten aus Adobe Campaign.

### Registerkarte „Text“ {#text-tab}

![Registerkarte &quot;Text&quot;im Dialogfeld &quot;Bearbeiten&quot;der E-Mail-Teaser-Komponente](/help/email/assets/email-teaser-edit-text.png)

* **Vortitel** - Der Vortitel wird vor dem Titel des Teasers angezeigt.
* **Titel** - Definiert einen Titel, der als Überschrift für den Teaser angezeigt wird.
   * Klicken Sie auf das Kampagnensymbol , um die [Adobe Campaign-Variable auswählen](/help/email/campaign-variables.md) zum Einfügen von dynamischen Inhalten aus Adobe Campaign.
   * **Titel von verknüpfter Seite übernehmen** - Bei Aktivierung dieser Option wird der Titel mit dem Titel der verknüpften Seite ausgefüllt.
* **Beschreibung** - Definiert eine Beschreibung, die als Unter-Überschrift für den Teaser angezeigt wird.
   * Klicken Sie auf **Adobe Campaign-Variable auswählen** Symbol zum Öffnen [Adobe Campaign-Variable auswählen](/help/email/campaign-variables.md) zum Einfügen von dynamischen Inhalten aus Adobe Campaign.
   * **Beschreibung von verknüpfter Seite übernehmen** - Bei Aktivierung dieser Option wird die Beschreibung mit der Beschreibung der verknüpften Seite ausgefüllt.
* **ID** - Diese Option ermöglicht die Steuerung der eindeutigen Kennung der Komponente im HTML.
   * Wenn Sie das Feld leer lassen, wird automatisch eine eindeutige ID generiert, die Sie durch Überprüfen des resultierenden Inhalts finden können.
   * Sofern eine ID angegeben wird, ist vom Autor sicherzustellen, dass diese eindeutig ist.
   * Eine Änderung der ID kann sich auf CSS auswirken.

### Registerkarte „Asset“ {#asset-tab}

![Registerkarte &quot;Bild&quot;im Dialogfeld &quot;Bearbeiten&quot;der E-Mail-Teaser-Komponente](/help/email/assets/email-teaser-edit-image.png)

* **Vorgestelltes Bild von Seite übernehmen** – Verwendet das in den Seiteneigenschaften der verknüpften Seite definierte Bild oder das der aktuellen Seite, wenn keines gefunden wird.
* **Bild-Asset** – Ziehen Sie ein Asset aus dem [Asset-Browser](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html?lang=de) oder tippen Sie auf die Option **Durchsuchen**, um es aus einem lokalen Dateisystem hochzuladen.
   * Tippen oder klicken Sie auf **Löschen**, um das aktuell ausgewählte Bild zu deaktivieren.
   * Tippen oder klicken Sie auf **Bearbeiten** nach [Verwalten der Ausgabeformate des Assets](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/manage-digital-assets.html?lang=de) im Asset-Editor.
* **Alternativtext für Barrierefreiheit** – In diesem Feld können Sie eine Beschreibung des Bildes für sehbehinderte Benutzer definieren.
   * **Alternativtext von Seite übernehmen** – Diese Option verwendet die alternative Beschreibung des verknüpften Asset-Werts der `dc:description`-Metadaten in DAM oder der aktuellen Seite, wenn kein Asset verknüpft ist.
* **Keinen Alternativtext angeben** – Mit dieser Option wird das Bild so markiert, dass es von unterstützenden Technologien wie Bildschirmlesegeräten ignoriert wird, wenn das Bild rein dekorativ ist oder sonst keine zusätzlichen Informationen für die Seite liefert.

>[!NOTE]
>
>[Dynamic Media-Funktionen](image.md#dynamic-media) sind derzeit nicht in der Teaser-Komponente verfügbar.

### Registerkarte „Arten“ {#styles-tab-edit}

Die E-Mail-Teaser-Komponente unterstützt die AEM [Stilsystem.](/help/get-started/authoring.md#component-styling)

Verwenden Sie das Dropdown-Menü, um die Stile auszuwählen, die Sie auf die Komponente anwenden möchten. Die im Dialogfeld „Bearbeiten“ vorgenommenen Auswahlen haben denselben Effekt wie die in der Komponenten-Symbolleiste ausgewählten.

Stile müssen für diese Komponente im [Dialogfeld &quot;Design&quot;](#design-dialog) , damit die Registerkarte verfügbar ist.

## Dialogfeld „Bearbeiten“ {#edit-dialog}

Die E-Mail-Teaser-Komponente delegiert das Rendern von Bildern an die [Bildkomponente](image.md). Daher wird das [Dialogfeld „Bearbeiten“](image.md#edit-dialog) dem Inhaltsautor zur Bearbeitung des Teaser-Bildes zur Verfügung gestellt.

## Dialogfeld „Design“ {#design-dialog}

Das Dialogfeld „Design“ ermöglicht es dem Vorlagenautor, die Teaser-Optionen zu definieren, die der Inhaltsautor bei Verwendung dieser Komponente hat.

### Registerkarte „Teaser“ {#teaser-tab}

![Dialogfeld &quot;Design&quot;der E-Mail-Teaser-Komponente](/help/email/assets/email-teaser-design.png)

* **Zulässige Überschriftenelemente** - Verwenden Sie die Dropdown-Liste, um festzulegen, welche Überschriftenelemente von einem Autor für den Titeltyp des Teasers ausgewählt werden können.
* **Standard-Überschriftenelement des Titels** - Das HTML-Standardelement für Überschriften, das für den Titeltyp des Teasers verwendet wird
* **Aktionsaufrufe**
   * **Aktionsaufrufe deaktivieren** - Blendet die Option **Aktionsaufrufe** für Inhaltsautoren aus.
* **Elemente**
   * **Vortitel ausblenden** - Blendet die Option **Vortitel** für Inhaltsautoren aus.
   * **Titel ausblenden** - Blendet die Option **Titel** für Inhaltsautoren aus.
      * Bei Auswahl der Option wird der **Titeltyp** ausgeblendet.
   * **Titeltyp anzeigen**
   * **Beschreibung ausblenden** - Blendet die Option **Beschreibung** für Inhaltsautoren aus.
* **Bilddelegat** - Informationsanzeige, die angibt, an welche Komponente der E-Mail-Teaser die Bildverarbeitung delegiert.

### Registerkarte „Stile“ {#styles-tab}

Die E-Mail-Teaser-Komponente unterstützt die AEM [Stilsystem.](/help/get-started/authoring.md#component-styling)
