---
title: Adaptive Forms-Kernkomponente - Texteingabe (Textfeld)
description: Verwenden oder Anpassen der adaptiven Forms-Texteingabe-Kernkomponente
role: Architect, Developer, Admin, User
source-git-commit: 0e4fb8454b7ef84eb5b1b73b01c982a2f9c12381
workflow-type: tm+mt
source-wordcount: '1727'
ht-degree: 1%

---


# Texteingabe (Textfeld) {#text-input-adaptive-forms-core-component}

Eine Texteingabekomponente (Textfeld) ermöglicht es einem Benutzer, eine oder mehrere Textzeilen einzugeben und zu bearbeiten, je nach dem Typattribut des Eingabeelements. Die Texteingabekomponente kann in einem Formular platziert werden und ist in der Regel mit einem hilfreichen Text beschriftet, der den Zweck leicht identifiziert. Dies sind ein grundlegendes Element jeder Form, das häufig verwendet wird, um verschiedene Datentypen von Benutzern zu erfassen. Diese sind einfach, flexibel und können so konfiguriert werden, dass Eingaben validiert und die Genauigkeit der Datenerfassung verbessert werden.


**Beispiel**

![](/help/adaptive-forms/assets/text-input.png)


## Verwendung {#reasons-to-use-text-input-field}

Es gibt mehrere Gründe für die Verwendung der Texteingabekomponente in einem adaptiven Formular:

* **Datenerfassung**: Texteingabefelder sind eines der gebräuchlichsten Formularelemente, mit denen ein breites Spektrum an Informationen von Benutzern erfasst wird, z. B. Namen, E-Mail-Adressen, Telefonnummern und andere Arten von Textdaten.

* **Benutzerfreundlich**: Texteingabefelder sind einfach und einfach zu verwenden, sodass Benutzer Text einfach eingeben und bearbeiten können.

* **Flexibilität**: Texteingabefelder können verwendet werden, um eine breite Palette von Informationen zu sammeln, von kurzen, einzeiligen Texteinträgen bis hin zu längeren, mehrzeiligen Texteinträgen.

## Version und Kompatibilität {#version-and-compatibility}

Die Kernkomponente &quot;Adaptive Forms-Texteingabe&quot;wurde im Februar 2023 als Teil der Kernkomponenten 2.0.4 veröffentlicht. Hier finden Sie eine Tabelle mit allen unterstützten Versionen, AEM Kompatibilität und Links zur entsprechenden Dokumentation:

| Komponentenversion | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Kompatibel mit<br>[Version 2.0.4](/help/versions.md) und höher | Kompatibel | Kompatibel |

