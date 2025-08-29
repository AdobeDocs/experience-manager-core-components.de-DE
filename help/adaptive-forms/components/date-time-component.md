---
title: Kernkomponente „Datum und Uhrzeit“ der adaptiven Forms
description: Verwenden oder Anpassen der Datums- und Uhrzeitkernkomponente von Adaptive Forms.
role: Architect, Developer, Admin, User
source-git-commit: daeabccaff39e255c111c6af2540ca4d5be0c709
workflow-type: tm+mt
source-wordcount: '1898'
ht-degree: 74%

---


# Datums- und Uhrzeitkomponente

Eine Datums- und Uhrzeitkomponente in einem adaptiven Formular ist ein Benutzeroberflächenelement, mit dem Benutzende sowohl **Datum und Uhrzeit** über eine Kalender- und Uhrenschnittstelle auswählen oder Werte in einem bestimmten Format manuell eingeben können. Es stellt eine genaue, standardisierte Eingabe für Anwendungsfälle sicher, in denen sowohl Datum als auch Uhrzeit wichtig sind.

**Beispiel**

![Beispiel](/help/adaptive-forms/assets/date-time-picker.png)

## Verwendung {#reasons-to-use-date-time-picker}

Es gibt verschiedene Gründe, warum es sinnvoll ist, eine Datums- und Uhrzeitauswahl in ein Formular einzufügen, darunter:

- **Komfort**: Benutzende können einfach sowohl ein Datum als auch eine Uhrzeit auswählen, ohne Werte manuell eingeben zu müssen.
- **Konsistenz**: Erzwingt ein Standardformat für Datums- und Uhrzeiteingaben im gesamten Formular.
- **Verbessertes Benutzererlebnis**: Bietet eine intuitive Benutzeroberfläche mit Kalender- und Zeitauswahl.
- **Ereignisplanung** Nützlich bei der Terminbuchung, in Interviews oder in Formularen zur Besprechungsplanung.
- **Reisen und Reservierungen**: Ermöglicht Benutzern die Auswahl von Ein-/Auscheckdaten und -zeiten.
- **Datengenauigkeit**: Reduziert Eingabefehler im Vergleich zur Eingabe in Freitext.

## Version und Kompatibilität {#version-and-compatibility}

Die Kernkomponente „Datum und Uhrzeit“ von Adaptive Forms wurde im **August 2025** als Teil von **Kernkomponenten 2.24.6** für Cloud Service und höher veröffentlicht.

| Komponentenversion | AEM as a Cloud Service | AEM 6.5.16.0 Forms oder höher |
|---|---|---|
| v1 | Kompatibel mit<br>[Version 2.24.6](/help/adaptive-forms/version.md) und höher | |

Weitere Informationen zu Versionen finden Sie unter [Kernkomponentenversionen](/help/adaptive-forms/version.md).

## Technische Details {#technical-details}

