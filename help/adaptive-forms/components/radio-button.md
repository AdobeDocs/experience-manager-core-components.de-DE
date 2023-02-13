---
title: Adaptive Forms-Kernkomponente - Optionsfeld
description: Verwenden oder Anpassen der Kernkomponente für das adaptive Forms-Optionsfeld.
role: Architect, Developer, Admin, User
source-git-commit: b378fbd5695f82b8fc9de3a2d53a8387099ae33b
workflow-type: tm+mt
source-wordcount: '1645'
ht-degree: 1%

---


# Optionsschaltfläche {#radio-button-adaptive-forms-core-component}

Ein Optionsfeld in einem adaptiven Formular ist ein Typ eines Eingabeelements, mit dem ein Benutzer eine Option aus einer Gruppe verwandter Optionen auswählen kann. Es wird durch eine kleine kreisförmige Schaltfläche dargestellt, die entweder ausgefüllt oder leer ist, um anzugeben, ob die Option aktiviert ist oder nicht. Wenn ein Benutzer ein Optionsfeld auswählt, werden die anderen in der Gruppe deaktiviert. Optionsfelder werden in der Regel verwendet, wenn mehrere sich gegenseitig ausschließende Optionen vorhanden sind und jeweils nur eine ausgewählt werden kann.

**Beispiel**

![](/help/adaptive-forms/assets/radio-button.png)

**Dialogfeld &quot;Eigenschaften&quot;**

![](/help/adaptive-forms/assets/radio-button-properties.png)

In diesem Beispiel wird das Element Optionen verwendet, um die Optionsfelder zusammenzufassen. Die **Text anzeigen** -Element verwendet wird, um eine Bezeichnung für ein Element bereitzustellen und **Datenwert** wird verwendet, um den Wert anzugeben, der beim Senden des Formulars an den Server gesendet wird.

Jede Optionsfeld-Option verfügt über einen eindeutigen Datenwert und das Attribut Text anzeigen . Wenn ein Benutzer &quot;1-10&quot;auswählt, wird der entsprechende Datenwert beim Senden des Formulars an den Server gesendet. Diese Daten können dann von einem serverseitigen Skript verarbeitet werden, um zu bestimmen, welche Optionen vom Benutzer ausgewählt wurden, und können für verschiedene Aktionen verwendet werden, z. B. zum Aktualisieren anderer Felder im Formular oder zum Senden der Formulardaten an ein serverseitiges Skript zur weiteren Verarbeitung.

Darüber hinaus kann jedes Optionsfeld so konfiguriert werden, dass es für jede Option unterschiedliche Verarbeitungswerte gibt. Dies kann mithilfe des adaptiven Forms-Regeleditors festgelegt werden.

## Verwendung {#reasons-to-use-radio-button}

Es gibt verschiedene Gründe für die Verwendung von Optionsfeldern in einem Formular, darunter:

* **Eingeschränkte Auswahl**: Optionsfelder werden verwendet, um eine Liste vordefinierter Optionen bereitzustellen, aus denen der Benutzer auswählen kann. Es kann jeweils nur eine Option ausgewählt werden. Dies ist nützlich, wenn die Anzahl der Optionen begrenzt ist und sich gegenseitig ausschließt.

* **Repräsentation löschen**: Radiobuttons sind klar und leicht zu verstehen, sodass Benutzer leicht wissen können, was sie auswählen.

* **Konsistenz**: Die Verwendung von Optionsfeldern stellt eine konsistente und standardisierte Methode zur Darstellung von Optionen für Benutzer sicher, wodurch das Verständnis und die Interaktion mit dem Formular erleichtert werden.

* **Einfachere Verwendung**: Radiobuttons sind einfach zu bedienen, insbesondere für Benutzer, die nicht mit Technologie vertraut sind oder nur über eingeschränkte Mobilität verfügen.

## Version und Kompatibilität {#version-and-compatibility}

Die Kernkomponente für das adaptive Forms-Optionsfeld wurde im Februar 2023 als Teil der Kernkomponenten 2.0.4 veröffentlicht. Hier finden Sie eine Tabelle mit allen unterstützten Versionen, AEM Kompatibilität und Links zur entsprechenden Dokumentation:

|  |  |
|---|---|
| Komponentenversion | AEM as a Cloud Service |
| --- | --- |
| v1 | Kompatibel mit<br>[Version 2.0.4](/help/versions.md) und höher | Kompatibel | Kompatibel |

