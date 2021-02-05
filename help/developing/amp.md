---
title: AMP-Unterstützung für die Kernkomponenten
description: Die Kernkomponenten unterstützen AMP (Accelerated Mobile Pages)
translation-type: ht
source-git-commit: a4df0c8603614cf831ffd66cbcfc1f7ef964c25b
workflow-type: ht
source-wordcount: '558'
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

Um AMP für eine Seite zu aktivieren, müssen Sie den **AMP-Modus** in der [Seitenrichtlinie](https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/sites/authoring/features/templates.html#editing-a-template-page-policy-template-author-developer) auswählen.

![Optionen für AMP-Seitenrichtlinien](/help/assets/amp-policy.png)

* **Kein AMP**: Die Seite wird nur als Standard-HTML bereitgestellt.
* **Gepaartes AMP**: Die Seite wird sowohl als AMP als auch als HTML bereitgestellt.
* **Nur AMP**: Die Seite wird nur als AMP bereitgestellt.

Die AMP-Einstellungen für eine Seite können auch in den [Seiteneigenschaften](https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.translate.html) einer einzelnen Seite überschrieben werden.

![Eigenschaften der AMP-Seite](/help/assets/amp-page-properties.png)

* **Von Seitenvorlage übernehmen**: Dies ist der Standardwert, mit dem die Einstellung aus der Richtlinie der Seitenvorlage übernommen werden kann.
* **Kein AMP**: Die Seite wird nur als Standard-HTML bereitgestellt.
* **Gepaartes AMP**: Die Seite wird sowohl als AMP als auch als HTML bereitgestellt.
* **Nur AMP**: Die Seite wird nur als AMP bereitgestellt.

### CSS-Anforderungen {#css-requirements}

Bei Verwendung von AMP mit den Kernkomponenten besteht der Hauptunterschied darin, dass für AMP alle [CSS-Anweisungen inline](including-clientlibs.md#inlining) im Element `<head>` referenziert und optimiert werden müssen.

Zu diesem Zweck wird eine angepasste Seitenkomponente verwendet, die nur AMP-spezifische CSS-Anweisungen für die Komponenten lädt, die auf der Seite vorhanden sind.

>[!NOTE]
>
>Aufgrund von Einschränkungen des AMP-Designs unterstützt Adobe die Verwendung des responsiven Rasters mit der AMP-Version Ihrer Seite nicht.

Weitere Anforderungen und technische Details finden Sie in der [GitHub-Entwicklerdokumentation](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp).
