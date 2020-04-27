---
title: Formularoptionen-Komponente
description: Die Kernkomponente „Formularoptionen“ ermöglicht die Auswahl aus vordefinierten Optionen in verschiedenen Formaten.
translation-type: ht
source-git-commit: 95c0621f5423bfa515fe5e8b693e127ea56b4ae0

---


# Formularoptionen-Komponente {#form-options-component}

Die Kernkomponente „Formularoptionen“ ermöglicht die Auswahl aus vordefinierten Optionen in verschiedenen Formaten.

## Nutzung {#usage}

Die Kernkomponente „Formularoptionen-Komponente“ ermöglicht die Übermittlung verschiedener Arten von Optionen, die auf vielerlei Arten präsentiert werden und die zusammen mit der [Formularcontainer-Komponente](form-container.md) verwendet werden sollten.

Die Darstellung der Optionen, Beschriftungen und individuellen Optionen kann vom Inhaltseditor im Dialogfeld [Konfigurieren](#configure-dialog) definiert werden.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Formularoptionen-Komponente ist v2, die mit Version 2.0.0 der Kernkomponenten im Januar 2018 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.3 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |--- |---|
| v2 | Kompatibel | Kompatibel | Kompatibel | Kompatibel |
| [v1](/help/components/v1/form-options-v1.md) | Kompatibel | Kompatibel | Kompatibel | - |

Weitere Informationen zu Kernkomponentenversionen und -freigaben finden Sie in den [Kernkomponentenversionen](/help/versions.md).

## Musterkomponentenausgabe {#sample-component-output}

Um die Formularoptionen-Komponente kennenzulernen und Beispiele für die Konfigurationsoptionen sowie HTML- und JSON-Ausgaben anzuzeigen, besuchen Sie die [Komponentenbibliothek](https://adobe.com/go/aem_cmp_library_form_options_de).

### Technische Details {#technical-details}

Die neueste technische Dokumentation zur Formularoptionen-Komponente [finden Sie auf GitHub](https://adobe.com/go/aem_cmp_tech_form_options_v2_de).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Im Dialogfeld „Konfigurieren“ kann der Inhaltsautor den Typ der Optionen festlegen, die angezeigt werden sollen, Beschriftungen definieren und festlegen, welche Optionen verfügbar sind.

![](/help/assets/screen_shot_2018-01-12at113153.png)

* **Typen** - Wie die Optionen angezeigt werden
   * **Kontrollkästchen**
   * **Optionsfelder**
   * **Dropdown**
   * **Dropdown für mehrere Auswahlen**
* **Titel**
Der Titel, der als Beschriftung für die Optionen angezeigt werden wird
* **Name**
Der Name des Feldes, das mit den Formulardaten übermittelt wurde.
* **Quelle**
Wo die Optionen definiert sind
   * **Lokal**
Definiert innerhalb der Komponente
      * Tippen oder klicken Sie auf die Schaltfläche **Hinzufügen**, um einen Wert hinzuzufügen, und auf **Entfernen**, um einen Wert zu entfernen.
      * **Wert**
Der Wert, der gespeichert wird, wenn diese Option beim Übermitteln des Formulars ausgewählt wird
      * **Text**
Der Beschriftung der im Formular angezeigten Option
      * **Aktiv**
Diese Option wird als ausgewählt markiert, wenn das Formular geladen wird.
      * **Deaktiviert**
Die Option ist nicht auswählbar, wird aber trotzdem angezeigt
      * **Liste**
Eine statische Liste, die anderswo in AEM definiert ist, wird für die Optionen verwendet
         * **Liste**
Der Pfad der statischen Liste in AEM
            * Verwenden Sie die Schaltfläche „Durchsuchen“, um die Listenressource zu finden.
      * **Datenquelle**
Eine Datenquelle wird für die Optionen verwendet.
         * **Datenquelle**
Ressourcentyp der Datenquelle
* **Hilfemeldung**
Ein Hinweis für den Benutzer, was in das Feld eingegeben werden kann

## Dialogfeld „Design“ {#design-dialog}

### Registerkarte „Stile“ {#styles-tab}

Die Formularoptionen-Komponente unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).
