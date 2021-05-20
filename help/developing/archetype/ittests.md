---
title: it.tests-Modul des AEM-Projektarchetyps
description: Verwendung der Integrationstests des AEM-Projektarchetyps
feature: Kernkomponenten, AEM-Projektarchetyp
role: Architect, Developer, Administrator
exl-id: 0abc0265-3a3f-4323-97e6-3af0c62299ef
source-git-commit: 8ff36ca143af9496f988b1ca65475497181def1d
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 100%

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
