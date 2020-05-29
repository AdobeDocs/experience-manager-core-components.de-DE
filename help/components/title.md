---
title: Titelkomponente
description: Die Kernkomponente „Titelkomponente“ ist eine Komponente für Abschnittsüberschriften, die eine Bearbeitung im Kontext ermöglicht.
translation-type: tm+mt
source-git-commit: c186e9ec3944d785ab0376769cf7f2307049a809
workflow-type: tm+mt
source-wordcount: '558'
ht-degree: 84%

---


# Titelkomponente{#title-component}

Die Kernkomponente „Titelkomponente“ ist eine Komponente für Abschnittsüberschriften, die eine Bearbeitung im Kontext ermöglicht.

## Nutzung {#usage}

Die Titelkomponente soll als Titel oder Überschrift eines Inhaltsabschnitts verwendet werden. Die verfügbaren Überschriftenebenen können vom Vorlagenautor im [Dialogfeld „Design“](#design-dialog) definiert werden. Der Inhaltseditor kann aus verfügbaren Überschriftenebenen im [Dialogfeld „Bearbeiten“](#edit-dialog) auswählen. Für zusätzlichen Komfort steht auch eine einfache direkte Bearbeitung des Überschriftentexts zur Verfügung.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Titelkomponente ist v2, die mit Version 2.0.0 der Kernkomponenten im Januar 2018 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.3 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|---|---|
| v2 | - | Kompatibel | Kompatibel | Kompatibel |
| [v1](v1/title-v1.md) | Kompatibel | Kompatibel | Kompatibel | - |

Weitere Informationen zu Kernkomponentenversionen und -freigaben finden Sie in den [Kernkomponentenversionen](/help/versions.md).

## Musterkomponentenausgabe {#sample-component-output}

Um die Titelkomponente sowie Beispiele für die Konfigurationsoptionen sowie HTML- und JSON-Ausgaben zu erhalten, besuchen Sie die [Komponentenbibliothek](https://adobe.com/go/aem_cmp_library_title).

### Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur Titelkomponente [finden Sie auf GitHub](https://adobe.com/go/aem_cmp_tech_title_v2).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Dialogfeld „Bearbeiten“ {#edit-dialog}

Im Dialogfeld „Bearbeiten“ kann der Inhaltsautor den Titeltext definieren sowie die Überschriftenebene auswählen.

* **Titel** - Wenn leer, wird der Seitentitel verwendet
* **Typ/Größe** - Definiert die Überschriftenebene des Titels
* **Link** - Definiert den Inhalt, auf den der Titel verweist. Dies kann ein Pfad zu einer Inhaltsseite, eine externe URL oder ein Seitenanker sein.
* **ID** - Diese Option ermöglicht die Steuerung des eindeutigen Bezeichners der Komponente im HTML und in der [Datenschicht](/help/developing/data-layer/overview.md).
   * Wenn Sie das Feld leer lassen, wird automatisch eine eindeutige ID generiert und Sie können die resultierende Seite überprüfen.
   * Wenn eine ID angegeben wird, muss der Autor sicherstellen, dass sie eindeutig ist.
   * Eine Änderung der ID kann sich auf die Verfolgung von CSS, JS und Datenschichten auswirken.

![Dialogfeld &quot;Bearbeiten&quot;der Titelkomponente](/help/assets/title-edit.png)

>[!NOTE]
>
>Die Möglichkeit, einen Link für den Titel zu definieren, wurde mit Version 2.2.0 der Kernkomponenten eingeführt.

Der Editor für die Bearbeitung im Kontext kann auch verwendet werden, um den Text der Titelkomponente zu bearbeiten.

![Ersetzende Bearbeitung der Titelkomponente](/help/assets/title-edit-inline.png)

## Dialogfeld „Design“ {#design-dialog}

Das Dialogfeld „Design“ ermöglicht es dem Vorlagenautor, die standardmäßige Überschriftenebene zu definieren, die Titelkomponenten bei der Erstellung durch Inhaltsautoren haben.

### Registerkarte „Größen“{#sizes-tab}

![Entwurfsdialogfeld der Titelkomponente](/help/assets/title-design.png)

* **Zulässige Typen/Größen für Autoren** - Aktiviert oder deaktiviert die Überschrifttypen, die für Inhaltsautoren verfügbar sind, wenn sie die Titelkomponente verwenden.
* **Standardtyp/-größe** - Definieren Sie den Überschrifttyp, der automatisch zugewiesen wird, wenn ein Inhaltsautor die Titelkomponente zu einer Seite hinzufügt.
* **Link deaktivieren** - Deaktiviert die Unterstützung für Links in der Titelkomponente, um Inhaltsautoren zu verbieten, von Titeln zu verlinken.

>[!NOTE]
>
>Die Möglichkeit, einen Link für den Titel zu definieren, wurde mit Version 2.2.0 der Kernkomponenten eingeführt.

### Registerkarte „Stile“ {#styles-tab}

Die Titelkomponente unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).
