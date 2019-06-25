---
title: Navigationskomponente
seo-title: Navigationskomponente
description: 'null'
seo-description: Mit der Navigationskomponente können Benutzer leicht auf eine globale Site-Struktur navigieren.
uuid: 616 c 03 fb -39 b 3-402 a-b 990-f 56 c 87 bc 6 df 4
content-type: Referenz
topic-tags: authoring
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-new
discoiquuid: da 8 d 67 d 7-b 65 e -4041-bc 0 e-e 998 f 24 a 68 f 9
disttype: dist5
gnavtheme: light
groupsectionnavitems: keine
hidemerchandisingbar: inherit
hidepromocomponent: inherit
modalsize: 426x240
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: c58826c133eb112b305fa4facbe2a81e577eb896

---


# Navigation Component{#navigation-component}

Mit der Navigationskomponente können Benutzer leicht auf eine globale Site-Struktur navigieren.

## Nutzung {#usage}

Die Navigationskomponente ermöglicht eine Navigationshierarchie, die aus den Live-Kopien eines Blueprints, aus den Sprachkopien einer Sprachmaster oder aus einer einfachen Seitenstruktur erstellt werden kann. Dadurch können Benutzer der Seite leicht auf eine Site-Struktur navigieren.

The [edit dialog](#edit-dialog) allows the content author to define the navigation root page along with the depth of navigation. The [design dialog](#design-dialog) allows the template author to define default values for the navigation root and depth.

## Version and Compatibility {#version-and-compatibility}

Die aktuelle Version der Navigationskomponente ist v 1, die mit Version 2.0.0 der Kernkomponenten im Januar 2018 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v1 | Kompatibel | Kompatibel | Kompatibel |


For more information about Core Component versions and releases, see the document [Core Components Versions](versions.md).

## Sample Component Output {#sample-component-output}

To experience the Navigation Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](http://opensource.adobe.com/aem-core-wcm-components/library/navigation.html).

## Technical Details {#technical-details}

The latest technical documentation about the Navigation Component [can be found on GitHub](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/navigation/v1/navigation).

Further details about developing Core Components can be found in the [Core Components developer documentation](developing.md.

>[!NOTE]
>
>As of Core Components release 2.1.0, the Navigation Component supports [schema.org microdata](https://schema.org).

## Edit Dialog {#edit-dialog}

Im Dialogfeld &quot;Bearbeiten&quot; kann der Inhaltsautor die Stammseite für die Navigation und die Tiefe der Navigationsstruktur definieren.

![](assets/screen_shot_2018-04-03at112055.png)

* **Navigation Root**
The Root Page, der zum Generieren der Navigationsstruktur verwendet wird.
* **Ausschluss-Stammordner**
Ausschließen des Navigationsstammordners in der resultierenden Struktur, schließen Sie nur untergeordnete Elemente ein.
* **Sammlung aller untergeordneten Seiten**
sammeln Alle Seiten, die sich auf dem Navigationsstamm befinden.
* **Navigationsstrukturtiefe**
Definiert, wie viele Ebenen die Komponente in der Navigationsstruktur relativ zum Navigationsstamm anzeigen soll (nur verfügbar, wenn **alle untergeordneten Seiten** nicht ausgewählt sind).

## Design Dialog {#design-dialog}

Das Entwurfsdialogfeld ermöglicht es dem Vorlagenautor, die Standardwerte für die Navigationsstammseite und die Navigationstiefe festzulegen, die den Autoren angezeigt werden.

### Properties Tab {#properties-tab}

![](assets/screen_shot_2018-04-03at112357.png)

* **Navigation Root**
Der Standardwert der Stammseite der Navigationsstruktur, die zum Generieren der Navigationsstruktur verwendet und standardmäßig verwendet wird, wenn der Inhaltsautor die Komponente der Seite hinzufügt.
* **Exclude Navigation Root**
Der Standardwert der Option, um den Navigationsstamm in der resultierenden Struktur auszuschließen.
* **Alle untergeordneten Seiten**
erfassen Der Standardwert der Option zur Sammlung aller Seiten, die sich auf dem Navigationsstamm befinden.
* **Navigationsstruktur Der**
Standardwert der Navigationsstruktur der Navigationsstruktur.

### Styles Tab {#styles-tab}

The Navigation Component supports the AEM [Style System](authoring.md#component-styling).