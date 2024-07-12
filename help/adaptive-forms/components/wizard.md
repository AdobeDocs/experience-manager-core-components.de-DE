---
title: Kernkomponente „Assistent“ für adaptive Formulare
description: Verwenden oder Anpassen der Kernkomponente „Assistent“ für adaptive Formulare.
role: Architect, Developer, Admin, User
exl-id: fd785cd2-5ed6-4efb-997f-ce9056ed113d
source-git-commit: 8bba79956a04020647d5d04f9fe6fa674affedf1
workflow-type: tm+mt
source-wordcount: '2186'
ht-degree: 100%

---

# Komponente „Assistent“{#wizard-adaptive-forms-core-component}

Ein Assistenten-Layout in einem adaptiven Formular ist in mehrere Schritte oder Seiten unterteilt, wobei Benutzende das Formular Schritt für Schritt durchlaufen. Dieses Layout wird als „Assistent“ bezeichnet, da es den Benutzer schrittweise durch das Formular führt.

Jeder Schritt des Assistenten beinhaltet in der Regel eine Gruppe verwandter Formularfelder und einen Navigationsmechanismus, z. B. die Schaltflächen „Weiter“ und „Zurück“, mit denen sich Benutzende zwischen den Schritten bewegen können. Benutzende können erst mit dem nächsten Schritt fortfahren, nachdem der aktuelle Schritt abgeschlossen und alle erforderlichen Felder ausgefüllt wurden.

Das Assistenten-Layout ist nützlich, wenn Formulare viele Felder oder Informationen enthalten, die ausgefüllt werden müssen, da das Formular in kleinere, besser überblickbare Abschnitte unterteilt wird. Außerdem können sich Benutzende auf eine Gruppe von Feldern konzentrieren, sodass das Ausfüllen des Formulars sie nicht überfordert.

Dieses Layout kann jedoch auch die Komplexität des Formulars erhöhen, da Benutzende mehrere Seiten durchlaufen müssen, um es auszufüllen. Daher müssen vor der Verwendung des Assistenten-Layouts die Anforderungen des Formulars sowie die Bedürfnisse der Benutzenden sorgfältig überlegt werden.
Sie können die Kernkomponente „Assistent“ für adaptive Formulare verwenden, um ein Assistenten-Layout zu erstellen.

**Beispiel**

![Beispiel](/help/adaptive-forms/assets/wizard.png)

## Verwendung {#reasons-to-use-wizard-in-an-adaptive-form}

Es gibt mehrere Gründe, warum die Verwendung eines Assistenten-Layouts in einem adaptiven Formular von Vorteil sein kann:

- **Einfachheit**: Die Unterteilung eines Formulars in mehrere Schritte kann Benutzenden helfen, das Formular besser zu verstehen und auszufüllen, da sie sich jeweils auf eine Gruppe von Feldern konzentrieren können.

- **Organisation**: Mit einem Assistenten-Layout können Sie Formulare nach Thema oder Zweck organisieren. Außerdem können zugehörige Felder gruppiert werden, was den Formularausfüll-Prozess logischer und effizienter gestaltet.

- **Validierung**: Ein Assistenten-Layout ermöglicht die schrittweise Überprüfung, durch die Benutzende Fehler schon beim Ausfüllen anstatt erst am Ende erkennen und korrigieren können.

- **Fortschrittsanzeige**: Ein Assistenten-Layout kann den Fortschritt des Formulars anzeigen, damit Benutzende wissen, wie viel vom Formular noch auszufüllen ist.

- **Lange Formulare**: Wenn ein Formular viele Felder enthält, können sich Benutzende leicht überfordert fühlen, wenn sie alle gleichzeitig angezeigt werden. Dagegen wirkt die Unterteilung in kleinere, besser handhabbare Abschnitte weniger abschreckend.

