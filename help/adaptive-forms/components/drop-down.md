---
title: Adaptive Forms-Kernkomponente - Dropdown-Liste
description: Verwenden oder Anpassen der Dropdown-Kernkomponente "Adaptive Forms".
role: Architect, Developer, Admin, User
source-git-commit: 1e6460d318f4f9a5dfdcbb81723da01b51b72f3f
workflow-type: tm+mt
source-wordcount: '1673'
ht-degree: 1%

---


# Dropdown-Liste {#drop-down-list-adaptive-forms-core-component}

Über eine Dropdown-Liste in einem adaptiven Formular können Benutzer eine oder mehrere Optionen aus einer Liste vordefinierter Optionen auswählen. Die Optionen können vom Typ String, Number oder Boolean sein. Darüber hinaus kann die Dropdown-Listenkomponente so konfiguriert werden, dass sie unterschiedliche Validierungs- und Standardwerte aufweist.

**Beispiel**
![](/help/adaptive-forms/assets/drop-down-list.png)

## Verwendung {#reasons-to-use-drop-down-list}

Es gibt verschiedene Gründe, warum es sinnvoll ist, eine Dropdown-Liste in ein adaptives Formular einzufügen, darunter:

* **Lange Liste von Optionen**: Dropdown-Listen sind nützlich für Situationen, in denen eine lange Liste von Optionen für ein Feld verfügbar ist. Sie nehmen im Formular weniger Platz ein als eine Liste von Optionsfeldern oder Kontrollkästchen und können für Benutzer weniger überwältigend sein.

* **Konsistenz**: Dropdown-Listen bieten Konsistenz im Design und Layout des Formulars, wodurch die Navigation für Benutzer intuitiver und einfacher wird.

* **Klarheit**: Dropdown-Listen können das Formular klarer und verständlicher machen, indem eine klare und knappe Liste von Optionen bereitgestellt wird.

* **Anwendererlebnis**: Dropdown-Listen können verwendet werden, um das Formular benutzerfreundlicher zu gestalten, indem eine klare und intuitive Möglichkeit zur Auswahl von Optionen bereitgestellt wird.

* **Datenanalyse**: Dropdown-Listen können verwendet werden, um Daten aus verschiedenen Quellen zu sammeln und zu analysieren oder sie als Eingabe für die weitere Verarbeitung zu verwenden.


**Dialogfeld &quot;Eigenschaften&quot;**

![](/help/adaptive-forms/assets/drop-down-list-properties.png)

In diesem Beispiel wird das Element Optionen verwendet, um die Listenelemente zu definieren. Die **Text anzeigen** -Element wird verwendet, um eine Beschriftung für Listenelemente bereitzustellen und **Datenwert** wird verwendet, um den Wert anzugeben, der beim Senden des Formulars an den Server gesendet wird.

Jede Dropdown-Listenoption verfügt über einen eindeutigen Datenwert und das Attribut Text anzeigen . Wenn ein Benutzer die Option &quot;Rot&quot;auswählt, wird der entsprechende Datenwert beim Senden des Formulars an den Server gesendet. Diese Daten können dann von einem serverseitigen Skript verarbeitet werden, um zu bestimmen, welche Optionen vom Benutzer ausgewählt wurden, und können für verschiedene Aktionen verwendet werden, z. B. zum Aktualisieren anderer Felder im Formular oder zum Senden der Formulardaten an ein serverseitiges Skript zur weiteren Verarbeitung.

Darüber hinaus kann die Dropdownliste so konfiguriert werden, dass für jede Option unterschiedliche Verarbeitungswerte verwendet werden. Dies kann mithilfe des adaptiven Forms-Regeleditors festgelegt werden.

## Version und Kompatibilität {#version-and-compatibility}

Die Kernkomponente für die Dropdownliste &quot;Adaptive Forms&quot;wurde im Februar 2023 als Teil der Kernkomponenten 2.0.4 veröffentlicht. Hier finden Sie eine Tabelle mit allen unterstützten Versionen, AEM Kompatibilität und Links zur entsprechenden Dokumentation:

| Komponentenversion | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Kompatibel mit<br>[Version 2.0.4](/help/versions.md) und höher | Kompatibel | Kompatibel |

