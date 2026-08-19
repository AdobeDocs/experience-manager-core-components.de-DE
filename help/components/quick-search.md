---
title: Schnellsuch-Komponente
description: Die Schnellsuch-Komponente bietet Suchfunktionen für eine Website und zeigt Suchergebnisse an, damit Besucher die Website durchsuchen und die Ergebnisse filtern können, optional unter Verwendung der KI-gestützten semantischen Suche über den Umschalter für die semantische Suche .
role: Developer, Admin, User
exl-id: fc40ce1d-e69a-4a40-853e-67a37228271b
TQID: https://experienceleague.adobe.com/wU-3pacdEz9ne8b53-mKJy-XxRdyz2gu4Jvj-yFgGOw
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: e2c1b6d3-bb7e-4fe8-8c72-f7b403298e91
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
source-git-commit: f939ce7498d9ec1901bea4b5fbf631365ba923fa
workflow-type: tm+mt
source-wordcount: 909
ht-degree: 41%

---


# Schnellsuch-Komponente {#quick-search-component}

Die Schnellsuch-Komponente bietet Suchfunktionen für eine Website und zeigt Suchergebnisse an, damit Besucher mühelos übereinstimmende Inhalte finden und Ergebnisse anzeigen können.

{{traditional-aem}}

## Nutzung {#usage}

Die Schnellsuch-Komponente bietet Site-Besuchern die Möglichkeit, nach Inhalten zu suchen, die Ergebnisse unmittelbar anzuzeigen und leicht zu den passenden Seiten zu navigieren. Neue Ergebnisse werden dynamisch abgerufen, wenn der Benutzer die Suchergebnisse durchblättert.

