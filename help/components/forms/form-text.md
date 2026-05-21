---
title: Formulartext-Komponente
description: Die Kernkomponente „Formulartext-Komponente“ ermöglicht die Eingabe von Formulartext zur Übermittlung.
role: Developer, Admin, User
exl-id: e8fa3881-51fb-4726-9654-8f93acfb7464
TQID: https://experienceleague.adobe.com/9js-R-LzxStEKmgs59UvZBz-htCWyIx-PQIjpIKJAqc
product_v2: id: c45915cf-e157-4af7-a80d-97b905bcb3a5id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: e2c1b6d3-bb7e-4fe8-8c72-f7b403298e91
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: cc72dcf1-72e1-48cc-b434-e7c27d62d67c
source-git-commit: 73aa5234ac63fa3be99feebce448bb6722513838
workflow-type: tm+mt
source-wordcount: 581
ht-degree: 100%

---

# Formulartext-Komponente{#form-text-component}

Die Kernkomponente „Formulartext-Komponente“ ermöglicht die Eingabe von Formulartext zur Übermittlung.

## Nutzung {#usage}

Die Formulartext-Komponente ermöglicht die Übermittlung verschiedener Texttypen und sollte zusammen mit der [Formular-Container-Komponente](form-container.md) verwendet werden. Der Typ der Textvalidierung, Beschriftung und Hilfemeldungen kann vom Inhaltseditor im [Dialogfeld „Konfigurieren“](#configure-dialog) definiert werden.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Formulartext-Komponente ist v2, die mit Version 2.0.0 der Kernkomponenten im Januar 2018 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |--- |---|---|
| v2 | Kompatibel mit<br>[Version 2.17.4](/help/versions.md) und vorherigen | Kompatibel | Kompatibel | Kompatibel |
| [v1](/help/components/v1/form-text-v1.md) | Kompatibel | Kompatibel | – | Kompatibel |

Weitere Informationen zu Kernkomponentenversionen und -freigaben finden Sie im Dokument [Kernkomponentenversionen](/help/versions.md).

## Musterkomponentenausgabe {#sample-component-output}

Um die Formulartext-Komponente kennenzulernen und Beispiele für die Konfigurationsoptionen sowie HTML- und JSON-Ausgaben anzuzeigen, besuchen Sie die [Komponentenbibliothek](https://adobe.com/go/aem_cmp_library_form_text_de).

### Technische Details {#technical-details}

Die neueste technische Dokumentation zur Formulartext-Komponente [finden Sie auf GitHub](https://adobe.com/go/aem_cmp_tech_form_text_v2_de).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Das Dialogfeld „Konfigurieren“ ermöglicht es dem Inhaltsautor, den Texttyp sowie Standardwerte und Beschriftungen zu definieren.

### Registerkarte „Eigenschaften“ {#properties-tab}

![Registerkarte „Eigenschaften“](/help/assets/form-text-edit-properties.png)

* **Beschränkung** - Der Typ des einzustellenden Texts und der validiert wird mit
   * **Text**
   * **Textbereich**
   * **E-Mail**
   * **Tel**
   * **Datum**
   * **Nummer**
   * **Kennwort**
* **Textzeilen** - Anzahl der im Textbereich anzuzeigenden Zeilen (nur angezeigt, wenn **Beschränkung** auf **Textbereich** festgelegt ist).
* **Beschriftung** - Die Beschriftung, die für das Feld angezeigt wird
* **Beschriftung ausblenden** - Erforderlich, wenn die Beschriftung nur für Ein-/Ausgabehilfe erforderlich ist und keine zusätzlichen visuellen Informationen über das Feld enthält.
* **Elementname** - Der Name des mit den Formulardaten gesendeten Felds.
* **Wert** – Der Standardwert, mit dem das Feld vorausgefüllt wird
* **ID** – Diese Option dient zur Kontrolle der eindeutigen Kennung der Komponente in der HTML-Datei und auf der [Datenschicht](/help/developing/data-layer/overview.md).
   * Wenn Sie das Feld leer lassen, wird automatisch eine eindeutige ID generiert, die Sie über die resultierende Seite finden.
   * Sofern eine ID angegeben wird, ist vom Autor bzw. der Autorin sicherzustellen, dass diese eindeutig ist.
   * Änderungen der ID können sich auf das CSS-, JS- und Datenschicht-Tracking auswirken.

### Registerkarte „Info“ {#about-tab}

![Registerkarte „Info“](/help/assets/form-text-edit-about.png)

* **Hilfemeldung** – Ein Hinweis für den Benutzer dahingehend, was im Feld eingegeben werden kann
* **Hilfemeldung als Platzhalter anzeigen** - Bestimmt, ob die Hilfemeldung in der Formulareingabe angezeigt wird, wenn sie leer ist und sich nicht im Fokus befindet

### Registerkarte „Beschränkungen“ {#constraints-tab}

![Registerkarte „Beschränkungen“](/help/assets/form-text-edit-constraints.png)

* **Beschränkungsmeldung**
   * Meldung wird beim Senden des Formulars als QuickInfo angezeigt, wenn der Wert den ausgewählten Typ nicht validiert
   * Wird nicht für Beschränkungstypen **Text** und **Textbereich** angezeigt
* **Erforderlich** - Gibt an, ob der Benutzer einen Wert ausfüllen muss, bevor das Formular senden kann
   * **Erforderliche Meldung** – Meldung, die als QuickInfo angezeigt wird, wenn das Feld leer gelassen wird
* **Schreibgeschützt:** Wenn ausgewählt, kann der Benutzer den Wert des Felds nicht ändern

## Dialogfeld „Design“ {#design-dialog}

### Registerkarte „Arten“ {#styles-tab}

Die Formulartext-Komponente unterstützt das [Stilsystem](/help/get-started/authoring.md#component-styling) von AEM.
