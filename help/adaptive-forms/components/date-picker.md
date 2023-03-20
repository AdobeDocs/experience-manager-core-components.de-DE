---
title: Adaptive Forms-Kernkomponente - Datumsauswahl
description: Verwenden oder Anpassen der Kernkomponente für die Datumsauswahl in der adaptiven Forms.
role: Architect, Developer, Admin, User
exl-id: aa9402de-ca57-4c19-8d36-2dd0a78d6806
source-git-commit: d2a6108f17f6e0c6b91bec84893d64a8bd48effd
workflow-type: tm+mt
source-wordcount: '1666'
ht-degree: 1%

---

# Datumsauswahl {#date-picker-adaptive-forms-core-component}

Eine Datumsauswahl-Komponente in einem adaptiven Formular ist ein Element der Benutzeroberfläche, mit dem Benutzer ein Datum aus einem Kalender auswählen oder manuell ein Datum in einem bestimmten Format eingeben können. Die Datumsauswahl-Komponente kann so konfiguriert werden, dass sie unterschiedliche Formatierungen, Validierungen und Standardwerte aufweist.

**Beispiel**

![](/help/adaptive-forms/assets/date-picker.png)

## Verwendung {#reasons-to-use-drop-date-picker}

Es gibt verschiedene Gründe, warum es sinnvoll ist, eine Datumsauswahl in ein adaptives Formular einzuschließen, darunter:

* **Praktik**: Mit einer Datumsauswahlkomponente können Benutzer einfach ein Datum aus einem Kalender auswählen, ohne das Datum manuell in ein Textfeld eingeben zu müssen. Dies kann Zeit sparen und Fehler reduzieren.

* **Anwendererlebnis**: Mit der Datumsauswahl-Komponente kann das Formular benutzerfreundlicher gestaltet werden, indem eine klare und intuitive Methode zur Auswahl des Datums bereitgestellt wird.

* **Datenanalyse**: Die Datumsauswahl-Komponente kann verwendet werden, um Daten aus verschiedenen Quellen zu erfassen und zu analysieren oder sie als Eingabe für die weitere Verarbeitung zu verwenden.

* **Ereignisverwaltung**: Die Datumsauswahl-Komponente kann in Ereignisverwaltungs-Websites verwendet werden, um das Ereignisdatum auszuwählen.

* **Reservierung**: Die Komponente Datumsauswahl kann in Buchungs- und Reservierungs-Websites verwendet werden, um die Ein- und Auscheckdaten auszuwählen.

* **Datumsformat**: Mit der Datumsauswahl-Komponente kann das Format korrigiert werden, in dem das Datum angezeigt und eingegeben wird. Stellen Sie sicher, dass das Datumsformat im gesamten Formular konsistent ist, um ein konsistentes Benutzererlebnis zu gewährleisten.

## Version und Kompatibilität {#version-and-compatibility}

Die Kernkomponente &quot;Adaptive Forms Accordion&quot;wurde im Februar 2023 als Teil der Kernkomponenten 2.0.4 für Cloud Service und Kernkomponenten 1.1.12 für AEM 6.5.16.0 Forms oder höher veröffentlicht. In der folgenden Tabelle finden Sie alle unterstützten Versionen, AEM Kompatibilität und Links zur entsprechenden Dokumentation:

| Komponentenversion | AEM as a Cloud Service | AEM 6.5.16.0 Forms oder höher |
|---|---|---|
| v1 | Kompatibel mit<br>[Version 2.0.4](/help/adaptive-forms/version.md) und höher | Kompatibel mit<br>[Version 1.1.12](/help/adaptive-forms/version.md) und höher, jedoch weniger als 2.0.0. |

Informationen zu Kernkomponentenversionen und -versionen finden Sie im Abschnitt [Kernkomponenten-Versionen](/help/adaptive-forms/version.md) Dokument.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->


## Technische Details {#technical-details}

