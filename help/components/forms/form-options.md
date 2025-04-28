---
title: Formularoptionen-Komponente
description: Die Kernkomponente „Formularoptionen“ ermöglicht die Auswahl aus vordefinierten Optionen in verschiedenen Formaten.
role: Architect, Developer, Admin, User
exl-id: 8a74bd37-9b12-4fa6-bff2-53e337b16251
source-git-commit: 6fbc781db555bc6abaed1d122a9a8756e3d53222
workflow-type: ht
source-wordcount: '546'
ht-degree: 100%

---

# Formularoptionen-Komponente {#form-options-component}

Die Kernkomponente „Formularoptionen“ ermöglicht die Auswahl aus vordefinierten Optionen in verschiedenen Formaten.

## Nutzung {#usage}

Die Kernkomponente „Formularoptionen-Komponente“ ermöglicht die Übermittlung verschiedener Arten von Optionen, die auf vielerlei Arten präsentiert werden und die zusammen mit der [Formular-Container-Komponente](form-container.md) verwendet werden sollten.

Die Darstellung der Optionen, Beschriftungen und individuellen Optionen kann vom Inhaltseditor im Dialogfeld [Konfigurieren](#configure-dialog) definiert werden.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Formularoptionen-Komponente ist v2, die mit Version 2.0.0 der Kernkomponenten im Januar 2018 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |--- |---|
| v2 | Kompatibel mit<br>[Version 2.17.4](/help/versions.md) und vorherigen | Kompatibel | Kompatibel | Kompatibel |
| [v1](/help/components/v1/form-options-v1.md) | Kompatibel | Kompatibel | – | Kompatibel |

Weitere Informationen zu Kernkomponentenversionen und -freigaben finden Sie im Dokument [Kernkomponentenversionen](/help/versions.md).

## Musterkomponentenausgabe {#sample-component-output}

Um die Formularoptionen-Komponente kennenzulernen und Beispiele für die Konfigurationsoptionen sowie HTML- und JSON-Ausgaben anzuzeigen, besuchen Sie die [Komponentenbibliothek](https://adobe.com/go/aem_cmp_library_form_options_de).

### Technische Details {#technical-details}

Die neueste technische Dokumentation zur Formularoptionen-Komponente [finden Sie auf GitHub](https://adobe.com/go/aem_cmp_tech_form_options_v2_de).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Im Dialogfeld „Konfigurieren“ kann der Inhaltsautor den Typ der Optionen festlegen, die angezeigt werden sollen, Beschriftungen definieren und festlegen, welche Optionen verfügbar sind.

![Dialogfeld „Bearbeiten“ der Formularoptionen-Komponente](/help/assets/form-options-edit.png)

* **Typ** - Wie die Optionen angezeigt werden
   * **Kontrollkästchen**
   * **Optionsfelder**
   * **Dropdown**
   * **Dropdown für mehrere Auswahlen**
* **Titel** - Der Titel, der als Beschriftung für die Optionen angezeigt wird
* **Name** - Der Name des mit den Formulardaten gesendeten Felds
* **Quelle** - Wo die Optionen definiert sind
   * **Lokal** - Definiert in der Komponente
      * Tippen oder klicken Sie auf die Schaltfläche **Hinzufügen**, um einen Wert hinzuzufügen, und auf **Entfernen**, um einen Wert zu entfernen.
         * **Wert** - Der Wert, der gespeichert wird, wenn diese Option beim Senden des Formulars ausgewählt wird.
         * **Text** - Die Bezeichnung für die Option, die im Formular angezeigt wird
         * **Aktiv** - Die Option wird als ausgewählt markiert, wenn das Formular geladen wird
         * **Deaktiviert** - Die Option ist nicht auswählbar, wird aber trotzdem angezeigt
   * **Liste** – Eine an anderer Stelle in AEM definierte statische Liste wird für die Option verwendet
      * **Liste** - Der Pfad der statischen Liste in AEM
         * Verwenden Sie die Schaltfläche „Durchsuchen“, um die Listenressource zu finden.
   * **Datenquelle** - Eine Datenquelle wird für die Optionen verwendet
      * **Datenquelle** – Der Ressourcentyp der Datenquelle.
* **Hilfemeldung** – Ein Hinweis für den Benutzer dahingehend, was im Feld eingegeben werden kann.
* **ID** – Diese Option dient zur Kontrolle der eindeutigen Kennung der Komponente in der HTML-Datei und auf der [Datenschicht](/help/developing/data-layer/overview.md).
   * Wenn Sie das Feld leer lassen, wird automatisch eine eindeutige ID generiert, die Sie über die resultierende Seite finden.
   * Sofern eine ID angegeben wird, ist vom Autor bzw. der Autorin sicherzustellen, dass diese eindeutig ist.
   * Änderungen der ID können sich auf das CSS-, JS- und Datenschicht-Tracking auswirken.

## Dialogfeld „Design“ {#design-dialog}

### Registerkarte „Arten“ {#styles-tab}

Die Formularoptionen-Komponente unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).
