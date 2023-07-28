---
title: Kernkomponente „Datumsauswahl“ für adaptive Formulare
description: Verwenden oder Anpassen der Datumsauswahl-Kernkomponente in adaptiven Formularen.
role: Architect, Developer, Admin, User
exl-id: aa9402de-ca57-4c19-8d36-2dd0a78d6806
source-git-commit: 7888cfa0f1358ce8018fc1e3cc3b19eb66a82b9d
workflow-type: ht
source-wordcount: '1702'
ht-degree: 100%

---

# Datumsauswahl {#date-picker-adaptive-forms-core-component}

Datumsauswahl-Komponenten in einem adaptiven Formular sind Elemente der Benutzeroberfläche, mit denen Benutzende ein Datum aus einem Kalender auswählen oder manuell ein Datum in einem bestimmten Format eingeben können. Sie können die Datumsauswahl-Komponente so konfigurieren, dass sie unterschiedliche Formatierungen, Validierungen und Standardwerte aufweist.

**Beispiel**

![](/help/adaptive-forms/assets/date-picker.png)

## Verwendung {#reasons-to-use-drop-date-picker}

Die Verwendung der Datumsauswahl in einem adaptiven Formular kann verschiedene Vorteile haben, darunter:

* **Komfort**: Benutzende können mit einer Datumsauswahl-Komponente einfach ein Datum aus einem Kalender auswählen, ohne das Datum manuell in ein Textfeld eingeben zu müssen. Dies kann Zeit sparen und Fehler reduzieren.

* **Benutzererlebnis**: Sie können mit der Datumsauswahl-Komponente das Formular benutzerfreundlicher gestalten, indem Sie eine klare und intuitive Methode zur Auswahl des Datums bereitstellen.

* **Datenanalyse**: Die Datumsauswahl-Komponente kann verwendet werden, um Daten aus verschiedenen Quellen zu erfassen und zu analysieren oder sie als Eingabe für die weitere Verarbeitung zu verwenden.

* **Event-Management**: Sie können die Datumsauswahl-Komponente auf Event-Management-Websites zur Auswahl einer Veranstaltung verwenden.

* **Buchung und Reservierung**: Die Datumsauswahl-Komponente kann auf Buchungs- und Reservierungs-Websites verwendet werden, um die Ein- und Auscheckdaten auszuwählen.

* **Datumsformat**: Sie können die Datumsauswahl-Komponente verwenden, um das Format zu korrigieren, in dem das Datum angezeigt und eingegeben wird. Stellen Sie sicher, dass das Datumsformat im gesamten Formular gleich ist, um ein konsistentes Benutzererlebnis zu gewährleisten.

## Version und Kompatibilität {#version-and-compatibility}

Die Kernkomponente „Akkordeon“ für adaptive Formulare wurde im Februar 2023 als Teil der Kernkomponenten 2.0.4 für Cloud Service und der Kernkomponenten 1.1.12 für AEM 6.5.16.0 Forms oder höher veröffentlicht. Hier finden Sie eine Tabelle mit allen unterstützten Versionen, AEM-Kompatibilität und Links zur entsprechenden Dokumentation:

| Komponentenversion | AEM as a Cloud Service | AEM 6.5.16.0 Forms oder höher |
|---|---|---|
| v1 | Kompatibel mit<br>[Version 2.0.4](/help/adaptive-forms/version.md) und höher | Kompatibel mit<br>[Version 1.1.12](/help/adaptive-forms/version.md) und höher (aber nur bis Version 2.0.0). |

