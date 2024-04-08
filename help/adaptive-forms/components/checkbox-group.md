---
title: Kernkomponente für adaptive Formulare – Kontrollkästchen-Gruppe
description: Verwenden oder Anpassen der Kernkomponente für adaptive Formulare – Kontrollkästchen-Gruppe.
role: Architect, Developer, Admin, User
exl-id: 2ced0223-e664-470b-a400-b6865d3a67c9
source-git-commit: e4274194026c3370b52be17171776847374a86b5
workflow-type: tm+mt
source-wordcount: '1869'
ht-degree: 98%

---

# Kontrollkästchen-Gruppe {#button-component-adaptive-forms-core-component}

Eine Kontrollkästchen-Gruppe in einem adaptiven Formular ist ein Satz verwandter Kontrollkästchen, mit denen Benutzende eine oder mehrere Optionen aus einer Liste auswählen können. Jedes Kontrollkästchen wird durch einen Datenwert (Wert, der zur Verarbeitung von Elementen einer Kontrollkästchen-Gruppe verwendet wird) und einen Anzeigewert (Beschriftung für jedes Kontrollkästchen-Element, die seinen Zweck beschreibt) dargestellt

**Beispiel**

![Beispiel einer Kontrollkästchengruppe](/help/adaptive-forms/assets/checkbox-group.png)

**Dialogfeld „Eigenschaften“**

![Dialogfeld „Eigenschaften der Kontrollkästchengruppe“](/help/adaptive-forms/assets/checkbox-group-properties.png)

In diesem Beispiel wird das Element Optionen verwendet, um die Kontrollkästchen zu gruppieren. Sie können das Element **Text anzeigen** verwenden, um eine Beschriftung für ein Element bereitzustellen und **Datenwert** verwenden, um den Wert anzugeben, der beim Senden des Formulars an den Server gesendet wird.

Jede Kontrollkästchen-Option / -Element verfügt über einen eindeutigen Datenwert und das Attribut „Text anzeigen“. Wenn Benutzende die Kontrollkästchen „Sohn“ und „Tochter“ aktivieren, wird der entsprechende Datenwert beim Senden des Formulars an den Server gesendet. Diese Daten können dann von einem server-seitigen Skript verarbeitet werden, um zu bestimmen, welche Optionen von Benutzenden ausgewählt wurden, und können für verschiedene Aktionen verwendet werden, z. B. zum Aktualisieren anderer Felder im Formular oder zum Senden der Formulardaten an ein server-seitiges Skript zur weiteren Verarbeitung.

Darüber hinaus können Sie die Kontrollkästchen-Gruppe so konfigurieren, dass sie für jede Option unterschiedliche Verarbeitungswerte aufweist. Dies können Sie mithilfe des Regel-Editors für adaptive Formulare festlegen.

## Verwendung {#reasons-to-use-check-box-group}

Es gibt verschiedene Gründe, warum von vorteilhaft ist, eine Kontrollkästchen-Gruppe in ein adaptives Formular aufzunehmen, einschließlich:

- **Mehrfachauswahl**: Benutzende können mit einer Kontrollkästchen-Gruppe mehrere Optionen aus einer Liste auswählen, was in Situationen nützlich sein kann, in denen mehrere Auswahlen zulässig oder erforderlich sind.

- **Benutzererlebnis**: Sie können mit der Kontrollkästchen-Gruppe das Formular benutzerfreundlicher gestalten, indem Sie eine klare und intuitive Möglichkeit für Benutzende bereitstellen, mehrere Optionen auszuwählen.

- **Datenanalyse**: Sie können die Kontrollkästchen-Gruppe verwenden, um Daten aus verschiedenen Quellen zu sammeln und zu analysieren oder sie als Eingabe für die weitere Verarbeitung zu verwenden.

- **Umfragen**: Sie können die Kontrollkästchen-Gruppe in Umfragen verwenden, um mehrere Optionen für eine Frage auszuwählen.

- **Benutzereinstellungen**: Sie können die Kontrollkästchen-Gruppe verwenden, um Benutzereinstellungen für verschiedene Optionen zu erfassen.

- **Datenwert**: Eine Kontrollkästchen-Gruppe kann auch verwendet werden, um Elemente einer Kontrollkästchen-Gruppe zu verarbeiten.

## Version und Kompatibilität {#version-and-compatibility}

Die Kernkomponente „Akkordeon“ für adaptive Formulare wurde im Februar 2023 als Teil der Kernkomponenten 2.0.4 für Cloud Service und der Kernkomponenten 1.1.12 für AEM 6.5.16.0 Forms oder höher veröffentlicht. Hier finden Sie eine Tabelle mit allen unterstützten Versionen, AEM-Kompatibilität und Links zur entsprechenden Dokumentation:

| Komponentenversion | AEM as a Cloud Service | AEM 6.5.16.0 Forms oder höher |
|---|---|---|
| v1 | Kompatibel mit<br>[Version 2.0.4](/help/adaptive-forms/version.md) und höher | Kompatibel mit<br>[Version 1.1.12](/help/adaptive-forms/version.md) und höher (aber nur bis Version 2.0.0). |

Informationen zu Versionen und Freigaben der Kernkomponente finden Sie im Dokument [Kernkomponenten-Versionen](/help/adaptive-forms/version.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technische Details {#technical-details}

Aktuelle Informationen zur Kernkomponente für adaptive Formulare – Kontrollkästchen-Gruppe finden Sie in der technischen Dokumentation auf [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/checkboxgroup/v1/checkboxgroup). Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Entwicklerdokumentation für Kernkomponenten](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Sie können im Dialogfeld „Konfigurieren“ einfach das Kontrollkästchen-Erlebnis für Besuchende anpassen. Sie können auch einfache Kontrollkästchen-Optionen für ein nahtloses Benutzererlebnis definieren.


### Registerkarte „Allgemein“ {#basic-tab}

![Registerkarte „Allgemein“](/help/adaptive-forms/assets/checkbox_basictab.png)

- **Name**: Der Name identifiziert die Komponente eindeutig im Regel-Editor. Sonderzeichen und Leerzeichen sind in den Namensfolgen nicht zulässig.

- **Titel**: Mit dem Titel können Sie eine Komponente in einem Formular leicht identifizieren. Standardmäßig wird der Titel über der Komponente angezeigt. Wenn Sie keinen Titel hinzufügen, wird der Name der Komponente anstelle des Titeltexts angezeigt.

<!-- **Allow Rich Text for Title** - This features enables users to format plain text titles, incorporating features like bold, italic, underlined text, various fonts, font sizes, colors, and additional option to enhance visual presentation and customization. It offers greater flexibility and creative control in making titles stand out within documents, websites, or applications.  
    Upon selecting the checkbox for **Allow Rich Text for Title** , formatting options become visible to style the component's title. To access all available formatting options, you can click on the `Fullscreen` ![Fullscreen icon](/help/adaptive-forms/assets/fullscreen-icon.png) tab.
     
     ![Rich text support](/help/adaptive-forms/assets/richtext-support-title.png) -->

- **Titel ausblenden**: Wählen Sie die Option aus, um den Titel der Komponente auszublenden.

- **Optionen** - Sie können Datenwerte hinzufügen und Textpaare anzeigen, indem Sie die **Hinzufügen** Schaltfläche.\
  Nachdem eine neue Option hinzugefügt wurde, können die folgenden Aktionen ausgeführt werden:
   - **Datenwert**: Mit dieser Option können Sie den zu sendenden Inhalt eingeben, wenn eine Option ausgewählt ist.
   - **Text anzeigen**: Mit dieser Option können Sie den Inhalt eingeben, der in einem adaptiven Formular angezeigt werden soll.
   - **Löschen**: Tippen oder klicken, um die Option eines Kontrollkästchens zu löschen.
   - **Neu anordnen**: Tippen oder klicken und ziehen Sie, um die Reihenfolge der Bedienfelder neu anzuordnen.

<!-- You can also format the options for checkbox group using **Allow Rich Text for Options**. 
  
     ![Rich text support for options](/help/adaptive-forms/assets/richtext-for-options.png)

    Once you select the checkbox for **Allow Rich Text for Options** formatting options become visible to style the component's options. To access all available formatting options, you can click on the `Fullscreen` ![Fullscreen icon](/help/adaptive-forms/assets/fullscreen-icon.png) tab.
     ![Rich text support for options](/help/adaptive-forms/assets/richtextoptions-support.png)

    -->

- **Bindungsverweis**: Bindungsverweis ist ein Verweis auf ein Datenelement, das in einer externen Datenquelle gespeichert ist und in einem Formular verwendet wird. Sie können mit dem Bindungsverweis Daten dynamisch an Formularfelder binden, sodass das Formular die aktuellsten Daten aus der Datenquelle anzeigen kann. Beispielsweise kann ein Bindungsverweis verwendet werden, um den Namen und die Adresse von Kundinnen und Kunden in einem Formular anzuzeigen, basierend auf der im Formular eingegebenen Kunden-ID. Der Bindungsverweis kann auch verwendet werden, um die Datenquelle mit den im Formular eingegebenen Daten zu aktualisieren. Auf diese Weise können Sie mit AEM Forms Formulare erstellen, die mit externen Datenquellen interagieren und so eine nahtlose Benutzererfahrung bei der Datenerfassung und Datenverwaltung bieten.

- **Als ungebundenes Formularelement markieren**: Mit dieser Option können Sie Formularfelder konfigurieren, die mit keinem Schema verbunden sind. Mit dieser Option können Sie Daten speichern, ohne die Datenquelle zu aktualisieren. Außerdem können Sie damit Daten auf eine benutzerdefinierte Art und Weise verarbeiten, getrennt von der standardmäßigen Datenbankintegration.

- **Datentyp des gesendeten Werts**: Diese Option gibt den Datentyp des Werts an, der bei Auswahl einer Option gesendet wird. Wenn der **Datentyp des gesendeten Werts** auf `Number` eingestellt ist und Sie auf der Registerkarte **Optionen** Zeichenfolgendaten zu **Datenwert** hinzufügen, zeigt der Bildschirm die Fehlermeldung `Value type mismatch`.

- **Anzeigeoptionen**: Diese Option wird verwendet, um die visuelle Ausrichtung von Kontrollkästchen in einem adaptiven Formular festzulegen. Folgende zwei Optionen werden unterstützt:
   - **Horizontal**: Wenn diese Option aktiviert ist, werden Kontrollkästchen in einem adaptiven Formular von links nach rechts angezeigt.
   - **Vertikal**: Wenn diese Option ausgewählt ist, werden Kontrollkästchen in einem adaptiven Formular von oben nach unten angezeigt.

- **Standardoptionen**: Sie können mit dieser Option vorab ausgewählte Standardwerte hinzufügen, wenn das Formular lädt. Verwenden Sie das Symbol „Löschen“, um die hinzugefügten Optionen zu entfernen. Wenn der **Datentyp des gesendeten Werts** auf `Number` gesetzt ist und Sie Zeichenfolgendaten zu **Standardoptionen** hinzufügen, zeigt der Bildschirm die Fehlermeldung `Value type mismatch`.
- **Komponente ausblenden**: Wählen Sie die Option, um die Komponente aus dem Formular auszublenden. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor. Dies ist nützlich, wenn Sie Informationen speichern müssen, die Benutzende nicht sehen oder direkt ändern müssen.
- **Komponente deaktivieren**: Wählen Sie die Option zum Deaktivieren der Komponente aus. Die deaktivierte Komponente ist nicht aktiv und Endbenutzende können sie nicht bearbeiten. Benutzende können den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor.
- **Schreibgeschützt**: Wählen Sie die Option aus, um die Komponente nicht bearbeitbar zu machen. Benutzende können den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor.

### Registerkarte „Validierung“ {#validation-tab}

![Registerkarte „Validierung“](/help/adaptive-forms/assets/checkbox_validationtab.png)

- **Erforderlich**: Wählen Sie diese Option, wenn Sie die Komponente in einem adaptiven Formular anzeigen möchten. Nachdem Sie die Option ausgewählt haben, müssen Sie eine Auswahl treffen, bevor Sie mit der Formularübermittlung fortfahren. Wenn diese Option aktiviert ist, kann die Option **Komponente ausblenden** oder **Komponente deaktivieren** auf der Registerkarte **Allgemein** nicht ausgewählt werden.

- **Fehlermeldung**: Mit dieser Option können Sie eine Nachricht eingeben, die angezeigt wird, wenn das Kontrollkästchen **Erforderlich** aktiviert ist und das Feld leer bleibt.

- **Meldung zur Skriptvalidierung**: Mit dieser Option können Sie eine Meldung eingeben, die angezeigt werden soll, wenn die Skriptvalidierung fehlschlägt.

### Registerkarte „Hilfe-Inhalt“ {#helpcontent-tab}

![Registerkarte „Hilfe-Inhalt“](/help/adaptive-forms/assets/checkbox_helptab.png)

- **Kurzbeschreibung**: Eine Kurzbeschreibung ist eine kurze Erklärung, die zusätzliche Informationen oder Klarstellungen über den Zweck eines Formularfelds bietet. Es hilft Benutzenden zu verstehen, welcher Datentyp in das Feld eingegeben werden soll, und kann Richtlinien oder Beispiele bereitstellen, um sicherzustellen, dass die eingegebenen Informationen gültig sind und die gewünschten Kriterien erfüllen. Standardmäßig bleiben kurze Beschreibungen ausgeblendet. Aktivieren Sie die Option **Kurzbeschreibung immer anzeigen**, um sie unterhalb der Komponente anzuzeigen.

- **Kurzbeschreibung immer anzeigen**: Aktivieren Sie diese Option, um die Kurzbeschreibung unterhalb der Komponente anzuzeigen.

- **Hilfetext**: Hilfetext bezieht sich auf zusätzliche Informationen oder Anleitungen, die den Benutzenden bereitgestellt werden, um sie beim korrekten Ausfüllen eines Formularfelds zu unterstützen. Er erscheint, wenn Benutzende auf das Hilfesymbol (i) neben der Komponente klicken. Hilfetext enthält detailliertere Informationen als die Beschriftung oder der Platzhaltertext eines Formularfelds und soll den Benutzenden dabei helfen, die Anforderungen oder Einschränkungen des Felds zu verstehen. Er kann auch Vorschläge oder Beispiele anbieten, um das Ausfüllen des Formulars einfacher und genauer zu gestalten.

### Registerkarte „Barrierefreiheit“ {#accessibility-tab}

![Registerkarte „Barrierefreiheit“](/help/adaptive-forms/assets/checkbox_accessibility.png)

**Text für Bildschirmlesehilfen** – Das ist zusätzlicher Text, der von Hilfstechnologien wie etwa Bildschirmlesehilfen für sehbehinderte Personen vorgelesen wird. Dieser Text enthält eine Audiobeschreibung des Zwecks des Formularfelds und kann Informationen über den Titel, die Beschreibung, den Namen und alle relevanten Nachrichten (benutzerdefinierten Text) des Felds enthalten. Der Text der Bildschirmlesehilfe hilft sicherzustellen, dass das Formular allen Benutzenden zugänglich ist, auch Personen mit Sehschwäche, und bietet ihnen ein umfassendes Verständnis des Formularfelds und seiner Anforderungen.

## Dialogfeld „Design“ {#design-dialog}

Verwenden Sie das Dialogfeld „Design“, um CSS-Stile für die Komponente der Kontrollkästchen-Gruppen zu definieren und zu verwalten.

### Registerkarte „Stile“ {#styles-tab}

Die Kernkomponente für adaptive Formulare – Kontrollkästchen-Gruppe unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).

![Dialogfeld „Design“](/help/adaptive-forms/assets/checkbox-style.png)

- **Standard-CSS-Klassen**: Sie können eine standardmäßige CSS-Klasse für die Kernkomponente für adaptive Formulare – Kontrollkästchen-Gruppe bereitstellen.

- **Zulässige Stile**: Sie können Stile definieren, indem Sie einen Namen und die CSS-Klasse angeben, die den Stil darstellen. Sie können beispielsweise einen Stil mit dem Namen „Fettschrift“ erstellen und die CSS-Klasse „Schriftbreite: Fett“ bereitstellen. Sie können diese Stile bei einem adaptiven Formular im adaptiven Formular-Editor anwenden. Um einen Stil anzuwenden, wählen Sie im Editor für adaptive Formulare die Komponente aus, auf die Sie den Stil anwenden möchten, navigieren Sie zum Eigenschaften-Dialog und wählen Sie den gewünschten Stil aus der Dropdown-Liste **Stile**. Wenn Sie die Stile aktualisieren oder ändern müssen, kehren Sie einfach zum Dialogfeld „Design“ zurück, aktualisieren die Stile auf der Registerkarte „Stile“ und speichern die Änderungen.

### Benutzerdefinierte Eigenschaften

![Dialogfeld „Benutzerdefinierte Eigenschaften“](/help/adaptive-forms/assets/checkbox-customproperties.png)

Mit der Option „Benutzerdefinierte Eigenschaften“ können Sie mithilfe der Formularvorlage benutzerdefinierte Attribute (Schlüsselwertpaare) mit einer Kernkomponente eines adaptiven Formulars verknüpfen. Die benutzerdefinierten Eigenschaften werden im Eigenschaftenbereich der Headless-Ausgabedarstellung der Komponente angezeigt. So kann ein dynamisches Formularverhalten erzeugt werden, das sich je nach den benutzerdefinierten Attributwerten anpasst. Beispielsweise können Entwickelnde verschiedene Ausgabedarstellungen einer Headless-Formularkomponente für Mobile-, Desktop- oder Web-Plattformen entwerfen und so das Benutzererlebnis auf einer Vielzahl von Geräten erheblich verbessern.

- **Gruppenname**: Sie können einen Namen angeben, um die Gruppe der benutzerdefinierten Eigenschaften zu kennzeichnen. Sie können mehrere Gruppen benutzerdefinierter Eigenschaften hinzufügen, löschen oder neu anordnen. Nach dem Hinzufügen der Gruppe benutzerdefinierter Eigenschaften werden folgende Optionen angezeigt:

   - **Schlüssel-Wert-Paare**: Sie können mehrere Namen und Werte benutzerdefinierter Eigenschaften hinzufügen, indem Sie für jede Gruppe benutzerdefinierter Eigenschaften auf **Hinzufügen** klicken.

   - **Löschen**: Tippen oder klicken Sie auf diese Option, um den Namen und den Wert der benutzerdefinierten Eigenschaft zu löschen.

   - **Neu anordnen**: Ordnen Sie den Namen und Wert der benutzerdefinierten Eigenschaft Antippen oder Klicken und Ziehen neu an.

## Ähnliche Artikel {#related-articles}

{{more-like-this}})

## Siehe auch {#see-also}

{{see-also}}