- **Vermeiden von Abbrüchen**: Ein Assistenten-Layout kann auch dazu beitragen, den Formularabbruch zu reduzieren, da Benutzende mit höherer Wahrscheinlichkeit ein Formular ausfüllen, wenn sie den Fortschritt sehen und verstehen können, wie viel noch zu erledigen ist.

- **Mobile Erlebnisse**: Ein Assistenten-Layout kann auch für Formulare von Vorteil sein, die auf Mobilgeräte geladen werden, da es kleinere Seiten ermöglicht, die schneller geladen werden und leichter zu navigieren sind.

Insgesamt kann ein Assistenten-Layout das Ausfüllen eines Formulars einfacher und effizienter gestalten. Es ist jedoch wichtig, die Komplexität des Formulars und die Anforderungen der Benutzenden zu berücksichtigen, bevor Sie sich für die Verwendung dieses Layouts entscheiden.

## Version und Kompatibilität {#version-and-compatibility}

Die Kernkomponente „Assistent“ für adaptive Formulare wurde im Februar 2023 als Teil der Kernkomponenten 2.0.4 veröffentlicht. Hier finden Sie eine Tabelle mit allen unterstützten Versionen, Informationen zur AEM Kompatibilität und Links zur entsprechenden Dokumentation:

|  |  |
|---|---|
| Komponentenversion | AEM as a Cloud Service |
| --- | --- |
| v1 | Kompatibel mit<br>[Version 2.0.4](/help/adaptive-forms/version.md) und höher | Kompatibel | Kompatibel |

