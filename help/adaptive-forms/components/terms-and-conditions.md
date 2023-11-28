---
title: Adaptive Forms-Kernkomponente - Geschäftsbedingungen
description: Verwenden oder Anpassen der Kernkomponente "Adaptive Forms-Geschäftsbedingungen".
role: Architect, Developer, Admin, User
exl-id: c607d554-ad2d-4434-856d-91e174ef3149
source-git-commit: f0b450ef93a32a56000c31d82bf92394c57b55f9
workflow-type: tm+mt
source-wordcount: '2639'
ht-degree: 66%

---

# Komponente &quot;Allgemeine Geschäftsbedingungen&quot;

A **Geschäftsbedingungen** -Komponente bezieht sich auf einen Abschnitt in einem Formular, in dem die Bedingungen, Regeln und Bedingungen erläutert werden, denen Benutzer bei der Verwendung eines Dienstes oder beim Zugriff auf Inhalte zustimmen oder diese erfüllen müssen.

Die **Geschäftsbedingungen** -Komponente ist eine Composite-Komponente, die aus Text-, Kontrollkästchen- und Link-Komponenten besteht. Die Textkomponente enthält einen Titel sowie einen kurzen Überblick über Zweck und Umfang der Nutzungsbedingungen. Es enthält auch ein Kontrollkästchen, mit dem der Benutzer explizit seine Zustimmung erteilen kann. Sie können auch einen Zustimmungstext durch Links ersetzen.

**Beispiel**

![Bedingungen](/help/adaptive-forms/assets/terms-and-conditions.png)

