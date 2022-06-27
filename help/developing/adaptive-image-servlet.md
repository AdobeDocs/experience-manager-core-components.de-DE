---
title: Adaptives Bildservlet
description: Erfahren Sie, wie die Kernkomponenten das Adaptive Bildservlet für die Bildbereitstellung verwenden und wie Sie dessen Verwendung optimieren können.
role: Architect, Developer, Admin, User
source-git-commit: 3ff1343ab4ef7a52f910984a0bcd8fc4201441bf
workflow-type: tm+mt
source-wordcount: '254'
ht-degree: 58%

---


# Adaptives Bildservlet {#adaptive-image-servlet}

Erfahren Sie, wie die Kernkomponenten das Adaptive Bildservlet für die Bildbereitstellung verwenden und wie Sie dessen Verwendung optimieren können.

## Adaptive Bildbereitstellung oder Web-optimierte Bildbereitstellung? {#options}

Die Bild-Kernkomponente kann zwei Methoden zur Bereitstellung von Bildern verwenden.

* Das Adaptive Bildservlet ist die Standardeinstellung.
* [Weboptimierte Bildbereitstellung](/help/developing/web-optimized-image-delivery.md) ist für AEMaaCS verfügbar und reduziert die Download-Größe um durchschnittlich 25 %.

In diesem Dokument wird das standardmäßige Adaptive Image Servlet beschrieben.

## Übersicht {#overview}

Standardmäßig verwendet die Bildkomponente das Adaptive Bildservlet der Kernkomponente, um Bilder bereitzustellen. [Das Adaptive Bildservlet](https://github.com/adobe/aem-core-wcm-components/wiki/The-Adaptive-Image-Servlet) übernimmt die Bildverarbeitung sowie das Streaming und kann von Entwicklern bei der [Anpassung der Kernkomponenten](/help/developing/customizing.md) genutzt werden.

## Optimieren der Auswahl für die Ausgabedarstellung {#optimizing-rendition-selection}

Das Adaptive Image Servlet versucht, die beste Ausgabedarstellung für die angeforderte Bildgröße und den angeforderten Bildtyp auszuwählen. Es wird empfohlen, die zulässigen Breiten von DAM-Ausgabeformaten und Bildkomponenten synchron zu definieren, damit die Verarbeitung durch das Adaptive Image Servlet so gering wie möglich ist.

Dadurch wird die Leistung verbessert und verhindert, dass einige Bilder von der zugrunde liegenden Bildverarbeitungsbibliothek nicht korrekt verarbeitet werden.

## Verwenden zuletzt bearbeiteter Header {#last-modified}

Bedingte Anforderungen über den `Last-Modified`-Header werden vom Adaptiven Bildservlet unterstützt, aber die Zwischenspeicherung des `Last-Modified`-Headers [muss im Dispatcher aktiviert werden](https://experienceleague.adobe.com/docs/experience-manager-dispatcher/using/configuring/dispatcher-configuration.html?lang=de#caching-http-response-headers).

Die Dispatcher-Musterkonfiguration des [AEM-Projektarchetyps](/help/developing/archetype/overview.md) enthält diese Konfiguration bereits.
