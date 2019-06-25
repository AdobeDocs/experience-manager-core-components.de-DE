---
title: Einführung in Kernkomponenten
seo-title: Einführung in Kernkomponenten
description: 'Kernkomponenten wurden eingeführt, um robuste und erweiterbare Basiskomponenten bereitzustellen, die auf aktuellen Technologie und Best Practices basieren. '
seo-description: 'Kernkomponenten wurden eingeführt, um robuste und erweiterbare Basiskomponenten bereitzustellen, die auf aktuellen Technologie und Best Practices basieren. '
uuid: b 815 c 7 d 1-fbb 0-4480-bd 23-42606 ff 8 b 1 eb
contentOwner: Benutzer
content-type: Referenz
topic-tags: Einführung
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-new
discoiquuid: c 44 bb 0 d 7-5 d 91-4659-878 e-a 0658 fe 29 aa 2
translation-type: tm+mt
source-git-commit: 7130f4ae8add8c8dc3cdfcc4addd0621722b89f7

---


# Core Components Introduction{#core-components-introduction}

In Adobe Experience Manager sind Komponenten die strukturellen Elemente, aus denen der Inhalt von bearbeiteten Seiten besteht. Komponenten waren immer ein Grundelement des AEM-Erlebnisses, wodurch die Seitenerstellung einfach, aber für den Autor und die Entwicklung von Komponenten flexibel und erweiterbar ist.

Kernkomponenten wurden eingeführt, um robuste und erweiterbare Basiskomponenten bereitzustellen, auf der neuesten Technologie und Best Practices basieren und die Richtlinien zur Barrierefreiheit einhalten und mit dem WCAG 2.0 AA-Standard konform sind. Kernkomponenten ermöglichen die flexiblere und anpassbare Seitenbearbeitung und erweitern die benutzerdefinierten Funktionen für den Entwickler einfach.

## Testen der Kernkomponenten

