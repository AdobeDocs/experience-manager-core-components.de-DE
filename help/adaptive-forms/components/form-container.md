---
title: Kernkomponente für adaptive Formulare – Formular-Container
description: Ein adaptives Formular zu einer Web-Seite hinzufügen.
role: Architect, Developer, Admin, User
exl-id: 03c4cf7c-51d6-4850-a566-1c0514d52dab
source-git-commit: 8bba79956a04020647d5d04f9fe6fa674affedf1
workflow-type: tm+mt
source-wordcount: '1341'
ht-degree: 100%

---

# Formular-Container {#form-container-adaptive-forms-core-component}

Mit Formularen können Besuchende von Websites mit der Website interagieren, indem sie wertvolle Informationen bereitstellen, die die Interaktion und Benutzerzufriedenheit steigern können. Ein Container für adaptive Formulare in Adobe Experience Manager-Sites (AEM) ermöglicht es Besitzenden von Websites, ihren Seiten ganz einfach Formulare hinzuzufügen. Dies erleichtert die Kommunikation zwischen Website-Besuchenden und Besitzenden oder der Organisation der Website, da Besuchende auf diese Weise Feedback geben, Anfragen stellen und andere Aktionen ausführen können

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
<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technische Details {#technical-details}

Aktuelle Informationen über die Container-Kernkomponente für adaptive Formulare finden Sie in der technischen Dokumentation auf [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/container/v1/container). Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Entwicklerdokumentation für Kernkomponenten](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Mit dem Dialogfeld „Konfigurieren“ können Sie das Formular-Container-Erlebnis für Besuchende einfach anpassen. Sie können Formular-Container-Optionen auch einfach definieren, um ein nahtloses Anwendererlebnis zu gewährleisten.

### Registerkarte „Allgemein“ {#basic-tab}

![Registerkarte „Allgemein“](/help/adaptive-forms/assets/formcontainer_basictab.png)

- **Titel**: Mit dem Titel können Sie eine Komponente in einem Formular leicht identifizieren. Standardmäßig wird der Titel oberhalb der Komponente angezeigt. Wenn Sie keinen Titel hinzufügen, wird der Name der Komponente anstelle des Titeltexts angezeigt.

- **Vorbefüllungs-Services**: Diese Option ermöglicht es Benutzenden, einen Vorbefüllungs-Service zum Abrufen von Daten auszuwählen, wenn das adaptive Formular gerendert wird. Weitere Informationen zum [Erstellen und Konfigurieren eines Vorbefüllungs-Services](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/prepopulate-adaptive-form-fields.html?lang=de#aem-forms-custom-prefill-service).

- **Client-Bibliothekskategorie**: Benutzende können eine benutzerdefinierte JavaScript-Bibliothek pro adaptivem Formular konfigurieren. Es wird empfohlen, nur die wiederverwendbaren Funktionen in der Bibliothek zu behalten, die von den Drittanbieter-Bibliotheken „jquery“ und „underscore.js“ abhängig sind.
Bisweilen befindet sich bei komplexen **Validierungsregeln** das exakte Validierungsskript in den benutzerdefinierten Funktionen. Benutzende können diese benutzerdefinierten Funktionen über den Ausdruck für die Feldvalidierung abrufen. Um diese benutzerdefinierte Funktionsbibliothek bei Server-seitigen Validierungen bekannt und verfügbar zu machen, kann der Formularbenutzer bzw. die -benutzerin den Namen der AEM-Client-Bibliothek auf der Registerkarte **[!UICONTROL Allgemein]** des Dialogfelds „Container für adaptive Formulare bearbeiten“, wie nachfolgend dargestellt konfigurieren.

Der Benutzer bzw. die Benutzerin kann eine benutzerdefinierte JavaScript-Bibliothek für jedes adaptive Formular konfigurieren. Legen Sie in der Bibliothek nur die wiederverwendbaren Funktionen ab, die von den Drittanbieter-Bibliotheken „jquery“ und „underscore“ abhängen.

### Registerkarte „Datenmodell“ {#data-model-tab}

![Registerkarte „Übermittlung“](/help/adaptive-forms/assets/formcontainer_fdmtab.png)

Sie können das Formulardatenmodell verwenden, um ein Formular mit einer Datenquelle zu verbinden und Daten basierend auf Benutzeraktionen zu senden und zu empfangen. Sie können auch ein Formular mit einem JSON-Schema verbinden, um die gesendeten Daten in einem vordefinierten Format zu empfangen. Verbinden Sie Ihr Formular je nach Anforderung mit einem JSON-Schema oder Formulardatenmodell:
- Erstellen Sie ein JSON-Schema und laden Sie es in Ihre Umgebung hoch
- Erstellen eines Formulardatenmodells

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

## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html)

-->

## Ähnliche Artikel {#related-articles}

{{more-like-this}}

## Siehe auch {#see-also}

{{see-also}}