---
title: Adaptive Forms-Kernkomponente - Kontrollkästchen
description: Verwenden oder Anpassen der Kernkomponente "Adaptive Forms Checkbox".
role: Architect, Developer, Admin, User
exl-id: c6ca4800-bd10-4aeb-957a-fb1780cf94f3
source-git-commit: a567b5ad937d426abe16c34e039e19cd0b1af5b0
workflow-type: tm+mt
source-wordcount: '1706'
ht-degree: 53%

---

# Kontrollkästchen {#checkbox-component}

Ein Kontrollkästchen ist ein grafisches Element der Benutzeroberfläche, das häufig in Softwareanwendungen und Formularen verwendet wird, um Benutzern die Möglichkeit zu geben, zwischen zwei Optionen eine binäre Auswahl zu treffen: &quot;Aktiviert&quot;(aktiviert) oder &quot;Nicht aktiviert&quot;(deaktiviert).

Ein Kontrollkästchen wird in der Regel als kleines Quadrat dargestellt, das durch Klicken oder Tippen ein- oder ausgeschaltet werden kann. Wenn ein Kontrollkästchen aktiviert ist, wird ein Häkchen angezeigt, das anzeigt, dass die zugehörige Option oder Funktion aktiv oder aktiviert ist.

**Beispiel**

![Kontrollkästchengruppe](/help/adaptive-forms/assets/checkbox-example.png)

## Verwendung {#reasons-to-use-checkbox}

Häufige Gründe für die Verwendung des Kontrollkästchens in einem adaptiven Formular sind:

- **Benutzerfreundlichkeit**: Kontrollkästchen sind visuell klar und bieten eine einfache Möglichkeit, binäre Entscheidungen zu treffen. Sie sind intuitiv und leicht zu verstehen, sodass sie benutzerfreundlich sind.

- **Einverständnis und Einigung**: Kontrollkästchen werden verwendet, um die Zustimmung des Benutzers zu verschiedenen Zwecken zu erhalten, z. B. zur Annahme von Nutzungsbedingungen, zum Abonnieren von Newslettern oder zur Bestätigung der Altersüberprüfung. Sie machen deutlich, dass der Benutzer aktiv einer Sache zustimmt.

- **Visuelle Bestätigung**: Aktivierte Kontrollkästchen bieten Benutzern eine visuelle Bestätigung, dass ihre Auswahl aufgezeichnet wurde. Dieses Feedback hilft Benutzerfehler zu vermeiden und stellt sicher, dass die Benutzer wissen, dass ihre Auswahlmöglichkeiten registriert wurden.

- **Fehlervermeidung**: Kontrollkästchen reduzieren die Fehlerwahrscheinlichkeit, indem sie es Benutzern ermöglichen, die Optionen vor der Formularübermittlung zu überprüfen und zu bestätigen.

## Version und Kompatibilität {#version-and-compatibility}

Die Kernkomponente &quot;Adaptive Forms Checkbox&quot;wurde als Teil der Kernkomponenten 2.0.52 veröffentlicht. In der folgenden Tabelle finden Sie alle unterstützten Versionen, AEM Kompatibilität und Links zur entsprechenden Dokumentation:

|  |  |
|---|---|
| Komponentenversion | AEM as a Cloud Service |
| --- | --- |
| v1 | Kompatibel mit<br>[Version 2.0.52](/help/versions.md) und höher | Kompatibel | Kompatibel |

Informationen zu Versionen und Freigaben der Kernkomponente finden Sie im Dokument [Kernkomponenten-Versionen](/help/versions.md).

## Technische Details {#technical-details}

