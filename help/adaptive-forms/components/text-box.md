---
title: Kernkomponente für adaptive Formulare – Texteingabe (Textfeld)
description: Verwenden oder Anpassen der Texteingabe-Kernkomponente für adaptive Formulare.
role: Architect, Developer, Admin, User
exl-id: 49d9fe69-0578-4489-beaa-a18cdb14add7
source-git-commit: 9f151ae26c9d2006b74656ec5086f1a5e9fc4b30
workflow-type: ht
source-wordcount: '2120'
ht-degree: 100%

---

# Textfeld-Komponente{#text-input-adaptive-forms-core-component}

Eine Texteingabekomponente (Textfeld) ermöglicht es Benutzenden, eine oder mehrere Zeilen Text einzugeben und zu bearbeiten, je nach dem Typattribut des Eingabeelements. Die Texteingabekomponente kann in einem Formular platziert werden und ist in der Regel mit einem hilfreichen Text beschriftet, der ihren Zweck leicht erkennen lässt. Diese sind grundlegende Elemente eines jeden Formulars, die häufig verwendet werden, um verschiedene Datentypen von Benutzenden zu erfassen. Diese sind einfach, flexibel und können so konfiguriert werden, dass Eingaben überprüft werden und die Genauigkeit der Datenerfassung verbessert wird.

**Beispiel**

![Beispiel](/help/adaptive-forms/assets/text-input.png)


## Verwendung {#reasons-to-use-text-input-field}

Es gibt mehrere Gründe für die Verwendung der Texteingabekomponente in einem adaptiven Formular:

- **Datenerfassung**: Texteingabefelder sind eines der gebräuchlichsten Formularelemente, mit denen ein breites Spektrum an Informationen von Benutzenden erfasst wird, z. B. Namen, E-Mail-Adressen, Telefonnummern und andere Arten von Textdaten.

- **Benutzerfreundlich**: Texteingabefelder sind einfach und leicht zu verwenden, sodass Benutzende einfach einen Text eingeben und bearbeiten können.

- **Flexibel**: Sie können Texteingabefelder verwenden, um eine breite Palette von Informationen zu sammeln – von kurzen, einzeiligen Texteinträgen bis hin zu längeren, mehrzeiligen Texteinträgen.

## Version und Kompatibilität {#version-and-compatibility}

Die Kernkomponente für Textfelder in adaptiven Formularen wurde im Februar 2023 als Teil der Kernkomponenten 2.0.4 für Cloud Service und der Kernkomponenten 1.1.12 für AEM 6.5.16.0 Forms oder höher veröffentlicht. Hier finden Sie eine Tabelle mit allen unterstützten Versionen, AEM-Kompatibilität und Links zur entsprechenden Dokumentation:

| Komponentenversion | AEM as a Cloud Service | AEM 6.5.16.0 Forms oder höher |
|---|---|---|
| v1 | Kompatibel mit<br>[Version 2.0.4](/help/adaptive-forms/version.md) und höher | Kompatibel mit<br>[Version 1.1.12](/help/adaptive-forms/version.md) und höher (aber nur bis Version 2.0.0). |

