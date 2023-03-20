---
title: Adaptive Forms-Kernkomponente - E-Mail-Eingabe
description: Verwenden oder Anpassen der Kernkomponente "Adaptive Forms-E-Mail-Eingabe".
role: Architect, Developer, Admin, User
exl-id: f6a2974b-991e-4cea-9ef8-0b03e8975eeb
source-git-commit: d2a6108f17f6e0c6b91bec84893d64a8bd48effd
workflow-type: tm+mt
source-wordcount: '1683'
ht-degree: 1%

---

# Email-Eingabe {#Email-input-adaptive-forms-core-component}

Die Kernkomponente für die E-Mail-Eingabe im adaptiven Formular wird verwendet, um E-Mail-Adressen von Benutzern zu erfassen. Über das E-Mail-Eingabefeld kann der Browser überprüfen, ob die eingegebenen Daten ein gültiges E-Mail-Adressformat sind. Es wird normalerweise als Textfeld dargestellt und verfügt über Mustervalidierungen, um nur gültige E-Mail-Adressen zu akzeptieren. Das E-Mail-Eingabefeld kann mit zusätzlichen Attributen wie &quot;erforderlich&quot;, &quot;Platzhalter&quot;und &quot;Muster&quot;weiter angepasst werden, um Überprüfungen für die Eingabedaten festzulegen.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

Es gibt verschiedene Gründe, warum es sinnvoll ist, eine E-Mail-Eingabekomponente in ein adaptives Formular einzuschließen:

* **Benutzerfreundlichkeit**: Eine E-Mail-Eingabe erleichtert den Benutzern die Eingabe ihrer E-Mail-Adressen, da sie einen klaren Hinweis auf die in dem Feld erwarteten Daten liefert.

* **Personalisierte Kommunikation**: Das Erfassen von E-Mail-Adressen von Benutzern über ein Formular ermöglicht eine personalisierte Kommunikation, z. B. das Senden von Bestätigungs-E-Mails oder Newslettern.

* **Lead-Generierung**: Durch die Erfassung von E-Mail-Adressen über ein Formular können Unternehmen ihre E-Mail-Liste erstellen und für die Lead-Generierung verwenden.

* **Benutzerauthentifizierung**: E-Mail-Adressen können als Mittel zur Authentifizierung für den Zugriff auf eingeschränkte Inhalte oder Dienste verwendet werden.

* **Feedback-Sammlung**: Eine E-Mail-Eingabe in einem Feedback-Formular ermöglicht es dem Unternehmen, mit dem Benutzer zu kommunizieren, um dessen Feedback zu verfolgen oder zu klären.

## Version und Kompatibilität {#version-and-compatibility}

Die Kernkomponente &quot;Adaptive Forms Accordion&quot;wurde im Februar 2023 als Teil der Kernkomponenten 2.0.4 für Cloud Service und Kernkomponenten 1.1.12 für AEM 6.5.16.0 Forms oder höher veröffentlicht. In der folgenden Tabelle finden Sie alle unterstützten Versionen, AEM Kompatibilität und Links zur entsprechenden Dokumentation:

| Komponentenversion | AEM as a Cloud Service | AEM 6.5.16.0 Forms oder höher |
|---|---|---|
| v1 | Kompatibel mit<br>[Version 2.0.4](/help/adaptive-forms/version.md) und höher | Kompatibel mit<br>[Version 1.1.12](/help/adaptive-forms/version.md) und höher, jedoch weniger als 2.0.0. |

