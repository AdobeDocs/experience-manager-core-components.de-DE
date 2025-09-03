---
title: Kernkomponente für adaptive Formulare – Freihandsignatur
description: Verwenden oder Anpassen der Kernkomponente „Freihandsignatur“ in adaptiven Formularen.
role: Architect, Developer, Admin, User
exl-id: 608c4368-d539-4d05-a75c-c077ea822f93
source-git-commit: 006f6c844ab9e7a784dabea026867939445479e9
workflow-type: tm+mt
source-wordcount: '1761'
ht-degree: 98%

---

# Komponente „Freihandsignatur“

<span>Komponente „Freihandsignatur“ befindet sich im Early-Adopter-Programm. Sie können von Ihrer offiziellen E-Mail-ID aus an `aem-forms-ea@adobe.com` schreiben, um dem Early-Adopter-Programm beizutreten und Zugriff auf die Funktion anzufordern.</span>

Eine Komponente des Typs „Freihandsignatur“ in einem adaptiven Formular ist ein Element der Benutzeroberfläche, mit dem Benutzende ihre **Signatur** direkt innerhalb des Formulars zeichnen können, indem sie eine Maus, einen Stift oder einen Touchscreen verwenden. Sie stellt sicher, dass handschriftliches Einverständnis sowie handschriftliche Genehmigungen oder Verifizierungen in digitalen Workflows korrekt erfasst werden.

**Beispiel**

![Beispiel](/help/adaptive-forms/assets/scribble-signature.png){width=50%,align-center}

**Verschiedene im Signaturfenster verfügbare Optionen**

- **A:** Klicken Sie auf das Symbol **Zeichnen**, um Ihre Signatur auf der Arbeitsfläche zu zeichnen.
- **B:** Klicken Sie auf das Symbol **Löschen**, um die Signatur auf der Arbeitsfläche zu löschen.
- **C:** Klicken Sie auf das Symbol **Geolocation**, um die Geolocation zusammen mit der Signatur hinzuzufügen.
- **D:** Klicken Sie auf das **Tastatursymbol**, um Ihren Namen auf der Arbeitsfläche einzugeben.

Nach Auswählen des Symbols **Speichern** im Fenster „Freihandsignatur“ können Sie die Signatur nicht mehr bearbeiten. Wenn Sie die Signatur bearbeiten möchten, müssen Sie die aktuelle Signatur ignorieren und mit der obigen Option „Pinsel“/„Tastatur“ erneut signieren.

>[!NOTE]
>
> Signaturen werden immer im PNG-Format gespeichert.

## Verwendung {#reasons-to-use-scribble-signature}

Es gibt verschiedene Gründe, warum es sinnvoll ist, ein Feld des Typs „Freihandsignatur“ in ein Formular einzufügen:

- **Digitales Einverständnis**: Ermöglicht es Benutzenden, rechtsgültige Signaturen elektronisch bereitzustellen.
- **Verbessertes Anwendererlebnis**: Bietet eine natürliche Möglichkeit, Signaturen direkt auf Geräten vorzunehmen, ohne etwas scannen oder hochladen zu müssen.
- **Papierlose Workflows**: Beseitigt die Notwendigkeit, Dokumente zu drucken, zu signieren und wieder einzuscannen.
- **Authentifizierung**: Dient als zusätzliche Ebene der Bestätigung und Genehmigung.
- **Datengenauigkeit**: Stellt die korrekte Erfassung der handschriftlichen Eingabe der unterzeichnenden Person in digitaler Form sicher.

## Version und Kompatibilität {#version-and-compatibility}

Die Kernkomponente „Freihandsignatur“ für adaptive Formulare wurde im **August 2025** als Teil der **Kernkomponenten 2.24.6** für Cloud Service und höher veröffentlicht.

| Komponentenversion | AEM as a Cloud Service | AEM 6.5.16.0 Forms oder höher |
|---|---|---|
| v1 | Kompatibel mit<br>[Version 2.24.6](/help/adaptive-forms/version.md) und höher | |

Weitere Informationen zu Versionen finden Sie unter [Kernkomponentenversionen](/help/adaptive-forms/version.md).

## Technische Details {#technical-details}

