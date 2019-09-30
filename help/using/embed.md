---
title: Embed Component
seo-title: Embed Component
description: The Embed Component enables embedding external content in an AEM content page.
seo-description: he Embed Component enables embedding external content in an AEM content page.
content-type: Referenz
topic-tags: Kernkomponenten
translation-type: tm+mt
source-git-commit: 6882a0d8247328c403dc11a25ed9d079aefede69

---


# Embed Component{#embed-component}

Die Komponente "Core-Komponenten einbetten"ermöglicht das Einbetten externer Inhalte in eine AEM-Inhaltsseite.

## Nutzung {#usage}

The Core Component Embed Component allows the content author to define selected external content to be embedded within an AEM content page. In addition, there is an option to define free-form HTML to be embedded as well.

* Die Eigenschaften der Komponente können im Dialogfeld [Konfigurieren](#configure-dialog) definiert werden.
* Die Standardeinstellungen für die Komponente beim Hinzufügen zu einer Seite können im Dialogfeld [Design](#design-dialog) definiert werden.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Einbettungskomponente ist Version 1, die mit Version 2.7.0 der Kernkomponenten im September 2019 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |---|
| v1 | Kompatibel | Kompatibel | Kompatibel |

Weitere Informationen zu Kernkomponentenversionen und -freigaben finden Sie in den [Kernkomponentenversionen](versions.md).

## Musterkomponentenausgabe {#sample-component-output}

To experience the Embed Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](http://opensource.adobe.com/aem-core-wcm-components/library/embed.html).

## Technische Details {#technical-details}

The latest technical documentation about the Embed Component can be found on GitHub.[](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/embed/v1/embed)

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](developing.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

The configure dialog allows the content author to define the external resource to be embedded on the page. Wählen Sie zunächst aus, welche Ressource eingebettet werden soll: **URL**, **Einbettbar** oder **HTML**.

### URL {#url}

Die einfachste Einbettung ist die URL. Fügen Sie einfach die URL der Ressource ein, die Sie in das Feld **URL** einbetten möchten. Die Komponente versucht, auf die Ressource zuzugreifen. Wenn sie von einem der Prozessoren wiedergegeben werden kann, wird eine Bestätigungsmeldung unter dem Feld " **URL** "angezeigt. Andernfalls wird das Feld mit Fehler gekennzeichnet.

Die Einbettungskomponente wird mit Prozessoren für die folgenden Arten von Ressourcen geliefert:

* Ressourcen, die dem [oEmbed-Standard](https://oembed.com/) entsprechen, einschließlich Facebook Post, Instagram, SoundCloud, Twitter und YouTube
* Pinterest

Entwickler können zusätzliche URL-Prozessoren hinzufügen, indem sie der Entwicklerdokumentation der Einbettungskomponente [folgen.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/embed/v1/embed#extending-the-embed-component)

![](assets/screen-shot-2019-09-25-10.08.29.png)

### Einbetten {#embeddable}

Einbettbare ermöglichen eine stärkere Anpassung der eingebetteten Ressource, die parametrisiert werden kann und zusätzliche Informationen enthält. Ein Autor kann aus vorkonfigurierten vertrauenswürdigen Einbettbaren auswählen und die Komponente wird mit einem YouTube-Prozessor geliefert.

Das Feld **Einbetten** definiert den zu verwendenden Prozessortyp. Im Falle des YouTube-Prozessors können Sie dann Folgendes definieren:

* **Video-ID** - Die eindeutige Video-ID von YouTube der Ressource, die Sie einbetten möchten
* **Breite** - Die Breite des eingebetteten Videos
* **Höhe** - Die Höhe des eingebetteten Videos

Andere Prozessoren bieten ähnliche Felder an und können von einem Entwickler anhand der Entwicklerdokumentation der Einbettungskomponente definiert [werden.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/embed/v1/embed#extending-the-embed-component)

![](assets/screen-shot-2019-09-25-10.15.00.png)

>[!NOTE]
>Eingebettete Prozessoren müssen auf Vorlagenebene über das [Designdialogfeld](#design-dialog) aktiviert werden, damit sie dem Seitenautor zur Verfügung stehen.

### HTML {#html}

Mit der Einbettungskomponente können Sie Ihrer Seite Freiform-HTML hinzufügen.

![](assets/screen-shot-2019-09-25-10.20.00.png)

>[!NOTE]
>Unsichere Tags wie Skripten werden aus dem eingegebenen HTML gefiltert und nicht auf der resultierenden Seite wiedergegeben.

## Dialogfeld „Design“ {#design-dialog}

Im Dialogfeld "Entwurf"kann der Vorlagenautor die Optionen festlegen, die dem Inhaltsautor, der die Einbettungskomponente verwendet, zur Verfügung stehen, sowie die beim Platzieren der Einbettungskomponente festgelegten Standardwerte.

![](assets/screen-shot-2019-09-25-10.25.28.png)

* **URL** deaktivieren - Deaktiviert die Option " **URL** "für den Inhaltsautor, wenn ausgewählt
* **Disable Embeddables - Disables the Embeddable option for the content author when selected, regardless of which embeddable processors are allowed.******
* **Disable HTML - Disables the HTML option for the content author when selected.******
* **Allowed Embeddables - Multislect that defines which embeddable processors are avaiable to the content author, provided that the Embeddable option is active.******
