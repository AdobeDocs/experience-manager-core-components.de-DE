---
title: Sprachnavigationskomponente
description: Die Sprachnavigationskomponente stellt eine Sprache/Ländernavigation für eine Site bereit, sodass Besucher zur gleichen Seite in einem anderen Gebietsschema navigieren können.
role: Architect, Developer, Admin, User
exl-id: 10b218b4-c439-4a0f-a46f-0b15d78b0360
source-git-commit: 327c239b02e0aecee878784c918bfa98d960530e
workflow-type: ht
source-wordcount: '957'
ht-degree: 100%

---

# Sprachnavigationskomponente {#language-navigation-component}

Die Sprachnavigationskomponente stellt eine Sprache/Ländernavigation für eine Site bereit, sodass Besucher zur gleichen Seite in einem anderen Gebietsschema navigieren können.

## Nutzung {#usage}

Webseiten werden oft in verschiedenen Sprachen für verschiedene Regionen angeboten. Mit der Sprachnavigationskomponente kann ein Besucher dieselbe Seite in verschiedenen Sprachen/Gebietsschemata anzeigen. Wenn Sie ein Leser auf der schweizerischen deutschen Version der Website sind, können Sie einfach zur US-englischen Version der gleichen Seite wechseln. Die Sprachnavigationskomponente verarbeitet die Struktur der Site-Sprache und findet die zugehörige Seite automatisch.

