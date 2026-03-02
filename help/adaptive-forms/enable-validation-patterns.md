---
title: Aktivieren und Verwenden von Validierungsmustern für Texteingaben in Adobe Experience Manager Adaptive Forms
description: Erfahren Sie, wie Sie Vorlagenrichtlinien konfigurieren, um Validierungsmuster wie Telefonnummern, Sozialversicherungsnummern und Postleitzahlen offenzulegen, und diese dann in Ihrem adaptiven Forms verwenden.
hide: true
hidefromtoc: true
source-git-commit: 1ac3d987337f8279e762ab5357d32bb732dea0be
workflow-type: tm+mt
source-wordcount: '861'
ht-degree: 1%

---


# Aktivieren und Verwenden von Validierungsmustern für Texteingaben in Adobe Experience Manager Adaptive Forms

## Übersicht

In Adobe Experience Manager (Adobe Experience Manager) Forms werden bestimmte Validierungsformate (z. B. Sozialversicherungsnummern, E-Mail-Adressen oder Postleitzahlen) für Texteingabekomponenten auf Vorlagenrichtlinienebene gesteuert. In diesem Handbuch wird Folgendes erläutert:

1. Greifen Sie auf den Vorlageneditor zu und konfigurieren Sie die Richtlinie der Texteingabekomponente, um Validierungsmuster anzuzeigen.
2. Erstellen Sie ein adaptives Formular und wenden Sie diese Überprüfungsmuster auf eine Texteingabekomponente an.

## Voraussetzungen

- Zugriff auf eine Adobe Experience Manager-Instanz mit aktiviertem Forms.
- Berechtigungen zum Bearbeiten von Vorlagen (normalerweise Teil der `template-authors`).
- Berechtigungen zum Erstellen und Bearbeiten von adaptiven Forms.

## Teil 1: Aktivieren von Validierungsmustern in der Vorlage

