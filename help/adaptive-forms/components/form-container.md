---
title: Kernkomponente für adaptive Formulare – Formular-Container
description: Ein adaptives Formular zu einer Web-Seite hinzufügen.
role: Architect, Developer, Admin, User
exl-id: 8df7f862-4d59-4c3f-88dd-f0c937081f4f
source-git-commit: 7888cfa0f1358ce8018fc1e3cc3b19eb66a82b9d
workflow-type: tm+mt
source-wordcount: '755'
ht-degree: 96%

---

# Formular-Container {#form-container-adaptive-forms-core-component}

Mit Formularen können Besuchende von Websites mit der Website interagieren, indem sie wertvolle Informationen bereitstellen, die die Interaktion und Benutzerzufriedenheit steigern können. Ein Container für adaptive Formulare in Adobe Experience Manager-Sites (AEM) ermöglicht es Besitzenden von Websites, ihren Seiten ganz einfach Formulare hinzuzufügen. Dies erleichtert die Kommunikation zwischen Website-Besuchenden und Besitzenden oder der Organisation der Website, da Besuchende auf diese Weise Feedback geben, Anfragen stellen und andere Aktionen ausführen können

## Verwendung {#reasons-to-use-forms-container}

Es gibt mehrere Gründe, warum ein Formular einer Website hinzugefügt werden kann:

* **Datenerfassung**: Formulare können verwendet werden, um Daten von Website-Besuchenden für verschiedene Zwecke zu erfassen, wie z. B. Marktforschung, Benutzerverhaltensanalyse und mehr.

* **Lead-Generierung**: Ein Formular kann verwendet werden, um Informationen potenzieller Kunden und Kundinnen zu sammeln, wie z. B. Name und E-Mail-Adresse, um Leads für Verkaufs- und Marketing-Maßnahmen zu generieren.

* **E-Commerce**: Formulare können für Online-Shopping verwendet werden, sodass die Kundschaft Bestellungen aufgeben und Zahlungen über die Website tätigen kann.

* **Kontakt**: Mit einem Kontaktformular können Besuchende der Website einfach den Besitzenden oder die Organisation der Website erreichen.

* **Befragungen und Umfragen**: Formulare können verwendet werden, um Feedback und Meinungen von Besuchenden der Website durch Befragungen und Umfragen zu sammeln.

* **Registrierung für Veranstaltungen**: Formulare können zur Registrierung für Veranstaltungen verwendet werden, sodass sich Website-Besuchende für Veranstaltungen oder Webinare anmelden können.

* **Abonnements**: Formulare können für Website-Abonnements verwendet werden, sodass sich Besuchende für einen Newsletter oder andere regelmäßige Nachrichten anmelden können.

* **Benutzerauthentifizierung**: Formulare können für die Benutzerauthentifizierung verwendet werden, sodass Website-Besuchende Konten erstellen und sich anmelden können, um auf exklusive Inhalte oder Funktionen zuzugreifen.

* **Erhöhung der Konversionsrate**: Ein gut gestaltetes Formular kann die Konversionsrate erhöhen, indem das Formular es den Benutzenden erleichtert, eine gewünschte Aktion auszuführen, z. B. ein Produkt zu erwerben oder sich für einen Service anzumelden.


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

* **Vorbefüllungs-Services**: Diese Option ermöglicht es Benutzenden, einen Vorbefüllungs-Service zum Abrufen von Daten auszuwählen, wenn das adaptive Formular gerendert wird. Weitere Informationen zum [Erstellen und Konfigurieren eines Vorbefüllungs-Services](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/prepopulate-adaptive-form-fields.html?lang=de#aem-forms-custom-prefill-service).

* **Client-Bibliothekskategorie**: Benutzende können eine benutzerdefinierte JavaScript-Bibliothek pro adaptivem Formular konfigurieren. Es wird empfohlen, nur die wiederverwendbaren Funktionen in der Bibliothek zu behalten, die von den Drittanbieter-Bibliotheken „jquery“ und „underscore.js“ abhängig sind.

### Registerkarte „Übermittlung“ {#submission-tab}

![Registerkarte „Übermittlung“](/help/adaptive-forms/assets/formcontainer_submissiontab.png)

Benutzende können verschiedene Aktionen für Übermittlungen adaptiver Formulare konfigurieren.

* **Umleitungs-URL/-pfad**: Diese Option ermöglicht es, eine Seite für jedes Formular zu konfigurieren, zu dem die Formularbenutzenden nach dem Übermitteln eines adaptiven Formulars umgeleitet werden. Klicken Sie hier, um weitere Informationen zum [Konfigurieren von Umleitungsseiten](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-redirect-page.html?lang=de) zu erhalten.

![Registerkarte „Nachricht anzeigen“](/help/adaptive-forms/assets/formconatiner_showmessage.png)

* **Nachricht anzeigen**: Mit dieser Option können Benutzende eine Nachricht hinzufügen, die angezeigt wird, wenn das adaptive Formular erfolgreich übermittelt wurde. Der vordefinierte Text ist im Dialogfeld enthalten und kann geändert werden. Das Dialogfeld „Nachricht anzeigen“ unterstützt Rich-Text-Formatierungswerkzeuge, mit denen der hinzugefügte Text formatiert werden kann.

* **Übermittlungsaktion**: Eine Übermittlungsaktion wird ausgelöst, wenn in einem adaptiven Formular auf die Schaltfläche „Senden“ geklickt wird. Benutzende können in der Dropdown-Liste „Übermittlungsaktionen“ auswählen, die standardmäßig unterstützt werden. Erfahren Sie, wie Sie [eine Übermittlungsaktion auf der Registerkarte „Übermittlung“ konfigurieren](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html?lang=de#supporting-custom-functions-in-validation-expressions-br).

## Verwandter Artikel {#related-article}

* [Erstellen eines adaptiven Formulars auf der AEM Sites-Seite oder im Experience Fragment](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html)

* [Erstellen eines eigenständigen adaptiven Formulars](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html?lang=de)
