---
title: Kernkomponente „Bedienfeld-Container“ für adaptive Formulare
description: Verwenden oder Anpassen der Kernkomponente „Bedienfeld-Container“ für adaptive Formulare.
role: Architect, Developer, Admin, User
source-git-commit: 7888cfa0f1358ce8018fc1e3cc3b19eb66a82b9d
workflow-type: tm+mt
source-wordcount: '1402'
ht-degree: 87%

---

# Bedienfeld-Container {#panel-container-adaptive-forms-core-component}

In einem adaptiven Formular ist ein Bedienfeld ein Container-Element, das zum Gruppieren verwandter Formularelemente verwendet werden kann. So können Sie verschiedene Formularelemente logisch und sinnvoll gruppieren und organisieren. Dies kann die Gesamtstruktur und Lesbarkeit des Formulars verbessern, sodass Benutzende es einfacher verstehen und leichter darin navigieren können.

Sie können Bedienfelder auch verwenden, um ausblendbare Abschnitte zu erstellen. Damit können komplexe oder weniger häufig verwendete Formularfelder ausgeblendet werden, sodass das Formular übersichtlich bleibt und leicht zu verwenden ist. Sie können auch andere Komponenten wie Text, Kontrollkästchen und Schaltflächen einbeziehen.

Sie können auch verschiedene regelbasierte Aktionen festlegen, z. B. ein Formular senden, eine Website öffnen, Komponenten ein-/ausblenden oder eine Instanz eines Bedienfelds hinzufügen.

**Beispiel**

![](/help/adaptive-forms/assets/panel-container.png)

## Verwendung {#reasons-to-use-panel-container}

Es gibt verschiedene Gründe für die Verwendung eines Bedienfelds in einem Formular, darunter:

* **Organisieren von Formularelementen**: Sie können ein Bedienfeld verwenden, um verwandte Formularelemente zusammenzufassen, sodass das Formular für Benutzende übersichtlicher und leichter zu navigieren ist.

* **Verbessern der Formularstruktur**: Sie können durch die Gruppierung von Formularelementen in Bedienfelder die Gesamtstruktur und Lesbarkeit des Formulars verbessern und es Benutzenden dadurch leichter verständlich machen.

* **Erstellen ausblendbarer Abschnitte**: Sie können Bedienfelder verwenden, um ausblendbare Abschnitte zu erstellen. Diese können für das Ausblenden komplexer oder seltener verwendeter Formularfelder nützlich sein, sodass das Formular übersichtlich bleibt und einfach zu verwenden ist.

* **Verbesserte Benutzerfreundlichkeit**: Sie können durch Verwendung von Bedienfeldern zur Organisation von Formularelementen das Formular benutzerfreundlicher und einfacher gestalten, was dazu führen kann, dass mehr Formulare ausgefüllt werden.

## Version und Kompatibilität {#version-and-compatibility}

Die Kernkomponente „Bedienfeld-Container“ für adaptive Formulare wurde im Februar 2023 als Teil der Kernkomponenten 2.0.4 veröffentlicht. Hier finden Sie eine Tabelle mit allen unterstützten Versionen, Informationen zur AEM-Kompatibilität und Links zur entsprechenden Dokumentation:

|  |  |
|---|---|
| Komponentenversion | AEM as a Cloud Service |
| --- | --- |
| v1 | Kompatibel mit<br>[Version 2.0.4](/help/versions.md) und höher | Kompatibel | Kompatibel |

