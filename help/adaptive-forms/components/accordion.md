---
title: Akkordeon für adaptive Formulare
description: Verwenden Sie Akkordeon, um ein langes oder komplexes Formular zu organisieren und zu vereinfachen, indem Sie es in kleinere, besser verwaltbare Abschnitte unterteilen.
role: Architect, Developer, Admin, User
exl-id: 0ed38eee-fc22-4708-82eb-3fb1839b1ff2
source-git-commit: 0cfdc56fe5508e156eee2ae818be311748af7247
workflow-type: ht
source-wordcount: '1677'
ht-degree: 100%

---

# Akkordeon-Komponente  {#accordion-component-adaptive-forms-core-component}

Mit der Akkordeon-Kernkomponente können Benutzende erweiterbare und ausblendbare Abschnitte in einem adaptiven Formular erstellen. Es wird häufig verwendet, um lange oder komplexe Formulare zu organisieren und zu vereinfachen, indem sie in kleinere, besser verwaltbare Abschnitte unterteilt werden. Jeder Abschnitt eines Akkordeons wird in der Regel durch eine Kopfzeile dargestellt, auf die Benutzende klicken können, um den entsprechenden Inhalt zu erweitern oder auszublenden. Der Inhalt kann eine beliebige Kernkomponente sein.

## Verwendung {#usage}

Es gibt mehrere Gründe, warum es sinnvoll ist, ein Akkordeon in ein adaptives Formular einzuschließen, darunter:

* **Platzeinsparung**: Benutzende können mit einem Akkordeon Abschnitte eines Formulars erweitern und ausblenden und so den Platz reduzieren, der zum Anzeigen aller Formularfelder auf einmal benötigt wird.

* **Navigation**: Sie können ein Akkordeon verwenden, um eine hierarchische Navigationsstruktur zu erstellen, die es Benutzenden erleichtert, die benötigten Formularfelder zu finden.

* **Benutzererlebnis**: Sie können Akkordeon verwenden, um das Formular benutzerfreundlicher zu gestalten, indem es Benutzenden eine klare und intuitive Möglichkeit bietet, auf Formularfelder zuzugreifen und sie auszufüllen.

* **Lange Formulare**: Akkordeon ist eine ideale Komponente für die Verarbeitung langer Formulare, da sich Benutzende dadurch auf einen Abschnitt auf einmal konzentrieren können, anstatt zu versuchen, viele Informationen gleichzeitig zu verarbeiten.

Sie können Folgendes verwenden:

* Im [Konfigurieren-Dialogfeld](#configure-dialog) können Sie Eigenschaften der Akkordeon-Komponente angeben.

* Sie können das [Popover „Bedienfeld auswählen“](#select-panel-popover) verwenden, um die Reihenfolge der Bedienfelder des Akkordeons zu definieren. Dadurch kann der Autor die Bedienfelder in der Reihenfolge anordnen, in der sie angezeigt werden sollen.

* Optionen für Formularautorinnen und -autoren zum Aktivieren oder Deaktivieren bestimmter Funktionen in [Dialogfeld „Design“](#design-dialog). Eine Autorin oder ein Autor kann beispielsweise bestimmte Felder oder Abschnitte eines Formulars deaktivieren. Diese Optionen ermöglichen es der Autorin oder dem Autor, den Entwurf und die Funktionen des Formulars besser zu steuern, wodurch es einfacher wird, Formulare zu erstellen, die auf die spezifischen Anforderungen des Unternehmens zugeschnitten sind.

Das Dialogfeld „Konfigurieren“ und das Popover „Bedienfeld auswählen“, sowie das Dialogfeld „Design“ sind alle Teil der Kernkomponenten, die erstellt wurden, um das Authoring der Formulare zu vereinfachen und eine effiziente Methode zum Erstellen komplexer Formulare bereitzustellen.

## Version und Kompatibilität {#version-and-compatibility}

Die Kernkomponente „Akkordeon“ für adaptive Formulare wurde im Februar 2023 als Teil der Kernkomponenten 2.0.4 für Cloud Service und der Kernkomponenten 1.1.12 für AEM 6.5.16.0 Forms oder höher veröffentlicht. Hier finden Sie eine Tabelle mit allen unterstützten Versionen, AEM-Kompatibilität und Links zur entsprechenden Dokumentation:

| Komponentenversion | AEM as a Cloud Service | AEM 6.5.16.0 Forms oder höher |
|---|---|---|
| v1 | Kompatibel mit<br>[Version 2.0.4](/help/adaptive-forms/version.md) und höher | Kompatibel mit<br>[Version 1.1.12](/help/adaptive-forms/version.md) und höher (aber nur bis Version 2.0.0). |

Informationen zu Versionen und Freigaben der Kernkomponente finden Sie im Dokument [Kernkomponenten-Versionen](/help/adaptive-forms/version.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technische Details {#technical-details}

Aktuelle Informationen zur Akkordeon-Komponente finden Sie in der technischen Dokumentation auf [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/accordion/v1/accordion). Sie finden weitere Informationen zur Entwicklung von Kernkomponenten in der [Entwicklerdokumentation für Kernkomponenten](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Sie können das Akkordeon-Erlebnis für Besuchende im Dialogfeld „Konfigurieren“ einfach anpassen. Sie können auch Akkordeon-Elemente, Bedienfelder, Verhalten und Erscheinungsbild problemlos für ein nahtloses Benutzererlebnis definieren.

### Registerkarte „Allgemein“ {#basic-tab}

![Registerkarte „Allgemein“](/help/adaptive-forms/assets/accordion_basictab.png)

* **Name**: Sie können eine Formularkomponente sowohl im Formular als auch im Regel-Editor leicht mit ihrem eindeutigen Namen identifizieren. Der Name darf jedoch keine Leerzeichen oder Sonderzeichen enthalten.

* **Titel**: Sie können mit dem Titel leicht eine Komponente in einem Formular identifizieren. Standardmäßig wird der Titel über der Komponente angezeigt. Wenn Sie keinen Titel hinzufügen, wird der Name der Komponente anstelle des Titeltexts angezeigt.

* **Titel ausblenden**: Wählen Sie die Option aus, um den Titel der Komponente auszublenden.

* **Daten in Objekt aufnehmen**: Wählen Sie „Daten in ein Objekt aufnehmen“ aus, um die Felddaten aus dem Assistenten in ein JSON-Objekt einzufügen. Wenn diese Option nicht ausgewählt ist, hat die JSON-Datei „Daten senden“ eine flache Struktur für die Felder des Assistenten.

* **Layout**: Sie können für Ihren Assistenten entweder ein festes Layout (einfach) oder ein flexibles Layout (responsives Raster) verwenden. Das einfache Layout behält alles fest an der Stelle, während Sie mit dem responsiven Raster die Position der Komponenten an Ihre Bedürfnisse anpassen können. Verwenden Sie beispielsweise das responsive Raster, um „Vorname“, „Mittelname“ und „Nachname“ in einem Formular in einer einzigen Zeile auszurichten.

* **Bindungsverweis**: Bindungsverweis ist ein Verweis auf ein Datenelement, das in einer externen Datenquelle gespeichert ist und in einem Formular verwendet wird. Sie können mit dem Bindungsverweis Daten dynamisch an Formularfelder binden, sodass das Formular die aktuellsten Daten aus der Datenquelle anzeigen kann. Beispielsweise kann ein Bindungsverweis verwendet werden, um den Namen und die Adresse von Kundinnen und Kunden in einem Formular anzuzeigen, basierend auf der im Formular eingegebenen Kunden-ID. Der Bindungsverweis kann auch verwendet werden, um die Datenquelle mit den im Formular eingegebenen Daten zu aktualisieren. Auf diese Weise können Sie mit AEM Forms Formulare erstellen, die mit externen Datenquellen interagieren und so eine nahtlose Benutzererfahrung bei der Datenerfassung und Datenverwaltung bieten.
* **Komponente ausblenden**: Wählen Sie die Option, um die Komponente aus dem Formular auszublenden. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor. Dies ist nützlich, wenn Sie Informationen speichern müssen, die Benutzende nicht sehen oder direkt ändern müssen.
* **Komponente deaktivieren**: Wählen Sie die Option zum Deaktivieren der Komponente aus. Die deaktivierte Komponente ist nicht aktiv und Endbenutzende können sie nicht bearbeiten. Benutzende können den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor.

### Registerkarte „Elemente“ {#items-tab}

![Registerkarte „Elemente“](/help/adaptive-forms/assets/accordion_itemstab.png)

Mit der Hinzufügen-Schaltfläche können Sie eine Komponente auswählen, die als Bedienfeld im Fenster „Komponentenauswahl“ hinzugefügt werden soll. Nach dem Hinzufügen der Komponente werden die folgenden Optionen angezeigt:

* **Symbol**: Das Symbol identifiziert die Komponente des Bedienfelds in der Liste. Sie können den Mauszeiger über das Symbol bewegen, um den vollständigen Komponentennamen als QuickInfo anzuzeigen.
* **Beschreibung**: Die Beschreibung, die als Text des Bedienfelds verwendet wird. Standardmäßig wird der Name der Komponente für das Bedienfeld ausgewählt.
* **Entfernen** - Tippen oder klicken Sie, um das Bedienfeld aus der Akkordeon-Komponente zu löschen.
* **Neu anordnen** - Tippen oder klicken und ziehen Sie, um die Reihenfolge der Bedienfelder neu anzuordnen.

### Registerkarte „Hilfe-Inhalt“ {#help-content}

![Registerkarte „Hilfe-Inhalt“](/help/adaptive-forms/assets/accordion_helpcontent.png)

* **Kurzbeschreibung** – Eine Kurzbeschreibung ist eine kurze Erklärung, die zusätzliche Informationen oder Klarstellungen über den Zweck eines Formularfelds bietet. Es hilft Benutzenden zu verstehen, welcher Datentyp in das Feld eingegeben werden soll, und kann Richtlinien oder Beispiele bereitstellen, um sicherzustellen, dass die eingegebenen Informationen gültig sind und die gewünschten Kriterien erfüllen. Standardmäßig bleiben kurze Beschreibungen ausgeblendet. Aktivieren Sie die Option **Kurzbeschreibung immer anzeigen**, um sie unterhalb der Komponente anzuzeigen.

* **Kurzbeschreibung immer anzeigen** – Aktivieren Sie diese Option, um die Kurzbeschreibung unterhalb der Komponente anzuzeigen.

* **Hilfetext** – Hilfetext bezieht sich auf zusätzliche Informationen oder Anleitungen, die den Benutzenden bereitgestellt werden, um sie beim korrekten Ausfüllen eines Formularfelds zu unterstützen. Er erscheint, wenn Benutzende auf das Hilfesymbol (i) neben der Komponente klicken. Hilfetext enthält detailliertere Informationen als die Beschriftung oder der Platzhaltertext eines Formularfelds und soll den Benutzenden dabei helfen, die Anforderungen oder Einschränkungen des Felds zu verstehen. Er kann auch Vorschläge oder Beispiele anbieten, um das Ausfüllen des Formulars einfacher und genauer zu gestalten.

### Registerkarte „Barrierefreiheit“ {#accessibility}

![Registerkarte „Barrierefreiheit“](/help/adaptive-forms/assets/accordion_accessibility.png)

**Text für Bildschirmlesehilfen** – Das ist zusätzlicher Text, der von Hilfstechnologien wie etwa Bildschirmlesehilfen für sehbehinderte Personen vorgelesen wird. Dieser Text enthält eine Audiobeschreibung des Zwecks des Formularfelds und kann Informationen über den Titel, die Beschreibung, den Namen und alle relevanten Nachrichten (benutzerdefinierten Text) des Felds enthalten. Der Text der Bildschirmlesehilfe hilft sicherzustellen, dass das Formular allen Benutzenden zugänglich ist, auch Personen mit Sehschwäche, und bietet ihnen ein umfassendes Verständnis des Formularfelds und seiner Anforderungen.

## Dialogfeld „Design“ {#design-dialog}

Im Dialogfeld „Design“ können Vorlagenerstellende steuern, wie Elemente standardmäßig angezeigt werden. Für die Akkordeon-Komponente in adaptiven Formularen können Sie Folgendes festlegen:

* Der Typ der zulässigen und als Standard festgelegten HTML-Überschriftenelemente (z. B. H1, H2, H3, usw.)
* Kernkomponenten, die Sie mit dem adaptiven Formular-Editor Akkordeon hinzufügen können
* Einfache Namen für Stile (CSS-Klassen), die Sie im Dialogfeld „Eigenschaften“ der Akkordeon-Komponente im adaptiven Formular-Editor anwenden können.

Dadurch wird das Erstellen und Anpassen von Formularen einfacher und effizienter.

### Registerkarte „Eigenschaften“ {#properties-tab-design}

Auf der Registerkarte &quot;Eigenschaften&quot; können Vorlagenautorinnen und -autoren standardmäßige und zulässige HTML-Überschriftenelemente für Formularautorinnen und -autoren festlegen:

![Registerkarte „Eigenschaften“ im Dialogfeld „Design“](/help/assets/accordion-design-properties.png)

* **Zulässige Überschriftenelemente**: Dropdown-Liste mit mehreren Optionen, über die Vorlagenautorinnen und -autoren auswählen können, welche Überschriftenelemente der Formularautor für das Akkordeon verwenden kann.

* **Standardüberschriftenelement**: Eine Dropdown-Liste legt das standardmäßige Überschriftenelement für die Akkordeon-Komponente fest.

### Registerkarte „Zugelassene Komponenten“ {#allowed-components-tab}

Die **Zugelassene Komponenten**-Registerkarte ermöglicht es dem Vorlagen-Editor, die Komponenten festzulegen, die den Bedienfeldern in der Akkordeon-Komponente im adaptiven Formular-Editor als Elemente hinzugefügt werden können.

![Registerkarte „Zugelassene Komponenten“](/help/adaptive-forms/assets/accordion_allowedcomponents.png)

### Registerkarte „Stile“ {#styles-tab}

Sie können die Registerkarte zum Definieren und Verwalten von CSS-Stilen für eine Komponente verwenden. Die Kernkomponente „Akkordeon“ in adaptiven Formularen unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).

![Registerkarte „Stile“](/help/adaptive-forms/assets/accordion_style.png)

* **Standard-CSS-Klassen**: Sie können eine standardmäßige CSS-Klasse für die Akkordeon-Komponente bereitstellen.

* **Zulässige Stile**: Sie können Stile definieren, indem Sie einen Namen und die CSS-Klasse angeben, die den Stil darstellen. Sie können beispielsweise einen Stil mit dem Namen „Fettschrift“ erstellen und die CSS-Klasse „Schriftbreite: Fett“ bereitstellen. Sie können diese Stile bei einem adaptiven Formular im adaptiven Formular-Editor anwenden. Um einen Stil anzuwenden, wählen Sie im Editor für adaptive Formulare die Komponente aus, auf die Sie den Stil anwenden möchten, navigieren Sie zum Eigenschaften-Dialog und wählen Sie den gewünschten Stil aus der Dropdown-Liste **Stile**. Wenn Sie die Stile aktualisieren oder ändern müssen, kehren Sie einfach zum Dialogfeld „Design“ zurück, aktualisieren die Stile auf der Registerkarte „Stile“ und speichern die Änderungen.

