---
title: Kernkomponente „Telefoneingabe“ für adaptive Formulare
description: Verwenden oder Anpassen der Kernkomponente „Telefoneingabe“ für adaptive Formulare.
role: Architect, Developer, Admin, User
exl-id: d06179ac-04bd-4af4-b6ac-c4c78086058c
source-git-commit: 0bebc248ee2b708f7677950d90356abd5bc70a98
workflow-type: tm+mt
source-wordcount: '1793'
ht-degree: 100%

---

# Telefoneingabe {#telephone-input-adaptive-forms-core-component}

Mit der Kernkomponente „Telefoneingabe“ für adaptive Formulare können Benutzende eine Telefonnummer eingeben. Im Telefoneingabefeld werden Tastaturen von Mobilgeräten angezeigt, die für Telefonnummern relevant sind. Zur Spezifikation des Formats und der Beschreibung der Telefonnummer können zusätzliche Attribute wie „Muster“ und „Platzhalter“ verwendet werden.

Das Telefoneingabefeld wird häufig in Kontakt-, Registrierungs- und anderen Formularen verwendet, bei denen unter den Kontaktdaten auch eine Telefonnummer angegeben werden muss. Das Telefoneingabefeld kann auch verwendet werden, um sicherzustellen, dass die Benutzenden eine gültige Telefonnummer eingeben, da der Browser bestimmte Einschränkungen vorgeben kann, z. B. die Länge und das Format der Telefonnummer entsprechend dem Attribut „Muster“.

## Verwendung {#reasons-to-use-telephone-input}

Häufige Gründe für die Verwendung eines Telefoneingabefelds in einem adaptiven Formular sind:

* **Kontaktinformationen**: Ein Telefoneingabefeld wird häufig verwendet, um die Telefonnummer von Benutzenden zur Kontaktaufnahme zu erfassen.

* **Erhöhte Datengenauigkeit**: Das Formular kann bei Verwendung eines Telefoneingabefelds bestimmte Einschränkungen hinsichtlich des Formats der Telefonnummer durchsetzen und somit dazu beitragen, dass die eingegebenen Daten korrekt und vollständig sind.

* **Besseres Benutzererlebnis**: Ein Telefoneingabefeld bietet eine klare und intuitive Möglichkeit für Benutzende, ihre Telefonnummer einzugeben und verbessert somit das Benutzererlebnis.

## Version und Kompatibilität {#version-and-compatibility}

Die Kernkomponente „Akkordeon“ für adaptive Formulare wurde im Februar 2023 als Teil der Kernkomponenten 2.0.4 für Cloud Service und der Kernkomponenten 1.1.12 für AEM 6.5.16.0 Forms oder höher veröffentlicht. Hier finden Sie eine Tabelle mit allen unterstützten Versionen, AEM-Kompatibilität und Links zur entsprechenden Dokumentation:

| Komponentenversion | AEM as a Cloud Service | AEM 6.5.16.0 Forms oder höher |
|---|---|---|
| v1 | Kompatibel mit<br>[Version 2.0.4](/help/adaptive-forms/version.md) und höher | Kompatibel mit<br>[Version 1.1.12](/help/adaptive-forms/version.md) und höher (aber nur bis Version 2.0.0). |

