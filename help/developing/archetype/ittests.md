---
title: it.tests-Modul des AEM-Projektarchetyps
description: Verwendung der Integrationstests des AEM-Projektarchetyps
translation-type: ht
source-git-commit: 9d737b31efc8c346775ea5296f7599295af07cf1
workflow-type: ht
source-wordcount: '75'
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
