---
title: Inhaltskomponente
description: Die Inhaltsverzeichniskomponente erstellt ein "ToC", das auf den Titeln im Seiteninhalt basiert und es Ihren Lesern ermöglicht, schnell auf der Seite zu navigieren.
role: Architect, Developer, Admin, User
exl-id: 006adde2-ebff-4e74-8e79-325cccd43e8f
source-git-commit: 394a8b968d7bcde7e766ed719c5914ec5cb60744
workflow-type: tm+mt
source-wordcount: '759'
ht-degree: 22%

---

# Inhaltskomponente {#table-of-contents-component}

Die Inhaltsverzeichniskomponente erstellt ein &quot;ToC&quot;, das auf den Titeln im Seiteninhalt basiert und es Ihren Lesern ermöglicht, schnell auf der Seite zu navigieren.

## Nutzung {#usage}

Die Komponente &quot;Inhaltsverzeichnis&quot;bietet Site-Besuchern die Möglichkeit, schnell durch den Inhalt Ihrer Seite durch ein effizient generiertes Inhaltsverzeichnis zu navigieren, das auf den Titeln des Seiteninhalts basiert.

* Das ToC wird serverseitig generiert.
* Er wird vollständig vom Dispatcher zwischengespeichert, um eine schnelle Bereitstellung zu ermöglichen.
* Es funktioniert mit allen Komponenten auf der Seite, nicht nur mit den Kernkomponenten.

Die [Dialogfeld &quot;Bearbeiten&quot;](#edit-dialog) ermöglicht es dem Inhaltsautor, den Bereich der Titel zu definieren, die in der ToC verwendet werden sollen. Verwenden der [Dialogfeld &quot;Design&quot;](#design-dialog)kann der Vorlagenautor den Standardwert für die Titel festlegen, wenn ein Inhaltsautor einer Seite eine Inhaltsverzeichniskomponente hinzufügt und die in der Inhaltsdatei enthaltenen Titel auf der Grundlage von Klassennamen beschränkt.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Inhaltsverzeichniskomponente ist v1, die mit Version 2.20.0 der Kernkomponenten im Mai 2022 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|
| v1 | Kompatibel | Kompatibel |

Weitere Informationen zu Kernkomponentenversionen und -freigaben finden Sie in den [Kernkomponentenversionen](/help/versions.md).

## Musterkomponentenausgabe {#sample-component-output}

Um die Inhaltsverzeichniskomponente zu erleben und Beispiele für die Konfigurationsoptionen sowie HTML- und JSON-Ausgaben zu sehen, besuchen Sie die [Komponentenbibliothek](https://adobe.com/go/aem_cmp_library_tableofcontents).

### Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur Inhaltskomponente [finden Sie auf GitHub](https://adobe.com/go/aem_cmp_tech_tableofcontents_v1).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Dialogfeld „Bearbeiten“ {#edit-dialog}

Das Dialogfeld &quot;Bearbeiten&quot;ermöglicht es dem Inhaltsautor, die Bereiche der Titelebenen zu definieren, die die Inhaltskomponente als ToC rendern soll.

![Dialogfeld &quot;Bearbeiten&quot;der Inhaltskomponente](/help/assets/tableofcontents-edit.png)

**Listentyp** - Diese Option definiert, ob es sich bei der Liste um eine Liste mit Aufzählungszeichen oder eine nummerierte Liste handeln soll.
* **Titelstartstufe** - Diese Option definiert die höchste Ebene von Titeln, die die Inhaltskomponente rendern soll.
* **Titel-Stopp-Level** - Mit dieser Option wird die niedrigste Ebene von Titeln definiert, die die Inhaltskomponente rendern soll.
* **ID** – Diese Option dient zur Kontrolle der eindeutigen Kennung der Komponente in der HTML-Datei und auf der [Datenschicht](/help/developing/data-layer/overview.md).
   * Wenn Sie das Feld leer lassen, wird automatisch eine eindeutige ID generiert, die Sie über die resultierende Seite finden.
   * Sofern eine ID angegeben wird, ist vom Autor sicherzustellen, dass diese eindeutig ist.
   * Änderungen der ID können sich auf das CSS-, JS- und Datenschicht-Tracking auswirken.

## Dialogfeld „Design“ {#design-dialog}

Über das Dialogfeld &quot;Design&quot;kann der Vorlagenautor den Standardwert für den Titelbereich der Inhaltskomponente festlegen sowie die in der Inhaltsdatei enthaltenen Titel basierend auf Klassennamen einschränken.

### Registerkarte „Eigenschaften“ {#properties-tab}

![Dialogfeld „Design“ der Schnellsuch-Komponente](/help/assets/tableofcontents-design.png)

* **Listentyp beschränken** - Diese Option definiert den Listentyp, den die Komponente generiert. Durch Auswahl dieser Option wird die Möglichkeit des Inhaltsautors eingeschränkt, einen anderen Listentyp auszuwählen.
* **Einschränken der Startebene** - Diese Option definiert die höchste Titelebene, die der Inhaltsautor zum Definieren des ToC auswählen kann.
* **Beschränken der Stopp-Ebene** - Diese Option definiert die niedrigste Titelebene, die der Inhaltsautor zum Definieren des ToC auswählen kann.
* **Klassennamen einschließen** - Wenn diese Option festgelegt ist, werden nur Titel mit den angegebenen Klassennamen oder in Elementen der angegebenen Klassennamen in der Inhaltskomponente berücksichtigt.
   * Tippen oder klicken Sie auf **Hinzufügen** -Symbol, um einen oder mehrere Klassennamen hinzuzufügen.
   * Tippen oder klicken Sie auf **Löschen** neben einem Klassennamen klicken, um ihn zu löschen.
* **Klassennamen ignorieren** - Wenn diese Option festgelegt ist, werden Titel mit den angegebenen Klassennamen oder in Elementen der angegebenen Klassennamen von der Inhaltskomponente ignoriert.
   * Tippen oder klicken Sie auf **Hinzufügen** -Symbol, um einen oder mehrere Klassennamen hinzuzufügen.
   * Tippen oder klicken Sie auf **Löschen** neben einem Klassennamen klicken, um ihn zu löschen.

### Registerkarte „Arten“ {#styles-tab}

Die Inhaltsverzeichniskomponente unterstützt die AEM [Stilsystem](/help/get-started/authoring.md#component-styling).

## Adobe Client-Datenschicht {#data-layer}

Die Inhaltsverzeichniskomponente unterstützt die [Adobe Client-Datenschicht.](/help/developing/data-layer/overview.md)
