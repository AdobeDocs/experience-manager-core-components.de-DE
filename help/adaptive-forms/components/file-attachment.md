---
title: Kernkomponente „Dateianhang“ von adaptiven Formularen
description: Verwenden oder Anpassen der Kernkomponente „Dateianhang“ von adaptiven Formularen.
role: Architect, Developer, Admin, User
exl-id: 64a54fc6-db52-481f-bf5a-60c05122004d
source-git-commit: 6725784bd4c94d433c91d6bd65d14d03cbefd954
workflow-type: tm+mt
source-wordcount: '2061'
ht-degree: 100%

---


# Dateianhang-Komponente {#file-attachment-adaptive-forms-core-component}

<span class="preview"> Die Funktion **Datentyp des gesendeten Werts** ist im Rahmen des Early-Adopter-Programms verfügbar. Sie können von Ihrer offiziellen E-Mail-Adresse aus an aem-forms-ea@adobe.com schreiben, um dem Early-Adopter-Programm beizutreten und den Zugriff auf diese Funktion zu beantragen. </span>

Durch Verwendung der Dateianhang-Komponente in einem adaptiven Formular können Benutzende Dateien von ihrem lokalen Computer oder Gerät auswählen und hochladen. Die Dateianhang-Komponente kann so konfiguriert werden, dass bestimmte Dateitypen, Größenbeschränkungen und mehrere Anhänge zulässig sind.

{{traditional-aem}}

**Beispiel**

![Beispiel](/help/adaptive-forms/assets/upload-image.png)


## Verwendung {#reasons-to-use-file-attachment}

Es gibt mehrere Gründe, warum es sinnvoll ist, eine Dateianhang-Komponente in einem adaptiven Formular zu verwenden, darunter:

- **Sammeln zusätzlicher Informationen**: Eine Dateianhang-Komponente ermöglicht es Benutzenden, Dokumente, Bilder, Videos oder andere Dateitypen im Zuge der Formularübermittlung hochzuladen. Dies kann für die Übermittlung von zusätzlichen Informationen nützlich sein, wie etwa von Lebensläufen, Informationsmaterialien oder Begleitunterlagen.

- **Einfache Freigabe großer Dateien**: Die Dateianhang-Komponente ermöglicht es Benutzenden, große Dateien einfach für andere freizugeben, ohne auf externe File-Sharing-Dienste angewiesen zu sein.

- **Komfort**: Die Dateianhang-Komponente ermöglicht es Benutzenden, Dateien von ihrem lokalen Computer hochzuladen, ohne das Formular verlassen oder andere Tools verwenden zu müssen.

- **Datenanalyse**: Die Dateianhang-Komponente kann verwendet werden, um Daten aus verschiedenen Quellen zu sammeln und zu analysieren oder als Eingabe für die weitere Verarbeitung zu verwenden.

- **Benutzererlebnis**: Die Dateianhang-Komponente kann verwendet werden, um das Formular benutzerfreundlicher zu gestalten, indem eine klare und intuitive Möglichkeit für Benutzende zum Hochladen von Dateien bereitgestellt wird.

## Version und Kompatibilität {#version-and-compatibility}

Die Kernkomponente für Dateianhänge in adaptiven Formularen wurde im Februar 2023 als Teil der Kernkomponenten 2.0.4 für Cloud Service und der Kernkomponenten 1.1.12 für AEM 6.5.16.0 Forms oder höher veröffentlicht. Hier finden Sie eine Tabelle mit allen unterstützten Versionen, AEM-Kompatibilität und Links zur entsprechenden Dokumentation:

| Komponentenversion | AEM as a Cloud Service | AEM 6.5.16.0 Forms oder höher |
|---|---|---|
| v1 | Kompatibel mit<br>[Version 2.0.4](/help/adaptive-forms/version.md) und höher | Kompatibel mit<br>[Version 1.1.12](/help/adaptive-forms/version.md) und höher (aber nur bis Version 2.0.0). |

