---
title: Kernkomponente „Optionsschaltfläche“ für adaptive Formulare
description: Verwenden oder Anpassen der Kernkomponente „Optionsschaltfläche“ für adaptive Formulare.
role: Architect, Developer, Admin, User
exl-id: 86b5e9ec-58ac-4cd5-9c7c-4269247ec34f
source-git-commit: 6725784bd4c94d433c91d6bd65d14d03cbefd954
workflow-type: ht
source-wordcount: '2135'
ht-degree: 100%

---


# Optionsschaltflächen-Komponente {#radio-button-adaptive-forms-core-component}

Eine Optionsschaltfläche in einem adaptiven Formular ist eine Art Eingabeelement, mit dem Benutzende eine Option aus einer Gruppe verwandter Optionen auswählen können. Sie wird durch eine kleine kreisförmige Schaltfläche dargestellt, die entweder ausgefüllt oder leer ist, um anzugeben, ob die Option ausgewählt ist oder nicht. Wenn Benutzende eine Optionsschaltfläche auswählen, werden die anderen in der Gruppe deaktiviert. Optionsschaltflächen werden in der Regel verwendet, wenn mehrere sich gegenseitig ausschließende Optionen bestehen und jeweils nur eine gleichzeitig ausgewählt werden kann.

{{traditional-aem}}

**Beispiel**

![Beispiel](/help/adaptive-forms/assets/radio-button.png)

**Dialogfeld „Eigenschaften“**

![Beispiel](/help/adaptive-forms/assets/radio-button-properties.png)

In diesem Beispiel wird das Optionenelement verwendet, um die Optionsschaltflächen in einer Gruppe zusammenzufassen. Sie können das Element **Text anzeigen** verwenden, um eine Beschriftung für ein Element bereitzustellen und **Datenwert** verwenden, um den Wert anzugeben, der beim Senden des Formulars an den Server gesendet wird.

Jede Optionsschaltflächen-Option verfügt über einen eindeutigen Datenwert und ein eigenes Textanzeige-Attribut. Wenn Benutzende „1–10“ auswählen, wird der entsprechende Datenwert beim Absenden des Formulars an den Server gesendet. Diese Daten können dann von einem server-seitigen Skript verarbeitet werden, um zu bestimmen, welche Optionen von Benutzenden ausgewählt wurden, und können für verschiedene Aktionen verwendet werden, z. B. zum Aktualisieren anderer Felder im Formular oder zum Senden der Formulardaten an ein server-seitiges Skript zur weiteren Verarbeitung.

Darüber hinaus kann jede Optionsschaltfläche so konfiguriert werden, dass für jede Option unterschiedliche Verarbeitungswerte vorhanden sind. Dies kann mithilfe des Regeleditors für adaptive Formulare festgelegt werden

## Verwendung {#reasons-to-use-radio-button}

Es gibt verschiedene Gründe für die Verwendung von Optionsschaltflächen in einem Formular, darunter:

- **Eingeschränkung der Auswahl**: Optionsschaltflächen werden verwendet, um eine Liste vordefinierter Optionen bereitzustellen, aus denen die Benutzenden auswählen können. Es kann jeweils nur eine Option gleichzeitig ausgewählt werden. Dies ist nützlich, wenn die Anzahl der Optionen begrenzt ist und diese sich gegenseitig ausschließen.

- **Übersichtliche Darstellung**: Optionsschaltflächen sind übersichtlich und leicht zu verstehen, sodass die Auswahl für Benutzende vereinfacht wird.

- **Konsistenz**: Die Verwendung von Optionsschaltflächen ist eine konsistente und standardisierte Methode zur Darstellung von Optionen für Benutzende, wodurch das Verständnis und die Interaktion mit dem Formular erleichtert werden.

- **Einfachere Verwendung**: Optionsschaltflächen sind einfach zu bedienen, insbesondere für Benutzende, die nicht technologieaffin sind oder die über eingeschränkte Mobilität verfügen.

## Version und Kompatibilität {#version-and-compatibility}

