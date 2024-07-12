---
title: Kernkomponente „Bedienfeld-Container“ für adaptive Formulare
description: Verwenden oder Anpassen der Kernkomponente „Bedienfeld-Container“ für adaptive Formulare.
role: Architect, Developer, Admin, User
exl-id: 104836fe-8325-47de-978d-1ff2d6a9dd15
source-git-commit: 4c510b8fe59f4be6e1b329ee4257ab1b780fbf22
workflow-type: tm+mt
source-wordcount: '2225'
ht-degree: 100%

---

# Bedienfeld-Komponente{#panel-container-adaptive-forms-core-component}

In einem adaptiven Formular ist ein Bedienfeld ein Container-Element, das zum Gruppieren verwandter Formularelemente verwendet werden kann. So können Sie verschiedene Formularelemente logisch und sinnvoll gruppieren und organisieren. Dies kann die Gesamtstruktur und Lesbarkeit des Formulars verbessern, sodass Benutzende es einfacher verstehen und leichter darin navigieren können.

Sie können Bedienfelder auch verwenden, um ausblendbare Abschnitte zu erstellen. Damit können komplexe oder weniger häufig verwendete Formularfelder ausgeblendet werden, sodass das Formular übersichtlich bleibt und leicht zu verwenden ist. Sie können auch andere Komponenten wie Text, Kontrollkästchen und Schaltflächen einbeziehen.

Sie können auch verschiedene regelbasierte Aktionen festlegen, z. B. ein Formular senden, eine Website öffnen, Komponenten ein-/ausblenden oder eine Instanz eines Bedienfelds hinzufügen.

**Beispiel**

![Beispiel](/help/adaptive-forms/assets/panel-container.png)

## Verwendung {#reasons-to-use-panel-container}

Es gibt verschiedene Gründe für die Verwendung eines Bedienfelds in einem Formular, darunter:

- **Organisieren von Formularelementen**: Sie können ein Bedienfeld verwenden, um verwandte Formularelemente zusammenzufassen, sodass das Formular für Benutzende übersichtlicher und leichter zu navigieren ist.

- **Verbessern der Formularstruktur**: Sie können durch die Gruppierung von Formularelementen in Bedienfelder die Gesamtstruktur und Lesbarkeit des Formulars verbessern und es Benutzenden dadurch leichter verständlich machen.

- **Erstellen ausblendbarer Abschnitte**: Sie können Bedienfelder verwenden, um ausblendbare Abschnitte zu erstellen. Diese können für das Ausblenden komplexer oder seltener verwendeter Formularfelder nützlich sein, sodass das Formular übersichtlich bleibt und einfach zu verwenden ist.

- **Verbesserte Benutzerfreundlichkeit**: Sie können durch Verwendung von Bedienfeldern zur Organisation von Formularelementen das Formular benutzerfreundlicher und einfacher gestalten, was dazu führen kann, dass mehr Formulare ausgefüllt werden.

## Version und Kompatibilität {#version-and-compatibility}

Die Kernkomponente „Bedienfeld-Container“ für adaptive Formulare wurde im Februar 2023 als Teil der Kernkomponenten 2.0.4 veröffentlicht. Hier finden Sie eine Tabelle mit allen unterstützten Versionen, Informationen zur AEM-Kompatibilität und Links zur entsprechenden Dokumentation:

|  |  |
|---|---|
| Komponentenversion | AEM as a Cloud Service |
| --- | --- |
| v1 | Kompatibel mit<br>[Version 2.0.4](/help/adaptive-forms/version.md) und höher | Kompatibel | Kompatibel |