Informationen zu Kernkomponentenversionen und -versionen finden Sie im Abschnitt [Kernkomponenten-Versionen](/help/versions.md) Dokument.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technische Details {#technical-details}

Die neuesten Informationen zur Dropdown-Liste-Kernkomponente &quot;Adaptive Forms&quot;finden Sie in der technischen Dokumentation zu [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/dropdown/v1/dropdown). Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie im Abschnitt [Entwicklerdokumentation für Kernkomponenten](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Im Dialogfeld &quot;Konfigurieren&quot;können Sie das Erlebnis Ihrer Dropdown-Liste für Besucher einfach anpassen. Für ein nahtloses Benutzererlebnis können Sie auch Dropdown-Listenoptionen definieren.

![Registerkarte &quot;Allgemein&quot;](/help/adaptive-forms/assets/dropdown_basictab.png)

* **Name** - Sie können eine Formularkomponente sowohl im Formular als auch im Regeleditor leicht mit ihrem eindeutigen Namen identifizieren, der Name darf jedoch keine Leerzeichen oder Sonderzeichen enthalten.

* **Titel** - Mit dem Titel können Sie eine Komponente in einem Formular leicht identifizieren. Standardmäßig wird der Titel über der Komponente angezeigt. Wenn Sie keinen Titel hinzufügen, wird der Name der Komponente anstelle des Titeltexts angezeigt.

* **Titel ausblenden** - Wählen Sie die Option aus, um den Titel der Komponente auszublenden.

* **Mehrfachauswahl zulassen** - Wählen Sie diese Option aus, um mehrere Optionen aus einer Dropdown-Liste auszuwählen.

* **Wert speichern unter** - Diese Option gibt den Datentyp des Werts an, der gesendet wird, wenn eine Option ausgewählt ist. Wenn die Variable **Wert speichern unter** auf `Number` und fügen Sie Zeichenfolgendaten hinzu **Datenwert** &#x200B; &#x200B; auf der **Optionen** auf, zeigt der Bildschirm ein `Value type mismatch` Fehlermeldung.

   Im **Optionen** -Registerkarte können Sie Datenwerte hinzufügen und Textpaare anzeigen, indem Sie die **Hinzufügen** Schaltfläche. Nachdem eine neue Option hinzugefügt wurde, werden die folgenden Aktionen ausgeführt:

   * **Datenwert** - Mit dieser Option können Sie den zu sendenden Inhalt eingeben, wenn eine Option ausgewählt ist.
   * **Text anzeigen** - Mit dieser Option können Sie den Inhalt eingeben, der in einem adaptiven Formular angezeigt werden soll.
   * **Löschen** - Tippen oder klicken Sie, um die Option eines Dropdown-Menüs zu löschen.
   * **Neu anordnen** - Tippen oder klicken und ziehen Sie, um die Reihenfolge für die Option eines Dropdown-Menüs neu anzuordnen.

* **Standardoptionen** - Mit dieser Option können Sie Standardwerte hinzufügen. Verwenden Sie das Symbol Löschen , um die hinzugefügte Option zu entfernen. Wenn die Variable **Wert speichern unter** auf `Number` und fügen Sie Zeichenfolgendaten hinzu **Standardoptionen**, zeigt der Bildschirm eine `Value type mismatch` Fehlermeldung.

* **Platzhaltertext** - Platzhaltertext in einer Formularkomponente bezieht sich auf eine kurze Beschriftung oder Eingabeaufforderung, die in einem Eingabefeld angezeigt wird, um den Benutzer darauf hinzuweisen, welcher Informationstyp in dieses Feld eingegeben werden soll. Platzhaltertext verschwindet, wenn der Benutzer mit der Eingabe in das Feld beginnt, und wird wieder angezeigt, wenn das Feld leer bleibt. Es bietet einen visuellen Hinweis für den Benutzer, fungiert jedoch nicht als permanente Bezeichnung oder Wert für das Feld.

* **Bindungsverweis** - Ein Bindungsverweis ist ein Verweis auf ein Datenelement, das in einer externen Datenquelle gespeichert und in einem Formular verwendet wird. Mit der Bindungsreferenz können Sie Daten dynamisch an Formularfelder binden, sodass das Formular die aktuellsten Daten aus der Datenquelle anzeigen kann. Beispielsweise kann eine Bindungsverweis verwendet werden, um den Namen und die Adresse eines Kunden in einem Formular anzuzeigen, basierend auf der im Formular eingegebenen Kundenkennung. Die Bindungsverweis kann auch verwendet werden, um die Datenquelle mit den im Formular eingegebenen Daten zu aktualisieren. Auf diese Weise können Sie mit AEM Forms Formulare erstellen, die mit externen Datenquellen interagieren und so eine nahtlose Benutzererfahrung bei der Datenerfassung und -verwaltung bieten.

* **Komponente ausblenden** - Wählen Sie die Option, um die Komponente aus dem Formular auszublenden. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regeleditor. Dies ist nützlich, wenn Sie Informationen speichern müssen, die vom Benutzer nicht gesehen oder direkt geändert werden müssen.
* **Komponente deaktivieren** - Wählen Sie die Option zum Deaktivieren der Komponente aus. Die deaktivierte Komponente ist vom Endbenutzer nicht aktiv oder kann nicht bearbeitet werden. Der Benutzer kann den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regeleditor.
* **Schreibgeschützt** - Wählen Sie die Option aus, um die Komponente nicht bearbeitbar zu machen. Der Benutzer kann den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regeleditor.

### Registerkarte &quot;Validierung&quot; {#validation-tab}

![Registerkarte &quot;Validierung&quot;](/help/adaptive-forms/assets/dropdown_validationtab.png)

* **Erforderlich** - Wählen Sie diese Option, wenn Sie die Komponente in einem adaptiven Formular anzeigen möchten. Sie können die **Komponente ausblenden** oder **Komponente deaktivieren**  im **Allgemein** Registerkarte angezeigt, wenn diese Option aktiviert ist.

* **Fehlermeldung** - Mit dieser Option können Sie eine Nachricht eingeben, die angezeigt wird, wenn die **Erforderlich** aktiviert ist und das Formularfeld leer bleibt.

* **Überprüfungsmeldung für Skripten** - Mit dieser Option können Sie eine Meldung eingeben, die angezeigt werden soll, wenn die Skriptvalidierung fehlschlägt.

### Registerkarte &quot;Hilfe-Inhalt&quot; {#help-content-tab}

![Registerkarte &quot;Hilfe-Inhalt&quot;](/help/adaptive-forms/assets/dropdown_helptab.png)

* **Kurzbeschreibung** - Eine kurze Beschreibung ist eine kurze Texterklärung, die zusätzliche Informationen oder Klarstellungen zum Zweck eines bestimmten Formularfelds bietet. Es hilft dem Benutzer zu verstehen, welcher Datentyp in das Feld eingegeben werden soll, und kann Richtlinien oder Beispiele bereitstellen, um sicherzustellen, dass die eingegebenen Informationen gültig sind und die gewünschten Kriterien erfüllen. Standardmäßig bleiben kurze Beschreibungen ausgeblendet. Aktivieren Sie die **Kurzbeschreibung immer anzeigen** -Option, um sie unter der Komponente anzuzeigen.

* **Kurzbeschreibung immer anzeigen** - Aktivieren Sie die Option, um die Kurzbeschreibung unter der Komponente anzuzeigen.

* **Hilfetext** - Hilfetext bezieht sich auf zusätzliche Informationen oder Anleitungen, die dem Benutzer bereitgestellt werden, um ihn beim korrekten Ausfüllen eines Formularfelds zu unterstützen. Er wird angezeigt, wenn der Benutzer auf das Hilfesymbol (i) neben der Komponente klickt. Hilfetext enthält detailliertere Informationen als die Beschriftung oder der Platzhaltertext eines Formularfelds und soll dem Benutzer dabei helfen, die Anforderungen oder Einschränkungen des Felds zu verstehen. Es kann auch Vorschläge oder Beispiele anbieten, um das Ausfüllen des Formulars zu vereinfachen und genauer zu gestalten.

### Registerkarte „Erreichbarkeit“ {#accessibility-tab}

![Registerkarte &quot;Barrierefreiheit&quot;](/help/adaptive-forms/assets/dropdown_accessibilitytab.png)

* **Text für Bildschirmlesehilfen** - Text für Bildschirmlesehilfen bezieht sich auf zusätzlichen Text, der speziell für Hilfstechnologien wie Bildschirmlesehilfen vorgesehen ist, die von sehbehinderten Personen verwendet werden. Dieser Text enthält eine Audiobeschreibung des Zwecks des Formularfelds und kann Informationen über den Titel, die Beschreibung, den Namen und alle relevanten Nachrichten (benutzerdefinierten Text) des Felds enthalten. Der Text der Bildschirmlesehilfe hilft sicherzustellen, dass das Formular für alle Benutzer zugänglich ist, auch für Benutzer mit Sehbehinderungen, und bietet ihnen ein umfassendes Verständnis des Formularfelds und seiner Anforderungen.

## Dialogfeld „Design“ {#design-dialog}

Das Dialogfeld &quot;Design&quot;wird verwendet, um CSS-Stile für die Dropdown-Listenkomponente zu definieren und zu verwalten.


### Registerkarte „Arten“ {#styles-tab}

Das Dialogfeld &quot;Design&quot;wird zum Definieren und Verwalten von CSS-Stilen für eine Komponente verwendet. Die Kernkomponente der Dropdown-Liste &quot;Adaptive Forms&quot;unterstützt die AEM [Stilsystem](/help/get-started/authoring.md#component-styling).

**Standard-CSS-Klassen**: Sie können eine standardmäßige CSS-Klasse für die Dropdown-Liste Kernkomponente &quot;Adaptive Forms&quot;bereitstellen.

**Zulässige Stile**: Sie können Stile definieren, indem Sie einen Namen und die CSS-Klasse angeben, die den Stil darstellt. Sie können beispielsweise einen Stil mit dem Namen &quot;fett Text&quot;erstellen und die CSS-Klasse &quot;font-weight: fett&quot;. Sie können diese Stile im adaptiven Forms-Editor verwenden oder auf ein adaptives Formular anwenden. Um einen Stil anzuwenden, wählen Sie im adaptiven Forms-Editor die Komponente aus, auf die Sie den Stil anwenden möchten, navigieren Sie zum Dialogfeld &quot;Eigenschaften&quot;und wählen Sie den gewünschten Stil aus dem **Stile** Dropdown-Liste. Wenn Sie die Stile aktualisieren oder ändern müssen, kehren Sie einfach zum Dialogfeld &quot;Design&quot;zurück, aktualisieren Sie die Stile auf der Registerkarte &quot;Stile&quot;und speichern Sie die Änderungen.