Die Kernkomponente für Optionsfelder in adaptiven Formularen wurde im Februar 2023 als Teil der Kernkomponenten 2.0.4 für Cloud Service und der Kernkomponenten 1.1.12 für AEM 6.5.16.0 Forms oder höher veröffentlicht. Hier finden Sie eine Tabelle mit allen unterstützten Versionen, AEM-Kompatibilität und Links zur entsprechenden Dokumentation:

| Komponentenversion | AEM as a Cloud Service | AEM 6.5.16.0 Forms oder höher |
|---|---|---|
| v1 | Kompatibel mit<br>[Version 2.0.4](/help/adaptive-forms/version.md) und höher | Kompatibel mit<br>[Version 1.1.12](/help/adaptive-forms/version.md) und höher (aber nur bis Version 2.0.0). |

Informationen zu Versionen und Freigaben der Kernkomponente finden Sie im Dokument [Kernkomponenten-Versionen](/help/adaptive-forms/version.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion_de). -->

## Technische Details {#technical-details}

Aktuelle Informationen zur Kernkomponente „Optionsschaltfläche“ für adaptive Formulare finden Sie in der technischen Dokumentation auf [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/radiobutton/v1/radiobutton). Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Entwicklerdokumentation für Kernkomponenten](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Im Dialogfeld „Konfigurieren“ können Sie Optionsschaltflächen für Besuchende einfach anpassen. Durch die Definition von Optionsschaltflächen-Optionen können Sie ein nahtloses Benutzererlebnis gewährleisten.

### Registerkarte „Allgemein“

![Registerkarte „Allgemein“](/help/adaptive-forms/assets/radiobutton_basictab.png)

- **Name**: Sie können eine Formularkomponente sowohl im Formular als auch im Regeleditor durch ihren eindeutigen Namen identifizieren. Der Name darf keine Leerzeichen oder Sonderzeichen enthalten.

- **Titel**: Mit dem Titel können Sie eine Komponente in einem Formular leicht identifizieren. Standardmäßig wird der Titel oberhalb der Komponente angezeigt. Wenn Sie keinen Titel hinzufügen, wird der Name der Komponente anstelle des Titeltexts angezeigt.
- **Rich-Text für Titel zulassen**: Diese Funktionen ermöglichen es Benutzenden, einfache Texttitel zu formatieren, die Funktionen wie fett, kursiv, unterstrichener Text, verschiedene Schriftarten, Schriftgrößen, Farben und zusätzliche Optionen enthalten und so die visuelle Darstellung und Anpassung zu verbessern. Sie bietet mehr Flexibilität und kreative Kontrolle bei der Hervorhebung von Titeln in Dokumenten, Websites oder Anwendungen.\
  Durch Aktivieren des Kontrollkästchens **Rich-Text für Titel zulassen** werden Formatierungsoptionen sichtbar, mit denen Sie den Titel der Komponente gestalten können. Um auf alle verfügbaren Formatierungsoptionen zuzugreifen, können Sie auf die Registerkarte ![Vollbildsymbol](/help/adaptive-forms/assets/fullscreen-icon.png) klicken.

  ![Rich-Text-Unterstützung](/help/adaptive-forms/assets/richtext-support-title.png)

- **Titel ausblenden**: Wählen Sie die Option aus, um den Titel der Komponente auszublenden.

- **Optionen**: Sie können Datenwerte hinzufügen und Textpaare anzeigen, indem Sie die Schaltfläche **Hinzufügen** verwenden.\
  Nachdem eine neue Option hinzugefügt wurde, können die folgenden Aktionen ausgeführt werden:
   - **Datenwert**: Mit dieser Option können Sie den zu sendenden Inhalt eingeben, wenn eine Option ausgewählt ist.
   - **Text anzeigen** – Mit dieser Option können Sie den Inhalt eingeben, der in einem adaptiven Formular angezeigt werden soll.
   - **Löschen** – Durch Tippen oder Klicken können Sie die Option einer Optionsschaltfläche löschen.
   - **Neu anordnen**: Durch Tippen oder Klicken und Ziehen können Sie die Anordnung der Optionen anpassen.
Sie können die Optionen für die Optionsfeldgruppe auch mit **Rich-Text für Optionen zulassen** formatieren.

  ![Rich-Text-Unterstützung für Optionen](/help/adaptive-forms/assets/richtext-for-options.png)

  Sobald Sie das Kontrollkästchen **Rich-Text für Optionen zulassen** aktivieren, werden Formatierungsoptionen sichtbar, um die Optionen der Komponente zu gestalten. Um auf alle verfügbaren Formatierungsoptionen zuzugreifen, können Sie auf die Registerkarte `Fullscreen` ![Vollbildschirmsymbol](/help/adaptive-forms/assets/fullscreen-icon.png) klicken.

  ![Rich-Text-Unterstützung für Optionen](/help/adaptive-forms/assets/richtextoptions-support.png)

- **Bindungsreferenz**: Eine Bindungsreferenz ist ein Verweis auf ein Datenelement, das in einer externen Datenquelle gespeichert ist und in einem Formular verwendet wird. Sie können mit dem Bindungsverweis Daten dynamisch an Formularfelder binden, sodass das Formular die aktuellsten Daten aus der Datenquelle anzeigen kann. Beispielsweise kann ein Bindungsverweis verwendet werden, um den Namen und die Adresse von Kundinnen und Kunden in einem Formular anzuzeigen, basierend auf der im Formular eingegebenen Kunden-ID. Der Bindungsverweis kann auch verwendet werden, um die Datenquelle mit den im Formular eingegebenen Daten zu aktualisieren. Auf diese Weise können Sie mit AEM Forms Formulare erstellen, die mit externen Datenquellen interagieren und so eine nahtlose Benutzererfahrung bei der Datenerfassung und Datenverwaltung bieten.

- **Als ungebundenes Formularelement markieren**: Mit dieser Option können Sie Formularfelder konfigurieren, die mit keinem Schema verbunden sind. Mit dieser Option können Sie Daten speichern, ohne die Datenquelle zu aktualisieren. Außerdem können Sie damit Daten auf eine benutzerdefinierte Art und Weise verarbeiten, getrennt von der standardmäßigen Datenbankintegration.

- **Datentyp des gesendeten Werts**: Diese Option gibt den Datentyp des Werts an, der bei Auswahl einer Option gesendet wird. Wenn der **Datentyp des gesendeten Werts** auf `Number` festgelegt ist und Sie auf der Registerkarte **Optionen** Zeichenfolgedaten zum **Datenwert** hinzufügen, wird am Bildschirm die Fehlermeldung `Value type mismatch` angezeigt.

- **Standardoptionen**: Mit dieser Option können Sie vorab ausgewählte Standardwerte hinzufügen, wenn das Formular geladen wird. Wenn der **Datentyp des übermittelten Wertes** auf `Number` eingestellt ist und Sie den **Standardoptionen** Zeichenfolgen-Daten hinzufügen, wird auf dem Bildschirm die Fehlermeldung `Value type mismatch` angezeigt.

- **Anzeigeoptionen**: Diese Option wird verwendet, um die visuelle Ausrichtung von Optionsschaltflächen in einem adaptiven Formular festzulegen. Folgende zwei Optionen werden unterstützt:
   - **Horizontal** – Wenn diese Option aktiviert ist, werden Optionsschaltflächen in einem adaptiven Formular von links nach rechts angezeigt.
   - **Vertikal** – Wenn diese Option aktiviert ist, werden Optionsschaltflächen in einem adaptiven Formular von oben nach unten angezeigt.
- **Komponente ausblenden**: Wählen Sie diese Option, um die Komponente aus dem Formular auszublenden. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor. Dies ist nützlich, wenn Sie Informationen speichern müssen, die Benutzende nicht sehen oder direkt ändern müssen.
- **Komponente deaktivieren**: Wählen Sie die Option zum Deaktivieren der Komponente aus. Die deaktivierte Komponente ist nicht aktiv und Endbenutzende können sie nicht bearbeiten. Benutzende können den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor.
- **Schreibgeschützt**: Wählen Sie die Option aus, um die Komponente nicht bearbeitbar zu machen. Benutzende können den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor.

### Registerkarte „Validierung“ {#validation-tab}

![Registerkarte „Validierung“](/help/adaptive-forms/assets/radiobutton_validationtab.png)

- **Erforderlich**: Wählen Sie diese Option, wenn Sie die Komponente in einem adaptiven Formular anzeigen möchten. Nachdem Sie die Option ausgewählt haben, müssen Sie eine Auswahl treffen, bevor Sie mit der Formularübermittlung fortfahren. Wenn diese Option aktiviert ist, kann die Option **Komponente ausblenden** oder **Komponente deaktivieren** auf der Registerkarte **Allgemein** nicht ausgewählt werden.
- **Fehlermeldung**: Mit dieser Option können Sie eine Nachricht eingeben, die angezeigt wird, wenn das Kontrollkästchen **Erforderlich** aktiviert ist und das Feld leer bleibt.

- **Meldung zur Skriptvalidierung**: Mit dieser Option können Sie eine Meldung eingeben, die angezeigt werden soll, wenn die Skriptvalidierung fehlschlägt.

### Registerkarte „Hilfe-Inhalt“ {#helpcontent-tab}

![Registerkarte „Hilfe-Inhalt“](/help/adaptive-forms/assets/radiobutton_helptab.png)

- **Kurzbeschreibung**: Eine Kurzbeschreibung ist eine kurze Erklärung, die zusätzliche Informationen oder Klarstellungen über den Zweck eines Formularfelds bietet. Es hilft Benutzenden zu verstehen, welcher Datentyp in das Feld eingegeben werden soll, und kann Richtlinien oder Beispiele bereitstellen, um sicherzustellen, dass die eingegebenen Informationen gültig sind und die gewünschten Kriterien erfüllen. Standardmäßig bleiben kurze Beschreibungen ausgeblendet. Aktivieren Sie die Option **Kurzbeschreibung immer anzeigen**, um sie unterhalb der Komponente anzuzeigen.

- **Kurzbeschreibung immer anzeigen**: Aktivieren Sie diese Option, um die Kurzbeschreibung unterhalb der Komponente anzuzeigen.

- **Hilfetext**: Hilfetext bezieht sich auf zusätzliche Informationen oder Anleitungen, die den Benutzenden bereitgestellt werden, um sie beim korrekten Ausfüllen eines Formularfelds zu unterstützen. Er erscheint, wenn Benutzende auf das Hilfesymbol (i) neben der Komponente klicken. Hilfetext enthält detailliertere Informationen als die Beschriftung oder der Platzhaltertext eines Formularfelds und soll den Benutzenden dabei helfen, die Anforderungen oder Einschränkungen des Felds zu verstehen. Er kann auch Vorschläge oder Beispiele anbieten, um das Ausfüllen des Formulars einfacher und genauer zu gestalten.

### Registerkarte „Barrierefreiheit“ {#accessibility-tab}

![Registerkarte „Barrierefreiheit“](/help/adaptive-forms/assets/radiobutton_accessibilitytab.png)

- **Text für Bildschirmlesehilfen** – Das ist zusätzlicher Text, der von Hilfstechnologien wie etwa Bildschirmlesehilfen für sehbehinderte Personen vorgelesen wird. Dieser Text enthält eine Audiobeschreibung des Zwecks des Formularfelds und kann Informationen über den Titel, die Beschreibung, den Namen und alle relevanten Nachrichten (benutzerdefinierten Text) des Felds enthalten. Der Text der Bildschirmlesehilfe hilft sicherzustellen, dass das Formular allen Benutzenden zugänglich ist, auch Personen mit Sehschwäche, und bietet ihnen ein umfassendes Verständnis des Formularfelds und seiner Anforderungen.
   - **Benutzerdefinierter Text**: Wählen Sie diese Option aus, um den benutzerdefinierten Text für ARIA-Barrierefreiheitsbeschriftungen zu verwenden. Wenn Sie diese Option auswählen, wird das Benutzerdefinierter Dialogfeld „Text“ angezeigt. Sie können relevante Informationen im Benutzerdefinierter Dialogfeld „Text“ hinzufügen.
   - **Beschreibung**: Wählen Sie diese Option aus, um die Beschreibung für ARIA-Barrierefreiheitsbeschriftungen zu verwenden.
   - **Titel**: Wählen Sie diese Option aus, um den Titel für ARIA-Barrierefreiheitsbeschriftungen zu verwenden.
   - **Name**: Wählen Sie diese Option aus, um den Namen für ARIA-Barrierefreiheitsbeschriftungen zu verwenden.
   - **Keine**: Wählen Sie diese Option aus, wenn Sie keine ARIA-Barrierefreiheitsbezeichnungen hinzufügen möchten.

## Dialogfeld „Design“ {#design-dialog}

Das Dialogfeld „Design“ wird verwendet, um CSS-Stile für die Komponente „Optionsschaltfläche“ zu definieren und zu verwalten.


### Registerkarte „Stile“ {#styles-tab}

Sie können die Registerkarte zum Definieren und Verwalten von CSS-Stilen für eine Komponente verwenden. Die Kernkomponente „Optionsschaltfläche“ für adaptive Formulare unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).

