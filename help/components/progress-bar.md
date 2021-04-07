---
title: Fortschrittsleistenkomponente
description: Die Fortschrittsleistenkomponente visualisiert den Fortschritt bei der Erreichung eines Ziels.
role: Architekt, Entwickler, Administrator, Geschäftspraktiker
translation-type: ht
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: ht
source-wordcount: '343'
ht-degree: 100%

---


# Fortschrittsleistenkomponente {#progress-bar-component}

Die Kernkomponente „Fortschrittsleistenkomponente“ visualisiert den Fortschritt bei der Erreichung eines Ziels.

## Verwendung {#usage}

Mit der Fortschrittsleistenkomponente können Inhaltsautoren eine Fortschrittsleiste einfach durch Festlegen eines Prozentsatzes für die Fertigstellung erstellen, was eine intuitive visuelle Anzeige des Fortschritts bei der Erreichung eines Ziels ermöglicht.

## Version und Kompatibilität {#version-and-compatibility}

Die in diesem Dokument beschriebene Fortschrittsleistenkomponente liegt aktuell in der Version v1 vor, die im Mai 2020 im Rahmen von Version 2.9.0 der Kernkomponenten vorgestellt wurde.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|---|
| v1 | Kompatibel | Kompatibel | Kompatibel |

## Musterkomponentenausgabe {#sample-component-output}

Näheres zur Fortschrittsleistenkomponente und Beispiele für zugehörige Konfigurationsoptionen sowie HTML- und JSON-Ausgaben finden Sie in der [Komponentenbibliothek](https://adobe.com/go/aem_cmp_library_progressbar_de).

### Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur Fortschrittsleistenkomponente finden Sie auf [GitHub](https://adobe.com/go/aem_cmp_tech_progress_v1).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

![Dialogfeld „Bearbeiten“ der Fortschrittsleistenkomponente](/help/assets/progress-bar-edit.png)

* **Abschluss** - Der Fortschritt in Prozent
* **ID** - Diese Option dient zur Kontrolle der eindeutigen Kennung der Komponente in der HTML-Datei und auf der [Datenschicht](/help/developing/data-layer/overview.md).
   * Wenn Sie das Feld leer lassen, wird automatisch eine eindeutige ID generiert, die Sie über die resultierende Seite finden.
   * Sofern eine ID angegeben wird, ist vom Autor sicherzustellen, dass diese eindeutig ist.
   * Änderungen der ID können sich auf das CSS-, JS- und Datenschicht-Tracking auswirken.

## Dialogfeld „Design“ {#design-dialog}

Über das Dialogfeld „Design“ können Vorlagenautoren die Stile definieren, die auf die Fortschrittsleiste angewendet werden.

### Registerkarte „Stile“ {#styles-tab}

Die Fortschrittsleistenkomponente unterstützt das [Stilsystem](/help/get-started/authoring.md#component-styling) von AEM.

## Adobe Client-Datenschicht {#data-layer}

Die Fortschrittsleistenkomponente unterstützt die [Adobe Client-Datenschicht](/help/developing/data-layer/overview.md).