>[!VIDEO](https://video.tv.adobe.com/v/3480390/)

### Schritt 1: Aufrufen der Vorlagenkonsole

1. Klicken Sie auf dem Adobe Experience Manager-Startbildschirm **Tools** (das Hammersymbol) in der linken Seitenleiste.
2. Navigieren Sie zu **Allgemein > Vorlagen**.
3. Wählen Sie den Ordner aus, der Ihre Projektvorlagen enthält (z. B. Kernkomponentenbeispiele).
4. Suchen Sie die spezifische Vorlage, die Sie ändern möchten (z. B. AF Blank), und wählen Sie sie aus.
5. Klicken Sie **Bearbeiten** (oder öffnen Sie die Vorlage direkt).

### Schritt 2: Zugreifen auf die Komponentenstruktur

1. Stellen Sie sicher, dass Sie sich in **Struktur**-Ansicht befinden (wählen Sie ggf. „Struktur“ aus der Dropdown-Liste „Modus“ oben rechts).
2. Suchen Sie den Haupt **Layout-Container** oder den spezifischen Container, in dem Ihre Texteingabekomponente zulässig ist.
3. Klicken Sie auf den Container, um die Liste der zulässigen Komponenten anzuzeigen.
4. Suchen Sie die Komponente **Adaptives Formular - Textfeld** in der Liste.
5. Klicken Sie auf **Richtlinie**-Symbol (dargestellt durch ein Datei-/Schubladensymbol) neben dem Komponentennamen.

### Schritt 3: Konfigurieren der Richtlinie für die Texteingabekomponente

1. Klicken Sie im Richtlinien-Editor auf **Registerkarte** Formate“ auf der rechten Seite des Fensters.
2. Daraufhin wird eine Liste der verfügbaren Validierungsmuster angezeigt. Markieren Sie die Kästchen für die Formate, die Sie aktivieren möchten:
   - Telefonnummer
   - Sozialversicherungsnummer
   - E-Mail (alphanumerisch)
   - Postleitzahl

### Schritt 4: Richtlinie definieren und speichern

1. Wechseln Sie zurück zur Registerkarte **Richtlinie** (oder überprüfen Sie die Einstellungen auf der linken Seite).
2. Geben **im Feld** einen eindeutigen Namen ein (z. B. `new-textinput-default-policy`).
3. Klicken Sie auf **Fertig** (Häkchen) oben rechts, um Ihre Änderungen zu speichern.

## Teil 2: Erstellen eines Formulars und Verwenden von Validierungsmustern

Nachdem Validierungsmuster in der Vorlage aktiviert wurden, können Sie ein adaptives Formular erstellen und sie auf Texteingabekomponenten anwenden.

>[!VIDEO](https://video.tv.adobe.com/v/3480391/)

### Schritt 1: Adaptives Formular erstellen

1. Navigieren Sie zur Benutzeroberfläche von **Forms und Dokumente**.
2. Klicken Sie auf **Erstellen** oben rechts.
3. Wählen Sie **adaptives Formular** aus den Dropdown-Optionen aus.
4. Wählen Sie die Vorlage aus, in der Sie die Validierungsmuster aktiviert haben (z. B **&quot;**„), und klicken Sie auf **Weiter**.
5. Im Bildschirm Eigenschaften hinzufügen :
   - Geben Sie **Formular einen** Titel“ ein (z. B. „testPolicy„). Das Feld **Name** wird basierend auf dem Titel automatisch ausgefüllt.
   - Stellen Sie sicher **dass die richtige (Design** Client-Bibliothek) ausgewählt ist (z. B. `adaptiveform.theme.canvas3`).
6. Klicken Sie auf **Erstellen**. Eine Erfolgsmeldung wird angezeigt.
7. Klicken Sie **Bearbeiten**, um das Formular im Editor zu öffnen.

### Schritt 2: Hinzufügen einer Texteingabekomponente

1. Suchen Sie im Formular-Editor den **Komponenten** in der linken Seitenleiste.
2. Verwenden Sie die Suchleiste, um die Komponente **Textfeld für adaptive Formulare** zu finden. Durch Eingabe von „Text“ wird die Liste gefiltert.
3. Klicken Sie auf die Komponente **Textfeld für adaptive Formulare** und ziehen Sie sie in den Hauptbereich der Arbeitsfläche.

### Schritt 3: Konfigurieren der Komponentenformatierung

1. Klicken Sie auf die neu hinzugefügte Komponente **Texteingabe**, um sie auszuwählen.
2. Klicken Sie auf das **Konfigurieren**-Symbol (dargestellt durch einen Schraubenschlüssel) in der Symbolleiste, die über der Komponente angezeigt wird.
3. Navigieren Sie im Dialogfeld „Eigenschaften“ zur Registerkarte **Formate** .
4. Suchen Sie das Dropdown **Menü „Typ** und ändern Sie die Auswahl in **Telefonnummer** (oder ein anderes aktiviertes Format).

### Schritt 4: Konfigurieren der Datenvalidierung

1. Navigieren Sie im Dialogfeld für die Komponentenkonfiguration zur Registerkarte **Validierung**.
2. Suchen Sie den Abschnitt **Überprüfungsmuster**.
3. Klicken Sie auf **Dropdown** Menü „Typ“.
4. Wählen Sie **Telefonnummer** aus der Liste der Überprüfungsmuster aus. Dadurch wird sichergestellt, dass im Formular ein Fehler ausgegeben wird, wenn der Benutzer Text eingibt, der keinem gültigen Telefonnummernformat entspricht.
5. Klicken Sie auf **Fertig** (Häkchen) oben rechts im Dialogfeld, um Ihre Änderungen zu speichern.

## Überprüfung

So überprüfen Sie, ob die Validierungsmuster ordnungsgemäß funktionieren:

1. Vorschau des Formulars im Editor.
2. Geben Sie Testdaten in die Komponente **Texteingabe** ein.
3. Bestätigen Sie Folgendes:
   - Die aktivierten Validierungsmuster werden auf den Registerkarten Formate und Validierung der Komponente angezeigt.
   - Ungültige Eingabe-Trigger für entsprechende Fehlermeldungen.
   - Gültige Eingabe wird fehlerfrei akzeptiert.

## Fehlerbehebung

- **Problem** Die Überprüfungsmuster werden nicht in der Formularkomponente angezeigt.
   - **Lösung:** Stellen Sie sicher, dass die Vorlagenrichtlinie korrekt gespeichert wurde und dass Sie beim Erstellen des Formulars die richtige Vorlage verwenden.

- **Problem:** auf den Vorlageneditor kann nicht zugegriffen werden.
   - **Lösung:** Vergewissern Sie sich, dass Sie über die erforderlichen Berechtigungen zum Bearbeiten von Vorlagen verfügen (Mitgliedschaft in der `template-authors`).

- **Problem:** Die Texteingabekomponente validiert eine Eingabe nicht korrekt.
   - **Lösung:** Überprüfen Sie die Einstellungen für das Überprüfungsmuster auf der Registerkarte Validierung der Komponente erneut und stellen Sie sicher, dass das richtige Muster ausgewählt ist.

## Nächste Schritte

Nach der Aktivierung und Verwendung von Validierungsmustern für Texteingaben in Ihrem Adobe Experience Manager Adaptive Forms:

- Konfigurieren Sie zusätzliche Validierungsmuster für andere Datentypen.
- Erkunden Sie andere Komponentenrichtlinien, um das Formularverhalten anzupassen.
- Richten Sie die Verarbeitung von Formularübermittlungen und die Datenverarbeitungslogik ein.
