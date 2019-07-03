---
title: Textkomponente
seo-title: Textkomponente
description: Die Textkomponente ist eine Komponente zur Bearbeitung und Zusammensetzung von Rich-Texten, die eine direkte Bearbeitung ermöglicht.
seo-description: Die Textkomponente ist eine Komponente zur Bearbeitung und Zusammensetzung von Rich-Texten, die eine direkte Bearbeitung ermöglicht.
uuid: 5f8eee8f-7317-4712-a77f-e34e8a024187
contentOwner: Benutzer
content-type: Referenz
topic-tags: Kernkomponenten
discoiquuid: 9a290584-565e-4392-999c-999ee4a93da1
translation-type: tm+mt
source-git-commit: eef608fb06001485aa2c2c0b574af412ed7f15a4

---


# Textkomponente{#text-component}

Die Kernkomponente Textkomponente ist eine Komponente zur Bearbeitung und Zusammensetzung von Rich-Texten, die eine direkte Bearbeitung ermöglicht.

## Nutzung {#usage}

Die Textkomponente bietet einen robusten Rich-Text-Editor, der eine einfache Textbearbeitung in einem vereinfachten Inline-Editor sowie ein Vollbildformat ermöglicht.

Das [Dialogfeld „Bearbeiten“](#edit-dialog) verfügt über eine Inline-Bearbeitung mit eingeschränkten Optionen, während im Vollbildbearbeitungsdialogfeld alle Funktionen verfügbar sind. Mithilfe des [Dialogfelds „Design“](#design-dialog) können Textformatierungsoptionen wie Überschriften, Sonderzeichen und Absatzstile für die Vorlage für den Inhaltsautor konfiguriert werden.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Textkomponente ist v2, die mit Version 2.0.0 der Kernkomponenten im Januar 2018 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|---|---|---|---|
| v2 | Kompatibel | Kompatibel | Kompatibel |
| [v1](text-v1.md) | Kompatibel | Kompatibel | Kompatibel |

Weitere Informationen zu Kernkomponentenversionen und -freigaben finden Sie in den [Kernkomponentenversionen](versions.md).

## Musterkomponentenausgabe {#sample-component-output}

To experience the Text Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](http://opensource.adobe.com/aem-core-wcm-components/library/text.html).

### Technische Details {#technical-details}

The latest technical documentation about the Text Component [can be found on GitHub](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/text/v2/text).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](developing.md).

## Die Textkomponente und der Rich-Text-Editor {#the-text-component-and-the-rich-text-editor}

Die Textkomponente der Kernkomponenten nutzt den AEM-Rich-Text-Editor (RTE). Der Rich-Text-Editor (RTE) bietet Inhaltsautoren eine große Bandbreite an Funktionen zum Bearbeiten von ihren Textinhalten. Der RTE ist in seiner Konfiguration sehr flexibel und bietet eine Reihe von Optionen. Further details about how the RTE can be configured can be found in the articles [Configure the Rich Text Editor](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/rich-text-editor.html) and [Configure the Rich Text Editor plug-ins](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/configure-rich-text-editor-plug-ins.html).

Der Rest dieses Artikels zeigt die Standardkonfiguration der Textkomponente der Kernkomponenten mit der vordefinierten RTE-Konfiguration.

