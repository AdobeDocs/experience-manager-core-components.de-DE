---
title: ui.tests-Modul des AEM-Projektarchetyps
description: Verwendung der AEM Projektarchiv-UI-Tests
translation-type: tm+mt
source-git-commit: 9d737b31efc8c346775ea5296f7599295af07cf1
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 26%

---


# ui.tests-Modul des AEM-Projektarchetyps {#uitests-module}

Das Projekt umfasst drei Teststufen:

* [Unit-Tests](core.md#unit-tests)
* [Integrationstests](ittests.md)
* UI-Tests

In diesem Artikel werden die im Modul ui.tests verfügbaren UI-Tests beschrieben.

## Ausführen von UI-Tests {#running-tests}

Führen Sie zum Testen Folgendes aus:

```shell
mvn verify -Pui-tests-local-execution
```

Nach der Ausführung sind Berichte und Protokolle im Ordner `target/reports` verfügbar.

## Zusätzliche Optionen {#additional-options}

UI-Tests können mit vielen verschiedenen Optionen ausgeführt werden, unter anderem zum kostenlosen Testen mit einem lokalen Browser und als Docker-Bild. Weitere Informationen finden Sie in der Datei [README.md des Moduls ui.tests](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/ui.tests).
