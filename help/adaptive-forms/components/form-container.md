---
title: Adaptive Forms-Kernkomponente - Formular-Container
description: Fügen Sie ein adaptives Formular zu einer Webseite hinzu.
role: Architect, Developer, Admin, User
source-git-commit: d2a6108f17f6e0c6b91bec84893d64a8bd48effd
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 2%

---


# Formular-Container {#form-container-adaptive-forms-core-component}

Mit Forms können Besucher von Websites mit der Website interagieren, indem sie wertvolle Informationen bereitstellen, die die Interaktion und Benutzerzufriedenheit steigern können. Ein Container für adaptive Formulare in Adobe Experience Manager (AEM) Sites ermöglicht es Website-Eigentümern, ihren Seiten einfach Formulare hinzuzufügen. Dies erleichtert die Kommunikation zwischen Website-Besuchern und dem Eigentümer oder der Organisation der Website, da Besucher auf diese Weise Feedback geben, Anfragen stellen und andere Aktionen ausführen können.

## Verwendung {#reasons-to-use-forms-container}

Es gibt mehrere Gründe, warum ein Formular einer Website hinzugefügt werden kann:

* **Datenerfassung**: Forms kann verwendet werden, um Daten von Website-Besuchern für verschiedene Zwecke zu erfassen, wie z. B. Marktforschung, Benutzerverhaltensanalyse und mehr.

* **Lead-Generierung**: Ein Formular kann verwendet werden, um Informationen potenzieller Kunden zu sammeln, wie z. B. Name und E-Mail-Adresse, um Leads für Verkaufs- und Marketingaktivitäten zu generieren.

* **E-Commerce**: Forms kann für Online-Shopping verwendet werden, sodass Kunden Bestellungen aufgeben und Zahlungen über die Website tätigen können.

* **Kontakt**: Mit einem Kontaktformular können Besucher der Website einfach den Website-Eigentümer oder die Organisation erreichen.

* **Umfragen und Umfragen**: Forms kann verwendet werden, um Feedback und Meinungen von Besuchern der Website durch Umfragen und Umfragen zu sammeln.

* **Ereignisregistrierung**: Forms kann für die Ereignisregistrierung verwendet werden, sodass sich Website-Besucher für Veranstaltungen oder Webinare anmelden können.

* **Abonnements**: Forms kann für Website-Abonnements verwendet werden, sodass sich Besucher für einen Newsletter oder andere regelmäßige Nachrichten anmelden können.

* **Benutzerauthentifizierung**: Forms kann für die Benutzerauthentifizierung verwendet werden, sodass Website-Besucher Konten erstellen und sich anmelden können, um auf exklusive Inhalte oder Funktionen zuzugreifen.

* **Konversionsrate erhöhen**: Ein gut gestaltetes Formular kann die Konversionsrate steigern, indem es es den Benutzern erleichtert, eine gewünschte Aktion auszuführen, z. B. ein Produkt zu erwerben oder sich für einen Dienst anzumelden.


## Version und Kompatibilität {#version-and-compatibility}

Die Kernkomponente &quot;Adaptive Forms Accordion&quot;wurde im Februar 2023 als Teil der Kernkomponenten 2.0.4 für Cloud Service und Kernkomponenten 1.1.12 für AEM 6.5.16.0 Forms oder höher veröffentlicht. In der folgenden Tabelle finden Sie alle unterstützten Versionen, AEM Kompatibilität und Links zur entsprechenden Dokumentation:

| Komponentenversion | AEM as a Cloud Service | AEM 6.5.16.0 Forms oder höher |
|---|---|---|
| v1 | Kompatibel mit<br>[Version 2.0.4](/help/adaptive-forms/version.md) und höher | Kompatibel mit<br>[Version 1.1.12](/help/adaptive-forms/version.md) und höher, jedoch weniger als 2.0.0. |

Informationen zu Kernkomponentenversionen und -versionen finden Sie im Abschnitt [Kernkomponenten-Versionen](/help/adaptive-forms/version.md) Dokument.
<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technische Details {#technical-details}

Laden Sie die neuesten Informationen zur Kernkomponente &quot;Adaptiver Forms-Container&quot;in der technischen Dokumentation zu [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/container/v1/container). Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie im Abschnitt [Entwicklerdokumentation für Kernkomponenten](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Mit dem Dialogfeld &quot;Konfigurieren&quot;können Sie das Erlebnis Ihres Formular-Containers für Besucher einfach anpassen. Sie können Formularcontainer-Optionen auch einfach definieren, um eine nahtlose Benutzererfahrung zu gewährleisten.

### Einfache Registerkarte {#basic-tab}

![Registerkarte &quot;Allgemein&quot;](/help/adaptive-forms/assets/formcontainer_basictab.png)

* **Vorbefüllungsdienste** - Mit dieser Option kann der Benutzer einen Vorbefüllungs-Dienst zum Abrufen von Daten auswählen, wenn das adaptive Formular wiedergegeben wird. Weitere Informationen [Erstellen und Konfigurieren eines Vorbefüllungs-Dienstes](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/prepopulate-adaptive-form-fields.html?lang=en#aem-forms-custom-prefill-service).

* **Kategorie der Client-Bibliothek** - Der Benutzer kann die benutzerdefinierte JavaScript-Bibliothek pro adaptivem Formular konfigurieren. Es wird empfohlen, nur die wiederverwendbaren Funktionen in der Bibliothek zu behalten, die von den Drittanbieter-Bibliotheken jquery und underscore.js abhängig sind.

### Registerkarte &quot;Einsendung&quot; {#submission-tab}

![Registerkarte &quot;Übermittlung&quot;](/help/adaptive-forms/assets/formcontainer_submissiontab.png)

Benutzer können verschiedene Aktionen für Übermittlungen adaptiver Formulare konfigurieren.

* **Umleitungs-URL/Pfad** - Diese Option ermöglicht es dem Benutzer, eine Seite für jedes Formular zu konfigurieren, zu dem die Formularbenutzer nach dem Senden eines adaptiven Formulars umgeleitet werden. Weitere Informationen finden Sie hier . [Konfigurieren von Umleitungsseiten](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-redirect-page.html).

![Registerkarte &quot;Meldung anzeigen&quot;](/help/adaptive-forms/assets/formconatiner_showmessage.png)

* **Nachricht anzeigen** - Mit dieser Option können Benutzer eine Nachricht hinzufügen, die angezeigt wird, wenn das adaptive Formular erfolgreich gesendet wurde. Der vordefinierte Text ist im Dialogfeld enthalten und kann vom Benutzer geändert werden. Das Dialogfeld &quot;Meldung anzeigen&quot;unterstützt Rich-Text-Formatierungswerkzeuge, mit denen Benutzer den hinzugefügten Text formatieren können.

* **Übermittlungsaktion** - Eine Sendeaktion wird ausgelöst, wenn ein Benutzer in einem adaptiven Formular auf die Schaltfläche Senden klickt. Benutzer können in der Dropdown-Liste die Option Übermittlungsaktionen auswählen, die standardmäßig unterstützt werden. Erfahren Sie, wie Sie [Konfigurieren einer Sendeaktion auf der Registerkarte &quot;Sendung&quot;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html#supporting-custom-functions-in-validation-expressions-br).
