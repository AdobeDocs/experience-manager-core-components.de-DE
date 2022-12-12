---
title: E-Mail-Teaser-Komponente
description: Die E-Mail-Teaser-Komponente kann ein Bild, einen Titel, einen Rich-Text und optional einen Link zu weiteren Inhalten anzeigen.
role: Architect, Developer, Admin, User
exl-id: d6123b22-7cba-406c-986d-b6f00322d135
source-git-commit: 33976c0e745ad091a142109f70541f01a31edc5b
workflow-type: ht
source-wordcount: '0'
ht-degree: 100%

---


# E-Mail-Teaser-Komponente {#email-teaser-component}

Die E-Mail-Teaser-Komponente kann ein Bild, einen Titel, einen Rich-Text und optional einen Link zu weiteren Inhalten anzeigen.

## Verwendung {#usage}

Mit der E-Mail-Teaser-Komponente kann der Inhaltsautor bzw. die Inhaltsautorin problemlos einen Teaser erstellen, indem er bzw. sie ein Bild, einen Titel oder einen Rich-Text verwendet und Links zu weiteren Inhalten oder anderen Aktionen erstellt.

* Der Vorlagenautor bzw. die Vorlagenautorin kann im [Dialogfeld „Design“](#design-dialog) festlegen, ob die Optionen zum Erstellen von CTAs und zum Hinzufügen von Links verfügbar sind, sowie verschiedene Anzeigeoptionen deaktivieren.
* Der Inhaltsautor bzw. die Inhaltsautorin kann das [Dialogfeld „Konfigurieren“](#configure-dialog) verwenden, um ein Bild auszuwählen, CTAs zu definieren, Titel und Beschreibungen festzulegen und Links zum jeweiligen Teaser zu konfigurieren.
* Eine Änderung des Teaser-Bilds kann im [Dialogfeld „Bearbeiten“](image.md#edit-dialog) der [E-Mail-Bildkomponente](image.md) vorgenommen werden.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der E-Mail-Teaser-Komponente ist v1. Sie wurde mit dem Release X der E-Mail-Kernkomponenten im Oktober 2022 eingeführt und wird in diesem Dokument beschrieben.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|
| v1 | Kompatibel | Kompatibel |

## Muster für Komponentenausgabe {#sample-component-output}

Um die E-Mail-Teaser-Komponente sowie Beispiele für ihre Konfigurationsoptionen sowie HTML- und JSON-Ausgaben anzusehen, besuchen Sie die [Komponentenbibliothek](https://adobe.com/go/aem_cmp_library_email_teaser).

### Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur E-Mail-Teaser-Komponente [finden Sie auf GitHub](https://adobe.com/go/aem_cmp_tech_email_teaser_v1).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Der Inhaltsautor kann das Dialogfeld „Konfigurieren“ verwenden, um die Eigenschaften des einzelnen Teasers zu definieren. Es gibt auch ein [Dialogfeld „Bearbeiten“](#edit-dialog) zum Bearbeiten des Teaserbilds, wenn eines ausgewählt ist.

### Registerkarte „Links“ {#links-tab}

![Registerkarte „Links“ im Dialogfeld „Bearbeiten“ der E-Mail-Teaser-Komponente](/help/email/assets/email-teaser-edit-links.png)

Der Teaser-Titel, die Beschreibung und das Bild können aus dem verknüpften Inhalt oder aus dem Inhalt übernommen werden, der über den ersten CTA verknüpft ist. Wenn weder ein Link noch ein CTA spezifiziert ist, werden der Titel, die Beschreibung und das Bild vom aktuellen Inhalt übernommen.

* **Verknüpfung** – Diese Datei verweist auf Inhalte, eine externe URL oder einen Anker.
   * Klicken Sie auf das Kampagnensymbol, um das Dialogfeld [Adobe Campaign-Variable auswählen](/help/email/campaign-variables.md) zum Einfügen von dynamischen Inhalten aus Adobe Campaign zu öffnen.
* **Aktionsaufrufe** – Diese Option ermöglicht Links mit mehreren Zielen.
   * Die im ersten Aktionsaufruf verknüpfte Seite wird beim Vererben des Teaser-Titels, der Beschreibung oder des Bildes verwendet.
   * Klicken Sie auf das Kampagnensymbol, um das Dialogfeld [Adobe Campaign-Variable auswählen](/help/email/campaign-variables.md) zu öffnen und dynamische Inhalte aus Adobe Campaign einzufügen.

### Registerkarte „Text“ {#text-tab}

![Registerkarte „Text“ im Dialogfeld „Bearbeiten“ der E-Mail-Teaser-Komponente](/help/email/assets/email-teaser-edit-text.png)

* **Vortitel** - Der Vortitel wird vor dem Titel des Teasers angezeigt.
* **Titel** - Definiert einen Titel, der als Überschrift für den Teaser angezeigt wird.
   * Klicken Sie auf das Kampagnensymbol, um das Dialogfeld [Adobe Campaign-Variable auswählen](/help/email/campaign-variables.md) zu öffnen und dynamische Inhalte aus Adobe Campaign einzufügen.
   * **Titel von verknüpfter Seite übernehmen** - Bei Aktivierung dieser Option wird der Titel mit dem Titel der verknüpften Seite ausgefüllt.
* **Beschreibung** - Definiert eine Beschreibung, die als Unter-Überschrift für den Teaser angezeigt wird.
   * Klicken Sie auf das Symbol **Adobe Campaign-Variable auswählen**, um das Dialogfeld [Adobe Campaign-Variable auswählen](/help/email/campaign-variables.md) zu öffnen und dynamische Inhalte aus Adobe Campaign einzufügen.
   * **Beschreibung von verknüpfter Seite übernehmen** – Bei Aktivierung dieser Option wird die Beschreibung mit der Beschreibung der verknüpften Seite ausgefüllt.
* **ID** – Diese Option ermöglicht das Festlegen der eindeutigen Kennung der Komponente in HTML.
   * Wenn das Feld leer bleibt, wird automatisch eine eindeutige ID generiert, den Sie im resultierenden Inhalt finden.
   * Sofern eine ID angegeben wird, ist vom Autor bzw. der Autorin sicherzustellen, dass diese eindeutig ist.
   * Die Änderung der ID kann sich auf CSS auswirken.

### Registerkarte „Asset“ {#asset-tab}

![Registerkarte „Bild“ im Dialogfeld „Bearbeiten“ der E-Mail-Teaser-Komponente](/help/email/assets/email-teaser-edit-image.png)

* **Vorgestelltes Bild von Seite übernehmen** – Verwendet das in den Seiteneigenschaften der verknüpften Seite definierte Bild oder das der aktuellen Seite, wenn keines gefunden wird.
* **Bild-Asset** – Ziehen Sie ein Asset aus dem [Asset-Browser](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html?lang=de) oder tippen Sie auf die Option **Durchsuchen**, um es aus einem lokalen Dateisystem hochzuladen.
   * Tippen oder klicken Sie auf **Löschen**, um die Auswahl des aktuell ausgewählten Bilds aufzuheben.
   * Tippen oder klicken Sie auf **Bearbeiten**, um die [Ausgabedarstellungen des Assets](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/manage-digital-assets.html?lang=de) im Asset-Editor zu verwalten.
* **Alternativtext für Barrierefreiheit** – In diesem Feld können Sie eine Beschreibung des Bildes für sehbehinderte Benutzer definieren.
   * **Alternativtext von Seite übernehmen** – Diese Option verwendet die alternative Beschreibung des verknüpften Asset-Werts der `dc:description`-Metadaten in DAM oder der aktuellen Seite, wenn kein Asset verknüpft ist.
* **Keinen Alternativtext angeben** – Mit dieser Option wird das Bild so markiert, dass es von unterstützenden Technologien wie Bildschirmlesegeräten ignoriert wird, wenn das Bild rein dekorativ ist oder sonst keine zusätzlichen Informationen für die Seite liefert.

>[!NOTE]
>
>[Dynamic Media-Funktionen](image.md#dynamic-media) sind derzeit nicht in der Teaser-Komponente verfügbar.

### Registerkarte „Arten“ {#styles-tab-edit}

Die E-Mail-Teaser-Komponente unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).

Verwenden Sie das Dropdown-Menü, um die Stile auszuwählen, die Sie auf die Komponente anwenden möchten. Die im Dialogfeld „Bearbeiten“ vorgenommenen Auswahlen haben denselben Effekt wie die in der Komponenten-Symbolleiste ausgewählten.

Stile müssen für diese Komponente im [Dialogfeld „Design“](#design-dialog) konfiguriert werden, damit die Registerkarte zur Verfügung steht.

## Dialogfeld „Bearbeiten“ {#edit-dialog}

Die E-Mail-Teaser-Komponente delegiert das Rendern von Bildern an die [Bild-Komponente](image.md). Daher wird das [Dialogfeld „Bearbeiten“](image.md#edit-dialog) dem Inhaltsautor zur Bearbeitung des Teaser-Bildes zur Verfügung gestellt.

## Dialogfeld „Design“ {#design-dialog}

Das Dialogfeld „Design“ ermöglicht es dem Vorlagenautor, die Teaser-Optionen zu definieren, die der Inhaltsautor bei Verwendung dieser Komponente hat.

### Registerkarte „Teaser“ {#teaser-tab}

![Dialogfeld „Design“ der E-Mail-Teaser-Komponente](/help/email/assets/email-teaser-design.png)

* **Zulässige Überschriftenelemente** – Verwenden Sie die Dropdown-Liste, um festzulegen, welche HTML-Elemente von einem Autor bzw. einer Autorin für den Titeltyp des Teasers ausgewählt werden können.
* **Standard-Überschriftenelement des Titels** – Das HTML-Standardelement für Überschriften, das für den Titeltyp des Teasers verwendet wird
* **Aktionsaufrufe**
   * **Aktionsaufrufe deaktivieren** - Blendet die Option **Aktionsaufrufe** für Inhaltsautoren aus.
* **Elemente**
   * **Vortitel ausblenden** - Blendet die Option **Vortitel** für Inhaltsautoren aus.
   * **Titel ausblenden** - Blendet die Option **Titel** für Inhaltsautoren aus.
      * Bei Auswahl der Option wird der **Titeltyp** ausgeblendet.
   * **Titeltyp anzeigen**
   * **Beschreibung ausblenden** – Blendet die Option **Beschreibung** für Inhaltsautoren bzw. Inhaltsautorinnen aus.
* **Bilddelegat** – Informationsanzeige, aus der ersichtlich ist, an welche Komponente der E-Mail-Teaser die Handhabung des Bilds delegiert.

### Registerkarte „Arten“ {#styles-tab}

Die E-Mail-Teaser-Komponente unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).