Erhalten Sie die neuesten technischen Details zur Kernkomponente „Freihandsignatur“ für adaptive Formulare auf [GitHub](https://github.com/adobe/aem-core-forms-components). Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Entwicklerdokumentation zu Kernkomponenten](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Das Dialogfeld „Konfigurieren“ ermöglicht die Anpassung der Komponente „Freihandsignatur“.

### Registerkarte „Allgemein“ {#basic-tab}

![Registerkarte „Allgemein“](/help/adaptive-forms/assets/scribble-signature-basictab.png)

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

- **Titel des Signaturdialogfelds**: Der Titel des Signaturdialogfelds definiert den Text, der oben im Dialogfeld zur Signaturerfassung angezeigt wird. Er dient als Eingabeaufforderung oder Anweisung für Benutzende, wenn sie eine Signatur bereitstellen müssen. Der Text führt Benutzende durch den Signaturvorgang und gestaltet die Interaktion klar und intuitiv.

### Registerkarte „Validierung“

![Registerkarte „Validierung“](/help/adaptive-forms/assets/scribble-signature-validation.png)

- **Erforderlich**: Wählen Sie diese Option, wenn Sie die Komponente in einem adaptiven Formular anzeigen möchten. Nachdem Sie die Option ausgewählt haben, müssen Sie eine Auswahl treffen, bevor Sie mit der Formularübermittlung fortfahren. Wenn diese Option aktiviert ist, kann die Option **Komponente ausblenden** oder **Komponente deaktivieren** auf der Registerkarte **Allgemein** nicht ausgewählt werden.

- **Fehlermeldung**: Mit dieser Option können Sie eine Nachricht eingeben, die angezeigt wird, wenn das Kontrollkästchen **Erforderlich** aktiviert ist und das Feld leer bleibt.

- **Meldung zur Skriptvalidierung**: Mit dieser Option können Sie eine Meldung eingeben, die angezeigt werden soll, wenn die Skriptvalidierung fehlschlägt.

### Registerkarte „Hilfe-Inhalt“ {#help-content-tab}

![Registerkarte „Hilfe-Inhalt“](/help/adaptive-forms/assets/scribble-signature-helptab.png)

- **Kurzbeschreibung**: Eine Kurzbeschreibung ist eine kurze Erklärung, die zusätzliche Informationen oder Klarstellungen über den Zweck eines Formularfelds bietet. Es hilft Benutzenden zu verstehen, welcher Datentyp in das Feld eingegeben werden soll, und kann Richtlinien oder Beispiele bereitstellen, um sicherzustellen, dass die eingegebenen Informationen gültig sind und die gewünschten Kriterien erfüllen. Standardmäßig bleiben kurze Beschreibungen ausgeblendet. Aktivieren Sie die Option **Kurzbeschreibung immer anzeigen**, um sie unterhalb der Komponente anzuzeigen.

- **Kurzbeschreibung immer anzeigen** – Aktivieren Sie die Option, um die Kurzbeschreibung unterhalb der Komponente anzuzeigen.

- **Hilfetext**: Hilfetext bezieht sich auf zusätzliche Informationen oder Anleitungen, die den Benutzenden bereitgestellt werden, um sie beim korrekten Ausfüllen eines Formularfelds zu unterstützen. Er erscheint, wenn Benutzende auf das Hilfesymbol (i) neben der Komponente klicken. Hilfetext enthält detailliertere Informationen als die Beschriftung oder der Platzhaltertext eines Formularfelds und soll den Benutzenden dabei helfen, die Anforderungen oder Einschränkungen des Felds zu verstehen. Er kann auch Vorschläge oder Beispiele anbieten, um das Ausfüllen des Formulars einfacher und genauer zu gestalten.

### Registerkarte „Barrierefreiheit“ {#accessibility-tab}

![Registerkarte „Barrierefreiheit“](/help/adaptive-forms/assets/scribble-signature-accessibilitytab.png)

- **Text für Bildschirmlesehilfen** – Das ist zusätzlicher Text, der von Hilfstechnologien wie etwa Bildschirmlesehilfen für sehbehinderte Personen vorgelesen wird. Dieser Text enthält eine Audiobeschreibung des Zwecks des Formularfelds und kann Informationen über den Titel, die Beschreibung, den Namen und alle relevanten Nachrichten (benutzerdefinierten Text) des Felds enthalten. Der Text der Bildschirmlesehilfe hilft sicherzustellen, dass das Formular allen Benutzenden zugänglich ist, auch Personen mit Sehschwäche, und bietet ihnen ein umfassendes Verständnis des Formularfelds und seiner Anforderungen.
   - **Benutzerdefinierter Text**: Wählen Sie diese Option aus, um den benutzerdefinierten Text für ARIA-Barrierefreiheitsbeschriftungen zu verwenden. Wenn Sie diese Option auswählen, wird das Benutzerdefinierter Dialogfeld „Text“ angezeigt. Sie können relevante Informationen im Benutzerdefinierter Dialogfeld „Text“ hinzufügen.
   - **Beschreibung**: Wählen Sie diese Option aus, um die Beschreibung für ARIA-Barrierefreiheitsbeschriftungen zu verwenden.
   - **Titel**: Wählen Sie diese Option aus, um den Titel für ARIA-Barrierefreiheitsbeschriftungen zu verwenden.
   - **Name**: Wählen Sie diese Option aus, um den Namen für ARIA-Barrierefreiheitsbeschriftungen zu verwenden.
   - **Keine**: Wählen Sie diese Option aus, wenn Sie keine ARIA-Barrierefreiheitsbezeichnungen hinzufügen möchten.

## Dialogfeld „Design“ {#design-dialog}

Im Dialogfeld „Design“ können Sie CSS-Stile für die Komponente „Freihandsignatur“ definieren und verwalten.

### Registerkarte „Stile“ {#styles-tab}

Sie können die Registerkarte zum Definieren und Verwalten von CSS-Stilen für eine Komponente verwenden. Die Kernkomponente „Freihandsignatur“ für adaptive Formulare unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).

![Dialogfeld „Design“](/help/adaptive-forms/assets/checkbox-style.png)

- **Standard-CSS-Klassen**: Sie können eine Standard-CSS-Klasse für die Kernkomponente „Freihandsignatur“ für adaptive Formulare angeben.

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