Informationen zu Versionen und Freigaben der Kernkomponente finden Sie im Dokument [Kernkomponenten-Versionen](/help/adaptive-forms/version.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technische Details {#technical-details}

Aktuelle Informationen zur Kernkomponente „Telefoneingabe“ für adaptive Formulare finden Sie in der technischen Dokumentation auf [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/telephoneinput/v1/telephoneinput). Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Entwicklerdokumentation für Kernkomponenten](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Im Dialogfeld „Konfigurieren“ können Sie das Telefoneingabefeld für Besuchende einfach anpassen. Sie können auch Optionen für die Telefoneingabe definieren, um das Benutzererlebnis zu verbessern.

![Registerkarte „Allgemein“](/help/adaptive-forms/assets/telephoneinput_basictab.png)

* **Name**: Sie können eine Formularkomponente sowohl im Formular als auch im Regel-Editor leicht mit ihrem eindeutigen Namen identifizieren. Der Name darf jedoch keine Leerzeichen oder Sonderzeichen enthalten.

* **Titel**: Sie können mit dem Titel leicht eine Komponente in einem Formular identifizieren. Standardmäßig wird der Titel über der Komponente angezeigt. Wenn Sie keinen Titel hinzufügen, wird der Name der Komponente anstelle des Titeltexts angezeigt.

* **Titel ausblenden**: Wählen Sie die Option aus, um den Titel der Komponente auszublenden.

* **Platzhaltertext**: Platzhaltertext in einer Formularkomponente bezieht sich auf eine kurze Beschriftung oder Eingabeaufforderung, die in einem Eingabefeld angezeigt wird, um Benutzende darauf hinzuweisen, welcher Informationstyp in dieses Feld eingegeben werden soll. Der Platzhaltertext verschwindet, wenn Benutzende mit der Eingabe in das Feld beginnen, und erscheint wieder, wenn das Feld leer bleibt. Er stellt einen visuellen Hinweis für Benutzende bereit, fungiert jedoch nicht als permanente Beschriftung oder Wert für das Feld.

* **Bindungsverweis**: Bindungsverweis ist ein Verweis auf ein Datenelement, das in einer externen Datenquelle gespeichert ist und in einem Formular verwendet wird. Sie können mit dem Bindungsverweis Daten dynamisch an Formularfelder binden, sodass das Formular die aktuellsten Daten aus der Datenquelle anzeigen kann. Beispielsweise kann ein Bindungsverweis verwendet werden, um den Namen und die Adresse von Kundinnen und Kunden in einem Formular anzuzeigen, basierend auf der im Formular eingegebenen Kunden-ID. Der Bindungsverweis kann auch verwendet werden, um die Datenquelle mit den im Formular eingegebenen Daten zu aktualisieren. Auf diese Weise können Sie mit AEM Forms Formulare erstellen, die mit externen Datenquellen interagieren und so eine nahtlose Benutzererfahrung bei der Datenerfassung und Datenverwaltung bieten.

* **Komponente ausblenden**: Wählen Sie die Option, um die Komponente aus dem Formular auszublenden. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor. Dies ist nützlich, wenn Sie Informationen speichern müssen, die Benutzende nicht sehen oder direkt ändern müssen.

* **Komponente deaktivieren**: Wählen Sie die Option zum Deaktivieren der Komponente aus. Die deaktivierte Komponente ist nicht aktiv und Endbenutzende können sie nicht bearbeiten. Benutzende können den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor.

* **Schreibgeschützt**: Wählen Sie die Option aus, um die Komponente nicht bearbeitbar zu machen. Benutzende können den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor.

* **Standardwert**: Mit dieser Option können Sie einen Standardwert in ein Formularfeld einfügen. Wenn **Komponente deaktiviert** oder **Schreibgeschützte Komponente** ausgewählt ist, wird auf dem Bildschirm der Standardwert angezeigt. Wird kein Wert in das Formularfeld eingegeben, wird bei der Formularübermittlung dieser Wert gesendet.

### Registerkarte „Validierung“ {#validation-tab}

![Registerkarte „Validierung“](/help/adaptive-forms/assets/telephoneinput_validationtab.png)

* **Erforderlich**: Wählen Sie diese Option, wenn Sie die Komponente in einem adaptiven Formular anzeigen möchten. Wenn diese Option aktiviert ist, kann die Option **Komponente ausblenden** oder **Komponente deaktivieren** auf der Registerkarte **Allgemein** nicht ausgewählt werden.

* **Fehlermeldung**: Mit dieser Option können Sie eine Nachricht eingeben, die angezeigt wird, wenn das Kontrollkästchen **Erforderlich** aktiviert ist und das Feld leer bleibt.

* **Skriptüberprüfungsmeldung**: Mit dieser Option können Sie eine Meldung eingeben, die angezeigt werden soll, wenn die Skriptüberprüfung fehlschlägt.

* **Maximale Zeichenanzahl**: Mit dieser Option können Sie die maximal zulässige Anzahl von Zeichen angeben, die in der Komponente erlaubt sind. Wenn Sie Zeichen eingeben, die größer sind als der in **Maximale Zeichenanzahl** angegebene Wert, wird eine Fehlermeldung auf dem Bildschirm angezeigt. Über das Dialogfeld **Fehlermeldung zur maximalen Zeichenanzahl** können Sie eine benutzerdefinierte Fehlermeldung hinzufügen.

* **Fehlermeldung zur maximalen Zeichenanzahl**: Über das Dialogfeld **Fehlermeldung zur maximalen Zeichenanzahl** können Sie eine benutzerdefinierte Fehlermeldung einfügen, wenn Sie mehr Zeichen eingeben, als in der Option **Maximale Zeichenanzahl** erlaubt.

* **Mindestanzahl von Zeichen**: Mit dieser Option können Sie die zulässige Mindestanzahl von Zeichen im Feld angeben. Wenn Sie Zeichen eingeben, die kleiner sind als der Wert in **Mindestanzahl von Zeichen**, wird eine Fehlermeldung auf dem Bildschirm angezeigt. Über das Dialogfeld **Fehlermeldung zur Mindestanzahl von Zeichen** können Sie eine benutzerdefinierte Fehlermeldung hinzufügen.

* *Fehlermeldung zur Mindestanzahl von Zeichen**: Im Dialogfeld **Fehlermeldung zur Mindestanzahl von Zeichen** können Sie eine benutzerdefinierte Fehlermeldung hinzufügen, die angezeigt wird, wenn weniger Zeichen eingegeben werden als die in der Option **Mindestanzahl von Zeichen** definierten.

Die Option **Überprüfungsmuster** ermöglicht die Eingabe eines Musters zur Überprüfung der eingegebenen Telefonnummer. Die eingegebene Telefonnummer wird anhand des in der Option **Muster** angegeben Werts überprüft. Falls die Überprüfung der Telefonnummer anhand des in der Option **Muster** eingegebenen Werts fehlschlägt, wird auf dem Bildschirm eine Fehlermeldung angezeigt.

* **Muster** – Mit dieser Option können Sie die zulässigen Überprüfungsmuster für Telefonnummern eingeben. Reguläre Ausdrücke sind ebenfalls zulässig.

* **Fehlermeldung**: Mit dieser Option können Sie eine Nachricht eingeben, die auf dem Bildschirm angezeigt wird, wenn die Überprüfung der eingegebenen Telefonnummer anhand des in der Option **Muster** angegebenen Werts fehlschlägt.

### Registerkarte „Hilfe-Inhalt“ {#help-content-tab}

![Registerkarte „Hilfe-Inhalt“](/help/adaptive-forms/assets/telephoneinput_helptab.png)

* **Kurzbeschreibung**: Eine Kurzbeschreibung ist eine kurze Erklärung, die zusätzliche Informationen oder Klarstellungen über den Zweck eines Formularfelds bietet. Es hilft Benutzenden zu verstehen, welcher Datentyp in das Feld eingegeben werden soll, und kann Richtlinien oder Beispiele bereitstellen, um sicherzustellen, dass die eingegebenen Informationen gültig sind und die gewünschten Kriterien erfüllen. Standardmäßig bleiben kurze Beschreibungen ausgeblendet. Aktivieren Sie die Option **Kurzbeschreibung immer anzeigen**, um sie unterhalb der Komponente anzuzeigen.

* **Kurzbeschreibung immer anzeigen**: Aktivieren Sie diese Option, um die Kurzbeschreibung unterhalb der Komponente anzuzeigen.

* **Hilfetext**: Hilfetext bezieht sich auf zusätzliche Informationen oder Anleitungen, die den Benutzenden bereitgestellt werden, um sie beim korrekten Ausfüllen eines Formularfelds zu unterstützen. Er erscheint, wenn Benutzende auf das Hilfesymbol (i) neben der Komponente klicken. Hilfetext enthält detailliertere Informationen als die Beschriftung oder der Platzhaltertext eines Formularfelds und soll den Benutzenden dabei helfen, die Anforderungen oder Einschränkungen des Felds zu verstehen. Er kann auch Vorschläge oder Beispiele anbieten, um das Ausfüllen des Formulars einfacher und genauer zu gestalten.

### Registerkarte „Barrierefreiheit“ {#accessibility-tab}

![Registerkarte „Barrierefreiheit“](/help/adaptive-forms/assets/telephoneinput_accessibilitytab.png)

**Text für Bildschirmlesehilfen** – Das ist zusätzlicher Text, der von Hilfstechnologien wie etwa Bildschirmlesehilfen für sehbehinderte Personen vorgelesen wird. Dieser Text enthält eine Audiobeschreibung des Zwecks des Formularfelds und kann Informationen über den Titel, die Beschreibung, den Namen und alle relevanten Nachrichten (benutzerdefinierten Text) des Felds enthalten. Der Text der Bildschirmlesehilfe hilft sicherzustellen, dass das Formular allen Benutzenden zugänglich ist, auch Personen mit Sehschwäche, und bietet ihnen ein umfassendes Verständnis des Formularfelds und seiner Anforderungen.

## Dialogfeld „Design“ {#design-dialog}

Das Dialogfeld „Design“ wird verwendet, um CSS-Stile für die Telefoneingabe-Komponente zu definieren und zu verwalten.

### Registerkarte „Stile“ {#styles-tab}

Sie können die Registerkarte zum Definieren und Verwalten von CSS-Stilen für eine Komponente verwenden. Die Kernkomponente „Telefoneingabe“ für adaptive Formulare unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).

![Dialogfeld „Design“](/help/adaptive-forms/assets/telephoneinput_designdialog.png)

* **Standard-CSS-Klassen**: Sie können eine Standard-CSS-Klasse für die Kernkomponente „Telefoneingabe“ für adaptive Formulare bereitstellen.

* **Zulässige Stile**: Sie können Stile definieren, indem Sie den Namen und die CSS-Klasse für den Stil angeben. Sie können beispielsweise einen Stil mit dem Namen „Fettschrift“ erstellen und die CSS-Klasse „Schriftbreite: Fett“ bereitstellen. Sie können diese Stile bei einem adaptiven Formular im adaptiven Formular-Editor anwenden. Um einen Stil anzuwenden, wählen Sie im Editor für adaptive Formulare die Komponente aus, auf die Sie den Stil anwenden möchten, navigieren Sie zum Eigenschaften-Dialog und wählen Sie den gewünschten Stil aus der Dropdown-Liste **Stile**. Wenn Sie die Stile aktualisieren oder ändern müssen, kehren Sie einfach zum Dialogfeld „Design“ zurück, aktualisieren die Stile auf der Registerkarte „Stile“ und speichern die Änderungen.

### Registerkarte „Formate“ {#format-tab}

Auf der Registerkarte „Formate“ können Sie standardmäßige und benutzerdefinierte Zahlenformate angeben.

![Registerkarte „Formate“](/help/adaptive-forms/assets/telephoneinput_format.png)

## Verwandter Artikel {#related-article}

* [Erstellen eines adaptiven Formulars in einer AEM Sites-Seite oder einem Experience Fragment](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=de)

* [Erstellen eines eigenständigen adaptiven Formulars](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html?lang=de)


>[!MORELIKETHIS]
>
>* [Akkordeon](/help/adaptive-forms/components/accordion.md)
>* [Schaltfläche](/help/adaptive-forms/components/button.md)
>* [Kontrollkästchen „Gruppe“](/help/adaptive-forms/components/checkbox-group.md)
>* [Datumsauswahl](/help/adaptive-forms/components/date-picker.md)
>* [Dropdown-Liste](/help/adaptive-forms/components/drop-down.md)
>* [E-Mail-Eingabe](/help/adaptive-forms/components/email-input.md)
>* [Formular-Container](/help/adaptive-forms/components/form-container.md)
>* [Dateianhang](/help/adaptive-forms/components/file-attachment.md)
>* [Fußzeile](/help/adaptive-forms/components/footer.md)
>* [Kopfzeile](/help/adaptive-forms/components/header.md)
>* [Horizontale Registerkarten](/help/adaptive-forms/components/horizontal-tabs.md)
>* [Bild](/help/adaptive-forms/components/image.md)
>* [Zahleneingabe](/help/adaptive-forms/components/number-input.md)
>* [Bedienfeld-Container](/help/adaptive-forms/components/panel-container.md)
>* [Optionsschaltfläche](/help/adaptive-forms/components/radio-button.md)
>* [Schaltfläche „Zurücksetzen“](/help/adaptive-forms/components/reset-button.md)
>* [Schaltfläche „Senden“](/help/adaptive-forms/components/submit-button.md)
>* [Texteingabe](/help/adaptive-forms/components/text-input.md)
>* [Text](/help/adaptive-forms/components/text.md)
>* [Titel](/help/adaptive-forms/components/title.md)
>* [Assistent](/help/adaptive-forms/components/wizard.md)

## Siehe auch {#see-also}

{{see-also}}