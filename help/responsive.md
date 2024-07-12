---
title: Responsives Design der Kernkomponenten
description: Erfahren Sie mehr über das responsive Design der Kernkomponenten und darüber, wie es sich auf Ihr Projekt auswirken kann.
role: Architect, Developer, Admin, User
exl-id: c0eff174-6803-4b44-aeb1-eae3bc8a36ea
source-git-commit: 5f49fb45869d1721e16a787a2c6ff927b6ad49fe
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 100%

---

# Responsives Design der Kernkomponenten {#responsive-design}

Alle Kernkomponenten sind so konzipiert, dass sie vollständig responsiv sind und auf allen Geräten ein nahtloses Erlebnis bieten. Es ist wichtig zu beachten, dass einige fortgeschrittene Komponenten, wie z. B. [Karussell](/help/components/carousel.md)-, [Registerkarten](/help/components/tabs.md)- und [Akkordeon-Komponenten](/help/components/accordion.md), im Rahmen des Implementierungsprojekts besondere Überlegungen erfordern, um die Reaktionsfähigkeit unter allen Bedingungen zu gewährleisten.

In Anbetracht der vielfältigen Möglichkeiten, wie diese Komponenten responsives Verhalten zeigen können, und angesichts der Verpflichtung von Adobe, die Kernkomponenten standardmäßig schlank zu halten, wird die Verantwortung für die Implementierung detaillierter responsiver Aspekte absichtlich dem Projekt überlassen.

Auf schmalen Bildschirmen kann sich beispielsweise die Registerkarten-Komponente anpassen, indem breite Registerkarten auf neue Zeilen aufgeteilt werden, indem ein vertikaler Bildlauf ermöglicht wird, indem Registerkarten in Dropdown-Menüs umgewandelt werden oder ein Akkordeon-Stil verwendet wird. Aufgrund der potenziellen Auswirkungen auf die Leistung, die die Implementierung all dieser Verhaltensweisen mit sich bringen würde, sind die [Clientlibs](/help/developing/including-clientlibs.md#provided) als Ausgangspunkt für Implementierende gedacht und nicht als umfassende Lösung.