Informationen zu Kernkomponentenversionen und -versionen finden Sie im Abschnitt [Kernkomponenten-Versionen](/help/versions.md) Dokument.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technische Details {#technical-details}

Die neuesten Informationen zur Kernkomponente für das adaptive Forms-Optionsfeld finden Sie in der technischen Dokumentation zu [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/radiobutton/v1/radiobutton). Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie im Abschnitt [Entwicklerdokumentation für Kernkomponenten](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Im Dialogfeld &quot;Konfigurieren&quot;können Sie das Optionsfeld-Erlebnis für Besucher einfach anpassen. Für ein nahtloses Benutzererlebnis können Sie auch problemlos Optionsfeld-Optionen definieren.

![Registerkarte &quot;Allgemein&quot;](/help/adaptive-forms/assets/radiobutton_basictab.png)

* **Name** - Sie können eine Formularkomponente sowohl im Formular als auch im Regeleditor leicht mit ihrem eindeutigen Namen identifizieren, der Name darf jedoch keine Leerzeichen oder Sonderzeichen enthalten.

* **Titel** - Mit dem Titel können Sie eine Komponente in einem Formular leicht identifizieren. Standardmäßig wird der Titel über der Komponente angezeigt. Wenn Sie keinen Titel hinzufügen, wird der Name der Komponente anstelle des Titeltexts angezeigt.

* **Titel ausblenden** - Wählen Sie die Option aus, um den Titel der Komponente auszublenden.

   Im **Optionen** -Registerkarte können Sie Datenwerte hinzufügen und Textpaare anzeigen, indem Sie die **Hinzufügen** Schaltfläche. Nachdem eine neue Option hinzugefügt wurde, können die folgenden Aktionen ausgeführt werden:

   * **Datenwert** - Mit dieser Option können Sie den zu sendenden Inhalt eingeben, wenn eine Option ausgewählt ist.
   * **Text anzeigen** - Mit dieser Option können Sie den Inhalt eingeben, der in einem adaptiven Formular angezeigt werden soll.
   * **Löschen** - Tippen oder klicken Sie, um die Option eines Optionsfelds zu löschen.
   * **Neu anordnen** - Tippen oder klicken und ziehen Sie, um die Reihenfolge der Optionen neu anzuordnen.

* **Bindungsverweis** - Ein Bindungsverweis ist ein Verweis auf ein Datenelement, das in einer externen Datenquelle gespeichert und in einem Formular verwendet wird. Mit der Bindungsreferenz können Sie Daten dynamisch an Formularfelder binden, sodass das Formular die aktuellsten Daten aus der Datenquelle anzeigen kann. Beispielsweise kann eine Bindungsverweis verwendet werden, um den Namen und die Adresse eines Kunden in einem Formular anzuzeigen, basierend auf der im Formular eingegebenen Kundenkennung. Die Bindungsverweis kann auch verwendet werden, um die Datenquelle mit den im Formular eingegebenen Daten zu aktualisieren. Auf diese Weise können Sie mit AEM Forms Formulare erstellen, die mit externen Datenquellen interagieren und so eine nahtlose Benutzererfahrung bei der Datenerfassung und -verwaltung bieten.

* **Datentyp des gesendeten Werts** - Diese Option gibt den Datentyp des Werts an, der gesendet wird, wenn eine Option ausgewählt ist. Wenn die Variable **Datentyp des gesendeten Werts** auf `Number` und fügen Sie Zeichenfolgendaten hinzu **Datenwert** &#x200B; &#x200B; auf der **Optionen** auf, zeigt der Bildschirm ein `Value type mismatch` Fehlermeldung.

* **Standardoptionen** - Mit dieser Option können Sie vorab ausgewählte Standardwerte hinzufügen, wenn das Formular geladen wird. Wenn die Variable **Datentyp des gesendeten Werts** auf `Number` und fügen Sie Zeichenfolgendaten hinzu **Standardoptionen**, zeigt der Bildschirm eine `Value type mismatch` Fehlermeldung.

* **Anzeigeoptionen** - Diese Option wird verwendet, um die visuelle Ausrichtung von Optionsfeldern in einem adaptiven Formular festzulegen. Folgende zwei Optionen werden unterstützt:
   * **Horizontal** - Wenn diese Option aktiviert ist, werden Optionsfelder in einem adaptiven Formular von links nach rechts angezeigt.
   * **Vertikal** - Wenn diese Option aktiviert ist, werden Optionsfelder in einem adaptiven Formular von oben nach unten angezeigt.
* **Komponente ausblenden** - Wählen Sie die Option, um die Komponente aus dem Formular auszublenden. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regeleditor. Dies ist nützlich, wenn Sie Informationen speichern müssen, die vom Benutzer nicht gesehen oder direkt geändert werden müssen.
* **Komponente deaktivieren** - Wählen Sie die Option zum Deaktivieren der Komponente aus. Die deaktivierte Komponente ist vom Endbenutzer nicht aktiv oder kann nicht bearbeitet werden. Der Benutzer kann den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regeleditor.
* **Schreibgeschützt** - Wählen Sie die Option aus, um die Komponente nicht bearbeitbar zu machen. Der Benutzer kann den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regeleditor.

### Registerkarte &quot;Validierung&quot; {#validation-tab}

![Registerkarte &quot;Validierung&quot;](/help/adaptive-forms/assets/radiobutton_validationtab.png)

* **Erforderlich** - Wählen Sie diese Option, wenn Sie die Komponente in einem adaptiven Formular anzeigen möchten. Sie können die **Komponente ausblenden** oder **Komponente deaktivieren**  im **Allgemein** Registerkarte angezeigt, wenn diese Option aktiviert ist.

* **Fehlermeldung** - Mit dieser Option können Sie eine Nachricht eingeben, die angezeigt wird, wenn die **Erforderlich** aktiviert ist und das Formularfeld leer bleibt.

* **Überprüfungsmeldung für Skripten** - Mit dieser Option können Sie eine Meldung eingeben, die angezeigt werden soll, wenn die Skriptvalidierung fehlschlägt.

### Registerkarte &quot;Hilfe-Inhalt&quot; {#helpcontent-tab}

![Registerkarte &quot;Hilfe-Inhalt&quot;](/help/adaptive-forms/assets/radiobutton_helptab.png)

* **Kurzbeschreibung** - Eine kurze Beschreibung ist eine kurze Texterklärung, die zusätzliche Informationen oder Klarstellungen zum Zweck eines bestimmten Formularfelds bietet. Es hilft dem Benutzer zu verstehen, welcher Datentyp in das Feld eingegeben werden soll, und kann Richtlinien oder Beispiele bereitstellen, um sicherzustellen, dass die eingegebenen Informationen gültig sind und die gewünschten Kriterien erfüllen. Standardmäßig bleiben kurze Beschreibungen ausgeblendet. Aktivieren Sie die **Kurzbeschreibung immer anzeigen** -Option, um sie unter der Komponente anzuzeigen.

* **Kurzbeschreibung immer anzeigen** - Aktivieren Sie die Option, um die Kurzbeschreibung unter der Komponente anzuzeigen.

* **Hilfetext** - Hilfetext bezieht sich auf zusätzliche Informationen oder Anleitungen, die dem Benutzer bereitgestellt werden, um ihn beim korrekten Ausfüllen eines Formularfelds zu unterstützen. Er wird angezeigt, wenn der Benutzer auf das Hilfesymbol (i) neben der Komponente klickt. Hilfetext enthält detailliertere Informationen als die Beschriftung oder der Platzhaltertext eines Formularfelds und soll dem Benutzer dabei helfen, die Anforderungen oder Einschränkungen des Felds zu verstehen. Es kann auch Vorschläge oder Beispiele anbieten, um das Ausfüllen des Formulars zu vereinfachen und genauer zu gestalten.

### Registerkarte „Erreichbarkeit“ {#accessibility-tab}

![Registerkarte &quot;Barrierefreiheit&quot;](/help/adaptive-forms/assets/radiobutton_accessibilitytab.png)

* **Text für Bildschirmlesehilfen** - Text für Bildschirmlesehilfen bezieht sich auf zusätzlichen Text, der speziell für Hilfstechnologien wie Bildschirmlesehilfen vorgesehen ist, die von sehbehinderten Personen verwendet werden. Dieser Text enthält eine Audiobeschreibung des Zwecks des Formularfelds und kann Informationen über den Titel, die Beschreibung, den Namen und alle relevanten Nachrichten (benutzerdefinierten Text) des Felds enthalten. Der Text der Bildschirmlesehilfe hilft sicherzustellen, dass das Formular für alle Benutzer zugänglich ist, auch für Benutzer mit Sehbehinderungen, und bietet ihnen ein umfassendes Verständnis des Formularfelds und seiner Anforderungen.


## Dialogfeld „Design“ {#design-dialog}

Das Dialogfeld &quot;Design&quot;wird verwendet, um CSS-Stile für die Optionsfeld-Komponente zu definieren und zu verwalten.


### Registerkarte „Arten“ {#styles-tab}

Das Dialogfeld &quot;Design&quot;wird zum Definieren und Verwalten von CSS-Stilen für eine Komponente verwendet. Die Kernkomponente für das adaptive Forms-Optionsfeld unterstützt die AEM [Stilsystem](/help/get-started/authoring.md#component-styling).

**Standard-CSS-Klassen**: Sie können eine standardmäßige CSS-Klasse für die Kernkomponente &quot;Adaptives Forms-Optionsfeld&quot;bereitstellen.

**Zulässige Stile**: Sie können Stile definieren, indem Sie einen Namen und die CSS-Klasse angeben, die den Stil darstellt. Sie können beispielsweise einen Stil mit dem Namen &quot;fett Text&quot;erstellen und die CSS-Klasse &quot;font-weight: fett&quot;. Sie können diese Stile im adaptiven Forms-Editor verwenden oder auf ein adaptives Formular anwenden. Um einen Stil anzuwenden, wählen Sie im adaptiven Forms-Editor die Komponente aus, auf die Sie den Stil anwenden möchten, navigieren Sie zum Dialogfeld &quot;Eigenschaften&quot;und wählen Sie den gewünschten Stil aus dem **Stile** Dropdown-Liste. Wenn Sie die Stile aktualisieren oder ändern müssen, kehren Sie einfach zum Dialogfeld &quot;Design&quot;zurück, aktualisieren Sie die Stile auf der Registerkarte &quot;Stile&quot;und speichern Sie die Änderungen.