If you want to get started straight away trying out the Core Components, head over to the [Component Library](http://opensource.adobe.com/aem-core-wcm-components/library.html). Die Komponentenbibliothek ist ein Online-Showcase der aktuellen Version der Hauptkomponenten, mit dem Sie mit Variationen der Komponenten interagieren und die HTML- und JSON-Beispielausgabe sehen können.

The [We.Retail reference site](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html) also illustrates how the core components can be used.

## Core Components - Core Features {#core-components-core-features}

Die Kernkomponenten sind:

|  |  |
|--- |--- |
| Vorkonfigurierbar | Vorlagen können definieren, wie die Seitenautoren sie verwenden können. |
| Vielseitig | Autoren können die meisten Inhaltstypen erstellen. |
| Einfach zu verwenden | Autoren können Inhalte effizient erstellen und verwalten. |
| Produktionsbereit | Einsatzbereit! Sie sind robust, gut getestet und funktionieren gut. |
| Accessible | Sie erfüllen WCAG 2.0-Standards, geben ARIA-Beschriftungen an und unterstützen Tastaturnavigation. |
| Einfach zu formatieren | Die Komponenten implementieren das Stilsystem und die Markierung folgt BEM CSS-Benennung. |
| SEO-freundlich | Die HTML-Ausgabe ist semantisch und stellt schema.org microdata anmerkungen bereit. |
| PWA/SPA/App Ready | Die optimierte JSON-Ausgabe kann auch für die clientseitige Wiedergabe verwendet werden. |
| Erweiterbar | Um benutzerdefinierte Anforderungen zu behandeln, ohne komplett neu beginnen zu müssen, können Sie alles erweitern. |
| Open Source | Wenn etwas nicht so wie nötig sein sollte, tragen Sie zu github (Apache-Lizenz) bei. |
| Versionierung | Die Kernkomponenten brechen Ihre Site nicht auf, wenn Sie Dinge verbessern, die sich möglicherweise auf Sie auswirken. |

## Available Components {#available-components}

Die aktuelle Version der Kernkomponenten enthält die folgenden Komponenten.

* [Akkordion](accordion.md)
* [Breadcrumb](breadcrumb.md)
* [Schaltfläche](button.md)
* [Container](container.md)
* [Karussell](carousel.md)
* [Inhaltsfragment](content-fragment-component.md)
* [Inhaltsfragmentliste](content-fragment-list.md)
* [Herunterladen](download.md)
* [Formularschaltfläche](form-button.md)
* [Formular-Container](form-container.md)
* [Ausgeblendetes Formular](form-hidden.md)
* [Formularoptionen](form-options.md)
* [Formulartext](form-text.md)
* [Bild](image.md)
* [Sprachnavigation](language-navigation.md)
* [Liste](list.md)
* [Navigation](navigation.md)
* [Page](page.md)
* [Schnellsuche](quick-search.md)
* [Trennzeichen](separator.md)
* [Freigabe in Social Media](sharing.md)
* [Registerkarten](tabs.md)
* [Text](text.md)
* [Titel](title.md)

>[!NOTE]
>
>Core Components are not immediately available to authors, the [development team must first integrate them to your environment](using.md). Once integrated, they may be made available and pre-configured via the [template editor](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html) or in [design mode](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/default-components-designmode.html).

>[!CAUTION]
>
>Einige Versionen einzelner Kernkomponenten sind möglicherweise nur mit bestimmten Versionen von AEM kompatibel.
>
>See the individual help page (linked to in the previous list) for the specific component for compatibility information or reference the [Core Components Versions](versions.md) document for more information.

## When to Use Core Components {#when-to-use-core-components}

Da die Kernkomponenten völlig neu sind und mehrere Vorteile bieten, sollten Sie für neue AEM-Projekte verwendet werden. Bei vorhandenen Projekten sollte eine Migration Teil eines größeren Projekts sein, z. B. ein Rebranding oder eine Gesamtrefaktorierung.

For specific use recommendations, see [When to Use the Core Components?](developing.md) im Dokument [Entwicklung Kernkomponenten](developing.md) .

## Gems Session Overview {#gems-session-overview}

For an introduction to the Core Components, the features they offer, and how they are leveraged in AEM, check out the AEM Gems Session [AEM Core Components.](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/AEM-Core-Components.html)

[Gems on Adobe Experience Manager](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/aem-index.html) ist eine Reihe von technischen Tiefstellungen von Adobe-Experten. Diese Reihe ergänzt die Produktdokumentation und alle anderen technischen Kanäle und ermöglicht es Entwicklern, Kontakt zu erhalten und ein bestimmtes Thema tief zu betrachten.

## WKND Developer Tutorial {#wknd-developer-tutorial}

Get started developing AEM Sites with Core Components by following [this step by step tutorial.](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/getting-started.html)

## Core Components Support {#core-components-support}

Core-Komponenten sind ein wesentlicher Bestandteil von AEM und unterstützen wie vorliegend unter denselben Bedingungen, wie sie als Teil des Quickstart bereitgestellt wurden.

Wie andere Produktmerkmale gilt auch für das Ende der Lebensdauer Folgendes:

* Komponenten werden zuerst als veraltet angekündigt, bevor sie entfernt werden.
* Frühestens werden sie aus der AEM-Version entfernt, die nach der Mitteilung bekannt ist.

Dadurch erhalten Kunden mindestens einen Versionszyklus, um zur neuen Version der Komponente zu wechseln, bevor die Unterstützung endet.

Die Version der einzelnen Komponenten stellt klar die von dieser Version unterstützten AEM-Versionen dar. Wenn Support-Argumente für eine Version von AEM verfügbar sind, dann wird die Unterstützung der Kernkomponenten für diese Version von AEM unterstützt.

For details about the support of component customizations, see the [Customizing Core Components](customizing.md) page of the relevant Core Components Version.

## Foundation Component Support {#foundation-component-support}

Da die Foundation-Komponenten aufgrund vieler Versionen als Grundlage für so viele Projekte bereitgestellt wurden, werden sie in absehbarer Zukunft weiterhin unterstützt.

However, Adobe&#39;s development emphasis has shifted to the Core Components and new features will be added to them, whereas [nearly all Foundation Components have been deprecated with AEM 6.5](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/default-components-foundation.html) and only bug fixes will be made to the Foundation Components going forward.
