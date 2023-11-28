---
title: Web-optimierte Bildbereitstellung
description: Erfahren Sie, wie die Kernkomponenten die Funktionen zur Web-optimierten Bildbereitstellung von AEM as a Cloud Service nutzen können, um Bilder effizienter bereitzustellen.
role: Architect, Developer, Admin, User
exl-id: 6080ab8b-f53c-4d5e-812e-16889da4d7de
source-git-commit: d8c8f4c3395313b21f56fd7d98175924287c367c
workflow-type: tm+mt
source-wordcount: '1023'
ht-degree: 97%

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

Nachdem Sie die Web-optimierte Bildbereitstellung aktiviert haben, sollten Sie auch Ihre Dispatcher-Konfiguration überprüfen, um sicherzustellen, dass die Anforderung an den Bild-Service nicht blockiert wird. Die URLs dieses Service haben die folgende Form.

```text
/adobe/dynamicmedia/deliver/dm-aid--741ed388-d5f8-4797-8095-10c896dc9f1d/skitouring.jpg?quality=80&preferwebp=true
```

Dies kann mit diesem regulären Ausdruck verallgemeinert werden.

```text
\/adobe\/dynamicmedia\/deliver\/([^:[]|*\/])\/([\w-])\.(gif|png|png8|jpg|pjpg|bjpg|webp|webpll|webply)(?[a-z0-9=&]*)?
```

## Überprüfen der WebP-Bereitstellung {#verifying}

Die Web-optimierte Bildbereitstellung ist für alle, die die Inhalte nutzen, transparent und hat keine Auswirkungen auf das Markup. Die Endbenutzenden bemerken einzig eine schnellere Ladezeit.

Um die tatsächliche Verhaltensänderung zu beobachten, müssen Sie daher die Seitenquelle anzeigen.

