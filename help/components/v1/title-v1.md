---
title: Titelkomponente (v1)
description: Die Kernkomponente „Titelkomponente“ ist eine Komponente für Abschnittsüberschriften, die eine Bearbeitung im Kontext ermöglicht.
index: n
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# Titelkomponente (v1) {#title-component-v}

Die Kernkomponente „Titelkomponente“ ist eine Komponente für Abschnittsüberschriften, die eine Bearbeitung im Kontext ermöglicht.

## Nutzung {#usage}

Die Titelkomponente soll als Titel oder Überschrift eines Inhaltsabschnitts verwendet werden.

Die verfügbaren Überschriftenebenen können vom Vorlagenautor im [Dialogfeld „Design“](#design-dialog) definiert werden. Der Inhaltseditor kann aus verfügbaren Überschriftenebenen im [Dialogfeld „Bearbeiten“](#edit-dialog) auswählen. Für zusätzlichen Komfort steht auch eine einfache direkte Bearbeitung des Überschriftentexts zur Verfügung.

## Version und Kompatibilität {#version-and-compatibility}

In diesem Dokument wird v1 der Titelkomponente beschrieben, die ursprünglich mit Version 1.0.0 der Kernkomponenten mit AEM 6.3 eingeführt wurde.

In der folgenden Tabelle ist die Kompatibilität von v1 der Titelkomponente aufgeführt.

| AEM-Version | Titelkomponente v1 |
|--- |--- |
| 6.3 | Kompatibel |
| 6.4 | Kompatibel |

>[!CAUTION]
>
>In diesem Dokument wird v1 der Titelkomponente beschrieben.
>
>Weitere Informationen zur aktuellen Version der Titelkomponente finden Sie im Dokument [Titelkomponente](/help/components/title.md).

## Musterkomponentenausgabe {#sample-component-output}

Im Folgenden finden Sie ein Beispiel von [We.Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

### Screenshot {#screenshot}

![](/help/assets/chlimage_1-36.png)

### HTML {#html}

```
<div class="cmp cmp-title aem-GridColumn aem-GridColumn--default--12">
     <h2>Welcome! This is our finest equipment!</h2>
</div>
```

### JSON {#json}

```
"title": {
              "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
              ":type": "weretail/components/content/title",
              "jcr:title": "Welcome! This is our finest equipment!",
              "type": "h2"
            }
```

>[!NOTE]
>
>Für JSON-Exporte aus den Kernkomponenten ist Version 1.1.0 der Kernkomponenten erforderlich. Weitere Informationen finden Sie in den [Kompatibilitätsinformationen für Kernkomponenten v1](/help/versions.md).

## Dialogfeld „Bearbeiten“ {#edit-dialog}

Im Dialogfeld „Bearbeiten“ kann der Inhaltsautor den Titeltext definieren sowie die Überschriftenebene auswählen.

>[!NOTE]
>
>Bei einem leeren Wert für den Titel wird der Seitentitel angezeigt.

![](/help/assets/chlimage_1-91.png)

Der Editor für die Bearbeitung im Kontext kann auch verwendet werden, um den Text der Titelkomponente zu bearbeiten.

![](/help/assets/chlimage_1-37.png)

## Dialogfeld „Design“ {#design-dialog}

Das Dialogfeld „Design“ ermöglicht es dem Vorlagenautor, die standardmäßige Überschriftenebene zu definieren, die Titelkomponenten bei der Erstellung durch Inhaltsautoren haben.

![](/help/assets/chlimage_1-92.png)

## Technische Details {#technical-details}

The latest technical documentation about the Title Component [can be found on GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/title/v1/title).

Das gesamte Kernkomponentenprojekt kann von GitHub heruntergeladen werden.

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation von Kernkomponenten für Entwickler](/help/developing/overview.md).
