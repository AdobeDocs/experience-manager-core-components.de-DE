---
title: Adaptive Forms-Kernkomponente - Schaltfläche
description: Verwenden oder Anpassen der Kernkomponente der Schaltfläche "Adaptive Forms".
role: Architect, Developer, Admin, User
source-git-commit: 945e1793ae4e959f83960db46d2de4257916fe32
workflow-type: tm+mt
source-wordcount: '1491'
ht-degree: 2%

---


# Schaltflächenkomponente  {#button-component-adaptive-forms-core-component}

Eine Schaltfläche in einem adaptiven Formular ist ein UI-Element, mit dem Benutzer eine Aktion auslösen können, wenn darauf geklickt wird. Mit dem Schaltflächenelement können Sie ein Formular senden, ein Formular zurücksetzen oder andere Aktionen durchführen, z. B. zu einer anderen Seite navigieren oder benutzerdefinierten Code auslösen. Die Schaltfläche kann mit der Schaltflächen-Kernkomponente erstellt werden.

Mit dem Regeleditor für adaptive Forms können Benutzer verschiedene Aktionen für die Schaltflächenkomponente festlegen. Dazu gehören das Öffnen einer Website, das Anzeigen oder Ausblenden von Formularkomponenten, das Hinzufügen einer Instanz eines Bedienfelds oder einer Komponente, das Senden oder Zurücksetzen eines Formulars und mehr.

Adaptive Forms bietet auch separate Schaltflächenkomponenten zum Senden oder Zurücksetzen eines Formulars. Die Schaltflächenkomponente kann jedoch auch so konfiguriert werden, dass diese Aktionen bei Bedarf ausgeführt werden.

Benutzer können über den Regeleditor für adaptive Forms auf die vollständige Liste der für die Schaltflächenkomponente unterstützten Aktionen zugreifen. Mit dem Regeleditor können Benutzer Regeln erstellen, die von verschiedenen Ereignissen ausgelöst werden, z. B. durch Klicken auf eine Schaltfläche, beim Laden eines Formulars oder beim Ändern eines Feldwerts. Diese Regeln können dann für verschiedene Aktionen verwendet werden, z. B. zum Anzeigen oder Ausblenden von Komponenten, zum Festlegen von Feldwerten oder zum Senden des Formulars.

## Verwendung {#reasons-to-use-button}

Es gibt verschiedene Gründe, warum es sinnvoll ist, eine Schaltfläche in ein adaptives Formular einzuschließen, darunter:

* **Formularübermittlung**: Normalerweise wird eine Schaltfläche zum Senden eines Formulars verwendet, sodass Benutzer die eingegebenen Daten zur Verarbeitung an den Server senden können.

* **Formularzurücksetzung**: Schaltflächen können auch verwendet werden, um ein Formular zurückzusetzen und alle vom Benutzer eingegebenen Daten zu löschen.

* **Navigation**: Schaltflächen können verwendet werden, um zwischen verschiedenen Abschnitten eines Formulars oder verschiedenen Seiten auf einer Website zu navigieren.

* **Ereignisverarbeitung**: Schaltflächen können verwendet werden, um verschiedene Ereignisse wie das Öffnen einer Website, das Anzeigen/Ausblenden von Komponenten oder das Hinzufügen einer Instanz eines Bedienfelds oder einer Komponente zur Schaltfläche Trigger.

* **Interaktivität**: Schaltflächen können zum Erstellen interaktiver Formulare verwendet werden. Beispielsweise kann eine Schaltfläche zum Öffnen eines modalen Dialogfelds oder zum Umschalten eines Bereichs des Formulars verwendet werden.

## Version und Kompatibilität {#version-and-compatibility}

Die Kernkomponente &quot;Adaptive Forms-Schaltfläche&quot;v1 wurde im Februar 2023 als Teil der Kernkomponenten 2.0.4 veröffentlicht. Hier finden Sie eine Tabelle mit allen unterstützten Versionen, AEM Kompatibilität und Links zur entsprechenden Dokumentation:

|  |  |
|---|---|
| Komponentenversion | AEM as a Cloud Service |
| --- | --- |
| v1 | Kompatibel mit<br>[Version 2.0.4](/help/versions.md) und höher | Kompatibel | Kompatibel |

