---
title: Integration von Kernkomponenten und Adobe Analytics über die Adobe Client-Datenschicht
description: Konfigurieren von Adobe Analytics für die Registrierung von Kernkomponenten-Ereignissen
translation-type: ht
source-git-commit: f930a0d6004a29369b189137dd9c52e637ea3a61
workflow-type: ht
source-wordcount: '1000'
ht-degree: 100%

---


# Integration von Kernkomponenten und Adobe Analytics über die Adobe Client-Datenschicht{#analytics-integration}

In diesem Dokument wird beschrieben, wie Sie auf Basis von AEM, der Adobe Client-Datenschicht, Adobe Experience Platform Launch und Adobe Analytics eine End-to-End-Konfiguration für das Tracking von Folgendem einrichten:

* der beim Laden einer Seite auf der Adobe Client-Datenschicht gespeicherten Seiten-ID
* des beim Klicken auf ein Bild auf der Adobe Client-Datenschicht gespeicherten Bildpfades

Hier werden als Beispiel die Kernkomponenten verwendet, Sie können aber auch Ihre eigenen benutzerdefinierten Komponenten verwenden.

## Schritt 1: Erstellen einer Report Suite in Adobe Analytics{#create-report-suite}

Sie müssen eine Report Suite erstellen, um Ihre Daten aggregieren und analysieren zu können.

1. Rufen Sie `https://analytics.adobe.com` auf.
1. Melden Sie sich mit Ihrer Adobe ID an.
1. Klicken Sie auf das **Analytics**-Symbol.
1. Navigieren sie zu **Admin > Report Suites**.
1. Klicken Sie auf **Neu erstellen > Report Suite**.
1. Füllen Sie das Formular aus:
   1. **Report Suite-ID**: `yourSuiteID`
   1. **Site-Titel**: `Your suite description`
   1. **Zeitzone**: wie gewünscht
   1. **Aufschaltdatum**: das aktuelle Datum oder wie gewünscht
   1. **Geschätzte Seitenansichten pro Tag**: 100 oder wie gewünscht
1. Klicken Sie auf **Report Suite erstellen**.

Nach erfolgreicher Fertigstellung erhalten Sie folgende Meldung in grüner Schriftfarbe: `Report Suite <yourReportSuite> has been successfully created.`

## Schritt 2: Einsehbarmachen der Report Suite{#make-visible}

Damit Sie die neue Report Suite verwenden können, muss sie einsehbar sein.

