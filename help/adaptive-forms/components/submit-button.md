---
title: Kernkomponente „Senden-Schaltfläche“ für adaptive Formulare
description: Verwenden oder Anpassen der Kernkomponente „Senden-Schaltfläche“ für adaptive Formulare.
role: Architect, Developer, Admin, User
exl-id: e4b8e475-79b9-4c4d-9f11-a125a424d32b
source-git-commit: e0ed415bd7f45fdca6fbbb8ba409604d9e82a647
workflow-type: tm+mt
source-wordcount: '1380'
ht-degree: 83%

---

# Schaltfläche „Senden“ {#submit-button}

Eine Senden-Schaltfläche in einem adaptiven Formular ist eine Schaltfläche, mit der Benutzende die Formulardaten zur Verarbeitung an einen Server senden können. Wenn die Senden-Schaltfläche angeklickt wird, werden die Formulardaten an den Server gesendet, wo sie gespeichert, verarbeitet oder für verschiedene Zwecke verwendet werden können, z. B. zum Senden einer E-Mail oder zum Aktualisieren einer Datenbank.

Die Senden-Schaltfläche ist normalerweise der letzte Schritt im Formularausfüllprozess und wird verwendet, um den Prozess zum Senden der Formulardaten an den Server zu initiieren.

**Beispiel**

![Schaltflächenbeispiel](/help/adaptive-forms/assets/example-button.png)

## Verwendung {#reasons-to-use-submit-button}

Die Gründe für die Verwendung einer Senden-Schaltfläche in einem adaptiven Formular sind:

- **Datenübermittlung**: Die Senden-Schaltfläche ist der primäre Mechanismus zum Senden von Formulardaten zur Verarbeitung an einen Server.

- **Verbessertes Benutzererlebnis**: Eine gut gestaltete Senden-Schaltfläche kann das Benutzererlebnis verbessern, indem sie eine deutliche Rückmeldung zum Übermittlungsprozess des Formulars gibt und anzeigt, wann das Formular erfolgreich gesendet wurde.

- **Datenvalidierung**: Die Senden-Schaltfläche kann zum Auslösen von Datenvalidierungsprüfungen verwendet werden, um sicherzustellen, dass die Formulardaten vollständig und korrekt sind, bevor sie an den Server gesendet werden.


## Version und Kompatibilität {#version-and-compatibility}

Die Kernkomponente „Akkordeon“ für adaptive Formulare wurde im Februar 2023 als Teil der Kernkomponenten 2.0.4 für Cloud Service und der Kernkomponenten 1.1.12 für AEM 6.5.16.0 Forms oder höher veröffentlicht. Hier finden Sie eine Tabelle mit allen unterstützten Versionen, AEM-Kompatibilität und Links zur entsprechenden Dokumentation:

| Komponentenversion | AEM as a Cloud Service | AEM 6.5.16.0 Forms oder höher |
|---|---|---|
| v1 | Kompatibel mit<br>[Version 2.0.4](/help/adaptive-forms/version.md) und höher | Kompatibel mit<br>[Version 1.1.12](/help/adaptive-forms/version.md) und höher (aber nur bis Version 2.0.0). |

