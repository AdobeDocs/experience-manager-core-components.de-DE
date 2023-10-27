---
title: Kernkomponente „Horizontale Registerkarten“ für adaptive Formulare
description: Verwenden oder Anpassen der Kernkomponente „Horizontale Registerkarten“ für adaptive Formulare.
role: Architect, Developer, Admin, User
exl-id: fbdf330b-3b85-4f94-9dab-eea8465fba67
source-git-commit: 37ac7d3a9ae8c88d4c9be8129cfbd1eb4a7cccd1
workflow-type: ht
source-wordcount: '2195'
ht-degree: 100%

---

# Horizontale Registerkarten {#horizontal-tabs-adaptive-forms-core-component}

Horizontale Registerkarten in adaptiven Formularen sind so aufgebaut, dass mehrere Abschnitte eines Formulars gruppiert und als separate, horizontal ausgerichtete Registerkarten angezeigt werden. Benutzende können zwischen den Registerkarten wechseln, um auf verschiedene Abschnitte des Formulars zuzugreifen. Jede Registerkarte dient als Auslöser zum Anzeigen und Ausblenden des jeweiligen Formularinhalts. Mit horizontalen Registerkarten können Sie lange Formulare in überschaubare Abschnitte organisieren und das Benutzererlebnis verbessern. Registerkarten können ein Formular für Benutzende mit Behinderungen barrierefreier gestalten, da sie mithilfe der Tastaturnavigation zwischen Abschnitten wechseln können.

Die Registerkarten bestehen in der Regel aus einer Reihe von Links oder Schaltflächen, wobei jeder Link oder jede Schaltfläche einem Abschnitt des Formulars entspricht. Wenn Benutzende auf eine Registerkarte klicken, wird der Formularinhalt dynamisch aktualisiert und der entsprechende Abschnitt wird angezeigt.

## Verwendung {#reasons-to-use-horizontal-tabs}

Die häufigsten Gründe für die Verwendung horizontaler Registerkarten in einem adaptiven Formular sind:

- **Verbesserte Benutzerfreundlichkeit**: Horizontale Registerkarten erleichtern Benutzenden die Navigation durch das Formular, insbesondere wenn das Formular mehrere Abschnitte oder eine große Anzahl von Feldern enthält.

- **Platz-Management**: Horizontale Registerkarten sparen Platz auf dem Bildschirm, indem sie verwandte Formularabschnitte in Registerkarten gruppieren und jeweils nur einen Abschnitt anzeigen.

- **Bessere Organisation**: Registerkarten bieten eine klare und übersichtliche Struktur für ein Formular, sodass Benutzende das Formular besser verstehen und ausfüllen können.

- **Erhöhte Benutzerinteraktion**: Horizontale Registerkarten können ein Formular für Benutzende visuell ansprechender und interessanter gestalten, wodurch die Formularausfüllungsrate verbessert werden kann.

## Version und Kompatibilität {#version-and-compatibility}

Die Kernkomponente „Horizontale Registerkarten“ für adaptive Formulare wurde im Februar 2023 als Teil der Kernkomponenten 2.0.4 veröffentlicht. Hier finden Sie eine Tabelle mit allen unterstützten Versionen, Informationen zur AEM-Kompatibilität und Links zur entsprechenden Dokumentation:

|  |  |
|---|---|
| Komponentenversion | AEM as a Cloud Service |
| --- | --- |
| v1 | Kompatibel mit<br>[Version 2.0.4](/help/versions.md) und höher | Kompatibel | Kompatibel |

Informationen zu Versionen und Freigaben der Kernkomponente finden Sie im Dokument [Kernkomponenten-Versionen](/help/versions.md).


<!-- ## Sample Component Output {#sample-component-output}

To experience the Horizontal-tabs  Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_Horizontal-tabs ). -->


## Technische Details {#technical-details}