Informationen zu Versionen und Freigaben der Kernkomponente finden Sie im Dokument [Kernkomponenten-Versionen](/help/adaptive-forms/version.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technische Details {#technical-details}

Aktuelle Informationen zur Kernkomponente „Textbox“ für adaptive Formulare finden Sie in der technischen Dokumentation auf [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/textinput/v1/textinput). Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Entwicklerdokumentation für Kernkomponenten](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Mit dem Dialogfeld „Konfigurieren“ können das Besuchererlebnis bei der Texteingabe einfach anpassen. Sie können auch Optionen zur Texteingabe definieren, die für ein nahtloses Benutzererlebnis sorgen.

### Registerkarte „Allgemein“

![Registerkarte „Allgemein“](/help/adaptive-forms/assets/textinput_basictab.png)

- **Name**: Sie können eine Formularkomponente sowohl im Formular als auch im Regeleditor durch ihren eindeutigen Namen identifizieren. Der Name darf keine Leerzeichen oder Sonderzeichen enthalten.

- **Titel**: Mit dem Titel können Sie eine Komponente in einem Formular leicht identifizieren. Standardmäßig wird der Titel oberhalb der Komponente angezeigt. Wenn Sie keinen Titel hinzufügen, wird der Name der Komponente anstelle des Titeltexts angezeigt.
- **Rich-Text für Titel zulassen**: Diese Funktionen ermöglichen es Benutzenden, einfache Texttitel zu formatieren, die Funktionen wie fett, kursiv, unterstrichener Text, verschiedene Schriftarten, Schriftgrößen, Farben und zusätzliche Optionen enthalten und so die visuelle Darstellung und Anpassung zu verbessern. Sie bietet mehr Flexibilität und kreative Kontrolle bei der Hervorhebung von Titeln in Dokumenten, Websites oder Anwendungen.\
  Durch Aktivieren des Kontrollkästchens **Rich-Text für Titel zulassen** werden Formatierungsoptionen sichtbar, mit denen Sie den Titel der Komponente gestalten können. Um auf alle verfügbaren Formatierungsoptionen zuzugreifen, können Sie auf die Registerkarte ![Vollbildsymbol](/help/adaptive-forms/assets/fullscreen-icon.png) klicken.

  ![Rich-Text-Unterstützung](/help/adaptive-forms/assets/richtext-support-title.png)

- **Titel ausblenden**: Wählen Sie die Option aus, um den Titel der Komponente auszublenden.

- **Platzhaltertext**: Platzhaltertext in einer Formularkomponente bezieht sich auf eine kurze Beschriftung oder Eingabeaufforderung, die in einem Eingabefeld angezeigt wird, um Benutzende darauf hinzuweisen, welcher Informationstyp in dieses Feld eingegeben werden soll. Der Platzhaltertext verschwindet, wenn Benutzende mit der Eingabe in das Feld beginnen, und erscheint wieder, wenn das Feld leer bleibt. Er stellt einen visuellen Hinweis für Benutzende bereit, fungiert jedoch nicht als permanente Beschriftung oder Wert für das Feld.
- **Bindungsreferenz**: Eine Bindungsreferenz ist ein Verweis auf ein Datenelement, das in einer externen Datenquelle gespeichert ist und in einem Formular verwendet wird. Sie können mit dem Bindungsverweis Daten dynamisch an Formularfelder binden, sodass das Formular die aktuellsten Daten aus der Datenquelle anzeigen kann. Beispielsweise kann ein Bindungsverweis verwendet werden, um den Namen und die Adresse von Kundinnen und Kunden in einem Formular anzuzeigen, basierend auf der im Formular eingegebenen Kunden-ID. Der Bindungsverweis kann auch verwendet werden, um die Datenquelle mit den im Formular eingegebenen Daten zu aktualisieren. Auf diese Weise können Sie mit AEM Forms Formulare erstellen, die mit externen Datenquellen interagieren und so eine nahtlose Benutzererfahrung bei der Datenerfassung und Datenverwaltung bieten.
- **Als ungebundenes Formularelement markieren**: Mit dieser Option können Sie Formularfelder konfigurieren, die mit keinem Schema verbunden sind. Mit dieser Option können Sie Daten speichern, ohne die Datenquelle zu aktualisieren. Außerdem können Sie damit Daten auf eine benutzerdefinierte Art und Weise verarbeiten, getrennt von der standardmäßigen Datenbankintegration.

- **Komponente ausblenden**: Wählen Sie diese Option, um die Komponente aus dem Formular auszublenden. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor. Dies ist nützlich, wenn Sie Informationen speichern müssen, die Benutzende nicht sehen oder direkt ändern müssen.

- **Komponente deaktivieren**: Wählen Sie die Option zum Deaktivieren der Komponente aus. Die deaktivierte Komponente ist nicht aktiv und Endbenutzende können sie nicht bearbeiten. Benutzende können den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor.

- **Schreibgeschützt**: Wählen Sie die Option aus, um die Komponente nicht bearbeitbar zu machen. Benutzende können den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor.

- **Standardwert**: Sie können mit dieser Option einen Standardwert in ein Formularfeld einfügen. Der Text verschwindet, wenn Benutzende mit der Eingabe in das Feld beginnen. Wenn **Komponente deaktiviert** oder **Schreibgeschützte Komponente** ausgewählt ist, wird der Standardwert auf dem Bildschirm angezeigt. Wenn die Benutzenden keinen Wert in das Formularfeld eingeben, wird dieser Wert zum Zeitpunkt der Formularübermittlung gesendet.

- **Mehrere Zeilen zulassen**: Benutzende können mit dieser Option mehrere Zeilen in ein Formularfeld eingeben.

- **Attribut für automatisches Ausfüllen**: Benutzende können mit dieser Option einen Wert eingeben, der im Formularfeld automatisch basierend auf den gespeicherten Informationen eingefügt wird.

### Registerkarte „Validierung“ {#validation-tab}

![Registerkarte „Validierung“](/help/adaptive-forms/assets/textinput_validationtab.png)

- **Erforderlich**: Wählen Sie diese Option, wenn Sie die Komponente in einem adaptiven Formular anzeigen möchten. Nach Auswahl der Option müssen Sie einen Wert eingeben, bevor Sie mit der Formularübermittlung fortfahren. Wenn diese Option aktiviert ist, kann die Option **Komponente ausblenden** oder **Komponente deaktivieren** auf der Registerkarte **Allgemein** nicht ausgewählt werden.

- **Fehlermeldung**: Mit dieser Option können Sie eine Nachricht eingeben, die angezeigt wird, wenn das Kontrollkästchen **Erforderlich** aktiviert ist und das Feld leer bleibt.

- **Skriptüberprüfungsmeldung**: Mit dieser Option können Sie eine Meldung eingeben, die angezeigt werden soll, wenn die Skriptüberprüfung fehlschlägt.

- **Maximale Zeichenanzahl**: Mit dieser Option können Sie die maximal zulässige Anzahl von Zeichen angeben, die in der Komponente erlaubt sind. Wenn Sie Zeichen eingeben, die größer sind als der in **Maximale Zeichenanzahl** angegebene Wert, wird eine Fehlermeldung auf dem Bildschirm angezeigt. Über das Dialogfeld **Fehlermeldung zur maximalen Zeichenanzahl** können Sie eine benutzerdefinierte Fehlermeldung hinzufügen.

- **Fehlermeldung zur maximalen Zeichenanzahl**: Über das Dialogfeld **Fehlermeldung zur maximalen Zeichenanzahl** können Sie eine benutzerdefinierte Fehlermeldung einfügen, wenn Sie mehr Zeichen eingeben, als in der Option **Maximale Zeichenanzahl** erlaubt.

- **Mindestanzahl von Zeichen**: Mit dieser Option können Sie die zulässige Mindestanzahl von Zeichen im Feld angeben. Wenn Sie Zeichen eingeben, die kleiner sind als der Wert in **Mindestanzahl von Zeichen**, wird eine Fehlermeldung auf dem Bildschirm angezeigt. Über das Dialogfeld **Fehlermeldung zur Mindestanzahl von Zeichen** können Sie eine benutzerdefinierte Fehlermeldung hinzufügen.

- **Fehlermeldung zur Mindestanzahl von Zeichen**: Über das Dialogfeld **Fehlermeldung zur Mindestanzahl von Zeichen** können Sie eine benutzerdefinierte Fehlermeldung hinzufügen, wenn Sie weniger Zeichen eingeben, als der in der Option **Mindestanzahl von Zeichen** angegebene Wert.

Die Option **Überprüfungsmuster** ermöglicht die Eingabe eines Musters zur Überprüfung des eingegebenen Texts. Falls der Text nicht mit dem in der Option **Muster** eingegebenen Wert übereinstimmt, wird die Fehlermeldung auf dem Bildschirm angezeigt.

- **Muster**: Mit dieser Option können Sie die zulässigen Überprüfungsmuster für Text eingeben. Reguläre Ausdrücke sind ebenfalls zulässig.

- **Fehlermeldung**: Sie können mit dieser Option eine Nachricht eingeben, die auf dem Bildschirm erscheint, wenn der eingegebene Text nicht mit dem in der Option **Muster** übereinstimmt

### Registerkarte „Hilfe-Inhalt“ {#help-content-tab}

![Registerkarte „Hilfe-Inhalt“](/help/adaptive-forms/assets/textinput_helptab.png)

- **Kurzbeschreibung**: Eine Kurzbeschreibung ist eine kurze Erklärung, die zusätzliche Informationen oder Klarstellungen über den Zweck eines Formularfelds bietet. Es hilft Benutzenden zu verstehen, welcher Datentyp in das Feld eingegeben werden soll, und kann Richtlinien oder Beispiele bereitstellen, um sicherzustellen, dass die eingegebenen Informationen gültig sind und die gewünschten Kriterien erfüllen. Standardmäßig bleiben kurze Beschreibungen ausgeblendet. Aktivieren Sie die Option **Kurzbeschreibung immer anzeigen**, um sie unterhalb der Komponente anzuzeigen.

- **Kurzbeschreibung immer anzeigen**: Aktivieren Sie diese Option, um die Kurzbeschreibung unterhalb der Komponente anzuzeigen.

- **Hilfetext**: Hilfetext bezieht sich auf zusätzliche Informationen oder Anleitungen, die den Benutzenden bereitgestellt werden, um sie beim korrekten Ausfüllen eines Formularfelds zu unterstützen. Er erscheint, wenn Benutzende auf das Hilfesymbol (i) neben der Komponente klicken. Hilfetext enthält detailliertere Informationen als die Beschriftung oder der Platzhaltertext eines Formularfelds und soll den Benutzenden dabei helfen, die Anforderungen oder Einschränkungen des Felds zu verstehen. Er kann auch Vorschläge oder Beispiele anbieten, um das Ausfüllen des Formulars einfacher und genauer zu gestalten.

### Registerkarte „Barrierefreiheit“ {#accessibility-tab}

![Registerkarte „Barrierefreiheit“](/help/adaptive-forms/assets/textinput_accessibiltytab.png)

- **Text für Bildschirmlesehilfen** – Das ist zusätzlicher Text, der von Hilfstechnologien wie etwa Bildschirmlesehilfen für sehbehinderte Personen vorgelesen wird. Dieser Text enthält eine Audiobeschreibung des Zwecks des Formularfelds und kann Informationen über den Titel, die Beschreibung, den Namen und alle relevanten Nachrichten (benutzerdefinierten Text) des Felds enthalten. Der Text der Bildschirmlesehilfe hilft sicherzustellen, dass das Formular allen Benutzenden zugänglich ist, auch Personen mit Sehschwäche, und bietet ihnen ein umfassendes Verständnis des Formularfelds und seiner Anforderungen.
   - **Benutzerdefinierter Text**: Wählen Sie diese Option aus, um den benutzerdefinierten Text für ARIA-Barrierefreiheitsbeschriftungen zu verwenden. Wenn Sie diese Option auswählen, wird das Benutzerdefinierter Dialogfeld „Text“ angezeigt. Sie können relevante Informationen im Benutzerdefinierter Dialogfeld „Text“ hinzufügen.
   - **Beschreibung**: Wählen Sie diese Option aus, um die Beschreibung für ARIA-Barrierefreiheitsbeschriftungen zu verwenden.
   - **Titel**: Wählen Sie diese Option aus, um den Titel für ARIA-Barrierefreiheitsbeschriftungen zu verwenden.
   - **Name**: Wählen Sie diese Option aus, um den Namen für ARIA-Barrierefreiheitsbeschriftungen zu verwenden.
   - **Keine**: Wählen Sie diese Option aus, wenn Sie keine ARIA-Barrierefreiheitsbezeichnungen hinzufügen möchten.

## Dialogfeld „Design“ {#design-dialog}

Das Dialogfeld „Design“ wird verwendet, um CSS-Stile für die Komponente „Textfeld“ zu definieren und zu verwalten.

### Registerkarte „Stile“ {#styles-tab}

Sie können die Registerkarte zum Definieren und Verwalten von CSS-Stilen für eine Komponente verwenden. Die Kernkomponente „Textfeld“ für adaptive Formulare unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).

![Registerkarte „Stile“](/help/adaptive-forms/assets/datepicker_styletab.png)

- **Standard-CSS-Klassen**: Sie können eine standardmäßige CSS-Klasse für die Textfeld-Kernkomponente für adaptive Formulare bereitstellen.

- **Zulässige Stile**: Sie können Stile definieren, indem Sie den Namen und die CSS-Klasse für den Stil angeben. Sie können beispielsweise einen Stil mit dem Namen „Fettschrift“ erstellen und die CSS-Klasse „Schriftbreite: Fett“ bereitstellen. Sie können diese Stile bei einem adaptiven Formular im adaptiven Formular-Editor anwenden. Um einen Stil anzuwenden, wählen Sie im Editor für adaptive Formulare die Komponente aus, auf die Sie den Stil anwenden möchten, navigieren Sie zum Eigenschaften-Dialog und wählen Sie den gewünschten Stil aus der Dropdown-Liste **Stile**. Wenn Sie die Stile aktualisieren oder ändern müssen, kehren Sie einfach zum Dialogfeld „Design“ zurück, aktualisieren die Stile auf der Registerkarte „Stile“ und speichern die Änderungen.

### Benutzerdefinierte Eigenschaften

![Dialogfeld „Benutzerdefinierte Eigenschaften“](/help/adaptive-forms/assets/datepicker_customproperties.png)

Mit der Option „Benutzerdefinierte Eigenschaften“ können Sie mithilfe der Formularvorlage benutzerdefinierte Attribute (Schlüsselwertpaare) mit einer Kernkomponente eines adaptiven Formulars verknüpfen. Die benutzerdefinierten Eigenschaften werden im Eigenschaftenbereich der Headless-Ausgabedarstellung der Komponente angezeigt. So kann ein dynamisches Formularverhalten erzeugt werden, das sich je nach den benutzerdefinierten Attributwerten anpasst. Beispielsweise können Entwickelnde verschiedene Ausgabedarstellungen einer Headless-Formularkomponente für Mobile-, Desktop- oder Web-Plattformen entwerfen und so das Benutzererlebnis auf einer Vielzahl von Geräten erheblich verbessern.

- **Gruppenname**: Sie können einen Namen angeben, um die Gruppe der benutzerdefinierten Eigenschaften zu kennzeichnen. Sie können mehrere Gruppen benutzerdefinierter Eigenschaften hinzufügen, löschen oder neu anordnen. Nach dem Hinzufügen der Gruppe benutzerdefinierter Eigenschaften werden folgende Optionen angezeigt:

   - **Schlüssel-Wert-Paare**: Sie können mehrere Namen und Werte benutzerdefinierter Eigenschaften hinzufügen, indem Sie für jede Gruppe benutzerdefinierter Eigenschaften auf **Hinzufügen** klicken.

   - **Löschen**: Tippen oder klicken Sie auf diese Option, um den Namen und den Wert der benutzerdefinierten Eigenschaft zu löschen.

   - **Neu anordnen**: Ordnen Sie den Namen und Wert der benutzerdefinierten Eigenschaft Antippen oder Klicken und Ziehen neu an.

### Registerkarte „Formate“ {#formats-tab}

Auf der Registerkarte „Formate“ können Sie standardmäßige und benutzerdefinierte Datumsformate angeben.

![Registerkarte „Format“](/help/adaptive-forms/assets/emailinput_formattab.png)

<!--

## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html)

-->

## Ähnliche Artikel {#related-articles}

{{more-like-this}}

## Siehe auch {#see-also}

{{see-also}}