Informationen zu Kernkomponentenversionen und -versionen finden Sie im Abschnitt [Kernkomponenten-Versionen](/help/adaptive-forms/version.md) Dokument.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technische Details {#technical-details}

Laden Sie die neuesten Informationen zur Kernkomponente &quot;Adaptive Forms-E-Mail-Eingabe&quot;in der technischen Dokumentation zu [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/emailinput/v1/emailinput). Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie im Abschnitt [Entwicklerdokumentation für Kernkomponenten](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Im Dialogfeld &quot;Konfigurieren&quot;können Sie das E-Mail-Eingabeerlebnis für Besucher einfach anpassen. Sie können auch E-Mail-Eingabeoptionen definieren, um eine nahtlose Benutzererfahrung zu gewährleisten.

### Einfache Registerkarte {#basic-tab}

![Registerkarte &quot;Allgemein&quot;](/help/adaptive-forms/assets/email_basictab.png)

* **Name** - Der Name identifiziert die Komponente eindeutig im Regeleditor. Sonderzeichen und Leerzeichen sind in den Namensfolgen nicht zulässig.

* **Titel** - Mit dem Titel können Sie eine Komponente in einem Formular leicht identifizieren. Standardmäßig wird der Titel über der Komponente angezeigt. Wenn Sie keinen Titel hinzufügen, wird der Name der Komponente anstelle des Titeltexts angezeigt.

* **Titel ausblenden** - Wählen Sie die Option aus, um den Titel der Komponente auszublenden.

* **Platzhaltertext** - Platzhaltertext in einer Formularkomponente bezieht sich auf eine kurze Beschriftung oder Eingabeaufforderung, die in einem Eingabefeld angezeigt wird, um den Benutzer darauf hinzuweisen, welcher Informationstyp in dieses Feld eingegeben werden soll. Platzhaltertext verschwindet, wenn der Benutzer mit der Eingabe in das Feld beginnt, und wird wieder angezeigt, wenn das Feld leer bleibt. Es bietet einen visuellen Hinweis für den Benutzer, fungiert jedoch nicht als permanente Bezeichnung oder Wert für das Feld.

* **Bindungsverweis** - Ein Bindungsverweis ist ein Verweis auf ein Datenelement, das in einer externen Datenquelle gespeichert und in einem Formular verwendet wird. Mit der Bindungsreferenz können Sie Daten dynamisch an Formularfelder binden, sodass das Formular die aktuellsten Daten aus der Datenquelle anzeigen kann. Beispielsweise kann eine Bindungsverweis verwendet werden, um den Namen und die Adresse eines Kunden in einem Formular anzuzeigen, basierend auf der im Formular eingegebenen Kundenkennung. Die Bindungsverweis kann auch verwendet werden, um die Datenquelle mit den im Formular eingegebenen Daten zu aktualisieren. Auf diese Weise können Sie mit AEM Forms Formulare erstellen, die mit externen Datenquellen interagieren und so eine nahtlose Benutzererfahrung bei der Datenerfassung und -verwaltung bieten.
* **Komponente ausblenden** - Wählen Sie die Option, um die Komponente aus dem Formular auszublenden. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regeleditor. Dies ist nützlich, wenn Sie Informationen speichern müssen, die vom Benutzer nicht gesehen oder direkt geändert werden müssen.
* **Komponente deaktivieren** - Wählen Sie die Option zum Deaktivieren der Komponente aus. Die deaktivierte Komponente ist vom Endbenutzer nicht aktiv oder kann nicht bearbeitet werden. Der Benutzer kann den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regeleditor.
* **Schreibgeschützt** - Wählen Sie die Option aus, um die Komponente nicht bearbeitbar zu machen. Der Benutzer kann den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regeleditor.

* **Standardwert** - Mit dieser Option können Sie einen Standardwert in ein Formularfeld einfügen. Wenn **Komponente deaktiviert** oder **Schreibgeschützte Komponente** ausgewählt ist, wird der Standardwert auf dem Bildschirm angezeigt. Wenn kein Wert vom Benutzer in das Formularfeld eingegeben wird, wird dieser Wert zum Zeitpunkt der Formularübermittlung gesendet


### Registerkarte &quot;Validierung&quot; {#validation-tab}

![Registerkarte &quot;Validierung&quot;](/help/adaptive-forms/assets/email_validationtab.png)

* **Erforderlich** - Wählen Sie diese Option, wenn Sie die Komponente in einem adaptiven Formular anzeigen möchten. Sie können die **Komponente ausblenden** oder **Komponente deaktivieren**  im **Allgemein** Registerkarte angezeigt, wenn diese Option aktiviert ist.

* **Fehlermeldung** - Mit dieser Option können Sie eine Nachricht eingeben, die angezeigt wird, wenn die **Erforderlich** aktiviert ist und das Formularfeld leer bleibt.

* **Überprüfungsmeldung für Skripten** - Mit dieser Option können Sie eine Meldung eingeben, die angezeigt werden soll, wenn die Skriptvalidierung fehlschlägt.

* **Maximale Zeichenanzahl** - Mit dieser Option können Sie die maximal zulässige Anzahl von Zeichen im Feld angeben. Wenn Sie Zeichen eingeben, die größer sind als der in **Maximale Zeichenanzahl**, wird eine Fehlermeldung auf dem Bildschirm angezeigt. Die **Fehlermeldung zu maximal Zeichen** können Sie eine benutzerdefinierte Fehlermeldung hinzufügen.

* **Fehlermeldung zu maximal Zeichen** - die **Fehlermeldung zu maximal Zeichen** können Sie eine benutzerdefinierte Fehlermeldung hinzufügen, wenn Sie Zeichen eingeben, die über dem in der Variablen **Maximale Zeichenanzahl** -Option.

* **Mindestanzahl von Zeichen** - Mit dieser Option können Sie die zulässige Mindestanzahl von Zeichen im Feld angeben. Wenn Sie Zeichen eingeben, die kleiner sind als der in **Mindestanzahl von Zeichen**, wird eine Fehlermeldung auf dem Bildschirm angezeigt. Die **Fehlermeldung bei minimalen Zeichen** können Sie eine benutzerdefinierte Fehlermeldung hinzufügen.

* **Fehlermeldung bei minimalen Zeichen** - die **Fehlermeldung bei minimalen Zeichen** können Sie eine benutzerdefinierte Fehlermeldung hinzufügen, wenn Sie Zeichen eingeben, die kleiner sind als der in der Variablen **Mindestanzahl von Zeichen** -Option.

<br>

    Mit der Option **Überprüfungsmuster** können Sie ein Muster eingeben, um die eingegebene E-Mail-ID zu validieren. Falls die E-Mail-ID nicht mit dem in der Option **Muster** eingegebenen Wert validiert werden kann, wird die Fehlermeldung auf dem Bildschirm angezeigt.
    * **Muster** - Mit dieser Option können Sie die zulässigen Überprüfungsmuster für E-Mails eingeben. Reguläre Ausdrücke sind ebenfalls zulässig.
    * **Fehlermeldung** - Mit dieser Option können Sie eine Meldung eingeben, die auf dem Bildschirm angezeigt wird, wenn die E-Mail-ID nicht mit dem in der Option **Muster** eingegebenen Wert validiert werden kann.

### Registerkarte &quot;Hilfe-Inhalt&quot; {#help-content-tab}

![Registerkarte &quot;Hilfe-Inhalt&quot;](/help/adaptive-forms/assets/email_helptab.png)

* **Kurzbeschreibung** - Eine kurze Beschreibung ist eine kurze Texterklärung, die zusätzliche Informationen oder Klarstellungen zum Zweck eines bestimmten Formularfelds bietet. Es hilft dem Benutzer zu verstehen, welcher Datentyp in das Feld eingegeben werden soll, und kann Richtlinien oder Beispiele bereitstellen, um sicherzustellen, dass die eingegebenen Informationen gültig sind und die gewünschten Kriterien erfüllen. Standardmäßig bleiben kurze Beschreibungen ausgeblendet. Aktivieren Sie die **Kurzbeschreibung immer anzeigen** -Option, um sie unter der Komponente anzuzeigen.

* **Kurzbeschreibung immer anzeigen** - Aktivieren Sie die Option, um die Kurzbeschreibung unter der Komponente anzuzeigen.

* **Hilfetext** - Hilfetext bezieht sich auf zusätzliche Informationen oder Anleitungen, die dem Benutzer bereitgestellt werden, um ihn beim korrekten Ausfüllen eines Formularfelds zu unterstützen. Er wird angezeigt, wenn der Benutzer auf das Hilfesymbol (i) neben der Komponente klickt. Hilfetext enthält detailliertere Informationen als die Beschriftung oder der Platzhaltertext eines Formularfelds und soll dem Benutzer dabei helfen, die Anforderungen oder Einschränkungen des Felds zu verstehen. Es kann auch Vorschläge oder Beispiele anbieten, um das Ausfüllen des Formulars zu vereinfachen und genauer zu gestalten.

### Registerkarte „Erreichbarkeit“ {#accessibility-tab}

![Registerkarte &quot;Barrierefreiheit&quot;](/help/adaptive-forms/assets/email_accessibilitytab.png)

**Text für Bildschirmlesehilfen** - Text für Bildschirmlesehilfen bezieht sich auf zusätzlichen Text, der speziell für Hilfstechnologien wie Bildschirmlesehilfen vorgesehen ist, die von sehbehinderten Personen verwendet werden. Dieser Text enthält eine Audiobeschreibung des Zwecks des Formularfelds und kann Informationen über den Titel, die Beschreibung, den Namen und alle relevanten Nachrichten (benutzerdefinierten Text) des Felds enthalten. Der Text der Bildschirmlesehilfe hilft sicherzustellen, dass das Formular für alle Benutzer zugänglich ist, auch für Benutzer mit Sehbehinderungen, und bietet ihnen ein umfassendes Verständnis des Formularfelds und seiner Anforderungen.

## Dialogfeld „Design“ {#design-dialog}

Das Dialogfeld &quot;Design&quot;wird verwendet, um CSS-Stile für die E-Mail-Eingabekomponente zu definieren und zu verwalten.

### Registerkarte „Arten“ {#styles-tab}

Die Registerkarte wird verwendet, um CSS-Stile für eine Komponente zu definieren und zu verwalten. Die Kernkomponente &quot;Adaptive Forms-E-Mail-Eingabe&quot;unterstützt die AEM [Stilsystem](/help/get-started/authoring.md#component-styling).

![Registerkarte &quot;Stil&quot;](/help/adaptive-forms/assets/email_designdialog.png)

* **Standard-CSS-Klassen**: Sie können eine Standard-CSS-Klasse für die Adaptive Forms-E-Mail-Eingabekomponente bereitstellen.

* **Zulässige Stile**: Sie können Stile definieren, indem Sie einen Namen und die CSS-Klasse angeben, die den Stil darstellt. Sie können beispielsweise einen Stil mit dem Namen &quot;fett Text&quot;erstellen und die CSS-Klasse &quot;font-weight: fett&quot;. Sie können diese Stile im adaptiven Forms-Editor verwenden oder auf ein adaptives Formular anwenden. Um einen Stil anzuwenden, wählen Sie im adaptiven Forms-Editor die Komponente aus, auf die Sie den Stil anwenden möchten, navigieren Sie zum Dialogfeld &quot;Eigenschaften&quot;und wählen Sie den gewünschten Stil aus dem **Stile** Dropdown-Liste. Wenn Sie die Stile aktualisieren oder ändern müssen, kehren Sie einfach zum Dialogfeld &quot;Design&quot;zurück, aktualisieren Sie die Stile auf der Registerkarte &quot;Stile&quot;und speichern Sie die Änderungen.

### Registerkarte &quot;Formate&quot; {#format-tab}

Auf der Registerkarte &quot;Formate&quot;können Sie standardmäßige und benutzerdefinierte Datumsformate angeben.

![Registerkarte &quot;Design&quot;](/help/adaptive-forms/assets/emailinput_designformattab.png)

