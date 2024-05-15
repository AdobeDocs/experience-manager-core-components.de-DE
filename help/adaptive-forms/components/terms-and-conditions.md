---
title: Kernkomponente für adaptive Formulare - Nutzungsbedingungen
description: Verwenden oder Anpassen der Nutzungsbedingungs-Kernkomponente für adaptive Formulare.
role: Architect, Developer, Admin, User
exl-id: c607d554-ad2d-4434-856d-91e174ef3149
source-git-commit: 58a0f0f2ef6d9dec3ce2436dad954a8a7aca188c
workflow-type: tm+mt
source-wordcount: '3115'
ht-degree: 99%

---

# Komponente &quot;Allgemeine Geschäftsbedingungen&quot;

<span class="preview"> Dieser Artikel enthält Inhalte zum   **Rich-Text für Titel zulassen**   und   **Rich-Text für Optionen zulassen**   Funktionen, Funktionen vor der Veröffentlichung. Die Vorabveröffentlichungsfunktion ist nur über unseren [Vorabveröffentlichungskanal](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/release-notes/prerelease.html?lang=de#new-features) zugänglich.</span>

Eine **Nutzungsbedingungskomponente** bezieht sich auf einen Abschnitt eines Formulars, in dem die Bedingungen, Regeln und Vorgaben erläutert werden, denen Benutzende bei der Verwendung eines Dienstes oder beim Zugriff auf Inhalte zustimmen oder die sie erfüllen müssen.

Die **Nutzungsbedingungskomponente** ist eine Composite-Komponente aus Text, Kontrollkästchen und Links. Die Textkomponente enthält einen Titel sowie einen kurzen Überblick über Zweck und Umfang der Nutzungsbedingungen. Ferner enthält sie ein Kontrollkästchen, mit dem Benutzende explizit ihre Zustimmung erteilen können. Sie können auch einen Zustimmungstext durch Links ersetzen.

>[!NOTE]
>
> Für AEM 6.5 Forms wurde diese Komponente mit AEM 6.5 Forms Service Pack 19 (6.5.19.0) eingeführt. Um diese Komponente zu aktivieren, stellen Sie sicher, dass die erforderlichen Versionen der Forms-Kernkomponenten und der WCM-Kernkomponenten installiert sind. Ausführliche Informationen zu den Versionen der Kernkomponenten für adaptive Formulare finden Sie unter [Kernkomponentenversionen für adaptive Formulare](/help/adaptive-forms/version.md)

**Beispiel**

![Nutzungsbedingungen](/help/adaptive-forms/assets/terms-and-conditions.png)

Unter [Unterkomponenten der Nutzungsbedingungskomponente](#sub-component) finden Sie weitere Informationen zu den verschiedenen Komponenten der Nutzungsbedingungskomponente.

## Verwendung {#reasons-to-use-termsandconditions}

- **Nutzungsvereinbarung**: Die Komponente dient als Vereinbarung zwischen dem Dienstleister und Benutzenden. Benutzende müssen die Bedingungen bestätigen und akzeptieren, bevor sie auf den Dienst oder Inhalt zugreifen können.

- **Einhaltung gesetzlicher Vorschriften**: Gewährleistet die Einhaltung rechtlicher Vorschriften und den Schutz des Dienstleisters, indem die Rechte, Pflichten und Verbindlichkeiten beider Parteien klar festgelegt werden.

- **Registrierungsverfahren**: Registrierungs- und Anmeldeformulare mit der **Nutzungsbedingungskomponente**, deren Bedingungen Benutzende vor der Erstellung eines Kontos oder der Nutzung eines Dienstes explizit zustimmen müssen.

- **E-Commerce-Transaktionen**: Online-Websites mit der **Nutzungsbedingungskomponente**, auf der Benutzende aufgefordert werden, den Bedingungen als Teil des Checkout-Prozesses zuzustimmen, bevor ein Online-Kauf erfolgt.

- **Sicherheits- und Datenschutzabkommen**: Die **Nutzungsbedingungskomponente** informiert darüber, wie Benutzerdaten erfasst, gespeichert und verwendet werden, häufig ergänzt durch eine separate Datenschutzrichtlinie.

## Version und Kompatibilität {#version-and-compatibility}

Die Kernkomponente „Akkordeon“ für adaptive Formulare wurde im Februar 2023 als Teil der Kernkomponenten 2.0.62 für Cloud Service und der Kernkomponenten 1.1.28 für AEM 6.5.16.0 Forms oder höher veröffentlicht. Hier finden Sie eine Tabelle mit allen unterstützten Versionen, AEM-Kompatibilität und Links zur entsprechenden Dokumentation:

| Komponentenversion | AEM as a Cloud Service | AEM 6.5.16.0 Forms oder höher |
|---|---|---|
| v1 | Kompatibel mit<br>[Version 2.0.62](/help/adaptive-forms/version.md) und höher | Kompatibel mit<br>[Version 1.1.28](/help/adaptive-forms/version.md) und höher (aber nur bis Version 2.0.0). |

Informationen zu Versionen und Freigaben der Kernkomponente finden Sie im Dokument [Kernkomponenten-Versionen](/help/adaptive-forms/version.md).

## Technische Details {#technical-details}

Die neuesten Informationen zur Kernkomponente „Allgemeine Geschäftsbedingungen“ für adaptive Formulare finden Sie in der technischen Dokumentation auf [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/checkboxgroup/v1/checkboxgroup). Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Entwicklerdokumentation für Kernkomponenten](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Sie können das Erlebnis Ihrer Besuchenden mit der Nutzungsbedingungskomponte über das Dialogfeld „Konfigurieren“ bequem anpassen. Für ein nahtloses Benutzererlebnis können Sie auch bequem Nutzungsbedingungsoptionen festlegen.

### Registerkarte „Allgemein“

![Registerkarte „Allgemein“](/help/adaptive-forms/assets/terms-and-conditions-basic-tab.png)

- **Name**: Durch den Namen wird die Komponente im Regel-Editor eindeutig identifiziert. Sonderzeichen und Leerzeichen sind im Namen nicht zulässig.

- **Titel**: Sie können mit dem Titel leicht eine Komponente in einem Formular identifizieren. Standardmäßig wird der Titel über der Komponente angezeigt. Wenn Sie keinen Titel hinzufügen, wird der Name der Komponente anstelle des Titeltexts angezeigt.
- **Rich-Text für Titel zulassen**: Diese Funktionen ermöglichen es Benutzenden, einfache Texttitel zu formatieren, die Funktionen wie fett, kursiv, unterstrichener Text, verschiedene Schriftarten, Schriftgrößen, Farben und zusätzliche Optionen enthalten und so die visuelle Darstellung und Anpassung zu verbessern. Sie bietet mehr Flexibilität und kreative Kontrolle bei der Hervorhebung von Titeln in Dokumenten, Websites oder Anwendungen.\
  Durch Aktivieren des Kontrollkästchens **Rich-Text für Titel zulassen** werden Formatierungsoptionen sichtbar, mit denen Sie den Titel der Komponente gestalten können. Um auf alle verfügbaren Formatierungsoptionen zuzugreifen, können Sie auf die Registerkarte ![Vollbildsymbol](/help/adaptive-forms/assets/fullscreen-icon.png) klicken.

  ![Rich-Text-Unterstützung](/help/adaptive-forms/assets/richtext-support-title.png)

- **Bestätigungsoptionen anzeigen** - Wählen Sie die Option aus, um das Zustimmungs-Kontrollkästchen anzuzeigen, mit dem der Benutzer explizit seine Zustimmung geben kann.

- **Als Popup anzeigen** - Wählen Sie die Option aus, um die Nutzungsbedingungskomponente in einem Popup-Fenster anzuzeigen.

- **Einverständnistext durch Weblink(s) ersetzen** - Wählen Sie die Option, um einen Einverständnistext durch einen Weblink zu ersetzen. Wenn die Option deaktiviert ist, wird standardmäßig der Einverständnistext angezeigt.

- **Titel ausblenden** - Wählen Sie die Option aus, um den Titel der Komponente auszublenden.

- **Daten untergeordneter Komponenten bei Formularübermittlung gruppieren (Daten in Objekt einschließen)** – Wenn die Option ausgewählt ist, werden die Daten aus den untergeordneten Komponenten innerhalb des JSON-Objekts der übergeordneten Komponente verschachtelt. Wenn jedoch die Option nicht ausgewählt ist, weisen die gesendeten JSON-Daten eine flache Struktur auf, ohne dass ein Objekt für die übergeordnete Komponente vorhanden ist. Zum Beispiel:

   - Wenn die Option ausgewählt ist, werden die Daten aus den untergeordneten Komponenten (z. B. Straße, Stadt und Postleitzahl) innerhalb der übergeordneten Komponente (Adresse) als JSON-Objekt verschachtelt. Dadurch wird eine hierarchische Struktur erstellt, und die Daten werden unter der übergeordneten Komponente angeordnet.

     Struktur der übermittelten Daten:

     ```JSON
     { "Address":
     
     { "Street": "123 Main Street", "City": "New York", "Zip Code": "12345" }
     
     }
     ```

   - Wenn die Option nicht ausgewählt ist, weisen die gesendeten JSON-Daten eine flache Struktur auf, ohne dass ein Objekt für die übergeordnete Komponente (Adresse) vorhanden ist. Alle Daten befinden sich auf derselben Ebene ohne hierarchische Organisation.

     Struktur der übermittelten Daten:

     ```JSON
        { "Street": "123 Main Street", "City": "New York", "Zip Code": "12345" }
     ```

- **Verbindungsreferenz**: Eine Verbindungsreferenz ist ein Verweis auf ein Datenelement, das in einer externen Datenquelle gespeichert ist und in einem Formular verwendet wird. Sie können mit dem Bindungsverweis Daten dynamisch an Formularfelder binden, sodass das Formular die aktuellsten Daten aus der Datenquelle anzeigen kann. Beispielsweise kann ein Bindungsverweis verwendet werden, um den Namen und die Adresse von Kundinnen und Kunden in einem Formular anzuzeigen, basierend auf der im Formular eingegebenen Kunden-ID. Der Bindungsverweis kann auch verwendet werden, um die Datenquelle mit den im Formular eingegebenen Daten zu aktualisieren. Auf diese Weise können Sie mit AEM Forms Formulare erstellen, die mit externen Datenquellen interagieren und so eine nahtlose Benutzererfahrung bei der Datenerfassung und Datenverwaltung bieten.

- **Komponente ausblenden**: Wählen Sie die Option, um die Komponente aus dem Formular auszublenden. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor. Dies ist nützlich, wenn Sie Informationen speichern müssen, die Benutzende nicht sehen oder direkt ändern müssen.
- **Komponente deaktivieren**: Wählen Sie die Option zum Deaktivieren der Komponente aus. Die deaktivierte Komponente ist nicht aktiv und Endbenutzende können sie nicht bearbeiten. Benutzende können den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor.
- **Schreibgeschützt**: Wählen Sie die Option aus, um die Komponente nicht bearbeitbar zu machen. Benutzende können den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor.

### Registerkarte „Hilfe-Inhalt“ {#help-content-tab}

![Registerkarte „Hilfe-Inhalt“](/help/adaptive-forms/assets/terms-and-conditions-help-tab.png)

- **Kurzbeschreibung**: Eine Kurzbeschreibung ist eine kurze Erklärung, die zusätzliche Informationen oder Klarstellungen über den Zweck eines Formularfelds bietet. Es hilft Benutzenden zu verstehen, welcher Datentyp in das Feld eingegeben werden soll, und kann Richtlinien oder Beispiele bereitstellen, um sicherzustellen, dass die eingegebenen Informationen gültig sind und die gewünschten Kriterien erfüllen. Standardmäßig bleiben kurze Beschreibungen ausgeblendet. Aktivieren Sie die Option **Kurzbeschreibung immer anzeigen**, um sie unterhalb der Komponente anzuzeigen.

- **Kurzbeschreibung immer anzeigen**: Aktivieren Sie diese Option, um die Kurzbeschreibung unterhalb der Komponente anzuzeigen.

- **Hilfetext**: Hilfetext bezieht sich auf zusätzliche Informationen oder Anleitungen, die den Benutzenden bereitgestellt werden, um sie beim korrekten Ausfüllen eines Formularfelds zu unterstützen. Er erscheint, wenn Benutzende auf das Hilfesymbol (i) neben der Komponente klicken. Hilfetext enthält detailliertere Informationen als die Beschriftung oder der Platzhaltertext eines Formularfelds und soll den Benutzenden dabei helfen, die Anforderungen oder Einschränkungen des Felds zu verstehen. Er kann auch Vorschläge oder Beispiele anbieten, um das Ausfüllen des Formulars einfacher und genauer zu gestalten.

### Registerkarte „Barrierefreiheit“

![Registerkarte „Barrierefreiheit“](/help/adaptive-forms/assets/terms-and-conditions-accessibility-tab.png)

- **Text für Bildschirmlesehilfen** – Das ist zusätzlicher Text, der von Hilfstechnologien wie etwa Bildschirmlesehilfen für sehbehinderte Personen vorgelesen wird. Dieser Text enthält eine Audiobeschreibung des Zwecks des Formularfelds und kann Informationen über den Titel, die Beschreibung, den Namen und alle relevanten Nachrichten (benutzerdefinierten Text) des Felds enthalten. Der Text der Bildschirmlesehilfe hilft sicherzustellen, dass das Formular allen Benutzenden zugänglich ist, auch Personen mit Sehschwäche, und bietet ihnen ein umfassendes Verständnis des Formularfelds und seiner Anforderungen.
- **HTML-Rolle für die Ankündigung durch die Bildschirmlesehilfe** – Die HTML-Rolle ist ein Attribut, mit dem der Zweck eines HTML-Elements für Hilfstechnologien wie Bildschirmlesehilfen spezifiziert wird. Rollenattribute werden verwendet, um für ein Element zusätzlichen Kontext und eine semantische Bedeutung bereitzustellen, wodurch es für Bildschirmlesehilfen einfacher wird, den Inhalt zu interpretieren und ihn Benutzenden mitzuteilen. In AEM Forms kann beispielsweise die Beschriftung eines Formularfelds die Rolle „Beschriftung“ haben und sein Eingabefeld die Rolle „Textfeld“. Dadurch kann die Bildschirmlesehilfe die Beziehung zwischen Beschrfitung und Eingabefeld verstehen und diese Informationen den Benutzenden korrekt mitteilen.

## Dialogfeld „Design“ {#design-dialog}

Im Dialogfeld „Design“ können Sie CSS-Stile für die Nutzungsbedingungskomponente definieren und verwalten.


### Registerkarte „Stile“ {#styles-tab}

Sie können die Registerkarte zum Definieren und Verwalten von CSS-Stilen für eine Komponente verwenden. Die Nutzungsbedingungs-Kernkomponente für adaptive Formulare unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).

![Dialogfeld „Design“](/help/adaptive-forms/assets/checkbox-style.png)

- **Standard-CSS-Klassen**: Sie können eine standardmäßige CSS-Klasse für die Kernkomponente „Allgemeine Geschäftsbedingungen“ für adaptive Formulare bereitstellen.

- **Zulässige Stile**: Sie können Stile definieren, indem Sie den Namen und die CSS-Klasse für den Stil angeben. Sie können beispielsweise einen Stil mit dem Namen „Fettschrift“ erstellen und die CSS-Klasse „Schriftbreite: Fett“ bereitstellen. Sie können diese Stile bei einem adaptiven Formular im adaptiven Formular-Editor anwenden. Um einen Stil anzuwenden, wählen Sie im Editor für adaptive Formulare die Komponente aus, auf die Sie den Stil anwenden möchten, navigieren Sie zum Eigenschaften-Dialog und wählen Sie den gewünschten Stil aus der Dropdown-Liste **Stile**. Wenn Sie die Stile aktualisieren oder ändern müssen, kehren Sie einfach zum Dialogfeld „Design“ zurück, aktualisieren die Stile auf der Registerkarte „Stile“ und speichern die Änderungen.

### Benutzerdefinierte Eigenschaften

![Dialogfeld „Benutzerdefinierte Eigenschaften“](/help/adaptive-forms/assets/checkbox-customproperties.png)

Mit der Option „Benutzerdefinierte Eigenschaften“ können Sie mithilfe der Formularvorlage benutzerdefinierte Attribute (Schlüsselwertpaare) mit einer Kernkomponente eines adaptiven Formulars verknüpfen. Die benutzerdefinierten Eigenschaften werden im Eigenschaftenbereich der Headless-Ausgabedarstellung der Komponente angezeigt. So kann ein dynamisches Formularverhalten erzeugt werden, das sich je nach den benutzerdefinierten Attributwerten anpasst. Beispielsweise können Entwickelnde verschiedene Ausgabedarstellungen einer Headless-Formularkomponente für Mobile-, Desktop- oder Web-Plattformen entwerfen und so das Benutzererlebnis auf einer Vielzahl von Geräten erheblich verbessern.

- **Gruppenname**: Sie können einen Namen angeben, um die Gruppe der benutzerdefinierten Eigenschaften zu kennzeichnen. Sie können mehrere Gruppen benutzerdefinierter Eigenschaften hinzufügen, löschen oder neu anordnen. Nach dem Hinzufügen der Gruppe benutzerdefinierter Eigenschaften werden folgende Optionen angezeigt:

   - **Schlüssel-Wert-Paare**: Sie können mehrere Namen und Werte benutzerdefinierter Eigenschaften hinzufügen, indem Sie für jede Gruppe benutzerdefinierter Eigenschaften auf **Hinzufügen** klicken.

   - **Löschen**: Tippen oder klicken Sie auf diese Option, um den Namen und den Wert der benutzerdefinierten Eigenschaft zu löschen.

   - **Neu anordnen**: Ordnen Sie den Namen und Wert der benutzerdefinierten Eigenschaft Antippen oder Klicken und Ziehen neu an.

## Unterkomponenten der Nutzungsbedingungskomponente {#sub-component}

Eine **Nutzungsbedingungskomponente** ist eine aus folgenden Unterkomponenten zusammengesetzte Komponente:
- [Link-Komponente](#link)
- [Textkomponente](#text)
- [Kontrollkästchen-Komponente](#checkbox)

### Link-Komponente{#link}

Diese Komponente ersetzt einen Zustimmungstext durch einen Weblink oder Links. Es wird in einem Szenario verwendet, in dem Benutzende Verweise auf bestimmte Abschnitte, zusätzliche Informationen oder externe Dokumente anbieten möchten. Über das Dialogfeld „Konfigurieren“ können Sie die **Link-Komponente** für Besuchende bequem anpassen.

#### Registerkarte „Allgemein“

![Registerkarte „Allgemein“](/help/adaptive-forms/assets/link-basic-tab.png)

- **Name**: Durch den Namen wird die Komponente im Regel-Editor eindeutig identifiziert. Sonderzeichen und Leerzeichen sind im Namen nicht zulässig.

- **Titel**: Sie können mit dem Titel leicht eine Komponente in einem Formular identifizieren. Standardmäßig wird der Titel über der Komponente angezeigt. Wenn Sie keinen Titel hinzufügen, wird der Name der Komponente anstelle des Titeltexts angezeigt.
- **Rich-Text für Titel zulassen**: Mit dieser Funktion können Sie Titel mit Optionen wie fett, kursiv, Schriftarten, Farben und Ausrichtung formatieren und so die visuelle Darstellung und Anpassung verbessern. Sie bietet mehr Flexibilität und kreative Kontrolle bei der Hervorhebung von Titeln in Dokumenten, Websites oder Anwendungen.\
  Durch Aktivieren des Kontrollkästchens **Rich-Text für Titel zulassen** werden Formatierungsoptionen sichtbar, mit denen Sie den Titel der Komponente gestalten können. Um auf alle verfügbaren Formatierungsoptionen zuzugreifen, können Sie auf die Registerkarte ![Vollbildsymbol](/help/adaptive-forms/assets/fullscreen-icon.png) klicken.

  ![Rich-Text-Unterstützung](/help/adaptive-forms/assets/richtext-support-title.png)

- **Titel ausblenden**: Wählen Sie die Option aus, um den Titel der Komponente auszublenden.

- **Links** - Geben Sie den Link und den entsprechenden Anzeigetext an, der anstelle des Zustimmungstextes verwendet werden soll. Sie können mehrere Links hinzufügen, indem Sie auf die Schaltfläche **Hinzufügen** klicken.
Nachdem eine neue Option hinzugefügt wurde, können die folgenden Aktionen ausgeführt werden:
   - **Link**: Mit dieser Option können Sie die URL für die Umleitung eingeben, wenn eine Option ausgewählt wird.
   - **Text anzeigen** – Mit dieser Option können Sie den Inhalt eingeben, der in einem adaptiven Formular angezeigt werden soll.
   - **Löschen** – Durch Tippen oder Klicken können Sie die Option einer Optionsschaltfläche löschen.
   - **Neu anordnen** – Durch Tippen oder Klicken und Ziehen können Sie die Anordnung der Optionen anpassen.

  Sie können die Optionen für die Kontrollkästchengruppe auch mit **Rich-Text für Optionen zulassen** formatieren. Sobald Sie das Kontrollkästchen **Rich-Text für Optionen zulassen** aktivieren, werden Formatierungsoptionen sichtbar, um die Optionen der Komponente zu gestalten. Um auf alle verfügbaren Formatierungsoptionen zuzugreifen, können Sie auf die Registerkarte `Fullscreen` ![Vollbildschirmsymbol](/help/adaptive-forms/assets/fullscreen-icon.png) klicken.

  ![Rich-Text-Unterstützung für Optionen](/help/adaptive-forms/assets/link-options.png)

- **Verbindungsreferenz**: Eine Verbindungsreferenz ist ein Verweis auf ein Datenelement, das in einer externen Datenquelle gespeichert ist und in einem Formular verwendet wird. Sie können mit dem Bindungsverweis Daten dynamisch an Formularfelder binden, sodass das Formular die aktuellsten Daten aus der Datenquelle anzeigen kann. Beispielsweise kann ein Bindungsverweis verwendet werden, um den Namen und die Adresse von Kundinnen und Kunden in einem Formular anzuzeigen, basierend auf der im Formular eingegebenen Kunden-ID. Der Bindungsverweis kann auch verwendet werden, um die Datenquelle mit den im Formular eingegebenen Daten zu aktualisieren. Auf diese Weise können Sie mit AEM Forms Formulare erstellen, die mit externen Datenquellen interagieren und so ein nahtloses Benutzererlebnis bei der Datenerfassung und -verwaltung bieten.

- **Als ungebundenes Formularelement markieren**: Mit dieser Option können Sie Formularfelder konfigurieren, die mit keinem Schema verbunden sind. Mit dieser Option können Sie Daten speichern, ohne die Datenquelle zu aktualisieren. Außerdem können Sie damit Daten auf eine benutzerdefinierte Art und Weise verarbeiten, getrennt von der standardmäßigen Datenbankintegration.
- **Komponente ausblenden**: Wählen Sie diese Option, um die Komponente aus dem Formular auszublenden. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor. Dies ist nützlich, wenn Sie Informationen speichern müssen, die Benutzende nicht sehen oder direkt ändern müssen.

- **Komponente deaktivieren**: Mit dieser Option können Sie die Komponente deaktivieren oder sperren. Die deaktivierte Komponente ist nicht aktiv und Endbenutzende können sie nicht bearbeiten. Benutzende können den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor.
- **Schreibgeschützt**: Wählen Sie die Option aus, um die Komponente nicht bearbeitbar zu machen. Benutzende können den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor.

#### Registerkarte „Validierung“

![Registerkarte „Validierung“](/help/adaptive-forms/assets/link-validation-tab.png)

- **Erforderlich**: Wählen Sie diese Option, wenn Sie die Komponente in einem adaptiven Formular anzeigen möchten. Nachdem Sie die Option ausgewählt haben, müssen Sie eine Auswahl treffen, bevor Sie mit der Formularübermittlung fortfahren. Wenn diese Option aktiviert ist, kann die Option **Komponente ausblenden** oder **Komponente deaktivieren** auf der Registerkarte **Allgemein** nicht ausgewählt werden.

- **Fehlermeldung**: Mit dieser Option können Sie eine Nachricht eingeben, die angezeigt wird, wenn das Kontrollkästchen **Erforderlich** aktiviert ist und das Feld leer bleibt.

- **Meldung zur Skriptvalidierung**: Mit dieser Option können Sie eine Meldung eingeben, die angezeigt werden soll, wenn die Skriptvalidierung fehlschlägt.

### Registerkarte „Hilfe-Inhalt“ {#helpcontent-tab}

![Registerkarte „Hilfe-Inhalt“](/help/adaptive-forms/assets/link-help-tab.png)

- **Kurzbeschreibung**: Eine Kurzbeschreibung ist eine kurze Erklärung, die zusätzliche Informationen oder Klarstellungen über den Zweck eines Formularfelds bietet. Es hilft Benutzenden zu verstehen, welcher Datentyp in das Feld eingegeben werden soll, und kann Richtlinien oder Beispiele bereitstellen, um sicherzustellen, dass die eingegebenen Informationen gültig sind und die gewünschten Kriterien erfüllen. Standardmäßig bleiben kurze Beschreibungen ausgeblendet. Aktivieren Sie die Option **Kurzbeschreibung immer anzeigen**, um sie unterhalb der Komponente anzuzeigen.

- **Kurzbeschreibung immer anzeigen**: Aktivieren Sie diese Option, um die Kurzbeschreibung unterhalb der Komponente anzuzeigen.

- **Hilfetext**: Hilfetext bezieht sich auf zusätzliche Informationen oder Anleitungen, die den Benutzenden bereitgestellt werden, um sie beim korrekten Ausfüllen eines Formularfelds zu unterstützen. Er erscheint, wenn Benutzende auf das Hilfesymbol (i) neben der Komponente klicken. Hilfetext enthält detailliertere Informationen als die Beschriftung oder der Platzhaltertext eines Formularfelds und soll den Benutzenden dabei helfen, die Anforderungen oder Einschränkungen des Felds zu verstehen. Er kann auch Vorschläge oder Beispiele anbieten, um das Ausfüllen des Formulars einfacher und genauer zu gestalten.

### Registerkarte „Barrierefreiheit“

![Registerkarte „Barrierefreiheit“](/help/adaptive-forms/assets/link-accessibilty-tab.png)

**Text für Bildschirmlesehilfen** – Das ist zusätzlicher Text, der von Hilfstechnologien wie etwa Bildschirmlesehilfen für sehbehinderte Personen vorgelesen wird. Dieser Text enthält eine Audiobeschreibung des Zwecks des Formularfelds und kann Informationen über den Titel, die Beschreibung, den Namen und alle relevanten Nachrichten (benutzerdefinierten Text) des Felds enthalten. Der Text der Bildschirmlesehilfe hilft sicherzustellen, dass das Formular allen Benutzenden zugänglich ist, auch Personen mit Sehschwäche, und bietet ihnen ein umfassendes Verständnis des Formularfelds und seiner Anforderungen.

### Textkomponente {#text}

Die **Textkomponente** zeigt den Textinhalt an, der Benutzenden Informationen bereitstellt. Diese Komponente enthält die tatsächlichen Nutzungsbedingungen, die Rechtssprache oder andere relevante Textinformationen.

Über das Dialogfeld „Konfigurieren“ können Sie die [Textkomponente](/help/adaptive-forms/components/text.md) individuell für Besuchende anpassen. Nutzen Sie das Dialogfeld [„Konfigurieren“ der Textkomponente](/help/adaptive-forms/components/text.md#configure-dialog), um schnell und einfach Textoptionen für ein nahtloses Benutzererlebnis zu definieren.


### Kontrollkästchen-Komponente {#checkbox}

Benutzende geben ihre Zustimmung oder Bestätigung über ein Kontrollkästchen. Es dient als visueller Indikator dafür, dass Benutzende die genannten Bedingungen gelesen und akzeptiert haben. Um ihre Zustimmung anzuzeigen, müssen Benutzende das Kontrollkästchen aktivieren.

Über das Dialogfeld „Konfigurieren“ können Sie die [Kontrollkästchen-Komponente](/help/adaptive-forms/components/checkbox.md) individuell für Besuchende anpassen. Nutzen Sie das Dialogfeld [„Konfigurieren“ der Kontrollkästchen-Komponente](/help/adaptive-forms/components/checkbox.md#configure-dialog), um die Eigenschaften des Kontrollkästchens für ein nahtloses Benutzererlebnis zu definieren.


## Ähnliche Artikel {#related-articles}

{{more-like-this}}

## Siehe auch {#see-also}

{{see-also}}
