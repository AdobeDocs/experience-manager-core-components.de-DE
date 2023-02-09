---
title: Adaptive Forms-Kernkomponente - Kontrollkästchengruppe
description: Verwenden oder Anpassen der Kernkomponente "Adaptive Forms Checkbox Group".
role: Architect, Developer, Admin, User
source-git-commit: 0e4fb8454b7ef84eb5b1b73b01c982a2f9c12381
workflow-type: tm+mt
source-wordcount: '1683'
ht-degree: 2%

---


# Kontrollkästchen-Gruppe {#button-component-adaptive-forms-core-component}

Eine Kontrollkästchengruppe in einem adaptiven Formular ist ein Satz verwandter Kontrollkästchen, mit denen Benutzer eine oder mehrere Optionen aus einer Liste auswählen können. Jedes Kontrollkästchen wird durch einen Datenwert (Wert, der zur Verarbeitung von Elementen einer Kontrollkästchengruppe verwendet wird) und einen Anzeigewert (Beschriftung für jedes Kontrollkästchen-Element, das seinen Zweck beschreibt) dargestellt

**Beispiel**

![](/help/adaptive-forms/assets/checkbox-group.png)

**Dialogfeld &quot;Eigenschaften&quot;**

![](/help/adaptive-forms/assets/checkbox-group-properties.png)

In diesem Beispiel wird das Element Optionen verwendet, um die Kontrollkästchen zu gruppieren. Die **Text anzeigen** -Element verwendet wird, um eine Bezeichnung für ein Element bereitzustellen und **Datenwert** wird verwendet, um den Wert anzugeben, der beim Senden des Formulars an den Server gesendet wird.

Jede Kontrollkästchen-Option/jedes Element verfügt über einen eindeutigen Datenwert und das Attribut &quot;Text anzeigen&quot;. Wenn ein Benutzer die Kontrollkästchen &quot;Sohn&quot;und &quot;Tochter&quot;aktiviert, wird der entsprechende Datenwert beim Senden des Formulars an den Server gesendet. Diese Daten können dann von einem serverseitigen Skript verarbeitet werden, um zu bestimmen, welche Optionen vom Benutzer ausgewählt wurden, und können für verschiedene Aktionen verwendet werden, z. B. zum Aktualisieren anderer Felder im Formular oder zum Senden der Formulardaten an ein serverseitiges Skript zur weiteren Verarbeitung.

Darüber hinaus kann die Kontrollkästchengruppe so konfiguriert werden, dass sie für jede Option unterschiedliche Verarbeitungswerte aufweist. Dies kann mithilfe des adaptiven Forms-Regeleditors festgelegt werden.

## Verwendung {#reasons-to-use-check-box-group}

Es gibt verschiedene Gründe, warum es sinnvoll ist, eine Kontrollkästchengruppe in ein adaptives Formular einzuschließen:

* **Mehrfachauswahl**: Mit einer Kontrollkästchengruppe können Benutzer mehrere Optionen aus einer Liste auswählen, was in Situationen nützlich sein kann, in denen mehrere Auswahlen zulässig oder erforderlich sind.

* **Anwendererlebnis**: Mit der Kontrollkästchengruppe kann das Formular benutzerfreundlicher gestaltet werden, indem eine klare und intuitive Möglichkeit für Benutzer bereitgestellt wird, mehrere Optionen auszuwählen.

* **Datenanalyse**: Die Kontrollkästchengruppe kann verwendet werden, um Daten aus verschiedenen Quellen zu sammeln und zu analysieren oder sie als Eingabe für die weitere Verarbeitung zu verwenden.

* **Umfragen**: Die Kontrollkästchengruppe kann in Umfragen verwendet werden, um mehrere Optionen für eine Frage auszuwählen.

* **Benutzereinstellungen**: Die Kontrollkästchengruppe kann verwendet werden, um Benutzereinstellungen für verschiedene Optionen zu erfassen.

* **Datenwert**: Eine Kontrollkästchengruppe kann auch verwendet werden, um Elemente einer Kontrollkästchengruppe zu verarbeiten.

