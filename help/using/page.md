---
title: Seitenkomponente
description: Die Seitenkomponente ist eine Erweiterungskomponente für Seiten, die mit dem Vorlageneditor arbeitet und es ermöglicht, Seitenkopf-/Fußzeilen- und Strukturkomponenten mit dem Vorlageneditor zusammenzustellen.
translation-type: tm+mt
source-git-commit: 60df01ca9efe59b67bad57610d04496a2cdded9e

---


# Seitenkomponente{#page-component}

The Page Component is an extensible page component designed to work with the [template editor](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html) and allows page header/footer and structure components to be assembled with the template editor.

## Nutzung {#usage}

Die Seitenkomponente bildet die Grundlage aller Seiten, die mit den Kernkomponenten entworfen wurden, sowie bearbeitbarer Vorlagen. Mithilfe der Seitenkomponente können Kopfzeilen, Fußzeilen und der Struktur der Seite als Vorlage unter Verwendung der anderen Kernkomponenten definiert werden.

Im [Dialogfeld „Design“](#design-dialog) können benutzerdefinierte Client-seitige Bibliotheken für die Seite definiert werden. Im Gegensatz zu anderen Komponenten, die ein Dialogfeld „Bearbeiten“ haben, auf das direkt von der Komponente aus zugegriffen werden kann, weil die Komponente die Seite selbst ist, ist das [Dialogfeld „Bearbeiten“](#edit-dialog) der Seitenkomponente das Fenster „Seiteneigenschaften“.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Seitenkomponente ist v2, die mit Version 2.0.0 der Kernkomponenten im Januar 2018 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.3 | AEM 6.4 | AEM 6.5 | AEM als Cloud-Dienst |
|---|---|---|---|---|
| [v2](page-v1.md) | Kompatibel | Kompatibel | Kompatibel | Kompatibel |
| v1 | Kompatibel | Kompatibel | Kompatibel | - |

Weitere Informationen zu Kernkomponentenversionen und -freigaben finden Sie in den [Kernkomponentenversionen](versions.md).

>[!NOTE]
>
>To enable redirect at `cq:Page` level for version 2 of the page component and AEM 6.3, [service pack 2](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp2-release-notes.html) or later is required. Diese Umleitung war in früheren Versionen nicht verfügbar.

## Musterkomponentenausgabe {#sample-component-output}

Im Folgenden finden Sie ein Beispiel von [We.Retail](https://docs.adobe.com/content/help/en/experience-manager-65/developing/bestpractices/we-retail/we-retail.html).

### Screenshot {#screenshot}

![](assets/chlimage_1.png)

### Technische Details {#technical-details}

The latest technical documentation about the Page Component [can be found on GitHub](https://adobe.com/go/aem_cmp_tech_page_v2).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](developing.md).

## Dialogfeld „Bearbeiten“ {#edit-dialog}

Because the component represents the entire page, settings that would normally be in an edit dialog are found in the [Page Properties](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html) window.

## Dialogfeld „Design“{#design-dialog}

Da die Komponente die gesamte Seite darstellt, wird das Dialogfeld „Design“ über **Seiteninformationen > Seitenrichtlinien** aufgerufen, wenn Sie die Seitenvorlage bearbeiten.

![](assets/screen_shot_2018-04-03at113410.png)

>[!NOTE]
>
>In früheren Versionen von AEM hieß die **Seitenrichtlinie** noch **Seitendesign**.

### Registerkarte „Eigenschaften“{#properties-tab}

Mithilfe des Fensters „Seitendesign“ können Sie die zu ladenden Client-Bibliotheken sowie die Webressourcenbibliothek für die Seite definieren.

* **Client-Bibliothek**
Dies definiert die Kategorien der Client-Bibliothek, die geladen werden sollen. JavaScript wird am Textende hinzugefügt und die CSS wird dem Seitenkopf hinzugefügt.
* **Seitenkopf Client-Bibliotheken JavaScript**
Dies definiert die JavaScript-Client-Bibliothekskategorien, die im Seitenkopf geladen werden.
   * Kategorien, die hier definiert werden und auch im Feld **Client-Bibliotheken** vorhanden sind, haben JavaScript, das anstelle am Textende in der Seitenkopfzeile geladen wird.
   * Es wird keine CSS geladen, es sei denn, die Kategorie ist ebenfalls im Feld **Client-Bibliotheken** enthalten.

* **Webressourcen Client-Bibliothek**
Die Kategorie der Client-Bibliothek, die verwendet wird, um Webressourcen wie etwa Favicons zu bedienen.

![](assets/screenshot_2018-10-19at104949.png)

Bibliotheken können wie folgt für die beiden Felder **Client-Bibliotheken** und **Seitenkopf Client-Bibliotheken JavaScript** konfiguriert werden:

* Um ein neues Feld hinzuzufügen, klicken oder tippen Sie auf die Schaltfläche **Hinzufügen** unter den Feldern.
* Um ein Feld zu entfernen, klicken oder tippen Sie neben dem Feld, das entfernt werden soll, auf das Papierkorbsymbol.
* Um die Ladereihenfolge neu anzuordnen, klicken oder tippen Sie auf den Griff neben dem Feld, das verschoben werden soll, und ziehen Sie es.

Weitere Informationen zur Verwendung clientseitiger Bibliotheken finden Sie unter [Verwenden clientseitiger Bibliotheken](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/clientlibs.html).

>[!CAUTION]
>
>Die Möglichkeit, Client-Bibliotheken für den Seitenkopf separat zu definieren, wurde mit Version 2.2.0 der Kernkomponenten eingeführt.

### Registerkarte „Stile“ {#styles-tab}

Die Seitenkomponente unterstützt das AEM-[Stilsystem](authoring.md#component-styling).
