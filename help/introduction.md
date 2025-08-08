---
title: Einführung in Kernkomponenten
description: Erhalten Sie Lösungen für Probleme mit den Kernkomponenten und ermöglichen Sie anderen, Elemente in AEM zu erstellen.
role: Architect, Developer, Admin, User
exl-id: d294db22-4cb0-48a4-9366-03fda5b8bb8e
source-git-commit: f35fba4bee041b8d64dea69437c5d441950df7c6
workflow-type: tm+mt
source-wordcount: '836'
ht-degree: 100%

---


# Einführung in Kernkomponenten{#core-components-introduction}

{{traditional-aem}}

In Adobe Experience Manager sind Komponenten die strukturellen Elemente, aus denen der Inhalt von bearbeiteten Seiten besteht. Komponenten waren immer ein Grundelement des AEM-Erlebnisses, wodurch die Seitenerstellung einfach, aber für den Autor und die Entwicklung von Komponenten flexibel und erweiterbar ist.

Die Kernkomponenten sind eine Reihe standardisierter Web Content Management (WCM) für AEM, um die Entwicklungszeit zu verkürzen und die Wartungskosten Ihrer Websites zu senken.

## Ressourcen {#resources}

* **[Komponentenbibliothek:](https://www.adobe.com/go/aem_cmp_library_de)** Eine Sammlung von Beispielen zum Anzeigen der Komponenten in ihren verschiedenen Konfigurationen.
* **Komponentendokumentation (dieses Dokument):** Für Entwickler und Autoren mit Details zu den einzelnen Komponenten.
* **[GitHub-Repository für Kernkomponenten:](https://github.com/adobe/aem-core-wcm-components)** Für Entwicklerdetails zu den einzelnen Komponenten und Projekt-Download.
* Erste Schritte:
   * **[Erfolg mit den Kernkomponenten:](/help/developing/success.md)** Richtlinien, die rechtzeitig vor Beginn eines Projekts zu berücksichtigen sind, bei dem die Kernkomponenten verwendet werden.
   * **[WKND-Tutorial:](https://experienceleague.adobe.com/docs/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html?lang=de)** Ein zweitägiges Tutorial zum Erstellen einer neuen Website.
   * **[Summit-Tutorial:](https://expleague.azureedge.net/labs/L767/index.html)** Ein zweistündiges Tutorial zum Erstellen einer neuen Website (von einem Lab beim US Summit 2019).
   * **[Gems-Webinar:](https://helpx.adobe.com/de/experience-manager/kt/eseminars/gems/AEM-Core-Components.html)** Eine Führung durch die Kernkomponenten (aufgenommen am Dezember 2018).

## Funktionen {#features}

|  |  |
|---|---|
| Produktionsbereit | Die Kernkomponenten sind 30 robuste WCM-Komponenten, die gut getestet und weit verbreitet sind und eine gute Leistung erbringen. |
| Cloud-fähig | Ob in [AEM as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/landing/home.html?lang=de), in [Adobe Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams) oder On-Premise - sie funktionieren einfach. |
| Vielseitig | Die Komponenten stellen allgemeine Konzepte dar, mit denen die Autoren nahezu jedes Layout zusammenstellen können. |
| Konfigurierbar | [Inhaltsrichtlinien](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/full-stack/components-templates/templates.html?lang=de#content-policies) auf Vorlagenebene definieren, welche Funktionen die Seitenautoren verwenden dürfen oder nicht. |
| [Responsiv](responsive.md) | Alle Kernkomponenten sind so konzipiert, dass sie vollständig responsiv sind und ein nahtloses Erlebnis auf allen Geräten gewährleisten. |
| Verfolgbar | Die [Adobe Client-Datenschicht-Integration](/help/developing/data-layer/overview.md) ermöglicht die Verfolgung aller Aspekte des Besuchererlebnisses. |
| Barrierefrei | Sie erfüllen [WCAG 2.1-Standards](https://www.w3.org/TR/WCAG21/), bieten ARIA-Bezeichnungen und unterstützen die Tastennavigation ([bekannte Probleme](https://github.com/adobe/aem-core-wcm-components/issues?utf8=✓&q=is%3Aissue+is%3Aopen+accessibility+in%3Atitle)). |
| SEO-freundlich | Die HTML-Ausgabe ist schematisch und stellt [schema.org](https://schema.org)-Mikrodatenanmerkungen bereit. |
| WebApp-fähig | Die [optimierte JSON-Ausgabe](https://experienceleague.adobe.com/docs/experience-manager-learn/foundation/development/develop-sling-model-exporter.html?lang=de) ermöglicht das Client-seitige Rendern, wobei die [kontextbezogene Bearbeitung](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html?lang=de) weiterhin möglich ist. |
| AMP-Unterstützung | Die Komponenten verfügen über integrierte [Unterstützung für den AMP-Standard](/help/developing/amp.md), wodurch mobile Erlebnisse beschleunigt werden. |
| Design-Kit | Mit einem [Benutzeroberflächen-Kit für Adobe XD](https://experienceleague.adobe.com/docs/experience-manager-learn/assets/AEM-CoreComponents-UI-Kit.xd?lang=de) können Designer Wireframes erstellen, die sie dann [nach Bedarf formatieren](https://github.com/adobe/aem-guides-wknd/releases/download/aem-guides-wknd-0.0.2/AEM_UI-kit-WKND.xd) können. |
| Themen-fähig | Die Komponenten implementieren das [Stilsystem](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/features/style-system.html?lang=de) und das Markup folgt den [BEM-CSS-Konventionen](https://getbem.com/). |
| Anpassbar | Verschiedene Muster ermöglichen eine [einfache Anpassung](developing/customizing.md), von der Anpassung des HTML-Codes bis hin zur Wiederverwendung erweiterter Funktionen. |
| Versionierung | Die [Versionierungsrichtlinie](https://github.com/adobe/aem-core-wcm-components/wiki/Versioning-policies) stellt sicher, dass die Kernkomponenten Ihre Website nicht beschädigen, wenn Funktionen verbessert werden, die sich auf Sie auswirken könnten. |
| Lokalisierbar | Mit der intelligenten Referenzauflösung ist es bestimmten Komponenten möglich, [entsprechende lokalisierte Inhalte automatisch zu finden und anzuzeigen](get-started/localization.md). |
| Open Source | Wenn etwas nicht so ist, wie es sein sollte, [bringen Sie Ihre Verbesserungen ein!](https://github.com/adobe/aem-core-wcm-components/blob/master/CONTRIBUTING.md) |


## Die WCM-Komponenten {#the-wcm-components}

Die aktuelle Version der Kernkomponenten enthält die folgenden Komponenten:

### Vorlagenkomponenten {#template-components}

* [Seite](components/page.md)
* [Navigation](components/navigation.md)
* [Sprachnavigation](components/language-navigation.md)
* [Breadcrumb](components/breadcrumb.md)
* [Schnellsuche](components/quick-search.md)
* [Inhalt](components/tableofcontents.md)

### Komponenten zum Erstellen von Seiten {#page-authoring-components}

* [Titel](components/title.md)
* [Text](components/text.md)
* [Bild](components/image.md)
* [Schaltfläche](components/button.md)
* [Teaser](components/teaser.md)
* [Download](components/download.md)
* [Liste](components/list.md)
* [Experience Fragment](components/experience-fragment.md)
* [Inhaltsfragment](components/content-fragment-component.md)
* [Inhaltsfragmentliste](components/content-fragment-list.md)
* [Einbetten](components/embed.md)
* [Social Media Sharing](components/sharing.md) (veraltet)
* [Trennzeichen](components/separator.md)
* [Fortschrittsleiste](components/progress-bar.md)
* [PDF-Viewer](components/pdf-viewer.md)

### Container-Komponenten {#container-components}

* [Container](components/container.md)
* [Karussell](components/carousel.md)
* [Registerkarten](components/tabs.md)
* [Akkordeon](components/accordion.md)

### Formularkomponenten {#form-components}

* [Formular-Container](components/forms/form-container.md)
* [Formulartext](components/forms/form-text.md)
* [Formularoptionen](components/forms/form-options.md)
* [Ausgeblendetes Formular](components/forms/form-hidden.md)
* [Formularschaltfläche](components/forms/form-button.md)

>[!NOTE]
>
>Kernkomponenten sind für Autoren nicht sofort verfügbar. Das [Entwicklerteam muss sie zuerst in Ihre Umgebung integrieren](get-started/using.md). Nach der Integration können sie über den [Vorlageneditor](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=de) bereitgestellt und vorkonfiguriert werden.

>[!NOTE]
>
>Einige Versionen einzelner Kernkomponenten sind möglicherweise nur mit bestimmten Versionen von AEM kompatibel.
>
>Weitere Informationen zu Kompatibilitätsinformationen finden Sie auf der Hilfeseite für die jeweilige Komponente (Links in der vorherigen Liste) oder im Dokument [Kernkomponentenversionen](versions.md).

## Systemanforderungen {#system-requirements}

| Version der Kernkomponenten | AEM as a Cloud Service | AEM 6.5 LTS | AEM 6.5 | Java SE-Version | Maven-Version |
|---|---|---|---|---|---|
| [2.29.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.29.0) | Kontinuierlich | 6.5 LTS GA | 6.5.21.0+ | 8, 11 | 3.3.9+ |

Die Anforderungen aus früheren Kernkomponenten-Versionen finden Sie unter [Kernkomponenten-Versionen](versions.md).

Die Kernkomponenten erfordern die Verwendung [bearbeitbarer Vorlagen](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/page-authoring/template-editor-feature-video-use.html?lang=de) und unterstützen weder die klassische Benutzeroberfläche noch statische Vorlagen. Sehen Sie sich bei Bedarf die [AEM-Modernisierungs-Tools](https://opensource.adobe.com/aem-modernize-tools/) an, um Ihr Projekt mit diesen modernen AEM-Funktionen zu aktualisieren.

Informationen zum Einrichten Ihrer lokalen Entwicklungsumgebung finden Sie in [dieser Übersicht für AEM as a Cloud Service-SDK](https://experienceleague.adobe.com/docs/experience-manager-learn/cloud-service/local-development-environment-set-up/overview.html?lang=de) oder in diesem Dokument [für ältere Versionen von AEM](https://experienceleague.adobe.com/docs/experience-manager-learn/foundation/development/set-up-a-local-aem-development-environment.html?lang=de).

>[!TIP]
>
>Die Kernkomponenten sind automatisch Teil von AEM as a Cloud Service und Sie haben immer die neueste Version der Kernkomponenten.
>
>Weitere Informationen zu den ersten Schritten mit den Kernkomponenten in AEM as a Cloud Service und On-Premise finden Sie im Dokument [Verwenden von Kernkomponenten](/help/get-started/using.md).

## Andere Komponenten {#other-components}

AEM-Autoren stehen zusätzliche Komponenten zur Verfügung, die auf den Kernkomponenten basieren.

* [Die E-Mail-Kernkomponenten](/help/email/introduction.md) – Entdecken Sie Komponenten, die auf den Kernkomponenten basieren und speziell für die Verwendung mit Adobe Campaign entwickelt wurden.
* [Kernkomponenten für adaptive Formulare](/help/adaptive-forms/introduction.md) – Mithilfe der Kernkomponenten für adaptive Formulare können Sie Registrierungsprozesse in Adobe Experience Manager optimal gestalten.
