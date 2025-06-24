---
title: Kernkomponente für adaptive Formulare – Formular-Container
description: Ein adaptives Formular zu einer Web-Seite hinzufügen.
role: Architect, Developer, Admin, User
exl-id: 03c4cf7c-51d6-4850-a566-1c0514d52dab
source-git-commit: 6725784bd4c94d433c91d6bd65d14d03cbefd954
workflow-type: tm+mt
source-wordcount: '1524'
ht-degree: 97%

---


# Formular-Container {#form-container-adaptive-forms-core-component}

<span class="preview"> In diesem Artikel wird die Funktion **Entwürfe** <!--and **Hamburger Menu Support** --> erläutert, bei der es sich um eine Vorabveröffentlichungsfunktion handelt. Die Vorabveröffentlichungsfunktion ist nur über unseren [Vorabveröffentlichungskanal](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/release-notes/prerelease.html?lang=de#new-features) zugänglich.</span>

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

Die Kernkomponente „Adaptive Forms Akkordeon“ wurde im Februar 2023 als Teil der Kernkomponenten 2.0.4 für Cloud Service und der Kernkomponenten 1.1.12 für AEM 6.5.16.0 Forms oder höher veröffentlicht. Hier finden Sie eine Tabelle mit allen unterstützten Versionen, AEM-Kompatibilität und Links zur entsprechenden Dokumentation:

| Komponentenversion | AEM as a Cloud Service | AEM 6.5.16.0 Forms oder höher |
|---|---|---|
| v1 | Kompatibel mit<br>[Version 2.0.4](/help/adaptive-forms/version.md) und höher | Kompatibel mit<br>[Version 1.1.12](/help/adaptive-forms/version.md) und höher (aber nur bis Version 2.0.0). |

Informationen zu Versionen und Freigaben der Kernkomponente finden Sie im Dokument [Kernkomponenten-Versionen](/help/adaptive-forms/version.md).
<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technische Details {#technical-details}

Aktuelle Informationen über die Container-Kernkomponente für adaptive Formulare finden Sie in der technischen Dokumentation auf [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/container/v1/container). Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Entwicklerdokumentation für Kernkomponenten](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Mit dem Dialogfeld „Konfigurieren“ können Sie das Formular-Container-Erlebnis für Besuchende einfach anpassen. Sie können Formular-Container-Optionen auch einfach definieren, um ein nahtloses Anwendererlebnis zu gewährleisten.

### Registerkarte „Allgemein“ {#basic-tab}

![Registerkarte „Allgemein“](/help/adaptive-forms/assets/formcontainer_basictab1.png)

- **Titel**: Mit dem Titel können Sie eine Komponente in einem Formular leicht identifizieren. Standardmäßig wird der Titel oberhalb der Komponente angezeigt. Wenn Sie keinen Titel hinzufügen, wird der Name der Komponente anstelle des Titeltexts angezeigt.

- **Vorbefüllungs-Services**: Diese Option ermöglicht es Benutzenden, einen Vorbefüllungs-Service zum Abrufen von Daten auszuwählen, wenn das adaptive Formular gerendert wird. Weitere Informationen zum [Erstellen und Konfigurieren eines Vorbefüllungs-Services](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/prepopulate-adaptive-form-fields.html?lang=de#aem-forms-custom-prefill-service).

- **Rolle**: Die Rolle ist ein HTML-Attribut, mit dem der Zweck eines HTML-Elements für Hilfstechnologien wie Bildschirmlesehilfen angegeben wird. Rollenattribute werden verwendet, um für ein Element zusätzlichen Kontext und eine semantische Bedeutung bereitzustellen, wodurch es für Bildschirmlesehilfen einfacher wird, den Inhalt zu interpretieren und ihn Benutzenden mitzuteilen. In AEM Forms kann beispielsweise die Beschriftung eines Formularfelds die Rolle „Beschriftung“ haben und sein Eingabefeld die Rolle „Textfeld“. Dadurch kann die Bildschirmlesehilfe die Beziehung zwischen Beschrfitung und Eingabefeld verstehen und diese Informationen den Benutzenden korrekt mitteilen.

- **Client-Bibliothekskategorie**: Benutzende können eine benutzerdefinierte JavaScript-Bibliothek pro adaptivem Formular konfigurieren. Es wird empfohlen, nur die wiederverwendbaren Funktionen in der Bibliothek zu behalten, die von den Drittanbieter-Bibliotheken „jquery“ und „underscore.js“ abhängig sind.
Bisweilen befindet sich bei komplexen **Validierungsregeln** das exakte Validierungsskript in den benutzerdefinierten Funktionen. Benutzende können diese benutzerdefinierten Funktionen über den Ausdruck für die Feldvalidierung abrufen. Um diese benutzerdefinierte Funktionsbibliothek bei Server-seitigen Validierungen bekannt und verfügbar zu machen, können Benutzende von Formularen den Namen der AEM-Client-Bibliothek auf der Registerkarte **[!UICONTROL Allgemein]** in den Eigenschaften des Containers für adaptive Formulare konfigurieren.
Der Benutzer bzw. die Benutzerin kann eine benutzerdefinierte JavaScript-Bibliothek für jedes adaptive Formular konfigurieren. Legen Sie in der Bibliothek nur die wiederverwendbaren Funktionen ab, die von den Drittanbieter-Bibliotheken „jquery“ und „underscore“ abhängen.

<!--
- **Enable the hamburger menu for mobile view** - Select the checkbox to integrate a hamburger menu into your form for mobile view. Represented by three horizontal lines stacked vertically, this menu provides a clear and uncluttered display for panels on smaller devices, especially on mobile devices. For more information about the hamburger menu, refer to the [Learn more about the hamburger menu](#learn-more-about-the-hamburger-menu) section. -->


### Registerkarte „Datenmodell“ {#data-model-tab}

![Registerkarte „Übermittlung“](/help/adaptive-forms/assets/formcontainer_fdmtab.png)

Sie können das Formulardatenmodell verwenden, um ein Formular mit einer Datenquelle zu verbinden und Daten basierend auf Benutzeraktionen zu senden und zu empfangen. Sie können auch ein Formular mit einem JSON-Schema verbinden, um die gesendeten Daten in einem vordefinierten Format zu empfangen. Verbinden Sie Ihr Formular je nach Anforderung mit einem JSON-Schema oder Formulardatenmodell:
- Erstellen Sie ein JSON-Schema und laden Sie es in Ihre Umgebung hoch
- Erstellen eines Formulardatenmodells

### Entwürfe

![Registerkarte „Übermittlung“](/help/adaptive-forms/assets/formcontainer_autosavetab.png)

- **Entwürfe automatisch speichern**: Aktivieren Sie das Kontrollkästchen **Entwürfe automatisch speichern**, um das Speichern von Formularen als Entwürfe zu aktivieren.
- **Einstellung speichern**: Konfigurieren Sie **Einstellung speichern** als **Entwürfe in regelmäßigen Abständen speichern**, um das Formular nach einem bestimmten Zeitintervall automatisch zu speichern.
  **Speicherintervall (Sekunden)**: Geben Sie das Zeitintervall (in Sekunden) an, um die Dauer festzulegen, nach der das Formular automatisch in dem definierten Intervall gespeichert wird.

### Registerkarte „Übermittlung“ {#submission-tab}

Benutzende können verschiedene Aktionen für Übermittlungen adaptiver Formulare konfigurieren.

- **Umleitungs-URL/-pfad**: Diese Option ermöglicht es, eine Seite für jedes Formular zu konfigurieren, zu dem die Formularbenutzenden nach dem Übermitteln eines adaptiven Formulars umgeleitet werden. Klicken Sie hier, um weitere Informationen zum [Konfigurieren von Umleitungsseiten](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-redirect-page.html?lang=de) zu erhalten.

![Registerkarte „Übermittlung“](/help/adaptive-forms/assets/formcontainer_submissiontab.png)

- **Nachricht anzeigen**: Mit dieser Option können Benutzende eine Nachricht hinzufügen, die angezeigt wird, wenn das adaptive Formular erfolgreich übermittelt wurde. Der vordefinierte Text ist im Dialogfeld enthalten und kann geändert werden. Das Dialogfeld „Nachricht anzeigen“ unterstützt Rich-Text-Formatierungswerkzeuge, mit denen der hinzugefügte Text formatiert werden kann.

![Registerkarte „Nachricht anzeigen“](/help/adaptive-forms/assets/formconatiner_showmessage.png)

- **Übermittlungsaktion**: Eine Übermittlungsaktion wird ausgelöst, wenn in einem adaptiven Formular auf die Schaltfläche „Senden“ geklickt wird. Benutzende können in der Dropdown-Liste „Übermittlungsaktionen“ auswählen, die standardmäßig unterstützt werden. Erfahren Sie, wie Sie [eine Übermittlungsaktion auf der Registerkarte „Übermittlung“ konfigurieren](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html?lang=de#supporting-custom-functions-in-validation-expressions-br).

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

<!--
## Learn more about the hamburger menu

A hamburger menu, often referred to as a mobile menu or navigation drawer, is a popular design element in mobile user interfaces. It features three horizontal lines stacked vertically, resembling a hamburger. The design efficiently conserves screen space by hiding secondary navigation options until they are needed, especially on smaller devices such as mobile. AEM forms can be efficiently organized within the hamburger menu, enabling users to access various panels within a form without overwhelming the main interface.

Consider a scenario, where a financial institution offers an online loan application form that requires users to provide detailed information across several panels, such as personal details, financial information, loan preferences, and supporting documents. The form includes multiple panels and options that can clutter the interface, especially on mobile devices. Users need an organized way to navigate through these panels without feeling overwhelmed. The hamburger menu is implemented to enhance the user experience on mobile devices.

### Components of hamburger menu

![Hamburger Menu](/help/adaptive-forms/assets/hamburger-menu.png){width=50%, align=center}

**A. Hamburger menu**: The hamburger menu features a navigation panel that slides out or drops down when the hamburger icon is clicked or tapped. The menu displays the panel headings, and selecting a panel shifts the focus to that panel. It allows users to easily navigate between different panels.

![Hamburger Menu](/help/adaptive-forms/assets/hamburger-menu-icon.png){width=50%}

**B. Breadcrumb**: Breadcrumbs indicate the user’s current location within the form. They offer a hierarchical trail that shows the user’s navigation path and helps them understand their position in the form.

**C. Active panel**: The active panel refers to the section or part of the form that is currently being displayed. When a user selects an option from the hamburger menu, the corresponding panel becomes the active panel, showing the relevant fields and information for that section.

### Points to consider while working with the hamburger menu

- The hamburger menu displays only the names of the panels. Here are different scenarios illustrating how the panel name appears in the navigation pane of the hamburger menu based on the configuration properties of the panel:  
  
  - If you set the properties of the panel to hidden, the panel's name does not appear in the navigation pane of the hamburger menu. For example, if you configure the properties of the `Financial Information` panel as `hidden`, the panel name does not appear in the navigation pane of the hamburger menu.
    
    ![Hidden panel](/help/adaptive-forms/assets/hidden-panel.png){width=50%}

  - If you set the properties of the panel to `disabled`, its name appears in the navigation pane of the hamburger menu, but you cannot select or edit it. For example, if you configure the properties of the `Financial Information` panel as `disabled`, the panel name appears in the navigation pane, but it cannot be selected or edited. 
     
    ![Disabled panel](/help/adaptive-forms/assets/disabled-panel.png){width=50%}

  - If you hide the  title of the panel, it does not appear in the navigation pane of the hamburger menu. A blank space shows up instead, but you can navigate to the fields of the panel by clicking on that space. For example, if you hide the title of the `Financial Information` panel, the blank space appears in its place in the navigation pane of the hamburger menu. You can navigate to the fields of the panel by clicking on the blank space.
    
    ![Hidden title panel](/help/adaptive-forms/assets/hidden-title-panel.png){width=50%}

- By default, the navigation pane in the breadcrumb component supports up to three levels of navigation. However, with the custom component, you can configure the navigation hierarchy to accommodate as many levels as needed.
- When using the hamburger menu, the user can navigate between panels using arrows. However, once a panel is selected, the menu automatically closes, and focus shifts to the fields within the chosen panel.

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

![Basic tab](/help/adaptive-forms/assets/formcontainer_basictab.png)
-->

## Ähnliche Artikel {#related-articles}

{{more-like-this}}

## Siehe auch {#see-also}

{{see-also}}