Informationen zu Versionen und Freigaben der Kernkomponente finden Sie im Dokument [Kernkomponenten-Versionen](/help/adaptive-forms/version.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->


## Technische Details {#technical-details}

Die neuesten Informationen zur Datumsauswahl-Kernkomponente für adaptive Formulare erhalten Sie in der technischen Dokumentation auf [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/datepicker/v1/datepicker). Sie finden weitere Informationen zur Entwicklung von Kernkomponenten in der [Entwicklerdokumentation für Kernkomponenten](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Sie können die Datumsauswahl im Dialogfeld „Konfigurieren“ einfach anpassen. Sie können auch Optionen für die Datumsauswahl definieren, um das Benutzererlebnis zu verbessern.

### Registerkarte „Allgemein“ {#basic-tab}

![Registerkarte „Allgemein“](/help/adaptive-forms/assets/datepicker_basictab.png)

* **Name**: Durch den Namen wird die Komponente im Regel-Editor eindeutig identifiziert. Sonderzeichen und Leerzeichen sind im Namen nicht zulässig.

* **Titel**: Titel ist eine Zeichenfolge, die in einem adaptiven Formular oberhalb einer Komponente angezeigt wird. Der Titel identifiziert die Komponente eindeutig in der Baumstruktur eines adaptiven Formulars. Wenn Sie keinen Titel hinzufügen, wird der Name der Komponente anstelle des Titeltexts angezeigt.

* **Titel ausblenden**: Wählen Sie diese Option, um den Titel des Komponententyps in einem adaptiven Formular auszublenden.

* **Platzhaltertext**: Platzhaltertext in einer Formularkomponente ist eine kurze Beschriftung oder Eingabeaufforderung in einem Eingabefeld, um Benutzende darüber zu informieren, welchen Text sie in dieses Feld eingeben sollen. Der Platzhaltertext verschwindet, wenn Benutzende mit der Eingabe in das Feld beginnen, und erscheint wieder, wenn das Feld leer bleibt. Er stellt einen visuellen Hinweis für Benutzende bereit, fungiert jedoch nicht als permanente Beschriftung oder Wert für das Feld.

* **Komponente ausblenden**: Wählen Sie diese Option, um die Komponente im Formular auszublenden. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor. Dies ist nützlich, wenn Sie Informationen speichern müssen, die Benutzende nicht sehen oder direkt ändern müssen.
* **Komponente deaktivieren**: Wählen Sie die Option zum Deaktivieren der Komponente aus. Die deaktivierte Komponente ist nicht aktiv und Endbenutzende können sie nicht bearbeiten. Benutzende können den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor.
* **Schreibgeschützt**: Wählen Sie die Option aus, um die Komponente nicht bearbeitbar zu machen. Benutzende können den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor.
* **Standarddatum**: Mit dieser Option können Sie dem Formularfeld ein Datum hinzufügen. Das eingegebene Datum wird standardmäßig an der Stelle der Komponente angezeigt. Wird kein Datum eingegeben, wird bei der Formularübermittlung dieser Wert gesendet. Wenn **Deaktiverte Komponente** oder **Schreibgeschützte Komponente** ausgewählt wird, wird das Standarddatum auf dem Bildschirm angezeigt und bei der Formularübermittlung gesendet.


### Registerkarte „Validierung“ {#validation-tab}

![Registerkarte „Validierung“](/help/adaptive-forms/assets/datepicker_validation.png)

* **Erforderlich**: Wählen Sie diese Option, wenn Sie die Komponente in einem adaptiven Formular anzeigen möchten. Wenn diese Option aktiviert ist, kann die Option **Komponente ausblenden** oder **Komponente deaktivieren** auf der Registerkarte **Allgemein** nicht ausgewählt werden.

* **Fehlermeldung**: Mit dieser Option können Sie eine Nachricht eingeben, die angezeigt wird, wenn das Kontrollkästchen **Erforderlich** aktiviert ist und das Feld leer bleibt.

* **Meldung zur Skriptvalidierung**: Mit dieser Option können Sie eine Meldung eingeben, die angezeigt wird, wenn die Skriptvalidierung fehlschlägt.

* **Mindestdatum** – Sie können mit dieser Option das erforderliche Mindestdatum eingeben. Wenn Sie ein Datum eingeben, das vor dem in „Mindestdatum“ angegebenen Datum liegt, erscheint eine Fehlermeldung auf dem Bildschirm. Sie können der **Mindest-Fehlermeldung** eine benutzerdefinierte Fehlermeldung hinzufügen.

* **Mindest-Fehlermeldung** – Sie können der **Mindest-Fehlermeldung** eine benutzerdefinierte Fehlermeldung hinzufügen, die angezeigt wird, wenn Sie ein Datum eingeben, das vor dem in der Option **Mindestdatum** angegebenen liegt.

* **Maximales Datum** – Sie können mit dieser Option das maximale Datum eingeben. Wenn Sie ein Datum eingeben, das nach dem in „Maximales Datum“ angegebenen Datum liegt, erscheint eine Fehlermeldung auf dem Bildschirm. Sie können im Dialog **Maximal-Fehlermeldung** eine benutzerdefinierte Fehlermeldung hinzufügen.

* **Maximal-Fehlermeldung** – Sie können im Dialogfeld **Maximal-Fehlermeldung** eine benutzerdefinierte Fehlermeldung hinzufügen, die angezeigt wird, wenn Sie ein Datum eingeben, das nach der Option **Maximales Datum** liegt.


### Registerkarte „Hilfe-Inhalt“ {#help-content-tab}

![Registerkarte „Hilfe-Inhalt“](/help/adaptive-forms/assets/datepicker_helptab.png)

* **Kurzbeschreibung**: Eine Kurzbeschreibung ist eine kurze Erklärung, die zusätzliche Informationen oder Klarstellungen über den Zweck eines Formularfelds bietet. Es hilft Benutzenden zu verstehen, welcher Datentyp in das Feld eingegeben werden soll, und kann Richtlinien oder Beispiele bereitstellen, um sicherzustellen, dass die eingegebenen Informationen gültig sind und die gewünschten Kriterien erfüllen. Standardmäßig bleiben kurze Beschreibungen ausgeblendet. Aktivieren Sie die Option **Kurzbeschreibung immer anzeigen**, um sie unterhalb der Komponente anzuzeigen.

* **Kurzbeschreibung immer anzeigen** – Aktivieren Sie die Option, um die Kurzbeschreibung unterhalb der Komponente anzuzeigen.

* **Hilfetext**: Hilfetext bezieht sich auf zusätzliche Informationen oder Anleitungen, die den Benutzenden bereitgestellt werden, um sie beim korrekten Ausfüllen eines Formularfelds zu unterstützen. Er erscheint, wenn Benutzende auf das Hilfesymbol (i) neben der Komponente klicken. Hilfetext enthält detailliertere Informationen als die Beschriftung oder der Platzhaltertext eines Formularfelds und soll den Benutzenden dabei helfen, die Anforderungen oder Einschränkungen des Felds zu verstehen. Er kann auch Vorschläge oder Beispiele anbieten, um das Ausfüllen des Formulars einfacher und genauer zu gestalten.


### Registerkarte „Barrierefreiheit“ {#accessibility-tab}

![Registerkarte „Barrierefreiheit“](/help/adaptive-forms/assets/datepicker_accessibilitytab.png)

**Text für Bildschirmlesehilfen** – Das ist zusätzlicher Text, der von Hilfstechnologien wie etwa Bildschirmlesehilfen für sehbehinderte Personen vorgelesen wird. Dieser Text enthält eine Audiobeschreibung des Zwecks des Formularfelds und kann Informationen über den Titel, die Beschreibung, den Namen und alle relevanten Nachrichten (benutzerdefinierten Text) des Felds enthalten. Der Text der Bildschirmlesehilfe hilft sicherzustellen, dass das Formular allen Benutzenden zugänglich ist, auch Personen mit Sehschwäche, und bietet ihnen ein umfassendes Verständnis des Formularfelds und seiner Anforderungen.

### Registerkarte „Formate“ {#format-tab}

![Registerkarte „Formate“](/help/adaptive-forms/assets/datepicker_formattab.png)

* **Anzeigeformat** – Stellt das Format dar, in dem das Datum angezeigt wird. Die Option **Typ** ermöglicht die Auswahl des Datumsformats. Sie können das Datumsformat auch mithilfe der Option **Benutzerdefiniert** im Dropdown-Menü **Typ** anpassen.

* **Format bearbeiten** – Stellt ein Datumsformat dar, in dem das Datum bearbeitet werden kann. Die Option **Typ** ermöglicht die Auswahl des Datumsformats. Sie können das Datumsformat auch mithilfe der Option **Benutzerdefiniert** im Dropdown-Menü **Typ** anpassen.

* **Anzeigeformat** – Stellt das Format dar, in dem das Datum angezeigt wird. Mit der Option „Typ“ können Sie das Datumsformat auswählen. Sie können das Datumsformat auch mithilfe der Option **Benutzerdefiniert** im Dropdown-Menü **Typ** anpassen.

* **Format bearbeiten** – Stellt ein Datumsformat dar, in dem Sie das Datum bearbeiten können. Mit der Option „Typ“ können Sie das Datumsformat auswählen. Sie können das Datumsformat auch mithilfe der Option **Benutzerdefiniert** im Dropdown-Menü **Typ** anpassen.

## Dialogfeld „Design“ {#design-dialog}

Das Dialogfeld „Design“ wird verwendet, um CSS-Stile für die Komponente „Datumsauswahl“ zu definieren und zu verwalten.

### Registerkarte „Stile“ {#styles-tab}

Sie können die Registerkarte zum Definieren und Verwalten von CSS-Stilen für eine Komponente verwenden. Die Kernkomponente „Datumsauswahl“ in adaptiven Formularen unterstützt das [Stilsystem](/help/get-started/authoring.md#component-styling) von AEM.

![Registerkarte „Stile“](/help/adaptive-forms/assets/datepicker_styletab.png)

* **Standard-CSS-Klassen**: Sie können für die Datumsauswahl-Kernkomponente in adaptiven Formularen eine Standard-CSS-Klasse bereitstellen.

* **Zulässige Stile**: Sie können Stile definieren, indem Sie den Namen und die CSS-Klasse für den Stil angeben. Sie können beispielsweise einen Stil mit dem Namen „Fettschrift“ erstellen und die CSS-Klasse „Schriftbreite: Fett“ bereitstellen. Sie können diese Stile bei einem adaptiven Formular im adaptiven Formular-Editor anwenden. Um einen Stil anzuwenden, wählen Sie im Editor für adaptive Formulare die Komponente aus, auf die Sie den Stil anwenden möchten, navigieren Sie zum Eigenschaften-Dialog und wählen Sie den gewünschten Stil aus der Dropdown-Liste **Stile**. Wenn Sie die Stile aktualisieren oder ändern müssen, kehren Sie einfach zum Dialogfeld „Design“ zurück, aktualisieren die Stile auf der Registerkarte „Stile“ und speichern die Änderungen.

### Registerkarte „Formate“ {#formats-tab}

Auf der Registerkarte „Formate“ können Sie standardmäßige und benutzerdefinierte Datumsformate angeben.

![Registerkarte „Format“](/help/adaptive-forms/assets/datepicker_formatpolicy.png)

## Verwandter Artikel {#related-article}

* [Erstellen eines adaptiven Formulars in einer AEM Sites-Seite oder einem Experience Fragment](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=de)

* [Erstellen eines eigenständigen adaptiven Formulars](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html?lang=de)
