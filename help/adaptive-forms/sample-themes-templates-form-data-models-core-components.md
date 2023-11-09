---
title: Wie erhalten Sie Beispieldesigns und -vorlagen für AEM Forms-Kernkomponenten?
description: AEM Forms-Kernkomponenten bieten Beispiel-Designs, Vorlagen und Formulardatenmodelle für adaptive Formulare.
solution: Experience Manager Forms
topic: Administration
role: Admin, User
level: Intermediate
exl-id: aef6e88b-dcae-4777-9893-9257d7702f43
source-git-commit: 1dd55fdd836dff89763887d88af2671ed1f9ce2b
workflow-type: tm+mt
source-wordcount: '1304'
ht-degree: 69%

---

# Beispiel-Designs, -vorlagen und -formulardatenmodelle {#sample-themes-templates-and-data-models}

Kernkomponenten von [!DNL AEM Forms] bieten gebrauchsfertige Beispiel-Designs, -vorlagen und -formulardatenmodelle, um schnell und einfach vielseitig anwendbare adaptive Formulare zu erstellen. Diese helfen Formularautoren auch dabei, die Erweiterbarkeit, Anpassungsfähigkeit und Reaktionsfähigkeit von [Adaptive Forms-Kernkomponenten](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/adaptive-forms/introduction.html?lang=de) um einfache Formulare in kürzester Zeit und komplexe Formulare einfach zu erstellen, während eine nahtlose Verbindung mit der Datenbank hergestellt wird.

Folgende Beispiel-Designs, -vorlagen und -formulardatenmodelle sind im Paket mit den Referenzinhalten enthalten:

