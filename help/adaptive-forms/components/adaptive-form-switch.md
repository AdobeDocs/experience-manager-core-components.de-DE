---
title: Kernkomponente für adaptive Formulare – Komponente „Schalter“
description: Verwenden oder Anpassen der Kernkomponente „Schalter“ für adaptive Formulare.
role: Architect, Developer, Admin, User
exl-id: 6ff2ca76-1514-42eb-bde3-60259af2d187
source-git-commit: 4c510b8fe59f4be6e1b329ee4257ab1b780fbf22
workflow-type: tm+mt
source-wordcount: '1922'
ht-degree: 98%

---

# Komponente für adaptiven Formularwechsel{#switch-adaptive-forms-core-component}

Die Komponente „Schalter“ ist eine grafische Benutzeroberfläche, die in Formularen verwendet wird und es Benutzenden ermöglicht, zwischen zwei Optionen auszuwählen. Normalerweise handelt es sich dabei um einen Umschalter mit zwei Status, mit dem Benutzende zwischen zwei Status wählen können: Aktivierung oder Deaktivierung einer Funktion oder einer Einstellung. Die Komponente „Schalter“ wurde entwickelt, um den aktuellen Status visuell darzustellen und anzuzeigen, ob eine bestimmte Funktion aktiviert oder deaktiviert ist.

Die Komponente „Schalter“ ist ein boolesches Steuerungselement, das den Wert auf „true“ oder „false“ setzt. Beispielsweise wird es verwendet, um eine Funktion ein- oder auszuschalten, z. B. um einen Ton ein- oder auszuschalten oder Bluetooth oder WLAN zu aktivieren bzw. zu deaktivieren.

![Beispiel für die Komponente „Schalter“](/help/adaptive-forms/assets/switch-example.png)

## Verwendung {#reasons-to-use-switch}

Die häufigsten Gründe für die Verwendung von einem Schalter in einem adaptiven Formular sind:

- **Benutzerinteraktion**: Benutzende können mit der Komponente „Schalter“ interagieren, indem sie darauf klicken oder tippen.

- **Status**: Die Komponente „Schalter“ hat zwei Status: EIN und AUS. Der anfänglichen Status der Komponente „Schalter“ hängt von der Standardeinstellung oder dem aktuellen Status der Funktion ab, die sie steuert.

- **Visuelle Darstellung**: Der aktuellen Status der Komponente „Schalter“ wird visuell widergespiegelt, indem sich ihre Farbe oder Position verändert.

- **Kontrollfunktionen**: Die Komponente „Schalter“ wird verwendet, um bestimmte Funktionen in einem AEM-Formular zu aktivieren oder zu deaktivieren. So können Benutzer bzw. Benutzerinnen beispielsweise eine Funktion aktivieren oder deaktivieren.

## Version und Kompatibilität {#version-and-compatibility}

Die Kernkomponente „Schalter“ für adaptive Formulare wurde als Teil der Kernkomponenten 2.0.64 veröffentlicht. Hier finden Sie eine Tabelle mit allen unterstützten Versionen, AEM-Kompatibilität und Links zur entsprechenden Dokumentation:

|  |  |
|---|---|
| Komponentenversion | AEM as a Cloud Service |
| --- | --- |
| v1 | Kompatibel mit<br>[Version 2.0.64](/help/adaptive-forms/version.md) und höher | Kompatibel | Kompatibel |

Informationen zu Versionen und Freigaben der Kernkomponente finden Sie im Dokument [Kernkomponenten-Versionen](/help/adaptive-forms/version.md).

## Technische Details {#technical-details}

