---
title: ui.apps-Modul des AEM-Projektarchetyps
description: ui.apps-Modul des AEM-Projektarchetyps
translation-type: tm+mt
source-git-commit: 6f7166c46940ed451721e0760d565d58efe412ab
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 100%

---


# ui.apps-Modul des AEM-Projektarchetyps {#uiapps-module}

Das Maven-Modul (`<src-directory>/<project>/ui.apps`) ui.apps enthält den gesamten Rendercode, der für die unten stehende Site benötigt wird `/apps`. Dazu gehört auch CSS/JS, das im AEM-Format &quot;clientlibs&quot; gespeichert wird. Dazu gehören auch HTML-Skripte zum Rendern von dynamischem HTML. Sie können sich das Modul ui.apps als Zuordnung zur Struktur im JCR vorstellen, jedoch in einem Format, das auf einem Dateisystem gespeichert und der Quellcodeverwaltung verpflichtet werden kann. 

Das Apache Jackrabbit FileVault-Paket-Plugin wird verwendet, um den Inhalt des Moduls ui.apps in ein AEM-Paket zu kompilieren, das für AEM bereitgestellt werden kann. Die globalen Konfigurationen für das Plugin werden in der übergeordneten Datei pom.xml definiert.

## Übergeordnete POM {#parent-pom}

[Das übergeordnete POM](/help/developing/archetype/using.md#parent-pom) (`<src>/<project>/pom.xml`) enthält `<plugin>` Abschnitte, die verschiedene Konfigurationen für die im Projekt verwendeten Plugins definieren. Dies beinhaltet eine Konfiguration für das `filterSource` Jackrabbit FileVault Package Plugin. Der `filterSource` Verweis auf den Speicherort der `filter.xml` Datei, die zum Definieren der jcr-Pfade verwendet wird, die im Paket enthalten sind.

Zusätzlich zum Jackrabbit FileVault Package Plugin ist eine Definition des Content Package Plugins, das verwendet wird, um das Paket in AEM zu verschieben. Beachten Sie, dass Variablen für `aem.host`, `aem.port`, `vault.user`und `vault.password` verwendet werden, die den globalen Eigenschaften entsprechen, die in demselben übergeordneten POM definiert sind.

## ui.apps/pom.xml {#uiapps-pom}

Das ui.apps pom (`<src>/<project>/ui.apps/pom.xml`) stellt die `embedded` Tags für die `filevault-package-maven-plugin`bereit. Die `embedded` -Tags enthalten das kompilierte Kernpaket als Teil des ui.apps-Pakets und wo es installiert wird.

Beachten Sie, dass die Pakete core.wcm.components.all und core.wcm.components.example als Unterpaket enthalten sind. Dadurch wird jedes Mal das Kernkomponenten-Paket zusammen mit dem WKND-Code bereitgestellt.

Die Beispiele &quot;core.wcm.components.all&quot; und &quot;core.wcm.components.example&quot; werden als Abhängigkeiten in die Abhängigkeitsliste aufgenommen. Als bewährtes Verfahren werden jedoch Versionen für Abhängigkeiten hier weggelassen und in der [übergeordneten Pom-Datei](/help/developing/archetype/using.md#core-components)verwaltet.

## filter.xml {#filter}

Die `filter.xml` Datei für das Modul ui.apps befindet sich unter `<src>/<project>/ui.apps/src/main/content/META-INF/vault/filter.xml` und enthält die Pfade, die mit dem Paket ui.apps eingeschlossen und installiert werden.
