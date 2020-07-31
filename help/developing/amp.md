---
title: AMP-Unterstützung für die Kernkomponenten
description: Die Kernkomponenten unterstützen AMP (Accelerated Mobile Pages)
translation-type: ht
source-git-commit: 905096d909d4fbf624152ba3b5cbc1d80637245f
workflow-type: ht
source-wordcount: '493'
ht-degree: 100%

---


# AMP-Unterstützung für die Kernkomponenten {#amp-support}

Ab [Version 2.11.0](/help/versions.md) der Kernkomponenten wird [AMP (Accelerated Mobile Pages)](https://developers.google.com/amp) vollständig unterstützt.

Dieses Dokument gibt einen Überblick darüber, wie AMP unterstützt wird und wie Sie es für Ihre Sites aktivieren können. Ausführliche technische Informationen finden Sie in der [GitHub-Entwicklerdokumentation](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp).

## Was ist AMP? {#what-is-amp}

Accelerated Mobile Pages oder AMP ist ein Open-Source-Framework, das ursprünglich von Google entwickelt wurde, um Seiten für das Browsen auf Mobilgeräten zu optimieren. AMP-Seiten laden in der Regel viel schneller als normale Web-Seiten und bieten so bessere mobile Erlebnisse.

## AMP in den Kernkomponenten {#amp-in-core-components}

Die Unterstützung für AMP in den Kernkomponenten ist [vollständig konfigurierbar.](#enabling-amp) AMP-Versionen von Seiten können exklusiv, parallel zu den Standard-HTML-Versionen oder gar nicht bereitgestellt werden.

Die Kernkomponenten nutzen `amp` als Sling-Selektor zum Rendern von AMP-Seiten. Zum Beispiel würde mit `example.html` die normale Seite und mit `example.amp.html` die AMP-Version gerendert.

### Voraussetzungen {#requirements}

Bei Verwendung von AMP mit den Kernkomponenten besteht der Hauptunterschied darin, dass für AMP alle CSS-Anweisungen inline im `<head>`-Element referenziert und optimiert werden müssen.

Zu diesem Zweck wird eine angepasste Seitenkomponente verwendet, die nur AMP-spezifische CSS-Anweisungen für die Komponenten lädt, die auf der Seite vorhanden sind.

Weitere Anforderungen und technische Details finden Sie in der [GitHub-Entwicklerdokumentation](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp).

### Verwenden von AMP in den Kernkomponenten {#using-amp}

Sie können für jedes Projekt einzeln festlegen, ob AMP genutzt wird oder nicht. Da AMP- und Standard-HTML-Seiten parallel bereitgestellt werden können, kann AMP auch nur auf bestimmten Seiten eines Projekts verwendet werden.

### Installieren der AMP-Unterstützung {#installing-amp}

Da AMP optional ist, wird es als Erweiterung für die Kernkomponenten bereitgestellt.

* Bei AEM as a Cloud Service-Projekten ist die Erweiterung automatisch verfügbar.
* Bei lokalen und AMS-Projekten muss die Erweiterung bei der Installation der Kernkomponenten explizit installiert werden.

Nachdem die Erweiterung installiert wurde, muss der Komponentenautor einfach die Supertypen der Komponente auf jene in der Erweiterung verweisen.

### Aktivieren von AMP für Seiten {#enabling-amp}

Um AMP für eine Seite zu aktivieren, müssen Sie den **AMP-Modus** in der [Seitenrichtlinie](https://docs.adobe.com/content/help/de-DE/experience-manager-65/authoring/siteandpage/templates.html#editingatemplatepagepolicies) auswählen.

![Optionen für AMP-Seitenrichtlinien](/help/assets/amp-policy.png)

* **Kein AMP**: Die Seite wird nur als Standard-HTML bereitgestellt.
* **Gepaartes AMP**: Die Seite wird sowohl als AMP als auch als HTML bereitgestellt.
* **Nur AMP**: Die Seite wird nur als AMP bereitgestellt.

Die AMP-Einstellungen für eine Seite können auch in den [Seiteneigenschaften](https://docs.adobe.com/content/help/de-DE/experience-manager-65/authoring/authoring/editing-page-properties.html) einer einzelnen Seite überschrieben werden.

![Eigenschaften der AMP-Seite](/help/assets/amp-page-properties.png)

* **Von Seitenvorlage übernehmen**: Dies ist der Standardwert, mit dem die Einstellung aus der Richtlinie der Seitenvorlage übernommen werden kann.
* **Kein AMP**: Die Seite wird nur als Standard-HTML bereitgestellt.
* **Gepaartes AMP**: Die Seite wird sowohl als AMP als auch als HTML bereitgestellt.
* **Nur AMP**: Die Seite wird nur als AMP bereitgestellt.
