---
title: Einführung in Kernkomponenten
seo-title: Einführung in Kernkomponenten
description: 'Kernkomponenten wurden eingeführt, um robuste und erweiterbare Basiskomponenten bereitzustellen, die auf aktueller Technologie und Best Practices basieren. '
seo-description: 'Kernkomponenten wurden eingeführt, um robuste und erweiterbare Basiskomponenten bereitzustellen, die auf aktueller Technologie und Best Practices basieren. '
uuid: b815c7d1-fbb0-4480-bd23-42606ff8b1eb
contentOwner: Benutzer
content-type: Referenz
topic-tags: Einführung
products: SG_EXPERIENCEMANAGER/CORECOMPONENTS-new
discoiquuid: c44bb0d7-5d91-4659-878e-a0658fe29aa2
translation-type: ht
source-git-commit: 7130f4ae8add8c8dc3cdfcc4addd0621722b89f7

---


# Einführung in Kernkomponenten{#core-components-introduction}

In Adobe Experience Manager sind Komponenten die strukturellen Elemente, aus denen der Inhalt von bearbeiteten Seiten besteht. Komponenten waren immer ein Grundelement des AEM-Erlebnisses, wodurch die Seitenerstellung einfach, aber für den Autor und die Entwicklung von Komponenten flexibel und erweiterbar ist.

Kernkomponenten wurden eingeführt, um stabile und erweiterbare Basiskomponenten bereitzustellen, auf der neuesten Technologie und Best Practices basieren und die Richtlinien zur Barrierefreiheit einhalten sowie mit dem WCAG 2.0 AA-Standard konform sind. Kernkomponenten machen die Seitenerstellung flexibler und anpassbarer. Die Erweiterung auf benutzerdefinierte Funktionen ist für den Entwickler einfach.

## Testen der Kernkomponenten

