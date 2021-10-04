---
title: Wege zum Erfolg mit den Kernkomponenten
description: So implementieren Sie Ihr Projekt erfolgreich mit den Kernkomponenten
role: Architect, Developer, Admin, User
exl-id: 1ea8cd1c-8435-4ded-82dc-5a7896c53e0c
source-git-commit: 888719359f9a1d1c9dccff97fb639b332f2be54c
workflow-type: tm+mt
source-wordcount: '560'
ht-degree: 97%

---

# Wege zum Erfolg mit den Kernkomponenten {#paths-to-success}

Die Kernkomponenten sind leistungsstark, flexibel und einfach zu verwenden und anzupassen. Die Einhaltung von wichtigen, in diesem Dokument dargelegten Richtlinien stellt sicher, dass Ihr Projekt mit den Kernkomponenten erfolgreich ist.

## Zwei Wege zum Erfolg {#two-paths}

Es gibt zwei grundsätzliche Ansätze zur Implementierung der Kernkomponenten, die zum Erfolg führen können. Diese weisen jedoch ihre eigenen Kompromisse auf, die von Projekt zu Projekt berücksichtigt werden müssen.

1. Ordnen Sie Ihre Designs den Kernkomponenten zu und verwenden Sie den von ihnen bereitgestellten HTML-Code. Oder
1. Wenn Sie bereits definierte HTML-Standards einhalten müssen, erfordert die Implementierung mehr Aufwand und Sie können nicht alle Vorteile der Kernkomponenten nutzen.

## Häufig auftretende Probleme bei der Implementierung der Komponenten {#common-pitfalls}

Zwei häufig auftretende Probleme, die dazu führen, dass Projekte mit Kernkomponenten nicht erfolgreich sind, sind:

* **Endgültige Designs** – Diese werden auf Führungsebene genehmigt und dem Entwicklungs-Team zur pixelgenauen Implementierung übergeben werden, ohne die zugrunde liegende Technologie berücksichtigt wird.
* **Ein unternehmensweites HTML-Stilhandbuch** – Solche Handbücher müssen von den Komponenten allzu oft dogmatisch befolgt werden, indem Stile „von oben nach unten“ angewandt werden.

In beiden Fällen sind die Anforderungen an die Komponenten so eng und spezifisch, dass es schwierig ist, die Kernkomponenten oder eine vordefinierten Komponente an diese anzupassen, was zu einer massiven Entwicklung von kundenspezifischen Komponenten führt.

## Frühzeitiger Einsatz {#start-early}

Anstatt die Kernkomponenten erst in der Implementierungsphase Ihres Projekts zu berücksichtigen, sollten Sie bereits in der Wireframe- und Design-Phase mit den Kernkomponenten beginnen.

### Nutzung der Komponentenbibliothek {#component-library}

Berücksichtigen Sie die [Komponentenbibliothek](https://adobe.com/go/aem_cmp_library_de) bereits in der Design-Phase. Die Kernkomponenten sind leistungsstark und flexibel und können Ihnen als ein guter Ausgangspunkt dienen. Fügen Sie benutzerdefinierte Komponenten nur hinzu, wenn eine echte geschäftliche Notwendigkeit besteht, die mit einer Kernkomponente nicht angemessen erfüllt werden kann.

### Nutzung des Benutzeroberflächen-Kits für Adobe XD {#ui-kit}

Sobald eine benutzerdefinierte Komponente nachweislich benötigt wird, verwenden Sie das [Benutzeroberflächen-Kit für Adobe XD](https://experienceleague.adobe.com/docs/experience-manager-learn/assets/AEM-CoreComponents-UI-Kit.xd), damit die Designer die Kernkomponenten beim Erstellen der Wireframes und Designs als Bausteine verwenden können.

## Leistungsstarke Funktionen nicht übersehen {#powerful-features}

Die Funktionen von AEM und den Kernkomponenten können sehr leistungsstark, aber auch sehr subtil sein. Daher sind die Möglichkeiten bestimmter Funktionen für einen Designer eventuell nicht sofort ersichtlich.

### Inhaltsfragmente {#content-fragments}

[Inhaltsfragmente](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/content-fragments.html) ermöglichen es Ihnen, kanalneutrale Inhalte zusammen mit (möglicherweise kanalspezifischen) Varianten zu erstellen. Sie können diese Fragmente und ihre Varianten bei der Erstellung Ihrer Inhaltsseiten verwenden.

In Verbindung mit dem aktualisierten JSON Exporter können strukturierte Inhaltsfragmente auch verwendet werden, um AEM-Inhalte über Content Services anderen Kanälen als AEM-Seiten bereitzustellen.

### Experience Fragment-Vorlagen {#experience-fragment-templates}

Wenn ein Autor Teile einer Seite (die sogenannten Fragmente eines Erlebnisses) wiederverwenden möchte. Ohne [Experience Fragments](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/experience-fragments.html) müsste der Autor dieses Fragment kopieren und einfügen. Das Erstellen und Verwalten dieser zum Kopieren/Einfügen vorgesehenen Erlebnisse sind zeitaufwendige und fehleranfällige Verfahren. Mit Experience Fragments ersparen Sie sich das Kopieren/Einfügen.

### Die Einbettungskomponente {#embed-component}

[Die Einbettungskomponente](/help/components/embed.md) ermöglicht nicht nur die einfache Einbindung externer Ressourcen wie YouTube-Videoinhalte, sondern ist auch erweiterbar, um Inhalte aufzunehmen, die auf die Bedürfnisse eines Projekts zugeschnitten sind.
