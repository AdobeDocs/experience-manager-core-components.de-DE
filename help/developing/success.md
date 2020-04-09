---
title: Pfade zum Erfolg mit den Kernkomponenten
description: Wie Sie erfolgreich sind, wenn Sie Ihr Projekt mit den Kernkomponenten implementieren
translation-type: tm+mt
source-git-commit: c338428a681f652d17bb972fb6a2abf216a338c3

---


# Pfade zum Erfolg mit den Kernkomponenten {#paths-to-success}

Die Kernkomponenten sind leistungsfähig, flexibel und einfach zu verwenden und anzupassen. Die Einhaltung der in diesem Dokument erläuterten Richtlinien stellt sicher, dass Ihr Projekt mit den Kernkomponenten erfolgreich ist.

## Zwei Erfolgspfade {#two-paths}

Es gibt zwei grundsätzliche Ansätze zur Umsetzung der Kernkomponenten, die zum Erfolg führen können, aber ihre eigenen Kompromisse haben, die von Projekt zu Projekt in Betracht gezogen werden müssen.

1. Ordnen Sie Ihre Entwürfe den Hauptkomponenten zu und verwenden Sie den HTML-Code, den sie bereitstellen. Oder
1. Wenn Sie bereits definierte HTML-Standards einhalten müssen, benötigen Sie mehr Aufwand und nicht alle Vorteile der Kernkomponenten.

## Häufige Fallstricke in der Komponentenimplementierung {#common-pitfalls}

Zwei häufig auftretende Probleme, die dazu führen, dass Projekte mit Kernkomponenten nicht erfolgreich sind, sind:

* **Fertige Designs** - Diese können sogar auf C-Level genehmigt werden und werden an das Entwicklungsteam übergeben, um pixelgenau zu implementieren, ohne dass die zugrunde liegende Technologie betroffen ist.
* **Eine Firma-weite HTML-Stilführung** - Auf solche Handbücher müssen allzu oft dogmatisch die Komponenten folgen, die Stile von oben nach unten anwenden.

In beiden Fällen sind die Anforderungen an die Komponenten so eng und spezifisch, dass es schwierig ist, die Kernkomponenten oder alle vordefinierten Komponenten einzuhalten, was zu einer massiven Entwicklung von kundenspezifischen Komponenten führt.

## Beginn früh {#start-early}

Anstatt die Kernkomponenten nur in der Implementierungsphase Ihres Projekts zu berücksichtigen, sollten Sie bereits während der Wireframing- und Entwurfsphase mit den Kernkomponenten Beginn machen.

### Komponentenbibliothek verwenden {#component-library}

Verweisen Sie auf die [Komponentenbibliothek](https://adobe.com/go/aem_cmp_library) , die sich bereits in der Entwurfsphase befindet. Die Kernkomponenten sind leistungsfähig und flexibel und können Sie als Ausgangspunkt nehmen. Fügen Sie nur benutzerdefinierte Komponenten hinzu, wenn eine echte geschäftliche Notwendigkeit besteht, die mit einer Core-Komponente wirklich nicht erreicht werden kann.

### Verwenden des UI-Kits für Adobe XD {#ui-kit}

Sobald eine benutzerdefinierte Komponente nachweislich benötigt wird, verwenden Sie das [UI-Kit für Adobe XD](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/assets/overview/AEM_UI-kit_Wireframe.xd) , damit die Designer Beginn beim Erstellen der Wireframes und der Entwürfe mit den Core-Komponenten als Bausteine erstellen können.

## Leistungsstarke Funktionen nicht übersehen {#powerful-features}

Funktionen von AEM und den Core-Komponenten können sehr leistungsstark, aber auch sehr subtil sein, und die Möglichkeiten für bestimmte Funktionen sind für einen Designer möglicherweise nicht sofort sichtbar.

### Inhaltsfragmente {#content-fragments}

[Inhaltsfragmente ermöglichen es Ihnen, kanalneutrale Inhalte zusammen mit (möglicherweise kanalspezifischen) Varianten zu erstellen. ](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/content-fragments.html) Sie können diese Fragmente und ihre Varianten bei der Erstellung Ihrer Inhaltsseiten verwenden.

In Verbindung mit dem aktualisierten JSON Exporter können strukturierte Inhaltsfragmente auch verwendet werden, um AEM-Inhalte über Content Services anderen Kanälen als AEM-Seiten bereitzustellen.

### Erlebnisfragmentvorlagen {#experience-fragment-templates}

Wenn ein Autor Teile (ein Fragment eines Erlebnisses) einer Seite wiederverwenden möchte. Ohne [Erlebnisfragmente muss der Autor dieses Fragment kopieren und einfügen,](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/experience-fragments.html) um es zu erstellen. Das Erstellen und Verwalten dieser zum Kopieren/Einfügen vorgesehenen Erlebnisse sind zeitaufwendige und fehleranfällige Verfahren. Mit Experience Fragments ersparen Sie sich das Kopieren/Einfügen.

### Die Einbettungskomponente {#embed-component}

[Die Einbettungskomponente](/help/components/embed.md) ermöglicht nicht nur die einfache Einbindung externer Ressourcen wie YouTube-Videoinhalte, sondern ist auch erweiterbar, damit sie für spezifische Inhalte eines Projekts geeignet ist.