---
title: Inhaltskomponenten-KI-Suche
description: Die Inhaltsdatenkomponente bietet den Besuchern Ihrer Site eine generative KI-gestützte KI-Suche.
role: Developer, Admin, User
product_v2: id: c45915cf-e157-4af7-a80d-97b905bcb3a5id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: e2c1b6d3-bb7e-4fe8-8c72-f7b403298e91
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080b
source-git-commit: e721e8b9469646300432b87d42bfb742aaf5f3fb
workflow-type: tm+mt
source-wordcount: 805
ht-degree: 16%

---


# Inhaltskomponenten-KI-Suche {#content-ai-search-component}

Die Inhaltsdatenkomponente bietet den Besuchern Ihrer Site eine generative KI-gestützte KI-Suche.

{{traditional-aem}}

## Nutzung {#usage}

Mit der KI-Suche „Inhaltsdaten“ können Besuchende eine [Content-Source](https://experienceleague.adobe.com/en/docs/experience-manager-content-ai/using/contentsources) direkt auf einer Seite durchsuchen und optional eine von KI erstellte generative Ergebniszusammenfassung anzeigen. Es kombiniert ein standardmäßiges Volltext-/semantisches Suchfeld mit einem umschaltbaren Bedienfeld **KI-generierte Zusammenfassung anzeigen** das von AEM Content AI unterstützt wird.

Mit [ Dialogfeld „Bearbeiten](#edit-dialog) kann der Inhaltsautor den Inhaltsbereich der Suche, das Suchverhalten und die generativen Einstellungen definieren. Es gibt kein Dialogfeld „Design“, da auf Vorlagenebene keine Einstellungen verfügbar sind.

>[!NOTE]
>
>Um die Inhaltskomponente verwenden zu können, müssen Sie Zugriff auf eine Content-KI-Source haben und Ihr Administrator muss die KI-Suche für Ihr Projekt aktiviert haben. Weitere KI-Suchen finden [ im Dokument „Konfigurieren ](/help/developing/ai-search.md) Inhaltsdatenkomponente“.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle KI-Suche der Inhaltsdatenkomponente ist v1, die mit Version 2.32.0 der Kernkomponenten im Juli 2026 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|---|---|---|---|---|
| v1 | – | – | – | Laufend |

Weitere Informationen zu Kernkomponentenversionen und -freigaben finden Sie im Dokument [Kernkomponentenversionen.](/help/versions.md)

## Musterkomponentenausgabe {#sample-component-output}

Um die Inhaltskomponenten-KI-Suche sowie Beispiele für die Konfigurationsoptionen sowie HTML- und JSON-Ausgaben zu erhalten, besuchen Sie die [Komponentenbibliothek.](https://adobe.com/go/aem_cmp_library_ai_search)

## Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur Inhaltsdatenkomponente [finden Sie auf GitHub.](https://adobe.com/go/aem_cmp_tech_ai_search_v1)

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Dialogfeld „Bearbeiten“ {#edit-dialog}

Das Dialogfeld „Bearbeiten“ ermöglicht es dem Inhaltsautor, den Inhaltsbereich der Suche, das Suchverhalten und die generativen Einstellungen zu definieren. Es gibt kein Dialogfeld „Design“, da auf Vorlagenebene keine Einstellungen verfügbar sind.

### Registerkarte „Inhaltsbereich“ {#content-scope}

![Registerkarte „Inhaltsbereich“ des Dialogfelds „Bearbeiten“](/help/assets/content-ai-search-edit-content-scope.png)

* **ID** - Diese Option dient zur Kontrolle der eindeutigen Kennung der Komponente in der HTML und auf der [Datenschicht.](/help/developing/data-layer/overview.md)
  * Wenn Sie das Feld leer lassen, wird automatisch eine eindeutige ID generiert, die Sie über die resultierende Seite finden.
  * Sofern eine ID angegeben wird, ist vom Autor bzw. der Autorin sicherzustellen, dass diese eindeutig ist.
  * Änderungen der ID können sich auf das CSS-, JS- und Datenschicht-Tracking auswirken.
* **Content-Source-**: Dieses Feld definiert den Typ der Inhaltsquelle. Wenn Sie einen Typ auswählen, werden in **Dropdown-Liste** Content Source&quot; übereinstimmende Quellen angezeigt.
  * **ACQUISITION**: Der Standardwert, der für öffentliche Quellen mit anonymen Zugriff verwendet wird, die über eine crawlen-/Akquise-Pipeline indiziert werden
  * **AEM_AUTHOR** - Eine inhaltsbezogene KI-seitige Quelle, deren Inhalt von einer AEM-Autoreninstanz erfasst wurde
  * **AEM_PUBLISH** -Eine inhaltsbezogene KI-seitige Quelle, deren Inhalt von einer AEM-Veröffentlichungsinstanz erfasst wurde
  * **CUSTOM** - Eine Quelle, die außerhalb der eigenen Aufnahme-Pipelines von AEM registriert ist
* **Inhaltsquellen** - Dies definiert den Content Source, nach dem diese Komponente sucht.
  * Verfügbare Einträge entsprechen bereits vorhandenen und verfügbaren Inhaltsquellen (**verfügbar** sowie dem in **Content Source Type** festgelegten
  * Weitere Informationen finden Sie [ Dokument „Einrichten und Verwalten ](https://experienceleague.adobe.com/en/docs/experience-manager-content-ai/using/contentsources) Content-KI-Quellen“.

### Registerkarte Suchverhalten {#search-behavior}

![Registerkarte „Suchverhalten“ im Dialogfeld „Bearbeiten“](/help/assets/content-ai-search-edit-search-behavior.png)

* **Ergebnis-Layout** - Mit dieser Option wird definiert, wie die Suchergebnisse dem Besucher angezeigt werden.
  * **Karten** - Mit dieser Option werden die Ergebnisse in einem Rasterformat angezeigt.
  * **Liste** - Mit dieser Option werden die Ergebnisse in einem Listenformat angezeigt.
* **Ergebnisgröße** - Definiert die Anzahl der Ergebnisse, die pro Suchanfrage abgerufen werden.
  * Der Standardwert ist `12`.
  * Besucher können weitere Ergebnisse laden, wenn zusätzliche Übereinstimmungen verfügbar sind.
* **Platzhaltertext** - Dies ist der Text, der im leeren Sucheingabefeld angezeigt wird, bevor der Besucher eine Suchabfrage aufruft.

### Registerkarte „Generative Suche“ {#generative-search}

![Registerkarte „Generative Suche“ im Dialogfeld „Bearbeiten“](/help/assets/content-ai-search-edit-generative-search.png)

* **Umschalter für generative Zusammenfassung für Besucher anzeigen** - Wenn diese Option deaktiviert ist, können Besuchende nicht ändern, ob die KI-Zusammenfassung angezeigt wird.
  * Der Standardwert ist aktiviert.
* **Generative Zusammenfassung standardmäßig anzeigen** - Mit dieser Option wird der Standardstatus des Umschalters „Besucherzugriff“ für die von KI generierte Zusammenfassung festgelegt.
  * Der Standardwert ist aktiviert.
* **GenSearch Error Fallback** - Definiert, wie sich die Suche verhalten soll oder fehlerhaft ist.
  * **Nur Ergebnisse (Fehler ausblenden)** - Wenn ein Fehler auftritt, werden nur die zurückgegebenen Ergebnisse angezeigt, nicht der Fehler und nicht die Schaltfläche „Erneut versuchen“. Dies ist der Standardwert.
  * **Fehler mit Wiederholen anzeigen** - Wenn ein Fehler auftritt, wird der Fehler mit der Schaltfläche „Wiederholen“ angezeigt.
  * **Nur Fehlermeldung anzeigen** - Wenn ein Fehler auftritt, nur die Fehlermeldung anzeigen, aber keine Ergebnisse.
