---
title: Integration von Kernkomponenten und Adobe Experience Platform Launch über die Adobe Client-Datenschicht
description: 'Konfigurieren von Adobe Experience Platform Launch für die Registrierung von Kernkomponenten-Ereignissen mit Adobe Experience Platform Launch '
translation-type: ht
source-git-commit: 85fb3612aed12b7bfdc05f0a569ae7c7364e6121
workflow-type: ht
source-wordcount: '1160'
ht-degree: 100%

---


# Integration von Kernkomponenten und Adobe Experience Platform Launch über die Adobe Client-Datenschicht{#launch-integration}

Die Integration der Kernkomponenten in Adobe Experience Platform Launch erfolgt mithilfe der Adobe Client-Datenschicht. Dieses Dokument zeigt dies am Beispiel der Konfiguration für das Tracking von Bildkomponenten in Adobe Experience Platform Launch.

Durch diese Konfiguration liefert Experience Platform Launch die folgende Ausgabe in der Browser-Konsole, wenn auf eine Bild-Kernkomponente geklickt wird.

![Beispiel für Ausgabe der Konsole ](/help/assets/launch-console-output.png)

## Integrieren von Experience Platform Launch mit AEM {#launch-aem}

Zunächst müssen Sie Adobe Experience Platform Launch mit Ihrer AEM-Site integrieren.

### Schritt 1: Erstellen einer Integration in Adobe I/O {#create-io-integration}

Melden Sie sich zunächst bei Adobe I/O an, um die Konfiguration einer Integration anzulegen.

1. Rufen Sie `https://console.adobe.io` auf.
1. Melden Sie sich mit Ihrer Adobe ID an.
1. Klicken Sie im Bereich „Quick Start“ (Schnellstart) auf die Schaltfläche **Create Integration** (Integration erstellen).
1. Wählen Sie **Access an API** (Auf API zugreifen) aus und klicken Sie auf **Continue** (Weiter).
1. Wählen Sie unterhalb des Eintrags „Adobe Experience Platform“ **Experience Platform Launch API** aus und klicken Sie auf **Continue** (Weiter).

### Schritt 2: Erstellen einer IMS-Konfiguration in AEM {#ims-configuration}

Sie müssen in AEM die Integration definieren, die Sie durch Anlegen der Konfiguration in Adobe I/O begonnen haben.

1. Wechseln Sie zur Startseite von AEM und klicken Sie auf **Tools > Sicherheit > Adobe IMS-Konfigurationen**.
1. Klicken Sie auf **Erstellen**.
1. Wählen Sie für **Cloud-Lösung** die Option **Adobe Experience Platform Launch** aus.
1. Klicken Sie auf **Neues Zertifikat erstellen**.
1. Geben Sie einen Alias für das Zertifikat ein, z. B. **aem-launch-certificate**.
1. Klicken Sie auf **Zertifikat erstellen** und im daraufhin angezeigten Popup-Fenster auf **OK**, um das Zertifikat zu erstellen.
1. Klicken Sie auf **Öffentlichen Schlüssel herunterladen** und im daraufhin angezeigten Popup-Fenster auf **Herunterladen**.

### Schritt 3: Abschließen der Adobe I/O-Konfiguration {#finish-io}

Mit dem in der AEM IMS-Konfiguration erstellten Zertifikat und Schlüssel können Sie Ihre Adobe I/O-Konfiguration abschließen.

