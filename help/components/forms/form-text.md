---
title: Formulartext-Komponente
description: Die Kernkomponente „Formulartext-Komponente“ ermöglicht die Eingabe von Formulartext zur Übermittlung.
translation-type: ht
source-git-commit: 95c0621f5423bfa515fe5e8b693e127ea56b4ae0

---


# Formulartext-Komponente{#form-text-component}

Die Kernkomponente „Formulartext-Komponente“ ermöglicht die Eingabe von Formulartext zur Übermittlung.

## Nutzung {#usage}

Die Formulartext-Komponente ermöglicht die Übermittlung verschiedener Texttypen und sollte zusammen mit der [Formularcontainer-Komponente](form-container.md) verwendet werden. Der Typ der Textvalidierung, Beschriftung und Hilfemeldungen kann vom Inhaltseditor im [Dialogfeld „Konfigurieren“](#configure-dialog) definiert werden.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Formulartext-Komponente ist v2, die mit Version 2.0.0 der Kernkomponenten im Januar 2018 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.3 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |--- |---|
| v2 | Kompatibel | Kompatibel | Kompatibel | Kompatibel |
| [v1](/help/components/v1/form-text-v1.md) | Kompatibel | Kompatibel | Kompatibel | - |

Weitere Informationen zu Kernkomponentenversionen und -freigaben finden Sie in den [Kernkomponentenversionen](/help/versions.md).

## Musterkomponentenausgabe {#sample-component-output}

Um die Formulartext-Komponente kennenzulernen und Beispiele für die Konfigurationsoptionen sowie HTML- und JSON-Ausgaben anzuzeigen, besuchen Sie die [Komponentenbibliothek](https://adobe.com/go/aem_cmp_library_form_text_de).

### Technische Details {#technical-details}

Die neueste technische Dokumentation zur Formulartext-Komponente [finden Sie auf GitHub](https://adobe.com/go/aem_cmp_tech_form_text_v2_de).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Das Dialogfeld „Konfigurieren“ ermöglicht es dem Inhaltsautor, den Texttyp sowie Standardwerte und Beschriftungen zu definieren.

### Registerkarte „Allgemein“ {#main-tab}

![](/help/assets/chlimage_1-23.png)

* **Einschränkung**
Die Art des Textes, der eingegeben und anhand dem validiert wird
   * **Text**
   * **Textbereich**
   * **E-Mail**
   * **Tel**
   * **Datum**
   * **Nummer**
   * **Kennwort**
* **Textzeile**
Anzahl der Zeilen, die im Textbereich angezeigt werden sollen (nur angezeigt, wenn **Beschränkung** auf **Textbereich** festgelegt ist)
* **Beschriftung**
Die Beschriftung, die für das Feld angezeigt wird
* **Beschriftung ausblenden**
Erforderlich, wenn die Beschriftung nur für Zugangszwecke erforderlich ist und keine weiteren visuellen Informationen über das Feld vermittelt
* **Element Name**
Der Name des mit den Formulardaten gesendeten Felds
* **Wert,**
Der im Feld vorbelegte Standardwert

### Registerkarte „Info“ {#about-tab}

![](/help/assets/chlimage_1-24.png)

* **Hilfemeldung**
: Sie weist den Benutzer darauf hin, was im Feld eingegeben werden kann
* **Bestimmt, ob die Hilfemeldung in der Formulareingabe angezeigt wird, wenn sie leer ist und sich nicht im Fokus befindet**


### Registerkarte „Beschränkungen“{#constraints-tab}

![](/help/assets/chlimage_1-25.png)

* **Beschränkungsmeldung**
   * Meldung wird beim Senden des Formulars als QuickInfo angezeigt, wenn der Wert den ausgewählten Typ nicht validiert
   * Wird nicht für Beschränkungstypen **Text** und **Textbereich** angezeigt
* **Erforderlich**
Wenn ausgewält, muss der Benutzer einen Wert ausfüllen, bevor das Formular gesendet werden kann
* **Schreibgeschützt**
Wenn ausgewählt, kann der Benutzer den Wert des Felds nicht ändern

## Dialogfeld „Design“ {#design-dialog}

Es gibt kein Dialogfeld „Design“ für die Formulartext-Komponente.
