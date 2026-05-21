---
title: Responsives Design der Kernkomponenten
description: Erfahren Sie mehr über das responsive Design der Kernkomponenten und darüber, wie es sich auf Ihr Projekt auswirken kann.
role: Developer, Admin, User
exl-id: c0eff174-6803-4b44-aeb1-eae3bc8a36ea
TQID: https://experienceleague.adobe.com/wUpRlK8WxDuQzmFJFWAwFZUY-1fo9qOOgbOn-GEwBok
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 73aa5234ac63fa3be99feebce448bb6722513838
workflow-type: tm+mt
source-wordcount: 178
ht-degree: 100%

---

# Responsives Design der Kernkomponenten {#responsive-design}

Alle Kernkomponenten sind so konzipiert, dass sie vollständig responsiv sind und auf allen Geräten ein nahtloses Erlebnis bieten. Es ist wichtig zu beachten, dass einige fortgeschrittene Komponenten, wie z. B. [Karussell](/help/components/carousel.md)-, [Registerkarten](/help/components/tabs.md)- und [Akkordeon-Komponenten](/help/components/accordion.md), im Rahmen des Implementierungsprojekts besondere Überlegungen erfordern, um die Reaktionsfähigkeit unter allen Bedingungen zu gewährleisten.

In Anbetracht der vielfältigen Möglichkeiten, wie diese Komponenten responsives Verhalten zeigen können, und angesichts der Verpflichtung von Adobe, die Kernkomponenten standardmäßig schlank zu halten, wird die Verantwortung für die Implementierung detaillierter responsiver Aspekte absichtlich dem Projekt überlassen.

Auf schmalen Bildschirmen kann sich beispielsweise die Registerkarten-Komponente anpassen, indem breite Registerkarten auf neue Zeilen aufgeteilt werden, indem ein vertikaler Bildlauf ermöglicht wird, indem Registerkarten in Dropdown-Menüs umgewandelt werden oder ein Akkordeon-Stil verwendet wird. Aufgrund der potenziellen Auswirkungen auf die Leistung, die die Implementierung all dieser Verhaltensweisen mit sich bringen würde, sind die [Clientlibs](/help/developing/including-clientlibs.md#provided) als Ausgangspunkt für Implementierende gedacht und nicht als umfassende Lösung.
