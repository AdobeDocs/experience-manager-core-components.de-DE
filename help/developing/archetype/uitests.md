---
title: ui.tests-Modul des AEM-Projektarchetyps
description: Verwendung der Benutzeroberflächentests des AEM-Projektarchetyps
translation-type: ht
source-git-commit: 9d737b31efc8c346775ea5296f7599295af07cf1
workflow-type: ht
source-wordcount: '112'
ht-degree: 100%

---


# ui.tests-Modul des AEM-Projektarchetyps {#uitests-module}

Das Projekt umfasst drei Teststufen:

* [Unit-Tests](core.md#unit-tests)
* [Integrationstests](ittests.md)
* Benutzeroberflächentests

In diesem Artikel werden die im ui.tests-Modul verfügbaren Benutzeroberflächentests beschrieben.

## Ausführen von Benutzeroberflächentests {#running-tests}

Führen Sie zum Testen Folgendes aus:

```shell
mvn verify -Pui-tests-local-execution
```

Nach der Ausführung sind Berichte und Protokolle im Ordner `target/reports` verfügbar.

## Zusätzliche Optionen {#additional-options}

Benutzeroberflächentests können mit vielen verschiedenen Optionen ausgeführt werden, unter anderem für Headless-Tests mit einem lokalen Browser und als Docker-Image. Weitere Informationen finden Sie in der [Datei README.md des ui.tests-Moduls](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/ui.tests).