Siehe [Unterkomponenten der Komponente &quot;Geschäftsbedingungen&quot;](#sub-component) , um mehr über die verschiedenen Komponenten der Komponente &quot;Allgemeine Geschäftsbedingungen&quot;zu erfahren.

## Verwendung {#reasons-to-use-termsandconditions}

- **Benutzervereinbarung**: Die Komponente dient als Vereinbarung zwischen dem Dienstleister und dem Benutzer. Benutzer müssen die Bedingungen bestätigen und akzeptieren, bevor sie auf den Dienst oder Inhalt zugreifen.

- **Rechtliche Einhaltung**: Es gewährleistet die rechtliche Einhaltung und den Schutz des Dienstleisters, indem die Rechte, Verantwortlichkeiten und Verbindlichkeiten beider Parteien dargelegt werden.

- **Registrierungsverfahren**: Die Registrierungs- oder Registrierungsformulare enthalten die **Geschäftsbedingungen** -Komponente, die die ausdrückliche Zustimmung der Benutzer zu den Bedingungen verlangt, bevor sie ein Konto erstellen oder einen Dienst verwenden.

- **E-Commerce-Transaktionen**: Online-Websites beinhalten die **Geschäftsbedingungen** -Komponente, damit Benutzer im Rahmen des Checkout-Prozesses aufgefordert werden, den Geschäftsbedingungen zuzustimmen, bevor sie online Käufe tätigen.

- **Sicherheits- und Datenschutzabkommen**: Die **Geschäftsbedingungen** -Komponente enthält Details dazu, wie die Benutzerdaten erfasst, gespeichert und verwendet werden, häufig ergänzt durch eine separate Datenschutzrichtlinie

## Version und Kompatibilität {#version-and-compatibility}

Die Kernkomponente „Akkordeon“ für adaptive Formulare wurde im Februar 2023 als Teil der Kernkomponenten 2.0.4 für Cloud Service und der Kernkomponenten 1.1.12 für AEM 6.5.16.0 Forms oder höher veröffentlicht. Hier finden Sie eine Tabelle mit allen unterstützten Versionen, AEM-Kompatibilität und Links zur entsprechenden Dokumentation:

| Komponentenversion | AEM as a Cloud Service | AEM 6.5.16.0 Forms oder höher |
|---|---|---|
| v1 | Kompatibel mit<br>[Version 2.0.4](/help/adaptive-forms/version.md) und höher | Kompatibel mit<br>[Version 1.1.12](/help/adaptive-forms/version.md) und höher (aber nur bis Version 2.0.0). |

Informationen zu Versionen und Freigaben der Kernkomponente finden Sie im Dokument [Kernkomponenten-Versionen](/help/adaptive-forms/version.md).

## Technische Details {#technical-details}

Aktuelle Informationen zur Kernkomponente für adaptive Formulare – Kontrollkästchen-Gruppe finden Sie in der technischen Dokumentation auf [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/checkboxgroup/v1/checkboxgroup). Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Entwicklerdokumentation für Kernkomponenten](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Im Dialogfeld &quot;Konfigurieren&quot;können Sie das Komponentenerlebnis für Bedingungen für Besucher einfach anpassen. Für ein nahtloses Benutzererlebnis können Sie auch problemlos Nutzungsbedingungen und -optionen definieren.

### Registerkarte „Allgemein“

![Registerkarte „Allgemein“](/help/adaptive-forms/assets/terms-and-conditions-basic-tab.png)

- **Name**: Durch den Namen wird die Komponente im Regel-Editor eindeutig identifiziert. Sonderzeichen und Leerzeichen sind im Namen nicht zulässig.

- **Titel**: Sie können mit dem Titel leicht eine Komponente in einem Formular identifizieren. Standardmäßig wird der Titel über der Komponente angezeigt. Wenn Sie keinen Titel hinzufügen, wird der Name der Komponente anstelle des Titeltexts angezeigt.

- **Option &quot;Genehmigung einblenden&quot;** - Wählen Sie die Option aus, um das Kontrollkästchen für die Zustimmung anzuzeigen, mit dem der Benutzer explizit seine Zustimmung einholen kann.

- **Als Popup anzeigen** - Wählen Sie die Option aus, um die Komponente &quot;Bedingungen&quot;in einem Popup-Fenster anzuzeigen.

- **Ersetzen des Zustimmungstextes durch Weblinks**: Wählen Sie die Option, um einen Zustimmungstext durch einen Web-Link zu ersetzen.  Wenn die Option deaktiviert ist, wird standardmäßig der Text für die Zustimmung angezeigt.

- **Titel ausblenden**: Wählen Sie die Option aus, um den Titel der Komponente auszublenden.

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

**Text für Bildschirmlesehilfen** – Das ist zusätzlicher Text, der von Hilfstechnologien wie etwa Bildschirmlesehilfen für sehbehinderte Personen vorgelesen wird. Dieser Text enthält eine Audiobeschreibung des Zwecks des Formularfelds und kann Informationen über den Titel, die Beschreibung, den Namen und alle relevanten Nachrichten (benutzerdefinierten Text) des Felds enthalten. Der Text der Bildschirmlesehilfe hilft sicherzustellen, dass das Formular allen Benutzenden zugänglich ist, auch Personen mit Sehschwäche, und bietet ihnen ein umfassendes Verständnis des Formularfelds und seiner Anforderungen.

## Dialogfeld „Design“ {#design-dialog}

Das Dialogfeld &quot;Design&quot;wird verwendet, um CSS-Stile für die Komponente &quot;Allgemeine Geschäftsbedingungen&quot;zu definieren und zu verwalten.


### Registerkarte „Stile“ {#styles-tab}

Sie können die Registerkarte zum Definieren und Verwalten von CSS-Stilen für eine Komponente verwenden. Die Kernkomponente &quot;Adaptive Forms - Geschäftsbedingungen&quot;unterstützt die AEM [Stilsystem](/help/get-started/authoring.md#component-styling).

![Dialogfeld „Design“](/help/adaptive-forms/assets/checkbox-style.png)

- **Standard-CSS-Klassen**: Sie können eine standardmäßige CSS-Klasse für die Kernkomponente für adaptive Formulare – Kontrollkästchen-Gruppe bereitstellen.

- **Zulässige Stile**: Sie können Stile definieren, indem Sie einen Namen und die CSS-Klasse angeben, die den Stil darstellen. Sie können beispielsweise einen Stil mit dem Namen „Fettschrift“ erstellen und die CSS-Klasse „Schriftbreite: Fett“ bereitstellen. Sie können diese Stile bei einem adaptiven Formular im adaptiven Formular-Editor anwenden. Um einen Stil anzuwenden, wählen Sie im Editor für adaptive Formulare die Komponente aus, auf die Sie den Stil anwenden möchten, navigieren Sie zum Eigenschaften-Dialog und wählen Sie den gewünschten Stil aus der Dropdown-Liste **Stile**. Wenn Sie die Stile aktualisieren oder ändern müssen, kehren Sie einfach zum Dialogfeld „Design“ zurück, aktualisieren die Stile auf der Registerkarte „Stile“ und speichern die Änderungen.

### Benutzerdefinierte Eigenschaften

![Dialogfeld &quot;Benutzerdefinierte Eigenschaften&quot;](/help/adaptive-forms/assets/checkbox-customproperties.png)

Mit benutzerdefinierten Eigenschaften können Sie benutzerdefinierte Attribute (Schlüssel-Wert-Paare) mithilfe der Formularvorlage mit einer Kernkomponente des adaptiven Formulars verknüpfen. Die benutzerdefinierten Eigenschaften werden im Abschnitt &quot;Eigenschaften&quot;der Headless-Ausgabe der Komponente angezeigt. Dies ermöglicht das Erstellen eines dynamischen Formularverhaltens, das sich basierend auf den benutzerdefinierten Attributwerten anpasst. Beispielsweise können Entwickler verschiedene Ausgabeformate einer Headless-Forms-Komponente für mobile, Desktop- oder Webplattformen entwerfen, wodurch das Benutzererlebnis auf einer Vielzahl von Geräten erheblich verbessert wird.

- **Gruppenname**: Sie können einen Namen angeben, um die benutzerdefinierte Eigenschaftsgruppe zu identifizieren. Sie können mehrere benutzerdefinierte Eigenschaftsgruppen hinzufügen, löschen oder neu anordnen. Nachdem Sie die benutzerdefinierte Eigenschaftsgruppe hinzugefügt haben, sehen Sie die folgenden Optionen:

   - **Schlüssel-Wert-Paare**: Sie können mehrere benutzerdefinierte Eigenschaftsnamen und benutzerdefinierte Eigenschaftswerte hinzufügen, indem Sie auf das **Hinzufügen** -Schaltfläche für jede benutzerdefinierte Eigenschaftsgruppe.

   - **Löschen**: Tippen oder klicken Sie auf , um den benutzerdefinierten Eigenschaftsnamen und den benutzerdefinierten Eigenschaftswert zu löschen.

   - **Neu anordnen**: Tippen oder klicken und ziehen Sie, um die Reihenfolge des benutzerdefinierten Eigenschaftsnamens und des benutzerdefinierten Eigenschaftswerts neu anzuordnen.

## Unterkomponenten der Komponente &quot;Geschäftsbedingungen&quot; {#sub-component}

**Geschäftsbedingungen** component ist eine zusammengesetzte Komponente, die die folgenden Unterkomponenten umfasst:
- [Komponente „Link“](#link)
- [Textkomponente](#text)
- [Kontrollkästchenkomponente](#checkbox)

### Komponente „Link“{#link}

Diese Komponente ersetzt einen Zustimmungstext durch einen Web-Link oder Links. Es wird in einem Szenario verwendet, in dem der Benutzer Verweise auf bestimmte Abschnitte, zusätzliche Informationen oder externe Dokumente anbieten möchte. Sie können die **Link** -Komponente für Besucher mit dem Dialogfeld &quot;Konfigurieren&quot;.

#### Registerkarte „Allgemein“

![Registerkarte „Allgemein“](/help/adaptive-forms/assets/link-basic-tab.png)

- **Name**: Durch den Namen wird die Komponente im Regel-Editor eindeutig identifiziert. Sonderzeichen und Leerzeichen sind im Namen nicht zulässig.

- **Titel**: Sie können mit dem Titel leicht eine Komponente in einem Formular identifizieren. Standardmäßig wird der Titel über der Komponente angezeigt. Wenn Sie keinen Titel hinzufügen, wird der Name der Komponente anstelle des Titeltexts angezeigt.

- **Titel ausblenden**: Wählen Sie die Option aus, um den Titel der Komponente auszublenden.

- **Links** - Geben Sie den Link und den entsprechenden Anzeigetext an, der anstelle des Zustimmungstextes verwendet wird. Sie können mehrere Links hinzufügen, indem Sie auf **Hinzufügen** Schaltfläche.

- **Verbindungsreferenz**: Eine Verbindungsreferenz ist ein Verweis auf ein Datenelement, das in einer externen Datenquelle gespeichert ist und in einem Formular verwendet wird. Sie können mit dem Bindungsverweis Daten dynamisch an Formularfelder binden, sodass das Formular die aktuellsten Daten aus der Datenquelle anzeigen kann. Beispielsweise kann ein Bindungsverweis verwendet werden, um den Namen und die Adresse von Kundinnen und Kunden in einem Formular anzuzeigen, basierend auf der im Formular eingegebenen Kunden-ID. Der Bindungsverweis kann auch verwendet werden, um die Datenquelle mit den im Formular eingegebenen Daten zu aktualisieren. Auf diese Weise können Sie mit AEM Forms Formulare erstellen, die mit externen Datenquellen interagieren und so ein nahtloses Benutzererlebnis bei der Datenerfassung und -verwaltung bieten.

- **Als ungebundenes Formularelement markieren**: Wählen Sie die Option zum Konfigurieren eines Formularfelds, das keinem Schema zugeordnet ist. Mit dieser Option können Sie Daten speichern, ohne die Datenquelle zu aktualisieren. Außerdem können Sie damit Daten auf eine benutzerdefinierte Art und Weise, getrennt von der standardmäßigen Datenbankintegration, verarbeiten.

- **Komponente ausblenden**: Wählen Sie diese Option, um die Komponente aus dem Formular auszublenden. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor. Dies ist nützlich, wenn Sie Informationen speichern müssen, die Benutzende nicht sehen oder direkt ändern müssen.

- **Komponente deaktivieren** - Wählen Sie die Option zum Deaktivieren oder Sperren der Komponente aus. Die deaktivierte Komponente ist nicht aktiv und Endbenutzende können sie nicht bearbeiten. Benutzende können den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor.
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

**Text** -Komponente zeigt den Textinhalt an, der Benutzern Informationen bereitstellt. Diese Komponente enthält die tatsächlichen Geschäftsbedingungen, die Rechtssprache oder andere relevante Textinformationen.

Sie können die [Textkomponente](/help/adaptive-forms/components/text.md) individuell für Besucher mit dem Dialogfeld Konfigurieren . Um Textoptionen für ein nahtloses Benutzererlebnis zu definieren, verwenden Sie die [Dialogfeld &quot;Konfigurieren&quot;der Textkomponente](/help/adaptive-forms/components/text.md#configure-dialog).


### Kontrollkästchenkomponente {#checkbox}

Ein Kontrollkästchen wird verwendet, um die Zustimmung oder Bestätigung des Benutzers einzuholen. Es dient als visueller Indikator dafür, dass der Benutzer die beschriebenen Bedingungen gelesen und akzeptiert hat. Es ist erforderlich, das Kontrollkästchen zur Angabe der Zustimmung des Benutzers auszuwählen.

Sie können die [Kontrollkästchenkomponente](/help/adaptive-forms/components/checkbox.md) individuell für Besucher mit dem Dialogfeld Konfigurieren . Um die Eigenschaften des Kontrollkästchens für ein nahtloses Benutzererlebnis zu definieren, verwenden Sie die [Dialogfeld der Checkbox-Komponente konfigurieren](/help/adaptive-forms/components/checkbox.md#configure-dialog).


## Ähnliche Artikel {#related-articles}

{{more-like-this}}

## Siehe auch {#see-also}

{{see-also}}
