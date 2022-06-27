---
title: Weboptimierte Bildbereitstellung
description: Erfahren Sie, wie die Kernkomponenten AEM Web-optimierten Bildbereitstellungsfunktionen von as a Cloud Service nutzen können, um Bilder effizienter bereitzustellen.
role: Architect, Developer, Admin, User
source-git-commit: 20436ffb5d6a6346738be1e6f5e6e2e8a68e76c9
workflow-type: tm+mt
source-wordcount: '1170'
ht-degree: 0%

---


# Weboptimierte Bildbereitstellung {#web-optimized-image-delivery}

Erfahren Sie, wie die Kernkomponenten AEM Web-optimierten Bildbereitstellungsfunktionen von as a Cloud Service nutzen können, um Bilder effizienter bereitzustellen.

>[!NOTE]
>
>Der Web-optimierte Bildbereitstellungsdienst ist eine Vorabversionsfunktion mit der für Juni 2022 erwarteten Version von AEM as a Cloud Service mit GA im Juli.
>
>Weitere Informationen zu den Vorabversionsfunktionen von AEMaaCS finden Sie im Dokument [Adobe Experience Manager as a Cloud Service-Vorabversionskanal](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/release-notes/prerelease.html?lang=de)

##  Übersicht {#overview}

Die Web-optimierte Bildbereitstellungsfunktion von AEM as a Cloud Service stellt Bild-Assets aus dem DAM in [WebP-Format.](https://developers.google.com/speed/webp) WebP kann die Download-Größe eines Bildes im Durchschnitt um etwa 25 % reduzieren, was zu einem schnelleren Laden der Seite führt.

Die Aktivierung der Web-optimierten Bildbereitstellung in den Kernkomponenten ist einfach. Da alle gängigen Browser WebP unterstützen, ist das Erlebnis für den Endbenutzer transparent. Der einzige Unterschied, den sie bemerken werden, ist, dass Inhalte schneller geladen werden!

## Aktivieren der Web-optimierten Bildbereitstellung für Kernkomponenten {#activating}

Um die Web-optimierte Bildbereitstellung zu aktivieren, bearbeiten Sie eine Seitenvorlage und aktivieren Sie einfach die Option **Web-optimierte Bilder aktivieren** im Dialogfeld &quot;Design&quot;der [Bildkomponente.](/help/components/image.md#design-dialog) Diese Option ist für die Versionen 1, 2 und 3 der Bildkomponente verfügbar.

Wenn Sie nicht mit Designdialogfeldern und AEM Seitenvorlagen vertraut sind, [lesen Sie bitte dieses Dokument.](/help/get-started/authoring.md#pre-configuring-core-components)

![Weboptimierte Bildbereitstellung im Dialogfeld &quot;Design&quot;aktivieren](/help/assets/web-optimized-image-delivery.png)

Das war´s! Bilder werden jetzt von der Bildkomponente im WebP-Format bereitgestellt.

Nachdem Sie den Web-optimierten Bildversand aktiviert haben, sollten Sie auch Ihre Dispatcher-Konfiguration überprüfen, um sicherzustellen, dass die Anforderung an den Bilddienst nicht blockiert wird. Die URLs dieses Dienstes haben das folgende Formular.

```text
/adobe/dynamicmedia/deliver/dm-aid--741ed388-d5f8-4797-8095-10c896dc9f1d/skitouring.jpg?quality=80&preferwebp=true
```

Dies kann mit diesem regulären Ausdruck verallgemeinert werden.

```text
\/adobe\/dynamicmedia\/deliver\/([^:[]|*\/])\/([\w-])\.(gif|png|png8|jpg|pjpg|bjpg|webp|webpll|webply)(?[a-z0-9=&]*)?
```

## WebP-Bereitstellung überprüfen {#verifying}

Die Web-optimierte Bildbereitstellung ist für den Verbraucher des Inhalts transparent und hat keine Auswirkungen auf das Markup. Ein Endbenutzer bemerkt nur eine schnellere Ladezeit.

Um die tatsächliche Verhaltensänderung zu beobachten, müssen Sie daher die Seitenquelle anzeigen.

1. Bearbeiten Sie AEM eine Seite, die auf der Vorlage basiert, auf der Sie [aktivierte Web-optimierte Bildbereitstellung](#activating) für die Bildkomponente.
1. Wählen Sie im Seiteneditor die **Seiteninformationen** Schaltfläche oben links und dann **Als veröffentlicht anzeigen**.
1. Sehen Sie sich mithilfe der Entwicklertools Ihrer Browser die Seitenquelle an und sehen Sie, wie das gerenderte Markup bleibt, aber dass das Bild im `src` Attributpunkte auf [die URL des neuen Bilddienstes.](#activating)

## Wenn die Web-optimierte Bildbereitstellung nicht verfügbar ist {#fallback}

Die Web-optimierte Bildbereitstellung ist nur in AEM as a Cloud Service verfügbar. In Fällen, in denen sie nicht verfügbar ist, z. B. wenn AEM 6.5 vor Ort oder auf einer lokalen Entwicklungsinstanz ausgeführt wird, wird die Bildbereitstellung auf [Adaptives Bildservlet.](/help/developing/adaptive-image-servlet.md)

Ebenso wie die Aktivierung einer Web-optimierten Bildbereitstellung das Markup nicht beeinflusst, hat ein Zurückfallen auf das Adaptive Image Servlet ebenfalls keine Auswirkungen auf das Markup, da nur die URL in der `src` -Attribut `img` -Element geändert.

## Häufig gestellte Fragen {#faq}

### Warum gibt es keine solche Option, um Web-optimierte Bilder in meiner Umgebung zu aktivieren? {#missing-option}

Die Funktion ist nur auf AEM as a Cloud Service verfügbar. Lokales oder On-Premise-AEM der Bildkomponente [Fallback](#fallback) zur Verwendung des Adaptive Image Servlet.

### Warum funktioniert der Dienst nicht mit dem lokalen SDK? {#local-sdk}

Bei Verwendung des AEM SDK in `localhost`, der Bilddienst nicht verfügbar ist und das Bild-Rendering [Fallback](#fallback) zur Verwendung des Adaptive Image Servlet.

Um den Web-optimierten Bildbereitstellungsdienst zu verwenden, stellen Sie das Projekt in einer AEMaaCS-Entwicklungsumgebung bereit, um genau testen zu können, wie sich der Bilddienst mit dem Bilddienst verhält.

### Warum funktioniert der Dienst nicht für einige Bilder auf meiner Seite? {#some-images}

Der Bilddienst funktioniert nur für Assets unter `/content/dam` und funktioniert nicht für Bilder, die direkt auf die Seite hochgeladen und unter einer `cq:Page` -Objekt. Solche Assets werden weiterhin mit dem Adaptive Image Servlet als [Fallback.](#fallback)

### Warum zeigt der Dienst ein schlechteres Bild an oder beschränkt die Bildgröße? {#quality}

Der Web-optimierte Bilddienst berücksichtigt alle Bildausgabeformate, die 2048 px und kleiner sind, und wählt die größte davon als Grundlage für die Anwendung der angeforderten Einstellungen (Breite, Zuschnitt, Format, Qualität usw.).

Der Bilddienst hochlädt Bilder nie. Diese Ausgabeformate definieren daher die beste Größe und Qualität, die der Bilddienst bereitstellen kann. Vergewissern Sie sich daher, dass alle Assets die 2048-px-Zoom-Ausgabe aufweisen, und verarbeiten Sie sie andernfalls erneut.

### Die URL meiner Bilder endet immer noch mit .JPG oder .PNG, nicht mit .WEBP, und es gibt kein SRCSET-Attribut oder PICTURE-Element. Verwendet dies wirklich optimierte Webformate? {#content-negotiation}

Zur Bereitstellung von WebP-Formaten verwendet der Web-optimierte Bildbereitstellungsdienst eine Technik namens &quot;Inhaltsvermittlung&quot;. Dies besteht darin, ein WebP-Dateiformat zurückzugeben, selbst wenn eine JPG- oder PNG-Dateierweiterung angefordert wird, jedoch nur, wenn der Browser, der die Anforderung sendet, eine `image/webp` HTTP-Akzeptierungs-Header. Browser, die diese Technik unterstützen, können diese Kopfzeile dann bereitstellen und ältere Browser erhalten weiterhin das JPG- oder PNG-Dateiformat.

Der Vorteil dieser Technik besteht darin, dass die `img` -Element und seine Attribute können gleich bleiben, was zu einer optimalen Kompatibilität für vorhandene Sites führt und den reibungslosen Übergang zur Web-optimierten Bildbereitstellung gewährleistet.

### Kann ich die Web-optimierte Bildbereitstellung mit meiner eigenen Komponente verwenden?

Ja, der Web-optimierte Bildbereitstellungsdienst kann von benutzerdefinierten Komponenten verwendet werden. Adobe empfiehlt [Erweitern der Bildkomponente](/help/developing/customizing.md) in diesem Fall.

Im Folgenden finden Sie eine Dienstschnittstelle, die zum Generieren der Asset-URL verwendet werden kann.

```
com.adobe.cq.wcm.spi.AssetDelivery.getDeliveryURL(Resource resource, Map<String, Object> parameterMap)
```

Dieser Dienst akzeptiert eine Asset-Ressource als obligatorischen ersten Parameter und kann eine optionale Zuordnung der gewünschten Bildtransformationen erstellen, die angewendet werden sollen und die die folgenden Parameter enthalten können.

* `path` - Asset-ID, die bereitgestellt werden soll, muss vom Muster sein. `([^:\[\]\|\*\/]+)` (z. B.: `unicorn–1234`)
* `seoname` - Benutzerdefinierter, SEO-zentrierter Name, der an die Bild-URL angehängt werden soll, kann Bindestriche enthalten, muss vom Muster sein. `([\w-]+)` (z. B.: `my-friend-the-unicorn`)
* `format` - Das gewünschte Bildformat kann `gif`, `png`, `png8`, `jpg`, `pjpg`, `bjpg`, `webp`, `webpll`, `webply` (z. B.: `webp`)
* `preferwebp` - Senden Sie nach Möglichkeit die WebP-Ausgabe, wobei Sie die `format` Parameter ([Siehe Häufig gestellte Fragen zu Inhaltsverhandlungen](#content-negotiation)), boolesch (z. B.: `true`)
* `width` - Die gewünschte Bildauflösung in Pixel muss größer als 1 sein (z. B.: `400`)
* `quality` - Die gewünschte Komprimierung zwischen `1` und `100` (z. B.: `75`)
* `c` - Die gewünschten Bildzuschnittkoordinaten, kommagetrennte Pixelwerte (z. B.: `100,100,400,200`)
* `r` - Die gewünschte Bildrotation kann `90`, `180`, `270` (z. B.: `90`)
* `flip` - Das gewünschte Bild-Flipping kann `h`, `v`, `hv` (z. B.: `h`)

### Wie lautet die URL eines Bildes, das vom neuen Bilddienst bereitgestellt wird? {#url}

Siehe vorherigen Abschnitt [Aktivieren der Web-optimierten Bildbereitstellung für Kernkomponenten](#activating) für eine Beispiel-URL und einen regulären Ausdruck.

### Können Bilder nach der Aktivierung Web-optimierter Bilder nicht angezeigt werden?

Nein, das sollte niemals geschehen.

* Auf der HTML ändert sich das Markup bei der Aktivierung Web-optimierter Bilder nicht, sondern nur der Wert des SCR-Attributs für das Bildelement.
* Wenn der neue Bilddienst nicht verfügbar ist oder das gewünschte Bild nicht verarbeiten kann, wird die generierte URL [Fallback zum Adaptive Image Servlet.](#fallback)
* Dispatcher-Regeln können den Web-optimierten Bilddienst blockieren und [sollte beim Aktivieren der Funktion überprüft werden.](#activating)
