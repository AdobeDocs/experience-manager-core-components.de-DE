---
title: Adaptive Forms-Kernkomponente - Bedienfeldcontainer
description: Verwenden oder Anpassen der Kernkomponente des adaptiven Forms-Bedienfeldcontainers.
role: Architect, Developer, Admin, User
exl-id: 104836fe-8325-47de-978d-1ff2d6a9dd15
source-git-commit: d2a6108f17f6e0c6b91bec84893d64a8bd48effd
workflow-type: tm+mt
source-wordcount: '1696'
ht-degree: 2%

---

# Bedienfeldcontainer {#panel-container-adaptive-forms-core-component}

In einem adaptiven Formular ist ein Bedienfeld ein Container-Element, das zum Gruppieren verwandter Formularelemente verwendet werden kann. Dadurch können Sie verschiedene Formularelemente logisch und sinnvoll gruppieren und organisieren. Dies kann dazu beitragen, die Gesamtstruktur und Lesbarkeit des Formulars zu verbessern, wodurch Benutzer leichter verstehen und navigieren können.

Bedienfelder können verwendet werden, um ausblendbare Abschnitte zu erstellen. Diese können für das Ausblenden komplexer oder seltener verwendeter Formularfelder nützlich sein, sodass das Formular einfach und einfach zu verwenden ist. Sie können auch andere Komponenten wie Text, Kontrollkästchen und Schaltflächen einfügen.

Sie kann auch verwendet werden, um verschiedene regelbasierte Aktionen festzulegen, z. B. Formular senden, eine Website öffnen, Komponenten ein-/ausblenden oder eine Instanz eines Bedienfelds hinzuzufügen.

**Beispiel**

![](/help/adaptive-forms/assets/panel-container.png)

## Verwendung {#reasons-to-use-panel-container}

Es gibt verschiedene Gründe für die Verwendung eines Bedienfelds in einem Formular, darunter:

* **Organisieren von Formularelementen**: Ein Bedienfeld kann verwendet werden, um verwandte Formularelemente zusammenzufassen, was Benutzern das Verständnis und die Navigation im Formular erleichtert.

* **Verbessern der Formularstruktur**: Durch die Gruppierung von Formularelementen in Bedienfelder kann die Gesamtstruktur und Lesbarkeit des Formulars verbessert werden, was das Verständnis erleichtert.

* **Erstellen ausblendbarer Abschnitte**: Bedienfelder können verwendet werden, um ausblendbare Abschnitte zu erstellen. Diese können für das Ausblenden komplexer oder seltener verwendeter Formularfelder nützlich sein, sodass das Formular einfach und einfach zu verwenden ist.

* **Verbesserte Benutzerfreundlichkeit**: Durch die Verwendung von Bedienfeldern zur Organisation von Formularelementen kann das Formular benutzerfreundlicher und einfacher zu verwenden sein, was zu höheren Abschlussraten führen kann.

## Version und Kompatibilität {#version-and-compatibility}

Die Kernkomponente &quot;Adaptive Forms Accordion&quot;wurde im Februar 2023 als Teil der Kernkomponenten 2.0.4 für Cloud Service und Kernkomponenten 1.1.12 für AEM 6.5.16.0 Forms oder höher veröffentlicht. In der folgenden Tabelle finden Sie alle unterstützten Versionen, AEM Kompatibilität und Links zur entsprechenden Dokumentation:

| Komponentenversion | AEM as a Cloud Service | AEM 6.5.16.0 Forms oder höher |
|---|---|---|
| v1 | Kompatibel mit<br>[Version 2.0.4](/help/adaptive-forms/version.md) und höher | Kompatibel mit<br>[Version 1.1.12](/help/adaptive-forms/version.md) und höher, jedoch weniger als 2.0.0. |