Mit [&#x200B; Dialogfeld „Bearbeiten](#edit-dialog) kann der Inhaltsautor definieren, wo in der Inhaltsstruktur die Suche beginnen soll, und optional den Umschalter Semantische Suche ausblenden. Mit dem [Design-](#design-dialog) kann der Vorlagenautor den Standardwert festlegen, an dem in der Inhaltsstruktur die Suche beginnen soll, die maximale Ergebnissatzgröße, die minimale Suchbegrifflänge und ob der Umschalter für die semantische Suche standardmäßig für Besuchende angezeigt wird.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Schnellsuch-Komponente ist v3, die mit [Version 2.32.0](/help/versions.md) der Kernkomponenten eingeführt wurde, wobei ein optionaler Umschalter für die semantische Suche hinzugefügt wurde, und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |--- |---|---|
| v3 | – | Kompatibel* | Kompatibel* | Kompatibel |
| [v2](/help/components/v2/quick-search.md) | – | Kompatibel | Kompatibel | Kompatibel |
| [v1](/help/components/v1/quick-search.md) | Kompatibel mit<br>[Version 2.17.4](/help/versions.md) und vorherigen | Kompatibel | – | Kompatibel |

*Der Umschalter Semantische Suche ist nur bei AEM as a Cloud Service verfügbar.

Weitere Informationen zu Kernkomponentenversionen und -freigaben finden Sie im Dokument [Kernkomponentenversionen.](/help/versions.md)

## Musterkomponentenausgabe {#sample-component-output}

Um die Schnellsuch-Komponente kennenzulernen und Beispiele für die Konfigurationsoptionen sowie die HTML- und JSON-Ausgabe zu sehen, besuchen Sie die [Komponentenbibliothek.](https://adobe.com/go/aem_cmp_library_search)

## Technische Details {#technical-details}

>[!NOTE]
>
>Der Schutz der Suchkomponente oder einer beliebigen AEM-basierten Anwendung gegen DOS-Angriffe sollte auf höherer Ebene implementiert werden, z. B. durch Verwendung von `mod_security` auf dem Dispatcher.

Die aktuelle technische Dokumentation zur Schnellsuch-Komponente [finden Sie auf GitHub.](https://adobe.com/go/aem_cmp_tech_search_v3)

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Dialogfeld „Bearbeiten“ {#edit-dialog}

Im Dialogfeld „Bearbeiten“ kann der Inhaltsautor definieren, wo in der Inhaltsstruktur die Suche beginnen soll, und optional den Umschalter Semantische Suche ausblenden.

![Dialogfeld „Bearbeiten“ der Schnellsuch-Komponente](/help/assets/quick-search-edit-v3.png)

**Suchstamm** - Die Stammseite, von der aus die Suche gestartet werden soll. Der Suchstamm kann ein Blueprint-Master, ein Sprachen-Master oder eine normale Seite sein.
* **ID** – Diese Option dient zur Kontrolle der eindeutigen Kennung der Komponente in der HTML-Datei und in der [Datenschicht](/help/developing/data-layer/overview.md).
  * Wenn Sie das Feld leer lassen, wird automatisch eine eindeutige ID generiert, die Sie über die resultierende Seite finden.
  * Sofern eine ID angegeben wird, ist vom Autor bzw. der Autorin sicherzustellen, dass diese eindeutig ist.
  * Änderungen der ID können sich auf das CSS-, JS- und Datenschicht-Tracking auswirken.
* **Umschalter für die semantische Suche in dieser Instanz ausblenden** - Wenn diese Option aktiviert ist, wird der Umschalter für die semantische Suche ausgeblendet, unabhängig davon, wie [&#x200B; Dialogfeld „Design](#design-dialog) konfiguriert ist, um es anzuzeigen.
  * Deaktivieren Sie diese Option, um die Standardeinstellung der Vorlage zu verwenden.
  * Diese Option kann den Umschalter nicht zwingen, auf einer Platzierung anzuzeigen, auf der das Dialogfeld „Design“ ihn ausblendet.

>[!NOTE]
>
>Wenn der **Suchstamm** nicht konfiguriert ist oder nicht aufgelöst werden kann, sucht die Schnellsuche standardmäßig unterhalb der aktuellen Seite.

>[!NOTE]
>
>Der Umschalter für die semantische Suche gibt nur dann KI-gestützte Ergebnisse zurück, wenn die Umgebung mit AEM Content AI konfiguriert ist. In AEM 6.5- und AEM 6.5 LTS-Umgebungen, die nicht mit Content-KI konfiguriert sind, blenden Sie den Umschalter [mithilfe des Design-](#design-dialog)) aus, damit Besuchenden kein Suchmodus angeboten wird, der nicht funktioniert.

## Dialogfeld „Design“ {#design-dialog}

Im Dialogfeld „Design“ kann der Vorlagenautor den Standardwert festlegen, an dem die Suche in der Inhaltsstruktur beginnen soll, sowie eine maximale Ergebnissatzgröße, minimale Suchbegriffslänge und ob der Umschalter für die semantische Suche standardmäßig Besuchern angezeigt wird.

### Registerkarte „Eigenschaften“ {#properties-tab}

![Design-Dialog der Schnellsuch-Komponente](/help/assets/quick-search-design-v3.png)

* **Suchstamm** - Der Standardwert des Suchstamms, wenn ein Inhaltsautor die Schnellsuch-Komponente auf einer Inhaltsseite platziert
* **Ergebnisgröße** - Die maximale Anzahl der Ergebnisse, die von einer Suchanfrage abgerufen werden
* **Mindestlänge des Suchbegriffs** - Mindestlänge des Suchbegriffs, um die Suche zu starten
* **Umschalter für semantische Suche ausblenden** - Wenn diese Option aktiviert ist, wird der Umschalter **Semantische Suche**, der unter [Verwendung](#usage) beschrieben ist, Website-Besuchern nicht standardmäßig angezeigt, und die Komponente verhält sich wie [die v2-Komponente (nur Volltextsuche).](/help/components/v2/quick-search.md)
  * Standardmäßig deaktiviert.
  * Inhaltsautoren können dies auch für eine einzelne Schnellsuch-Komponente im [Bearbeiten“ überschreiben](#edit-dialog)

>[!NOTE]
>
>Der Umschalter für die semantische Suche gibt nur dann KI-gestützte Ergebnisse zurück, wenn die Umgebung mit AEM Content AI konfiguriert ist. In AEM 6.5- und AEM 6.5 LTS-Umgebungen, die nicht mit Content-KI konfiguriert sind, blenden Sie den Umschalter mithilfe des Design-Dialogfelds aus, damit Besuchenden kein Suchmodus angeboten wird, der nicht funktioniert.

>[!NOTE]
>
>**Die Größe der Ergebnisse** und die **Minimale Länge für Suchbegriff** können nur im Designmodus festgelegt werden und daher nur auf Vorlagenebene, d. h. Inhaltsautoren können diese Werte nicht ändern.

>[!CAUTION]
>
>**Die Größe der Ergebnisse** und die **Minimale Länge für Suchbegriff** können Auswirkungen auf die Leistung haben, wenn sie zu hoch oder zu niedrig eingestellt sind.

### Registerkarte „Arten“ {#styles-tab}

Die Komponente „Schnellsuche“ unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).
