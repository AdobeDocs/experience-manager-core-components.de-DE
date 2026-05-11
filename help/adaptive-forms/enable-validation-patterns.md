---
title: Aktivieren und Verwenden von Überprüfungsmustern für Texteingaben in adaptiven Formularen von Adobe Experience Manager
description: Erfahren Sie, wie Sie Vorlagenrichtlinien konfigurieren, um Überprüfungsmuster wie Telefonnummern, Sozialversicherungsnummern und Postleitzahlen verfügbar zu machen, und verwenden sie diese dann in Ihrem adaptiven Formular.
hide: true
exl-id: e4500666-1346-4558-861d-da9541dcef51
source-git-commit: 59064c359aea14af99675709bbddf9a933a959df
workflow-type: ht
source-wordcount: '861'
ht-degree: 100%

---

# Aktivieren und Verwenden von Überprüfungsmustern für Texteingaben in adaptiven Formularen von Adobe Experience Manager

## Übersicht

In Adobe Experience Manager (Adobe Experience Manager) Forms werden bestimmte Validierungsformate (z. B. Sozialversicherungsnummern, E-Mail-Adressen oder Postleitzahlen) für Texteingabekomponenten auf Vorlagenrichtlinienebene gesteuert. In diesem Handbuch wird erläutert, wie Sie:

1. Auf den Vorlageneditor zugreifen und die Richtlinie für die Texteingabekomponente konfigurieren, um Überprüfungsmuster verfügbar zu machen.
2. Ein adaptives Formular erstellen und diese Überprüfungsmuster auf eine Texteingabekomponente anwenden.

## Voraussetzungen

- Zugriff auf eine Adobe Experience Manager-Instanz, in der Forms aktiviert ist.
- Berechtigungen zum Bearbeiten von Vorlagen (normalerweise Teil der Gruppe `template-authors`).
- Berechtigungen zum Erstellen und Bearbeiten von adaptiven Formularen.

## Teil 1: Aktivieren von Überprüfungsmustern in der Vorlage

