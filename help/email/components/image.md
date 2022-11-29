---
title: E-Mail-Bildkomponente
description: Die E-Mail-Bildkomponente ist eine adaptive Bildkomponente, die eine Bearbeitung im Kontext ermöglicht.
role: Architect, Developer, Admin, User
exl-id: f5d40047-3082-4edd-a5f6-6ab3e33997f9
source-git-commit: 33976c0e745ad091a142109f70541f01a31edc5b
workflow-type: tm+mt
source-wordcount: '1683'
ht-degree: 63%

---


# E-Mail-Bildkomponente {#email-image-component}

Die E-Mail-Bildkomponente ist eine adaptive Bildkomponente, die eine Bearbeitung im Kontext ermöglicht.

## Nutzung {#usage}

Die E-Mail-Bildkomponente bietet adaptive Bildauswahl und responsives Verhalten mit verzögertem Laden für den Seitenbesucher sowie einfache Drag-and-Drop-Bildplatzierung und -konfiguration für den Inhaltsautor.

* Die Bildbreiten sowie zusätzliche Einstellungen können vom Vorlagenautor im [Dialogfeld „Design“](#design-dialog) definiert werden.
* Der Inhaltseditor kann Elemente im [Dialogfeld „Konfigurieren“](#configure-dialog) hochladen oder auswählen.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der E-Mail-Bildkomponente ist v1, die mit Version x der E-Mail-Kernkomponenten im Oktober 2022 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|
| v1 | Kompatibel | Kompatibel |

Weitere Informationen zu Kernkomponentenversionen und -versionen finden Sie im Dokument . [Versionen der E-Mail-Kernkomponenten](/help/email/versions.md).

## Responsive Funktionen {#responsive-features}

Die E-Mail-Bildkomponente verfügt über zuverlässige responsive Funktionen, die sofort einsatzbereit sind. Auf der Seitenvorlagenebene kann das [Design-Dialogfeld](#design-dialog) verwendet werden, um die Standardbreiten des Bild-Assets zu definieren. Die E-Mail-Bildkomponente lädt dann automatisch die korrekte Breite, die je nach Größe des Browser-Fensters angezeigt werden soll. Wenn die Größe des Fensters geändert wird, lädt die E-Mail-Bildkomponente dynamisch die korrekte Bildgröße. Komponentenentwickler müssen sich keine Gedanken über die Definition benutzerdefinierter Medienabfragen machen, da die E-Mail-Bildkomponente bereits für das Laden Ihres Inhalts optimiert ist.

Darüber hinaus unterstützt die E-Mail-Bildkomponente verzögertes Laden, um das Laden des tatsächlichen Bild-Assets so lange zu verschieben, bis es im Browser sichtbar ist, wodurch die Reaktionsgeschwindigkeit Ihres Inhalts erhöht wird.

>[!TIP]
>
>Standardmäßig wird die E-Mail-Bildkomponente über das Adaptive Bildservlet bereitgestellt. Bitte lesen Sie das Dokument [Adaptive Image Servlet](#adaptive-image-servlet) für Details zur Funktionsweise.

## Dynamic Media-Unterstützung {#dynamic-media}

Die E-Mail-Bildkomponente unterstützt [Dynamic Media](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/dynamicmedia/dynamic-media.html?lang=de#dynamicmedia) Assets. [Wenn diese Funktionen aktiviert sind](#design-dialog), können Sie Dynamic Media-Bild-Assets per Drag-and-Drop oder über den Assets-Browser hinzufügen, wie Sie es mit jedem anderen Bild tun würden. Darüber hinaus werden auch Bild-Modifikatoren, Bildvorgaben und Smartes Zuschneiden unterstützt.

Ihre mit den E-Mail-Kernkomponenten erstellten E-Mail-Erlebnisse können umfassende, Sensei-gestützte, robuste, leistungsstarke, plattformübergreifende Dynamic Media-Bildfunktionen bieten.

## SVG-Unterstützung {#svg-support}

Skalierbare Vektorgrafiken (SVG) werden von der E-Mail-Bildkomponente unterstützt.

* Das Drag-and-Drop eines SVG-Assets aus DAM und das Hochladen eines SVG-Datei-Uploads aus einem lokalen Dateisystem werden beide unterstützt.
* Die ursprüngliche SVG-Datei wird gestreamt (Transformationen werden übersprungen).
* Bei einem SVG-Bild werden die „Smart-Bilder“ und die „Smart-Größen“ auf ein leeres Array im Bildmodell festgelegt.

### Sicherheit {#security}

Aus Sicherheitsgründen wird die ursprüngliche SVG niemals direkt vom Bild-Editor aufgerufen. Es wird durch `<img src=“path-to-component”>` aufgerufen. Dadurch wird verhindert, dass der Browser Skripte ausführt, die in der SVG-Datei eingebettet sind.

## Musterkomponentenausgabe {#sample-component-output}

Um die E-Mail-Bildkomponente sowie Beispiele für die Konfigurationsoptionen sowie HTML- und JSON-Ausgaben zu erhalten, besuchen Sie die [Komponentenbibliothek.](https://adobe.com/go/aem_cmp_library_email_image)

### Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur E-Mail-Bildkomponente [finden Sie auf GitHub.](https://adobe.com/go/aem_cmp_tech_email_image_v1)

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler.](/help/developing/overview.md)

Die Bildkomponente unterstützt [Schema.org-Mikrodaten.](https://schema.org)

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Die E-Mail-Bildkomponente bietet ein Dialogfeld zum Konfigurieren, in dem das Bild selbst zusammen mit seiner Beschreibung und den grundlegenden Eigenschaften definiert ist.

### Registerkarte „Asset“ {#asset-tab}

![Registerkarte &quot;Asset&quot;im Dialogfeld &quot;Konfigurieren&quot;der E-Mail-Bildkomponente](/help/email/assets/email-image-configure-asset.png)

* **Vorgestelltes Bild von Seite übernehmen** – Diese Option verwendet das [vorgestellte Bild der verknüpften Seite](page.md) oder das vorgestellte Bild der aktuellen Seite, wenn das Bild nicht verknüpft ist.

* **Alternativtext für Barrierefreiheit** – In diesem Feld können Sie eine Beschreibung des Bildes für sehbehinderte Benutzer definieren.

   * **Alternativtext von Seite übernehmen** – Diese Option verwendet die alternative Beschreibung des verknüpften Asset-Werts der `dc:description`-Metadaten in DAM oder der aktuellen Seite, wenn kein Asset verknüpft ist.

* **Bild-Asset**
   * Ziehen Sie ein Asset aus dem [Asset-Browser](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html?lang=de) oder tippen Sie auf die Option **Durchsuchen**, um es von einem lokalen Dateisystem hochzuladen.
   * Tippen oder klicken Sie auf **Löschen**, um das aktuell ausgewählte Bild zu deaktivieren.
   * Tippen oder klicken Sie auf **Bearbeiten** nach [Verwalten der Ausgabeformate des Assets](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/manage-digital-assets.html?lang=de) im Asset-Editor.

* **Keinen Alternativtext angeben** – Mit dieser Option wird das Bild so markiert, dass es von unterstützenden Technologien wie Bildschirmlesegeräten ignoriert wird, wenn das Bild rein dekorativ ist oder sonst keine zusätzlichen Informationen für die Seite liefert.

* **Verzögertes Laden deaktivieren** - Diese Option lädt alle Bildkomponenten vorab, ohne sie nach Bedarf zu laden.

### Registerkarte „Metadaten“ {#metadata-tab}

![Registerkarte „Metadaten“ im Dialogfeld „Konfigurieren“ der Bildkomponente](/help/email/assets/email-image-configure-metadata.png)

* **Vorgabetyp** – Hier wird der Typ der verfügbaren Bildvorgaben festgelegt, entweder **Bildvorgabe** oder **Smartes Zuschneiden**. Dies ist nur verfügbar, wenn die [Dynamic Media-Funktionen](#dynamic-meida) aktiviert sind.
   * **Bildvorgabe** - Wann **Vorgabetyp** von **Bildvorgabe** ausgewählt ist, wird die Dropdown-Liste **Bildvorgabe** verfügbar ist, sodass aus den verfügbaren Dynamic Media-Vorgaben ausgewählt werden kann. Dies ist nur verfügbar, wenn für das ausgewählte Asset Vorgaben definiert sind.
   * **Smartes Zuschneiden** - Wann **Vorgabetyp** von **Smartes Zuschneiden** ausgewählt ist, wird die Dropdown-Liste **Ausgabedarstellung** verfügbar ist, sodass aus den verfügbaren Ausgabeformaten des ausgewählten Assets ausgewählt werden kann. Dies ist nur verfügbar, wenn für das ausgewählte Asset Ausgabedarstellungen definiert sind.
   * **Bild-Modifikatoren** - Hier können zusätzliche Dynamic Media-Image-Serving-Befehle definiert werden, die durch `&`, unabhängig davon, **Vorgabetyp** ausgewählt ist.
* **Beschriftung** – Zusätzliche Informationen über das Bild, die standardmäßig unter dem Bild angezeigt werden.
   * **Beschriftung aus DAM abrufen** – Wenn die Option aktiviert ist, wird der Beschriftungstext des Bildes mit dem Wert der `dc:title`-Metadaten in DAM gefüllt. Nur verfügbar, wenn ein Asset aus dem DAM ausgewählt wurde.
   * **Beschriftung als Pop-up anzeigen** – Wenn die Option aktiviert ist, wird die Beschriftung nicht unter dem Bild angezeigt, sondern von einigen Browsern als Popup, wenn der Mauszeiger über das Bild bewegt wird.
* **Verknüpfung** – Verknüpfen Sie das Bild mit einer anderen Ressource.
   * Verwenden Sie das Dialogfeld „Auswahl“, um eine Verknüpfung zu einer anderen AEM-Ressource herzustellen.
   * Geben Sie die absolute URL ein, wenn Sie keine Verknüpfung zu einer AEM-Ressource erstellen. Nicht absolute URLs werden als relativ zu AEM interpretiert.
   * **Link in neuer Registerkarte öffnen** – Mit dieser Option wird der Link in einem neuen Browser-Fenster geöffnet.
* **ID** - Diese Option ermöglicht die Steuerung der eindeutigen Kennung der Komponente im HTML.
   * Wenn Sie das Feld leer lassen, wird automatisch eine eindeutige ID generiert, die Sie über die resultierende Seite finden.
   * Sofern eine ID angegeben wird, ist vom Autor sicherzustellen, dass diese eindeutig ist.
   * Eine Änderung der ID kann sich auf CSS auswirken.
* **Festgelegt mit** - Diese Option definiert die Breite des Bildes in Pixel.
* **Bild auf verfügbare Breite skalieren** - Diese Option gilt `"width":"100%"` zum Bildstil-Attribut.

>[!TIP]
>
>**Smartes Zuschneiden** und **Bildvorgabe** sind Optionen, die sich gegenseitig ausschließen. Wenn ein Autor eine Bildvorgabe zusammen mit einer Ausgabedarstellung von Typ „Smartes Zuschneiden“ verwenden muss, muss der Autor **Bild-Modifikatoren** verwenden, um Vorgaben manuell hinzuzufügen.

### Registerkarte „Arten“ {#styles-tab-edit}

![Registerkarte &quot;Stile&quot;im Dialogfeld &quot;Bearbeiten&quot;der E-Mail-Bildkomponente](/help/assets/image-configure-styles.png)

Die E-Mail-Bildkomponente unterstützt die AEM [Stilsystem.](/help/get-started/authoring.md#component-styling)

Verwenden Sie das Dropdown-Menü, um die Stile auszuwählen, die Sie auf die Komponente anwenden möchten. Die im Dialogfeld „Bearbeiten“ vorgenommenen Auswahlen haben denselben Effekt wie die in der Komponenten-Symbolleiste ausgewählten.

Stile müssen für diese Komponente im [Dialogfeld &quot;Design&quot;](#design-dialog) , damit die Registerkarte verfügbar ist.

## Dialogfeld „Design“ {#design-dialog}

### Registerkarte „Haupt“ {#main-tab}

![Registerkarte „Haupt“ im Dialogfeld „Design“ der Bildkomponente](/help/email/assets/email-image-design-main.png)

* **DM-Funktionen aktivieren** – Wenn diese Option aktiviert ist, sind die [Dynamic Media-Funktionen](#dynamic-media) verfügbar.
   * Diese Option wird nur angezeigt, wenn „Dynamic Media“ in der Umgebung aktiviert ist.
* **Web-optimierte Grafiken aktivieren** – Wenn diese Option aktiviert ist, liefert [der Web-optimierte Bildbereitstellungs-Service](/help/developing/web-optimized-image-delivery.md) Bilder im WebP-Format. Dadurch wird die Bildgröße durchschnittlich um 25 % verringert.
   * Diese Option ist nur in AEMaaCS verfügbar.
   * Wenn diese Option deaktiviert ist oder der Web-optimierte Bildbereitstellungsdienst nicht verfügbar ist, wird der [Adaptives Bildservlet](/help/developing/adaptive-image-servlet.md) verwendet.
* **Bild ist dekorativ** – Festlegen, ob die Option für dekorative Bilder automatisch aktiviert ist, wenn die Bildkomponente einer Seite hinzugefügt wird.
* **Alternativtext von DAM abrufen** - Festlegen, ob die Option zum Abrufen des Alternativtexts aus DAM automatisch aktiviert ist, wenn die Bildkomponente einer Seite hinzugefügt wird.
* **Beschriftung aus DAM abrufen** – Festlegen, ob die Option zum Abrufen der Beschriftung aus DAM automatisch aktiviert ist, wenn die Bildkomponente einer Seite hinzugefügt wird.
* **Beschriftung als Pop-up anzeigen** – Festlegen, ob die Option zum Anzeigen der Bildbeschriftung als Popup automatisch aktiviert ist, wenn die Bildkomponente einer Seite hinzugefügt wird.
* **Breite ändern** – Dieser Wert wird verwendet, um die Breite der Basisbilder zu ändern, die DAM-Assets sind.
   * Das Seitenverhältnis der Bilder wird beibehalten.
   * Wenn der Wert größer ist als die tatsächliche Breite des Bildes, hat dieser Wert keine Auswirkung.
   * Dieser Wert hat keine Auswirkungen auf SVG-Bilder.

Sie können eine Liste von Breiten in Pixeln für das Bild definieren, und die Komponente lädt, basierend auf der Browser-Größe, automatisch die am besten geeignete Breite. Dies ist ein wichtiger Teil der [Responsive Funktionen](#responsive-features) der E-Mail-Bildkomponente.

* **Breiten** – Definiert eine Liste der Breiten in Pixel für das Bild und die Komponente lädt automatisch die passende Breite basierend auf der Größe des Browsers.
   * Tippen oder klicken Sie auf die Schaltfläche **Hinzufügen**, um eine weitere Größe hinzuzufügen.
      * Verwenden Sie die Griffpunkte, um die Reihenfolge der Größen neu anzuordnen.
      * Verwenden Sie das Symbol **Löschen**, um eine Breite zu entfernen.
   * Standardmäßig wird das Laden von Bildern verzögert, bis sie sichtbar werden.
      * Wählen Sie die Option **Lazy Loading deaktivieren** aus, um die Bilder schon beim Laden der Seite zu laden.
* **JPEG-Qualität** – Der Qualitätsfaktor (in Prozent von 0 bis 100) für umgewandelte (z. B. skalierte oder zugeschnittene) JPEG-Bilder.
* **Standardbreite** - Die Standardbreite von Bildern in Pixel, die im Dialogfeld &quot;Design&quot;verwendet werden

>[!TIP]
>
>Tipps zur Optimierung der Auswahl für die Ausgabedarstellung durch sorgfältige Definition der Breiten finden Sie im Dokument [Adaptive Image Servlet](/help/developing/adaptive-image-servlet.md).

### Registerkarte „Stile“ {#styles-tab}

Die E-Mail-Bildkomponente unterstützt die AEM [Stilsystem](/help/get-started/authoring.md#component-styling).
