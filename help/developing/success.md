---
title: Wege zum Erfolg mit den Kernkomponenten
description: So implementieren Sie Ihr Projekt erfolgreich mit den Kernkomponenten
role: Developer, Admin, User
exl-id: 1ea8cd1c-8435-4ded-82dc-5a7896c53e0c
TQID: https://experienceleague.adobe.com/hV-KF86ktxXulypPRnkb6RwOrVXnXP2W1utXzgpG0CI
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: e2c1b6d3-bb7e-4fe8-8c72-f7b403298e91
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 73aa5234ac63fa3be99feebce448bb6722513838
workflow-type: tm+mt
source-wordcount: 592
ht-degree: 100%

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

Berücksichtigen Sie die [Komponentenbibliothek](https://adobe.com/go/aem_cmp_library_de) bereits in der Design-Phase. Die Kernkomponenten sind leistungsstark und flexibel und können Ihnen als ein guter Ausgangspunkt dienen. Fügen Sie benutzerdefinierte Komponenten nur hinzu, wenn eine echte geschäftliche Anforderung besteht, die mit einer Kernkomponente nicht angemessen erfüllt werden kann.

### Nutzung des Benutzeroberflächen-Kits für Adobe XD {#ui-kit}

Sobald eine benutzerdefinierte Komponente nachweislich benötigt wird, verwenden Sie das Benutzeroberflächen-Kit für Adobe XD, [das hier heruntergeladen werden kann](https://experienceleague.adobe.com/docs/experience-manager-learn/assets/AEM-CoreComponents-UI-Kit.xd?lang=de), damit die Designerinnen und Designer die Kernkomponenten beim Erstellen der Wireframes und Designs als Bausteine verwenden können.

## Leistungsstarke Funktionen nicht übersehen {#powerful-features}

Die Funktionen von AEM und den Kernkomponenten können sehr leistungsstark, aber auch sehr subtil sein. Daher sind die Möglichkeiten bestimmter Funktionen für einen Designer eventuell nicht sofort ersichtlich.

### Inhaltsfragmente {#content-fragments}

[Inhaltsfragmente](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/content-fragments.html?lang=de) ermöglichen es Ihnen, kanalneutrale Inhalte zusammen mit (möglicherweise kanalspezifischen) Varianten zu erstellen. Sie können diese Fragmente und ihre Varianten bei der Erstellung Ihrer Inhaltsseiten verwenden.

In Verbindung mit dem aktualisierten JSON Exporter können strukturierte Inhaltsfragmente auch verwendet werden, um AEM-Inhalte über Content Services anderen Kanälen als AEM-Seiten bereitzustellen.

### Experience Fragment-Vorlagen {#experience-fragment-templates}

Wenn ein Autor Teile einer Seite (die sogenannten Fragmente eines Erlebnisses) wiederverwenden möchte. Ohne [Experience Fragments](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/experience-fragments.html?lang=de) müsste der Autor dieses Fragment kopieren und einfügen. Das Erstellen und Verwalten dieser zum Kopieren/Einfügen vorgesehenen Erlebnisse sind zeitaufwendige und fehleranfällige Verfahren. Mit Experience Fragments ersparen Sie sich das Kopieren/Einfügen.

### Die Einbettungskomponente {#embed-component}

[Die Einbettungskomponente](/help/components/embed.md) ermöglicht nicht nur die einfache Einbindung externer Ressourcen wie YouTube-Videoinhalte, sondern ist auch erweiterbar, um Inhalte aufzunehmen, die auf die Bedürfnisse eines Projekts zugeschnitten sind.
