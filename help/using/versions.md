---
title: Kernkomponenten-Versionen
seo-title: Kernkomponenten-Versionen
description: Kernkomponenten werden als Versionen veröffentlicht, die mehr als eine Version derselben Kernkomponenten enthalten können. In diesem Dokument wird erläutert, welche Versionen veröffentlicht werden und wie die Kompatibilität mit Kernkomponenten und AEM verstanden werden kann.
seo-description: Kernkomponenten werden als Versionen veröffentlicht, die mehr als eine Version derselben Kernkomponenten enthalten können. In diesem Dokument wird erläutert, welche Versionen veröffentlicht werden und wie die Kompatibilität mit Kernkomponenten und AEM verstanden werden kann.
uuid: a916a923-8c5e-456a-84b5-b52228e21434
contentOwner: bohnert
content-type: reference
topic-tags: introduction
products: SG_EXPERIENCEMANAGER/CORECOMPONENTS
discoiquuid: a3a98b2f-65bf-4493-82ad-01717938fdbc
translation-type: tm+mt
source-git-commit: 1a78794d95b9fb4932c9560c167cf41d9b17470b

---


# Kernkomponenten-Versionen {#core-components-versions}

Die aktuelle Version der Core-Komponenten ist 2.8.0 und mit AEM 6.5 kompatibel. Es wurde im Dezember 2019 als eine wichtige Aktualisierung veröffentlicht 2.0.0. In Version 2.0.0 wurden neue Komponenten sowie v2-Aktualisierungen vorhandener Komponenten eingeführt.