Aktuelle Informationen zur Kernkomponente „Schalter“ für adaptive Formulare finden Sie in der technischen Dokumentation auf [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/switch/v1/switch). Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Entwicklerdokumentation für Kernkomponenten](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Im Dialogfeld „Konfigurieren“ können Sie das Erlebnis für die Komponente „Schalter“ für Besuchende ganz einfach anpassen. Sie können auch Optionen für die Komponente „Schalter“ definieren, um das Benutzererlebnis zu verbessern.

### Registerkarte „Allgemein“

![Registerkarte „Allgemein“](/help/adaptive-forms/assets/switch-basic.png)

- **Name**: Sie können eine Formularkomponente sowohl im Formular als auch im Regeleditor durch ihren eindeutigen Namen identifizieren. Der Name darf keine Leerzeichen oder Sonderzeichen enthalten.

- **Titel**: Mit dem Titel können Sie eine Komponente in einem Formular leicht identifizieren. Standardmäßig wird der Titel neben der Komponente angezeigt. Wenn Sie keinen Titel hinzufügen, wird die Komponente nicht angezeigt.
- **Rich-Text für Titel zulassen**: Diese Funktionen ermöglichen es Benutzenden, einfache Texttitel zu formatieren, die Funktionen wie fett, kursiv, unterstrichener Text, verschiedene Schriftarten, Schriftgrößen, Farben und zusätzliche Optionen enthalten und so die visuelle Darstellung und Anpassung zu verbessern. Sie bietet mehr Flexibilität und kreative Kontrolle bei der Hervorhebung von Titeln in Dokumenten, Websites oder Anwendungen.\
  Durch Aktivieren des Kontrollkästchens **Rich-Text für Titel zulassen** werden Formatierungsoptionen sichtbar, mit denen Sie den Titel der Komponente gestalten können. Um auf alle verfügbaren Formatierungsoptionen zuzugreifen, können Sie auf die Registerkarte ![Vollbildsymbol](/help/adaptive-forms/assets/fullscreen-icon.png) klicken.

  ![Rich-Text-Unterstützung](/help/adaptive-forms/assets/richtext-support-title.png)

- **Titel ausblenden**: Wählen Sie die Option aus, um den Titel der Komponente auszublenden.

- **Wert des Status „Deaktivieren“ beibehalten** – Wenn Sie diese Option auswählen, können Sie den Wert angeben, der zurückgegeben werden soll, wenn die Komponente „Schalter“ nicht ausgewählt ist.
- **Optionen** – Geben Sie den Datenwert und den Anzeigetext für jede Option an.
   - **Aktivierter Datenwert** – Geben Sie den Wert an, der gesendet werden soll, wenn der Schalter in einem adaptiven Formular aktiviert ist.
   - **Aktivierte Textanzeige** – Geben Sie den Text an, der als Beschriftung angezeigt werden soll, wenn der Schalter in einem adaptiven Formular aktiviert wird.
   - **Deaktivierter Datenwert** – Geben Sie den Wert an, der gesendet werden soll, wenn der Schalter in einem adaptiven Formular nicht aktiviert ist. Diese Option ist nur sichtbar, wenn der Schalter **Wert des Status „Deaktivieren“ beibehalten** aktiviert ist.
   - **Deaktivierter Anzeigetext** – Geben Sie den Text an, der als Beschriftung angezeigt werden soll, wenn der Schalter in einem adaptiven Formular nicht aktiviert ist. Diese Option ist nur sichtbar, wenn der Schalter **Wert des Status „Deaktivieren“ beibehalten** aktiviert ist.

  Sie können die Optionen für die Schalterkomponente auch mit **Rich-Text für Optionen zulassen** formatieren.

  ![Rich-Text-Unterstützung für Optionen](/help/adaptive-forms/assets/switch-optipn-rich-text.png)

  Durch Aktivieren des Kontrollkästchens **Rich-Text für Optionen zulassen** werden Formatierungsoptionen sichtbar, mit denen Sie die Optionen der Komponente gestalten können. Um auf alle verfügbaren Formatierungsoptionen zuzugreifen, können Sie auf die Registerkarte `Fullscreen` ![Vollbildsymbol](/help/adaptive-forms/assets/fullscreen-icon.png) klicken.

  ![Rich-Text-Unterstützung für Optionen](/help/adaptive-forms/assets/switch-richtext-for-display.png)

- **Verbindungsreferenz**: Eine Verbindungsreferenz ist ein Verweis auf ein Datenelement, das in einer externen Datenquelle gespeichert ist und in einem Formular verwendet wird. Sie können mit dem Bindungsverweis Daten dynamisch an Formularfelder binden, sodass das Formular die aktuellsten Daten aus der Datenquelle anzeigen kann. Beispielsweise kann ein Bindungsverweis verwendet werden, um den Namen und die Adresse von Kundinnen und Kunden in einem Formular anzuzeigen, basierend auf der im Formular eingegebenen Kunden-ID. Der Bindungsverweis kann auch verwendet werden, um die Datenquelle mit den im Formular eingegebenen Daten zu aktualisieren. Auf diese Weise können Sie mit AEM Forms Formulare erstellen, die mit externen Datenquellen interagieren und so ein nahtloses Benutzererlebnis bei der Datenerfassung und -verwaltung bieten.
- **Als ungebundenes Formularelement markieren**: Mit dieser Option können Sie Formularfelder konfigurieren, die mit keinem Schema verbunden sind. Mit dieser Option können Sie Daten speichern, ohne die Datenquelle zu aktualisieren. Außerdem können Sie damit Daten auf eine benutzerdefinierte Art und Weise verarbeiten, getrennt von der standardmäßigen Datenbankintegration.

- **Datentyp des gesendeten Werts**: Diese Option gibt den Datentyp des Werts an, der bei Auswahl einer Option gesendet wird. Wenn der **Datentyp des gesendeten Werts** auf `Number` festgelegt ist und Sie auf der Registerkarte **Optionen** Zeichenfolgedaten zum **Datenwert** hinzufügen, wird auf dem Bildschirm die Fehlermeldung `Value type mismatch` angezeigt.
- **Komponente ausblenden**: Wählen Sie diese Option, um die Komponente aus dem Formular auszublenden. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor. Dies ist nützlich, wenn Sie Informationen speichern müssen, die Benutzende nicht sehen oder direkt ändern müssen.

- **Komponente deaktivieren**: Mit dieser Option können Sie die Komponente deaktivieren oder sperren. Die deaktivierte Komponente ist nicht aktiv und Endbenutzende können sie nicht bearbeiten. Benutzende können den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor.

- **Standardwert**: Mit dieser Option können Sie einen Standardwert in ein Formularfeld einfügen. Wenn **Komponente deaktiviert** oder **Schreibgeschützte Komponente** ausgewählt ist, wird der Standardwert auf dem Bildschirm angezeigt. Wenn Benutzende keinen Wert in das Formularfeld eingeben, wird dieser Wert zum Zeitpunkt der Formularübermittlung gesendet.

### Registerkarte „Validierung“ {#validation-tab}

![Registerkarte „Validierung“](/help/adaptive-forms/assets/switch-validation.png)

- **Erforderlich**: Wählen Sie diese Option, wenn Sie die Komponente in einem adaptiven Formular anzeigen möchten. Nachdem Sie die Option ausgewählt haben, müssen Sie eine Auswahl treffen, bevor Sie mit der Formularübermittlung fortfahren. Wenn diese Option aktiviert ist, kann die Option **Komponente ausblenden** oder **Komponente deaktivieren** auf der Registerkarte **Allgemein** nicht ausgewählt werden.

- **Fehlermeldung**: Mit dieser Option können Sie eine Nachricht eingeben, die angezeigt wird, wenn das Kontrollkästchen **Erforderlich** aktiviert ist und das Feld leer bleibt.

- **Meldung zur Skriptvalidierung**: Mit dieser Option können Sie eine Meldung eingeben, die angezeigt werden soll, wenn die Skriptvalidierung fehlschlägt.

### Registerkarte „Hilfe-Inhalt“ {#helpcontent-tab}

![Registerkarte „Hilfe-Inhalt“](/help/adaptive-forms/assets/switch-help.png)

- **Kurzbeschreibung**: Eine Kurzbeschreibung ist eine kurze Erklärung, die zusätzliche Informationen oder Klarstellungen über den Zweck eines Formularfelds bietet. Es hilft Benutzenden zu verstehen, welcher Datentyp in das Feld eingegeben werden soll, und kann Richtlinien oder Beispiele bereitstellen, um sicherzustellen, dass die eingegebenen Informationen gültig sind und die gewünschten Kriterien erfüllen. Standardmäßig bleiben kurze Beschreibungen ausgeblendet. Aktivieren Sie die Option **Kurzbeschreibung immer anzeigen**, um sie unterhalb der Komponente anzuzeigen.

- **Kurzbeschreibung immer anzeigen**: Aktivieren Sie diese Option, um die Kurzbeschreibung unterhalb der Komponente anzuzeigen.

- **Hilfetext**: Hilfetext bezieht sich auf zusätzliche Informationen oder Anleitungen, die den Benutzenden bereitgestellt werden, um sie beim korrekten Ausfüllen eines Formularfelds zu unterstützen. Er erscheint, wenn Benutzende auf das Hilfesymbol (i) neben der Komponente klicken. Hilfetext enthält detailliertere Informationen als die Beschriftung oder der Platzhaltertext eines Formularfelds und soll den Benutzenden dabei helfen, die Anforderungen oder Einschränkungen des Felds zu verstehen. Er kann auch Vorschläge oder Beispiele anbieten, um das Ausfüllen des Formulars einfacher und genauer zu gestalten.

### Registerkarte „Barrierefreiheit“ {#accessibility-tab}

![Registerkarte „Barrierefreiheit“](/help/adaptive-forms/assets/switch-accessibility.png)

- **Text für Bildschirmlesehilfen**: Text für Bildschirmlesehilfen bezieht sich auf zusätzlichen Text, der für Hilfstechnologien wie Bildschirmlesehilfen vorgesehen ist, die von Personen mit Sehschwäche verwendet werden. Dieser Text enthält eine Audiobeschreibung des Zwecks des Formularfelds und kann Informationen über den Titel, die Beschreibung, den Namen und alle relevanten Nachrichten (benutzerdefinierten Text) des Felds enthalten. Der Text der Bildschirmlesehilfe hilft sicherzustellen, dass das Formular allen Benutzenden zugänglich ist, auch Personen mit Sehschwäche, und bietet ihnen ein umfassendes Verständnis des Formularfelds und seiner Anforderungen.
   - **Benutzerdefinierter Text**: Wählen Sie diese Option aus, um den benutzerdefinierten Text für ARIA-Barrierefreiheitsbeschriftungen zu verwenden. Wenn Sie diese Option auswählen, wird das Benutzerdefinierter Dialogfeld „Text“ angezeigt. Sie können relevante Informationen im Benutzerdefinierter Dialogfeld „Text“ hinzufügen.
   - **Beschreibung**: Wählen Sie diese Option aus, um die Beschreibung für ARIA-Barrierefreiheitsbeschriftungen zu verwenden.
   - **Titel**: Wählen Sie diese Option aus, um den Titel für ARIA-Barrierefreiheitsbeschriftungen zu verwenden.
   - **Name**: Wählen Sie diese Option aus, um den Namen für ARIA-Barrierefreiheitsbeschriftungen zu verwenden.
   - **Keine**: Wählen Sie diese Option aus, wenn Sie keine ARIA-Barrierefreiheitsbezeichnungen hinzufügen möchten.

### Registerkarte „Stile“ {#styles-tab}

![Registerkarte „Stile“](/help/adaptive-forms/assets/switch-styles.png)

- **Beschriftungen ausblenden** – Wählen Sie diese Option aus, um die Beschriftungen der Komponente „Schalter“ auszublenden.

- **Beschriftungen anzeigen** – Wählen Sie diese Option aus, um die Beschriftungen der Komponente „Schalter“ anzuzeigen.

## Dialogfeld „Design“ {#design-dialog}

Das Dialogfeld „Design“ wird verwendet, um CSS-Stile für die Komponente „Schalter“ zu definieren und zu verwalten.

### Registerkarte „Stile“ {#styles-design-tab}

Die Kernkomponente „Schalter“ für adaptive Formulare unterstützt das [AEM-Stilsystem](/help/get-started/authoring.md#component-styling).

![Dialogfeld „Design“](/help/adaptive-forms/assets/checkbox-style.png)

- **Standard-CSS-Klassen**: Sie können eine Standard-CSS-Klasse für die Adaptive Forms Switch-Kernkomponente bereitstellen.

- **Zulässige Stile**: Sie können Stile definieren, indem Sie den Namen und die CSS-Klasse für den Stil angeben. Sie können beispielsweise einen Stil mit dem Namen „Fettschrift“ erstellen und die CSS-Klasse „Schriftbreite: Fett“ bereitstellen. Sie können diese Stile bei einem adaptiven Formular im adaptiven Formular-Editor anwenden. Um einen Stil anzuwenden, wählen Sie im Editor für adaptive Formulare die Komponente aus, auf die Sie den Stil anwenden möchten, navigieren Sie zum Eigenschaften-Dialog und wählen Sie den gewünschten Stil aus der Dropdown-Liste **Stile**. Wenn Sie die Stile aktualisieren oder ändern müssen, kehren Sie einfach zum Dialogfeld „Design“ zurück, aktualisieren die Stile auf der Registerkarte „Stile“ und speichern die Änderungen.

### Benutzerdefinierte Eigenschaften

![Dialogfeld „Benutzerdefinierte Eigenschaften“](/help/adaptive-forms/assets/checkbox-customproperties.png)

Mit der Option „Benutzerdefinierte Eigenschaften“ können Sie mithilfe der Formularvorlage benutzerdefinierte Attribute (Schlüsselwertpaare) mit einer Kernkomponente eines adaptiven Formulars verknüpfen. Die benutzerdefinierten Eigenschaften werden im Eigenschaftenbereich der Headless-Ausgabedarstellung der Komponente angezeigt. So kann ein dynamisches Formularverhalten erzeugt werden, das sich je nach den benutzerdefinierten Attributwerten anpasst. Beispielsweise können Entwickelnde verschiedene Ausgabedarstellungen einer Headless-Formularkomponente für Mobile-, Desktop- oder Web-Plattformen entwerfen und so das Benutzererlebnis auf einer Vielzahl von Geräten erheblich verbessern.
- **Gruppenname**: Sie können einen Namen angeben, um die Gruppe der benutzerdefinierten Eigenschaften zu kennzeichnen. Sie können mehrere Gruppen benutzerdefinierter Eigenschaften hinzufügen, löschen oder neu anordnen. Nach dem Hinzufügen der Gruppe benutzerdefinierter Eigenschaften werden folgende Optionen angezeigt:

   - **Schlüssel-Wert-Paare**: Sie können mehrere Namen und Werte benutzerdefinierter Eigenschaften hinzufügen, indem Sie für jede Gruppe benutzerdefinierter Eigenschaften auf **Hinzufügen** klicken.

   - **Löschen**: Tippen oder klicken Sie auf diese Option, um den Namen und den Wert der benutzerdefinierten Eigenschaft zu löschen.

   - **Neu anordnen**: Ordnen Sie den Namen und Wert der benutzerdefinierten Eigenschaft Tippen oder Klicken und Ziehen neu an.

## Ähnliche Artikel {#related-articles}

{{more-like-this}}

## Siehe auch {#see-also}

{{see-also}}
