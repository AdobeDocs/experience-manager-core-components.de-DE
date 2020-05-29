---
title: Verwenden der Adobe Client-Datenschicht zur Integration der Kernkomponenten und des Adobe Launch
description: Konfigurieren von Adobe Launch zur Registrierung von Core Component-Ereignissen mit Adobe Launch
translation-type: tm+mt
source-git-commit: f930a0d6004a29369b189137dd9c52e637ea3a61
workflow-type: tm+mt
source-wordcount: '1160'
ht-degree: 2%

---


# Verwenden der Adobe Client-Datenschicht zur Integration der Kernkomponenten und des Adobe Launch {#launch-integration}

Die Hauptkomponenten können mithilfe der Adobe Client-Datenschicht in Adobe Launch integriert werden. In diesem Dokument wird die Konfiguration von Adobe Launch zur Verfolgung von Klickkomponenten als Beispiel beschrieben.

Nach der Konfiguration erzeugt Launch die folgende Ausgabe in der Browser-Konsole, wenn auf eine Core Image-Komponente geklickt wird.

![Ausgabedokument](/help/assets/launch-console-output.png)

## Integration mit AEM starten {#launch-aem}

Der erste Adobe Launch muss in Ihre AEM-Site integriert werden.

### Schritt 1: Erstellen einer Integration in Adobe I/O {#create-io-integration}

Melden Sie sich zuerst bei der Adobe-E/A-Datei an, um Beginn zu kontaktieren, der eine Integration konfiguriert.

1. Wechseln zu `https://console.adobe.io`.
1. Melden Sie sich mit Ihrer Adobe ID an.
1. Klicken Sie im Abschnitt Quick Beginn auf Integration **erstellen**.
1. Select **Access an API** and click **Continue**.
1. Wählen Sie **Experience Platform Launch API** unter Adobe Experience Platform und klicken Sie auf **Weiter**.

### Schritt 2: Erstellen einer IMS-Konfiguration in AEM {#ims-configuration}

In AEM müssen Sie die Integration definieren, die Sie mit der Konfiguration in Adobe I/O begonnen haben.

1. Wechseln Sie zur AEM-Startseite und klicken Sie auf **Tools -> Sicherheit -> Adobe IMS-Konfigurationen**.
1. Klicken Sie auf **Erstellen**.
1. Als **Cloud-Lösung** wählen Sie **Adobe Launch**.
1. Klicken Sie auf Neues Zertifikat **erstellen**.
1. Geben Sie einen Alias für das Zertifikat ein, z. B. **aem-launch-certificate**.
1. Klicken Sie auf **Zertifikat** erstellen und dann im Popup auf **OK** , um das Zertifikat zu erstellen.
1. Klicken Sie auf Öffentlichen Schlüssel **herunterladen** und klicken Sie im Popup auf **Herunterladen**.

### Schritt 3: Schließen der Adobe-E/A-Konfiguration {#finish-io}

Mit dem in der AEM IMS-Konfiguration erstellten Zertifikat und Schlüssel können Sie Ihre Adobe-E/A-Konfiguration abschließen.