Erhalten Sie die neuesten technischen Details zur Datums- und Uhrzeitkernkomponente von Adaptive Forms auf [GitHub](https://github.com/adobe/aem-core-forms-components). Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie unter [Dokumentation für Kernkomponenten-Entwickler](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Das Dialogfeld „Konfigurieren“ ermöglicht die Anpassung des Datums und der Uhrzeit.

### Registerkarte „Allgemein“ {#basic-tab}

![Registerkarte „Allgemein“](/help/adaptive-forms/assets/datetime_basictab.png)

- **Name**: Durch den Namen wird die Komponente im Regel-Editor eindeutig identifiziert. Sonderzeichen und Leerzeichen sind im Namen nicht zulässig.

- **Titel**: Titel ist eine Zeichenfolge, die in einem adaptiven Formular oberhalb einer Komponente angezeigt wird. Der Titel identifiziert die Komponente eindeutig in der Baumstruktur eines adaptiven Formulars. Wenn Sie keinen Titel hinzufügen, wird der Name der Komponente anstelle des Titeltexts angezeigt.
- **Rich-Text für Titel zulassen**: Diese Funktionen ermöglichen es Benutzenden, einfache Texttitel zu formatieren, die Funktionen wie fett, kursiv, unterstrichener Text, verschiedene Schriftarten, Schriftgrößen, Farben und zusätzliche Optionen enthalten und so die visuelle Darstellung und Anpassung zu verbessern. Sie bietet mehr Flexibilität und kreative Kontrolle bei der Hervorhebung von Titeln in Dokumenten, Websites oder Anwendungen.\
  Durch Aktivieren des Kontrollkästchens **Rich-Text für Titel zulassen** werden Formatierungsoptionen sichtbar, mit denen Sie den Titel der Komponente gestalten können. Um auf alle verfügbaren Formatierungsoptionen zuzugreifen, können Sie auf die Registerkarte ![Vollbildsymbol](/help/adaptive-forms/assets/fullscreen-icon.png) klicken.

  ![Rich-Text-Unterstützung](/help/adaptive-forms/assets/richtext-support-title.png)

- **Titel ausblenden**: Wählen Sie diese Option, um den Titel des Komponententyps in einem adaptiven Formular auszublenden.

- **Platzhaltertext**: Platzhaltertext in einer Formularkomponente ist eine kurze Beschriftung oder Eingabeaufforderung in einem Eingabefeld, um Benutzende darüber zu informieren, welchen Text sie in dieses Feld eingeben sollen. Der Platzhaltertext verschwindet, wenn Benutzende mit der Eingabe in das Feld beginnen, und erscheint wieder, wenn das Feld leer bleibt. Er stellt einen visuellen Hinweis für Benutzende bereit, fungiert jedoch nicht als permanente Beschriftung oder Wert für das Feld.
- **Bindungsreferenz**: Eine Bindungsreferenz ist ein Verweis auf ein Datenelement, das in einer externen Datenquelle gespeichert ist und in einem Formular verwendet wird. Sie können mit dem Bindungsverweis Daten dynamisch an Formularfelder binden, sodass das Formular die aktuellsten Daten aus der Datenquelle anzeigen kann. Beispielsweise kann ein Bindungsverweis verwendet werden, um den Namen und die Adresse von Kundinnen und Kunden in einem Formular anzuzeigen, basierend auf der im Formular eingegebenen Kunden-ID. Der Bindungsverweis kann auch verwendet werden, um die Datenquelle mit den im Formular eingegebenen Daten zu aktualisieren. Auf diese Weise können Sie mit AEM Forms Formulare erstellen, die mit externen Datenquellen interagieren und so ein nahtloses Benutzererlebnis bei der Datenerfassung und -verwaltung bieten.

- **Als ungebundenes Formularelement markieren**: Mit dieser Option können Sie Formularfelder konfigurieren, die mit keinem Schema verbunden sind. Mit dieser Option können Sie Daten speichern, ohne die Datenquelle zu aktualisieren. Außerdem können Sie damit Daten auf eine benutzerdefinierte Art und Weise verarbeiten, getrennt von der standardmäßigen Datenbankintegration.

- **Komponente ausblenden**: Wählen Sie diese Option, um die Komponente aus dem Formular auszublenden. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor. Dies ist nützlich, wenn Sie Informationen speichern müssen, die Benutzende nicht sehen oder direkt ändern müssen.
- **Komponente deaktivieren**: Wählen Sie die Option zum Deaktivieren der Komponente aus. Die deaktivierte Komponente ist nicht aktiv und Endbenutzende können sie nicht bearbeiten. Benutzende können den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor.
- **Schreibgeschützt**: Wählen Sie die Option aus, um die Komponente nicht bearbeitbar zu machen. Benutzende können den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor.
- **Standarddatum und -uhrzeit** - Mit dieser Option können Sie dem Formularfeld ein Datum und eine Uhrzeit hinzufügen. Das eingegebene Datum wird standardmäßig an der Stelle der Komponente angezeigt. Wenn Benutzende kein Datum oder keine Uhrzeit eingeben, wird dieser Wert zum Zeitpunkt der Formularübermittlung gesendet. Wenn **Komponente deaktiviert** oder **Schreibgeschützte Komponente** ausgewählt ist, werden Standarddatum und -uhrzeit auf dem Bildschirm angezeigt und bei der Formularübermittlung gesendet.

### Registerkarte „Validierung“ {#validation-tab}

![Registerkarte „Validierung“](/help/adaptive-forms/assets/datetime_validation.png)

- **Erforderlich**: Wählen Sie diese Option, wenn Sie die Komponente in einem adaptiven Formular anzeigen möchten. Nachdem Sie die Option ausgewählt haben, müssen Sie eine Auswahl treffen, bevor Sie mit der Formularübermittlung fortfahren. Wenn diese Option aktiviert ist, kann die Option **Komponente ausblenden** oder **Komponente deaktivieren** auf der Registerkarte **Allgemein** nicht ausgewählt werden.

- **Fehlermeldung**: Mit dieser Option können Sie eine Nachricht eingeben, die angezeigt wird, wenn das Kontrollkästchen **Erforderlich** aktiviert ist und das Feld leer bleibt.

- **Meldung zur Skriptvalidierung**: Mit dieser Option können Sie eine Meldung eingeben, die angezeigt wird, wenn die Skriptvalidierung fehlschlägt.

- **Mindestdatum** – Sie können mit dieser Option das erforderliche Mindestdatum eingeben. Wenn Sie ein Datum eingeben, das vor dem in „Mindestdatum und -uhrzeit“ angegebenen Datum liegt, wird eine Fehlermeldung auf dem Bildschirm angezeigt. Sie können der **Mindest-Fehlermeldung** eine benutzerdefinierte Fehlermeldung hinzufügen.

- **Mindestfehlermeldung** - Sie können im Dialogfeld **Mindestfehlermeldung** eine benutzerdefinierte Fehlermeldung hinzufügen, die angezeigt wird, wenn Sie ein Datum oder eine Uhrzeit eingeben, die vor dem in der Option **Mindestdatum** angegebenen Datum oder Uhrzeit liegt.

- **Maximales Datum** - Mit dieser Option können Sie das erforderliche Datum und die maximale Uhrzeit eingeben. Wenn Sie ein Datum oder eine Uhrzeit eingeben, die nach dem in „Maximales Datum“ angegebenen Datum oder der angegebenen Uhrzeit liegt, wird eine Fehlermeldung auf dem Bildschirm angezeigt. Sie können im Dialog **Maximal-Fehlermeldung** eine benutzerdefinierte Fehlermeldung hinzufügen.

- **Maximal-Fehlermeldung** - Sie können im Dialogfeld **Maximal-Fehlermeldung** eine benutzerdefinierte Fehlermeldung hinzufügen, die angezeigt wird, wenn Sie ein Datum oder eine Uhrzeit eingeben, die nach dem in der Option **Maximales Datum** angegebenen Datum oder der Uhrzeit liegt.

### Registerkarte „Hilfe-Inhalt“ {#help-content-tab}

![Registerkarte „Hilfe-Inhalt“](/help/adaptive-forms/assets/datetime_helptab.png)

- **Kurzbeschreibung**: Eine Kurzbeschreibung ist eine kurze Erklärung, die zusätzliche Informationen oder Klarstellungen über den Zweck eines Formularfelds bietet. Es hilft Benutzenden zu verstehen, welcher Datentyp in das Feld eingegeben werden soll, und kann Richtlinien oder Beispiele bereitstellen, um sicherzustellen, dass die eingegebenen Informationen gültig sind und die gewünschten Kriterien erfüllen. Standardmäßig bleiben kurze Beschreibungen ausgeblendet. Aktivieren Sie die Option **Kurzbeschreibung immer anzeigen**, um sie unterhalb der Komponente anzuzeigen.

- **Kurzbeschreibung immer anzeigen** – Aktivieren Sie die Option, um die Kurzbeschreibung unterhalb der Komponente anzuzeigen.

- **Hilfetext**: Hilfetext bezieht sich auf zusätzliche Informationen oder Anleitungen, die den Benutzenden bereitgestellt werden, um sie beim korrekten Ausfüllen eines Formularfelds zu unterstützen. Er erscheint, wenn Benutzende auf das Hilfesymbol (i) neben der Komponente klicken. Hilfetext enthält detailliertere Informationen als die Beschriftung oder der Platzhaltertext eines Formularfelds und soll den Benutzenden dabei helfen, die Anforderungen oder Einschränkungen des Felds zu verstehen. Er kann auch Vorschläge oder Beispiele anbieten, um das Ausfüllen des Formulars einfacher und genauer zu gestalten.


### Registerkarte „Barrierefreiheit“ {#accessibility-tab}

![Registerkarte „Barrierefreiheit“](/help/adaptive-forms/assets/datetime_accessibilitytab.png)

- **Text für Bildschirmlesehilfen** – Das ist zusätzlicher Text, der von Hilfstechnologien wie etwa Bildschirmlesehilfen für sehbehinderte Personen vorgelesen wird. Dieser Text enthält eine Audiobeschreibung des Zwecks des Formularfelds und kann Informationen über den Titel, die Beschreibung, den Namen und alle relevanten Nachrichten (benutzerdefinierten Text) des Felds enthalten. Der Text der Bildschirmlesehilfe hilft sicherzustellen, dass das Formular allen Benutzenden zugänglich ist, auch Personen mit Sehschwäche, und bietet ihnen ein umfassendes Verständnis des Formularfelds und seiner Anforderungen.
   - **Benutzerdefinierter Text**: Wählen Sie diese Option aus, um den benutzerdefinierten Text für ARIA-Barrierefreiheitsbeschriftungen zu verwenden. Wenn Sie diese Option auswählen, wird das Benutzerdefinierter Dialogfeld „Text“ angezeigt. Sie können relevante Informationen im Benutzerdefinierter Dialogfeld „Text“ hinzufügen.
   - **Beschreibung**: Wählen Sie diese Option aus, um die Beschreibung für ARIA-Barrierefreiheitsbeschriftungen zu verwenden.
   - **Titel**: Wählen Sie diese Option aus, um den Titel für ARIA-Barrierefreiheitsbeschriftungen zu verwenden.
   - **Name**: Wählen Sie diese Option aus, um den Namen für ARIA-Barrierefreiheitsbeschriftungen zu verwenden.
   - **Keine**: Wählen Sie diese Option aus, wenn Sie keine ARIA-Barrierefreiheitsbezeichnungen hinzufügen möchten.

<!--
### Formats Tab {#format-tab}

![Formats tab](/help/adaptive-forms/assets/datepicker_formattab.png)

-   **Display Format** - It represents the date format that is displayed to the user. The **Type** option allows the user to select the date format. You can also customize the date format using the **Custom** option in the **Type** dropdown menu.

-   **Edit Format** - It represents a date format in which the user can edit the date. The **Type** option allows the user to select the date format. You can also customize the date format using the **Custom** option in the **Type** dropdown menu.
-  **Format error message** - This option allows you to enter the message displayed on the screen when the entered date is not in the correct format.
- **Language** - This feature is used for formatting the specific field. When a user selects any language option from the **Type** drop-down menu, the **IETF BCP 47 language tag** option appears in the panel. You can choose the language for field formatting when translating an Adaptive Form into a specific language.
  
The set of languages is not visible by default, but users can input a custom **IETF BCP 47 language tag** by updating the template policy:

  1. Open the corresponding template associated with an Adaptive Form in the template editor.
  2. Select the existing policy as `datepicker-default-policy` from the drop-down menu.
   
        ![Date Picker template Policy](/help/adaptive-forms/assets/date-picker-template-policy.png)

  3. Click **Done**.

        >[!NOTE]
        >
        > For further information on how to translate an Adaptive Form to a specific locale, [click here](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/supporting-new-language-localization-core-components).
-->

## Dialogfeld „Design“ {#design-dialog}

Sie können das Dialogfeld „Design“ verwenden, um CSS-Stile für die Datums- und Uhrzeitkomponente zu definieren und zu verwalten.

### Registerkarte „Stile“ {#styles-tab}

Sie können die Registerkarte zum Definieren und Verwalten von CSS-Stilen für eine Komponente verwenden. Die Kernkomponente „Datum und Uhrzeit“ von Adaptive Forms unterstützt das AEM [Stilsystem](/help/get-started/authoring.md#component-styling).

![Registerkarte „Stile“](/help/adaptive-forms/assets/datepicker_styletab.png)

- **Standard-CSS** Klassen: Sie können eine standardmäßige CSS-Klasse für die Datums- und Uhrzeit-Kernkomponente von Adaptive Forms bereitstellen.

- **Zulässige Stile**: Sie können Stile definieren, indem Sie den Namen und die CSS-Klasse für den Stil angeben. Sie können beispielsweise einen Stil mit dem Namen „Fettschrift“ erstellen und die CSS-Klasse „Schriftbreite: Fett“ bereitstellen. Sie können diese Stile bei einem adaptiven Formular im adaptiven Formular-Editor anwenden. Um einen Stil anzuwenden, wählen Sie im Editor für adaptive Formulare die Komponente aus, auf die Sie den Stil anwenden möchten, navigieren Sie zum Eigenschaften-Dialog und wählen Sie den gewünschten Stil aus der Dropdown-Liste **Stile**. Wenn Sie die Stile aktualisieren oder ändern müssen, kehren Sie einfach zum Dialogfeld „Design“ zurück, aktualisieren die Stile auf der Registerkarte „Stile“ und speichern die Änderungen.

### Benutzerdefinierte Eigenschaften

![Dialogfeld „Benutzerdefinierte Eigenschaften“](/help/adaptive-forms/assets/datepicker_customproperties.png)

Mit der Option „Benutzerdefinierte Eigenschaften“ können Sie mithilfe der Formularvorlage benutzerdefinierte Attribute (Schlüsselwertpaare) mit einer Kernkomponente eines adaptiven Formulars verknüpfen. Die benutzerdefinierten Eigenschaften werden im Eigenschaftenbereich der Headless-Ausgabedarstellung der Komponente angezeigt. So kann ein dynamisches Formularverhalten erzeugt werden, das sich je nach den benutzerdefinierten Attributwerten anpasst. Beispielsweise können Entwickelnde verschiedene Ausgabedarstellungen einer Headless-Formularkomponente für Mobile-, Desktop- oder Web-Plattformen entwerfen und so das Benutzererlebnis auf einer Vielzahl von Geräten erheblich verbessern.

- **Gruppenname**: Sie können einen Namen angeben, um die Gruppe der benutzerdefinierten Eigenschaften zu kennzeichnen. Sie können mehrere Gruppen benutzerdefinierter Eigenschaften hinzufügen, löschen oder neu anordnen. Nach dem Hinzufügen der Gruppe benutzerdefinierter Eigenschaften werden folgende Optionen angezeigt:

   - **Schlüssel-Wert-Paare**: Sie können mehrere Namen und Werte benutzerdefinierter Eigenschaften hinzufügen, indem Sie für jede Gruppe benutzerdefinierter Eigenschaften auf **Hinzufügen** klicken.

   - **Löschen**: Tippen oder klicken Sie auf diese Option, um den Namen und den Wert der benutzerdefinierten Eigenschaft zu löschen.

   - **Neu anordnen**: Ordnen Sie den Namen und Wert der benutzerdefinierten Eigenschaft Antippen oder Klicken und Ziehen neu an.

<!--
### Formats Tab {#formats-tab}

The formats tab allows you to specify default and custom date formats.

![Formattab](/help/adaptive-forms/assets/datepicker_formatpolicy.png)



## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html?lang=de)

-->

## Ähnliche Artikel {#related-articles}

{{more-like-this}}

## Siehe auch {#see-also}

{{see-also}}


