---
title: Einführung in Kernkomponenten
description: 'Kernkomponenten wurden eingeführt, um robuste und erweiterbare Basiskomponenten bereitzustellen, die auf aktueller Technologie und Best Practices basieren. '
translation-type: tm+mt
source-git-commit: 71c1cca664dde91968df16848650df9f0f0a5218

---


# Einführung in Kernkomponenten{#core-components-introduction}

In Adobe Experience Manager sind Komponenten die strukturellen Elemente, aus denen der Inhalt von bearbeiteten Seiten besteht. Komponenten waren immer ein Grundelement des AEM-Erlebnisses, wodurch die Seitenerstellung einfach, aber für den Autor und die Entwicklung von Komponenten flexibel und erweiterbar ist.

Die Kernkomponenten sind eine Reihe standardisierter Web-Content-Management-Komponenten (WCM) für AEM, um die Entwicklungszeit zu verkürzen und die Wartungskosten Ihrer Websites zu senken.

## Ressourcen {#resources}

* **[Komponentenbibliothek:](https://www.adobe.com/go/aem_cmp_library)**Eine Beispielsammlung zur Ansicht der Komponenten in ihren verschiedenen Konfigurationen.
* **Komponentendokumentation (dieses Dokument):** Für Entwickler und Autoren mit Details zu den einzelnen Komponenten.
* Erste Schritte:
   * **[Erfolg mit den Kernkomponenten:](/help/developing/success.md)**Richtlinien, die vor dem Beginn eines Projekts, das die Kernkomponenten verwendet, zu berücksichtigen sind.
   * **[WKND-Tutorial:](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)**Ein zweitägiges Lernprogramm zum Erstellen einer neuen Site.
   * **[Summit-Lernprogramm:](https://expleague.azureedge.net/labs/L767/index.html)**Ein zweistündiges Tutorial zum Aufbau einer neuen Site (von einem Lab auf dem US Summit 2019).
   * **[Gems Webinar:](https://helpx.adobe.com/de/experience-manager/kt/eseminars/gems/AEM-Core-Components.html)**Eine Führung durch die Kernkomponenten (aufgenommen am Dezember 2018).

## Funktionen {#features}

|||—|—||Produktionsbereit| Die Kernkomponenten sind 27 robuste Komponenten, die gut getestet, weit verbreitet und gut funktionieren.||Cloud-Ready| Ob auf [AEM als Cloud-Dienst](https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/landing/home.translate.html), auf [Adobe Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams)oder lokal - sie funktionieren nur.||Vielseitig| Die Komponenten stellen allgemeine Konzepte dar, mit denen die Autoren nahezu jedes Layout zusammenstellen können.||Konfigurierbar| [Inhaltsrichtlinien](https://docs.adobe.com/content/help/en/experience-manager-65/developing/platform/templates/page-templates-editable.html#content-policies) auf Vorlagenebene definieren, welche Funktionen die Seitenautoren verwenden dürfen oder nicht.|
|Accessible| They comply [WCAG 2.1 standard](https://www.w3.org/TR/WCAG21/), provide ARIA labels, and support keyboard navigation ([known issues](https://github.com/adobe/aem-core-wcm-components/issues?utf8= ✓&amp;q=is%3Aissue+is%3Aopen+accessibility+in%3Atitle)).|
|SEO-Friendly| The HTML output is semantic and provides [schema.org](https://schema.org) microdata annotations.||WebApp-Ready| Die [optimierte JSON-Ausgabe](https://docs.adobe.com/content/help/en/experience-manager-learn/foundation/development/develop-sling-model-exporter.html) ermöglicht das clientseitige Rendering, wobei auch [kontextbezogene Bearbeitung](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html)möglich ist.|| Design Kit| Ein [UI-Kit für Adobe XD](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/assets/overview/AEM_UI-kit_Wireframe.xd) ermöglicht Designern, Wireframes zu erstellen, die sie dann nach Bedarf [gestalten können](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/assets/overview/AEM_UI-kit_WKND.xd).|
|Themeable| The components implement the [Style System](https://docs.adobe.com/content/help/en/experience-manager-65/developing/components/style-system.html), and the markup follows [BEM CSS conventions](http://getbem.com/).||Anpassbar| Mehrere Muster ermöglichen eine [einfache Anpassung](developing/customizing.md), von der Anpassung des HTML bis zur erweiterten Funktionswiederverwendung.||Versionierung| Die [Versionierungsrichtlinie](https://github.com/adobe/aem-core-wcm-components/wiki/Versioning-policies) stellt sicher, dass die Kernkomponenten Ihre Site nicht unterbrechen, wenn Sie Dinge verbessern, die sich auf Sie auswirken könnten.|
|Localizable|Smart reference resolution allows certain components to find and [render corresponding localized content automatically](get-started/localization.md).||Open Sourcing| Wenn etwas nicht so ist, wie es sollte, [tragen Sie Ihre Verbesserungen bei!](https://github.com/adobe/aem-core-wcm-components/blob/master/CONTRIBUTING.md)|

## Die Komponenten {#the-components}

Die aktuelle Version der Kernkomponenten enthält die folgenden Komponenten.

### Vorlagenkomponenten {#template-components}

* [Seite](components/page.md)
* [Navigation](components/navigation.md)
* [Sprachnavigation](components/language-navigation.md)
* [Breadcrumb](components/breadcrumb.md)
* [Schnellsuche](components/quick-search.md)

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
* [Freigabe in Social Media](components/sharing.md)
* [Trennzeichen](components/separator.md)

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
>Kernkomponenten sind für Autoren nicht sofort verfügbar. Das [Entwicklerteam muss sie zuerst in Ihre Umgebung integrieren](get-started/using.md). Nach der Integration können sie über den [Vorlageneditor](https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/sites/authoring/features/templates.translate.html) bereitgestellt und vorkonfiguriert werden.

>[!NOTE]
>
>Einige Versionen einzelner Kernkomponenten sind möglicherweise nur mit bestimmten Versionen von AEM kompatibel.
>
>Weitere Informationen zu Kompatibilitätsinformationen finden Sie auf der Hilfeseite für die jeweilige Komponente (Links in der vorherigen Liste) oder im Dokument [Kernkomponentenversionen](versions.md).

## Systemanforderungen {#system-requirements}

| Kernkomponenten | AEM as a Cloud Service | AEM 6.5 | AEM 6.4 | AEM 6.3 | Java SE | Maven |
---------|---------|---------|---------|---------|---------|---------
| [2.8.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.8.0) | Kontinuierlich | 6.5.0.0+ | 6.4.4.0+ | 6.3.3.4+ | 8, 11 | 3.3.9+ |

Die Anforderungen aus früheren Versionen der Core-Komponenten finden Sie unter [Core-Komponentenversionen](versions.md).

Die Kernkomponenten erfordern die Verwendung [bearbeitbarer Vorlagen](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/page-authoring/template-editor-feature-video-use.html) und unterstützen keine klassische Benutzeroberfläche oder statische Vorlagen. Überprüfen Sie bei Bedarf die [AEM-Modernisierungstools](https://opensource.adobe.com/aem-modernize-tools/pages/tools.html) , um Ihr Projekt mit diesen modernen AEM-Funktionen zu aktualisieren.

Um Ihre lokale Entwicklungs-Umgebung einzurichten, lesen Sie [diese Übersicht für AEM als Cloud-Dienst-SDK](https://docs.adobe.com/content/help/en/experience-manager-learn/cloud-service/local-development-environment-set-up/overview.html) oder dieses Dokument [für ältere Versionen von AEM](https://docs.adobe.com/content/help/en/experience-manager-learn/foundation/development/set-up-a-local-aem-development-environment.html).
