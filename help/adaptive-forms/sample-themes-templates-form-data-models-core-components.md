---
title: Wie erhalten Sie Beispielthemen und -vorlagen für AEM Forms?
description: AEM Forms-Kernkomponenten bieten Beispiel-Designs, Vorlagen und Formulardatenmodelle für adaptive Formulare
solution: Experience Manager Forms
topic: Administration
role: Admin, User
hide: true
hidefromtoc: true
level: Intermediate
source-git-commit: ebbe3471164341076fe085bbef9c93fcb1fe382a
workflow-type: tm+mt
source-wordcount: '1259'
ht-degree: 10%

---


# Muster-Designs, Vorlagen und Formulardatenmodelle {#sample-themes-templates-and-data-models}

[!DNL AEM Forms] Kernkomponenten bieten gebrauchsfertige Beispielthemen, Vorlagen und Formulardatenmodelle, um schnell und einfach flexible adaptive Formulare zu erstellen. Diese helfen Formularautoren auch dabei, die Erweiterbarkeit, Anpassungsfähigkeit und Reaktionsfähigkeit von [AEM Forms-Kernkomponenten](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/adaptive-forms/introduction.html?lang=de) um einfache Formulare in kürzester Zeit und komplexe Formulare einfach zu erstellen, während eine nahtlose Verbindung mit der Datenbank hergestellt wird.

Die im Referenzinhaltspaket enthaltenen Musterdesigns, Vorlagen und Formulardatenmodelle sind:

| Vorlagen | Designs | Formulardatenmodelle |
---------|----------|---------
| [Allgemein](#Basic) | [Arbeitsfläche](#Canvas) | Microsoft® Dynamics 365 |
| [Leer](#Blank) | [WKND](#WKND) | Salesforce |
| [Kontakt](#Contact-Us) | [Easel](#Easel) |  |
| [Aktualisierung der Kontaktdetails](#Contact-Details-Update) |   |   |
| [Einverständnisformular](#Consent-Form) | |  |
| [Anfrage zum Protokolldienst](#Log-Service-Request) |  |  |
| [Feedback geben](#Give-Feedback) |  |  |
| [Vorteile der Registrierung](#Benefits-Enrollment) |  |   |
| [Zusammenfassung der Leistungen für Arbeitnehmer](#Employee-Benefits-Summary) |   |   |
| [Kontoauszug anfordern](#Request-for-Account-Statement) |   |   |
| [Sicherheitsüberprüfungsformular](#Safety-Inspection) |   |   |
| [Qualitätskontrolle](#Quality-Control-Inspection) |   |   |
| [Kaufanfrage](#Purchase-Request) |  |  |

## Beispieldesigns {#Sample-Themes}

Anhand von Beispieldesigns können Autoren die Formatierung für Formulare definieren und anpassen. Autoren mit Grundkenntnissen von CSS können Designs nach Bedarf anpassen.

**Wie bekomme ich diese Themen?**
* So erhalten Sie diese Themen **Forms as a Cloud Service** Umgebung, [Aktivieren der adaptiven Forms-Kernkomponenten](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/setup-configure-migrate/enable-adaptive-forms-core-components.html?lang=de) und verwenden Sie [Front-End-Pipeline](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/using-themes-in-core-components.html) um diese Designs bereitzustellen.
* So bringen Sie diese Themen zu einem **AEM 6.5 Forms** Umgebung, [Aktivieren der adaptiven Forms-Kernkomponenten](https://experienceleague.adobe.com/docs/experience-manager-65/forms/adaptive-forms-core-components/enable-adaptive-forms-core-components.html) und verwenden Sie [Package Manager](https://experienceleague.adobe.com/docs/experience-manager-65/forms/adaptive-forms-core-components/create-or-customize-themes-for-adaptive-forms-core-components) um diese Designs bereitzustellen.

Die **vorkonfiguriert** [Kernkomponenten des adaptiven Formulars](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/adaptive-forms/introduction.html?lang=de) Themen sind:

![OOTB-Themen](/help/adaptive-forms/assets/OOTB-themes.png)

### Canvas {#Canvas}

Das Arbeitsflächendesign ist das Standarddesign für Formulare und hebt die Verwendung von Grundfarben, Transparenz und flachen Symbolen hervor. Im Screenshot unten sehen Sie, wie das Canvas -Design aussieht.

![Arbeitsflächendesign](/help/adaptive-forms/assets/Safety-Inspection-Theme-Canvas.png)

### WKND {#WKND}

Das WKND-Design verkörpert ein lebendiges, fantasievolles und ansprechendes Design, um Ihren Formularen ein stilvolles Erscheinungsbild zu verleihen. Das Design basiert auf dem Erscheinungsbild und Stil von [WKND-Site](https://wknd.site/us/en.html) , auf der eine Reise- und Abenteuerwebsite aufbaut [Adobe Experience Manager-Kernkomponenten](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/adaptive-forms/introduction.html?lang=de).

![WKND-Design](/help/adaptive-forms/assets/Safety-Inspection-Form-Theme.png)


### Easel {#Easel}

Einfaches Design hilft dabei, ein ansprechendes und einfach einzurichtendes Formular zu erstellen. Es ist auf Einfachheit und Benutzerfreundlichkeit abgestimmt. Das Easel-Design basiert auf dem Konzept, wo ein tragbarer Stand von Künstlern verwendet, um eine Leinwand während der Arbeit an ihren Gemälden zu unterstützen.

![Easel-Design](/help/adaptive-forms/assets/Safety-Inspection-Theme-Easel.png)

## Beispielvorlagen {#Sample-templates}

Vorlagen definieren die anfängliche Formularstruktur, den Inhalt und die Aktionen, die in Ihrem Formular repliziert werden sollen, oder verwenden eine ähnliche Vorlagenstruktur wie das Formular, z. B. Einverständnisformular, Registrierungsformular für Vorteile und vieles mehr.

**Wie erhalten Sie diese Vorlagen?**
Sie können die Vorlagen abrufen, indem Sie eine [AEM auf Archetyp 43 oder höher basierendes Projekt](https://github.com/adobe/aem-project-archetype) auf **AEM Forms as a Cloud Service** oder **AEM 6.5** Forms-Umgebung.

Die **vorkonfiguriert** [Kernkomponenten des adaptiven Formulars](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/adaptive-forms/introduction.html?lang=de) Vorlagen sind:

![Referenzvorlagen](/help/adaptive-forms/assets/reference-templates-core-components.png)

### Einfach {#Basic}

Eine einfache Vorlage hilft Ihnen beim schnellen Erstellen eines Registrierungserlebnisformulars. Sie können sie auch verwenden, um eine Vorschau der Funktionen von [Adaptive Forms-Kernkomponenten](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/adaptive-forms/introduction.html?lang=de). Es bietet ein Assistenten-Layout für eine abschnittsweise Darstellung der Daten.

![Grundlegende Vorlage](/help/adaptive-forms/assets/Basic-template-desktop-view.png)

### Leer {#Blank}

Eine leere Arbeitsflächenvorlage wird verwendet, um eine Struktur, einen Inhalt und Regeln für adaptive Formulare von Grund auf neu zu erstellen. In die leere Vorlage sind keine Formularkomponenten eingefügt.

![Leere Vorlage](/help/adaptive-forms/assets/Blank-temp-desktop-view.png)

### Kontakt {#Contact-Us}

Die Formularvorlage Kontaktformular wird verwendet, um ein Formular zu erstellen, das die Kommunikation zwischen Website-Besuchern und Formular-Administratoren erleichtert. Benutzer können über das Formular Abfragen, Feedback oder Supportanfragen senden.

![Kontaktvorlage](/help/adaptive-forms/assets/Contact-us-desktop-view.png)

### Aktualisierung der Kontaktdetails {#Contact-Details-Update}

Die Vorlage für die Aktualisierung von Kontaktdetails hilft Autoren bei der Erstellung eines Formulars für die Aktualisierung von Adresse und Kontaktdaten von Kunden. Das Formular unterstützt Kunden auch bei der Aktualisierung personenbezogener Daten in Bezug auf Abonnements oder Vorteile, um eine nahtlose Kommunikation und einen unterbrechungsfreien Zugriff auf die Dienste oder Vorteile zu gewährleisten.

![Contact-details-update](/help/adaptive-forms/assets/Contact-details-update.png)

### Einverständnisformular {#Consent-Form}

Die Vorlage für das Einverständnisformular wird verwendet, um ein Formular für die Beschaffung eines Rechtsdokuments von Teilnehmern zu erstellen, die an einer bestimmten Aktivität, einem Forschungsstudium, einem medizinischen Verfahren oder einer Situation teilnehmen, in der ihre personenbezogenen Daten oder Rechte involviert sein können. Das Formular gewährleistet Transparenz, schützt die Rechte des Teilnehmers und schafft ein klares Verständnis dessen, was der Einzelne zustimmt.

![Einverständnisformular](/help/adaptive-forms/assets/Consent-form-desktop-view.png)

### Protokolldienstanfrage {#Log-Service-Request}

Die Protokolldienst-Anforderungsvorlage hilft beim Erstellen eines Formulars, das protokollspezifische Protokollierungsdienste von einem Dienstleister anfordert. Das Formular dient als formelle Anfrage zum Erstellen eines Tickets für Ereignisse, Aktivitäten oder Daten, die zur Überwachung oder zum Tracking-Status protokolliert werden.

![Anforderungsvorlage für Protokolldienst](/help/adaptive-forms/assets/Log-service-request-desktop-view.png)


### Feedback geben {#Give-Feedback}

Mit der Rückmeldevorlage können Sie ein Formular erstellen, das eine konstruktive Rückmeldung an eine andere Person oder ein Team liefert. Das Formular hilft sicherzustellen, dass das Feedback klar, spezifisch und umsetzbar ist, und fördert offene Kommunikation und Verbesserung.

![Feedback-Vorlage geben](/help/adaptive-forms/assets/Give-feedback-desktop-view.png)


### Leistungseinstufung {#Benefits-Enrollment}

Mit der Vorlage für das Anmeldeformular für Vorteile können Sie ein Formular erstellen, in dem Sie wichtige Informationen von Ihren Mitarbeitern zu ihren bevorzugten Vorteilen und Deckungsoptionen erfassen. Sie begleitet in der Regel den jährlichen Zeitraum der Leistungseinstufung.

![Vorteilen der Registrierungsvorlage](/help/adaptive-forms/assets/Benefits-enrollment-form-template.png)


### Zusammenfassung der Arbeitnehmervorteile {#Employee-Benefits-Summary}

Die Vorlage für die Zusammenfassung der Leistungen für Arbeitnehmer wird verwendet, um ein Formular zu erstellen, in dem wichtige Details zu den Vorteilen einer Person erfasst werden. Es hilft bei der schnellen und präzisen Bewertung der Abdeckung, indem ein umfassender Überblick über effiziente Hilfe und Unterstützung bereitgestellt wird.
![Zusammenfassung der Arbeitnehmervorteile](/help/adaptive-forms/assets/Employee-benefits-summary.png)


### Kontoauszug anfordern {#Request-for-Account-Statement}

Die Vorlage für Kontoauszugsanfragen hilft bei der Erstellung eines Formulars, das den Prozess des Abrufs einer präzisen und aktuellen Kundenanweisung auslöst. Die Erklärung enthält eine detaillierte Aufzeichnung von Finanztransaktionen, -aktivitäten oder anderen relevanten Informationen über Kunden, die dieses Formular verwenden.

![Request-for-account-statement](/help/adaptive-forms/assets/Request-for-account-statment.png)

### Sicherheitskontrolle {#Safety-Inspection}

Die Vorlage für Sicherheitsüberprüfungsformulare hilft bei der Erstellung eines Formulars zur Eingabe von Details für eine sichere Arbeitsumgebung. Durch regelmäßige Inspektionen mit diesem Formular können potenzielle Risiken ermittelt werden. Der Vordruck umfasst verschiedene Aspekte wie Notausstiege, Brandsicherheit, elektrische Sicherheit, Gefahrstoffe, persönliche Schutzausrüstung, Ergonomie der Workstation für die Sicherheit und das Wohlbefinden von Mitarbeitern, Besuchern und Kunden.

![Sicherheitskontrollformular](/help/adaptive-forms/assets/Safety-inspection-form.png)

### Qualitätskontrolle {#Quality-Control-Inspection}

Anhand der Vorlage für die Qualitätskontrolle wird ein Formular erstellt, in dem das Erscheinungsbild, die Abmessungen, die Funktionalität, die Dokumentation, die Testergebnisse und die Gesamtqualität eines Produkts oder Artikels bewertet und dokumentiert werden. Sie hilft bei der Identifizierung von Mängeln, Nichtkonformitäten und Korrekturmaßnahmen, die zur Gewährleistung der Einhaltung von Qualitätsstandards erforderlich sind.

![Qualitätskontrolle](/help/adaptive-forms/assets/Quality-Control-Inspection.png)


### Kaufanfrage {#Purchase-Request}

Mit der Vorlage für Bestellformulare können Sie ein Formular erstellen, um den Vergabeverfahren einzuleiten und es Mitarbeitern zu ermöglichen, den Kauf von für ihre Arbeit erforderlichen Waren oder Dienstleistungen förmlich anzufordern. Das Formular erfasst wichtige Details wie Artikelbeschreibung, Menge, bevorzugter Lieferant (falls zutreffend), Budgetzuweisung, Begründung des Kaufs, Lieferinformationen und erforderliche Genehmigungen.

![purchase-request-form](/help/adaptive-forms/assets/Purchase-request-form.png)

## Referenzformular-Datenmodelle {#reference-models}

Nachdem Sie ein auf [Kernkomponente](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/adaptive-forms/introduction.html?lang=de), können Sie Ihr Formular mit den Datenbankservern Microsoft® Dynamics 365 und Salesforce verbinden, um Geschäftsabläufe zu ermöglichen. Beispiel:

* Schreiben Sie Daten in Microsoft® Dynamics 365 und Salesforce bei der Übermittlung des adaptiven Formulars.
* Schreiben Sie Daten in Microsoft® Dynamics 365 und Salesforce über benutzerdefinierte Entitäten, die im Formulardatenmodell definiert sind, und umgekehrt.
* Abfragen von Microsoft® Dynamics 365- und Salesforce-Server auf Daten und Vorausfüllen von Adaptive Forms.
* Lesen Sie Daten von Microsoft® Dynamics 365- und Salesforce-Servern.

Sie können die folgenden Formulardatenmodelle erhalten, indem Sie das [Referenzinhaltspaket](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-forms-reference-content.ui.content-2.1.0.zip) installieren:

* Microsoft® Dynamics 365
* Salesforce

Informationen zur Verwendung dieser Modelle finden Sie unter [Konfigurieren von Microsoft® Dynamics 365- und Salesforce-Cloud-Services](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/integrate/use-form-data-model/configure-msdynamics-salesforce.html#configure-dynamics-cloud-service)
