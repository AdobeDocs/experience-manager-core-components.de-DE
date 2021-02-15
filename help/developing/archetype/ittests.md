---
title: it.tests Module of AEM Project Archetype
description: Verwendung der AEM Project Archetype-Integrationstests
translation-type: tm+mt
source-git-commit: 9d737b31efc8c346775ea5296f7599295af07cf1
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 46%

---


# it.tests Module of the AEM Project Archetype {#ittests-module}

Das Projekt umfasst drei Teststufen:

* [Unit-Tests](core.md#unit-tests)
* Integrationstests
* [UI-Tests](uitests.md)

In diesem Artikel werden die Integrationstests beschrieben, die im Rahmen des Moduls &quot;it.tests&quot;verfügbar sind.

## Ausführen von Integrationstests {#running-tests}

Die Server-seitigen Integrationstests ermöglichen die Ausführung von Komponententests in der AEM-Umgebung, d. h. auf dem AEM-Server. Führen Sie zum Testen Folgendes aus:

```
mvn clean verify -PintegrationTests
```
