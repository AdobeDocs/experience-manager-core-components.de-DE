---
title: Akkordeon für adaptive Formulare
description: Verwenden Sie Akkordeon, um ein langes oder komplexes Formular zu organisieren und zu vereinfachen, indem Sie es in kleinere, besser verwaltbare Abschnitte unterteilen.
role: Architect, Developer, Admin, User
exl-id: 0ed38eee-fc22-4708-82eb-3fb1839b1ff2
source-git-commit: 6725784bd4c94d433c91d6bd65d14d03cbefd954
workflow-type: ht
source-wordcount: '0'
ht-degree: 100%

---


# Akkordeon-Komponente {#accordion-component-adaptive-forms-core-component}

Mit der Akkordeon-Kernkomponente können Benutzende erweiterbare und ausblendbare Abschnitte in einem adaptiven Formular erstellen. Es wird häufig verwendet, um lange oder komplexe Formulare zu organisieren und zu vereinfachen, indem sie in kleinere, besser verwaltbare Abschnitte unterteilt werden. Jeder Abschnitt eines Akkordeons wird in der Regel durch eine Kopfzeile dargestellt, auf die Benutzende klicken können, um den entsprechenden Inhalt zu erweitern oder auszublenden. Der Inhalt kann eine beliebige Kernkomponente sein.

![Beispiel](/help/adaptive-forms/assets/example-accordion.png)

{{traditional-aem}}

## Verwendung {#usage}

Es gibt mehrere Gründe, warum es sinnvoll ist, ein Akkordeon in ein adaptives Formular einzuschließen, darunter:

- **Platzeinsparung**: Benutzende können mit einem Akkordeon Abschnitte eines Formulars erweitern und ausblenden und so den Platz reduzieren, der zum Anzeigen aller Formularfelder auf einmal benötigt wird.

- **Navigation**: Sie können ein Akkordeon verwenden, um eine hierarchische Navigationsstruktur zu erstellen, die es Benutzenden erleichtert, die benötigten Formularfelder zu finden.

- **Benutzererlebnis**: Sie können Akkordeon verwenden, um das Formular benutzerfreundlicher zu gestalten, indem es Benutzenden eine klare und intuitive Möglichkeit bietet, auf Formularfelder zuzugreifen und sie auszufüllen.

- **Lange Formulare**: Akkordeon ist eine ideale Komponente für die Verarbeitung langer Formulare, da sich Benutzende dadurch auf einen Abschnitt auf einmal konzentrieren können, anstatt zu versuchen, viele Informationen gleichzeitig zu verarbeiten.

Sie können Folgendes verwenden:

- Im [Konfigurieren-Dialogfeld](#configure-dialog) können Sie Eigenschaften der Akkordeon-Komponente angeben.

- Sie können das [Popover „Bedienfeld auswählen“](#select-panel-popover) verwenden, um die Reihenfolge der Bedienfelder des Akkordeons zu definieren. Dadurch kann der Autor die Bedienfelder in der Reihenfolge anordnen, in der sie angezeigt werden sollen.

- Optionen für Formularautorinnen und -autoren zum Aktivieren oder Deaktivieren bestimmter Funktionen in [Dialogfeld „Design“](#design-dialog). Eine Autorin oder ein Autor kann beispielsweise bestimmte Felder oder Abschnitte eines Formulars deaktivieren. Diese Optionen ermöglichen es der Autorin oder dem Autor, den Entwurf und die Funktionen des Formulars besser zu steuern, wodurch es einfacher wird, Formulare zu erstellen, die auf die spezifischen Anforderungen des Unternehmens zugeschnitten sind.

Das Dialogfeld „Konfigurieren“ und das Popover „Bedienfeld auswählen“, sowie das Dialogfeld „Design“ sind alle Teil der Kernkomponenten, die erstellt wurden, um das Authoring der Formulare zu vereinfachen und eine effiziente Methode zum Erstellen komplexer Formulare bereitzustellen.

## Version und Kompatibilität {#version-and-compatibility}


Die Kernkomponente für adaptive Formulare bei Akkordeon wurde im Februar 2023 als Teil der Kernkomponenten 2.0.4 veröffentlicht. Hier finden Sie eine Tabelle mit allen unterstützten Versionen, AEM-Kompatibilität und Links zur entsprechenden Dokumentation:

|  |  |
|---|---|
| Komponentenversion | AEM as a Cloud Service |
| --- | --- |
| v1 | Kompatibel mit<br>[Version 2.0.4](/help/adaptive-forms/version.md) und höher | Kompatibel | Kompatibel |

Informationen zu Versionen und Freigaben der Kernkomponente finden Sie im Dokument [Kernkomponenten-Versionen](/help/adaptive-forms/version.md).


<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion_de). -->

## Technische Details {#technical-details}

Aktuelle Informationen zur Akkordeon-Komponente finden Sie in der technischen Dokumentation auf [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/accordion/v1/accordion). Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Entwicklerdokumentation für Kernkomponenten](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Sie können das Akkordeon-Erlebnis für Besuchende im Dialogfeld „Konfigurieren“ einfach anpassen. Sie können auch Akkordeon-Elemente, Bedienfelder, Verhalten und Erscheinungsbild problemlos für ein nahtloses Benutzererlebnis definieren.

### Registerkarte „Allgemein“ {#basic-tab}

![Registerkarte „Allgemein“](/help/adaptive-forms/assets/acc-basic.png)

- **Name**: Sie können eine Formularkomponente sowohl im Formular als auch im Regeleditor durch ihren eindeutigen Namen identifizieren. Der Name darf keine Leerzeichen oder Sonderzeichen enthalten.

- **Titel**: Mit dem Titel können Sie eine Komponente in einem Formular leicht identifizieren. Standardmäßig wird der Titel oberhalb der Komponente angezeigt. Wenn Sie keinen Titel hinzufügen, wird der Name der Komponente anstelle des Titeltexts angezeigt.

- **Rich-Text für Titel zulassen**: Diese Funktionen ermöglichen es Benutzenden, einfache Texttitel zu formatieren, die Funktionen wie fett, kursiv, unterstrichener Text, verschiedene Schriftarten, Schriftgrößen, Farben und zusätzliche Optionen enthalten und so die visuelle Darstellung und Anpassung zu verbessern. Sie bietet mehr Flexibilität und kreative Kontrolle bei der Hervorhebung von Titeln in Dokumenten, Websites oder Anwendungen.\
  Durch Aktivieren des Kontrollkästchens **Rich-Text für Titel zulassen** werden Formatierungsoptionen sichtbar, mit denen Sie den Titel der Komponente gestalten können. Um auf alle verfügbaren Formatierungsoptionen zuzugreifen, können Sie auf die Registerkarte ![Vollbildsymbol](/help/adaptive-forms/assets/fullscreen-icon.png) klicken.

  ![Rich-Text-Unterstützung](/help/adaptive-forms/assets/richtext-support-title.png)

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

<!--  **Layout** - You can have either a fixed layout (Simple) or a flexible layout (Responsive Grid) for your wizard. The Simple layout keeps everything fixed in the place, while the Responsive Grid allows you to adjust the position of components to suit your needs. For example, use Responsive Grid to align "First Name", "Middle Name" and "Last Name" in a form in a single row. -->

- **Bindungsreferenz**: Eine Bindungsreferenz ist ein Verweis auf ein Datenelement, das in einer externen Datenquelle gespeichert ist und in einem Formular verwendet wird. Sie können mit dem Bindungsverweis Daten dynamisch an Formularfelder binden, sodass das Formular die aktuellsten Daten aus der Datenquelle anzeigen kann. Beispielsweise kann ein Bindungsverweis verwendet werden, um den Namen und die Adresse von Kundinnen und Kunden in einem Formular anzuzeigen, basierend auf der im Formular eingegebenen Kunden-ID. Der Bindungsverweis kann auch verwendet werden, um die Datenquelle mit den im Formular eingegebenen Daten zu aktualisieren. Auf diese Weise können Sie mit AEM Forms Formulare erstellen, die mit externen Datenquellen interagieren und so eine nahtlose Benutzererfahrung bei der Datenerfassung und Datenverwaltung bieten.

- **Komponente ausblenden**: Wählen Sie diese Option, um die Komponente aus dem Formular auszublenden. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor. Dies ist nützlich, wenn Sie Informationen speichern müssen, die Benutzende nicht sehen oder direkt ändern müssen.

- **Komponente deaktivieren**: Wählen Sie die Option zum Deaktivieren der Komponente aus. Die deaktivierte Komponente ist nicht aktiv und Endbenutzende können sie nicht bearbeiten. Benutzende können den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor.

- **Schreibgeschützt**: Wählen Sie die Option aus, um die Komponente nicht bearbeitbar zu machen. Benutzende können den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor.

### Akkordeon wiederholen {#repeat-accordion}

![Akkordeon wiederholen](/help/adaptive-forms/assets/repeat-accordion.png)

Sie können die Wiederholungsoptionen verwenden, um Akkordeon-Bedienfelder und die untergeordneten Komponenten zu duplizieren, eine minimale und maximale Wiederholungsanzahl zu definieren und die Replikation ähnlicher Abschnitte innerhalb eines Formulars zu erleichtern. Bei der Interaktion mit der Akkordeon-Komponente und dem Zugriff auf ihre Einstellungen werden die folgenden Optionen angezeigt:

- **Akkordeon wiederholbar machen**: Eine Umschalter-Funktion, mit der Benutzer die Wiederholungsfunktion aktivieren oder deaktivieren können.
- **Mindestwiederholungen**: Legt fest, wie oft das Akkordeon-Bedienfeld mindestens wiederholt werden kann. Der Wert null zeigt an, dass das Akkordeon-Bedienfeld nicht wiederholt wird. Der Standardwert ist null.
- **Maximale Wiederholungen**: Legt fest, wie oft das Akkordeon-Bedienfeld maximal wiederholt werden kann. Standardmäßig ist dieser Wert unbegrenzt.

Um wiederholbare Abschnitte innerhalb des Akkordeons effektiv zu verwalten, folgen Sie den Schritten, die im Artikel [Erstellen von Formularen mit wiederholbaren Abschnitten](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/create-forms-repeatable-sections.html?lang=de) beschrieben sind.

### Registerkarte „Elemente“ {#items-tab}

![Registerkarte „Elemente“](/help/adaptive-forms/assets/acc-items.png)

Mit der Hinzufügen-Schaltfläche können Sie eine Komponente auswählen, die als Bedienfeld im Fenster „Komponentenauswahl“ hinzugefügt werden soll. Nach dem Hinzufügen der Komponente werden die folgenden Optionen angezeigt:

- **Symbol**: Das Symbol identifiziert die Komponente des Bedienfelds in der Liste. Sie können den Mauszeiger über das Symbol bewegen, um den vollständigen Komponentennamen als QuickInfo anzuzeigen.
- **Beschreibung**: Die Beschreibung, die als Text des Bedienfelds verwendet wird. Standardmäßig wird der Name der Komponente für das Bedienfeld ausgewählt.
- **Entfernen**: Tippen oder klicken Sie, um das Bedienfeld aus der Akkordeon-Komponente zu löschen.
- **Neu anordnen**: Tippen oder klicken und ziehen Sie, um die Reihenfolge der Bedienfelder neu anzuordnen.

### Registerkarte „Hilfe-Inhalt“ {#help-content}

![Registerkarte „Hilfe-Inhalt“](/help/adaptive-forms/assets/acc-helpcontent.png)

- **Kurzbeschreibung**: Eine Kurzbeschreibung ist eine kurze Erklärung, die zusätzliche Informationen oder Klarstellungen über den Zweck eines Formularfelds bietet. Es hilft Benutzenden zu verstehen, welcher Datentyp in das Feld eingegeben werden soll, und kann Richtlinien oder Beispiele bereitstellen, um sicherzustellen, dass die eingegebenen Informationen gültig sind und die gewünschten Kriterien erfüllen. Standardmäßig bleiben kurze Beschreibungen ausgeblendet. Aktivieren Sie die Option **Kurzbeschreibung immer anzeigen**, um sie unterhalb der Komponente anzuzeigen.

- **Kurzbeschreibung immer anzeigen**: Aktivieren Sie diese Option, um die Kurzbeschreibung unterhalb der Komponente anzuzeigen.

- **Hilfetext**: Hilfetext bezieht sich auf zusätzliche Informationen oder Anleitungen, die den Benutzenden bereitgestellt werden, um sie beim korrekten Ausfüllen eines Formularfelds zu unterstützen. Er erscheint, wenn Benutzende auf das Hilfesymbol (i) neben der Komponente klicken. Hilfetext enthält detailliertere Informationen als die Beschriftung oder der Platzhaltertext eines Formularfelds und soll den Benutzenden dabei helfen, die Anforderungen oder Einschränkungen des Felds zu verstehen. Er kann auch Vorschläge oder Beispiele anbieten, um das Ausfüllen des Formulars einfacher und genauer zu gestalten.

### Registerkarte „Barrierefreiheit“ {#accessibility}

![Registerkarte „Barrierefreiheit“](/help/adaptive-forms/assets/acc-accessisbilty.png)

Auf der Registerkarte **„Barrierefreiheit“** werden Werte für [ARIA-Barrierefreiheitsbeschriftungen](https://www.w3.org/WAI/standards-guidelines/aria/) für die Komponente festgelegt. Es stehen verschiedene Optionen zur Verfügung für die Verwendung des Textes für die Bildschirmlesehilfe:

- **Text für Bildschirmlesehilfen**: Text für Bildschirmlesehilfen bezieht sich auf zusätzlichen Text, der speziell für Hilfstechnologien wie Bildschirmlesehilfen vorgesehen ist, die von Personen mit einer Sehschwäche verwendet werden. Dieser Text enthält eine Audiobeschreibung des Zwecks des Formularfelds und kann Informationen über den Titel, die Beschreibung, den Namen und alle relevanten Nachrichten (benutzerdefinierten Text) des Felds enthalten. Der Text der Bildschirmlesehilfe hilft sicherzustellen, dass das Formular allen Benutzenden zugänglich ist, auch Personen mit Sehschwäche, und bietet ihnen ein umfassendes Verständnis des Formularfelds und seiner Anforderungen.

   - **Benutzerdefinierter Text**: Wählen Sie diese Option aus, um den benutzerdefinierten Text für ARIA-Barrierefreiheitsbeschriftungen zu verwenden. Wenn Sie diese Option auswählen, wird das Benutzerdefinierter Dialogfeld „Text“ angezeigt. Sie können relevante Informationen im Benutzerdefinierter Dialogfeld „Text“ hinzufügen.
   - **Beschreibung**: Wählen Sie diese Option aus, um die Beschreibung für ARIA-Barrierefreiheitsbeschriftungen zu verwenden.
   - **Titel**: Wählen Sie diese Option aus, um den Titel für ARIA-Barrierefreiheitsbeschriftungen zu verwenden.
   - **Name**: Wählen Sie diese Option aus, um den Namen für ARIA-Barrierefreiheitsbeschriftungen zu verwenden.
   - **Keine**: Wählen Sie diese Option aus, wenn Sie keine ARIA-Barrierefreiheitsbezeichnungen hinzufügen möchten.

<!--

### Properties Tab {#properties-tab}

![Properties tab of the edit dialog of the Accordion Component](/help/assets/accordion-edit-properties.png)

*   **Single item expansion** - When selected, this option forces a single accordion item to be expanded at a time. Expanding one item will then collapse all others.
*   **Expanded items** - This option defines the items that are expanded by default when the page is loaded.
    * When **Single item expansion** is selected, one panel must be selected. By default the first panel is selected.
    * When **Single item expansion** is not selected, this option is a multi-select and is optional.
*   **ID** - This option allows to control the unique identifier of the component in the HTML and in the [Data Layer](/help/developing/data-layer/overview.md).
    * If left blank, a unique ID is automatically generated for you and can be found by inspecting the resulting page.
    * If an ID is specified, it is the responsibility of the author to make sure that it is unique.
    * Changing the ID can have an impact on CSS, JS and Data Layer tracking.

## Select Panel Popover {#select-panel-popover}

The **Select Panel** option (![Select panel icon](/help/assets/select-panel-icon.png)) on the component toolbar enables content authors to modify the panels in an accordion with ease. By selecting this option, the author can switch to a different panel for editing and rearrange the order of the panels in the accordion. The configured panels will be displayed in a drop-down menu for the author to choose from. This feature optimizes the editing process and makes it user-friendly for content authors.

![Select panel popover](/help/assets/select-panel-popover.png)


* The panels are displayed in a numbered list, reflecting the assigned arrangement.
* Each panel is listed with its component type in bold, followed by a brief description in lighter font.
* By clicking or tapping on a panel in the drop-down, you can easily switch the view in the editor to that specific panel.
* To rearrange the panels, simply use the drag handles to move them into the desired order. -->

## Dialogfeld „Design“ {#design-dialog}

Im Dialogfeld „Design“ können Vorlagenerstellende steuern, wie Elemente standardmäßig angezeigt werden. Für die Akkordeon-Komponente in adaptiven Formularen können Sie Folgendes festlegen:

- Der Typ der zulässigen und als Standard festgelegten HTML-Überschriftenelemente (z. B. H1, H2, H3, usw.)
- Kernkomponenten, die Sie mit dem adaptiven Formular-Editor Akkordeon hinzufügen können
- Einfache Namen für Stile (CSS-Klassen), die Sie im Dialogfeld „Eigenschaften“ der Akkordeon-Komponente im adaptiven Formular-Editor anwenden können.

Dadurch wird das Erstellen und Anpassen von Formularen einfacher und effizienter.

### Registerkarte „Eigenschaften“ {#properties-tab-design}

Auf der Registerkarte „Eigenschaften“ können Vorlagenautorinnen und -autoren standardmäßige und zulässige HTML-Überschriftenelemente für Formularautorinnen und -autoren festlegen:

![Registerkarte „Eigenschaften“ im Dialogfeld „Design“](/help//adaptive-forms/assets/accordion-design-properties.png)

- **Zulässige Überschriftenelemente**: Dropdown-Liste mit mehreren Optionen, über die Vorlagenautorinnen und -autoren auswählen können, welche Überschriftenelemente der Formularautor für das Akkordeon verwenden kann.

- **Standardüberschriftenelement**: Eine Dropdown-Liste legt das standardmäßige Überschriftenelement für die Akkordeon-Komponente fest.

### Registerkarte „Zugelassene Komponenten“ {#allowed-components-tab}

![Registerkarte „Zugelassene Komponenten“ des Dialogfelds „Design“](/help//adaptive-forms/assets/accordion-allowed-components.png)

Die **Zugelassene Komponenten**-Registerkarte ermöglicht es dem Vorlagen-Editor, die Komponenten festzulegen, die den Bedienfeldern in der Akkordeon-Komponente im adaptiven Formular-Editor als Elemente hinzugefügt werden können.

### Registerkarte „Stile“ {#styles-tab}

![Registerkarte „Stil“ des Dialogfelds „Design“](/help/adaptive-forms/assets/accordion-styles-tab.png)

Sie können das Dialogfeld „Design“ zum Definieren und Verwalten von CSS-Stilen für eine Komponente verwenden. Die Akkordeon-Kernkomponente in adaptive Formularen unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).

- **Standard-CSS-Klassen**: Sie können eine standardmäßige CSS-Klasse für die Akkordeon-Komponente bereitstellen.

- **Zulässige Stile**: Sie können Stile definieren, indem Sie einen Namen und die CSS-Klasse angeben, die den Stil darstellen. Sie können beispielsweise einen Stil mit dem Namen „Fettschrift“ erstellen und die CSS-Klasse „Schriftbreite: Fett“ bereitstellen. Sie können diese Stile bei einem adaptiven Formular im adaptiven Formular-Editor anwenden. Um einen Stil anzuwenden, wählen Sie im Editor für adaptive Formulare die Komponente aus, auf die Sie den Stil anwenden möchten, navigieren Sie zum Eigenschaften-Dialog und wählen Sie den gewünschten Stil aus der Dropdown-Liste **Stile**. Wenn Sie die Stile aktualisieren oder ändern müssen, kehren Sie einfach zum Dialogfeld „Design“ zurück, aktualisieren die Stile auf der Registerkarte „Stile“ und speichern die Änderungen.

### Benutzerdefinierte Eigenschaften

![accordion-custom-properties-tab](/help/adaptive-forms/assets/accordion-custom-properties-tab.png)
Mit der Option „Benutzerdefinierte Eigenschaften“ können Sie mithilfe der Formularvorlage benutzerdefinierte Attribute (Schlüsselwertpaare) mit einer Kernkomponente eines adaptiven Formulars verknüpfen. Die benutzerdefinierten Eigenschaften werden im Eigenschaftenbereich der Headless-Ausgabedarstellung der Komponente angezeigt. So kann ein dynamisches Formularverhalten erzeugt werden, das sich je nach den benutzerdefinierten Attributwerten anpasst. Beispielsweise können Entwickelnde verschiedene Ausgabedarstellungen einer Headless-Formularkomponente für Mobile-, Desktop- oder Web-Plattformen entwerfen und so das Benutzererlebnis auf einer Vielzahl von Geräten erheblich verbessern.

- **Gruppenname**: Sie können einen Namen angeben, um die Gruppe der benutzerdefinierten Eigenschaften zu kennzeichnen. Sie können mehrere Gruppen benutzerdefinierter Eigenschaften hinzufügen, löschen oder neu anordnen. Nach dem Hinzufügen der Gruppe benutzerdefinierter Eigenschaften werden folgende Optionen angezeigt:

   - **Schlüssel-Wert-Paare**: Sie können mehrere Namen und Werte benutzerdefinierter Eigenschaften hinzufügen, indem Sie für jede Gruppe benutzerdefinierter Eigenschaften auf **Hinzufügen** klicken.

   - **Löschen**: Tippen oder klicken Sie auf diese Option, um den Namen und den Wert der benutzerdefinierten Eigenschaft zu löschen.

   - **Neu anordnen**: Ordnen Sie den Namen und Wert der benutzerdefinierten Eigenschaft Antippen oder Klicken und Ziehen neu an.

## Ähnliche Artikel {#related-articles}

{{more-like-this}}

## Siehe auch {#see-also}

{{see-also}}