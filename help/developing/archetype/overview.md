---
title: AEM-Projektarchetyp
description: Eine Projektvorlage für AEM-basierte Anwendungen
translation-type: tm+mt
source-git-commit: 2faa092a075ab0512e9bd5654884534936c0ad53

---


# AEM-Projektarchetyp {#aem-project-archetype}

Der AEM Project Archetype ist eine Maven-Vorlage, die ein minimales, auf Best Practices basierendes Adobe Experience Manager (AEM)-Projekt als Ausgangspunkt für Ihre Website erstellt.

>[!TIP]
>
>Der neueste AEM-Projektarchetyp [ist auf GitHub zu finden](https://github.com/adobe/aem-project-archetype).

## Ressourcen {#resources}

* **Archetypdokumentation (dieses Dokument):** Überblick über die Architektur des Archetyps und die verschiedenen Module.
   * **[Verwenden des Archetyps:](using.md)**Weitere Informationen zur Verwendung des Archetyps und der verfügbaren Module
   * **[ui.frontend:](uifrontend.md)**Verwenden des Front-End-Buildmoduls
* Die folgenden Übungen basieren auf diesem Archetyp:
   * **[WKND-Site:](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)**Erfahren Sie, wie eine neue Website Beginn wird.
   * **[WKND-Einzelseitenanwendung:](https://helpx.adobe.com/experience-manager/kt/sites/using/getting-started-spa-wknd-tutorial-develop.html)**Erfahren Sie, wie Sie eine React- oder Angular-Webapp erstellen, die in AEM vollständig autorisiert ist.

## Funktionen {#features}

* **Best Practice:** Bootstrapping Ihrer Site mit allen von Adobe empfohlenen Vorgehensweisen.
* **Low-Code:** Bearbeiten Sie Ihre Vorlagen, erstellen Sie Inhalte, stellen Sie Ihre CSS bereit und Ihre Site kann live geschaltet werden.
* **Cloud-bereit:** Falls gewünscht, verwenden Sie [AEM als Cloud-Dienst](https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/landing/home.translate.html) , um in wenigen Tagen live zu gehen und Skalierbarkeit und Wartung zu erleichtern.
* **Dispatcher:** Ein Projekt ist nur mit einer [Dispatcher-Konfiguration](https://docs.adobe.com/content/help/en/experience-manager-dispatcher/using/dispatcher.html) abgeschlossen, die Geschwindigkeit und Sicherheit gewährleistet.
* **Multi-Site:** Bei Bedarf generiert der Archetyp die Inhaltsstruktur für ein [mehrsprachiges und mehrregionales Setup](https://docs.adobe.com/content/help/en/experience-manager-65/administering/introduction/msm.html).
* **Hauptkomponenten:** Autoren können nahezu jedes Layout mit unserem vielseitigen [Satz standardisierter Komponenten](/help/introduction.md)erstellen.
* **Bearbeitbare Vorlagen:** Stellen Sie praktisch jede [Vorlage ohne Code](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/page-authoring/template-editor-feature-video-use.html)zusammen und definieren Sie, was die Autoren bearbeiten dürfen.
* **Responsive Layout:** Auf Vorlagen oder einzelnen Seiten [definieren Sie, wie die Elemente für die definierten Haltepunkte umfließen](https://docs.adobe.com/content/help/en/experience-manager-65/authoring/siteandpage/responsive-layout.html) .
* **Kopf- und Fußzeile:** Stellen Sie sie mithilfe der [lokale Anpassung-Funktionen der Komponenten](https://docs.adobe.com/content/help/en/experience-manager-core-components/using/get-started/localization.html)ohne Code zusammen und lokalisieren Sie sie.
* **Stilsystem:** Vermeiden Sie das Erstellen benutzerdefinierter Komponenten, indem Autoren verschiedene Stile [anwenden](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/style-system.html) können.
* **Front-End-Build:** Front-End-Entwickler können [AEM-Seiten](uifrontend.md#webpack-dev-server) mit dem Modell abgleichen und Client-Bibliotheken [mit Webpack, TypeScript und SASS](uifrontend.md) erstellen.
* **WebApp-bereit:** Verwenden Sie für Sites, die [React](uifrontend-react.md) oder [Angular](uifrontend-angular.md)verwenden, das [SPA-SDK](https://docs.adobe.com/content/help/en/experience-manager-64/developing/headless/spas/spa-architecture.html) , um das Authoring [im Kontext der App](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html)beizubehalten.
* **Beispielcode:** Sehen Sie sich die Komponente HelloWorld und die Beispielmodelle, Servelets, Filter und Planungen an.
* **Open Source:** Wenn etwas nicht so ist, wie es sollte, [tragen](https://github.com/adobe/aem-core-wcm-components/blob/master/CONTRIBUTING.md) Sie Ihre Verbesserungen!

## Nutzung

Um ein Projekt zu erstellen, passen Sie die folgende Befehlszeile an Ihre Anforderungen an:

```
mvn -B archetype:generate \
 -D archetypeGroupId=com.adobe.granite.archetypes \
 -D archetypeArtifactId=aem-project-archetype \
 -D archetypeVersion=23 \
 -D aemVersion=cloud \
 -D appTitle="My Site" \
 -D appId="mysite" \
 -D groupId="com.mysite" \
 -D frontendModule=general \
 -D includeExamples=n
```

* Set `aemVersion=cloud` for [AEM as a Cloud Service](https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/landing/home.translate.html);\
   Wird `aemVersion=6.5.0` für [Adobe Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams)oder lokal eingestellt.
Die Abhängigkeit der Kernkomponenten wird nur für Nicht-Cloud-AEM-Versionen hinzugefügt, da die Kernkomponenten OOTB für AEM als Cloud-Dienst bereitgestellt werden.
* Passen Sie `appTitle="My Site"` die Definition des Website-Titels und der Komponenten-Gruppen an.
* Passen Sie `appId="mysite"` die Definition von &quot;Maven artifactId&quot;, die Namen der Komponenten-, Konfigurations- und Inhaltsordner sowie die Namen der Client-Bibliothek an.
* Passen Sie `groupId="com.mysite"` die Definition der Maven groupId und des Java Source-Pakets an.
* Suchen Sie die Liste der verfügbaren Eigenschaften, um zu sehen, ob Sie mehr anpassen möchten.

## Verfügbare Eigenschaften

| Name | Default | Beschreibung |
--------------------------|----------------|--------------------
| `appTitle` |  | Der Titel der Anwendung wird für den Titel der Website und für die Gruppen der Komponenten (z. `"My Site"`). |
| `appId` |  | Technischer Name, wird für Komponenten-, Konfigurations- und Inhaltsordnernamen sowie Client-Bibliotheksnamen (z. `"mysite"`). |
| `artifactId` | *`${appId}`* | Base Maven artifact ID (e.g. `"mysite"`). |
| `groupId` |  | Base Maven group ID (e.g. `"com.mysite"`). |
| `package` | *`${groupId}`* | Java Source Package (z. `"com.mysite"`). |
| `version` | `1.0-SNAPSHOT` | Projektversion (z. `1.0-SNAPSHOT`). |
| `aemVersion` | `6.5.0` | Zielgruppe AEM-Version (kann `cloud` für [AEM als Cloud-Dienst](https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/landing/home.translate.html)verwendet werden; oder `6.5.0`, `6.4.4`oder `6.3.3` für [Adobe Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams) oder lokale Dienste). |
| `sdkVersion` | `latest` | Wenn `aemVersion=cloud` eine [SDK](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/developing/aem-as-a-cloud-service-sdk.html) -Version angegeben werden kann (z. `2020.02.2265.20200217T222518Z-200130`). |
| `includeDispatcherConfig` | `y` | Umfasst eine Dispatcher-Konfiguration für Cloud oder für AMS/On-Premise, je nach Wert von `aemVersion` (kann `y` oder `n`). |
| `frontendModule` | `none` | Enthält ein WebPack-Frontend-Build-Modul, das die Client-Bibliotheken generiert (kann für normale Sites `general` oder `none` für normale Sites verwendet werden; kann `angular` oder `react` für eine Einzelseitenanwendung verwendet werden, die den [SPA-Editor](https://docs.adobe.com/content/help/en/experience-manager-65/developing/headless/spas/spa-overview.html)implementiert. |
| `languageCountry` | `en_us` | Language and country code to create the content structure from (e.g. `en_us`). |
| `singleCountry` | `y` | Umfasst eine Struktur für den Inhalt von SprachMaster (kann `y`oder `n`). |
| `includeExamples` | `y` | Enthält eine Beispielsite für die [Komponentenbibliothek](https://www.aemcomponents.dev/) (kann `y`oder `n`). |
| `includeErrorHandler` | `n` | Enthält eine benutzerdefinierte 404-Antwortseite, die für die gesamte Instanz global ist (kann `y` oder `n`). |

## Systemanforderungen

| Archetyp | AEM as a Cloud Service | AEM 6.5 | AEM 6.4 | AEM 6.3 | Java SE | Maven |
---------|---------|---------|---------|---------|---------|---------
| [23](https://github.com/adobe/aem-project-archetype/releases/tag/aem-project-archetype-23) | Kontinuierlich | 6.5.0.0+ | 6.4.4.0+ | 6.3.3.4+ | 8, 11 | 3.3.9+ |

Richten Sie Ihre lokale Entwicklungs-Umgebung für [AEM als Cloud-Dienst-SDK](https://docs.adobe.com/content/help/en/experience-manager-learn/cloud-service/local-development-environment-set-up/overview.html) oder für [ältere Versionen von AEM](https://docs.adobe.com/content/help/en/experience-manager-learn/foundation/development/set-up-a-local-aem-development-environment.html)ein.

### Bekannte Probleme

When running on Windows and generating the dispatcher configuration, you should be running in an elevated command prompt or the Windows Subsystem for Linux (see [#329](https://github.com/adobe/aem-project-archetype/issues/329)).

Beim Ausführen des Archetyps im interaktiven Modus (ohne `-B` Parameter) können die Eigenschaften mit den Standardwerten nicht geändert werden, es sei denn, die letzte Bestätigung wird verworfen. Dadurch werden die Fragen wiederholt, indem die Eigenschaften mit den Standardwerten in die Fragen aufgenommen werden (Einzelheiten siehe[ARCHETYPE-308](https://issues.apache.org/jira/browse/ARCHETYPE-308) ).

## Weiterführende Literatur {#further-reading}

Weitere Informationen zur Verwendung des Archetyps, einschließlich der Vorteile, Optionen und der Funktionsweise der Module, finden Sie im Dokument [Verwenden des Archetyps.](using.md)