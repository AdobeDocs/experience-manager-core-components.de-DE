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
translation-type: tm+mt
source-git-commit: 8a34ecc432e489b8dc025aeda29d8eba9c788861

---


# Sprachnavigationskomponente{#language-navigation-component}

Die Sprachnavigationskomponente stellt eine Sprache/Ländernavigation für eine Site bereit, sodass Besucher zur gleichen Seite in einem anderen Gebietsschema navigieren können.

## Nutzung {#usage}

Websites werden häufig für verschiedene Regionen in mehreren Sprachen bereitgestellt. Mit der Sprachnavigationskomponente kann ein Besucher dieselbe Seite in verschiedenen Sprachen/Gebietsschemata anzeigen. Wenn Sie ein Leser auf der schweizerischen deutschen Version der Website sind, können Sie einfach zur US-englischen Version der gleichen Seite wechseln. Die Komponente "Sprachnavigation" verarbeitet die Sprache der Site-Sprache und findet die zugehörige Seite automatisch.

Das Dialogfeld [Bearbeiten](#edit-dialog) ermöglicht die Definition des globalen Site-Navigationsstamms sowie die Festlegung, wie tief in die Struktur die Navigation gehen soll. Im Dialogfeld [Design](#design-dialog)kann der Vorlagenautor die Standardwerte für dieselben Optionen festlegen.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Sprachnavigationskomponente ist v1, die mit Version 2.0.0 der Kernkomponenten im Januar 2018 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v1 | Kompatibel | Kompatibel | Kompatibel |

Weitere Informationen zu Kernkomponentenversionen und -freigaben finden Sie in den [Kernkomponentenversionen](versions.md).

## Musterkomponentenausgabe {#sample-component-output}

To experience the Language Navigation Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](http://opensource.adobe.com/aem-core-wcm-components/library/language-navigation/language-structure/us/en/language-navigation.html).

## Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur Sprachnavigationskomponente [finden Sie unter github](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/languagenavigation/v1/languagenavigation).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](developing.md).

## Dialogfeld „Design“ {#design-dialog}

Das Dialogfeld „Bearbeiten“ ermöglicht die Definition des globalen Site-Navigationsstamms sowie die Festlegung, wie tief in die Struktur die Navigation gehen soll.

In der Regel müssen diese Konfigurationen nur auf der Seitenvorlage vorgenommen werden. Sie können jedoch über das [Dialogfeld "Bearbeiten](#edit-dialog)«auf der Seitenebene geändert werden.

### Registerkarte „Eigenschaften“{#properties-tab}

![](assets/screen_shot_2018-01-12at133642.png)

* **Navigationsstamm**
   * Hier sollte die langsame Navigation der Site beginnen.
   * Die Sprachstruktur der Site beginnt auf der nächsten Ebene unter diesem Stamm.
* **Sprachstrukturtiefe**
   * So stellen die zahlreichen Ebenen der Inhaltsstruktur unter dem **Navigationsstamm** die Sprachstruktur der Site dar. Beispiele:
      * `1` normalerweise bedeutet, dass Sie nur die Sprache auswählen können.
      * `2` bedeutet, dass Sie eine Sprache und ein Land auswählen.
      * `3` in der Regel bedeutet, dass Sie eine Auswahl von "lang" ," country" und "region" haben.

#### Beispiel {#example}

Nehmen wir an, dass Ihr Inhalt wie folgt aussieht:

```
/content
+-- we-retail
   +-- language-masters
   +-- us
      +-- en
      \-- es
   +-- ch
      +-- de
      +-- fr
      +-- it
+-- wknd-events
\-- wknd-shop
```

Für die Site "We. Retail" möchten Sie wahrscheinlich die Komponente" Sprachnavigation" auf einer Seitenvorlage als Teil der Kopfzeile platzieren. Sobald ein Teil der Vorlage ein Teil der Vorlage ist, können Sie den **Navigationsstamm** der Komponente auf `/content/we-retail` da festlegen, wo der lokalisierte Inhalt für diese Site beginnt. Sie möchten auch die **Sprachstrukturtiefe** festlegen, damit `2` die Struktur von zwei Ebenen liegt (Land dann laguage).

Mit dem **Navigationsstamm** -Wert weiß die Sprachkomponente, dass die `/content/we-retail` Navigation beginnt und dass sie Sprachnavigationsoptionen generieren kann, indem die nächsten beiden Ebenen in der Inhaltsstruktur als Sprachnavigationsstruktur der Site erkannt werden (wie durch den Wert **der Sprachstruktur** definiert).

Unabhängig davon, welche Seite ein Benutzer ansieht, kann die Komponente "Sprachnavigation" die entsprechende Seite in einer anderen Sprache finden, indem sie den Speicherort der aktuellen Seite kennen und rückwärts an den Stamm weiterarbeiten und dann auf die entsprechende Seite weiterleitet.

### Registerkarte „Stile“ {#styles-tab}

Die Sprachnavigationskomponente unterstützt das AEM-[Stilsystem](authoring.md#component-styling).

## Dialogfeld „Bearbeiten“ {#edit-dialog}

Normalerweise muss die Komponente "Wenig" nur zu den Seitenvorlagen einer Site hinzugefügt und konfiguriert werden. Wenn die Komponente "Sprachnavigation" zu einer einzelnen Inhaltsseite hinzugefügt werden muss, erlaubt das Dialogfeld" Bearbeiten" dem Inhaltsautor die Konfiguration derselben Werte wie im [Design-Dialogfeld](#design-dialog)beschrieben.

![](assets/screen_shot_2018-01-12at133353.png)
