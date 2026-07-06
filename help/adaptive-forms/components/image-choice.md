---
title: Kernkomponente „Bildauswahl“ für adaptive Forms
description: Verwenden der Kernkomponente „Bildauswahl“.
role: Developer, Admin, User
hide: true
source-git-commit: 0af65c80f9cc58c4ba48d5b3dc7a026820bd2833
workflow-type: tm+mt
source-wordcount: '1318'
ht-degree: 58%

---

# Adaptives Formular - Bildauswahl-Feld {#image-choice}

Die Bildauswahl-Komponente in einem Formular ermöglicht es Benutzenden, Auswahlen basierend auf visuellen Darstellungen (z. B. Bildern) und nicht auf textbasierten Optionen vorzunehmen. Es stellt eine Reihe von Bildern dar, die jeweils eine eigene Auswahl darstellen. Benutzer können ein oder mehrere Bilder auswählen, wobei visuelles Feedback ihre Auswahl angibt. Diese Komponente ist für Optionen wie Produktvarianten, Umfrageantworten oder Profilbilder nützlich. Es verbessert die Benutzerinteraktion und Klarheit durch eine intuitive, visuell ansprechende Auswahlmethode.

## Nutzung

Es gibt mehrere wichtige Funktionen der Bildauswahl-Komponente wie:

- **Bilddarstellung:** Benutzer sehen Bilder anstelle von herkömmlichen Textbeschriftungen oder Optionsfeldern. Jedes Bild entspricht einer Auswahl, die ausgewählt werden kann, wodurch eine visuelle Darstellung der verfügbaren Optionen bereitgestellt wird.

- **Anklickbare Bilder:** Benutzer können eine Option auswählen, indem sie direkt auf das Bild klicken. Das ausgewählte Bild wird oft hervorgehoben, um anzuzeigen, dass es ausgewählt wurde.

- **Einzelne oder mehrere Auswahlen:** Je nach Design der Komponente können Benutzende entweder ein einzelnes Bild oder mehrere Bilder auswählen.

## Version und Kompatibilität {#version-and-compatibility}

Die Adaptive Forms Image Choice-Komponente wurde als Teil der Kernkomponenten 2.0.64 veröffentlicht. Hier finden Sie eine Tabelle mit allen unterstützten Versionen, AEM-Kompatibilität und Links zur entsprechenden Dokumentation:

| Komponentenversion | AEM as a Cloud Service |
|---|---|
| v1 | Kompatibel mit<br>[Version 2.0.64](/help/adaptive-forms/version.md) und höher |

Informationen zu Versionen und Freigaben der Kernkomponente finden Sie im Dokument [Kernkomponenten-Versionen](/help/adaptive-forms/version.md).

## Technische Details {#technical-details}

