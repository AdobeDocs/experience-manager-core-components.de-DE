---
title: Bildkomponente
description: Die Bildkomponenten-Kernkomponente ist eine adaptive Bildkomponente.
role: Architect, Developer, Admin, User
exl-id: c5e57f4b-139f-40e7-8d79-be9a74360b63
source-git-commit: dd30def59a8f037864da875ef4c831b11f766e57
workflow-type: ht
source-wordcount: '0'
ht-degree: 100%

---


# Bildkomponente {#image-component}

Die Bildkomponenten-Kernkomponente ist eine adaptive Bildkomponente.

{{traditional-aem}}

## Verwendung {#usage}

Die Bildkomponente bietet adaptive Bildauswahl und responsives Verhalten mit verzögertem Laden für die Menschen, die eine Seite besuchen, sowie einfache Bildplatzierung für die Inhaltsautorin bzw. den Inhaltsautor. 

Inhaltsautorinnen und Inhaltsautoren können das [Dialogfeld „Bearbeiten“](#edit-dialog) verwenden, um das Bild-Asset zu bearbeiten, um z. B. einen Zuschnitt anzuwenden oder das Bild zu drehen.

Die Bildbreiten sowie zusätzliche Einstellungen können vom Vorlagenautor im [Dialogfeld „Design“](#design-dialog) definiert werden. Der Inhaltseditor kann Elemente im [Dialogfeld „Konfigurieren“](#configure-dialog) hochladen oder auswählen.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Bildkomponente ist v3, die mit Version 2.18.0 der Kernkomponenten im Februar 2022 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |--- |---|---|
| v3 | – | Kompatibel | Kompatibel | Kompatibel |
| [v2](v2/image.md) | Kompatibel | Kompatibel | – | Kompatibel |
| [v1](v1/image-v1.md) | Kompatibel | Kompatibel | – | Kompatibel |

Weitere Informationen zu Kernkomponentenversionen und -freigaben finden Sie in den [Kernkomponentenversionen](/help/versions.md).

## Responsive Funktionen {#responsive-features}

Die Bildkomponente verfügt über robuste responsive Funktionen, die direkt sofort bereitgestellt werden können. Auf der Seitenvorlagenebene kann das [Design-Dialogfeld](#design-dialog) verwendet werden, um die Standardbreiten des Bild-Assets zu definieren. Die Bildkomponente lädt dann automatisch die richtige Breite für die Anzeige, abhängig von der Größe des Browser-Fensters. Wenn die Größe des Fensters geändert wird, lädt die Bildkomponente die korrekte Bildgröße dynamisch. Komponentenentwickler müssen sich keine Gedanken darüber machen, wie sie benutzerdefinierte Medienabfragen definieren, da die Bildkomponente bereits optimiert ist, um Ihren Inhalt zu laden.

Darüber hinaus unterstützt die Bildkomponente verzögertes Laden, um das Laden des tatsächlichen Bild-Assets zu verzögern, bis es im Browser sichtbar ist, wodurch die Reaktionsgeschwindigkeit Ihrer Seiten zunimmt.

>[!TIP]
>
>Standardmäßig wird die Bildkomponente durch das Adaptive Image Servlet gesteuert. Details zur Funktionsweise erhalten Sie unter [Adaptive Image Servlet](/help/developing/adaptive-image-servlet.md).

### Unterschiede zu v2 {#v2-differences}

Im Gegensatz zur Version 2 der Bildkomponente verwendet Version 3 die Browser-native Reaktionsfähigkeit. Das bedeutet, dass der Browser eine Reihe von Quellen für ein Bild für verschiedene Breiten erhält und der Browser die beste Wahl trifft.

In den meisten Fällen ziehen Browser es vor, lokal eine größere Breite zu verkleinern, um einen kleineren Viewport zu erhalten, anstatt das Bild mit geringerer Breite vom Server abzurufen. Dies ist der Grund, warum die Bildkomponente nicht für die Ausrichtung von Grafiken verwendet werden sollte (unterschiedliche Bilder/Zuschnitte für verschiedene Darstellungsfelder).

[Bitte lesen Sie die GitHub-Dokumentation der Komponente](https://github.com/adobe/aem-core-wcm-components/tree/main/content/src/content/jcr_root/apps/core/wcm/components/image/v3/image#javascript-data-attribute-bindings) für weitere Informationen.

## Dynamic Media-Unterstützung {#dynamic-media}

Die Bildkomponente (ab [Version 2.13.0](/help/versions.md)) unterstützt [Dynamic Media](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/dynamic-media.html?lang=de)-Assets. [Wenn diese Funktionen aktiviert sind](#design-dialog), können Sie Dynamic Media-Bild-Assets per Drag-and-Drop oder über den Assets-Browser hinzufügen, wie Sie es mit jedem anderen Bild tun würden. Darüber hinaus werden auch Bild-Modifikatoren, Bildvorgaben und Smartes Zuschneiden unterstützt.

Ihre mit Kernkomponenten erstellten Web-Erlebnisse können jetzt funktionsreiche, Sensei-gestützte, robuste, leistungsstarke und plattformübergreifende Dynamic Media-Bildfunktionen enthalten.

## Unterstützung für Remote Assets {#remote-assets}

Die Bildkomponente (ab [Version 2.23.2](/help/versions.md)) unterstützt Remote-Assets. [Wenn sie konfiguriert sind,](/help/developing/remote-assets.md) können Sie Assets aus einem Remote-Service für Ihre Bildkomponente auswählen.

## SVG-Unterstützung {#svg-support}

Skalierbare Vektorgrafiken (SVG) werden von der Bildkomponente unterstützt.

* Es wird sowohl das Verschieben eines SVG-Assets per Drag-and-Drop aus DAM als auch das Hochladen einer SVG-Datei aus einem lokalen Dateisystem unterstützt.
* Die ursprüngliche SVG-Datei wird gestreamt (Transformationen werden übersprungen).
* Bei einem SVG-Bild werden die „Smart-Bilder“ und die „Smart-Größen“ auf ein leeres Array im Bildmodell festgelegt.

### Sicherheit {#security}

Aus Sicherheitsgründen wird die ursprüngliche SVG niemals direkt vom Bild-Editor aufgerufen. Es wird durch `<img src="path-to-component">` aufgerufen. Dadurch wird verhindert, dass der Browser Skripte ausführt, die in der SVG-Datei eingebettet sind.

## Muster für Komponentenausgabe {#sample-component-output}

Um die Bildkomponente zu erleben und Beispiele für ihre Konfigurationsoptionen sowie die HTML- und JSON-Ausgabe zu sehen, besuchen Sie die [Komponentenbibliothek](https://adobe.com/go/aem_cmp_library_image_de).

### Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur Bildkomponente [finden Sie auf GitHub](https://adobe.com/go/aem_cmp_tech_image_v3_de).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

Die Bildkomponente unterstützt [Schema.org-Mikrodaten](https://schema.org).

## Dialogfeld „Bearbeiten“ {#edit-dialog}

Das Dialogfeld „Bearbeiten“ ermöglicht Inhaltsautorinnen und Inhaltsautoren das Zuschneiden und Zoomen des Bildes.

Je nachdem, ob [Dynamic Media](#dynamic-media) oder [Remote-Assets-Unterstützung](#remote-assets) aktiviert ist, unterscheiden sich die für die Bildbearbeitung verfügbaren Optionen.

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
>Bildbearbeitungsvorgänge werden für GIF-Bilder nicht unterstützt. Alle Änderungen, die im Bearbeitungsmodus an GIFs vorgenommen werden, bleiben nicht bestehen.

### Bearbeiten von Dynamic Media-Assets {#dynamic-media-assets}

Wenn Sie die [Funktionen von Dynamic Media aktiviert haben](#dynamic-media), muss die Bildbearbeitung selbst in der Asset-Konsole erfolgen.

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Die Bildkomponente bietet ein Dialogfeld zum Konfigurieren, in dem das Bild selbst zusammen mit seiner Beschreibung und den grundlegenden Eigenschaften definiert ist.

### Registerkarte „Asset“ {#asset-tab}

![Registerkarte „Asset“ im Dialogfeld „Konfigurieren“ der Bildkomponente](/help/assets/image-configure-asset.png)

* **Vorgestelltes Bild von Seite übernehmen** – Diese Option verwendet das [vorgestellte Bild der verknüpften Seite](page.md) oder das vorgestellte Bild der aktuellen Seite, wenn das Bild nicht verknüpft ist.

* **Bild-Asset** – Dies wird automatisch ausgefüllt, wenn **Vorgestelltes Bild von Seite übernehmen** ausgewählt ist. Heben Sie die Auswahl auf, um das Bild manuell zu definieren, indem Sie die folgenden Optionen festlegen.

   * Ziehen Sie ein Asset aus dem [Asset-Browser](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/fundamentals/environment-tools.html?lang=de) oder tippen Sie auf die Option **Durchsuchen**, um es aus einem lokalen Dateisystem hochzuladen.
   * Tippen oder klicken Sie auf **Löschen**, um die Auswahl des aktuell ausgewählten Bilds aufzuheben.
   * Tippen oder klicken Sie auf **Auswählen**, um zum Auswählen eines Bildes den [Asset-Browser](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/fundamentals/environment-tools.html?lang=de) zu öffnen.
      * Wenn die [Remote-Assets-Unterstützung](#remote-assets) aktiviert ist, haben Sie mehrere Optionen zum Auswählen eines Assets:
         * Mit der Option **Lokal** wird ein Asset aus der lokalen AEM-Asset-Bibliothek ausgewählt.
         * Mit **Remote** wird aus einer Dynamic Media-Bibliothek außerhalb Ihrer AEM-Instanz ausgewählt.
   * Tippen oder klicken Sie auf **Bearbeiten**, um die [Ausgabedarstellungen des Assets](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/manage/manage-digital-assets.html?lang=de) im Asset-Editor zu verwalten.

* **Alternativtext für Barrierefreiheit** – In diesem Feld können Sie eine Beschreibung des Bildes für sehbehinderte Benutzer definieren.

   * **Alternativtext von Seite übernehmen** – Diese Option verwendet die alternative Beschreibung des verknüpften Asset-Werts der `dc:description`-Metadaten in DAM oder der aktuellen Seite, wenn kein Asset verknüpft ist.

* **Keinen Alternativtext angeben** – Mit dieser Option wird das Bild so markiert, dass es von unterstützenden Technologien wie Bildschirmlesegeräten ignoriert wird, etwa wenn das Bild rein dekorativ ist oder sonst keine zusätzlichen Informationen für die Seite liefert.

### Registerkarte „Metadaten“ {#metadata-tab}

![Registerkarte „Metadaten“ im Dialogfeld „Konfigurieren“ der Bildkomponente](/help/assets/image-configure-metadata.png)

* **Vorgabetyp** – Hier wird der Typ der verfügbaren Bildvorgaben festgelegt, entweder **Bildvorgabe** oder **Smartes Zuschneiden**. Dies ist nur verfügbar, wenn die [Dynamic Media-Funktionen](#dynamic-meida) aktiviert sind.
   * **Bildvorgabe** – Wenn der **Vorgabetyp** **Bildvorgabe** ausgewählt ist, ist die Dropdown-Liste **Bildvorgabe** verfügbar, sodass aus den verfügbaren Dynamic Media-Vorgaben ausgewählt werden kann. Dies ist nur verfügbar, wenn für das ausgewählte Asset Vorgaben definiert sind.
   * **Smartes Zuschneiden** – Wenn der **Vorgabetyp** **Smartes Zuschneiden** ausgewählt ist, ist die Dropdown-Liste **Ausgabedarstellung** verfügbar, sodass aus den verfügbaren Ausgabedarstellungen des ausgewählten Assets ausgewählt werden kann. Dies ist nur verfügbar, wenn für das ausgewählte Asset Ausgabedarstellungen definiert sind.
   * **Bild-Modifikatoren** – Hier können zusätzliche Befehle zur Dynamic Media-Bildbereitstellung definiert werden, die durch `&` getrennt sind, unabhängig davon, welcher **Vorgabetyp** ausgewählt ist.
* **Beschriftung** – Zusätzliche Informationen über das Bild, die standardmäßig unter dem Bild angezeigt werden.
   * **Beschriftung aus DAM abrufen** – Wenn diese Option aktiviert ist, wird der Beschriftungstext des Bildes mit dem Wert der `dc:title`-Metadaten in DAM gefüllt.
   * **Beschriftung als Popup anzeigen** – Wenn diese Option aktiviert ist, wird die Beschriftung von einigen Browsern nicht unter dem Bild angezeigt, sondern als Popup, wenn der Mauszeiger über das Bild bewegt wird.
* **Verknüpfung** – Verknüpfen Sie das Bild mit einer anderen Ressource.
   * Verwenden Sie das Dialogfeld „Auswahl“, um eine Verknüpfung zu einer anderen AEM-Ressource herzustellen.
   * Geben Sie die absolute URL ein, wenn Sie keine Verknüpfung zu einer AEM-Ressource erstellen. Nicht-absolute URLs werden als relativ zu AEM interpretiert.
   * **Link in neuer Registerkarte öffnen** – Mit dieser Option wird der Link in einem neuen Browser-Fenster geöffnet.
* **ID** – Mit dieser Option können Sie die eindeutige Kennung der Komponente in der HTML-Datei und in der [Datenschicht](/help/developing/data-layer/overview.md) steuern.
   * Wenn Sie das Feld leer lassen, wird automatisch eine eindeutige ID generiert, die Sie über die resultierende Seite finden.
   * Sofern eine ID angegeben wird, ist vom Autor bzw. der Autorin sicherzustellen, dass diese eindeutig ist.
   * Änderungen der ID können sich auf das CSS-, JS- und Datenschicht-Tracking auswirken.

>[!TIP]
>
>**Smartes Zuschneiden** und **Bildvorgabe** sind Optionen, die sich gegenseitig ausschließen. Wenn eine Autorin oder ein Autor eine Bildvorgabe zusammen mit einer Ausgabedarstellung von Typ „Smartes Zuschneiden“ verwenden muss, muss sie bzw. er **Bild-Modifikatoren** verwenden, um Vorgaben manuell hinzuzufügen.

### Registerkarte „Arten“ {#styles-tab-edit}

![Registerkarte „Arten“ im Dialogfeld „Bearbeiten“ der Bildkomponente](/help/assets/image-configure-styles.png)

Die Bildkomponente unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).

Verwenden Sie das Dropdown-Menü, um die Stile auszuwählen, die Sie auf die Komponente anwenden möchten. Die im Dialogfeld „Bearbeiten“ vorgenommenen Auswahlen haben denselben Effekt wie die in der Komponenten-Symbolleiste ausgewählten.

Stile müssen für diese Komponente im [Dialogfeld „Design“](#design-dialog) konfiguriert werden, damit das Dropdown-Menü zur Verfügung steht.

## Dialogfeld „Design“ {#design-dialog}

### Registerkarte „Haupt“ {#main-tab}

![Registerkarte „Haupt“ im Dialogfeld „Design“ der Bildkomponente](/help/assets/image-design-main.png)

* **DM-Funktionen aktivieren** – Wenn diese Option aktiviert ist, sind die [Dynamic Media-Funktionen](#dynamic-media) verfügbar.
   * Diese Option wird nur angezeigt, wenn „Dynamic Media“ in der Umgebung aktiviert ist.
* **Web-optimierte Grafiken aktivieren** – Wenn diese Option aktiviert ist, liefert [der Web-optimierte Bildbereitstellungs-Service](/help/developing/web-optimized-image-delivery.md) Bilder im WebP-Format. Dadurch wird die Bildgröße durchschnittlich um 25 % verringert.
   * Diese Option ist nur in AEMaaCS verfügbar.
   * Wenn diese Option deaktiviert ist oder der Web-optimierte Bildbereitstellungs-Service nicht verfügbar ist, wird das [Adaptive Image Servlet](/help/developing/adaptive-image-servlet.md) verwendet.
* **Lazy Loading deaktivieren** – Wenn diese Option aktiviert ist, lädt die Komponente alle Bilder vorab, ohne dass das Laden verzögert wird.
* **Bild ist dekorativ** – Festlegen, ob die Option für dekorative Bilder automatisch aktiviert ist, wenn die Bildkomponente einer Seite hinzugefügt wird.
* **Alternativtext von DAM abrufen** - Festlegen, ob die Option zum Abrufen des Alternativtexts aus DAM automatisch aktiviert ist, wenn die Bildkomponente einer Seite hinzugefügt wird.
* **Beschriftung aus DAM abrufen** – Festlegen, ob die Option zum Abrufen der Beschriftung aus DAM automatisch aktiviert ist, wenn die Bildkomponente einer Seite hinzugefügt wird.
* **Beschriftung als Pop-up anzeigen** – Festlegen, ob die Option zum Anzeigen der Bildbeschriftung als Popup automatisch aktiviert ist, wenn die Bildkomponente einer Seite hinzugefügt wird.
* **Breite ändern** – Dieser Wert wird verwendet, um die Breite der Basisbilder zu ändern, die DAM-Assets sind.
   * Das Seitenverhältnis der Bilder wird beibehalten.
   * Wenn der Wert größer ist als die tatsächliche Breite des Bildes, hat dieser Wert keine Auswirkung.
   * Dieser Wert hat keine Auswirkungen auf SVG-Bilder.

Sie können eine Liste von Breiten in Pixeln für das Bild definieren, und die Komponente lädt, basierend auf der Browser-Größe, automatisch die am besten geeignete Breite. Dies ist ein wichtiger Teil der [responsiven Funktionen](#responsive-features) der Bildkomponente.

* **Breiten** – Definiert eine Liste der Breiten in Pixel für das Bild und die Komponente lädt automatisch die passende Breite basierend auf der Größe des Browsers.
   * Tippen oder klicken Sie auf die Schaltfläche **Hinzufügen**, um eine weitere Größe hinzuzufügen.
      * Verwenden Sie die Griffpunkte, um die Größenreihenfolge neu anzuordnen.
      * Verwenden Sie das Symbol **Löschen**, um eine Breite zu entfernen.
   * Standardmäßig wird das Laden von Bildern verzögert, bis sie sichtbar werden.
      * Wählen Sie die Option **Verzögertes Laden deaktivieren**, um die Bilder schon beim Laden der Seite zu laden.
* **JPEG-Qualität** – Der Qualitätsfaktor (in Prozent von 0 bis 100) für umgewandelte (z. B. skalierte oder zugeschnittene) JPEG-Bilder.

>[!TIP]
>
>Tipps zur Optimierung der Auswahl für die Ausgabedarstellung durch sorgfältige Definition der Breiten finden Sie im Dokument [Adaptive Image Servlet](/help/developing/adaptive-image-servlet.md).

### Registerkarte „Arten“ {#styles-tab}

Die Bildkomponente unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).

## Adobe Client-Datenschicht {#data-layer}

Die Bildkomponente unterstützt die [Adobe Client-Datenschicht](/help/developing/data-layer/overview.md).
