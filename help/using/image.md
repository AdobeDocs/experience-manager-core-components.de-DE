---
title: Bildkomponente
seo-title: Bildkomponente
description: Die Core Component Image Component ist eine Komponente für adaptive Bildkomponenten, die ersetzende Bearbeitung bietet.
seo-description: Die Core Component Image Component ist eine Komponente für adaptive Bildkomponenten, die ersetzende Bearbeitung bietet.
uuid: 1 a 229 d 42-2428-43 aa -895 a -9 b 7 c 1 bf 2834
contentOwner: Benutzer
content-type: Referenz
topic-tags: authoring
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-new
discoiquuid: d 4684 f 33-2 fb 5-4 f 32-866 f -7136 cf 1800 d 7
translation-type: tm+mt
source-git-commit: 1bbec9b1f109df88964dce051a58d111bf6cafaa

---


# Bildkomponente{#image-component}

Die Core Component Image Component ist eine Komponente des adaptiven Bilds, die eine ersetzende Bearbeitung bietet.

## Nutzung {#usage}

Die Image-Komponente ermöglicht eine einfache Platzierung von Bild-Assets und bietet eine ersetzende Bearbeitung. Es bietet eine adaptive Bildauswahl mit verzögertem Laden sowie Beschneiden für den Inhaltsautor.

