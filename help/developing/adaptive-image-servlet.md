---
title: Adaptive Image Servlet
description: Erfahren Sie, wie die Kernkomponenten das Adaptive Image Servlet für die Bildbereitstellung verwenden und wie Sie dessen Verwendung optimieren können.
role: Developer, Admin, User
exl-id: d9199d51-6f09-4000-9525-afc30474437e
TQID: https://experienceleague.adobe.com/zfjxGeTjON5PKCAp63gcBb76rDEmIPewkGcLFvsNb0c
product_v2: id: c45915cf-e157-4af7-a80d-97b905bcb3a5id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 73aa5234ac63fa3be99feebce448bb6722513838
workflow-type: tm+mt
source-wordcount: 487
ht-degree: 100%

---

# Adaptive Image Servlet {#adaptive-image-servlet}

Erfahren Sie, wie die Kernkomponenten das Adaptive Image Servlet für die Bildbereitstellung verwenden und wie Sie dessen Verwendung optimieren können.

>[!WARNING]
>
>Aus Leistungsgründen wird dringend empfohlen, Bilder in DAM zu speichern und eine Web-optimierte Bildbereitstellung zu verwenden.
>
>Das Speichern von Bildern direkt unter dem Komponentenknoten ist für die gelegentliche Verwendung vorgesehen. Es nutzt nicht die DAM-Ausgabedarstellungen, um die Verarbeitung im Adaptive Image Servlet zu reduzieren, und lässt nicht die Leistungsvorteile einer Web-optimierten Bildbereitstellung zu, was zu möglichen Leistungsproblemen führt.

## Adaptive Image Servlet oder Web-optimierte Bildbereitstellung? {#options}

Die Bild-Kernkomponente kann zwei Methoden zur Bereitstellung von Bildern verwenden.

* Das Adaptive Image Servlet ist die Standardeinstellung.
* Die [Web-optimierte Bildbereitstellung](/help/developing/web-optimized-image-delivery.md) ist für AEMaaCS verfügbar und reduziert die Download-Größe um durchschnittlich 25 %.

In diesem Dokument wird das standardmäßige Adaptive Image Servlet beschrieben.

## Übersicht {#overview}

Standardmäßig verwendet die Bildkomponente das Adaptive Image Servlet der Kernkomponente, um Bilder bereitzustellen. [Das Adaptive Image Servlet](https://github.com/adobe/aem-core-wcm-components/wiki/The-Adaptive-Image-Servlet) übernimmt die Bildverarbeitung sowie das Streaming und kann von Entwicklern bei der [Anpassung der Kernkomponenten](/help/developing/customizing.md) genutzt werden.

## Ausgabedarstellungsauswahl {#rendition-selection}

Das Adaptive Image Servlet wählt automatisch die am besten geeignete Ausgabedarstellung aus, je nach Größe des Containers, in dem es angezeigt wird. Der Auswahlprozess für Ausgabedarstellungen sieht wie folgt aus.

1. Das Adaptive Image Servlet prüft alle verfügbaren Ausgabedarstellungen des Bild-Assets.
1. Es werden nur solche ausgewählt, die den gleichen MIME-Typ wie das ursprünglich referenzierte Asset haben.
   * E.g. wenn das ursprüngliche Asset ein PNG war, werden nur PNG-Ausgabedarstellungen berücksichtigt.
1. Zwischen diesen Ausgabedarstellungen werden die Dimensionen berücksichtigt und sie mit der Größe des Containers verglichen, in dem das Bild angezeigt werden soll.
1. Wenn die Ausgabedarstellung größer oder gleich der Container-Größe ist, wird sie einer Liste von möglichen Ausgabedarstellungen hinzugefügt.
1. Wenn die Ausgabedarstellung kleiner als die Container-Größe ist, wird sie ignoriert.
1. Diese Kriterien gewährleisten, dass die Ausgabedarstellung nicht hochskaliert wird, was sich auf die Bildqualität auswirken würde.
1. Das Adaptive Image Servlet wählt dann die Ausgabedarstellung mit der kleinsten Dateigröße aus der Kandidatenliste aus.

## Optimieren der Auswahl für die Ausgabedarstellung {#optimizing-rendition-selection}

Das Adaptive Image Servlet versucht, die beste Ausgabedarstellung für die angeforderte Bildgröße und den angeforderten Bildtyp auszuwählen. Es wird empfohlen, die zulässigen Breiten von DAM-Ausgabeformaten und Bildkomponenten synchron zu definieren, damit die Verarbeitung durch das Adaptive Image Servlet so gering wie möglich ist.

Dadurch wird die Leistung verbessert und verhindert, dass einige Bilder von der zugrunde liegenden Bildverarbeitungsbibliothek nicht korrekt verarbeitet werden.

## Verwenden der zuletzt geänderten Kopfzeilen {#last-modified}

Bedingte Anforderungen über den `Last-Modified`-Header werden vom Adaptiven Bildservlet unterstützt, aber die Zwischenspeicherung des `Last-Modified`-Headers [muss im Dispatcher aktiviert werden](https://experienceleague.adobe.com/docs/experience-manager-dispatcher/using/configuring/dispatcher-configuration.html?lang=de#caching-http-response-headers).

Die Dispatcher-Musterkonfiguration des [AEM-Projektarchetyps](/help/developing/archetype/overview.md) enthält diese Konfiguration bereits.
