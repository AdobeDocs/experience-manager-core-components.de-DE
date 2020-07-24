---
title: AMP-Unterstützung für die Kernkomponenten
description: Die Kernkomponenten unterstützen AMP - beschleunigte Mobilseiten
translation-type: tm+mt
source-git-commit: 905096d909d4fbf624152ba3b5cbc1d80637245f
workflow-type: tm+mt
source-wordcount: '493'
ht-degree: 0%

---


# AMP-Unterstützung für die Kernkomponenten {#amp-support}

Ab [Version 2.11.0](/help/versions.md) der Kernkomponenten wird [AMP - Accelerated Mobile Pages](https://developers.google.com/amp) - vollständig unterstützt.

Dieses Dokument gibt einen Überblick darüber, wie AMP unterstützt wird und wie Sie es für Ihre Sites aktivieren können. Ausführliche technische Informationen finden Sie jedoch in der [GitHub-Entwicklerdokumentation.](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)

## Was ist AMP? {#what-is-amp}

Accelerated Mobile Pages oder AMP ist ein Open-Source-Framework, das ursprünglich von Google entwickelt wurde, um Seiten für das Browsen auf Mobilgeräten zu optimieren. AMP-Seiten laden in der Regel viel schneller als normale Webseiten und bieten so bessere mobile Erlebnisse.

## AMP in den Hauptkomponenten {#amp-in-core-components}

Die Unterstützung für AMP in den Core-Komponenten ist [vollständig konfigurierbar.](#enabling-amp) AMP-Versionen von Seiten können exklusiv neben den Standard-HTML-Versionen oder gar nicht bereitgestellt werden.

Die Kernkomponenten werden `amp` als Sling-Selektor zum Rendern einer AMP-Seite verwendet. Zum Beispiel `example.html` würde die normale Seite gerendert und `example.amp.html` wäre die AMP-Version.

### Voraussetzungen {#requirements}

Bei Verwendung von AMP mit den Core-Komponenten besteht der Hauptunterschied darin, dass für AMP alle CSS sowohl im Element als auch optimiert `<head>` werden müssen.

Um dies zu unterstützen, wird eine benutzerdefinierte Seitenkomponente verwendet, die nur das AMP-spezifische CSS für Komponenten lädt, die auf der Seite vorhanden sind.

Weitere Anforderungen und technische Details finden Sie in der [GitHub-Entwicklerdokumentation.](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)

### Verwenden von AMP in den Hauptkomponenten {#using-amp}

Einzelne Projekte können entscheiden, ob sie AMP nutzen oder nicht. Da AMP- und Standard-HTML-Seiten parallel bereitgestellt werden können, kann ein Projekt AMP nur auf bestimmten Seiten des Projekts verwenden.

### Installieren der AMP-Unterstützung {#installing-amp}

Da AMP optional ist, wird es als Erweiterung der Core-Komponenten bereitgestellt.

* Bei AEM als Cloud Service-Projekten ist die Erweiterung automatisch verfügbar.
* Bei lokalen und AMS-Projekten muss die Erweiterung bei der Installation der Core-Komponenten explizit installiert werden.

Nachdem die Erweiterung installiert wurde, muss der Komponentenautor einfach darauf verweisen, dass die übergeordneten Komponenten auf die in der Erweiterung befindlichen überlagerten Komponenten verweisen.

### Aktivieren von AMP für Seiten {#enabling-amp}

Um AMP für eine Seite zu aktivieren, muss der **AMP-Modus** in der [Seitenrichtlinie ausgewählt werden.](https://docs.adobe.com/content/help/en/experience-manager-65/authoring/siteandpage/templates.html#editingatemplatepagepolicies)

![Optionen für AMP-Seitenrichtlinien](/help/assets/amp-policy.png)

* **Kein AMP** - Die Seite wird nur als Standard-HTML bereitgestellt.
* **Paartes AMP** - Die Seite wird sowohl als AMP als auch als HTML bereitgestellt.
* **Nur** AMP: Die Seite wird nur als AMP bereitgestellt.

Die AMP-Einstellungen für eine Seite können auch in den [Seiteneigenschaften](https://docs.adobe.com/content/help/en/experience-manager-65/authoring/authoring/editing-page-properties.html) einer einzelnen Seite überschrieben werden.

![Eigenschaften der AMP-Seite](/help/assets/amp-page-properties.png)

* **Von Seitenvorlage übernehmen** - Dies ist der Standardwert, mit dem die Einstellung aus der Richtlinie der Seitenvorlage übernommen werden kann.
* **Kein AMP** - Die Seite wird nur als Standard-HTML bereitgestellt.
* **Paartes AMP** - Die Seite wird sowohl als AMP als auch als HTML bereitgestellt.
* **Nur** AMP: Die Seite wird nur als AMP bereitgestellt.
