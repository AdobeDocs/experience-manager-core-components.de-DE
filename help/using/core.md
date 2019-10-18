---
title: Kernmodul des AEM-Projektarchetyps
seo-title: Kernmodul des AEM-Projektarchetyps
description: Kernmodul des AEM-Projektarchetyps
seo-description: Kernmodul des AEM-Projektarchetyps
contentOwner: Bohnert
content-type: Referenz
topic-tags: Kernkomponenten
translation-type: tm+mt
source-git-commit: 683b4f4705c226275439a408423cbf1b23bea66f

---


# Kernmodul des AEM-Projektarchetyps {#core-module}

Das Core-Maven-Modul (`<src-directory>/<project>/core`) enthält den gesamten Java-Code, der für die Implementierung benötigt wird. Das Modul verpackt den gesamten Java-Code und stellt ihn als OSGi-Paket für die AEM-Instanz bereit.

Das im `<src-directory>/<project>/core/pom.xml` definierten Maven Bundle-Plugin ist für die Kompilierung des Java-Codes in ein OSGi-Bundle verantwortlich, das vom AEM OSGi-Container erkannt werden kann. Beachten Sie, dass hier der Speicherort der Sling-Modelle definiert wird.

Obwohl es selten vorkommt, dass das Kernpaket unabhängig vom ui.apps-Modul in Umgebungen auf der obersten Ebene bereitgestellt werden muss, ist die direkte Bereitstellung des Kernpakets während der lokalen Entwicklung/Tests nützlich. Das Maven Sling Plugin ermöglicht die Bereitstellung des Core Bundles in AEM, wobei das `autoInstallBundle` Profil, wie im [übergeordneten POM](overview.md#parent-pom)definiert, direkt genutzt wird.

```
mvn -PautoInstallBundle clean install
```

Nach erfolgreicher Ausführung sollte die Bundels-Konsole angezeigt werden können unter `http://<host>:<port>/system/console/bundles`.
