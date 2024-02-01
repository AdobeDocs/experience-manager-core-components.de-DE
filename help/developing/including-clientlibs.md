---
title: Client-Bibliotheken und die Kernkomponenten
description: Die Kernkomponenten sind mit einer Reihe von Client-Bibliotheken ausgestattet und bieten die Möglichkeit, eigene zu integrieren.
role: Architect, Developer, Admin
exl-id: 84e7c178-247b-42a2-99bf-6d1699ecee14
source-git-commit: d39fe0084522f67664203a026340b23d325c1883
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 65%

---


# Client-Bibliotheken und die Kernkomponenten {#client-libraries}

Die Kernkomponenten sind mit einer Reihe von Client-Bibliotheken ausgestattet und bieten die Möglichkeit, eigene zu integrieren.

## Bereitgestellte Client-Bibliotheken {#provided}

Die Kernkomponenten stellen die folgenden Client-Bibliotheken standardmäßig bereit.

* Die **site** clientlibs bieten das minimalistische funktionale Verhalten der Komponenten, die auf die Site angewendet werden sollen.
   * Sie dienen als Ausgangspunkt für die Beschleunigung von Projekten, wobei Implementierungen ermutigt werden, [anpassen](/help/developing/customizing.md) um das gewünschte Erscheinungsbild und die gewünschte Funktionalität zu erzielen.
* Die **editor** clientlibs werden auf das Authoring-Dialogfeld angewendet, um die erwartete Funktionalität und Darstellung sicherzustellen.
* Die **editorhook** clientlibs werden auf die Site angewendet, wenn sie im Bearbeitungsmodus geladen werden.
   * Sie enthalten JavaScript-Code, der bei von Editoren ausgelösten Ereignissen ausgeführt wird, was die Initialisierung dynamischer Funktionen erleichtert.
* Einige Komponenten können bestimmte zusätzliche Client-Bibliotheken haben, die für die Verwendung in bestimmten Situationen entwickelt wurden, z. B. wenn sie neben [Dynamic Media](/help/components/image.md#dynamic-media) zum Beispiel.

## Einschließen von Client-Bibliotheken {#including}

Je nach Nutzungsszenario gibt es verschiedene Möglichkeiten, [Client-Bibliotheken](/help/developing/archetype/front-end.md#clientlibs) einzuschließen. Im Folgenden finden Sie Beispiele für Beispiele [HTL-Snippets](https://experienceleague.adobe.com/docs/experience-manager-htl/using/overview.html?lang=de) für jede.

### Empfohlene Standardverwendung {#recommended-default-usage}

Wenn Sie keine Zeit haben, die beste Lösung für Ihre Situation zu ermitteln, schließen Sie Ihre Client-Bibliotheken mit ein, indem Sie die folgenden HTL-Zeilen in Ihr Seitenelement `head` einfügen:

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @
    categories='wknd.base', defer=true}">
    ${clientlibs.jsAndCssIncludes @ context="unsafe"}
</sly>
```

Dies umfasst sowohl das CSS als auch das JS in Ihrem Seitenelement `head`, fügt jedoch das Attribut `defer` zu Ihren JS-`script`-Einfügungen hinzu, sodass Browser warten, bis das DOM bereit ist, bevor sie Ihre Skripten ausführen, und somit die Seitenladegeschwindigkeit optimieren.

### Einfache Verwendung {#basic-usage}

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

### Nur CSS oder JS {#css-js-only}

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

### Attribute {#attributes}

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

### Inline {#inlining}

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

### Laden von kontextsensitivem CSS und JavaScript {#context-aware-loading}

Die [Seitenkomponente](/help/components/page.md) unterstützt auch das Laden von kontextsensitivem CSS, JavaScript oder von Meta-Tags, die vom Entwickler definiert wurden.

Dies geschieht durch Erstellen einer [kontextsensitiven Ressource](context-aware-configs.md) für `com.adobe.cq.wcm.core.components.config.HtmlPageItemsConfig` unter Verwendung der folgenden Struktur:

```text
com.adobe.cq.wcm.core.components.config.HtmlPageItemsConfig
    - prefixPath="/some/path"
    + item01
        - element=["link"|"script"|"meta"]
        - location=["header"|"footer"]
        + attributes
            - attributeName01="attributeValue01"
            - attributeName02="attributeValue02"
            ...
    + item02
        ...
    ...
```

[Weitere Informationen finden Sie in der technischen Dokumentation zur Seitenkomponente.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/page/v2/page#loading-of-context-aware-cssjs)