![Dialogfeld „Design“](/help/adaptive-forms/assets/checkbox-style.png)

- **Standard-CSS-Klassen**: Sie können eine standardmäßige CSS-Klasse für die Kernkomponente „Optionsschaltfläche“ für adaptive Formulare bereitstellen.

- **Zulässige Stile**: Sie können Stile definieren, indem Sie den Namen und die CSS-Klasse für den Stil angeben. Sie können beispielsweise einen Stil mit dem Namen „Fettschrift“ erstellen und die CSS-Klasse „Schriftbreite: Fett“ bereitstellen. Sie können diese Stile bei einem adaptiven Formular im adaptiven Formular-Editor anwenden. Um einen Stil anzuwenden, wählen Sie im Editor für adaptive Formulare die Komponente aus, auf die Sie den Stil anwenden möchten, navigieren Sie zum Eigenschaften-Dialog und wählen Sie den gewünschten Stil aus der Dropdown-Liste **Stile**. Wenn Sie die Stile aktualisieren oder ändern müssen, kehren Sie einfach zum Dialogfeld „Design“ zurück, aktualisieren die Stile auf der Registerkarte „Stile“ und speichern die Änderungen.

### Benutzerdefinierte Eigenschaften

![Dialogfeld „Benutzerdefinierte Eigenschaften“](/help/adaptive-forms/assets/checkbox-customproperties.png)

