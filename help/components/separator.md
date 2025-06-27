---
title: Trennzeichenkomponente
description: Die Trennzeichen-Komponente erstellt einen Umbruch zwischen Komponenten auf einer Seite
role: Architect, Developer, Admin, User
exl-id: 79f19368-67fa-4864-93f7-2aa801d13fdb
source-git-commit: dd30def59a8f037864da875ef4c831b11f766e57
workflow-type: ht
source-wordcount: '0'
ht-degree: 100%

---


# Trennzeichenkomponente {#separator-component}

Die Kernkomponente „Trennzeichenkomponente“ zeigt eine horizontale Linie zum Trennen von Inhalten an.

{{traditional-aem}}

## Nutzung {#usage}

Mit der Trennzeichenkomponente kann der Inhaltsautor einfach eine horizontale Linie als Trennlinie zwischen Inhalten erstellen, um Informationen auf einer Seite besser zu organisieren.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Trennzeichenkomponente ist v1, die mit Version 2.3.0 der Kernkomponenten im Februar 2019 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|---|---|---|---|---|
| v1 | Kompatibel mit<br>[Version 2.17.4](/help/versions.md) und vorherigen | Kompatibel | Kompatibel | Kompatibel |

## Musterkomponentenausgabe {#sample-component-output}

Um die Trennzeichenkomponente sowie Beispiele für die Konfigurationsoptionen sowie HTML- und JSON-Ausgaben zu erhalten, besuchen Sie die [Komponentenbibliothek](https://adobe.com/go/aem_cmp_library_separator_de).

### Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur Trennzeichenkomponente [finden Sie auf GitHub](https://adobe.com/go/aem_cmp_tech_separator_v1_de).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

![Dialogfeld „Bearbeiten“ der Trennzeichenkomponente](/help/assets/separator-edit.png)

* **ID** – Diese Option dient zur Kontrolle der eindeutigen Kennung der Komponente in der HTML-Datei und auf der [Datenschicht](/help/developing/data-layer/overview.md).
   * Wenn Sie das Feld leer lassen, wird automatisch eine eindeutige ID generiert, die Sie über die resultierende Seite finden.
   * Sofern eine ID angegeben wird, ist vom Autor bzw. der Autorin sicherzustellen, dass diese eindeutig ist.
   * Änderungen der ID können sich auf das CSS-, JS- und Datenschicht-Tracking auswirken.

## Dialogfeld „Design“ {#design-dialog}

Das Dialogfeld „Design“ ermöglicht es dem Vorlagenautor, die Stile zu definieren, die auf die Trennzeichenkomponente angewendet werden.

### Registerkarte „Arten“ {#styles-tab}

Die Trennzeichenkomponente unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).