Informationen zu Versionen und Freigaben der Kernkomponente finden Sie im Dokument [Kernkomponenten-Versionen](/help/adaptive-forms/version.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technische Details {#technical-details}

Die neuesten Informationen zur Kernkomponente „Titel“ für adaptive Formulare finden Sie in der technischen Dokumentation auf [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/wizard/v1/wizard). Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Entwicklerdokumentation für Kernkomponenten](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Im Dialogfeld „Konfigurieren“ können Sie den Assistenten für Besuchende einfach anpassen. Sie können auch Assistenten-Optionen definieren, um das Benutzererlebnis zu verbessern.

### Registerkarte „Allgemein“ {#basic-tab}

![Registerkarte „Allgemein“](/help/adaptive-forms/assets/wizard-basic.png)

- **Name**: Sie können eine Formularkomponente sowohl im Formular als auch im Regeleditor durch ihren eindeutigen Namen identifizieren. Der Name darf keine Leerzeichen oder Sonderzeichen enthalten.

- **Titel**: Mit dem Titel können Sie eine Komponente in einem Formular leicht identifizieren. Standardmäßig wird der Titel oberhalb der Komponente angezeigt.

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

<!--   **Wrap data in an object** - Choose "Wrap data in an object" to put the field data from the Wizard inside a JSON object. If not chosen, the submit data JSON has a flat structure for the Wizard's fields.

-   **Layout** - You can have either a fixed layout (Simple) or a flexible layout (Responsive Grid) for your wizard. The Simple layout keeps everything fixed in the place, while the Responsive Grid allows you to adjust the position of components to suit your needs. For example, use Responsive Grid to align "First Name", "Middle Name" and "Last Name" in a form in a single row.  -->

- **Bindungsreferenz**: Eine Bindungsreferenz ist ein Verweis auf ein Datenelement, das in einer externen Datenquelle gespeichert ist und in einem Formular verwendet wird. Sie können mit dem Bindungsverweis Daten dynamisch an Formularfelder binden, sodass das Formular die aktuellsten Daten aus der Datenquelle anzeigen kann. Beispielsweise kann ein Bindungsverweis verwendet werden, um den Namen und die Adresse von Kundinnen und Kunden in einem Formular anzuzeigen, basierend auf der im Formular eingegebenen Kunden-ID. Der Bindungsverweis kann auch verwendet werden, um die Datenquelle mit den im Formular eingegebenen Daten zu aktualisieren. Auf diese Weise können Sie mit AEM Forms Formulare erstellen, die mit externen Datenquellen interagieren und so ein nahtloses Benutzererlebnis bei der Datenerfassung und -verwaltung bieten.

- **Komponente ausblenden**: Wählen Sie diese Option, um die Komponente aus dem Formular auszublenden. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor. Dies ist nützlich, wenn Sie Informationen speichern müssen, die Benutzende nicht sehen oder direkt ändern müssen.

- **Komponente deaktivieren**: Wählen Sie die Option zum Deaktivieren der Komponente aus. Die deaktivierte Komponente ist nicht aktiv und Endbenutzende können sie nicht bearbeiten. Benutzende können den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor.

- **Schreibgeschützt**: Wählen Sie die Option aus, um die Komponente nicht bearbeitbar zu machen. Benutzende können den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor.

### Registerkarte „Assistent wiederholen“ {#repeat-wizard-tab}

![Assistent wiederholen](/help/adaptive-forms/assets/wizard-repeat.png)

Sie können die Wiederholungsoptionen verwenden, um den Assistenten und seine untergeordneten Komponenten zu duplizieren, eine minimale und maximale Wiederholungsanzahl zu definieren und die Replikation ähnlicher Abschnitte innerhalb eines Formulars zu erleichtern. Bei der Interaktion mit der Assistentenkomponente und dem Zugriff auf ihre Einstellungen werden die folgenden Optionen angezeigt:

- **Assistenten wiederholbar machen**: Eine Umschalter-Funktion, mit der Benutzende die Wiederholungsfunktion aktivieren oder deaktivieren können.
- **Mindestwiederholungen**: Legt fest, wie oft das Assistenten-Bedienfeld mindestens wiederholt werden kann. Der Wert null zeigt an, dass das Bedienfeld „Assistent“ nicht wiederholt wird. Der Standardwert ist null.
- **Maximale Wiederholungen**: Legt fest, wie oft das Assistenten-Bedienfeld maximal wiederholt werden kann. Standardmäßig ist dieser Wert unbegrenzt.

Um wiederholbare Abschnitte im Assistenten effektiv zu verwalten, folgen Sie den Schritten, die im Artikel [Erstellen von Formularen mit wiederholbaren Abschnitten](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/create-forms-repeatable-sections.html?lang=de) beschrieben sind.

### Registerkarte „Elemente“ {#items-tab}

![Registerkarte „Elemente“](/help/adaptive-forms/assets/wizard_itemstab.png)

Mit dieser Option können Sie adaptive Formularkomponenten hinzufügen, indem Sie auf „Hinzufügen“ klicken. Diese Schaltfläche wird standardmäßig angezeigt, wenn der Assistent im Bearbeitungsmodus hinzugefügt wird.

### Registerkarte „Hilfe“ {#help-tab}

![Registerkarte „Hilfe“](/help/adaptive-forms/assets/wizard_helptab.png)

- **Kurzbeschreibung**: Eine Kurzbeschreibung ist eine kurze Erklärung, die zusätzliche Informationen oder Klarstellungen über den Zweck eines Formularfelds bietet. Es hilft Benutzenden zu verstehen, welcher Datentyp in das Feld eingegeben werden soll, und kann Richtlinien oder Beispiele bereitstellen, um sicherzustellen, dass die eingegebenen Informationen gültig sind und die gewünschten Kriterien erfüllen. Standardmäßig bleiben kurze Beschreibungen ausgeblendet. Aktivieren Sie die Option **Kurzbeschreibung immer anzeigen**, um sie unterhalb der Komponente anzuzeigen.

- **Kurzbeschreibung immer anzeigen**: Aktivieren Sie diese Option, um die Kurzbeschreibung unterhalb der Komponente anzuzeigen.

- **Hilfetext**: Hilfetext bezieht sich auf zusätzliche Informationen oder Anleitungen, die den Benutzenden bereitgestellt werden, um sie beim korrekten Ausfüllen eines Formularfelds zu unterstützen. Er erscheint, wenn Benutzende auf das Hilfesymbol (i) neben der Komponente klicken. Hilfetext enthält detailliertere Informationen als die Beschriftung oder der Platzhaltertext eines Formularfelds und soll den Benutzenden dabei helfen, die Anforderungen oder Einschränkungen des Felds zu verstehen. Er kann auch Vorschläge oder Beispiele anbieten, um das Ausfüllen des Formulars einfacher und genauer zu gestalten.


### Registerkarte „Barrierefreiheit“ {#accessibility}

![Registerkarte „Barrierefreiheit“](/help/adaptive-forms/assets/wizard_accessibiltytab.png)

- **Text für Bildschirmlesehilfen** – Das ist zusätzlicher Text, der von Hilfstechnologien wie etwa Bildschirmlesehilfen für sehbehinderte Personen vorgelesen wird. Dieser Text enthält eine Audiobeschreibung des Zwecks des Formularfelds und kann Informationen über den Titel, die Beschreibung, den Namen und alle relevanten Nachrichten (benutzerdefinierten Text) des Felds enthalten. Der Text der Bildschirmlesehilfe hilft sicherzustellen, dass das Formular allen Benutzenden zugänglich ist, auch Personen mit Sehschwäche, und bietet ihnen ein umfassendes Verständnis des Formularfelds und seiner Anforderungen.
   - **Benutzerdefinierter Text**: Wählen Sie diese Option aus, um den benutzerdefinierten Text für ARIA-Barrierefreiheitsbeschriftungen zu verwenden. Wenn Sie diese Option auswählen, wird das Benutzerdefinierter Dialogfeld „Text“ angezeigt. Sie können relevante Informationen im Benutzerdefinierter Dialogfeld „Text“ hinzufügen.
   - **Beschreibung**: Wählen Sie diese Option aus, um die Beschreibung für ARIA-Barrierefreiheitsbeschriftungen zu verwenden.
   - **Titel**: Wählen Sie diese Option aus, um den Titel für ARIA-Barrierefreiheitsbeschriftungen zu verwenden.
   - **Name**: Wählen Sie diese Option aus, um den Namen für ARIA-Barrierefreiheitsbeschriftungen zu verwenden.
   - **Keine**: Wählen Sie diese Option aus, wenn Sie keine ARIA-Barrierefreiheitsbezeichnungen hinzufügen möchten.

- **HTML-Rolle für die Ankündigung durch die Bildschirmlesehilfe** – Die HTML-Rolle ist ein Attribut, mit dem der Zweck eines HTML-Elements für Hilfstechnologien wie Bildschirmlesehilfen spezifiziert wird. Rollenattribute werden verwendet, um für ein Element zusätzlichen Kontext und eine semantische Bedeutung bereitzustellen, wodurch es für Bildschirmlesehilfen einfacher wird, den Inhalt zu interpretieren und ihn Benutzenden mitzuteilen. In AEM Forms kann beispielsweise die Beschriftung eines Formularfelds die Rolle „Beschriftung“ haben und sein Eingabefeld die Rolle „Textfeld“. Dadurch kann die Bildschirmlesehilfe die Beziehung zwischen Beschrfitung und Eingabefeld verstehen und diese Informationen den Benutzenden korrekt mitteilen.


## Dialogfeld „Design“ {#design-dialog}

Im Dialogfeld „Design“ können Vorlagenerstellende steuern, wie Elemente standardmäßig angezeigt werden. Für die Komponente „Assistent“ für adaptive Formulare können Sie Folgendes festlegen:

- Die Kernkomponenten, die ein Formularersteller bzw. eine Formularerstellerin dem Assistierenden im Editor für adaptive Formulare hinzufügen kann.
- Einfache Namen für Stile (CSS-Klassen), die im Eigenschaften-Dialogfeld der Assistenten-Komponente im Editor für adaptive Formulare angewendet werden können.

Dadurch wird das Erstellen und Anpassen von Formularen einfacher und effizienter.

### Registerkarte „Zugelassene Komponenten“ {#allowed-components-tab}

![Registerkarte „Zugelassene Komponenten“](/help/adaptive-forms/assets/tabs-allowed-component.png)

Über die Registerkarte **Zugelassene Komponenten** kann der Person, die die Vorlage bearbeitet, festlegen, welche Komponenten als Elemente zu den Bedienfeldern der Assistenten-Komponente im Editor für adaptive Formulare hinzugefügt werden können.

### Registerkarte „Stile“ {#styles-tab}

Sie können das Dialogfeld „Design“ zum Definieren und Verwalten von CSS-Stilen für eine Komponente verwenden. Die Assistenten-Kernkomponente für adaptive Formulare unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).

![Registerkarte „Stile“](/help/adaptive-forms/assets/tabs-styles-tab.png)

- **Standard-CSS-Klassen**: Sie können eine standardmäßige CSS-Klasse für die Assistenten-Kernkomponente für adaptive Formulare bereitstellen.

- **Zulässige Stile**: Sie können Stile definieren, indem Sie den Namen und die CSS-Klasse für den Stil angeben. Sie können beispielsweise einen Stil mit dem Namen „Fettschrift“ erstellen und die CSS-Klasse „Schriftbreite: Fett“ bereitstellen. Sie können diese Stile bei einem adaptiven Formular im adaptiven Formular-Editor anwenden. Um einen Stil anzuwenden, wählen Sie im Editor für adaptive Formulare die Komponente aus, auf die Sie den Stil anwenden möchten, navigieren Sie zum Eigenschaften-Dialog und wählen Sie den gewünschten Stil aus der Dropdown-Liste **Stile**. Wenn Sie die Stile aktualisieren oder ändern müssen, kehren Sie einfach zum Dialogfeld „Design“ zurück, aktualisieren die Stile auf der Registerkarte „Stile“ und speichern die Änderungen.

### Registerkarte „Benutzerdefinierte Eigenschaften“

![Registerkarte „Benutzerdefinierte Eigenschaften“](/help/adaptive-forms/assets/tabs-custom-properties.png)

Mit der Option „Benutzerdefinierte Eigenschaften“ können Sie mithilfe der Formularvorlage benutzerdefinierte Attribute (Schlüsselwertpaare) mit einer Kernkomponente eines adaptiven Formulars verknüpfen. Die benutzerdefinierten Eigenschaften werden im Eigenschaftenbereich der Headless-Ausgabedarstellung der Komponente angezeigt. So kann ein dynamisches Formularverhalten erzeugt werden, das sich je nach den benutzerdefinierten Attributwerten anpasst. Beispielsweise können Entwickelnde verschiedene Ausgabedarstellungen einer Headless-Formularkomponente für Mobile-, Desktop- oder Web-Plattformen entwerfen und so das Benutzererlebnis auf einer Vielzahl von Geräten erheblich verbessern.

- **Gruppenname**: Sie können einen Namen angeben, um die Gruppe der benutzerdefinierten Eigenschaften zu kennzeichnen. Sie können mehrere Gruppen benutzerdefinierter Eigenschaften hinzufügen, löschen oder neu anordnen. Nach dem Hinzufügen der Gruppe benutzerdefinierter Eigenschaften werden folgende Optionen angezeigt:

   - **Schlüssel-Wert-Paare**: Sie können mehrere Namen und Werte benutzerdefinierter Eigenschaften hinzufügen, indem Sie für jede Gruppe benutzerdefinierter Eigenschaften auf **Hinzufügen** klicken.

   - **Löschen**: Tippen oder klicken Sie auf diese Option, um den Namen und den Wert der benutzerdefinierten Eigenschaft zu löschen.

   - **Neu anordnen**: Ordnen Sie den Namen und Wert der benutzerdefinierten Eigenschaft Antippen oder Klicken und Ziehen neu an.

## Ähnliche Artikel {#related-articles}

{{more-like-this}}

## Siehe auch {#see-also}

{{see-also}}