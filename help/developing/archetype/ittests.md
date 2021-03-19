---
title: it.tests-Modul des AEM-Projektarchetyps
description: Verwendung der Integrationstests des AEM-Projektarchetyps
feature: Hauptkomponenten, AEM Projektarchiv
role: Architekt, Entwickler, Administrator
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 90%

---


# it.tests-Modul des AEM-Projektarchetyps {#ittests-module}

Das Projekt umfasst drei Teststufen:

* [Unit-Tests](core.md#unit-tests)
* Integrationstests
* [Benutzeroberflächentests](uitests.md)

In diesem Artikel werden die im it.tests-Modul verfügbaren Integrationstests beschrieben.

## Ausführen von Integrationstests {#running-tests}

Die Server-seitigen Integrationstests ermöglichen die Ausführung von Komponententests in der AEM-Umgebung, d. h. auf dem AEM-Server. Führen Sie zum Testen Folgendes aus:

```
mvn clean verify -PintegrationTests
```
