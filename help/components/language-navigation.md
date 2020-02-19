---
title: Sprachnavigationskomponente
description: Die Sprachnavigationskomponente stellt eine Sprache/Ländernavigation für eine Site bereit, sodass Besucher zur gleichen Seite in einem anderen Gebietsschema navigieren können.
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# Sprachnavigationskomponente{#language-navigation-component}

Die Sprachnavigationskomponente stellt eine Sprache/Ländernavigation für eine Site bereit, sodass Besucher zur gleichen Seite in einem anderen Gebietsschema navigieren können.

## Nutzung {#usage}

Webseiten werden oft in verschiedenen Sprachen für verschiedene Regionen angeboten. Mit der Sprachnavigationskomponente kann ein Besucher dieselbe Seite in verschiedenen Sprachen/Gebietsschemata anzeigen. Wenn Sie ein Leser auf der schweizerischen deutschen Version der Website sind, können Sie einfach zur US-englischen Version der gleichen Seite wechseln. Die Komponente &quot;Sprachnavigation&quot;versteht die Sprachstruktur der Site und findet die entsprechende Seite automatisch.

* Ein Beispiel dafür, wie die Lokalisierungsfunktion der Sprachnavigationskomponente funktioniert, finden Sie [unten](#example).
* Ein Beispiel dafür, wie die Lokalisierungsfunktionen der anderen Kernkomponenten zusammenarbeiten, finden Sie auf der Seite [Kernkomponenten](/help/get-started/localization.md) unter „Lokalisierungsfunktionen“.

Das Dialogfeld [Bearbeiten](#edit-dialog) ermöglicht die Definition des globalen Site-Navigationsstamms sowie die Festlegung, wie tief in die Struktur die Navigation gehen soll. Im Dialogfeld [Design](#design-dialog)kann der Vorlagenautor die Standardwerte für dieselben Optionen festlegen.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Sprachnavigationskomponente ist v1, die mit Version 2.0.0 der Kernkomponenten im Januar 2018 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.3 | AEM 6.4 | AEM 6.5 | AEM als Cloud Service |
|--- |--- |--- |--- |---|
| v1 | Kompatibel | Kompatibel | Kompatibel | Kompatibel |

Weitere Informationen zu Kernkomponentenversionen und -freigaben finden Sie in den [Kernkomponentenversionen](/help/versions.md).

## Musterkomponentenausgabe {#sample-component-output}

To experience the Language Navigation Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_langnav).

## Technische Details {#technical-details}

The latest technical documentation about the Language Navigation Component [can be found on GitHub](https://adobe.com/go/aem_cmp_tech_langnav_v1).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Dialogfeld „Design“ {#design-dialog}

Das Dialogfeld „Bearbeiten“ ermöglicht die Definition des globalen Site-Navigationsstamms sowie die Festlegung, wie tief in die Struktur die Navigation gehen soll.

Normalerweise müssen diese Konfigurationen nur auf der Ebene der Seitenvorlage durchgeführt werden. Sie können jedoch auch über das [Dialogfeld „Bearbeiten“](#edit-dialog) auf der Seitenebene geändert werden.

### Registerkarte „Eigenschaften“{#properties-tab}

![](/help/assets/screen_shot_2018-01-12at133642.png)

* **Navigationsstamm**
   * Hier sollte die Sprachnavigation der Site beginnen.
   * Die Sprachstruktur der Site beginnt auf der nächsten Ebene unter diesem Stamm.
* **Sprachstrukturtiefe**
   * So stellen die zahlreichen Ebenen der Inhaltsstruktur unter dem **Navigationsstamm** die Sprachstruktur der Site dar. Beispiele:
      * `1` bedeutet normalerweise, dass Sie nur die Sprache auswählen können.
      * `2` bedeutet in der Regel, dass Sie eine Auswahl an Sprache und Land haben.
      * `3` bedeutet in der Regel, dass Sie eine Auswahl an Sprache, Land und Region haben.

#### Beispiel {#example}

Nehmen wir an, dass Ihr Inhalt wie folgt aussieht:

```
/content
+-- we-retail
   +-- language-masters
   +-- us
      +-- en
      \-- es
   \-- ch
      +-- de
      +-- fr
      \-- it
+-- wknd-events
\-- wknd-shop
```

Für die Site „We.Retail“ möchten Sie wahrscheinlich die Sprachnavigationskomponente auf einer Seitenvorlage als Teil der Kopfzeile platzieren. Sobald die Komponente ein Teil der Vorlage ist, können Sie den **Navigationsstamm** der Komponente auf `/content/we-retail` festlegen, da dort der lokalisierte Inhalt für diese Site beginnt. You would also want to set the **Language Structure Depth** to be `2` since your structure is of two levels (country then language).

Mit dem **Navigationsstamm**-Wert weiß die Sprachkomponente, dass nach `/content/we-retail` die Navigation beginnt und dass sie Sprachnavigationsoptionen generieren kann, indem die nächsten beiden Ebenen in der Inhaltsstruktur als Sprachnavigationsstruktur der Site erkannt werden (wie durch den Wert **der Sprachstruktur** definiert).

Unabhängig davon, welche Seite ein Benutzer ansieht, kann die Sprachnavigationskomponente die entsprechende Seite in einer anderen Sprache finden, indem sie den Speicherort der aktuellen Seite kennt, den Stamm rückwärts entlang arbeitet und dann auf die entsprechende Seite weiterleitet.

### Registerkarte „Stile“ {#styles-tab}

Die Sprachnavigationskomponente unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).

## Dialogfeld „Bearbeiten“ {#edit-dialog}

In der Regel muss die Komponente Sprachnavigation nur zu den Seitenvorlagen einer Site hinzugefügt und konfiguriert werden. Wenn die Sprachnavigationskomponente zu einer einzelnen Inhaltsseite hinzugefügt werden muss, erlaubt das Dialogfeld „Bearbeiten“ dem Inhaltsautor die Konfiguration derselben Werte wie im [Design-Dialogfeld](#design-dialog) beschrieben.

![](/help/assets/screen_shot_2018-01-12at133353.png)
