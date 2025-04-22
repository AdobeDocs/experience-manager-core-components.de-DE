---
title: Komponente für ausgeblendetes Formular
description: Die Kernkomponente „Komponente für ausgeblendetes Formular“ ermöglicht die Anzeige eines ausgeblendeten Felds.
role: Architect, Developer, Admin, User
exl-id: 0364cd3b-3c09-46db-9392-a67e3f9ea7a5
source-git-commit: 6fbc781db555bc6abaed1d122a9a8756e3d53222
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 99%

---

# Komponente für ausgeblendetes Formular {#form-hidden-component}

Die Kernkomponente „Komponente für ausgeblendetes Formular“ ermöglicht die Anzeige eines ausgeblendeten Felds.

## Nutzung {#usage}

Die Kernkomponente „Komponente für ausgeblendetes Formular“ ermöglicht die Erstellung ausgeblendeter Felder, um Informationen über die aktuelle Seite zurück an AEM zu senden. Sie soll zusammen mit der [Formular-Container-Komponente](form-container.md) verwendet werden.

Die Feldeigenschaften können vom Inhaltseditor im [Dialogfeld „Konfigurieren“](form-hidden.md) definiert werden.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Komponente für ausgeblendetes Formular ist v2, die mit Version 2.0.0 der Kernkomponenten im Januar 2018 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |--- |---|---|
| v2 | Kompatibel mit<br>[Version 2.17.4](/help/versions.md) und vorherigen | Kompatibel | Kompatibel | Kompatibel |
| [v1](/help/components/v1/form-hidden-v1.md) | Kompatibel | Kompatibel | - | Kompatibel |

Weitere Informationen zu Kernkomponentenversionen und -freigaben finden Sie im Dokument [Kernkomponentenversionen](/help/versions.md).

## Musterkomponentenausgabe {#sample-component-output}

Um die Komponente für ein ausgeblendetes Formular kennenzulernen und Beispiele für die Konfigurationsoptionen sowie HTML- und JSON-Ausgaben anzuzeigen, besuchen Sie die [Komponentenbibliothek](https://adobe.com/go/aem_cmp_library_form_hidden_de).

### Technische Details {#technical-details}

Die neueste technische Dokumentation zur Komponente für ausgeblendetes Formular [finden Sie auf GitHub](https://adobe.com/go/aem_cmp_tech_form_hidden_v2_de).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Über das Dialogfeld „Konfigurieren“ kann der Inhaltsautor die Parameter des ausgeblendeten Felds definieren.

![„Ausgeblendetes Formular“ im Dialogfeld „Bearbeiten“](/help/assets/form-hidden-edit.png)

* **Name** - Der Name des mit den Formulardaten gesendeten Felds
* **Wert** - Der Wert des mit den Formulardaten gesendeten Felds
* **ID** – Diese Option dient zur Kontrolle der eindeutigen Kennung der Komponente in der HTML-Datei und auf der [Datenschicht](/help/developing/data-layer/overview.md).
   * Wenn Sie das Feld leer lassen, wird automatisch eine eindeutige ID generiert, die Sie über die resultierende Seite finden.
   * Sofern eine ID angegeben wird, ist vom Autor bzw. der Autorin sicherzustellen, dass diese eindeutig ist.
   * Änderungen der ID können sich auf das CSS-, JS- und Datenschicht-Tracking auswirken.

Da die Komponente für ausgeblendetes Formular normalerweise keine sichtbaren Attribute aufweist, zeigt der Platzhalter der Komponente im Editor die Feldwerte **Name** und **Wert** an, wenn sie zugewiesen werden, um dem Autor zu helfen, die passende Komponente für ausgeblendetes Formular zu identifizieren.

![Beispiel einer Komponente für ein ausgeblendetes Formular](/help/assets/form-hidden-example.png)

## Dialogfeld „Design“ {#design-dialog}

### Registerkarte „Arten“ {#styles-tab}

Die Komponente für ausgeblendetes Formular unterstützt das [Stilsystem](/help/get-started/authoring.md#component-styling) von AEM.