Laden Sie die neuesten Informationen zur Kernkomponente für die adaptive Forms-Datumsauswahl in der technischen Dokumentation zu [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/datepicker/v1/datepicker). Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie im Abschnitt [Entwicklerdokumentation für Kernkomponenten](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Im Dialogfeld &quot;Konfigurieren&quot;können Sie die Datumsauswahl für Besucher einfach anpassen. Für ein nahtloses Benutzererlebnis können Sie auch einfach Datumsauswahloptionen definieren.

### Einfache Registerkarte {#basic-tab}

![Registerkarte &quot;Allgemein&quot;](/help/adaptive-forms/assets/datepicker_basictab.png)

* **Name** - Der Name identifiziert die Komponente im Regeleditor eindeutig. Sonderzeichen und Leerzeichen sind in den Namensfolgen nicht zulässig.

* **Titel** - Titel ist eine Zeichenfolge, die oben in einer Komponente in einem adaptiven Formular angezeigt wird. Der Titel identifiziert die Komponente eindeutig in der Baumstruktur eines adaptiven Formulars. Wenn Sie keinen Titel hinzufügen, wird der Name der Komponente anstelle des Titeltexts angezeigt.

* **Titel ausblenden** - Wählen Sie diese Option, um den Titel des Komponententyps in einem adaptiven Formular auszublenden.

* **Platzhaltertext** - Platzhaltertext in einer Formularkomponente bezieht sich auf eine kurze Beschriftung oder Eingabeaufforderung, die in einem Eingabefeld angezeigt wird, um den Benutzer darauf hinzuweisen, welcher Informationstyp in dieses Feld eingegeben werden soll. Platzhaltertext verschwindet, wenn der Benutzer mit der Eingabe in das Feld beginnt, und wird wieder angezeigt, wenn das Feld leer bleibt. Es bietet einen visuellen Hinweis für den Benutzer, fungiert jedoch nicht als permanente Bezeichnung oder Wert für das Feld.

* **Komponente ausblenden** - Wählen Sie die Option, um die Komponente aus dem Formular auszublenden. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regeleditor. Dies ist nützlich, wenn Sie Informationen speichern müssen, die vom Benutzer nicht gesehen oder direkt geändert werden müssen.
* **Komponente deaktivieren** - Wählen Sie die Option zum Deaktivieren der Komponente aus. Die deaktivierte Komponente ist vom Endbenutzer nicht aktiv oder kann nicht bearbeitet werden. Der Benutzer kann den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regeleditor.
* **Schreibgeschützt** - Wählen Sie die Option aus, um die Komponente nicht bearbeitbar zu machen. Der Benutzer kann den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regeleditor.
* **Standarddatum** - Mit dieser Option können Sie dem Formularfeld ein Datum hinzufügen. Das eingegebene Datum wird standardmäßig an der Stelle der Komponente angezeigt. Wenn kein Datum vom Benutzer eingegeben wird, wird dieser Wert zum Zeitpunkt der Formularübermittlung gesendet. In diesem Fall **Komponente deaktiviert** oder **Schreibgeschützte Komponente** ausgewählt ist, wird das Standarddatum auf dem Bildschirm angezeigt und zum Zeitpunkt der Formularübermittlung gesendet.


### Registerkarte &quot;Validierung&quot; {#validation-tab}

![Registerkarte &quot;Validierung&quot;](/help/adaptive-forms/assets/datepicker_validation.png)

* **Erforderlich** - Wählen Sie diese Option, wenn Sie die Komponente in einem adaptiven Formular anzeigen möchten. Sie können die **Komponente ausblenden** oder **Komponente deaktivieren** im **Allgemein** Registerkarte angezeigt, wenn diese Option aktiviert ist.

* **Fehlermeldung** - Mit dieser Option können Sie eine Nachricht eingeben, die angezeigt wird, wenn die **Erforderlich** aktiviert ist und das Formularfeld leer bleibt.

* **Überprüfungsmeldung für Skripten** - Mit dieser Option können Sie eine Meldung eingeben, die angezeigt werden soll, wenn die Skriptvalidierung fehlschlägt.

* **Mindestdatum** - Mit dieser Option können Sie das erforderliche Mindestdatum eingeben. Wenn Sie ein Datum eingeben, das vor dem unter &quot;Mindestdatum&quot;angegebenen Datum liegt, wird eine Fehlermeldung auf dem Bildschirm angezeigt. Die **Mindestfehlermeldung** können Sie eine benutzerdefinierte Fehlermeldung hinzufügen.

* **Mindestfehlermeldung** - die **Mindestfehlermeldung** können Sie eine benutzerdefinierte Fehlermeldung hinzufügen, die angezeigt werden soll, wenn Sie ein Datum eingeben, das vor dem in der Variablen **Mindestdatum** -Option.

* **Max. Datum** - Mit dieser Option können Sie das erforderliche Höchstdatum eingeben. Wenn Sie ein Datum eingeben, das nach dem im Feld &quot;Maximum Date&quot;angegebenen Datum liegt, wird eine Fehlermeldung auf dem Bildschirm angezeigt. Die **Maximale Fehlermeldung** können Sie eine benutzerdefinierte Fehlermeldung hinzufügen.

* **Maximale Fehlermeldung** - die **Maximale Fehlermeldung** können Sie eine benutzerdefinierte Fehlermeldung hinzufügen, die angezeigt werden soll, wenn Sie ein Datum eingeben, das nach dem in der Variablen **Max. Datum** -Option.


### Registerkarte &quot;Hilfe-Inhalt&quot; {#help-content-tab}

![Registerkarte &quot;Hilfe-Inhalt&quot;](/help/adaptive-forms/assets/datepicker_helptab.png)

* **Kurzbeschreibung** - Eine kurze Beschreibung ist eine kurze Texterklärung, die zusätzliche Informationen oder Klarstellungen zum Zweck eines bestimmten Formularfelds bietet. Es hilft dem Benutzer zu verstehen, welcher Datentyp in das Feld eingegeben werden soll, und kann Richtlinien oder Beispiele bereitstellen, um sicherzustellen, dass die eingegebenen Informationen gültig sind und die gewünschten Kriterien erfüllen. Standardmäßig bleiben kurze Beschreibungen ausgeblendet. Aktivieren Sie die **Kurzbeschreibung immer anzeigen** -Option, um sie unter der Komponente anzuzeigen.

* **Kurzbeschreibung immer anzeigen**- Aktivieren Sie die Option, um die Kurzbeschreibung unter der Komponente anzuzeigen.

* **Hilfetext** - Hilfetext bezieht sich auf zusätzliche Informationen oder Anleitungen, die dem Benutzer bereitgestellt werden, um ihn beim korrekten Ausfüllen eines Formularfelds zu unterstützen. Er wird angezeigt, wenn der Benutzer auf das Hilfesymbol (i) neben der Komponente klickt. Hilfetext enthält detailliertere Informationen als die Beschriftung oder der Platzhaltertext eines Formularfelds und soll dem Benutzer dabei helfen, die Anforderungen oder Einschränkungen des Felds zu verstehen. Es kann auch Vorschläge oder Beispiele anbieten, um das Ausfüllen des Formulars zu vereinfachen und genauer zu gestalten.


### Registerkarte „Erreichbarkeit“ {#accessibility-tab}

![Registerkarte &quot;Barrierefreiheit&quot;](/help/adaptive-forms/assets/datepicker_accessibilitytab.png)

**Text für Bildschirmlesehilfen** - Text für Bildschirmlesehilfen bezieht sich auf zusätzlichen Text, der speziell für Hilfstechnologien wie Bildschirmlesehilfen vorgesehen ist, die von sehbehinderten Personen verwendet werden. Dieser Text enthält eine Audiobeschreibung des Zwecks des Formularfelds und kann Informationen über den Titel, die Beschreibung, den Namen und alle relevanten Nachrichten (benutzerdefinierten Text) des Felds enthalten. Der Text der Bildschirmlesehilfe hilft sicherzustellen, dass das Formular für alle Benutzer zugänglich ist, auch für Benutzer mit Sehbehinderungen, und bietet ihnen ein umfassendes Verständnis des Formularfelds und seiner Anforderungen.

### Registerkarte &quot;Formate&quot; {#format-tab}

![Registerkarte &quot;Formate&quot;](/help/adaptive-forms/assets/datepicker_formattab.png)

* **Anzeigeformat** - Es stellt das Datumsformat dar, das dem Benutzer angezeigt wird. Die **Typ** ermöglicht dem Benutzer die Auswahl des Datumsformats. Sie können das Datumsformat auch mithilfe des **Benutzerdefiniert** in der **Typ** Dropdown-Menü.

* **Format bearbeiten** - Es stellt ein Datumsformat dar, in dem der Benutzer das Datum bearbeiten kann. Die **Typ** ermöglicht dem Benutzer die Auswahl des Datumsformats. Sie können das Datumsformat auch mithilfe des **Benutzerdefiniert** in der **Typ** Dropdown-Menü.

* **Anzeigeformat** - Es stellt das Datumsformat dar, das dem Benutzer angezeigt wird. Mit der Option Typ kann der Benutzer das Datumsformat auswählen. Sie können das Datumsformat auch mithilfe des **Benutzerdefiniert** in der **Typ** Dropdown-Menü.

* **Format bearbeiten** - Es stellt ein Datumsformat dar, in dem der Benutzer das Datum bearbeitet. Mit der Option Typ kann der Benutzer das Datumsformat auswählen. Sie können das Datumsformat auch mithilfe des **Benutzerdefiniert** in der **Typ** Dropdown-Menü.

## Dialogfeld „Design“ {#design-dialog}

Das Dialogfeld &quot;Design&quot;wird verwendet, um CSS-Stile für die Komponente &quot;Date-Picker&quot;zu definieren und zu verwalten.

### Registerkarte „Arten“ {#styles-tab}

Die Registerkarte wird verwendet, um CSS-Stile für eine Komponente zu definieren und zu verwalten. Die Kernkomponente für die adaptive Forms-Datumsauswahl unterstützt die AEM [Stilsystem](/help/get-started/authoring.md#component-styling).

![Registerkarte &quot;Stil&quot;](/help/adaptive-forms/assets/datepicker_styletab.png)

* **Standard-CSS-Klassen**: Sie können eine standardmäßige CSS-Klasse für die Adaptive Forms-Kernkomponente zur Datumsauswahl bereitstellen.

* **Zulässige Stile**: Sie können Stile definieren, indem Sie einen Namen und die CSS-Klasse angeben, die den Stil darstellt. Sie können beispielsweise einen Stil mit dem Namen &quot;fett Text&quot;erstellen und die CSS-Klasse &quot;font-weight: fett&quot;. Sie können diese Stile im adaptiven Forms-Editor verwenden oder auf ein adaptives Formular anwenden. Um einen Stil anzuwenden, wählen Sie im adaptiven Forms-Editor die Komponente aus, auf die Sie den Stil anwenden möchten, navigieren Sie zum Dialogfeld &quot;Eigenschaften&quot;und wählen Sie den gewünschten Stil aus dem **Stile** Dropdown-Liste. Wenn Sie die Stile aktualisieren oder ändern müssen, kehren Sie einfach zum Dialogfeld &quot;Design&quot;zurück, aktualisieren Sie die Stile auf der Registerkarte &quot;Stile&quot;und speichern Sie die Änderungen.

### Registerkarte &quot;Formate&quot; {#formats-tab}

Auf der Registerkarte &quot;Formate&quot;können Sie standardmäßige und benutzerdefinierte Datumsformate angeben.

![Formatregisterkarte](/help/adaptive-forms/assets/datepicker_formatpolicy.png)

