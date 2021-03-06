---
title: Kernmodul des AEM-Projektarchetyps
description: Kernmodul des AEM-Projektarchetyps
feature: Kernkomponenten, AEM-Projektarchetyp
role: Architect, Developer, Admin
exl-id: 49e80d8c-2b41-4c42-b45e-c2e3b4b16a59
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: ht
source-wordcount: '187'
ht-degree: 100%

---

# Kernmodul des AEM-Projektarchetyps {#core-module}

Das Core-Maven-Modul (`<src-directory>/<project>/core`) enthält den gesamten Java-Code, der für die Implementierung benötigt wird. Das Modul verpackt den gesamten Java-Code und stellt ihn als OSGi-Paket für die AEM-Instanz bereit.

Das im `<src-directory>/<project>/core/pom.xml` definierten Maven Bundle-Plug-in ist für die Kompilierung des Java-Codes in ein OSGi-Bundle verantwortlich, das vom AEM OSGi-Container erkannt werden kann. Beachten Sie, dass hier der Speicherort der Sling-Modelle definiert wird.

Obwohl es selten vorkommt, dass das Kernpaket unabhängig vom ui.apps-Modul in Umgebungen auf der obersten Ebene bereitgestellt werden muss, ist die direkte Bereitstellung des Kernpakets während der lokalen Entwicklung/Tests nützlich. Das Maven Sling-Plug-in ermöglicht die Bereitstellung des Core Bundles in AEM, wobei das `autoInstallBundle` Profil, wie im [übergeordneten POM](/help/developing/archetype/using.md#parent-pom) definiert, direkt genutzt wird.

```shell
mvn -PautoInstallBundle clean install
```

Nach der Ausführung sollte die Bundles-Konsole unter `http://<host>:<port>/system/console/bundles` angezeigt werden.

## Unit-Tests {#unit-tests}

Die Unit-Tests im Kernmodul stellen klassische Unit-Tests des im Bundle enthaltenen Codes vor. Führen Sie zum Testen Folgendes aus:

```shell
mvn clean test
```
