---
title: Einbettungskomponente
description: Die Einbettungskomponente ermöglicht das Einbetten externer Inhalte in eine AEM-Inhaltsseite.
translation-type: tm+mt
source-git-commit: 601bee9df2a82255c92fcf30b8dacde70b0583dc
workflow-type: tm+mt
source-wordcount: '1341'
ht-degree: 65%

---


# Einbettungskomponente{#embed-component}

Die Einbettungskomponente der Kernkomponenten ermöglicht das Einbetten externer Inhalte in eine AEM-Inhaltsseite.

## Verwendung {#usage}

Mit der Einbettungskomponente der Kernkomponenten kann der Inhaltsautor ausgewählte externe Inhalte definieren, die in eine AEM-Inhaltsseite eingebettet werden sollen. Darüber hinaus gibt es die Möglichkeit, einzubettende Freiform-HTML zu definieren.

* Die Eigenschaften der Komponente können im [Dialogfeld „Konfigurieren“](#configure-dialog) definiert werden.
* Die Standardeinstellungen für die Komponente beim Hinzufügen zu einer Seite können im [Dialogfeld „Design“](#design-dialog) definiert werden.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Einbettungskomponente ist v1. Sie wurde mit Version 2.7.0 der Kernkomponenten im September 2019 eingeführt und wird in diesem Dokument beschrieben.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Kompatibel | Kompatibel | Kompatibel |

Weitere Informationen zu Kernkomponentenversionen und -freigaben finden Sie in den [Kernkomponentenversionen](/help/versions.md).

## Musterkomponentenausgabe {#sample-component-output}

Um die Einbettungskomponente auszuprobieren sowie Beispiele für ihre Konfigurationsoptionen sowie HTML- und JSON-Ausgaben zu erhalten, besuchen Sie die [Komponentenbibliothek](https://adobe.com/go/aem_cmp_library_embed_de).

## Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur Einbettungskomponente [finden Sie auf GitHub](https://adobe.com/go/aem_cmp_tech_embed_v1_de).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Im Dialogfeld „Konfigurieren“ kann der Inhaltsautor die externe Ressource definieren, die auf der Seite eingebettet werden soll. Wählen Sie zunächst, welche Ressource eingebettet werden soll:

* [URL](#url)
* [Einbettbare Prozessoren](#embeddable)
* [HTML](#html)

Für jeden Typ von einbettbarem Element können Sie die **Anzeigen-ID** festlegen. Diese Option dient zur Kontrolle der eindeutigen Kennung der Komponente in der HTML-Datei und auf der [Datenschicht](/help/developing/data-layer/overview.md).

* Wenn Sie das Feld leer lassen, wird automatisch eine eindeutige ID generiert, die Sie über die resultierende Seite finden.
* Sofern eine ID angegeben wird, ist vom Autor sicherzustellen, dass diese eindeutig ist.
* Änderungen der ID können sich auf das CSS-, JS- und Datenschicht-Tracking auswirken.

### URL {#url}

Die einfachste Form von Einbettung ist die URL. Fügen Sie im Feld **URL** einfach die URL der Ressource ein, die Sie einbetten möchten. Die Komponente wird versuchen, auf die Ressource zuzugreifen. Wenn sie von einem der Prozessoren wiedergegeben werden kann, wird eine Bestätigungsmeldung unter dem Feld **URL** angezeigt. Andernfalls wird das Feld mit einem Fehler markiert.

Die Einbettungskomponente wird mit Prozessoren für die folgenden Arten von Ressourcen bereitgestellt:

* Ressourcen, die dem [oEmbed-Standard](https://oembed.com/) entsprechen, einschließlich Facebook Post, Instagram, SoundCloud, Twitter und YouTube
* Pinterest

Entwickler können zusätzliche URL-Prozessoren hinzufügen, indem sie der [Entwicklerdokumentation der Einbettungskomponente folgen](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/embed/v1/embed#extending-the-embed-component).

![Dialogfeld „Bearbeiten“ der Einbettungskomponente mit Auswahl der Option „URL“](/help/assets/embed-url.png)

### Einbettbare Prozessoren {#embeddable}

Einbettbare Prozessoren ermöglichen eine bessere Anpassung der eingebetteten Ressource, die parametrisiert werden und zusätzliche Informationen enthalten kann. Ein Autor kann aus vorkonfigurierten vertrauenswürdigen Einbettungsvariablen wählen und die Komponente wird mit einer YouTube-Einbettungsoption ausgeliefert.

Im Feld **Einbettbare Prozessoren** wird der zu verwendende Prozessortyp definiert. Im Falle des einbettbaren YouTube-Prozessors können Sie dann Folgendes definieren:

* **Video-ID** - Die eindeutige Video-ID der YouTube-Ressource, die Sie einbetten möchten
* **Breite** - Die Breite des eingebetteten Videos
* **Höhe** - Die Höhe des eingebetteten Videos
* **Mute**  aktivieren: Dieser Parameter gibt an, ob das Video standardmäßig stummgeschaltet abgespielt wird. Durch Aktivierung dieser Funktion erhöht sich die Wahrscheinlichkeit, dass Autoplay in modernen Browsern funktioniert.
* **Automatische Wiedergabe**  aktivieren: Dieser Parameter gibt an, ob beim Laden des Players automatisch der Beginn für das erste Video abgespielt wird. Dies ist nur bei der Veröffentlichungsinstanz oder bei Verwendung der Option **Ansicht als Veröffentlicht** in der Authoring-Instanz wirksam.
* **Schleife**  aktivieren: Bei einem einzelnen Video gibt dieser Parameter an, ob der Player das erste Video wiederholt abspielen soll. Bei einer Wiedergabeliste spielt der Player die gesamte Wiedergabeliste ab, und beim ersten Video wird erneut der Beginn abgespielt.
* **Inline-Wiedergabe aktivieren (iOS)**  - Dieser Parameter steuert, ob Videos unter iOS im Inline-Modus (ein) oder Vollbild (aus) in einem HTML5-Player abgespielt werden.
* **Uneingeschränkte Videos**  - Wenn diese Option deaktiviert ist, werden verwandte Videos vom gleichen Kanal wie das gerade abgespielte Video stammen, andernfalls werden sie von einem beliebigen Kanal gesendet.

Beachten Sie, dass die Optionen zum Aktivieren über das [Designdialogfeld](#design-dialog) aktiviert werden müssen und als Standardwerte festgelegt werden können.

Andere einbettbare Prozessoren weisen ähnliche Felder auf und können von einem Entwickler [unter Beachtung der Entwicklerdokumentation der Einbettungskomponente definiert werden](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/embed/v1/embed#extending-the-embed-component).

![Dialogfeld „Bearbeiten“ der Einbettungskomponente mit Auswahl der Option „Einbettbare Prozessoren“](/help/assets/embed-embeddable.png)

>[!NOTE]
>Einbettbare Prozessoren müssen auf der Vorlagenebene über das [Dialogfeld „Design“](#design-dialog) aktiviert werden, damit sie dem Seitenautor zur Verfügung stehen.

### HTML {#html}

Mit der Einbettungskomponente können Sie Ihrer Seite Freiform-HTML hinzufügen.

![Dialogfeld „Bearbeiten“ der Einbettungskomponente mit Auswahl der Option „HTML“](/help/assets/embed-html.png)

>[!NOTE]
>Unsichere Tags wie Skripte werden aus der eingegebenen HTML gefiltert und auf der resultierenden Seite nicht wiedergegeben.

#### Sicherheit {#security}

Das HTML-Markup, das der Autor eingeben kann, wird aus Sicherheitsgründen gefiltert, um siteübergreifende Skriptangriffe zu verhindern, die es Autoren z. B. erlauben würden, sich Administratorrechte zu verschaffen.

*Im Allgemeinen* werden alle Skript- und `style`-Elemente sowie alle `on*`- und `style`-Attribute aus der Ausgabe entfernt.

Die Regeln sind jedoch komplizierter, da die Einbettungskomponente AEM globalen HTML AntiSamy-Filterregelsatz des Sanitärrahmens folgt, der unter `/libs/cq/xssprotection/config.xml` zu finden ist. Dies kann bei Bedarf von einem Entwickler für eine projektspezifische Konfiguration überlagert werden.

Weitere Sicherheitsinformationen finden Sie in der [AEM-Entwicklerdokumentation für lokale Installationen](https://docs.adobe.com/content/help/en/experience-manager-65/developing/introduction/security.html) sowie in [AEM as a Cloud Service-Installationen.](https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/security/home.translate.html)

>[!NOTE]
>Obwohl die Regeln des AntiSamy-Bereinigungs-Frameworks durch eine Überlagerung von `/libs/cq/xssprotection/config.xml` konfiguriert werden können, wirken sich diese Änderungen nicht nur auf die Einbettungs-Kernkomponente, sondern auf das gesamte HTL- und JSP-Verhalten aus.

## Dialogfeld „Design“ {#design-dialog}

Der Dialogfeld „Design“ ermöglicht es dem Vorlagenautor, die Optionen, die für den Inhaltsautor bei Verwendung der Einbettungskomponente verfügbar sind, sowie die Standardeinstellungen bei Platzierung der Einbettungskomponente zu definieren.

### Registerkarte &quot;Einbettbare Typen&quot; {#embeddable-types-tab}

![Dialogfeld „Design“ der Einbettungskomponente](/help/assets/embed-design.png)

* **URL deaktivieren** - Deaktiviert bei Auswahl die Option **URL** für den Inhaltsautor.
* **Einbettbare Prozessoren deaktivieren** - Deaktiviert bei Auswahl die Option **Einbettbare Prozessoren** für den Inhaltsautor, unabhängig davon, welche einbettbaren Prozessoren zulässig sind.
* **HTML deaktivieren** - Deaktiviert bei Auswahl die **HTML**-Option für den Inhaltsautor.
* **Zulässige Einbettungen**  - Multiselect, das definiert, welche einbettbaren Prozessoren für den Inhaltsersteller verfügbar sind, sofern die Option  **** Einbetten aktiv ist.

### YouTube-Registerkarte {#youtube-tab}

![Registerkarte &quot;YouTube&quot;des Dialogfelds &quot;Design&quot;der Komponente &quot;Einbetten&quot;](/help/assets/embed-design-youtube.png)

* **Konfiguration des Ton-Verhaltens**  zulassen - Ermöglicht dem Inhaltsersteller, die Option &quot; **Multimedia** aktivieren&quot;in der Komponente zu konfigurieren, wenn der YouTube-Einbettungstyp ausgewählt ist
   * **Standardwert von stumm**  - Legt bei Auswahl des YouTube-Einbettungstyps automatisch die Option  **Muteaktivieren** fest
* **Konfiguration des autoplay-Verhaltens**  zulassen - Ermöglicht dem Inhaltsersteller die Konfiguration der Option &quot; **Autoplay** aktivieren&quot;in der Komponente, wenn der YouTube-Einbettungstyp ausgewählt ist
   * **Standardwert der automatischen Wiedergabe** : Legt bei Auswahl des YouTube-Einbettungstyps automatisch die Option &quot; **Autoplayage** aktivieren&quot;fest
* **Konfiguration des Schleifenverhaltens**  zulassen: Ermöglicht dem Inhaltsersteller, die Option &quot;Loopoption  **** aktivieren&quot;in der Komponente zu konfigurieren, wenn der YouTube-Einbettungstyp ausgewählt ist
   * **Standardwert für Schleife**  - Legt die Option &quot;Schleife  **** aktivieren&quot;automatisch fest, wenn der YouTube-Einbettungstyp ausgewählt ist.
* **Konfiguration der Inline-Wiedergabe zulassen (iOS)**  - Ermöglicht dem Inhaltsersteller, die  **Option &quot;Inline-Wiedergabe** aktivieren&quot;(iOS)in der Komponente zu konfigurieren, wenn der YouTube-Einbettungstyp ausgewählt ist
   * **Standardwert der Inline-Wiedergabe (iOS)**  - Legt die  **Option &quot;Inline-Wiedergabe** aktivieren&quot;(iOS)automatisch fest, wenn der YouTube-Einbettungstyp ausgewählt ist
* **Konfiguration von Inline-Videos**  zulassen - Ermöglicht es Inhaltsautoren, die Option &quot; **Uneingeschränkte verwandte** Videos&quot;in der Komponente zu konfigurieren, wenn der YouTube-Einbettungstyp ausgewählt ist
   * **Standardwert von unbeschränkten zugehörigen Videos**  - Legt automatisch die Option &quot; **Uneingeschränkte verwandte** Videos&quot;fest, wenn der YouTube-Einbettungstyp ausgewählt ist
