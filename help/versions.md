---
title: Kernkomponenten-Versionen
description: Kernkomponenten werden als Versionen veröffentlicht, die mehr als eine Version derselben Kernkomponenten enthalten können. In diesem Dokument wird erläutert, welche Versionen veröffentlicht werden und wie die Kompatibilität mit Kernkomponenten und AEM verstanden werden kann.
translation-type: tm+mt
source-git-commit: c64276bb95aeaef4223fc2a0dc2c3cfdf8609f5a
workflow-type: tm+mt
source-wordcount: '1848'
ht-degree: 78%

---


# Kernkomponenten-Versionen {#core-components-versions}

Die aktuelle Version der Kernkomponenten ist 2.12.1 und mit [AEM as a Cloud Service](https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/landing/home.translate.html)- und [lokalen AEM](https://docs.adobe.com/content/help/en/experience-manager-65/user-guide/home.html)-Installationen kompatibel. Es wurde im November 2020 als Patch-Version für 2.12.0 veröffentlicht. In Version 2.12.0 wurden mehrere neue Funktionen für Formulare, Metadaten und die Datenschicht eingeführt.

## Versionsverlauf und Kompatibilität {#release-history-and-compatibility}

Die Kernkomponenten sind so konzipiert, dass sie flexibel und mit allen unterstützten AEM-Versionen kompatibel sind. Daher kann eine Version der Komponenten mehrere Versionen derselben Komponente enthalten.

Die folgenden Tabellen zeigen die Kompatibilität der Versionen der Kernkomponenten mit den Komponentenversionen an, in denen Versionen enthalten sind.

### Versionsverlauf und Anforderungen {#release-history-requirements}

Die folgende Tabelle, deren Inhalt [auf GitHub mit vollständigen Versionsinformationen](https://github.com/adobe/aem-core-wcm-components/releases) verfügbar ist, bietet einen Überblick über die Versionen der Kernkomponenten und deren Kompatibilität mit AEM-Versionen und Java-Versionen.

| Version | Beschreibung | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service | Java | Veröffentlichungsdatum |
|---|---|---|---|---|---|---|
| [2.12.1](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.11.1) | Dies war ein Patch Release für 2.12.0, das einen wichtigen Fehler in der Image-Komponente behebt. | 6.4.8.1+ * | 6.5.5.0+ * | Kontinuierlich | 8, 11 | 5. November 2020 |
| [2.12.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.11.0) | Mit dieser Version wurde [ein neuer POST-Formularhandler eingeführt.](/help/components/forms/form-container.md#post-data) die Möglichkeit, benutzerdefinierte CSS-, JavaScript- und Metadaten- [Tags über eine kontextbezogene Konfiguration einzuschließen;](/help/developing/including-clientlibs.md#context-aware-loading) und ein `DataLayerBuilder` Dienstprogramm zur [Vereinfachung der Datenschichtintegration in benutzerdefinierten Komponenten.](/help/developing/data-layer/integrations.md#enabling-custom-components) | 6.4.8.1+ * | 6.5.5.0+ * | Kontinuierlich | 8, 11 | 29. Oktober 2020 |
| [2.11.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.11.0) | This release introduced [AMP support.](/help/developing/amp.md) | 6.4.8.1+ * | 6.5.5.0+ * | Kontinuierlich | 8, 11 | 20. Juli 2020 |
| [2.10.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.10.0) | This release introduced the [PDF Viewer component.](/help/components/pdf-viewer.md) | 6.4.8.1+ | 6.5.5.0+ | Kontinuierlich | 8, 11 | 17. Juni 2020 |
| [2.9.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.9.0) | This release enabled integration with the [Adobe Client Data Layer](/help/developing/data-layer/overview.md) and introduced the [Progress Bar component.](/help/components/progress-bar.md) | 6.4.8.0+ | 6.5.4.0+ | Kontinuierlich | 8, 11 | 29. Mai 2020 |
| [2.8.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.8.0) | Diese Version konzentrierte sich auf Fehlerbehebungen mit kleinen Verbesserungen. | 6.4.4.0+ | 6.5.0.0+ | Kontinuierlich | 8, 11 | 5. Dezember 2019 |
| [2.7.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.7.0) | This release introduced the new [Embed component.](/help/components/embed.md) | 6.4.4.0+ | 6.5.0.0+ | Kontinuierlich | 8, 11 | 25. September 2019 |
| [2.6.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.6.0) | This release introduced the new [Experience Fragment component.](/help/components/experience-fragment.md) | 6.4.4.0+ | 6.5.0.0+ | Kontinuierlich | 8, 11 | 6. September 2019 |
| [2.5.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.5.0) | This release introduced the new [Accordion,](/help/components/accordion.md) [Button,](/help/components/button.md) [Container,](/help/components/container.md) and [Download components.](/help/components/download.md) | 6.4.2.0+ | 6.5.0.0+ | Kontinuierlich | 8, 11 | 25. Juni 2019 |
| [2.4.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.4.0) | This release introduced the [Content Fragment List Component.](/help/components/content-fragment-list.md) | 6.4.2.0+ | 6.5.0.0+ | Kontinuierlich | 8, 11 | 7. Mai 2019 |
| [2.3.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.3.2) | This release focused on refinements to the [Component Library,](https://aemcomponents.dev) but also contains some feature enhancements for the [Separator Component.](/help/components/separator.md) | 6.4.2.0+ | 6.5.0.0+ | Kontinuierlich | 8 | 14. März 2019 |
| [2.3.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.3.0) | This release focused on the [Component Library](https://aemcomponents.dev) as well as introducing the new [Separator Component,](/help/components/separator.md) but also contains some feature enhancements for the [Image Component.](/help/components/image.md) | 6.4.2.0+ | - | - | 8 | 11. Februar 2019 |
| [2.2.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.2.2) | This release mainly focused on bug fixes, but also contains some feature enhancements for the [Carousel Component.](/help/components/carousel.md) | 6.4.2.0+ | - | - | 8 | 27. November 2018 |
| [2.2.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.2.0) | In dieser Version wurden die [Registerkartenkomponente](/help/components/tabs.md) und die [Karussell-Komponente](/help/components/carousel.md) sowie Verbesserungen der [Bildkomponente,](/help/components/image.md) der [Seitenkomponente und der](/help/components/page.md) Titelkomponente [](/help/components/title.md) und die erweiterte Verfolgung eingeführt. | 6.4.2.0+ | - | - | 8 | 16. Oktober 2018 |
| [2.1.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.1.0) | In dieser Version wurde die [Teaser-Komponente](/help/components/teaser.md) mit Verbesserungen der [Bildkomponente](/help/components/image.md) und zahlreichen Fehlerkorrekturen eingeführt. | 6.4.2.0+ | - | - | 8 | 13. Juli 2018 |
| [2.0.8](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.8) | Dies war eine Fehlerbehebung. | 6.4.0.0+ | - | - | 8 | 12. Juni 2018 |
| [2.0.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.6) | In dieser Version wurden Verbesserungen unter der Haube, Fehlerkorrekturen und kleine Verbesserungen hinzugefügt, einschließlich Unterstützung für das Spiegeln von Bildern in der [Bildkomponente.](/help/components/image.md) | 6.4.0.0+ | - | - | 8 | 11. April 2018 |
| [2.0.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.4) | Diese Version konzentrierte sich hauptsächlich auf Verbesserungen unter der Haube, Fehlerkorrekturen sowie einige kleinere Verbesserungen der [Bildkomponente,](/help/components/image.md) [Seitenkomponente und](/help/components/page.md) [Inhaltsfragment-Komponente.](/help/components/content-fragment-component.md) | 6.4.0.0+ | - | - | 8 | 7. März 2018 |
| [2.0.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.0) | In dieser Version wurden die [Navigationskomponente,](/help/components/navigation.md) die [Sprachnavigationskomponente und die](/help/components/language-navigation.md) Schnellsuchkomponente [vorgestellt und das](/help/components/quick-search.md) Stilsystem [](/help/get-started/authoring.md#component-styling) für alle Komponenten implementiert. | 6.4.0.0+ | - | - | 8 | 16. Januar 2018 |
| [1.1.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.1.0) | Diese Version implementiert den JSON-Export für alle Komponenten und stellt die [Inhaltsfragment-Komponente vor.](/help/components/content-fragment-component.md) | 6.4.0.0+ | - | - | 8 | 10. Oktober 2017 |
| [1.0.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.6) | In dieser Version werden mehrere Korrekturen für die [Bildkomponente hinzugefügt.](/help/components/image.md) | 6.4.0.0+ | - | - | 8 | 4. August 2017 |
| [1.0.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.4) | In dieser Version werden Fehlerbehebungen für die [Seitenkomponente,](/help/components/page.md) die [Bildkomponente und verschiedene globale Korrekturen und Verbesserungen hinzugefügt](/help/components/image.md) . | 6.4.0.0+ | - | - | 8 | 26. April 2017 |
| [1.0.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.all-1.0.2) | Diese Version fügt Korrekturen für animierte GIF-Bilder in der [Bildkomponente hinzu.](/help/components/image.md) | 6.4.0.0+ | - | - | 7 | 22. März 2017 |
| [1.0.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.0) | Erstmalige Freigabe von Kernkomponenten. | 6.4.0.0+ | - | - | 7 | 20. März 2017 |

>[!NOTE]
>
>(*) Seit Version 2.11.0 ist `org.apache.sling.models.impl` Version 1.4.12 oder höher erforderlich (aufgrund von [SLING-8781](https://issues.apache.org/jira/browse/SLING-8781)). Dies wird für AEM 6.4 und 6.5 in einem zukünftigen Service Pack bereitgestellt. Bis dahin ist das Paket Sling Models im `core.wcm.components.all` Paket enthalten.

>[!TIP]
>
>Wie bei AEM empfiehlt Adobe, dass Entwickler die [neueste Freigabe und Versionen der Kernkomponenten](https://github.com/adobe/aem-core-wcm-components/releases/latest) verwenden, die mit der Version von AEM kompatibel sind, die sie ausführen, um die aktuellsten Fehlerbehebungen und Funktionen zu nutzen.

### Komponentenversionen und -freigaben {#component-versions-and-releases}

Die folgende Tabelle zeigt, welche Versionen welcher Komponenten in welchen Releases der Kernkomponenten enthalten sind.

|  | Release 1.0.0–1.0.6 | Release 1.1.0 | Release 2.0.0–2.0.8 | Release 2.1.0 | Release 2.2.0–2.2.0 | Release 2.3.0–2.3.2 | Release 2.4.0 | Release 2.5.0 | Release 2.6.0 | Release 2.7.0-2.8.0 | Release 2.9.0+ |
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
| **[Accordion](components/accordion.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 | v1 |
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

Weitere Informationen zu Kernkomponentenversionen finden Sie in der [Entwicklerdokumentation der Kernkomponenten](developing/guidelines.md).

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
