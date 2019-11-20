---
title: Kernmodul des AEM-Projektarchetyps
seo-title: Kernmodul des AEM-Projektarchetyps
description: Kernmodul des AEM-Projektarchetyps
seo-description: Kernmodul des AEM-Projektarchetyps
contentOwner: bohnert
content-type: reference
topic-tags: core-components
translation-type: tm+mt
source-git-commit: ca7a47d8ac91516659c115a3f27c09f0ee4b8b33

---


# Kernmodul des AEM-Projektarchetyps {#core-module}

Das Core-Maven-Modul (`<src-directory>/<project>/core`) enthält den gesamten Java-Code, der für die Implementierung benötigt wird. Das Modul verpackt den gesamten Java-Code und stellt ihn als OSGi-Paket für die AEM-Instanz bereit.

Das im `<src-directory>/<project>/core/pom.xml` definierten Maven Bundle-Plugin ist für die Kompilierung des Java-Codes in ein OSGi-Bundle verantwortlich, das vom AEM OSGi-Container erkannt werden kann. Beachten Sie, dass hier der Speicherort der Sling-Modelle definiert wird.

Obwohl es selten vorkommt, dass das Kernpaket unabhängig vom ui.apps-Modul in Umgebungen auf der obersten Ebene bereitgestellt werden muss, ist die direkte Bereitstellung des Kernpakets während der lokalen Entwicklung/Tests nützlich. Das Maven Sling Plugin ermöglicht die Bereitstellung des Core Bundles in AEM, wobei das `autoInstallBundle` Profil, wie im [übergeordneten POM](overview.md#parent-pom)definiert, direkt genutzt wird.

```
mvn -PautoInstallBundle clean install
```

Once successfully executed, you should be able to see the Bundles Console at `http://<host>:<port>/system/console/bundles`.
