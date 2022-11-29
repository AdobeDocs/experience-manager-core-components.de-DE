---
title: Komponente "Email Title"
description: Die Komponente "E-Mail-Titel"ist eine Komponente für Abschnittsüberschriften für E-Mails, die eine direkte Bearbeitung ermöglicht.
role: Architect, Developer, Admin, User
exl-id: f65b6973-bb36-406f-bbea-f85a23f5340b
source-git-commit: 33976c0e745ad091a142109f70541f01a31edc5b
workflow-type: tm+mt
source-wordcount: '636'
ht-degree: 51%

---


# Komponente &quot;Email Title&quot; {#email-title-component}

Die Komponente &quot;E-Mail-Titel&quot;ist eine Komponente für Abschnittsüberschriften für E-Mails, die eine direkte Bearbeitung ermöglicht.

## Nutzung {#usage}

Die Komponente &quot;E-Mail-Titel&quot;soll als Titel oder Überschrift eines Abschnitts einer E-Mail verwendet werden.

* Die verfügbaren Überschriftenebenen können vom Vorlagenautor im [Dialogfeld „Design“](#design-dialog) definiert werden.
* Der Inhaltsautor kann aus den verfügbaren Überschriftenebenen in der [Dialogfeld &quot;Bearbeiten&quot;.](#edit-dialog)

Für zusätzlichen Komfort steht auch eine einfache direkte Bearbeitung des Überschriftentexts zur Verfügung.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der E-Mail-Titelkomponente ist v1, die mit Version x der E-Mail-Kernkomponenten im Oktober 2022 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|
| v1 | Kompatibel | Kompatibel |

Weitere Informationen zu Kernkomponentenversionen und -versionen finden Sie im Dokument . [Kernversionen von E-Mail-Komponenten](/help/versions.md).

## Musterkomponentenausgabe {#sample-component-output}

Um die Titelkomponente sowie Beispiele für die Konfigurationsoptionen sowie HTML- und JSON-Ausgaben zu erhalten, besuchen Sie die [Komponentenbibliothek.](https://adobe.com/go/aem_cmp_library_email_title)

### Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur Titelkomponente [finden Sie auf GitHub](https://adobe.com/go/aem_cmp_tech_email_title_v1).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Dialogfeld „Bearbeiten“ {#edit-dialog}

Im Dialogfeld „Bearbeiten“ kann der Inhaltsautor den Titeltext definieren sowie die Überschriftenebene auswählen.

* **Titel** - Wenn leer, wird der Seitentitel verwendet
   * Klicken Sie auf das Kampagnensymbol , um die [Adobe Campaign-Variable auswählen](/help/email/campaign-variables.md) zum Einfügen von dynamischen Inhalten aus Adobe Campaign.
* **Typ/Größe** - Definiert die Überschriftenebene des Titels
* **Verknüpfung** - Definiert den Inhalt, auf den der Titel verweist. Dies kann ein Pfad zu einer Inhaltsseite, eine externe URL oder ein Seitenanker sein.
   * Klicken Sie auf das Kampagnensymbol , um die [Adobe Campaign-Variable auswählen](/help/email/campaign-variables.md) zum Einfügen von dynamischen Inhalten aus Adobe Campaign.
* **ID** - Diese Option ermöglicht die Steuerung der eindeutigen Kennung der Komponente im HTML.
   * Wenn Sie das Feld leer lassen, wird automatisch eine eindeutige ID generiert, die Sie über die resultierende Seite finden.
   * Sofern eine ID angegeben wird, ist vom Autor sicherzustellen, dass diese eindeutig ist.
   * Eine Änderung der ID kann sich auf CSS auswirken.

![Dialogfeld &quot;Bearbeiten&quot;der E-Mail-Titelkomponente](/help/email/assets/email-title-edit.png)

Der Editor für die Bearbeitung im Kontext kann auch verwendet werden, um den Text der Titelkomponente zu bearbeiten.

![Bearbeitung im Kontext der Komponente &quot;E-Mail-Titel&quot;](/help/email/assets/email-title-edit-inline.png)

### Registerkarte „Stile“ {#styles-tab-edit}

Die E-Mail-Titelkomponente unterstützt den AEM [Stilsystem.](/help/get-started/authoring.md#component-styling)

Verwenden Sie das Dropdown-Menü, um die Stile auszuwählen, die Sie auf die Komponente anwenden möchten. Die im Dialogfeld „Bearbeiten“ vorgenommenen Auswahlen haben denselben Effekt wie die in der Komponenten-Symbolleiste ausgewählten.

Stile müssen für diese Komponente im [Dialogfeld &quot;Design&quot;](#design-dialog) , damit das Dropdown-Menü verfügbar ist.

![Registerkarte „Arten“ im Dialogfeld „Bearbeiten“ der Titelkomponente](/help/email/assets/email-title-edit-styles.png)

## Dialogfeld „Design“ {#design-dialog}

Das Dialogfeld „Design“ ermöglicht es dem Vorlagenautor, die standardmäßige Überschriftenebene zu definieren, die Titelkomponenten bei der Erstellung durch Inhaltsautoren haben.

### Registerkarte „Größen“ {#sizes-tab}

![Dialogfeld „Design“ der Titelkomponente](/help/email/assets/email-title-design.png)

* **Zulässige Typen/Größen für Autoren** - Aktivieren oder deaktivieren Sie Überschrifttypen, die für Inhaltsautoren verfügbar sein werden, wenn sie die Komponente &quot;E-Mail-Titel&quot;verwenden.
* **Standardtyp/Größe** - Definieren Sie den Überschrifttyp, der automatisch zugewiesen wird, wenn ein Inhaltsautor die E-Mail-Titelkomponente zu einer Seite hinzufügt.
* **Link deaktivieren** - Deaktivieren Sie die Unterstützung für Links in der Komponente &quot;E-Mail-Titel&quot;, um Inhaltsautoren die Verknüpfung von Titeln zu verweigern.

### Registerkarte „Stile“ {#styles-tab}

Die E-Mail-Titelkomponente unterstützt den AEM [Stilsystem](/help/get-started/authoring.md#component-styling).