## Version und Kompatibilität {#version-and-compatibility}

Die Kernkomponente &quot;Adaptive Forms Checkbox Group&quot;wurde im Februar 2023 als Teil der Kernkomponenten 2.0.4 veröffentlicht. Hier finden Sie eine Tabelle mit allen unterstützten Versionen, AEM Kompatibilität und Links zur entsprechenden Dokumentation:

| Komponentenversion | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Kompatibel mit<br>[Version 2.0.4](/help/versions.md) und höher | Kompatibel | Kompatibel |

Informationen zu Kernkomponentenversionen und -versionen finden Sie im Abschnitt [Kernkomponenten-Versionen](/help/versions.md) Dokument.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technische Details {#technical-details}

Die neuesten Informationen zur Kernkomponente der adaptiven Forms-Checkbox-Gruppe finden Sie in der technischen Dokumentation zu [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/checkboxgroup/v1/checkboxgroup). Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie im Abschnitt [Entwicklerdokumentation für Kernkomponenten](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Mit dem Dialogfeld &quot;Konfigurieren&quot;können Sie das Kontrollkästchen-Erlebnis für Besucher einfach anpassen. Sie können auch einfache Kontrollkästchenoptionen für ein nahtloses Benutzererlebnis definieren.


### Einfache Registerkarte {#basic-tab}

![Registerkarte &quot;Allgemein&quot;](/help/adaptive-forms/assets/checkbox_basictab.png)

* **Name** - Der Name identifiziert die Komponente eindeutig im Regeleditor. Sonderzeichen und Leerzeichen sind in den Namensfolgen nicht zulässig.

* **Titel** - Mit dem Titel können Sie eine Komponente in einem Formular leicht identifizieren. Standardmäßig wird der Titel über der Komponente angezeigt. Wenn Sie keinen Titel hinzufügen, wird der Name der Komponente anstelle des Titeltexts angezeigt.

* **Titel ausblenden** - Wählen Sie die Option aus, um den Titel der Komponente auszublenden.

* **Optionen** - Sie können Datenwerte hinzufügen und Textpaare anzeigen, indem Sie die **Hinzufügen** Schaltfläche. Nachdem eine neue Option hinzugefügt wurde, können die folgenden Aktionen ausgeführt werden:

   * **Datenwert** - Mit dieser Option können Sie den zu sendenden Inhalt eingeben, wenn eine Option ausgewählt ist.
   * **Text anzeigen** - Mit dieser Option können Sie den Inhalt eingeben, der in einem adaptiven Formular angezeigt werden soll.
   * **Löschen** - Tippen oder klicken Sie, um die Option eines Kontrollkästchens zu löschen.
   * **Neu anordnen** - Tippen oder klicken und ziehen Sie, um die Reihenfolge der Bedienfelder neu anzuordnen.

* **Bindungsverweis** - Ein Bindungsverweis ist ein Verweis auf ein Datenelement, das in einer externen Datenquelle gespeichert und in einem Formular verwendet wird. Mit der Bindungsreferenz können Sie Daten dynamisch an Formularfelder binden, sodass das Formular die aktuellsten Daten aus der Datenquelle anzeigen kann. Beispielsweise kann eine Bindungsverweis verwendet werden, um den Namen und die Adresse eines Kunden in einem Formular anzuzeigen, basierend auf der im Formular eingegebenen Kundenkennung. Die Bindungsverweis kann auch verwendet werden, um die Datenquelle mit den im Formular eingegebenen Daten zu aktualisieren. Auf diese Weise können Sie mit AEM Forms Formulare erstellen, die mit externen Datenquellen interagieren und so eine nahtlose Benutzererfahrung bei der Datenerfassung und -verwaltung bieten.

* **Datentyp des gesendeten Werts** - Diese Option gibt den Datentyp des Werts an, der gesendet wird, wenn eine Option ausgewählt ist. Wenn die Variable **Datentyp des gesendeten Werts** auf `Number` und fügen Sie Zeichenfolgendaten hinzu **Datenwert** &#x200B; &#x200B; auf der **Optionen** auf, zeigt der Bildschirm ein `Value type mismatch` Fehlermeldung.

* **Anzeigeoptionen** - Diese Option wird verwendet, um die visuelle Ausrichtung von Kontrollkästchen in einem adaptiven Formular festzulegen. Folgende zwei Optionen werden unterstützt:
   * **Horizontal** - Wenn diese Option aktiviert ist, werden Kontrollkästchen in einem adaptiven Formular von links nach rechts angezeigt.
   * **Vertikal** - Wenn diese Option ausgewählt ist, werden Kontrollkästchen in einem adaptiven Formular von oben nach unten angezeigt.

* **Standardoptionen** - Mit dieser Option können Sie vorab ausgewählte Standardwerte hinzufügen, wenn das Formular geladen wird. Verwenden Sie das Symbol Löschen , um die hinzugefügten Optionen zu entfernen. Wenn die Variable **Datentyp des gesendeten Werts** auf `Number` und fügen Sie Zeichenfolgendaten hinzu **Standardoptionen**, zeigt der Bildschirm eine `Value type mismatch` Fehlermeldung.
* **Komponente ausblenden** - Wählen Sie die Option, um die Komponente aus dem Formular auszublenden. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regeleditor. Dies ist nützlich, wenn Sie Informationen speichern müssen, die vom Benutzer nicht gesehen oder direkt geändert werden müssen.
* **Komponente deaktivieren** - Wählen Sie die Option zum Deaktivieren der Komponente aus. Die deaktivierte Komponente ist vom Endbenutzer nicht aktiv oder kann nicht bearbeitet werden. Der Benutzer kann den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regeleditor.
* **Schreibgeschützt** - Wählen Sie die Option aus, um die Komponente nicht bearbeitbar zu machen. Der Benutzer kann den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regeleditor.

### Registerkarte &quot;Validierung&quot; {#validation-tab}

![Registerkarte &quot;Validierung&quot;](/help/adaptive-forms/assets/checkbox_validationtab.png)

* **Erforderlich** - Wählen Sie diese Option, wenn Sie die Komponente in einem adaptiven Formular anzeigen möchten. Sie können die **Komponente ausblenden** oder **Komponente deaktivieren**  im **Allgemein** Registerkarte angezeigt, wenn diese Option aktiviert ist.

* **Fehlermeldung** - Mit dieser Option können Sie eine Nachricht eingeben, die angezeigt wird, wenn die **Erforderlich** aktiviert ist und das Formularfeld leer bleibt.

* **Überprüfungsmeldung für Skripten** - Mit dieser Option können Sie eine Meldung eingeben, die angezeigt werden soll, wenn die Skriptvalidierung fehlschlägt.

### Registerkarte &quot;Hilfe-Inhalt&quot; {#helpcontent-tab}

![Registerkarte &quot;Hilfe-Inhalt&quot;](/help/adaptive-forms/assets/checkbox_helptab.png)

* **Kurzbeschreibung** - Eine kurze Beschreibung ist eine kurze Texterklärung, die zusätzliche Informationen oder Klarstellungen zum Zweck eines bestimmten Formularfelds bietet. Es hilft dem Benutzer zu verstehen, welcher Datentyp in das Feld eingegeben werden soll, und kann Richtlinien oder Beispiele bereitstellen, um sicherzustellen, dass die eingegebenen Informationen gültig sind und die gewünschten Kriterien erfüllen. Standardmäßig bleiben kurze Beschreibungen ausgeblendet. Aktivieren Sie die **Kurzbeschreibung immer anzeigen** -Option, um sie unter der Komponente anzuzeigen.

* **Kurzbeschreibung immer anzeigen** - Aktivieren Sie die Option, um die Kurzbeschreibung unter der Komponente anzuzeigen.

* **Hilfetext** - Hilfetext bezieht sich auf zusätzliche Informationen oder Anleitungen, die dem Benutzer bereitgestellt werden, um ihn beim korrekten Ausfüllen eines Formularfelds zu unterstützen. Er wird angezeigt, wenn der Benutzer auf das Hilfesymbol (i) neben der Komponente klickt. Hilfetext enthält detailliertere Informationen als die Beschriftung oder der Platzhaltertext eines Formularfelds und soll dem Benutzer dabei helfen, die Anforderungen oder Einschränkungen des Felds zu verstehen. Es kann auch Vorschläge oder Beispiele anbieten, um das Ausfüllen des Formulars zu vereinfachen und genauer zu gestalten.

### Registerkarte „Erreichbarkeit“ {#accessibility-tab}

![Registerkarte &quot;Barrierefreiheit&quot;](/help/adaptive-forms/assets/checkbox_accessibility.png)

* **Text für Bildschirmlesehilfen** - Text für Bildschirmlesehilfen bezieht sich auf zusätzlichen Text, der speziell für Hilfstechnologien wie Bildschirmlesehilfen vorgesehen ist, die von sehbehinderten Personen verwendet werden. Dieser Text enthält eine Audiobeschreibung des Zwecks des Formularfelds und kann Informationen über den Titel, die Beschreibung, den Namen und alle relevanten Nachrichten (benutzerdefinierten Text) des Felds enthalten. Der Text der Bildschirmlesehilfe hilft sicherzustellen, dass das Formular für alle Benutzer zugänglich ist, auch für Benutzer mit Sehbehinderungen, und bietet ihnen ein umfassendes Verständnis des Formularfelds und seiner Anforderungen.

   Im **Zugänglichkeit** Registerkarte, werden Werte festgelegt für [Barrierefreiheit in ARIA](https://www.w3.org/WAI/standards-guidelines/aria/) Beschriftungen für die Komponente. Für die Verwendung des Textes für die Bildschirmlesehilfe stehen verschiedene Optionen zur Verfügung:

* **Benutzerdefinierter Text**: Wählen Sie diese Option aus, um den benutzerdefinierten Text für ARIA-Barrierefreiheitsbeschriftungen zu verwenden. Wenn Sie diese Option auswählen, wird das Dialogfeld &quot;Benutzerdefinierter Text&quot;angezeigt. Sie können relevante Informationen im Dialogfeld &quot;Benutzerdefinierter Text&quot;hinzufügen.

* **Titel**: Wählen Sie diese Option aus, um den Titel für ARIA-Barrierefreiheitsbeschriftungen zu verwenden.


## Dialogfeld „Design“ {#design-dialog}

Das Dialogfeld &quot;Design&quot;wird verwendet, um CSS-Stile für die Kontrollkästchengruppen-Komponente zu definieren und zu verwalten.

### Registerkarte „Arten“ {#styles-tab}

Die Kernkomponente &quot;Adaptive Forms Checkbox Group&quot;unterstützt die AEM [Stilsystem](/help/get-started/authoring.md#component-styling).

**Standard-CSS-Klassen**: Sie können eine standardmäßige CSS-Klasse für die Kernkomponente &quot;Adaptive Forms Checkbox Group&quot;bereitstellen.

**Zulässige Stile**: Sie können Stile definieren, indem Sie einen Namen und die CSS-Klasse angeben, die den Stil darstellt. Sie können beispielsweise einen Stil mit dem Namen &quot;fett Text&quot;erstellen und die CSS-Klasse &quot;font-weight: fett&quot;. Sie können diese Stile im adaptiven Forms-Editor verwenden oder auf ein adaptives Formular anwenden. Um einen Stil anzuwenden, wählen Sie im adaptiven Forms-Editor die Komponente aus, auf die Sie den Stil anwenden möchten, navigieren Sie zum Dialogfeld &quot;Eigenschaften&quot;und wählen Sie den gewünschten Stil aus dem **Stile** Dropdown-Liste. Wenn Sie die Stile aktualisieren oder ändern müssen, kehren Sie einfach zum Dialogfeld &quot;Design&quot;zurück, aktualisieren Sie die Stile auf der Registerkarte &quot;Stile&quot;und speichern Sie die Änderungen.

