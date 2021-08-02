---
title: Textkomponente
description: Die Textkomponente ist eine Komponente zur Bearbeitung und Zusammensetzung von Rich-Texten, die eine direkte Bearbeitung ermöglicht.
role: Architect, Developer, Admin, User
exl-id: bcea202a-9ecb-4dcd-99b6-0848cbb9d500
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: ht
source-wordcount: '2213'
ht-degree: 100%

---

# Textkomponente{#text-component}

Die Kernkomponente „Textkomponente“ ist eine Komponente zur Bearbeitung und Zusammensetzung von Rich-Texten, die eine direkte Bearbeitung ermöglicht.

## Nutzung {#usage}

Die Textkomponente bietet einen robusten Rich-Text-Editor, der eine einfache Textbearbeitung in einem vereinfachten Inline-Editor sowie ein Vollbildformat ermöglicht.

Das [Dialogfeld „Bearbeiten“](#edit-dialog) verfügt über eine Inline-Bearbeitung mit eingeschränkten Optionen, während im Vollbildbearbeitungsdialogfeld alle Funktionen verfügbar sind. Mithilfe des [Dialogfelds „Design“](#design-dialog) können Textformatierungsoptionen wie Überschriften, Sonderzeichen und Absatzstile für die Vorlage für den Inhaltsautor konfiguriert werden.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Textkomponente ist v2, die mit Version 2.0.0 der Kernkomponenten im Januar 2018 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|---|
| v2 | Kompatibel | Kompatibel | Kompatibel |
| [v1](v1/text-v1.md) | Kompatibel | Kompatibel | - |

Weitere Informationen zu Kernkomponentenversionen und -freigaben finden Sie in den [Kernkomponentenversionen](/help/versions.md).

## Musterkomponentenausgabe {#sample-component-output}

Um die Textkomponente sowie Beispiele für die Konfigurationsoptionen sowie HTML- und JSON-Ausgaben zu erhalten, besuchen Sie die [Komponentenbibliothek](https://adobe.com/go/aem_cmp_library_text_de).

### Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur Textkomponente [finden Sie auf GitHub](https://adobe.com/go/aem_cmp_tech_text_v2_de).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Die Textkomponente und der Rich-Text-Editor {#the-text-component-and-the-rich-text-editor}

Die Textkomponente der Kernkomponenten nutzt den AEM-Rich-Text-Editor (RTE). Der Rich-Text-Editor (RTE) bietet Inhaltsautoren eine große Bandbreite an Funktionen zum Bearbeiten von ihren Textinhalten. Der RTE ist in seiner Konfiguration sehr flexibel und bietet eine Reihe von Optionen. Weitere Informationen dazu, wie der RTE konfiguriert werden kann, finden Sie in den Artikeln [Konfigurieren des Rich-Text-Editors](https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/implementing/configuring-and-extending/rich-text-editor.html) und [Konfigurieren der Plug-ins für Rich-Text-Editor](https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/implementing/configuring-and-extending/configure-rich-text-editor-plug-ins.html).

Der Rest dieses Artikels zeigt die Standardkonfiguration der Textkomponente der Kernkomponenten mit der vordefinierten RTE-Konfiguration.

>[!NOTE]
>
>In der Textkomponente sind nur Optionen verfügbar, die durch die [Benutzeroberflächenkonfigurationen des RTE](https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/implementing/configuring-and-extending/configure-rich-text-editor-plug-ins.html) aktiviert sind.

## Dialogfeld „Bearbeiten“ {#edit-dialog}

Das Dialogfeld „Bearbeiten“ bietet die standardmäßigen Rich-Text-Formatierungswerkzeuge, die ein Benutzer wahrscheinlich erwarten würde, um Text zu verfassen.

![Dialogfeld „Bearbeiten“ der Textkomponente](/help/assets/text-edit.png)

### Fett

![Symbol „Fett“](/help/assets/text-bold.png)

Wird verwendet, um eine fette Formatierung auf den ausgewählten Text anzuwenden oder den nach dem Cursor eingegebenen Text fett zu formatieren.

**Strg+B** kann als Tastaturbefehl verwendet werden.

### Kursiv

![Symbol „Kursiv“](/help/assets/text-italic.png)

Wird verwendet, um eine kursive Formatierung auf den ausgewählten Text anzuwenden oder nach dem Cursor eingegebenen Text kursiv zu formatieren.

**Strg+I** kann als Tastaturbefehl verwendet werden.

### Unterstrichen

![Symbol „Unterstrichen“](/help/assets/text-underline.png)

Wird verwendet, um eine unterstrichene Formatierung auf den ausgewählten Text anzuwenden oder Text, der nach dem Cursor eingegeben wird, zu unterstreichen.

**Strg+U** kann als Tastaturbefehl verwendet werden.

### Tiefgestellt

![Symbol „Tiefgestellt“](/help/assets/text-subscript.png)

Wird verwendet, um ausgewählten Text oder Text, der nach dem Cursor eingegeben wird, als tiefgestellt zu formatieren.

### Hochgestellt

![Symbol „Hochgestellt“](/help/assets/text-superscript.png)

Wird verwendet, um ausgewählten Text oder Text, der nach dem Cursor eingegeben wird, als hochgestellt zu formatieren.

### Als Text einfügen

![Symbol „Als Text einfügen“](/help/assets/text-paste-text.png)

Fügt einen kopierten Text als normalen Text ohne Formatierung ein.

Wenn Sie diese Option wählen, wird ein Fenster geöffnet, in dem der Text als normaler Text ohne Formatierung eingefügt werden kann, bevor er in den Text eingefügt wird. Akzeptieren durch Tippen oder Klicken auf das Häkchen, abbrechen durch Tippen oder Klicken auf das x.

![Beispiel für „Als Text einfügen“](/help/assets/text-paste-text-example.png)

### Aus Word einfügen

![Symbol „Aus Word einfügen“](/help/assets/text-paste-word.png)

Wenn Sie diese Option wählen, wird ein Fenster geöffnet, in dem der formatierte Text als Vorschau eingefügt werden kann, bevor er in den Text eingefügt wird. Akzeptieren durch Tippen oder Klicken auf das Häkchen, abbrechen durch Tippen oder Klicken auf das x.

![Beispiel für „Aus Word einfügen“](/help/assets/text-paste-word-example.png)

### Hyperlink

![Symbol „Hyperlink“](/help/assets/text-hyperlink.png)

Mit dieser Option können Sie den ausgewählten Text in einen Hyperlink konvertieren oder einen bereits definierten Link ändern. Diese Option ist nur aktiv, wenn bereits Text ausgewählt ist, und öffnet ein Fenster mit zusätzlichen Optionen zum Festlegen des Links.

![Beispiel für „Hyperlink“](/help/assets/text-hyperlink-example.png)

* Geben Sie den Pfad ein.
   * Wählen Sie im Dialogfeld „Auswahl öffnen“ einen Pfad in AEM aus.
   * Wenn der Link in AEM nicht angezeigt wird, geben Sie die absolute URL ein.
      * Nicht-absolute Pfade werden als relativ zu AEM interpretiert.
* Alternativen beschreibenden Text für den Link eingeben
* Linkverhalten auswählen
   * Target
   * Selbe Registerkarte
   * Neue Registerkarte
   * Übergeordneter Frame
   * Top-Frame

   Tippen oder klicken Sie auf das Häkchen, um den Link anzuwenden, oder auf das x um abzubrechen.

### Verknüpfung aufheben

![Symbol „Verknüpfung aufheben“](/help/assets/text-unlink.png)

Mit dieser Option können Sie einen bereits auf den ausgewählten Text angewendeten Link entfernen. Diese Option ist nur aktiv, wenn bereits ein Link ausgewählt ist.

### Suchen

![Symbol „Suchen“](/help/assets/text-find.png)

Verwenden Sie diese Option, um den Text nach dem Vorkommen einer angegebenen Textzeichenfolge zu durchsuchen. Wenn Sie diese Option auswählen, wird ein Fenster zum Festlegen der Suchoptionen geöffnet.

![Beispiel für „Suchen“](/help/assets/text-find-example.png)

Geben Sie den Text ein, nach dem Sie suchen möchten, und tippen oder klicken Sie auf **Suchen**, um die Suche zu starten. Tippen Sie auf das x, um abzubrechen.
Wenn Sie eine genaue Übereinstimmung der Groß- und Kleinschreibung möchten, wählen Sie die Option **Groß-/Kleinschreibung berücksichtigen**, bevor Sie die Suche starten.
Wenn eine Übereinstimmung gefunden wird, wird sie hervorgehoben und das Suchdialogfeld wird abgeblendet. Tippen oder klicken Sie im abgeblendeten Dialogfeld erneut auf die Schaltfläche **Suchen**, um nach dem nächsten Vorkommen zu suchen.

![Beispiel für mittels „Suchen“ gefundenen Text](/help/assets/text-find-example-found.png)

Wenn keine weiteren Vorkommen gefunden werden, wird eine Meldung angezeigt und die Suche wird am Anfang des Texts neu gestartet.

![Beispiel für „Suchen“ mit keinen weiteren Vorkommen](/help/assets/text-find-example-found-end.png)

### Ersetzen

![Symbol „Ersetzen“](/help/assets/text-replace.png)

Verwenden Sie diese Option, um den Text nach dem Vorkommen einer angegebenen Textzeichenfolge zu durchsuchen und die Übereinstimmungen durch eine andere Zeichenfolge zu ersetzen. Wenn Sie diese Option auswählen, wird ein Fenster zum Festlegen der Optionen für Suchen und Ersetzen geöffnet.

![Beispiel für „Ersetzen“](/help/assets/text-replace-example.png)

Geben Sie den Text ein, für den Sie eine Suche durchführen möchten, sowie den Text, durch den er ersetzt werden soll.

* Tippen oder klicken Sie auf **Suchen**, um mit der Suche zu beginnen. Klicken oder tippen Sie auf das x, um abzubrechen.
* Wenn Sie eine genaue Übereinstimmung der Groß- und Kleinschreibung möchten, wählen Sie die Option **Groß-/Kleinschreibung berücksichtigen**, bevor Sie die Suche starten.
* Wählen Sie **Alle ersetzen** aus, um alle Vorkommen des Texts gleichzeitig zu ersetzen.

Wenn eine Übereinstimmung gefunden wird, wird sie hervorgehoben und das Suchdialogfeld wird abgeblendet. Klicken Sie erneut im abgeblendeten Dialogfeld auf die Schaltfläche **Suchen**, um nach dem nächsten Vorkommen zu suchen, oder klicken Sie auf **Ersetzen**, um den markierten, übereinstimmenden Text zu ersetzen. Beachten Sie, dass die Schaltfläche **Ersetzen** nur aktiv ist, nachdem der Suchtext gefunden wurde.

Das Dialogfeld „Suchen und ersetzen“ wird transparent, wenn auf „Suchen“ geklickt wird, und undurchsichtig, wenn auf „Ersetzen“ geklickt wird. Dadurch kann der Autor den Text überprüfen, den der Autor ersetzen wird.

>[!NOTE]
>
>Bei Verwendung der Funktion zum Ersetzen sollte die Zeichenfolge zum Ersetzen gleichzeitig mit der Suchzeichenfolge eingegeben werden. Sie können jedoch weiterhin auf „Suchen“ klicken, um nach der Zeichenfolge zu suchen, bevor Sie sie ersetzen. Wenn die Zeichenfolge zum Ersetzen eingegeben wird, nachdem auf „Suchen“ geklickt wurde, wird die Suche auf den Anfang des Textes zurückgesetzt.


### Text linksbündig ausrichten

![Symbol „Linksbündig ausrichten“](/help/assets/text-left.png)

Wird verwendet, um den Text am linken Rand auszurichten.

### Text zentrieren

![Symbol „Text zentrieren“](/help/assets/text-center.png)

Wird zum Zentrieren des Texts verwendet.

### Text rechtsbündig ausrichten

![Symbol „Rechtsbündig ausrichten“](/help/assets/text-right.png)

Wird verwendet, um den Text am rechten Rand auszurichten.

### Aufzählungszeichen

![Symbol „Aufzählungszeichen“](/help/assets/text-bullet.png)

Wird verwendet, um den ausgewählten Text als Liste mit Aufzählungszeichen zu formatieren oder eine Liste mit Aufzählungszeichen nach dem Cursor einzufügen.

Um eine Liste mit Aufzählungszeichen zu beenden, tippen oder klicken Sie erneut auf die Schaltfläche **Aufzählung** oder geben Sie zwei Zeilenumbrüche hintereinander ein.

### Nummerierung

![Symbol „Nummerierung“](/help/assets/text-numbered.png)

Wird verwendet, um den ausgewählten Text als nummerierte Liste zu formatieren oder eine nummerierte Liste nach dem Cursor einzufügen.

Um eine nummerierte Liste zu beenden, tippen oder klicken Sie erneut auf die Schaltfläche **Nummeriert** oder geben Sie zwei Zeilenumbrüche hintereinander ein.

### Ausrücken

![Symbol „Ausrücken“](/help/assets/text-outdent.png)

Wird verwendet, um den Einzug des ausgewählten Texts oder des nach dem Cursor eingegebenen Texts zu verringern.

Nur aktiv, wenn der ausgewählte Text bzw. die ausgewählte Position bereits eingerückt ist.

### Einzug

![Symbol „Einzug“](/help/assets/text-outdent.png)

Wird verwendet, um den Einzug des ausgewählten Texts oder des nach dem Cursor eingegebenen Textes zu erhöhen.

### Tabelle

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
      * Oder es sollte keine Kopfzeile verwendet werden.
* **Beschriftung** - Beschriftung der Tabelle

### Rechtschreibprüfung

![Symbol „Rechtschreibprüfung“](/help/assets/text-spellcheck.png)

Wird verwendet, um die Rechtschreibung des Textinhalts zu überprüfen. Mögliche Rechtschreibfehler sind durch gestrichelte rote Linien unterstrichen.

Weitere Details zur Rechtschreibprüfung und zum Anpassen von Rechtschreibprüfungswörterbüchern finden Sie im Dokument [Konfigurieren der Plug-ins für Rich-Text-Editor](https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/implementing/configuring-and-extending/configure-rich-text-editor-plug-ins.html).

### Sonderzeichen {#special-characters}

![Symbol „Sonderzeichen“](/help/assets/text-special-characters.png)

Wird verwendet, um Sonderzeichen in den Text einzufügen. Wenn Sie diese Option auswählen, wird ein Fenster geöffnet, in dem die verfügbaren Zeichen angezeigt werden.

![Beispiel für „Sonderzeichen“](/help/assets/text-special-characters-example.png)

Tippen oder klicken Sie auf das gewünschte Zeichen, um es nach dem Cursor in den Text einzufügen. Es können mehrere Zeichen eingefügt werden. Tippen oder klicken Sie auf das x, um das Auswahlfenster zu schließen.

### Quellenbearbeitung

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

### Absatzformat

![Symbol „Absatzformat“](/help/assets/text-paragraph.png)

Wird verwendet, um Absatzformatierung auf den ausgewählten Text anzuwenden oder auf Text, der nach dem Cursor eingefügt wird. Durch Auswahl dieser Optionen wird eine Dropdown-Liste geöffnet, in der das Absatzformat ausgewählt ist.

![Beispiel für „Absatzformat“](/help/assets/text-paragraph-example.png)

### Inline-Bearbeitung {#in-line-editing}

Die Textkomponente kann auch inline bearbeitet werden, aufgrund von Platzbeschränkungen sind jedoch nicht alle Formatierungsoptionen inline verfügbar. Um alle Optionen anzuzeigen, wechseln Sie zum Vollbildmodus.

![Beispiel für die Inline-Bearbeitung](/help/assets/text-edit-inline-example.png)

### Einstellung und ID {#setting-id}

Diese Option dient zur Kontrolle der eindeutigen Kennung der Komponente in der HTML-Datei und auf der [Datenschicht](/help/developing/data-layer/overview.md).

* Wenn Sie das Feld leer lassen, wird automatisch eine eindeutige ID generiert, die Sie über die resultierende Seite finden.
* Sofern eine ID angegeben wird, ist vom Autor sicherzustellen, dass diese eindeutig ist.
* Änderungen der ID können sich auf das CSS-, JS- und Datenschicht-Tracking auswirken.

## Dialogfeld „Design“ {#design-dialog}

Im Dialogfeld „Design“ kann der Vorlagenautor festlegen, welche Textformatierungsoptionen den Inhaltsautoren zur Verfügung stehen.

### Registerkarte „Plug-ins“ {#plugins-tab}

Über die Registerkarte „Plug-ins“ können verschiedene Textformatierungsoptionen aktiviert und deaktiviert werden, die den Inhaltsautoren zur Verfügung stehen sollen.

### Funktionen {#features}

![„Funktionen“ im Dialogfeld „Design“](/help/assets/text-design-features.png)

Die folgenden Funktionen können für die Komponente aktiviert oder deaktiviert werden.

* Unformatierten Text einfügen
* Aus Word einfügen
* Suchen und Ersetzen
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
* Um die Reihenfolge der Formate zu ändern, tippen oder klicken Sie und ziehen Sie die Griffe.

### Sonderzeichen {#configuring-special-characters}

![„Sonderzeichen“ im Dialogfeld „Design“](/help/assets/text-design-special-characters.png)

Die Option zum Einfügen von Sonderzeichen kann für die Komponente aktiviert oder deaktiviert werden. Bei Aktivierung können die zulässigen Zeichen definiert werden.

* Tippen oder klicken Sie auf die Schaltfläche **Hinzufügen**, um ein neues Zeichen einzufügen.
* Geben Sie den HTML-Code des Zeichens und eine Beschreibung ein, die im Dialogfeld „Bearbeiten“ angezeigt wird.
* Um ein Zeichen zu entfernen, tippen oder klicken Sie auf die Schaltfläche **Löschen**.
* Um die Reihenfolge der Zeichen zu ändern, tippen oder klicken Sie und ziehen Sie die Griffe.

## Registerkarte „Stile“ {#styles-tab}

Die Textkomponente unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).

## Adobe Client-Datenschicht {#data-layer}

Die Textkomponente unterstützt die [Adobe Client-Datenschicht](/help/developing/data-layer/overview.md).
