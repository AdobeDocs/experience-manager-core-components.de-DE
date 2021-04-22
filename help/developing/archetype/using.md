---
title: Verwenden des AEM-Projektarchetyps
description: Detaillierte Nutzungsanleitungen für den AEM-Projektarchetyp
feature: Kernkomponenten, AEM-Projektarchetyp
role: Architect, Developer, Administrator
exl-id: a3978d8b-4904-42aa-9ee2-9c1f884327bb
translation-type: ht
source-git-commit: 8ff36ca143af9496f988b1ca65475497181def1d
workflow-type: ht
source-wordcount: '2069'
ht-degree: 100%

---

# AEM-Projektarchetyp {#aem-project-archetype}

Der AEM-Projektarchetyp erstellt ein Adobe Experience Manager-Projekt mit minimalen Best Practices als Ausgangspunkt für Ihre eigenen AEM-Projekte. Die Eigenschaften, die bei Verwendung dieses Archetyps angegeben werden müssen, ermöglichen es Ihnen, die Namen für alle Teile dieses Projekts anzugeben und bestimmte optionale Funktionen zu steuern.

## Warum Archetyp verwenden {#why-use-the-archetype}

Mithilfe des AEM-Projektarchetyps können Sie auf dem Weg zum Aufbau eines AEM-Projekts mit bewährten Verfahren und nur wenigen Tastenanschlägen beginnen. Durch Verwendung des Archetyps werden alle Teile bereits vorhanden sein, sodass das resultierende Projekt minimal ist, es jedoch bereits alle [Schlüsselfunktionen](#what-you-get) von AEM implementiert, sodass Sie nur auf dem Aufbau aufbauen und erweitern müssen.

Natürlich gibt es viele Elemente, die in ein erfolgreiches AEM-Projekt eingehen, aber die Verwendung des AEM-Projektarchetyps ist eine solide Grundlage und wird dringend für jedes AEM-Projekt empfohlen.

## Erste Schritte {#getting-started}

Der Projektarchetyp erleichtert die ersten Schritte der Entwicklung in AEM. Sie haben dabei mehrere Möglichkeiten.

* WKND-Tutorial: Eine hervorragende Einführung in die Entwicklung in AEM, einschließlich der Nutzung des Archetyps, finden Sie im Tutorial [Erste Schritte mit AEM Sites - WKND-Tutorial](https://docs.adobe.com/content/help/de-DE/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html). Es bietet ein praktisches Beispiel dafür, wie Sie mithilfe des Archetyps ein einfaches Projekt implementieren können.
* WKND Events Tutorial: Wenn Sie besonders an der Entwicklung von Single Page Applications (SPA) in AEM interessiert sind, sollten Sie sich das entsprechende [WKND Events Tutorial](https://helpx.adobe.com/de/experience-manager/kt/sites/using/getting-started-spa-wknd-tutorial-develop.html) ansehen.
* Herunterladen und selbst starten: Sie können den aktuellen Projektarchetyp, der auf GitHub verfügbar ist, einfach herunterladen und Ihr erstes Projekt erstellen, indem Sie [die folgenden einfachen Schritte ausführen](#how-to-use-the-archetype).

## Was Sie mit dem Archetyp erhalten {#what-you-get}

Der AEM-Archetyp besteht aus Modulen:

* **[core](core.md)**: ist ein Java-Bundle, das alle Kernfunktionen wie OSGi-Dienste, Listener und Scheduler sowie komponentenbezogenen Java-Code wie Servlets und Anforderungsfilter enthält.
* **[it.tests](ittests.md)**: sind Java-basierte Integrationstests.
* **[ui.apps](uiapps.md)**: enthält die `/apps`- und `/etc`-Teile des Projekts, d. h. JS- und CSS-clientlibs, Komponenten und Vorlagen.
* **[ui.content](uicontent.md)**: enthält Beispielinhalt mit den Komponenten des Moduls ui.apps.
* **ui.config**: enthält runmode-spezifische OSGi-Konfigurationen für das Projekt.
* **[ui.frontend.general](uifrontend.md)**: **(optional)** enthält die Artefakte, die zur Verwendung des allgemeinen Webpack-basierten Front-End-Buildmoduls erforderlich sind.
* **[ui.frontend.react](uifrontend-react.md)**: **(optional)** enthält die Artefakte, die erforderlich sind, wenn der Archetyp zum Erstellen eines SPA-Projekts auf der Grundlage von React verwendet wird.
* **[ui.frontend.angular](uifrontend-angular.md)**: **(optional)** enthält die Artefakte, die erforderlich sind, wenn der Archetyp zum Erstellen eines auf Angular basierenden SPA-Projekts verwendet wird.
* **[ui.tests](uitests.md)**: enthält Selenium-basierte Benutzeroberflächentests.
* **all**: ist ein Inhaltspaket, das alle kompilierten Module (Bundles und Inhaltspakete) inklusive aller Abhängigkeiten des Anbieters einbettet.
* **analyse**: führt eine Analyse für das Projekt aus, die eine zusätzliche Validierung für die Bereitstellung in AEM as a Cloud Service bietet.

![](/help/assets/archetype-structure.png)

Die in Maven dargestellten Module des AEM-Archetyps werden als Inhaltspakete bereitgestellt, die das Programm, den Inhalt und die erforderlichen OSGi-Pakete darstellen.

## Verwendung des Archetyps {#how-to-use-the-archetype}

Um den Archetyp zu verwenden, müssen Sie zunächst ein Projekt erstellen, das die Module in einer lokalen Dateistruktur wie [zuvor beschrieben](#what-you-get) generiert. Im Rahmen der Projekterstellung können mehrere Eigenschaften für Ihr Projekt definiert werden, z. B. Projektname, Version usw.

Beim Erstellen des Projekts mit Maven werden die Artefakte (Pakete und OSGi-Pakete) erstellt, die in AEM bereitgestellt werden können. Zusätzliche Maven-Befehle und -Profile können verwendet werden, um die Projektartefakte auf einer AEM-Instanz bereitzustellen.

### Erstellen eines Projekts {#create-project}

Für den Einstieg können Sie die [AEM Eclipse-Erweiterung](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developer-tools/eclipse.html?lang=de-DE) verwenden und dem Assistenten für neue Projekte folgen. Wählen Sie dann **AEM Sample Multi-Module Project**, um eine veröffentlichte Version des Archetyps zu verwenden.

Natürlich können Sie auch direkt Maven aufrufen.

```shell
mvn -B archetype:generate \
 -D archetypeGroupId=com.adobe.aem \
 -D archetypeArtifactId=aem-project-archetype \
 -D archetypeVersion=XX \
 -D aemVersion=cloud \
 -D appTitle="My Site" \
 -D appId="mysite" \
 -D groupId="com.mysite" \
 -D frontendModule=general \
 -D includeExamples=n
```

* Legen Sie `XX` auf die [Versionsnummer](https://github.com/adobe/aem-project-archetype/blob/master/VERSIONS.md) des neuesten AEM-Projektarchetyps fest.
* Legen Sie `aemVersion=cloud` für [AEM as a Cloud Service](https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/landing/home.translate.html) fest.\
   Legen Sie `aemVersion=6.5.0` für [Adobe Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams) oder On-Premise fest.
Die Abhängigkeit der Kernkomponenten wird nur für AEM-Versionen ohne Cloud Service hinzugefügt, da die Kernkomponenten für AEM as a Cloud Service standardmäßig bereitgestellt werden.
* Passen Sie `appTitle="My Site"` an, um den Titel der Website und die Komponentengruppen festzulegen.
* Passen Sie `appId="mysite"` an, um die Maven-Artefakt-ID (artifactId), die Namen der Komponenten-, Konfigurations- und Inhaltsordner sowie die Namen der Client-Bibliotheken festzulegen.
* Passen Sie `groupId="com.mysite"` an, um die Maven-Gruppen-ID (groupId) und das Java-Quellpaket festzulegen.
* Durchsuchen Sie die Liste der verfügbaren Eigenschaften, um festzustellen, ob Sie weitere anpassen möchten.

>[!NOTE]
>
>Es empfiehlt sich, das `adobe-public` Profil Ihrer Maven- `settings.xml` Datei hinzuzufügen, um repo.adobe.com automatisch zum Maven-Build-Prozess hinzuzufügen.
>
>Ein Beispiel für POM [finden Sie hier](https://helpx.adobe.com/de/experience-manager/kb/SetUpTheAdobeMavenRepository.html).

### Eigenschaften {#properties}

Die folgenden Eigenschaften sind beim Erstellen eines Projekts mit dem Archetyp verfügbar.

| Name | Default | Beschreibung |
--------------------------|----------------|--------------------
| `appTitle` |  | Der Titel der App; wird für den Titel der Website und die Komponentengruppen verwendet (z. B. `"My Site"`). |
| `appId` |  | Technischer Name; wird für Komponenten-, Konfigurations- und Inhaltsordnernamen sowie die Namen der Client-Bibliotheken verwendet (z. B. `"mysite"`). |
| `artifactId` | *`${appId}`* | Maven-Basisartefakt-ID (z. B. `"mysite"`). |
| `groupId` |  | Maven-Basisgruppen-ID (z. B. `"com.mysite"`). |
| `package` | *`${groupId}`* | Java-Quellpaket (z. B. `"com.mysite"`). |
| `version` | `1.0-SNAPSHOT` | Projektversion (z. B. `1.0-SNAPSHOT`). |
| `aemVersion` | `6.5.0` | Ziel-AEM-Version (kann `cloud` für [AEM as a Cloud Service](https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/landing/home.translate.html) sein; oder `6.5.0` oder `6.4.4` für [Adobe Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams) oder On-Premise). |
| `sdkVersion` | `latest` | Wenn `aemVersion=cloud`, dann kann eine [SDK](https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/implementing/developing/aem-as-a-cloud-service-sdk.html)-Version angegeben werden (z. B. `2020.02.2265.20200217T222518Z-200130`). |
| `includeDispatcherConfig` | `y` | Enthält eine Dispatcher-Konfiguration für Cloud oder für AMS/On-Premise, je nach dem Wert von `aemVersion` (kann `y` oder `n` sein). |
| `frontendModule` | `none` | Enthält ein WebPack-Frontend-Build-Modul, das die Client-Bibliotheken generiert (kann `general` oder `none` für reguläre Websites sein; kann `angular` oder `react` für eine Single Page App sein, die den [SPA-Editor](https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/implementing/headless/spa/introduction.html) implementiert). |
| `languageCountry` | `en_us` | Sprach- und Länder-Code zur Erstellung der Inhaltsstruktur (z. B. `en_us`). |
| `singleCountry` | `y` | Enthält eine Inhaltsstruktur für den Sprach-Master (kann `y`oder `n` sein). |
| `includeExamples` | `y` | Enthält eine Beispiel-Website für die [Komponentenbibliothek](https://www.aemcomponents.dev/) (kann `y` oder `n` sein). |
| `includeErrorHandler` | `n` | Enthält eine benutzerdefinierte 404-Antwortseite, die für die gesamte Instanz global ist (kann `y` oder `n` sein). |

>[!NOTE]
>
> Wenn der Archetyp zum ersten Mal im interaktiven Modus ausgeführt wird, können Eigenschaften mit Standardwerten nicht geändert werden (weitere Informationen finden Sie unter [ARCHETYPE-308](https://issues.apache.org/jira/browse/ARCHETYPE-308) ). Der Wert kann geändert werden, wenn die Eigenschaftsbestätigung am Ende verweigert und der Fragebogen wiederholt wird oder indem der Parameter in der Befehlszeile (z. `-DoptionIncludeExamples=n`).

>[!NOTE]
>
>Bei Ausführung unter Windows und Generierung der Dispatcher-Konfiguration sollte die Ausführung in einer Eingabeaufforderung mit erhöhten Rechten oder im Windows-Subsystem für Linux erfolgen (siehe [Problem 329](https://github.com/adobe/aem-project-archetype/issues/329)).

### Profile {#profiles}

Das generierte Maven-Projekt unterstützt bei der Ausführung verschiedene Bereitstellungsprofile `mvn install`.

| Profil-ID | Beschreibung |
--------------------------|------------------------------
| `autoInstallBundle` | Installiert das Kernpaket mit dem maven-sling-plugin für die Felix-Konsole |
| `autoInstallPackage` | Installiert das Inhaltspaket ui.content und ui.apps mit dem content-package-maven-plugin im Package Manager für die Standard-Autoreninstanz auf localhost, Port 4502. Hostname und Port können mit den benutzerdefinierten Eigenschaften `aem.host` und `aem.port` geändert werden. |
| `autoInstallPackagePublish` | Installiert das Inhaltspaket ui.content und ui.apps mit dem content-package-maven-plugin im Package Manager für die Standard-Veröffentlichungsinstanz auf localhost, Port 4503. Hostname und Port können mit den benutzerdefinierten Eigenschaften `aem.host` und `aem.port` geändert werden. |
| `autoInstallSinglePackage` | Installiert das Inhaltspaket `all` mit dem content-package-maven-plugin im Package Manager für die Standard-Autoreninstanz auf localhost, Port 4502. Hostname und Port können mit den benutzerdefinierten Eigenschaften `aem.host` und `aem.port` geändert werden. |
| `autoInstallSinglePackagePublish` | Installiert das Inhaltspaket `all` mit dem content-package-maven-plugin im Package Manager für die Standard-Veröffentlichungsinstanz auf localhost, Port 4503. Hostname und Port können mit den benutzerdefinierten Eigenschaften `aem.host` und `aem.port` geändert werden. |
| `integrationTests` | Führt die bereitgestellten Integrationstests auf der AEM-Instanz aus (nur für die `verify` Phase) |

### Erstellen und Installieren {#building-and-installing}

Um alle im Projektstammordner ausgeführten Module zu erstellen, verwenden Sie den folgenden Maven-Befehl.

```shell
mvn clean install
```

Wenn Sie über eine ausgeführte AEM-Instanz verfügen, können Sie das gesamte Projekt erstellen und verpacken und mit dem folgenden Maven-Befehl in AEM bereitstellen.

```shell
mvn clean install -PautoInstallPackage
```

Führen Sie zum Bereitstellen auf einer Veröffentlichungsinstanz diesen Befehl aus.

```shell
mvn clean install -PautoInstallPackagePublish
```

Sie können diesen Befehl auch ausführen, um eine Bereitstellung in einer Veröffentlichungsinstanz durchzuführen.

```shell
mvn clean install -PautoInstallPackage -Daem.port=4503
```

Sie können auch nur das Bundle für den Autor bereitstellen, indem Sie diesen Befehl ausführen.

```shell
mvn clean install -PautoInstallBundle
```

## Übergeordnete POM {#parent-pom}

Die `pom.xml` am Stamm des Projekts (`<src-directory>/<project>/pom.xml`) wird als übergeordneter POM bezeichnet und treibt die Struktur des Projekts sowie Abhängigkeiten und bestimmte globale Eigenschaften des Projekts.

### Globale Projekteigenschaften {#global-properties}

Im `<properties>` Abschnitt des übergeordneten POM werden verschiedene globale Eigenschaften definiert, die für die Bereitstellung Ihres Projekts auf einer AEM-Instanz wichtig sind, z. B. Benutzername/Kennwort, Hostname/Anschluss usw.

Diese Eigenschaften sind für die Bereitstellung auf einer lokalen AEM-Instanz eingerichtet, da dies der häufigste Build ist, den Entwickler ausführen. Beachten Sie, dass Eigenschaften für eine Autoreninstanz sowie für eine Veröffentlichungsinstanz bereitgestellt werden müssen. An dieser Stelle werden die Anmeldeinformationen auch für die Authentifizierung mit der AEM-Instanz festgelegt. Es werden die standardmäßigen admin:admin-Anmeldeinformationen verwendet.

Diese Eigenschaften werden so eingerichtet, dass sie bei der Bereitstellung in Umgebungen mit höherer Ebene überschrieben werden können. Auf diese Weise müssen sich die POM-Dateien nicht ändern, aber Variablen wie `aem.host` `sling.password` und können über Befehlszeilenargumente überschrieben werden:

```shell
mvn -PautoInstallPackage clean install -Daem.host=production.hostname -Dsling.password=productionpasswd
```

### Modulstruktur {#module-structure}

Der `<modules>` Abschnitt des übergeordneten POM definiert die Module, die das Projekt erstellen wird. Standardmäßig erstellt das Projekt [die zuvor definierten](#what-you-get) Standardmodule: core, ui.apps, ui.content, ui.tests und it.launcher. Im Laufe der Entwicklung eines Projekts können immer mehr Module hinzugefügt werden.

### Abhängigkeiten {#dependencies}

Im `<dependencyManagement>` Abschnitt des übergeordneten POM werden alle Abhängigkeiten und Versionen der im Projekt verwendeten APIs definiert. Versionen sollten im übergeordneten POM verwaltet werden. Untermodule wie core und ui.apps sollten keine Versionsinformationen enthalten.

#### Uber-Jar {#uber-jar}

Eine der wichtigsten Abhängigkeiten ist die [AEM uber-jar](https://docs.adobe.com/content/help/de-DE/experience-manager-65/developing/devtools/ht-projects-maven.html#ExperienceManagerAPIDependencies). Dies umfasst alle AEM-APIs mit nur einem einzigen Abhängigkeitseintrag für die Version von AEM.

>[!NOTE]
>
>Als Best Practice sollten Sie die Version uber-jar aktualisieren, um sie an die Zielversion von AEM anzupassen. Wenn Sie beispielsweise eine Bereitstellung auf AEM 6.4 planen, sollten Sie die Version der uber-jar auf 6.4.0 aktualisieren.

#### Kernkomponenten {#core-components}

Der AEM-Projektarchiv nutzt natürlich die Kernkomponenten.

Die Kernkomponenten werden in AEM automatisch im Standard-Ausführungsmodus installiert und von der WKND-Beispiel-Site verwendet. In einem [Produktions-Ausführungsmodus](https://docs.adobe.com/content/help/de-DE/experience-manager-65/administering/security/production-ready.html) (`nosamplecontent`) sind die Kernkomponenten nicht verfügbar.

Um die Kernkomponenten in allen Implementierungen zu nutzen, empfiehlt es sich daher, sie in das Maven-Projekt einzubeziehen.

>[!NOTE]
>
>Nach jeder Version der Kernkomponenten wird im Allgemeinen eine Version des AEM-Projektarchetyps veröffentlicht, sodass der neueste Archetyp die neueste Version der Kernkomponenten verwendet.
>
>Eine neue Version des Archetyps folgt möglicherweise nicht direkt einer neuen Version der Kernkomponenten, daher sollten Sie die Abhängigkeit von den Kernkomponenten auf die neueste Version aktualisieren.

>[!NOTE]
>
>Die Datei „core.wcm.components.example“enthält eine Reihe von Beispielseiten, die Beispiele für die Kernkomponenten illustrieren. Als Best Practice sollten Sie bei der Bereitstellung eines Projekts für die Produktion diese Abhängigkeit und die Einbeziehung von Unterpaketen entfernen.

## Testen {#testing}

Es gibt drei Testebenen im Projekt, und da es sich bei ihnen um unterschiedliche Testtypen handelt, werden sie auf unterschiedliche Weise oder an verschiedenen Orten durchgeführt.

* Unit-Test im Kern: Hier werden klassische Unit-Tests des im Bundle enthaltenen Codes vorgestellt. Führen Sie zum Testen Folgendes aus:
   * `mvn clean test`
* Serverseitige Integrationstests: Diese führen geräteähnliche Tests in der AEM-Umgebung, d. h. auf dem AEM-Server, aus. Führen Sie zum Testen Folgendes aus:
   * `mvn clean verify -PintegrationTests`
* Clientseitige Hobbes.js-Tests: Hierbei handelt es sich um JavaScript-basierte Browser-basierte Tests, die das Verhalten auf der Browserseite überprüfen. So testen Sie:
   1. Laden Sie AEM genau wie eine Seite in Ihren Browser.
   1. Öffnen Sie die Seite im [Entwicklermodus](https://docs.adobe.com/content/help/de-DE/experience-manager-65/developing/components/developer-mode.html).
   1. Öffnen Sie das linke Bedienfeld und wechseln Sie zur Registerkarte **Tests**.
   1. Suchen Sie die generierten **MyName-Tests** und führen Sie sie aus.

## Nächste Schritte {#next-steps}

Sie haben den AEM-Projektarchetyp erstellt und installiert. Was jetzt? Der Archetyp ist klein, besteht aber aus vielen Beispielen leistungsfähiger AEM-Funktionen, die gemäß empfohlenen Best Practices konfiguriert wurden. Verwenden Sie diese, um anzuzeigen, wie Sie diese Funktionen in Ihrem Projekt nutzen können. Bei jedem Projekt müssen Sie wahrscheinlich folgende Aufgaben durchführen:

* [Komponenten durch Erweiterung der vorhandenen Kernkomponenten anpassen](/help/developing/customizing.md)
* [Zusätzliche Vorlagen hinzufügen](https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/sites/authoring/features/templates.translate.html)
* [Lokalisierungsstruktur anpassen](https://docs.adobe.com/content/help/de-DE/experience-manager-65/administering/introduction/tc-prep.html)
* [Informationen zum Front-End-Build-Modul abrufen](uifrontend.md)
