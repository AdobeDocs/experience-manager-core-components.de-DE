---
title: Kernkomponente „Datumsauswahl“ für adaptive Formulare
description: Verwenden oder Anpassen der Datumsauswahl-Kernkomponente in adaptiven Formularen.
role: Architect, Developer, Admin, User
exl-id: aa9402de-ca57-4c19-8d36-2dd0a78d6806
source-git-commit: 6725784bd4c94d433c91d6bd65d14d03cbefd954
workflow-type: ht
source-wordcount: '2298'
ht-degree: 100%

---


# Datumsauswahl-Komponente{#date-picker-adaptive-forms-core-component}

Datumsauswahl-Komponenten in einem adaptiven Formular sind Elemente der Benutzeroberfläche, mit denen Benutzende ein Datum aus einem Kalender auswählen oder manuell ein Datum in einem bestimmten Format eingeben können. Sie können die Datumsauswahl-Komponente so konfigurieren, dass sie unterschiedliche Formatierungen, Validierungen und Standardwerte aufweist.

{{traditional-aem}}

**Beispiel**

![Beispiel](/help/adaptive-forms/assets/date-picker.png)

## Verwendung {#reasons-to-use-drop-date-picker}

Die Verwendung der Datumsauswahl in einem adaptiven Formular kann verschiedene Vorteile haben, darunter:

- **Komfort**: Benutzende können mit einer Datumsauswahl-Komponente einfach ein Datum aus einem Kalender auswählen, ohne das Datum manuell in ein Textfeld eingeben zu müssen. Dies kann Zeit sparen und Fehler reduzieren.

- **Benutzererlebnis**: Sie können mit der Datumsauswahl-Komponente das Formular benutzerfreundlicher gestalten, indem Sie eine klare und intuitive Methode zur Auswahl des Datums bereitstellen.

- **Datenanalyse**: Die Datumsauswahl-Komponente kann verwendet werden, um Daten aus verschiedenen Quellen zu erfassen und zu analysieren oder sie als Eingabe für die weitere Verarbeitung zu verwenden.

- **Event-Management**: Sie können die Datumsauswahl-Komponente auf Event-Management-Websites zur Auswahl einer Veranstaltung verwenden.

- **Buchung und Reservierung**: Die Datumsauswahl-Komponente kann auf Buchungs- und Reservierungs-Websites verwendet werden, um die Ein- und Auscheckdaten auszuwählen.

- **Datumsformat**: Sie können die Datumsauswahl-Komponente verwenden, um das Format zu korrigieren, in dem das Datum angezeigt und eingegeben wird. Stellen Sie sicher, dass das Datumsformat im gesamten Formular gleich ist, um ein konsistentes Benutzererlebnis zu gewährleisten.

## Version und Kompatibilität {#version-and-compatibility}

Die Kernkomponente für die Datumsauswahl in adaptiven Formularen wurde im Februar 2023 als Teil der Kernkomponenten 2.0.4 für Cloud Service und der Kernkomponenten 1.1.12 für AEM 6.5.16.0 Forms oder höher veröffentlicht. Hier finden Sie eine Tabelle mit allen unterstützten Versionen, AEM-Kompatibilität und Links zur entsprechenden Dokumentation:

| Komponentenversion | AEM as a Cloud Service | AEM 6.5.16.0 Forms oder höher |
|---|---|---|
| v1 | Kompatibel mit<br>[Version 2.0.4](/help/adaptive-forms/version.md) und höher | Kompatibel mit<br>[Version 1.1.12](/help/adaptive-forms/version.md) und höher (aber nur bis Version 2.0.0). |

Informationen zu Versionen und Freigaben der Kernkomponente finden Sie im Dokument [Kernkomponenten-Versionen](/help/adaptive-forms/version.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion_de). -->

## Technische Details {#technical-details}

