---
title: Embed Component
seo-title: Embed Component
description: The Embed Component enables embedding external content in an AEM content page.
seo-description: The Embed Component enables embedding external content in an AEM content page.
content-type: Referenz
topic-tags: Kernkomponenten
translation-type: tm+mt
source-git-commit: d748bf211ec36d12cac016ca9bf707f24db1ce48

---


# Embed Component{#embed-component}

The Core Components Embed Component allows embedding external content in an AEM content page.

## Nutzung {#usage}

The Core Component Embed Component allows the content author to define selected external content to be embedded within an AEM content page. In addition, there is an option to define free-form HTML to be embedded as well.

* The component's properties can be defined in the [configure dialog](#configure-dialog).
* Die Standardeinstellungen für die Komponente beim Hinzufügen zu einer Seite können im Dialogfeld [Design](#design-dialog) definiert werden.

## Version und Kompatibilität {#version-and-compatibility}

The current version of the Embed Component is v1, which was introduced with release 2.7.0 of the Core Components in September 2019, and is described in this document.

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

Im Dialogfeld "Konfigurieren"kann der Inhaltsersteller die externe Ressource definieren, die auf der Seite eingebettet werden soll. First choose which type of resource should be embedded: URL, Embeddable, or HTML.************

### URL {#url}

Die einfachste Einbettung ist die URL. Fügen Sie einfach die URL der Ressource ein, die Sie in das Feld **URL** einbetten möchten. The component will attempt to access the resource and if it can be rendered by one of the processors, it will display a confirmation message below the URL field. **** Andernfalls wird das Feld mit Fehler gekennzeichnet.

Die Einbettungskomponente wird mit Prozessoren für die folgenden Arten von Ressourcen geliefert:

* Ressourcen, die dem [oEmbed-Standard](https://oembed.com/) entsprechen, einschließlich Facebook Post, Instagram, SoundCloud, Twitter und YouTube
* Pinterest

Developers can add additional URL processors by [following the developer documentation of the Embed Component.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/embed/v1/embed#extending-the-embed-component)

![](assets/screen-shot-2019-09-25-10.08.29.png)

### Einbettbar {#embeddable}

Einbettbare ermöglichen eine stärkere Anpassung der eingebetteten Ressource, die parametrisiert werden kann und zusätzliche Informationen enthält. Ein Autor kann aus vorkonfigurierten vertrauenswürdigen Einbettungsvariablen auswählen und die Komponente wird mit einer YouTube-Einbettung geliefert, die standardmäßig installiert werden kann.

Das Feld **Einbetten** definiert den zu verwendenden Prozessortyp. Im Falle der YouTube-Einbettung können Sie dann Folgendes definieren:

* **Video-ID** - Die eindeutige Video-ID von YouTube der Ressource, die Sie einbetten möchten
* **Breite** - Die Breite des eingebetteten Videos
* **Höhe** - Die Höhe des eingebetteten Videos

Andere Einbettungsvariablen bieten ähnliche Felder an und können von einem Entwickler anhand der Entwicklerdokumentation der Einbettungskomponente definiert werden. [Dies gilt auch für Einbettungselemente.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/embed/v1/embed#extending-the-embed-component)

![](assets/screen-shot-2019-09-25-10.15.00.png)

>[!NOTE]
>Einbettbare müssen auf Vorlagenebene über das [Designdialogfeld](#design-dialog) aktiviert werden, damit sie dem Seitenautor zur Verfügung stehen.

### HTML {#html}

Mit der Einbettungskomponente können Sie Ihrer Seite Freiform-HTML hinzufügen.

![](assets/screen-shot-2019-09-25-10.20.00.png)

>[!NOTE]
>Unsichere Tags wie Skripten werden aus dem eingegebenen HTML gefiltert und nicht auf der resultierenden Seite wiedergegeben.

## Dialogfeld „Design“ {#design-dialog}

The design dialog allows the template author to define the options available to the content author who uses the Embed Component and the defaults set when placing the Embed Component.

![](assets/screen-shot-2019-09-25-10.25.28.png)

* **URL** deaktivieren - Deaktiviert die Option " **URL** "für den Inhaltsautor, wenn ausgewählt
* **Einbettbare** deaktivieren: Deaktiviert die Option " **Einbetten** "für den Inhaltsersteller, sofern ausgewählt, unabhängig davon, welche Prozessoren einbetten können.
* **HTML** deaktivieren - Deaktiviert die **HTML** -Option für den Inhaltsautor, wenn diese ausgewählt ist.
* **Zulässige Einbettungen** - Diese Option definiert, welche einbettbaren Prozessoren für den Inhaltsersteller verfügbar sind, sofern die Option **Einbetten** aktiv ist.
