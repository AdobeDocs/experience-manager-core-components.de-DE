---
title: AEM Projektarchetyp Front-End-Build
description: Eine Projektvorlage für AEM-basierte Anwendungen
translation-type: ht
source-git-commit: 2926c51c2ab97b50b9ec4942cd5415c15a1411b6
workflow-type: ht
source-wordcount: '1622'
ht-degree: 100%

---


# ui.frontend-Modul des AEM-Projektarchetyps {#uifrontend-module}

Der AEM-Projektarchetyp enthält einen optionalen, dedizierten Front-End-Build-Mechanismus, der auf Webpack basiert. Das ui.frontend-Modul wird damit zum zentralen Speicherort für alle Front-End-Ressourcen des Projekts, einschließlich JavaScript- und CSS-Dateien. Um diese nützliche und flexible Funktion in vollem Umfang nutzen zu können, müssen Sie wissen, welchen Anteil die Front-End-Entwicklung an einem AEM-Projekt hat.

## AEM-Projekte und Front-End-Entwicklung {#aem-and-front-end-development}

In stark vereinfachten Begriffen kann davon ausgegangen werden, dass AEM-Projekte aus zwei separaten, aber miteinander verbundenen Teilen bestehen:

* Back-End-Entwicklung, die die Logik von AEM unterstützt und Java-Bibliotheken, OSGi-Dienste usw. produziert
* Front-End-Entwicklung, die die Präsentation und das Verhalten der resultierenden Website steuert und JavaScript- sowie CSS-Bibliotheken erzeugt

Da sich diese beiden Entwicklungsprozesse auf verschiedene Teile des Projekts konzentrieren, kann die Back-End- und Front-End-Entwicklung parallel erfolgen.

![Diagramm zum Front-End-Workflow](/help/assets/front-end-flow.png)

Jedes daraus resultierende Projekt muss jedoch die Ergebnisse beider Entwicklungsmaßnahmen nutzen, d. h. sowohl für das Back-End als auch für das Front-End.

Beim Ausführen von `npm run dev` wird der Front-End-Build-Prozess gestartet, der die im ui.frontend-Modul gespeicherten JavaScript- und CSS-Dateien erfasst und zwei minimierte Client-Bibliotheken (oder ClientLibs) namens `clientlib-site` und `clientlib-dependencies` erzeugt und im ui.apps-Modul ablegt. ClientLibs können in AEM bereitgestellt werden und ermöglichen die Speicherung des Client-seitigen Codes im Repository.

Wenn der gesamte AEM-Projektarchetyp mit `mvn clean install -PautoInstallPackage` ausgeführt wird, werden alle Projektartefakte einschließlich der ClientLibs an die AEM-Instanz gesendet.