Informationen zu Versionen und Freigaben der Kernkomponente finden Sie im Dokument [Kernkomponenten-Versionen](/help/adaptive-forms/version.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technische Details {#technical-details}

Die neuesten Informationen zur Kernkomponente „Senden-Schaltfläche“ für adaptive Formulare finden Sie in der technischen Dokumentation auf [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/button/v1/button). Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Entwicklerdokumentation für Kernkomponenten](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Im Dialogfeld „Konfigurieren“ können Sie die Senden-Schaltfläche für Besuchende einfach anpassen. Sie können auch Optionen für die Senden-Schaltfläche definieren, um das Benutzererlebnis zu verbessern.

### Registerkarte „Allgemein“ {#basic-tab}

![Registerkarte „Allgemein“](/help/adaptive-forms/assets/button_basictab.png)

- **Name**: Sie können eine Formularkomponente sowohl im Formular als auch im Regel-Editor leicht mit ihrem eindeutigen Namen identifizieren. Der Name darf jedoch keine Leerzeichen oder Sonderzeichen enthalten.

- **Titel**: Sie können mit dem Titel leicht eine Komponente in einem Formular identifizieren. Standardmäßig wird der Titel über der Komponente angezeigt. Wenn Sie keinen Titel hinzufügen, wird der Name der Komponente anstelle des Titeltexts angezeigt.

- **Bindungsverweis**: Bindungsverweis ist ein Verweis auf ein Datenelement, das in einer externen Datenquelle gespeichert ist und in einem Formular verwendet wird. Sie können mit dem Bindungsverweis Daten dynamisch an Formularfelder binden, sodass das Formular die aktuellsten Daten aus der Datenquelle anzeigen kann. Beispielsweise kann ein Bindungsverweis verwendet werden, um den Namen und die Adresse von Kundinnen und Kunden in einem Formular anzuzeigen, basierend auf der im Formular eingegebenen Kunden-ID. Der Bindungsverweis kann auch verwendet werden, um die Datenquelle mit den im Formular eingegebenen Daten zu aktualisieren. Auf diese Weise können Sie mit AEM Forms Formulare erstellen, die mit externen Datenquellen interagieren und so eine nahtlose Benutzererfahrung bei der Datenerfassung und Datenverwaltung bieten.
- **Als ungebundenes Formularelement markieren**: Wählen Sie die Option zum Konfigurieren eines Formularfelds, das keinem Schema zugeordnet ist. Mit dieser Option können Sie Daten speichern, ohne die Datenquelle zu aktualisieren. Außerdem können Sie damit Daten auf eine benutzerdefinierte Art und Weise, getrennt von der standardmäßigen Datenbankintegration, verarbeiten.

- **Komponente ausblenden**: Wählen Sie diese Option, um die Komponente aus dem Formular auszublenden. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor. Dies ist nützlich, wenn Sie Informationen speichern müssen, die Benutzende nicht sehen oder direkt ändern müssen.
- **Komponente deaktivieren**: Wählen Sie die Option zum Deaktivieren der Komponente aus. Die deaktivierte Komponente ist nicht aktiv und Endbenutzende können sie nicht bearbeiten. Benutzende können den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor.
- **Schreibgeschützt**: Wählen Sie die Option aus, um die Komponente nicht bearbeitbar zu machen. Benutzende können den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor.

### Registerkarte „Hilfe-Inhalt“ {#help-content}

![Registerkarte „Hilfe-Inhalt“](/help/adaptive-forms/assets/button_helptab.png)

- **Kurzbeschreibung**: Eine Kurzbeschreibung ist eine kurze Erklärung, die zusätzliche Informationen oder Klarstellungen über den Zweck eines Formularfelds bietet. Es hilft Benutzenden zu verstehen, welcher Datentyp in das Feld eingegeben werden soll, und kann Richtlinien oder Beispiele bereitstellen, um sicherzustellen, dass die eingegebenen Informationen gültig sind und die gewünschten Kriterien erfüllen. Standardmäßig bleiben kurze Beschreibungen ausgeblendet. Aktivieren Sie die Option **Kurzbeschreibung immer anzeigen**, um sie unterhalb der Komponente anzuzeigen.

- **Kurzbeschreibung immer anzeigen**: Aktivieren Sie diese Option, um die Kurzbeschreibung unterhalb der Komponente anzuzeigen.

- **Hilfetext**: Hilfetext bezieht sich auf zusätzliche Informationen oder Anleitungen, die den Benutzenden bereitgestellt werden, um sie beim korrekten Ausfüllen eines Formularfelds zu unterstützen. Er erscheint, wenn Benutzende auf das Hilfesymbol (i) neben der Komponente klicken. Hilfetext enthält detailliertere Informationen als die Beschriftung oder der Platzhaltertext eines Formularfelds und soll den Benutzenden dabei helfen, die Anforderungen oder Einschränkungen des Felds zu verstehen. Er kann auch Vorschläge oder Beispiele anbieten, um das Ausfüllen des Formulars einfacher und genauer zu gestalten.

### Barrierefreiheit {#accessibility}

![Registerkarte „Barrierefreiheit“](/help/adaptive-forms/assets/button_accessibilitytab.png)

**Text für Bildschirmlesehilfen** – Das ist zusätzlicher Text, der von Hilfstechnologien wie etwa Bildschirmlesehilfen für sehbehinderte Personen vorgelesen wird. Dieser Text enthält eine Audiobeschreibung des Zwecks des Formularfelds und kann Informationen über den Titel, die Beschreibung, den Namen und alle relevanten Nachrichten (benutzerdefinierten Text) des Felds enthalten. Der Text der Bildschirmlesehilfe hilft sicherzustellen, dass das Formular allen Benutzenden zugänglich ist, auch Personen mit Sehschwäche, und bietet ihnen ein umfassendes Verständnis des Formularfelds und seiner Anforderungen.

## Dialogfeld „Design“ {#design-dialog}

Das Design-Dialogfeld wird verwendet, um CSS-Stile für die Komponente „Senden-Schaltfläche“ zu definieren und zu verwalten.

### Registerkarte „Stile“ {#styles-tab}

Sie können die Registerkarte zum Definieren und Verwalten von CSS-Stilen für eine Komponente verwenden. Die Kernkomponente „Senden-Schaltfläche“ für adaptive Formulare unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).

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