Die Bildbreiten sowie die Beschneidung und zusätzliche Einstellungen können vom Vorlagenautor im [Designdialogfeld definiert](#design-dialog)werden. Der Content-Editor kann Assets im Dialogfeld [&quot;Konfigurieren&quot; hochladen oder auswählen](#configure-dialog) und das Bild im [Bearbeitungsdialogfeld](#edit-dialog)beschneiden. Zur einfachen Vereinfachung ist auch einfach ersetzende Änderungen des Bildes verfügbar.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Image-Komponente ist v 2, die mit Version 2.0.0 der Kernkomponenten im Januar 2018 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v2 | Kompatibel | Kompatibel | Kompatibel |
| [v1](image-v1.md) | Kompatibel | Kompatibel | Kompatibel |

Weitere Informationen zu Core-Komponentenversionen und -versionen finden Sie in den Core [-Komponentenversionen](versions.md).

## SVG-Unterstützung {#svg-support}

Skalierbare Vektorgrafiken (SVG) werden von der Image-Komponente unterstützt.

* Die Drag &amp; Drop eines SVG-Assets aus DAM und das Hochladen eines SVG-Datei-Uploads aus einem lokalen Dateisystem werden beide unterstützt.
* Die adaptiven Bildservlet-Streams werden gestreamt (Konvertierungen werden übersprungen).
* Bei einem SVG-Bild werden die &quot;Smart Images&quot; und die&quot; Smart-Größen&quot; auf ein leeres Array im Bildmodell festgelegt.

### Sicherheit {#security}

Aus Sicherheitsgründen wird die ursprüngliche SVG nicht direkt vom Bild-Editor aufgerufen. It is called through `<img src=“path-to-component”>`. Der Browser verhindert, dass Skripten, die in der SVG-Datei eingebettet sind, nicht ausgeführt werden.

>[!CAUTION]
>
>Der SVG-Support erfordert Version 2.1.0 der Kernkomponenten oder höher zusammen mit [Service Pack 2](https://helpx.adobe.com/experience-manager/6-4/release-notes/sp-release-notes.html) für AEM 6.4 oder [Service Pack 3](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html) für AEM 6.3 oder höher, um [neue Bildbearbeitungsfunktionen](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/image-editor.html) in AEM zu unterstützen.

## Musterkomponentenausgabe {#sample-component-output}

Nachfolgend finden Sie ein Beispiel aus [We. Retail](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html).

### Screenshot {#screenshot}

![](assets/chlimage_1-7.png)

### Komponentenbibliothek

Rufen Sie die [Komponentenbibliothek auf, um die Image-Komponente sowie Beispiele für die Konfigurationsoptionen sowie HTML- und JSON-Ausgabe zu erhalten](http://opensource.adobe.com/aem-core-wcm-components/library/image.html).

### Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur Bildkomponente [finden Sie unter github](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/image/v2/image).

Weitere Informationen zur Entwicklung Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Komponenten](developing.md).

>[!NOTE]
>
>Ab Version 2.1.0 von Core Components unterstützt die Image-Komponente [schema.org microdata](https://schema.org).

## Dialogfeld konfigurieren {#configure-dialog}

Zusätzlich zum standardmäßigen [Dialogfeld](#edit-dialog) zum Bearbeiten und [Entwerfen bietet die Image](#design-dialog)-Komponente ein Dialogfeld für die Konfiguration, bei dem das Bild selbst mit der Beschreibung und den grundlegenden Eigenschaften definiert wird.

### Asset-Registerkarte {#asset-tab}

![](assets/screen_shot_2018-01-08at114245.png)

* **Bild-Asset**
   * Legen Sie ein Asset aus dem [Asset-Browser ab](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/author-environment-tools.html) oder tippen Sie auf die **Durchsuchen** -Option, um es aus einem lokalen Dateisystem hochzuladen.
   * Tippen oder klicken **Sie auf Leeren** , um das aktuell ausgewählte Bild zu deaktivieren.
   * Tippen oder klicken **Sie auf Bearbeiten** , um [die Darstellungen des Assets](https://helpx.adobe.com/experience-manager/6-5/assets/using/managing-assets-touch-ui.html) im Asset Editor zu mange.

### Registerkarte &quot;Metadaten « {#metadata-tab}

![](assets/screen_shot_2018-01-08at114527.png)

* **Bild ist dekorativ**,
wenn das Bild von Hilfstechnologien ignoriert werden soll und daher kein alternativer Text benötigt wird. Dies gilt nur für dekorative Bilder.
* **Alternative Textalternative Textalternative**
der Bedeutung oder Funktion des Bilds für Sehbehinderte.
   * Alternativen Text von DAM abrufen: Wenn geprüft wird, ob der Alternativtext des Bilds mit dem Wert der `dc:description` Metadaten in DAM gefüllt ist.

* **Beschriftung**
Zusätzliche Informationen über das Bild, die standardmäßig unter dem Bild angezeigt werden.
   * **Beschriftung von DAM**
abrufen, wenn der Beschriftungstext des Bilds mit dem Wert der `dc:title` Metadaten in DAM gefüllt wird.
   * **Beschriftung als Popup**
anzeigen Wenn aktiviert, wird die Beschriftung nicht unter dem Bild angezeigt, sondern als Popup, der von einigen Browsern angezeigt wird, wenn die Maus über das Bild bewegt wird.

* **Verknüpfung**
   * Verknüpfen Sie das Bild mit einer anderen Ressource.
   * Verwenden Sie das Auswahldialogfeld, um eine Verknüpfung zu einer anderen AEM-Ressource herzustellen.
   * Geben Sie die absolute URL ein, wenn Sie keine Verknüpfung zu einer AEM-Ressource erstellen. Nicht-Solute-urls werden relativ zu AEM interpretiert.

## Dialogfeld bearbeiten {#edit-dialog}

Das Dialogfeld &quot;Bearbeiten&quot; ermöglicht dem Autor das Beschneiden, Ändern der Startkarte und das Zoomen des Bildes.

![](assets/chlimage_1-8.png)

* Beschneiden beginnen

   ![](assets/chlimage_1-9.png)

   Wenn Sie diese Option auswählen, wird eine Dropdown-Liste für vordefinierte Beschnittrahmen geöffnet.

   * Wählen Sie die Option **&quot;Frei&quot;** , um Ihren eigenen Beschneidungstext zu definieren.
   * Wählen Sie &quot;Beschneiden **entfernen** &quot; , um das ursprüngliche Asset anzuzeigen.
   Nachdem Sie eine Beschneidungsoption ausgewählt haben, verwenden Sie die blauen Griffe, um die Beschneidung auf dem Bild anzupassen.

   ![](assets/chlimage_1-10.png)

* Nach rechts drehen

   ![](assets/chlimage_1-11.png)

   Verwenden Sie diese Option, um das Bild um 90 ° nach rechts (im Uhrzeigersinn) zu drehen.

* Horizontal spiegeln

   ![](assets/screen_shot_2018-04-16at091404.png)

   Verwenden Sie diese Option, um das Bild horizontal zu spiegeln oder um 180 ° entlang der y-Achse zu drehen.

* Vertikal spiegeln

   ![](assets/screen_shot_2018-04-16at091410.png)

   Verwenden Sie diese Option, um das Bild vertikal zu spiegeln oder um 180 ° entlang der x-Achse zu drehen.

* Startkarte

   >[!CAUTION]
   >
   >Die Startkarte-Funktion erfordert Version 2.1.0 der Kernkomponenten oder höher zusammen mit [Service Pack 2](https://helpx.adobe.com/experience-manager/6-4/release-notes/sp-release-notes.html) für AEM 6.4 oder [Service Pack 3](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html) für AEM 6.3 oder höher, um [neue Bildbearbeitungsfunktionen](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/image-editor.html) in AEM zu unterstützen.

   ![](assets/chlimage_1-12.png)

   Verwenden Sie diese Option, um eine Startkarte auf das Bild anzuwenden. Wenn Sie diese Option auswählen, wird ein neues Fenster geöffnet, in dem der Benutzer die Form der Karte auswählen kann:

   * **Rechteckige Karte hinzufügen**
   * **Kreisdiagramm hinzufügen**
   * **Polygon-Map hinzufügen**
      * Standardmäßig wird eine Dreiecksmap hinzugefügt. Doppelklicken Sie auf eine Zeile der Form, um einer neuen Seite einen neuen blauen Größengriff hinzuzufügen.
   Nachdem eine Map-Form ausgewählt wurde, wird das Bild überlagert, um die Größe zu ändern. Ziehen Sie die blauen Größenänderungsgriffe per Drag &amp; Drop, um die Form anzupassen.

   ![](assets/chlimage_1-13.png)

   Nachdem Sie die Startkarte gepostet haben, klicken Sie darauf, um eine schwebende Symbolleiste zu öffnen, um den Pfad des Links zu definieren.

   * **Pfad**
      * Verwenden Sie die Option Pfadauswahl, um einen Pfad in AEM auszuwählen.
      * Wenn der Pfad nicht in AEM angegeben ist, verwenden Sie die absolute URL. Nicht absolute Pfade werden relativ zu AEM interpretiert.
   * **Alternative Beschreibung**
des Pfadziels Alternative Beschreibung
   * **Target**
      * **Gleiche Registerkarte**
      * **Neue Registerkarte**
      * **Übergeordneter Frame**
      * **Top-Frame**
   Tippen oder klicken Sie auf das blaue Häkchen zum Speichern, das schwarze X zum Abbrechen und den roten Papierkorb, um die Karte zu löschen.

   ![](assets/chlimage_1-14.png)

* Zoom zurücksetzen

   ![](assets/chlimage_1-15.png)

   Wenn das Bild bereits gezoomt wurde, verwenden Sie diese Option, um den Zoomgrad zurückzusetzen.

* Zoom-Regler öffnen

   ![](assets/chlimage_1-16.png)

   Mit dieser Option können Sie einen Schieberegler anzeigen, um den Zoomgrad des Bildes zu steuern.

   ![](assets/chlimage_1-17.png)

Der ersetzende Editor kann auch zum Ändern des Bildes verwendet werden. Aufgrund von Leerzeichen sind nur einfache Optionen verfügbar. Für vollständige Bearbeitungsoptionen verwenden Sie den Vollbildmodus.

![](assets/chlimage_1-18.png)

>[!NOTE]
>
>Bildbearbeitungsvorgänge (Beschneiden, Spiegeln, Drehen) werden für GIF-Bilder nicht unterstützt. Alle Änderungen, die im Bearbeitungsmodus an GIFS vorgenommen wurden, bleiben bestehen.

## Design-Dialogfeld {#design-dialog}

Das Design-Dialogfeld ermöglicht es dem Vorlagenautor, die Beschneidungs-, Upload- und Drehung- und Upload-Optionen zu definieren, die der Inhaltsautor bei Verwendung dieser Komponente hat.

### Hauptregisterkarte {#main-tab}

Auf der **Registerkarte &quot;Main&quot;** können Sie eine Liste der Breiten in Pixel definieren, um das Bild automatisch in die gewünschte Breite aus der Liste zu laden.

Darüber hinaus können Sie festlegen, welche allgemeinen Komponentenoptionen automatisch oder deaktiviert werden, wenn der Autor die Komponente einer Seite hinzufügt.

![](assets/screenshot_2018-10-19at102756.png)

* **Verzögertes Laden**
aktivieren, wenn die Option für verzögertes Laden automatisch aktiviert ist, wenn die Bildkomponente einer Seite hinzugefügt wird.
* **Bild ist dekorativ**
Definiert, wenn die dekorative Bildoption automatisch aktiviert ist, wenn die Bildkomponente einer Seite hinzugefügt wird.
* **Alternativen Text aus DAM**
abrufen, wenn die Option zum Abrufen des alternativen Textes aus DAM automatisch aktiviert ist, wenn die Bildkomponente einer Seite hinzugefügt wird.
* **Beschriftung von DAM**
abrufen, wenn die Option zum Abrufen der Beschriftung von DAM automatisch aktiviert ist, wenn die Bildkomponente einer Seite hinzugefügt wird.
* **Beschriftung als Popup
definieren** definieren, wenn die Option zum Anzeigen der Bildbeschriftung automatisch aktiviert ist, wenn die Bildkomponente einer Seite hinzugefügt wird.
* **Deaktivieren Sie die UUID-Verfolgung**,
um die Verfolgung der UUID des Bild-Assets zu deaktivieren.

* **Breiten**
Definieren eine Liste der Breiten in Pixel, um das Bild automatisch in der Liste zu laden.
   * Tippen oder klicken Sie auf **die Schaltfläche Hinzufügen** , um eine weitere Größe hinzuzufügen.
      * Verwenden Sie die Griffpunkte, um die Reihenfolge der Größen neu anzuordnen.
      * Verwenden Sie das **Symbol Löschen** , um eine Breite zu entfernen.
   * Standardmäßig werden Bilder, die geladen werden, deinstalliert, bis sie sichtbar werden.
      * Wählen Sie die Option **Verzögertes Laden** deaktivieren, um die Bilder beim Laden der Seite zu laden.
* **JPEG-Qualität**
Der Qualitätsfaktor (in Prozent zwischen 0 und 100) für transformierte (z. B. skalierte oder beschnittene) JPEG-Bilder.

>[!CAUTION]
>
>Die Option JPEG-Qualität ist ab Version 2.2.0 der Core-Komponenten verfügbar.

>[!NOTE]
>
>Ab Version 2.2.0 der Core-Komponenten fügt die Image-Komponente das eindeutige UUID-Attribut `data-asset-id` dem Bild-Asset hinzu, um die Verfolgung und Analyse der Anzahl der Ansichten zu ermöglichen, die einzelne Assets empfangen.

### Registerkarte &quot;Funktionen « {#features-tab}

Auf der **Registerkarte &quot;Funktionen** &quot; können Sie festlegen, welche Optionen den Autoren für Inhalte zur Verfügung stehen, wenn Sie die Komponente verwenden, einschließlich Optionen für Upload-Optionen, Ausrichtung und Beschneiden.

* Quelle

   ![](assets/chlimage_1-19.png)

   Wählen Sie die Option **zum Hochladen von Assets aus dem Dateisystem** zulassen, damit Autoren von Inhalten Bilder von seinem lokalen Computer hochladen können. Wenn Sie erzwingen möchten, dass Autoren nur Assets aus AEM auswählen, wählen Sie diese Option aus.

* Ausrichtung

   ![](assets/chlimage_1-20.png)

* **Drehen**
Sie diese Option, damit der Inhaltsautor die Option &quot;Rechts **drehen&quot; verwenden** kann.
* **Verwenden Sie diese**
Option, damit der Inhaltsautor die Option &quot;Horizontal **spiegeln** «und **&quot; Vertikal** spiegeln&quot; verwenden kann.

   >[!CAUTION]
   >
   >Die **Option &quot;Spiegeln&quot;** ist standardmäßig deaktiviert. Durch Aktivieren wird im Dialogfeld &quot;Bearbeiten&quot; der Image-Komponente die **Schaltflächen&quot; Vertikal** spiegeln&quot; und **&quot;Horizontal** spiegeln&quot; angezeigt. Die Funktion wird jedoch derzeit nicht von AEM unterstützt, und die Änderungen, die mit diesen Optionen vorgenommen wurden, bleiben nicht erhalten.

<!-- 
Comment Type: remark
Last Modified By: Chris Bohnert (bohnert)
Last Modified Date: 2017-11-20T05:51:34.378-0500

<p>Added caution based on CQDOC-11457. Hid the flip options in the procedure using the <strong>Draft</strong> option so that when this feature is implemented in CQ-4221539, the <strong>Draft</strong> property can simply be removed along with the caution.</p>
 -->

* Beschneiden

   ![](assets/chlimage_1-21.png)

   Wählen Sie die Option **&quot;Beschneiden** zulassen&quot; aus, damit der Inhaltsautor das Bild in der Komponente im Bearbeitungsdialogfeld beschneiden kann.
   * Klicken **Sie auf Hinzufügen** , um ein vordefiniertes Beschneidungsseitenverhältnis hinzuzufügen.
   * Geben Sie einen beschreibenden Namen ein, der im **Dropdown-** Menü &quot;Beschneiden&quot; angezeigt wird.
   * Geben Sie das numerische Verhältnis des Aspekts ein.
   * Verwenden Sie die Ziehpunkte, um die Reihenfolge des Seitenverhältnisses neu anzuordnen.
   * Verwenden Sie das Papierkorbsymbol, um ein Seitenverhältnis zu löschen.
   >[!CAUTION]
   >
   >Beachten Sie, dass in AEM Seitenverhältnisse als **Höhe/Breite definiert** werden. Dies unterscheidet sich von der herkömmlichen Definition von Breite/Höhe und erfolgt aus älteren Kompatibilitätsgründen. Die Autoren des Inhalts achten auf keine Unterschiede, solange Sie einen klaren Namen des Verhältnisses angeben, da der Name in der Benutzeroberfläche angezeigt wird und nicht das Verhältnis selbst.

### Stile Registerkarte {#styles-tab-1}

Die Image-Komponente unterstützt das AEM [-Stilsystem](authoring.md#component-styling).