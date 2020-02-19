---
title: Front-End-Build für Angular-SPAs
description: Beschreibung des Front-End-Build-Prozesses für angular-basierte SPA-Projekte
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# Front-End-Build für Angular-SPAs {#frontend-angular}

In diesem Dokument werden die Details des Projekts erläutert, das beim Erstellen einer Einzelseitenanwendung (SPA) auf Basis des Angular-Frameworks mit dem Archetyp erstellt wurde. Das heißt, wenn Sie die `frontendModule` Option auf `angular`.

## Überblick {#overview}

Dieses Projekt wurde mit der [Angular-CLI](https://github.com/angular/angular-cli)ausgestattet.

Diese Anwendung wurde entwickelt, um das AEM-Modell einer Site zu verwenden. Das Layout wird automatisch mit den Hilfekomponenten aus dem Paket [@adobe/cq-angular-editable-components](https://www.npmjs.com/package/@adobe/cq-angular-editable-components) generiert.

## Skripten {#scripts}

Im Projektverzeichnis können Sie die folgenden Befehle ausführen.

### npm start {#npm-start}

```
npm start
```

Mit diesem Befehl wird die App im Entwicklungsmodus ausgeführt, indem das JSON-Modell von einer lokalen AEM-Instanz proxiert wird, die unter http://localhost:4502 ausgeführt wird. Hierbei wird davon ausgegangen, dass das gesamte Projekt mindestens einmal (`mvn clean install -PautoInstallPackage` im Projektstamm) in AEM bereitgestellt wurde.

Nachdem Sie npm im Verzeichnis ui.frontend ausgeführt haben, wird Ihre App automatisch im Browser geöffnet (unter dem Pfad http://localhost:4200/content/${appId}/${country}/${language}/home.html). Wenn Sie Änderungen vornehmen, wird die Seite neu geladen.

Wenn Sie Fehler im Zusammenhang mit CORS erhalten, sollten Sie AEM wie folgt konfigurieren:

1. Navigieren Sie zum Configuration Manager (http://localhost:4502/system/console/configMgr).
1. Öffnen Sie die Konfiguration für &quot;Adobe Granite Cross-Origin Resource Sharing Policy&quot;
1. Erstellen Sie eine neue Konfiguration mit den folgenden zusätzlichen Werten:
   * Zulässige Herkunft: http://localhost:4200
   * Unterstützte Kopfzeilen: Genehmigung
   * Zulässige Methoden: OPTIONEN

### npm-Test {#npm-test}

```
npm test
```

Mit diesem Befehl wird der Karma-Testlauf gestartet. Weitere Informationen finden Sie in der [Angular-Dokumentation zum Ausführen von Tests](https://angular.io/guide/testing) .

### npm run test:debug {#npm-run-test-debug}

```
npm run test:debug
```

Mit diesem Befehl wird der Karma-Test-Läufer im interaktiven Überwachungsmodus gestartet.

### npm run build {#npm-run-build}

```
npm run build
```

Mit diesem Befehl wird die App für die Produktion im Ordner Build erstellt. Es bündelt Angular im Produktionsmodus und optimiert den Build für die beste Leistung. Weitere Informationen finden Sie in der [Angular-Dokumentation zur Bereitstellung](https://angular.io/guide/deployment) .

Darüber hinaus wird eine AEM ClientLib aus der App mithilfe des [aem-clientlib-generator](https://github.com/wcm-io-frontend/aem-clientlib-generator) -Pakets generiert.

Weitere Informationen zur Verwendung von AEM ClientLibs durch den Projektarchiv finden Sie in der allgemeinen Dokumentation[ zum Modul ](uifrontend.md#clientlibs)ui.frontend.

## Browserunterstützung {#browser-support}

Standardmäßig verwendet dieses Projekt die Standardoption von [BrowserList](https://github.com/browserslist/browserslist), um Zielbrowser zu identifizieren. Zusätzlich enthält es Polyfills für moderne Sprachfunktionen, um ältere Browser (z.B. Internet Explorer 11) zu unterstützen. Wenn die Unterstützung solcher Browser nicht erforderlich ist, können die Polyfill-Abhängigkeiten und Importe entfernt werden.
