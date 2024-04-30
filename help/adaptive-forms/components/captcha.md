---
title: Kernkomponente für adaptive Formulare – Formular-Container
description: Ein adaptives Formular zu einer Web-Seite hinzufügen.
role: Architect, Developer, Admin, User
hide: true
hidefromtoc: true
exl-id: 1e413ef3-7a6f-41fc-825d-dbe09ebaffe9
source-git-commit: e843ccf5c030cd4f1015e3290347b5799828537a
workflow-type: ht
source-wordcount: '869'
ht-degree: 100%

---

# Google reCAPTCHA {#google-recaptcha}

CAPTCHA („Completely Automated Public Turing test to tell Computers and Humans Apart“ – „vollautomatischer öffentlicher Turing-Test zur Unterscheidung von Computern und Menschen“) ist ein Programm, das bei Onlinetransaktionen eingesetzt wird, um zwischen Menschen und Bots oder automatisierten Programmen zu unterscheiden. Es stellt eine herausfordernde Aufgabe und bewertet die Benutzerantwort, um festzustellen, ob es sich um einen Menschen oder einen Bot handelt, der mit der Site interagiert. Dabei wird verhindert, dass der Benutzer fortfährt, wenn der Test fehlschlägt, wodurch Onlinetransaktionen sicherer werden, da Bots keinen Spam senden oder andere bösartige Zwecke verfolgen können.

AEM Forms as a Cloud Service unterstützt Google reCAPTCHA v2 in adaptiven Formularen. Sie können es verwenden, um eine CAPTCHA-Herausforderung bei der Formularübermittlung zu stellen

## Verwendung {#reasons-to-use-google-recaptcha}

- **Spam- und Bot-Prävention**: Einer der Hauptgründe für die Verwendung von reCAPTCHA ist, zu verhindern, dass Spam-Sendungen und bösartige Bots Ihr Formular überschwemmen. Die erweiterten Algorithmen von reCAPTCHA können automatisierte Versuche beim Senden des Formulars erkennen und so sicherstellen, dass nur legitime Benutzerinnen und Benutzer mit dem Formular interagieren können.

- **Verbesserte Sicherheit**: Durch die Implementierung von reCAPTCHA fügen Sie Ihrem adaptiven Formular eine zusätzliche Sicherheitsschicht hinzu. Dies hilft, sensible Informationen zu schützen und zu verhindern, dass böswillige Menschen Schwachstellen ausnutzen.

- **Anwendererlebnis**: CAPTCHAs können zwar manchmal als Unannehmlichkeiten betrachtet werden, aber der adaptive Ansatz von reCAPTCHA bedeutet, dass den meisten Benutzerinnen und Benutzern ein optimiertes, benutzerfreundliches Erlebnis präsentiert wird, das nur eine minimale Interaktion erfordert. Dies kann dazu beitragen, ein positives Anwendererlebnis zu erhalten und gleichzeitig Bots fernzuhalten.

- **Anpassungsfähigkeit**: Der adaptive Mechanismus von reCAPTCHA analysiert das Benutzerverhalten und Interaktionen, um festzustellen, ob es sich um Menschen handelt oder nicht. Das bedeutet, dass das Niveau der Herausforderung, die der Benutzerin bzw. dem Benutzer präsentiert wird, variieren kann, je nach der Wahrscheinlichkeit, mit der es sich um einen Bot handelt. Diese Anpassungsfähigkeit reduziert die Reibung für echte Benutzerinnen und Benutzer und gewährleistet gleichzeitig eine hohe Sicherheit.

- **Geringere manuelle Moderation**: Durch eine erhebliche Reduzierung der Anzahl von Spam-Einsendungen und von Bots generierten Inhalten kann reCAPTCHA Zeit und Ressourcen sparen, die sonst für manuelle Moderation und Bereinigung ausgegeben werden müssten.

## Version und Kompatibilität {#version-and-compatibility}

Die Kernkomponente „Google reCAPTCHA“ für adaptive Formulare wurde im August 2023 als Teil der „Version“ der Kernkomponenten veröffentlicht. Hier finden Sie eine Tabelle mit allen unterstützten Versionen, AEM-Kompatibilität und Links zur entsprechenden Dokumentation:


|  |  |
|---|---|
| Komponentenversion | AEM as a Cloud Service |
| --- | --- |
| v1 | Kompatibel mit<br>[Version 2.0.4](/help/versions.md) und höher | Kompatibel | Kompatibel |

Informationen zu Versionen und Freigaben der Kernkomponente finden Sie im Dokument [Kernkomponenten-Versionen](/help/versions.md).

## Technische Details {#technical-details}

Die neuesten Informationen zur Kernkomponente „Google reCAPTCHA“ für adaptive Formulare finden Sie in der technischen Dokumentation auf [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/recaptcha/v1/recaptcha). Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Entwicklerdokumentation für Kernkomponenten](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Sie können Ihr Google reCAPTCHA-Erlebnis für Besucherinnen und Besucher im Dialogfeld „Konfigurieren“ einfach anpassen. Sie können auch einfach Optionen für Google reCAPTCHA definieren, um ein nahtloses Anwendererlebnis zu gewährleisten.

### Registerkarte „Allgemein“ {#basic-tab}

- **Name**: Sie können eine Formularkomponente sowohl im Formular als auch im Regeleditor durch ihren eindeutigen Namen identifizieren. Der Name darf keine Leerzeichen oder Sonderzeichen enthalten.

- **Titel**: Sie können mit dem Titel leicht eine Komponente in einem Formular identifizieren. Standardmäßig wird der Titel über der Komponente angezeigt. Wenn Sie keinen Titel hinzufügen, wird der Name der Komponente anstelle des Titeltexts angezeigt.

- **Titel ausblenden**: Wählen Sie die Option aus, um den Titel der Komponente auszublenden.

- **Konfiguration** -

- **Typ** -

- **Komponente ausblenden**: Wählen Sie diese Option, um die Komponente aus dem Formular auszublenden. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor. Dies ist nützlich, wenn Sie Informationen speichern müssen, die Benutzende nicht sehen oder direkt ändern müssen.

- **Komponente deaktivieren**: Wählen Sie die Option zum Deaktivieren der Komponente aus. Die deaktivierte Komponente ist nicht aktiv und Endbenutzende können sie nicht bearbeiten. Die Daten der deaktivierten Komponente werden nicht übermittelt. Die Benutzerin bzw. der Benutzer kann den Wert des Felds sehen, kann ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor.

- **Schreibgeschützt**: Wählen Sie die Option aus, um die Komponente nicht bearbeitbar zu machen. Benutzende können den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor.

### Registerkarte „Validierung“ {#validation-tab}

- **Fehlermeldung**: Mit dieser Option können Sie eine Nachricht eingeben, die angezeigt wird, wenn das Kontrollkästchen **Erforderlich** aktiviert ist und das Formularfeld leer bleibt.

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

