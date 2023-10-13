---
title: Bildkomponente
description: Die Bildkomponenten-Kernkomponente ist eine adaptive Bildkomponente.
role: Architect, Developer, Admin, User
exl-id: c5e57f4b-139f-40e7-8d79-be9a74360b63
source-git-commit: a10c98aecf6d3c0d989f2e3c18affc51850f60bc
workflow-type: tm+mt
source-wordcount: '2061'
ht-degree: 72%

---


# Bildkomponente {#image-component}

Die Bildkomponenten-Kernkomponente ist eine adaptive Bildkomponente.

## Verwendung {#usage}

Die Bildkomponente bietet adaptive Bildauswahl und responsives Verhalten mit verzögertem Laden für den Seitenbesucher und einfacher Bildplatzierung für den Inhaltsautor.

Inhaltsautorinnen und Inhaltsautoren können das [Dialogfeld „Bearbeiten“](#edit-dialog) verwenden, um das Bild-Asset zu bearbeiten, um z. B. einen Zuschnitt anzuwenden oder das Bild zu drehen.

Die Bildbreiten sowie zusätzliche Einstellungen können vom Vorlagenautor im [Dialogfeld „Design“](#design-dialog) definiert werden. Der Inhaltseditor kann Elemente im [Dialogfeld „Konfigurieren“](#configure-dialog) hochladen oder auswählen.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Bildkomponente ist v3, die mit Version 2.18.0 der Kernkomponenten im Februar 2022 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM Versionen, mit denen die Komponentenversionen kompatibel sind, und Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v3 | - | Kompatibel | Kompatibel |
| [v2](v2/image.md) | Kompatibel | Kompatibel | Kompatibel |
| [v1](v1/image-v1.md) | Kompatibel | Kompatibel | Kompatibel |

Weitere Informationen zu Kernkomponentenversionen und -freigaben finden Sie in den [Kernkomponentenversionen](/help/versions.md).

## Responsive Funktionen {#responsive-features}

Die Bildkomponente verfügt über robuste responsive Funktionen, die direkt sofort bereitgestellt werden können. Auf der Seitenvorlagenebene kann das [Design-Dialogfeld](#design-dialog) verwendet werden, um die Standardbreiten des Bild-Assets zu definieren. Die Bildkomponente lädt automatisch die richtige Breite, die je nach Größe des Browser-Fensters angezeigt werden soll. Wenn die Größe des Fensters geändert wird, lädt die Bildkomponente die korrekte Bildgröße dynamisch. Komponentenentwickler müssen sich keine Gedanken darüber machen, wie sie benutzerdefinierte Medienabfragen definieren, da die Bildkomponente bereits optimiert ist, um Ihren Inhalt zu laden.

Darüber hinaus unterstützt die Bildkomponente verzögertes Laden, um das Laden des tatsächlichen Bild-Assets zu verzögern, bis es im Browser sichtbar ist, wodurch die Reaktionsgeschwindigkeit Ihrer Seiten zunimmt.

>[!TIP]
>
>Standardmäßig wird die Bildkomponente durch das Adaptive Image Servlet gesteuert. Siehe [Adaptives Bildservlet](/help/developing/adaptive-image-servlet.md) für Details zur Funktionsweise.

## Dynamic Media-Unterstützung {#dynamic-media}

Die Bildkomponente (ab [Version 2.13.0](/help/versions.md)) unterstützt [Dynamic Media](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/dynamic-media.html)-Assets. [Wenn diese Funktionen aktiviert sind](#design-dialog), können Sie Dynamic Media-Bild-Assets per Drag-and-Drop oder über den Assets-Browser hinzufügen, wie Sie es mit jedem anderen Bild tun würden. Darüber hinaus werden auch Bild-Modifikatoren, Bildvorgaben und Smartes Zuschneiden unterstützt.

Ihre mit Kernkomponenten erstellten Web-Erlebnisse können jetzt funktionsreiche, Sensei-gestützte, robuste, leistungsstarke und plattformübergreifende Dynamic Media-Bildfunktionen enthalten.

## Unterstützung für Next Generation Dynamic Media {#next-gen-dm}

Die Bildkomponente (ab [Version 2.23.2](/help/versions.md)) unterstützt Remote-Assets von Dynamic Media.

[Wenn sie konfiguriert sind](/help/developing/next-gen-dm.md), können Sie Assets aus einem Remote-Service von Next Generation Dynamic Media für Ihre Bildkomponente auswählen.

## SVG-Unterstützung {#svg-support}

Skalierbare Vektorgrafiken (SVG) werden von der Bildkomponente unterstützt.

* Das Drag &amp; Drop eines SVG-Assets aus DAM und das Hochladen einer SVG-Datei, die aus einem lokalen Dateisystem hochgeladen wurde, werden beide unterstützt.
* Die ursprüngliche SVG-Datei wird gestreamt (Transformationen werden übersprungen).
* Bei einem SVG-Bild werden die „Smart-Bilder“ und die „Smart-Größen“ auf ein leeres Array im Bildmodell festgelegt.

### Sicherheit {#security}

Aus Sicherheitsgründen wird die ursprüngliche SVG niemals direkt vom Bild-Editor aufgerufen. Es wird durch `<img src="path-to-component">` aufgerufen. Dadurch wird verhindert, dass der Browser Skripte ausführt, die in der SVG-Datei eingebettet sind.

## Muster für Komponentenausgabe {#sample-component-output}

Um die Bildkomponente zu erleben und Beispiele für die Konfigurationsoptionen und die HTML- und JSON-Ausgabe zu sehen, besuchen Sie die [Komponentenbibliothek](https://adobe.com/go/aem_cmp_library_image_de).

### Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur Bildkomponente [finden Sie auf GitHub](https://adobe.com/go/aem_cmp_tech_image_v3_de).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

Die Bildkomponente unterstützt [Schema.org-Mikrodaten](https://schema.org).

## Dialogfeld „Bearbeiten“ {#edit-dialog}

Das Dialogfeld „Bearbeiten“ ermöglicht Inhaltsautorinnen und Inhaltsautoren das Zuschneiden und Zoomen des Bildes.

Je nachdem, ob Sie [Dynamic Media](#dynamic-media) aktiviert oder [Dynamic Media der nächsten Generation](#next-gen-dm) Funktionen aktiviert sind, unterscheiden sich die für die Bearbeitung von Bildern verfügbaren Optionen.

### Bearbeitung von Standard-Assets {#standard-assets}

Wenn Sie Standard-AEM-Assets bearbeiten, können Sie auf das Symbol **Bearbeiten** im Kontextmenü der Bildkomponente klicken.

![Dialogfeld „Bearbeiten“ der Bildkomponente](/help/assets/image-edit.png)

* Zuschneiden beginnen

  ![Symbol „Zuschneiden beginnen“](/help/assets/image-start-crop.png)

  Wenn Sie diese Option auswählen, wird eine Dropdown-Liste für vordefinierte Zuschneideproportionen geöffnet.

   * Wählen Sie **Beschnitt entfernen**, um das ursprüngliche Asset anzuzeigen.

  Nachdem Sie eine Zuschnittoption ausgewählt haben, verwenden Sie die blauen Griffe, um die Beschneidung auf dem Bild anzupassen.

  ![Optionen für das Zuschneiden](/help/assets/image-crop-options.png)

* Nach rechts drehen

  ![Symbol „Nach rechts drehen“](/help/assets/image-rotate-right.png)

  Verwenden Sie diese Option, um das Bild um 90° nach rechts (im Uhrzeigersinn) zu drehen.

* Zoom zurücksetzen

  ![Symbol „Zoom zurücksetzen“](/help/assets/image-reset-zoom.png)

  Wenn das Bild bereits gezoomt wurde, verwenden Sie diese Option, um den Zoom-Grad zurückzusetzen.

* Zoom-Regler öffnen

  ![Symbol „Zoom-Regler öffnen“](/help/assets/image-zoom.png)

  Mit dieser Option können Sie einen Schieberegler anzeigen, um den Zoom-Grad des Bildes zu steuern.

  ![Steuerelement des Zoom-Reglers](/help/assets/image-zoom-slider.png)

Der Editor für die Bearbeitung im Kontext kann auch zum Ändern des Bildes verwendet werden. Aus Platzgründen sind nur einfache Optionen inline verfügbar. Für vollständige Bearbeitungsoptionen verwenden Sie den Vollbildmodus.

![Optionen für die Bildbearbeitung im Kontext](/help/assets/image-in-place-edit.png)

>[!NOTE]
>
>Bildbearbeitungsvorgänge werden für GIF-Bilder nicht unterstützt. Änderungen, die im Bearbeitungsmodus an GIF vorgenommen werden, bleiben nicht erhalten.

### Bearbeiten von Dynamic Media-Assets {#dynamic-media-assets}

Wenn Sie die [Funktionen von Dynamic Media aktiviert haben](#dynamic-media), muss die Bildbearbeitung selbst in der Asset-Konsole erfolgen.

### Bearbeiten von Assets von Next Generation Dynamic Media {#next-gen-dm-assets}

Wenn Sie [Next Generation Dynamic Media konfiguriert haben](#next-gen-dm), ist die Option **Smartes Zuschneiden** in den Kontextmenüs der Komponente verfügbar.

![Smartes Zuschneiden](/help/assets/image-smart-crop.png)

Verwenden Sie das Dialogfeld, um das smarte Zuschneiden anzupassen.

![Dialogfeld „Smartes Zuschneiden“](/help/assets/image-smart-crop-dialog.png)

>[!TIP]
>
>Weitere Informationen zum smarten Zuschneiden finden Sie [in diesem Video zur Funktion.](https://experienceleague.adobe.com/docs/experience-manager-learn/assets/dynamic-media/images/smart-crop-feature-video-use.html?lang=de)

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Die Bildkomponente bietet ein Dialogfeld zum Konfigurieren, in dem das Bild selbst zusammen mit seiner Beschreibung und den grundlegenden Eigenschaften definiert ist.

### Registerkarte „Asset“ {#asset-tab}

![Registerkarte „Asset“ im Dialogfeld „Konfigurieren“ der Bildkomponente](/help/assets/image-configure-asset.png)

* **Vorgestelltes Bild von Seite übernehmen** – Diese Option verwendet das [vorgestellte Bild der verknüpften Seite](page.md) oder das vorgestellte Bild der aktuellen Seite, wenn das Bild nicht verknüpft ist.

* **Bild-Asset** – Dies wird automatisch ausgefüllt, wenn **Vorgestelltes Bild von Seite übernehmen** ausgewählt ist. Heben Sie die Auswahl auf, um das Bild manuell zu definieren, indem Sie die folgenden Optionen festlegen.

   * Ziehen Sie ein Asset aus dem [Asset-Browser](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/fundamentals/environment-tools.html) oder tippen Sie auf **durchsuchen** -Option, damit Sie sie von einem lokalen Dateisystem hochladen können.
   * Tippen oder klicken Sie auf **Löschen**, um die Auswahl des aktuell ausgewählten Bilds aufzuheben.
   * Tippen oder klicken **Auswahl** , um die [Asset-Browser](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/fundamentals/environment-tools.html) sodass Sie ein Bild auswählen können.
      * Wenn die [Funktionen von Next Generation Dynamic Media](#next-gen-dm) aktiviert sind, haben Sie mehrere Optionen, um ein Asset auszuwählen:
         * Mit der Option **Lokal** wird ein Asset aus der lokalen AEM-Asset-Bibliothek ausgewählt.
         * Mit **Remote** wird aus einer Dynamic Media-Bibliothek außerhalb Ihrer AEM-Instanz ausgewählt.
   * Tippen oder klicken Sie auf **Bearbeiten**, um die [Ausgabedarstellungen des Assets](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/manage/manage-digital-assets.html) im Asset-Editor zu verwalten.

* **Alternativtext für Barrierefreiheit** – In diesem Feld können Sie eine Beschreibung des Bildes für sehbehinderte Benutzer definieren.

   * **Alternativtext von Seite übernehmen** – Diese Option verwendet die alternative Beschreibung des verknüpften Asset-Werts der `dc:description`-Metadaten in DAM oder der aktuellen Seite, wenn kein Asset verknüpft ist.

* **Kein Alternativtext** - Markiert das Bild, das von Hilfstechnologien wie Bildschirmlesehilfen ignoriert werden soll, wenn das Bild rein dekorativ ist oder anderweitig keine zusätzlichen Informationen an die Seite weitergibt.

### Registerkarte „Metadaten“ {#metadata-tab}

![Registerkarte „Metadaten“ im Dialogfeld „Konfigurieren“ der Bildkomponente](/help/assets/image-configure-metadata.png)

* **Vorgabetyp** – Hier wird der Typ der verfügbaren Bildvorgaben festgelegt, entweder **Bildvorgabe** oder **Smartes Zuschneiden**. Dies ist nur verfügbar, wenn die [Dynamic Media-Funktionen](#dynamic-meida) aktiviert sind.
   * **Bildvorgabe** – Wenn der **Vorgabetyp** **Bildvorgabe** ausgewählt ist, ist die Dropdown-Liste **Bildvorgabe** verfügbar, sodass aus den verfügbaren Dynamic Media-Vorgaben ausgewählt werden kann. Dies ist nur verfügbar, wenn für das ausgewählte Asset Vorgaben definiert sind.
   * **Smartes Zuschneiden** - Wann **Vorgabetyp** von **Smartes Zuschneiden** ausgewählt ist, wird die Dropdownliste **Ausgabedarstellung** verfügbar ist, sodass aus den verfügbaren Ausgabeformaten des ausgewählten Assets ausgewählt werden kann. Dies ist nur verfügbar, wenn für das ausgewählte Asset Ausgabedarstellungen definiert sind.
   * **Bild-Modifikatoren** – Hier können zusätzliche Befehle zur Dynamic Media-Bildbereitstellung definiert werden, die durch `&` getrennt sind, unabhängig davon, welcher **Vorgabetyp** ausgewählt ist.
* **Beschriftung** – Zusätzliche Informationen über das Bild, die standardmäßig unter dem Bild angezeigt werden.
   * **Beschriftung von DAM abrufen** - Wenn diese Option aktiviert ist, wird der Beschriftungstext des Bildes mit dem Wert der `dc:title` Metadaten in DAM.
   * **Beschriftung als Popup anzeigen** - Wenn diese Option aktiviert ist, wird die Beschriftung nicht unter dem Bild angezeigt, sondern von einigen Browsern als Popup, wenn der Mauszeiger über das Bild bewegt wird.
* **Verknüpfung** – Verknüpfen Sie das Bild mit einer anderen Ressource.
   * Verwenden Sie das Dialogfeld „Auswahl“, um eine Verknüpfung zu einer anderen AEM-Ressource herzustellen.
   * Geben Sie die absolute URL ein, wenn Sie keine Verknüpfung zu einer AEM-Ressource erstellen. Nicht absolute URLs werden als relativ zu AEM interpretiert.
   * **Link in neuer Registerkarte öffnen** – Mit dieser Option wird der Link in einem neuen Browser-Fenster geöffnet.
* **ID** - Mit dieser Option können Sie die eindeutige Kennung der Komponente im HTML und im [Datenschicht](/help/developing/data-layer/overview.md).
   * Wenn Sie das Feld leer lassen, wird automatisch eine eindeutige ID generiert, die Sie über die resultierende Seite finden.
   * Sofern eine ID angegeben wird, ist vom Autor bzw. der Autorin sicherzustellen, dass diese eindeutig ist.
   * Das Ändern der ID kann sich auf das CSS-, JS- und Datenschicht-Tracking auswirken.

>[!TIP]
>
>**Smartes Zuschneiden** und **Bildvorgabe** sind Optionen, die sich gegenseitig ausschließen. Wenn ein Autor eine Bildvorgabe zusammen mit einer Ausgabedarstellung für smartes Zuschneiden verwenden muss, muss der Autor die **Bild-Modifikatoren** , um Vorgaben manuell hinzuzufügen.

### Registerkarte „Arten“ {#styles-tab-edit}

![Registerkarte „Arten“ im Dialogfeld „Bearbeiten“ der Bildkomponente](/help/assets/image-configure-styles.png)

Die Bildkomponente unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).

Verwenden Sie das Dropdown-Menü, um die Stile auszuwählen, die Sie auf die Komponente anwenden möchten. Die im Dialogfeld „Bearbeiten“ vorgenommenen Auswahlen haben denselben Effekt wie die in der Komponenten-Symbolleiste ausgewählten.

Stile müssen für diese Komponente im [Dialogfeld &quot;Design&quot;](#design-dialog) für das Dropdown-Menü verfügbar sein.

## Dialogfeld „Design“ {#design-dialog}

### Registerkarte „Haupt“ {#main-tab}

![Registerkarte „Haupt“ im Dialogfeld „Design“ der Bildkomponente](/help/assets/image-design-main.png)

* **DM-Funktionen aktivieren** – Wenn diese Option aktiviert ist, sind die [Dynamic Media-Funktionen](#dynamic-media) verfügbar.
   * Diese Option wird nur angezeigt, wenn „Dynamic Media“ in der Umgebung aktiviert ist.
* **Web-optimierte Bilder aktivieren** - Wenn aktiviert, [der weboptimierte Bildbereitstellungsdienst](/help/developing/web-optimized-image-delivery.md) liefert Bilder im WebP-Format, wodurch die Bildgröße um durchschnittlich 25 % verringert wird.
   * Diese Option ist nur in AEMaaCS verfügbar.
   * Wenn diese Option deaktiviert ist oder der Web-optimierte Bildbereitstellungsdienst nicht verfügbar ist, wird die [Adaptives Bildservlet](/help/developing/adaptive-image-servlet.md) verwendet.
* **Verzögertes Laden deaktivieren** - Wenn diese Option aktiviert ist, lädt die Komponente alle Bilder ohne verzögertes Laden vorab.
* **Bild ist dekorativ** – Festlegen, ob die Option für dekorative Bilder automatisch aktiviert ist, wenn die Bildkomponente einer Seite hinzugefügt wird.
* **Alternativtext von DAM abrufen** - Festlegen, ob die Option zum Abrufen des Alternativtexts aus DAM automatisch aktiviert ist, wenn die Bildkomponente einer Seite hinzugefügt wird.
* **Beschriftung aus DAM abrufen** – Festlegen, ob die Option zum Abrufen der Beschriftung aus DAM automatisch aktiviert ist, wenn die Bildkomponente einer Seite hinzugefügt wird.
* **Beschriftung als Pop-up anzeigen** – Festlegen, ob die Option zum Anzeigen der Bildbeschriftung als Popup automatisch aktiviert ist, wenn die Bildkomponente einer Seite hinzugefügt wird.
* **Breite ändern** – Dieser Wert wird verwendet, um die Breite der Basisbilder zu ändern, die DAM-Assets sind.
   * Das Seitenverhältnis der Bilder wird beibehalten.
   * Wenn der Wert größer ist als die tatsächliche Breite des Bildes, hat dieser Wert keine Auswirkung.
   * Dieser Wert hat keine Auswirkungen auf SVG-Bilder.

Sie können eine Liste der Breiten in Pixel für das Bild definieren und die Komponente lädt automatisch die passende Breite basierend auf der Browser-Größe. Dies ist ein wichtiger Teil der [responsiven Funktionen](#responsive-features) der Bildkomponente.

* **Breiten** – Definiert eine Liste der Breiten in Pixel für das Bild und die Komponente lädt automatisch die passende Breite basierend auf der Größe des Browsers.
   * Tippen oder klicken Sie auf die Schaltfläche **Hinzufügen**, um eine weitere Größe hinzuzufügen.
      * Verwenden Sie die Griffpunkte, um die Größenreihenfolge neu anzuordnen.
      * Verwenden Sie das Symbol **Löschen**, um eine Breite zu entfernen.
   * Standardmäßig wird das Laden von Bildern verzögert, bis sie sichtbar werden.
      * Wählen Sie die Option **Verzögertes Laden deaktivieren** sodass Sie die Bilder beim Laden der Seite laden können.
* **JPEG-Qualität** - Der Qualitätsfaktor (in Prozent von 0 bis 100) für umgewandelte (z. B. skalierte oder zugeschnittene) JPEG-Bilder.

>[!TIP]
>
>Tipps zur Optimierung der Auswahl für die Ausgabedarstellung durch sorgfältige Definition der Breiten finden Sie im Dokument [Adaptive Image Servlet](/help/developing/adaptive-image-servlet.md).

### Registerkarte „Arten“ {#styles-tab}

Die Bildkomponente unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).

## Adobe Client-Datenschicht {#data-layer}

Die Bildkomponente unterstützt die [Adobe Client-Datenschicht](/help/developing/data-layer/overview.md).