Mit der Option „Benutzerdefinierte Eigenschaften“ können Sie mithilfe der Formularvorlage benutzerdefinierte Attribute (Schlüsselwertpaare) mit einer Kernkomponente eines adaptiven Formulars verknüpfen. Die benutzerdefinierten Eigenschaften werden im Eigenschaftenbereich der Headless-Ausgabedarstellung der Komponente angezeigt. So kann ein dynamisches Formularverhalten erzeugt werden, das sich je nach den benutzerdefinierten Attributwerten anpasst. Beispielsweise können Entwickelnde verschiedene Ausgabedarstellungen einer Headless-Formularkomponente für Mobile-, Desktop- oder Web-Plattformen entwerfen und so das Benutzererlebnis auf einer Vielzahl von Geräten erheblich verbessern.

- **Gruppenname**: Sie können einen Namen angeben, um die Gruppe der benutzerdefinierten Eigenschaften zu kennzeichnen. Sie können mehrere Gruppen benutzerdefinierter Eigenschaften hinzufügen, löschen oder neu anordnen. Nach dem Hinzufügen der Gruppe benutzerdefinierter Eigenschaften werden folgende Optionen angezeigt:

   - **Schlüssel-Wert-Paare**: Sie können mehrere Namen und Werte benutzerdefinierter Eigenschaften hinzufügen, indem Sie für jede Gruppe benutzerdefinierter Eigenschaften auf **Hinzufügen** klicken.

   - **Löschen**: Tippen oder klicken Sie auf diese Option, um den Namen und den Wert der benutzerdefinierten Eigenschaft zu löschen.

   - **Neu anordnen**: Ordnen Sie den Namen und Wert der benutzerdefinierten Eigenschaft Antippen oder Klicken und Ziehen neu an.

## Ähnliche Artikel {#related-articles}

{{more-like-this}}

## Siehe auch {#see-also}

{{see-also}}