>[!NOTE]
>
>Only options enabled by [UI configurations of the RTE](https://chl-author-preview.corp.adobe.com/content/help/en/experience-manager/6-5/sites/administering/using/rich-text-editor.html) are available by in the Text Component.

## Dialogfeld „Bearbeiten“ {#edit-dialog}

Das Dialogfeld „Bearbeiten“ bietet die standardmäßigen Rich-Text-Formatierungswerkzeuge, die ein Benutzer wahrscheinlich erwarten würde, um Text zu verfassen.

![](assets/screen_shot_2018-01-11at143025.png)

### Fett

![](assets/screen_shot_2018-01-11at125602.png)

Wird verwendet, um eine fette Formatierung auf den ausgewählten Text anzuwenden oder den nach dem Cursor eingegebenen Text fett zu formatieren.

**Strg+B** kann als Tastaturbefehl verwendet werden.

### Kursiv

![](assets/screen_shot_2018-01-11at125609.png)

Wird verwendet, um eine kursive Formatierung auf den ausgewählten Text anzuwenden oder nach dem Cursor eingegebenen Text kursiv zu formatieren.

**Strg+I** kann als Tastaturbefehl verwendet werden.

### Unterstrichen

![](assets/screen_shot_2018-01-11at125615.png)

Wird verwendet, um eine unterstrichene Formatierung auf den ausgewählten Text anzuwenden oder Text, der nach dem Cursor eingegeben wird, zu unterstreichen.

**Strg+U** kann als Tastaturbefehl verwendet werden.

### Tiefgestellt

![](assets/screen_shot_2018-01-11at125703.png)

Wird verwendet, um ausgewählten Text oder Text, der nach dem Cursor eingegeben wird, als tiefgestellt zu formatieren.

### Hochgestellt

![](assets/screen_shot_2018-01-11at125708.png)

Wird verwendet, um ausgewählten Text oder Text, der nach dem Cursor eingegeben wird, als hochgestellt zu formatieren.

### Als Text einfügen

![](assets/screen_shot_2018-01-11at125713.png)

Fügt einen kopierten Text als normalen Text ohne Formatierung ein.

Wenn Sie diese Option wählen, wird ein Fenster geöffnet, in dem der Text als normaler Text ohne Formatierung eingefügt werden kann, bevor er in den Text eingefügt wird. Akzeptieren durch Tippen oder Klicken auf das Häkchen, abbrechen durch Tippen oder Klicken auf das x.

![](assets/screen_shot_2018-01-11at143234.png)

### Aus Word einfügen

![](assets/screen_shot_2018-01-11at125717.png)

Wenn Sie diese Option wählen, wird ein Fenster geöffnet, in dem der formatierte Text als Vorschau eingefügt werden kann, bevor er in den Text eingefügt wird. Akzeptieren durch Tippen oder Klicken auf das Häkchen, abbrechen durch Tippen oder Klicken auf das x.

![](assets/screen_shot_2018-01-11at143250.png)

### Hyperlink

![](assets/screen_shot_2018-01-11at125839.png)

Mit dieser Option können Sie den ausgewählten Text in einen Hyperlink konvertieren oder einen bereits definierten Link ändern. Diese Option ist nur aktiv, wenn bereits Text ausgewählt ist, und öffnet ein Fenster mit zusätzlichen Optionen zum Festlegen des Links.

![](assets/screen_shot_2018-01-11at130003.png)

* Adresse eingeben
   * Wählen Sie im Dialogfeld „Auswahl öffnen“ einen Pfad in AEM aus.
   * Wenn sich der Link nicht in AEM befindet, geben Sie die absolute URL ein (nicht absolute Pfade werden als relativ zu AEM interpretiert)
* Alternativen beschreibenden Text für den Link eingeben
* Linkverhalten auswählen
   * Target
   * Selbe Registerkarte
   * Neue Registerkarte
   * Übergeordneter Frame
   * Top-Frame
   Tippen oder klicken Sie auf das Häkchen, um den Link anzuwenden, oder auf das x um abzubrechen.

### Verknüpfung aufheben

![](assets/screen_shot_2018-01-11at125901.png)

Mit dieser Option können Sie einen bereits auf den ausgewählten Text angewendeten Link entfernen. Diese Option ist nur aktiv, wenn bereits ein Link ausgewählt ist.

### Suchen

![](assets/screen_shot_2018-01-11at125906.png)

Verwenden Sie diese Option, um den Text nach dem Vorkommen einer angegebenen Textzeichenfolge zu durchsuchen. Wenn Sie diese Option auswählen, wird ein Fenster zum Festlegen der Suchoptionen geöffnet.

![](assets/screen_shot_2018-01-11at130107.png)

Geben Sie den Text ein, nach dem Sie suchen möchten, und tippen oder klicken Sie auf **Suchen**, um die Suche zu starten. Tippen Sie auf das x, um abzubrechen.
Wenn Sie eine genaue Übereinstimmung der Groß- und Kleinschreibung möchten, wählen Sie die Option **Groß-/Kleinschreibung berücksichtigen**, bevor Sie die Suche starten.
Wenn eine Übereinstimmung gefunden wird, wird sie hervorgehoben und das Suchdialogfeld wird abgeblendet. Tippen oder klicken Sie im abgeblendeten Dialogfeld erneut auf die Schaltfläche **Suchen**, um nach dem nächsten Vorkommen zu suchen.

![](assets/screen_shot_2018-01-11at130145.png)

Wenn keine weiteren Vorkommen gefunden werden, wird eine Meldung angezeigt und die Suche wird am Anfang des Texts neu gestartet.

![](assets/screen_shot_2018-01-11at130241.png)

### Ersetzen

![](assets/screen_shot_2018-01-11at125910.png)

Verwenden Sie diese Option, um den Text nach dem Vorkommen einer angegebenen Textzeichenfolge zu durchsuchen und die Übereinstimmungen durch eine andere Zeichenfolge zu ersetzen. Wenn Sie diese Option auswählen, wird ein Fenster zum Festlegen der Optionen für Suchen und Ersetzen geöffnet.

![](assets/screen_shot_2018-01-11at130441.png)

Geben Sie den Text ein, für den Sie eine Suche durchführen möchten, sowie den Text, durch den er ersetzt werden soll.

Tippen oder klicken Sie auf **Suchen**, um mit der Suche zu beginnen. Klicken oder tippen Sie auf das x, um abzubrechen.

Wenn Sie eine genaue Übereinstimmung der Groß- und Kleinschreibung möchten, wählen Sie die Option **Groß-/Kleinschreibung berücksichtigen**, bevor Sie die Suche starten.

Wenn eine Übereinstimmung gefunden wird, wird sie hervorgehoben und das Suchdialogfeld wird abgeblendet. Klicken Sie erneut im abgeblendeten Dialogfeld auf die Schaltfläche **Suchen**, um nach dem nächsten Vorkommen zu suchen, oder klicken Sie auf **Ersetzen**, um den markierten, übereinstimmenden Text zu ersetzen. Beachten Sie, dass die Schaltfläche **Ersetzen** nur aktiv ist, nachdem der Suchtext gefunden wurde.

Wählen Sie **Alle ersetzen** aus, um alle Vorkommen des Texts gleichzeitig zu ersetzen.

### Text links ausrichten

![](assets/screen_shot_2018-01-11at142012.png)

Wird verwendet, um den Text am linken Rand auszurichten.

### Text zentrieren

![](assets/screen_shot_2018-01-11at142017.png)

Wird zum Zentrieren des Texts verwendet.

### Text rechts ausrichten

![](assets/screen_shot_2018-01-11at142021.png)

Wird verwendet, um den Text am rechten Rand auszurichten.

### Aufzählungszeichen

![](assets/screen_shot_2018-01-11at142025.png)

Wird verwendet, um den ausgewählten Text als Liste mit Aufzählungszeichen zu formatieren oder eine Liste mit Aufzählungszeichen nach dem Cursor einzufügen.

Um eine Liste mit Aufzählungszeichen zu beenden, tippen oder klicken Sie erneut auf die Schaltfläche **Aufzählung** oder geben Sie zwei Zeilenumbrüche hintereinander ein.

### Nummeriert

![](assets/screen_shot_2018-01-11at142030.png)

Wird verwendet, um den ausgewählten Text als nummerierte Liste zu formatieren oder eine nummerierte Liste nach dem Cursor einzufügen.

Um eine nummerierte Liste zu beenden, tippen oder klicken Sie erneut auf die Schaltfläche **Nummeriert** oder geben Sie zwei Zeilenumbrüche hintereinander ein.

### Ausrücken

![](assets/screen_shot_2018-01-11at141917.png)

Wird verwendet, um den Einzug des ausgewählten Texts oder des nach dem Cursor eingegebenen Texts zu verringern.

Nur aktiv, wenn der ausgewählte Text bzw. die ausgewählte Position bereits eingerückt ist.

### Einzug

![](assets/screen_shot_2018-01-11at141922.png)

Wird verwendet, um den Einzug des ausgewählten Texts oder des nach dem Cursor eingegebenen Textes zu erhöhen.

### Tabelle

![](assets/screen_shot_2018-01-11at141928.png)

Wird verwendet, um eine Tabelle in den Text einzufügen. Wenn Sie diese Option auswählen, wird ein Fenster zum Festlegen der Details der Tabelle geöffnet.

![](assets/screen_shot_2018-01-11at142405.png)

* **Spalten**
Die Anzahl der Spalten der Tabelle (erforderlich)
* **Zeilen**
Die Anzahl der Zeilen der Tabelle (erforderlich)
* **Breite**
Die Gesamtbreite der Tabelle
* **Höhe**
Die Gesamthöhe der Tabelle
* **Zellumrandung**
Der Abstand um den Zelleninhalt
* **Zellenabstand**
Der Abstand zwischen Zellen
* **Rand**
Die Stärke der Rahmenlinien der Tabelle
* Für die Kopfzeile der Tabelle:
   * Die erste Zeile sollte verwendet werden
   * Die erste Spalte sollte verwendet werden
   * Die erste Zeile und erste Spalte sollten verwendet werden
   * Oder es sollte keine Kopfzeile verwendet werden.
* **Beschriftung**
Die Beschriftung der Tabelle

### Rechtschreibprüfung

![](assets/screen_shot_2018-01-11at141935.png)

Wird verwendet, um die Rechtschreibung des Textinhalts zu überprüfen. Mögliche Rechtschreibfehler sind durch gestrichelte rote Linien unterstrichen.

Further details about spell checking and customizing spell check dictionaries can be found in the document [Configure the Rich Text Editor Plug-Ins](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/configure-rich-text-editor-plug-ins.html).

### Sonderzeichen {#special-characters}

![](assets/screen_shot_2018-01-11at142600.png)

Wird verwendet, um Sonderzeichen in den Text einzufügen. Wenn Sie diese Option auswählen, wird ein Fenster geöffnet, in dem die verfügbaren Zeichen angezeigt werden.

![](assets/screen_shot_2018-01-11at142635.png)

Tippen oder klicken Sie auf das gewünschte Zeichen, um es nach dem Cursor in den Text einzufügen. Es können mehrere Zeichen eingefügt werden. Tippen oder klicken Sie auf das x, um das Auswahlfenster zu schließen.

### Quellenbearbeitung

![](assets/screen_shot_2018-01-11at142746.png)

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

![](assets/screen_shot_2018-01-11at142752.png)

Wird verwendet, um Absatzformatierung auf den ausgewählten Text anzuwenden oder auf Text, der nach dem Cursor eingefügt wird. Durch Auswahl dieser Optionen wird eine Dropdown-Liste geöffnet, in der das Absatzformat ausgewählt ist.

![](assets/screen_shot_2018-01-11at142828.png)

Die Textkomponente kann auch inline bearbeitet werden, aufgrund von Platzbeschränkungen sind jedoch nicht alle Formatierungsoptionen inline verfügbar. Um alle Optionen anzuzeigen, wechseln Sie zum Vollbildmodus.

![](assets/screen_shot_2018-01-11at142921.png)

## Dialogfeld „Design“ {#design-dialog}

Im Dialogfeld „Design“ kann der Vorlagenautor festlegen, welche Textformatierungsoptionen den Inhaltsautoren zur Verfügung stehen.

### Registerkarte „Plug-ins“ {#plugins-tab}

Über die Registerkarte „Plug-ins“ können verschiedene Textformatierungsoptionen aktiviert und deaktiviert werden, die den Inhaltsautoren zur Verfügung stehen sollen.

### Funktionen {#features}

![](assets/chlimage_1-28.png)

Die folgenden Funktionen können für die Komponente aktiviert oder deaktiviert werden.

* Unformatierten Text einfügen
* Aus Word einfügen
* Suchen und Ersetzen
* Rechtschreibprüfung
* Quellbearbeitung

### Formatierung {#formatting}

![](assets/chlimage_1-29.png)

Die folgenden Formatierungsoptionen können für die Komponente aktiviert oder deaktiviert werden.

* Tabelle
* Listen
* Ausrichtung
* Fett, kursiv, unterstrichen
* Links
* Tiefgestellt/hochgestellt

### Absatzformate {#paragraph-styles}

![](assets/chlimage_1-30.png)

Absatzstile können für die Komponente aktiviert oder deaktiviert werden. Bei Aktivierung können die zulässigen Formate definiert werden.

* Tippen oder klicken Sie auf die Schaltfläche **Hinzufügen**, um einen neuen Stil einzufügen.
* Geben Sie den Code des Stils und eine Beschreibung ein, die im Dialogfeld „Bearbeiten“ angezeigt wird.
* Um einen Stil zu entfernen, tippen Sie auf die Schaltfläche **Löschen**.
* Um die Reihenfolge der Formate zu ändern, tippen oder klicken Sie und ziehen Sie die Griffe.

### Konfigurieren von Sonderzeichen {#configuring-special-characters}

![](assets/chlimage_1-31.png)

Die Option zum Einfügen von Sonderzeichen kann für die Komponente aktiviert oder deaktiviert werden. Bei Aktivierung können die zulässigen Zeichen definiert werden.

* Tippen oder klicken Sie auf die Schaltfläche **Hinzufügen**, um ein neues Zeichen einzufügen.
* Geben Sie den HTML-Code des Zeichens und eine Beschreibung ein, die im Dialogfeld „Bearbeiten“ angezeigt wird.
* Um ein Zeichen zu entfernen, tippen oder klicken Sie auf die Schaltfläche **Löschen**.
* Um die Reihenfolge der Zeichen zu ändern, tippen oder klicken Sie und ziehen Sie die Griffe.

## Registerkarte „Stile“ {#styles-tab}

Die Textkomponente unterstützt das AEM-[Stilsystem](authoring.md#component-styling).