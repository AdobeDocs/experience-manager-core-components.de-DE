---
title: Hauptkomponenten-Versionen
seo-title: Hauptkomponenten-Versionen
description: Core-Komponenten werden als Versionen veröffentlicht, die mehr als eine Version derselben Kernkomponenten enthalten. In diesem Dokument wird erläutert, welche Versionen und Versionen veröffentlicht werden und wie die Kompatibilität mit Kernkomponenten und AEM verstanden wird.
seo-description: Core-Komponenten werden als Versionen veröffentlicht, die mehr als eine Version derselben Kernkomponenten enthalten. In diesem Dokument wird erläutert, welche Versionen und Versionen veröffentlicht werden und wie die Kompatibilität mit Kernkomponenten und AEM verstanden wird.
uuid: a 916 a 923-8 c 5 e -456 a -84 b 5-b 52228 e 21434
contentOwner: Benutzer
content-type: Referenz
topic-tags: Einführung
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-new
discoiquuid: a 3 a 98 b 2 f -65 bf -4493-82 ad -1717938 fdbc
translation-type: tm+mt
source-git-commit: 1bbec9b1f109df88964dce051a58d111bf6cafaa

---


# Hauptkomponenten-Versionen{#core-components-versions}

Die aktuelle Version der Kernkomponenten ist 2.4.0 und ist mit AEM 6.5 kompatibel. Es wurde im Mai 2019 als kleinere Aktualisierung an Version 2.0.0 veröffentlicht. Mit Version 2.0.0 wurden neue Komponenten zusammen mit Version 2 der vorhandenen Komponenten eingeführt.

