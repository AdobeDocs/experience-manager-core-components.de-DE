---
title: ui.tests-Modul des AEM-Projektarchetyps
description: Verwendung des AEM-Projektarchetyps JUnit Tests
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 100%

---


# ui.tests-Modul des AEM-Projektarchetyps {#uitests-module}

Das Projekt umfasst drei Teststufen:

## Unit-Tests {#unit-tests}

Die Unit-Tests im [Kernmodul](core.md) stellen klassische Komponententests des im Bundle enthaltenen Codes vor. Führen Sie zum Testen Folgendes aus:

```
mvn clean test
```

## Integrationstests {#integration-tests}

Die Server-seitigen Integrationstests ermöglichen die Ausführung von Komponententests in der AEM-Umgebung, d. h. auf dem AEM-Server. Führen Sie zum Testen Folgendes aus:

```
mvn clean verify -PintegrationTests
```

## Client-seitige Tests {#client-side-tests}

Bei den `client-side Hobbes.js` Tests handelt es sich um JavaScript-basierte Browser-seitige Tests zur Überprüfung des Browser-seitigen Verhaltens.

Sie führen Tests wie folgt durch: Wenn Sie eine AEM-Seite anzeigen, die Sie im Browser testen möchten, öffnen Sie diese Seite im **Entwicklermodus**. Dazu öffnen Sie das linke Bedienfeld und wechseln zur Registerkarte „**Tests**“. Suchen Sie dann die generierten **MyName-Tests** und führen Sie sie aus.
