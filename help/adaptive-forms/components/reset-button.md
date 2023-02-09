---
title: Adaptive Forms-Kernkomponente - Schaltfläche "Zurücksetzen"
description: Verwenden oder Anpassen der Kernkomponente für die Schaltfläche "Zurücksetzen"der adaptiven Forms
role: Architect, Developer, Admin, User
source-git-commit: 945e1793ae4e959f83960db46d2de4257916fe32
workflow-type: tm+mt
source-wordcount: '1173'
ht-degree: 2%

---


# Zurücksetzen {#reset-button}

Eine Schaltfläche zum Zurücksetzen in einem adaptiven Formular ist eine Schaltfläche, mit der Benutzer alle Formularfelder löschen oder auf ihre Standardwerte zurücksetzen können. Wenn auf die Schaltfläche zum Zurücksetzen geklickt wird, werden alle Daten gelöscht, die in die Formularfelder eingegeben wurden, und die Felder kehren in ihren ursprünglichen Status zurück. Die Schaltfläche &quot;Zurücksetzen&quot;wird in der Regel als Alternative zur Senden-Schaltfläche verwendet und bietet Benutzern die Möglichkeit, neu zu beginnen, wenn sie falsche oder unerwünschte Daten in das Formular eingegeben haben.


## Verwendung {#reasons-to-use-reset-button}

Die Gründe für die Verwendung einer Schaltfläche zum Zurücksetzen in einem adaptiven Formular sind:

* **Benutzerfreundlichkeit**: Eine Zurücksetzen-Schaltfläche bietet Benutzern eine schnelle und einfache Möglichkeit, das Formular zu löschen und neu zu beginnen, ohne jedes Feld manuell löschen zu müssen.

* **Verbesserte Benutzerfreundlichkeit**: Eine Zurücksetzen-Schaltfläche kann das Benutzererlebnis verbessern, indem sie es Benutzern ermöglicht, Fehler einfach zu korrigieren oder ihre Eingaben zu ändern.

* **Fehlervermeidung**: Durch die Verwendung einer Zurücksetzungsschaltfläche können Benutzer vermeiden, versehentlich falsche Daten zu übermitteln, was zu Fehlern oder Verarbeitungsproblemen führen kann.

* **Konsistenz**: Die Verwendung einer Zurücksetzen-Schaltfläche in einem Formular sorgt für Konsistenz in der Benutzererfahrung, da Zurücksetzen-Schaltflächen häufig bei Formularen zum Tragen kommen.

* **Besseres Data Management**: Durch die Verwendung einer Zurücksetzungsschaltfläche können die Formulardaten organisiert und genau gehalten werden, da die Wahrscheinlichkeit, dass Benutzer inkonsistente oder falsche Daten senden, geringer ist.

## Version und Kompatibilität {#version-and-compatibility}

Die Kernkomponente für die Schaltfläche &quot;Zurücksetzen&quot;der adaptiven Forms wurde im Februar 2023 als Teil der Kernkomponenten 2.0.4 veröffentlicht. Hier finden Sie eine Tabelle mit allen unterstützten Versionen, AEM Kompatibilität und Links zur entsprechenden Dokumentation:

|  |  |
|---|---|
| Komponentenversion | AEM as a Cloud Service |
| --- | --- |
| v1 | Kompatibel mit<br>[Version 2.0.4](/help/versions.md) und höher | Kompatibel | Kompatibel |

