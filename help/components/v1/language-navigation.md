---
title: Sprachnavigationskomponente (v1)
description: Die Sprachnavigationskomponente stellt eine Sprache/Ländernavigation für eine Site bereit, sodass Besuchende zur gleichen Seite in einem anderen Gebietsschema navigieren können.
role: Architect, Developer, Admin, User
exl-id: 41194ba0-6833-40e5-88d9-036e9c231edd
index: n
source-git-commit: 92a3ec273a5be6751c1503835b9c2e5cbd61bb9e
workflow-type: ht
source-wordcount: '800'
ht-degree: 100%

---


# Sprachnavigationskomponente (v1) {#language-navigation-component}

Die Sprachnavigationskomponente stellt eine Sprache/Ländernavigation für eine Site bereit, sodass Besucher zur gleichen Seite in einem anderen Gebietsschema navigieren können.

## Nutzung {#usage}

Webseiten werden oft in verschiedenen Sprachen für verschiedene Regionen angeboten. Mit der Sprachnavigationskomponente kann ein Besucher dieselbe Seite in verschiedenen Sprachen/Gebietsschemata anzeigen. Wenn Sie ein Leser auf der schweizerischen deutschen Version der Website sind, können Sie einfach zur US-englischen Version der gleichen Seite wechseln. Die Sprachnavigationskomponente verarbeitet die Struktur der Site-Sprache und findet die zugehörige Seite automatisch.

* Ein Beispiel dafür, wie die Lokalisierungsfunktion der Sprachnavigationskomponente funktioniert, finden Sie [unten](#example).
* Ein Beispiel dafür, wie die Lokalisierungsfunktionen der anderen Kernkomponenten zusammenarbeiten, finden Sie auf der Seite [Kernkomponenten](/help/get-started/localization.md) unter „Lokalisierungsfunktionen“.

Das Dialogfeld [Bearbeiten](#edit-dialog) ermöglicht die Definition des globalen Site-Navigationsstamms sowie die Festlegung, wie tief in die Struktur die Navigation gehen soll. Im Dialogfeld [Design](#design-dialog) kann der Vorlagenautor die Standardwerte für dieselben Optionen festlegen.

## Version und Kompatibilität {#version-and-compatibility}

In diesem Dokument wird die v1 der Sprachnavigationskomponente beschrieben, die mit Version 2.0.0 der Kernkomponenten im Januar 2018 eingeführt wurde.

>[!CAUTION]
>
>In diesem Dokument wird die v1 der Sprachnavigationskomponente beschrieben.
>
>Weitere Informationen zur aktuellen Version der Sprachnavigationskomponente finden Sie im Dokument [Sprachnavigationskomponente](/help/components/language-navigation.md).

## Musterkomponentenausgabe {#sample-component-output}

Um die Sprachnavigationskomponente und Beispiele für die Konfigurationsoptionen sowie HTML- und JSON-Ausgaben zu erhalten, besuchen Sie die [Komponentenbibliothek](https://adobe.com/go/aem_cmp_library_langnav_de).

## Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur Sprachnavigationskomponente [finden Sie auf GitHub](https://adobe.com/go/aem_cmp_tech_langnav_v1_de).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Dialogfeld „Design“ {#design-dialog}

Das Dialogfeld „Bearbeiten“ ermöglicht die Definition des globalen Site-Navigationsstamms sowie die Festlegung, wie tief in die Struktur die Navigation gehen soll.

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

Normalerweise muss die Sprachnavigationskomponente nur zu den Seitenvorlagen einer Site hinzugefügt und konfiguriert werden. Wenn die Sprachnavigationskomponente zu einer einzelnen Inhaltsseite hinzugefügt werden muss, erlaubt das Dialogfeld „Bearbeiten“ dem Inhaltsautor die Konfiguration derselben Werte wie im [Design-Dialogfeld](#design-dialog) beschrieben.

Zusätzlich können Sie eine **ID** festlegen. Diese Option dient zur Kontrolle der eindeutigen Kennung der Komponente in der HTML-Datei und auf der [Datenschicht](/help/developing/data-layer/overview.md).

* Wenn Sie das Feld leer lassen, wird automatisch eine eindeutige ID generiert, die Sie über die resultierende Seite finden.
* Sofern eine ID angegeben wird, ist vom Autor bzw. der Autorin sicherzustellen, dass diese eindeutig ist.
* Änderungen der ID können sich auf das CSS-, JS- und Datenschicht-Tracking auswirken.

![Dialogfeld „Bearbeiten“ der Sprachnavigationskomponente](/help/assets/language-navigation-edit.png)

## Adobe Client-Datenschicht {#data-layer}

Die Sprachnavigationskomponente unterstützt die [Adobe Client-Datenschicht](/help/developing/data-layer/overview.md).