1. Gehen Sie wie in [Schritt 1 zur Adobe-Konsole zurück.](#create-io-integration)
1. Geben Sie im Fenster &quot;Neue Integration **** erstellen&quot;einen Namen und eine Beschreibung ein, z. B. die **AEM Launch-Datenschicht**.
1. Laden Sie unter &quot;Zertifikate **mit**&#x200B;öffentlichen Schlüsseln&quot;das Zertifikat hoch, das Sie in [Schritt 2 erstellt haben.](#ims-configuration)
1. Wählen Sie das Profil **Start - Test**.
1. Klicken Sie auf **Integration erstellen**.
1. Klicken Sie auf **Weiter zu den Integrationsdetails**. Sie benötigen diese Details später, um die IMS-Konfiguration in Ihrer AEM-Instanz abzuschließen.

### Schritt 4: IMS-Konfiguration beenden {#finish-ims}

Mit den Adobe I/O-Integrationsdetails können Sie die AEM IMS-Konfiguration abschließen.

1. Klicken Sie auf der Registerkarte AEM in der Registerkarte **Adobe IMS Technical Account Configuration** von [Schritt 2 auf](#ims-configuration) Next ****.
1. Geben Sie einen Titel wie **IMS-Konfiguration für Adobe Launch** ein.
1. Kopieren Sie auf der Registerkarte &quot;Adobe-E/A&quot;den **API-Schlüssel (Client-ID)**.
1. Fügen Sie auf der Registerkarte &quot;AEM&quot;den zuvor kopierten Schlüssel in das Feld &quot; **API-Schlüssel&quot;ein**.
1. Klicken Sie in der Adobe-E/A-Datei auf **Clientgeheimnis abrufen** und kopieren Sie es.
1. Fügen Sie es auf der Registerkarte &quot;AEM&quot;in das Feld &quot; **Clientgeheimnis&quot;ein** .
1. Wählen Sie auf der Registerkarte &quot;Adobe-E/A&quot;die Registerkarte &quot; **JWT** &quot;und kopieren Sie die URL, z. B. `https://ims-na1.adobelogin.com`.
1. Fügen Sie auf der Registerkarte &quot;AEM&quot;die URL in das Feld &quot; **Autorisierungsserver** &quot;ein.
1. Kopieren Sie auf der Registerkarte &quot;Adobe-E/A&quot;die JWT-Nutzlast (den Code zwischen den Klammern).
1. Fügen Sie es auf der Registerkarte &quot;AEM&quot;in das Feld &quot; **Payload** &quot;ein.
1. Klicken Sie auf **Erstellen** , um die IMS-Konfiguration in AEM zu erstellen.

### Schritt 5a: Erstellen einer Eigenschaft in Adobe Launch {#create-property}

Eine Eigenschaft definiert Funktionen, die von Launch auf Ihre Site übertragen werden können.

1. Gehen Sie zu Adobe Launch `https://launch.adobe.com`.
1. Melden Sie sich mit Ihrer Adobe ID an.
1. Click **New Property**.
1. Geben Sie einen Namen ein, z. B. AEM-Datenschicht **starten**.
1. Geben Sie Ihre Domäne ein.
1. Klicken Sie auf **Speichern**.

### Schritt 5b - Regel beim Start erstellen {#launch-rule}

Mithilfe der von Ihnen erstellten Eigenschaft können Sie eine Regel definieren, die angibt, was bei einer Aktion geschehen soll.

1. Klicken Sie in [Schritt 5](#create-property) AEM-Datenschicht **starten auf die neu hinzugefügte Eigenschaft**.
1. Wählen Sie die Registerkarte **Regeln** und klicken Sie auf Neue Regel **erstellen**.
1. Geben Sie einen Namen ein, z. B. **image-click**.
1. Klicken Sie auf die **+** -Schaltfläche unter den **Ereignissen**.
1. Wählen Sie **Core** als **Extension**, **klicken Sie auf** als **Ereignistyp** und geben Sie **.cmp-image** **** alsCSS-Selektor ein.
1. Klicken Sie auf Änderungen **beibehalten**.
1. Klicken Sie auf die **+** -Schaltfläche unter **Aktionen**.
1. Wählen Sie **Core** als **Erweiterung**, **Benutzerdefinierter Code** als **Aktionstyp** und klicken Sie auf Editor **öffnen**.
1. Geben Sie im Editor den folgenden Code ein: `console.log("DOM click event tracked by Launch for image: ", event.target.src);`
1. Klicken Sie auf **Speichern**.
1. Klicken Sie auf Änderungen **beibehalten**.
1. Klicken Sie auf **Speichern** , um die neue Regel zu erstellen.

### Schritt 6: Veröffentlichen der Startregel {#publish-rule}

Um die neue Regel für Ihre AEM-Site verfügbar zu machen, müssen Sie sie veröffentlichen.

1. Wählen Sie auf der Registerkarte **Adobe Launch** die Registerkarte **Publishing** .
1. Click **Add New Library**.
1. Geben Sie einen **Namen** ein, z. B. **demo-1**.
1. Wählen Sie für die **Umgebung** die gewünschten Optionen aus, z. B. **Entwicklung (Entwicklung)**.
1. Klicken Sie auf **Hinzufügen Ressource**.
1. Wählen Sie **Regeln -> Bild-Klick -> Neueste** und klicken Sie auf **Auswählen und Erstellen einer neuen Revision**.
1. Klicken Sie auf **Speichern und Build zur Entwicklung erstellen**.
1. Klicken Sie im Popup auf Updates **anwenden und fortfahren**.
1. Wenn die Bibliothek erstellt wurde, klicken Sie auf das Auslassungssymbol und wählen Sie &quot; **Zur Genehmigung**&#x200B;übermitteln&quot;.
1. Klicken Sie im Popup auf **Senden**.
1. Klicken Sie auf das Auslassungssymbol und wählen Sie &quot; **Für Staging** erstellen&quot;.
1. Wenn der Build abgeschlossen ist, klicken Sie auf das Auslassungssymbol und wählen Sie &quot; **Zur Veröffentlichung** genehmigen&quot;.
1. Klicken Sie im Popup auf **Genehmigen**.
1. Klicken Sie auf das Auslassungszeichen und wählen Sie &quot; **Erstellen und Veröffentlichen in Produktion**&quot;.
1. Klicken Sie im Popup auf **Veröffentlichen**.

### Schritt 7: Aktivieren der Cloud-Konfigurationen für Ihre Site {#enable-configurations}

Zur Verwendung der Integration muss sie in AEM als Cloud-Konfiguration zugewiesen werden.

1. Klicken Sie in der AEM-Konsole auf **Tools -> Allgemein -> Konfigurationsbrowser**.
1. Überprüfen Sie die Beispiele für **Kernkomponenten** und klicken Sie auf **Eigenschaften**.
1. Überprüfen Sie die **Cloud-Konfigurationen** und klicken Sie auf **Speichern &amp; Schließen**.

### Schritt 8: Erstellen einer Startintegration mit Ihrer Site in AEM {#create-launch-integration}

Eine Startintegration ist erforderlich, damit AEM mit Launch funktioniert

1. Klicken Sie in der AEM-Konsole auf **Werkzeuge -> Cloud-Dienste -> Adobe Launch-Konfigurationen**.
1. Wählen Sie Beispiele für **Hauptkomponenten** und klicken Sie auf **Erstellen**.
1. Geben Sie einen **Titel** ein, z. B. **Startkonfiguration**.
1. Wählen Sie die in [Schritt 4 erstellte IMS-Konfiguration aus.](#finish-ims)
1. Wählen Sie nach Bedarf die **Firma** aus.
1. Wählen Sie als **Eigenschaft** die neu hinzugefügte Eigenschaft &quot;Start&quot;aus, die in [Schritt 5 erstellt wurde.](#create-property)
1. Verschieben Sie den Regler **Produktionscode beim Autor** einschließen nach rechts und klicken Sie auf **Weiter**.
1. Klicken Sie auf **Weiter**.
1. Klicken Sie auf **Weiter**.
1. Klicken Sie auf **Erstellen**.

### Schritt 9: Verbinden Ihrer AEM-Site mit der Integration von Launch {#connect-aem}

Damit AEM die Startintegration verwenden kann, muss sie als Cloud-Konfiguration zugewiesen werden.

1. Klicken Sie in der AEM-Konsole auf **Sites** und überprüfen Sie die Site &quot; **Core-** Komponenten&quot;.
1. Klicken Sie auf **Eigenschaften**.
1. Select the **Advanced** tab.
1. Wählen Sie als **Cloud-Konfiguration** die **Hauptkomponenten-Beispiele** und klicken Sie auf **Auswählen**.
1. Klicken Sie auf **Speichern und schließen**.

### Schritt 10 - Überprüfen Sie, ob die Launch-Logik auf die Seite angewendet wird {#verify-launch}

Testen Sie, ob die bisherigen Schritte erfolgreich waren.

1. Öffnen Sie die Image-Seite der Core-Komponentenbibliothek im Vorschau-Modus: `http://<lhost&gt;:<port&gt;/editor.html/content/core-components-examples/library/page-authoring/image.html`
1. Klicken Sie auf ein Bild und vergewissern Sie sich, dass die Nachricht in der Browser-Konsole angezeigt `A Core Image was clicked` wird.

## Integration mit AEM und der Datenschicht starten {#data-layer-launch}

Nachdem die Integration zwischen AEM und Launch eingerichtet wurde, können wir sie in die Datenschicht integrieren.

### Schritt 1: Erstellen einer Regel in Adobe Launch {#create-rule}

Wiederholen Sie die Schritte in [Schritt 5](#launch-rule) , um eine neue Regel in Adobe Launch mit den folgenden Werten hinzuzufügen.

* Name: `image-click-data-layer`
* EREIGNISSE:
   * Erweiterung: Core
   * Ereignistyp: DOM-bereit
* AKTIONEN:
   * Erweiterung: Core
   * Aktionstyp: Benutzerdefinierter Code
   * Code:

      ```
        function onImageClick(event) {
          console.log("Data layer click event tracked by Launch for image: " + event.info.path);
          console.log("dataLayer.getState(): ", adobeDataLayer.getState()); 
        }
        adobeDataLayer.addEventListener('image clicked', onImageClick);
      ```

### Schritt 2: Veröffentlichen Sie die Startregel, um sie Ihrer AEM-Site zur Verfügung zu stellen. {#publish-rule-2}

Wiederholen Sie die Schritte in [Schritt 6](#publish-rule) , um die neue Regel zu veröffentlichen.

### Schritt 3 - Überprüfen Sie, ob die Launch-Logik auf die Seite angewendet wird {#verify}

1. Öffnen Sie die Image-Seite der Core-Komponentenbibliothek im Vorschau-Modus: `http://<host&gt;:<port&gt;/editor.html/content/core-components-examples/library/page-authoring/image.html`
1. Klicken Sie auf ein Bild und vergewissern Sie sich, dass die folgende Meldung in der Browser-Konsole angezeigt wird:

   ![Ausgabe der Datenschichtkonsole](/help/assets/data-layer-console-output.png)
