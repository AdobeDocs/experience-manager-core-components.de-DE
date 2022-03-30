---
title: Bildkomponente (v2)
description: Die Kernkomponente „Bildkomponente“ ist eine anpassungsfähige Bildkomponente mit Funktionen zur Bearbeitung im Kontext.
role: Architect, Developer, Admin, User
exl-id: 3f2b93f9-c48d-43ef-a78a-accd5090fe6f
source-git-commit: c64cdbf3779318c9cf018658d43684946de9c15b
workflow-type: tm+mt
source-wordcount: '2231'
ht-degree: 99%

---

# Bildkomponente (v2) {#image-component}

Die Kernkomponente „Bildkomponente“ ist eine adaptive Bildkomponente, die eine direkte Bearbeitung ermöglicht.

## Nutzung {#usage}

Die Bildkomponente bietet adaptive Bildauswahl und reaktionsfähiges Verhalten mit verzögertem Laden für den Seitenbesucher sowie einfache Bildplatzierung und Zuschneiden für den Inhaltsautor.

Die Bildbreiten sowie die Beschneidung und zusätzliche Einstellungen können vom Vorlagenautor im [Dialogfeld „Design“](#design-dialog) definiert werden. Der Inhaltseditor kann Assets im [Dialogfeld „Konfigurieren“](#configure-dialog) hochladen oder auswählen und das Bild im [Dialogfeld „Bearbeiten“](#edit-dialog) beschneiden. Für zusätzlichen Komfort ist auch eine einfache, ersetzende Änderung des Bildes verfügbar.

## Version und Kompatibilität {#version-and-compatibility}

In diesem Dokument wird die v2 der Bildkomponente beschrieben, die ursprünglich mit Version 2.0.0 der Kernkomponenten im Januar 2018 eingeführt wurde.

>[!CAUTION]
>
>In diesem Dokument wird die Bildkomponente v1 beschrieben.
>
>Weitere Informationen zur aktuellen Version der Bildkomponente finden Sie im Dokument [Bildkomponente](/help/components/image.md).

## Responsive Funktionen {#responsive-features}

Die Bildkomponente verfügt über robuste responsive Funktionen, die direkt sofort bereitgestellt werden können. Auf der Seitenvorlagenebene kann das [Design-Dialogfeld](#design-dialog) verwendet werden, um die Standardbreiten des Bild-Assets zu definieren. Die Bildkomponente lädt dann automatisch die korrekte Breite, die je nach Größe des Browserfensters angezeigt wird. Wenn die Größe des Fensters geändert wird, lädt die Bildkomponente die korrekte Bildgröße dynamisch. Komponentenentwickler müssen sich keine Gedanken darüber machen, wie sie benutzerdefinierte Medienabfragen definieren, da die Bildkomponente bereits optimiert ist, um Ihren Inhalt zu laden.

Darüber hinaus unterstützt die Bildkomponente verzögertes Laden, um das Laden des tatsächlichen Bild-Assets zu verzögern, bis es im Browser sichtbar ist, wodurch die Reaktionsgeschwindigkeit Ihrer Seiten zunimmt.

>[!TIP]
>
>Weitere technische Details zu diesen Funktionen und Tipps zur Optimierung der Auswahl für die Ausgabedarstellung finden Sie im Abschnitt zum [Adaptive Image Servlet](#adaptive-image-servlet).

## Dynamic Media-Unterstützung {#dynamic-media}

Die Bildkomponente (ab [Version 2.13.0](/help/versions.md)) unterstützt [Dynamic Media](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/dynamicmedia/dynamic-media.html?lang=de#dynamicmedia)-Assets. [Wenn diese Funktionen aktiviert sind](#design-dialog), können Sie Dynamic Media-Bild-Assets per Drag-and-Drop oder über den Assets-Browser hinzufügen, wie Sie es mit jedem anderen Bild tun würden. Darüber hinaus werden auch Bild-Modifikatoren, Bildvorgaben und Smartes Zuschneiden unterstützt.

Ihre mit Kernkomponenten erstellten Web-Erlebnisse können jetzt funktionsreiche, Sensei-gestützte, robuste, leistungsstarke und plattformübergreifende Dynamic Media-Bildfunktionen enthalten.

## SVG-Unterstützung {#svg-support}

Skalierbare Vektorgrafiken (SVG) werden von der Bildkomponente unterstützt.

* Das Drag-and-Drop eines SVG-Assets aus DAM und das Hochladen eines SVG-Datei-Uploads aus einem lokalen Dateisystem werden beide unterstützt.
* Das Adaptive Bildservlet streamt die ursprüngliche SVG-Datei (Transformationen werden übersprungen).
* Bei einem SVG-Bild werden die „Smart-Bilder“ und die „Smart-Größen“ auf ein leeres Array im Bildmodell festgelegt.

### Sicherheit {#security}

Aus Sicherheitsgründen wird die ursprüngliche SVG niemals direkt vom Bild-Editor aufgerufen. Es wird durch `<img src=“path-to-component”>` aufgerufen. Dadurch wird verhindert, dass der Browser Skripte ausführt, die in der SVG-Datei eingebettet sind.

>[!CAUTION]
>
>Für die SVG-Unterstützung sind die Kernkomponenten in Version 2.1.0 oder höher zusammen mit [Service Pack 2](https://experienceleague.adobe.com/docs/experience-manager-64/release-notes/sp-release-notes.html?lang=de) für AEM 6.4 oder höher erforderlich, damit [neue Bildbearbeitungsfunktionen](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/full-stack/components-templates/image-editor.html) in AEM unterstützt werden.

## Musterkomponentenausgabe {#sample-component-output}

Um die Bildkomponente zu erleben und Beispiele für ihre Konfigurationsoptionen sowie die HTML- und JSON-Ausgabe zu sehen, besuchen Sie die [Komponentenbibliothek](https://adobe.com/go/aem_cmp_library_image_de).

### Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur Bildkomponente [finden Sie auf GitHub](https://adobe.com/go/aem_cmp_tech_image_v2_de).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

Die Bildkomponente unterstützt [Schema.org-Mikrodaten](https://schema.org).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Zusätzlich zum standardmäßigen [Dialogfeld „Bearbeiten“](#edit-dialog) und zum [Dialogfeld „Design“](#design-dialog) bietet die Bildkomponente ein Dialogfeld für die Konfiguration, bei dem das Bild selbst mit seiner Beschreibung und den grundlegenden Eigenschaften definiert wird.

### Registerkarte „Asset“ {#asset-tab}

![Registerkarte „Asset“ im Dialogfeld „Konfigurieren“ der Bildkomponente](/help/assets/image-configure-asset.png)

* **Bild-Asset**
   * Ziehen Sie ein Asset aus dem [Asset-Browser](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html?lang=de) oder tippen Sie auf die Option **Durchsuchen**, um es von einem lokalen Dateisystem hochzuladen.
   * Tippen oder klicken Sie auf **Löschen**, um das aktuell ausgewählte Bild zu deaktivieren.
   * Tippen oder klicken Sie auf **Bearbeiten**, um die [Ausgabedarstellungen des Assets](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/manage-digital-assets.html?lang=de) im Asset-Editor zu verwalten.

### Registerkarte „Metadaten“ {#metadata-tab}

![Registerkarte „Metadaten“ im Dialogfeld „Konfigurieren“ der Bildkomponente](/help/assets/image-configure-metadata.png)

* **Vorgabetyp** - Hier wird der Typ der verfügbaren Bildvorgaben festgelegt, entweder **Bildvorgabe** oder **Smartes Zuschneiden**. Dies ist nur verfügbar, wenn die [Dynamic Media-Funktionen](#dynamic-meida) aktiviert sind.
   * **Bildvorgabe** - Wenn der **Vorgabetyp** **Bildvorgabe** ausgewählt ist, ist die Dropdown-Liste **Bildvorgabe** verfügbar, sodass aus den verfügbaren Dynamic Media-Vorgaben ausgewählt werden kann. Dies ist nur verfügbar, wenn für das ausgewählte Asset Vorgaben definiert sind.
   * **Smartes Zuschneiden** - Wenn der **Vorgabetyp** **Smartes Zuschneiden** ausgewählt ist, ist die Dropdown-Liste **Ausgabedarstellung** verfügbar, sodass aus den verfügbaren Ausgabedarstellungen des ausgewählten Assets werden kann. Dies ist nur verfügbar, wenn für das ausgewählte Asset Ausgabedarstellungen definiert sind.
   * **Bild-Modifikatoren** - Hier können zusätzliche Befehle zur Dynamic Media-Bildbereitstellung definiert werden, die durch `&` getrennt sind, unabhängig davon, welcher **Vorgabetyp** ausgewählt ist.
* **Bild ist dekorativ** - Überprüfen Sie, ob das Bild von Hilfstechnologien ignoriert werden soll und daher keinen alternativen Text erfordert. Dies gilt nur für dekorative Bilder.
* **Alternativtext** - Textalternativen zur Bedeutung oder Funktion des Bildes für sehbeeinträchtigte Leser.
   * **Alternativtext von DAM abrufen** - Wenn die Option aktiviert ist, wird der Alternativtext des Bildes mit dem Wert der `dc:description`-Metadaten in DAM gefüllt.
* **Beschriftung** - Zusätzliche Informationen über das Bild, die standardmäßig unter dem Bild angezeigt werden.
   * **Beschriftung aus DAM abrufen** - Wenn die Option aktiviert ist, wird der Beschriftungstext des Bildes mit dem Wert der `dc:title`-Metadaten in DAM gefüllt.
   * **Beschriftung als Pop-up anzeigen** - Wenn die Option aktiviert ist, wird die Beschriftung nicht unter dem Bild angezeigt, sondern von einigen Browsern als Popup, wenn der Mauszeiger über das Bild bewegt wird.
* **Verknüpfung** - Verknüpfen Sie das Bild mit einer anderen Ressource.
   * Verwenden Sie das Dialogfeld „Auswahl“, um eine Verknüpfung zu einer anderen AEM-Ressource herzustellen.
   * Geben Sie die absolute URL ein, wenn Sie keine Verknüpfung zu einer AEM-Ressource erstellen. Nicht absolute URLs werden als relativ zu AEM interpretiert.
* **ID** – Diese Option dient zur Kontrolle der eindeutigen Kennung der Komponente in der HTML-Datei und auf der [Datenschicht](/help/developing/data-layer/overview.md).
   * Wenn Sie das Feld leer lassen, wird automatisch eine eindeutige ID generiert, die Sie über die resultierende Seite finden.
   * Sofern eine ID angegeben wird, ist vom Autor sicherzustellen, dass diese eindeutig ist.
   * Änderungen der ID können sich auf das CSS-, JS- und Datenschicht-Tracking auswirken.

>[!TIP]
>
>**Smartes Zuschneiden** und **Bildvorgabe** sind Optionen, die sich gegenseitig ausschließen. Wenn ein Autor eine Bildvorgabe zusammen mit einer Ausgabedarstellung von Typ „Smartes Zuschneiden“ verwenden muss, muss der Autor **Bild-Modifikatoren** verwenden, um Vorgaben manuell hinzuzufügen.

## Dialogfeld „Bearbeiten“ {#edit-dialog}

Das Dialogfeld „Bearbeiten“ ermöglicht dem Inhaltsautor das Zuschneiden, Ändern der Startkarte und das Zoomen des Bildes.

>[!NOTE]
>
>Funktionen zum Zuschneiden, Drehen und Zoomen gelten nicht für Dynamic Media-Assets. Wenn die [Dynamic Media-Funktionen](#dynamic-media) aktiviert sind, sollten solche Bearbeitungen an Dynamic Media-Assets über das Dialogfeld [Konfigurieren](#configure-dialog) vorgenommen werden.

![Dialogfeld „Bearbeiten“ der Bildkomponente](/help/assets/image-edit.png)

* Zuschneiden beginnen

   ![Symbol „Zuschneiden beginnen“](/help/assets/image-start-crop.png)

   Wenn Sie diese Option auswählen, wird eine Dropdown-Liste für vordefinierte Zuschneideproportionen geöffnet.

   * Wählen Sie die Option **Freihand**, um Ihre eigene Zuschnittsart zu definieren.
   * Wählen Sie **Beschnitt entfernen**, um das ursprüngliche Asset anzuzeigen.

   Nachdem Sie eine Zuschnittoption ausgewählt haben, verwenden Sie die blauen Griffe, um die Beschneidung auf dem Bild anzupassen.

   ![Optionen für das Zuschneiden](/help/assets/image-crop-options.png)

* Nach rechts drehen

   ![Symbol „Nach rechts drehen“](/help/assets/image-rotate-right.png)

   Verwenden Sie diese Option, um das Bild um 90° nach rechts (im Uhrzeigersinn) zu drehen.

* Horizontal spiegeln

   ![Symbol „Horizontal spiegeln“](/help/assets/image-flip-horizontal.png)

   Verwenden Sie diese Option, um das Bild horizontal zu spiegeln oder um 180° entlang der y-Achse zu drehen.

* Vertikal spiegeln

   ![Symbol „Vertikal spiegeln“](/help/assets/image-flip-vertical.png)

   Verwenden Sie diese Option, um das Bild vertikal zu spiegeln oder um 180° entlang der x-Achse zu drehen.

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
>Bildbearbeitungsvorgänge (Beschneiden, Spiegeln, Drehen) werden für GIF-Bilder nicht unterstützt. Alle Änderungen, die im Bearbeitungsmodus an GIFs vorgenommen wurden, bleiben nicht bestehen.

## Dialogfeld „Design“ {#design-dialog}

Das Dialogfeld „Design“ ermöglicht es dem Vorlagenautor, die Beschneidungs-, Drehungs- und Upload-Optionen zu definieren, die der Inhaltsautor bei Verwendung dieser Komponente hat.

### Registerkarte „Allgemein“ {#main-tab}

Auf der Registerkarte **Haupt** können Sie eine Liste der Breiten in Pixel für das Bild definieren, und die Komponente lädt automatisch die passende Breite basierend auf der Browser-Größe. Dies ist ein wichtiger Teil der [responsiven Funktionen](#responsive-features) der Bildkomponente.

Darüber hinaus können Sie festlegen, welche allgemeinen Komponentenoptionen automatisch aktiviert oder deaktiviert werden, wenn der Autor die Komponente zu einer Seite hinzufügt.

![Registerkarte „Haupt“ im Dialogfeld „Design“ der Bildkomponente](/help/assets/image-design-main.png)

* **DM-Funktionen aktivieren** - Wenn diese Option aktiviert ist, sind die [Dynamic Media-Funktionen](#dynamic-media) verfügbar.
* **Lazy Loading aktivieren** - Festlegen, ob die Option für verzögertes Laden (Lazy Loading) automatisch aktiviert ist, wenn die Bildkomponente einer Seite hinzugefügt wird.
* **Bild ist dekorativ** - Festlegen, ob die Option für dekorative Bilder automatisch aktiviert ist, wenn die Bildkomponente einer Seite hinzugefügt wird.
* **Alternativtext von DAM abrufen** - Festlegen, ob die Option zum Abrufen des Alternativtexts aus DAM automatisch aktiviert ist, wenn die Bildkomponente einer Seite hinzugefügt wird.
* **Beschriftung aus DAM abrufen** - Festlegen, ob die Option zum Abrufen der Beschriftung aus DAM automatisch aktiviert ist, wenn die Bildkomponente einer Seite hinzugefügt wird.
* **Beschriftung als Pop-up anzeigen** - Festlegen, ob die Option zum Anzeigen der Bildbeschriftung als Popup automatisch aktiviert ist, wenn die Bildkomponente einer Seite hinzugefügt wird.
* **UUID-Tracking deaktivieren** - Option aktivieren, um das Tracking der UUID des Bild-Assets zu deaktivieren.
* **Breiten** - Definiert eine Liste der Breiten in Pixel für das Bild und die Komponente lädt automatisch die passende Breite basierend auf der Größe des Browsers.
   * Tippen oder klicken Sie auf die Schaltfläche **Hinzufügen**, um eine weitere Größe hinzuzufügen.
      * Verwenden Sie die Griffpunkte, um die Reihenfolge der Größen neu anzuordnen.
      * Verwenden Sie das Symbol **Löschen**, um eine Breite zu entfernen.
   * Standardmäßig wird das Laden von Bildern verzögert, bis sie sichtbar werden.
      * Wählen Sie die Option **Lazy Loading deaktivieren** aus, um die Bilder schon beim Laden der Seite zu laden.
* **JPEG-Qualität** - Der Qualitätsfaktor (in Prozent von 0 bis 100) für umgewandelte (z. B. skalierte oder zugeschnittene) JPEG-Bilder.

>[!TIP]
>
>Weitere technische Details zu den Funktionen und Tipps zur Optimierung der Auswahl für die Ausgabedarstellung durch sorgfältiges Definieren der Breiten finden Sie im Abschnitt zum [Adaptive Image Servlet](#adaptive-image-servlet).

### Registerkarte „Funktionen“ {#features-tab}

Auf der Registerkarte **Funktionen** können Sie festlegen, welche Optionen den Inhaltsautoren zur Verfügung stehen, wenn sie die Komponente verwenden, einschließlich Optionen fürs Hochladen, Ausrichtung und Beschneiden.

* Quelle

   ![Registerkarte „Funktionen“ im Dialogfeld „Design“ der Bildkomponente](/help/assets/image-design-features-source.png)

   Wählen Sie die Option **Asset-Uploads aus Dateisystem zulassen**, damit Inhaltsautoren Bilder von ihrem lokalen Computer hochladen können. Wenn Sie erzwingen möchten, dass Autoren nur Assets aus AEM auswählen, wählen Sie diese Option ab.

* Ausrichtung

   ![Registerkarte „Funktionen“ im Dialogfeld „Design“ der Bildkomponente](/help/assets/image-design-features-orientation.png)

* **Drehen** – Verwenden Sie diese Option, damit der Inhaltsautor die Option 
**Nach rechts drehen** verwenden kann.
* **Spiegeln** – Verwenden Sie diese Option, damit der Inhaltsautor die Optionen 
**Horizontal spiegeln** und **Vertikal spiegeln** verwenden kann.

   >[!CAUTION]
   >
   >Die Option **Spiegeln** ist standardmäßig deaktiviert. Durch Aktivieren werden im Dialogfeld „Bearbeiten“ der Bildkomponente die Felder **Vertikal spiegeln** und **Horizontal spiegeln** angezeigt. Die Funktion wird jedoch derzeit nicht von AEM unterstützt, und die Änderungen, die mit diesen Optionen vorgenommen werden, bleiben nicht erhalten.

* Beschneiden

   ![Registerkarte „Funktionen“ im Dialogfeld „Design“ der Bildkomponente](/help/assets/image-design-features-cropping.png)

   Wählen Sie die Option **Beschneiden zulassen** aus, damit der Inhaltsautor das Bild in der Komponente im Dialogfeld „Bearbeiten“ beschneiden kann.
   * Klicken Sie auf **Hinzufügen**, um ein vordefiniertes Bildseitenverhältnis hinzuzufügen.
   * Geben Sie einen beschreibenden Namen ein, der im Dropdown-Menü **Zuschneiden** angezeigt wird.
   * Geben Sie das numerische Seitenverhältnis des Bildes ein.
   * Verwenden Sie die Ziehpunkte, um die Reihenfolge der Seitenverhältnisse neu anzuordnen.
   * Verwenden Sie das Papierkorbsymbol, um ein Seitenverhältnis zu löschen.

   >[!CAUTION]
   >
   >Beachten Sie, dass die Beschneidungsverhältnisse als **Höhe/Breite** definiert sind. Dies unterscheidet sich von der herkömmlichen Definition als Breite/Höhe und erfolgt aus Gründen der Legacy-Kompatibilität. Den Inhaltsautoren wird kein Unterschied bewusst werden, solange Sie einen klaren Namen für das Verhältnis angeben, da nur der Name in der Benutzeroberfläche angezeigt wird und nicht das Verhältnis selbst.

### Registerkarte „Arten“ {#styles-tab-1}

Die Bildkomponente unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).

## Adaptives Bildservlet {#adaptive-image-servlet}

Die Bildkomponente verwendet das Adaptive Bildservlet der Kernkomponente. [Das Adaptive Bildservlet](https://github.com/adobe/aem-core-wcm-components/wiki/The-Adaptive-Image-Servlet) übernimmt die Bildverarbeitung sowie das Streaming und kann von Entwicklern bei der [Anpassung der Kernkomponenten](/help/developing/customizing.md) genutzt werden.

### Optimieren der Auswahl für die Ausgabedarstellung {#optimizing-rendition-selection}

Das Adaptive Image Servlet versucht, die beste Ausgabedarstellung für die angeforderte Bildgröße und den angeforderten Bildtyp auszuwählen. Es wird empfohlen, die zulässigen Breiten von DAM-Ausgabeformaten und Bildkomponenten synchron zu definieren, damit die Verarbeitung durch das Adaptive Image Servlet so gering wie möglich ist.

Dadurch wird die Leistung verbessert und verhindert, dass einige Bilder von der zugrunde liegenden Bildverarbeitungsbibliothek nicht korrekt verarbeitet werden.

>[!NOTE]
>
>Bedingte Anforderungen über den `Last-Modified`-Header werden vom Adaptiven Bildservlet unterstützt, aber die Zwischenspeicherung des `Last-Modified`-Headers [muss im Dispatcher aktiviert werden](https://experienceleague.adobe.com/docs/experience-manager-dispatcher/using/configuring/dispatcher-configuration.html?lang=de#caching-http-response-headers).
>
>Die Dispatcher-Musterkonfiguration des [AEM-Projektarchetyps](/help/developing/archetype/overview.md) enthält diese Konfiguration bereits.

## Adobe Client-Datenschicht {#data-layer}

Die Bildkomponente unterstützt die [Adobe Client-Datenschicht](/help/developing/data-layer/overview.md).