Weitere Informationen finden Sie im Abschnitt [Versionsverlauf und Kompatibilität](#versions-and-releases) dieses Dokuments.

Sie können auch die [Komponentenbibliothek](http://opensource.adobe.com/aem-core-wcm-components/library.html) besuchen, in der Sie die aktuelle Version der Kernkomponenten und Beispiele für ihre Verwendung finden.

## Versionen {#versions-and-releases}

Kernkomponenten werden über GitHub verteilt. Dadurch kann Adobe den Komponenten schneller Funktionen hinzufügen und die Community-Eingabe außerhalb des AEM-Versionszyklus zulassen.

Die Kernkomponenten werden mit definierten AEM-Versionen bereitgestellt, mit denen sie kompatibel sind. Dies bedeutet, dass eine AEM-Version mehrere Versionen der Kernkomponenten unterstützt. Dies bietet mehr Flexibilität als die früheren Foundation-Komponenten, die an eine bestimmte Version von AEM gebunden waren.

### Versionen {#versions}

Die Hauptiteration der Kernkomponenten sind die **Versionen**. Jede Komponente hat eine Version. Versionen werden mit dem Zusatz **v** bezeichnet und es ihnen eine positive Ganzzahl ungleich Null angehängt, z. B. v1 und v2. Versionen werden nur für Änderungen inkrementiert, die nicht abwärtskompatibel sind. Dies gilt normalerweise für die Einführung neuer Funktionen und Funktionalitäten.

Entwickler und Administratoren können Versionen der Kernkomponenten anhand einer Zahl in ihren Ressourcentyppfaden und in den vollständig qualifizierten Java-Klassennamen ihrer Implementierungen erkennen. Diese Versionsnummer stellt eine Hauptversion dar, wie in [der semantischen Versionierung der Richtlinien](https://semver.org/) dargestellt wird.

Weitere Informationen zu Kernkomponentenversionen finden Sie in der [Entwicklerdokumentation der Kernkomponenten](guidelines.md).

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

## Versionsverlauf und Kompatibilität {#release-history-and-compatibility}

Die Kernkomponenten wurden zuerst mit AEM 6.3 veröffentlicht und sind so ausgelegt, dass sie flexibel und mit allen unterstützten AEM-Versionen kompatibel sind. Daher kann eine Version der Komponenten mehrere Versionen derselben Komponente enthalten.

Die folgenden Tabellen zeigen die Kompatibilität der Versionen der Kernkomponenten mit den Komponentenversionen an, in denen Versionen enthalten sind.

### Versionsverlauf und unterstützte AEM-Versionen {#release-history-supported-aem-versions}

Die folgende Tabelle, deren Inhalt [auf GitHub mit vollständigen Versionsinformationen](https://github.com/adobe/aem-core-wcm-components/releases) verfügbar ist, bietet einen Überblick über die Versionen der Kernkomponenten und deren Kompatibilität mit AEM-Versionen und Java-Versionen.

| Version | Beschreibung | AEM 6.3 | AEM 6.4 | AEM 6.5 | Java | Veröffentlichungsdatum |
|---|---|---|---|---|---|---|
| [2.8.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.8.0) | Diese Version konzentrierte sich auf Fehlerbehebungen mit kleinen Verbesserungen. | 6.3.3.4+ | 6.4.4.0+ | 6.5.0.0+ | 8, 11 | 5. Dezember 2019 |
| [2.7.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.7.0) | Mit dieser Version wurde die neue Einbettungskomponente eingeführt. | 6.3.3.4+ | 6.4.4.0+ | 6.5.0.0+ | 8, 11 | &amp;#x200B;25. September 2019 |
| [2.6.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.6.0) | Mit dieser Version wurde die neue Experience Fragment-Komponente eingeführt. | 6.3.3.4+ | 6.4.4.0+ | 6.5.0.0+ | 8, 11 | &amp;#x200B;6. September 2019 |
| [2.5.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.5.0) | Mit dieser Version wurden die neuen Komponenten Akkordeon, Schaltfläche, Container und Download eingeführt. | 6.3.3.0+ | 6.4.2.0+ | 6.5.0.0+ | 8, 11 | &amp;#x200B;25. Juni 2019 |
| [2.4.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.4.0) | Mit dieser Version wurde die Inhaltsfragmentlisten-Komponente eingeführt. | 6.3.3.0+ | 6.4.2.0+ | 6.5.0.0+ | 8, 11 | &amp;#x200B;7. Mai 2019 |
| [2.3.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.3.2) | Diese Version konzentriert sich auf Verfeinerungen in der Komponentenbibliothek, enthält aber auch einige Funktionsverbesserungen für die Trennzeichenkomponente | 6.3.3.0+ | 6.4.2.0+ | 6.5.0.0+ | 8 | &amp;#x200B;14. März 2019 |
| [2.3.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.3.0) | Diese Version konzentriert sich sowohl auf die Komponentenbibliothek als auch auf die Einführung der neuen Trennzeichenkomponente, enthält jedoch auch einige Funktionsverbesserungen für die Bild-Komponente. | 6.3.3.0+ | 6.4.2.0+ | - | 8 | &amp;#x200B;11. Februar 2019 |
| [2.2.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.2.2) | Diese Version konzentriert sich hauptsächlich auf Fehlerbehebungen, enthält aber auch einige Funktionsverbesserungen für die Karussell-Komponente. | 6.3.3.0+ | 6.4.2.0+ | - | 8 | &amp;#x200B;27. November 2018 |
| [2.2.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.2.0) | Registerkarten- und Karussell-Komponenten eingeführt, Verbesserungen der Bild-, Seiten- und Titelkomponenten und eine verbesserte Verfolgung | 6.3.3.0+ | 6.4.2.0+ | - | 8 | &amp;#x200B;16. Oktober 2018 |
| [2.1.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.1.0) | Teaser-Komponente eingeführt, Verbesserungen der Bildkomponente und zahlreiche Fehlerkorrekturen | 6.3.3.0+ | 6.4.2.0+ | - | 8 | &amp;#x200B;13. Juli 2018 |
| [2.0.8](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.8) | Version mit Fehlerkorrekturen | 6.3.2.0+ | 6.4.0.0+ | - | 8 | &amp;#x200B;12. Juni 2018 |
| [2.0.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.6) | Zusätzliche Hintergrundverbesserungen, Fehlerkorrekturen, und kleine Verbesserungen, einschließlich der Unterstützung von Image Flip. | 6.3.2.0+ | 6.4.0.0+ | - | 8 | &amp;#x200B;11. April 2018 |
| [2.0.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.4) | Meist Hintergrundverbesserungen, Fehlerbehebungen und einige kleinere Verbesserungen der Bild-, Seiten- und Inhaltsfragment-Komponenten | 6.3.2.0+ | 6.4.0.0+ | - | 8 | &amp;#x200B;7. März 2018 |
| [2.0.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.0) | Komponenten zur Navigation, Sprachnavigation und Schnellsuche wurden eingeführt. Für alle Komponenten implementiertes Stilsystem. | 6.3.2.0+ | 6.4.0.0+ | - | 8 | &amp;#x200B;16. Januar 2018 |
| [1.1.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.1.0) | Implementierung des JSON-Exports für alle Komponenten, Einführung der Inhaltsfragment-Komponente | 6.3.1.0 | 6.4.0.0+ | - | 8 | &amp;#x200B;10. Oktober 2017 |
| [1.0.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.6) | Mehrere Fehlerbehebungen für die Bildkomponente | 6.3.0.0+ | 6.4.0.0+ | - | 8 | &amp;#x200B;4. August 2017 |
| [1.0.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.4) | Fehlerbehebungen der Seitenkomponente, der Bildkomponente, verschiedene globale Korrekturen und Verbesserungen | 6.3.0.0+ | 6.4.0.0+ | - | 8 | &amp;#x200B;26. April 2017 |
| [1.0.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.all-1.0.2) | Korrekturen für animierte GIF-Bilder in der Bildkomponente | 6.3.0.0+ | 6.4.0.0+ | - | 7 | &amp;#x200B;22. März 2017 |
| [1.0.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.0) | Erstmalige Freigabe von Kernkomponenten | 6.3.0.0+ | 6.4.0.0+ | - | 7 | &amp;#x200B;20. März 2017 |

>[!NOTE]
>
>Wie bei AEM empfiehlt Adobe, dass Entwickler die [neueste Freigabe und Versionen der Kernkomponenten](https://github.com/adobe/aem-core-wcm-components/releases/latest) verwenden, die mit der Version von AEM kompatibel sind, die sie ausführen, um die aktuellsten Fehlerbehebungen und Funktionen zu nutzen.

### Komponentenversionen und -freigaben {#component-versions-and-releases}

Die folgende Tabelle zeigt, welche Versionen welcher Komponenten in welchen Freigaben der Kernkomponenten enthalten sind.

|  | Freigabe 1.0.0 - 1.0.6 | Freigabe 1.1.0 | Freigabe 2.0.0 - 2.0.8 | Freigabe 2.1.0 | Freigabe 2.2.0 - 2.2.0 | Freigabe 2.3.0 - 2.3.2 | Freigabe 2.4.0 | Freigabe 2.5.0 | Freigabe 2.6.0 | Freigabe 2.7.0+ |
|---|---|---|---|---|---|---|---|---|---|---|
| **[Seite](page.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Titel](title.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Bild](image.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Liste](list.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Breadcrumb](breadcrumb.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Freigabe in Social Media](sharing.md)** | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Formular-Container](form-container.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Formulartext](form-text.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Formularoptionen](form-options.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Ausgeblendetes Formular](form-hidden.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Formularschaltfläche](form-button.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Inhaltsfragment](content-fragment-component.md)** |  | Sandbox | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Navigation](navigation.md)** |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Sprachnavigation](language-navigation.md)** |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Schnellsuche](quick-search.md)** |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Teaser](teaser.md)** |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Registerkarten](tabs.md)** |  |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Karussell](carousel.md)** |  |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Trennzeichen](separator.md)** |  |  |  |  |  | v1 | v1 | v1 | v1 | v1 |
| **[Inhaltsfragmentliste](content-fragment-list.md)** |  |  |  |  |  |  | v1 | v1 | v1 | v1 |
| **[Akkordeon](accordion.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 |
| **[Schaltfläche](button.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 |
| **[Container](separator.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 |
| **[Download](separator.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 |
| **[Experience Fragment](separator.md)** |  |  |  |  |  |  |  |  | v1 | v1 |
| **[Einbetten](separator.md)** |  |  |  |  |  |  |  |  |  | v1 |

## Dokumentation {#documentation}

[Authoring mit Kernkomponenten](authoring.md) beschreibt die Nutzung der Kernkomponenten und der Funktionen, die für Inhaltsautoren und Vorlagenautoren verfügbar sind. Jede Komponente wird detailliert dokumentiert.

[Komponentenbibliothek](http://opensource.adobe.com/aem-core-wcm-components/library.html) ist eine Präsentation der aktuellen Version der meisten Kernkomponenten und zeigt, wie sie verwendet werden können.

[Entwicklung von Kernkomponenten](developing.md) beschreibt die technischen Funktionen der Kernkomponenten, deren Verwendung in Ihren Projekten, die Anpassung und Best Practices.

[Einführung zu den Kernkomponenten](introduction.md) bietet eine Übersicht über die Kompatibilität der Kernkomponenten zwischen verschiedenen Versionen, Anwendungsfällen und Unterstützung.

Das [WKND-Tutorial](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html) ist eine hervorragende Einführung in die Entwicklung für AEM, einschließlich der Verwendung der Kernkomponenten.
