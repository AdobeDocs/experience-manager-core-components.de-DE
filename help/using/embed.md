---
title: Komponente einbetten
seo-title: Komponente einbetten
description: Die Einbettungskomponente ermöglicht das Einbetten externer Inhalte in eine AEM-Inhaltsseite.
seo-description: Die Einbettungskomponente ermöglicht das Einbetten externer Inhalte in eine AEM-Inhaltsseite.
content-type: Referenz
topic-tags: Kernkomponenten
translation-type: tm+mt
source-git-commit: e4fdefd392281f4f9101b28a15846c922e3a52c1

---


# Komponente einbetten{#embed-component}

Die Komponente "Core-Komponenten einbetten"ermöglicht das Einbetten externer Inhalte in eine AEM-Inhaltsseite.

## Nutzung {#usage}

Mit der Komponente "Einbettung der Kernkomponente"kann der Inhaltsersteller ausgewählte externe Inhalte definieren, die in eine AEM-Inhaltsseite eingebettet werden sollen. Darüber hinaus gibt es die Möglichkeit, frei formbares HTML zu definieren, das ebenfalls eingebettet werden soll.

* The component's properties can be defined in the [configure dialog](#configure-dialog).
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

Die aktuelle technische Dokumentation zur Embed-Komponente [finden Sie auf GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/embed/v1/embed).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](developing.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Im Dialogfeld "Konfigurieren"kann der Inhaltsersteller die externe Ressource definieren, die auf der Seite eingebettet werden soll. Wählen Sie zunächst aus, welche Ressource eingebettet werden soll:

* [URL](#url)
* [Einbettbar](#embeddable)
* [HTML](#html)

### URL {#url}

Die einfachste Einbettung ist die URL. Fügen Sie einfach die URL der Ressource ein, die Sie in das Feld **URL** einbetten möchten. Die Komponente versucht, auf die Ressource zuzugreifen. Wenn sie von einem der Prozessoren wiedergegeben werden kann, wird eine Bestätigungsmeldung unter dem Feld " **URL** "angezeigt. Andernfalls wird das Feld mit Fehler gekennzeichnet.

Die Einbettungskomponente wird mit Prozessoren für die folgenden Arten von Ressourcen geliefert:

* Ressourcen, die dem [oEmbed-Standard](https://oembed.com/) entsprechen, einschließlich Facebook Post, Instagram, SoundCloud, Twitter und YouTube
* Pinterest

Entwickler können zusätzliche URL-Prozessoren hinzufügen, indem sie der Entwicklerdokumentation der Einbettungskomponente [folgen.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/embed/v1/embed#extending-the-embed-component)

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

#### Sicherheit {#security}

Das HTML-Markup, das der Autor eingeben kann, wird aus Sicherheitsgründen gefiltert, um Site-übergreifende Skriptangriffe zu vermeiden, die Autoren z. B. Administratorrechte zuweisen könnten.

Im Allgemeinen werden alle Skripten und `style` -Elemente sowie alle `on*` und `style` Attribute aus der Ausgabe entfernt.

Die Regeln sind jedoch komplizierter als die, da die Einbettungskomponente dem globalen HTML-AntiSami-Filterregelsatz von AEM folgt, der unter `/libs/cq/xssprotection/config.xml`finden wird. Dies kann bei Bedarf von einem Entwickler für eine projektspezifische Konfiguration überlagert werden.

>[!NOTE]
>Obwohl die AntiSamy-Regeln durch Überlagerung konfiguriert werden können, wirken sich diese Änderungen auf das gesamte Verhalten von HTL und JSP aus und nicht nur auf die Komponente "Core einbetten". `/libs/cq/xssprotection/config.xml`

## Dialogfeld „Design“ {#design-dialog}

Im Dialogfeld "Entwurf"kann der Vorlagenautor die Optionen festlegen, die dem Inhaltsautor, der die Einbettungskomponente verwendet, zur Verfügung stehen, sowie die beim Platzieren der Einbettungskomponente festgelegten Standardwerte.

![](assets/screen-shot-2019-09-25-10.25.28.png)

* **URL** deaktivieren - Deaktiviert die Option " **URL** "für den Inhaltsautor, wenn ausgewählt
* **Einbettbare** deaktivieren: Deaktiviert die Option " **Einbetten** "für den Inhaltsersteller, sofern ausgewählt, unabhängig davon, welche Prozessoren einbetten können.
* **HTML** deaktivieren - Deaktiviert die **HTML** -Option für den Inhaltsautor, wenn diese ausgewählt ist.
* **Zulässige Einbettungen** - Diese Option definiert, welche einbettbaren Prozessoren für den Inhaltsersteller verfügbar sind, sofern die Option **Einbetten** aktiv ist.
