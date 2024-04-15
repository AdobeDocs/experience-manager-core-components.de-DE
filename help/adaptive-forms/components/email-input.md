---
title: Kernkomponente „E-Mail-Eingabe“ für adaptive Formulare
description: Verwenden oder Anpassen der Kernkomponente „E-Mail-Eingabe“ für adaptive Formulare.
role: Architect, Developer, Admin, User
exl-id: f6a2974b-991e-4cea-9ef8-0b03e8975eeb
source-git-commit: 79b99d4f6b5a2b186ff3dbf570a58dc86bf24d4a
workflow-type: tm+mt
source-wordcount: '2054'
ht-degree: 93%

---

# E-Mail-Eingabe {#Email-input-adaptive-forms-core-component}

<span class="preview"> Dieser Artikel enthält Inhalte zum **Rich-Text für Titel zulassen** -Funktion, einer Funktion vor der Veröffentlichung. Die Vorabversion-Funktion ist nur über unsere [Pre-Release-Kanal](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/release-notes/prerelease.html?lang=de#new-features).</span>

Die Kernkomponente „E-Mail-Eingabe“ für adaptive Formulare wird verwendet, um E-Mail-Adressen von Benutzenden zu erfassen. Über das E-Mail-Eingabefeld kann der Browser überprüfen, ob die eingegebenen Daten ein gültiges E-Mail-Adressformat haben. Es wird normalerweise als Textfeld dargestellt und verfügt über Mustervalidierungen, damit nur gültige E-Mail-Adressen akzeptiert werden. Das E-Mail-Eingabefeld kann mit zusätzlichen Attributen wie „erforderlich“, „Platzhalter“ und „Muster“ weiter angepasst werden, um Validierungsverfahren für die Eingabedaten festzulegen.

**Beispiel**
![Beispiel](/help/adaptive-forms/assets/emailid-example.png)

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

Es gibt verschiedene Gründe, warum es sinnvoll ist, eine E-Mail-Eingabe-Komponente in ein adaptives Formular einzufügen:

- **Benutzerfreundlichkeit**: Eine E-Mail-Eingabe erleichtert den Benutzenden die Eingabe ihrer E-Mail-Adressen, da sie unmissverständlich angibt, welche Daten in diesem Feld erwartet werden.

- **Personalisierte Kommunikation**: Das Erfassen von E-Mail-Adressen von Benutzenden über ein Formular ermöglicht eine personalisierte Kommunikation, z. B. das Senden von Bestätigungs-E-Mails oder Newslettern.

- **Lead-Generierung**: Durch die Erfassung von E-Mail-Adressen über ein Formular können Unternehmen eine E-Mail-Liste erstellen und für die Lead-Generierung verwenden.

- **Benutzerauthentifizierung**: E-Mail-Adressen können zur Authentifizierung für den Zugriff auf beschänkt zugängliche Inhalte oder Dienste verwendet werden.

- **Feedback-Sammlung**: Eine E-Mail-Eingabe in einem Feedback-Formular ermöglicht es Unternehmen, mit Benutzenden zu kommunizieren, um ihr Feedback einzuholen oder darauf zu reagieren.

## Version und Kompatibilität {#version-and-compatibility}

Die Kernkomponente „Akkordeon“ für adaptive Formulare wurde im Februar 2023 als Teil der Kernkomponenten 2.0.4 für Cloud Service und der Kernkomponenten 1.1.12 für AEM 6.5.16.0 Forms oder höher veröffentlicht. Hier finden Sie eine Tabelle mit allen unterstützten Versionen, AEM-Kompatibilität und Links zur entsprechenden Dokumentation:

| Komponentenversion | AEM as a Cloud Service | AEM 6.5.16.0 Forms oder höher |
|---|---|---|
| v1 | Kompatibel mit<br>[Version 2.0.4](/help/adaptive-forms/version.md) und höher | Kompatibel mit<br>[Version 1.1.12](/help/adaptive-forms/version.md) und höher (aber nur bis Version 2.0.0). |

Informationen zu Versionen und Freigaben der Kernkomponente finden Sie im Dokument [Kernkomponenten-Versionen](/help/adaptive-forms/version.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technische Details {#technical-details}

Die neuesten Informationen über die Kernkomponente „E-Mail-Eingabe“ für adaptive Formulare finden Sie in der technischen Dokumentation auf [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/emailinput/v1/emailinput). Sie finden weitere Informationen zur Entwicklung von Kernkomponenten in der [Entwicklerdokumentation für Kernkomponenten](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Im Dialogfeld „Konfigurieren“ können Sie die E-Mail-Eingabe einfach anpassen. Sie können auch Optionen für die E-Mail-Eingabe definieren, um das Benutzererlebnis zu verbessern.

### Registerkarte „Allgemein“ {#basic-tab}

![Registerkarte „Allgemein“](/help/adaptive-forms/assets/email_basictab.png)

- **Name**: Der Name identifiziert die Komponente eindeutig im Regel-Editor. Sonderzeichen und Leerzeichen sind in den Namensfolgen nicht zulässig.

- **Titel**: Mit dem Titel können Sie eine Komponente in einem Formular leicht identifizieren. Standardmäßig wird der Titel über der Komponente angezeigt. Wenn Sie keinen Titel hinzufügen, wird der Name der Komponente anstelle des Titeltexts angezeigt.
- **Rich-Text für Titel zulassen** - Diese Funktionen ermöglichen es Benutzern, einfache Texttitel zu formatieren, die Funktionen wie fett, kursiv, unterstrichen Text, verschiedene Schriftarten, Schriftgrößen, Farben und zusätzliche Optionen enthalten, um die visuelle Präsentation und Anpassung zu verbessern. Es bietet mehr Flexibilität und kreative Kontrolle, damit Titel in Dokumenten, Websites oder Anwendungen hervorgehoben werden.\
  Nach Auswahl des Kontrollkästchens für **Rich-Text für Titel zulassen** , werden Formatierungsoptionen angezeigt, um den Titel der Komponente zu formatieren. Um auf alle verfügbaren Formatierungsoptionen zuzugreifen, können Sie auf die ![Symbol &quot;Vollbild&quot;](/help/adaptive-forms/assets/fullscreen-icon.png) Registerkarte.

  ![Rich-Text-Unterstützung](/help/adaptive-forms/assets/richtext-support-title.png)

- **Titel ausblenden**: Wählen Sie diese Option aus, um den Titel der Komponente auszublenden.

- **Platzhaltertext** – Platzhaltertext in einer Formularkomponente ist eine kurze Beschriftung oder Eingabeaufforderung in einem Eingabefeld, um Benutzende darüber zu informieren, welchen Text sie in dieses Feld eingeben sollen. Der Platzhaltertext verschwindet, wenn Benutzende mit der Eingabe in das Feld beginnen, und erscheint wieder, wenn das Feld leer bleibt. Er stellt einen visuellen Hinweis für Benutzende bereit, fungiert jedoch nicht als permanente Beschriftung oder Wert für das Feld.
- **Bindungsverweis**: Bindungsverweis ist ein Verweis auf ein Datenelement, das in einer externen Datenquelle gespeichert ist und in einem Formular verwendet wird. Sie können mit dem Bindungsverweis Daten dynamisch an Formularfelder binden, sodass das Formular die aktuellsten Daten aus der Datenquelle anzeigen kann. Beispielsweise kann ein Bindungsverweis verwendet werden, um den Namen und die Adresse von Kundinnen und Kunden in einem Formular anzuzeigen, basierend auf der im Formular eingegebenen Kunden-ID. Der Bindungsverweis kann auch verwendet werden, um die Datenquelle mit den im Formular eingegebenen Daten zu aktualisieren. Auf diese Weise können Sie mit AEM Forms Formulare erstellen, die mit externen Datenquellen interagieren und so eine nahtlose Benutzererfahrung bei der Datenerfassung und Datenverwaltung bieten.
- **Als ungebundenes Formularelement markieren**: Mit dieser Option können Sie Formularfelder konfigurieren, die mit keinem Schema verbunden sind. Mit dieser Option können Sie Daten speichern, ohne die Datenquelle zu aktualisieren. Außerdem können Sie damit Daten auf eine benutzerdefinierte Art und Weise verarbeiten, getrennt von der standardmäßigen Datenbankintegration.
- **Komponente ausblenden**: Wählen Sie diese Option, um die Komponente aus dem Formular auszublenden. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor. Dies ist nützlich, wenn Sie Informationen speichern müssen, die Benutzende nicht sehen oder direkt ändern müssen.
- **Komponente deaktivieren**: Wählen Sie die Option zum Deaktivieren der Komponente aus. Die deaktivierte Komponente ist nicht aktiv und Endbenutzende können sie nicht bearbeiten. Benutzende können den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor.
- **Schreibgeschützt**: Wählen Sie die Option aus, um die Komponente nicht bearbeitbar zu machen. Benutzende können den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor.

- **Standardwert**: Mit dieser Option können Sie einen Standardwert in ein Formularfeld einfügen. Wenn **Komponente deaktiviert** oder **Schreibgeschützte Komponente** ausgewählt ist, wird auf dem Bildschirm der Standardwert angezeigt. Wird kein Wert in das Formularfeld eingegeben, wird bei der Formularübermittlung dieser Wert gesendet.

- **Automatisches Füllattribut**: Mit der Option können Benutzer einen Wert eingeben, der automatisch im Formularfeld mit den gespeicherten Informationen eingefügt wird.

### Registerkarte „Validierung“ {#validation-tab}

![Registerkarte „Validierung“](/help/adaptive-forms/assets/email_validationtab.png)

- **Erforderlich**: Wählen Sie diese Option, wenn Sie die Komponente in einem adaptiven Formular anzeigen möchten. Nach Auswahl der Option müssen Sie einen Wert eingeben, bevor Sie mit der Formularübermittlung fortfahren. Wenn diese Option aktiviert ist, können Sie die Option **Komponente ausblenden** oder **Komponente deaktivieren** in der Registerkarte **Allgemein** nicht auswählen.

- **Fehlermeldung**: Mit dieser Option können Sie eine Nachricht eingeben, die angezeigt wird, wenn das Kontrollkästchen **Erforderlich** aktiviert ist und das Feld leer bleibt.

- **Meldung zur Skriptvalidierung**: Mit dieser Option können Sie eine Meldung eingeben, die angezeigt wird, wenn die Skriptvalidierung fehlschlägt.

- **Maximale Zeichenanzahl**: Mit dieser Option können Sie die maximal zulässige Anzahl von Zeichen im Feld angeben. Wenn Sie mehr als die in **Maximale Zeichenanzahl** festgelegten Zeichen eingeben, wird eine Fehlermeldung auf dem Bildschirm angezeigt. Über das Dialogfeld **Fehlermeldung zur maximalen Zeichenanzahl** können Sie eine benutzerdefinierte Fehlermeldung hinzufügen.

- **Fehlermeldung zur maximalen Zeichenanzahl**: Über das Dialogfeld **Fehlermeldung zur maximalen Zeichenanzahl** können Sie eine benutzerdefinierte Fehlermeldung einfügen, wenn Sie mehr Zeichen eingeben, als in der Option **Maximale Zeichenanzahl** erlaubt.

- **Mindestanzahl von Zeichen**: Mit dieser Option können Sie die zulässige Mindestanzahl von Zeichen im Feld angeben. Wenn Sie Zeichen eingeben, die kleiner sind als der Wert in **Mindestanzahl von Zeichen**, wird eine Fehlermeldung auf dem Bildschirm angezeigt. Über das Dialogfeld **Fehlermeldung zur Mindestanzahl von Zeichen** können Sie eine benutzerdefinierte Fehlermeldung hinzufügen.

- **Fehlermeldung zur Mindestanzahl von Zeichen**: Im Dialogfeld **Fehlermeldung zur Mindestanzahl von Zeichen** können Sie eine benutzerdefinierte Fehlermeldung hinzufügen, die angezeigt wird, wenn weniger Zeichen eingegeben werden als die in der Option **Mindestanzahl von Zeichen** definierten.
<br>

Mit der Option **Überprüfungsmuster** können Sie ein Muster eingeben, um die eingegebene E-Mail-ID zu validieren. Falls die E-Mail-ID nicht mit dem in der Option **Muster** eingegebenen Wert validiert werden kann, wird die Fehlermeldung auf dem Bildschirm angezeigt.

- **Muster** – Mit dieser Option können Sie die zulässigen Überprüfungsmuster für E-Mails eingeben. Reguläre Ausdrücke sind ebenfalls zulässig.
- **Fehlermeldung** – Mit dieser Option können Sie eine Meldung eingeben, die auf dem Bildschirm angezeigt wird, wenn die E-Mail-ID nicht mit dem in der Option **Muster** eingegebenen Wert validiert werden kann.

### Registerkarte „Hilfe-Inhalt“ {#help-content-tab}

![Registerkarte „Hilfe-Inhalt“](/help/adaptive-forms/assets/email_helptab.png)

- **Kurzbeschreibung**: Eine Kurzbeschreibung ist eine kurze Erklärung, die zusätzliche Informationen oder Klarstellungen über den Zweck eines Formularfelds bietet. Es hilft Benutzenden zu verstehen, welcher Datentyp in das Feld eingegeben werden soll, und kann Richtlinien oder Beispiele bereitstellen, um sicherzustellen, dass die eingegebenen Informationen gültig sind und die gewünschten Kriterien erfüllen. Standardmäßig bleiben kurze Beschreibungen ausgeblendet. Aktivieren Sie die Option **Kurzbeschreibung immer anzeigen**, um sie unterhalb der Komponente anzuzeigen.

- **Kurzbeschreibung immer anzeigen**: Aktivieren Sie diese Option, um die Kurzbeschreibung unterhalb der Komponente anzuzeigen.

- **Hilfetext**: Hilfetext bezieht sich auf zusätzliche Informationen oder Anleitungen, die den Benutzenden bereitgestellt werden, um sie beim korrekten Ausfüllen eines Formularfelds zu unterstützen. Er erscheint, wenn Benutzende auf das Hilfesymbol (i) neben der Komponente klicken. Hilfetext enthält detailliertere Informationen als die Beschriftung oder der Platzhaltertext eines Formularfelds und soll den Benutzenden dabei helfen, die Anforderungen oder Einschränkungen des Felds zu verstehen. Er kann auch Vorschläge oder Beispiele anbieten, um das Ausfüllen des Formulars einfacher und genauer zu gestalten.

### Registerkarte „Barrierefreiheit“ {#accessibility-tab}

![Registerkarte „Barrierefreiheit“](/help/adaptive-forms/assets/email_accessibilitytab.png)

**Text für Bildschirmlesehilfen** – Das ist zusätzlicher Text, der von Hilfstechnologien wie etwa Bildschirmlesehilfen für sehbehinderte Personen vorgelesen wird. Dieser Text enthält eine Audiobeschreibung des Zwecks des Formularfelds und kann Informationen über den Titel, die Beschreibung, den Namen und alle relevanten Nachrichten (benutzerdefinierten Text) des Felds enthalten. Der Text der Bildschirmlesehilfe hilft sicherzustellen, dass das Formular allen Benutzenden zugänglich ist, auch Personen mit Sehschwäche, und bietet ihnen ein umfassendes Verständnis des Formularfelds und seiner Anforderungen.

## Dialogfeld „Design“ {#design-dialog}

Das Design-Dialogfeld wird verwendet, um CSS-Stile für die E-Mail-Eingabe-Komponente zu definieren und zu verwalten.

### Registerkarte „Stile“ {#styles-tab}

Sie können die Registerkarte zum Definieren und Verwalten von CSS-Stilen für eine Komponente verwenden. Die Kernkomponente „E-Mail-Eingabe“ für adaptive Formulare unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).

![Registerkarte „Stile“](/help/adaptive-forms/assets/datepicker_styletab.png)

- **Standard-CSS-Klassen**: Sie können für die Kernkomponente „E-Mail-Eingabe“ für adaptive Formulare eine Standard-CSS-Klasse bereitstellen.

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
