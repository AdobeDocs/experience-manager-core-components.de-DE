---
title: AMP-Unterstützung für die Kernkomponenten
description: Die Kernkomponenten unterstützen AMP (Accelerated Mobile Pages)
translation-type: tm+mt
source-git-commit: d8503d92c2d4948e54b2ad7d5407e4c7c98ebf83
workflow-type: tm+mt
source-wordcount: '534'
ht-degree: 95%

---


# AMP-Unterstützung für die Kernkomponenten {#amp-support}

Ab [Version 2.11.0](/help/versions.md) der Kernkomponenten wird [AMP (Accelerated Mobile Pages)](https://developers.google.com/amp) vollständig unterstützt.

Dieses Dokument gibt einen Überblick darüber, wie AMP unterstützt wird und wie Sie es für Ihre Sites aktivieren können. Ausführliche technische Informationen finden Sie in der [GitHub-Entwicklerdokumentation](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp).

## Was ist AMP? {#what-is-amp}

Accelerated Mobile Pages oder AMP ist ein Open-Source-Framework, das ursprünglich von Google entwickelt wurde, um Seiten für das Browsen auf Mobilgeräten zu optimieren. AMP-Seiten laden in der Regel viel schneller als normale Web-Seiten und bieten so bessere mobile Erlebnisse.

## AMP in den Kernkomponenten {#amp-in-core-components}

Die Unterstützung für AMP in den Kernkomponenten ist [vollständig konfigurierbar.](#enabling-amp) AMP-Versionen von Seiten können exklusiv, parallel zu den Standard-HTML-Versionen oder gar nicht bereitgestellt werden.

Die Kernkomponenten nutzen `amp` als Sling-Selektor zum Rendern von AMP-Seiten. Zum Beispiel würde mit `example.html` die normale Seite und mit `example.amp.html` die AMP-Version gerendert.

Sie können für jedes Projekt einzeln festlegen, ob AMP genutzt wird oder nicht. Da AMP- und Standard-HTML-Seiten parallel bereitgestellt werden können, kann AMP auch nur auf bestimmten Seiten eines Projekts verwendet werden.

## Erste Schritte mit AMP-Unterstützung in Ihrem Projekt {#getting-started}

Obwohl AMP-Unterstützung umfangreiche Flexibilität bietet, müssen Sie für den Einstieg nur wenige einfache Schritte befolgen:

1. Installieren Sie bei Bedarf die Erweiterung für die AMP-Unterstützung.
   * Für AEM as a Cloud Service-Projekte ist die Erweiterung automatisch mit den Kernkomponenten verfügbar und es ist keine Installation erforderlich.
   * Bei lokalen und AMS-Projekten muss die Erweiterung bei der Installation der Kernkomponenten explizit installiert werden.
1. Nachdem die AMP-Erweiterung installiert wurde, muss der Komponentenautor einfach die Supertypen der Komponente auf jene in der Erweiterung verweisen.
1. [Aktivieren Sie die AMP-Unterstützung](#enabling-amp) auf Vorlagenebene oder auf den einzelnen Seiten.
1. [Stellen Sie ggf. eingebettetes CSS bereit](#css-requirements).

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

### CSS-Anforderungen {#css-requirements}

When using AMP with the Core Components, the main difference is that AMP requires all [CSS to be inlined](including-clientlibs.md#inlining) in the `<head>` element as well as optimized.

Zu diesem Zweck wird eine angepasste Seitenkomponente verwendet, die nur AMP-spezifische CSS-Anweisungen für die Komponenten lädt, die auf der Seite vorhanden sind.

Weitere Anforderungen und technische Details finden Sie in der [GitHub-Entwicklerdokumentation](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp).
