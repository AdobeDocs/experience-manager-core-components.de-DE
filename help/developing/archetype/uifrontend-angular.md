---
title: Front-End-Build für Angular-SPAs
description: Beschreibung des Front-End-Build-Prozesses für Angular-basierte SPA-Projekte
feature: Kernkomponenten, AEM-Projektarchetyp
role: Architect, Developer, Admin
exl-id: 5726e29d-081c-42bb-bf4e-2852043b21d6
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 100%

---

# Front-End-Build für Angular-SPAs {#frontend-angular}

In diesem Dokument werden die Details des Projekts erläutert, das erstellt wird, wenn mithilfe des Archetyps eine Single Page Application (SPA) basierend auf dem Angular Framework erstellt wird, das heißt, wenn Sie die Option `frontendModule` auf `angular` festlegen.

## Übersicht {#overview}

Dieses Projekt nutzt die [Angular-CLI](https://github.com/angular/angular-cli) per Bootstrapping.

Dieses Programm verarbeitet das AEM-Modell einer Site und generiert automatisch das Layout mit den Hilfekomponenten des Pakets [@adobe/cq-angular-editable-components](https://www.npmjs.com/package/@adobe/cq-angular-editable-components).

## Skripte {#scripts}

Im Projektverzeichnis können Sie die folgenden Befehle ausführen.

### npm start {#npm-start}

```
npm start
```

Mit diesem Befehl wird die App im Entwicklungsmodus ausgeführt, indem eine lokale AEM-Instanz, die unter http://localhost:4502 ausgeführt wird, als Proxy des JSON-Modells fungiert. Dabei wird davon ausgegangen, dass das gesamte Projekt mindestens einmal in AEM bereitgestellt wurde (`mvn clean install -PautoInstallPackage` im Projektstamm).

Nachdem Sie „npm start“ im ui.frontend-Verzeichnis ausgeführt haben, wird Ihre App automatisch im Browser geöffnet (unter dem Pfad http://localhost:4200/content/${appId}/${country}/${language}/home.html). Wenn Sie Änderungen vornehmen, wird die Seite neu geladen.

Falls Fehler im Zusammenhang mit CORS auftreten, sollten Sie AEM wie folgt konfigurieren:

1. Navigieren Sie zum Konfigurations-Manager (http://localhost:4502/system/console/configMgr).
1. Öffnen Sie die Konfiguration für „Adobe Granite Cross-Origin Resource Sharing Policy“.
1. Erstellen Sie eine neue Konfiguration mit den folgenden zusätzlichen Werten:
   * Zulässiger Ursprung: http://localhost:4200
   * Unterstützte Header: Authorization
   * Zulässige Methoden: OPTIONS

### npm test {#npm-test}

```shell
npm test
```

Mit diesem Befehl wird der Karma-Test-Runner gestartet. Weitere Informationen finden Sie in der [Angular-Dokumentation zum Ausführen von Tests](https://angular.io/guide/testing).

### npm run test:debug {#npm-run-test-debug}

```shell
npm run test:debug
```

Mit diesem Befehl wird der Karma-Test-Runner im interaktiven Überwachungsmodus gestartet.

### npm run build {#npm-run-build}

```shell
npm run build
```

Mit diesem Befehl wird die App für die Produktion im Build-Ordner erstellt. Er integriert Angular im Produktionsmodus und optimiert den Build für die beste Leistung. Weitere Informationen finden Sie in der [Angular-Dokumentation zur Bereitstellung](https://angular.io/guide/deployment).

Darüber hinaus wird eine AEM ClientLib aus der App mithilfe des Pakets [aem-clientlib-generator](https://github.com/wcm-io-frontend/aem-clientlib-generator) generiert.

Weitere Informationen zur Verwendung von AEM ClientLibs durch den Projektarchetyp finden Sie in der allgemeinen [Dokumentation zum ui.frontend-Modul](uifrontend.md#clientlibs).

## Browserunterstützung {#browser-support}

Standardmäßig verwendet dieses Projekt die Standardoption von [Browserslist](https://github.com/browserslist/browserslist), um Zielbrowser zu identifizieren. Zusätzlich enthält es Polyfills für moderne Sprachfunktionen, um ältere Browser (z. B. Internet Explorer 11) zu unterstützen. Wenn die Unterstützung solcher Browser nicht erforderlich ist, können die Polyfill-Abhängigkeiten und Importe entfernt werden.