Die neuesten Informationen zur Datumsauswahl-Kernkomponente für adaptive Formulare erhalten Sie in der technischen Dokumentation auf [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/datepicker/v1/datepicker). Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Entwicklerdokumentation für Kernkomponenten](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Sie können die Datumsauswahl im Dialogfeld „Konfigurieren“ einfach anpassen. Sie können auch Optionen für die Datumsauswahl definieren, um das Benutzererlebnis zu verbessern.

### Registerkarte „Allgemein“ {#basic-tab}

![Registerkarte „Allgemein“](/help/adaptive-forms/assets/datepicker_basictab.png)

- **Name**: Durch den Namen wird die Komponente im Regel-Editor eindeutig identifiziert. Sonderzeichen und Leerzeichen sind im Namen nicht zulässig.

- **Titel**: Titel ist eine Zeichenfolge, die in einem adaptiven Formular oberhalb einer Komponente angezeigt wird. Der Titel identifiziert die Komponente eindeutig in der Baumstruktur eines adaptiven Formulars. Wenn Sie keinen Titel hinzufügen, wird der Name der Komponente anstelle des Titeltexts angezeigt.
- **Rich-Text für Titel zulassen**: Diese Funktionen ermöglichen es Benutzenden, einfache Texttitel zu formatieren, die Funktionen wie fett, kursiv, unterstrichener Text, verschiedene Schriftarten, Schriftgrößen, Farben und zusätzliche Optionen enthalten und so die visuelle Darstellung und Anpassung zu verbessern. Sie bietet mehr Flexibilität und kreative Kontrolle bei der Hervorhebung von Titeln in Dokumenten, Websites oder Anwendungen.\
  Durch Aktivieren des Kontrollkästchens **Rich-Text für Titel zulassen** werden Formatierungsoptionen sichtbar, mit denen Sie den Titel der Komponente gestalten können. Um auf alle verfügbaren Formatierungsoptionen zuzugreifen, können Sie auf die Registerkarte ![Vollbildsymbol](/help/adaptive-forms/assets/fullscreen-icon.png) klicken.

  ![Rich-Text-Unterstützung](/help/adaptive-forms/assets/richtext-support-title.png)

- **Titel ausblenden**: Wählen Sie diese Option, um den Titel des Komponententyps in einem adaptiven Formular auszublenden.

- **Platzhaltertext**: Platzhaltertext in einer Formularkomponente ist eine kurze Beschriftung oder Eingabeaufforderung in einem Eingabefeld, um Benutzende darüber zu informieren, welchen Text sie in dieses Feld eingeben sollen. Der Platzhaltertext verschwindet, wenn Benutzende mit der Eingabe in das Feld beginnen, und erscheint wieder, wenn das Feld leer bleibt. Er stellt einen visuellen Hinweis für Benutzende bereit, fungiert jedoch nicht als permanente Beschriftung oder Wert für das Feld.
- **Bindungsreferenz**: Eine Bindungsreferenz ist ein Verweis auf ein Datenelement, das in einer externen Datenquelle gespeichert ist und in einem Formular verwendet wird. Sie können mit dem Bindungsverweis Daten dynamisch an Formularfelder binden, sodass das Formular die aktuellsten Daten aus der Datenquelle anzeigen kann. Beispielsweise kann ein Bindungsverweis verwendet werden, um den Namen und die Adresse von Kundinnen und Kunden in einem Formular anzuzeigen, basierend auf der im Formular eingegebenen Kunden-ID. Der Bindungsverweis kann auch verwendet werden, um die Datenquelle mit den im Formular eingegebenen Daten zu aktualisieren. Auf diese Weise können Sie mit AEM Forms Formulare erstellen, die mit externen Datenquellen interagieren und so ein nahtloses Benutzererlebnis bei der Datenerfassung und -verwaltung bieten.

- **Als ungebundenes Formularelement markieren**: Mit dieser Option können Sie Formularfelder konfigurieren, die mit keinem Schema verbunden sind. Mit dieser Option können Sie Daten speichern, ohne die Datenquelle zu aktualisieren. Außerdem können Sie damit Daten auf eine benutzerdefinierte Art und Weise verarbeiten, getrennt von der standardmäßigen Datenbankintegration.

- **Komponente ausblenden**: Wählen Sie diese Option, um die Komponente aus dem Formular auszublenden. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor. Dies ist nützlich, wenn Sie Informationen speichern müssen, die Benutzende nicht sehen oder direkt ändern müssen.
- **Komponente deaktivieren**: Wählen Sie die Option zum Deaktivieren der Komponente aus. Die deaktivierte Komponente ist nicht aktiv und Endbenutzende können sie nicht bearbeiten. Benutzende können den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor.
- **Schreibgeschützt**: Wählen Sie die Option aus, um die Komponente nicht bearbeitbar zu machen. Benutzende können den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor.
- **Standarddatum**: Mit dieser Option können Sie dem Formularfeld ein Datum hinzufügen. Das eingegebene Datum wird standardmäßig an der Stelle der Komponente angezeigt. Wird kein Datum eingegeben, wird bei der Formularübermittlung dieser Wert gesendet. Wenn **Deaktiverte Komponente** oder **Schreibgeschützte Komponente** ausgewählt wird, wird das Standarddatum auf dem Bildschirm angezeigt und bei der Formularübermittlung gesendet.


### Registerkarte „Validierung“ {#validation-tab}

![Registerkarte „Validierung“](/help/adaptive-forms/assets/datepicker_validation.png)

- **Erforderlich**: Wählen Sie diese Option, wenn Sie die Komponente in einem adaptiven Formular anzeigen möchten. Nachdem Sie die Option ausgewählt haben, müssen Sie eine Auswahl treffen, bevor Sie mit der Formularübermittlung fortfahren. Wenn diese Option aktiviert ist, kann die Option **Komponente ausblenden** oder **Komponente deaktivieren** auf der Registerkarte **Allgemein** nicht ausgewählt werden.

- **Fehlermeldung**: Mit dieser Option können Sie eine Nachricht eingeben, die angezeigt wird, wenn das Kontrollkästchen **Erforderlich** aktiviert ist und das Feld leer bleibt.

- **Meldung zur Skriptvalidierung**: Mit dieser Option können Sie eine Meldung eingeben, die angezeigt wird, wenn die Skriptvalidierung fehlschlägt.

- **Mindestdatum** – Sie können mit dieser Option das erforderliche Mindestdatum eingeben. Wenn Sie ein Datum eingeben, das vor dem in „Mindestdatum“ angegebenen Datum liegt, erscheint eine Fehlermeldung auf dem Bildschirm. Sie können der **Mindest-Fehlermeldung** eine benutzerdefinierte Fehlermeldung hinzufügen.

- **Mindest-Fehlermeldung** – Sie können der **Mindest-Fehlermeldung** eine benutzerdefinierte Fehlermeldung hinzufügen, die angezeigt wird, wenn Sie ein Datum eingeben, das vor dem in der Option **Mindestdatum** angegebenen liegt.
- **Mindestdatum ausschließen**: Mit dieser Option können Sie das Mindestdatum in einem bestimmten Datumsbereich oder einer Reihe von Daten weglassen.

- **Maximales Datum** – Sie können mit dieser Option das maximale Datum eingeben. Wenn Sie ein Datum eingeben, das nach dem in „Maximales Datum“ angegebenen Datum liegt, erscheint eine Fehlermeldung auf dem Bildschirm. Sie können im Dialog **Maximal-Fehlermeldung** eine benutzerdefinierte Fehlermeldung hinzufügen.

- **Maximal-Fehlermeldung** – Sie können im Dialogfeld **Maximal-Fehlermeldung** eine benutzerdefinierte Fehlermeldung hinzufügen, die angezeigt wird, wenn Sie ein Datum eingeben, das nach der Option **Maximales Datum** liegt.

- **Maximales Datum ausschließen**: Mit dieser Option können Sie das maximale Datum in einem bestimmten Datumsbereich oder einer Reihe von Daten weglassen.

### Registerkarte „Hilfe-Inhalt“ {#help-content-tab}

![Registerkarte „Hilfe-Inhalt“](/help/adaptive-forms/assets/datepicker_helptab.png)

- **Kurzbeschreibung**: Eine Kurzbeschreibung ist eine kurze Erklärung, die zusätzliche Informationen oder Klarstellungen über den Zweck eines Formularfelds bietet. Es hilft Benutzenden zu verstehen, welcher Datentyp in das Feld eingegeben werden soll, und kann Richtlinien oder Beispiele bereitstellen, um sicherzustellen, dass die eingegebenen Informationen gültig sind und die gewünschten Kriterien erfüllen. Standardmäßig bleiben kurze Beschreibungen ausgeblendet. Aktivieren Sie die Option **Kurzbeschreibung immer anzeigen**, um sie unterhalb der Komponente anzuzeigen.

- **Kurzbeschreibung immer anzeigen** – Aktivieren Sie die Option, um die Kurzbeschreibung unterhalb der Komponente anzuzeigen.

- **Hilfetext**: Hilfetext bezieht sich auf zusätzliche Informationen oder Anleitungen, die den Benutzenden bereitgestellt werden, um sie beim korrekten Ausfüllen eines Formularfelds zu unterstützen. Er erscheint, wenn Benutzende auf das Hilfesymbol (i) neben der Komponente klicken. Hilfetext enthält detailliertere Informationen als die Beschriftung oder der Platzhaltertext eines Formularfelds und soll den Benutzenden dabei helfen, die Anforderungen oder Einschränkungen des Felds zu verstehen. Er kann auch Vorschläge oder Beispiele anbieten, um das Ausfüllen des Formulars einfacher und genauer zu gestalten.


### Registerkarte „Barrierefreiheit“ {#accessibility-tab}

![Registerkarte „Barrierefreiheit“](/help/adaptive-forms/assets/datepicker_accessibilitytab.png)

- **Text für Bildschirmlesehilfen** – Das ist zusätzlicher Text, der von Hilfstechnologien wie etwa Bildschirmlesehilfen für sehbehinderte Personen vorgelesen wird. Dieser Text enthält eine Audiobeschreibung des Zwecks des Formularfelds und kann Informationen über den Titel, die Beschreibung, den Namen und alle relevanten Nachrichten (benutzerdefinierten Text) des Felds enthalten. Der Text der Bildschirmlesehilfe hilft sicherzustellen, dass das Formular allen Benutzenden zugänglich ist, auch Personen mit Sehschwäche, und bietet ihnen ein umfassendes Verständnis des Formularfelds und seiner Anforderungen.
   - **Benutzerdefinierter Text**: Wählen Sie diese Option aus, um den benutzerdefinierten Text für ARIA-Barrierefreiheitsbeschriftungen zu verwenden. Wenn Sie diese Option auswählen, wird das Benutzerdefinierter Dialogfeld „Text“ angezeigt. Sie können relevante Informationen im Benutzerdefinierter Dialogfeld „Text“ hinzufügen.
   - **Beschreibung**: Wählen Sie diese Option aus, um die Beschreibung für ARIA-Barrierefreiheitsbeschriftungen zu verwenden.
   - **Titel**: Wählen Sie diese Option aus, um den Titel für ARIA-Barrierefreiheitsbeschriftungen zu verwenden.
   - **Name**: Wählen Sie diese Option aus, um den Namen für ARIA-Barrierefreiheitsbeschriftungen zu verwenden.
   - **Keine**: Wählen Sie diese Option aus, wenn Sie keine ARIA-Barrierefreiheitsbezeichnungen hinzufügen möchten.

### Registerkarte „Formate“ {#format-tab}

![Registerkarte „Formate“](/help/adaptive-forms/assets/datepicker_formattab.png)

- **Anzeigeformat** – Stellt das Format dar, in dem das Datum angezeigt wird. Die Option **Typ** ermöglicht die Auswahl des Datumsformats. Sie können das Datumsformat auch mithilfe der Option **Benutzerdefiniert** im Dropdown-Menü **Typ** anpassen.

- **Format bearbeiten** – Stellt ein Datumsformat dar, in dem das Datum bearbeitet werden kann. Die Option **Typ** ermöglicht die Auswahl des Datumsformats. Sie können das Datumsformat auch mithilfe der Option **Benutzerdefiniert** im Dropdown-Menü **Typ** anpassen.
- **Fehlermeldung formatieren**: Mit dieser Option können Sie die auf dem Bildschirm angezeigte Nachricht eingeben, wenn das eingegebene Datum nicht das richtige Format aufweist.
- **Sprache**: Diese Funktion wird zur Formatierung des spezifischen Felds verwendet. Wenn eine Benutzerin bzw. ein Benutzer eine Sprachoption aus dem Dropdown-Menü **Typ** auswählt, erscheint die Option **IETF BCP 47-Sprach-Tag** im Panel. Sie können die Sprache für die Feldformatierung wählen, wenn Sie ein adaptives Formular in eine bestimmte Sprache übersetzen.

Die Sprachauswahl ist standardmäßig nicht sichtbar, aber Benutzende können ein benutzerdefiniertes **IETF BCP 47-Sprach-Tag** eingeben, indem sie die Vorlagenrichtlinie aktualisieren:

1. Öffnen Sie im Vorlageneditor die entsprechende Vorlage, die mit einem adaptiven Formular verknüpft ist.
2. Wählen Sie die bestehende Richtlinie als `datepicker-default-policy` aus dem Dropdown-Menü.

   ![Richtlinie für Datumsauswahl-Vorlagen](/help/adaptive-forms/assets/date-picker-template-policy.png)

3. Klicken Sie auf **Fertig**.

   >[!NOTE]
   >
   > Weitere Informationen zur Übersetzung eines adaptiven Formulars in ein bestimmtes Gebietsschema finden Sie [hier](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/supporting-new-language-localization-core-components).

## Dialogfeld „Design“ {#design-dialog}

Das Dialogfeld „Design“ wird verwendet, um CSS-Stile für die Komponente „Datumsauswahl“ zu definieren und zu verwalten.

### Registerkarte „Stile“ {#styles-tab}

Sie können die Registerkarte zum Definieren und Verwalten von CSS-Stilen für eine Komponente verwenden. Die Kernkomponente „Datumsauswahl“ in adaptiven Formularen unterstützt das [Stilsystem](/help/get-started/authoring.md#component-styling) von AEM.

![Registerkarte „Stile“](/help/adaptive-forms/assets/datepicker_styletab.png)

- **Standard-CSS-Klassen**: Sie können für die Datumsauswahl-Kernkomponente in adaptiven Formularen eine Standard-CSS-Klasse bereitstellen.

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

![Registerkarte „Format“](/help/adaptive-forms/assets/datepicker_formatpolicy.png)

<!--

## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html?lang=de)

-->

## Ähnliche Artikel {#related-articles}

{{more-like-this}}

## Siehe auch {#see-also}

{{see-also}}


