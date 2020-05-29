---
title: Verwenden der Adobe Client-Datenschicht zur Integration von Kernkomponenten und Adobe Analytics
description: Konfiguration von Adobe Analytics zur Registrierung von Core Component-Ereignissen
translation-type: tm+mt
source-git-commit: f930a0d6004a29369b189137dd9c52e637ea3a61
workflow-type: tm+mt
source-wordcount: '1000'
ht-degree: 3%

---


# Verwenden der Adobe Client-Datenschicht zur Integration von Kernkomponenten und Adobe Analytics {#analytics-integration}

In diesem Dokument wird beschrieben, wie Sie eine End-to-End-Konfiguration auf Basis von AEM, der Adobe Client Data Layer, Adobe Launch und Adobe Analytics einrichten, um Folgendes zu verfolgen:

* Die in der Adobe Client-Datenschicht gespeicherte Seiten-ID, wenn eine Seite geladen wird
* Der in der Adobe Client-Datenschicht gespeicherte Bildpfad, wenn auf ein Bild geklickt wird

Hier werden die Kernkomponenten als Beispiel verwendet, können aber auch für Ihre eigenen benutzerdefinierten Komponenten verwendet werden.

##  Schritt 1: Report Suite in Adobe Analytics erstellen {#create-report-suite}

Zur Aggregat- und Analyse Ihrer Daten muss zunächst eine Report Suite erstellt werden.

1. Wechseln zu `https://analytics.adobe.com`.
1. Melden Sie sich mit Ihrer Adobe ID an.
1. Click the **Analytics** icon.
1. Gehen Sie zu **Admin -> Report Suites**.
1. Click **Create New -> Report Suite**.
1. Füllen Sie das Formular aus:
   1. **Berichtssuite-ID**: `yourSuiteID`
   1. **Site-Titel**: `Your suite description`
   1. **Zeitzone**: Gegebenenfalls
   1. **Aufschaltdatum**: dem heutigen Datum oder gegebenenfalls
   1. **Geschätzte Ansichten pro Tag**: 100 oder gegebenenfalls
1. Click **Create Report Suite**.

Bei erfolgreichem Abschluss erhalten Sie folgende grüne Nachricht: `Report Suite <yourReportSuite> has been successfully created.`

## Schritt 2: Report Suite sichtbar machen {#make-visible}

Um die neue Report Suite verwenden zu können, muss sie sichtbar sein.

