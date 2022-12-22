---
title: Frontend-Build für React-SPAs
description: Beschreibung des Frontend-Build-Prozesses für React-basierte SPA-Projekte
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: dd8ef13a-9686-47a9-b6af-e486ff10c4d8
source-git-commit: 0eea0cd65063c739e5b405b0380b73962a858e48
workflow-type: ht
source-wordcount: '512'
ht-degree: 100%

---

# Frontend-Build für React-SPAs {#frontend-react}

In diesem Dokument werden die Details des Projekts erläutert, das erstellt wird, wenn mithilfe des Archetyps eine Single Page Application (SPA) basierend auf dem React Framework erstellt wird, das heißt, wenn Sie die Option `frontendModule` auf `react` festlegen.

## Übersicht {#overview}

Dieses Projekt nutzt die [create-react-app](https://github.com/facebook/create-react-app) per Bootstrapping.

Dieses Programm verarbeitet das AEM-Modell einer Site und generiert automatisch das Layout mit den Hilfekomponenten des Pakets [@adobe/cq-response-editable-components](https://www.npmjs.com/package/@adobe/aem-react-editable-components).

## Skripte {#scripts}

Im Projektverzeichnis können Sie die folgenden Befehle ausführen:

### npm start {#npm-start}

```shell
npm start
```

Mit diesem Befehl wird die App im Entwicklungsmodus ausgeführt, indem eine lokale AEM-Instanz, die unter http://localhost:4502 ausgeführt wird, als Proxy des JSON-Modells fungiert. Dabei wird davon ausgegangen, dass das gesamte Projekt mindestens einmal in AEM bereitgestellt wurde (`mvn clean install -PautoInstallPackage` im Projektstamm).

Nach der Ausführung von `npm start` im Verzeichnis „[ui.frontend](uifrontend.md)“ wird Ihre App automatisch im Browser geöffnet (unter dem Pfad `http://localhost:3000/content/<appId>/<country>/<language>/home.html`). Wenn Sie Änderungen vornehmen, wird die Seite neu geladen.

Falls Fehler im Zusammenhang mit CORS auftreten, sollten Sie AEM wie folgt konfigurieren:

1. Navigieren Sie zum Konfigurations-Manager (http://localhost:4502/system/console/configMgr).
1. Öffnen Sie die Konfiguration für „Adobe Granite Cross-Origin Resource Sharing Policy“.
1. Erstellen Sie eine neue Konfiguration mit den folgenden zusätzlichen Werten:
   * Zulässiger Ursprung: http://localhost:3000
   * Unterstützte Header: Authorization
   * Zulässige Methoden: OPTIONS

### npm test {#npm-test}

```shell
npm test
```

Mit diesem Befehl wird der Test-Runner im interaktiven Überwachungsmodus gestartet. Weitere Informationen finden Sie in der [React-Dokumentation zum Ausführen von Tests](https://facebook.github.io/create-react-app/docs/running-tests).

### npm run build {#npm-run-build}

```shell
npm run build
```

Mit diesem Befehl wird die App für die Produktion im Build-Ordner erstellt. Sie integriert React im Produktionsmodus und optimiert den Build für die beste Leistung. Weitere Informationen finden Sie in der [React-Dokumentation zur Bereitstellung](https://facebook.github.io/create-react-app/docs/deployment).

Darüber hinaus wird eine AEM ClientLib aus der App mithilfe des Pakets [aem-clientlib-generator](https://github.com/wcm-io-frontend/aem-clientlib-generator) generiert.

## Browser-Unterstützung {#browser-support}

Standardmäßig verwendet dieses Projekt die Standardoption von [Browserslist](https://github.com/browserslist/browserslist), um Zielbrowser zu identifizieren. Zusätzlich enthält es Polyfills für moderne Sprachfunktionen, um ältere Browser (z. B. Internet Explorer 11) zu unterstützen. Wenn die Unterstützung solcher Browser nicht erforderlich ist, können die Polyfill-Abhängigkeiten und Importe entfernt werden.

## Code-Aufteilung {#code-splitting}

Die React-App ist so konfiguriert, dass sie standardmäßig [Codeaufteilung](https://webpack.js.org/guides/code-splitting) verwendet. Beim Erstellen der App für die Produktion wird der Code in mehreren Blöcken ausgegeben:

```shell
$ ls build/static/js
2.5b77f553.chunk.js
2.5b77f553.chunk.js.map
main.cff1a559.chunk.js
main.cff1a559.chunk.js.map
runtime~main.a8a9905a.js
runtime~main.a8a9905a.js.map
```

Das Laden von Blöcken nur bei Bedarf kann die App-Leistung erheblich verbessern.

Damit diese Funktion mit AEM verwendet werden kann, muss die App ermitteln können, welche JS- und CSS-Dateien aus dem von AEM generierten HTML-Code angefordert werden müssen. Dies kann mit dem Schlüssel „entrypoints“ in der Datei asset-manifest.json erreicht werden. Die Datei wird in clientlib.config.js analysiert und nur die Einstiegspunktdateien werden in die ClientLib gebündelt. Die verbleibenden Dateien werden im Ressourcenverzeichnis von ClientLib abgelegt und dynamisch angefordert, d. h. erst geladen, wenn sie tatsächlich benötigt werden.

Weitere Informationen zur Verwendung von AEM ClientLibs durch den Projektarchetyp finden Sie in der allgemeinen [Dokumentation zum ui.frontend-Modul](uifrontend.md#clientlibs).