Informationen zu Kernkomponentenversionen und -versionen finden Sie im Abschnitt [Kernkomponenten-Versionen](/help/versions.md) Dokument.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technische Details {#technical-details}

Laden Sie die neuesten Informationen zur Kernkomponente für die Schaltfläche &quot;Forms zurücksetzen&quot;in der technischen Dokumentation zu [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/button/v1/button). Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie im Abschnitt [Entwicklerdokumentation für Kernkomponenten](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Im Dialogfeld &quot;Konfigurieren&quot;können Sie das Erlebnis für die Schaltfläche &quot;Zurücksetzen&quot;für Besucher einfach anpassen. Sie können die Optionen für die Schaltfläche &quot;Zurücksetzen&quot;auch einfach definieren, um ein nahtloses Benutzererlebnis zu gewährleisten.

### Einfache Registerkarte {#basic-tab}

![Einfache Registerkarte](/help/adaptive-forms/assets/button_basictab.png)

* **Name** - Sie können eine Formularkomponente sowohl im Formular als auch im Regeleditor leicht mit ihrem eindeutigen Namen identifizieren, der Name darf jedoch keine Leerzeichen oder Sonderzeichen enthalten.

* **Titel** - Mit dem Titel können Sie eine Komponente in einem Formular leicht identifizieren. Standardmäßig wird der Titel über der Komponente angezeigt. Wenn Sie keinen Titel hinzufügen, wird der Name der Komponente anstelle des Titeltexts angezeigt.

* **Bindungsverweis** - Ein Bindungsverweis ist ein Verweis auf ein Datenelement, das in einer externen Datenquelle gespeichert und in einem Formular verwendet wird. Mit der Bindungsreferenz können Sie Daten dynamisch an Formularfelder binden, sodass das Formular die aktuellsten Daten aus der Datenquelle anzeigen kann. Beispielsweise kann eine Bindungsverweis verwendet werden, um den Namen und die Adresse eines Kunden in einem Formular anzuzeigen, basierend auf der im Formular eingegebenen Kundenkennung. Die Bindungsverweis kann auch verwendet werden, um die Datenquelle mit den im Formular eingegebenen Daten zu aktualisieren. Auf diese Weise können Sie mit AEM Forms Formulare erstellen, die mit externen Datenquellen interagieren und so eine nahtlose Benutzererfahrung bei der Datenerfassung und -verwaltung bieten.

* **Komponente ausblenden** - Wählen Sie die Option, um die Komponente aus dem Formular auszublenden. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regeleditor. Dies ist nützlich, wenn Sie Informationen speichern müssen, die vom Benutzer nicht gesehen oder direkt geändert werden müssen.
* **Komponente deaktivieren** - Wählen Sie die Option zum Deaktivieren der Komponente aus. Die deaktivierte Komponente ist vom Endbenutzer nicht aktiv oder kann nicht bearbeitet werden. Der Benutzer kann den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regeleditor.
* **Schreibgeschützt** - Wählen Sie die Option aus, um die Komponente nicht bearbeitbar zu machen. Der Benutzer kann den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regeleditor.

### Registerkarte &quot;Hilfe-Inhalt&quot; {#help-content}

![Registerkarte &quot;Hilfe-Inhalt&quot;](/help/adaptive-forms/assets/button_helptab.png)

* **Kurzbeschreibung** - Eine kurze Beschreibung ist eine kurze Texterklärung, die zusätzliche Informationen oder Klarstellungen zum Zweck eines bestimmten Formularfelds bietet. Es hilft dem Benutzer zu verstehen, welcher Datentyp in das Feld eingegeben werden soll, und kann Richtlinien oder Beispiele bereitstellen, um sicherzustellen, dass die eingegebenen Informationen gültig sind und die gewünschten Kriterien erfüllen. Standardmäßig bleiben kurze Beschreibungen ausgeblendet. Aktivieren Sie die **Kurzbeschreibung immer anzeigen** -Option, um sie unter der Komponente anzuzeigen.

* **Kurzbeschreibung immer anzeigen** - Aktivieren Sie die Option, um die Kurzbeschreibung unter der Komponente anzuzeigen.

* **Hilfetext** - Hilfetext bezieht sich auf zusätzliche Informationen oder Anleitungen, die dem Benutzer bereitgestellt werden, um ihn beim korrekten Ausfüllen eines Formularfelds zu unterstützen. Er wird angezeigt, wenn der Benutzer auf das Hilfesymbol (i) neben der Komponente klickt. Hilfetext enthält detailliertere Informationen als die Beschriftung oder der Platzhaltertext eines Formularfelds und soll dem Benutzer dabei helfen, die Anforderungen oder Einschränkungen des Felds zu verstehen. Es kann auch Vorschläge oder Beispiele anbieten, um das Ausfüllen des Formulars zu vereinfachen und genauer zu gestalten.

### Barrierefreiheit {#accessibility}

![Registerkarte &quot;Barrierefreiheit&quot;](/help/adaptive-forms/assets/button_accessibilitytab.png)

* **Text für Bildschirmlesehilfen** - Text für Bildschirmlesehilfen bezieht sich auf zusätzlichen Text, der speziell für Hilfstechnologien wie Bildschirmlesehilfen vorgesehen ist, die von sehbehinderten Personen verwendet werden. Dieser Text enthält eine Audiobeschreibung des Zwecks des Formularfelds und kann Informationen über den Titel, die Beschreibung, den Namen und alle relevanten Nachrichten (benutzerdefinierten Text) des Felds enthalten. Der Text der Bildschirmlesehilfe hilft sicherzustellen, dass das Formular für alle Benutzer zugänglich ist, auch für Benutzer mit Sehbehinderungen, und bietet ihnen ein umfassendes Verständnis des Formularfelds und seiner Anforderungen.

## Dialogfeld „Design“ {#design-dialog}

Das Dialogfeld &quot;Design&quot;wird verwendet, um CSS-Stile für die Komponente &quot;Schaltfläche zurücksetzen&quot;zu definieren und zu verwalten.


### Registerkarte „Arten“ {#styles-tab}

Das Dialogfeld &quot;Design&quot;wird zum Definieren und Verwalten von CSS-Stilen für eine Komponente verwendet. Die Kernkomponente &quot;Forms-Schaltfläche zum Zurücksetzen&quot;unterstützt die AEM [Stilsystem](/help/get-started/authoring.md#component-styling).

**Standard-CSS-Klassen**: Sie können eine standardmäßige CSS-Klasse für die Kernkomponente &quot;Kernkomponente&quot;der adaptiven Forms-Schaltfläche &quot;Zurücksetzen&quot;bereitstellen.

**Zulässige Stile**: Sie können Stile definieren, indem Sie einen Namen und die CSS-Klasse angeben, die den Stil darstellt. Sie können beispielsweise einen Stil mit dem Namen &quot;fett Text&quot;erstellen und die CSS-Klasse &quot;font-weight: fett&quot;. Sie können diese Stile im adaptiven Forms-Editor verwenden oder auf ein adaptives Formular anwenden. Um einen Stil anzuwenden, wählen Sie im adaptiven Forms-Editor die Komponente aus, auf die Sie den Stil anwenden möchten, navigieren Sie zum Dialogfeld &quot;Eigenschaften&quot;und wählen Sie den gewünschten Stil aus dem **Stile** Dropdown-Liste. Wenn Sie die Stile aktualisieren oder ändern müssen, kehren Sie einfach zum Dialogfeld &quot;Design&quot;zurück, aktualisieren Sie die Stile auf der Registerkarte &quot;Stile&quot;und speichern Sie die Änderungen.