Die neuesten Informationen zur Kernkomponente „Horizontale Registerkarten“ für adaptive Formulare erfahren Sie in der technischen Dokumentation auf [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/pageHorizontal tabs/v1/pageHorizontal tabs). Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Entwicklerdokumentation für Kernkomponenten](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Im Konfigurieren-Dialogfeld können Sie die horizontalen Registerkarten einfach anpassen. Sie können auch Optionen für horizontale Registerkarten definieren, um das Benutzererlebnis zu verbessern.

### Registerkarte „Allgemein“ {#basic-tab}

![Registerkarte „Allgemein“](/help/adaptive-forms/assets/tabs-on-top-basic.png)

- **Name**: Sie können eine Formularkomponente sowohl im Formular als auch im Regel-Editor leicht mit ihrem eindeutigen Namen identifizieren. Der Name darf jedoch keine Leerzeichen oder Sonderzeichen enthalten.

- **Titel**: Sie können mit dem Titel leicht eine Komponente in einem Formular identifizieren. Standardmäßig wird der Titel über der Komponente angezeigt. Wenn Sie keinen Titel hinzufügen, wird der Name der Komponente anstelle des Titeltexts angezeigt.

- **Titel ausblenden**: Wählen Sie die Option aus, um den Titel der Komponente auszublenden.


- **Daten untergeordneter Komponenten bei Formularübermittlung gruppieren (Daten in Objekt einschließen)** – Wenn die Option ausgewählt ist, werden die Daten aus den untergeordneten Komponenten innerhalb des JSON-Objekts der übergeordneten Komponente verschachtelt. Wenn jedoch die Option nicht ausgewählt ist, weisen die gesendeten JSON-Daten eine flache Struktur auf, ohne dass ein Objekt für die übergeordnete Komponente vorhanden ist. Zum Beispiel:

   - Wenn die Option ausgewählt ist, werden die Daten aus den untergeordneten Komponenten (z. B. Straße, Stadt und Postleitzahl) innerhalb der übergeordneten Komponente (Adresse) als JSON-Objekt verschachtelt. Dadurch wird eine hierarchische Struktur erstellt, und die Daten werden unter der übergeordneten Komponente angeordnet.

     Struktur der übermittelten Daten:

     ```JSON
     { "Address":
     
     { "Street": "123 Main Street", "City": "New York", "Zip Code": "12345" }
     
     }
     ```

   - Wenn die Option nicht ausgewählt ist, weisen die gesendeten JSON-Daten eine flache Struktur auf, ohne dass ein Objekt für die übergeordnete Komponente (Adresse) vorhanden ist. Alle Daten befinden sich auf derselben Ebene ohne hierarchische Organisation.


     Struktur der übermittelten Daten:

     ```JSON
        { "Street": "123 Main Street", "City": "New York", "Zip Code": "12345" }
     ```

- **Layout**: Sie können für Ihren Assistenten entweder ein festes Layout (einfach) oder ein flexibles Layout (responsives Raster) verwenden. Das einfache Layout behält alles fest an der Stelle, während Sie mit dem responsiven Raster die Position der Komponenten an Ihre Bedürfnisse anpassen können. Verwenden Sie beispielsweise das responsive Raster, um „Vorname“, „Mittelname“ und „Nachname“ in einem Formular in einer einzigen Zeile auszurichten.

- **Bindungsverweis**: Bindungsverweis ist ein Verweis auf ein Datenelement, das in einer externen Datenquelle gespeichert ist und in einem Formular verwendet wird. Sie können mit dem Bindungsverweis Daten dynamisch an Formularfelder binden, sodass das Formular die aktuellsten Daten aus der Datenquelle anzeigen kann. Beispielsweise kann ein Bindungsverweis verwendet werden, um den Namen und die Adresse von Kundinnen und Kunden in einem Formular anzuzeigen, basierend auf der im Formular eingegebenen Kunden-ID. Der Bindungsverweis kann auch verwendet werden, um die Datenquelle mit den im Formular eingegebenen Daten zu aktualisieren. Auf diese Weise können Sie mit AEM Forms Formulare erstellen, die mit externen Datenquellen interagieren und so ein nahtloses Benutzererlebnis bei der Datenerfassung und -verwaltung bieten.
- **Komponente ausblenden**: Wählen Sie diese Option, um die Komponente aus dem Formular auszublenden. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor. Dies ist nützlich, wenn Sie Informationen speichern müssen, die Benutzende nicht sehen oder direkt ändern müssen.
- **Komponente deaktivieren**: Wählen Sie die Option zum Deaktivieren der Komponente aus. Die deaktivierte Komponente ist nicht aktiv und Endbenutzende können sie nicht bearbeiten. Benutzende können den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor.

### Registerkarten oben wiederholen {#repeat-tabs-on-top}

![Registerkarte „Barrierefreiheit“](/help/adaptive-forms/assets/repeat-tabsontop.png)

Sie können die Wiederholungsoptionen verwenden, um die Komponente „Horizontale Registerkarten“ und ihre untergeordneten Komponenten zu duplizieren, eine minimale und maximale Wiederholungsanzahl zu definieren und die Replikation ähnlicher Abschnitte innerhalb eines Formulars zu erleichtern. Bei der Interaktion mit der Komponente „Horizontale Registerkarten“ und dem Zugriff auf ihre Einstellungen werden die folgenden Optionen angezeigt:

- **Horizontale Registerkarten wiederholbar machen**: Eine Umschalter-Funktion, mit der Benutzende die Wiederholungsfunktion aktivieren oder deaktivieren können.
- **Mindestwiederholungen**: Legt fest, wie oft die Komponente „Horizontale Registerkarten“ mindestens wiederholt werden kann. Der Wert null zeigt an, dass die Komponente „Horizontale Registerkarten“ nicht wiederholt wird. Der Standardwert ist null.
- **Maximale Wiederholungen**: Legt fest, wie oft die Komponente „Horizontale Registerkarten“ maximal wiederholt werden kann. Standardmäßig ist dieser Wert unbegrenzt.

Um wiederholbare Abschnitte innerhalb der horizontalen Registerkarten effektiv zu verwalten, folgen Sie den Schritten, die im Artikel [Erstellen von Formularen mit wiederholbaren Abschnitten](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/create-forms-repeatable-sections.html?lang=de) beschrieben sind.

### Registerkarte „Elemente“ {#items-tab}

![Registerkarte „Elemente“](/help/adaptive-forms/assets/items-tabs-on-top.png)

Mit der Schalfläche **Hinzufügen** können Sie eine Komponente vom Komponentenauswahl-Fenster auswählen und als Bedienfeld hinzufügen. Nach dem Hinzufügen der Komponente werden die folgenden Optionen angezeigt:

- **Symbol**: Das Symbol identifiziert die Komponente des Bedienfelds in der Liste. Sie können den Mauszeiger über das Symbol bewegen, um den vollständigen Komponentennamen als QuickInfo anzuzeigen.
- **Beschreibung**: Die Beschreibung, die als Text des Bedienfelds verwendet wird. Standardmäßig der Name der für das Bedienfeld ausgewählten Komponente.
- **Entfernen**: Tippen oder klicken Sie, um das Bedienfeld aus der Komponente „Horizontale Registerkarten“ zu löschen.
- **Neu anordnen**: Tippen oder klicken und ziehen Sie, um die Reihenfolge der Bedienfelder neu anzuordnen.

### Registerkarte „Hilfe-Inhalt“ {#help-content}

![Registerkarte „Hilfe-Inhalt“](/help/adaptive-forms/assets/helpcontent-tabs-on-top.png)

- **Kurzbeschreibung**: Eine Kurzbeschreibung ist eine kurze Erklärung, die zusätzliche Informationen oder Klarstellungen über den Zweck eines Formularfelds bietet. Es hilft Benutzenden zu verstehen, welcher Datentyp in das Feld eingegeben werden soll, und kann Richtlinien oder Beispiele bereitstellen, um sicherzustellen, dass die eingegebenen Informationen gültig sind und die gewünschten Kriterien erfüllen. Standardmäßig bleiben kurze Beschreibungen ausgeblendet. Aktivieren Sie die Option **Kurzbeschreibung immer anzeigen**, um sie unterhalb der Komponente anzuzeigen.

- **Kurzbeschreibung immer anzeigen**: Aktivieren Sie diese Option, um die Kurzbeschreibung unterhalb der Komponente anzuzeigen.

- **Hilfetext**: Hilfetext bezieht sich auf zusätzliche Informationen oder Anleitungen, die den Benutzenden bereitgestellt werden, um sie beim korrekten Ausfüllen eines Formularfelds zu unterstützen. Er erscheint, wenn Benutzende auf das Hilfesymbol (i) neben der Komponente klicken. Hilfetext enthält detailliertere Informationen als die Beschriftung oder der Platzhaltertext eines Formularfelds und soll den Benutzenden dabei helfen, die Anforderungen oder Einschränkungen des Felds zu verstehen. Er kann auch Vorschläge oder Beispiele anbieten, um das Ausfüllen des Formulars einfacher und genauer zu gestalten.

### Registerkarte „Barrierefreiheit“ {#accessibility}

![Registerkarte „Barrierefreiheit“](/help/adaptive-forms/assets/accessibilty-tabs-on-top.png)

- **Text für Bildschirmlesehilfen** – Das ist zusätzlicher Text, der von Hilfstechnologien wie etwa Bildschirmlesehilfen für sehbehinderte Personen vorgelesen wird. Dieser Text enthält eine Audiobeschreibung des Zwecks des Formularfelds und kann Informationen über den Titel, die Beschreibung, den Namen und alle relevanten Nachrichten (benutzerdefinierten Text) des Felds enthalten. Der Text der Bildschirmlesehilfe hilft sicherzustellen, dass das Formular allen Benutzenden zugänglich ist, auch Personen mit Sehschwäche, und bietet ihnen ein umfassendes Verständnis des Formularfelds und seiner Anforderungen.

- **HTML-Rolle für die Ankündigung durch die Bildschirmlesehilfe** – Die HTML-Rolle ist ein Attribut, mit dem der Zweck eines HTML-Elements für Hilfstechnologien wie Bildschirmlesehilfen spezifiziert wird. Rollenattribute werden verwendet, um für ein Element zusätzlichen Kontext und eine semantische Bedeutung bereitzustellen, wodurch es für Bildschirmlesehilfen einfacher wird, den Inhalt zu interpretieren und ihn Benutzenden mitzuteilen. In AEM Forms kann beispielsweise die Beschriftung eines Formularfelds die Rolle „Beschriftung“ haben und sein Eingabefeld die Rolle „Textfeld“. Dadurch kann die Bildschirmlesehilfe die Beziehung zwischen Beschrfitung und Eingabefeld verstehen und diese Informationen den Benutzenden korrekt mitteilen.

## Dialogfeld „Design“ {#design-dialog}

Im Dialogfeld „Design“ können Vorlagenerstellende steuern, wie Elemente standardmäßig angezeigt werden. Für die Komponente „Horizontale Registerkarten“ in adaptiven Formularen können Sie folgende Einstellungen vornehmen:

- Kernkomponenten, die Sie mit dem Editor für adaptive Formulare den horizontalen Registerkarten hinzufügen können
- Einfache Namen für Stile (CSS-Klassen), die Sie im Dialogfeld „Eigenschaften“ der Komponente „Horizontale Registerkarten“ im Editor für adaptive Formulare anwenden können.

Dadurch wird das Erstellen und Anpassen von Formularen einfacher und effizienter.

### Registerkarte „Zugelassene Komponenten“ {#allowed-components-tab}

In der Registerkarte **Zugelassene Komponenten** können Vorlagen-Bearbeitende die Komponenten festlegen, die den Bedienfeldern in der Komponente „Horizontale Registerkarten“ im Editor für adaptive Formulare als Elemente hinzugefügt werden können.

### Registerkarte „Stile“ {#styles-tab}

Sie können das Dialogfeld „Design“ zum Definieren und Verwalten von CSS-Stilen für eine Komponente verwenden. Die Kernkomponente „Horizontale Registerkarten“ für adaptive Formulare unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).

