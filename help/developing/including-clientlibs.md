---
title: Einschließlich Client-Bibliotheken
description: Es gibt verschiedene Möglichkeiten, Clientbibliotheken einzubeziehen, je nach Anwendungsfall.
translation-type: tm+mt
source-git-commit: 24f718be2ba66113eda970c213c6ce4baec51752
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 3%

---


# Einschließlich Client-Bibliotheken {#including-client-libraries}

Je nach Anwendungsfall gibt es verschiedene Möglichkeiten, [Client-Bibliotheken](/help/developing/archetype/uifrontend.md#clientlibs) einzuschließen. Dieses Dokument enthält Beispiele und Beispiele für [HTML-Snippets](https://docs.adobe.com/content/help/de-DE/experience-manager-htl/using/overview.html) .

## Empfohlene Standardverwendung {#recommended-default-usage}

Wenn Sie keine Zeit haben, um zu untersuchen, was in Ihrer Situation am besten ist, schließen Sie Ihre Client-Bibliotheken mit ein, indem Sie die folgenden HTML-Zeilen in Ihr Seitenelement `head` einfügen:

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @
    categories='wknd.base', defer=true}">
    ${clientlibs.jsAndCssIncludes @ context="unsafe"}
</sly>
```

Dies umfasst sowohl das CSS als auch das JS auf Ihrer Seite `head`, fügt jedoch das `defer` -Attribut zu Ihren JS-Inhalten hinzu `script` , sodass die Browser warten, bis das DOM bereit ist, bevor Sie Ihre Skripten ausführen, und somit die Seitenladegeschwindigkeit optimieren.

## Grundlegende Nutzung {#basic-usage}

Die grundlegende Syntax, die sowohl JS als auch CSS einer Client Library-Kategorie enthalten muss, die alle zugehörigen CSS- `link` und/oder JS- `script` Elemente generiert, lautet wie folgt:

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.jsAndCssIncludes @ context="unsafe"}
</sly>
```

Um dies für mehrere Client-Bibliotheks-Kategorien gleichzeitig zu tun, kann ein Zeichenfolgen-Array an den `categories` Parameter übergeben werden:

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @
    categories=['wknd.base', 'cq.foundation']}">
    ${clientlibs.jsAndCssIncludes @ context="unsafe"}
</sly>
```

## Nur CSS oder JS {#css-js-only}

Häufig möchte man die CSS-Includes im HTML- `head` Element platzieren, und die JS-Datei enthält sie direkt vor dem Schließen des `body` Elements.
&#x200B;
Verwenden Sie `head`Folgendes, um nur das CSS und nicht das JS einzuschließen `cssIncludes`:

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.cssIncludes @ context="unsafe"}
</sly>
```

Verwenden Sie vor dem `body` Schließen Folgendes, um nur das JS und nicht das CSS einzuschließen `jsIncludes`:

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.jsIncludes @ context="unsafe"}
</sly>
```

## Attribute {#attributes}

Um Attribute auf die generierten CSS- `link` Elemente und/oder JS- `script` Elemente anzuwenden, sind eine Reihe von Parametern möglich:

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @
    categories='wknd.base',
    media='print',
    async=true,
    defer=true,
    onload='console.log(\'loaded: \' + this.src)',
    crossorigin='anonymous'}">
    ${clientlibs.jsAndCssIncludes @ context="unsafe"}
</sly>
```

CSS- `link` Attribute, die an `jsAndCssIncludes` und `cssIncludes`:

* `media`: Zeichenfolge &#x200B; JS- `script` Attribute, die an `jsAndCssIncludes` und `jsIncludes`:

* `async`: Boolesch
* `defer`: Boolesch
* `onload`: string
* `crossorigin`: string

## Inline {#inlining}

In einigen Fällen, entweder zur Optimierung oder für E-Mail oder [AMP,](amp.md) ist es möglicherweise erforderlich, die CSS oder JS in die Ausgabe des HTML einzubinden.
&#x200B;
Um das CSS inline zu gestalten, `cssInline` können Sie es verwenden. In diesem Fall müssen Sie das umliegende `style` Element schreiben:

```html
<style type="text/css"
    data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.cssInline @ context="unsafe"}
</style>
```

Ebenso können Sie zum Inline-Markieren des JS verwenden. In diesem Fall müssen Sie das umliegende `jsInline` `script` Element schreiben:

```html
<script type="text/javascript"
    data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.jsInline @ context="unsafe"}
</script>
```
