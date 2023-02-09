---
title: Adaptive Forms-Kernkomponente - Zahleneingabe
description: Verwenden oder Anpassen der Eingabe-Kernkomponente "Adaptive Forms Number".
role: Architect, Developer, Admin, User
source-git-commit: 945e1793ae4e959f83960db46d2de4257916fe32
workflow-type: tm+mt
source-wordcount: '1780'
ht-degree: 1%

---


# Zahleneingabe {#number-input-adaptive-forms-core-component}

Eine Zahleneingabe-Komponente in einem adaptiven Formular ist ein Formularfeldtyp, mit dem Benutzer numerische Werte eingeben können. Die Komponente wird in der Regel durch ein Textfeld mit einem Nach-oben- und Nach-unten-Pfeil zum Erhöhen und Verringern der Zahl dargestellt.

Sie kann auch mit Attributen wie min, max, step, value und mehr verwendet werden. Mit diesen Attributen können Sie die im Feld zulässigen Mindest- und Höchstwerte, das Schrittervall zum Erhöhen oder Verringern der Zahl und den Standardwert des Felds festlegen.

Mit dieser Komponente können numerische Daten wie Alter, Menge und mehr erfasst werden. und kann auch für mathematische Operationen wie Addition und Subtraktion verwendet werden. Diese Komponente kann auch zur Validierung der vom Benutzer eingegebenen numerischen Daten verwendet werden.

Für die Barrierefreiheit ist es wichtig, einen &quot;Titel&quot;anzugeben, der den Zweck des Zahleneingabefelds beschreibt und welche Art von Eingabe erwartet wird.

**Beispiel**

![](/help/adaptive-forms/assets/numeric-stepper.png)

## Verwendung {#reasons-to-use-number-input-numeric-stepper}

Es gibt mehrere Gründe, warum es sinnvoll ist, eine numerische Eingabekomponente in ein adaptives Formular einzuschließen, darunter:

* **Mathematische Operationen**: Numerische Felder können verwendet werden, um mathematische Operationen wie Addition, Subtraktion, Multiplikation und Division durchzuführen.

* **Datenbereich**: Numerische Felder können verwendet werden, um einen Bereich gültiger Werte mithilfe von Min-, Max- und Schrittattributen festzulegen.

* **Dynamische Inhalte**: Numerische Komponenten können verwendet werden, um dynamische Daten basierend auf den Formularfeldern anzuzeigen.


## Version und Kompatibilität {#version-and-compatibility}

Die Eingabe-Kernkomponente für die adaptive Forms-Nummer wurde im Februar 2023 als Teil der Kernkomponenten 2.0.4 veröffentlicht. Hier finden Sie eine Tabelle mit allen unterstützten Versionen, AEM Kompatibilität und Links zur entsprechenden Dokumentation:

|  |  |
|---|---|
| Komponentenversion | AEM as a Cloud Service |
| --- | --- |
| v1 | Kompatibel mit<br>[Version 2.0.4](/help/versions.md) und höher | Kompatibel | Kompatibel |

Informationen zu Kernkomponentenversionen und -versionen finden Sie im Abschnitt [Kernkomponenten-Versionen](/help/versions.md) Dokument.


