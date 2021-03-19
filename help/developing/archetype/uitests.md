---
title: ui.tests-Modul des AEM-Projektarchetyps
description: Verwendung der Benutzeroberflächentests des AEM-Projektarchetyps
feature: Hauptkomponenten, AEM Projektarchiv
role: Architekt, Entwickler, Administrator
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 93%

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
