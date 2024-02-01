---
title: Responsives Design der Kernkomponenten
description: Erfahren Sie mehr über das responsive Design der Kernkomponenten und darüber, wie es sich auf Ihr Projekt auswirken kann.
role: Architect, Developer, Admin, User
source-git-commit: d39fe0084522f67664203a026340b23d325c1883
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 0%

---


# Responsives Design der Kernkomponenten {#responsive-design}

Alle Kernkomponenten sind so konzipiert, dass sie vollständig responsiv sind und auf allen Geräten ein nahtloses Erlebnis bieten. Beachten Sie, dass einige erweiterte Komponenten, wie z. B. die [Karussell,](/help/components/carousel.md) [Registerkarten,](/help/components/tabs.md) und [Accordion-Komponenten](/help/components/accordion.md) kann im Rahmen des Durchführungsprojekts besondere Überlegungen erfordern, um die Reaktionsfähigkeit unter allen Bedingungen zu wahren.

Angesichts der vielfältigen Möglichkeiten, mit denen diese Komponenten responsives Verhalten zeigen können, und der in der Adobe-Verpflichtung enthaltenen Verpflichtung, die Kernkomponenten einfach zu handhaben, wird die Verantwortung für die Implementierung detaillierter responsiver Aspekte absichtlich dem Projekt überlassen.

Auf schmalen Bildschirmen kann sich beispielsweise die Registerkarten-Komponente anpassen, indem breite Registerkarten auf neue Zeilen aufgeteilt werden, indem ein vertikaler Bildlauf ermöglicht wird, indem Registerkarten in Dropdown-Menüs umgewandelt werden oder ein Akkordeon-Stil verwendet wird. Aufgrund der potenziellen Auswirkungen auf die Leistung, die die Implementierung all dieser Verhaltensweisen verursachen würde, wird die [clientlibs](/help/developing/including-clientlibs.md#provided) sind als Ausgangspunkt für Implementoren und nicht als umfassende Lösung gedacht.
