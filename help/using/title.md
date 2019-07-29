---
title: Titelkomponente
seo-title: Titelkomponente
description: 'null'
seo-description: Die Kernkomponente „Titelkomponente“ ist eine Komponente für Abschnittsüberschriften, die eine Bearbeitung im Kontext ermöglicht.
uuid: cf190861-e5cd-42b8-9193-842b8df8c5c6
contentOwner: Benutzer
content-type: Referenz
topic-tags: Authoring
products: SG_EXPERIENCEMANAGER/CORECOMPONENTS-new
discoiquuid: 243efc75-fcf9-427d-9303-9642b0602991
index: y
internal: n
snippet: y
translation-type: ht
source-git-commit: eef608fb06001485aa2c2c0b574af412ed7f15a4

---


# Titelkomponente{#title-component}

Die Kernkomponente „Titelkomponente“ ist eine Komponente für Abschnittsüberschriften, die eine Bearbeitung im Kontext ermöglicht.

## Nutzung {#usage}

Die Titelkomponente soll als Titel oder Überschrift eines Inhaltsabschnitts verwendet werden. Die verfügbaren Überschriftenebenen können vom Vorlagenautor im [Dialogfeld „Design“](#design-dialog) definiert werden. Der Inhaltseditor kann aus verfügbaren Überschriftenebenen im [Dialogfeld „Bearbeiten“](#edit-dialog) auswählen. Für zusätzlichen Komfort steht auch eine einfache direkte Bearbeitung des Überschriftentexts zur Verfügung.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Titelkomponente ist v2, die mit Version 2.0.0 der Kernkomponenten im Januar 2018 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|---|---|---|---|
| v2 | Kompatibel | Kompatibel | Kompatibel |
| [v1](title-v1.md) | Kompatibel | Kompatibel | Kompatibel |

Weitere Informationen zu Kernkomponentenversionen und -freigaben finden Sie in den [Kernkomponentenversionen](versions.md).

## Musterkomponentenausgabe {#sample-component-output}

Um die Titelkomponente zu erleben und Beispiele für ihre Konfigurationsoptionen sowie die HTML- und JSON-Ausgabe zu sehen, besuchen Sie die [Komponentenbibliothek](http://opensource.adobe.com/de/aem-core-wcm-components/library/title.html).

### Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur Titelkomponente [finden Sie auf GitHub](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/title/v2/title).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](developing.md).

## Dialogfeld „Bearbeiten“ {#edit-dialog}

Im Dialogfeld „Bearbeiten“ kann der Inhaltsautor den Titeltext definieren sowie die Überschriftenebene auswählen.

* **Titel** - Wenn leer, wird der Seitentitel verwendet
* **Typ/Größe** - Definiert die Überschriftenebene des Titels
* **Link** - Definiert den Inhalt, auf den der Titel verweist. Dies kann ein Pfad zu einer Inhaltsseite, eine externe URL oder ein Seitenanker sein.

![](assets/screenshot_2018-10-19at110055.png)

>[!CAUTION]
>
>Die Möglichkeit, einen Link für den Titel zu definieren, wurde mit Version 2.2.0 der Kernkomponenten eingeführt.

Der Editor für die Bearbeitung im Kontext kann auch verwendet werden, um den Text der Titelkomponente zu bearbeiten.

![](assets/chlimage_1-37.png)

## Dialogfeld „Design“ {#design-dialog}

Das Dialogfeld „Design“ ermöglicht es dem Vorlagenautor, die standardmäßige Überschriftenebene zu definieren, die Titelkomponenten bei der Erstellung durch Inhaltsautoren haben.

### Registerkarte „Größen“{#sizes-tab}

![](assets/screenshot_2018-10-19at110120.png)

* **Zulässige Typen/Größen für Autoren** - Aktiviert oder deaktiviert die Überschrifttypen, die für Inhaltsautoren verfügbar sind, wenn sie die Titelkomponente verwenden.
* **Standardtyp/-größe** - Definieren Sie den Überschrifttyp, der automatisch zugewiesen wird, wenn ein Inhaltsautor die Titelkomponente zu einer Seite hinzufügt.
* **Link deaktivieren** - Deaktiviert die Unterstützung für Links in der Titelkomponente, um Inhaltsautoren zu verbieten, von Titeln zu verlinken.

>[!CAUTION]
>
>Die Möglichkeit, einen Link für den Titel zu definieren, wurde mit Version 2.2.0 der Kernkomponenten eingeführt.

### Registerkarte „Stile“ {#styles-tab}

Die Titelkomponente unterstützt das AEM-[Stilsystem](authoring.md#component-styling).