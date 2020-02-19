---
title: ui.tests Module von AEM Project Archetype
description: Verwendung von AEM Project Archetype JUnit-Tests
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# ui.tests Module of the AEM Project Archetype {#uitests-module}

Das Projekt umfasst drei Teststufen:

## Komponententests {#unit-tests}

The unit test in the [core module](core.md) showcases classic unit testing of the code contained in the bundle. Führen Sie zum Testen Folgendes aus:

```
mvn clean test
```

## Integrationstests {#integration-tests}

Die serverseitigen Integrationstests ermöglichen die Ausführung von Komponententests in der AEM-Umgebung, d. h. auf dem AEM-Server. Führen Sie zum Testen Folgendes aus:

```
mvn clean verify -PintegrationTests
```

## Clientseitige Tests {#client-side-tests}

Bei den `client-side Hobbes.js` Tests handelt es sich um JavaScript-basierte Browser-basierte Tests zur Überprüfung des Browser-seitigen Verhaltens.

Um zu testen, öffnen Sie beim Anzeigen einer AEM-Seite, die Sie im Browser testen möchten, die Seite im **Entwicklermodus** , indem Sie das linke Bedienfeld öffnen und zur Registerkarte &quot; **Tests** &quot;wechseln. Suchen Sie dann die generierten **MyName-Tests** und führen Sie sie aus.
