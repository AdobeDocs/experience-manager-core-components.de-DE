---
title: Web-optimierte Bildbereitstellung
description: Erfahren Sie, wie die Kernkomponenten die Funktionen zur Web-optimierten Bildbereitstellung von AEM as a Cloud Service nutzen können, um Bilder effizienter bereitzustellen.
role: Architect, Developer, Admin, User
exl-id: 6080ab8b-f53c-4d5e-812e-16889da4d7de
source-git-commit: eb1822cb41a849695afb5125745ed5f78e3e70a4
workflow-type: tm+mt
source-wordcount: '1061'
ht-degree: 54%

---

# Web-optimierte Bildbereitstellung {#web-optimized-image-delivery}

Erfahren Sie, wie die Kernkomponenten die Funktionen zur Web-optimierten Bildbereitstellung von AEM as a Cloud Service nutzen können, um Bilder effizienter bereitzustellen.

## Übersicht {#overview}

Die Funktion der Web-optimierten Bildbereitstellung von AEM as a Cloud Service stellt Bild-Assets aus dem DAM im [WebP-Format bereit.](https://developers.google.com/speed/webp) WebP kann die Download-Größe eines Bildes im Durchschnitt um etwa 25 % reduzieren, was zu einem schnelleren Laden von Seiten führt.

Die Aktivierung der Web-optimierten Bildbereitstellung in den Kernkomponenten ist einfach. Da alle gängigen Browser WebP unterstützen, ist das Erlebnis für den Endbenutzenden transparent. Der einzige bemerkbare Unterschied ist, dass Inhalte schneller geladen werden!

## Aktivieren der Web-optimierten Bildbereitstellung für Kernkomponenten {#activating}

Um die Web-optimierte Bildbereitstellung zu aktivieren, bearbeiten Sie eine Seitenvorlage und aktivieren Sie einfach die Option **Web-optimierte Grafiken aktivieren** im Dialogfeld „Design“ der [Bildkomponente.](/help/components/image.md#design-dialog) Diese Option ist für die Versionen 1, 2 und 3 der Bildkomponente verfügbar.

Wenn Sie nicht mit Design-Dialogfeldern und AEM-Seitenvorlagen vertraut sind, [lesen Sie bitte dieses Dokument](/help/get-started/authoring.md#pre-configuring-core-components).

![Aktivierung der Web-optimierten Bildbereitstellung im Dialogfeld „Design“](/help/assets/web-optimized-image-delivery.png)

Das war´s! Bilder werden jetzt von der Bildkomponente im WebP-Format bereitgestellt.

Nachdem Sie den Web-optimierten Bildversand aktiviert haben, sollten Sie Ihre Dispatcher-Konfiguration überprüfen, um sicherzustellen, dass die Anforderung an den Bildbereitstellungsdienst nicht blockiert wird. Siehe [dieser FAQ-Eintrag](#failure-to-deliver) für weitere Informationen.

## Überprüfen der WebP-Bereitstellung {#verifying}

Die Web-optimierte Bildbereitstellung ist für den Verbraucher des Inhalts transparent. Ein Endbenutzer bemerkt nur eine schnellere Ladezeit. Um eine tatsächliche Verhaltensänderung zu beobachten, müssen Sie daher den Inhaltstyp der gerenderten Bilder im Browser überprüfen. Alle modernen Browser unterstützen WebP. Weitere Informationen finden Sie unter [diese Website](https://caniuse.com/webp) für Details zur Browserunterstützung.

1. Bearbeiten Sie in AEM eine Seite, die auf der Vorlage basiert, auf der Sie die [Web-optimierte Bildbereitstellung für die Bildkomponente aktiviert haben](#activating).
1. Wählen Sie im Seiteneditor oben links die Schaltfläche **Seiteninformationen** und dann **Als veröffentlicht anzeigen**.
1. Öffnen Sie die Entwicklertools Ihres Browsers und wählen Sie die Registerkarte Netzwerk aus.
1. Laden Sie die Seite neu, suchen Sie nach HTTP-Anforderungen, um die Bilder zu laden, und überprüfen Sie den Inhaltstyp des Bildes, das der Browser empfangen hat.

## Wann die Web-optimierte Bildbereitstellung nicht verfügbar ist {#fallback}

Die Web-optimierte Bildbereitstellung ist nur in AEM as a Cloud Service verfügbar. In Fällen, in denen sie nicht verfügbar ist, z. B. wenn AEM 6.5 lokal oder auf einer lokalen Entwicklungsinstanz ausgeführt wird, fällt die Bildbereitstellung auf die Verwendung des [Adaptive Image Servlets](/help/developing/adaptive-image-servlet.md) zurück.

Wenn Sie zum Adaptive Image Servlet zurückkehren, ändert sich die `src` -Attribut `img` -Elemente in der Seitenquelle.

## Häufig gestellte Fragen {#faq}

### Warum gibt es in meiner Umgebung keine Option, um Web-optimierte Bilder zu aktivieren? {#missing-option}

Die Funktion ist nur in AEM as a Cloud Service verfügbar. Wenn AEM lokal ausgeführt wird, [kehrt die Bildkomponente zur Verwendung des Adaptive Image Servlets zurück](#fallback).

### Warum funktioniert der Service nicht mit dem lokalen SDK? {#local-sdk}

Wenn Sie das AEM SDK auf `localhost` verwenden, ist der Bild-Service nicht verfügbar und das Rendern von Bildern [fällt auf die Verwendung des Adaptive Image Servlets zurück](#fallback).

Um den Service zur Web-optimierten Bildbereitstellung zu verwenden, stellen Sie das Projekt in einer AEMaaCS-Entwicklungsumgebung bereit, um genau testen zu können, wie sich die Bilder mit dem Bild-Service verhalten.

### Warum funktioniert der Service für einige Bilder auf meiner Seite nicht? {#some-images}

Der Bild-Service funktioniert nur für Assets, die sich unter `/content/dam` befinden. Er funktioniert nicht für Bilder, die direkt auf die Seite hochgeladen und unter einem `cq:Page`-Objekt gespeichert werden. Solche Assets werden weiterhin mit dem Adaptive Image Servlet als [Ausweichlösung](#fallback) bereitgestellt.

### Warum zeigt der Service ein Bild mit schlechterer Qualität an oder begrenzt die Größe der Bilder? {#quality}

Wenn Bild-Assets unter `/content/dam` verarbeitet werden, AEM as a Cloud Service Umgebungen optimierte Ausgabedarstellungen unterschiedlicher Dimensionen generieren. Der Web-optimierte Bilddienst analysiert die von der Bild-Kernkomponente angeforderte Breite, berücksichtigt das Originalbild und alle Ausgabeformate, die 2048 px und kleiner sind, und wählt die größte davon aus (innerhalb der Größenbeschränkungen und der Größenbeschränkungen kann der Bilddienst derzeit 50 MB und `12k`x`12k`) als Grundlage für die Anwendung der angeforderten Einstellungen (Breite, Zuschnitt, Format, Qualität usw.).

Um die Wiedergabetreue der Ausgabe zu wahren, skaliert der Bilddienst keine Bilder. Die oben genannten Ausgabeformate definieren die beste Qualität, die der Bilddienst bereitstellen kann. Da Sie häufig nicht in der Lage sind, die Größe und/oder Abmessungen des ursprünglichen Bild-Assets zu beeinflussen, stellen Sie sicher, dass Ihre Bild-Assets alle eine 2048-px-Zoom-Wiedergabe aufweisen, und verarbeiten Sie sie andernfalls erneut.

### Die URLs meiner Bilder enden immer noch mit .JPG oder .PNG, nicht mit .WEBP und es gibt kein SRCSET-Attribut oder PICTURE-Element. Verwendet dies wirklich optimierte Web-Formate? {#content-negotiation}

Zur Bereitstellung von WebP-Formaten führt der Web-optimierte Bildbereitstellungsdienst [Server-gesteuerte Inhaltsverhandlungen.](https://developer.mozilla.org/en-US/docs/Web/HTTP/Content_negotiation#server-driven_content_negotiation) Dies hilft bei der Auswahl des optimalen Ausgabeformats für das Bild basierend auf den vom Kunden beworbenen Funktionen, sodass der Bildbereitstellungsdienst die Dateierweiterung ignorieren kann.

Der Vorteil der Nutzung von Content-Verhandlungsprozessen besteht darin, dass Browser, die keine WebP-Unterstützung bewerben, weiterhin das JPG- oder PNG-Dateiformat erhalten, ohne dass Änderungen am Markup der Seite erforderlich sind. Dies bietet eine optimale Kompatibilität für bestehende Sites und garantiert einen möglichst reibungslosen Übergang zur Web-optimierten Bildbereitstellung.

### Kann ich die Web-optimierte Bildbereitstellung mit meiner eigenen Komponente verwenden?

Ja, der Web-optimierte Bildbereitstellungsdienst kann von benutzerdefinierten Komponenten verwendet werden, die durch [Erweiterung der Bildkomponente](/help/developing/customizing.md) erstellt wurden.

Im Folgenden finden Sie eine Service-Schnittstelle, die zum Generieren der Asset-URL verwendet werden kann.

```
com.adobe.cq.wcm.spi.AssetDelivery.getDeliveryURL(Resource resource, Map<String, Object> parameterMap)
```

>[!WARNING]
>
>Direkte URL-Einbettungen in ein Erlebnis, das nicht über die oben genannte SPI (auf AEM as a Cloud Service Sites verfügbar) erstellt wurde, verstoßen gegen die [Nutzungsbedingungen von Media Library](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/admin/medialibrary.html?lang=en#use-media-library).

### Können Bilder nach der Aktivierung Web-optimierter Bilder möglicherweise nicht angezeigt werden? {#failure-to-deliver}

Nein, das sollte niemals aus folgenden Gründen geschehen.

* Auf der HTML ändert sich das Markup bei der Aktivierung Web-optimierter Bilder nicht, sondern nur der Wert der `src` -Attribut für das Bildelement geändert.
* Wenn der neue Bild-Service nicht verfügbar ist oder das gewünschte Bild nicht verarbeiten kann, wird die generierte URL immer [auf das Adaptive Image Servlet zurückfallen](#fallback).

Dispatcher-Regeln können jedoch den Web-optimierten Bildbereitstellungsdienst blockieren. URLs des Bildbereitstellungsdienstes beginnen mit `/adobe`und die Überprüfung der Dispatcher-Protokolle auf abgelehnte Anfragen als [hier beschrieben](https://experienceleague.adobe.com/docs/experience-manager-learn/ams/dispatcher/common-logs.html#filter-rejects) sollte bei der Fehlerbehebung bei Fehlern helfen, die bei der Bereitstellung der Bilder an den Browser aufgetreten sind.
