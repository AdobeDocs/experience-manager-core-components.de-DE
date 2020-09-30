---
title: Seitenkomponente
description: Die Seitenkomponente ist eine Erweiterungskomponente für Seiten, die mit dem Vorlageneditor arbeitet und es ermöglicht, Seitenkopf-/Fußzeilen- und Strukturkomponenten mit dem Vorlageneditor zusammenzustellen.
translation-type: tm+mt
source-git-commit: 4813748bcfa83ce7c73e81d4e4d445ecc8215d26
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Seitenkomponente{#page-component}

Die Seitenkomponente ist eine Erweiterungskomponente für Seiten, die mit dem [Vorlageneditor](https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/sites/authoring/features/templates.translate.html) arbeitet und es ermöglicht, Seitenkopf-/Fußzeilen- und Strukturkomponenten mit dem Vorlageneditor zusammenzustellen.

## Verwendung {#usage}

Die Seitenkomponente bildet die Grundlage aller Seiten, die mit den Kernkomponenten entworfen wurden, sowie bearbeitbarer Vorlagen. Mithilfe der Seitenkomponente können Kopfzeilen, Fußzeilen und der Struktur der Seite als Vorlage unter Verwendung der anderen Kernkomponenten definiert werden.

Im [Dialogfeld „Design“](#design-dialog) können benutzerdefinierte Client-seitige Bibliotheken für die Seite definiert werden. Im Gegensatz zu anderen Komponenten, die ein Dialogfeld „Bearbeiten“ haben, auf das direkt von der Komponente aus zugegriffen werden kann, weil die Komponente die Seite selbst ist, ist das [Dialogfeld „Bearbeiten“](#edit-dialog) der Seitenkomponente das Fenster „Seiteneigenschaften“.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Seitenkomponente ist v2, die mit Version 2.0.0 der Kernkomponenten im Januar 2018 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|---|
| v2 | Kompatibel | Kompatibel | Kompatibel |
| [v1](v1/page-v1.md) | Kompatibel | Kompatibel | - |

Weitere Informationen zu Kernkomponentenversionen und -freigaben finden Sie in den [Kernkomponentenversionen](/help/versions.md).

### Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur Seitenkomponente [finden Sie auf GitHub](https://adobe.com/go/aem_cmp_tech_page_v2_de).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Dialogfeld „Bearbeiten“ {#edit-dialog}

Da die Komponente die gesamte Seite darstellt, befinden sich Einstellungen, die normalerweise in einem Dialogfeld „Bearbeiten“ enthalten wären, im Fenster [Seiteneigenschaften](https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.translate.html).

## Dialogfeld „Design“ {#design-dialog}

Da die Komponente die gesamte Seite darstellt, wird das Dialogfeld „Design“ über **Seiteninformationen > Seitenrichtlinien** aufgerufen, wenn Sie die Seitenvorlage bearbeiten.

![Seitenrichtlinie](/help/assets/page-policy.png)

>[!NOTE]
>
>In früheren Versionen von AEM hieß die **Seitenrichtlinie** noch **Seitendesign**.

### Registerkarte „Eigenschaften“ {#properties-tab}

Mithilfe des Fensters „Seitendesign“ können Sie die zu ladenden Client-Bibliotheken sowie die Webressourcenbibliothek für die Seite definieren.

* **Client-Bibliotheken** – Damit werden Kategorien der Client-Bibliothek definiert, die geladen werden. JavaScript wird am Textende hinzugefügt und das CSS wird dem Seitenkopf hinzugefügt.
* **JavaScript-Seitenkopf der Client-Bibliotheken**
Definiert die Kategorien der JavaScript-Client-Bibliothek, die im Seitenkopf geladen werden.
   * Kategorien, die hier definiert werden und auch im Feld **Client-Bibliotheken** vorhanden sind, haben JavaScript, das anstelle am Textende in der Seitenkopfzeile geladen wird.
   * Es wird keine CSS geladen, es sei denn, die Kategorie ist ebenfalls im Feld **Client-Bibliotheken** enthalten.

* **Client-Bibliothek der Web-Ressourcen**
Die Kategorie der Client-Bibliothek, die verwendet wird, um Web-Ressourcen wie etwa Favicons zu bedienen.

* **Zur Elementauswahl des Hauptinhalts wechseln** – Wird als Barrierefreiheitsfunktion verwendet, um direkt zum Hauptinhalt der Seite zu springen.

![Dialogfeld „Design“ der Seitenkomponente](/help/assets/page-design.png)

Bibliotheken können wie folgt für die beiden Felder **Client-Bibliotheken** und **Seitenkopf Client-Bibliotheken JavaScript** konfiguriert werden:

* Um ein neues Feld hinzuzufügen, klicken oder tippen Sie auf die Schaltfläche **Hinzufügen** unter den Feldern.
* Um ein Feld zu entfernen, klicken oder tippen Sie neben dem Feld, das entfernt werden soll, auf das Papierkorbsymbol.
* Um die Ladereihenfolge neu anzuordnen, klicken oder tippen Sie auf den Griff neben dem Feld, das verschoben werden soll, und ziehen Sie es.

Weitere Informationen zur Verwendung clientseitiger Bibliotheken finden Sie unter [Verwendung clientseitiger Bibliotheken](https://helpx.adobe.com/de/experience-manager/6-5/sites/developing/using/clientlibs.html).

>[!CAUTION]
>
>Die Möglichkeit, Client-Bibliotheken für den Seitenkopf separat zu definieren, wurde mit Version 2.2.0 der Kernkomponenten eingeführt.

### Registerkarte „Stile“ {#styles-tab}

Die Seitenkomponente unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).
