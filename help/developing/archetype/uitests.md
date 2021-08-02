---
title: ui.tests-Modul des AEM-Projektarchetyps
description: Verwendung der Benutzeroberflächentests des AEM-Projektarchetyps
feature: Kernkomponenten, AEM-Projektarchetyp
role: Architect, Developer, Admin
exl-id: eb3c9b34-f10e-410f-bcf3-34f94f124c7c
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: ht
source-wordcount: '117'
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
