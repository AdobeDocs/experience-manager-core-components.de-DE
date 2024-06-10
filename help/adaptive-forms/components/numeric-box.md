---
title: Kernkomponente „Zahleneingabe“ für adaptive Formulare
description: Verwenden oder Anpassen der Kernkomponente „Zahleneingabe“ für adaptive Formulare.
role: Architect, Developer, Admin, User
exl-id: 75604ecf-1ec5-4e97-b934-d6ed49726147
source-git-commit: b4a66a407e92398a98441c65ab588b9720777dfa
workflow-type: ht
source-wordcount: '2283'
ht-degree: 100%

---

# Komponente „Numerisches Feld“{#number-input-adaptive-forms-core-component}

Mit der Komponente „Numerisches Feld“ für adaptive Formulare wird Benutzenden ein Formularfeld zur Eingabe numerischer Werte bereitgestellt. In der Regel wird die Komponente durch ein Textfeld mit einem Aufwärts- und Abwärtspfeil zum Erhöhen und Verringern der Zahl dargestellt.

Auch Attribute wie „Min.“, „Max.“ „Schritt“ und „Wert“ können damit verwendet werden. Sie können mit diesen Attributen die im Feld zulässigen Mindest- und Höchstwerte, das Schrittintervall zum Erhöhen oder Verringern der Zahl und den Standardwert des Felds festlegen.

Sie können mit dieser Komponente numerische Daten wie Alter und Menge erfassen. Auch mathematische Operationen wie Additionen und Subtraktionen können damit durchgeführt werden. Außerdem kann diese Komponente zur Gültigkeitsprüfung der von Benutzenden eingegebenen numerischen Daten verwendet werden.

Für die Barrierefreiheit ist es wichtig, einen „Titel“ anzugeben, der den Zweck des Zahleneingabefelds beschreibt und Informationen zur Art der erwarteten Eingabe bereitstellt.

**Beispiel**

![Beispiel](/help/adaptive-forms/assets/numeric-stepper.png)

## Verwendung {#reasons-to-use-number-input-numeric-stepper}

Es gibt mehrere Gründe, warum es sinnvoll ist, eine numerische Eingabekomponente in ein adaptives Formular einzuschließen, darunter:

- **Mathematische Operationen**: Sie können in numerischen Feldern mathematische Operationen wie Additionen, Subtraktionen, Multiplikationen und Divisionen durchführen.

- **Datenbereich**: Sie können numerische Felder dazu verwenden, um einen Bereich gültiger Werte mithilfe von Min.-, Max.- und Schrittattributen festzulegen.

- **Dynamische Inhalte**: Sie können numerische Komponenten dazu verwenden, um dynamische Daten basierend auf den Formularfeldern anzuzeigen.

## Version und Kompatibilität {#version-and-compatibility}

Die Kernkomponente „Akkordeon“ für adaptive Formulare wurde im Februar 2023 als Teil der Kernkomponenten 2.0.4 für Cloud Service und der Kernkomponenten 1.1.12 für AEM 6.5.16.0 Forms oder höher veröffentlicht. Hier finden Sie eine Tabelle mit allen unterstützten Versionen, AEM-Kompatibilität und Links zur entsprechenden Dokumentation:

| Komponentenversion | AEM as a Cloud Service | AEM 6.5.16.0 Forms oder höher |
|---|---|---|
| v1 | Kompatibel mit<br>[Version 2.0.4](/help/adaptive-forms/version.md) und höher | Kompatibel mit<br>[Version 1.1.12](/help/adaptive-forms/version.md) und höher (aber nur bis Version 2.0.0). |

Informationen zu Versionen und Freigaben der Kernkomponente finden Sie im Dokument [Kernkomponenten-Versionen](/help/adaptive-forms/version.md).