Informationen zu Versionen und Freigaben der Kernkomponente finden Sie im Dokument [Kernkomponenten-Versionen](/help/versions.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technische Details {#technical-details}

Die neuesten Informationen zur Kernkomponente „Bedienfeld-Container“ für adaptive Formulare finden Sie in der technischen Dokumentation auf [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/panelcontainer/v1/panelcontainer). Sie finden weitere Informationen zur Entwicklung von Kernkomponenten in der [Entwicklerdokumentation für Kernkomponenten](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Mit dem Dialogfeld „Konfigurieren“ können Sie Bedienfeld-Container mühelos für Besuchende anpassen. Sie können auch Optionen für Bedienfeld-Container definieren, um das Benutzererlebnis zu verbessern.

### Registerkarte „Allgemein“ {#basic-tab}

![Registerkarte „Allgemein“](/help/adaptive-forms/assets/basic-panel.png)

* **Name**: Sie können eine Formularkomponente sowohl im Formular als auch im Regel-Editor leicht mit ihrem eindeutigen Namen identifizieren. Der Name darf jedoch keine Leerzeichen oder Sonderzeichen enthalten.

* **Titel**: Sie können mit dem Titel leicht eine Komponente in einem Formular identifizieren. Standardmäßig wird der Titel über der Komponente angezeigt. Wenn Sie keinen Titel hinzufügen, wird der Name der Komponente anstelle des Titeltexts angezeigt.

* **Titel ausblenden**: Wählen Sie die Option aus, um den Titel der Komponente auszublenden.

* **Daten in Objekt aufnehmen**: Wählen Sie „Daten in ein Objekt aufnehmen“ aus, um die Felddaten aus dem Assistenten in ein JSON-Objekt einzufügen. Wenn diese Option nicht ausgewählt ist, hat die JSON-Datei „Daten senden“ eine flache Struktur für die Felder des Assistenten.

* **Layout**: Sie können für Ihren Assistenten entweder ein festes Layout (einfach) oder ein flexibles Layout (responsives Raster) verwenden. Das einfache Layout behält alles fest an der Stelle, während Sie mit dem responsiven Raster die Position der Komponenten an Ihre Bedürfnisse anpassen können. Verwenden Sie beispielsweise das responsive Raster, um „Vorname“, „Mittelname“ und „Nachname“ in einem Formular in einer einzigen Zeile auszurichten.

* **Bindungsverweis**: Bindungsverweis ist ein Verweis auf ein Datenelement, das in einer externen Datenquelle gespeichert ist und in einem Formular verwendet wird. Sie können mit dem Bindungsverweis Daten dynamisch an Formularfelder binden, sodass das Formular die aktuellsten Daten aus der Datenquelle anzeigen kann. Beispielsweise kann ein Bindungsverweis verwendet werden, um den Namen und die Adresse von Kundinnen und Kunden in einem Formular anzuzeigen, basierend auf der im Formular eingegebenen Kunden-ID. Der Bindungsverweis kann auch verwendet werden, um die Datenquelle mit den im Formular eingegebenen Daten zu aktualisieren. Auf diese Weise können Sie mit AEM Forms Formulare erstellen, die mit externen Datenquellen interagieren und so eine nahtlose Benutzererfahrung bei der Datenerfassung und Datenverwaltung bieten.
* **Komponente ausblenden**: Wählen Sie die Option, um die Komponente aus dem Formular auszublenden. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor. Dies ist nützlich, wenn Sie Informationen speichern müssen, die Benutzende nicht sehen oder direkt ändern müssen.
* **Komponente deaktivieren**: Wählen Sie die Option zum Deaktivieren der Komponente aus. Die deaktivierte Komponente ist nicht aktiv und Endbenutzende können sie nicht bearbeiten. Benutzende können den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor.

### Registerkarte &quot;Bedienfeld wiederholen&quot; {#repeat-panel}

![Tab Wiederholen](/help/adaptive-forms/assets/repeat-panel.png)

Sie können die Wiederholungsoptionen verwenden, um Bedienfeldcontainer und die untergeordneten Komponenten zu duplizieren, eine minimale und maximale Wiederholungsanzahl zu definieren und die Replikation ähnlicher Abschnitte innerhalb eines Formulars zu erleichtern. Bei der Interaktion mit der Bedienfeldcontainer-Komponente und dem Zugriff auf die Einstellungen werden die folgenden Optionen angezeigt:

* **Assistent wiederholbar machen**: Eine Umschalter-Funktion, mit der Benutzer die Wiederholungsfunktion aktivieren oder deaktivieren können.
* **Mindestwiederholungen**: Legt fest, wie oft der Bedienfeldcontainer mindestens wiederholt werden kann. Der Wert null zeigt an, dass das Bedienfeld &quot;Assistent&quot;nicht wiederholt wird. der Standardwert ist null.
* **Maximale Wiederholungen**: Legt fest, wie oft der Bedienfeldcontainer maximal wiederholt werden kann. Standardmäßig ist dieser Wert unbegrenzt.

Um wiederholbare Abschnitte im Bedienfeldcontainer effektiv zu verwalten, führen Sie die Schritte aus, die im Abschnitt [Erstellen von Formularen mit wiederholbaren Abschnitten](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/create-forms-repeatable-sections.html) Artikel.

### Registerkarte „Hilfe-Inhalt“ {#help-content}

![Registerkarte „Hilfe-Inhalt“](/help/adaptive-forms/assets/helpcontent-panel.png)


* **Kurzbeschreibung** – Eine Kurzbeschreibung ist eine kurze Erklärung, die zusätzliche Informationen oder Klarstellungen über den Zweck eines Formularfelds bietet. Es hilft Benutzenden zu verstehen, welcher Datentyp in das Feld eingegeben werden soll, und kann Richtlinien oder Beispiele bereitstellen, um sicherzustellen, dass die eingegebenen Informationen gültig sind und die gewünschten Kriterien erfüllen. Standardmäßig bleiben kurze Beschreibungen ausgeblendet. Aktivieren Sie die Option **Kurzbeschreibung immer anzeigen**, um sie unterhalb der Komponente anzuzeigen.

* **Kurzbeschreibung immer anzeigen** – Aktivieren Sie diese Option, um die Kurzbeschreibung unterhalb der Komponente anzuzeigen.

* **Hilfetext** – Hilfetext bezieht sich auf zusätzliche Informationen oder Anleitungen, die den Benutzenden bereitgestellt werden, um sie beim korrekten Ausfüllen eines Formularfelds zu unterstützen. Er erscheint, wenn Benutzende auf das Hilfesymbol (i) neben der Komponente klicken. Hilfetext enthält detailliertere Informationen als die Beschriftung oder der Platzhaltertext eines Formularfelds und soll den Benutzenden dabei helfen, die Anforderungen oder Einschränkungen des Felds zu verstehen. Er kann auch Vorschläge oder Beispiele anbieten, um das Ausfüllen des Formulars einfacher und genauer zu gestalten.

### Registerkarte „Barrierefreiheit“ {#accessibility}

![Registerkarte „Barrierefreiheit“](/help/adaptive-forms/assets/accessibilty-panel.png)


* **Text für Bildschirmlesehilfen** – Das ist zusätzlicher Text, der von Hilfstechnologien wie etwa Bildschirmlesehilfen für sehbehinderte Personen vorgelesen wird. Dieser Text enthält eine Audiobeschreibung des Zwecks des Formularfelds und kann Informationen über den Titel, die Beschreibung, den Namen und alle relevanten Nachrichten (benutzerdefinierten Text) des Felds enthalten. Der Text der Bildschirmlesehilfe hilft sicherzustellen, dass das Formular allen Benutzenden zugänglich ist, auch Personen mit Sehschwäche, und bietet ihnen ein umfassendes Verständnis des Formularfelds und seiner Anforderungen.

* **HTML-Rolle für die Ankündigung durch die Bildschirmlesehilfe** – Die HTML-Rolle ist ein Attribut, mit dem der Zweck eines HTML-Elements für Hilfstechnologien wie Bildschirmlesehilfen spezifiziert wird. Rollenattribute werden verwendet, um für ein Element zusätzlichen Kontext und eine semantische Bedeutung bereitzustellen, wodurch es für Bildschirmlesehilfen einfacher wird, den Inhalt zu interpretieren und ihn Benutzenden mitzuteilen. In AEM Forms kann beispielsweise die Beschriftung eines Formularfelds die Rolle „Beschriftung“ haben und sein Eingabefeld die Rolle „Textfeld“. Dadurch kann die Bildschirmlesehilfe die Beziehung zwischen Beschrfitung und Eingabefeld verstehen und diese Informationen den Benutzenden korrekt mitteilen.

## Verwandter Artikel {#related-article}

* [Erstellen eines adaptiven Formulars auf der AEM Sites-Seite oder im Experience Fragment](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html)

* [Erstellen eines eigenständigen adaptiven Formulars](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html?lang=de)