>[!TIP]
>
>In der [AEM Entwicklungsdokumentation](https://docs.adobe.com/content/help/de-DE/experience-manager-65/developing/introduction/clientlibs.html) erfahren Sie mehr darüber, wie AEM mit ClientLibs umgeht und wie sie [eingeschlossen](/help/developing/including-clientlibs.md) werden. Außerdem erfahren Sie weiter unten, [wie das ui.frontend-Modul sie verwendet](#clientlib-generation).

## Überblick über ClientLibs {#clientlibs}

Das Frontend-Modul wird mithilfe einer [AEM ClientLib](https://docs.adobe.com/content/help/de-DE/experience-manager-65/developing/introduction/clientlibs.html) bereitgestellt. Beim Ausführen des NPM Build-Skripts wird die App erstellt und das aem-clientlib-generator-Paket nimmt die resultierende Buildausgabe entgegen und wandelt sie in eine solche ClientLib um.

Eine ClientLib besteht aus den folgenden Dateien und Verzeichnissen:

* `css/`: CSS-Dateien, die im HTML-Code angefordert werden können
* `css.txt`: Teilt AEM die Reihenfolge und Namen der Dateien in `css/` mit, damit sie zusammengeführt werden können
* `js/`: JavaScript-Dateien, die im HTML-Code angefordert werden können
* `js.txt`: Teilt AEM die Reihenfolge und Namen der Dateien in `js/` mit, damit sie zusammengeführt werden können
* `resources/`: Quellzuordnungen, Nicht-Einstiegspunkt-Codeblöcke (die aus der Codeaufteilung resultieren), statische Kreativelemente (z. B. Symbole) usw.

## Mögliche Front-End-Entwicklungs-Workflows {#possible-workflows}

Das Front-End-Build-Modul ist ein nützliches und sehr flexibles Werkzeug ohne spezielle Vorgaben dazu, wie es verwendet werden sollte. Im Folgenden finden Sie zwei Beispiele für die *mögliche* Verwendung, aber Ihre individuellen Projektanforderungen können andere Anwendungsmodelle erforderlich machen.

### Verwenden des statischen Webpack Development Servers {#using-webpack}

Mit Webpack können Sie auf Basis der statischen Ausgabe von AEM-Webseiten innerhalb des ui.frontend-Moduls formatieren und entwickeln.

1. Zeigen Sie eine Vorschau der Seite in AEM an oder geben Sie `wcmmode=disabled` in die URL ein.
1. Zeigen Sie die Seitenquelle an und speichern Sie diese als statischen HTML-Code im ui.frontend-Modul.
1. [Starten Sie Webpack](#webpack-dev-server) und beginnen Sie mit der Formatierung und Generierung des erforderlichen JavaScript- und CSS-Codes.
1. Führen Sie `npm run dev` zum Generieren der ClientLibs aus.

In diesem Workflow kann ein AEM-Entwickler die Schritte 1 und 2 ausführen sowie den statischen HTML-Code an den Front-End-Entwickler weiterleiten, der die AEM-HTML-Ausgabe zur Entwicklung nutzt.

>[!TIP]
>
>Man kann auch mit der [Komponentenbibliothek](https://adobe.com/go/aem_cmp_library_de) Beispiele der Markup-Ausgabe jeder Komponente erfassen, um auf Komponentenebene und nicht auf Seitenebene zu arbeiten.

### Verwenden von Storybook {#using-storybook}

Mit [Storybook](https://storybook.js.org) können Sie mehr atomare Front-End-Entwicklung durchführen. Obwohl Storybook nicht im AEM-Projektarchetyp enthalten ist, können Sie die Anwendung installieren und Ihre Storybook-Artefakte im ui.frontend-Modul speichern. Sobald diese für Tests in AEM bereit sind, können sie durch Ausführen von `npm run dev` als ClientLibs bereitgestellt werden.

>[!NOTE]
>
>[Storybook](https://storybook.js.org) ist nicht im AEM-Projektarchetyp enthalten. Wenn Sie die Anwendung verwenden möchten, müssen Sie sie separat installieren.

### Bestimmen des Markups {#determining-markup}

Unabhängig davon, welchen Front-End-Entwicklungs-Workflow Sie für Ihr Projekt implementieren, müssen sich die Back-End-Entwickler und Front-End-Entwickler zunächst auf das Markup einigen. In der Regel definiert AEM das Markup, das von den Core-Komponenten bereitgestellt wird. [Dies kann jedoch bei Bedarf angepasst werden.](/help/developing/customizing.md#customizing-the-markup)

## Das ui.frontend-Modul {#ui-frontend-module}

Das AEM-Projektarchiv enthält einen optionalen, dedizierten Front-End-Build-Mechanismus, der auf Webpack basiert und die folgenden Funktionen enthält.

* Vollständige Unterstützung für TypeScript, ES6 und ES5 (mit entsprechenden Webpack-Wrappern)
* TypeScript- und JavaScript-Linting mit einem TSLint-Regelsatz
* ES5-Ausgabe für ältere Browserunterstützung
* Globbing
   * Importe müssen nirgendwo hinzugefügt werden
   * Alle JS- und CSS-Dateien können jetzt jeder Komponente hinzugefügt werden.
      * Best Practice ist unter `/clientlib/js`, `/clientlib/css`oder `/clientlib/scss`
   * Die Dateien `.content.xml` oder `js.txt`/`css.txt` sind nicht erforderlich, da alles über Webpack ausgeführt wird.
   * Der Globber ruft alle JS-Dateien im `/component/` Ordner ab.
      * Mit Webpack können CSS/SCSS-Dateien über JS-Dateien verkettet werden.
      * Sie werden durch die beiden Einstiegspunkte eingezogen `sites.js` und `vendors.js`.
   * Die einzige Datei, die von AEM verwendet wird, sind die Ausgabedateien `site.js` und `site.css` in `/clientlib-site` sowie `dependencies.js` und `dependencies.css` in `/clientlib-dependencies`
* Blöcke
   * Main (site js/css)
   * Anbieter (Abhängigkeiten js/css)
* Vollständige Unterstützung von Sass/Scss (Sass wird über Webpack zu CSS kompiliert)
* Statischer Webpack Development Server mit integriertem Proxy zu einer lokalen AEM-Instanz

>[!NOTE]
>
>Weitere technische Informationen zum ui.frontend-Modul finden Sie in der [Dokumentation zu GitHub](https://github.com/adobe/aem-project-archetype/blob/master/src/main/archetype/ui.frontend.general/README.md).

## Installation {#installation}

1. Installieren Sie [NodeJS](https://nodejs.org/en/download/) (ab Version 10) global. Dadurch wird auch npm installiert.
1. Navigieren Sie in Ihrem Projekt zu ui.frontend und führen Sie `npm install`.

>[!NOTE]
>
>Um den ui.frontend-Ordner zu füllen, müssen Sie den [Archetyp ausführen](overview.md) und dabei die Option `-DoptionIncludeFrontendModule=y` verwenden.

## Verwendung {#usage}

Die folgenden npm-Skripten verhelfen zum Frontend-Arbeitsablauf:

* `npm run dev` - Vollständige Erstellung mit deaktivierter JS-Optimierung (Baum-Shaking usw.) und aktivierten Quellkarten und deaktivierter CSS-Optimierung.
* `npm run prod` - Vollständige Erstellung mit aktivierter JS-Optimierung (Baum-Shaking usw.), deaktivierter Quellzuordnung und aktivierter CSS-Optimierung.
* `npm run start` - Startet einen statischen Webpack Development Server für die lokale Entwicklung mit minimalen Abhängigkeiten von AEM.

## Ausgabe {#output}

Das ui.frontend-Modul kompiliert den Code unter dem Ordner `ui.frontend/src` und gibt den kompilierten CSS- und JS-Code sowie alle Ressourcen unter dem Ordner `ui.frontend/dist` aus.

* **Site** - `site.js`, `site.css` und ein Ordner `resources/` für Layout-abhängige Bilder und Schriftarten werden im Clientlib-Site-Ordner `dist/` erstellt.
* **Abhängigkeiten** - `dependencies.js` und `dependencies.css` werden in einem Ordner `dist/clientlib-dependencies` erstellt.

### JavaScript {#javascript}

* Optimierung: Bei Produktions-Builds werden alle nicht verwendeten oder aufgerufenen JS entfernt.

### CSS {#css}

* Autoprefixierung - Alle CSS werden über einen Präfixer ausgeführt und alle Eigenschaften, für die Präfix erforderlich ist, werden automatisch in das CSS eingefügt.
* Optimierung: Beim Posten wird das gesamte CSS über einen Optimierer (cssnano) ausgeführt, der es gemäß den folgenden Standardregeln normalisiert:
   * Reduziert den CSS-Calc-Ausdruck, wo immer dies möglich ist, und stellt sowohl die Browserkompatibilität als auch die Komprimierung sicher
Konvertiert Werte für die äquivalente Länge, Zeit und Winkel. Beachten Sie, dass Längenwerte standardmäßig nicht konvertiert werden.
   * Entfernt Kommentare in und um Regeln, Selektoren und Deklarationen
   * Entfernt duplizierte Regeln, at-Regeln und Deklarationen
      * Beachten Sie, dass dies nur bei exakten Duplikaten funktioniert.
   * Entfernt leere Regeln, Medienabfragen und Regeln mit leeren Selektoren, da sie sich nicht auf die Ausgabe auswirken
   * Führt benachbarte Regeln durch Selektoren und überlappende Eigenschaften-/Wertpaare zusammen
   * Stellt sicher, dass in der CSS-Datei nur ein einziges @charset vorhanden ist, und verschiebt es an den Anfang des Dokuments
   * Ersetzt den ersten CSS-Suchbegriff durch den tatsächlichen Wert, wenn die resultierende Ausgabe kleiner ist
   * Komprimiert inline-SVG-Definitionen mit SVGO
* Bereinigen - Umfasst explizite Bereinigungsaufgabe zum Entfernen der generierten CSS-, JS- und Map-Dateien bei Bedarf.
* Quellzuordnung - nur Entwicklungs-Build

>[!NOTE]
>
>Die Option zum Erstellen des Front-End verwendet Konfigurationsdateien des nur dev- und prod-only webpack, die eine gemeinsame Konfigurationsdatei gemeinsam haben. Auf diese Weise können Entwicklungs- und Produktionseinstellungen unabhängig verändert werden.

### Generieren der Client-Bibliothek {#clientlib-generation}

Der Prozess zum Erstellen des ui.frontend-Moduls nutzt das Plugin [aem-clientlib-generator](https://www.npmjs.com/package/aem-clientlib-generator), um den kompilierten CSS- und JS-Code sowie alle Ressourcen in das ui.apps-Modul zu verschieben. Die Konfiguration von aem-clientlib-generator ist in `clientlib.config.js` definiert. Die folgenden Client-Bibliotheken werden generiert:

* **clientlib-site** - `ui.apps/src/main/content/jcr_root/apps/<app>/clientlibs/clientlib-site`
* **clientlib-dependencies** - `ui.apps/src/main/content/jcr_root/apps/<app>/clientlibs/clientlib-dependencies`

### Einbinden von Client-Bibliotheken auf Seiten {#clientlib-inclusion}

Die Kategorien `clientlib-site` und `clientlib-dependencies` sind auf den Seiten über die [Seitenrichtlinien-Konfiguration](https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/implementing/components-templates/templates.html#template-definitions) als Teil der Standardvorlage enthalten. Um die Richtlinie anzuzeigen, bearbeiten Sie die **Inhaltsseitenvorlage > Seiteninformationen > Seitenrichtlinie**.

Die endgültige Einbindung von Client-Bibliotheken auf der Seite &quot;Sites&quot; erfolgt wie folgt:

```
<HTML>
    <head>
        <link rel="stylesheet" href="clientlib-base.css" type="text/css">
        <script type="text/javascript" src="clientlib-dependencies.js"></script>
        <link rel="stylesheet" href="clientlib-dependencies.css" type="text/css">
        <link rel="stylesheet" href="clientlib-site.css" type="text/css">
    </head>
    <body>
        ....
        <script type="text/javascript" src="clientlib-site.js"></script>
        <script type="text/javascript" src="clientlib-base.js"></script>
    </body>
</HTML>
```

Die oben genannte Einbindung kann natürlich durch Aktualisierung der Seitenrichtlinie bzw. Änderung der Kategorien und Einbettungseigenschaften der jeweiligen Client-Bibliotheken geändert werden.

### Statischer Webpack Development Server {#webpack-dev-server}

Im ui.frontend-Modul ist ein webpack-dev-server enthalten, der ein Live-Neuladen für eine schnelle Front-End-Entwicklung außerhalb von AEM ermöglicht. Das Setup nutzt das html-webpack-plugin, um aus dem ui.frontend-Modul kompilierten CSS- und JS-Code automatisch in eine statische HTML-Vorlage zu injizieren.

#### Wichtige Dateien {#important-files}

* `ui.frontend/webpack.dev.js`
   * Enthält die Konfiguration für webpack-dev-server und verweist auf die zu verwendende HTML-Vorlage.
   * Enthält außerdem eine Proxy-Konfiguration für eine AEM-Instanz, die auf localhost:4502 ausgeführt wird.
* `ui.frontend/src/main/webpack/static/index.html`
   * Dies ist der statische HTML-Code, der auf dem Server ausgeführt wird.
   * Dadurch kann ein Entwickler Änderungen am CSS-/JS-Code vornehmen und sie sofort im Markup anzeigen.
   * Es wird davon ausgegangen, dass das in dieser Datei platzierte Markup das von AEM-Komponenten generierte Markup exakt widerspiegelt.
   * Das Markup in dieser Datei wird nicht automatisch mit dem AEM-Komponenten-Markup synchronisiert.
   * Diese Datei enthält auch Verweise auf in AEM gespeicherte Client-Bibliotheken wie Core Component CSS und Responsive Grid CSS.
   * Der Webpack Development Server ist so eingerichtet, dass er diesen eingebundenen CSS-/JS-Code von einer lokalen AEM-Instanz basierend auf der Konfiguration in `ui.frontend/webpack.dev.js` im Proxy zwischenspeichert.

#### Verwendung {#using-webpack-server}

1. Führen Sie im Stammverzeichnis des Projekts den Befehl `mvn -PautoInstallSinglePackage clean install` aus, um das gesamte Projekt in einer AEM-Instanz zu installieren, die auf `localhost:4502` ausgeführt wird.
1. Wechseln Sie zum Ordner `ui.frontend`.
1. Führen Sie den Befehl `npm run start` aus, um den Webpack Development Server zu starten. Nach dem Start sollte ein Browser (`localhost:8080` oder der nächste verfügbare Port) geöffnet werden.

Sie können jetzt CSS-, JS-, SCSS- und TS-Dateien ändern und die Änderungen sofort im Webpack Development Server anzeigen.