Informationen zu Versionen und Freigaben der Kernkomponente finden Sie im Dokument [Kernkomponenten-Versionen](/help/adaptive-forms/version.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technische Details {#technical-details}

Die neuesten Informationen zur Kernkomponente „Dateianhänge“ für adaptive Formulare finden Sie in der technischen Dokumentation zu [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/fileinput/v1/fileinput). Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Entwicklerdokumentation für Kernkomponenten](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Im Dialogfeld „Konfigurieren“ können Sie die Verwendung von Dateianhängen einfach anpassen. Sie können auch Optionen für den Dateianhang definieren, um das Benutzererlebnis zu verbessern.

### Registerkarte „Allgemein“ {#basic-tab}

![Registerkarte „Allgemein“](/help/adaptive-forms/assets/fileattachement_basictab1.png)

- **Name**: Sie können eine Formularkomponente sowohl im Formular als auch im Regeleditor durch ihren eindeutigen Namen identifizieren. Der Name darf keine Leerzeichen oder Sonderzeichen enthalten.

- **Titel**: Mit dem Titel können Sie eine Komponente in einem Formular leicht identifizieren. Standardmäßig wird der Titel oberhalb der Komponente angezeigt. Wenn Sie keinen Titel hinzufügen, wird der Name der Komponente anstelle des Titeltexts angezeigt.
- **Rich-Text für Titel zulassen**: Diese Funktionen ermöglichen es Benutzenden, einfache Texttitel zu formatieren, die Funktionen wie fett, kursiv, unterstrichener Text, verschiedene Schriftarten, Schriftgrößen, Farben und zusätzliche Optionen enthalten und so die visuelle Darstellung und Anpassung zu verbessern. Sie bietet mehr Flexibilität und kreative Kontrolle bei der Hervorhebung von Titeln in Dokumenten, Websites oder Anwendungen.\
  Durch Aktivieren des Kontrollkästchens **Rich-Text für Titel zulassen** werden Formatierungsoptionen sichtbar, mit denen Sie den Titel der Komponente gestalten können. Um auf alle verfügbaren Formatierungsoptionen zuzugreifen, können Sie auf die Registerkarte ![Vollbildsymbol](/help/adaptive-forms/assets/fullscreen-icon.png) klicken.

  ![Rich-Text-Unterstützung](/help/adaptive-forms/assets/richtext-support-title.png)

- **Titel ausblenden**: Wählen Sie diese Option aus, um den Titel der Komponente auszublenden.

- **Schaltflächentitel**: Diese Option wird verwendet, um die Beschriftung der Schaltfläche festzulegen, die in einem adaptiven Formular angezeigt wird.
- **Bindungsreferenz**: Eine Bindungsreferenz ist ein Verweis auf ein Datenelement, das in einer externen Datenquelle gespeichert ist und in einem Formular verwendet wird. Sie können mit dem Bindungsverweis Daten dynamisch an Formularfelder binden, sodass das Formular die aktuellsten Daten aus der Datenquelle anzeigen kann. Beispielsweise kann ein Bindungsverweis verwendet werden, um den Namen und die Adresse von Kundinnen und Kunden in einem Formular anzuzeigen, basierend auf der im Formular eingegebenen Kunden-ID. Der Bindungsverweis kann auch verwendet werden, um die Datenquelle mit den im Formular eingegebenen Daten zu aktualisieren. Auf diese Weise können Sie mit AEM Forms Formulare erstellen, die mit externen Datenquellen interagieren und so eine nahtlose Benutzererfahrung bei der Datenerfassung und Datenverwaltung bieten.
- **Als ungebundenes Formularelement markieren**: Mit dieser Option können Sie Formularfelder konfigurieren, die mit keinem Schema verbunden sind. Mit dieser Option können Sie Daten speichern, ohne die Datenquelle zu aktualisieren. Außerdem können Sie damit Daten auf eine benutzerdefinierte Art und Weise verarbeiten, getrennt von der standardmäßigen Datenbankintegration.
- **Datentyp des gesendeten Werts**: Wählen Sie die Option aus, um zu bestimmen, wie die angehängte Datei an den Server gesendet wird. Um den Anhang als Binärdaten zu senden, wählen Sie die Option `File` aus. Um den Anhang als Base64-codierte Zeichenfolge zu senden, wählen Sie die Option `String` aus. Wenn `String` ausgewählt ist, wird die Datei im Binärformat als Daten-URL an den Server gesendet. Der Server konvertiert die Daten-URL automatisch wieder in das Binärformat, wodurch die Kompatibilität mit bestehenden Aktionen gewährleistet wird, z. B. dem Senden von E-Mails und dem Generieren des Nachweises, ohne dass Benutzende Änderungen vornehmen müssen. Standardmäßig ist die Option `File` ausgewählt.
- **Komponente ausblenden**: Wählen Sie diese Option, um die Komponente aus dem Formular auszublenden. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor. Dies ist nützlich, wenn Sie Informationen speichern müssen, die Benutzende nicht sehen oder direkt ändern müssen.
- **Komponente deaktivieren**: Wählen Sie die Option zum Deaktivieren der Komponente aus. Die deaktivierte Komponente ist nicht aktiv und Endbenutzende können sie nicht bearbeiten. Benutzende können den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor.
- **Schreibgeschützt**: Wählen Sie die Option aus, um die Komponente nicht bearbeitbar zu machen. Benutzende können den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor.
- **Mehrere Anhänge zulassen**: Wählen Sie diese Option aus, um zuzulassen, dass mit der Schaltfläche **Dateianhang** mehrere Anhänge hochgeladen werden können.
- **Text ziehen und ablegen**: Dieser Text wird über der Schaltfläche **Anhängen** angezeigt, um Benutzende aufzufordern, Dateien entweder anzuhängen oder per Drag-and-Drop einzufügen. Sie haben die Möglichkeit, den oben auf der Schaltfläche **Anhängen** angezeigten Text anzupassen. Darüber hinaus können Sie den Text mithilfe des Rich-Text-Menüs formatieren.

### Registerkarte „Validierung“ {#validation-tab}

![Registerkarte „Validierung“](/help/adaptive-forms/assets/fileattachment_validationtab.png)

- **Erforderlich**: Wählen Sie diese Option, wenn Sie die Komponente in einem adaptiven Formular anzeigen möchten. Nach Auswahl dieser Option müssen Sie Anhänge hinzufügen, bevor Sie mit der Formularübermittlung fortfahren. Wenn diese Option aktiviert ist, kann die Option **Komponente ausblenden** oder **Komponente deaktivieren** auf der Registerkarte **Allgemein** nicht ausgewählt werden.
- **Fehlermeldung**: Mit dieser Option können Sie eine Nachricht eingeben, die angezeigt wird, wenn das Kontrollkästchen **Erforderlich** aktiviert ist und das Feld leer bleibt.

- **Meldung zur Skriptvalidierung**: Mit dieser Option können Sie eine Meldung eingeben, die angezeigt wird, wenn die Skriptvalidierung fehlschlägt.

<!--   **Minimum files error message** - This option is used to enter an error message that is displayed if you upload files lesser than the specified minimum number of files.-->

- **Maximale Dateigröße (MB)** – Mit dieser Option können Sie eine maximale Dateigröße angeben. Die Dateigrößen sind in MB angegeben.
  <!--   **Maximum files error message** - This option is used to enter an error message that is displayed if you upload files greater than the specified maximum number of files.-->

- **Fehlermeldung zur maximalen Dateigröße** – Mit dieser Option können Sie eine Fehlermeldung eingeben, die angezeigt wird, wenn Sie Dateien hochladen, deren Größe die in der Option **Maximale Dateigröße (MB)** angegebene Dateigröße überschreitet.

- **Zulässige Dateitypen** – Hier werden die Dateitypen spezifiziert, die über die Schaltfläche **Dateianhang** hochgeladen werden können. Sie können auch ein neues Dateiformat hinzufügen, indem Sie auf die Schaltfläche **Hinzufügen** klicken. Unterstützte Dateiformate sind: Audio, Video, Bild, Text oder PDF. Sie können zulässige Dateitypen auch löschen oder neu anordnen, indem Sie Folgendes verwenden:
   - **Löschen** – Durch Tippen oder Klicken können Sie bestimmte Dateitypen entfernen.
   - **Neu anordnen** – Durch Tippen oder Klicken und Ziehen können Sie die Anordnung zulässiger Dateitypen verändern.

  Wenn Sie eine Datei übermitteln, indem Sie deren Typ in ein zulässiges Dateitypformat ändern, wird während der Formularübermittlung ein Fehler ausgelöst.
- **Dateityp-Fehlermeldung** – Mit dieser Option können Sie eine Fehlermeldung eingeben, die angezeigt wird, wenn Sie andere Dateiformate hochladen als diejenigen, die in der Option **Zulässige Dateitypen** aufgeführt sind.

### Registerkarte „Hilfe-Inhalt“ {#help-content-tab}

![Registerkarte „Hilfe-Inhalt“](/help/adaptive-forms/assets/fileattachement_helpcontenttab.png)

- **Kurzbeschreibung**: Eine Kurzbeschreibung ist eine kurze Erklärung, die zusätzliche Informationen oder Klarstellungen über den Zweck eines Formularfelds bietet. Es hilft Benutzenden zu verstehen, welcher Datentyp in das Feld eingegeben werden soll, und kann Richtlinien oder Beispiele bereitstellen, um sicherzustellen, dass die eingegebenen Informationen gültig sind und die gewünschten Kriterien erfüllen. Standardmäßig bleiben kurze Beschreibungen ausgeblendet. Aktivieren Sie die Option **Kurzbeschreibung immer anzeigen**, um sie unterhalb der Komponente anzuzeigen.

- **Kurzbeschreibung immer anzeigen**: Aktivieren Sie diese Option, um die Kurzbeschreibung unterhalb der Komponente anzuzeigen.

- **Hilfetext**: Hilfetext bezieht sich auf zusätzliche Informationen oder Anleitungen, die den Benutzenden bereitgestellt werden, um sie beim korrekten Ausfüllen eines Formularfelds zu unterstützen. Er erscheint, wenn Benutzende auf das Hilfesymbol (i) neben der Komponente klicken. Hilfetext enthält detailliertere Informationen als die Beschriftung oder der Platzhaltertext eines Formularfelds und soll den Benutzenden dabei helfen, die Anforderungen oder Einschränkungen des Felds zu verstehen. Er kann auch Vorschläge oder Beispiele anbieten, um das Ausfüllen des Formulars einfacher und genauer zu gestalten.

### Registerkarte „Barrierefreiheit“ {#accessibility-tab}


![Registerkarte „Barrierefreiheit“](/help/adaptive-forms/assets/fileattachement_accessibilitytab.png)

- **Text für Bildschirmlesehilfen** – Das ist zusätzlicher Text, der von Hilfstechnologien wie etwa Bildschirmlesehilfen für sehbehinderte Personen vorgelesen wird. Dieser Text enthält eine Audiobeschreibung des Zwecks des Formularfelds und kann Informationen über den Titel, die Beschreibung, den Namen und alle relevanten Nachrichten (benutzerdefinierten Text) des Felds enthalten. Der Text der Bildschirmlesehilfe hilft sicherzustellen, dass das Formular allen Benutzenden zugänglich ist, auch Personen mit Sehschwäche, und bietet ihnen ein umfassendes Verständnis des Formularfelds und seiner Anforderungen.

   - **Benutzerdefinierter Text**: Wählen Sie diese Option aus, um den benutzerdefinierten Text für ARIA-Barrierefreiheitsbeschriftungen zu verwenden. Wenn Sie diese Option auswählen, wird das Benutzerdefinierter Dialogfeld „Text“ angezeigt. Sie können relevante Informationen im Benutzerdefinierter Dialogfeld „Text“ hinzufügen.
   - **Beschreibung**: Wählen Sie diese Option aus, um die Beschreibung für ARIA-Barrierefreiheitsbeschriftungen zu verwenden.
   - **Titel**: Wählen Sie diese Option aus, um den Titel für ARIA-Barrierefreiheitsbeschriftungen zu verwenden.
   - **Name**: Wählen Sie diese Option aus, um den Namen für ARIA-Barrierefreiheitsbeschriftungen zu verwenden.
   - **Keine**: Wählen Sie diese Option aus, wenn Sie keine ARIA-Barrierefreiheitsbezeichnungen hinzufügen möchten.

## Dialogfeld „Design“ {#design-dialog}

Das Dialogfeld „Design“ wird verwendet, um CSS-Stile für die Komponente „Dateianhang“ zu definieren und zu verwalten.

### Registerkarte „Stile“ {#styles-tab}

Die Kernkomponente „Dateianhänge“ für adaptive Formulare unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).

![Dialogfeld „Design“](/help/adaptive-forms/assets/checkbox-style.png)

- **Standard-CSS-Klassen**: Sie können eine standardmäßige CSS-Klasse für die Kernkomponente „Dateianhänge“ für adaptive Formulare bereitstellen.

- **Zulässige Stile**: Sie können Stile definieren, indem Sie den Namen und die CSS-Klasse für den Stil angeben. Sie können beispielsweise einen Stil mit dem Namen „Fettschrift“ erstellen und die CSS-Klasse „Schriftbreite: Fett“ bereitstellen. Sie können diese Stile bei einem adaptiven Formular im adaptiven Formular-Editor anwenden. Um einen Stil anzuwenden, wählen Sie im Editor für adaptive Formulare die Komponente aus, auf die Sie den Stil anwenden möchten, navigieren Sie zum Eigenschaften-Dialog und wählen Sie den gewünschten Stil aus der Dropdown-Liste **Stile**. Wenn Sie die Stile aktualisieren oder ändern müssen, kehren Sie einfach zum Dialogfeld „Design“ zurück, aktualisieren die Stile auf der Registerkarte „Stile“ und speichern die Änderungen.

### Benutzerdefinierte Eigenschaften

![Dialogfeld „Benutzerdefinierte Eigenschaften“](/help/adaptive-forms/assets/checkbox-customproperties.png)

Mit der Option „Benutzerdefinierte Eigenschaften“ können Sie mithilfe der Formularvorlage benutzerdefinierte Attribute (Schlüsselwertpaare) mit einer Kernkomponente eines adaptiven Formulars verknüpfen. Die benutzerdefinierten Eigenschaften werden im Eigenschaftenbereich der Headless-Ausgabedarstellung der Komponente angezeigt. So kann ein dynamisches Formularverhalten erzeugt werden, das sich je nach den benutzerdefinierten Attributwerten anpasst. Beispielsweise können Entwickelnde verschiedene Ausgabedarstellungen einer Headless-Formularkomponente für Mobile-, Desktop- oder Web-Plattformen entwerfen und so das Benutzererlebnis auf einer Vielzahl von Geräten erheblich verbessern.

- **Gruppenname**: Sie können einen Namen angeben, um die Gruppe der benutzerdefinierten Eigenschaften zu kennzeichnen. Sie können mehrere Gruppen benutzerdefinierter Eigenschaften hinzufügen, löschen oder neu anordnen. Nach dem Hinzufügen der Gruppe benutzerdefinierter Eigenschaften werden folgende Optionen angezeigt:

   - **Schlüssel-Wert-Paare**: Sie können mehrere Namen und Werte benutzerdefinierter Eigenschaften hinzufügen, indem Sie für jede Gruppe benutzerdefinierter Eigenschaften auf **Hinzufügen** klicken.

   - **Löschen**: Tippen oder klicken Sie auf diese Option, um den Namen und den Wert der benutzerdefinierten Eigenschaft zu löschen.

   - **Neu anordnen**: Ordnen Sie den Namen und Wert der benutzerdefinierten Eigenschaft Antippen oder Klicken und Ziehen neu an.
<!--

## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html)

-->

## Ähnliche Artikel {#related-articles}

{{more-like-this}}

## Siehe auch {#see-also}

{{see-also}}
