---
title: Fortschrittsleistenkomponente
description: Die Komponente "Fortschrittsleiste"stellt visuell den Fortschritt in Richtung eines Ziels dar
translation-type: tm+mt
source-git-commit: cba1d898d7789af7f4045ef9aa052b4da6a6b33a
workflow-type: tm+mt
source-wordcount: '324'
ht-degree: 22%

---


# Fortschrittsleistenkomponente {#progress-bar-component}

Die Komponente &quot;Core Component Progress Bar&quot;stellt visuell den Fortschritt in Richtung eines Ziels dar.

## Nutzung {#usage}

Die Fortschrittsleistenkomponente ermöglicht es dem Inhaltsautor, eine Fortschrittsleiste einfach zu erstellen, indem ein Prozentsatz der Fertigstellung definiert wird, was eine intuitive visuelle Anzeige des Fortschritts in Richtung eines Ziels ermöglicht.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Fortschrittsleistenkomponente ist Version 1, die mit Version 2.9.0 der Kernkomponenten im Mai 2020 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|---|
| v1 | Kompatibel | Kompatibel | Kompatibel |

## Musterkomponentenausgabe {#sample-component-output}

To experience the Progress Bar Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_progressbar).

### Technische Details {#technical-details}

The latest technical documentation about the Progress Bar Component [can be found on GitHub](https://adobe.com/go/aem_cmp_tech_progress_v1).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

![Dialogfeld &quot;Bearbeiten&quot;der Fortschrittsleistenkomponente](/help/assets/progress-bar-edit.png)

* **Abschluss** - Der Fortschritt in Prozent
* **ID** - Diese Option ermöglicht die Steuerung des eindeutigen Bezeichners der Komponente im HTML und in der [Datenschicht](/help/developing/data-layer/overview.md).
   * Wenn Sie das Feld leer lassen, wird automatisch eine eindeutige ID generiert und Sie können die resultierende Seite überprüfen.
   * Wenn eine ID angegeben wird, muss der Autor sicherstellen, dass sie eindeutig ist.
   * Eine Änderung der ID kann sich auf die Verfolgung von CSS, JS und Datenschichten auswirken.

## Dialogfeld „Design“ {#design-dialog}

Im Designdialogfeld kann der Vorlagenautor die Stile definieren, die auf die Fortschrittsleistenkomponente angewendet werden.

### Registerkarte „Stile“ {#styles-tab}

The Progress Bar Component supports the AEM [Style System](/help/get-started/authoring.md#component-styling).
