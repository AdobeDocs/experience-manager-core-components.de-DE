---
title: Sprachnavigationskomponente
seo-title: Sprachnavigationskomponente
description: 'null'
seo-description: Die Sprachnavigationskomponente stellt eine Sprache/Ländernavigation für eine Site bereit, sodass Besucher zur gleichen Seite in einem anderen Gebietsschema navigieren können.
uuid: ce736458-9cdf-4bc2-b90f-9c5a62fe1ca0
content-type: Referenz
topic-tags: Authoring
products: SG_EXPERIENCEMANAGER/CORECOMPONENTS-new
discoiquuid: 8f232eb0-65d5-4075-8668-75f1366882c8
disttype: dist5
gnavtheme: light
groupsectionnavitems: keine
hidemerchandisingbar: inherit
hidepromocomponent: inherit
modalsize: 426x240
index: y
internal: n
snippet: y
translation-type: ht
source-git-commit: eef608fb06001485aa2c2c0b574af412ed7f15a4

---


# Sprachnavigationskomponente{#language-navigation-component}

Die Sprachnavigationskomponente stellt eine Sprache/Ländernavigation für eine Site bereit, sodass Besucher zur gleichen Seite in einem anderen Gebietsschema navigieren können.

## Nutzung {#usage}

Oft werden Websites für verschiedene Regionen in mehreren Sprachen bereitgestellt. Mit der Sprachnavigationskomponente kann ein Besucher dieselbe Seite in verschiedenen Sprachen/Gebietsschemata anzeigen.

Das Dialogfeld [Bearbeiten](#edit-dialog) ermöglicht die Definition des globalen Site-Navigationsstamms sowie die Festlegung, wie tief in die Struktur die Navigation gehen soll. Im Dialogfeld [Design](#design-dialog)kann der Vorlagenautor die Standardwerte für dieselben Optionen festlegen.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Sprachnavigationskomponente ist v1, die mit Version 2.0.0 der Kernkomponenten im Januar 2018 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v1 | Kompatibel | Kompatibel | Kompatibel |


Weitere Informationen zu Kernkomponentenversionen und -freigaben finden Sie in den [Kernkomponentenversionen](versions.md).

## Musterkomponentenausgabe {#sample-component-output}

Um die Sprachnavigations-Komponente sowie Beispiele für die Konfigurationsoptionen sowie HTML- und JSON-Ausgaben zu erhalten, besuchen Sie die [Komponentenbibliothek](http://opensource.adobe.com/aem-core-wcm-components/library/language-navigation/language-structure/us/en/language-navigation.html).

## Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur Sprachnavigationskomponente [finden Sie auf GitHub](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/languagenavigation/v1/languagenavigation).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](developing.md).

## Dialogfeld „Bearbeiten“ {#edit-dialog}

Das Dialogfeld „Bearbeiten“ ermöglicht die Definition des globalen Site-Navigationsstamms sowie die Festlegung, wie tief in die Struktur die Navigation gehen soll.

![](assets/screen_shot_2018-01-12at133353.png)

* **Navigationsstamm**
Definiert die Stammseite der Navigationsstruktur.
   * Verwenden Sie die **Schaltfläche „Auswahl öffnen“**, um einfach in der Inhaltsstruktur zu navigieren und den Stamm auszuwählen.
* **Tiefe der Sprachstruktur**
Tiefe der globalen Sprachstruktur in Relation zum Navigationsstamm.

## Dialogfeld „Design“ {#design-dialog}

Über das Dialogfeld „Design“ kann der Vorlagenautor die Standardwerte für dieselben Optionen festlegen, die im Dialogfeld „Bearbeiten“ verfügbar sind.

### Registerkarte „Eigenschaften“{#properties-tab}

![](assets/screen_shot_2018-01-12at133642.png)

* **Navigationsstamm**
Standardwert des Navigationsstamms, wenn ein Inhaltsautor die Sprachumschalter-Komponente auf einer Inhaltsseite platziert
* **Sprachstrukturtiefe**
Standardwert der Tiefe der Sprachstruktur, wenn ein Inhaltsautor die Sprachumschalter-Komponente auf einer Inhaltsseite platziert

### Registerkarte „Stile“ {#styles-tab}

Die Sprachnavigationskomponente unterstützt das AEM-[Stilsystem](authoring.md#component-styling).