Laden Sie die neuesten Informationen zur Kernkomponente &quot;Adaptive Forms Checkbox&quot;in der technischen Dokumentation zu [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/checkbox/v1/checkbox). Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Entwicklerdokumentation für Kernkomponenten](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Im Dialogfeld &quot;Konfigurieren&quot;können Sie das Kontrollkästchen-Erlebnis für Besucher einfach anpassen. Sie können auch Kontrollkästchen-Optionen für ein nahtloses Benutzererlebnis definieren.

![Registerkarte „Allgemein“](/help/adaptive-forms/assets/checkbox-basic.png)

- **Name**: Sie können eine Formularkomponente sowohl im Formular als auch im Regeleditor durch ihren eindeutigen Namen identifizieren. Der Name darf keine Leerzeichen oder Sonderzeichen enthalten.

- **Titel** - Mit dem Titel können Sie eine Komponente in einem Formular leicht identifizieren. Standardmäßig wird der Titel neben der Komponente angezeigt. Wenn Sie keinen Titel hinzufügen, wird die Komponente nicht angezeigt.

- **Titel ausblenden**: Wählen Sie die Option aus, um den Titel der Komponente auszublenden.

- **Verbindungsreferenz**: Eine Verbindungsreferenz ist ein Verweis auf ein Datenelement, das in einer externen Datenquelle gespeichert ist und in einem Formular verwendet wird. Sie können mit dem Bindungsverweis Daten dynamisch an Formularfelder binden, sodass das Formular die aktuellsten Daten aus der Datenquelle anzeigen kann. Beispielsweise kann ein Bindungsverweis verwendet werden, um den Namen und die Adresse von Kundinnen und Kunden in einem Formular anzuzeigen, basierend auf der im Formular eingegebenen Kunden-ID. Der Bindungsverweis kann auch verwendet werden, um die Datenquelle mit den im Formular eingegebenen Daten zu aktualisieren. Auf diese Weise können Sie mit AEM Forms Formulare erstellen, die mit externen Datenquellen interagieren und so ein nahtloses Benutzererlebnis bei der Datenerfassung und -verwaltung bieten.

- **Als ungebundenes Formularelement markieren**: Wählen Sie die Option zum Konfigurieren eines Formularfelds, das keinem Schema zugeordnet ist. Mit dieser Option können Sie Daten speichern, ohne die Datenquelle zu aktualisieren. Außerdem können Sie damit Daten auf eine benutzerdefinierte Art und Weise, getrennt von der standardmäßigen Datenbankintegration, verarbeiten.

- **Datentyp des gesendeten Werts**: Diese Option gibt den Datentyp des Werts an, der gesendet wird, wenn eine Option ausgewählt ist. Wenn der **Datentyp des gesendeten Werts** auf `Number` festgelegt ist und Sie auf der Registerkarte **Optionen** Zeichenfolgedaten zum **Datenwert** hinzufügen, wird am Bildschirm die Fehlermeldung `Value type mismatch` angezeigt.

- **Komponente ausblenden**: Wählen Sie diese Option, um die Komponente aus dem Formular auszublenden. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor. Dies ist nützlich, wenn Sie Informationen speichern müssen, die Benutzende nicht sehen oder direkt ändern müssen.

- **Komponente deaktivieren** - Wählen Sie die Option zum Deaktivieren oder Sperren der Komponente aus. Die deaktivierte Komponente ist nicht aktiv und Endbenutzende können sie nicht bearbeiten. Benutzende können den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor.
- **Schreibgeschützt**: Wählen Sie die Option aus, um die Komponente nicht bearbeitbar zu machen. Benutzende können den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor.
- **Wenn aktiviert, Rückgabewert** -Wählen Sie diese Option aus, um festzulegen, welcher Wert dem Kontrollkästchen zugeordnet werden soll, wenn es aktiviert oder ausgewählt ist. Es ist die Aktion, die auftritt, wenn Sie das Kontrollkästchen markieren oder ankreuzen.
- **Aktivieren Sie die Option „Deaktivieren“.**- Wählen Sie die Option aus, um die Möglichkeit zum Deaktivieren eines zuvor aktivierten Kontrollkästchens zu aktivieren oder zu deaktivieren.
   - Wenn **Deaktivieren** aktiviert oder auf &quot;true&quot;gesetzt ist, bedeutet dies, dass der Benutzer das Kontrollkästchen nach seinem Ermessen aktivieren und deaktivieren kann. Sie können das Kontrollkästchen nach Bedarf aktivieren und deaktivieren.

   - Wenn **Deaktivieren** deaktiviert oder auf &quot;false&quot;gesetzt ist, bedeutet dies, dass der Benutzer die Markierung nicht mehr deaktivieren darf, sobald das Kontrollkästchen aktiviert wurde.
- **Wenn deaktiviert, Rückgabewert** - Mit der Option können Sie festlegen, welcher Wert mit dem Kontrollkästchen verknüpft werden soll, wenn es sich in einem deaktivierten oder deaktivierten Status befindet.

- **Standardwert**: Mit dieser Option können Sie einen Standardwert in ein Formularfeld einfügen. Wenn **Komponente deaktiviert** oder **Schreibgeschützte Komponente** ausgewählt ist, wird der Standardwert auf dem Bildschirm angezeigt. Wenn Benutzende keinen Wert in das Formularfeld eingeben, wird dieser Wert zum Zeitpunkt der Formularübermittlung gesendet.

### Registerkarte „Validierung“ {#validation-tab}

![Registerkarte „Validierung“](/help/adaptive-forms/assets/checkbox-validation.png)

- **Erforderlich**: Wählen Sie diese Option, wenn Sie die Komponente in einem adaptiven Formular anzeigen möchten. Nachdem Sie die Option ausgewählt haben, müssen Sie eine Auswahl treffen, bevor Sie mit der Formularübermittlung fortfahren. Wenn diese Option aktiviert ist, kann die Option **Komponente ausblenden** oder **Komponente deaktivieren** auf der Registerkarte **Allgemein** nicht ausgewählt werden.

- **Fehlermeldung**: Mit dieser Option können Sie eine Nachricht eingeben, die angezeigt wird, wenn das Kontrollkästchen **Erforderlich** aktiviert ist und das Feld leer bleibt.

- **Meldung zur Skriptvalidierung**: Mit dieser Option können Sie eine Meldung eingeben, die angezeigt werden soll, wenn die Skriptvalidierung fehlschlägt.

### Registerkarte „Hilfe-Inhalt“ {#helpcontent-tab}

![Registerkarte „Hilfe-Inhalt“](/help/adaptive-forms/assets/checkbox-help.png)

- **Kurzbeschreibung**: Eine Kurzbeschreibung ist eine kurze Erklärung, die zusätzliche Informationen oder Klarstellungen über den Zweck eines Formularfelds bietet. Es hilft Benutzenden zu verstehen, welcher Datentyp in das Feld eingegeben werden soll, und kann Richtlinien oder Beispiele bereitstellen, um sicherzustellen, dass die eingegebenen Informationen gültig sind und die gewünschten Kriterien erfüllen. Standardmäßig bleiben kurze Beschreibungen ausgeblendet. Aktivieren Sie die Option **Kurzbeschreibung immer anzeigen**, um sie unterhalb der Komponente anzuzeigen.

- **Kurzbeschreibung immer anzeigen**: Aktivieren Sie diese Option, um die Kurzbeschreibung unterhalb der Komponente anzuzeigen.

- **Hilfetext**: Hilfetext bezieht sich auf zusätzliche Informationen oder Anleitungen, die den Benutzenden bereitgestellt werden, um sie beim korrekten Ausfüllen eines Formularfelds zu unterstützen. Er erscheint, wenn Benutzende auf das Hilfesymbol (i) neben der Komponente klicken. Hilfetext enthält detailliertere Informationen als die Beschriftung oder der Platzhaltertext eines Formularfelds und soll den Benutzenden dabei helfen, die Anforderungen oder Einschränkungen des Felds zu verstehen. Er kann auch Vorschläge oder Beispiele anbieten, um das Ausfüllen des Formulars einfacher und genauer zu gestalten.

### Registerkarte „Barrierefreiheit“ {#accessibility-tab}

![Registerkarte „Barrierefreiheit“](/help/adaptive-forms/assets/checkbox-accessibility.png)

**Text für Bildschirmlesehilfen** – Das ist zusätzlicher Text, der von Hilfstechnologien wie etwa Bildschirmlesehilfen für sehbehinderte Personen vorgelesen wird. Dieser Text enthält eine Audiobeschreibung des Zwecks des Formularfelds und kann Informationen über den Titel, die Beschreibung, den Namen und alle relevanten Nachrichten (benutzerdefinierten Text) des Felds enthalten. Der Text der Bildschirmlesehilfe hilft sicherzustellen, dass das Formular allen Benutzenden zugänglich ist, auch Personen mit Sehschwäche, und bietet ihnen ein umfassendes Verständnis des Formularfelds und seiner Anforderungen.

## Dialogfeld „Design“ {#design-dialog}

Das Dialogfeld &quot;Design&quot;wird zum Definieren und Verwalten von CSS-Stilen für die Komponente &quot;Kontrollkästchen&quot;verwendet.

### Registerkarte „Stile“ {#styles-tab}

Die Kernkomponente &quot;Adaptives Forms-Kontrollkästchen&quot;unterstützt die AEM [Stilsystem](/help/get-started/authoring.md#component-styling).

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

## Ähnliche Artikel {#related-articles}

{{more-like-this}}

## Siehe auch {#see-also}

{{see-also}}
