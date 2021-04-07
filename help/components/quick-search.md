---
title: Schnellsuch-Komponente
description: Die Schnellsuch-Komponente bietet Suchfunktionen für eine Website und zeigt Suchergebnisse an, damit Besucher die Site durchsuchen und die Ergebnisse filtern können.
role: Architekt, Entwickler, Administrator, Geschäftspraktiker
translation-type: ht
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: ht
source-wordcount: '597'
ht-degree: 100%

---


# Schnellsuch-Komponente {#quick-search-component}

Die Schnellsuch-Komponente bietet Suchfunktionen für eine Website und zeigt Suchergebnisse an, damit Besucher mühelos übereinstimmende Inhalte finden und Ergebnisse anzeigen können.

## Verwendung {#usage}

Die Schnellsuch-Komponente bietet Site-Besuchern die Möglichkeit, nach Inhalten zu suchen, die Ergebnisse unmittelbar anzuzeigen und leicht zu den passenden Seiten zu navigieren. Neue Ergebnisse werden dynamisch abgerufen, wenn der Benutzer die Suchergebnisse durchblättert.

Im [Dialogfeld „Bearbeiten“](#edit-dialog) kann der Verfasser des Inhalts festlegen, wo die Suche in der Inhaltsstruktur beginnen soll. Im [Dialogfeld „Design“](#design-dialog) kann der Vorlagenautor den Standardwert festlegen, an dem die Suche in der Inhaltsstruktur beginnen soll, sowie eine maximale Ergebnissatzgröße und minimale Suchbegriffslänge festlegen.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Schnellsuch-Komponente ist v1, die mit Version 2.0.0 der Kernkomponenten im Januar 2018 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v1 | Kompatibel | Kompatibel | Kompatibel |

Weitere Informationen zu Kernkomponentenversionen und -freigaben finden Sie in den [Kernkomponentenversionen](/help/versions.md).

### Technische Details {#technical-details}

>[!NOTE]
>
>Der Schutz der Suchkomponente oder einer beliebigen AEM-basierten Anwendung gegen DOS-Angriffe sollte auf höherer Ebene implementiert werden, z. B. durch Verwendung von `mod_security` auf dem Dispatcher.

Die neueste technische Dokumentation zur Schnellsuch-Komponente [finden Sie auf GitHub](https://adobe.com/go/aem_cmp_tech_search_v1_de).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Dialogfeld „Bearbeiten“ {#edit-dialog}

Im Dialogfeld „Bearbeiten“ kann der Verfasser des Inhalts festlegen, wo die Suche in der Inhaltsstruktur beginnen soll.

![Dialogfeld „Bearbeiten“ der Schnellsuch-Komponente](/help/assets/quick-search-edit.png)

**Suchstamm** - Die Stammseite, von der aus die Suche gestartet werden soll. Der Suchstamm kann ein Blueprint-Master, ein Sprachen-Master oder eine normale Seite sein.
* **ID** – Diese Option dient zur Kontrolle der eindeutigen Kennung der Komponente in der HTML-Datei und auf der [Datenschicht](/help/developing/data-layer/overview.md).
   * Wenn Sie das Feld leer lassen, wird automatisch eine eindeutige ID generiert, die Sie über die resultierende Seite finden.
   * Sofern eine ID angegeben wird, ist vom Autor sicherzustellen, dass diese eindeutig ist.
   * Änderungen der ID können sich auf das CSS-, JS- und Datenschicht-Tracking auswirken.

## Dialogfeld „Design“ {#design-dialog}

Im Dialogfeld „Design“ kann der Vorlagenautor den Standardwert festlegen, an dem die Suche in der Inhaltsstruktur beginnen soll, sowie eine maximale Ergebnissatzgröße und minimale Suchbegriffslänge. Das Dialogfeld „Design“ ermöglicht dem Vorlagenautor, die für die Inhaltsautoren verfügbaren Textformatierungsoptionen zu definieren.

### Registerkarte „Eigenschaften“ {#properties-tab}

![Dialogfeld „Design“ der Schnellsuch-Komponente](/help/assets/quick-search-design.png)

* **Suchstamm**
Der Standardwert des Suchstamms, wenn ein Inhaltsautor die Komponente „Schnellsuche“ auf einer Inhaltsseite platziert
* **Ergebnisgröße**
Die maximale Anzahl von Ergebnissen, die durch eine Suchanfrage abgerufen werden
* **Minimale Länge für Suchbegriff**
Mindestlänge des Suchbegriffs, um die Suche zu starten

>[!NOTE]
>
>**Die Größe der Ergebnisse** und die **Minimale Länge für Suchbegriff** können nur im Designmodus festgelegt werden und daher nur auf Vorlagenebene, d. h. Inhaltsautoren können diese Werte nicht ändern.

>[!CAUTION]
>
>**Die Größe der Ergebnisse** und die **Minimale Länge für Suchbegriff** können Auswirkungen auf die Leistung haben, wenn sie zu hoch oder zu niedrig eingestellt sind.

### Registerkarte „Stile“ {#styles-tab}

Die Komponente „Schnellsuche“ unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).
