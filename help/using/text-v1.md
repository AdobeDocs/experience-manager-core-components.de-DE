---
title: Textkomponente (v 1)
seo-title: Textkomponente (v 1)
description: 'null'
seo-description: Die Textkomponente ist eine Rich-Text-Bearbeitung und eine Komponente, die eine ersetzende Bearbeitung bietet.
uuid: b 787 ebac-fa 5-416 a-b 96 b -9 d 2 ee 85428 ec
content-type: Referenz
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-new
discoiquuid: d 5 e 37 dc 7-dfd 4-4 a 44-89 b 6-c 15651472 c 43
disttype: dist5
gnavtheme: light
groupsectionnavitems: keine
hidemerchandisingbar: inherit
hidepromocomponent: inherit
modalsize: 426x240
noindex: 'true'
index: n
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 1bbec9b1f109df88964dce051a58d111bf6cafaa

---


# Textkomponente (v 1){#text-component-v}

Die Textkomponente ist eine Rich-Text-Bearbeitung und eine Komponente, die eine ersetzende Bearbeitung bietet.

## Nutzung {#usage}

Die Textkomponente bietet einen robusten Rich-Text-Editor, der eine einfache Textbearbeitung in einem vereinfachten Online-Editor sowie ein Vollbildformat ermöglicht.