<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technische Details {#technical-details}

Die neuesten Informationen zur Kernkomponente „Zahleneingabe“ für adaptive Formulare erfahren Sie in der technischen Dokumentation auf [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/numberinput/v1/numberinput). Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Entwicklerdokumentation für Kernkomponenten](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Sie können im Dialogfeld „Konfigurieren“ die Zahleneingabe für Besuchende einfach anpassen. Sie können auch Optionen für die Zahleneingabe definieren, um das Benutzererlebnis zu verbessern.

### Registerkarte „Allgemein“ {#basic-tab}

![Registerkarte „Allgemein“](/help/adaptive-forms/assets/numberinput_basictab.png)

- **Name**: Sie können eine Formularkomponente sowohl im Formular als auch im Regeleditor durch ihren eindeutigen Namen identifizieren. Der Name darf keine Leerzeichen oder Sonderzeichen enthalten.

- **Titel**: Mit dem Titel können Sie eine Komponente in einem Formular leicht identifizieren. Standardmäßig wird der Titel oberhalb der Komponente angezeigt. Wenn Sie keinen Titel hinzufügen, wird der Name der Komponente anstelle des Titeltexts angezeigt.
- **Rich-Text für Titel zulassen**: Diese Funktionen ermöglichen es Benutzenden, einfache Texttitel zu formatieren, die Funktionen wie fett, kursiv, unterstrichener Text, verschiedene Schriftarten, Schriftgrößen, Farben und zusätzliche Optionen enthalten und so die visuelle Darstellung und Anpassung zu verbessern. Sie bietet mehr Flexibilität und kreative Kontrolle bei der Hervorhebung von Titeln in Dokumenten, Websites oder Anwendungen.\
  Durch Aktivieren des Kontrollkästchens **Rich-Text für Titel zulassen** werden Formatierungsoptionen sichtbar, mit denen Sie den Titel der Komponente gestalten können. Um auf alle verfügbaren Formatierungsoptionen zuzugreifen, können Sie auf die Registerkarte ![Vollbildsymbol](/help/adaptive-forms/assets/fullscreen-icon.png) klicken.

  ![Rich-Text-Unterstützung](/help/adaptive-forms/assets/richtext-support-title.png)

- **Titel ausblenden**: Wählen Sie die Option aus, um den Titel der Komponente auszublenden.
- **Platzhaltertext**: Platzhaltertext in einer Formularkomponente bezieht sich auf eine kurze Beschriftung oder Eingabeaufforderung, die in einem Eingabefeld angezeigt wird, um Benutzende darauf hinzuweisen, welcher Informationstyp in dieses Feld eingegeben werden soll. Der Platzhaltertext verschwindet, wenn Benutzende mit der Eingabe in das Feld beginnen, und erscheint wieder, wenn das Feld leer bleibt. Er stellt einen visuellen Hinweis für Benutzende bereit, fungiert jedoch nicht als permanente Beschriftung oder Wert für das Feld.
- **Bindungsreferenz**: Eine Bindungsreferenz ist ein Verweis auf ein Datenelement, das in einer externen Datenquelle gespeichert ist und in einem Formular verwendet wird. Sie können mit dem Bindungsverweis Daten dynamisch an Formularfelder binden, sodass das Formular die aktuellsten Daten aus der Datenquelle anzeigen kann. Beispielsweise kann ein Bindungsverweis verwendet werden, um den Namen und die Adresse von Kundinnen und Kunden in einem Formular anzuzeigen, basierend auf der im Formular eingegebenen Kunden-ID. Der Bindungsverweis kann auch verwendet werden, um die Datenquelle mit den im Formular eingegebenen Daten zu aktualisieren. Auf diese Weise können Sie mit AEM Forms Formulare erstellen, die mit externen Datenquellen interagieren und so ein nahtloses Benutzererlebnis bei der Datenerfassung und -verwaltung bieten.
- **Als ungebundenes Formularelement markieren**: Mit dieser Option können Sie Formularfelder konfigurieren, die mit keinem Schema verbunden sind. Mit dieser Option können Sie Daten speichern, ohne die Datenquelle zu aktualisieren. Außerdem können Sie damit Daten auf eine benutzerdefinierte Art und Weise verarbeiten, getrennt von der standardmäßigen Datenbankintegration.
- **Komponente ausblenden**: Wählen Sie diese Option, um die Komponente aus dem Formular auszublenden. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor. Dies ist nützlich, wenn Sie Informationen speichern müssen, die Benutzende nicht sehen oder direkt ändern müssen.
- **Komponente deaktivieren**: Wählen Sie die Option zum Deaktivieren der Komponente aus. Die deaktivierte Komponente ist nicht aktiv und Endbenutzende können sie nicht bearbeiten. Benutzende können den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor.
- **Schreibgeschützt**: Wählen Sie die Option aus, um zu verhindern, dass die Komponente bearbeitet werden kann. Die Benutzenden können den Wert des Felds sehen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor.
- **Zahlentyp** – Mit dieser Option können Sie den Typ der numerischen Werte auswählen, die im Formularfeld zulässig sind. Sie können aus dem Dropdown-Menü entweder den Typ „Dezimalzahl“ oder „Ganzzahl“ auswählen.
- **Standardwert**: Mit dieser Option können Sie einen Standardwert in ein Formularfeld einfügen. Wenn **Komponente deaktiviert** oder **Schreibgeschützte Komponente** ausgewählt ist, wird auf dem Bildschirm der Standardwert angezeigt. Wird kein Wert in das Formularfeld eingegeben, wird bei der Formularübermittlung dieser Wert gesendet

### Registerkarte „Validierung“ {#validation-tab}

![Registerkarte „Validierung“](/help/adaptive-forms/assets/numberinput_validationtab.png)

- **Erforderlich**: Wählen Sie diese Option, wenn Sie die Komponente in einem adaptiven Formular anzeigen möchten. Nach Auswahl der Option müssen Sie einen Wert eingeben, bevor Sie mit der Formularübermittlung fortfahren. Wenn diese Option aktiviert ist, kann die Option **Komponente ausblenden** oder **Komponente deaktivieren** auf der Registerkarte **Allgemein** nicht ausgewählt werden.

- **Fehlermeldung**: Mit dieser Option können Sie eine Nachricht eingeben, die angezeigt wird, wenn das Kontrollkästchen **Erforderlich** aktiviert ist und das Feld leer bleibt.

- **Meldung zur Skriptvalidierung**: Mit dieser Option können Sie eine Meldung eingeben, die angezeigt wird, wenn die Skriptvalidierung fehlschlägt.

- **Niedrigste Zahl / Kleinste Zahl** – Diese Option können Sie verwenden, um die Mindestzahl für die Eingabe im Formularfeld auszuwählen. Wenn der in das Formularfeld eingegebene Wert kleiner ist als der in **Niedrigste Zahl / Kleinste Zahl**, erscheint eine Fehlermeldung.

- **Mindest-Fehlermeldung** – Mit dieser Option können Sie eine Fehlermeldung erstellen, die erscheint, wenn Benutzende einen Wert eingeben, der kleiner ist als der in der Option **Mindestzahl/Mindestzahl**.

- **Mindestwert ausschließen** – Sie können dieses Kontrollkästchen aktivieren, wenn Sie den in der Option **Niedrigste Zahl / Kleinste Zahl** angegebenen Wert nicht in den Bereich der Werte aufnehmen möchten, die in das Formularfeld eingegeben werden können.

- **Höchste Zahl / Größte Zahl** – Sie können diese Option verwenden, um die maximal zulässige Zahl auszuwählen, die in das Formularfeld eingegeben werden darf. Wenn die in das Formularfeld eingegebene Zahl größer ist als die in der Option **Höchste Zahl / Größte Zahl**, erscheint eine Fehlermeldung.

- **Maximal-Fehlermeldung** – Sie können mit dieser Option eine Fehlermeldung erstellen, die erscheint, wenn Benutzende einen Wert eingeben, der größer ist als der in der Option **Höchste Zahl / Größte Zahl** angegebene.

- **Höchstwert ausschließen** – Sie können dieses Kontrollkästchen aktivieren, wenn Sie den in der Option **Höchste Zahl / Größte Zahl** angegebenen Höchstwert nicht in den Wertebereich aufnehmen möchten, der in das Formularfeld eingegeben werden kann.

### Registerkarte „Hilfe-Inhalt“ {#help-content}

![Registerkarte „Hilfe-Inhalt“](/help/adaptive-forms/assets/numberinput_helptab.png)

- **Kurzbeschreibung**: Eine Kurzbeschreibung ist eine kurze Erklärung, die zusätzliche Informationen oder Klarstellungen über den Zweck eines Formularfelds bietet. Es hilft Benutzenden zu verstehen, welcher Datentyp in das Feld eingegeben werden soll, und kann Richtlinien oder Beispiele bereitstellen, um sicherzustellen, dass die eingegebenen Informationen gültig sind und die gewünschten Kriterien erfüllen. Standardmäßig bleiben kurze Beschreibungen ausgeblendet. Aktivieren Sie die Option **Kurzbeschreibung immer anzeigen**, um sie unterhalb der Komponente anzuzeigen.

- **Kurzbeschreibung immer anzeigen**: Aktivieren Sie diese Option, um die Kurzbeschreibung unterhalb der Komponente anzuzeigen.

- **Hilfetext**: Hilfetext bezieht sich auf zusätzliche Informationen oder Anleitungen, die den Benutzenden bereitgestellt werden, um sie beim korrekten Ausfüllen eines Formularfelds zu unterstützen. Er erscheint, wenn Benutzende auf das Hilfesymbol (i) neben der Komponente klicken. Hilfetext enthält detailliertere Informationen als die Beschriftung oder der Platzhaltertext eines Formularfelds und soll den Benutzenden dabei helfen, die Anforderungen oder Einschränkungen des Felds zu verstehen. Er kann auch Vorschläge oder Beispiele anbieten, um das Ausfüllen des Formulars einfacher und genauer zu gestalten.

### Registerkarte „Barrierefreiheit“ {#accessibility}

![Registerkarte „Barrierefreiheit“](/help/adaptive-forms/assets/numberinput_accessibility.png)

- **Text für Bildschirmlesehilfen**: Text für Bildschirmlesehilfen bezieht sich auf zusätzlichen Text, der für Hilfstechnologien wie Bildschirmlesehilfen vorgesehen ist, die von Personen mit Sehschwäche verwendet werden. Dieser Text enthält eine Audiobeschreibung des Zwecks des Formularfelds und kann Informationen über den Titel, die Beschreibung, den Namen und alle relevanten Nachrichten (benutzerdefinierten Text) des Felds enthalten. Der Text der Bildschirmlesehilfe hilft sicherzustellen, dass das Formular allen Benutzenden zugänglich ist, auch Personen mit Sehschwäche, und bietet ihnen ein umfassendes Verständnis des Formularfelds und seiner Anforderungen.
   - **Benutzerdefinierter Text**: Wählen Sie diese Option aus, um den benutzerdefinierten Text für ARIA-Barrierefreiheitsbeschriftungen zu verwenden. Wenn Sie diese Option auswählen, wird das Benutzerdefinierter Dialogfeld „Text“ angezeigt. Sie können relevante Informationen im Benutzerdefinierter Dialogfeld „Text“ hinzufügen.
   - **Beschreibung**: Wählen Sie diese Option aus, um die Beschreibung für ARIA-Barrierefreiheitsbeschriftungen zu verwenden.
   - **Titel**: Wählen Sie diese Option aus, um den Titel für ARIA-Barrierefreiheitsbeschriftungen zu verwenden.
   - **Name**: Wählen Sie diese Option aus, um den Namen für ARIA-Barrierefreiheitsbeschriftungen zu verwenden.
   - **Keine**: Wählen Sie diese Option aus, wenn Sie keine ARIA-Barrierefreiheits-Labels hinzufügen möchten.

### Registerkarte „Formate“ {#formats-configure-tab}

![Registerkarte „Barrierefreiheit“](/help/adaptive-forms/assets/numberinput_formattab.png)

- **Anzeigeformat**: Sie können mit dieser Option aus verschiedenen numerischen ganzzahligen Formaten für die Anzeige auswählen. Wenn Benutzende aus dem Dropdown-Menü **Typ** eine Option auswählen, erscheint im Bedienfeld die Option **Format**. Sie können das Format auswählen, in dem die Zahlen den Benutzenden angezeigt werden sollen.
- **Sprache**: Diese Funktion wird zur Formatierung des spezifischen Felds verwendet. Wenn eine Benutzerin bzw. ein Benutzer eine Sprachoption aus dem Dropdown-Menü **Typ** auswählt, erscheint die Option **IETF BCP 47-Sprach-Tag** im Panel. Sie können die Sprache für die Feldformatierung wählen, wenn Sie ein adaptives Formular in eine bestimmte Sprache übersetzen.

Die Sprachauswahl ist standardmäßig nicht sichtbar, aber Benutzende können ein benutzerdefiniertes **IETF BCP 47-Sprach-Tag** eingeben, indem sie die Vorlagenrichtlinie aktualisieren:

1. Öffnen Sie im Vorlageneditor die entsprechende Vorlage, die mit einem adaptiven Formular verknüpft ist.
2. Wählen Sie die bestehende Richtlinie als `numberinput-default-policy` aus dem Dropdown-Menü.

   ![Richtlinie für Datumsauswahl-Vorlagen](/help/adaptive-forms/assets/numberinput-template-policy.png)

3. Klicken Sie auf **Fertig**.

   >[!NOTE]
   >
   > Weitere Informationen zur Übersetzung eines adaptiven Formulars in ein bestimmtes Gebietsschema finden Sie [hier](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/supporting-new-language-localization-core-components).


## Dialogfeld „Design“ {#design-dialog}

Das Dialogfeld „Design“ wird verwendet, um CSS-Stile für die Komponente „Numerisches Feld“ zu definieren und zu verwalten.

### Registerkarte „Stile“ {#styles-tab}

Sie können die Registerkarte zum Definieren und Verwalten von CSS-Stilen für eine Komponente verwenden. Die Kernkomponente „Zahleneingabe“ für adaptive Formulare unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).

![Registerkarte „Stile“](/help/adaptive-forms/assets/datepicker_styletab.png)

- **Standard-CSS-Klassen**: Sie können eine standardmäßige CSS-Klasse für die Kernkomponente „Numerisches Feld“ für adaptive Formulare bereitstellen.

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
