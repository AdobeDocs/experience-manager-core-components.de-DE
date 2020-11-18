---
title: AEM-Projektarchetyp
description: Eine Projektvorlage für AEM-basierte Anwendungen
translation-type: tm+mt
source-git-commit: c9ec069a9eb12b8625be09d1c38dcaaf437bd5cb
workflow-type: tm+mt
source-wordcount: '1280'
ht-degree: 81%

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
* Die folgenden Tutorials basieren auf diesem Archetyp:
   * **[WKND-Site:](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)** Erfahren Sie, wie eine neue Website beginnen.
   * **[WKND Single Page App:](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html)** Erfahren Sie, wie Sie eine Web-App für React oder Angular erstellen, die vollständig in AEM erstellt werden kann.

## Funktionen {#features}

* **Best Practice:** Laden Sie Ihre Website mit den neuesten empfohlenen Verfahren von Adobe.
* **Wenig Code:** Bearbeiten Sie Ihre Vorlagen, erstellen Sie Inhalte, stellen Sie Ihre CSS bereit und Ihre Website kann live geschaltet werden.
* **Cloud-fähig:** Falls gewünscht, verwenden Sie [AEM as a Cloud Service](https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/landing/home.translate.html), um in wenigen Tagen live zu gehen und Skalierbarkeit und Wartung zu erleichtern.
* **Dispatcher:** Ein Projekt ist nur mit einer [Dispatcher-Konfiguration](https://docs.adobe.com/content/help/de-DE/experience-manager-dispatcher/using/dispatcher.html), die Geschwindigkeit und Sicherheit gewährleistet, abgeschlossen.
* **Mehrere Websites:** Bei Bedarf generiert der Archetyp die Inhaltsstruktur für eine [Konfigurationen mit mehreren Sprachen und Regionen](https://docs.adobe.com/content/help/de-DE/experience-manager-65/administering/introduction/msm.html).
* **Kernkomponenten:** Autoren können mit unserem vielseitigen [Satz standardisierter Komponenten](/help/introduction.md) nahezu jedes Layout erstellen.
* **Bearbeitbare Vorlagen:** Stellen Sie praktisch jede [Vorlage ohne Code](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/page-authoring/template-editor-feature-video-use.html) zusammen und legen Sie fest, was die Autoren bearbeiten dürfen.
* **Responsives Layout:** Definieren Sie auf Vorlagen oder einzelnen Seiten, [wie die Elemente die definierten Breakpoints umfließen](https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/sites/authoring/features/responsive-layout.translate.html).
* **Kopf- und Fußzeile:** Stellen Sie sie mithilfe der [Lokalisierungsfunktionen der Komponenten](https://docs.adobe.com/content/help/de-DE/experience-manager-core-components/using/get-started/localization.html) ohne Code zusammen und lokalisieren Sie sie.
* **Stilsystem:** Vermeiden Sie das Erstellen benutzerdefinierter Komponenten, indem Autoren [verschiedene Stile anwenden](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/style-system.html) können.
* **Frontend-Build:** Mit Webpack, TypeScript und SASS können Frontend-Entwickler [AEM-Seiten modellieren](uifrontend.md#webpack-dev-server) und [Client-Bibliotheken erstellen](uifrontend.md).
* **Web-App-fähig:** Verwenden Sie für Websites, die [React](uifrontend-react.md) oder [Angular](uifrontend-angular.md) verwenden, das [SPA-SDK](https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/implementing/headless/spa/developing.html), um die [kontextbezogene Inhaltserstellung der App](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html) beizubehalten.
* **Commerce aktiviert:** Für Projekte, die [AEM Commerce](https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/commerce/home.html) mithilfe der [Commerce-Kernkomponenten](https://github.com/adobe/aem-core-cif-components) mit Commerce-Lösungen wie [Magento](https://magento.com/de) integrieren möchten.
* **Beispiel-Code:** Sehen Sie sich die Komponente „HelloWorld“ und die Beispielmodelle, -Servlets, -filter und -planungen an.
* **Open Source:** Wenn etwas nicht so ist, wie es sein sollte, [bringen](https://github.com/adobe/aem-core-wcm-components/blob/master/CONTRIBUTING.md) Sie Ihre Verbesserungen ein!

## Nutzung

Passen Sie die folgende Befehlszeile an Ihre Anforderungen an, um ein Projekt zu erstellen:

```
mvn -B archetype:generate \
 -D archetypeGroupId=com.adobe.aem \
 -D archetypeArtifactId=aem-project-archetype \
 -D archetypeVersion=24 \
 -D appTitle="My Site" \
 -D appId="mysite" \
 -D groupId="com.mysite" \
```

* Legen Sie `aemVersion=cloud` für [AEM as a Cloud Service](https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/landing/home.translate.html) fest.\
   Legen Sie `aemVersion=6.5.0` für [Adobe Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams) oder On-Premise fest.
Die Abhängigkeit der Kernkomponenten wird nur für AEM-Versionen ohne Cloud Service hinzugefügt, da die Kernkomponenten für AEM as a Cloud Service standardmäßig bereitgestellt werden.
* Passen Sie `appTitle="My Site"` an, um den Titel der Website und die Komponentengruppen festzulegen.
* Passen Sie `appId="mysite"` an, um die Maven-Artefakt-ID (artifactId), die Namen der Komponenten-, Konfigurations- und Inhaltsordner sowie die Namen der Client-Bibliotheken festzulegen.
* Passen Sie `groupId="com.mysite"` an, um die Maven-Gruppen-ID (groupId) und das Java-Quellpaket festzulegen.
* Durchsuchen Sie die Liste der verfügbaren Eigenschaften, um festzustellen, ob Sie weitere anpassen möchten.

## Verfügbare Eigenschaften

| Name | Default | Beschreibung |
--------------------------|----------------|--------------------
| `appTitle` |  | Der Titel der App; wird für den Titel der Website und die Komponentengruppen verwendet (z. B. `"My Site"`). |
| `appId` |  | Technischer Name; wird für Komponenten-, Konfigurations- und Inhaltsordnernamen sowie die Namen der Client-Bibliotheken verwendet (z. B. `"mysite"`). |
| `artifactId` | *`${appId}`* | Maven-Basisartefakt-ID (z. B. `"mysite"`). |
| `groupId` |  | Maven-Basisgruppen-ID (z. B. `"com.mysite"`). |
| `package` | *`${groupId}`* | Java-Quellpaket (z. B. `"com.mysite"`). |
| `version` | `1.0-SNAPSHOT` | Projektversion (z. B. `1.0-SNAPSHOT`). |
| `aemVersion` | `cloud` | Ziel-AEM-Version (kann `cloud` für [AEM as a Cloud Service](https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/landing/home.translate.html) sein; oder `6.5.0` oder `6.4.4` für [Adobe Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams) oder On-Premise). |
| `sdkVersion` | `latest` | Wenn `aemVersion=cloud`, dann kann eine [SDK](https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/implementing/developing/aem-as-a-cloud-service-sdk.html)-Version angegeben werden (z. B. `2020.02.2265.20200217T222518Z-200130`). |
| `includeDispatcherConfig` | `y` | Enthält eine Dispatcher-Konfiguration für Cloud oder für AMS/On-Premise, je nach dem Wert von `aemVersion` (kann `y` oder `n` sein). |
| `frontendModule` | `general` | Enthält ein WebPack-Frontend-Build-Modul, das die Client-Bibliotheken generiert (kann `general` oder `none` für reguläre Websites sein; kann `angular` oder `react` für eine Single Page App sein, die den [SPA-Editor](https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/implementing/headless/spa/editor-overview.html) implementiert). |
| `language` | `en` | Sprachcode (ISO 639-1) zur Erstellung der Inhaltsstruktur (z. B. aus `en`, `deu`). |
| `country` | `us` | Ländercode (ISO 3166-1) zur Erstellung der Inhaltsstruktur (z. B. aus `US`). |
| `singleCountry` | `y` | Enthält eine Inhaltsstruktur für den Sprach-Master (kann `y` oder `n` sein). |
| `includeExamples` | `n` | Enthält eine Beispiel-Website für die [Komponentenbibliothek](https://www.aemcomponents.dev/) (kann `y` oder `n` sein). |
| `includeErrorHandler` | `n` | Enthält eine benutzerdefinierte 404-Antwortseite, die für die gesamte Instanz global ist (kann `y` oder `n` sein). |
| `includeCommerce` | `n` | Enthält [CIF-Kernkomponenten](https://github.com/adobe/aem-core-cif-components)-Abhängigkeiten und generiert entsprechende Artefakte. |
| `commerceEndpoint` |  | Nur für CIF erforderlich. Optionaler Endpunkt des zu verwendenden GraphQL-Service (z. B. `https://hostname.com/grapql`). |
| `datalayer` | `y` | Aktivieren Sie die Integration mit der [Adobe Client-Datenschicht](/help/developing/data-layer/overview.md). |
| `amp` | `n` | Aktivieren Sie [AMP](/help/developing/amp.md)-Unterstützung für erstellte Projektvorlagen. |

## Analyzer-Modul {#analyzer-module}

Das AEM-Analyse-Plugin Maven analysiert die Struktur der verschiedenen Inhaltspaketprojekte.

Informationen dazu, wie Sie es in ein AEM Maven-Projekt einbeziehen, finden Sie in der Dokumentation [zum](https://github.com/adobe/aemanalyser-maven-plugin/blob/main/aemanalyser-maven-plugin/README.md) AEM Analyzer Maven Plugin. Das Plugin ist in AEM Maven Archetype Version 25 und höher enthalten.

Nachstehend finden Sie eine Tabelle mit den Analyzern, die im Rahmen dieses Schritts ausgeführt werden. Beachten Sie, dass einige im lokalen SDK ausgeführt werden, während andere nur während der Cloud Manager-Pipeline-Bereitstellung ausgeführt werden.

| Modul | Funktion, Beispiel und Fehlerbehebung | Lokales SDK | Cloud Manager |
|---|---|---|---|
| `api-regions-exportsimports` | Überprüft, ob alle OSGI-Pakete ihre Import-Paket-Erklärungen haben, die mit der Ausfuhrpaket-Erklärung anderer im Maven-Projekt eingeschlossener Pakete übereinstimmen. <p> </p> Um eine Fehlerbehebung durchzuführen, überprüfen Sie das Manifest des Bundles, das Sie beim Export erwarten würden, um festzustellen, ob der falsche Name oder die falsche Version verwendet wurde. | Ja | Ja |
| `requirements-capabilities` | Überprüft, ob alle in OSGI-Bundles abgegebenen Anforderungsdeklarationen durch die Leistungsdeklarationen anderer im Maven-Projekt enthaltener Bundles erfüllt werden. <p> </p> Um eine Fehlerbehebung durchzuführen, sehen Sie sich das Manifest des Bundles an, das Sie vermutlich als Funktion zur Bestimmung des Fehlens des Bundles deklarieren würden. | Ja | Ja |
| `bundle-content` | Gibt eine Warnung aus, wenn ein Bundle anfänglichen Inhalt enthält, der mit Sling-Initial-Content angegeben wurde. Dies ist problematisch in der AEM als Cloud Service-Cluster-Umgebung. | Ja | Ja |
| `api-regions-crossfeature-dups` | Prüft, ob die OSGI-Pakete des Kunden keine Exportpaket-Deklarationen haben, die AEM als öffentliche API des Cloud Service außer Kraft setzen | Ja | Ja |

## Systemanforderungen

| Archetyp | AEM as a Cloud Service | AEM 6.5 | AEM 6.4 | Java SE | Maven |
|---------|---------|---------|---------|---------|---------|
| [24](https://github.com/adobe/aem-project-archetype/releases/tag/aem-project-archetype-24) | Kontinuierlich | 6.5.5.0+ | 6.4.8.1+ | 8, 11 | 3.3.9+ |

Richten Sie Ihre lokale Entwicklungsumgebung für das [AEM as a Cloud Service-SDK](https://docs.adobe.com/content/help/en/experience-manager-learn/cloud-service/local-development-environment-set-up/overview.html) oder [ältere Versionen von AEM](https://docs.adobe.com/content/help/en/experience-manager-learn/foundation/development/set-up-a-local-aem-development-environment.html) ein.

### Bekannte Probleme

Bei Ausführung unter Windows und Generierung der Dispatcher-Konfiguration sollte die Ausführung in einer Eingabeaufforderung mit erhöhten Rechten oder im Windows-Subsystem für Linux erfolgen (siehe [Nr. 329](https://github.com/adobe/aem-project-archetype/issues/329)).

Wenn Sie den Archetyp im interaktiven Modus (ohne den Parameter `-B`) ausführen, können die Eigenschaften mit Standardwerten nicht geändert werden, es sei denn, die endgültige Bestätigung wird verworfen, wodurch die Fragen wiederholt und die Eigenschaften mit Standardwerten in die Fragen aufgenommen werden (Details siehe
[ARCHETYP-308](https://issues.apache.org/jira/browse/ARCHETYPE-308)).

## Weiterführende Literatur {#further-reading}

Weitere Informationen zur Verwendung des Archetyps, einschließlich der Vorteile, Optionen und der Funktionsweise der Module, finden Sie im Dokument [Verwenden des Archetyps](using.md).
