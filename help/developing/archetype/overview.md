---
title: AEM-Projektarchetyp
description: Eine Projektvorlage für AEM-basierte Programme
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: 58994726-9b65-4035-9d45-60b745d577bb
source-git-commit: 0d004c90e789f23ff9e121fbd8ae11df9c9748b2
workflow-type: tm+mt
source-wordcount: '1192'
ht-degree: 100%

---

# AEM-Projektarchetyp {#aem-project-archetype}

Der AEM-Projektarchetyp ist eine Maven-Vorlage, anhand derer ein minimales, auf Best Practices basierendes Adobe Experience Manager (AEM)-Projekt als Ausgangspunkt für Ihre Website erstellt wird.

>[!TIP]
>
>Der neueste AEM-Projektarchetyp [ist auf GitHub zu finden](https://github.com/adobe/aem-project-archetype).

## Ressourcen {#resources}

* **Dokumentation zum Archetyp (dieses Dokument):** Überblick über die Architektur des Archetyps und die verschiedenen Module.
   * **[Verwenden des Archetyps:](using.md)** Weitere Informationen zur Verwendung des Archetyps und der verfügbaren Module
   * **[ui.frontend:](uifrontend.md)** Verwendung des Frontend-Build-Moduls
* **Die folgenden Tutorials basieren auf diesem Archetyp:**
   * **[WKND-Site:](https://experienceleague.adobe.com/docs/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html?lang=de)** Erfahren Sie, wie eine neue Website beginnen.
   * **[WKND Single Page App:](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html?lang=de)** Erfahren Sie, wie Sie eine Web-App für React oder Angular erstellen, die vollständig in AEM erstellt werden kann.

## Funktionen {#features}

* **Best Practice:** Laden Sie Ihre Website mit den neuesten empfohlenen Verfahren von Adobe.
* **Wenig Code:** Bearbeiten Sie Ihre Vorlagen, erstellen Sie Inhalte, stellen Sie Ihre CSS bereit und Ihre Website kann live geschaltet werden.
* **Cloud-fähig:** Falls gewünscht, verwenden Sie [AEM as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/landing/home.html?lang=de), um in wenigen Tagen live zu gehen und Skalierbarkeit und Wartung zu erleichtern.
* **Dispatcher:** Ein Projekt ist nur mit einer [Dispatcher-Konfiguration](https://experienceleague.adobe.com/docs/experience-manager-dispatcher/using/dispatcher.html?lang=de), die Geschwindigkeit und Sicherheit gewährleistet, abgeschlossen.
* **Mehrere Websites:** Bei Bedarf generiert der Archetyp die Inhaltsstruktur für eine [Konfigurationen mit mehreren Sprachen und Regionen](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/administering/reusing-content/msm/overview.html?lang=de).
* **Kernkomponenten:** Autoren können mit unserem vielseitigen [Satz standardisierter Komponenten](/help/introduction.md) nahezu jedes Layout erstellen.
* **Bearbeitbare Vorlagen:** Stellen Sie praktisch jede [Vorlage ohne Code](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/page-authoring/template-editor-feature-video-use.html?lang=de) zusammen und legen Sie fest, was die Autoren bearbeiten dürfen.
* **Responsives Layout:** Definieren Sie auf Vorlagen oder einzelnen Seiten, [wie die Elemente die definierten Breakpoints umfließen](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/get-started/localization.html?lang=de).
* **Kopf- und Fußzeile:** Stellen Sie sie mithilfe der [Lokalisierungsfunktionen der Komponenten](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/get-started/localization.html?lang=de) ohne Code zusammen und lokalisieren Sie sie.
* **Stilsystem:** Vermeiden Sie das Erstellen benutzerdefinierter Komponenten, indem Autoren [verschiedene Stile anwenden](https://experienceleague.adobe.com/docs/experience-manager-learn/getting-started-wknd-tutorial-develop/project-archetype/style-system.html?lang=de) können.
* **Frontend-Build:** Mit Webpack, TypeScript und SASS können Frontend-Entwickler [AEM-Seiten modellieren](uifrontend.md#webpack-dev-server) und [Client-Bibliotheken erstellen](uifrontend.md).
* **Web-App-fähig:** Verwenden Sie für Websites, die [React](uifrontend-react.md) oder [Angular](uifrontend-angular.md) verwenden, das [SPA-SDK](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/hybrid/developing.html?lang=de), um die [kontextbezogene Inhaltserstellung der App](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html?lang=de) beizubehalten.
* **Commerce aktiviert:** Für Projekte, die [AEM Commerce](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/home.html?lang=de) mithilfe der [Commerce-Kernkomponenten](https://github.com/adobe/aem-core-cif-components) mit Commerce-Lösungen wie [Magento](https://magento.com/de) integrieren möchten.
* **Beispiel-Code:** Sehen Sie sich die Komponente „HelloWorld“ und die Beispielmodelle, -Servlets, -filter und -planungen an.
* **Open Source:** Wenn etwas nicht so ist, wie es sein sollte, [bringen](https://github.com/adobe/aem-core-wcm-components/blob/master/CONTRIBUTING.md) Sie Ihre Verbesserungen ein!

## Nutzung {#usage}

Passen Sie die folgende Befehlszeile an Ihre Anforderungen an, um ein Projekt zu erstellen:

```shell
mvn -B org.apache.maven.plugins:maven-archetype-plugin:3.2.1:generate \
 -D archetypeGroupId=com.adobe.aem \
 -D archetypeArtifactId=aem-project-archetype \
 -D archetypeVersion=XX \
 -D appTitle="My Site" \
 -D appId="mysite" \
 -D groupId="com.mysite" \
```

* Ersetzen Sie `XX` durch die neueste [Archetyp-Versionsnummer](#requirements).
* Legen Sie `aemVersion=cloud` für [AEM as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/landing/home.html?lang=de) fest.\
   Legen Sie `aemVersion=6.5.0` für [Adobe Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams) oder On-Premise fest.
Die Abhängigkeit der Kernkomponenten wird nur für AEM-Versionen ohne Cloud Service hinzugefügt, da die Kernkomponenten für AEM as a Cloud Service standardmäßig bereitgestellt werden.
* Passen Sie `appTitle="My Site"` an, um den Titel der Website und die Komponentengruppen festzulegen.
* Passen Sie `appId="mysite"` an, um die Maven-Artefakt-ID (artifactId), die Namen der Komponenten-, Konfigurations- und Inhaltsordner sowie die Namen der Client-Bibliotheken festzulegen.
* Passen Sie `groupId="com.mysite"` an, um die Maven-Gruppen-ID (groupId) und das Java-Quellpaket festzulegen.
* Durchsuchen Sie die Liste der verfügbaren Eigenschaften, um festzustellen, ob Sie weitere anpassen möchten.

## Verfügbare Eigenschaften {#available-properties}

| Name | Standard | Beschreibung |
|---------------------------|----------------|--------------------|
| `appTitle` |  | Der Titel der App; wird für den Titel der Website und die Komponentengruppen verwendet (z. B. `"My Site"`). |
| `appId` |  | Technischer Name; wird für Komponenten-, Konfigurations- und Inhaltsordnernamen sowie die Namen der Client-Bibliotheken verwendet (z. B. `"mysite"`). |
| `artifactId` | *`${appId}`* | Maven-Basisartefakt-ID (z. B. `"mysite"`). |
| `groupId` |  | Maven-Basisgruppen-ID (z. B. `"com.mysite"`). Dieser Wert muss ein [gültiger Java-Paketname](https://docs.oracle.com/javase/specs/jls/se6/html/packages.html#7.7) sein. |
| `package` | *`${groupId}`* | Java-Quellpaket (z. B. `"com.mysite"`). |
| `version` | `1.0-SNAPSHOT` | Projektversion (z. B. `1.0-SNAPSHOT`). |
| `aemVersion` | `cloud` | Ziel-AEM-Version (kann `cloud` für [AEM as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/landing/home.html?lang=de) sein; oder `6.5.0` oder `6.4.4` für [Adobe Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams) oder On-Premise). |
| `sdkVersion` | `latest` | Wenn `aemVersion=cloud`, dann kann eine [SDK](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-as-a-cloud-service-sdk.html?lang=de)-Version angegeben werden (z. B. `2020.02.2265.20200217T222518Z-200130`). |
| `includeDispatcherConfig` | `y` | Enthält eine Dispatcher-Konfiguration für Cloud oder für AMS/On-Premise, je nach dem Wert von `aemVersion` (kann `y` oder `n` sein). |
| `frontendModule` | `general` | Enthält ein WebPack-Frontend-Build-Modul, das die Client-Bibliotheken generiert (kann `general` oder `none` für reguläre Websites sein; kann `angular` oder `react` für eine Single Page App sein, die den [SPA-Editor](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/hybrid/editor-overview.html?lang=de) implementiert). |
| `language` | `en` | Sprachcode (ISO 639-1) zur Erstellung der Inhaltsstruktur (z. B. aus `en`, `deu`). |
| `country` | `us` | Ländercode (ISO 3166-1) zur Erstellung der Inhaltsstruktur (z. B. aus `US`). |
| `singleCountry` | `y` | Enthält eine Inhaltsstruktur für den Sprach-Master (kann `y` oder `n` sein). |
| `includeExamples` | `n` | Enthält eine Beispiel-Website für die [Komponentenbibliothek](https://www.aemcomponents.dev/) (kann `y` oder `n` sein). |
| `includeErrorHandler` | `n` | Enthält eine benutzerdefinierte 404-Antwortseite, die für die gesamte Instanz global ist (kann `y` oder `n` sein). |
| `includeCommerce` | `n` | Enthält [CIF-Kernkomponenten](https://github.com/adobe/aem-core-cif-components)-Abhängigkeiten und generiert entsprechende Artefakte. |
| `commerceEndpoint` |  | Nur für CIF erforderlich. Optionaler Endpunkt des zu verwendenden GraphQL-Service (z. B. `https://hostname.com/grapql`). |
| `includeFormscommunications` | `n` | Enthält Abhängigkeiten, Vorlagen, Formulardatenmodelle und Designs für [Forms-Kernkomponenten](https://github.com/adobe/aem-core-forms-components) und generiert entsprechende Artefakte für Forms-Kommunikations-Programme. |
| `includeFormsenrollment` | `n` | Enthält Abhängigkeiten, Vorlagen, Formulardatenmodelle und Designs für [Forms-Kernkomponenten](https://github.com/adobe/aem-core-forms-components) und generiert entsprechende Artefakte für Forms-Registrierungs-Programme. |
| `sdkFormsVersion` | `latest` | Wenn `aemVersion=cloud` und eines von `includeFormsenrollment=y` oder `includeFormscommunications=y`, kann eine Forms SDK-Version angegeben werden (z. B. `2020.12.17.02`). |
| `datalayer` | `y` | Aktivieren Sie die Integration mit der [Adobe Client-Datenschicht](/help/developing/data-layer/overview.md). |
| `amp` | `n` | Aktivieren Sie [AMP](/help/developing/amp.md)-Unterstützung für erstellte Projektvorlagen. |
| `enableDynamicMedia` | `n` | Aktiviert die Foundation-Komponenten von Dynamic Media in den Einstellungen der Projektrichtlinien und aktiviert Dynamic Media-Funktionen in der Richtlinie der Kernbildkomponente. |
| `enableSSR` | `n` | Option zum Aktivieren von SSR für das Frontend-Projekt |
| `precompiledScripts` | `n` | Option zum [Vorkompilieren](/help/developing/archetype/precompiled-bundled-scripts.md) der Server-seitigen Skripte von `ui.apps` und Anfügen dieser Skripte an den Build als sekundäres Paket-Artefakt im `ui.apps`-Projekt. `aemVersion` sollte auf `cloud` gesetzt werden. |
| `includeFormsheadless` | `n` | Enthält Abhängigkeiten von [Forms-Kernkomponenten](https://github.com/adobe/aem-core-forms-components), `ui.frontend.react.forms.af` und Headless-Artefakte. |

## Systemanforderungen {#requirements}

| Archetyp | AEM as a Cloud Service | AEM 6.5 | Java SE | Maven |
|---------|---------|---------|---------|---------|
| [40](https://github.com/adobe/aem-project-archetype/releases/tag/aem-project-archetype-40) | Kontinuierlich | 6.5.7.0+ | 8, 11 | 3.3.9+ |

Richten Sie Ihre lokale Entwicklungsumgebung für das [AEM as a Cloud Service-SDK](https://experienceleague.adobe.com/docs/experience-manager-learn/cloud-service/local-development-environment-set-up/overview.html?lang=de) oder [ältere Versionen von AEM](https://experienceleague.adobe.com/docs/experience-manager-learn/foundation/development/set-up-a-local-aem-development-environment.html?lang=de) ein.

### Bekannte Probleme {#known-issues}

Bei Ausführung unter Windows und Generierung der Dispatcher-Konfiguration sollte die Ausführung in einer Eingabeaufforderung mit erhöhten Rechten oder im Windows-Subsystem für Linux erfolgen (siehe [Nr. 329](https://github.com/adobe/aem-project-archetype/issues/329)).

Wenn Sie den Archetyp im interaktiven Modus (ohne den Parameter `-B`) ausführen, können die Eigenschaften mit Standardwerten nicht geändert werden, es sei denn, die endgültige Bestätigung wird verworfen, wodurch die Fragen wiederholt und die Eigenschaften mit Standardwerten in die Fragen aufgenommen werden (Details siehe
[ARCHETYPE-308](https://issues.apache.org/jira/browse/ARCHETYPE-308)).

Sie können diesen Archetyp nicht in Eclipse verwenden, wenn Sie ein neues Projekt mit `File -> New -> Maven Project` starten, da das Post-Generation-Skript `archetype-post-generate.groovy` aufgrund eines Problems mit [Eclipse nicht ausgeführt wird.](https://bugs.eclipse.org/bugs/show_bug.cgi?id=514993) Die Lösung besteht darin, die oben genannte Befehlszeile zu verwenden und dann in Eclipse `File -> Import -> Existing Maven Project` zu verwenden.

## Weiterführende Literatur {#further-reading}

Weitere Informationen zur Verwendung des Archetyps, einschließlich der Vorteile, Optionen und der Funktionsweise der Module, finden Sie im Dokument [Verwenden des Archetyps](using.md).
