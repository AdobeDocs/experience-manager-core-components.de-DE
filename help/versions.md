---
title: Kernkomponenten-Versionen
description: Kernkomponenten werden als Versionen veröffentlicht, die mehr als eine Version derselben Kernkomponenten enthalten können. In diesem Dokument wird erläutert, welche Versionen veröffentlicht werden und wie die Kompatibilität mit Kernkomponenten und AEM verstanden werden kann.
translation-type: ht
source-git-commit: 3136a82a0b523e13227def893d516017873f4365
workflow-type: ht
source-wordcount: '1735'
ht-degree: 100%

---


# Kernkomponenten-Versionen {#core-components-versions}

Die aktuelle Version der Kernkomponenten ist 2.11.0 und mit [AEM as a Cloud Service](https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/landing/home.translate.html)- und [lokalen AEM](https://docs.adobe.com/content/help/en/experience-manager-65/user-guide/home.html)-Installationen kompatibel. Diese Version wurde im Juli 2020 als wichtige Aktualisierung zu Version 2.0.0 veröffentlicht. In Version 2.0.0 wurden neue Komponenten sowie v2-Aktualisierungen vorhandener Komponenten eingeführt.

## Versionsverlauf und Kompatibilität {#release-history-and-compatibility}

Die Kernkomponenten wurden zuerst mit AEM 6.3 veröffentlicht und sind so ausgelegt, dass sie flexibel und mit allen unterstützten AEM-Versionen kompatibel sind. Daher kann eine Version der Komponenten mehrere Versionen derselben Komponente enthalten.

Die folgenden Tabellen zeigen die Kompatibilität der Versionen der Kernkomponenten mit den Komponentenversionen an, in denen Versionen enthalten sind.

### Versionsverlauf und Anforderungen {#release-history-requirements}

Die folgende Tabelle, deren Inhalt [auf GitHub mit vollständigen Versionsinformationen](https://github.com/adobe/aem-core-wcm-components/releases) verfügbar ist, bietet einen Überblick über die Versionen der Kernkomponenten und deren Kompatibilität mit AEM-Versionen und Java-Versionen.

| Version | Beschreibung | AEM 6.3 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service | Java | Veröffentlichungsdatum |
|---|---|---|---|---|---|---|---|
| [2.11.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.11.0) | Mit dieser Version wurde AMP-Unterstützung eingeführt. | - | 6.4.8.1+ | 6.5.5.0+ | Kontinuierlich | 8, 11 | 20. Juli 2020 |
| [2.10.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.10.0) | Mit dieser Version wurde die neue PDF-Viewer-Komponente eingeführt. | - | 6.4.8.1+ | 6.5.5.0+ | Kontinuierlich | 8, 11 | 17. Juni 2020 |
| [2.9.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.9.0) | Die Version ermöglichte die Integration mit der Adobe Client-Datenschicht und führte die Fortschrittleistenkomponente ein. | - | 6.4.8.0+ | 6.5.4.0+ | Kontinuierlich | 8, 11 | 29. Mai 2020 |
| [2.8.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.8.0) | Diese Version konzentrierte sich auf Fehlerbehebungen mit kleinen Verbesserungen. | 6.3.3.4+ | 6.4.4.0+ | 6.5.0.0+ | Kontinuierlich | 8, 11 | 5. Dezember 2019 |
| [2.7.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.7.0) | Mit dieser Version wurde die neue Einbettungskomponente eingeführt. | 6.3.3.4+ | 6.4.4.0+ | 6.5.0.0+ | Kontinuierlich | 8, 11 | 25. September 2019 |
| [2.6.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.6.0) | Mit dieser Version wurde die neue Experience Fragment-Komponente eingeführt. | 6.3.3.4+ | 6.4.4.0+ | 6.5.0.0+ | Kontinuierlich | 8, 11 | 6. September 2019 |
| [2.5.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.5.0) | Mit dieser Version wurden die neuen Komponenten Accordion, Schaltfläche, Container und Download eingeführt. | 6.3.3.0+ | 6.4.2.0+ | 6.5.0.0+ | Kontinuierlich | 8, 11 | 25. Juni 2019 |
| [2.4.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.4.0) | Mit dieser Version wurde die Inhaltsfragmentlisten-Komponente eingeführt. | 6.3.3.0+ | 6.4.2.0+ | 6.5.0.0+ | Kontinuierlich | 8, 11 | 7. Mai 2019 |
| [2.3.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.3.2) | Diese Version konzentriert sich auf Verfeinerungen in der Komponentenbibliothek, enthält aber auch einige Funktionsverbesserungen für die Trennzeichenkomponente | 6.3.3.0+ | 6.4.2.0+ | 6.5.0.0+ | Kontinuierlich | 8 | 14. März 2019 |
| [2.3.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.3.0) | Diese Version konzentriert sich sowohl auf die Komponentenbibliothek als auch auf die Einführung der neuen Trennzeichenkomponente, enthält jedoch auch einige Funktionsverbesserungen für die Bild-Komponente. | 6.3.3.0+ | 6.4.2.0+ | - | - | 8 | 11. Februar 2019 |
| [2.2.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.2.2) | Diese Version konzentriert sich hauptsächlich auf Fehlerbehebungen, enthält aber auch einige Funktionsverbesserungen für die Karussell-Komponente. | 6.3.3.0+ | 6.4.2.0+ | - | - | 8 | 27. November 2018 |
| [2.2.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.2.0) | Registerkarten- und Karussell-Komponenten eingeführt, Verbesserungen der Bild-, Seiten- und Titelkomponenten und eine verbesserte Verfolgung | 6.3.3.0+ | 6.4.2.0+ | - | - | 8 | 16. Oktober 2018 |
| [2.1.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.1.0) | Teaser-Komponente eingeführt, Verbesserungen der Bildkomponente und zahlreiche Fehlerkorrekturen | 6.3.3.0+ | 6.4.2.0+ | - | - | 8 | 13. Juli 2018 |
| [2.0.8](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.8) | Version mit Fehlerkorrekturen | 6.3.2.0+ | 6.4.0.0+ | - | - | 8 | 12. Juni 2018 |
| [2.0.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.6) | Zusätzliche Hintergrundverbesserungen, Fehlerkorrekturen, und kleine Verbesserungen, einschließlich der Unterstützung von Image Flip. | 6.3.2.0+ | 6.4.0.0+ | - | - | 8 | 11. April 2018 |
| [2.0.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.4) | Meist Hintergrundverbesserungen, Fehlerbehebungen und einige kleinere Verbesserungen der Bild-, Seiten- und Inhaltsfragment-Komponenten | 6.3.2.0+ | 6.4.0.0+ | - | - | 8 | 7. März 2018 |
| [2.0.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.0) | Komponenten zur Navigation, Sprachnavigation und Schnellsuche wurden eingeführt. Für alle Komponenten implementiertes Stilsystem. | 6.3.2.0+ | 6.4.0.0+ | - | - | 8 | 16. Januar 2018 |
| [1.1.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.1.0) | Implementierung des JSON-Exports für alle Komponenten, Einführung der Inhaltsfragment-Komponente | 6.3.1.0 | 6.4.0.0+ | - | - | 8 | 10. Oktober 2017 |
| [1.0.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.6) | Mehrere Fehlerbehebungen für die Bildkomponente | 6.3.0.0+ | 6.4.0.0+ | - | - | 8 | 4. August 2017 |
| [1.0.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.4) | Fehlerbehebungen der Seitenkomponente, der Bildkomponente, verschiedene globale Korrekturen und Verbesserungen | 6.3.0.0+ | 6.4.0.0+ | - | - | 8 | 26. April 2017 |
| [1.0.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.all-1.0.2) | Korrekturen für animierte GIF-Bilder in der Bildkomponente | 6.3.0.0+ | 6.4.0.0+ | - | - | 7 | 22. März 2017 |
| [1.0.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.0) | Erstmalige Freigabe von Kernkomponenten | 6.3.0.0+ | 6.4.0.0+ | - | - | 7 | 20. März 2017 |

>[!NOTE]
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

Da die Foundation-Komponenten aufgrund vieler Versionen als Grundlage für so viele Projekte bereitgestellt wurden, werden sie in absehbarer Zukunft weiterhin unterstützt.

Der Entwicklungsschwerpunkt von Adobe wurde jedoch auf die Kernkomponenten verschoben, und neue Funktionen werden zu ihnen hinzugefügt, während [fast alle Foundation-Komponenten mit AEM 6.5 als veraltet gelten](https://docs.adobe.com/content/help/de-DE/experience-manager-65/authoring/siteandpage/default-components-foundation.html) und jetzt nur noch Fehlerkorrekturen an den Foundation-Komponenten vorgenommen werden.