Wenn Sie sofort anfangen möchten, die Kernkomponenten auszuprobieren, wechseln Sie zur [Komponentenbibliothek](http://opensource.adobe.com/aem-core-wcm-components/library.html). Die Komponentenbibliothek ist eine Online-Präsentation der aktuellen Version der meisten Kernkomponenten, mit der Sie mit Variationen der Komponenten interagieren und Beispiele von HTML- und JSON-Ausgaben anzeigen können.

Die [„We.Retail“ Referenz-Site](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html) zeigt außerdem, wie die Kernkomponenten verwendet werden können.

## Kernkomponenten - Kernfunktionen {#core-components-core-features}

Die Kernkomponenten sind:

|  |  |
|--- |--- |
| Vorkonfigurierbar | Vorlagen können definieren, wie die Seitenautoren sie verwenden können. |
| Vielseitig | Autoren können die meisten Inhaltstypen erstellen. |
| Einfach zu verwenden | Autoren können Inhalte effizient erstellen und verwalten. |
| Produktionsbereit | Sofort einsatzbereit! Sie sind stabil, gut getestet und funktionieren gut. |
| Barrierefrei | Sie erfüllen WCAG 2.0-Standards, geben ARIA-Beschriftungen an und unterstützen Tastaturnavigation. |
| Einfach zu formatieren | Die Komponenten implementieren das Stilsystem und die Markierung folgt der BEM-CSS-Benennung. |
| SEO-freundlich | Die HTML-Ausgabe ist semantisch und stellt schema.org Mikrodatenanmerkungen bereit. |
| Sofort einsatzbereit für PWA/SPA/App | Die optimierte JSON-Ausgabe kann auch für die Client-seitige Wiedergabe verwendet werden. |
| Erweiterbar | Um benutzerdefinierte Anforderungen zu behandeln, ohne komplett neu beginnen zu müssen, können Sie alles erweitern. |
| Open Source | Wenn etwas nicht so ist, wie es sein sollte, können Sie auf GitHub (Apache License) Verbesserungsvorschläge einreichen. |
| Versionierung | Die Kernkomponenten werden Ihre Website nicht beschädigen, wenn Sie Dinge verbessern, die sich möglicherweise auf Sie auswirken. |

## Verfügbare Komponenten {#available-components}

Die aktuelle Version der Kernkomponenten enthält die folgenden Komponenten.

* [Akkordeon](accordion.md)
* [Breadcrumb](breadcrumb.md)
* [Schaltfläche](button.md)
* [Container](container.md)
* [Karussell](carousel.md)
* [Inhaltsfragment](content-fragment-component.md)
* [Inhaltsfragmentliste](content-fragment-list.md)
* [Download](download.md)
* [Formularschaltfläche](form-button.md)
* [Formular-Container](form-container.md)
* [Ausgeblendetes Formular](form-hidden.md)
* [Formularoptionen](form-options.md)
* [Formulartext](form-text.md)
* [Bild](image.md)
* [Sprachnavigation](language-navigation.md)
* [Liste](list.md)
* [Navigation](navigation.md)
* [Seite](page.md)
* [Schnellsuche](quick-search.md)
* [Trennzeichen](separator.md)
* [Freigabe in Social Media](sharing.md)
* [Registerkarten](tabs.md)
* [Text](text.md)
* [Titel](title.md)

>[!NOTE]
>
>Kernkomponenten sind für Autoren nicht sofort verfügbar. Das [Entwicklerteam muss sie zuerst in Ihre Umgebung integrieren](using.md). Nach der Integration können sie über den [Vorlagen-Editor](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html) oder im [Entwurfsmodus](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/default-components-designmode.html) bereitgestellt und vorkonfiguriert werden.

>[!CAUTION]
>
>Einige Versionen einzelner Kernkomponenten sind möglicherweise nur mit bestimmten Versionen von AEM kompatibel.
>
>Weitere Informationen zu Kompatibilitätsinformationen finden Sie auf der Hilfeseite für die jeweilige Komponente (Links in der vorherigen Liste) oder im Dokument [Kernkomponentenversionen](versions.md).

## Wann Kernkomponenten zu verwenden sind {#when-to-use-core-components}

Da die Kernkomponenten völlig neu sind und mehrere Vorteile bieten, wird empfohlen, sie für neue AEM-Projekte zu verwenden. Bei vorhandenen Projekten sollte eine Migration Teil einer größeren Projektaufgabe sein, z. B. ein Rebranding oder eine Gesamtrefaktorierung.

Informationen zu spezifischen Empfehlungen der Nutzung finden Sie unter [Wann Kernkomponenten zu verwenden sind.](developing.md) im Dokument [Entwicklung von Kernkomponenten](developing.md) .

## Überblick über die Gems-Sitzung {#gems-session-overview}

Um eine Einführung in die Kernkomponenten, die angebotenen Funktionen und ihre Nutzung in AEM zu erhalten, sehen Sie sich die AEM-Gems-Sitzung [AEM-Kernkomponenten](https://helpx.adobe.com/de/experience-manager/de/eseminars/gems/AEM-Core-Components.html) an.

[Gems zu Adobe Experience Manager](https://helpx.adobe.com/experience-manager/de/eseminars/gems/aem-index.html) ist eine Reihe technischer Vertiefungen, die von Adobe-Experten angeboten werden. Diese Reihe ergänzt die Produktdokumentation und alle anderen technischen Kanäle und ermöglicht es Entwicklern, in Kontakt zu treten und ein bestimmtes Thema zu vertiefen.

## WKND-Entwickler-Tutorial {#wknd-developer-tutorial}

Beginnen Sie mit der Entwicklung von AEM Sites mit Kernkomponenten, indem Sie [dieses Tutorial schrittweise befolgen.](https://helpx.adobe.com/de/experience-manager/6-5/sites/developing/using/getting-started.html) befolgen.

## Support für Kernkomponenten {#core-components-support}

Kernkomponenten sind ein integraler Bestandteil von AEM und werden ohne Mängelgewähr unterstützt, zu den gleichen Bedingungen und Konditionen, als ob sie im Rahmen des Quickstarts geliefert würden.

Wie bei anderen Produktmerkmalen gilt für das Ende der Lebensdauer die allgemeine Regel:

* Komponenten werden zuerst als veraltet angekündigt, bevor sie entfernt werden.
* Sie werden dann frühestens nach Ankündigung aus dem AEM-Release entfernt.

Dadurch erhalten Kunden mindestens einen Versionszyklus, um zur neuen Version der Komponente zu wechseln, bevor die Unterstützung endet.

Die Version jeder Komponente gibt eindeutig die AEM-Versionen an, die sie unterstützt. Wenn der Support für eine Version von AEM eingestellt wird, gilt das auch für die Unterstützung der Kernkomponenten für diese Version von AEM.

Weitere Informationen zum Support von Komponentenanpassungen finden Sie auf der Seite [Anpassen von Kernkomponenten](customizing.md) der entsprechenden Kernkomponentenversion.

## Unterstützung von Foundation-Komponenten {#foundation-component-support}

Da die Foundation-Komponenten aufgrund vieler Versionen als Grundlage für so viele Projekte bereitgestellt wurden, werden sie in absehbarer Zukunft weiterhin unterstützt.

Der Entwicklungsschwerpunkt von Adobe wurde jedoch auf die Kernkomponenten verschoben, und neue Funktionen werden zu ihnen hinzugefügt, während [fast alle Foundation-Komponenten mit AEM 6.5 als veraltet gelten](https://helpx.adobe.com/de/experience-manager/6-5/sites/authoring/using/default-components-foundation.html) und jetzt nur noch Fehlerkorrekturen an den Foundation-Komponenten vorgenommen werden.