**Standard-CSS-Klassen**: Sie können für die Kernkomponente „Horizontale Registerkarten“ von adaptiven Formularen eine standardmäßige CSS-Klasse festlegen.

- **Zulässige Stile**: Sie können Stile definieren, indem Sie den Namen und die CSS-Klasse für den Stil angeben. Sie können beispielsweise einen Stil mit dem Namen „Fettschrift“ erstellen und die CSS-Klasse „Schriftbreite: Fett“ bereitstellen. Sie können diese Stile bei einem adaptiven Formular im adaptiven Formular-Editor anwenden. Um einen Stil anzuwenden, wählen Sie im Editor für adaptive Formulare die Komponente aus, auf die Sie den Stil anwenden möchten, navigieren Sie zum Eigenschaften-Dialog und wählen Sie den gewünschten Stil aus der Dropdown-Liste **Stile**. Wenn Sie die Stile aktualisieren oder ändern müssen, kehren Sie einfach zum Dialogfeld „Design“ zurück, aktualisieren die Stile auf der Registerkarte „Stile“ und speichern die Änderungen.

## Ähnliche Artikel {#related-articles}

- [Akkordeon](/help/adaptive-forms/components/accordion.md)
- [Schaltfläche](/help/adaptive-forms/components/button.md)
- [Kontrollkästchen „Gruppe“](/help/adaptive-forms/components/checkbox-group.md)
- [Datumsauswahl](/help/adaptive-forms/components/date-picker.md)
- [Dropdown-Liste](/help/adaptive-forms/components/drop-down.md)
- [E-Mail-Eingabe](/help/adaptive-forms/components/email-input.md)
- [Formular-Container](/help/adaptive-forms/components/form-container.md)
- [Dateianhang](/help/adaptive-forms/components/file-attachment.md)
- [Fußzeile](/help/adaptive-forms/components/footer.md)
- [Kopfzeile](/help/adaptive-forms/components/header.md)
- [Bild](/help/adaptive-forms/components/image.md)
- [Zahleneingabe](/help/adaptive-forms/components/number-input.md)
- [Bedienfeld-Container](/help/adaptive-forms/components/panel-container.md)
- [Optionsschaltfläche](/help/adaptive-forms/components/radio-button.md)
- [Schaltfläche „Zurücksetzen“](/help/adaptive-forms/components/reset-button.md)
- [Schaltfläche „Senden“](/help/adaptive-forms/components/submit-button.md)
- [Telefoneingabe](/help/adaptive-forms/components/telephone-input.md)
- [Texteingabe](/help/adaptive-forms/components/text-input.md)
- [Text](/help/adaptive-forms/components/text.md)
- [Titel](/help/adaptive-forms/components/title.md)
- [Assistent](/help/adaptive-forms/components/wizard.md)

