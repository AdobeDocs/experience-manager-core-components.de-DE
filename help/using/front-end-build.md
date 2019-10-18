---
title: AEM Project Archetype Front-End-Build
seo-title: AEM Project Archetype Front-End-Build
description: Eine Projektvorlage für AEM-basierte Anwendungen
seo-description: Eine Projektvorlage für AEM-basierte Anwendungen
contentOwner: Bohnert
content-type: Referenz
topic-tags: Kernkomponenten
translation-type: tm+mt
source-git-commit: 0a61f4e6d1ad8b4d5e3778018838dc70d496e1fc

---


# AEM Project Archetype Front-End-Build {#aem-project-archetype-front-end-build}

Der AEM-Projektarchiv enthält einen optionalen, dedizierten Front-End-Build-Mechanismus, der auf Webpack basiert und die folgenden Funktionen enthält.

* Vollständige Unterstützung für TypeScript, ES6 und ES5 (mit entsprechenden Webpack-Wrappern)
* TypeScript- und JavaScript-Linting mit einem TSLint-Regelsatz
* ES5-Ausgabe für ältere Browserunterstützung
* Globbing
   * Importe müssen nirgendwo hinzugefügt werden
   * Alle JS- und CSS-Dateien können jetzt jeder Komponente hinzugefügt werden
      * Best Practice ist unter `/clientlib/js`, `/clientlib/css`oder `/clientlib/scss`
   * Keine `.content.xml` oder `js.txt`/`css.txt` Dateien erforderlich, da alles über WebPack ausgeführt wird
   * Der Globber ruft alle JS-Dateien im `/component/` Ordner ab.
      * Mit WebPack können CSS/SCSS-Dateien über JS-Dateien verkettet werden.
      * Sie werden durch die beiden Einstiegspunkte eingezogen `sites.js` und `vendors.js`.
   * Die einzige Datei, die von AEM verwendet wird, sind die Ausgabedateien `site.js` und `site.css` in `/clientlib-site` sowie `dependencies.js` und `dependencies.css` in `/clientlib-dependencies`
* Blöcke
   * Main (site js/css)
   * Anbieter (Abhängigkeiten js/css)
* Vollständige Unterstützung von Sass/Scss (Sass wird über Webpack zu CSS kompiliert).

## Installation {#installation}

1. Installieren Sie [NodeJS](https://nodejs.org/en/download/) (ab Version 10) global. Dadurch wird auch npm installiert.
1. Navigieren Sie in Ihrem Projekt zu ui.frontend und führen Sie `npm install`.

## Nutzung {#usage}

Die folgenden npm-Skripten verhelfen zum Frontend-Arbeitsablauf:

* `npm run dev` - Vollständige Erstellung mit deaktivierter JS-Optimierung (Baum-Shaking usw.) und aktivierten Quellkarten und deaktivierter CSS-Optimierung.
* `npm run prod` - Vollständige Erstellung mit aktivierter JS-Optimierung (Baum-Shaking usw.), deaktivierter Quellzuordnung und aktivierter CSS-Optimierung.

## Ausgabe {#output}

### Allgemein {#general}

* Site - `site.js` und `site.css` werden in einem clientlib-site-Ordner erstellt.
* Abhängigkeiten - `dependencies.js` und `dependencies.css` werden in einem Ordner clientlib-dependencies erstellt.

### JavaScript {#javascript}

* Optimierung: Bei Produktions-Builds werden alle nicht verwendeten oder aufgerufenen JS entfernt.

### CSS {#css}

* Autoprefixierung - Alle CSS werden über einen Präfixer ausgeführt und alle Eigenschaften, für die Präfix erforderlich ist, werden automatisch in das CSS eingefügt.
* Optimierung: Beim Posten wird das gesamte CSS über einen Optimierer (cssnano) ausgeführt, der es gemäß den folgenden Standardregeln normalisiert:
   * Reduziert den CSS-Calc-Ausdruck, wo immer dies möglich ist, und stellt sowohl die Browserkompatibilität als auch die Komprimierung sicherKonvertiert Werte für die äquivalente Länge, Zeit und Winkel. Beachten Sie, dass Längenwerte standardmäßig nicht konvertiert werden.
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
>Die Option zum Erstellen des Front-End verwendet Konfigurationsdateien des nur dev- und prod-only webpack, die eine gemeinsame Konfigurationsdatei gemeinsam haben. Auf diese Weise können Entwicklungs- und Produktionseinstellungen unabhängig verändert werden.
