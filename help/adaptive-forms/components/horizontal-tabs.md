---
title: Adaptive Forms-Kernkomponente - Horizontale Registerkarten
description: Verwenden oder Anpassen der Kernkomponente Adaptive Forms Horizontal Registerkarten .
role: Architect, Developer, Admin, User
source-git-commit: 945e1793ae4e959f83960db46d2de4257916fe32
workflow-type: tm+mt
source-wordcount: '1584'
ht-degree: 3%

---


# Horizontale Registerkarten {#horizontal-tabs-adaptive-forms-core-component}

Horizontale Registerkarten in einem adaptiven Formular beziehen sich auf ein Entwurfsmuster, bei dem mehrere Abschnitte eines Formulars gruppiert und als separate Registerkarten angezeigt werden, die horizontal ausgerichtet sind. Der Benutzer kann zwischen den Registerkarten wechseln, um auf verschiedene Abschnitte des Formulars zuzugreifen. Jede Registerkarte dient als Trigger zum Anzeigen und Ausblenden des zugehörigen Formularinhalts. Mit den horizontalen Registerkarten können Sie lange Formulare in überschaubare Abschnitte organisieren und das Benutzererlebnis verbessern. Registerkarten können dazu beitragen, ein Formular für Benutzer mit Behinderungen barrierefreier zu machen, da sie mithilfe der Tastaturnavigation zwischen Abschnitten wechseln können.

Die Registerkarten werden in der Regel als eine Reihe von Links oder Schaltflächen erstellt, wobei jeder Link oder jede Schaltfläche einem Abschnitt des Formulars entspricht. Wenn ein Benutzer auf eine Registerkarte klickt, wird der Formularinhalt dynamisch aktualisiert, um den entsprechenden Abschnitt anzuzeigen.

## Verwendung {#reasons-to-use-horizontal-tabs}

Die häufigsten Gründe für die Verwendung horizontaler Registerkarten in einem adaptiven Formular sind:

* **Verbesserte Benutzerfreundlichkeit**: Horizontale Registerkarten erleichtern Benutzern die Navigation durch das Formular, insbesondere wenn das Formular mehrere Abschnitte oder eine große Anzahl von Feldern enthält.

* **Raummanagement**: Horizontale Registerkarten sparen Platz auf dem Bildschirm, indem sie verwandte Formularabschnitte in Registerkarten gruppieren und jeweils nur einen Abschnitt anzeigen.

* **Bessere Organisation**: Registerkarten bieten eine klare und organisierte Struktur für ein Formular, sodass Benutzer das Formular besser verstehen und ausfüllen können.

* **Erhöhte Benutzerinteraktion**: Horizontale Registerkarten können ein Formular für Benutzer visueller ansprechender und ansprechender gestalten, wodurch die Rate der Formularausfüllungen verbessert werden kann.

## Version und Kompatibilität {#version-and-compatibility}

Die Kernkomponente &quot;Horizontale Registerkarten für adaptive Forms&quot;wurde im Februar 2023 als Teil der Kernkomponenten 2.0.4 veröffentlicht. Hier finden Sie eine Tabelle mit allen unterstützten Versionen, AEM Kompatibilität und Links zur entsprechenden Dokumentation:

|  |  |
|---|---|
| Komponentenversion | AEM as a Cloud Service |
| --- | --- |
| v1 | Kompatibel mit<br>[Version 2.0.4](/help/versions.md) und höher | Kompatibel | Kompatibel |

Informationen zu Kernkomponentenversionen und -versionen finden Sie im Abschnitt [Kernkomponenten-Versionen](/help/versions.md) Dokument.


<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->


## Technische Details {#technical-details}

