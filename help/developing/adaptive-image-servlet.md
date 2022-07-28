---
title: Adaptive Image Servlet
description: Erfahren Sie, wie die Kernkomponenten das Adaptive Image Servlet für die Bildbereitstellung verwenden und wie Sie dessen Verwendung optimieren können.
role: Architect, Developer, Admin, User
exl-id: d9199d51-6f09-4000-9525-afc30474437e
source-git-commit: dd07fa714a23759d43ca491232674d88bc7bf88e
workflow-type: ht
source-wordcount: '254'
ht-degree: 100%

---

# Adaptive Image Servlet {#adaptive-image-servlet}

Erfahren Sie, wie die Kernkomponenten das Adaptive Image Servlet für die Bildbereitstellung verwenden und wie Sie dessen Verwendung optimieren können.

## Adaptive Image Servlet oder Web-optimierte Bildbereitstellung? {#options}

Die Bild-Kernkomponente kann zwei Methoden zur Bereitstellung von Bildern verwenden.

* Das Adaptive Image Servlet ist die Standardeinstellung.
* Die [Web-optimierte Bildbereitstellung](/help/developing/web-optimized-image-delivery.md) ist für AEMaaCS verfügbar und reduziert die Download-Größe um durchschnittlich 25 %.

In diesem Dokument wird das standardmäßige Adaptive Image Servlet beschrieben.

## Übersicht {#overview}

Standardmäßig verwendet die Bildkomponente das Adaptive Image Servlet der Kernkomponente, um Bilder bereitzustellen. [Das Adaptive Image Servlet](https://github.com/adobe/aem-core-wcm-components/wiki/The-Adaptive-Image-Servlet) übernimmt die Bildverarbeitung sowie das Streaming und kann von Entwicklern bei der [Anpassung der Kernkomponenten](/help/developing/customizing.md) genutzt werden.

## Optimieren der Auswahl für die Ausgabedarstellung {#optimizing-rendition-selection}

Das Adaptive Image Servlet versucht, die beste Ausgabedarstellung für die angeforderte Bildgröße und den angeforderten Bildtyp auszuwählen. Es wird empfohlen, die zulässigen Breiten von DAM-Ausgabeformaten und Bildkomponenten synchron zu definieren, damit die Verarbeitung durch das Adaptive Image Servlet so gering wie möglich ist.

Dadurch wird die Leistung verbessert und verhindert, dass einige Bilder von der zugrunde liegenden Bildverarbeitungsbibliothek nicht korrekt verarbeitet werden.

## Verwenden der zuletzt bearbeiteten Header {#last-modified}

Bedingte Anforderungen über den `Last-Modified`-Header werden vom Adaptiven Bildservlet unterstützt, aber die Zwischenspeicherung des `Last-Modified`-Headers [muss im Dispatcher aktiviert werden](https://experienceleague.adobe.com/docs/experience-manager-dispatcher/using/configuring/dispatcher-configuration.html?lang=de#caching-http-response-headers).

Die Dispatcher-Musterkonfiguration des [AEM-Projektarchetyps](/help/developing/archetype/overview.md) enthält diese Konfiguration bereits.