Informationen zu Versionen und Freigaben der Kernkomponente finden Sie im Dokument [Kernkomponenten-Versionen](/help/adaptive-forms/version.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technische Details {#technical-details}

Die neuesten Informationen zur Kernkomponente „Bedienfeld-Container“ für adaptive Formulare finden Sie in der technischen Dokumentation auf [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/panelcontainer/v1/panelcontainer). Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Entwicklerdokumentation für Kernkomponenten](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Mit dem Dialogfeld „Konfigurieren“ können Sie Bedienfeld-Container mühelos für Besuchende anpassen. Sie können auch Optionen für Bedienfeld-Container definieren, um das Benutzererlebnis zu verbessern.

### Registerkarte „Allgemein“ {#basic-tab}

![Registerkarte „Allgemein“](/help/adaptive-forms/assets/basic-panel.png)

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

- **Bindungsreferenz**: Eine Bindungsreferenz ist ein Verweis auf ein Datenelement, das in einer externen Datenquelle gespeichert ist und in einem Formular verwendet wird. Sie können mit dem Bindungsverweis Daten dynamisch an Formularfelder binden, sodass das Formular die aktuellsten Daten aus der Datenquelle anzeigen kann. Beispielsweise kann ein Bindungsverweis verwendet werden, um den Namen und die Adresse von Kundinnen und Kunden in einem Formular anzuzeigen, basierend auf der im Formular eingegebenen Kunden-ID. Der Bindungsverweis kann auch verwendet werden, um die Datenquelle mit den im Formular eingegebenen Daten zu aktualisieren. Auf diese Weise können Sie mit AEM Forms Formulare erstellen, die mit externen Datenquellen interagieren und so eine nahtlose Benutzererfahrung bei der Datenerfassung und Datenverwaltung bieten.
- **Komponente ausblenden**: Wählen Sie diese Option, um die Komponente aus dem Formular auszublenden. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor. Dies ist nützlich, wenn Sie Informationen speichern müssen, die Benutzende nicht sehen oder direkt ändern müssen.
- **Komponente deaktivieren**: Wählen Sie die Option zum Deaktivieren der Komponente aus. Die deaktivierte Komponente ist nicht aktiv und Endbenutzende können sie nicht bearbeiten. Benutzende können den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor.
- **Schreibgeschützt**: Wählen Sie die Option aus, um die Komponente nicht bearbeitbar zu machen. Benutzende können den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor.

### Registerkarte „Bedienfeld wiederholen“ {#repeat-panel}

![Registerkarte „Wiederholen“](/help/adaptive-forms/assets/repeat-panel.png)

Sie können die Wiederholungsoptionen verwenden, um den Bedienfeld-Container und seine untergeordneten Komponenten zu duplizieren, eine minimale und maximale Wiederholungsanzahl zu definieren und die Replikation ähnlicher Abschnitte innerhalb eines Formulars zu erleichtern. Bei der Interaktion mit der Bedienfeld-Container-Komponente und dem Zugriff auf ihre Einstellungen werden die folgenden Optionen angezeigt:

- **Bereich wiederholbar machen**: Eine Umschalter-Funktion, mit der Benutzende die Wiederholungsfunktion aktivieren oder deaktivieren können.
- **Mindestwiederholungen**: Legt fest, wie oft der Bedienfeld-Container mindestens wiederholt werden kann. Der Wert null zeigt an, dass das Bedienfeld „Assistent“ nicht wiederholt wird. Der Standardwert ist null.
- **Maximale Wiederholungen**: Legt fest, wie oft der Bedienfeld-Container maximal wiederholt werden kann. Standardmäßig ist dieser Wert unbegrenzt.

Um wiederholbare Abschnitte innerhalb des Bedienfeld-Containers effektiv zu verwalten, folgen Sie den Schritten, die im Artikel [Erstellen von Formularen mit wiederholbaren Abschnitten](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/create-forms-repeatable-sections.html?lang=de) beschrieben sind.

### Registerkarte „Hilfe-Inhalt“ {#help-content}

![Registerkarte „Hilfe-Inhalt“](/help/adaptive-forms/assets/helpcontent-panel.png)

- **Kurzbeschreibung**: Eine Kurzbeschreibung ist eine kurze Erklärung, die zusätzliche Informationen oder Klarstellungen über den Zweck eines Formularfelds bietet. Es hilft Benutzenden zu verstehen, welcher Datentyp in das Feld eingegeben werden soll, und kann Richtlinien oder Beispiele bereitstellen, um sicherzustellen, dass die eingegebenen Informationen gültig sind und die gewünschten Kriterien erfüllen. Standardmäßig bleiben kurze Beschreibungen ausgeblendet. Aktivieren Sie die Option **Kurzbeschreibung immer anzeigen**, um sie unterhalb der Komponente anzuzeigen.

- **Kurzbeschreibung immer anzeigen**: Aktivieren Sie diese Option, um die Kurzbeschreibung unterhalb der Komponente anzuzeigen.

- **Hilfetext**: Hilfetext bezieht sich auf zusätzliche Informationen oder Anleitungen, die den Benutzenden bereitgestellt werden, um sie beim korrekten Ausfüllen eines Formularfelds zu unterstützen. Er erscheint, wenn Benutzende auf das Hilfesymbol (i) neben der Komponente klicken. Hilfetext enthält detailliertere Informationen als die Beschriftung oder der Platzhaltertext eines Formularfelds und soll den Benutzenden dabei helfen, die Anforderungen oder Einschränkungen des Felds zu verstehen. Er kann auch Vorschläge oder Beispiele anbieten, um das Ausfüllen des Formulars einfacher und genauer zu gestalten.

### Registerkarte „Barrierefreiheit“ {#accessibility}

![Registerkarte „Barrierefreiheit“](/help/adaptive-forms/assets/accessibilty-panel.png)


- **Text für Bildschirmlesehilfen** – Das ist zusätzlicher Text, der von Hilfstechnologien wie etwa Bildschirmlesehilfen für sehbehinderte Personen vorgelesen wird. Dieser Text enthält eine Audiobeschreibung des Zwecks des Formularfelds und kann Informationen über den Titel, die Beschreibung, den Namen und alle relevanten Nachrichten (benutzerdefinierten Text) des Felds enthalten. Der Text der Bildschirmlesehilfe hilft sicherzustellen, dass das Formular allen Benutzenden zugänglich ist, auch Personen mit Sehschwäche, und bietet ihnen ein umfassendes Verständnis des Formularfelds und seiner Anforderungen.
   - **Benutzerdefinierter Text**: Wählen Sie diese Option aus, um den benutzerdefinierten Text für ARIA-Barrierefreiheitsbeschriftungen zu verwenden. Wenn Sie diese Option auswählen, wird das Benutzerdefinierter Dialogfeld „Text“ angezeigt. Sie können relevante Informationen im Benutzerdefinierter Dialogfeld „Text“ hinzufügen.
   - **Beschreibung**: Wählen Sie diese Option aus, um die Beschreibung für ARIA-Barrierefreiheitsbeschriftungen zu verwenden.
   - **Titel**: Wählen Sie diese Option aus, um den Titel für ARIA-Barrierefreiheitsbeschriftungen zu verwenden.
   - **Name**: Wählen Sie diese Option aus, um den Namen für ARIA-Barrierefreiheitsbeschriftungen zu verwenden.
   - **Keine**: Wählen Sie diese Option aus, wenn Sie keine ARIA-Barrierefreiheitsbezeichnungen hinzufügen möchten.

- **HTML-Rolle für die Ankündigung durch die Bildschirmlesehilfe** – Die HTML-Rolle ist ein Attribut, mit dem der Zweck eines HTML-Elements für Hilfstechnologien wie Bildschirmlesehilfen spezifiziert wird. Rollenattribute werden verwendet, um für ein Element zusätzlichen Kontext und eine semantische Bedeutung bereitzustellen, wodurch es für Bildschirmlesehilfen einfacher wird, den Inhalt zu interpretieren und ihn Benutzenden mitzuteilen. In AEM Forms kann beispielsweise die Beschriftung eines Formularfelds die Rolle „Beschriftung“ haben und sein Eingabefeld die Rolle „Textfeld“. Dadurch kann die Bildschirmlesehilfe die Beziehung zwischen Beschrfitung und Eingabefeld verstehen und diese Informationen den Benutzenden korrekt mitteilen.

## Dialogfeld „Design“ {#design-dialog}

Verwenden Sie das Dialogfeld „Design“, um CSS-Stile für die Bedienfeld-Komponente zu definieren und zu verwalten.

### Registerkarte „Zugelassene Komponenten“ {#allowed-components-tab}

![Registerkarte „Zugelassene Komponenten“ des Dialogfelds „Design“](/help/adaptive-forms/assets/panel-container-allowed-component.png)

Über die Registerkarte **Zugelassene Komponenten** kann die Person, die die Vorlage bearbeitet, festlegen, welche Komponenten im Editor für adaptive Formulare als Elemente zu den Bedienfeldern in der Komponente hinzugefügt werden können.

### Registerkarte „Standardkomponenten“ {#default-components-tab}

![Registerkarte „Standardkomponenten“ des Dialogfelds „Design“](/help/adaptive-forms/assets/panel-container-default-component.png)

Über die Registerkarte **Standardkomponenten** kann die Person, die die Vorlage bearbeitet, festlegen, welche Komponenten standardmäßig als Elemente der Formular-Container-Komponente im Editor für adaptive Formulare angezeigt werden sollen.

### Registerkarte „Responsive Einstellungen“ {#responsive-tab}

![Registerkarte „Responsive Einstellungen“ des Dialogfelds „Design“](/help/adaptive-forms/assets/panel-container-responsive-style-tab.png)

Über die Registerkarte **Responsive Einstellungen** kann die Person, die die Vorlage bearbeitet, die Anzahl der Rasterspalten der Formular-Container-Komponente im Editor für adaptive Formulare festlegen.

### Registerkarte „Container-Einstellungen“

![Registerkarte „Container-Einstellungen“](/help/adaptive-forms/assets/panel-container-container-settings.png)

- **Layout**: Sie können für Ihren Assistenten entweder ein festes Layout (einfach) oder ein flexibles Layout (responsives Raster) verwenden. Das einfache Layout behält alles fest an der Stelle, während Sie mit dem responsiven Raster die Position der Komponenten an Ihre Bedürfnisse anpassen können. Verwenden Sie beispielsweise das responsive Raster, um „Vorname“, „Mittelname“ und „Nachname“ in einem Formular in einer einzigen Zeile auszurichten.

- **Layout deaktivieren**: Mit dieser Option können Sie die Layout-Auswahl im Dialogfeld „Bearbeiten“ einer Komponente deaktivieren.

- **Hintergrundbild aktivieren**: Mit dieser Option können Sie die Einstellungen des Bedienfelds so konfigurieren, dass die visuelle Darstellung durch einen visuellen Hintergrund verbessert wird.

- **Hintergrundfarbe aktivieren**: Mit dieser Option können Sie die Hintergrundfarbe des Bedienfelds festlegen oder ändern. Diese Funktion wird in der Benutzeroberfläche häufig verwendet, um das Erscheinungsbild der Bedienfelder an eine größere Benutzeroberfläche anzupassen. Wenn Sie die Option **Hintergrundfarbe aktivieren** auswählen, wird die Option **Nur Farbfelder** angezeigt. Mit der Option **Nur Farbfelder** können Sie Farben für Hintergrund, Text und andere visuelle Elemente innerhalb des Bedienfelds mithilfe der Schaltfläche **Hinzufügen** festlegen oder auswählen

### Registerkarte „Stile“ {#styles-tab}

Die Kernkomponente „Dateianhänge“ für adaptive Formulare unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).

![Dialogfeld „Design“](/help/adaptive-forms/assets/panel-container-styles-tab.png)

- **Standard-CSS-Klassen**: Sie können eine standardmäßige CSS-Klasse für die Kernkomponente „Bedienfeld-Container“ für adaptive Formulare bereitstellen.

- **Zulässige Stile**: Sie können Stile definieren, indem Sie den Namen und die CSS-Klasse für den Stil angeben. Sie können beispielsweise einen Stil mit dem Namen „Fettschrift“ erstellen und die CSS-Klasse „Schriftbreite: Fett“ bereitstellen. Sie können diese Stile bei einem adaptiven Formular im adaptiven Formular-Editor anwenden. Um einen Stil anzuwenden, wählen Sie im Editor für adaptive Formulare die Komponente aus, auf die Sie den Stil anwenden möchten, navigieren Sie zum Eigenschaften-Dialog und wählen Sie den gewünschten Stil aus der Dropdown-Liste **Stile**. Wenn Sie die Stile aktualisieren oder ändern müssen, kehren Sie einfach zum Dialogfeld „Design“ zurück, aktualisieren die Stile auf der Registerkarte „Stile“ und speichern die Änderungen.

### Registerkarte „Benutzerdefinierte Eigenschaften“

![Dialogfeld „Benutzerdefinierte Eigenschaften“](/help/adaptive-forms/assets/panel-container-custom-properties.png)

Mit der Option „Benutzerdefinierte Eigenschaften“ können Sie mithilfe der Formularvorlage benutzerdefinierte Attribute (Schlüsselwertpaare) mit einer Kernkomponente eines adaptiven Formulars verknüpfen. Die benutzerdefinierten Eigenschaften werden im Eigenschaftenbereich der Headless-Ausgabedarstellung der Komponente angezeigt. So kann ein dynamisches Formularverhalten erzeugt werden, das sich je nach den benutzerdefinierten Attributwerten anpasst. Beispielsweise können Entwickelnde verschiedene Ausgabedarstellungen einer Headless-Formularkomponente für Mobile-, Desktop- oder Web-Plattformen entwerfen und so das Benutzererlebnis auf einer Vielzahl von Geräten erheblich verbessern.

- **Gruppenname**: Sie können einen Namen angeben, um die Gruppe der benutzerdefinierten Eigenschaften zu kennzeichnen. Sie können mehrere Gruppen benutzerdefinierter Eigenschaften hinzufügen, löschen oder neu anordnen. Nach dem Hinzufügen der Gruppe benutzerdefinierter Eigenschaften werden folgende Optionen angezeigt:

   - **Schlüssel-Wert-Paare**: Sie können mehrere Namen und Werte benutzerdefinierter Eigenschaften hinzufügen, indem Sie für jede Gruppe benutzerdefinierter Eigenschaften auf **Hinzufügen** klicken.

   - **Löschen**: Tippen oder klicken Sie auf diese Option, um den Namen und den Wert der benutzerdefinierten Eigenschaft zu löschen.

   - **Neu anordnen**: Ordnen Sie den Namen und Wert der benutzerdefinierten Eigenschaft Antippen oder Klicken und Ziehen neu an.

<!--

## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html)

-->

## Ähnliche Artikel {#related-articles}

{{more-like-this}}

## Siehe auch {#see-also}

{{see-also}}