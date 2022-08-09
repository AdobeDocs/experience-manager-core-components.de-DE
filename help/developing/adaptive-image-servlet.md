---
title: Adaptive Image Servlet
description: Erfahren Sie, wie die Kernkomponenten das Adaptive Image Servlet für die Bildbereitstellung verwenden und wie Sie dessen Verwendung optimieren können.
role: Architect, Developer, Admin, User
exl-id: d9199d51-6f09-4000-9525-afc30474437e
source-git-commit: 420e6085da57e5dc6deb670a5f0498b018441cb8
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 61%

---

# Adaptives Bildservlet {#adaptive-image-servlet}

Erfahren Sie, wie die Kernkomponenten das Adaptive Image Servlet für die Bildbereitstellung verwenden und wie Sie dessen Verwendung optimieren können.

## Adaptive Image Servlet oder Web-optimierte Bildbereitstellung? {#options}

Die Bild-Kernkomponente kann zwei Methoden zur Bereitstellung von Bildern verwenden.

* Das Adaptive Image Servlet ist die Standardeinstellung.
* Die [Web-optimierte Bildbereitstellung](/help/developing/web-optimized-image-delivery.md) ist für AEMaaCS verfügbar und reduziert die Download-Größe um durchschnittlich 25 %.

In diesem Dokument wird das standardmäßige Adaptive Image Servlet beschrieben.

## Übersicht {#overview}

Standardmäßig verwendet die Bildkomponente das Adaptive Image Servlet der Kernkomponente, um Bilder bereitzustellen. [Das Adaptive Image Servlet](https://github.com/adobe/aem-core-wcm-components/wiki/The-Adaptive-Image-Servlet) übernimmt die Bildverarbeitung sowie das Streaming und kann von Entwicklern bei der [Anpassung der Kernkomponenten](/help/developing/customizing.md) genutzt werden.

## Ausgabedarstellungsauswahl {#rendition-selection}

Das Adaptive Bildservlet wählt automatisch die am besten geeignete Ausgabedarstellung aus, die basierend auf der Größe des Containers angezeigt werden soll, in dem es angezeigt wird. Der Auswahlprozess für Ausgabedarstellungen sieht wie folgt aus.

1. Das Adaptive Bildservlet überprüft alle verfügbaren Ausgabeformate des Bild-Assets.
1. Es werden nur diejenigen ausgewählt, die denselben MIME-/Typ des ursprünglich referenzierten Assets aufweisen.
   * Wenn das ursprüngliche Asset beispielsweise ein PNG war, werden nur PNG-Ausgabedarstellungen berücksichtigt.
1. Von diesen Ausgabedarstellungen werden die Dimensionen berücksichtigt und sie mit der Größe des Containers verglichen, in dem das Bild angezeigt werden soll.
   1. Wenn die Ausgabedarstellung >= die Containergröße ist, wird sie einer Liste von Kandidatenausgabeformaten hinzugefügt.
   1. Wenn die Ausgabedarstellung &lt; der Container-Größe ist, wird sie ignoriert.
   1. Diese Kriterien gewährleisten, dass die Ausgabedarstellung nicht hochskaliert wird, was sich auf die Bildqualität auswirken würde.
1. Das Adaptive Bildservlet wählt dann die Ausgabedarstellung mit der kleinsten Dateigröße aus der Kandidatenliste aus.

## Optimieren der Auswahl für die Ausgabedarstellung {#optimizing-rendition-selection}

Das Adaptive Image Servlet versucht, die beste Ausgabedarstellung für die angeforderte Bildgröße und den angeforderten Bildtyp auszuwählen. Es wird empfohlen, die zulässigen Breiten von DAM-Ausgabeformaten und Bildkomponenten synchron zu definieren, damit die Verarbeitung durch das Adaptive Image Servlet so gering wie möglich ist.

Dadurch wird die Leistung verbessert und verhindert, dass einige Bilder von der zugrunde liegenden Bildverarbeitungsbibliothek nicht korrekt verarbeitet werden.

## Verwenden von zuletzt geänderten Kopfzeilen {#last-modified}

Bedingte Anforderungen über den `Last-Modified`-Header werden vom Adaptiven Bildservlet unterstützt, aber die Zwischenspeicherung des `Last-Modified`-Headers [muss im Dispatcher aktiviert werden](https://experienceleague.adobe.com/docs/experience-manager-dispatcher/using/configuring/dispatcher-configuration.html?lang=de#caching-http-response-headers).

Die Dispatcher-Musterkonfiguration des [AEM-Projektarchetyps](/help/developing/archetype/overview.md) enthält diese Konfiguration bereits.