Die neuesten Informationen zur Kernkomponente &quot;Horizontale Registerkarten für adaptive Forms&quot;finden Sie in der technischen Dokumentation zu [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/pageHorizontal Registerkarten/v1/pageHorizontal). Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie im Abschnitt [Entwicklerdokumentation für Kernkomponenten](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Im Dialogfeld &quot;Konfigurieren&quot;können Sie das Erlebnis für horizontale Registerkarten einfach für Besucher anpassen. Für ein nahtloses Benutzererlebnis können Sie auch Optionen für horizontale Registerkarten definieren.

### Einfache Registerkarte {#basic-tab}

![Registerkarte &quot;Allgemein&quot;](/help/adaptive-forms/assets/tabsontop_basictab.png)

* **Name** - Sie können eine Formularkomponente sowohl im Formular als auch im Regeleditor leicht mit ihrem eindeutigen Namen identifizieren, der Name darf jedoch keine Leerzeichen oder Sonderzeichen enthalten.

* **Titel** - Mit dem Titel können Sie eine Komponente in einem Formular leicht identifizieren. Standardmäßig wird der Titel über der Komponente angezeigt. Wenn Sie keinen Titel hinzufügen, wird der Name der Komponente anstelle des Titeltexts angezeigt.

* **Titel ausblenden** - Wählen Sie die Option aus, um den Titel der Komponente auszublenden.

* **Daten in Objekt einschließen** - Wählen Sie &quot;Daten in ein Objekt einschließen&quot;aus, um die Felddaten aus dem Assistenten in ein JSON-Objekt einzufügen. Wenn diese Option nicht ausgewählt ist, hat die JSON-Datei für die Übermittlungsdaten eine flache Struktur für die Felder des Assistenten.

* **Layout** - Sie können für Ihren Assistenten entweder ein festes Layout (einfach) oder ein flexibles Layout (responsives Raster) verwenden. Das einfache Layout behält alles fest an der Stelle, während das responsive Raster es Ihnen ermöglicht, die Position der Komponenten an Ihre Bedürfnisse anzupassen. Verwenden Sie beispielsweise das responsive Raster, um &quot;Vorname&quot;, &quot;Vorname&quot;und &quot;Nachname&quot;in einem Formular in einer einzigen Zeile auszurichten.

* **Bindungsverweis** - Ein Bindungsverweis ist ein Verweis auf ein Datenelement, das in einer externen Datenquelle gespeichert und in einem Formular verwendet wird. Mit der Bindungsreferenz können Sie Daten dynamisch an Formularfelder binden, sodass das Formular die aktuellsten Daten aus der Datenquelle anzeigen kann. Beispielsweise kann eine Bindungsverweis verwendet werden, um den Namen und die Adresse eines Kunden in einem Formular anzuzeigen, basierend auf der im Formular eingegebenen Kundenkennung. Die Bindungsverweis kann auch verwendet werden, um die Datenquelle mit den im Formular eingegebenen Daten zu aktualisieren. Auf diese Weise können Sie mit AEM Forms Formulare erstellen, die mit externen Datenquellen interagieren und so eine nahtlose Benutzererfahrung bei der Datenerfassung und -verwaltung bieten.
* **Komponente ausblenden** - Wählen Sie die Option, um die Komponente aus dem Formular auszublenden. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regeleditor. Dies ist nützlich, wenn Sie Informationen speichern müssen, die vom Benutzer nicht gesehen oder direkt geändert werden müssen.
* **Komponente deaktivieren** - Wählen Sie die Option zum Deaktivieren der Komponente aus. Die deaktivierte Komponente ist vom Endbenutzer nicht aktiv oder kann nicht bearbeitet werden. Der Benutzer kann den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regeleditor.

### Registerkarte „Elemente“ {#items-tab}

![Registerkarte &quot;Elemente&quot;](/help/adaptive-forms/assets/tabsontop_itemstab.png)

Die **Hinzufügen** -Schaltfläche können Sie eine Komponente auswählen, die als Bedienfeld im Fenster zur Komponentenauswahl hinzugefügt werden soll. Nach dem Hinzufügen der Komponente werden die folgenden Optionen angezeigt:

* **Symbol** - Das Symbol identifiziert die Komponente des Bedienfelds in der Liste. Sie können den Mauszeiger über das Symbol bewegen, um den vollständigen Komponentennamen als QuickInfo anzuzeigen.
* **Beschreibung** - Die Beschreibung, die als Text des Bedienfelds verwendet wird. Standardmäßig der Name der für das Bedienfeld ausgewählten Komponente.
* **Entfernen** - Tippen oder klicken Sie, um das Bedienfeld aus der Akkordeon-Komponente zu löschen.
* **Neu anordnen** - Tippen oder klicken und ziehen Sie, um die Reihenfolge der Bedienfelder neu anzuordnen.

### Registerkarte &quot;Hilfe-Inhalt&quot; {#help-content}

![Registerkarte &quot;Hilfe-Inhalt&quot;](/help/adaptive-forms/assets/tabsontop_helptab.png)

* **Kurzbeschreibung** - Eine kurze Beschreibung ist eine kurze Texterklärung, die zusätzliche Informationen oder Klarstellungen zum Zweck eines bestimmten Formularfelds bietet. Es hilft dem Benutzer zu verstehen, welcher Datentyp in das Feld eingegeben werden soll, und kann Richtlinien oder Beispiele bereitstellen, um sicherzustellen, dass die eingegebenen Informationen gültig sind und die gewünschten Kriterien erfüllen. Standardmäßig bleiben kurze Beschreibungen ausgeblendet. Aktivieren Sie die **Kurzbeschreibung immer anzeigen** -Option, um sie unter der Komponente anzuzeigen.

* **Kurzbeschreibung immer anzeigen** - Aktivieren Sie die Option, um die Kurzbeschreibung unter der Komponente anzuzeigen.

* **Hilfetext** - Hilfetext bezieht sich auf zusätzliche Informationen oder Anleitungen, die dem Benutzer bereitgestellt werden, um ihn beim korrekten Ausfüllen eines Formularfelds zu unterstützen. Er wird angezeigt, wenn der Benutzer auf das Hilfesymbol (i) neben der Komponente klickt. Hilfetext enthält detailliertere Informationen als die Beschriftung oder der Platzhaltertext eines Formularfelds und soll dem Benutzer dabei helfen, die Anforderungen oder Einschränkungen des Felds zu verstehen. Es kann auch Vorschläge oder Beispiele anbieten, um das Ausfüllen des Formulars zu vereinfachen und genauer zu gestalten.

### Registerkarte „Erreichbarkeit“ {#accessibility}

![Registerkarte &quot;Barrierefreiheit&quot;](/help/adaptive-forms/assets/tabsontop_accessibilitytab.png)

* **Text für Bildschirmlesehilfen** - Text für Bildschirmlesehilfen bezieht sich auf zusätzlichen Text, der speziell für Hilfstechnologien wie Bildschirmlesehilfen vorgesehen ist, die von sehbehinderten Personen verwendet werden. Dieser Text enthält eine Audiobeschreibung des Zwecks des Formularfelds und kann Informationen über den Titel, die Beschreibung, den Namen und alle relevanten Nachrichten (benutzerdefinierten Text) des Felds enthalten. Der Text der Bildschirmlesehilfe hilft sicherzustellen, dass das Formular für alle Benutzer zugänglich ist, auch für Benutzer mit Sehbehinderungen, und bietet ihnen ein umfassendes Verständnis des Formularfelds und seiner Anforderungen.

* **HTML-Rolle für die Ankündigung durch die Bildschirmlesehilfe** - Die HTML-Rolle ist ein Attribut, mit dem der Zweck eines HTML-Elements für Hilfstechnologien wie Bildschirmlesehilfen angegeben wird. Das Rollenattribut wird verwendet, um einem Element zusätzlichen Kontext und eine semantische Bedeutung zu verleihen, wodurch Bildschirmlesehilfen die Interpretation und Ankündigung des Inhalts für den Benutzer erleichtern. In AEM Forms kann beispielsweise die Beschriftung eines Formularfelds die Rolle &quot;label&quot;haben und sein Eingabefeld die Rolle &quot;textbox&quot;. Dies hilft der Bildschirmlesehilfe, die Beziehung zwischen Titel und Eingabefeld zu verstehen und sie dem Benutzer korrekt anzukündigen.

## Dialogfeld „Design“ {#design-dialog}

Im Dialogfeld &quot;Design&quot;können Vorlagenautoren steuern, wie Elemente standardmäßig angezeigt werden. Für die Adaptive Forms Accordion-Komponente können Sie Folgendes festlegen:

* Die Kernkomponenten, die ein Formularersteller dem Akkordeon im adaptiven Forms-Editor hinzufügen kann
* Einfache Namen für Stile (CSS-Klassen), die im Dialogfeld &quot;Eigenschaften&quot;der Accordion-Komponente im adaptiven Forms-Editor angewendet werden können.

Dadurch wird das Erstellen und Anpassen von Formularen einfacher und effizienter.

### Registerkarte „Zugelassene Komponenten“ {#allowed-components-tab}

Die **Zugelassene Komponenten** -Tab ermöglicht es dem Vorlageneditor, die Komponenten festzulegen, die den Bedienfeldern in der Komponente Horizontale Registerkarten im Editor für adaptive Forms als Elemente hinzugefügt werden können.

### Registerkarte „Arten“ {#styles-tab}

Das Dialogfeld &quot;Design&quot;wird zum Definieren und Verwalten von CSS-Stilen für eine Komponente verwendet. Die Kernkomponente &quot;Horizontale Registerkarten der adaptiven Forms&quot;unterstützt die AEM [Stilsystem](/help/get-started/authoring.md#component-styling).

**Standard-CSS-Klassen**: Sie können eine standardmäßige CSS-Klasse für die Kernkomponente Adaptive Forms Horizontal Registerkarten bereitstellen.

**Zulässige Stile**: Sie können Stile definieren, indem Sie einen Namen und die CSS-Klasse angeben, die den Stil darstellt. Sie können beispielsweise einen Stil mit dem Namen &quot;fett Text&quot;erstellen und die CSS-Klasse &quot;font-weight: fett&quot;. Sie können diese Stile im adaptiven Forms-Editor verwenden oder auf ein adaptives Formular anwenden. Um einen Stil anzuwenden, wählen Sie im adaptiven Forms-Editor die Komponente aus, auf die Sie den Stil anwenden möchten, navigieren Sie zum Dialogfeld &quot;Eigenschaften&quot;und wählen Sie den gewünschten Stil aus dem **Stile** Dropdown-Liste. Wenn Sie die Stile aktualisieren oder ändern müssen, kehren Sie einfach zum Dialogfeld &quot;Design&quot;zurück, aktualisieren Sie die Stile auf der Registerkarte &quot;Stile&quot;und speichern Sie die Änderungen.