Informationen zu Kernkomponentenversionen und -versionen finden Sie im Abschnitt [Kernkomponenten-Versionen](/help/versions.md) Dokument.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technische Details {#technical-details}

Die neuesten Informationen zu den adaptiven Forms-Registerkarten auf der Hauptkomponente finden Sie in der technischen Dokumentation zu [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/textinput/v1/textinput). Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie im Abschnitt [Entwicklerdokumentation für Kernkomponenten](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Im Dialogfeld &quot;Konfigurieren&quot;können Sie Ihre Texteingabe-Erfahrung für Besucher einfach anpassen. Sie können auch Texteingabeoptionen definieren, die für ein nahtloses Benutzererlebnis sorgen.

![Einfache Registerkarte](/help/adaptive-forms/assets/textinput_basictab.png)

* **Name** - Sie können eine Formularkomponente sowohl im Formular als auch im Regeleditor leicht mit ihrem eindeutigen Namen identifizieren, der Name darf jedoch keine Leerzeichen oder Sonderzeichen enthalten.

* **Titel** - Mit dem Titel können Sie eine Komponente in einem Formular leicht identifizieren. Standardmäßig wird der Titel über der Komponente angezeigt. Wenn Sie keinen Titel hinzufügen, wird der Name der Komponente anstelle des Titeltexts angezeigt.

* **Titel ausblenden** - Wählen Sie die Option aus, um den Titel der Komponente auszublenden.

* **Platzhaltertext** - Platzhaltertext in einer Formularkomponente bezieht sich auf eine kurze Beschriftung oder Eingabeaufforderung, die in einem Eingabefeld angezeigt wird, um den Benutzer darauf hinzuweisen, welcher Informationstyp in dieses Feld eingegeben werden soll. Platzhaltertext verschwindet, wenn der Benutzer mit der Eingabe in das Feld beginnt, und wird wieder angezeigt, wenn das Feld leer bleibt. Es bietet einen visuellen Hinweis für den Benutzer, fungiert jedoch nicht als permanente Bezeichnung oder Wert für das Feld.
* **Bindungsverweis** - Ein Bindungsverweis ist ein Verweis auf ein Datenelement, das in einer externen Datenquelle gespeichert und in einem Formular verwendet wird. Mit der Bindungsreferenz können Sie Daten dynamisch an Formularfelder binden, sodass das Formular die aktuellsten Daten aus der Datenquelle anzeigen kann. Beispielsweise kann eine Bindungsverweis verwendet werden, um den Namen und die Adresse eines Kunden in einem Formular anzuzeigen, basierend auf der im Formular eingegebenen Kundenkennung. Die Bindungsverweis kann auch verwendet werden, um die Datenquelle mit den im Formular eingegebenen Daten zu aktualisieren. Auf diese Weise können Sie mit AEM Forms Formulare erstellen, die mit externen Datenquellen interagieren und so eine nahtlose Benutzererfahrung bei der Datenerfassung und -verwaltung bieten.
* **Komponente ausblenden** - Wählen Sie die Option, um die Komponente aus dem Formular auszublenden. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regeleditor. Dies ist nützlich, wenn Sie Informationen speichern müssen, die vom Benutzer nicht gesehen oder direkt geändert werden müssen.
* **Komponente deaktivieren** - Wählen Sie die Option zum Deaktivieren der Komponente aus. Die deaktivierte Komponente ist vom Endbenutzer nicht aktiv oder kann nicht bearbeitet werden. Der Benutzer kann den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regeleditor.
* **Schreibgeschützt** - Wählen Sie die Option aus, um die Komponente nicht bearbeitbar zu machen. Der Benutzer kann den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regeleditor.
* **Standardwert** - Mit dieser Option können Sie einen Standardwert in ein Formularfeld einfügen. Der Text verschwindet, wenn der Benutzer mit der Eingabe in das Feld beginnt. Wenn **Komponente deaktiviert** oder **Schreibgeschützte Komponente** ausgewählt ist, wird der Standardwert auf dem Bildschirm angezeigt. Wenn kein Wert vom Benutzer in das Formularfeld eingegeben wird, wird dieser Wert zum Zeitpunkt der Formularübermittlung gesendet.
* **Mehrere Zeilen zulassen** - Mit dieser Option können Benutzer mehrere Zeilen in ein Formularfeld eingeben.
* **Rich-Text zulassen** - Das Dialogfeld &quot;Bearbeiten&quot;bietet standardmäßige Rich-Text-Formatierungswerkzeuge, mit denen der Benutzer Text formatieren kann.
* **Attribut für automatische Füllung** - Die Option zum automatischen Ausfüllen füllt füllt das Formularfeld nach einem Muster oder nach einem zuvor eingegebenen Text. Wenn der Benutzer beginnt, Text in das Formularfeld einzugeben, werden Vorschläge in einer Dropdown-Liste angezeigt, aus der er die entsprechende Option auswählen kann.

### Registerkarte &quot;Validierung&quot; {#validation-tab}

![Registerkarte &quot;Validierung&quot;](/help/adaptive-forms/assets/textinput_validationtab.png)

* **Erforderlich** - Wählen Sie diese Option, wenn Sie die Komponente in einem adaptiven Formular anzeigen möchten. Sie können die **Komponente ausblenden** oder **Komponente deaktivieren**  im **Allgemein** Registerkarte angezeigt, wenn diese Option aktiviert ist.

* **Fehlermeldung** - Mit dieser Option können Sie eine Nachricht eingeben, die angezeigt wird, wenn die **Erforderlich** aktiviert ist und das Feld leer bleibt.

* **Überprüfungsmeldung für Skripten** - Mit dieser Option können Sie eine Meldung eingeben, die angezeigt werden soll, wenn die Skriptvalidierung fehlschlägt.

* **Maximale Zeichenanzahl** - Mit dieser Option können Sie die maximal zulässige Anzahl von Zeichen in der Komponente angeben. Wenn Sie Zeichen eingeben, die größer sind als der in **Maximale Zeichenanzahl**, wird eine Fehlermeldung auf dem Bildschirm angezeigt. Die **Fehlermeldung zu maximal Zeichen** können Sie eine benutzerdefinierte Fehlermeldung hinzufügen.

* **Fehlermeldung zu maximal Zeichen** - die **Fehlermeldung zu maximal Zeichen** können Sie eine benutzerdefinierte Fehlermeldung hinzufügen, wenn Sie Zeichen eingeben, die über dem in der Variablen **Maximale Zeichenanzahl** -Option.

* **Mindestanzahl von Zeichen** - Mit dieser Option können Sie die zulässige Mindestanzahl von Zeichen im Feld angeben. Wenn Sie Zeichen eingeben, die kleiner sind als der in **Mindestanzahl von Zeichen**, wird eine Fehlermeldung auf dem Bildschirm angezeigt. Die **Fehlermeldung bei minimalen Zeichen** können Sie eine benutzerdefinierte Fehlermeldung hinzufügen.

* **Fehlermeldung bei minimalen Zeichen** - die **Fehlermeldung bei minimalen Zeichen** können Sie eine benutzerdefinierte Fehlermeldung hinzufügen, wenn Sie Zeichen eingeben, die kleiner sind als der in der Variablen **Mindestanzahl von Zeichen** -Option.

Die **Überprüfungsmuster** ermöglicht die Eingabe eines Musters zur Validierung des eingegebenen Texts. Falls der Text nicht mit dem eingegebenen Wert validiert werden kann **Muster** -Option, wird die Fehlermeldung auf dem Bildschirm angezeigt.
* **Muster** - Mit dieser Option können Sie die zulässigen Überprüfungsmuster für Text eingeben. Reguläre Ausdrücke sind ebenfalls zulässig.
* **Fehlermeldung** - Mit dieser Option können Sie eine Nachricht eingeben, die auf dem Bildschirm angezeigt wird, wenn der eingegebene Text nicht mit dem im **Muster** option

### Registerkarte &quot;Hilfe-Inhalt&quot; {#help-content-tab}

![Registerkarte &quot;Hilfe-Inhalt&quot;](/help/adaptive-forms/assets/textinput_helptab.png)

* **Kurzbeschreibung** - Eine kurze Beschreibung ist eine kurze Texterklärung, die zusätzliche Informationen oder Klarstellungen zum Zweck eines bestimmten Formularfelds bietet. Es hilft dem Benutzer zu verstehen, welcher Datentyp in das Feld eingegeben werden soll, und kann Richtlinien oder Beispiele bereitstellen, um sicherzustellen, dass die eingegebenen Informationen gültig sind und die gewünschten Kriterien erfüllen. Standardmäßig bleiben kurze Beschreibungen ausgeblendet. Aktivieren Sie die **Kurzbeschreibung immer anzeigen** -Option, um sie unter der Komponente anzuzeigen.

* **Kurzbeschreibung immer anzeigen** - Aktivieren Sie die Option, um die Kurzbeschreibung unter der Komponente anzuzeigen.

* **Hilfetext** - Hilfetext bezieht sich auf zusätzliche Informationen oder Anleitungen, die dem Benutzer bereitgestellt werden, um ihn beim korrekten Ausfüllen eines Formularfelds zu unterstützen. Er wird angezeigt, wenn der Benutzer auf das Hilfesymbol (i) neben der Komponente klickt. Hilfetext enthält detailliertere Informationen als die Beschriftung oder der Platzhaltertext eines Formularfelds und soll dem Benutzer dabei helfen, die Anforderungen oder Einschränkungen des Felds zu verstehen. Es kann auch Vorschläge oder Beispiele anbieten, um das Ausfüllen des Formulars zu vereinfachen und genauer zu gestalten.

### Registerkarte „Erreichbarkeit“ {#accessibility-tab}

![Registerkarte &quot;Barrierefreiheit&quot;](/help/adaptive-forms/assets/textinput_accessibiltytab.png)

* **Text für Bildschirmlesehilfen** - Text für Bildschirmlesehilfen bezieht sich auf zusätzlichen Text, der speziell für Hilfstechnologien wie Bildschirmlesehilfen vorgesehen ist, die von sehbehinderten Personen verwendet werden. Dieser Text enthält eine Audiobeschreibung des Zwecks des Formularfelds und kann Informationen über den Titel, die Beschreibung, den Namen und alle relevanten Nachrichten (benutzerdefinierten Text) des Felds enthalten. Der Text der Bildschirmlesehilfe hilft sicherzustellen, dass das Formular für alle Benutzer zugänglich ist, auch für Benutzer mit Sehbehinderungen, und bietet ihnen ein umfassendes Verständnis des Formularfelds und seiner Anforderungen.

## Dialogfeld „Design“ {#design-dialog}

Das Dialogfeld &quot;Design&quot;wird verwendet, um CSS-Stile für die Komponente &quot;Textfeld&quot;zu definieren und zu verwalten.

### Registerkarte „Arten“ {#styles-tab}

Das Dialogfeld &quot;Design&quot;wird zum Definieren und Verwalten von CSS-Stilen für eine Komponente verwendet. Die Kernkomponente &quot;Adaptives Forms-Textfeld&quot;unterstützt die AEM [Stilsystem](/help/get-started/authoring.md#component-styling).

**Standard-CSS-Klassen**: Sie können eine standardmäßige CSS-Klasse für die Kernkomponente &quot;Adaptives Forms-Textfeld&quot;bereitstellen.

**Zulässige Stile**: Sie können Stile definieren, indem Sie einen Namen und die CSS-Klasse angeben, die den Stil darstellt. Sie können beispielsweise einen Stil mit dem Namen &quot;fett Text&quot;erstellen und die CSS-Klasse &quot;font-weight: fett&quot;. Sie können diese Stile im adaptiven Forms-Editor verwenden oder auf ein adaptives Formular anwenden. Um einen Stil anzuwenden, wählen Sie im adaptiven Forms-Editor die Komponente aus, auf die Sie den Stil anwenden möchten, navigieren Sie zum Dialogfeld &quot;Eigenschaften&quot;und wählen Sie den gewünschten Stil aus dem **Stile** Dropdown-Liste. Wenn Sie die Stile aktualisieren oder ändern müssen, kehren Sie einfach zum Dialogfeld &quot;Design&quot;zurück, aktualisieren Sie die Stile auf der Registerkarte &quot;Stile&quot;und speichern Sie die Änderungen.

### Registerkarte &quot;Formate&quot; {#format-tab}

Auf der Registerkarte &quot;Formate&quot;können Sie standardmäßige und benutzerdefinierte Zahlenformate angeben.