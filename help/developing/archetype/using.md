---
title: Verwenden des AEM-Projektarchetyps
description: Erfahren Sie, wie Sie mit dem AEM Projektarchetyp ein Adobe Experience Manager-Projekt mit minimalen Best Practices als Ausgangspunkt für Ihre eigenen AEM erstellen können.
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: a3978d8b-4904-42aa-9ee2-9c1f884327bb
source-git-commit: bd92a5d1884056ca7b44ea28e5817d8bde10a4d9
workflow-type: tm+mt
source-wordcount: '1092'
ht-degree: 33%

---


# Verwenden des AEM-Projektarchetyps {#using-the-archetype}

In diesem Dokument wird erläutert, wie Sie mit dem AEM Projektarchetyp ein Adobe Experience Manager-Projekt mit minimalen Best Practices als Ausgangspunkt für Ihre eigenen AEM erstellen können.

Der Schwerpunkt liegt auf allgemeinen Nutzungsmustern und dem, was der Archetyp für Sie tut. Detaillierte Build-Optionen und technische Anweisungen finden Sie in der Dokumentation im GitHub-Repository des Archetyps.

>[!TIP]
>
>Die aktuelle AEM Projektarchetyp und die zugehörige technische Dokumentation [finden Sie auf GitHub.](https://github.com/adobe/aem-project-archetype)

## Erste Schritte {#getting-started}

Der Projektarchetyp erleichtert die ersten Schritte der Entwicklung in AEM. Sie können Ihre ersten Schritte mit dem Archetyp auf verschiedene Weise durchführen.

* **WKND-Tutorial** - Eine hervorragende Einführung in die Entwicklung in AEM, einschließlich der Nutzung des Archetyps, finden Sie unter [Erste Schritte mit AEM Sites - WKND-Tutorial](https://experienceleague.adobe.com/docs/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html?lang=de) für ein praktisches Beispiel, das Sie durch die Verwendung des Archetyps zur Implementierung eines einfachen Projekts führt.
* **WKND-Events-Tutorial** - Wenn Sie besonders an der Entwicklung von Einzelseiten-Apps (SPA) auf AEM interessiert sind, besuchen Sie [WKND Events-Tutorial.](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html?lang=de)
* **Fang selbst an!** - Sie können die [aktueller Projektarchetyp, der auf GitHub verfügbar ist](https://github.com/adobe/aem-project-archetype) und erstellen Sie Ihr erstes Projekt selbst.

## Verwendung des Archetyps {#how-to-use-the-archetype}

Der erste Schritt bei Verwendung des Archetyps besteht darin, ein Projekt zu erstellen, das [die Module](#what-you-get) in einer lokalen Dateistruktur. Im Rahmen der Projekterstellung können verschiedene Eigenschaften für Ihr Projekt definiert werden, z. B. Projektname, Version, Aktivierung verschiedener Optionen usw.

>[!TIP]
>
>Jedes Mal, wenn Sie den Archetyp erstellen, wird auch eine Reihe von Readmes generiert, die Ihnen die technischen Details und die Verwendung der einzelnen Module als [unten verlinkt.](#what-you-get)

Beim Erstellen des Projekts mit Maven werden die Artefakte (Pakete und OSGi-Pakete) erstellt, die in AEM bereitgestellt werden können. Zusätzliche Maven-Befehle und -Profile können verwendet werden, um die Projektartefakte auf einer AEM-Instanz bereitzustellen.

## Was Sie mit dem Archetyp erhalten {#what-you-get}

Der Archetyp besteht aus Modulen, die alle bei Verwendung des Archetyps automatisch erstellt werden.

* **[core](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/core)** ist ein Java-Bundle, das alle Kernfunktionen wie OSGi-Dienste, Listener und Scheduler sowie komponentenbezogenen Java-Code wie Servlets und Anforderungsfilter enthält.
* **[it.tests](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/it.tests)** sind Java-basierte Integrationstests.
* **[ui.apps](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.apps)** enthält die `/apps` und `/etc` Teile des Projekts, d. h. JS- und CSS-Client-Bibliotheken, Komponenten und Vorlagen.
* **[ui.content](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.content)** enthält Beispielinhalt, der die Komponenten des Moduls ui.apps verwendet.
* **[ui.config](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.config)** enthält runmode-spezifische OSGi-Konfigurationen für das Projekt.
* **[ui.frontend.general](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.frontend.general)** enthält die Artefakte, die für die Verwendung des allgemeinen Webpack-basierten Front-End-Buildmoduls erforderlich sind (optional).
* **[ui.frontend.react](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.frontend.react)** **(optional)** enthält die Artefakte, die erforderlich sind, wenn der Archetyp zum Erstellen eines SPA Projekts auf der Basis von React verwendet wird (optional, abhängig von Build-Parametern).
* **[ui.frontend.angular](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.frontend.angular)** **(optional)** enthält die Artefakte, die erforderlich sind, wenn der Archetyp zum Erstellen eines SPA auf der Basis von Angular verwendet wird (optional, abhängig von Build-Parametern).
* **[ui.tests](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.tests)** enthält Selenium-basierte UI-Tests.
* **[all](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/all)** ist ein einzelnes Inhaltspaket, das alle kompilierten Module (Pakete und Inhaltspakete) einschließlich aller Abhängigkeiten von Anbietern einbettet.
* **[dispatcher.ams](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/dispatcher.ams)** enthält die grundlegenden Dispatcher-Konfigurationen für AMS/On-Premise-Projekte (optional, abhängig von Build-Parametern).
* **[dispatcher.cloud](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/dispatcher.cloud)** enthält die grundlegenden Dispatcher-Konfigurationen für AEMaaCS-Projekte (optional, abhängig von Build-Parametern).

![Inhaltspaket-Organisation](/help/assets/content-package-organization.png)

Die in Maven dargestellten Module des Archetyps werden AEM als Inhaltspakete bereitgestellt, die die Anwendung, den Inhalt und die erforderlichen OSGi-Pakete darstellen.

## Übergeordnete POM {#parent-pom}

Die `pom.xml` am Stamm des Projekts (`<src-directory>/<project>/pom.xml`) wird als übergeordnete POM bezeichnet und bestimmt die Struktur des Projekts sowie Abhängigkeiten und bestimmte globale Eigenschaften des Projekts.

### Globale Projekteigenschaften {#global-properties}

Im `<properties>` Abschnitt des übergeordneten POM werden verschiedene globale Eigenschaften definiert, die für die Bereitstellung Ihres Projekts auf einer AEM-Instanz wichtig sind, z. B. Benutzername/Kennwort, Hostname/Anschluss usw.

Diese Eigenschaften sind für die Bereitstellung auf einer lokalen AEM-Instanz eingerichtet, da dies der häufigste Build ist, den Entwickler ausführen. Beachten Sie, dass Eigenschaften für eine Autoreninstanz sowie für eine Veröffentlichungsinstanz bereitgestellt werden müssen. An dieser Stelle werden die Anmeldeinformationen auch für die Authentifizierung mit der AEM-Instanz festgelegt. Die Standardeinstellung `admin:admin` -Anmeldedaten verwendet werden.

Diese Eigenschaften werden so eingerichtet, dass sie bei der Bereitstellung in Umgebungen mit höherer Ebene überschrieben werden können. Auf diese Weise müssen sich die POM-Dateien nicht ändern, aber Variablen wie `aem.host` `sling.password` und können über Befehlszeilenargumente überschrieben werden:

```shell
mvn -PautoInstallPackage clean install -Daem.host=production.hostname -Dsling.password=productionpasswd
```

### Modulstruktur {#module-structure}

Der `<modules>` Abschnitt des übergeordneten POM definiert die Module, die das Projekt erstellen wird. Standardmäßig erstellt das Projekt [die zuvor definierten Standardmodule.](#what-you-get) Im Laufe der Entwicklung eines Projekts können immer mehr Module hinzugefügt werden.

### Abhängigkeiten {#dependencies}

Im `<dependencyManagement>` Abschnitt des übergeordneten POM werden alle Abhängigkeiten und Versionen der im Projekt verwendeten APIs definiert. Versionen sollten im übergeordneten POM verwaltet werden. Untermodule sollten keine Versionsinformationen enthalten.

#### Uber-Jar {#uber-jar}

Eine der wichtigsten Abhängigkeiten ist die [AEM Java-API-JAR.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-as-a-cloud-service-sdk.html?lang=de) Dies umfasst alle AEM-APIs mit nur einem einzigen Abhängigkeitseintrag für die Version von AEM.

>[!NOTE]
>
>Als Best Practice sollten Sie die Version uber-jar aktualisieren, um sie an die Zielversion von AEM anzupassen. Wenn Sie beispielsweise eine Bereitstellung auf AEM 6.5 planen, sollten Sie die Version der uber-jar auf 6.5.X aktualisieren, wobei `X` ist das neueste Service Pack.

#### Kernkomponenten {#core-components}

Der Archetyp nutzt natürlich die [Kernkomponenten.](/help/introduction.md) Um die Kernkomponenten in allen Implementierungen zu nutzen, empfiehlt es sich daher, sie als Teil des Maven-Projekts einzubeziehen.

Die Datei „core.wcm.components.example“enthält eine Reihe von Beispielseiten, die Beispiele für die Kernkomponenten illustrieren. Als Best Practice sollten Sie bei der Bereitstellung eines Projekts für die Produktion diese Abhängigkeit und die Einbeziehung von Unterpaketen entfernen.

>[!NOTE]
>
>Die Kernkomponenten und der Archetyp werden als separate GitHub-Projekte verwaltet und unterscheiden sich daher von ihren Versionen.
>
>Bei jeder Version des Archetyps wird die neueste Version der Kernkomponenten verwendet, die zum Zeitpunkt der Veröffentlichung verfügbar sind. Möglicherweise möchten Sie die Abhängigkeit von den Kernkomponenten jedoch manuell aktualisieren.

## Testing {#testing}

Es gibt drei Testebenen im Projekt, und da es sich bei ihnen um unterschiedliche Testtypen handelt, werden sie auf unterschiedliche Weise oder an verschiedenen Orten durchgeführt.

* **[Unit-Tests](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/core)** - Testen von klassischen Einheiten des im Bundle enthaltenen Codes
* **[Integrationstests](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/it.tests)** - Server-seitige Integrationstests, die in der AEM-Umgebung, d. h. auf dem AEM, geräteähnliche Tests ausführen
* **[UI-Tests](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.tests)** - Selenium-basierte Browser-seitige Tests, die das Browser-seitige Verhalten überprüfen
