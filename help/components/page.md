---
title: Seitenkomponente
description: Die Seitenkomponente ist eine Erweiterungskomponente für Seiten, die mit dem Vorlageneditor arbeitet und es ermöglicht, Seitenkopf-/Fußzeilen- und Strukturkomponenten mit dem Vorlageneditor zusammenzustellen.
translation-type: ht
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# Seitenkomponente{#page-component}

Die Seitenkomponente ist eine Erweiterungskomponente für Seiten, die mit dem [Vorlageneditor](https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/sites/authoring/features/templates.translate.html) arbeitet und es ermöglicht, Seitenkopf-/Fußzeilen- und Strukturkomponenten mit dem Vorlageneditor zusammenzustellen.

## Nutzung {#usage}

Die Seitenkomponente bildet die Grundlage aller Seiten, die mit den Kernkomponenten entworfen wurden, sowie bearbeitbarer Vorlagen. Mithilfe der Seitenkomponente können Kopfzeilen, Fußzeilen und der Struktur der Seite als Vorlage unter Verwendung der anderen Kernkomponenten definiert werden.

Im [Dialogfeld „Design“](#design-dialog) können benutzerdefinierte Client-seitige Bibliotheken für die Seite definiert werden. Im Gegensatz zu anderen Komponenten, die ein Dialogfeld „Bearbeiten“ haben, auf das direkt von der Komponente aus zugegriffen werden kann, weil die Komponente die Seite selbst ist, ist das [Dialogfeld „Bearbeiten“](#edit-dialog) der Seitenkomponente das Fenster „Seiteneigenschaften“.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Seitenkomponente ist v2, die mit Version 2.0.0 der Kernkomponenten im Januar 2018 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.3 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|---|---|
| v2 | Kompatibel | Kompatibel | Kompatibel | Kompatibel |
| [v1](v1/page-v1.md) | Kompatibel | Kompatibel | Kompatibel | - |

Weitere Informationen zu Kernkomponentenversionen und -freigaben finden Sie in den [Kernkomponentenversionen](/help/versions.md).

>[!NOTE]
>
>Um die Umleitung auf `cq:Page`-Ebene für Version 2 der Seitenkomponente und AEM 6.3 zu aktivieren, ist [Service Pack 2](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp2-release-notes.html) oder höher erforderlich. Diese Umleitung war in früheren Versionen nicht verfügbar.

## Musterkomponentenausgabe {#sample-component-output}

Im Folgenden finden Sie ein Beispiel von [We.Retail](https://docs.adobe.com/content/help/en/experience-manager-65/developing/bestpractices/we-retail/we-retail.html).

### Screenshot {#screenshot}

![](/help/assets/chlimage_1.png)

### Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur Seitenkomponente [finden Sie auf GitHub](https://adobe.com/go/aem_cmp_tech_page_v2).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Dialogfeld „Bearbeiten“ {#edit-dialog}

Da die Komponente die gesamte Seite darstellt, befinden sich Einstellungen, die normalerweise in einem Dialogfeld „Bearbeiten“ enthalten wären, im Fenster [Seiteneigenschaften](https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.translate.html).

## Dialogfeld „Design“{#design-dialog}

Da die Komponente die gesamte Seite darstellt, wird das Dialogfeld „Design“ über **Seiteninformationen > Seitenrichtlinien** aufgerufen, wenn Sie die Seitenvorlage bearbeiten.

![](/help/assets/screen_shot_2018-04-03at113410.png)

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

![](/help/assets/screenshot_2018-10-19at104949.png)

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
