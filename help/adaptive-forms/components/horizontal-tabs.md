---
title: Kernkomponente „Horizontale Registerkarten“ für adaptive Formulare
description: Verwenden oder Anpassen der Kernkomponente „Horizontale Registerkarten“ für adaptive Formulare.
role: Architect, Developer, Admin, User
exl-id: fbdf330b-3b85-4f94-9dab-eea8465fba67
source-git-commit: d2a6108f17f6e0c6b91bec84893d64a8bd48effd
workflow-type: tm+mt
source-wordcount: '1609'
ht-degree: 91%

---

# Horizontale Registerkarten {#horizontal-tabs-adaptive-forms-core-component}

Horizontale Registerkarten in adaptiven Formularen sind so aufgebaut, dass mehrere Abschnitte eines Formulars gruppiert und als separate, horizontal ausgerichtete Registerkarten angezeigt werden. Benutzende können zwischen den Registerkarten wechseln, um auf verschiedene Abschnitte des Formulars zuzugreifen. Jede Registerkarte dient als Auslöser zum Anzeigen und Ausblenden des jeweiligen Formularinhalts. Mit horizontalen Registerkarten können Sie lange Formulare in überschaubare Abschnitte organisieren und das Benutzererlebnis verbessern. Registerkarten können ein Formular für Benutzende mit Behinderungen barrierefreier gestalten, da sie mithilfe der Tastaturnavigation zwischen Abschnitten wechseln können.

Die Registerkarten bestehen in der Regel aus einer Reihe von Links oder Schaltflächen, wobei jeder Link oder jede Schaltfläche einem Abschnitt des Formulars entspricht. Wenn Benutzende auf eine Registerkarte klicken, wird der Formularinhalt dynamisch aktualisiert und der entsprechende Abschnitt wird angezeigt.

## Verwendung {#reasons-to-use-horizontal-tabs}

Die häufigsten Gründe für die Verwendung horizontaler Registerkarten in einem adaptiven Formular sind:

* **Verbesserte Benutzerfreundlichkeit**: Horizontale Registerkarten erleichtern Benutzenden die Navigation durch das Formular, insbesondere wenn das Formular mehrere Abschnitte oder eine große Anzahl von Feldern enthält.

* **Platz-Management**: Horizontale Registerkarten sparen Platz auf dem Bildschirm, indem sie verwandte Formularabschnitte in Registerkarten gruppieren und jeweils nur einen Abschnitt anzeigen.

* **Bessere Organisation**: Registerkarten bieten eine klare und übersichtliche Struktur für ein Formular, sodass Benutzende das Formular besser verstehen und ausfüllen können.

* **Erhöhte Benutzerinteraktion**: Horizontale Registerkarten können ein Formular für Benutzende visuell ansprechender und interessanter gestalten, wodurch die Formularausfüllungsrate verbessert werden kann.

## Version und Kompatibilität {#version-and-compatibility}

Die Kernkomponente &quot;Adaptive Forms Accordion&quot;wurde im Februar 2023 als Teil der Kernkomponenten 2.0.4 für Cloud Service und Kernkomponenten 1.1.12 für AEM 6.5.16.0 Forms oder höher veröffentlicht. In der folgenden Tabelle finden Sie alle unterstützten Versionen, AEM Kompatibilität und Links zur entsprechenden Dokumentation:

| Komponentenversion | AEM as a Cloud Service | AEM 6.5.16.0 Forms oder höher |
|---|---|---|
| v1 | Kompatibel mit<br>[Version 2.0.4](/help/adaptive-forms/version.md) und höher | Kompatibel mit<br>[Version 1.1.12](/help/adaptive-forms/version.md) und höher, jedoch weniger als 2.0.0. |

Informationen zu Versionen und Freigaben der Kernkomponente finden Sie im Dokument [Kernkomponenten-Versionen](/help/adaptive-forms/version.md).


<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->


## Technische Details {#technical-details}