## Siehe auch {#see-also}

- [Erstellen eines adaptiven AEM-Formulars](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html?lang=de)
- [Hinzufügen eines adaptiven AEM-Formulars zu einer AEM Sites-Seite](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=de)
- [Anwenden von Designs auf ein adaptives AEM-Formular](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/using-themes-in-core-components.html?lang=de)
- [Hinzufügen von Komponenten zu adaptiven AEM-Formularen](/help/adaptive-forms/introduction.md#adaptive-forms-core-components-components)
- [Verwenden von reCAPTCHA in einem adaptiven AEM-Formular](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/add-components-to-an-adaptive-form/captcha-adaptive-forms.html?lang=de)
- [Generieren der PDF-Version (DoR) eines adaptiven AEM-Formulars](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/generate-document-of-record-core-components.html?lang=de)
- [Übersetzen eines adaptiven AEM-Formulars](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/using-aem-translation-workflow-to-localize-adaptive-forms-core-components.html?lang=de)
- [Aktivieren von Adobe Analytics für ein adaptives Formular, um die Formularnutzung zu verfolgen.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/integrate/services/enable-adobe-analytics-adaptive-form-using-experience-cloud-setup-automation.html?lang=de)
- [Verbinden eines adaptiven Formulars mit Microsoft SharePoint](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components.html#create-sharepoint-configuration?lang=de)
- [Verbinden eines adaptiven Formulars mit Microsoft Power Automate](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components.html?lang=de#microsoft-power-automate)
- [Verbinden eines adaptiven Formulars mit Microsoft OneDrive](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components.html?lang=de#submit-to-onedrive)
- [Verbinden eines adaptiven Formulars mit Microsoft Azure Blob Storage](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components.html?lang=de#submit-to-azure-blob-storage)
- [Verbinden eines adaptiven Formulars mit Salesforce](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/integrate/use-form-data-model/oauth2-client-credentials-flow-for-server-to-server-integration.html?lang=de)
- [Verwenden von Adobe Sign in einem adaptiven AEM-Formular](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/use-adobe-sign/working-with-adobe-sign.html?lang=de)
- [Hinzufügen eines neuen Gebietsschemas für ein adaptives Formular](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/supporting-new-language-localization-core-components.html?lang=de)
- [Senden von Daten adaptiver Formulare an eine Datenbank](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/integrate/use-form-data-model/data-integration.html?lang=de)
- [Senden von Daten adaptiver Formulare an einen REST-Endpunkt](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components.html#submit-to-rest-endpoint?lang=de)
- [Senden von Daten adaptiver Formulare an einen AEM-Workflow](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components.html?lang=de#invoke-an-aem-workflow)
- [Verwenden von Forms Portal zur Auflistung von adaptiven AEM-Formularen auf einer AEM-Website](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-forms-portal.html?lang=de)