---
title: Einschließen von Client-Bibliotheken
description: Je nach Nutzungsszenario gibt es verschiedene Möglichkeiten, Client-Bibliotheken einzuschließen.
translation-type: ht
source-git-commit: f74883359561e5ff6ca679d58bedbdeb100f7b0b
workflow-type: ht
source-wordcount: '333'
ht-degree: 100%

---


# Einschließen von Client-Bibliotheken {#including-client-libraries}

Je nach Nutzungsszenario gibt es verschiedene Möglichkeiten, [Client-Bibliotheken](/help/developing/archetype/uifrontend.md#clientlibs) einzuschließen. Dieses Dokument enthält besipielhafte [HTML-Snippets](https://docs.adobe.com/content/help/de-DE/experience-manager-htl/using/overview.html) für alle diese Möglichkeiten.

## Empfohlene Standardverwendung {#recommended-default-usage}

Wenn Sie keine Zeit haben, die beste Lösung für Ihre Sitution zu ermitteln, schließen Sie Ihre Client-Bibliotheken mit ein, indem Sie die folgenden HTML-Zeilen in Ihr Seitenelement `head` einfügen:

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @
    categories='wknd.base', defer=true}">
    ${clientlibs.jsAndCssIncludes @ context="unsafe"}
</sly>
```

Dies umfasst sowohl das CSS als auch das JS in Ihrem Seitenelement `head`, fügt jedoch das Attribut `defer` zu Ihren JS-`script`-Einfügungen hinzu, sodass Browser warten, bis das DOM bereit ist, bevor sie Ihre Skripten ausführen, und somit die Seitenladegeschwindigkeit optimieren.

## Einfache Verwendung {#basic-usage}

Die grundlegende Syntax, die sowohl JS als auch CSS einer Client-Bibliothek-Kategorie enthält und die alle zugehörigen CSS-`link`-Elemente und/oder JS-`script`-Elemente generiert, lautet wie folgt:

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.jsAndCssIncludes @ context="unsafe"}
</sly>
```

Um dies für mehrere Client-Bibliothek-Kategorien gleichzeitig zu tun, kann ein Zeichenfolgen-Array an den Parameter `categories` übergeben werden:

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @
    categories=['wknd.base', 'cq.foundation']}">
    ${clientlibs.jsAndCssIncludes @ context="unsafe"}
</sly>
```

## Nur CSS oder JS {#css-js-only}

Häufig sollen die CSS-Einfügungen im HTML-Element `head` platziert werden und die JS-Einfügungen direkt vor dem Ende des Elements `body`.

Um im Element `head` nur das CSS und nicht das JS einzuschließen, verwenden Sie `cssIncludes`:

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.cssIncludes @ context="unsafe"}
</sly>
```

Vor dem Ende des Elements `body`, um nur das JS und nicht das CSS einzuschließen, verwenden Sie `jsIncludes`:

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.jsIncludes @ context="unsafe"}
</sly>
```

## Attribute {#attributes}

Um Attribute auf die generierten CSS-`link`-Elemente und/oder JS-`script`-Elemente anzuwenden, ist eine Reihe von Parametern möglich:

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

CSS-`link`-Attribute, die an `jsAndCssIncludes` und `cssIncludes` weitergegeben werden können:

* `media`: Zeichenfolgen-JS-`script`-Attribute, die an `jsAndCssIncludes` und `jsIncludes` weitergegeben werden können:
* `async`: Boolesch
* `defer`: Boolesch
* `onload`: Zeichenfolge
* `crossorigin`: Zeichenfolge

## Inline {#inlining}

In einigen Fällen – zur Optimierung oder für E-Mail oder für [AMP](amp.md) – ist es möglicherweise erforderlich, das CSS oder JS inline in der HTML-Ausgabe zu referenzieren.

Um das CSS inline zu referenzieren, kann `cssInline` verwendet werden. In diesem Fall müssen Sie dieses umliegende `style`-Element schreiben:

```html
<style type="text/css"
    data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.cssInline @ context="unsafe"}
</style>
```

In ähnlicher Weise kann `jsInline` verwendet werden, um JS inline zu referenzieren. In diesem Fall müssen Sie dieses umliegende `script`-Element schreiben:

```html
<script type="text/javascript"
    data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.jsInline @ context="unsafe"}
</script>
```
