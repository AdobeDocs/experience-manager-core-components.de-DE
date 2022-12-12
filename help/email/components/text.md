---
title: E-Mail-Textkomponente
description: Die E-Mail-Textkomponente ist eine Komponente zur Bearbeitung und Erstellung von Rich-Texten, die eine Bearbeitung im Kontext ermöglicht.
role: Architect, Developer, Admin, User
exl-id: 4aa192f6-8314-40e7-8732-c6626d647986
source-git-commit: 33976c0e745ad091a142109f70541f01a31edc5b
workflow-type: ht
source-wordcount: '2328'
ht-degree: 100%

---


# E-Mail-Textkomponente {#email-text-component}

Die E-Mail-Textkomponente ist eine Komponente zur Bearbeitung und Erstellung von Rich-Texten, die eine Bearbeitung im Kontext ermöglicht.

## Verwendung {#usage}

Die E-Mail-Textkomponente bietet einen leistungsfähigen Rich-Text-Editor, der eine einfache Textbearbeitung in einem vereinfachten Inline-Editor sowie im Vollbild ermöglicht.

* Das [Dialogfeld „Bearbeiten“](#edit-dialog) verfügt über eine Inline-Bearbeitung mit eingeschränkten Optionen, während im Vollbild-Bearbeitungsdialogfeld alle Funktionen verfügbar sind.
* Durch Verwenden des [Dialogfelds „Design“](#design-dialog) können Textformatierungsoptionen wie Überschriften, Sonderzeichen und Absatzstile für die Vorlage des Inhaltsautors bzw. die Inhaltsautorin konfiguriert werden.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der E-Mail-Textkomponente ist v1. Sie wurde mit dem Release X der E-Mail-Kernkomponenten im Oktober 2022 eingeführt und wird in diesem Dokument beschrieben.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|
| v1 | Kompatibel | Kompatibel |

Weitere Informationen zu Kernkomponentenversionen und -Releases finden Sie im Dokument [E-Mail-Kernkomponentenversionen](/help/email/versions.md).

## Muster für Komponentenausgabe {#sample-component-output}

Um die Textkomponente sowie Beispiele für die Konfigurationsoptionen sowie HTML- und JSON-Ausgaben zu erhalten, besuchen Sie die [Komponentenbibliothek](https://adobe.com/go/aem_cmp_library_email_text).

### Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur E-Mail-Textkomponente [finden Sie auf GitHub](https://adobe.com/go/aem_cmp_tech_email_text_v1).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Die E-Mail-Textkomponente und der Rich-Text-Editor {#the-text-component-and-the-rich-text-editor}

Die E-Mail-Textkomponente nutzt den AEM-Rich-Text-Editor (RTE). Der Rich-Text-Editor (RTE) bietet Inhaltsautoren bzw. Inhaltsautorinnen eine große Bandbreite an Funktionen zum Bearbeiten von Textinhalten. Der RTE ist in seiner Konfiguration flexibel und bietet eine Reihe von Optionen. Weitere Informationen dazu, wie der RTE konfiguriert werden kann, finden Sie in den Artikeln [Konfigurieren des Rich-Text-Editors](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/configuring-and-extending/rich-text-editor.html?lang=de) und [Konfigurieren der Plug-ins für den Rich-Text-Editor](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/configuring-and-extending/configure-rich-text-editor-plug-ins.html?lang=de).

Der Rest dieses Dokuments zeigt die Standardkonfiguration der E-Mail-Textkomponente mit der vordefinierten RTE-Konfiguration.

>[!NOTE]
>
>In der E-Mail-Textkomponente sind nur Optionen verfügbar, die durch die [UI-Konfigurationen des RTE](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/configuring-and-extending/configure-rich-text-editor-plug-ins.html?lang=de) aktiviert sind.

## Dialogfeld „Bearbeiten“ {#edit-dialog}

![Dialogfeld „Bearbeiten“ der Textkomponente](/help/email/assets/email-text-edit.png)

### Formatierungsoptionen {#options}

Der Dialog „Bearbeiten“ bietet die standardmäßigen Rich-Text-Formatierungswerkzeuge zum Verfassen von Text.

#### Fett

![Symbol „Fett“](/help/assets/text-bold.png)

Wird verwendet, um eine fette Formatierung auf den ausgewählten Text anzuwenden oder den nach dem Cursor eingegebenen Text fett zu formatieren.

**Strg+B** kann als Tastaturbefehl verwendet werden.

#### Kursiv

![Symbol „Kursiv“](/help/assets/text-italic.png)

Wird verwendet, um eine kursive Formatierung auf den ausgewählten Text anzuwenden oder nach dem Cursor eingegebenen Text kursiv zu formatieren.

**Strg+I** kann als Tastaturbefehl verwendet werden.

#### Unterstrichen

![Symbol „Unterstrichen“](/help/assets/text-underline.png)

Wird verwendet, um eine unterstrichene Formatierung auf den ausgewählten Text anzuwenden oder Text, der nach dem Cursor eingegeben wird, zu unterstreichen.

**Strg+U** kann als Tastaturbefehl verwendet werden.

#### Tiefgestellt

![Symbol „Tiefgestellt“](/help/assets/text-subscript.png)

Wird verwendet, um ausgewählten Text oder Text, der nach dem Cursor eingegeben wird, als tiefgestellt zu formatieren.

#### Hochgestellt

![Symbol „Hochgestellt“](/help/assets/text-superscript.png)

Wird verwendet, um ausgewählten Text oder Text, der nach dem Cursor eingegeben wird, als hochgestellt zu formatieren.

#### Als Text einfügen

![Symbol „Als Text einfügen“](/help/assets/text-paste-text.png)

Fügt einen kopierten Text als unformatierten Text ein.

Wenn Sie diese Option wählen, wird ein Fenster geöffnet, in das der Text als unformatierter Text zur Vorschau eingefügt werden kann, bevor er in den Text eingefügt wird. Sie können diese Option durch Tippen oder Klicken auf das Häkchen akzeptieren oder den Vorgang durch Tippen oder Klicken auf das x abbrechen.

![Beispiel für „Als Text einfügen“](/help/assets/text-paste-text-example.png)

#### Aus Word einfügen

![Symbol „Aus Word einfügen“](/help/assets/text-paste-word.png)

Wenn Sie diese Option wählen, wird ein Fenster geöffnet, in dem der formatierte Text zur Vorschau eingefügt werden kann, bevor er in den Text eingefügt wird. Sie können diese Option durch Tippen oder Klicken auf das Häkchen akzeptieren oder den Vorgang durch Tippen oder Klicken auf das x abbrechen.

![Beispiel für „Aus Word einfügen“](/help/assets/text-paste-word-example.png)

#### Hyperlink

![Symbol „Hyperlink“](/help/assets/text-hyperlink.png)

Mit dieser Option können Sie den ausgewählten Text in einen Hyperlink konvertieren oder einen bereits definierten Link ändern. Diese Option öffnet ein Fenster mit zusätzlichen Optionen zum Festlegen des Links.

![Beispiel für „Hyperlink“](/help/assets/text-hyperlink-example.png)

* Geben Sie den Pfad ein.
   * Wählen Sie das Dialogfeld **Auswahl öffnen**, um in AEM einen Pfad auszuwählen
   * Wenn der Link in AEM nicht angezeigt wird, geben Sie die absolute URL ein.
      * Nicht-absolute Pfade werden als relativ zu AEM interpretiert.
* Alternativen beschreibenden Text für den Link eingeben
* Linkverhalten auswählen
   * Ziel
   * Selbe Registerkarte
   * Neue Registerkarte
   * Übergeordneter Frame
   * Top-Frame

Tippen oder klicken Sie auf das Häkchen, um den Link anzuwenden, oder auf das x um abzubrechen.

#### Verknüpfung aufheben

![Symbol „Verknüpfung aufheben“](/help/assets/text-unlink.png)

Mit dieser Option können Sie einen bereits auf den ausgewählten Text angewendeten Link entfernen. Diese Option ist nur aktiv, wenn bereits ein Link ausgewählt ist.

#### Anker {#anchor}

![Ankersymbol](/help/email/assets/anchor.png)

Verwenden Sie diese Option, um einen Anker in den Text einzufügen.

#### Suchen

![Symbol „Suchen“](/help/assets/text-find.png)

Verwenden Sie diese Option, um den Text nach dem Vorkommen einer angegebenen Textzeichenfolge zu durchsuchen. Wenn Sie diese Option auswählen, wird ein Fenster zum Festlegen der Suchoptionen geöffnet.

![Beispiel für „Suchen“](/help/assets/text-find-example.png)

Geben Sie den Text ein, nach dem Sie suchen möchten, und tippen oder klicken Sie auf **Suchen**, um die Suche zu starten. Tippen Sie auf das x, um abzubrechen.
Wenn Sie eine genaue Übereinstimmung der Groß- und Kleinschreibung möchten, wählen Sie die Option **Groß-/Kleinschreibung beachten**, bevor Sie die Suche starten.
Wenn eine Übereinstimmung gefunden wird, wird sie hervorgehoben und das Suchdialogfeld wird abgeblendet. Tippen oder klicken Sie im abgeblendeten Dialogfeld erneut auf die Schaltfläche **Suchen**, um nach dem nächsten Vorkommen zu suchen.

![Beispiel für mittels „Suchen“ gefundenen Text](/help/assets/text-find-example-found.png)

Wenn keine weiteren Vorkommen gefunden werden, wird eine Meldung angezeigt und die Suche wird am Anfang des Texts neu gestartet.

![Beispiel für „Suchen“ mit keinen weiteren Vorkommen](/help/assets/text-find-example-found-end.png)

#### Ersetzen

![Symbol „Ersetzen“](/help/assets/text-replace.png)

Verwenden Sie diese Option, um den Text nach dem Vorkommen einer angegebenen Textzeichenfolge zu durchsuchen und die Übereinstimmungen durch eine andere Zeichenfolge zu ersetzen. Wenn Sie diese Option auswählen, wird ein Fenster zum Festlegen der Optionen für Suchen und Ersetzen geöffnet.

![Beispiel für „Ersetzen“](/help/assets/text-replace-example.png)

Geben Sie den Text ein, für den Sie eine Suche durchführen möchten, sowie den Text, durch den er ersetzt werden soll.

* Tippen oder klicken Sie auf **Suchen**, um mit der Suche zu beginnen. Klicken oder tippen Sie auf das x, um abzubrechen.
* Wenn Sie eine genaue Übereinstimmung der Groß- und Kleinschreibung möchten, wählen Sie die Option **Groß-/Kleinschreibung beachten**, bevor Sie die Suche starten.
* Wählen Sie **Alle ersetzen** aus, um alle Vorkommen des Texts gleichzeitig zu ersetzen.

Wenn eine Übereinstimmung gefunden wird, wird sie hervorgehoben und das Suchdialogfeld wird abgeblendet. Klicken Sie erneut im abgeblendeten Dialogfeld auf die Schaltfläche **Suchen**, um nach dem nächsten Vorkommen zu suchen, oder klicken Sie auf **Ersetzen**, um den markierten, übereinstimmenden Text zu ersetzen. Beachten Sie, dass die Schaltfläche **Ersetzen** erst aktiv ist, nachdem der Suchtext gefunden wurde.

Das Dialogfeld „Suchen und ersetzen“ wird transparent, wenn auf „Suchen“ geklickt wird, und undurchsichtig, wenn auf „Ersetzen“ geklickt wird. Dadurch kann der Autor den Text überprüfen, den der Autor ersetzen wird.

>[!NOTE]
>
>Bei Verwendung der Funktion „Ersetzen“ sollte die zu ersetzende Zeichenfolge gleichzeitig mit der zu suchenden Zeichenfolge eingegeben werden. Sie können jedoch weiterhin auf „Suchen“ klicken, um nach der Zeichenfolge zu suchen, bevor Sie sie ersetzen. Wenn die Zeichenfolge zum Ersetzen eingegeben wird, nachdem auf „Suchen“ geklickt wurde, wird die Suche auf den Anfang des Textes zurückgesetzt.

#### Rückgängig machen

![Symbol „Rückgängig“](/help/email/assets/undo.png)

Wird verwendet, um die letzte Bearbeitung im Rich-Text-Editor rückgängig zu machen.

#### Wiederholen

![Symbol „Wiederholen“](/help/email/assets/redo.png)

Wird verwendet, um eine Bearbeitung, die mithilfe des Rückgängig-Symbols rückgängig gemacht wurde, erneut rückgängig zu machen.

#### Text linksbündig ausrichten

![Symbol „Linksbündig ausrichten“](/help/assets/text-left.png)

Wird verwendet, um den Text am linken Rand auszurichten.

#### Text zentrieren

![Symbol „Text zentrieren“](/help/assets/text-center.png)

Wird zum Zentrieren des Texts verwendet.

#### Text rechtsbündig ausrichten

![Symbol „Rechtsbündig ausrichten“](/help/assets/text-right.png)

Wird verwendet, um den Text am rechten Rand auszurichten.

#### Aufzählungszeichen

![Symbol „Aufzählungszeichen“](/help/assets/text-bullet.png)

Wird verwendet, um den ausgewählten Text als Liste mit Aufzählungszeichen zu formatieren oder eine Liste mit Aufzählungszeichen nach dem Cursor einzufügen.

Um eine Liste mit Aufzählungszeichen zu beenden, tippen oder klicken Sie erneut auf die Schaltfläche **Aufzählung** oder geben Sie zwei Zeilenumbrüche hintereinander ein.

#### Nummerierung

![Symbol „Nummerierung“](/help/assets/text-numbered.png)

Wird verwendet, um den ausgewählten Text als nummerierte Liste zu formatieren oder eine nummerierte Liste nach dem Cursor einzufügen.

Um eine nummerierte Liste zu beenden, tippen oder klicken Sie erneut auf die Schaltfläche **Nummeriert** oder geben Sie zwei Zeilenumbrüche hintereinander ein.

#### Ausrücken

![Symbol „Ausrücken“](/help/assets/text-outdent.png)

Wird verwendet, um den Einzug des ausgewählten Texts oder des nach dem Cursor eingegebenen Texts zu verringern.

Nur aktiv, wenn der ausgewählte Text bzw. die ausgewählte Position bereits eingerückt ist.

#### Einzug

![Symbol „Einzug“](/help/assets/text-indent.png)

Wird verwendet, um den Einzug des ausgewählten Texts oder des nach dem Cursor eingegebenen Textes zu erhöhen.

#### Tabelle

![Symbol „Tabelle“](/help/assets/text-table.png)

Wird verwendet, um eine Tabelle in den Text einzufügen. Wenn Sie diese Option auswählen, wird ein Fenster zum Festlegen der Details der Tabelle geöffnet.

![Beispiel für „Tabelle“](/help/assets/text-table-example.png)

* **Spalten** - Die Anzahl der Spalten der Tabelle (erforderlich)
* **Zeilen** - Die Anzahl der Zeilen der Tabelle (erforderlich)
* **Breite** - Die Gesamtbreite der Tabelle
* **Höhe** - Die Gesamthöhe der Tabelle
* **Textabstand** - Der Abstand um den Zelleninhalt
* **Zellenabstand** - Der Abstand zwischen Zellen
* **Rahmen** - Die Stärke der Randlinien der Tabelle
   * Für die Kopfzeile der Tabelle:
      * Die erste Zeile sollte verwendet werden
      * Die erste Spalte sollte verwendet werden
      * Die erste Zeile und erste Spalte sollten verwendet werden
      * Oder es sollte keine Kopfzeile verwendet werden
* **Beschriftung** - Beschriftung der Tabelle

#### Bild

![Bildsymbol](/help/email/assets/image-icon.png)

Wird zum Ausrichten eines eingefügten Bildes verwendet.

#### Rechtschreibprüfung

![Symbol „Rechtschreibprüfung“](/help/assets/text-spellcheck.png)

Wird verwendet, um die Rechtschreibung des Textinhalts zu überprüfen. Mögliche Rechtschreibfehler sind durch gestrichelte rote Linien unterstrichen.

Weitere Details zur Rechtschreibprüfung und zum Anpassen von Rechtschreibprüfungswörterbüchern finden Sie im Dokument [Konfigurieren der Plug-ins für Rich-Text-Editor](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/configuring-and-extending/configure-rich-text-editor-plug-ins.html?lang=de).

#### Sonderzeichen {#special-characters}

![Symbol „Sonderzeichen“](/help/assets/text-special-characters.png)

Wird verwendet, um Sonderzeichen in den Text einzufügen. Wenn Sie diese Option auswählen, wird ein Fenster geöffnet, in dem die verfügbaren Zeichen angezeigt werden.

![Beispiel für „Sonderzeichen“](/help/assets/text-special-characters-example.png)

Tippen oder klicken Sie auf das gewünschte Zeichen, um es nach dem Cursor in den Text einzufügen. Es können mehrere Zeichen eingefügt werden. Tippen oder klicken Sie auf das x, um das Auswahlfenster zu schließen.

#### Quellenbearbeitung

![Symbol „Quellenbearbeitung“](/help/assets/text-source.png)

Wird verwendet, um die HTML-Quelle des Texts anzuzeigen und zu ändern.

Tippen oder klicken Sie auf das Symbol **Quellbearbeitung**, um den Inhalt des Texts statt in der formatierten Ansicht als rohe HTML anzuzeigen. In diesem Modus sind alle anderen Formatierungsoptionen deaktiviert. Tippen oder klicken Sie erneut auf das Symbol **Quellbearbeitung**, um zur formatierten Ansicht zurückzukehren.

>[!CAUTION]
>
>Wie immer bei Zugriff auf rohe HTML müssen Sie bei der Verwendung der Option **Quellbearbeitung** Vorsicht walten lassen!
>
>HTML, die über die **Quellbearbeitung** eingegeben wurde, wird auf XSS-Risiken überprüft und alle Skripte, die eingefügt werden, werden entfernt und nicht auf der resultierenden Seite angezeigt. Fehlerhafte HTML-Einträge, die in der **Quellbearbeitung** eingegeben wurden, können die Vorlage für die Seite durchbrechen, was zu unerwarteten Formatierungen führen oder die resultierende Seite unbrauchbar machen kann.

>[!NOTE]
>
>Da HTML, die über die **Quellbearbeitung** eingegeben wird, auf XSS-Risiken und Skripten gescannt und solche automatisch entfernt werden, kann der tatsächlich verbleibende Inhalt von dem, was in der **Quellbearbeitung** eingegeben wurde, variieren. Aus diesem Grund müssen Sie zum Speichern von Änderungen, die mit der **Quellbearbeitung** vorgenommen wurden, erst die **Quellbearbeitung** verlassen, um den Text im normalen Editor vor dem Speichern anzuzeigen.

#### Absatzformat

![Symbol „Absatzformat“](/help/assets/text-paragraph.png)

Wird verwendet, um Absatzformatierung auf den ausgewählten Text anzuwenden oder auf Text, der nach dem Cursor eingefügt wird. Durch Auswahl dieser Optionen wird eine Dropdown-Liste geöffnet, in der das Absatzformat ausgewählt werden kann.

![Beispiel für „Absatzformat“](/help/assets/text-paragraph-example.png)

#### Adobe Campaign-Variable auswählen

![Adobe Campaign-Variablensymbol auswählen](/help/email/assets/select-adobe-campaign-variable-icon.png)

Öffnet das Dialogfeld [Adobe Campaign-Variable auswählen](/help/email/campaign-variables.md) zum Einfügen von dynamischen Inhalten aus Adobe Campaign.

### Inline-Bearbeitung {#in-line-editing}

Die Textkomponente kann auch inline bearbeitet werden. Um die Bearbeitung inline durchzuführen, wählen Sie auf der Inhaltsseite die E-Mail-Textkomponente aus.

![E-Mail-Textkomponente auswählen](/help/email/assets/email-text-select-component.png)

Tippen oder klicken Sie dann auf das Symbol **Bearbeiten** in der Symbolleiste, die über der Komponente eingeblendet wird. Die Symbolleiste ändert sich und zeigt eingeschränkte Textformatierungsoptionen an (einschließlich Zugriff auf die Option **Adobe Campaign-Variable auswählen**). Sie können dann den Text inline bearbeiten.

![Beispiel für die Inline-Bearbeitung](/help/email/assets/email-text-edit-inline-example.png)

Tippen oder klicken Sie auf das Häkchen in der Symbolleiste, um Ihre Änderungen zu speichern oder auf das X, um sie zu verwerfen.

Aufgrund von Platzbeschränkungen sind nicht alle Formatierungsoptionen inline verfügbar. Um alle Optionen anzuzeigen, wechseln Sie zum Vollbildmodus.

### Festlegen einer ID {#setting-id}

Diese Option ermöglicht das Festlegen der eindeutigen Kennung der Komponente in HTM.

* Wenn Sie das Feld leer lassen, wird automatisch eine eindeutige ID generiert, die Sie über die resultierende Seite finden.
* Sofern eine ID angegeben wird, ist vom Autor bzw. der Autorin sicherzustellen, dass diese eindeutig ist.
* Die Änderung der ID kann sich auf CSS auswirken.

## Dialogfeld „Design“ {#design-dialog}

Im Dialogfeld „Design“ kann der Vorlagenautor festlegen, welche Textformatierungsoptionen den Inhaltsautoren zur Verfügung stehen.

### Registerkarte „Plug-ins“ {#plugins-tab}

Die Registerkarte **Plugins** wird verwendet, um verschiedene Textformatierungsoptionen, die den Inhaltsautoren bzw. Inhaltsautorinnen zur Verfügung stehen, zu aktiveren oder zu deaktivieren.

### Funktionen {#features}

![„Funktionen“ im Dialogfeld „Design“](/help/assets/text-design-features.png)

Die folgenden Funktionen können für die Komponente aktiviert oder deaktiviert werden.

* Unformatierten Text einfügen
* Aus Word einfügen
* Suchen und Ersetzen
* Rückgängig machen und wiederholen
* Rechtschreibprüfung
* Optionen zur Änderung eingefügter Bilder
* HTML-Quellbearbeitung

### Formatierung {#formatting}

![„Formatierung“ im Dialogfeld „Design“](/help/assets/text-design-formatting.png)

Die folgenden Formatierungsoptionen können für die Komponente aktiviert oder deaktiviert werden.

* Tabelle
* Listen (Aufzählungszeichen, Nummer, Einzug, Ausrücken)
* Ausrichtung (links, rechts, zentriert)
* Fett, kursiv, unterstrichen
* Verknüpfen (und Verknüpfung aufheben)
* Tiefgestellt/hochgestellt

### Absatzformate {#paragraph-styles}

![„Absatzformate“ im Dialogfeld „Design“](/help/assets/text-design-paragraph.png)

Absatzstile können für die Komponente aktiviert oder deaktiviert werden. Bei Aktivierung können die zulässigen Formate definiert werden.

* Tippen oder klicken Sie auf die Schaltfläche **Hinzufügen**, um einen neuen Stil einzufügen.
* Geben Sie den Code des Stils und eine Beschreibung ein, die im Dialogfeld „Bearbeiten“ angezeigt wird.
* Um einen Stil zu entfernen, tippen Sie auf die Schaltfläche **Löschen**.
* Um die Reihenfolge der Formate zu ändern, tippen oder klicken Sie auf die Griffe und ziehen Sie sie in die gewünschte Reihenfolge.

### Sonderzeichen {#configuring-special-characters}

![„Sonderzeichen“ im Dialogfeld „Design“](/help/assets/text-design-special-characters.png)

Die Option zum Einfügen von Sonderzeichen kann für die Komponente aktiviert oder deaktiviert werden. Bei Aktivierung können die zulässigen Zeichen definiert werden.

* Tippen oder klicken Sie auf die Schaltfläche **Hinzufügen**, um ein neues Zeichen einzufügen.
* Geben Sie den HTML-Code des Zeichens und eine Beschreibung ein, die im Dialogfeld „Bearbeiten“ angezeigt wird.
* Um ein Zeichen zu entfernen, tippen oder klicken Sie auf die Schaltfläche **Löschen**.
* Um die Reihenfolge der Zeichen zu ändern, tippen oder klicken Sie auf die Griffe und ziehen Sie sie in die gewünschte Reihenfolge.

## Registerkarte „Arten“ {#styles-tab}

Die E-Mail-Textkomponente unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).