1. Wechseln Sie zur Adobe I/O-Konsole, wie in [Schritt 1](#create-io-integration) beschrieben.
1. Geben Sie im Fenster **Create a new Integration** (Neue Integration erstellen) einen Namen und eine Beschreibung ein, z. B. **AEM Launch-Datenschicht**.
1. Laden Sie in den **Zertifikaten mit öffentlichen Schlüsseln** das Zertifikat hoch, das Sie in [Schritt 2](#ims-configuration) erstellt haben.
1. Wählen Sie das Profil **Launch - Prod**.
1. Klicken Sie auf **Create Integration** (Integration erstellen).
1. Klicken Sie auf **Continue to integration details** (Weiter zu Integrationsdetails). Sie benötigen diese Details, um im nächsten Schritt die IMS-Konfiguration in Ihrer AEM-Instanz abzuschließen.

### Schritt 4: Abschließen der IMS-Konfiguration {#finish-ims}

Anhand der Integrationsdetails aus Adobe I/O können Sie die AEM IMS-Konfiguration abschließen.

1. Klicken Sie auf der AEM-Registerkarte unter der Registerkarte für die **Konfiguration des technischen Adobe IMS-Kontos** aus [Schritt 2](#ims-configuration) auf **Weiter**.
1. Geben Sie einen Titel ein, z. B. **IMS-Konfiguration für Adobe Experience Platform Launch**.
1. Kopieren Sie auf der Adobe I/O-Registerkarte den **API-Schlüssel (Client-ID)**.
1. Fügen Sie auf der AEM-Registerkarte den kopierten Schlüssel in das Feld **API-Schlüssel** ein.
1. Klicken Sie in Adobe I/O auf **Retrieve Client Secret** (Geheimen Client-Schlüssel abrufen) und kopieren Sie diesen.
1. Fügen Sie ihn auf der AEM-Registerkarte in das Feld **Client-Geheimnis** ein.
1. Wählen Sie auf der Adobe I/O-Registerkarte die Registerkarte **JWT** und kopieren Sie die URL, z. B. `https://ims-na1.adobelogin.com`.
1. Fügen Sie sie auf der AEM-Registerkarte in das Feld **Autorisierungsserver** ein.
1. Kopieren Sie auf der Adobe I/O-Registerkarte die JWT-Payload (der Code zwischen den Klammern).
1. Fügen Sie ihn auf der AEM-Registerkarte in das Feld **Payload** ein.
1. Klicken Sie auf **Erstellen**, um die IMS-Konfiguration in AEM zu erstellen.

### Schritt 5a: Erstellen einer Eigenschaft in Adobe Experience Platform Launch {#create-property}

Eine Eigenschaft definiert Funktionen, die von Experience Platform Launch in Ihre Site eingefügt werden können.

1. Rufen Sie Adobe Experience Platform Launch unter `https://launch.adobe.com` auf.
1. Melden Sie sich mit Ihrer Adobe ID an.
1. Klicken Sie auf **Neue Eigenschaft**.
1. Geben Sie einen Namen ein, z. B. **Launch-AEM-Datenschicht**.
1. Geben Sie Ihre Domäne ein.
1. Klicken Sie auf **Speichern**.

### Schritt 5b: Erstellen einer Regel in Experience Platform Launch {#launch-rule}

Über die von Ihnen erstellte Eigenschaft können Sie eine Regel definieren, die festlegt, was beim Eintreten einer bestimmten Aktion geschehen soll.

1. Klicken Sie auf die in [Schritt 5a](#create-property) neu hinzugefügte Eigenschaft **Launch-AEM-Datenschicht**.
1. Wählen Sie die Registerkarte **Regeln** und klicken Sie auf **Neue Regel erstellen**.
1. Geben Sie einen Namen ein, z. B. **Bild-Klick**.
1. Klicken Sie auf die **+**-Schaltfläche unterhalb von **Ereignisse**.
1. Wählen Sie **Core** als **Erweiterung** sowie **Klick** als **Ereignistyp** aus und geben Sie **.cmp-image** als **CSS-Auswahl** ein.
1. Klicken Sie auf **Änderungen beibehalten**.
1. Klicken Sie auf die **+**-Schaltfläche unterhalb von **Aktionen**.
1. Wählen Sie **Core** als **Erweiterung** sowie **Benutzerspezifischer Code** als **Aktionstyp** und klicken Sie auf **Editor öffnen**.
1. Geben Sie im Editor folgenden Code ein: `console.log("DOM click event tracked by Launch for image: ", event.target.src);`
1. Klicken Sie auf **Speichern**.
1. Klicken Sie auf **Änderungen beibehalten**.
1. Klicken Sie auf **Speichern**, um die neue Regel zu erstellen.

### Schritt 6: Veröffentlichen der Launch-Regel {#publish-rule}

Um die neue Regel für Ihre AEM-Site verfügbar zu machen, müssen Sie sie veröffentlichen.

1. Wählen Sie auf der Registerkarte **Adobe Experience Platform Launch** die Registerkarte **Publishing**.
1. Klicken Sie auf **Neue Bibliothek hinzufügen**.
1. Geben Sie einen geeigneten **Namen** ein, z. B. **demo-1**.
1. Wählen Sie für die **Umgebung** die gewünschte Option aus, z. B. **Entwicklung (Entwicklung)**.
1. Klicken Sie auf **Ressource hinzufügen**.
1. Wählen Sie **Regeln > Bild-Klick > Neueste** und klicken Sie auf **Auswählen und neue Revision erstellen**.
1. Klicken Sie auf **Speichern und für Entwicklung erstellen**.
1. Klicken Sie im Popup-Fenster auf **Aktualisierungen anwenden und fortfahren**.
1. Klicken Sie im Anschluss an die Erstellung der Bibliothek auf das Auslassungssymbol (...) und wählen Sie **Zur Genehmigung übermitteln**.
1. Klicken Sie im Popup-Fenster auf **Senden**.
1. Klicken Sie auf das Auslassungssymbol (...) und wählen Sie **Für Staging erstellen**.
1. Klicken Sie im Anschluss an die Erstellung auf das Auslassungssymbol (...) und wählen Sie **Für Publishing genehmigen**.
1. Klicken Sie im Popup-Fenster auf **Genehmigen**.
1. Klicken Sie auf das Auslassungssymbol (...) und wählen Sie **Erstellen und in Produktion veröffentlichen**.
1. Klicken Sie im Popup-Fenster auf **Veröffentlichen**.

### Schritt 7: Aktivieren der Cloud-Konfigurationen für Ihre Site {#enable-configurations}

Damit Sie die Integration verwenden können, muss sie in AEM als Cloud-Konfiguration zugewiesen werden.

1. Klicken Sie in der AEM-Konsole auf **Tools > Allgemein > Konfigurationsbrowser**.
1. Markieren Sie **Beispiele von Kernkomponenten** und klicken Sie auf **Eigenschaften**.
1. Markieren Sie **Cloud-Konfigurationen** und klicken Sie auf **Speichern und schließen**.

### Schritt 8: Erstellen einer Integration zwischen Experience Platform Launch und Ihrer Site in AEM {#create-launch-integration}

Damit AEM mit Adobe Experience Platform Launch zusammenarbeiten kann, ist eine Experience Platform Launch-Integration erforderlich.

1. Klicken Sie in der AEM-Konsole auf **Tools > Cloud Services > Adobe Experience Platform Launch-Konfigurationen**.
1. Wählen Sie **Beispiele von Kernkomponenten** und klicken Sie auf **Erstellen**.
1. Geben Sie einen **Titel** ein, z. B. **Lauch-Konfiguration**.
1. Wählen Sie die IMS-Konfiguration aus, die Sie in [Schritt 4](#finish-ims) erstellt haben.
1. Wählen Sie das passende **Unternehmen** aus.
1. Wählen Sie als **Eigenschaft** die neu hinzugefügte Experience Platform Launch-Eigenschaft aus, die Sie in [Schritt 5](#create-property) erstellt haben.
1. Verschieben Sie den Regler **Produktionscode bei Autor mit angeben** nach rechts und klicken Sie auf **Weiter**.
1. Klicken Sie auf **Weiter**.
1. Klicken Sie auf **Weiter**.
1. Klicken Sie auf **Erstellen**.

### Schritt 9: Verbinden Ihrer AEM-Site mit der Experience Platform Launch-Integration {#connect-aem}

Damit Sie die Experience Platform Launch-Integration verwenden können, muss sie als Cloud-Konfiguration zugewiesen werden.

1. Klicken Sie in der AEM-Konsole auf **Sites** und markieren Sie die Site **Kernkomponenten**.
1. Klicken Sie auf **Eigenschaften**.
1. Wählen Sie die Registerkarte **Erweitert**.
1. Wählen Sie für **Cloud-Konfiguration** die Option **Beispiele von Kernkomponenten** und klicken Sie auf **Auswählen**.
1. Klicken Sie auf **Speichern und schließen**.

### Schritt 10: Überprüfen, ob die Experience Platform Launch-Logik auf die Seite angewendet wird {#verify-launch}

Testen Sie, ob die bisherigen Schritte erfolgreich abgeschlossen wurden.

1. Öffnen Sie die Image-Seite der Kernkomponentenbibliothek im Vorschaumodus: `http://<lhost&gt;:<port&gt;/editor.html/content/core-components-examples/library/page-authoring/image.html`
1. Klicken Sie auf ein Bild und vergewissern Sie sich, dass in der Browser-Konsole die Meldung `A Core Image was clicked` angezeigt wird.

## Integration von AEM und Experience Platform Launch mit der Datenschicht{#data-layer-launch}

Nachdem die Integration zwischen AEM und Experience Platform Launch eingerichtet wurde, können Sie sie mit der Datenschicht integrieren.

### Schritt 1: Erstellen einer Regel in Adobe Experience Platform Launch {#create-rule}

Fügen Sie nach demselben Verfahren wie in [Schritt 5](#launch-rule) eine neue Regel in Adobe Experience Platform Launch hinzu, für die Sie folgende Werte verwenden.

* Name: `image-click-data-layer`
* EREIGNISSE:
   * Erweiterung: Core
   * Ereignistyp: DOM-bereit
* AKTIONEN:
   * Erweiterung: Core
   * Aktionstyp: Benutzerspezifischer Code
   * Code:

      ```
        function onImageClick(event) {
          console.log("Data layer click event tracked by Launch for image: " + event.info.path);
          console.log("dataLayer.getState(): ", adobeDataLayer.getState()); 
        }
        adobeDataLayer.addEventListener('image clicked', onImageClick);
      ```

### Schritt 2: Veröffentlichen der Experience Platform Launch-Regel, um sie für Ihre AEM-Site zur Verfügung verfügbar zu machen {#publish-rule-2}

Gehen Sie nach dem gleichen Verfahren wie in [Schritt 6](#publish-rule) vor, um die neue Regel zu veröffentlichen.

### Schritt 3: Überprüfen, ob die Experience Platform Launch-Logik auf die Seite angewendet wird {#verify}

1. Öffnen Sie die Image-Seite der Kernkomponentenbibliothek im Vorschaumodus: `http://<host&gt;:<port&gt;/editor.html/content/core-components-examples/library/page-authoring/image.html`
1. Klicken Sie auf ein Bild und vergewissern Sie sich, dass in der Browser-Konsole folgende Meldung angezeigt wird:

   ![Ausgabe der Datenschicht-Konsole](/help/assets/data-layer-console-output.png)