Weitere Informationen finden Sie im Abschnitt [Versionsverlauf und Kompatibilität](#versions-and-releases) dieses Dokuments.

Sie können auch die [Komponentenbibliothek](http://opensource.adobe.com/aem-core-wcm-components/library.html)auschecken, in der die aktuelle Version der Kernkomponenten präsentiert wird, und Beispiele für ihre Verwendung eingeben.

## Versionen und Versionen {#versions-and-releases}

Kernkomponenten werden über github verteilt. Dadurch kann Adobe den Komponenten schneller Funktionen hinzufügen und die Community-Eingabe außerhalb des AEM-Versionszyklus zulassen.

Die Kernkomponenten werden mit definierten AEM-Versionen bereitgestellt, mit denen sie kompatibel sind. Dies bedeutet, dass eine AEM-Version mehrere Versionen oder Versionen der Kernkomponenten unterstützt. Dies bietet mehr Flexibilität als die früheren Foundation-Komponenten, die an eine bestimmte Version von AEM gebunden waren.

### Versionen {#versions}

Die Hauptiteration der Kernkomponenten sind die **Versionen**. Jede Komponente hat eine Version. Versionen werden mit **dem Zusatz v** angehängt, der eine nicht null, positive Ganzzahl wie v 1 und v 2 angehängt hat. Versionen werden nur für Änderungen inkrementiert, die nicht abwärtskompatibel sind. Dies gilt normalerweise für die Einführung neuer Funktionen und Funktionen.

Entwickler und Administratoren können Versionen der Kernkomponenten anhand einer Zahl in ihren Ressourcentyppfaden und in den vollständig qualifizierten Java-Klassennamen ihrer Implementierungen erkennen. Diese Versionsnummer stellt eine Hauptversion dar, die durch [semantische Versionshinweise definiert](https://semver.org/)wird.

Weitere Informationen zu Core-Komponentenversionen finden Sie in der [Entwicklerdokumentation der Kernkomponenten](guidelines.md).

### Versionen {#releases}

Die Kernkomponenten werden über **Versionen bereitgestellt** und [stellen die tatsächlichen veröffentlichten Artefakte dar](https://github.com/adobe/aem-core-wcm-components/releases), die auf github verfügbar sind. Versionen werden mit einer Dezimalzahl im Format X.Y.Z gekennzeichnet und alle Kernkomponenten werden zusammen als bereitstellbares Paket erfasst.

* **Hauptversionen** können neue Versionen vorhandener Komponenten sowie völlig neue Komponenten sowie Standardfehlerbehebungen einführen. Dies wird durch eine Inkrementierung der X-Komponente der Versionsnummer dargestellt.

* **Wichtige Versionen** können neue Funktionen für vorhandene Versionen von Komponenten zusammen mit Fehlerbehebungen einführen. Dies wird durch eine Inkrementierung der Y-Komponente der Versionsnummer dargestellt.

* **Nebenversionen** enthalten nur Fehlerkorrekturen. Dies wird durch eine Inkrementierung der Z-Komponente der Versionsnummer dargestellt.

>[!NOTE]
>
>Versionen können mehrere Versionen derselben Komponente enthalten.
>
>Dieselbe Version einer Komponente kann in mehreren Versionen angezeigt werden.

## Versionsverlauf und Kompatibilität {#release-history-and-compatibility}

Die Kernkomponenten wurden zuerst mit AEM 6.3 veröffentlicht und sind so ausgelegt, dass sie flexibel und mit allen unterstützten AEM-Versionen kompatibel sind. Daher kann eine Version der Komponenten mehrere Versionen derselben Komponente enthalten.

Die folgenden Tabellen zeigen die Kompatibilität der Versionen der Kernkomponenten mit den Komponentenversionen, in denen Versionen enthalten sind.

### Versionsverlauf und unterstützte AEM-Versionen {#release-history-supported-aem-versions}

Die folgende Tabelle, deren Inhalt auf github mit vollständigen Versionshinweisen [](https://github.com/adobe/aem-core-wcm-components/releases)verfügbar ist, bietet einen Überblick über die Versionen der Kernkomponenten und deren Kompatibilität mit AEM-Versionen und Java-Versionen.

| Version | Beschreibung | AEM 6.3 | AEM 6.4 | AEM 6.5 | Java |
|---|---|---|---|---|---|
| [2.4.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.4.0) | Mit dieser Version wurde die Komponente &quot;Inhaltsfragment&quot; eingeführt. | 6.3.3.0 | 6.4.2.0 | 6.5.0.0 | 1.8 |
| [2.3.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.3.2) | Diese Version konzentriert sich auf Verfeinerungen in der Komponentenbibliothek, enthält aber auch einige Funktionsverbesserungen für die Trennzeichenkomponente. | 6.3.3.0 | 6.4.2.0 | 6.5.0.0 | 1.8 |
| [2.3.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.3.0) | Diese Version konzentriert sich sowohl auf die Komponentenbibliothek als auch auf die neue Trennzeichenkomponente, enthält jedoch einige Funktionsverbesserungen für die Image-Komponente. | 6.3.3.0 | 6.4.2.0 | - | 1.8 |
| [2.2.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.2.2) | Diese Version konzentriert sich hauptsächlich auf Fehlerbehebungen, enthält aber auch einige Funktionsverbesserungen für die Karussellkomponente. | 6.3.3.0 | 6.4.2.0 | - | 1.8 |
| [2.2.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.2.0) | Tabulatoren und Karussell-Komponenten, Verbesserungen der Bild-, Seiten- und Titelkomponenten und verbesserte Verfolgung | 6.3.3.0 | 6.4.2.0 | - | 1.8 |
| [2.1.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.1.0) | Teaser-Komponente, verbesserte Bildkomponentenverbesserungen und zahlreiche Fehlerkorrekturen | 6.3.3.0 | 6.4.2.0 | 1.8 |
| [2.0.8](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.8) | Bugfix-Version | 6.3.2.0 | 6.4.0.0 | - | 1.8 |
| [2.0.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.6) | Zusätzliche Verbesserungen unter den Verbesserungen, Fehlerbehebungen und kleinere Verbesserungen, einschließlich Unterstützung für das Spiegeln von Bildern. | 6.3.2.0 | 6.4.0.0 | - | 1.8 |
| [2.0.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.4) | Meist unter-the-Hood Verbesserungen, Fehlerbehebungen und einige kleinere Verbesserungen der Bild-, Seiten- und Inhaltsfragmente | 6.3.2.0 | 6.4.0.0 | - | 1.8 |
| [2.0.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.0) | Navigation, Sprachnavigation und Schnellsuche wurden eingeführt. Für alle Komponenten implementiertes Stilsystem. | 6.3.2.0 | 6.4.0.0 | - | 1.8 |
| [1.1.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.1.0) | Implementierung des JSON-Exports für alle Komponenten, Einführung in die Komponente &quot;Content Fragment « | 6.3.1.0 | 6.4.0.0 | 1.8 |
| [1.0.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.6) | Mehrere Fehlerbehebungen für die Image-Komponente | 6.3.0.0 | 6.4.0.0 | - | 1.8 |
| [1.0.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.4) | Fehlerbehebungen der Seitenkomponente, der Bildkomponente, verschiedener globaler Korrekturen und Verbesserungen | 6.3.0.0 | 6.4.0.0 | - | 1.8 |
| [1.0.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.all-1.0.2) | Korrekturen für animierte GIF-Bilder in der Image-Komponente | 6.3.0.0 | 6.4.0.0 | - | 1.7 |
| [1.0.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.0) | Erste Version der Kernkomponenten | 6.3.0.0 | 6.4.0.0 | - | 1.7 |

>[!NOTE]
>
>Wie bei AEM empfiehlt Adobe, dass Entwickler die [neueste Version und Versionen der verfügbaren Kernkomponenten](https://github.com/adobe/aem-core-wcm-components/releases/latest) verwenden, die mit der Version von AEM kompatibel sind, die sie ausführen, um die aktuellsten Fehlerbehebungen und Funktionen nutzen zu können.

### Komponentenversionen und Releases {component-versions-and-releases}

Die folgende Tabelle zeigt, welche Versionen von Komponenten in welchen Versionen der Kernkomponenten enthalten sind.

|  | Version 1.0.0 - 1.0.6 | Version 1.1.0 | Version 2.0.0 - 2.0.8 | Version 2.1.0 | Version 2.2.-2.2.0 | 2.3.0 |
|---|---|---|---|---|---|---|
| **[Page](page.md)** | v1 | v1 | v 1, v 2 | v 1, v 2 | v 1, v 2 | v 1, v 2 |
| **[Titel](title.md)** | v1 | v1 | v 1, v 2 | v 1, v 2 | v 1, v 2 | v 1, v 2 |
| **[Bild](image.md)** | v1 | v1 | v 1, v 2 | v 1, v 2 | v 1, v 2 | v 1, v 2 |
| **[Liste](list.md)** | v1 | v1 | v 1, v 2 | v 1, v 2 | v 1, v 2 | v 1, v 2 |
| **[Breadcrumb](breadcrumb.md)** | v1 | v1 | v 1, v 2 | v 1, v 2 | v 1, v 2 | v 1, v 2 |
| **[Freigabe in Social Media](sharing.md)** | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Formular-Container](form-container.md)** | v1 | v1 | v 1, v 2 | v 1, v 2 | v 1, v 2 | v 1, v 2 |
| **[Formulartext](form-text.md)** | v1 | v1 | v 1, v 2 | v 1, v 2 | v 1, v 2 | v 1, v 2 |
| **[Formularoptionen](form-options.md)** | v1 | v1 | v 1, v 2 | v 1, v 2 | v 1, v 2 | v 1, v 2 |
| **[Ausgeblendetes Formular](form-hidden.md)** | v1 | v1 | v 1, v 2 | v 1, v 2 | v 1, v 2 | v 1, v 2 |
| **[Formularschaltfläche](form-button.md)** | v1 | v1 | v 1, v 2 | v 1, v 2 | v 1, v 2 | v 1, v 2 |
| **[Inhaltsfragmente](content-fragment-component.md)** | Sandbox | v1 | v1 | v1 | v1 |
| **[Navigation](navigation.md)** | v1 | v1 | v1 | v1 |
| **[Sprachnavigation](language-navigation.md)** | v1 | v1 | v1 | v1 |
| **[Schnellsuche](quick-search.md)** | v1 | v1 | v1 | v1 |
| **[Teaser](teaser.md)** | v1 | v1 | v1 |
| **[Registerkarten](tabs.md)** | v1 | v1 |
| **[Karussell](carousel.md)** | v1 | v1 |
| **[Trennzeichen](separator.md)** | v1 |

## Dokumentation {#documentation}

[Das Authoring mit Core-Komponenten](authoring.md) beschreibt die Nutzung der Kernkomponenten und der Funktionen, die für Inhaltsautoren und Vorlagenautoren verfügbar sind. Jede Komponente wird detailliert dokumentiert.

[Die Komponentenbibliothek](http://opensource.adobe.com/aem-core-wcm-components/library.html) stellt die aktuelle Version der meisten Kernkomponenten dar und zeigt, wie sie verwendet werden können.

[Die Entwicklung von Kernkomponenten](developing.md) beschreibt die technischen Funktionen der Kernkomponenten, deren Verwendung in Ihren Projekten, die Anpassung und Best Practices.

[Core Components Introduction](introduction.md) bietet eine Übersicht über die Kompatibilität Kernkomponenten in verschiedenen Versionen, Anwendungsfällen und Support.