Informationen zu Kernkomponentenversionen und -versionen finden Sie im Abschnitt [Kernkomponenten-Versionen](/help/adaptive-forms/version.md) Dokument.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technische Details {#technical-details}

Laden Sie die neuesten Informationen zur Kernkomponente des adaptiven Forms-Bedienfeldcontainers in der technischen Dokumentation zu [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/panelcontainer/v1/panelcontainer). Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie im Abschnitt [Entwicklerdokumentation für Kernkomponenten](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Mit dem Dialogfeld &quot;Konfigurieren&quot;können Sie das Bedienfeld-Container-Erlebnis für Besucher einfach anpassen. Für ein nahtloses Benutzererlebnis können Sie auch problemlos Bedienfeld-Container-Optionen definieren.

### Einfache Registerkarte {#basic-tab}

![Registerkarte &quot;Allgemein&quot;](/help/adaptive-forms/assets/panelcontainer_basictab.png)

* **Name** - Sie können eine Formularkomponente sowohl im Formular als auch im Regeleditor leicht mit ihrem eindeutigen Namen identifizieren, der Name darf jedoch keine Leerzeichen oder Sonderzeichen enthalten.

* **Titel** - Mit dem Titel können Sie eine Komponente in einem Formular leicht identifizieren. Standardmäßig wird der Titel über der Komponente angezeigt. Wenn Sie keinen Titel hinzufügen, wird der Name der Komponente anstelle des Titeltexts angezeigt.

* **Titel ausblenden** - Wählen Sie die Option aus, um den Titel der Komponente auszublenden.

* **Daten in Objekt einschließen** - Wählen Sie &quot;Daten in ein Objekt einschließen&quot;aus, um die Felddaten aus dem Assistenten in ein JSON-Objekt einzufügen. Wenn diese Option nicht ausgewählt ist, hat die JSON-Datei für die Übermittlungsdaten eine flache Struktur für die Felder des Assistenten.

* **Layout** - Sie können für Ihren Assistenten entweder ein festes Layout (einfach) oder ein flexibles Layout (responsives Raster) verwenden. Das einfache Layout behält alles fest an der Stelle, während das responsive Raster es Ihnen ermöglicht, die Position der Komponenten an Ihre Bedürfnisse anzupassen. Verwenden Sie beispielsweise das responsive Raster, um &quot;Vorname&quot;, &quot;Vorname&quot;und &quot;Nachname&quot;in einem Formular in einer einzigen Zeile auszurichten.

* **Bindungsverweis** - Ein Bindungsverweis ist ein Verweis auf ein Datenelement, das in einer externen Datenquelle gespeichert und in einem Formular verwendet wird. Mit der Bindungsreferenz können Sie Daten dynamisch an Formularfelder binden, sodass das Formular die aktuellsten Daten aus der Datenquelle anzeigen kann. Beispielsweise kann eine Bindungsverweis verwendet werden, um den Namen und die Adresse eines Kunden in einem Formular anzuzeigen, basierend auf der im Formular eingegebenen Kundenkennung. Die Bindungsverweis kann auch verwendet werden, um die Datenquelle mit den im Formular eingegebenen Daten zu aktualisieren. Auf diese Weise können Sie mit AEM Forms Formulare erstellen, die mit externen Datenquellen interagieren und so eine nahtlose Benutzererfahrung bei der Datenerfassung und -verwaltung bieten.
* **Komponente ausblenden** - Wählen Sie die Option, um die Komponente aus dem Formular auszublenden. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regeleditor. Dies ist nützlich, wenn Sie Informationen speichern müssen, die vom Benutzer nicht gesehen oder direkt geändert werden müssen.
* **Komponente deaktivieren** - Wählen Sie die Option zum Deaktivieren der Komponente aus. Die deaktivierte Komponente ist vom Endbenutzer nicht aktiv oder kann nicht bearbeitet werden. Der Benutzer kann den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regeleditor.

### Registerkarte &quot;Hilfe-Inhalt&quot; {#help-content}

![Registerkarte &quot;Hilfe-Inhalt&quot;](/help/adaptive-forms/assets/panelcontainer_helptab.png)

* **Kurzbeschreibung** - Eine kurze Beschreibung ist eine kurze Texterklärung, die zusätzliche Informationen oder Klarstellungen zum Zweck eines bestimmten Formularfelds bietet. Es hilft dem Benutzer zu verstehen, welcher Datentyp in das Feld eingegeben werden soll, und kann Richtlinien oder Beispiele bereitstellen, um sicherzustellen, dass die eingegebenen Informationen gültig sind und die gewünschten Kriterien erfüllen. Standardmäßig bleiben kurze Beschreibungen ausgeblendet. Aktivieren Sie die **Kurzbeschreibung immer anzeigen** -Option, um sie unter der Komponente anzuzeigen.

* **Kurzbeschreibung immer anzeigen** - Aktivieren Sie die Option, um die Kurzbeschreibung unter der Komponente anzuzeigen.

* **Hilfetext** - Hilfetext bezieht sich auf zusätzliche Informationen oder Anleitungen, die dem Benutzer bereitgestellt werden, um ihn beim korrekten Ausfüllen eines Formularfelds zu unterstützen. Er wird angezeigt, wenn der Benutzer auf das Hilfesymbol (i) neben der Komponente klickt. Hilfetext enthält detailliertere Informationen als die Beschriftung oder der Platzhaltertext eines Formularfelds und soll dem Benutzer dabei helfen, die Anforderungen oder Einschränkungen des Felds zu verstehen. Es kann auch Vorschläge oder Beispiele anbieten, um das Ausfüllen des Formulars zu vereinfachen und genauer zu gestalten.

### Registerkarte „Erreichbarkeit“ {#accessibility}

![Registerkarte &quot;Barrierefreiheit&quot;](/help/adaptive-forms/assets/panelcontainer_accessibilitytab.png)

* **Text für Bildschirmlesehilfen** - Text für Bildschirmlesehilfen bezieht sich auf zusätzlichen Text, der von Hilfstechnologien wie Bildschirmlesehilfen gelesen werden soll, die von sehbehinderten Personen verwendet werden. Dieser Text enthält eine Audiobeschreibung des Zwecks des Formularfelds und kann Informationen über den Titel, die Beschreibung, den Namen und alle relevanten Nachrichten (benutzerdefinierten Text) des Felds enthalten. Der Text der Bildschirmlesehilfe hilft sicherzustellen, dass das Formular für alle Benutzer zugänglich ist, auch für Benutzer mit Sehbehinderungen, und bietet ihnen ein umfassendes Verständnis des Formularfelds und seiner Anforderungen.

* **HTML-Rolle für die Ankündigung durch die Bildschirmlesehilfe** - Die HTML-Rolle ist ein Attribut, mit dem der Zweck eines HTML-Elements für Hilfstechnologien wie Bildschirmlesehilfen angegeben wird. Das Rollenattribut wird verwendet, um einem Element zusätzlichen Kontext und eine semantische Bedeutung zu verleihen, wodurch Bildschirmlesehilfen die Interpretation und Ankündigung des Inhalts für den Benutzer erleichtern. In AEM Forms kann beispielsweise die Beschriftung eines Formularfelds die Rolle &quot;label&quot;haben und sein Eingabefeld die Rolle &quot;textbox&quot;. Dies hilft der Bildschirmlesehilfe, die Beziehung zwischen Titel und Eingabefeld zu verstehen und sie dem Benutzer korrekt anzukündigen.

## Dialogfeld „Design“ {#design-dialog}

Das Dialogfeld &quot;Design&quot;wird zum Definieren und Verwalten von CSS-Stilen für die Panel-Container-Komponente verwendet.

### Registerkarte „Zugelassene Komponenten“ {#allowed-components-tab}

![Registerkarten &quot;Zulässige Komponenten&quot;](/help/adaptive-forms/assets/panel_allowedcomponent.png)

Die **Zugelassene Komponenten** -Tab ermöglicht es dem Vorlageneditor, die Komponenten festzulegen, die den Bedienfeldern in der Bereichsbehälterkomponente im Adaptive Forms-Editor als Elemente hinzugefügt werden können.

### Registerkarte „Standardkomponenten“ {#default-component-tab}

Auf dieser Registerkarte kann der Vorlageneditor die Komponenten, die als Elemente hinzugefügt werden können, den Bedienfeldern in der Bereichscontainer-Komponente im Adaptive Forms-Editor zuordnen.

![Bedienfeldstandardkomponente](/help/adaptive-forms/assets/panel_defaultcomponent.png)

### Responsive Einstellungen {#responsive-settings}

Auf dieser Registerkarte kann der Vorlageneditor die Anzahl der Spalten festlegen, die im responsiven Raster angezeigt werden sollen.

![Responsives Raster](/help/adaptive-forms/assets/panel_responsivesettings.png)

### Registerkarte „Container-Einstellungen“ {#container-setting-tab}

Auf der Registerkarte Container-Einstellungen können Sie die Position von Komponenten im adaptiven Forms-Editor festlegen.

![Container-Einstellungen](/help/adaptive-forms/assets/panel_settings.png)

* **Layout**: Das einfache Layout behält alle festen Elemente im Ort bei, während das responsive Raster es Ihnen ermöglicht, die Position der Komponenten an Ihre Bedürfnisse anzupassen.
* **Layout deaktivieren**: Sie können die Layoutauswahl auch im Dialogfeld &quot;Bearbeiten&quot;deaktivieren, indem Sie die **Layout deaktivieren** aktivieren.
* **Hintergrundbild aktivieren**: Auf dieser Registerkarte können Sie das Hintergrundbild und die Hintergrundfarbe im Vorlageneditor festlegen.
* **Hintergrundfarbe aktivieren**: Auf dieser Registerkarte können Sie die Hintergrundfarbe im Vorlageneditor festlegen.

### Registerkarte „Arten“ {#styles-tab}

Die Registerkarte wird verwendet, um CSS-Stile für eine Komponente zu definieren und zu verwalten. Die Kernkomponente für den Container des adaptiven Forms-Bedienfelds unterstützt die AEM [Stilsystem](/help/get-started/authoring.md#component-styling).

![Registerkarte &quot;Stil&quot;](/help/adaptive-forms/assets/panel_style.png)

* **Standard-CSS-Klassen**: Sie können eine standardmäßige CSS-Klasse für die adaptive Forms-Kernkomponente bereitstellen.

* **Zulässige Stile**: Sie können Stile definieren, indem Sie einen Namen und die CSS-Klasse angeben, die den Stil darstellt. Sie können beispielsweise einen Stil mit dem Namen &quot;fett Text&quot;erstellen und die CSS-Klasse &quot;font-weight: fett&quot;. Sie können diese Stile in Adaptive Forms verwenden oder auf ein adaptives Formular anwenden. Um einen Stil anzuwenden, wählen Sie im adaptiven Forms-Editor die Komponente aus, auf die Sie den Stil anwenden möchten, navigieren Sie zum Dialogfeld &quot;Eigenschaften&quot;und wählen Sie den gewünschten Stil aus dem **Stile** Dropdown-Liste. Wenn Sie die Stile aktualisieren oder ändern müssen, kehren Sie einfach zum Dialogfeld &quot;Design&quot;zurück, aktualisieren Sie die Stile auf der Registerkarte &quot;Stile&quot;und speichern Sie die Änderungen.

* **HTML-Rolle für die Ankündigung durch die Bildschirmlesehilfe** - Die HTML-Rolle ist ein Attribut, mit dem der Zweck eines HTML-Elements für Hilfstechnologien wie Bildschirmlesehilfen angegeben wird. Das Rollenattribut wird verwendet, um einem Element zusätzlichen Kontext und eine semantische Bedeutung zu verleihen, wodurch Bildschirmlesehilfen die Interpretation und Ankündigung des Inhalts für den Benutzer erleichtern. In AEM Forms kann beispielsweise die Beschriftung eines Formularfelds die Rolle &quot;label&quot;haben und sein Eingabefeld die Rolle &quot;textbox&quot;. Dies hilft der Bildschirmlesehilfe, die Beziehung zwischen Titel und Eingabefeld zu verstehen und sie dem Benutzer korrekt anzukündigen.

