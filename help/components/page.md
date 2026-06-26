---
title: Seitenkomponente
description: Die Seitenkomponente ist eine Erweiterungskomponente für Seiten, die mit dem Vorlageneditor arbeitet und es ermöglicht, Seitenkopf-/Fußzeilen- und Strukturkomponenten mit dem Vorlageneditor zusammenzustellen.
role: Developer, Admin, User
exl-id: 2503e067-abed-427d-8a54-8b79e3451487
TQID: https://experienceleague.adobe.com/d70sxBsyVP2Qh-O3cOkZv6Wj-3ZiqpRYVnAYD6zNl3A
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: e2c1b6d3-bb7e-4fe8-8c72-f7b403298e91
subfeature_v2:
  - id: f86a5563-8f73-4ec0-be7d-a1782604870a
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: cc72dcf1-72e1-48cc-b434-e7c27d62d67c
source-git-commit: 2a9a69dd7eeade8cdc2f681a354350c4370d5d1b
workflow-type: tm+mt
source-wordcount: 778
ht-degree: 90%

---

# Seitenkomponente{#page-component}

Die Seitenkomponente ist eine Erweiterungskomponente für Seiten, die mit dem [Vorlageneditor](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=de) arbeitet und es ermöglicht, Seitenkopf-/Fußzeilen- und Strukturkomponenten mit dem Vorlageneditor zusammenzustellen.

{{traditional-aem}}

## Nutzung {#usage}

Die Seitenkomponente bildet die Grundlage aller Seiten, die mit den Kernkomponenten entworfen wurden, sowie bearbeitbarer Vorlagen. Mithilfe der Seitenkomponente können Kopfzeilen, Fußzeilen und die Struktur der Seite unter Verwendung der anderen Kernkomponenten als Vorlage definiert werden.

Im [Dialogfeld „Design“](#design-dialog) können benutzerdefinierte Client-seitige Bibliotheken für die Seite definiert werden. Im Gegensatz zu anderen Komponenten, die ein Dialogfeld „Bearbeiten“ haben, auf das direkt von der Komponente aus zugegriffen werden kann, weil die Komponente die Seite selbst ist, ist das [Dialogfeld „Bearbeiten“](#edit-dialog) der Seitenkomponente das Fenster „Seiteneigenschaften“.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Seitenkomponente ist v3, die mit Version 2.18.0 der Kernkomponenten im Februar 2022 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|---|---|---|---|---|
| v3 | – | Kompatibel | Kompatibel | Kompatibel |
| [v2](v2/page.md) | Kompatibel | Kompatibel | – | Kompatibel |
| [v1](v1/page-v1.md) | Kompatibel | Kompatibel | – | Kompatibel |

Weitere Informationen zu Kernkomponentenversionen und -freigaben finden Sie im Dokument [Kernkomponentenversionen](/help/versions.md).

### Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur Seitenkomponente [finden Sie auf GitHub](https://adobe.com/go/aem_cmp_tech_page_v3_de).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Dialogfeld „Bearbeiten“ {#edit-dialog}

Da die Komponente die gesamte Seite darstellt, befinden sich Einstellungen, die normalerweise in einem Dialogfeld „Bearbeiten“ enthalten wären, im Fenster [Seiteneigenschaften](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html?lang=de).

### Unterstützung strukturierter Daten {#structured-data}

[Version 2.31.0](/help/versions.md) der Kernkomponenten führte die Unterstützung strukturierter Daten (JSON-LD) auf Seitenebene der Typen [schema.org](https://schema.org) für alle Versionen der Seitenkomponente ein.  AEM rendert diese Blöcke Server-seitig im Seitenkopf.

[Version 2026.6.0 von AEM as a Cloud Service](https://experienceleague.adobe.com/de/docs/experience-manager-release-information/aem-release-updates/update-releases-roadmap) wurde die Möglichkeit für Autoren hinzugefügt, im Abschnitt **SEO** der Registerkarte **Erweitert** das Fenster Seiteneigenschaften zu verwenden, um einen oder mehrere JSON-LD-Blöcke zu einer Seite hinzuzufügen.

## Dialogfeld „Design“ {#design-dialog}

Da die Komponente die gesamte Seite darstellt, wird das Dialogfeld „Design“ über **Seiteninformationen > Seitenrichtlinien** aufgerufen, wenn Sie die Seitenvorlage bearbeiten.

![Seitenrichtlinie](/help/assets/page-policy.png)

>[!NOTE]
>
>In früheren Versionen von AEM hieß die **Seitenrichtlinie** noch **Seitendesign**.

### Registerkarte „Eigenschaften“ {#properties-tab}

Mithilfe des Fensters „Seitendesign“ können Sie die zu ladenden Client-Bibliotheken sowie die Web-Ressourcenbibliothek für die Seite definieren.

* **Client-Bibliotheken** - Damit werden Kategorien der Client-Bibliothek definiert, die geladen werden. JavaScript wird am Textende hinzugefügt und das CSS wird dem Seitenkopf hinzugefügt.
* **JavaScript-Seitenkopf der Client-Bibliotheken**
Definiert die Kategorien der JavaScript-Client-Bibliothek, die im Seitenkopf geladen werden.
   * Kategorien, die hier definiert werden und auch im Feld **Client-Bibliotheken** vorhanden sind, haben JavaScript, das anstelle am Textende in der Seitenkopfzeile geladen wird.
   * Es wird keine CSS geladen, es sei denn, die Kategorie ist ebenfalls im Feld **Client-Bibliotheken** enthalten.

* **Client-Bibliothek der Web-Ressourcen**
Die Kategorie der Client-Bibliothek, die verwendet wird, um Web-Ressourcen wie etwa Favicons zu bedienen.

* **Zur Auswahl des Hauptinhaltselements wechseln** - Wird als Barrierefreiheitsfunktion verwendet, um direkt zum Hauptinhalt der Seite zu springen.

* **Links in alternativen Sprachen rendern** – Wenn diese Option aktiviert ist, werden Links zu alternativen Sprachversionen der Seite in derselben Site zum Kopfbereich der Seite hinzugefügt.

![Dialogfeld „Design“ der Seitenkomponente](/help/assets/page-design.png)

Bibliotheken können wie folgt für die beiden Felder **Client-Bibliotheken** und **JavaScript-Seitenkopf der Client-Bibliotheken** konfiguriert werden:

* Um ein neues Feld hinzuzufügen, klicken oder tippen Sie auf die Schaltfläche **Hinzufügen** unter den Feldern.
* Um ein Feld zu entfernen, klicken oder tippen Sie neben dem Feld, das entfernt werden soll, auf das Papierkorbsymbol.
* Um die Ladereihenfolge neu anzuordnen, klicken oder tippen Sie auf den Griff neben dem Feld, das verschoben werden soll, und ziehen Sie es.

Weitere Informationen zur Verwendung clientseitiger Bibliotheken finden Sie unter [Verwendung clientseitiger Bibliotheken](https://helpx.adobe.com/de/experience-manager/6-5/sites/developing/using/clientlibs.html).

>[!CAUTION]
>
>Die Möglichkeit, Client-Bibliotheken für den Seitenkopf separat zu definieren, wurde mit Version 2.2.0 der Kernkomponenten eingeführt.

### Registerkarte „Arten“ {#styles-tab}

Die Seitenkomponente unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).

## Adobe Client-Datenschicht {#data-layer}

Die Seitenkomponente unterstützt die [Adobe Client-Datenschicht](/help/developing/data-layer/overview.md).