* Ein Beispiel dafür, wie die Lokalisierungsfunktion der Sprachnavigationskomponente funktioniert, finden Sie [unten](#example).
* Ein Beispiel dafür, wie die Lokalisierungsfunktionen der anderen Kernkomponenten zusammenarbeiten, finden Sie auf der Seite [Kernkomponenten](/help/get-started/localization.md) unter „Lokalisierungsfunktionen“.

Das Dialogfeld [Bearbeiten](#edit-dialog) ermöglicht die Definition des globalen Site-Navigationsstamms sowie die Festlegung, wie tief in die Struktur die Navigation gehen soll. Im Dialogfeld [Design](#design-dialog) kann der Vorlagenautor die Standardwerte für dieselben Optionen festlegen.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Sprachnavigationskomponente ist v2, die mit Version 2.18.0 der Kernkomponenten im Februar 2022 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v2 | - | Kompatibel | Kompatibel |
| [v1](v1/language-navigation.md) | Kompatibel | Kompatibel | Kompatibel |

Weitere Informationen zu Kernkomponentenversionen und -freigaben finden Sie im Dokument [Kernkomponentenversionen](/help/versions.md).

## Musterkomponentenausgabe {#sample-component-output}

Um die Sprachnavigationskomponente und Beispiele für die Konfigurationsoptionen sowie HTML- und JSON-Ausgaben zu erhalten, besuchen Sie die [Komponentenbibliothek](https://adobe.com/go/aem_cmp_library_langnav_de).

## Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur Sprachnavigationskomponente [finden Sie auf GitHub](https://adobe.com/go/aem_cmp_tech_langnav_v2_de).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Dialogfeld „Design“ {#design-dialog}

Das Dialogfeld „Bearbeiten“ ermöglicht die Definition des globalen Site-Navigationsstamms sowie die Festlegung, wie tief die Navigation in die Struktur gehen darf.

In der Regel müssen diese Konfigurationen nur auf der Seitenvorlage vorgenommen werden. Sie können jedoch auch über das [Dialogfeld „Bearbeiten“](#edit-dialog) auf der Seitenebene geändert werden.

### Registerkarte „Eigenschaften“ {#properties-tab}

![Dialogfeld „Design“ der Sprachnavigationskomponente](/help/assets/language-navigation-design.png)

* **Navigationsstamm**
   * Hier sollte die Sprachnavigation der Site beginnen.
   * Die Sprachstruktur der Site beginnt auf der nächsten Ebene unter diesem Stamm.
* **Sprachstrukturtiefe**
   * So stellen die zahlreichen Ebenen der Inhaltsstruktur unter dem **Navigationsstamm** die Sprachstruktur der Site dar. Beispiele:
      * `1` bedeutet normalerweise, dass Sie nur die Sprache auswählen können.
      * `2` bedeutet normalerweise, dass Sie eine Sprache und ein Land auswählen können.
      * `3` bedeutet normalerweise, dass Sie Sprache, Land und Region auswählen können.

#### Beispiel {#example}

Nehmen wir an, dass Ihr Inhalt wie folgt aussieht:

```
/content
+-- wknd
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

Für die Site „WKND“ möchten Sie auf einer Seitenvorlage womöglich die Sprachnavigationskomponente als Teil der Kopfzeile platzieren. Sobald die Komponente ein Teil der Vorlage ist, können Sie den **Navigationsstamm** der Komponente auf `/content/wknd` festlegen, da dort der lokalisierte Inhalt für diese Site beginnt. Sie sollten auch die **Sprachstrukturtiefe** auf `2` festlegen, da Ihre Struktur aus zwei Ebenen besteht (erst Land, dann Sprache).

Mit dem **Navigationsstamm**-Wert weiß die Sprachkomponente, dass nach `/content/wknd` die Navigation beginnt und dass sie Sprachnavigationsoptionen generieren kann, indem die nächsten beiden Ebenen in der Inhaltsstruktur als Sprachnavigationsstruktur der Site erkannt werden (wie durch den Wert **der Sprachstruktur** definiert).

Unabhängig davon, welche Seite ein Benutzer ansieht, kann die Sprachnavigationskomponente die entsprechende Seite in einer anderen Sprache finden, indem sie den Speicherort der aktuellen Seite kennt, den Stamm rückwärts entlang arbeitet und dann auf die entsprechende Seite weiterleitet.

### Registerkarte „Arten“ {#styles-tab}

Die Sprachnavigationskomponente unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).

## Dialogfeld „Bearbeiten“ {#edit-dialog}

### Registerkarte „Eigenschaften“ {#properties-tab-edit}

Normalerweise muss die Sprachnavigationskomponente nur zu den Seitenvorlagen einer Site hinzugefügt und konfiguriert werden. Wenn die Sprachnavigationskomponente zu einer einzelnen Inhaltsseite hinzugefügt werden muss, erlaubt das Dialogfeld „Bearbeiten“ dem Inhaltsautor die Konfiguration derselben Werte wie im [Design-Dialogfeld](#design-dialog) beschrieben

Zusätzlich können Sie eine **ID** festlegen. Diese Option dient zur Kontrolle der eindeutigen Kennung der Komponente in der HTML-Datei und auf der [Datenschicht](/help/developing/data-layer/overview.md).

* Wenn Sie das Feld leer lassen, wird automatisch eine eindeutige ID generiert, die Sie über die resultierende Seite finden.
* Sofern eine ID angegeben wird, ist vom Autor sicherzustellen, dass diese eindeutig ist.
* Änderungen der ID können sich auf das CSS-, JS- und Datenschicht-Tracking auswirken.

![Dialogfeld „Bearbeiten“ der Sprachnavigationskomponente](/help/assets/language-navigation-edit.png)

### Registerkarte „Erreichbarkeit“ {#accessibility-tab}

* **Kennzeichnung** – Diese Option sollte definiert werden, wenn sich auf der Seite mehr als eine Sprachnavigation befindet, um das Attribut „aria label“ der Komponente festzulegen.

![Registerkarte „Barrierefreiheit der Sprachnavigation“](/help/assets/language-navigation-edit-accessibility.png)

### Registerkarte „Arten“ {#styles-tab-edit}

Die Sprachnavigationskomponente unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).

Verwenden Sie das Dropdown-Menü, um die Stile auszuwählen, die Sie auf die Komponente anwenden möchten. Die im Dialogfeld „Bearbeiten“ vorgenommenen Auswahlen haben denselben Effekt wie die in der Komponenten-Symbolleiste ausgewählten.

Stile müssen für diese Komponente im [Dialogfeld „Design“](#design-dialog) konfiguriert werden, damit das Dropdown-Menü verfügbar ist.

![Registerkarte „Arten“ im Dialogfeld „Bearbeiten“ der Sprachnavigationskomponente](/help/assets/language-navigation-edit-styles.png)

## Adobe Client-Datenschicht {#data-layer}

Die Sprachnavigationskomponente unterstützt die [Adobe Client-Datenschicht](/help/developing/data-layer/overview.md).
