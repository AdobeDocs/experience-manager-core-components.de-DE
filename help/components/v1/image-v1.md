---
title: Bildkomponente (v1)
description: Die Kernkomponente „Bildkomponente“ ist eine anpassungsfähige Bildkomponente mit Funktionen zur Bearbeitung im Kontext.
index: n
role: Architektur, Entwickler, Administrator, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '1234'
ht-degree: 99%

---


# Bildkomponente (v1) {#image-component-v}

Die Kernkomponente „Bildkomponente“ ist eine anpassungsfähige Bildkomponente mit Funktionen zur Bearbeitung im Kontext.

## Verwendung {#usage}

Die Bildkomponente ermöglicht das einfache Platzieren von Bildmaterial und bietet die Möglichkeit zur direkten Bearbeitung. Es bietet eine anpassungsfähige Bildauswahl mit verzögertem Laden sowie Beschneiden für den Inhaltsautor.

Die zulässigen Bildbreiten sowie das Zuschneiden und zusätzliche Einstellungen können hier vom Vorlagenautor definiert werden [Designdialogfeld ](#design-dialog). Der Inhaltseditor kann Assets im [Dialogfeld „Konfigurieren“](#configure-dialog) hochladen oder auswählen und das Bild im [Dialogfeld „Bearbeiten“](#edit-dialog) beschneiden. Für zusätzlichen Komfort ist auch eine einfache, ersetzende Änderung des Bildes verfügbar.

## Version und Kompatibilität {#version-and-compatibility}

In diesem Dokument wird v1 der Bildkomponente beschrieben, die ursprünglich mit Version 1.0.0 der Kernkomponenten mit AEM 6.3 eingeführt wurde.

In der folgenden Tabelle ist die Kompatibilität der Bildkomponente v1 aufgeführt.

| AEM-Version | Bildkomponente v1 |
|--- |--- |
| 6.3 | Kompatibel |
| 6.4 | Kompatibel |

>[!CAUTION]
>
>In diesem Dokument wird die Bildkomponente v1 beschrieben.
>
>Weitere Informationen zur aktuellen Version der Bildkomponente finden Sie im Dokument [ Bildkomponente ](/help/components/image.md) .

## Musterkomponentenausgabe {#sample-component-output}

Im Folgenden finden Sie ein Beispiel von [We.Retail](https://helpx.adobe.com/de/experience-manager/6-4/sites/developing/using/we-retail.html).

### Screenshot {#screenshot}

![](/help/assets/chlimage_1-7.png)

### HTML {#html}

```
<div class="cmp cmp-image aem-GridColumn aem-GridColumn--default--12">
 
        <noscript data-cmp-image="{&#34;smartImages&#34;:[],&#34;smartSizes&#34;:[],&#34;lazyEnabled&#34;:true}">
            <img src="/content/we-retail/us/en/equipment/_jcr_content/root/responsivegrid/image.img.jpg" alt="Surfboard"/>
        </noscript>

</div>
```

### JSON {#json}

```
"image": {
              "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
              "smartSizes": [],
              "smartImages": [],
              "lazyEnabled": true,
              "src": "/content/we-retail/us/en/equipment/equipment/jcr%3acontent/root/responsivegrid/image.img.jpeg",
              ":type": "weretail/components/content/image"
            }
```

>[!NOTE]
>
>Für JSON-Exporte aus den Kernkomponenten ist Version 1.1.0 der Kernkomponenten erforderlich. Weitere Informationen finden Sie in den [Kompatibilitätsinformationen für Kernkomponenten v1](/help/versions.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Zusätzlich zum standardmäßigen [Dialogfeld „Bearbeiten“](#edit-dialog) und zum [Dialogfeld „Design“](#design-dialog) bietet die Bildkomponente ein Dialogfeld für die Konfiguration, bei dem das Bild selbst mit seiner Beschreibung und den grundlegenden Eigenschaften definiert wird.

![](/help/assets/chlimage_1-50.png)

* **Bild-Asset**
   * Ziehen Sie ein Asset aus dem [Asset-Browser](https://helpx.adobe.com/experience-manager/6-3/sites/authoring/using/author-environment-tools.html#main-pars_title) oder tippen Sie auf die Option **Durchsuchen**, um es von einem lokalen Dateisystem hochzuladen.
   * Tippen oder klicken Sie auf **Löschen**, um das aktuell ausgewählte Bild zu deaktivieren.
   * Tippen oder klicken Sie auf **Bearbeiten**, um die [Ausgabedarstellungen des Assets](https://helpx.adobe.com/experience-manager/6-3/assets/using/managing-assets-touch-ui.html#main-pars_title_19) im Asset-Editor zu verwalten.

* **Bild ist dekorativ** - Überprüfen Sie, ob das Bild von Hilfstechnologien ignoriert werden soll und daher keinen alternativen Text erfordert. Dies gilt nur für dekorative Bilder.
* **Alternativer Text** - Textalternativen zur Bedeutung oder Funktion des Bildes für sehbeeinträchtigte Leser.
* **Verknüpfung**
   * Verknüpfen Sie das Bild mit einer anderen Ressource.
   * Verwenden Sie das Dialogfeld „Auswahl“, um eine Verknüpfung zu einer anderen AEM-Ressource herzustellen.
   * Geben Sie die absolute URL ein, wenn Sie keine Verknüpfung zu einer AEM-Ressource erstellen. Nicht absolute URLs werden als relativ zu AEM interpretiert.

* **Beschriftung** - Zusätzliche Informationen über das Bild, die unter dem Bild angezeigt werden, sind standardmäßig verfügbar.
* **Beschriftung als Pop-up anzeigen** - Wenn die Option aktiviert ist, wird die Beschriftung nicht unter dem Bild angezeigt, sondern von einigen Browsern als Pop-up, wenn der Mauszeiger über das Bild bewegt wird.

## Dialogfeld „Bearbeiten“ {#edit-dialog}

Das Dialogfeld „Bearbeiten“ ermöglicht dem Inhaltsautor das Zuschneiden, Ändern der Startkarte und das Zoomen des Bildes.

![](/help/assets/chlimage_1-8.png)

* Zuschneiden beginnen

   ![](/help/assets/chlimage_1-9.png)

   Wenn Sie diese Option auswählen, wird eine Dropdown-Liste für vordefinierte Zuschneideproportionen geöffnet.

   * Wählen Sie die Option **Freihand**, um Ihre eigene Zuschnittsart zu definieren.
   * Wählen Sie **Zuschnitt entfernen**, um das ursprüngliche Asset anzuzeigen.

   Nachdem Sie eine Zuschnittoption ausgewählt haben, verwenden Sie die blauen Griffe, um die Beschneidung auf dem Bild anzupassen.

   ![](/help/assets/chlimage_1-10.png)

* Nach rechts drehen

   ![](/help/assets/chlimage_1-11.png)

   Verwenden Sie diese Option, um das Bild um 90° nach rechts (im Uhrzeigersinn) zu drehen.

* Startkarte

   ![](/help/assets/chlimage_1-12.png)

   Verwenden Sie diese Option, um eine Startkarte auf das Bild anzuwenden. Wenn der Benutzer diese Option auswählt, wird ein neues Fenster geöffnet, in dem er die Form der Karte auswählen kann:

   * **Rechteckige Karte hinzufügen**
   * **Kreisdiagramm hinzufügen**
   * **Polygon-Karte hinzufügen**

      * Standardmäßig wird eine Dreieckskarte hinzugefügt. Doppelklicken Sie auf eine Linie der Form, um zu einer neuen Seite einen neuen blauen Griff zur Größenanpassung hinzuzufügen.

   Nachdem eine Karten-Form ausgewählt wurde, wird sie mit dem Bild überlagert, sodass die Größe geändert werden kenn. Ziehen Sie die blauen Größenänderungsgriffe per Drag-and-Drop, um die Form anzupassen.

   ![](/help/assets/chlimage_1-13.png)

   Nachdem Sie die Größe der Startkarte angepasst haben, klicken Sie darauf, um eine schwebende Symbolleiste zu öffnen, um den Pfad des Links zu definieren.

   * **Pfad**
      * Verwenden Sie die Option „Pfadwähler“, um einen Pfad in AEM auszuwählen.
      * Wenn der Pfad sich nicht in AEM befindet, verwenden Sie die absolute URL. Nicht absolute Pfade werden relativ zu AEM interpretiert.

      * **Alternativer Text**
Alternative Beschreibung des Pfadziels
      * **Target**
         * **Selbe Registerkarte**
         * **Neue Registerkarte**
         * **Übergeordneter Frame**
         * **Top-Frame**

   Tippen oder klicken Sie auf das blaue Häkchen zum Speichern, auf das schwarze X zum Abbrechen oder auf den roten Papierkorb, um die Karte zu löschen.

   ![](/help/assets/chlimage_1-14.png)

* Zoom zurücksetzen

   ![](/help/assets/chlimage_1-15.png)

   Wenn das Bild bereits gezoomt wurde, verwenden Sie diese Option, um den Zoom-Grad zurückzusetzen.

* Zoom-Regler öffnen

   ![](/help/assets/chlimage_1-16.png)

   Mit dieser Option können Sie einen Schieberegler anzeigen, um den Zoom-Grad des Bildes zu steuern.

   ![](/help/assets/chlimage_1-17.png)

Der Editor für die Bearbeitung im Kontext kann auch zum Ändern des Bildes verwendet werden. Aus Platzgründen sind nur einfache Optionen inline verfügbar. Für vollständige Bearbeitungsoptionen verwenden Sie den Vollbildmodus.

![](/help/assets/chlimage_1-18.png)

>[!NOTE]
>
>Bildbearbeitungsvorgänge (Beschneiden, Spiegeln, Drehen) werden für GIF-Bilder nicht unterstützt. Alle Änderungen, die im Bearbeitungsmodus an GIFs vorgenommen wurden, bleiben nicht bestehen.

## Dialogfeld „Design“ {#design-dialog}

Das Dialogfeld „Design“ ermöglicht dem Vorlagenautor die Definition von Zuschnitt, Upload und Rotations-Upload, die vom Inhalts-Autor bei der Verwendung dieser Komponente genutzt werden.

### Allgemein {#main}

In dieser Registerkarte **Allgemein** können Sie eine Liste der zulässigen Breiten in Pixel definieren, damit das Bild automatisch die angemessenste Breite aus der Liste laden wird.

![](/help/assets/chlimage_1-51.png)

Tippen oder klicken Sie auf „Hinzufügen“, um eine weitere Größe hinzuzufügen.

* Verwenden Sie die Griffpunkte, um die Reihenfolge der Größen neu anzuordnen.
* Verwenden Sie das Symbol „Löschen“, um eine Breite zu entfernen.

Standardmäßig wird das Laden von Bildern verzögert, bis sie sichtbar werden. Wählen Sie die Option **Lazy Loading deaktivieren**, um die Bilder schon beim Laden der Seite zu laden.

### Funktionen {#features}

Auf der Registerkarte **Funktionen** können Sie festlegen, welche Optionen den Inhaltsautoren zur Verfügung stehen, wenn sie die Komponente verwenden, einschließlich Optionen fürs Hochladen, Ausrichtung und Beschneiden.

* Quelle

   ![](/help/assets/chlimage_1-19.png)

   Wählen Sie die Option **Asset-Uploads aus Dateisystem zulassen**, damit Inhaltsautoren Bilder von ihrem lokalen Computer hochladen können. Wenn Sie erzwingen möchten, dass Autoren nur Assets aus AEM auswählen, wählen Sie diese Option ab.

* Ausrichtung

   ![](/help/assets/chlimage_1-20.png)

   * **Drehen** - Verwenden Sie diese Option, damit der Inhaltsautor die Option **Nach Rechts drehen** verwenden kann.
   * **Spiegeln**
Verwenden Sie diese Option, damit der Inhaltsautor die Optionen 
**Horizontal spiegeln** und **Vertikal spiegeln** verwenden kann.
   >[!CAUTION]
   >
   >Die Option **Spiegeln** ist standardmäßig deaktiviert. Durch Aktivieren werden im Dialogfeld „Bearbeiten“ der Bildkomponente die Felder **Vertikal spiegeln** und **Horizontal spiegeln** angezeigt. Die Funktion wird jedoch derzeit nicht von AEM unterstützt, und die Änderungen, die mit diesen Optionen vorgenommen werden, bleiben nicht erhalten.

* Beschneiden

   ![](/help/assets/chlimage_1-21.png)

   Wählen Sie die Option **Beschneiden zulassen** aus, damit der Inhaltsautor das Bild in der Komponente im Dialogfeld „Bearbeiten“ beschneiden kann.
   * Klicken Sie auf **Hinzufügen**, um ein vordefiniertes Bildseitenverhältnis hinzuzufügen.
   * Geben Sie einen beschreibenden Namen ein, der im Dropdown-Menü **Zuschneiden** angezeigt wird.
   * Geben Sie das numerische Seitenverhältnis des Bildes ein.
   * Verwenden Sie die Ziehpunkte, um die Reihenfolge der Seitenverhältnisse neu anzuordnen.
   * Verwenden Sie das Papierkorbsymbol, um ein Seitenverhältnis zu löschen.

   >[!CAUTION]
   >
   >Beachten Sie, dass die Beschneidungsverhältnisse als **Höhe/Breite** definiert sind. Dies unterscheidet sich von der herkömmlichen Definition als Breite/Höhe und erfolgt aus Gründen der Legacy-Kompatibilität. Den Inhaltsautoren wird kein Unterschied bewusst werden, solange Sie einen klaren Namen für das Verhältnis angeben, da nur der Name in der Benutzeroberfläche angezeigt wird und nicht das Verhältnis selbst.

## Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur Bildkomponente [finden Sie auf GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/image/v1/image).

Das gesamte Kernkomponentenprojekt kann von GitHub heruntergeladen werden.

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).
