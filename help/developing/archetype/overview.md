---
title: AEM-Projektarchetyp
description: Eine Projektvorlage für AEM-basierte Anwendungen
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# AEM-Projektarchetyp {#aem-project-archetype}

Der AEM-Projektarchetyp erstellt ein Adobe Experience Manager-Projekt mit minimalen Best Practices als Ausgangspunkt für Ihre eigenen AEM-Projekte. Die Eigenschaften, die bei Verwendung dieses Archetyps angegeben werden müssen, ermöglichen es Ihnen, die Namen für alle Teile dieses Projekts anzugeben und bestimmte optionale Funktionen zu steuern.

>[!TIP]
>
>Der neueste AEM Project Archetype [kann auf GitHub](https://github.com/adobe/aem-project-archetype)gefunden werden.

## Funktionen {#features}

Der Archetyp verfügt über eine Reihe von Funktionen, die einen bequemen Ausgangspunkt für neue AEM-Projekte bieten sollen:

* Englisch und Französisch Seiten mit Beispielinhalt
* Eine Inhaltsvorlage, die auf der Funktion einer bearbeitbaren Vorlage mit einer Beispielinhaltsrichtlinie basiert
* Seitenkomponente basierend auf der [AEM-Seitenkomponente](/help/components/page.md)
* Beispiele für Inhaltskomponenten, die mit dem empfohlenen Proxy-Muster und einer Beispielkomponente &quot;helloworld&quot;implementiert wurden, basieren alle auf [AEM-Kernkomponenten](/help/introduction.md).
* Beispiele für [Formularkomponenten](/help/components/forms/form-container.md)
* Konfigurationen für Geräteemulatoren, Drag &amp; Drop-Einrichtung und Internationalisierung
* Client-Bibliotheken nach BEM-Benennungskonventionen sowie komponentenspezifische Stile
* Beispielpakete mit Beispielmodellen, Servelets, Filtern und Schedulern
* Einheiten-, Integrations- und clientseitige Tests
* Beispiele für SPA-Implementierungen in &quot;React&quot;oder &quot;Angular&quot;(optional)

## Warum Archetyp verwenden {#why-use-the-archetype}

Mithilfe des AEM-Projektarchetyps können Sie auf dem Weg zum Aufbau eines AEM-Projekts mit bewährten Verfahren und nur wenigen Tastenanschlägen beginnen. Durch Verwendung des Archetyps werden alle Teile bereits vorhanden sein, sodass das resultierende Projekt minimal ist, es jedoch bereits alle [Schlüsselfunktionen](#features) von AEM implementiert, sodass Sie nur auf dem Aufbau aufbauen und erweitern müssen.

Natürlich gibt es viele Elemente, die in ein erfolgreiches AEM-Projekt eingehen, aber die Verwendung des AEM-Projektarchetyps ist eine solide Grundlage und wird dringend für jedes AEM-Projekt empfohlen.

## Erste Schritte {#getting-started}

Der Projektarchiv erleichtert die Entwicklung auf AEM. Sie können Ihre ersten Schritte auf verschiedene Weise durchführen.

* WKND-Tutorial - Eine großartige Einführung in die Entwicklung von AEM, einschließlich der Nutzung des Archetyps, finden Sie im Tutorial [Erste Schritte mit AEM-Sites - WKND-Tutorial](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html) , in dem Sie anhand des Archetyps ein einfaches Projekt implementieren können.
* WKND Events Tutorial - Wenn Sie besonders an der Entwicklung von Einzelseitenanwendungen (SPA) auf AEM interessiert sind, sollten Sie sich das entsprechende [WKND Events Tutorial](https://helpx.adobe.com/experience-manager/kt/sites/using/getting-started-spa-wknd-tutorial-develop.html)ansehen.
* Downloaden und starten Sie selbst! - Sie können den aktuellen Projektarchiv, der auf GitHub verfügbar ist, einfach herunterladen und Ihr erstes Projekt erstellen, indem Sie die [folgenden](#how-to-use-the-archetype)Schritte ausführen.

## Was Sie mit dem Archetyp erhalten {#what-you-get}

Der AEM-Archetyp besteht aus Modulen:

* **[core](core.md)**: ist ein Java-Bundle, das alle Kernfunktionen wie OSGi-Dienste, Listener und Scheduler sowie komponentenbezogenen Java-Code wie Servlets und Anforderungsfilter enthält.
* **[ui.apps](uiapps.md)**: enthält die`/apps`und`/etc`Teile des Projekts, d.h. JS- und CSS-clientlibs, Komponenten, Vorlagen, runmode-spezifische Konfigurationen sowie Hobbes-Tests.
* **[ui.content](uicontent.md)**: enthält Beispielinhalt mit den Komponenten des Moduls ui.apps.
* **[ui.tests](uitests.md)**: ist ein Java-Bundle, das JUnit-Tests enthält, die serverseitig ausgeführt werden. Dieses Bundle soll nicht in der Produktion bereitgestellt werden.
* **ui.launcher**: enthält Klebercode, der das ui.tests-Bundle (und die abhängigen Bundles) auf dem Server bereitstellt und die Ausführung von JUnit auslöst.
* **[ui.frontend.general](uifrontend.md)**:**(optional)**enthält die Artefakte, die zur Verwendung des allgemeinen Webpack-basierten Front-End-Buildmoduls erforderlich sind.
* **[ui.frontend.response](uifrontend-react.md)**:**(optional)**enthält die Artefakte, die erforderlich sind, wenn der Archetyp zum Erstellen eines SPA-Projekts auf der Grundlage von React verwendet wird.
* **[ui.frontend.angular](uifrontend-angular.md)**:**(optional)**enthält die Artefakte, die erforderlich sind, wenn der Archetyp zum Erstellen eines auf Angular basierenden SPA-Projekts verwendet wird.

![](/help/assets/archetype-structure.png)

Die in Maven dargestellten Module des AEM-Archetyps werden als Inhaltspakete bereitgestellt, die die Anwendung, den Inhalt und die erforderlichen OSGi-Pakete darstellen.

## Voraussetzungen {#requirements}

Für die aktuelle Version des Archetyps gelten folgende Anforderungen:

* Adobe Experience Manager 6.3.3.0 oder höher (6.4.2 oder höher beim Generieren eines Projekts mit den Optionen zum Erstellen eines Angular- oder React-Front-End-Builds) oder [AEM als Cloud-Dienst](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html)
* Apache Maven (3.3.9 oder höher)
* Adobe Public Maven Repository in Ihren Maven-Einstellungen. Weitere Informationen finden Sie in diesem [Knowledge Base-Artikel](https://helpx.adobe.com/experience-manager/kb/SetUpTheAdobeMavenRepository.html).

Eine Liste der unterstützten AEM-Versionen früherer Archetypversionen finden Sie in den [historisch unterstützten AEM-Versionen](https://github.com/adobe/aem-project-archetype/blob/master/VERSIONS.md).

## Verwendung des Archetyps {#how-to-use-the-archetype}

Um den Archetyp zu verwenden, müssen Sie zunächst ein Projekt erstellen, das die Module in einer lokalen Dateistruktur wie [zuvor beschrieben](#what-you-get)generiert. Im Rahmen der Projekterstellung können mehrere Eigenschaften für Ihr Projekt definiert werden, z. B. Projektname, Version usw.

Beim Erstellen des Projekts mit Maven werden die Artefakte (Pakete und OSGi-Pakete) erstellt, die in AEM bereitgestellt werden können. Zusätzliche Maven-Befehle und -Profile können verwendet werden, um die Projektartefakte auf einer AEM-Instanz bereitzustellen.

### Erstellen eines Projekts {#create-project}

Für den Einstieg können Sie die [AEM Eclipse-Erweiterung](https://docs.adobe.com/content/help/en/experience-manager-65/developing/devtools/aem-eclipse.html) verwenden und dem Assistenten für neue Projekte folgen. Wählen Sie dann **AEM Sample Multi-Module Project** , um eine veröffentlichte Version des Archetyps zu verwenden.

Natürlich können Sie auch direkt Maven aufrufen.

```
mvn archetype:generate \
 -DarchetypeGroupId=com.adobe.granite.archetypes \
 -DarchetypeArtifactId=aem-project-archetype \
 -DarchetypeVersion=XX
```

Hierbei `XX` handelt es sich um die [Versionsnummer](https://github.com/adobe/aem-project-archetype/blob/master/VERSIONS.md) des neuesten AEM-Projektarchetyps.

>[!NOTE]
>
>Es empfiehlt sich, das `adobe-public` Profil Ihrer Maven- `settings.xml` Datei hinzuzufügen, um repo.adobe.com automatisch zum Maven-Build-Prozess hinzuzufügen.
>
>Ein Beispiel für POM [finden Sie hier](https://helpx.adobe.com/experience-manager/kb/SetUpTheAdobeMavenRepository.html).

### Eigenschaften {#properties}

Die folgenden Eigenschaften sind beim Erstellen eines Projekts mit dem Archetyp verfügbar.

| Name | Default | Beschreibung |
----------------------------|---------|--------------------
| `groupId` |  | Maven-Basis `groupId` |
| `artifactId` |  | Maven-Basis ArtefaktId |
| `version` |  | Version |
| `package` |  | Java-Quellpaket |
| `appID` |  | Anwendungs-ID für Komponenten-, Konfigurations- und Inhaltsordner und CSS-IDs |
| `appTitle` |  | Antragstitel für den Titel der Website und die Komponentengruppen |
| `aemVersion` | 6.5.0 | Target AEM-Version |
| `sdkVersion` |  |
| `languageCountry` | en_us | Sprach- und Ländercode zur Erstellung der lokalisierten Inhaltsstruktur (z. `en_us`) |
| `includeExamples` | y | Beispielsite Komponentenbibliothek einschließen |
| `includeErrorHandler` | n | Eine benutzerdefinierte 404-Antwortseite einschließen |
| `frontendModule` | none | Schließen Sie ein dediziertes Frontend-Modul ein (eines von `none`, [`general`](uifrontend.md), [`angular`](uifrontend-angular.md), [`react`](uifrontend-react.md)) |
| `singleCountry` | y | Erstellen einer Sprach-Master-Struktur in Beispielinhalt |
| `includeDispatcherConfig` | n | Definiert, ob eine Dispatcher-Konfiguration für das Projekt generiert wird, auf das <br> beim Erstellen eines Projekts für [`cloud`](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.cloud)AEM als Cloud-Dienst[ festgelegt wird, auf ](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html) <br> [`ams`](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams) den beim Erstellen eines Projekts für Adobe Managed Services |

>[!NOTE]
> Wenn der Archetyp zum ersten Mal im interaktiven Modus ausgeführt wird, können Eigenschaften mit Standardwerten nicht geändert werden (weitere Informationen finden Sie unter [ARCHETYPE-308](https://issues.apache.org/jira/browse/ARCHETYPE-308) ). Der Wert kann geändert werden, wenn die Eigenschaftsbestätigung am Ende verweigert und der Fragebogen wiederholt wird oder indem der Parameter in der Befehlszeile (z. `-DoptionIncludeExamples=n`).

>[!NOTE]
>Bei Ausführung unter Windows und Generierung der Dispatcher-Konfiguration sollten Sie an einer erhöhten Eingabeaufforderung oder im Windows-Subsystem für Linux ausgeführt werden (siehe [Problem 329](https://github.com/adobe/aem-project-archetype/issues/329)).

### Profile {#profiles}

Das generierte Maven-Projekt unterstützt bei der Ausführung verschiedene Bereitstellungsprofile `mvn install`.

| Profil-ID | Beschreibung |
--------------------------|------------------------------
| `autoInstallBundle` | Installieren Sie das Kernpaket mit dem maven-sling-Plug-In in der felix-Konsole |
| `autoInstallPackage` | Installieren Sie das Inhaltspaket ui.content und ui.apps mit dem content-package-maven-plugin im Package Manager, um die Standard-Autoreninstanz auf localhost, Port 4502, zu installieren. Hostname and port can be changed with the `aem.host` and `aem.port` user defined properties. |
| `autoInstallPackagePublish` | Installieren Sie das Inhaltspaket ui.content und ui.apps mit dem content-package-maven-plugin im Package Manager, um die standardmäßige Veröffentlichungsinstanz auf localhost, Port 4503, zu aktivieren. Hostname and port can be changed with the `aem.host` and `aem.port` user defined properties. |
| `autoInstallSinglePackage` | Install the `all` content package with the content-package-maven-plugin to the package manager to default author instance on localhost, port 4502. Hostname and port can be changed with the `aem.host` and `aem.port` user defined properties. |
| `autoInstallSinglePackagePublish` | Install the `all` content package with the content-package-maven-plugin to the package manager to default publish instance on localhost, port 4503. Hostname and port can be changed with the `aem.host` and `aem.port` user defined properties. |
| `integrationTests` | Führt die bereitgestellten Integrationstests auf der AEM-Instanz aus (nur für die `verify` Phase) |

### Erstellen und Installieren {#building-and-installing}

Um alle im Projektstammordner ausgeführten Module zu erstellen, verwenden Sie den folgenden Maven-Befehl.

```
mvn clean install
```

Wenn Sie über eine ausgeführte AEM-Instanz verfügen, können Sie das gesamte Projekt erstellen und verpacken und mit dem folgenden Maven-Befehl in AEM bereitstellen.

```
mvn clean install -PautoInstallPackage
```

Führen Sie zum Bereitstellen auf einer Veröffentlichungsinstanz diesen Befehl aus.

```
mvn clean install -PautoInstallPackagePublish
```

Sie können diesen Befehl auch ausführen, um eine Bereitstellung in einer Veröffentlichungsinstanz durchzuführen.

```
mvn clean install -PautoInstallPackage -Daem.port=4503
```

Sie können auch nur das Bundle für den Autor bereitstellen, indem Sie diesen Befehl ausführen.

```
mvn clean install -PautoInstallBundle
```

## Übergeordnete POM {#parent-pom}

Die `pom.xml` am Stamm des Projekts (`<src-directory>/<project>/pom.xml`) wird als übergeordneter POM bezeichnet und treibt die Struktur des Projekts sowie Abhängigkeiten und bestimmte globale Eigenschaften des Projekts.

### Globale Projekteigenschaften {#global-properties}

Im `<properties>` Abschnitt des übergeordneten POM werden verschiedene globale Eigenschaften definiert, die für die Bereitstellung Ihres Projekts auf einer AEM-Instanz wichtig sind, z. B. Benutzername/Kennwort, Hostname/Anschluss usw.

Diese Eigenschaften sind für die Bereitstellung auf einer lokalen AEM-Instanz eingerichtet, da dies der häufigste Build ist, den Entwickler ausführen. Beachten Sie, dass Eigenschaften für eine Autoreninstanz sowie für eine Veröffentlichungsinstanz bereitgestellt werden müssen. An dieser Stelle werden die Anmeldeinformationen auch für die Authentifizierung mit der AEM-Instanz festgelegt. Es werden die standardmäßigen admin:admin-Anmeldeinformationen verwendet.

Diese Eigenschaften werden so eingerichtet, dass sie bei der Bereitstellung in Umgebungen mit höherer Ebene überschrieben werden können. Auf diese Weise müssen sich die POM-Dateien nicht ändern, aber Variablen wie `aem.host` `sling.password` und können über Befehlszeilenargumente überschrieben werden:

````
mvn -PautoInstallPackage clean install -Daem.host=production.hostname -Dsling.password=productionpasswd
````

### Modulstruktur {#module-structure}

Der `<modules>` Abschnitt des übergeordneten POM definiert die Module, die das Projekt erstellen wird. Standardmäßig erstellt das Projekt [die zuvor definierten](#what-you-get)Standardmodule: core, ui.apps, ui.content, ui.tests und it.launcher. Im Laufe der Entwicklung eines Projekts können immer mehr Module hinzugefügt werden.

### Abhängigkeiten {#dependencies}

Im `<dependencyManagement>` Abschnitt des übergeordneten POM werden alle Abhängigkeiten und Versionen der im Projekt verwendeten APIs definiert. Versionen sollten im übergeordneten POM verwaltet werden. Untermodule wie core und ui.apps sollten keine Versionsinformationen enthalten.

#### Uber-Jar {#uber-jar}

Eine der wichtigsten Abhängigkeiten ist die [AEM uber-jar](https://docs.adobe.com/content/help/en/experience-manager-65/developing/devtools/ht-projects-maven.html#ExperienceManagerAPIDependencies). Dies umfasst alle AEM-APIs mit nur einem einzigen Abhängigkeitseintrag für die Version von AEM.

>[!NOTE]
>
>Als Best Practice sollten Sie die Version uber-jar aktualisieren, um sie an die Zielversion von AEM anzupassen. Wenn Sie beispielsweise eine Bereitstellung auf AEM 6.4 planen, sollten Sie die Version der uber-jar auf 6.4.0 aktualisieren.

#### Kernkomponenten {#core-components}

Der AEM-Projektarchiv nutzt natürlich die Kernkomponenten.

Die Kernkomponenten werden in AEM automatisch im Standard-Ausführungsmodus installiert und von der Web.Retail-Beispiel-Site verwendet. In einem [Produktions-Ausführungsmodus](https://docs.adobe.com/content/help/en/experience-manager-65/administering/security/production-ready.html) (`nosamplecontent`) sind die Kernkomponenten nicht verfügbar.

Um die Kernkomponenten in allen Implementierungen zu nutzen, empfiehlt es sich daher, sie in das Maven-Projekt einzubeziehen.

>[!NOTE]
>
>Nach jeder Version der Kernkomponenten wird im Allgemeinen eine Version des AEM-Projektarchetyps veröffentlicht, sodass der neueste Archetyp die neueste Version der Kernkomponenten verwendet.
>
>Eine neue Version des Archetyps folgt möglicherweise nicht direkt einer neuen Version der Kernkomponenten, daher sollten Sie die Abhängigkeit von den Kernkomponenten auf die neueste Version aktualisieren.

>[!NOTE]
>
>Die Datei &quot;core.wcm.components.example&quot;enthält eine Reihe von Beispielseiten, die Beispiele für die Kernkomponenten illustrieren. Als Best Practice sollten Sie bei der Bereitstellung eines Projekts für die Produktion diese Abhängigkeit und die Einbeziehung von Unterpaketen entfernen.

## Testen {#testing}

Es gibt drei Testebenen im Projekt, und da es sich bei ihnen um unterschiedliche Testtypen handelt, werden sie auf unterschiedliche Weise oder an verschiedenen Orten durchgeführt.

* Komponententest im Kern: Hier werden klassische Komponententests des im Bundle enthaltenen Codes vorgestellt. Führen Sie zum Testen Folgendes aus:
   * `mvn clean test`
* Serverseitige Integrationstests: Diese führen geräteähnliche Tests in der AEM-Umgebung, d. h. auf dem AEM-Server, aus. Führen Sie zum Testen Folgendes aus:
   * `mvn clean verify -PintegrationTests`
* Clientseitige Hobbes.js-Tests: Hierbei handelt es sich um JavaScript-basierte Browser-basierte Tests, die das Verhalten auf der Browserseite überprüfen. So testen Sie:
   1. Laden Sie AEM genau wie eine Seite in Ihren Browser.
   1. Öffnen Sie die Seite im [Entwicklermodus](https://docs.adobe.com/content/help/en/experience-manager-65/developing/components/developer-mode.html) .
   1. Öffnen Sie das linke Bedienfeld und wechseln Sie zur Registerkarte **Tests** .
   1. Suchen Sie die generierten **MyName-Tests** und führen Sie sie aus.

## Nächste Schritte {#next-steps}

Sie haben den AEM-Projektarchetyp erstellt und installiert. Was jetzt? Der Archetyp ist klein, besteht aber aus vielen Beispielen leistungsfähiger AEM-Funktionen, die gemäß empfohlenen Best Practices konfiguriert wurden. Verwenden Sie diese, um anzuzeigen, wie Sie diese Funktionen in Ihrem Projekt nutzen können. Bei jedem Projekt müssen Sie wahrscheinlich folgende Aufgaben durchführen:

* [Komponenten durch Erweiterung der vorhandenen Kernkomponenten anpassen](/help/developing/customizing.md)
* [Zusätzliche Vorlagen hinzufügen](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)
* [Lokalisierungsstruktur anpassen](https://docs.adobe.com/content/help/en/experience-manager-65/administering/introduction/tc-prep.html)
* [Informationen zum Front-End-Build-Modul abrufen](uifrontend.md)