Die neuesten Informationen zur Kernkomponente „Horizontale Registerkarten“ für adaptive Formulare erfahren Sie in der technischen Dokumentation auf [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/pageHorizontal tabs/v1/pageHorizontal tabs). Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Entwicklerdokumentation für Kernkomponenten](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Im Konfigurieren-Dialogfeld können Sie die horizontalen Registerkarten einfach anpassen. Sie können auch Optionen für horizontale Registerkarten definieren, um das Benutzererlebnis zu verbessern.

### Registerkarte „Allgemein“ {#basic-tab}

![Registerkarte „Allgemein“](/help/adaptive-forms/assets/tabsontop_basictab.png)

* **Name**: Sie können eine Formularkomponente sowohl im Formular als auch im Regel-Editor leicht mit ihrem eindeutigen Namen identifizieren. Der Name darf jedoch keine Leerzeichen oder Sonderzeichen enthalten.

* **Titel**: Sie können mit dem Titel leicht eine Komponente in einem Formular identifizieren. Standardmäßig wird der Titel über der Komponente angezeigt. Wenn Sie keinen Titel hinzufügen, wird der Name der Komponente anstelle des Titeltexts angezeigt.

* **Titel ausblenden**: Wählen Sie die Option aus, um den Titel der Komponente auszublenden.

* **Daten in Objekt aufnehmen**: Wählen Sie „Daten in ein Objekt aufnehmen“ aus, um die Felddaten aus dem Assistenten in ein JSON-Objekt einzufügen. Wenn diese Option nicht ausgewählt ist, hat die JSON-Datei „Daten senden“ eine flache Struktur für die Felder des Assistenten.

* **Layout**: Sie können für Ihren Assistenten entweder ein festes Layout (einfach) oder ein flexibles Layout (responsives Raster) verwenden. Das einfache Layout behält alles fest an der Stelle, während Sie mit dem responsiven Raster die Position der Komponenten an Ihre Bedürfnisse anpassen können. Verwenden Sie beispielsweise das responsive Raster, um „Vorname“, „Mittelname“ und „Nachname“ in einem Formular in einer einzigen Zeile auszurichten.

* **Bindungsverweis**: Bindungsverweis ist ein Verweis auf ein Datenelement, das in einer externen Datenquelle gespeichert ist und in einem Formular verwendet wird. Sie können mit dem Bindungsverweis Daten dynamisch an Formularfelder binden, sodass das Formular die aktuellsten Daten aus der Datenquelle anzeigen kann. Beispielsweise kann ein Bindungsverweis verwendet werden, um den Namen und die Adresse von Kundinnen und Kunden in einem Formular anzuzeigen, basierend auf der im Formular eingegebenen Kunden-ID. Der Bindungsverweis kann auch verwendet werden, um die Datenquelle mit den im Formular eingegebenen Daten zu aktualisieren. Auf diese Weise können Sie mit AEM Forms Formulare erstellen, die mit externen Datenquellen interagieren und so eine nahtlose Benutzererfahrung bei der Datenerfassung und Datenverwaltung bieten.
* **Komponente ausblenden**: Wählen Sie die Option, um die Komponente aus dem Formular auszublenden. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor. Dies ist nützlich, wenn Sie Informationen speichern müssen, die Benutzende nicht sehen oder direkt ändern müssen.
* **Komponente deaktivieren**: Wählen Sie die Option zum Deaktivieren der Komponente aus. Die deaktivierte Komponente ist nicht aktiv und Endbenutzende können sie nicht bearbeiten. Benutzende können den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor.

### Registerkarte „Elemente“ {#items-tab}

![Registerkarte „Elemente“](/help/adaptive-forms/assets/tabsontop_itemstab.png)

Mit der Schalfläche **Hinzufügen** können Sie eine Komponente vom Komponentenauswahl-Fenster auswählen und als Bedienfeld hinzufügen. Nach dem Hinzufügen der Komponente werden die folgenden Optionen angezeigt:

* **Symbol**: Das Symbol identifiziert die Komponente des Bedienfelds in der Liste. Sie können den Mauszeiger über das Symbol bewegen, um den vollständigen Komponentennamen als QuickInfo anzuzeigen.
* **Beschreibung** – Die Beschreibung, die als Text des Bedienfelds verwendet wird. Standardmäßig der Name der für das Bedienfeld ausgewählten Komponente.
* **Löschen** - Tippen oder klicken Sie, um das Bedienfeld aus der Komponente der horizontalen Registerkarte zu löschen.
* **Neu anordnen**: Tippen oder klicken und ziehen Sie, um die Reihenfolge der Bedienfelder neu anzuordnen.

### Registerkarte „Hilfe-Inhalt“ {#help-content}

![Registerkarte „Hilfe-Inhalt“](/help/adaptive-forms/assets/tabsontop_helptab.png)

* **Kurzbeschreibung** – Eine Kurzbeschreibung ist eine kurze Erklärung, die zusätzliche Informationen oder Klarstellungen über den Zweck eines Formularfelds bietet. Es hilft Benutzenden zu verstehen, welcher Datentyp in das Feld eingegeben werden soll, und kann Richtlinien oder Beispiele bereitstellen, um sicherzustellen, dass die eingegebenen Informationen gültig sind und die gewünschten Kriterien erfüllen. Standardmäßig bleiben kurze Beschreibungen ausgeblendet. Aktivieren Sie die Option **Kurzbeschreibung immer anzeigen**, um sie unterhalb der Komponente anzuzeigen.

* **Kurzbeschreibung immer anzeigen** – Aktivieren Sie diese Option, um die Kurzbeschreibung unterhalb der Komponente anzuzeigen.

* **Hilfetext** – Hilfetext bezieht sich auf zusätzliche Informationen oder Anleitungen, die den Benutzenden bereitgestellt werden, um sie beim korrekten Ausfüllen eines Formularfelds zu unterstützen. Er erscheint, wenn Benutzende auf das Hilfesymbol (i) neben der Komponente klicken. Hilfetext enthält detailliertere Informationen als die Beschriftung oder der Platzhaltertext eines Formularfelds und soll den Benutzenden dabei helfen, die Anforderungen oder Einschränkungen des Felds zu verstehen. Er kann auch Vorschläge oder Beispiele anbieten, um das Ausfüllen des Formulars einfacher und genauer zu gestalten.

### Registerkarte „Barrierefreiheit“ {#accessibility}

![Registerkarte „Barrierefreiheit“](/help/adaptive-forms/assets/tabsontop_accessibilitytab.png)

* **Text für Bildschirmlesehilfen** – Das ist zusätzlicher Text, der von Hilfstechnologien wie etwa Bildschirmlesehilfen für sehbehinderte Personen vorgelesen wird. Dieser Text enthält eine Audiobeschreibung des Zwecks des Formularfelds und kann Informationen über den Titel, die Beschreibung, den Namen und alle relevanten Nachrichten (benutzerdefinierten Text) des Felds enthalten. Der Text der Bildschirmlesehilfe hilft sicherzustellen, dass das Formular allen Benutzenden zugänglich ist, auch Personen mit Sehschwäche, und bietet ihnen ein umfassendes Verständnis des Formularfelds und seiner Anforderungen.

* **HTML-Rolle für die Ankündigung durch die Bildschirmlesehilfe** – Die HTML-Rolle ist ein Attribut, mit dem der Zweck eines HTML-Elements für Hilfstechnologien wie Bildschirmlesehilfen spezifiziert wird. Rollenattribute werden verwendet, um für ein Element zusätzlichen Kontext und eine semantische Bedeutung bereitzustellen, wodurch es für Bildschirmlesehilfen einfacher wird, den Inhalt zu interpretieren und ihn Benutzenden mitzuteilen. In AEM Forms kann beispielsweise die Beschriftung eines Formularfelds die Rolle „Beschriftung“ haben und sein Eingabefeld die Rolle „Textfeld“. Dadurch kann die Bildschirmlesehilfe die Beziehung zwischen Beschrfitung und Eingabefeld verstehen und diese Informationen den Benutzenden korrekt mitteilen.

## Dialogfeld „Design“ {#design-dialog}

Im Dialogfeld „Design“ können Vorlagenerstellende steuern, wie Elemente standardmäßig angezeigt werden. Für die Adaptive Forms-Komponente können Sie Folgendes festlegen:

* Die Kernkomponenten, die ein Formularersteller den horizontalen Registerkarten im Adaptive Forms-Editor hinzufügen kann
* Einfache Namen für Stile (CSS-Klassen), die im Eigenschaftendialogfeld der Komponente für horizontale Registerkarten im Adaptive Forms-Editor angewendet werden können.

Dadurch wird das Erstellen und Anpassen von Formularen einfacher und effizienter.

### Registerkarte „Zugelassene Komponenten“ {#allowed-components-tab}

In der Registerkarte **Zugelassene Komponenten** können Vorlagen-Bearbeitende die Komponenten festlegen, die den Bedienfeldern in der Komponente „Horizontale Registerkarten“ im Editor für adaptive Formulare als Elemente hinzugefügt werden können.

![Horizontale Registerkarten](/help/adaptive-forms/assets/horizontaltabs_designdilog.png)

### Registerkarte „Stile“ {#styles-tab}

Die Registerkarte wird verwendet, um CSS-Stile für eine Komponente zu definieren und zu verwalten. Die Kernkomponente „Horizontale Registerkarten“ für adaptive Formulare unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).

![Registerkarte &quot;Stil&quot;](/help/adaptive-forms/assets/horizontaltabs_designstyletab.png)

* **Standard-CSS-Klassen**: Sie können für die Kernkomponente „Horizontale Registerkarten“ von adaptiven Formularen eine standardmäßige CSS-Klasse festlegen.

* **Zulässige Stile**: Sie können Stile definieren, indem Sie den Namen und die CSS-Klasse für den Stil angeben. Sie können beispielsweise einen Stil mit dem Namen „Fettschrift“ erstellen und die CSS-Klasse „Schriftbreite: Fett“ bereitstellen. Sie können diese Stile bei einem adaptiven Formular im adaptiven Formular-Editor anwenden. Um einen Stil anzuwenden, wählen Sie im Editor für adaptive Formulare die Komponente aus, auf die Sie den Stil anwenden möchten, navigieren Sie zum Eigenschaften-Dialog und wählen Sie den gewünschten Stil aus der Dropdown-Liste **Stile**. Wenn Sie die Stile aktualisieren oder ändern müssen, kehren Sie einfach zum Dialogfeld „Design“ zurück, aktualisieren die Stile auf der Registerkarte „Stile“ und speichern die Änderungen.