Die neuesten Informationen zur Kernkomponente „Bildauswahl“ für adaptive Forms finden Sie in der technischen Dokumentation auf [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/). Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Entwicklerdokumentation für Kernkomponenten](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Im Dialogfeld „Konfigurieren“ können Sie die Bildauswahl-Komponente einfach anpassen.


### Registerkarte „Allgemein“ {#basic-tab}

![Auswahl der Registerkarten „Allgemein“](basic-tab-imagechoice.png)

- **Name**: Sie können eine Formularkomponente sowohl im Formular als auch im Regeleditor durch ihren eindeutigen Namen identifizieren. Der Name darf keine Leerzeichen oder Sonderzeichen enthalten.

- **Titel** - Mit dem Titel können Sie einen Komponententyp in einem adaptiven Formular leicht identifizieren. Standardmäßig wird der Titel neben der Komponente angezeigt.

- **Titel ausblenden** - Sie können den Titel ausblenden, indem Sie das Kontrollkästchen „Titel ausblenden“ aktivieren.

- **Optionen** - Hiermit können Sie ein oder mehrere Bilder hinzufügen und die Bildauswahleigenschaften anpassen. Zu den Bildauswahleigenschaften gehören „Datenwert“, „Bildreferenz-Asset“ und „Alternativtext“ für jedes Bild.

- **Bindungsreferenz**: Eine Bindungsreferenz ist ein Verweis auf ein Datenelement, das in einer externen Datenquelle gespeichert ist und in einem Formular verwendet wird. Sie können mit dem Bindungsverweis Daten dynamisch an Formularfelder binden, sodass das Formular die aktuellsten Daten aus der Datenquelle anzeigen kann.

  Beispielsweise kann ein Bindungsverweis verwendet werden, um den Namen und die Adresse von Kundinnen und Kunden in einem Formular anzuzeigen, basierend auf der im Formular eingegebenen Kunden-ID. Der Bindungsverweis kann auch verwendet werden, um die Datenquelle mit den im Formular eingegebenen Daten zu aktualisieren. Auf diese Weise können Sie mit AEM Forms Formulare erstellen, die mit externen Datenquellen interagieren und so ein nahtloses Benutzererlebnis bei der Datenerfassung und -verwaltung bieten.

- **Als ungebundenes Formularelement markieren**: Mit dieser Option können Sie Formularfelder konfigurieren, die mit keinem Schema verbunden sind. Mit dieser Option können Sie Daten speichern, ohne die Datenquelle zu aktualisieren. Außerdem können Sie damit Daten auf eine benutzerdefinierte Art und Weise verarbeiten, getrennt von der standardmäßigen Datenbankintegration.

- **Datentyp des gesendeten Werts**: Diese Option gibt den Datentyp des Werts an, der bei Auswahl einer Option gesendet wird. Wenn der **Datentyp des gesendeten Werts** auf `Number` festgelegt ist und Sie auf der Registerkarte **Optionen** Zeichenfolgedaten zum **Datenwert** hinzufügen, wird am Bildschirm die Fehlermeldung `Value type mismatch` angezeigt.

- **Anzeigeoptionen**: Damit haben Sie die Möglichkeit, das Bildauswahlfeld horizontal oder vertikal anzuzeigen.

- **Standardwert**: Mit dieser Option können Sie einen Standardwert (Datenwert) in ein Formularfeld einfügen. Wenn eine **deaktivierte Komponente** oder **Schreibgeschützte Komponente** ausgewählt ist, wird der Standardwert auf dem Bildschirm angezeigt. Wenn Benutzende keinen Wert in das Formularfeld eingeben, wird dieser Wert zum Zeitpunkt der Formularübermittlung gesendet.

- **Komponente ausblenden**: Wählen Sie diese Option, um die Komponente aus dem Formular auszublenden. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor. Dies ist nützlich, wenn Sie Informationen speichern müssen, die Benutzende nicht sehen oder direkt ändern müssen.

- **Komponente deaktivieren**: Wählen Sie diese Option, um die Komponente zu deaktivieren oder zu sperren. Die deaktivierte Komponente ist nicht aktiv und Endbenutzende können sie nicht bearbeiten. Benutzende können den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor.

- **Schreibgeschützt**: Mit dieser Option können Sie einen Standardwert (Datenwert) in ein Formularfeld einfügen. Wenn eine **deaktivierte Komponente** oder **Schreibgeschützte Komponente** ausgewählt ist, wird der Standardwert auf dem Bildschirm angezeigt. Wenn Benutzende keinen Wert in das Formularfeld eingeben, wird dieser Wert zum Zeitpunkt der Formularübermittlung gesendet.

- **Auswahltyp**: Mit dieser Option können Benutzerinnen und Benutzer eine einzelne oder mehrere Auswahlfelder für die Bildauswahl auswählen.

### Registerkarte „Validierung“ {#validation-tab}

![Bildauswahl auf der Registerkarte „Validierung“](validation-tab-image-choice.png)

- **Erforderlich**: Wählen Sie diese Option, wenn Sie die Komponente in einem adaptiven Formular anzeigen möchten. Nachdem Sie die Option ausgewählt haben, müssen Sie eine Auswahl treffen, bevor Sie mit der Formularübermittlung fortfahren. Wenn diese Option aktiviert ist **kann die Option** Komponente ausblenden“ oder **Komponente deaktivieren** auf der Registerkarte **Allgemein“ nicht ausgewählt werden.

- **Fehlermeldung** - Mit dieser Option können Sie eine Nachricht eingeben, die angezeigt wird, wenn das Kontrollkästchen **Erforderlich** aktiviert ist und das Feld für die Bildauswahl nicht ausgewählt ist.

- **Meldung zur Skriptvalidierung**: Mit dieser Option können Sie eine Meldung eingeben, die angezeigt werden soll, wenn die Skriptvalidierung fehlschlägt.

### Registerkarte „Hilfe-Inhalt“ {#helpcontent-tab}

![Auswahl des Hilfeinhalts und des Bildes](help-content-imagechoice.png)

- **Kurzbeschreibung**: Eine Kurzbeschreibung ist eine kurze Erklärung, die zusätzliche Informationen oder Klarstellungen über den Zweck eines Formularfelds bietet. Es hilft Benutzenden zu verstehen, welcher Datentyp in das Feld eingegeben werden soll, und kann Richtlinien oder Beispiele bereitstellen, um sicherzustellen, dass die eingegebenen Informationen gültig sind und die gewünschten Kriterien erfüllen. Standardmäßig bleiben kurze Beschreibungen ausgeblendet. Aktivieren Sie die Option **Kurzbeschreibung immer anzeigen**, um sie unterhalb der Komponente anzuzeigen.

- **Kurzbeschreibung immer anzeigen**: Aktivieren Sie diese Option, um die Kurzbeschreibung unterhalb der Komponente anzuzeigen.

- **Hilfetext**: Hilfetext bezieht sich auf zusätzliche Informationen oder Anleitungen, die den Benutzenden bereitgestellt werden, um sie beim korrekten Ausfüllen eines Formularfelds zu unterstützen. Er erscheint, wenn Benutzende auf das Hilfesymbol (i) neben der Komponente klicken. Hilfetext enthält detailliertere Informationen als die Beschriftung oder der Platzhaltertext eines Formularfelds und soll den Benutzenden dabei helfen, die Anforderungen oder Einschränkungen des Felds zu verstehen. Er kann auch Vorschläge oder Beispiele anbieten, um das Ausfüllen des Formulars einfacher und genauer zu gestalten.



### Registerkarte „Barrierefreiheit“ {#accessibility-tab}

![Barrierefreiheit der Bildauswahl](accessibility-imagechoice.png)

- **Text für Bildschirmlesehilfen**: Text für Bildschirmlesehilfen bezieht sich auf zusätzlichen Text, der für Hilfstechnologien wie Bildschirmlesehilfen vorgesehen ist, die von Personen mit Sehschwäche verwendet werden. Dieser Text enthält eine Audiobeschreibung des Zwecks des Formularfelds und kann Informationen über den Titel, die Beschreibung, den Namen und alle relevanten Nachrichten (benutzerdefinierten Text) des Felds enthalten. Der Text der Bildschirmlesehilfe hilft sicherzustellen, dass das Formular allen Benutzenden zugänglich ist, auch Personen mit Sehschwäche, und bietet ihnen ein umfassendes Verständnis des Formularfelds und seiner Anforderungen.
   - **Benutzerdefinierter Text**: Wählen Sie diese Option aus, um den benutzerdefinierten Text für ARIA-Barrierefreiheitsbeschriftungen zu verwenden. Wenn Sie diese Option auswählen, wird das Benutzerdefinierter Dialogfeld „Text“ angezeigt. Sie können relevante Informationen im Benutzerdefinierter Dialogfeld „Text“ hinzufügen.
   - **Titel**: Wählen Sie diese Option aus, um den Titel für ARIA-Barrierefreiheitsbeschriftungen zu verwenden.

## Ähnliche Artikel {#related-articles}

{{more-like-this}}

## Siehe auch {#see-also}

{{see-also}}