Das Dialogfeld [&quot;Bearbeiten&quot;](text-v1.md#main-pars_title) verfügt über eine integrierte Bearbeitung mit eingeschränkten Optionen, die im Vollbildbearbeitungsdialogfeld verfügbar sind. Mithilfe des [Designdialogfelds](text-v1.md#main-pars_title_1995166862)können Textformatierungsoptionen wie Überschriften, Sonderzeichen und Absatzstile für die Vorlage für den Inhaltsautor konfiguriert werden.

## Version und Kompatibilität {#version-and-compatibility}

In diesem Dokument wird die Version 1 der Textkomponente beschrieben, die ursprünglich mit Version 1.0.0 der Kernkomponenten mit AEM 6.3 eingeführt wurde.

In der folgenden Tabelle ist die Kompatibilität von v 1 der Textkomponente aufgeführt.

| AEM-Version | Textkomponente v 1 |
|--- |--- |
| 6.3 | Kompatibel |
| 6.4 | Kompatibel |

>[!CAUTION]
>
>In diesem Dokument wird v 1 der Textkomponente beschrieben.
>
>Weitere Informationen zur aktuellen Version der Textkomponente finden Sie im [Dokument Text Component](text.md) .

## Musterkomponentenausgabe {#sample-component-output}

Nachfolgend finden Sie ein Beispiel aus [We. Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

### Screenshot {#screenshot}

![](assets/chlimage_1-27.png)

### HTML {#html}

```
<div class="cmp cmp-text aem-GridColumn aem-GridColumn--default--12">
<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer porttitor ante a tortor volutpat maximus. Donec eu porta eros. Aenean sit amet eleifend arcu, eu vestibulum magna. Fusce eget nisi tincidunt, tristique felis quis, tincidunt est. Aliquam consequat aliquam quam non eleifend. Phasellus ut magna luctus, aliquam risus eget, fermentum augue. Aliquam lobortis accumsan magna, quis efficitur enim dictum eu. Pellentesque iaculis felis eget felis commodo, non euismod dolor euismod. Quisque nec arcu rutrum, mollis tortor non, sollicitudin odio. Sed dictum nulla mauris, eu pretium dui vulputate a. Maecenas lacus massa, egestas vitae tincidunt eu, interdum et magna. Lorem ipsum dolor sit amet, consectetur adipiscing elit. In eleifend ex lacus, in consectetur nunc interdum et. Donec interdum mi vitae dolor pretium mattis. In quis arcu sapien. Phasellus at metus vitae nisi tincidunt varius.<br />
</p>
</div>
```

### JSON {#json}

```
"text": {
              "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
              "text": "<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer porttitor ante a tortor volutpat maximus. Donec eu porta eros. Aenean sit amet eleifend arcu, eu vestibulum magna. Fusce eget nisi tincidunt, tristique felis quis, tincidunt est. Aliquam consequat aliquam quam non eleifend. Phasellus ut magna luctus, aliquam risus eget, fermentum augue. Aliquam lobortis accumsan magna, quis efficitur enim dictum eu. Pellentesque iaculis felis eget felis commodo, non euismod dolor euismod. Quisque nec arcu rutrum, mollis tortor non, sollicitudin odio. Sed dictum nulla mauris, eu pretium dui vulputate a. Maecenas lacus massa, egestas vitae tincidunt eu, interdum et magna. Lorem ipsum dolor sit amet, consectetur adipiscing elit. In eleifend ex lacus, in consectetur nunc interdum et. Donec interdum mi vitae dolor pretium mattis. In quis arcu sapien. Phasellus at metus vitae nisi tincidunt varius.</p>\n",
              "richText": true,
              ":type": "weretail/components/content/text"
            }
```

>[!NOTE]
>
>Für JSON-Exporte aus den Core-Komponenten ist Version 1.1.0 der Kernkomponenten erforderlich. Weitere Informationen finden Sie in den [Kompatibilitätsinformationen für Kernkomponenten v 1](versions.md#main-pars_title_236368006) .

## Dialogfeld bearbeiten {#edit-dialog}

Das Dialogfeld &quot;Bearbeiten&quot; bietet die standardmäßigen Rich-Text-Formatierungswerkzeuge, die ein Benutzer wahrscheinlich entwerfen würde.

![](assets/chlimage_1-52.png)

* Fett

   ![](assets/chlimage_1-53.png)

   Wird verwendet, um die fett formatierte Formatierung auf den ausgewählten Text anzuwenden oder den nach dem Cursor eingegebenen Text fett formatiert zu formatieren.

   **Strg + B** kann als Tastaturbefehl verwendet werden.

* Kursiv

   ![](assets/chlimage_1-54.png)

   Wird verwendet, um kuratierte Formatierungen auf den ausgewählten Text anzuwenden oder nach dem Cursor eingegebene Text kursiv zu formatieren.

   **Strg + I** kann als Tastaturbefehl verwendet werden.

* Unterstrichen

   ![](assets/chlimage_1-55.png)

   Wird verwendet, um unterstrichene Formatierungen auf den ausgewählten Text oder Unterstriche nach dem Cursor anzuwenden.

   **Strg + U** kann als Tastaturbefehl verwendet werden.

* Tiefgestellt

   ![](assets/chlimage_1-56.png)

   Wird verwendet, um ausgewählten Text oder Text, der nach dem Cursor eingegeben wurde, als tiefgestellt zu formatieren.

* Hochgestellt

   ![](assets/chlimage_1-57.png)

   Wird verwendet, um ausgewählten Text oder Text nach dem Cursor als Hochgestellte zu formatieren.

* Als Text einfügen

   ![](assets/chlimage_1-58.png)

   Fügt einen kopierten Text ohne Formatierung als normaler Text ein.

   Wenn Sie diese Option wählen, wird ein Fenster geöffnet, in dem der Text als normaler Text ohne Formatierung eingefügt werden kann, bevor er in den Text eingefügt wird. Akzeptieren Sie durch Tippen oder Klicken auf das Häkchen, Abbrechen durch Tippen oder Klicken auf x.

   ![](assets/chlimage_1-59.png)

* Aus Word einfügen

   ![](assets/chlimage_1-60.png)

   Wenn Sie diese Option wählen, wird ein Fenster geöffnet, in dem der Text als Vorschau eingefügt werden kann, bevor er in den Text eingefügt wird. Akzeptieren Sie durch Tippen oder Klicken auf das Häkchen, Abbrechen durch Tippen oder Klicken auf x.

   ![](assets/chlimage_1-61.png)

* Hyperlink

   ![](assets/chlimage_1-62.png)

   Mit dieser Option können Sie den ausgewählten Text in einen Hyperlink konvertieren oder einen bereits definierten Link ändern. Diese Option ist nur aktiv, wenn Text bereits ausgewählt ist und ein Fenster mit zusätzlichen Optionen zum Festlegen des Links geöffnet wird.

   ![](assets/chlimage_1-63.png)

   * Ort eingeben

      * Wählen Sie im Dialogfeld &quot;Auswahl öffnen&quot; einen Pfad in AEM aus.
      * Wenn sich der Link nicht in AEM befindet, geben Sie die absolute URL ein (nicht absolute Pfade werden als relativ zu AEM interpretiert)
   * Alternativen beschreibenden Text für den Link eingeben
   * Linkverhalten auswählen

      * Target
      * Selbe Registerkarte
      * Neue Registerkarte
      * Übergeordneter Frame
      * Top-Frame
   Tippen Sie auf das Häkchen oder klicken Sie auf das Häkchen, um den Link oder X abzubrechen.

* Verknüpfung aufheben

   ![](assets/chlimage_1-64.png)

   Mit dieser Option können Sie einen bereits auf den ausgewählten Text angewendeten Link entfernen. Diese Option ist nur aktiv, wenn bereits ein Link ausgewählt ist.

* Suchen Sie nach

   ![](assets/chlimage_1-65.png)

   Verwenden Sie diese Option, um den Text für Vorkommen einer angegebenen Textzeichenfolge zu suchen. Wenn Sie diese Option auswählen, wird ein Fenster zum Festlegen der Suchoptionen geöffnet.

   ![](assets/chlimage_1-66.png)

   Geben Sie den Text ein, für den Sie suchen möchten, tippen Sie auf &quot;Suchen&quot; oder klicken **Sie auf&quot; Suchen** &quot; , um die Suche zu starten. Tippen Sie auf das X, um es abzubrechen.

   Wenn Sie eine genaue Übereinstimmung mit dem Fall durchführen möchten, wählen Sie die Option **&quot;Groß-/Kleinschreibung berücksichtigen&quot; ,** bevor Sie die Suche starten.

   Wenn eine Übereinstimmung gefunden wird, wird sie hervorgehoben und das Suchdialogfeld ist abgeblendet. Tippen Sie im abgeblendeten Dialogfeld erneut auf **die Schaltfläche &quot;Suchen** &quot; , um nach dem nächsten Vorkommen zu suchen.

   ![](assets/chlimage_1-67.png)

   Wenn keine weiteren Vorkommen gefunden werden, wird eine Meldung angezeigt und die Suche wird am Anfang des Textes neu gestartet.

   ![](assets/chlimage_1-68.png)

* Replace

   ![](assets/chlimage_1-69.png)

   Verwenden Sie diese Option, um den Text für Vorkommen einer angegebenen Textzeichenfolge zu suchen und die Übereinstimmungen durch eine andere Zeichenfolge zu ersetzen. Wenn Sie diese Option auswählen, wird ein Fenster zum Festlegen der Optionen für Suchen und Ersetzen geöffnet.

   ![](assets/chlimage_1-70.png)

   Geben Sie den Text ein, für den Sie eine Suche durchführen möchten, sowie den Text, mit dem sie ersetzt werden soll.

   Tippen oder klicken **Sie auf Suchen** , um mit der Suche zu beginnen. Klicken oder tippen Sie auf das X, um es abzubrechen.

   Wenn Sie eine genaue Übereinstimmung mit dem Fall durchführen möchten, wählen Sie die Option **&quot;Groß-/Kleinschreibung berücksichtigen&quot; ,** bevor Sie die Suche starten.

   Wenn eine Übereinstimmung gefunden wird, wird sie hervorgehoben und das Suchdialogfeld ist abgeblendet. Klicken Sie erneut im abgeblendeten Dialogfeld auf **die Schaltfläche &quot;Suchen** «, um nach dem nächsten Vorkommen zu suchen, oder klicken Sie auf **&quot; Ersetzen** &quot; , um den markierten, übereinstimmenden Text zu ersetzen. Beachten Sie, **dass die Schaltfläche &quot;Ersetzen** &quot; nur aktiv ist, nachdem eine Übereinstimmung hergestellt wurde.

   Wählen Sie Alle **ersetzen** aus, um alle Vorkommen des Textes gleichzeitig zu ersetzen.

* Text links ausrichten

   ![](assets/chlimage_1-71.png)

   Wird verwendet, um den Text am linken Rand auszurichten.

* Text zentrieren

   ![](assets/chlimage_1-72.png)

   Wird zum Zentrieren des Textes verwendet.

* Text rechts ausrichten

   ![](assets/chlimage_1-73.png)

   Wird verwendet, um den Text am rechten Rand auszurichten.

* Aufzählungszeichen

   ![](assets/chlimage_1-74.png)

   Wird verwendet, um den ausgewählten Text als Liste mit Aufzählungszeichen zu formatieren oder eine Liste mit Aufzählungszeichen nach dem Cursor einzufügen.

   Um eine Liste mit Aufzählungszeichen zu beenden, tippen oder klicken Sie erneut auf **die Aufzählungstaste** oder geben Sie zwei Wagenrückgaben ein.

* Nummeriert

   ![](assets/chlimage_1-75.png)

   Wird verwendet, um den ausgewählten Text als nummerierte Liste zu formatieren oder eine nummerierte Liste nach dem Cursor einzufügen.

   Um eine nummerierte Liste zu beenden, tippen oder klicken Sie erneut auf **die Nummerierungsschaltfläche** oder geben Sie zwei Wagenrückgaben ein.

* Ausrücken

   ![](assets/chlimage_1-76.png)

   Wird verwendet, um den Einzug des ausgewählten Textes oder der eingegebenen Text nach dem Cursor zu verringern.

   Nur aktiv, wenn der ausgewählte Text bzw. die ausgewählte Position bereits eingerückt ist.

* Einzug

   ![](assets/chlimage_1-77.png)

   Wird verwendet, um den Einzug des ausgewählten Textes oder der eingegebenen Text nach dem Cursor zu erhöhen.

* Tabelle

   ![](assets/chlimage_1-78.png)

   Wird verwendet, um eine Tabelle in den Text einzufügen. Wenn Sie diese Option auswählen, wird ein Fenster zum Festlegen der Details der Tabelle geöffnet.

   ![](assets/chlimage_1-79.png)

   * **Spalten** - Die Anzahl der Spalten der Tabelle (erforderlich)
   * **Zeilen** - Die Anzahl der Tabellenzeilen (erforderlich)
   * **Breite** - Die Breite der Tabelle
   * **Höhe** - Die Höhe der Tabelle
   * **Zellauffüllung**- Der Abstand um den Zellinhalt
   * **Zellenabstand** - Der Abstand zwischen Zellen
   * **Rand** - Die Stärke der Randlinien der Tabelle
   * Für die Kopfzeile der Tabelle:

      * Die erste Zeile sollte verwendet werden
      * Die erste Spalte sollte verwendet werden
      * Die erste Zeile und erste Spalte sollten verwendet werden
      * Es sollte auch keine Kopfzeile verwendet werden.
   * **Beschriftung** - Beschriftung der Tabelle


* Rechtschreibprüfung

   ![](assets/chlimage_1-80.png)

   Wird verwendet, um die Rechtschreibung des Textinhalts zu prüfen. Mögliche Rechtschreibfehler sind durch beschädigte rote Linien unterstrichen.

* Sonderzeichen

   ![](assets/chlimage_1-81.png)

   Wird verwendet, um Sonderzeichen in den Text einzufügen. Wenn Sie diese Option auswählen, wird ein Fenster geöffnet, in dem die verfügbaren Zeichen angezeigt werden.

   ![](assets/chlimage_1-82.png)

   Tippen oder klicken Sie auf das gewünschte Zeichen, um es nach dem Cursor in den Text einzufügen. Es können mehrere Zeichen eingefügt werden. Tippen oder klicken Sie auf das X, um das Auswahlfenster zu schließen.

* Quellenbearbeitung

   ![](assets/chlimage_1-83.png)

   Wird verwendet, um die HTML-Quelle des Texts anzuzeigen und zu ändern.

   Tippen oder klicken Sie auf das **Quellbearbeitungssymbol** , um den Inhalt des Textes aus der formatierten Ansicht zu ändern, um den rohen HTML anzuzeigen. In diesem Modus sind alle anderen Formatierungsoptionen deaktiviert. Tippen Sie erneut auf das **Quellbearbeitungssymbol** , um zur formatierten Ansicht zurückzukehren.

   >[!CAUTION]
   >
   >Wie immer bei Zugriff auf rohe HTML muss die Unterstützung bei Verwendung der Option **&quot;Quell-Bearbeitung** &quot; vorgenommen werden.
   >
   >
   >HTML, die über **die Quell-Bearbeitung** eingegeben wurde, wird auf XSS-Risiken überprüft und alle Skripten, die eingefügt werden, werden entfernt und werden nicht auf der resultierenden Seite angezeigt. Fehlerhafte HTML-Einträge, die in **der Quell-Bearbeitung** eingegeben wurden, können die Vorlage für die Seite umbrechen, was zu unerwarteten Formatierungen führt oder die resultierende Seite unbrauchbar macht.

* Absatzformat

   ![](assets/chlimage_1-84.png)

   Wird verwendet, um Absatzformatierung auf den ausgewählten Text oder auf Text anzuwenden, der nach dem Cursor eingefügt wurde. Durch Auswahl dieser Optionen wird eine Dropdown-Liste geöffnet, in der das Absatzformat ausgewählt ist.

   ![](assets/chlimage_1-85.png)

Die Textkomponente kann auch online bearbeitet werden, aufgrund von Leerzeichen sind jedoch nicht alle Formatierungsoptionen online verfügbar. Um alle Optionen anzuzeigen, wechseln Sie zum Vollbildmodus.

![](assets/chlimage_1-86.png)

## Design-Dialogfeld {#design-dialog}

Im Entwurfsdialogfeld können Sie festlegen, welche Textformatierungsoptionen den Autoren zur Verfügung stehen.

### Funktionen {#features}

![](assets/chlimage_1-28.png)

Die folgenden Funktionen können für die Komponente aktiviert oder deaktiviert werden.

* Nur Text einfügen
* Vergangenes Wort
* Suchen und ersetzen
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
* Untergeordnetes/Hochgestellt

### Absatzformate {#paragraph-styles}

![](assets/chlimage_1-30.png)

Absatzstile können für die Komponente aktiviert oder deaktiviert werden. Bei Aktivierung können die zulässigen Formate definiert werden.

* Tippen oder klicken Sie auf **die Schaltfläche &quot;Hinzufügen** &quot; , um einen neuen Stil einzufügen.
* Geben Sie den Code des Stils und eine Beschreibung ein, die im Dialogfeld &quot;Bearbeiten&quot; angezeigt wird.
* Um einen Stil zu entfernen, tippen Sie auf die **Schaltfläche &quot;Löschen** &quot; .
* Um die Reihenfolge der Formate zu ändern, tippen oder klicken Sie auf und ziehen Sie die Griffe.

### Sonderzeichen {#special-characters}

![](assets/chlimage_1-31.png)

Die Option zum Einfügen von Sonderzeichen kann für die Komponente aktiviert oder deaktiviert werden. Bei Aktivierung können die zulässigen Zeichen definiert werden.

* Tippen oder klicken Sie auf **die Schaltfläche &quot;Hinzufügen** &quot; , um ein neues Zeichen einzufügen.
* Geben Sie den HTML-Code des Zeichens und eine Beschreibung ein, die im Dialogfeld &quot;Bearbeiten&quot; angezeigt wird.
* Um ein Zeichen zu entfernen, oder klicken Sie auf die **Schaltfläche &quot;Löschen** &quot; .
* Um die Reihenfolge der Zeichen zu ändern, tippen oder klicken Sie auf und ziehen Sie die Griffe.

## Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur Textkomponente [finden Sie unter github](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/text/v1/text).

Das gesamte Kernkomponentenprojekt kann von github heruntergeladen werden.

Weitere Informationen zur Entwicklung Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Komponenten](developing.md).
