---
title: Kernkomponente „Dropdown-Liste“ für adaptive Formulare
description: Verwenden oder Anpassen der Dropdown-Kernkomponente adaptiver Formulare.
role: Architect, Developer, Admin, User
exl-id: 9d59d0d2-d38f-4ed5-8b43-984c45f26f27
source-git-commit: ad3e3bca5cb46f14e864e4704c90ac3b62779794
workflow-type: tm+mt
source-wordcount: '1767'
ht-degree: 99%

---

# Dropdown-Liste {#drop-down-list-adaptive-forms-core-component}

Benutzende können über eine Dropdown-Liste in einem adaptiven Formular eine oder mehrere Optionen aus einer Liste vordefinierter Optionen auswählen. Die Optionen können vom Typ „Zeichenfolge“, „Zahl“ oder „Boolesch“ sein. Darüber hinaus können Sie die Komponente „Dropdown-Liste“ so konfigurieren, dass sie unterschiedliche Validierungswerte und Standardwerte aufweist.

**Beispiel**
![](/help/adaptive-forms/assets/drop-down-list.png)

## Verwendung {#reasons-to-use-drop-down-list}

Es gibt verschiedene Gründe, warum es sinnvoll sein kann, eine Dropdown-Liste in ein adaptives Formular einzufügen, darunter:

* **Lange Liste von Optionen**: Dropdown-Listen sind nützlich in Situationen, in denen für ein Feld eine lange Liste von Optionen verfügbar ist. Sie nehmen im Formular weniger Platz ein als eine Liste von Optionsschaltflächen oder Kontrollkästchen und sind für Benutzende weniger verwirrend.

* **Konsistenz**: Mit Dropdown-Listen wird das Design und Layout eines Formulars konsistenter, wodurch die Navigation für Benutzende intuitiver und einfacher wird.

* **Klarheit**: Dropdown-Listen können das Formular übersichtlicher und verständlicher machen, indem eine klare und knappe Liste von Optionen bereitgestellt wird.

* **Benutzererlebnis**: Sie können Dropdown-Listen verwenden, um das Formular benutzerfreundlicher zu gestalten, indem eine klare und intuitive Möglichkeit zur Auswahl von Optionen bereitgestellt wird.

* **Datenanalyse**: Dropdown-Listen können verwendet werden, um Daten aus verschiedenen Quellen zu sammeln und zu analysieren oder sie als Eingabe für die weitere Verarbeitung zu verwenden.


**Dialogfeld „Eigenschaften“**

![](/help/adaptive-forms/assets/drop-down-list-properties.png)

In diesem Beispiel wird das Element „Optionen“ verwendet, um die Listenelemente zu definieren. Im Feld **Text anzeigen** können Sie eine Beschriftung für die Listenelemente und im Feld **Datenwert** einen Wert eingeben. Dieser wird bei der Übermittlung des Formulars an den Server gesendet.

Jede Option der Dropdown-Liste verfügt über einen eindeutigen Datenwert und ein eindeutiges Attribut für den angezeigten Text. Wenn Benutzende die Option „Rot“ auswählen, wird der entsprechende Datenwert beim Übermitteln des Formulars an den Server gesendet. Diese Daten können dann von einem server-seitigen Skript verarbeitet werden, um zu bestimmen, welche Optionen von Benutzenden ausgewählt wurden, und können für verschiedene Aktionen verwendet werden, z. B. zum Aktualisieren anderer Felder im Formular oder zum Senden der Formulardaten an ein server-seitiges Skript zur weiteren Verarbeitung.

Zusätzlich können Sie die Dropdown-Liste so konfigurieren, dass für jede Option unterschiedliche Verarbeitungswerte verwendet werden. Verwenden Sie dazu den Regeleditor für adaptive Formulare.

## Version und Kompatibilität {#version-and-compatibility}

Die Kernkomponente „Akkordeon“ für adaptive Formulare wurde im Februar 2023 als Teil der Kernkomponenten 2.0.4 für Cloud Service und der Kernkomponenten 1.1.12 für AEM 6.5.16.0 Forms oder höher veröffentlicht. Hier finden Sie eine Tabelle mit allen unterstützten Versionen, AEM-Kompatibilität und Links zur entsprechenden Dokumentation:

| Komponentenversion | AEM as a Cloud Service | AEM 6.5.16.0 Forms oder höher |
|---|---|---|
| v1 | Kompatibel mit<br>[Version 2.0.4](/help/adaptive-forms/version.md) und höher | Kompatibel mit<br>[Version 1.1.12](/help/adaptive-forms/version.md) und höher (aber nur bis Version 2.0.0). |

Informationen zu Versionen und Freigaben der Kernkomponente finden Sie im Dokument [Kernkomponenten-Versionen](/help/adaptive-forms/version.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technische Details {#technical-details}

Erfahren Sie die neuesten Informationen zur Kernkomponente „Dropdown-Liste“ für adaptive Formulare in der technischen Dokumentation auf [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/dropdown/v1/dropdown). Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Entwicklerdokumentation für Kernkomponenten](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Im Dialogfeld zum Konfigurieren der Dropdown-Liste finden Sie allgemeine Optionen zum Anpassen. Sie können auch Optionen für Dropdown-Listen definieren, um das Benutzererlebnis zu verbessern.

![Registerkarte „Allgemein“](/help/adaptive-forms/assets/dropdown_basictab.png)

* **Name**: Sie können eine Formularkomponente sowohl im Formular als auch im Regeleditor durch ihren eindeutigen Namen identifizieren. Der Name darf keine Leerzeichen oder Sonderzeichen enthalten.

* **Titel** – Mit dem Titel können Sie eine Komponente in einem Formular leicht identifizieren. Standardmäßig wird der Titel oberhalb der Komponente angezeigt. Wenn Sie keinen Titel hinzufügen, wird der Name der Komponente anstelle des Titeltexts angezeigt.

* **Titel ausblenden**: Wählen Sie diese Option aus, um den Titel der Komponente auszublenden.

* **Mehrfachauswahl zulassen** – Wählen Sie diese Option aus, um die Auswahl mehrerer Optionen aus einer Dropdown-Liste zuzulassen.

* **Wert speichern unter** – Diese Option gibt den Datentyp des Werts an, der bei Auswahl einer Option gesendet wird. Wenn **Wert speichern unter** auf `Number` gesetzt ist, und Sie auf der Registerkarte **Optionen** zum **Datenwert** Zeichenfolgendaten hinzufügen, wird auf dem Bildschirm die Fehlermeldung `Value type mismatch` angezeigt.

  Auf der Registerkarte **Optionen** können Sie Datenwerte hinzufügen und Textpaare anzeigen, indem Sie die Schaltfläche **Hinzufügen** verwenden. Nachdem eine neue Option hinzugefügt wurde, werden die folgenden Aktionen ausgeführt:

   * **Datenwert** – Sie können mit dieser Option den zu sendenden Inhalt eingeben, wenn eine Option ausgewählt ist.
   * **Text anzeigen** – Sie können mit dieser Option den Inhalt eingeben, der in einem adaptiven Formular angezeigt werden soll.
   * **Löschen** – Durch Tippen bzw. Klicken können Sie eine Option eines Dropdown-Menüs löschen.
   * **Neu anordnen** – Durch Tippen bzw. Klicken und Ziehen können Sie die Reihenfolge der Optionen eines Dropdown-Menüs neu anordnen.

* **Standardoptionen** – Sie können mit dieser Option Standardwerte hinzufügen. Mit dem Löschen-Symbol können Sie eine hinzugefügte Option entfernen. Wenn **Wert speichern unter** auf `Number` gesetzt ist und Sie Zeichenfolgendaten zu **Standardoptionen** hinzufügen, wird auf dem Bildschirm die Feldermeldung `Value type mismatch` angezeigt.

* **Platzhaltertext**: Platzhaltertext in einer Formularkomponente ist eine kurze Beschriftung oder Eingabeaufforderung innerhalb eines Eingabefelds, die Benutzende darüber informiert, welche Art von Text in dieses Feld eingegeben werden soll. Der Platzhaltertext verschwindet, wenn Benutzende mit der Eingabe in das Feld beginnen, und erscheint wieder, wenn das Feld leer bleibt. Er stellt einen visuellen Hinweis für Benutzende bereit, fungiert jedoch nicht als permanente Beschriftung oder Wert für das Feld.

* **Bindungsverweis**: Bindungsverweis ist ein Verweis auf ein Datenelement, das in einer externen Datenquelle gespeichert ist und in einem Formular verwendet wird. Sie können mit dem Bindungsverweis Daten dynamisch an Formularfelder binden, sodass das Formular die aktuellsten Daten aus der Datenquelle anzeigen kann. Beispielsweise kann ein Bindungsverweis verwendet werden, um den Namen und die Adresse von Kundinnen und Kunden in einem Formular anzuzeigen, basierend auf der im Formular eingegebenen Kunden-ID. Der Bindungsverweis kann auch verwendet werden, um die Datenquelle mit den im Formular eingegebenen Daten zu aktualisieren. Auf diese Weise können Sie mit AEM Forms Formulare erstellen, die mit externen Datenquellen interagieren und so eine nahtlose Benutzererfahrung bei der Datenerfassung und Datenverwaltung bieten.

* **Komponente ausblenden**: Wählen Sie die Option, um die Komponente aus dem Formular auszublenden. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor. Dies ist nützlich, wenn Sie Informationen speichern müssen, die Benutzende nicht sehen oder direkt ändern müssen.
* **Komponente deaktivieren**: Wählen Sie die Option zum Deaktivieren der Komponente aus. Die deaktivierte Komponente ist nicht aktiv und Endbenutzende können sie nicht bearbeiten. Benutzende können den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor.
* **Schreibgeschützt**: Wählen Sie die Option aus, um die Komponente nicht bearbeitbar zu machen. Benutzende können den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor.

### Registerkarte „Validierung“ {#validation-tab}

![Registerkarte „Validierung“](/help/adaptive-forms/assets/dropdown_validationtab.png)

* **Erforderlich**: Wählen Sie diese Option, wenn Sie die Komponente in einem adaptiven Formular anzeigen möchten. Wenn diese Option aktiviert ist, kann die Option **Komponente ausblenden** oder **Komponente deaktivieren** auf der Registerkarte **Allgemein** nicht ausgewählt werden.

* **Fehlermeldung**: Mit dieser Option können Sie eine Nachricht eingeben, die angezeigt wird, wenn das Kontrollkästchen **Erforderlich** aktiviert ist und das Feld leer bleibt.

* **Meldung zur Skriptvalidierung**: Mit dieser Option können Sie eine Meldung eingeben, die angezeigt werden soll, wenn die Skriptvalidierung fehlschlägt.

### Registerkarte „Hilfe-Inhalt“ {#help-content-tab}

![Registerkarte „Hilfe-Inhalt“](/help/adaptive-forms/assets/dropdown_helptab.png)

* **Kurzbeschreibung**: Eine Kurzbeschreibung ist eine kurze Erklärung, die zusätzliche Informationen oder Klarstellungen über den Zweck eines Formularfelds bietet. Es hilft Benutzenden zu verstehen, welcher Datentyp in das Feld eingegeben werden soll, und kann Richtlinien oder Beispiele bereitstellen, um sicherzustellen, dass die eingegebenen Informationen gültig sind und die gewünschten Kriterien erfüllen. Standardmäßig bleiben kurze Beschreibungen ausgeblendet. Aktivieren Sie die Option **Kurzbeschreibung immer anzeigen**, um sie unterhalb der Komponente anzuzeigen.

* **Kurzbeschreibung immer anzeigen**: Aktivieren Sie diese Option, um die Kurzbeschreibung unterhalb der Komponente anzuzeigen.

* **Hilfetext**: Hilfetext bezieht sich auf zusätzliche Informationen oder Anleitungen, die den Benutzenden bereitgestellt werden, um sie beim korrekten Ausfüllen eines Formularfelds zu unterstützen. Er erscheint, wenn Benutzende auf das Hilfesymbol (i) neben der Komponente klicken. Hilfetext enthält detailliertere Informationen als die Beschriftung oder der Platzhaltertext eines Formularfelds und soll den Benutzenden dabei helfen, die Anforderungen oder Einschränkungen des Felds zu verstehen. Er kann auch Vorschläge oder Beispiele anbieten, um das Ausfüllen des Formulars einfacher und genauer zu gestalten.

### Registerkarte „Barrierefreiheit“ {#accessibility-tab}

![Registerkarte „Barrierefreiheit“](/help/adaptive-forms/assets/dropdown_accessibilitytab.png)


**Text für Bildschirmlesehilfen** – Das ist zusätzlicher Text, der von Hilfstechnologien wie etwa Bildschirmlesehilfen für sehbehinderte Personen vorgelesen wird. Dieser Text enthält eine Audiobeschreibung des Zwecks des Formularfelds und kann Informationen über den Titel, die Beschreibung, den Namen und alle relevanten Nachrichten (benutzerdefinierten Text) des Felds enthalten. Der Text der Bildschirmlesehilfe hilft sicherzustellen, dass das Formular allen Benutzenden zugänglich ist, auch Personen mit Sehschwäche, und bietet ihnen ein umfassendes Verständnis des Formularfelds und seiner Anforderungen.


## Dialogfeld „Design“ {#design-dialog}

Verwenden Sie das Design-Dialogfeld, um CSS-Stile für die Dropdown-Listenkomponente zu definieren und zu verwalten.

### Registerkarte „Stile“ {#styles-tab}

Sie können die Registerkarte zum Definieren und Verwalten von CSS-Stilen für eine Komponente verwenden. Die Kernkomponente „Dropdown-Liste“ für adaptive Formulare unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).

![Dropdown-Dialogfeld](/help/adaptive-forms/assets/dropdown_designdialog.png)

* **Standard-CSS-Klassen**: Sie können eine standardmäßige CSS-Klasse für die Kernkomponente „Dropdown-Liste“ für adaptive Formulare bereitstellen.

* **Zulässige Stile**: Sie können Stile definieren, indem Sie den Namen und die CSS-Klasse für den Stil angeben. Sie können beispielsweise einen Stil mit dem Namen „Fettschrift“ erstellen und die CSS-Klasse „Schriftbreite: Fett“ bereitstellen. Sie können diese Stile bei einem adaptiven Formular im adaptiven Formular-Editor anwenden. Um einen Stil anzuwenden, wählen Sie im Editor für adaptive Formulare die Komponente aus, auf die Sie den Stil anwenden möchten, navigieren Sie zum Eigenschaften-Dialog und wählen Sie den gewünschten Stil aus der Dropdown-Liste **Stile**. Wenn Sie die Stile aktualisieren oder ändern müssen, kehren Sie einfach zum Dialogfeld „Design“ zurück, aktualisieren die Stile auf der Registerkarte „Stile“ und speichern die Änderungen.

## Verwandter Artikel {#related-article}

* [Erstellen eines adaptiven Formulars in einer AEM Sites-Seite oder einem Experience Fragment](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=de)

* [Erstellen eines eigenständigen adaptiven Formulars](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html?lang=de)


## Siehe auch {#see-also}

* [Akkordeon](/help/adaptive-forms/components/accordion.md)
* [Schaltfläche](/help/adaptive-forms/components/button.md)
* [Kontrollkästchen Gruppe](/help/adaptive-forms/components/checkbox-group.md)
* [Datumsauswahl](/help/adaptive-forms/components/date-picker.md)
* [E-Mail-Eingabe](/help/adaptive-forms/components/email-input.md)
* [Formular-Container](/help/adaptive-forms/components/form-container.md)
* [Dateianhang](/help/adaptive-forms/components/file-attachment.md)
* [Fußzeile](/help/adaptive-forms/components/footer.md)
* [Kopfzeile](/help/adaptive-forms/components/header.md)
* [Horizontale Registerkarten](/help/adaptive-forms/components/horizontal-tabs.md)
* [Bild](/help/adaptive-forms/components/image.md)
* [Zahleneingabe](/help/adaptive-forms/components/number-input.md)
* [Bedienfeld-Container](/help/adaptive-forms/components/panel-container.md)
* [Optionsschaltfläche](/help/adaptive-forms/components/radio-button.md)
* [Schaltfläche „Zurücksetzen“](/help/adaptive-forms/components/reset-button.md)
* [Schaltfläche „Senden“](/help/adaptive-forms/components/submit-button.md)
* [Telefoneingabe](/help/adaptive-forms/components/telephone-input.md)
* [Texteingabe](/help/adaptive-forms/components/text-input.md)
* [Text](/help/adaptive-forms/components/text.md)
* [Titel](/help/adaptive-forms/components/title.md)
* [Assistent](/help/adaptive-forms/components/wizard.md)