<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technische Details {#technical-details}

Laden Sie die neuesten Informationen zur Eingabe-Kernkomponente für die adaptive Forms-Nummer in der technischen Dokumentation zu [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/numberinput/v1/numberinput). Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie im Abschnitt [Entwicklerdokumentation für Kernkomponenten](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Im Dialogfeld &quot;Konfigurieren&quot;können Sie Ihre Zahleneingabe-Erfahrung für Besucher einfach anpassen. Sie können auch Zahleneingabeoptionen definieren, um ein nahtloses Benutzererlebnis zu ermöglichen.

### Einfache Registerkarte {#basic-tab}

![Einfache Registerkarte](/help/adaptive-forms/assets/numberinput_basictab.png)

* **Name** - Sie können eine Formularkomponente sowohl im Formular als auch im Regeleditor leicht mit ihrem eindeutigen Namen identifizieren, der Name darf jedoch keine Leerzeichen oder Sonderzeichen enthalten.

* **Titel** - Mit dem Titel können Sie eine Komponente in einem Formular leicht identifizieren. Standardmäßig wird der Titel über der Komponente angezeigt. Wenn Sie keinen Titel hinzufügen, wird der Name der Komponente anstelle des Titeltexts angezeigt.

* **Titel ausblenden** - Wählen Sie die Option aus, um den Titel der Komponente auszublenden.

* **Platzhaltertext** - Platzhaltertext in einer Formularkomponente bezieht sich auf eine kurze Beschriftung oder Eingabeaufforderung, die in einem Eingabefeld angezeigt wird, um den Benutzer darauf hinzuweisen, welcher Informationstyp in dieses Feld eingegeben werden soll. Platzhaltertext verschwindet, wenn der Benutzer mit der Eingabe in das Feld beginnt, und wird wieder angezeigt, wenn das Feld leer bleibt. Es bietet einen visuellen Hinweis für den Benutzer, fungiert jedoch nicht als permanente Bezeichnung oder Wert für das Feld.
* **Bindungsverweis** - Ein Bindungsverweis ist ein Verweis auf ein Datenelement, das in einer externen Datenquelle gespeichert und in einem Formular verwendet wird. Mit der Bindungsreferenz können Sie Daten dynamisch an Formularfelder binden, sodass das Formular die aktuellsten Daten aus der Datenquelle anzeigen kann. Beispielsweise kann eine Bindungsverweis verwendet werden, um den Namen und die Adresse eines Kunden in einem Formular anzuzeigen, basierend auf der im Formular eingegebenen Kundenkennung. Die Bindungsverweis kann auch verwendet werden, um die Datenquelle mit den im Formular eingegebenen Daten zu aktualisieren. Auf diese Weise können Sie mit AEM Forms Formulare erstellen, die mit externen Datenquellen interagieren und so eine nahtlose Benutzererfahrung bei der Datenerfassung und -verwaltung bieten.
* **Komponente ausblenden** - Wählen Sie die Option, um die Komponente aus dem Formular auszublenden. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regeleditor. Dies ist nützlich, wenn Sie Informationen speichern müssen, die vom Benutzer nicht gesehen oder direkt geändert werden müssen.
* **Komponente deaktivieren** - Wählen Sie die Option zum Deaktivieren der Komponente aus. Die deaktivierte Komponente ist vom Endbenutzer nicht aktiv oder kann nicht bearbeitet werden. Der Benutzer kann den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regeleditor.
* **Schreibgeschützt** - Wählen Sie die Option, um die Komponente nicht bearbeitbar zu machen. Der Benutzer kann den Wert des Felds sehen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regeleditor.
* **Zahlentyp** - Mit dieser Option können Sie den Typ der numerischen Werte auswählen, &#x200B; im Formularfeld zulässig &#x200B;. Sie können entweder den Typ Dezimal oder Ganzzahl aus dem Dropdown-Menü auswählen.
* **Standardwert** - Mit dieser Option können Sie einen Standardwert in ein Formularfeld einfügen. Wenn **Komponente deaktiviert** oder **Schreibgeschützte Komponente** ausgewählt ist, wird der Standardwert auf dem Bildschirm angezeigt. Wenn kein Wert vom Benutzer in das Formularfeld eingegeben wird, wird dieser Wert zum Zeitpunkt der Formularübermittlung gesendet

### Registerkarte &quot;Validierung&quot; {#validation-tab}

![Registerkarte &quot;Validierung&quot;](/help/adaptive-forms/assets/numberinput_validationtab.png)

* **Erforderlich** - Wählen Sie diese Option, wenn Sie die Komponente in einem adaptiven Formular anzeigen möchten. Sie können die **Komponente ausblenden** oder **Komponente deaktivieren**  im **Allgemein** Registerkarte angezeigt, wenn diese Option aktiviert ist.

* **Fehlermeldung** - Mit dieser Option können Sie eine Nachricht eingeben, die angezeigt wird, wenn die **Erforderlich** aktiviert ist und das Feld leer bleibt.

* **Überprüfungsmeldung für Skripten** - Mit dieser Option können Sie eine Meldung eingeben, die angezeigt werden soll, wenn die Skriptvalidierung fehlschlägt.

* **Niedrigste Zahl/Kleinste Zahl** - Verwenden Sie diese Option, um die Mindestanzahl für die Eingabe im Formularfeld auszuwählen. Wenn der Wert kleiner ist als die in **Niedrigste Zahl/Kleinste Zahl** in das Formularfeld eingegeben wurde, wird die Fehlermeldung angezeigt.

* **Minimale Fehlermeldung** - Mit dieser Option können Sie eine Fehlermeldung eingeben, die angezeigt wird, wenn der Benutzer einen Wert eingibt, der unter dem im Feld **Mindestanzahl/Mindestanzahl** -Option.

* **Mindestwert ausschließen** - Aktivieren Sie dieses Kontrollkästchen, wenn Sie den im **Niedrigste Zahl/Kleinste Zahl** -Option, die in den Bereich der Werte aufgenommen &#x200B;, die in das Formularfeld eingegeben werden sollen.

* **Höchste Zahl/Größte Zahl** - Verwenden Sie diese Option, um die maximal zulässige Zahl auszuwählen, die in das Formularfeld eingegeben werden soll. Wenn die Zahl größer ist als die in **Höchste Zahl/Größte Zahl** in das Formularfeld eingegeben wurde, wird die Fehlermeldung angezeigt.

* **Maximale Fehlermeldung** - Mit dieser Option können Sie eine Fehlermeldung eingeben, die angezeigt wird, wenn der Benutzer einen Wert eingibt, der größer ist als der in der Variablen **Höchste Zahl/Größte Zahl** -Option.

* **Höchstwert ausschließen** - Aktivieren Sie dieses Kontrollkästchen, wenn Sie den im **Höchste Zahl/Größte Zahl** Option, die in den Wertebereich aufgenommen werden soll, der in das Formularfeld eingegeben werden soll.

### Registerkarte &quot;Hilfe-Inhalt&quot; {#help-content}

![Registerkarte &quot;Hilfe-Inhalt&quot;](/help/adaptive-forms/assets/numberinput_helptab.png)

* **Kurzbeschreibung** - Eine kurze Beschreibung ist eine kurze Texterklärung, die zusätzliche Informationen oder Klarstellungen zum Zweck eines bestimmten Formularfelds bietet. Es hilft dem Benutzer zu verstehen, welcher Datentyp in das Feld eingegeben werden soll, und kann Richtlinien oder Beispiele bereitstellen, um sicherzustellen, dass die eingegebenen Informationen gültig sind und die gewünschten Kriterien erfüllen. Standardmäßig bleiben kurze Beschreibungen ausgeblendet. Aktivieren Sie die **Kurzbeschreibung immer anzeigen** -Option, um sie unter der Komponente anzuzeigen.

* **Kurzbeschreibung immer anzeigen** - Aktivieren Sie die Option, um die Kurzbeschreibung unter der Komponente anzuzeigen.

* **Hilfetext** - Hilfetext bezieht sich auf zusätzliche Informationen oder Anleitungen, die dem Benutzer bereitgestellt werden, um ihn beim korrekten Ausfüllen eines Formularfelds zu unterstützen. Er wird angezeigt, wenn der Benutzer auf das Hilfesymbol (i) neben der Komponente klickt. Hilfetext enthält detailliertere Informationen als die Beschriftung oder der Platzhaltertext eines Formularfelds und soll dem Benutzer dabei helfen, die Anforderungen oder Einschränkungen des Felds zu verstehen. Es kann auch Vorschläge oder Beispiele anbieten, um das Ausfüllen des Formulars zu vereinfachen und genauer zu gestalten.

### Registerkarte „Erreichbarkeit“ {#accessibility}

![Registerkarte &quot;Barrierefreiheit&quot;](/help/adaptive-forms/assets/numberinput_accessibility.png)

* **Text für Bildschirmlesehilfen** - Text für Bildschirmlesehilfen bezieht sich auf zusätzlichen Text, der speziell für Hilfstechnologien wie Bildschirmlesehilfen vorgesehen ist, die von sehbehinderten Personen verwendet werden. Dieser Text enthält eine Audiobeschreibung des Zwecks des Formularfelds und kann Informationen über den Titel, die Beschreibung, den Namen und alle relevanten Nachrichten (benutzerdefinierten Text) des Felds enthalten. Der Text der Bildschirmlesehilfe hilft sicherzustellen, dass das Formular für alle Benutzer zugänglich ist, auch für Benutzer mit Sehbehinderungen, und bietet ihnen ein umfassendes Verständnis des Formularfelds und seiner Anforderungen.

### Registerkarte &quot;Formate&quot; {#formats-tab}

![Registerkarte &quot;Barrierefreiheit&quot;](/help/adaptive-forms/assets/numberinput_formattab.png)


* **Anzeigeformat** - Mit dieser Option können Sie die Option aus verschiedenen numerischen ganzzahligen Formaten für die Anzeige auswählen. Wenn der Benutzer eine Option aus dem **Typ** Dropdown-Menü, die **Format** wird im Bereich angezeigt. Sie können ein bestimmtes Format wählen, in dem dem Benutzer Zahlen angezeigt werden.

* **Anzahl der Ziffern vor dem Dezimaltrennzeichen (1234.000)** - Verwenden Sie diese Option, um die Anzahl der Ziffern anzugeben, die vor dem Dezimalpunkt angezeigt werden sollen.

* **Anzahl der Stellen nach dem Dezimaltrennzeichen (1234.000)** - Verwenden Sie diese Option, um die Anzahl der Ziffern anzugeben, die nach dem Dezimalpunkt angezeigt werden sollen.

## Dialogfeld „Design“ {#design-dialog}

Das Dialogfeld &quot;Design&quot;wird verwendet, um CSS-Stile für die Eingabekomponente &quot;Zahl&quot;zu definieren und zu verwalten.


### Registerkarte „Arten“ {#styles-tab}

Das Dialogfeld &quot;Design&quot;wird zum Definieren und Verwalten von CSS-Stilen für eine Komponente verwendet. Die Eingabekomponente für die adaptive Forms-Nummer unterstützt die AEM [Stilsystem](/help/get-started/authoring.md#component-styling).

**Standard-CSS-Klassen**: Sie können eine standardmäßige CSS-Klasse für die Eingabe-Kernkomponente &quot;Adaptive Forms Number&quot;bereitstellen.

**Zulässige Stile**: Sie können Stile definieren, indem Sie einen Namen und die CSS-Klasse angeben, die den Stil darstellt. Sie können beispielsweise einen Stil mit dem Namen &quot;fett Text&quot;erstellen und die CSS-Klasse &quot;font-weight: fett&quot;. Sie können diese Stile im adaptiven Forms-Editor verwenden oder auf ein adaptives Formular anwenden. Um einen Stil anzuwenden, wählen Sie im adaptiven Forms-Editor die Komponente aus, auf die Sie den Stil anwenden möchten, navigieren Sie zum Dialogfeld &quot;Eigenschaften&quot;und wählen Sie den gewünschten Stil aus dem **Stile** Dropdown-Liste. Wenn Sie die Stile aktualisieren oder ändern müssen, kehren Sie einfach zum Dialogfeld &quot;Design&quot;zurück, aktualisieren Sie die Stile auf der Registerkarte &quot;Stile&quot;und speichern Sie die Änderungen.

### Registerkarte &quot;Formate&quot; {#format-tab}

Auf der Registerkarte &quot;Formate&quot;können Sie standardmäßige und benutzerdefinierte Zahlenformate angeben.