>[!VIDEO](https://video.tv.adobe.com/v/3480390/)

### Schritt 1: Zugreifen auf die Vorlagenkonsole

1. Klicken Sie auf dem Adobe Experience Manager-Startbildschirm auf **Tools** (das Hammersymbol) in der linken Seitenleiste.
2. Navigieren Sie zu **Allgemein > Vorlagen**.
3. Wählen Sie den Ordner aus, der Ihre Projektvorlagen enthält (z. B. Kernkomponentenbeispiele).
4. Suchen Sie die konkrete Vorlage, die Sie ändern möchten (z. B. AF Blank), und wählen Sie sie aus.
5. Klicken Sie auf **Bearbeiten** (oder öffnen Sie die Vorlage direkt).

### Schritt 2: Zugreifen auf die Komponentenstruktur

1. Stellen Sie sicher, dass Sie sich in der Ansicht **Struktur** befinden (wählen Sie ggf. „Struktur“ aus der Dropdown-Liste „Modus“ oben rechts aus).
2. Suchen Sie den Haupt-**Layout-Container** oder den spezifischen Container, in dem Ihre Texteingabekomponente zulässig ist.
3. Klicken Sie auf den Container, um die Liste der zulässigen Komponenten anzuzeigen.
4. Suchen Sie die Komponente **Adaptives Formular - Textfeld** in der Liste.
5. Klicken Sie auf das Symbol **Richtlinie** (dargestellt durch ein Datei-/Schubladensymbol) neben dem Komponentennamen.

### Schritt 3: Konfigurieren der Richtlinie für die Texteingabekomponente

1. Klicken Sie im Richtlinieneditor auf die Registerkarte **Formate** auf der rechten Seite des Fensters.
2. Daraufhin wird eine Liste der verfügbaren Überprüfungsmuster angezeigt. Markieren Sie die Kästchen für die Formate, die Sie aktivieren möchten:
   - Telefonnummer
   - Sozialversicherungsnummer
   - E-Mail (alphanumerisch)
   - Postleitzahl

### Schritt 4: Definieren und Speichern der Richtlinie

1. Wechseln Sie zurück zur Registerkarte **Richtlinie** (oder überprüfen Sie die Einstellungen auf der linken Seite).
2. Geben Sie im Feld **Richtlinienname** einen eindeutigen Namen ein (z. B. `new-textinput-default-policy`).
3. Klicken Sie oben rechts auf das Symbol **Fertig** (Häkchen), um die Änderungen zu speichern.

## Teil 2: Erstellen eines Formulars und Verwenden von Überprüfungsmustern

Nachdem Überprüfungsmuster in der Vorlage aktiviert wurden, können Sie ein adaptives Formular erstellen und sie auf Texteingabekomponenten anwenden.

>[!VIDEO](https://video.tv.adobe.com/v/3480391/)

### Schritt 1: Erstellen eines adaptivenFormulars

1. Navigieren Sie zur Oberfläche **Formulare und Dokumente**.
2. Klicken Sie oben rechts auf die Schaltfläche **Erstellen**.
3. Wählen Sie **Adaptives Formular** aus den Optionen der Dropdown-Liste aus.
4. Wählen Sie die Vorlage aus, in der Sie die Überprüfungsmuster aktiviert haben (z. B **Blank**), und klicken Sie auf **Weiter**.
5. Am Bildschirm „Eigenschaften hinzufügen“:
   - Gegen Sie einen **Titel** für Ihr Formular ein (z. B. „TestRichtlinie“). Das Feld **Name** wird basierend auf dem Titel automatisch ausgefüllt. 
   - Stellen Sie sicher, dass die korrekte **Design-Client-Bibliothek** ausgewählt ist (z. B. `adaptiveform.theme.canvas3`).
6. Klicken Sie auf **Erstellen**. Eine Erfolgsmeldung wird angezeigt.
7. Klicken Sie auf **Bearbeiten**, um das Formular im Editor zu öffnen.

### Schritt 2: Hinzufügen einer Texteingabekomponente

1. Navigieren im Formular-Editor zum **Komponenten**-Browser in der linken Seitenleiste.
2. Verwenden Sie die Suchleiste, um die Komponente **Adaptives Formular – Textfeld** zu finden. Durch Eingabe von „Text“ wird die Liste gefiltert.
3. Klicken Sie auf die Komponente **Adaptives Formular – Textfeld** und ziehen Sie sie auf die Hauptarbeitsfläche.

### Schritt 3: Konfigurieren der Komponentenformatierung

1. Klicken Sie auf die neu hinzugefügte Komponente **Texteingabe**, um sie auszuwählen.
2. Klicken Sie auf das Symbol **Konfigurieren** (dargestellt durch einen Schraubenschlüssel) in der Symbolleiste, die über der Komponente angezeigt wird.
3. Navigieren Sie im Dialogfeld „Eigenschaften“ zur Registerkarte **Formate**. 
4. Navigieren Sie zum Dropdown-Menü **Typ** und ändern Sie die Auswahl in **Telefonnummer** (oder ein anderes aktiviertes Format).

### Schritt 4: Konfigurieren der Datenvalidierung

1. Navigieren Sie im Dialogfeld „Komponentenkonfiguration“ zur Registerkarte **Überprüfung**.
2. Navigieren Sie zum Abschnitt **Überprüfungsmuster**.
3. Klicken Sie auf das Dropdown-Menü **Typ**.
4. Wählen Sie **Telefonnummer** aus der Liste der Überprüfungsmuster aus. Dadurch wird sichergestellt, dass im Formular ein Fehler ausgegeben wird, wenn Benutzende Text eingeben, der keinem gültigen Telefonnummernformat entspricht.
5. Klicken Sie oben rechts im Dialogfeld auf das Symbol **Fertig** (Häkchen), um die Änderungen zu speichern.

## Überprüfung

So überprüfen Sie, ob die Überprüfungsmuster ordnungsgemäß funktionieren:

1. Zeigen Sie das Formular in der Vorschau im Editor an.
2. Geben Sie Testdaten in die Komponente **Texteingabe** ein.
3. Bestätigen Sie Folgendes:
   - Die aktivierten Überprüfungsmuster werden auf den Registerkarten „Formate“ und „Überprüfung“ der Komponente angezeigt.
   - Eine ungültige Eingabe löst entsprechende Fehlermeldungen aus.
   - Eine gültige Eingabe wird fehlerfrei akzeptiert.

## Fehlerbehebung

- **Problem:** Die Überprüfungsmuster werden nicht in der Formularkomponente angezeigt.
   - **Lösung:** Stellen Sie sicher, dass die Vorlagenrichtlinie korrekt gespeichert wurde und dass Sie beim Erstellen des Formulars die richtige Vorlage verwenden.

- **Problem:** Es kann nicht auf den Vorlageneditor zugegriffen werden.
   - **Lösung:** Vergewissern Sie sich, dass Sie über die erforderlichen Berechtigungen zum Bearbeiten von Vorlagen verfügen (Zugehörigkeit der Gruppe `template-authors`).

- **Problem:** Die Texteingabekomponente validiert eine Eingabe nicht korrekt.
   - **Lösung:** Überprüfen Sie die Einstellungen für das Überprüfungsmuster auf der Registerkarte „Überprüfung“ der Komponente erneut und stellen Sie sicher, dass das richtige Muster ausgewählt ist.

## Nächste Schritte

Nach der Aktivierung und Verwendung von Überprüfungsmustern für Texteingaben in Ihren adaptiven Formularen von Adobe Experience Manager:

- Konfigurieren Sie zusätzliche Überprüfungsmuster für andere Datentypen.
- Erkunden Sie andere Komponentenrichtlinien, um das Formularverhalten anzupassen.
- Richten Sie die Verarbeitung von Formularübermittlungen und die Datenverarbeitungslogik ein.