1. Wechseln zu `https://adminconsole.adobe.com`.
1. Melden Sie sich mit Ihrer Adobe ID an.
1. Klicken Sie auf die **Karte Adobe Analytics - &lt;IhreSite>**
1. Klicken Sie auf den Link **Adobe Analytics - &lt;Ihre Site>**
1. Select the **Permissions** tab
1. Klicken Sie auf die Schaltfläche **Bearbeiten** in der Zeile **Report Suites**
1. Klicken Sie auf die **+** -Schaltfläche der Report Suite, die Sie in [Schritt 1](#create-report-suite) erstellt haben, um sie der Kategorie **Einbezogene Berechtigungselemente** hinzuzufügen.
1. Klicken Sie auf **Speichern**.

## Schritt 3: Integration Ihrer AEM-Site mit Adobe Launch {#integrate-launch}

Start muss in Ihre AEM-Site integriert sein, um Daten zu generieren.

Führen Sie die Schritte im Dokument [Verwenden der Adobe Client-Datenschicht zum Integrieren von Kernkomponenten und Adobe Launch](launch-integration.md) aus.

## Schritt 4: Installieren und Konfigurieren der Adobe Analytics Extension in Adobe Launch {#install-extension}

Die Adobe Analytics-Erweiterung ermöglicht die Integration von Analytics in Launch.

1. Wählen Sie in Adobe Launch die neu hinzugefügte Eigenschaft aus, die Sie in [Schritt 3 erstellt haben.](#integrate-launch)
1. Navigieren Sie zur Registerkarte &quot; **Erweiterungen** &quot;und wählen Sie &quot; **Katalog**&quot;aus.
1. Suchen Sie nach **Adobe Analytics**.
1. Klicken Sie auf **Installieren**.
1. Konfigurieren Sie die Erweiterung.
   1. Geben Sie die **Analytics Report Suite-ID** ein, die in [Schritt 1](#create-report-suite) für die entsprechenden Umgebung erstellt wurde
   1. Zeichensatz **auf** UTF-8 festlegen
1. Klicken Sie auf Speichern

## Schritt 5: Erstellen eines Datenelements in Adobe Launch für die Seiten-ID {#create-data-element}

Für die Verfolgung der Seiten-ID ist in Launch ein Datenelement erforderlich.

1. Wählen Sie in Adobe Launch die in [Schritt 3 erstellte Eigenschaft aus.](#integrate-launch)
1. Wählen Sie die Registerkarte **Datenelemente** und klicken Sie auf **Hinzufügen Datenelement**:
   1. **Name**: `dl-page-id`
   1. **Erweiterung**: **Core**
   1. **Datenelementtyp**: **Benutzerdefinierter Code**
1. Klicken Sie auf Editor **öffnen**
1. Geben Sie im Editor den Code ein: `return adobeDataLayer.getState().page.id;`
1. Klicken Sie auf **Speichern**.
1. Klicken Sie auf **Speichern** , um das Datenelement zu erstellen.

## Schritt 6: Erstellen einer Regel in Adobe Launch zur Verfolgung der Seiten-ID in Analytics {#track-page}

Regeln ermöglichen die Verfolgung von Browsing-Attributen wie Seiten-ID in Analytics.

Wiederholen Sie die Schritte in Teil 5b des Dokuments [Verwenden der Adobe Client-Datenschicht zur Integration von Kernkomponenten und Adobe Launch](launch-integration.md#launch-rule) , um folgende Regel in Adobe Launch hinzuzufügen:

* **Name**: `track-dl-page-id`
* EREIGNISSE:
   * **Erweiterung**: **Core**
   * **Ereignistyp**: **Seitenende**
* AKTION 1:
   * **Erweiterung**: **Adobe Analytics**
   * **Aktionstyp**: **Variablen festlegen**
   * **prop1**: `%dl-page-id%`
* AKTION 2:
   * **Erweiterung**: **Adobe Analytics**
   * **Aktionstyp**: **Beacon senden**
   * Überprüfen Sie **s.t(): Daten an Adobe Analytics senden und als Ansicht behandeln**

## Schritt 7: Erstellen einer Regel in Adobe Launch, um das Image Click-Ereignis zu registrieren {#register-click}

Regeln ermöglichen die Verfolgung von Browsing-Attributen wie Klick-Ereignis in Analytics.

Wiederholen Sie die Schritte in Teil 5b des Dokuments [Verwenden der Adobe Client-Datenschicht zur Integration von Kernkomponenten und Adobe Launch](launch-integration.md#launch-rule) , um folgende Regel in Adobe Launch hinzuzufügen:

* **Name**: `register-dl-image-click`
* EREIGNISSE:
   * **Erweiterung**: **Core**
   * **Ereignistyp**: **Seitenende**
* AKTION 1:
   * **Erweiterung**: **Core**
   * **Aktionstyp**: **Benutzerdefinierter Code**
   * Editor: Geben Sie folgenden Code ein

      ```
      var myListener = function(event) {
        _satellite.track('dlImageClicked', event.info.path);
      };
      adobeDataLayer.addEventListener('image clicked', myListener());
      ```

## Schritt 8: Erstellen einer Regel in Adobe Launch zur Verfolgung des Image Click-Ereignisses in Analytics {#track-click}

Regeln ermöglichen die Verfolgung von Browsing-Attributen wie Klick-Ereignis in Analytics.

Wiederholen Sie die Schritte in Teil 5b des Dokuments [Verwenden der Adobe Client-Datenschicht zur Integration von Kernkomponenten und Adobe Launch](launch-integration.md#launch-rule) , um folgende Regel in Adobe Launch hinzuzufügen:

* **Name**: `track-dl-image-click`
* EREIGNISSE:
   * **Erweiterung**: **Core**
   * **Ereignistyp**: **Direktaufruf**
   * **Bezeichner**: `dlImageClicked`
* AKTION 1:
   * **Erweiterung**: **Adobe Analytics**
   * **Aktionstyp**: **Variablen festlegen**
   * **prop2**: Als `%event.detail%`
* AKTION 2:
   * **Erweiterung**: **Adobe Analytics**
   * **Aktionstyp**: **Beacon senden**
   * Überprüfen Sie **s.t(): Daten an Adobe Analytics senden und als Ansicht behandeln**

## Schritt 9: Veröffentlichen des Startcodes auf Ihrer Website {#publish-launch}

Um die Verfolgung dieser Regeln und Eigenschaften beim Start zu aktivieren, muss der Code veröffentlicht werden.

1. Wählen Sie auf der Registerkarte **Adobe Launch** die Registerkarte **Publishing** .
1. Click **Add New Library**.
1. As **Name** enter: `data-layer-analytics-1`.
1. Als **Umgebung** wählen Sie **Entwicklung (Entwicklung)**.
1. Klicken Sie auf **Hinzufügen Alle geänderten Ressourcen**.
1. Für jede der drei Regeln (`track-dl-page-id`, `register-dl-image-click` und `track-dl-image-click`):
1. Wählen Sie **Regeln -> Regel -> Neueste** und klicken Sie auf **Auswählen und Erstellen einer neuen Revision**.
1. Klicken Sie auf **Speichern und Build zur Entwicklung erstellen**.

## Schritt 10 - Auslösen Ihrer Seite zum Senden von Informationen an Adobe Analytics {#trigger-page}

In diesem Schritt installieren Sie die Chrome Extension **Launch und DTM Switch**. Mit dieser Erweiterung müssen Sie nur den Startcode für die Development-Umgebung erstellen und bereitstellen. Die Staging- und Production-Umgebung müssen nicht bereitgestellt werden.

1. Installieren Sie die Chrome Extension **Launch und DTM Switch** von Discovery.
1. Klicken Sie auf das Symbol zum **Starten des Switches** und legen Sie die Option Debuggen auf *EIN* fest.
1. Seite neu laden `http://<host>:<port>/content/core-components-examples/library/image.html`.
1. Öffnen Sie die Browser-Konsole, und Sie sollten Folgendes sehen.

![Analytics-Konsolenausgabe](/help/assets/analytics-console-output.png)

>[!TIP]
>
>Sie können auch die **Experience Cloud-Debugger** -Erweiterung für Chrome installieren, um Adobe Launch- und Analytics-spezifische Informationen zur Seite Ansicht.

## Schritt 11: Ansicht der verfolgten Informationen in Adobe Analytics {#view-info}

Jetzt können Sie die Ereignis, die Sie in Adobe Analytics ausgelöst haben, Ansicht werden.

1. Wechseln zu `https://analytics.adobe.com`.
1. Melden Sie sich mit Ihrer Adobe ID an.
1. Click the **Analytics** icon.
1. Select the **Reports** tab.
1. Wählen Sie in der Dropdown-Liste oben rechts die Report Suite aus, die Sie in [Schritt 1 erstellt haben.](#create-report-suite)
1. Wählen Sie in der ersten Spalte **Benutzerspezifischer Traffic -> Benutzerspezifischer Traffic 1-10 -> Custom Insight 1** aus, um die in der Datenschicht gespeicherten verfolgten Seiten-IDs (Pfade) Ansicht. Es sollte wie folgt aussehen:

   ![Custom Insight 1](/help/assets/custom-insight-1.png)

1. Greifen Sie auf **Custom Insight 2** zu, um die verfolgten Bildpfade in der Datenschicht Ansicht. Es sollte wie folgt aussehen:

   ![Custom Insight 2](/help/assets/custom-insight-2.png)