| Vorlagen | Designs | Formulardatenmodelle |
---------|----------|---------
| [Leer](#Blank) | [Arbeitsfläche](#Canvas) | Microsoft® Dynamics 365 |
| [Kontakt](#Contact-Us) | [WKND](#WKND) | Salesforce |
| [Aktualisierung der Kontaktdetails](#Contact-Details-Update) | [Easel](#Easel) |   |
| [Einverständnisformular](#Consent-Form) | [FSI](#FSI) |  |
| [Protokolldienstanfrage](#Log-Service-Request) | [Gesundheitswesen](#Healthcare) |  |
| [Feedback geben](#Give-Feedback) |  |  |
| [Registrierung für Nebenleistungen](#Benefits-Enrollment) |  |   |
| [Nebenleistungen für Mitarbeitende – Übersicht](#Employee-Benefits-Summary) |   |   |
| [Anforderung eines Kontoauszugs](#Request-for-Account-Statement) |   |   |
| [Sicherheitsinspektionsformular](#Safety-Inspection) |   |   |
| [Qualitätskontrollinspektion](#Quality-Control-Inspection) |   |   |
| [Kaufanfrage](#Purchase-Request) |  |  |

## Beispiel-Designs {#Sample-Themes}

Anhand von Referenzbeispieldesigns können Autoren die Formatierung für Formulare verwenden, definieren und anpassen. Autoren mit Grundkenntnissen von CSS können das Design gemäß Anforderungen anpassen.

**Wie bekomme ich diese Designs?**
Sie erhalten diese Designs anhand der folgenden Schritte, die unten für **AEM as a Cloud Service** Umgebung:

1. [Aktivieren der Kernkomponenten für adaptive Formulare](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/setup-configure-migrate/enable-adaptive-forms-core-components.html?lang=de)
1. [Bereitstellung eines AEM Archetyp 45-Projekts in Ihrer Umgebung](https://github.com/adobe/aem-project-archetype)


Wenn Sie einen AEM-Archetyp bereitstellen, können Sie nur die OOTB-Designs in Ihren Formularen verwenden, um die Designs gemäß Ihren Anforderungen anzupassen. [Verwenden der Front-End-Pipeline](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/using-themes-in-core-components.html?lang=de) , um die Designs bereitzustellen.

>[!NOTE]
>
> * Die Themen stehen nicht zur Verfügung für **AEM 6.5** Umgebung.

<!--

1. **AEM 6.5**

    1. [Enable Adaptive Form Core Components](https://experienceleague.adobe.com/docs/experience-manager-65/forms/adaptive-forms-core-components/enable-adaptive-forms-core-components.html)
    1. [Deploy an AEM Archetype 45 project to your environment](https://github.com/adobe/aem-project-archetype)


    When you deploy an AEM Archetype, you can only use the OOTB themes in your forms, To customize the themes as per your requirements, [Use the front-end pipeline](https://experienceleague.adobe.com/docs/experience-manager-65/forms/adaptive-forms-core-components/create-or-customize-themes-for-adaptive-forms-core-components.html) to deploy the themes.

-->


<!--

### Deploying an AEM Archetype 45 project to your environment {#using-archetype-to-deploy-themes}

You can get these themes by deploying an [AEM Archetype 45](https://github.com/adobe/aem-project-archetype) to your **AEM Forms as a Cloud Service** or **AEM 6.5** Forms environment.

### Enable core components and use front-end pipeline to deploy themes {#use-front-end-pipeline-to-deploy-themes}

1. To get these themes on **Forms as a Cloud Service** environment, [enable Adaptive Forms Core Components](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/setup-configure-migrate/enable-adaptive-forms-core-components.html) and use the [front-end pipeline](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/using-themes-in-core-components.html) to deploy these themes.
    
1. To get these themes on **AEM 6.5 Forms** environment, [enable Adaptive Forms Core Components](https://experienceleague.adobe.com/docs/experience-manager-65/forms/adaptive-forms-core-components/enable-adaptive-forms-core-components.html) and use the [Package Manager](https://experienceleague.adobe.com/docs/experience-manager-65/forms/adaptive-forms-core-components/create-or-customize-themes-for-adaptive-forms-core-components.html) to deploy these themes.

[Learn to use and customize themes in AEM Forms as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/using-themes-in-core-components.html). 

[Learn to use and customize themes in AEM 6.5](https://experienceleague.adobe.com/docs/experience-manager-65/forms/adaptive-forms-core-components/create-or-customize-themes-for-adaptive-forms-core-components.html).

-->

Die **vorkonfigurierten** Designs für [Kernkomponenten für adaptive Formulare](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/adaptive-forms/introduction.html?lang=de) sind:

![OOTB-Designs](/help/adaptive-forms/assets/archetype-45-themes-1.png)

### Canvas {#Canvas}

Das Arbeitsflächendesign ist das Standarddesign für Formulare und betont die Verwendung von Grundfarben, Transparenz und flachen Symbolen. Im Screenshot unten sehen Sie, wie das Design „Canvas“ aussieht.

![Design „Canvas“](/help/adaptive-forms/assets/Safety-Inspection-Theme-Canvas.png)

### WKND {#WKND}

Das Design „WKND“ verkörpert ein lebendiges, fantasievolles und ansprechendes Design, um Ihren Formularen ein stilvolles Erscheinungsbild zu verleihen. Das Design basiert auf dem Erscheinungsbild und Stil der [WKND-Site](https://wknd.site/us/en.html), einer Reise- und Abenteuer-Website, die auf [Kernkomponenten von Adobe Experience Manager](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/adaptive-forms/introduction.html?lang=de) aufbaut.

![Design „WKND“](/help/adaptive-forms/assets/Safety-Inspection-Form-Theme.png)


### Easel {#Easel}

Das Design „Easel“ hilft, ein ansprechendes und einfach einzurichtendes Formular zu erstellen. Es ist auf Einfachheit und Benutzerfreundlichkeit ausgelegt. Das Design basiert auf dem Konzept, dass ein tragbarer Stand von Künstlern verwendet wird, um eine Leinwand zu unterstützen, während sie an ihren Gemälden arbeiten.

![Design „Easel“](/help/adaptive-forms/assets/Safety-Inspection-Theme-Easel.png)

### FSI (Financial Services &amp; Insurance) {#FSI}

Das FSI-Thema legt großen Wert darauf, Ihr Formular sauber und praxisorientiert zu gestalten. Der leichte blaue Farbton wird auf das Formular angewendet, wenn Sie das FSI-Design anwenden, wie Sie im Bild sehen können.

![FSI-Design](/help/adaptive-forms/assets/fsi-theme-new1.png)


### Gesundheitswesen {#Healthcare}

Das Design Gesundheitsfürsorge verwendet umfassende, grüne Töne, um Elemente wie Registerkarten, Bedienfelder, Textfelder und Schaltflächen in Ihrem Formular zu akzentuieren.

![Gesundheitsthemen](/help/adaptive-forms/assets/healthcare-new-theme.png)


## Beispielvorlagen {#Sample-templates}

Vorlagen definieren die anfängliche Formularstruktur, den Inhalt und die Aktionen, die in Ihrem Formular repliziert werden sollen, oder verwenden eine ähnliche Vorlagenstruktur wie das gewünschte Formular, z. B. Einverständnisformular, Registrierungsformular für Nebenleistungen und vieles mehr.

**Wie bekommt man diese Vorlagen?**
Sie können diese Vorlagen abrufen, indem Sie eine [AEM Archetyp 45](https://github.com/adobe/aem-project-archetype) auf **AEM Forms as a Cloud Service** Umgebung oder **AEM 6.5 Forms** Umgebung.

<!--

>[!NOTE]
>
> * If you have [enabled core components and used front-end pipeline to deploy themes](#use-front-end-pipeline-to-deploy-themes), you need not to deploy an AEM Archetype.
> * You can find list of all OOTB templates when you create a form.

-->


Die **vorkonfigurierten** Vorlagen für [Kernkomponenten für adaptive Formulare](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/adaptive-forms/introduction.html?lang=de) sind:

![Referenzvorlagen](/help/adaptive-forms/assets/reference-templates-core-components.png)

<!--

### Basic {#Basic}

A basic template helps you quickly create an enrollment experience form. You can also use it to preview the functionality of [Adaptive Forms Core Components](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/adaptive-forms/introduction.html). It provides a wizard layout for section-by-section presentation of data.

![Basic Template](/help/adaptive-forms/assets/Basic-template-desktop-view.png)

-->

### Leer {#Blank}

Eine Vorlage mit einer leeren Arbeitsfläche wird verwendet, um von Grund auf eine Struktur, Inhalt und Regeln für ein Formular zu erstellen. In die leere Vorlage sind keine Formularkomponenten voreingefügt.

![Leere Vorlage](/help/adaptive-forms/assets/Blank-temp-desktop-view.png)

### Kontakt {#Contact-Us}

Die Formularvorlage „Kontakt“ wird verwendet, um ein Formular zu erstellen, das die Kommunikation zwischen Website-Besucherinnen und -Besuchern und Formular-Admins erleichtert. Benutzende können über das Formular Abfragen, Feedback oder Support-Anfragen senden.

![Vorlage „Kontakt“](/help/adaptive-forms/assets/Contact-us-desktop-view.png)

### Aktualisierung der Kontaktdetails {#Contact-Details-Update}

Die Vorlage für die Aktualisierung der Kontaktdetails hilft Autorinnen und Autoren bei der Erstellung eines Formulars für die Aktualisierung von Adressen und Kontaktdaten von Kundinnen und Kunden. Das Formular unterstützt Kundinnen und Kunden auch bei der Aktualisierung personenbezogener Daten in Bezug auf Abonnements oder Nebenleistungen, um eine nahtlose Kommunikation und einen unterbrechungsfreien Zugriff auf die Dienste oder Nebenleistungen zu gewährleisten.

![Contact-details-update](/help/adaptive-forms/assets/Contact-details-update.png)

### Einverständnisformular {#Consent-Form}

Die Vorlage für das Einverständnisformular wird verwendet, um ein Formular für die Beschaffung eines Rechtsdokuments von Teilnehmern zu erstellen, die an einer bestimmten Aktivität, einem Forschungsstudium, einem medizinischen Verfahren oder einer Situation teilnehmen, in der ihre personenbezogenen Daten oder Rechte involviert sein können. Das Formular gewährleistet Transparenz, schützt die Rechte der Teilnehmenden und schafft Klarheit darüber, womit sich eine Person einverstanden erklärt.

![Einverständnisformular](/help/adaptive-forms/assets/Consent-form-desktop-view.png)

### Protokolldienstanfrage {#Log-Service-Request}

Die Vorlage für eine Protokolldienstanfrage hilft bei der Erstellung eines Formulars, das protokollspezfische Protokollierungsdienste von einem Dienstleister anfordert. Das Formular dient als formelle Anfrage zum Erstellen eines Tickets für Ereignisse, Aktivitäten oder Datenprotokolle zur Überwachung oder zum Tracking des Status.

![Vorlage „Protokolldienstanfrage“](/help/adaptive-forms/assets/Log-service-request-desktop-view.png)


### Feedback geben {#Give-Feedback}

Mit der Vorlage „Feedback geben“ können Sie ein Formular erstellen, das eine konstruktive Rückmeldung an eine andere Person oder ein Team liefert. Das Formular trägt dazu bei sicherzustellen, dass das Feedback klar, spezifisch und umsetzbar ist, und fördert offene Kommunikation und Verbesserung.

![Vorlage „Feedback geben“](/help/adaptive-forms/assets/Give-feedback-desktop-view.png)


### Registrierung für Nebenleistungen {#Benefits-Enrollment}

Mit der Vorlage „Registrierung für Nebenleistungen“ können Sie ein Formular erstellen, in dem Sie wichtige Informationen von Ihren Mitarbeiterinnen und Mitarbeitern zu ihren bevorzugten Nebenleistungen und Absicherungsoptionen erfassen. Diese Vorlage wird in der Regel im jährlichen Anmeldezeitraum für Nebenleistungen verwendet.

![Vorlage „Registrierung für Nebenleistungen“](/help/adaptive-forms/assets/Benefits-enrollment-form-template.png)


### Nebenleistungen für Mitarbeitende – Übersicht {#Employee-Benefits-Summary}

Die Vorlage „Nebenleistungen für Mitarbeitende – Übersicht“ wird verwendet, um ein Formular zu erstellen, in dem wichtige Details zu den Nebenleistungen einer Einzelperson erfasst werden. Sie hilft bei der schnellen und präzisen Bewertung der Absicherung, indem ein umfassender Überblick gegeben wird, um effiziente Hilfe und Unterstützung leisten zu können.
![Nebenleistungen für Mitarbeitende – Übersicht](/help/adaptive-forms/assets/Employee-benefits-summary.png)


### Anforderung eines Kontoauszugs {#Request-for-Account-Statement}

Eine Anfrage für die Kontoauszugsvorlage hilft bei der Erstellung eines Formulars, das den Prozess des Abrufs einer genauen und aktuellen Kundenanweisung auslöst. Der Kontoauszug bietet eine detaillierte Aufzeichnung von Finanztransaktionen, Aktivitäten oder anderen relevanten Informationen über Kundinnen und Kunden, die dieses Formular verwenden.

![Request-for-account-statment](/help/adaptive-forms/assets/Request-for-account-statment.png)

### Sicherheitsinspektion {#Safety-Inspection}

Die Vorlage „Sicherheitsinspektionsformular“ hilft bei der Erstellung eines Formulars zur Eingabe von Details für eine sichere Arbeitsumgebung. Durch regelmäßige Inspektionen mithilfe dieses Formulars können potenzielle Risiken ermittelt werden. Das Formular umfasst verschiedene Aspekte wie Notausgänge, Brandsicherheit, elektrische Sicherheit, Gefahrstoffe, persönliche Schutzausrüstung und Arbeitsplatzergonomie für die Sicherheit und das Wohlbefinden von Mitarbeitenden, Besucherinnen und Besuchern sowie Kundinnen und Kunden.

![Sicherheitsinspektionsformular](/help/adaptive-forms/assets/Safety-inspection-form.png)

### Qualitätskontrollinspektion {#Quality-Control-Inspection}

Die Vorlage „Qualitätskontrollinspektion“ wird verwendet, um ein Formular zu erstellen, in dem das Erscheinungsbild, die Abmessungen, die Funktionalität, die Dokumentation, die Testergebnisse und die Gesamtqualität eines Produkts oder Artikels bewertet und dokumentiert werden. Sie hilft bei der Identifizierung von Mängeln und Nichtkonformitäten sowie Korrekturmaßnahmen, die zur Gewährleistung der Einhaltung von Qualitätsstandards erforderlich sind.

![Qualitätskontrollinspektion](/help/adaptive-forms/assets/Quality-Control-Inspection.png)


### Kaufanfrage {#Purchase-Request}

Mit der Vorlage „Kaufanfrage“ können Sie ein Formular erstellen, um den Beschaffungsprozess einzuleiten und es Mitarbeitenden zu ermöglichen, den Kauf von Waren oder Dienstleistungen anzufordern, die für ihre Arbeit erforderlich sind. Das Formular erfasst wichtige Details wie Artikelbeschreibung, Menge, bevorzugter Lieferant (falls anwendbar), Budgetzuweisung, Kaufbegründung, Lieferinformationen und erforderliche Genehmigungen.

![purchase-request-form](/help/adaptive-forms/assets/Purchase-request-form.png)

## Referenz-Formulardatenmodelle {#reference-models}

Nachdem Sie ein adaptives Formular basierend auf einer [Kernkomponente](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/adaptive-forms/introduction.html?lang=de) erstellt haben, können Sie Ihr Formular mit den Datenbank-Servern von Microsoft® Dynamics 365 und Salesforce verbinden, um Geschäftsabläufe zu ermöglichen. Zum Beispiel:

* Schreiben von Daten in Microsoft® Dynamics 365 und Salesforce bei der Übermittlung von adaptiven Formularen.
* Schreiben von Daten in Microsoft® Dynamics 365 und Salesforce durch benutzerdefinierte Entitäten, die im Formulardatenmodell definiert sind, und umgekehrt.
* Abfragen der Microsoft® Dynamics 365- und Salesforce-Server nach Daten und Vorausfüllen von adaptiven Formularen.
* Lesen von Daten von Microsoft® Dynamics 365- und Salesforce-Servern.

Sie können die folgenden Formulardatenmodelle erhalten, indem Sie das [Referenzinhaltspaket](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-forms-reference-content.ui.content-2.1.0.zip) installieren:

* Microsoft® Dynamics 365
* Salesforce

Informationen zur Verwendung dieser Modelle finden Sie unter [Konfigurieren von Microsoft Dynamics 365- und Salesforce-Cloud-Diensten](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/integrate/use-form-data-model/configure-msdynamics-salesforce.html?lang=de#configure-dynamics-cloud-service)