Informationen zu Kernkomponentenversionen und -versionen finden Sie im Abschnitt [Kernkomponenten-Versionen](/help/versions.md) Dokument.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technische Details {#technical-details}

Die neuesten Informationen zur Kernkomponente &quot;Adaptive Forms-Schaltfläche&quot;finden Sie in der technischen Dokumentation zu [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/button/v1/button). Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie im Abschnitt [Entwicklerdokumentation für Kernkomponenten](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Im Dialogfeld &quot;Konfigurieren&quot;können Sie Ihre Schaltflächen-Erfahrung für Besucher einfach anpassen. Für ein nahtloses Benutzererlebnis können Sie auch mühelos Schaltflächeneigenschaften definieren.

### Einfache Registerkarte {#basic-tab}

![Einfache Registerkarte](/help/adaptive-forms/assets/button_basictab.png)

* **Name** - Sie können eine Formularkomponente sowohl im Formular als auch im Regeleditor leicht mit ihrem eindeutigen Namen identifizieren, der Name darf jedoch keine Leerzeichen oder Sonderzeichen enthalten.

* **Titel** - Mit dem Titel können Sie eine Komponente in einem Formular leicht identifizieren. Standardmäßig wird der Titel über der Komponente angezeigt. Wenn Sie keinen Titel hinzufügen, wird der Name der Komponente anstelle des Titeltexts angezeigt.

* **Bindungsverweis** - Ein Bindungsverweis ist ein Verweis auf ein Datenelement, das in einer externen Datenquelle gespeichert und in einem Formular verwendet wird. Mit der Bindungsreferenz können Sie Daten dynamisch an Formularfelder binden, sodass das Formular die aktuellsten Daten aus der Datenquelle anzeigen kann. Beispielsweise kann eine Bindungsverweis verwendet werden, um den Namen und die Adresse eines Kunden in einem Formular anzuzeigen, basierend auf der im Formular eingegebenen Kundenkennung. Die Bindungsverweis kann auch verwendet werden, um die Datenquelle mit den im Formular eingegebenen Daten zu aktualisieren. Auf diese Weise können Sie mit AEM Forms Formulare erstellen, die mit externen Datenquellen interagieren und so eine nahtlose Benutzererfahrung bei der Datenerfassung und -verwaltung bieten.

* **Referenz zum Datensatzdokument** - Mit dieser Option können Sie ein Feld für ein adaptives Formular mit dem Feld Datensatzdokument verknüpfen. Wenn der Benutzer einen Wert in ein verknüpftes Feld eines adaptiven Formulars eingibt, wird dieser Wert auch im verknüpften Feld des entsprechenden Datensatzdokuments angezeigt. Beispielsweise kann eine Referenz zum Datensatzdokument verwendet werden, um den Namen und die Adresse eines Kunden in einem Datensatzdokument anzuzeigen, basierend auf der im Formular eingegebenen Kundenkennung. Auf diese Weise können Sie mit AEM Forms Datensatzdokument generieren und eine nahtlose Benutzererfahrung bei der Datenerfassung und -verwaltung bieten.

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


Im **Zugänglichkeit** Registerkarte, werden Werte festgelegt für [Barrierefreiheit in ARIA](https://www.w3.org/WAI/standards-guidelines/aria/) Beschriftungen für die Komponente. Für die Verwendung des Textes für die Bildschirmlesehilfe stehen verschiedene Optionen zur Verfügung:

* **Text für Bildschirmlesehilfen** - Text für Bildschirmlesehilfen bezieht sich auf zusätzlichen Text, der speziell für Hilfstechnologien wie Bildschirmlesehilfen vorgesehen ist, die von sehbehinderten Personen verwendet werden. Dieser Text enthält eine Audiobeschreibung des Zwecks des Formularfelds und kann Informationen über den Titel, die Beschreibung, den Namen und alle relevanten Nachrichten (benutzerdefinierten Text) des Felds enthalten. Der Text der Bildschirmlesehilfe hilft sicherzustellen, dass das Formular für alle Benutzer zugänglich ist, auch für Benutzer mit Sehbehinderungen, und bietet ihnen ein umfassendes Verständnis des Formularfelds und seiner Anforderungen.


   * **Benutzerdefinierter Text**: Wählen Sie diese Option aus, um den benutzerdefinierten Text für ARIA-Barrierefreiheitsbeschriftungen zu verwenden. Wenn Sie diese Option auswählen, wird das Dialogfeld &quot;Benutzerdefinierter Text&quot;angezeigt. Sie können relevante Informationen im Dialogfeld &quot;Benutzerdefinierter Text&quot;hinzufügen.
   * **Beschreibung**: Wählen Sie diese Option aus, um die Beschreibung für ARIA-Barrierefreiheitsbeschriftungen zu verwenden.
   * **Titel**: Wählen Sie diese Option aus, um den Titel für ARIA-Barrierefreiheitsbeschriftungen zu verwenden.
   * **Name**: Wählen Sie diese Option aus, um den Namen für ARIA-Barrierefreiheitsbeschriftungen zu verwenden.
   * **Keines**: Wählen Sie diese Option aus, wenn Sie keine ARIA-Barrierefreiheitsbezeichnungen hinzufügen möchten.

## Dialogfeld „Design“ {#design-dialog}

Das Dialogfeld &quot;Design&quot;wird verwendet, um CSS-Stile für die Schaltflächenkomponente zu definieren und zu verwalten.

### Registerkarte „Arten“ {#styles-tab}

Die Kernkomponente &quot;Forms-Schaltfläche&quot;unterstützt die AEM [Stilsystem](/help/get-started/authoring.md#component-styling).

**Standard-CSS-Klassen**: Sie können eine standardmäßige CSS-Klasse für die Kernkomponente &quot;Adaptive Forms-Schaltfläche&quot;bereitstellen.

**Zulässige Stile**: Sie können Stile definieren, indem Sie einen Namen und die CSS-Klasse angeben, die den Stil darstellt. Sie können beispielsweise einen Stil mit dem Namen &quot;fett Text&quot;erstellen und die CSS-Klasse &quot;font-weight: fett&quot;. Sie können diese Stile im adaptiven Forms-Editor verwenden oder auf ein adaptives Formular anwenden. Um einen Stil anzuwenden, wählen Sie im adaptiven Forms-Editor die Komponente aus, auf die Sie den Stil anwenden möchten, navigieren Sie zum Dialogfeld &quot;Eigenschaften&quot;und wählen Sie den gewünschten Stil aus dem **Stile** Dropdown-Liste. Wenn Sie die Stile aktualisieren oder ändern müssen, kehren Sie einfach zum Dialogfeld &quot;Design&quot;zurück, aktualisieren Sie die Stile auf der Registerkarte &quot;Stile&quot;und speichern Sie die Änderungen.

