---
title: Einbettungskomponente
description: Die Einbettungskomponente ermöglicht das Einbetten externer Inhalte in eine AEM-Inhaltsseite.
role: Architect, Developer, Admin, User
exl-id: 985fa304-70a3-4329-957e-76d1832a06f1
source-git-commit: 6fbc781db555bc6abaed1d122a9a8756e3d53222
workflow-type: ht
source-wordcount: '1343'
ht-degree: 100%

---

# Einbettungskomponente  {#embed-component}

Die Einbettungskomponente der Kernkomponenten ermöglicht das Einbetten externer Inhalte in eine AEM-Inhaltsseite.

## Nutzung {#usage}

Mit der Einbettungskomponente der Kernkomponenten kann der Inhaltsautor ausgewählte externe Inhalte definieren, die in eine AEM-Inhaltsseite eingebettet werden sollen. Darüber hinaus gibt es die Möglichkeit, einzubettende Freiform-HTML zu definieren.

* Die Eigenschaften der Komponente können im [Dialogfeld „Konfigurieren“](#configure-dialog) definiert werden.
* Die Standardeinstellungen für die Komponente beim Hinzufügen zu einer Seite können im [Dialogfeld „Design“](#design-dialog) definiert werden.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Einbettungskomponente ist v2, die mit Version 2.18.0 der Kernkomponenten im Februar 2022 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |---|---|---|
| v2 | – | Kompatibel | Kompatibel | Kompatibel |
| [v1](v1/embed.md) | Kompatibel | Kompatibel | – | Kompatibel |

Weitere Informationen zu Kernkomponentenversionen und -freigaben finden Sie im Dokument [Kernkomponentenversionen](/help/versions.md).

## Musterkomponentenausgabe {#sample-component-output}

Um die Einbettungskomponente auszuprobieren sowie Beispiele für ihre Konfigurationsoptionen sowie HTML- und JSON-Ausgaben zu erhalten, besuchen Sie die [Komponentenbibliothek](https://adobe.com/go/aem_cmp_library_embed).

## Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur Einbettungskomponente [finden Sie auf GitHub](https://adobe.com/go/aem_cmp_tech_embed_v2_de).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Im Dialogfeld „Konfigurieren“ kann der Inhaltsautor die externe Ressource definieren, die auf der Seite eingebettet werden soll.

### Registerkarte „Eigenschaften“ {#properties-tab}

Wählen Sie zunächst, welcher Ressourcentyp eingebettet werden soll:

* [URL](#url)
* [Einbettbare Prozessoren](#embeddable)
* [HTML ](#html)

Für jeden Typ von einbettbarem Element können Sie eine **ID** festlegen. Diese Option dient zur Kontrolle der eindeutigen Kennung der Komponente in der HTML-Datei und auf der [Datenschicht](/help/developing/data-layer/overview.md).

* Wenn Sie das Feld leer lassen, wird automatisch eine eindeutige ID generiert, die Sie über die resultierende Seite finden.
* Sofern eine ID angegeben wird, ist vom Autor bzw. der Autorin sicherzustellen, dass diese eindeutig ist.
* Änderungen der ID können sich auf das CSS-, JS- und Datenschicht-Tracking auswirken.

#### URL {#url}

Die einfachste Form von Einbettung ist die URL. Fügen Sie im Feld **URL** einfach die URL der Ressource ein, die Sie einbetten möchten. Die Komponente wird versuchen, auf die Ressource zuzugreifen. Wenn sie von einem der Prozessoren wiedergegeben werden kann, wird eine Bestätigungsmeldung unter dem Feld **URL** angezeigt. Andernfalls wird das Feld mit einem Fehler markiert.

Die Einbettungskomponente wird mit Prozessoren für die folgenden Arten von Ressourcen bereitgestellt:

* Ressourcen, die dem [oEmbed-Standard](https://oembed.com/) entsprechen, einschließlich Facebook Post, Instagram, SoundCloud, Twitter und YouTube
* Pinterest

Entwickler können zusätzliche URL-Prozessoren hinzufügen, indem sie der [Entwicklerdokumentation der Einbettungskomponente folgen](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/embed/v1/embed#extending-the-embed-component).

![Dialogfeld „Bearbeiten“ der Einbettungskomponente mit Auswahl der Option „URL“](/help/assets/embed-url.png)

#### Einbettbare Prozessoren {#embeddable}

Einbettbare Prozessoren ermöglichen eine bessere Anpassung der eingebetteten Ressource, die parametrisiert werden und zusätzliche Informationen enthalten kann. Ein Autor kann aus vorkonfigurierten vertrauenswürdigen einbettbaren Prozessoren auswählen und die Komponente wird standardmäßig mit einem einbettbaren YouTube-Prozessor ausgeliefert.

Im Feld **Einbettbare** Prozessoren wird der zu verwendende Prozessortyp definiert. Im Falle des einbettbaren YouTube-Prozessors können Sie dann Folgendes definieren:

* **Video-ID** - Die eindeutige Video-ID der YouTube-Ressource, die Sie einbetten möchten
* **Breite** - Die Breite des eingebetteten Videos
* **Höhe** - Die Höhe des eingebetteten Videos
* **Stummschalten aktivieren** - Dieser Parameter gibt an, ob das Video standardmäßig stummgeschaltet abgespielt werden soll. Durch Aktivierung dieser Funktion erhöht sich die Wahrscheinlichkeit, dass die automatische Wiedergabe in modernen Browsern funktioniert.
* **Automatische Wiedergabe aktivieren** - Dieser Parameter gibt an, ob das erste Video beim Laden des Players automatisch wiedergegeben wird. Dies ist nur in der Veröffentlichungsinstanz oder bei Verwendung der Option **Als veröffentlicht anzeigen** in der Autoreninstanz wirksam.
* **Schleife aktivieren** - Bei einem einzelnen Video gibt dieser Parameter an, ob der Player das erste Video wiederholt abspielen soll. Bei einer Wiedergabeliste spielt der Player die gesamte Wiedergabeliste ab und beginnt dann wieder beim ersten Video.
* **Inline-Wiedergabe (iOS) aktivieren** - Mit diesem Parameter wird gesteuert, ob Videos in einem HTML5-Player unter iOS inline (ein) oder im Vollbildmodus (aus) wiedergegeben werden.
* **Unbeschränkte zugehörige Videos** - Wenn diese Option deaktiviert ist, kommen verwandte Videos aus demselben Kanal wie das gerade abgespielte Video, andernfalls kommen sie aus einem beliebigen Kanal.

Andere einbettbare Prozessoren weisen ähnliche Felder auf und können von einem Entwickler [unter Beachtung der Entwicklerdokumentation der Einbettungskomponente](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/embed/v1/embed#extending-the-embed-component) definiert werden.

![Dialogfeld „Bearbeiten“ der Einbettungskomponente mit Auswahl der Option „Einbettbare Prozessoren“](/help/assets/embed-embeddable.png)

>[!NOTE]
>
>Einbettbare Prozessoren müssen auf der Vorlagenebene über das [Dialogfeld „Design“](#design-dialog) aktiviert werden, damit sie dem Seitenautor zur Verfügung stehen.

#### HTML  {#html}

Mit der Einbettungskomponente können Sie Ihrer Seite Freiform-HTML hinzufügen.

![Dialogfeld „Bearbeiten“ der Einbettungskomponente mit Auswahl der Option „HTML“](/help/assets/embed-html.png)

>[!NOTE]
>Unsichere Tags wie Skripte werden aus der eingegebenen HTML gefiltert und auf der resultierenden Seite nicht wiedergegeben.

##### Sicherheit {#security}

Das HTML-Markup, das der Autor eingeben kann, wird aus Sicherheitsgründen gefiltert, um Site-übergreifende Skriptangriffe zu verhindern, die es Autoren z. B. erlauben würden, sich Administratorrechte zu verschaffen.

Im Allgemeinen werden alle Skript- und `style`-Elemente sowie alle `on*`- und `style`-Attribute aus der Ausgabe entfernt.

Die Regeln sind jedoch komplizierter, da die Einbettungskomponente dem Filterregelsatz des globalen HTML-AntiSamy-Bereinigungs-Frameworks von AEM folgt, der unter `/libs/cq/xssprotection/config.xml` zu finden ist. Dies kann bei Bedarf von einem Entwickler für eine projektspezifische Konfiguration überlagert werden.

Weitere Sicherheitsinformationen finden Sie in der [AEM-Entwicklerdokumentation für lokale Installationen](https://experienceleague.adobe.com/docs/experience-manager-65/developing/introduction/security.html?lang=de) sowie in [AEM as a Cloud Service-Installationen.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/security/home.html?lang=de)

>[!NOTE]
>
>Obwohl die Regeln des AntiSamy-Bereinigungs-Frameworks durch eine Überlagerung von `/libs/cq/xssprotection/config.xml` konfiguriert werden können, wirken sich diese Änderungen nicht nur auf die Einbettungs-Kernkomponente, sondern auf das gesamte HTL- und JSP-Verhalten aus.

### Registerkarte „Arten“ {#styles-tab-edit}

![Registerkarte „Arten“ im Dialogfeld „Bearbeiten“ der Einbettungskomponente](/help/assets/embed-styles.png)

Die Einbettungskomponente unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).

Verwenden Sie das Dropdown-Menü, um die Stile auszuwählen, die Sie auf die Komponente anwenden möchten. Die im Dialogfeld „Bearbeiten“ vorgenommenen Auswahlen haben denselben Effekt wie die in der Komponenten-Symbolleiste ausgewählten.

Stile müssen für diese Komponente im [Dialogfeld „Design“](#design-dialog) konfiguriert werden, damit das Dropdown-Menü verfügbar ist.

## Dialogfeld „Design“ {#design-dialog}

Der Dialogfeld „Design“ ermöglicht es dem Vorlagenautor, die Optionen, die für den Inhaltsautor bei Verwendung der Einbettungskomponente verfügbar sind, sowie die Standardeinstellungen bei Platzierung der Einbettungskomponente zu definieren.

### Registerkarte „Typen einbettbarer Prozessoren“ {#embeddable-types-tab}

![Dialogfeld „Design“ der Einbettungskomponente](/help/assets/embed-design.png)

* **URL deaktivieren** - Deaktiviert bei Auswahl die Option **URL** für den Inhaltsautor.
* **Einbettbare Elemente deaktivieren** - Deaktiviert bei Auswahl die Option **Einbettbare Prozessoren** für den Inhaltsautor, unabhängig davon, welche einbettbaren Prozessoren zulässig sind.
* **HTML deaktivieren** - Deaktiviert bei Auswahl die **HTML**-Option für den Inhaltsautor.
* **Zulässige einbettbare Elemente** - Mehrfachauswahl, die definiert, welche einbettbaren Prozessoren für den Inhaltsautor verfügbar sind, sofern die Option **Einbettbare Prozessoren** aktiviert ist.

### Registerkarte „YouTube“ {#youtube-tab}

![Registerkarte „YouTube“ im Dialogfeld „Design“ der Einbettungskomponente](/help/assets/embed-design-youtube.png)

* **Konfiguration des Stummschaltungsverhaltens zulassen** - Erlaubt es dem Autor von Inhalten, die Option **Stummschalten aktivieren** in der Komponente zu konfigurieren, wenn der YouTube-Einbettungstyp ausgewählt ist.
   * **Standardwert für die Stummschaltung** - Legt bei Auswahl des YouTube-Einbettungstyps automatisch die Option **Stummschalten aktivieren** fest.
* **Konfiguration des automatischen Wiedergabeverhaltens zulassen** - Erlaubt es dem Autor von Inhalten, die Option **Automatische Wiedergabe aktivieren** in der Komponente zu konfigurieren, wenn der YouTube-Einbettungstyp ausgewählt ist.
   * **Standardwert für die automatische Wiedergabe** - Legt bei Auswahl des YouTube-Einbettungstyps automatisch die Option **Automatische Wiedergabe aktivieren** fest.
* **Konfiguration des Schleifenverhaltens zulassen** - Erlaubt es dem Autor von Inhalten, die Option **Schleife aktivieren** in der Komponente zu konfigurieren, wenn der YouTube-Einbettungstyp ausgewählt ist.
   * **Standardwert für Schleifen** - Legt bei Auswahl des YouTube-Einbettungstyps automatisch die Option **Schleife aktivieren** fest.
* **Konfiguration der Inline-Wiedergabe (iOS) zulassen** - Erlaubt es dem Autor von Inhalten, die Option **Inline-Wiedergabe (iOS) aktivieren** in der Komponente zu konfigurieren, wenn der YouTube-Einbettungstyp ausgewählt ist.
   * **Standardwert für die Inline-Wiedergabe (iOS)** - Legt bei Auswahl des YouTube-Einbettungstyps automatisch die Option **Inline-Wiedergabe (iOS) aktivieren** fest.
* **Konfiguration zugehöriger Videos zulassen** - Erlaubt es dem Autor von Inhalten, die Option **Unbeschränkte zugehörige Videos** in der Komponente zu konfigurieren, wenn der YouTube-Einbettungstyp ausgewählt ist.
   * **Standardwert für unbeschränkte zugehörige Videos** - Legt bei Auswahl des YouTube-Einbettungstyps automatisch die Option **Unbeschränkte zugehörige Videos** fest.