1. Rufen Sie `https://adminconsole.adobe.com` auf.
1. Melden Sie sich mit Ihrer Adobe ID an.
1. Klicken Sie auf die Karte **Adobe Analytics - &lt;IhreSite>**.
1. Klicken Sie auf den Link **Adobe Analytics - &lt;IhreSite>**.
1. Wählen Sie die Registerkarte **Berechtigungen** aus.
1. Klicken Sie auf die Schaltfläche **Bearbeiten** in der Zeile **Report Suites**.
1. Klicken Sie auf die **+**-Schaltfläche der Report Suite, die Sie in [Schritt 1](#create-report-suite) erstellt haben, um sie der Kategorie **Einbezogene Berechtigungselemente** hinzuzufügen.
1. Klicken Sie auf **Speichern**.

## Schritt 3: Integrieren Ihrer AEM-Site mit Adobe Experience Platform Launch {#integrate-launch}

Experience Platform Launch muss mit Ihrer AEM-Site integriert sein, um Daten generieren zu können.

Führen Sie die Schritte im Dokument [Integration von Kernkomponenten und Adobe Experience Platform Launch über die Adobe Client-Datenschicht](launch-integration.md) aus.

## Schritt 4: Installieren und Konfigurieren der Adobe Analytics-Erweiterung in Adobe Experience Platform Launch {#install-extension}

Die Adobe Analytics-Erweiterung ermöglicht die Integration von Analytics mit Experience Platform Launch .

1. Wählen Sie in Adobe Experience Platform Launch die neu hinzugefügte Eigenschaft aus, die Sie in [Schritt 3](#integrate-launch) erstellt haben.
1. Navigieren Sie zur Registerkarte **Erweiterungen** und wählen Sie **Katalog** aus.
1. Suchen Sie nach **Adobe Analytics**.
1. Klicken Sie auf **Installieren**.
1. Konfigurieren Sie die Erweiterung.
   1. Geben Sie die **Analytics Report Suite-ID** ein, die in [Schritt 1](#create-report-suite) für die entsprechenden Umgebungen erstellt wurde.
   1. Legen Sie für den **Zeichensatz** die Option „UTF-8“ fest.
1. Klicken Sie auf „Speichern“.

## Schritt 5: Erstellen eines Datenelements für die Seiten-ID in Adobe Experience Platform Launch {#create-data-element}

Experience Platform Launch benötigt für das Tracking der Seiten-ID ein Datenelement.

1. Wählen Sie in Adobe Experience Platform Launch die Eigenschaft aus, die Sie in [Schritt 3](#integrate-launch) erstellt haben.
1. Wählen Sie die Registerkarte **Datenelemente** und klicken Sie auf **Datenelement hinzufügen**:
   1. **Name**: `dl-page-id`
   1. **Erweiterung**: **Core**
   1. **Datenelement-Typ**: **Benutzerdefinierter Code**
1. Klicken Sie auf **Editor öffnen**.
1. Geben Sie im Editor folgenden Code ein: `return adobeDataLayer.getState().page.id;`
1. Klicken Sie auf **Speichern**.
1. Klicken Sie auf **Speichern**, um das Datenelement zu erstellen.

## Schritt 6: Erstellen einer Regel in Adobe Experience Platform Launch für das Tracking der Seiten-ID in Analytics {#track-page}

Regeln ermöglichen das Tracking von Browsing-Attributen wie der Seiten-ID in Analytics.

Wiederholen Sie die Schritte in Teil 5b des Dokuments [Integration von Kernkomponenten und Adobe Experience Platform Launch über die Adobe Client-Datenschicht](launch-integration.md#launch-rule), um in Adobe Experience Platform Launch folgende Regel hinzuzufügen:

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
   * Markieren Sie **s.t(): Daten an Adobe Analytics senden und als Seitenansicht behandeln**

## Schritt 7: Erstellen einer Regel in Adobe Experience Platform Launch für die Registrierung von Bild-Klick-Ereignissen in Analytics {#register-click}

Regeln ermöglichen es, in Analytics Browsing-Attribute wie etwa Klick-Ereignisse aufzuzeichnen.

Wiederholen Sie die Schritte in Teil 5b des Dokuments [Integration von Kernkomponenten und Adobe Experience Platform Launch über die Adobe Client-Datenschicht](launch-integration.md#launch-rule), um in Adobe Experience Platform Launch folgende Regel hinzuzufügen:

* **Name**: `register-dl-image-click`
* EREIGNISSE:
   * **Erweiterung**: **Core**
   * **Ereignistyp**: **Seitenende**
* AKTION 1:
   * **Erweiterung**: **Core**
   * **Aktionstyp**: **Benutzerspezifischer Code**
   * Editor: Geben Sie folgenden Code ein:

      ```
      var myListener = function(event) {
        _satellite.track('dlImageClicked', event.info.path);
      };
      adobeDataLayer.addEventListener('image clicked', myListener());
      ```

## Schritt 8: Erstellen einer Regel in Adobe Experience Platform Launch für das Tracking des Bild-Klick-Ereignisses in Analytics {#track-click}

Regeln ermöglichen es, in Analytics Browsing-Attribute wie etwa Klick-Ereignisse aufzuzeichnen.

Wiederholen Sie die Schritte in Teil 5b des Dokuments [Integration von Kernkomponenten und Adobe Experience Platform Launch über die Adobe Client-Datenschicht](launch-integration.md#launch-rule), um in Adobe Experience Platform Launch folgende Regel hinzuzufügen:

* **Name**: `track-dl-image-click`
* EREIGNISSE:
   * **Erweiterung**: **Core**
   * **Ereignistyp**: **Direktaufruf**
   * **Bezeichner**: `dlImageClicked`
* AKTION 1:
   * **Erweiterung**: **Adobe Analytics**
   * **Aktionstyp**: **Variablen festlegen**
   * **prop2**: Legen Sie hierfür `%event.detail%` fest.
* AKTION 2:
   * **Erweiterung**: **Adobe Analytics**
   * **Aktionstyp**: **Beacon senden**
   * Markieren Sie **s.t(): Daten an Adobe Analytics senden und als Seitenansicht behandeln**

## Schritt 9: Veröffentlichen des Experience Platform Launch-Codes auf Ihrer Website {#publish-launch}

Um das Tracking dieser Regeln und Eigenschaften in Experience Platform Launch zu aktivieren, muss der Code veröffentlicht werden.

1. Wählen Sie auf der Registerkarte **Adobe Experience Platform Launch** die Registerkarte **Publishing**.
1. Klicken Sie auf **Neue Bibliothek hinzufügen**.
1. Geben Sie unter **Name** Folgendes ein: `data-layer-analytics-1`
1. Wählen Sie für die **Umgebung** die Option **Entwicklung (Entwicklung)** aus.
1. Klicken Sie auf **Alle geänderten Ressourcen**.
1. Für alle drei Regeln (`track-dl-page-id`, `register-dl-image-click` und `track-dl-image-click`) gilt:
1. Wählen Sie **Regeln > Regel > Neueste** und klicken Sie auf **Auswählen und neue Revision erstellen**.
1. Klicken Sie auf **Speichern und für Entwicklung erstellen**.

## Schritt 10: Senden von Informationen an Adobe Analytics durch Ihre Seite {#trigger-page}

In diesem Schritt installieren Sie die Chrome-Erweiterung **Launch and DTM Switch**. Bei dieser Erweiterung muss nur der Experience Platform Launch-Code für die Entwicklungsumgebung erstellt und bereitgestellt werden. Die Staging- und Produktionsumgebung müssen nicht bereitgestellt werden.

1. Installieren Sie die Chrome-Erweiterung **Launch and DTM Switch** von Discovery.
1. Klicken Sie auf das Symbol **Launch Switch** und stellen Sie die Option für das Debuggen auf *EIN*.
1. Laden Sie die Seite `http://<host>:<port>/content/core-components-examples/library/image.html` neu.
1. Öffnen Sie die Browser-Konsole. Darin sollte eine Ausgabe ähnlich der folgenden angezeigt werden.

![Ausgabe der Analytics-Konsole](/help/assets/analytics-console-output.png)

>[!TIP]
>
>Wenn Sie ergänzend dazu die Erweiterung **Experience Cloud Debugger** für Chrome installieren, können Sie Adobe Experience Platform Launch- und Analytics-spezifische Informationen zur Seite einsehen.

## Schritt 11: Anzeigen von in Adobe Analytics aufgezeichneten Informationen {#view-info}

Sie können nun die in Adobe Analytics ausgelösten Ereignisse einsehen.

1. Rufen Sie `https://analytics.adobe.com` auf.
1. Melden Sie sich mit Ihrer Adobe ID an.
1. Klicken Sie auf das **Analytics**-Symbol.
1. Wählen Sie die Registerkarte **Berichte** aus.
1. Wählen Sie in der Dropdown-Liste oben rechts die Report Suite aus, die Sie in [Schritt 1](#create-report-suite) erstellt haben.
1. Wählen Sie in der ersten Spalte **Benutzerspezifischer Traffic > Benutzerspezifischer Traffic 1–10 > Custom Insight 1** aus, um die aufgezeichneten Seiten-IDs (Pfade) anzuzeigen, die auf der Datenschicht gespeichert wurden. Die Ausgabe sollte in etwa wie folgt aussehen:

   ![Custom Insight 1](/help/assets/custom-insight-1.png)

1. Rufen Sie **Custom Insight 2** auf, um die auf der Datenschicht gespeicherten aufgezeichneten Bildpfade anzuzeigen. Die Ausgabe sollte in etwa wie folgt aussehen:

   ![Custom Insight 2](/help/assets/custom-insight-2.png)
