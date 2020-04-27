---
title: Komponente für ausgeblendetes Formular
description: Die Kernkomponente „Komponente für ausgeblendetes Formular“ ermöglicht die Anzeige eines ausgeblendeten Felds.
translation-type: ht
source-git-commit: 95c0621f5423bfa515fe5e8b693e127ea56b4ae0

---


# Komponente für ausgeblendetes Formular{#form-hidden-component}

Die Kernkomponente „Komponente für ausgeblendetes Formular“ ermöglicht die Anzeige eines ausgeblendeten Felds.

## Nutzung {#usage}

Die Kernkomponente „Komponente für ausgeblendetes Formular“ ermöglicht die Erstellung ausgeblendeter Felder, um Informationen über die aktuelle Seite zurück an AEM zu senden. Sie soll zusammen mit der [Formularcontainer-Komponente](form-container.md) verwendet werden.

Die Feldeigenschaften können vom Inhaltseditor im [Dialogfeld „Konfigurieren“](form-hidden.md) definiert werden.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Komponente für ausgeblendetes Formular ist v2, die mit Version 2.0.0 der Kernkomponenten im Januar 2018 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.3 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |--- |---|
| v2 | Kompatibel | Kompatibel | Kompatibel | Kompatibel |
| [v1](/help/components/v1/form-hidden-v1.md) | Kompatibel | Kompatibel | Kompatibel | - |

Weitere Informationen zu Kernkomponentenversionen und -freigaben finden Sie in den [Kernkomponentenversionen](/help/versions.md).

## Musterkomponentenausgabe {#sample-component-output}

Um die Komponente für ein ausgeblendetes Formular kennenzulernen und Beispiele für die Konfigurationsoptionen sowie HTML- und JSON-Ausgaben anzuzeigen, besuchen Sie die [Komponentenbibliothek](https://adobe.com/go/aem_cmp_library_form_hidden_de).

### Technische Details {#technical-details}

Die neueste technische Dokumentation zur Komponente für ausgeblendetes Formular [finden Sie auf GitHub](https://adobe.com/go/aem_cmp_tech_form_hidden_v2_de).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Über das Dialogfeld „Konfigurieren“ kann der Inhaltsautor die Parameter des ausgeblendeten Felds definieren.

![](/help/assets/chlimage_1-26.png)

* **Name**
Der Name des mit den Formulardaten gesendeten Felds
* **Wert**
Der Wert des mit den Formulardaten gesendeten Felds
* **Kennung**
Die Kennung muss auf der Seite eindeutig sein und kann genutzt werden, um Skripte in dieses Formularfeld einzubinden.

Da die Komponente für ausgeblendetes Formular normalerweise keine sichtbaren Attribute aufweist, zeigt der Platzhalter der Komponente im Editor die Feldwerte **Name** und **Wert** an, wenn sie zugewiesen werden, um dem Autor zu helfen, die passende Komponente für ausgeblendetes Formular zu identifizieren.

![](/help/assets/screenshot_2018-10-19at094927.png)

## Dialogfeld „Design“ {#design-dialog}

Es gibt kein Dialogfeld „Design“ für die Komponente für ausgeblendetes Formular.
