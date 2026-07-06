---
title: Kernkomponente für adaptive Formulare – Formular-Container
description: Ein adaptives Formular zu einer Web-Seite hinzufügen.
role: Developer, Admin, User
exl-id: 03c4cf7c-51d6-4850-a566-1c0514d52dab
TQID: https://experienceleague.adobe.com/kMG6SKHisAUmKhOh9AFLI8NG6w0vH7tP4XimBKAMo-I
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: e2c1b6d3-bb7e-4fe8-8c72-f7b403298e91
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 0af65c80f9cc58c4ba48d5b3dc7a026820bd2833
workflow-type: tm+mt
source-wordcount: 2555
ht-degree: 64%

---

# Formular-Container {#form-container-adaptive-forms-core-component}

<span class="preview"> In diesem Artikel werden die Funktionen **Entwürfe** und **Hamburger-**) erläutert, die Vorabversionsfunktionen sind. Die Vorabversionsfunktion ist nur über unseren [Vorabversionskanal](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/release-notes/prerelease.html?lang=de#new-features) zugänglich.</span>

Mit Formularen können Besuchende von Websites mit der Website interagieren, indem sie wertvolle Informationen bereitstellen, die die Interaktion und Benutzerzufriedenheit steigern können. Ein Container für adaptive Formulare in Adobe Experience Manager-Sites (AEM) ermöglicht es Besitzenden von Websites, ihren Seiten ganz einfach Formulare hinzuzufügen. Dies erleichtert die Kommunikation zwischen Website-Besuchenden und Besitzenden oder der Organisation der Website, da Besuchende auf diese Weise Feedback geben, Anfragen stellen und andere Aktionen ausführen können

{{traditional-aem}}

## Verwendung {#reasons-to-use-forms-container}

Es gibt mehrere Gründe, warum ein Formular einer Website hinzugefügt werden kann:
- **Datenerfassung**: Formulare können verwendet werden, um Daten von Website-Besuchenden für verschiedene Zwecke zu erfassen, wie z. B. Marktforschung, Benutzerverhaltensanalyse und mehr.

- **Lead-Generierung**: Ein Formular kann verwendet werden, um Informationen potenzieller Kunden und Kundinnen zu sammeln, wie z. B. Name und E-Mail-Adresse, um Leads für Verkaufs- und Marketing-Maßnahmen zu generieren.

- **E-Commerce**: Formulare können für Online-Shopping verwendet werden, sodass die Kundschaft Bestellungen aufgeben und Zahlungen über die Website tätigen kann.

- **Kontakt**: Mit einem Kontaktformular können Besuchende der Website einfach den Besitzenden oder die Organisation der Website erreichen.

- **Befragungen und Umfragen**: Formulare können verwendet werden, um Feedback und Meinungen von Besuchenden der Website durch Befragungen und Umfragen zu sammeln.

- **Registrierung für Veranstaltungen**: Formulare können zur Registrierung für Veranstaltungen verwendet werden, sodass sich Website-Besuchende für Veranstaltungen oder Webinare anmelden können.

- **Abonnements**: Formulare können für Website-Abonnements verwendet werden, sodass sich Besuchende für einen Newsletter oder andere regelmäßige Nachrichten anmelden können.

- **Benutzerauthentifizierung**: Formulare können für die Benutzerauthentifizierung verwendet werden, sodass Website-Besuchende Konten erstellen und sich anmelden können, um auf exklusive Inhalte oder Funktionen zuzugreifen.

- **Erhöhung der Konversionsrate**: Ein gut gestaltetes Formular kann die Konversionsrate erhöhen, indem das Formular es den Benutzenden erleichtert, eine gewünschte Aktion auszuführen, z. B. ein Produkt zu erwerben oder sich für einen Service anzumelden.

## Version und Kompatibilität {#version-and-compatibility}

Die Kernkomponente „Akkordeon“ für adaptive Formulare wurde im Februar 2023 als Teil der Kernkomponenten 2.0.4 für Cloud Service und der Kernkomponenten 1.1.12 für AEM 6.5.16.0 Forms oder höher veröffentlicht. Hier finden Sie eine Tabelle mit allen unterstützten Versionen, AEM-Kompatibilität und Links zur entsprechenden Dokumentation:

| Komponentenversion | AEM as a Cloud Service | AEM 6.5.16.0 Forms oder höher |
|---|---|---|
| v1 | Kompatibel mit<br>[Version 2.0.4](/help/adaptive-forms/version.md) und höher | Kompatibel mit<br>[Version 1.1.12](/help/adaptive-forms/version.md) und höher (aber nur bis Version 2.0.0). |

Informationen zu Versionen und Freigaben der Kernkomponente finden Sie im Dokument [Kernkomponenten-Versionen](/help/adaptive-forms/version.md).
<!--
## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion_de). 
-->

## Technische Details {#technical-details}

Aktuelle Informationen über die Container-Kernkomponente für adaptive Formulare finden Sie in der technischen Dokumentation auf [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/container/v1/container). Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Entwicklerdokumentation für Kernkomponenten](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Mit dem Dialogfeld „Konfigurieren“ können Sie das Formular-Container-Erlebnis für Besuchende einfach anpassen. Sie können Formular-Container-Optionen auch einfach definieren, um ein nahtloses Anwendererlebnis zu gewährleisten.

### Registerkarte „Allgemein“ {#basic-tab}

![Registerkarte „Allgemein“](/help/adaptive-forms/assets/formcontainer_basictab1.png)

- **Titel**: Mit dem Titel können Sie eine Komponente in einem Formular leicht identifizieren. Standardmäßig wird der Titel oberhalb der Komponente angezeigt. Wenn Sie keinen Titel hinzufügen, wird der Name der Komponente anstelle des Titeltexts angezeigt.

- **Vorbefüllungs-Services**: Diese Option ermöglicht es Benutzenden, einen Vorbefüllungs-Service zum Abrufen von Daten auszuwählen, wenn das adaptive Formular gerendert wird. Weitere Informationen zum [Erstellen und Konfigurieren eines Vorbefüllungs-Services](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/prepopulate-adaptive-form-fields.html?lang=de#aem-forms-custom-prefill-service).

- **Rolle**: Die Rolle ist ein HTML-Attribut, mit dem der Zweck eines HTML-Elements für Hilfstechnologien wie Bildschirmlesehilfen angegeben wird. Rollenattribute werden verwendet, um für ein Element zusätzlichen Kontext und eine semantische Bedeutung bereitzustellen, wodurch es für Bildschirmlesehilfen einfacher wird, den Inhalt zu interpretieren und ihn Benutzenden mitzuteilen. In AEM Forms kann beispielsweise die Beschriftung eines Formularfelds die Rolle „Beschriftung“ haben und sein Eingabefeld die Rolle „Textfeld“. Dadurch kann die Bildschirmlesehilfe die Beziehung zwischen Beschrfitung und Eingabefeld verstehen und diese Informationen den Benutzenden korrekt mitteilen.

- **Client-Bibliothekskategorie**: Benutzende können eine benutzerdefinierte JavaScript-Bibliothek pro adaptivem Formular konfigurieren. Es wird empfohlen, nur die wiederverwendbaren Funktionen in der Bibliothek zu behalten, die von den Drittanbieter-Bibliotheken „jquery“ und „underscore.js“ abhängig sind.Bisweilen befindet sich bei komplexen **Validierungsregeln** das exakte Validierungsskript in den benutzerdefinierten Funktionen. Benutzende können diese benutzerdefinierten Funktionen über den Ausdruck für die Feldvalidierung abrufen. Um diese benutzerdefinierte Funktionsbibliothek bei Server-seitigen Validierungen bekannt und verfügbar zu machen, können Benutzende von Formularen den Namen der AEM-Client-Bibliothek auf der Registerkarte **[!UICONTROL Allgemein]** in den Eigenschaften des Containers für adaptive Formulare konfigurieren.Der Benutzer bzw. die Benutzerin kann eine benutzerdefinierte JavaScript-Bibliothek für jedes adaptive Formular konfigurieren. Legen Sie in der Bibliothek nur die wiederverwendbaren Funktionen ab, die von den Drittanbieter-Bibliotheken „jquery“ und „underscore“ abhängen.

- **Hamburger-Menü für Mobilansicht aktivieren** - Aktivieren Sie das Kontrollkästchen, um ein Hamburger-Menü in Ihr Formular für Mobilansicht zu integrieren. Dieses Menü wird durch drei horizontal gestapelte Linien dargestellt. Es bietet eine klare und übersichtliche Anzeige für Bedienfelder auf kleineren Geräten, insbesondere auf Mobilgeräten. Weitere Informationen zum Hamburger-Menü finden Sie im Abschnitt [Weitere Informationen zum Hamburger-Menü](#learn-more-about-the-hamburger-menu).


### Registerkarte „Datenmodell“ {#data-model-tab}

![Registerkarte „Datenmodell“](/help/adaptive-forms/assets/formcontainer_fdmtab.png)

Sie können das Formulardatenmodell verwenden, um ein Formular mit einer Datenquelle zu verbinden und Daten basierend auf Benutzeraktionen zu senden und zu empfangen. Sie können auch ein Formular mit einem JSON-Schema verbinden, um die gesendeten Daten in einem vordefinierten Format zu empfangen. Verbinden Sie Ihr Formular je nach Anforderung mit einem JSON-Schema oder Formulardatenmodell:
- **None** - Verknüpfen Sie das Formular nicht mit einem Datenmodell.
- **Schema** - Verbinden Sie das Formular mit einem JSON-Schema, das in Ihre Umgebung hochgeladen wurde.
- **Formulardatenmodell** - Verbinden Sie das Formular mit einem Formulardatenmodell, um es in externe Datenquellen zu integrieren.
- **Connector** - Verbinden des Formulars mit einer Connector-basierten Datenquelle.
- **Formularvorlagen** - Verknüpfen Sie das Formular mit einer Formularvorlage.

### Registerkarte Entwürfe {#drafts-tab}

![Registerkarte „Entwürfe“](/help/adaptive-forms/assets/formcontainer_autosavetab.png)

- **Entwürfe automatisch speichern**: Aktivieren Sie das Kontrollkästchen **Entwürfe automatisch speichern**, um das Speichern von Formularen als Entwürfe zu aktivieren.
- **Einstellung speichern**: Konfigurieren Sie **Einstellung speichern** als **Entwürfe in regelmäßigen Abständen speichern**, um das Formular nach einem bestimmten Zeitintervall automatisch zu speichern.
  **Speicherintervall (Sekunden)**: Geben Sie das Zeitintervall (in Sekunden) an, um die Dauer festzulegen, nach der das Formular automatisch in dem definierten Intervall gespeichert wird.

### Registerkarte „Übermittlung“ {#submission-tab}

Benutzende können verschiedene Aktionen für Übermittlungen adaptiver Formulare konfigurieren.

- **Beim Senden** - Wählen Sie **Umleiten zu URL**, um Formularbenutzende nach dem Senden an eine konfigurierte Seite zu senden, oder **Nachricht anzeigen**, um eine Bestätigungsmeldung im Formular anzuzeigen.

- **Umleitungs-URL/-pfad**: Diese Option ermöglicht es, eine Seite für jedes Formular zu konfigurieren, zu dem die Formularbenutzenden nach dem Übermitteln eines adaptiven Formulars umgeleitet werden. Klicken Sie hier, um weitere Informationen zum [Konfigurieren von Umleitungsseiten](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-redirect-page.html?lang=de) zu erhalten.

![Registerkarte „Übermittlung“](/help/adaptive-forms/assets/formcontainer_submissiontab.png)

- **Nachricht anzeigen**: Mit dieser Option können Benutzende eine Nachricht hinzufügen, die angezeigt wird, wenn das adaptive Formular erfolgreich übermittelt wurde. Der vordefinierte Text ist im Dialogfeld enthalten und kann geändert werden. Das Dialogfeld „Nachricht anzeigen“ unterstützt Rich-Text-Formatierungswerkzeuge, mit denen der hinzugefügte Text formatiert werden kann.

![Registerkarte „Nachricht anzeigen“](/help/adaptive-forms/assets/formconatiner_showmessage.png)

- **Übermittlungsaktion**: Eine Übermittlungsaktion wird ausgelöst, wenn in einem adaptiven Formular auf die Schaltfläche „Senden“ geklickt wird. Benutzende können in der Dropdown-Liste „Übermittlungsaktionen“ auswählen, die standardmäßig unterstützt werden. Erfahren Sie, wie Sie [eine Übermittlungsaktion auf der Registerkarte „Übermittlung“ konfigurieren](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html?lang=de#supporting-custom-functions-in-validation-expressions-br).

- **Aktionskonfiguration** - Konfigurieren von Zuordnungen für die Übergabe von Feldwerten als Anforderungsparameter für die Dankeseite.

- **POST-Anfrage aktivieren** - Wählen Sie diese Option, um die Formulardaten mithilfe einer HTTP-POST-Anfrage zu senden.

### Registerkarte „Datensatzdokument“ {#document-of-record-tab}

![Registerkarte „Datensatzdokument“](/help/adaptive-forms/assets/formcontainer_dortab.png)

Ein [Datensatzdokument (DoR) &#x200B;](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/generate-document-of-record-core-components) eine formale, druckbare Darstellung der über das Formular übermittelten Daten. Verwenden Sie die **Datensatzdokument**, um zu konfigurieren, wie ein Datensatzdokument generiert wird, wenn ein Benutzer das Formular sendet:

- **Keine** - Es wird kein Datensatzdokument für das Formular generiert.
- **Formularvorlage als Datensatzdokument-Vorlage zuordnen** - Verwenden Sie eine vorhandene Formularvorlage als DoR-Vorlage.
- **Datensatzdokument generieren** - Automatisches Generieren eines Datensatzdokuments basierend auf den gesendeten Formulardaten.
- **Dateianhänge aus Datensatzdokument ausschließen** - Wählen Sie diese Option, um Dateianhänge aus dem generierten Datensatzdokument wegzulassen.

## Dialogfeld „Design“ {#design-dialog}

Über das Dialogfeld „Design“ können Sie CSS-Stile für die Formular-Container-Komponente definieren und verwalten.

### Registerkarte „Zugelassene Komponenten“ {#allowed-components-tab}

![Registerkarte „Zugelassene Komponenten“ des Dialogfelds „Design“](/help/adaptive-forms/assets/formcontainer-allowedcomponents.png)

Über die Registerkarte **Zugelassene Komponenten** kann die Person, die die Vorlage bearbeitet, festlegen, welche Komponenten im Editor für adaptive Formulare als Elemente zu den Bedienfeldern in der Komponente hinzugefügt werden können.

### Registerkarte „Standardkomponenten“ {#default-components-tab}

![Registerkarte „Standardkomponenten“ des Dialogfelds „Design“](/help/adaptive-forms/assets/formcontainer-defaultcomponents.png)

Über die Registerkarte **Standardkomponenten** kann die Person, die die Vorlage bearbeitet, festlegen, welche Komponenten standardmäßig als Elemente der Formular-Container-Komponente im Editor für adaptive Formulare angezeigt werden sollen.

### Registerkarte „Responsive Einstellungen“ {#responsive-tab}

![Registerkarte „Responsive Einstellungen“ des Dialogfelds „Design“](/help/adaptive-forms/assets/formcontainer-responsivestyle.png)

Über die Registerkarte **Responsive Einstellungen** kann die Person, die die Vorlage bearbeitet, die Anzahl der Rasterspalten der Formular-Container-Komponente im Editor für adaptive Formulare festlegen.

### Registerkarte „Stile“ {#styles-tab}

Die Kernkomponente „Dateianhänge“ für adaptive Formulare unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).

![Dialogfeld „Design“](/help/adaptive-forms/assets/formcontainer-styletab.png)

- **Standard-CSS-Klassen**: Sie können eine standardmäßige CSS-Klasse für die Kernkomponente „Formular-Container“ für adaptive Formulare bereitstellen.

- **Zulässige Stile**: Sie können Stile definieren, indem Sie den Namen und die CSS-Klasse für den Stil angeben. Sie können beispielsweise einen Stil mit dem Namen „Fettschrift“ erstellen und die CSS-Klasse „Schriftbreite: Fett“ bereitstellen. Sie können diese Stile bei einem adaptiven Formular im adaptiven Formular-Editor anwenden. Um einen Stil anzuwenden, wählen Sie im Editor für adaptive Formulare die Komponente aus, auf die Sie den Stil anwenden möchten, navigieren Sie zum Eigenschaften-Dialog und wählen Sie den gewünschten Stil aus der Dropdown-Liste **Stile**. Wenn Sie die Stile aktualisieren oder ändern müssen, kehren Sie einfach zum Dialogfeld „Design“ zurück, aktualisieren die Stile auf der Registerkarte „Stile“ und speichern die Änderungen.

### Registerkarte „Benutzerdefinierte Eigenschaften“

![Dialogfeld „Benutzerdefinierte Eigenschaften“](/help/adaptive-forms/assets/formcontainer-custompropertiestab.png)

Mit der Option „Benutzerdefinierte Eigenschaften“ können Sie mithilfe der Formularvorlage benutzerdefinierte Attribute (Schlüsselwertpaare) mit einer Kernkomponente eines adaptiven Formulars verknüpfen. Die benutzerdefinierten Eigenschaften werden im Eigenschaftenbereich der Headless-Ausgabedarstellung der Komponente angezeigt. So kann ein dynamisches Formularverhalten erzeugt werden, das sich je nach den benutzerdefinierten Attributwerten anpasst. Beispielsweise können Entwickelnde verschiedene Ausgabedarstellungen einer Headless-Formularkomponente für Mobile-, Desktop- oder Web-Plattformen entwerfen und so das Benutzererlebnis auf einer Vielzahl von Geräten erheblich verbessern.

- **Gruppenname**: Sie können einen Namen angeben, um die Gruppe der benutzerdefinierten Eigenschaften zu kennzeichnen. Sie können mehrere Gruppen benutzerdefinierter Eigenschaften hinzufügen, löschen oder neu anordnen. Nach dem Hinzufügen der Gruppe benutzerdefinierter Eigenschaften werden folgende Optionen angezeigt:

   - **Schlüssel-Wert-Paare**: Sie können mehrere Namen und Werte benutzerdefinierter Eigenschaften hinzufügen, indem Sie für jede Gruppe benutzerdefinierter Eigenschaften auf **Hinzufügen** klicken.

   - **Löschen**: Tippen oder klicken Sie auf diese Option, um den Namen und den Wert der benutzerdefinierten Eigenschaft zu löschen.

   - **Neu anordnen**: Ordnen Sie den Namen und Wert der benutzerdefinierten Eigenschaft Antippen oder Klicken und Ziehen neu an.

## Weitere Informationen zum Hamburger-Menü {#learn-more-about-the-hamburger-menu}

Ein Hamburger-Menü, häufig als Mobilmenü oder Navigationsschublade bezeichnet, ist ein beliebtes Design-Element in mobilen Benutzeroberflächen. Es zeigt drei horizontale Linien, die vertikal gestapelt sind und einem Hamburger ähneln. Das Design spart effizient Platz auf dem Bildschirm, indem sekundäre Navigationsoptionen ausgeblendet werden, bis sie benötigt werden, insbesondere auf kleineren Geräten wie Mobilgeräten. AEM-Formulare können effizient im Hamburger-Menü organisiert werden, sodass Benutzende auf verschiedene Bereiche innerhalb eines Formulars zugreifen können, ohne die Hauptbenutzeroberfläche zu überfordern.

Betrachten wir ein Szenario, in dem ein Finanzinstitut ein Online-Kreditantragsformular anbietet, in dem die Benutzer detaillierte Informationen über mehrere Bedienfelder hinweg bereitstellen müssen, z. B. persönliche Details, Finanzinformationen, Kreditvoreinstellungen und Belege. Das Formular enthält mehrere Bedienfelder und Optionen, die die Benutzeroberfläche insbesondere auf Mobilgeräten überladen können. Benutzende benötigen eine organisierte Möglichkeit, durch diese Bedienfelder zu navigieren, ohne überfordert zu sein. Das Hamburger-Menü wird implementiert, um das Benutzererlebnis auf Mobilgeräten zu verbessern.

### Komponenten des Hamburger-Menüs

![Hamburger-](/help/adaptive-forms/assets/hamburger-menu.png){width=50%, align=center}

**a. Hamburger-**: Das Hamburger-Menü enthält einen Navigationsbereich, der beim Klicken oder Tippen auf das Hamburger-Symbol ausgeblendet oder heruntergefahren wird. Das Menü zeigt die Bereichsüberschriften an, und durch Auswahl eines Bereichs wird der Fokus auf diesen Bereich verschoben. Benutzende können damit einfach zwischen verschiedenen Bedienfeldern navigieren.

![Hamburger-](/help/adaptive-forms/assets/hamburger-menu-icon.png){width=50%}

**b. Breadcrumb**: Breadcrumbs geben den aktuellen Speicherort des Benutzers im Formular an. Sie bieten ein hierarchisches Protokoll, das den Navigationspfad der Benutzenden anzeigt und ihnen dabei hilft, ihre Position im Formular zu verstehen.

**C. Aktives Bedienfeld**: Das aktive Bedienfeld bezieht sich auf den Abschnitt oder Teil des Formulars, der derzeit angezeigt wird. Wenn ein(e) Benutzende(r) eine Option aus dem Hamburger-Menü auswählt, wird das entsprechende Bedienfeld zum aktiven Bedienfeld, das die relevanten Felder und Informationen für diesen Abschnitt anzeigt.

### Beim Arbeiten mit dem Hamburger-Menü zu berücksichtigende Punkte

- Das Menü „Hamburger“ zeigt nur die Namen der Bedienfelder an. Im Folgenden finden Sie verschiedene Szenarien, die zeigen, wie der Bereichsname basierend auf den Konfigurationseigenschaften des Bereichs im Navigationsbereich des Hamburger-Menüs angezeigt wird:

   - Wenn Sie die Eigenschaften des Bereichs auf „Ausgeblendet“ setzen, wird der Name des Bereichs nicht im Navigationsbereich des Hamburger-Menüs angezeigt. Wenn Sie beispielsweise die Eigenschaften des `Financial Information` Bedienfelds als `hidden` konfigurieren, wird der Bereichsname nicht im Navigationsbereich des Hamburger-Menüs angezeigt.

     ![Ausgeblendetes Bedienfeld](/help/adaptive-forms/assets/hidden-panel.png){width=50%}

   - Wenn Sie die Eigenschaften des Bedienfelds auf `disabled` setzen, wird sein Name im Navigationsbereich des Hamburger-Menüs angezeigt, Sie können ihn jedoch nicht auswählen oder bearbeiten. Wenn Sie beispielsweise die Eigenschaften des `Financial Information` Bedienfelds als `disabled` konfigurieren, wird der Bereichsname im Navigationsbereich angezeigt, kann jedoch nicht ausgewählt oder bearbeitet werden.

     ![Bedienfeld deaktiviert](/help/adaptive-forms/assets/disabled-panel.png){width=50%}

   - Wenn Sie den Titel des Bedienfelds ausblenden, wird es nicht im Navigationsbereich des Hamburger-Menüs angezeigt. Stattdessen wird eine leere Platzierung angezeigt. Sie können jedoch zu den Feldern des Bedienfelds navigieren, indem Sie auf diese Platzierung klicken. Wenn Sie beispielsweise den Titel des `Financial Information` Bedienfelds ausblenden, wird das leere Feld an dieser Stelle im Navigationsbereich des Hamburger-Menüs angezeigt. Sie können zu den Feldern des Bedienfelds navigieren, indem Sie auf die Leerstelle klicken.

     ![Ausgeblendetes Titelfeld](/help/adaptive-forms/assets/hidden-title-panel.png){width=50%}

- Standardmäßig unterstützt der Navigationsbereich in der Breadcrumb-Komponente bis zu drei Navigationsebenen. Mit der benutzerdefinierten Komponente können Sie jedoch die Navigationshierarchie so konfigurieren, dass sie beliebig viele Ebenen aufnimmt.
- Bei Verwendung des Menüs „Hamburger“ können Benutzende mit Pfeilen zwischen Bedienfeldern navigieren. Sobald ein Bedienfeld ausgewählt wurde, wird das Menü jedoch automatisch geschlossen und der Fokus wechselt zu den Feldern im ausgewählten Bedienfeld.

<!--
### Advantages to use hamburger menu

- **Space efficiency**: By hiding form navigation options until needed, the hamburger menu maximizes screen space, which is especially beneficial on smaller devices.

- **Clutter reduction**: It minimizes visual clutter by consolidating various form navigation links into a single, collapsible menu.

- **Improved focus**: With fewer visible navigation elements, users can concentrate on the main content of the form without being distracted by secondary options.

- **Simplified design**: It creates a more streamlined user interface, resulting in a cleaner and more organized form layout.

- **Enhanced mobile experience**: On mobile devices, where screen space is limited, the hamburger menu offers an efficient way to access all form navigation options without overwhelming the user.

### How to enable hamburger menu for your form?

To enable hamburger menu for form, perform the following steps:

1. Open form in an edit mode.
1. Open the Content browser, and select the **[!UICONTROL Guide Container]** component of your Adaptive Form. 
1. Click the Guide Container properties ![Guide properties](/help/adaptive-forms/assets/configure_icon.png) icon. The Adaptive Form Container dialog box opens. 
1. Click the  **[!UICONTROL Basic]** tab. 
1. Select the **[!UICONTROL Add hamburger menu support]** checkbox.
1. Click **[!UICONTROL Done]**.

![Basic tab](/help/adaptive-forms/assets/formcontainer_basictab1.png)
-->

## Ähnliche Artikel {#related-articles}

{{more-like-this}}

## Siehe auch {#see-also}

{{see-also}}