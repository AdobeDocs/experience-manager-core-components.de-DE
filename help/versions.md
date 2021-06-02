---
title: Kernkomponenten-Versionen
description: Kernkomponenten werden als Versionen veröffentlicht, die mehr als eine Version derselben Kernkomponenten enthalten können. In diesem Dokument wird erläutert, welche Versionen veröffentlicht werden und wie die Kompatibilität mit Kernkomponenten und AEM verstanden werden kann.
role: Architect, Developer, Administrator, Business Practitioner
exl-id: 7d4dbe46-4013-4217-b815-cdb1462072c6
source-git-commit: 9f7ecb12c7135033a87508901a5c8bd006f72a0e
workflow-type: tm+mt
source-wordcount: '2099'
ht-degree: 100%

---

# Kernkomponenten-Versionen {#core-components-versions}

Die aktuelle Version der Kernkomponenten ist 2.16.4 und mit [AEM as a Cloud Service](https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/landing/home.translate.html)- und [On-Premise-AEM](https://docs.adobe.com/content/help/de-DE/experience-manager-65/user-guide/home.html)-Installationen kompatibel.

## Versionsverlauf und Kompatibilität {#release-history-and-compatibility}

Die Kernkomponenten sind so konzipiert, dass sie flexibel und mit allen unterstützten AEM-Versionen kompatibel sind. Daher kann eine Version der Komponenten mehrere Versionen derselben Komponente enthalten.

Die folgenden Tabellen zeigen die Kompatibilität der Versionen der Kernkomponenten mit den Komponentenversionen an, in denen Versionen enthalten sind.

### Versionsverlauf und Anforderungen {#release-history-requirements}

Die folgende Tabelle, deren Inhalt [auf GitHub mit vollständigen Versionsinformationen](https://github.com/adobe/aem-core-wcm-components/releases) verfügbar ist, bietet einen Überblick über die Versionen der Kernkomponenten und deren Kompatibilität mit AEM-Versionen und Java-Versionen.

| Version | Beschreibung | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service | Java | Veröffentlichungsdatum |
|---|---|---|---|---|---|---|
| [2.16.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.16.4) | Dies ist eine Patch-Version, die ein Problem mit dem neuen Link-Handler behebt. | 6.4.8.1+ * | 6.5.5.0+ * | Kontinuierlich | 8, 11 | 19. Mai 2021 |
| [2.16.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.16.2) | Diese Patch-Version behob vor allem ein Problem mit dem neuen Link-Handler und fügte eine Verbesserung zur Unterstützung von Mehrseiten-Anwendungen für [PWA](/help/components/page.md#pwa-support) hinzu. | 6.4.8.1+ * | 6.5.5.0+ * | Kontinuierlich | 8, 11 | 15. Mai 2021 |
| [2.16.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.16.0) | Diese Version konzentrierte sich auf Verbesserungen der Barrierefreiheit sowie die Einführung eines neuen Link-Handlers für bestehende Komponenten. | 6.4.8.1+ * | 6.5.5.0+ * | Kontinuierlich | 8, 11 | 22. April 2021 |
| [2.15.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.15.2) | Es handelte sich hierbei um eine Patch-Version, die hauptsächlich Probleme mit der Abwärtskompatibilität von [Datenschicht](/help/developing/data-layer/overview.md) und IT-Tests, die in bestimmten Situationen fehlschlugen, behebt. | 6.4.8.1+ * | 6.5.5.0+ * | Kontinuierlich | 8, 11 | 16. März 2021 |
| [2.15.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.15.0) | Diese Version bietet Unterstützung für [Progressive Web Apps (PWA) in der Seitenkomponente](/help/components/page.md#pwa-support) und unterstützt Version 2.0.0 der [Adobe-Datenschicht](/help/developing/data-layer/overview.md). | 6.4.8.1+ * | 6.5.5.0+ * | Kontinuierlich | 8, 11 | 23. Februar 2021 |
| [2.14.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.14.0) | Diese Version enthält neue Optionen für die [Einbettungskomponente](/help/components/embed.md), führt den Marken-Slug auf der [Seitenebene](/help/components/page.md) ein und behebt viele Probleme. | 6.4.8.1+ * | 6.5.5.0+ * | Kontinuierlich | 8, 11 | 9. Februar 2021 |
| [2.13.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.13.2) | Dies war eine Patch-Version, die ein Problem mit dem RTE bei Verwendung in AEMaaCS behob. | 6.4.8.1+ * | 6.5.5.0+ * | Kontinuierlich | 8, 11 | 16. Dezember 2020 |
| [2.13.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.13.0) | Diese Version enthält neue Dynamic Media-Funktionen für die [Bildkomponente](/help/components/image.md). | 6.4.8.1+ * | 6.5.5.0+ * | Kontinuierlich | 8, 11 | 4. Dezember 2020 |
| [2.12.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.12.2) | Dies war eine Patch-Version für 2.12.0 mit kleineren Fehlerbehebungen. | 6.4.8.1+ * | 6.5.5.0+ * | Kontinuierlich | 8, 11 | 11. November 2020 |
| [2.12.1](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.12.1) | Dies war eine Patch-Version für 2.12.0, die einen größeren Fehler in der [Bildkomponente](/help/components/image.md) behob. | 6.4.8.1+ * | 6.5.5.0+ * | Kontinuierlich | 8, 11 | 5. November 2020 |
| [2.12.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.12.0) | Mit dieser Version wurden [ein neuer POST-Formularhandler](/help/components/forms/form-container.md#post-data), die Möglichkeit, benutzerdefinierte CSS-, JavaScript- und Metadaten-[Tags über eine kontextbezogene Konfiguration einzuschließen](/help/developing/including-clientlibs.md#context-aware-loading) sowie das Dienstprogramm `DataLayerBuilder` zur [Vereinfachung der Datenschichtintegration in benutzerdefinierten Komponenten](/help/developing/data-layer/integrations.md#enabling-custom-components) eingeführt. | 6.4.8.1+ * | 6.5.5.0+ * | Kontinuierlich | 8, 11 | 29. Oktober 2020 |
| [2.11.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.11.0) | Mit dieser Version wurde [AMP-Unterstützung](/help/developing/amp.md) eingeführt. | 6.4.8.1+ * | 6.5.5.0+ * | Kontinuierlich | 8, 11 | 20. Juli 2020 |
| [2.10.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.10.0) | Mit dieser Version wurde die [PDF-Viewer-Komponente](/help/components/pdf-viewer.md) eingeführt. | 6.4.8.1+ | 6.5.5.0+ | Kontinuierlich | 8, 11 | 17. Juni 2020 |
| [2.9.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.9.0) | Die Version ermöglichte die Integration mit der [Adobe Client-Datenschicht](/help/developing/data-layer/overview.md) und führte die [Fortschrittleistenkomponente](/help/components/progress-bar.md) ein. | 6.4.8.0+ | 6.5.4.0+ | Kontinuierlich | 8, 11 | 29. Mai 2020 |
| [2.8.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.8.0) | Diese Version konzentrierte sich auf Fehlerbehebungen mit kleinen Verbesserungen. | 6.4.4.0+ | 6.5.0.0+ | Kontinuierlich | 8, 11 | 5. Dezember 2019 |
| [2.7.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.7.0) | Mit dieser Version wurde die neue [Einbettungskomponente](/help/components/embed.md) eingeführt. | 6.4.4.0+ | 6.5.0.0+ | Kontinuierlich | 8, 11 | 25. September 2019 |
| [2.6.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.6.0) | Mit dieser Version wurde die neue [Experience Fragment-Komponente](/help/components/experience-fragment.md) eingeführt. | 6.4.4.0+ | 6.5.0.0+ | Kontinuierlich | 8, 11 | 6. September 2019 |
| [2.5.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.5.0) | In dieser Version wurden die neuen Komponenten [Akkordeon](/help/components/accordion.md), [Schaltfläche](/help/components/button.md), [Container](/help/components/container.md) und [Download](/help/components/download.md) eingeführt. | 6.4.2.0+ | 6.5.0.0+ | Kontinuierlich | 8, 11 | 25. Juni 2019 |
| [2.4.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.4.0) | Mit dieser Version wurde die [Inhaltsfragmentlisten-Komponente](/help/components/content-fragment-list.md) eingeführt. | 6.4.2.0+ | 6.5.0.0+ | Kontinuierlich | 8, 11 | 7. Mai 2019 |
| [2.3.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.3.2) | Diese Version konzentrierte sich auf Optimierungen in der [Komponentenbibliothek](https://aemcomponents.dev), enthält aber auch einige Funktionsverbesserungen für die [Trennzeichenkomponente](/help/components/separator.md). | 6.4.2.0+ | 6.5.0.0+ | Kontinuierlich | 8 | 14. März 2019 |
| [2.3.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.3.0) | Diese Version konzentrierte sich sowohl auf die [Komponentenbibliothek](https://aemcomponents.dev) als auch auf die Einführung der neuen [Trennzeichenkomponente](/help/components/separator.md), enthielt jedoch auch einige Funktionsverbesserungen für die [Bildkomponente](/help/components/image.md). | 6.4.2.0+ | - | - | 8 | 11. Februar 2019 |
| [2.2.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.2.2) | Diese Version konzentrierte sich hauptsächlich auf Fehlerbehebungen, enthielt aber auch einige Funktionsverbesserungen für die [Karussellkomponente](/help/components/carousel.md). | 6.4.2.0+ | - | - | 8 | 27. November 2018 |
| [2.2.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.2.0) | In dieser Version wurden die [Registerkartenkomponente](/help/components/tabs.md), die [Karussellkomponente](/help/components/carousel.md) und Verbesserungen der [Bildkomponente](/help/components/image.md), der [Seitenkomponente](/help/components/page.md) und der [Titelkomponente](/help/components/title.md) sowie verbessertes Tracking eingeführt. | 6.4.2.0+ | - | - | 8 | 16. Oktober 2018 |
| [2.1.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.1.0) | In dieser Version wurden die [Teaser-Komponente](/help/components/teaser.md) sowie Verbesserungen der [Bildkomponente](/help/components/image.md) und zahlreiche Fehlerbehebungen eingeführt. | 6.4.2.0+ | - | - | 8 | 13. Juli 2018 |
| [2.0.8](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.8) | Dies war eine Version mit Fehlerbehebungen. | 6.4.0.0+ | - | - | 8 | 12. Juni 2018 |
| [2.0.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.6) | In dieser Version wurden Hintergrundverbesserungen, Fehlerbehebungen und kleine Verbesserungen hinzugefügt, einschließlich Unterstützung für das Spiegeln von Bildern in der [Bildkomponente](/help/components/image.md). | 6.4.0.0+ | - | - | 8 | 11. April 2018 |
| [2.0.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.4) | Diese Version konzentrierte sich hauptsächlich auf Hintergrundverbesserungen, Fehlerbehebungen sowie einige kleinere Verbesserungen der [Bildkomponente](/help/components/image.md), [Seitenkomponente](/help/components/page.md) und [Inhaltsfragment-Komponente](/help/components/content-fragment-component.md). | 6.4.0.0+ | - | - | 8 | 7. März 2018 |
| [2.0.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.0) | In dieser Version wurden die [Navigationskomponente](/help/components/navigation.md), die [Sprachnavigations-Komponente](/help/components/language-navigation.md) und die [Schnellsuchkomponente](/help/components/quick-search.md) eingeführt sowie das [Stilsystem](/help/get-started/authoring.md#component-styling) für alle Komponenten implementiert. | 6.4.0.0+ | - | - | 8 | 16. Januar 2018 |
| [1.1.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.1.0) | Diese Version implementiert den JSON-Export für alle Komponenten und führt die [Inhaltsfragment-Komponente](/help/components/content-fragment-component.md) ein. | 6.4.0.0+ | - | - | 8 | 10. Oktober 2017 |
| [1.0.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.6) | In dieser Version werden mehrere Korrekturen für die [Bildkomponente](/help/components/image.md) hinzugefügt. | 6.4.0.0+ | - | - | 8 | 4. August 2017 |
| [1.0.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.4) | In dieser Version werden Fehlerbehebungen für die [Seitenkomponente](/help/components/page.md), die [Bildkomponente](/help/components/image.md) und verschiedene globale Korrekturen und Verbesserungen hinzugefügt. | 6.4.0.0+ | - | - | 8 | 26. April 2017 |
| [1.0.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.all-1.0.2) | Diese Version fügt Korrekturen für animierte GIF-Bilder in der [Bildkomponente](/help/components/image.md) hinzu. | 6.4.0.0+ | - | - | 7 | 22. März 2017 |
| [1.0.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.0) | Erstmalige Veröffentlichung von Kernkomponenten. | 6.4.0.0+ | - | - | 7 | 20. März 2017 |

>[!NOTE]
>
>(*) Ab Version 2.11.0 ist `org.apache.sling.models.impl`-Version 1.4.12 oder höher erforderlich (aufgrund von [SLING-8781](https://issues.apache.org/jira/browse/SLING-8781)). Diese wird für AEM 6.4 und 6.5 in einem zukünftigen Service Pack bereitgestellt. Bis dahin ist das Sling Models-Bundle im Paket `core.wcm.components.all` enthalten.

>[!TIP]
>
>Wie bei AEM empfiehlt Adobe, dass Entwickler die [neueste Freigabe und Versionen der Kernkomponenten](https://github.com/adobe/aem-core-wcm-components/releases/latest) verwenden, die mit der Version von AEM kompatibel sind, die sie ausführen, um die aktuellsten Fehlerbehebungen und Funktionen zu nutzen.

### Komponentenversionen und -freigaben {#component-versions-and-releases}

Die folgende Tabelle zeigt, welche Versionen welcher Komponenten in welchen Releases der Kernkomponenten enthalten sind.

|  | Release 1.0.0-1.0.6 | Release 1.1.0 | Release 2.0.0-2.0.8 | Release 2.1.0 | Release 2.2.0-2.2.0 | Release 2.3.0-2.3.2 | Release 2.4.0 | Release 2.5.0 | Release 2.6.0 | Release 2.7.0-2.8.0 | Release 2.9.0+ |
|---|---|---|---|---|---|---|---|---|---|---|---|
| **[Seite](components/page.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Titel](components/title.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Bild](components/image.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Liste](components/list.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Breadcrumb](components/breadcrumb.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Freigabe in Social Media](components/sharing.md)** | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Formular-Container](components/forms/form-container.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Formulartext](components/forms/form-text.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Formularoptionen](components/forms/form-options.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Ausgeblendetes Formular](components/forms/form-hidden.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Formularschaltfläche](components/forms/form-button.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Inhaltsfragment](components/content-fragment-component.md)** |  | Sandbox | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1, v2 | v1, v2 |
| **[Navigation](components/navigation.md)** |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Sprachnavigation](components/language-navigation.md)** |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Schnellsuche](components/quick-search.md)** |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Teaser](components/teaser.md)** |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Registerkarten](components/tabs.md)** |  |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Karussell](components/carousel.md)** |  |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Trennzeichen](components/separator.md)** |  |  |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Inhaltsfragmentliste](components/content-fragment-list.md)** |  |  |  |  |  |  | v1 | v1 | v1 | v1 | v1 |
| **[Akkordeon](components/accordion.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 | v1 |
| **[Schaltfläche](components/button.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 | v1 |
| **[Container](components/container.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 | v1 |
| **[Download](components/download.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 | v1 |
| **[Experience Fragment](components/experience-fragment.md)** |  |  |  |  |  |  |  |  | v1 | v1 | v1 |
| **[Einbetten](components/embed.md)** |  |  |  |  |  |  |  |  |  | v1 | v1 |
| **[Fortschrittsleiste](components/progress-bar.md)** |  |  |  |  |  |  |  |  |  |  | v1 |
| **[PDF-Viewer](components/pdf-viewer.md)** |  |  |  |  |  |  |  |  |  |  | v1 |

## Versionen {#versions-and-releases}

Kernkomponenten werden über GitHub verteilt. Dadurch kann Adobe den Komponenten schneller Funktionen hinzufügen und die Community-Eingabe außerhalb des AEM-Versionszyklus zulassen.

Die Kernkomponenten werden mit definierten AEM-Versionen bereitgestellt, mit denen sie kompatibel sind. Dies bedeutet, dass eine AEM-Version mehrere Versionen der Kernkomponenten unterstützt. Dies bietet mehr Flexibilität als die früheren Foundation-Komponenten, die an eine bestimmte Version von AEM gebunden waren.

### Versionen {#versions}

Die Hauptiteration der Kernkomponenten sind die **Versionen**. Jede Komponente hat eine Version. Versionen werden mit dem Zusatz **v** bezeichnet und es ihnen eine positive Ganzzahl ungleich Null angehängt, z. B. v1 und v2. Versionen werden nur für Änderungen inkrementiert, die nicht abwärtskompatibel sind. Dies gilt normalerweise für die Einführung neuer Funktionen und Funktionalitäten.

Entwickler und Administratoren können Versionen der Kernkomponenten anhand einer Zahl in ihren Ressourcentyppfaden und in den vollständig qualifizierten Java-Klassennamen ihrer Implementierungen erkennen. Diese Versionsnummer stellt eine Hauptversion dar, wie in [der semantischen Versionierung der Richtlinien](https://semver.org/) dargestellt wird.

Weitere Informationen zu Kernkomponentenversionen finden Sie in der [Entwicklerdokumentation zu den Kernkomponenten](developing/guidelines.md).

### Versionen {#releases}

Die Kernkomponenten werden über **Versionen** verfügbar gemacht. Sie [stellen die tatsächlichen veröffentlichten Artefakte dar, die auf GitHub verfügbar sind](https://github.com/adobe/aem-core-wcm-components/releases). Versionen werden mit einer Dezimalzahl im Format X.Y.Z gekennzeichnet und alle Kernkomponenten werden zusammen als bereitstellbares Paket erfasst.

* **Hauptversionen** können neue Versionen vorhandener Komponenten sowie völlig neue Komponenten sowie Standardfehlerbehebungen einführen. Dies wird durch eine Inkrementierung der X-Komponente der Versionsnummer dargestellt.
* **Wichtige Versionen** können neue Funktionen für vorhandene Versionen von Komponenten zusammen mit Fehlerbehebungen einführen. Dies wird durch eine Inkrementierung der Y-Komponente der Versionsnummer dargestellt.
* **Nebenversionen** enthalten nur Fehlerkorrekturen. Dies wird durch eine schrittweise Erhöhung in der Z-Komponente der Release-Nummer dargestellt.

>[!NOTE]
>
>Versionen können mehrere Versionen derselben Komponente enthalten.
>
>Dieselbe Version einer Komponente kann in mehreren Versionen angezeigt werden.

## Support für Kernkomponenten {#core-components-support}

Kernkomponenten sind ein integraler Bestandteil von AEM und werden ohne Mängelgewähr unterstützt, zu den gleichen Bedingungen und Konditionen, als ob sie im Rahmen des Quickstarts geliefert würden.

Wie bei anderen Produktmerkmalen gilt für das Ende der Lebensdauer die allgemeine Regel:

* Komponenten werden zuerst als veraltet angekündigt, bevor sie entfernt werden.
* Sie werden dann frühestens nach Ankündigung aus dem AEM-Release entfernt.

Dadurch erhalten Kunden mindestens einen Versionszyklus, um zur neuen Version der Komponente zu wechseln, bevor die Unterstützung endet.

Die Version jeder Komponente gibt eindeutig die AEM-Versionen an, die sie unterstützt. Wenn der Support für eine Version von AEM eingestellt wird, gilt das auch für die Unterstützung der Kernkomponenten für diese Version von AEM.

Weitere Informationen zum Support von Komponentenanpassungen finden Sie auf der Seite [Anpassen von Kernkomponenten](developing/customizing.md) der entsprechenden Kernkomponentenversion.

## Unterstützung von Foundation-Komponenten {#foundation-component-support}

Der Entwicklungsschwerpunkt von Adobe hat sich zu den Kernkomponenten verlagert. Weitere Funktionen werden fortlaufend hinzugefügt.

[Fast alle Foundation-Komponenten sind seit AEM 6.5 veraltet](https://docs.adobe.com/content/help/de-DE/experience-manager-65/authoring/siteandpage/default-components-foundation.html) und werden in Zukunft nur noch mit größeren Fehlerbehebungen aktualisiert.
