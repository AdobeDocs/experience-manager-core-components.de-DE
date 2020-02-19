---
title: Front-End-Build für React-SPAs
description: Beschreibung des Front-End-Build-Prozesses für react-basierte SPA-Projekte
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# Front-End-Build für React-SPAs {#frontend-react}

In diesem Dokument werden die Details des Projekts erläutert, das erstellt wurde, wenn mithilfe des Archetyps eine Einzelseitenanwendung (SPA) basierend auf dem React Framework erstellt wurde. Das heißt, wenn Sie die `frontendModule` Option auf `react`.

## Überblick {#overview}

Dieses Projekt wurde mit einer [create-response-App](https://github.com/facebook/create-react-app)im Bootstrapping-Format ausgestattet.

Diese Anwendung wurde entwickelt, um das AEM-Modell einer Site zu verwenden. Das Layout wird automatisch mit den Hilfekomponenten des Pakets [@adobe/cq-response-editable-components](https://www.npmjs.com/package/@adobe/cq-react-editable-components) generiert.

## Skripten {#scripts}

Im Projektverzeichnis können Sie die folgenden Befehle ausführen:

### npm start {#npm-start}

```
npm start
```

Mit diesem Befehl wird die App im Entwicklungsmodus ausgeführt, indem das JSON-Modell von einer lokalen AEM-Instanz proxiert wird, die unter http://localhost:4502 ausgeführt wird. Hierbei wird davon ausgegangen, dass das gesamte Projekt mindestens einmal (`mvn clean install -PautoInstallPackage` im Projektstamm) in AEM bereitgestellt wurde.

Nach der Ausführung `npm start` im Ordner &quot; [ui.frontend](uifrontend.md) &quot;wird Ihre App automatisch im Browser geöffnet (unter Pfad `http://localhost:3000/content/<appId>/<country>/<language>/home.html`). Wenn Sie Änderungen vornehmen, wird die Seite neu geladen.

Wenn Sie Fehler im Zusammenhang mit CORS erhalten, sollten Sie AEM wie folgt konfigurieren:

1. Navigieren Sie zum Configuration Manager (http://localhost:4502/system/console/configMgr).
1. Öffnen Sie die Konfiguration für &quot;Adobe Granite Cross-Origin Resource Sharing Policy&quot;
1. Erstellen Sie eine neue Konfiguration mit den folgenden zusätzlichen Werten:
   * Zulässige Herkunft: http://localhost:3000
   * Unterstützte Kopfzeilen: Genehmigung
   * Zulässige Methoden: OPTIONEN

### npm-Test {#npm-test}

```
npm test
```

Mit diesem Befehl wird der Testlauf im interaktiven Überwachungsmodus gestartet. Weitere Informationen finden Sie in der [React-Dokumentation zum Ausführen von Tests](https://facebook.github.io/create-react-app/docs/running-tests) .

### npm run build {#npm-run-build}

```
npm run build
```

Mit diesem Befehl wird die App für die Produktion im Ordner Build erstellt. Es bündelt React im Produktionsmodus und optimiert den Build für die beste Leistung. Weitere Informationen finden Sie in der Dokumentation [React zur Bereitstellung](https://facebook.github.io/create-react-app/docs/deployment) .

Darüber hinaus wird eine AEM ClientLib aus der App mithilfe des [aem-clientlib-generator](https://github.com/wcm-io-frontend/aem-clientlib-generator) -Pakets generiert.

## Browserunterstützung {#browser-support}

Standardmäßig verwendet dieses Projekt die Standardoption von [BrowserList](https://github.com/browserslist/browserslist), um Zielbrowser zu identifizieren. Zusätzlich enthält es Polyfills für moderne Sprachfunktionen, um ältere Browser (z.B. Internet Explorer 11) zu unterstützen. Wenn die Unterstützung solcher Browser nicht erforderlich ist, können die Polyfill-Abhängigkeiten und Importe entfernt werden.

## Codeaufteilung {#code-splitting}

Die React-App ist so konfiguriert, dass standardmäßig [Codeteilung](https://webpack.js.org/guides/code-splitting) verwendet wird. Beim Erstellen der App für die Produktion wird der Code in mehreren Abschnitten ausgegeben:

```
$ ls build/static/js
2.5b77f553.chunk.js
2.5b77f553.chunk.js.map
main.cff1a559.chunk.js
main.cff1a559.chunk.js.map
runtime~main.a8a9905a.js
runtime~main.a8a9905a.js.map
```

Das Laden von Abschnitten nur bei Bedarf kann die App-Leistung erheblich verbessern.

Damit diese Funktion mit AEM verwendet werden kann, muss die App ermitteln können, welche JS- und CSS-Dateien aus dem von AEM generierten HTML angefordert werden müssen. Dies kann mit dem Schlüssel &quot;entrypoints&quot;in der Datei asset-manifest.json erreicht werden. Die Datei wird in clientlib.config.js analysiert und nur die Einstiegspunktdateien werden in die ClientLib gebündelt. Die verbleibenden Dateien werden im Ressourcenverzeichnis von ClientLib abgelegt und werden dynamisch angefordert und daher erst geladen, wenn sie tatsächlich benötigt werden.

Weitere Informationen zur Verwendung von AEM ClientLibs durch den Projektarchiv finden Sie in der allgemeinen Dokumentation[ zum Modul ](uifrontend.md#clientlibs)ui.frontend.
