---
title: Akkordeon für adaptive Formulare
description: Verwenden Sie Akkordeon, um ein langes oder komplexes Formular zu organisieren und zu vereinfachen, indem Sie es in kleinere, besser verwaltbare Abschnitte unterteilen.
role: Architect, Developer, Admin, User
source-git-commit: 945e1793ae4e959f83960db46d2de4257916fe32
workflow-type: tm+mt
source-wordcount: '1768'
ht-degree: 3%

---

# Akkordeon-Komponente  {#accordion-component-adaptive-forms-core-component}

Mit der Accordion-Kernkomponente können Benutzer erweiterbare und ausblendbare Abschnitte in einem adaptiven Formular erstellen. Sie wird häufig verwendet, um lange oder komplexe Formulare zu organisieren und zu vereinfachen, indem sie in kleinere, besser verwaltbare Abschnitte unterteilt werden. Jeder Abschnitt eines Accordions wird in der Regel durch eine Kopfzeile dargestellt, auf die der Benutzer klicken kann, um den entsprechenden Inhalt zu erweitern oder zu reduzieren. Der Inhalt kann eine beliebige Kernkomponente sein.

## Verwendung {#usage}

Es gibt mehrere Gründe, warum es sinnvoll ist, ein Akkordeon in ein adaptives Formular einzuschließen, darunter:

* **Platzeinsparung**: Mit einem Akkordeon können Benutzer Abschnitte eines Formulars erweitern und reduzieren so den Platz, der zum Anzeigen aller Formularfelder auf einmal benötigt wird.

* **Navigation**: Ein Akkordeon kann verwendet werden, um eine hierarchische Navigationsstruktur zu erstellen, die es Benutzern erleichtert, die benötigten Formularfelder zu finden.

* **Anwendererlebnis**: Accordion kann verwendet werden, um das Formular benutzerfreundlicher zu gestalten, indem es Benutzern eine klare und intuitive Möglichkeit bietet, auf Formularfelder zuzugreifen und sie auszufüllen.

* **Long Forms**: Akkordeon ist eine ideale Komponente für die Verarbeitung langer Formulare, da Benutzer dadurch auf einen Abschnitt auf einmal fokussieren können, anstatt zu versuchen, viele Informationen gleichzeitig zu verarbeiten.

Sie können Folgendes verwenden:

* Die [Dialogfeld konfigurieren](#configure-dialog) um Eigenschaften der Accordion-Komponente anzugeben.

* Die [Popover &quot;Bedienfeld auswählen&quot;](#select-panel-popover)  um die Reihenfolge der Bedienfelder des Accordions zu definieren. Dadurch kann der Autor die Bedienfelder in der Reihenfolge anordnen, in der die Bedienfelder angezeigt werden sollen.

* Optionen für Formularverfasser zum Aktivieren oder Deaktivieren bestimmter Funktionen in [Dialogfeld &quot;Design&quot;](#design-dialog). Ein Autor kann beispielsweise bestimmte Felder oder Abschnitte eines Formulars deaktivieren. Diese Optionen ermöglichen es dem Autor, den Formularentwurf und die Formularfunktionen besser zu steuern, wodurch es einfacher wird, Formulare zu erstellen, die auf die spezifischen Anforderungen des Unternehmens zugeschnitten sind.

Das Dialogfeld &quot;Konfigurieren&quot;und das Popover &quot;Bedienfeld auswählen&quot;sowie das Dialogfeld &quot;Design&quot;sind alle Teil der Kernkomponenten, die erstellt wurden, um das Authoring der Formulare zu vereinfachen und eine effiziente Methode zum Erstellen komplexer Formulare bereitzustellen.

## Version und Kompatibilität {#version-and-compatibility}


Die Kernkomponente &quot;Adaptive Forms Accordion&quot;wurde im Februar 2023 als Teil der Kernkomponenten 2.0.4 veröffentlicht. Hier finden Sie eine Tabelle mit allen unterstützten Versionen, AEM Kompatibilität und Links zur entsprechenden Dokumentation:

|  |  |
|---|---|
| Komponentenversion | AEM as a Cloud Service |
| --- | --- |
| v1 | Kompatibel mit<br>[Version 2.0.4](/help/versions.md) und höher | Kompatibel | Kompatibel |

Informationen zu Kernkomponentenversionen und -versionen finden Sie im Abschnitt [Kernkomponenten-Versionen](/help/versions.md) Dokument.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technische Details {#technical-details}

Aktuelle Informationen zur Accordion-Komponente finden Sie in der technischen Dokumentation zu [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/accordion/v1/accordion). Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie im Abschnitt [Entwicklerdokumentation für Kernkomponenten](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Im Dialogfeld &quot;Konfigurieren&quot;können Sie das Akkordeon-Erlebnis für Besucher einfach anpassen. Sie können auch Accordion-Elemente, Bedienfelder, Verhalten und Erscheinungsbild mit Leichtigkeit definieren, um ein nahtloses Benutzererlebnis zu gewährleisten.

### Einfache Registerkarte {#basic-tab}

![Registerkarte &quot;Allgemein&quot;](/help/adaptive-forms/assets/accordion_basictab.png)

* **Name** - Sie können eine Formularkomponente sowohl im Formular als auch im Regeleditor leicht mit ihrem eindeutigen Namen identifizieren, der Name darf jedoch keine Leerzeichen oder Sonderzeichen enthalten.

* **Titel** - Mit dem Titel können Sie eine Komponente in einem Formular leicht identifizieren. Standardmäßig wird der Titel über der Komponente angezeigt. Wenn Sie keinen Titel hinzufügen, wird der Name der Komponente anstelle des Titeltexts angezeigt.

* **Titel ausblenden** - Wählen Sie die Option aus, um den Titel der Komponente auszublenden.

* **Daten in Objekt einschließen** - Wählen Sie &quot;Daten in ein Objekt einschließen&quot;aus, um die Felddaten aus dem Assistenten in ein JSON-Objekt einzufügen. Wenn diese Option nicht ausgewählt ist, hat die JSON-Datei für die Übermittlungsdaten eine flache Struktur für die Felder des Assistenten.

* **Layout** - Sie können für Ihren Assistenten entweder ein festes Layout (einfach) oder ein flexibles Layout (responsives Raster) verwenden. Das einfache Layout behält alles fest an der Stelle, während das responsive Raster es Ihnen ermöglicht, die Position der Komponenten an Ihre Bedürfnisse anzupassen. Verwenden Sie beispielsweise das responsive Raster, um &quot;Vorname&quot;, &quot;Vorname&quot;und &quot;Nachname&quot;in einem Formular in einer einzigen Zeile auszurichten.

* **Bindungsverweis** - Ein Bindungsverweis ist ein Verweis auf ein Datenelement, das in einer externen Datenquelle gespeichert und in einem Formular verwendet wird. Mit der Bindungsreferenz können Sie Daten dynamisch an Formularfelder binden, sodass das Formular die aktuellsten Daten aus der Datenquelle anzeigen kann. Beispielsweise kann eine Bindungsverweis verwendet werden, um den Namen und die Adresse eines Kunden in einem Formular anzuzeigen, basierend auf der im Formular eingegebenen Kundenkennung. Die Bindungsverweis kann auch verwendet werden, um die Datenquelle mit den im Formular eingegebenen Daten zu aktualisieren. Auf diese Weise können Sie mit AEM Forms Formulare erstellen, die mit externen Datenquellen interagieren und so eine nahtlose Benutzererfahrung bei der Datenerfassung und -verwaltung bieten.
* **Komponente ausblenden** - Wählen Sie die Option, um die Komponente aus dem Formular auszublenden. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regeleditor. Dies ist nützlich, wenn Sie Informationen speichern müssen, die vom Benutzer nicht gesehen oder direkt geändert werden müssen.
* **Komponente deaktivieren** - Wählen Sie die Option zum Deaktivieren der Komponente aus. Die deaktivierte Komponente ist vom Endbenutzer nicht aktiv oder kann nicht bearbeitet werden. Der Benutzer kann den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regeleditor.

### Registerkarte „Elemente“ {#items-tab}

![Registerkarte &quot;Elemente&quot;](/help/adaptive-forms/assets/accordion_itemstab.png)

Mit der Schaltfläche Hinzufügen können Sie eine Komponente auswählen, die als Bedienfeld im Fenster zur Komponentenauswahl hinzugefügt werden soll. Nach dem Hinzufügen der Komponente werden die folgenden Optionen angezeigt:

* **Symbol** - Das Symbol identifiziert die Komponente des Bedienfelds in der Liste. Sie können den Mauszeiger über das Symbol bewegen, um den vollständigen Komponentennamen als QuickInfo anzuzeigen.
* **Beschreibung** - Die Beschreibung, die als Text des Bedienfelds verwendet wird. Standardmäßig wird der Name der Komponente für das Bedienfeld ausgewählt.
* **Entfernen** - Tippen oder klicken Sie, um das Bedienfeld aus der Akkordeon-Komponente zu löschen.
* **Neu anordnen** - Tippen oder klicken und ziehen Sie, um die Reihenfolge der Bedienfelder neu anzuordnen.

### Registerkarte &quot;Hilfe-Inhalt&quot; {#help-content}

![Registerkarte &quot;Hilfe-Inhalt&quot;](/help/adaptive-forms/assets/accordion_helpcontent.png)

* **Kurzbeschreibung** - Eine kurze Beschreibung ist eine kurze Texterklärung, die zusätzliche Informationen oder Klarstellungen zum Zweck eines bestimmten Formularfelds bietet. Es hilft dem Benutzer zu verstehen, welcher Datentyp in das Feld eingegeben werden soll, und kann Richtlinien oder Beispiele bereitstellen, um sicherzustellen, dass die eingegebenen Informationen gültig sind und die gewünschten Kriterien erfüllen. Standardmäßig bleiben kurze Beschreibungen ausgeblendet. Aktivieren Sie die **Kurzbeschreibung immer anzeigen** -Option, um sie unter der Komponente anzuzeigen.

* **Kurzbeschreibung immer anzeigen** - Aktivieren Sie die Option, um die Kurzbeschreibung unter der Komponente anzuzeigen.

* **Hilfetext** - Hilfetext bezieht sich auf zusätzliche Informationen oder Anleitungen, die dem Benutzer bereitgestellt werden, um ihn beim korrekten Ausfüllen eines Formularfelds zu unterstützen. Er wird angezeigt, wenn der Benutzer auf das Hilfesymbol (i) neben der Komponente klickt. Hilfetext enthält detailliertere Informationen als die Beschriftung oder der Platzhaltertext eines Formularfelds und soll dem Benutzer dabei helfen, die Anforderungen oder Einschränkungen des Felds zu verstehen. Es kann auch Vorschläge oder Beispiele anbieten, um das Ausfüllen des Formulars zu vereinfachen und genauer zu gestalten.

### Registerkarte „Erreichbarkeit“ {#accessibility}

![Registerkarte &quot;Barrierefreiheit&quot;](/help/adaptive-forms/assets/accordion_accessibility.png)

Im **Zugänglichkeit** Registerkarte, werden Werte festgelegt für [Barrierefreiheit in ARIA](https://www.w3.org/WAI/standards-guidelines/aria/) Beschriftungen für die Komponente. Für die Verwendung des Textes für die Bildschirmlesehilfe stehen verschiedene Optionen zur Verfügung:

* **Text für Bildschirmlesehilfen** - Text für Bildschirmlesehilfen bezieht sich auf zusätzlichen Text, der speziell für Hilfstechnologien wie Bildschirmlesehilfen vorgesehen ist, die von sehbehinderten Personen verwendet werden. Dieser Text enthält eine Audiobeschreibung des Zwecks des Formularfelds und kann Informationen über den Titel, die Beschreibung, den Namen und alle relevanten Nachrichten (benutzerdefinierten Text) des Felds enthalten. Der Text der Bildschirmlesehilfe hilft sicherzustellen, dass das Formular für alle Benutzer zugänglich ist, auch für Benutzer mit Sehbehinderungen, und bietet ihnen ein umfassendes Verständnis des Formularfelds und seiner Anforderungen.


   * **Benutzerdefinierter Text**: Wählen Sie diese Option aus, um den benutzerdefinierten Text für ARIA-Barrierefreiheitsbeschriftungen zu verwenden. Wenn Sie diese Option auswählen, wird das Dialogfeld &quot;Benutzerdefinierter Text&quot;angezeigt. Sie können relevante Informationen im Dialogfeld &quot;Benutzerdefinierter Text&quot;hinzufügen.
   * **Beschreibung**: Wählen Sie diese Option aus, um die Beschreibung für ARIA-Barrierefreiheitsbeschriftungen zu verwenden.
   * **Titel**: Wählen Sie diese Option aus, um den Titel für ARIA-Barrierefreiheitsbeschriftungen zu verwenden.
   * **Name**: Wählen Sie diese Option aus, um den Namen für ARIA-Barrierefreiheitsbeschriftungen zu verwenden.
   * **Keines**: Wählen Sie diese Option aus, wenn Sie keine ARIA-Barrierefreiheitsbezeichnungen hinzufügen möchten.

<!--

### Properties Tab {#properties-tab}

![Properties tab of the edit dialog of the Accordion Component](/help/assets/accordion-edit-properties.png)

*   **Single item expansion** - When selected, this option forces a single accordion item to be expanded at a time. Expanding one item will then collapse all others.
*   **Expanded items** - This option defines the items that are expanded by default when the page is loaded.
    * When **Single item expansion** is selected, one panel must be selected. By default the first panel is selected.
    * When **Single item expansion** is not selected, this option is a multi-select and is optional.
*   **ID** - This option allows to control the unique identifier of the component in the HTML and in the [Data Layer](/help/developing/data-layer/overview.md).
    * If left blank, a unique ID is automatically generated for you and can be found by inspecting the resulting page.
    * If an ID is specified, it is the responsibility of the author to make sure that it is unique.
    * Changing the ID can have an impact on CSS, JS and Data Layer tracking.

## Select Panel Popover {#select-panel-popover}

The **Select Panel** option (![Select panel icon](/help/assets/select-panel-icon.png)) on the component toolbar enables content authors to modify the panels in an accordion with ease. By selecting this option, the author can switch to a different panel for editing and rearrange the order of the panels in the accordion. The configured panels will be displayed in a drop-down menu for the author to choose from. This feature optimizes the editing process and makes it user-friendly for content authors.

![Select panel popover](/help/assets/select-panel-popover.png)


* The panels are displayed in a numbered list, reflecting the assigned arrangement.
* Each panel is listed with its component type in bold, followed by a brief description in lighter font.
* By clicking or tapping on a panel in the drop-down, you can easily switch the view in the editor to that specific panel.
* To rearrange the panels, simply use the drag handles to move them into the desired order. -->

## Dialogfeld „Design“ {#design-dialog}

Im Dialogfeld &quot;Design&quot;können Vorlagenautoren steuern, wie Elemente standardmäßig angezeigt werden. Für die Adaptive Forms Accordion-Komponente können Sie Folgendes festlegen:

* Der Typ der zulässigen und als Standard festgelegten HTML-Überschriftenelemente (z. B. H1, H2, H3 usw.)
* Die Kernkomponenten, die ein Formularersteller dem Akkordeon im adaptiven Forms-Editor hinzufügen kann
* Einfache Namen für Stile (CSS-Klassen), die im Dialogfeld &quot;Eigenschaften&quot;der Accordion-Komponente im adaptiven Forms-Editor angewendet werden können.

Dadurch wird das Erstellen und Anpassen von Formularen einfacher und effizienter.

### Registerkarte „Eigenschaften“ {#properties-tab-design}

Auf der Registerkarte Eigenschaften können Vorlagenautoren standardmäßige und zulässige Überschriftenelemente für Formularautoren festlegen:

![Registerkarte „Eigenschaften“ im Dialogfeld „Design“](/help/assets/accordion-design-properties.png)

* **Zulässige Überschriftenelemente**: Eine Dropdown-Liste mit mehreren Optionen, über die der Vorlagenautor auswählen kann, welche Überschriftenelemente der Formularverfasser für das Akkordeon verwenden kann.

* **Standardüberschriftenelement**: Eine Dropdown-Liste legt das standardmäßige Überschriftenelement für die Accordion-Komponente fest.

### Registerkarte „Zugelassene Komponenten“ {#allowed-components-tab}

Die **Zugelassene Komponenten** -Tab ermöglicht es dem Vorlageneditor, die Komponenten festzulegen, die den Bedienfeldern in der Accordion-Komponente im adaptiven Forms-Editor als Elemente hinzugefügt werden können.

### Registerkarte „Arten“ {#styles-tab}

Das Dialogfeld &quot;Design&quot;wird zum Definieren und Verwalten von CSS-Stilen für eine Komponente verwendet. Die Kernkomponente &quot;Adaptives Forms-Akkordeon&quot;unterstützt die AEM [Stilsystem](/help/get-started/authoring.md#component-styling).

**Standard-CSS-Klassen**: Sie können eine standardmäßige CSS-Klasse für die Accordion-Komponente bereitstellen.

**Zulässige Stile**: Sie können Stile definieren, indem Sie einen Namen und die CSS-Klasse angeben, die den Stil darstellt. Sie können beispielsweise einen Stil mit dem Namen &quot;fett Text&quot;erstellen und die CSS-Klasse &quot;font-weight: fett&quot;. Sie können diese Stile im adaptiven Forms-Editor verwenden oder auf ein adaptives Formular anwenden. Um einen Stil anzuwenden, wählen Sie im adaptiven Forms-Editor die Komponente aus, auf die Sie den Stil anwenden möchten, navigieren Sie zum Dialogfeld &quot;Eigenschaften&quot;und wählen Sie den gewünschten Stil aus dem **Stile** Dropdown-Liste. Wenn Sie die Stile aktualisieren oder ändern müssen, kehren Sie einfach zum Dialogfeld &quot;Design&quot;zurück, aktualisieren Sie die Stile auf der Registerkarte &quot;Stile&quot;und speichern Sie die Änderungen.


<!-- 

The design dialog allows the template author to define the options available to the content author who uses the Accordion Component and the defaults set when placing the Accordion Component.


### Properties Tab {#properties-tab-design}

![Design dialog properties tab](/help/assets/accordion-design-properties.png)

* **Allowed Heading Elements** - This multi-select drop-down defines the accordion item heading HTML elements that are allowed to be selected by an author.
* **Default Heading Element** - This drop-down defines the default accordion item heading HTML element.

### Allowed Components Tab {#allowed-components-tab}

The **Allowed Components** tab is used to define which components can be added as items to panels in the Accordion Component by the content author.

The Allowed Components tab functions in the same way as the tab of the same name when [defining the policy and properties of a Layout Container in the Template Editor.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html#editing-a-template-layout-template-author)

### Styles Tab {#styles-tab}

The Accordion Component supports the AEM [Style System](/help/get-started/authoring.md#component-styling).

## Adobe Client Data Layer {#data-layer}

The Accordion Component supports the [Adobe Client Data Layer.](/help/developing/data-layer/overview.md)

-->