1. Bearbeiten Sie in AEM eine Seite, die auf der Vorlage basiert, auf der Sie die [Web-optimierte Bildbereitstellung für die Bildkomponente aktiviert haben](#activating).
1. Wählen Sie im Seiteneditor oben links die Schaltfläche **Seiteninformationen** und dann **Als veröffentlicht anzeigen**.
1. Wenn Sie mit den Entwickler-Tools Ihres Browsers den Quelltext der Seite anzeigen, werden Sie feststellen, dass das gerenderte Markup gleich bleibt, das Bild im `src`-Attribut jedoch auf [die URL des neuen Bild-Service](#activating) verweist.

## Wann die Web-optimierte Bildbereitstellung nicht verfügbar ist {#fallback}

Die Web-optimierte Bildbereitstellung ist nur in AEM as a Cloud Service verfügbar. In Fällen, in denen sie nicht verfügbar ist, z. B. wenn AEM 6.5 lokal oder auf einer lokalen Entwicklungsinstanz ausgeführt wird, fällt die Bildbereitstellung auf die Verwendung des [Adaptive Image Servlets](/help/developing/adaptive-image-servlet.md) zurück.

Ebenso wie die Aktivierung einer Web-optimierten Bildbereitstellung das Markup nicht beeinflusst, hat ein Zurückfallen auf das Adaptive Image Servlet ebenfalls keine Auswirkungen auf das Markup, da nur die URL im `src`-Attribut des `img`-Elements geändert wird.

## Häufig gestellte Fragen {#faq}

### Warum gibt es in meiner Umgebung keine Option, um Web-optimierte Bilder zu aktivieren? {#missing-option}

Die Funktion ist nur in AEM as a Cloud Service verfügbar. Wenn AEM lokal ausgeführt wird, [kehrt die Bildkomponente zur Verwendung des Adaptive Image Servlets zurück](#fallback).

### Warum funktioniert der Service nicht mit dem lokalen SDK? {#local-sdk}

Wenn Sie das AEM SDK auf `localhost` verwenden, ist der Bild-Service nicht verfügbar und das Rendern von Bildern [fällt auf die Verwendung des Adaptive Image Servlets zurück](#fallback).

Um den Service zur Web-optimierten Bildbereitstellung zu verwenden, stellen Sie das Projekt in einer AEMaaCS-Entwicklungsumgebung bereit, um genau testen zu können, wie sich die Bilder mit dem Bild-Service verhalten.

### Warum funktioniert der Service für einige Bilder auf meiner Seite nicht? {#some-images}

Der Bild-Service funktioniert nur für Assets, die sich unter `/content/dam` befinden. Er funktioniert nicht für Bilder, die direkt auf die Seite hochgeladen und unter einem `cq:Page`-Objekt gespeichert werden. Solche Assets werden weiterhin mit dem Adaptive Image Servlet als [Ausweichlösung](#fallback) bereitgestellt.

### Warum zeigt der Service ein Bild mit schlechterer Qualität an oder begrenzt die Größe der Bilder? {#quality}

Der Web-optimierte Bild-Service berücksichtigt alle Bildausgabeformate, die 2.048 Pixel und kleiner sind, und wählt die größte davon als Grundlage für die Anwendung der angeforderten Einstellungen (Breite, Zuschnitt, Format, Qualität usw.).

Der Bild-Service skaliert Bilder niemals hoch. Diese Ausgabeformate definieren daher die beste Größe und Qualität, die der Bild-Service bereitstellen kann. Vergewissern Sie sich daher, dass Ihre Assets alle die Zoom-Ausgabedarstellung von 2048 Pixeln aufweisen, und verarbeiten Sie sie andernfalls erneut.

### Die URLs meiner Bilder enden immer noch mit .JPG oder .PNG, nicht mit .WEBP und es gibt kein SRCSET-Attribut oder PICTURE-Element. Verwendet dies wirklich optimierte Web-Formate? {#content-negotiation}

Zur Bereitstellung von WebP-Formaten verwendet der Service zur Web-optimierten Bildbereitstellung eine Technik namens „Inhaltsaushandlung“. Diese besteht darin, ein WebP-Dateiformat zurückzugeben, selbst wenn eine JPG- oder PNG-Dateierweiterung angefordert wird, jedoch nur, wenn der Browser, der die Anforderung stellt, eine Kopfzeile zum Akzeptieren von `image/webp`-HTTP bereitstellt. Browser, die diese Technik unterstützen, können diese Kopfzeile dann bereitstellen, während ältere Browser weiterhin das JPG- oder PNG-Dateiformat erhalten.

Der Vorteil dieser Technik besteht darin, dass das `img`-Element und seine Attribute unverändert bleiben können, was zu einer optimalen Kompatibilität mit bestehenden Websites führt und einen möglichst reibungslosen Übergang zu einer Web-optimierten Bildbereitstellung gewährleistet.

### Kann ich die Web-optimierte Bildbereitstellung mit meiner eigenen Komponente verwenden?

Ja, der Service zur Web-optimierten Bildbereitstellung kann von benutzerdefinierten Komponenten verwendet werden. Adobe empfiehlt in diesem Fall das [Erweitern der Bildkomponente](/help/developing/customizing.md).

Im Folgenden finden Sie eine Service-Schnittstelle, die zum Generieren der Asset-URL verwendet werden kann.

```
com.adobe.cq.wcm.spi.AssetDelivery.getDeliveryURL(Resource resource, Map<String, Object> parameterMap)
```

**Beachten Sie, dass direkte URL-Einbettungen in ein Erlebnis, das nicht über Kernkomponenten erstellt wurde, die auf AEM Sites CS ausgeführt werden, einen Verstoß gegen Media Library-Lizenzbedingungen darstellen.**

### Wie lautet die URL eines Bildes, das vom neuen Bild-Service bereitgestellt wird? {#url}

Im vorherigen Abschnitt [Aktivieren der Web-optimierten Bildbereitstellung für Kernkomponenten](#activating) finden Sie eine Beispiel-URL und einen regulären Ausdruck.

### Können Bilder nach der Aktivierung Web-optimierter Bilder möglicherweise nicht angezeigt werden?

Nein, das sollte niemals geschehen.

* In der HTML ändert sich bei der Aktivierung Web-optimierter Bilder das Markup nicht, sondern nur der Wert des SRC-Attributs für das Bildelement.
* Wenn der neue Bild-Service nicht verfügbar ist oder das gewünschte Bild nicht verarbeiten kann, wird die generierte URL immer [auf das Adaptive Image Servlet zurückfallen](#fallback).
* Dispatcher-Regeln können den Service zur Web-optimierten Bildbereitstellung blockieren und [sollten deswegen beim Aktivieren der Funktion überprüft werden](#activating).
