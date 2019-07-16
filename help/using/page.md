---
title: Seitenkomponente
seo-title: Seitenkomponente
description: Die Seitenkomponente ist eine Erweiterungskomponente für Seiten, die mit dem Vorlageneditor arbeitet und es ermöglicht, Seitenkopf-/Fußzeilen- und Strukturkomponenten mit dem Vorlageneditor zusammenzustellen.
seo-description: Die Seitenkomponente ist eine Erweiterungskomponente für Seiten, die mit dem Vorlageneditor arbeitet und es ermöglicht, Seitenkopf-/Fußzeilen- und Strukturkomponenten mit dem Vorlageneditor zusammenzustellen.
uuid: 7052a5b1-e7f1-4944-a55c-faf739b6e89c
contentOwner: Benutzer
content-type: Referenz
topic-tags: Authoring
products: SG_EXPERIENCEMANAGER/CORECOMPONENTS-new
discoiquuid: cb1a745a-30c4-4ad6-a04f-fefb3666cd95
translation-type: ht
source-git-commit: 632d6abb1f13667cc0457152268d50af3bfabfc4

---


# Seitenkomponente{#page-component}

Die Seitenkomponente ist eine Erweiterungskomponente für Seiten, die den Einsatz mit dem [Vorlageneditor](https://helpx.adobe.com/de/experience-manager/6-5/sites/authoring/using/templates.html) arbeitet und es ermöglicht, Seitenkopf/Fußzeile und Strukturkomponenten mit dem Vorlageneditor zusammenzufügen.

## Nutzung {#usage}

Die Seitenkomponente bildet die Grundlage aller Seiten, die mit den Kernkomponenten entworfen wurden, sowie bearbeitbarer Vorlagen. Mithilfe der Seitenkomponente können Kopfzeilen, Fußzeilen und der Struktur der Seite als Vorlage unter Verwendung der anderen Kernkomponenten definiert werden.

Im [Dialogfeld „Design“](#design-dialog) können benutzerdefinierte Client-seitige Bibliotheken für die Seite definiert werden. Im Gegensatz zu anderen Komponenten, die ein Dialogfeld „Bearbeiten“ haben, auf das direkt von der Komponente aus zugegriffen werden kann, weil die Komponente die Seite selbst ist, ist das [Dialogfeld „Bearbeiten“](#edit-dialog) der Seitenkomponente das Fenster „Seiteneigenschaften“.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Seitenkomponente ist v2, die mit Version 2.0.0 der Kernkomponenten im Januar 2018 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|---|---|---|---|
| [v2](page-v1.md) | Kompatibel | Kompatibel | Kompatibel |
| v1 | Kompatibel | Kompatibel | Kompatibel |

Weitere Informationen zu Kernkomponentenversionen und -freigaben finden Sie in den [Kernkomponentenversionen](versions.md).

>[!NOTE]
>
>Um die Umleitung auf `cq:Page`-Ebene für Version 2 der Seitenkomponente und AEM 6.3 zu aktivieren, ist [Service Pack 2](https://helpx.adobe.com/de/experience-manager/6-3/release-notes/sp2-release-notes.html) oder höher erforderlich. Diese Umleitung war in früheren Versionen nicht verfügbar.

## Musterkomponentenausgabe {#sample-component-output}

Folgendes Beispiel wurde von [We.Retail](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html) übernommen.

### Screenshot {#screenshot}

![](assets/chlimage_1.png)

### Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur Seitenkomponente [finden Sie auf GitHub](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/page/v2/page).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](developing.md).

## Dialogfeld „Bearbeiten“ {#edit-dialog}

Da die Komponente die gesamte Seite darstellt, befinden sich Einstellungen, die normalerweise in einem Dialogfeld „Bearbeiten“ enthalten wären, im Fenster [„Seiteneigenschaften“](https://helpx.adobe.com/de/experience-manager/6-5/sites/authoring/using/editing-page-properties.html).

## Dialogfeld „Design“{#design-dialog}

Da die Komponente die gesamte Seite darstellt, wird das Dialogfeld „Design“ über **Seiteninformationen &gt; Seitenrichtlinien** aufgerufen, wenn Sie die Seitenvorlage bearbeiten.

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

Weitere Informationen zur Verwendung Client-seitiger Bibliotheken finden Sie unter [Verwendung von Client-seitigen Bibliotheken](https://helpx.adobe.com/de/experience-manager/6-5/sites/developing/using/clientlibs.html).

>[!CAUTION]
>
>Die Möglichkeit, Client-Bibliotheken für den Seitenkopf separat zu definieren, wurde mit Version 2.2.0 der Kernkomponenten eingeführt.

### Registerkarte „Stile“ {#styles-tab}

Die Seitenkomponente unterstützt das AEM-[Stilsystem](authoring.md#component-styling).