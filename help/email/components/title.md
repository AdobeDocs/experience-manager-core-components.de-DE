---
title: E-Mail-Titelkomponente
description: Die E-Mail-Titelkomponente ist eine Komponente für Abschnittsüberschriften für Ihre E-Mails, die eine direkte Bearbeitung ermöglicht.
role: Architect, Developer, Admin, User
exl-id: f65b6973-bb36-406f-bbea-f85a23f5340b
source-git-commit: 91969e4956bef1a511b8d588d5290a7999bf86ec
workflow-type: tm+mt
source-wordcount: '596'
ht-degree: 100%

---


# E-Mail-Titelkomponente {#email-title-component}

Die E-Mail-Titelkomponente ist eine Komponente für Abschnittsüberschriften für Ihre E-Mails, die eine direkte Bearbeitung ermöglicht.

## Verwendung {#usage}

Die E-Mail-Titelkomponente soll als Titel oder Überschrift eines Abschnitts einer E-Mail verwendet werden.

* Die verfügbaren Überschriftenebenen können vom Vorlagenautor im [Dialogfeld „Design“](#design-dialog) definiert werden.
* Der Inhaltsautor kann aus verfügbaren Überschriftenebenen im [Dialogfeld „Bearbeiten“](#edit-dialog) auswählen.

Für zusätzlichen Komfort steht auch eine einfache direkte Bearbeitung des Überschriftentexts zur Verfügung.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Komponente E-Mail-Titel ist v1, die mit der Freigabe X der E-Mail-Kernkomponenten im Oktober 2022 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|---|---|---|---|
| v1 | Kompatibel | – | – |

Weitere Informationen zu Kernkomponentenversionen finden Sie im Dokument [E-Mail-Kernkomponentenversionen](/help/versions.md).

### Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur Titelkomponente [finden Sie auf GitHub](https://adobe.com/go/aem_cmp_tech_email_title_v1).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Dialogfeld „Bearbeiten“ {#edit-dialog}

Im Dialogfeld „Bearbeiten“ kann der Inhaltsautor den Titeltext definieren sowie die Überschriftenebene auswählen.

* **Titel** - Wenn leer, wird der Seitentitel verwendet
   * Klicken Sie auf das Kampagnensymbol, um das Dialogfeld [Adobe Campaign-Variable auswählen](/help/email/campaign-variables.md) zum Einfügen von dynamischen Inhalten aus Adobe Campaign zu öffnen.
* **Typ/Größe** - Definiert die Überschriftenebene des Titels
* **Verknüpfung** - Definiert den Inhalt, auf den der Titel verweist. Dies kann ein Pfad zu einer Inhaltsseite, eine externe URL oder ein Seitenanker sein.
   * Klicken Sie auf das Kampagnensymbol, um das Dialogfeld [Adobe Campaign-Variable auswählen](/help/email/campaign-variables.md) zum Einfügen von dynamischen Inhalten aus Adobe Campaign zu öffnen.
* **ID** - Diese Option ermöglicht die Steuerung der eindeutigen Kennung der Komponente in HTML.
   * Wenn Sie das Feld leer lassen, wird automatisch eine eindeutige ID generiert, die Sie über die resultierende Seite finden.
   * Sofern eine ID angegeben wird, ist vom Autor bzw. der Autorin sicherzustellen, dass diese eindeutig ist.
   * Die Änderung der ID kann sich auf CSS auswirken.

![Dialog E-Mail-Titelkomponente bearbeiten](/help/email/assets/email-title-edit.png)

Der Editor für die Bearbeitung im Kontext kann auch verwendet werden, um den Text der Titelkomponente zu bearbeiten.

![In-Kontext-Bearbeitung der Komponente E-Mail-Titel](/help/email/assets/email-title-edit-inline.png)

### Registerkarte „Arten“ {#styles-tab-edit}

Die Komponente E-Mail-Titel unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).

Verwenden Sie das Dropdown-Menü, um die Stile auszuwählen, die Sie auf die Komponente anwenden möchten. Die im Dialogfeld „Bearbeiten“ vorgenommenen Auswahlen haben denselben Effekt wie die in der Komponenten-Symbolleiste ausgewählten.

Stile müssen für diese Komponente im [Dialogfeld „Design“](#design-dialog) konfiguriert werden, damit das Dropdown-Menü zur Verfügung steht.

![Registerkarte „Arten“ im Dialogfeld „Bearbeiten“ der Titelkomponente](/help/email/assets/email-title-edit-styles.png)

## Dialogfeld „Design“ {#design-dialog}

Das Dialogfeld „Design“ ermöglicht es dem Vorlagenautor, die standardmäßige Überschriftenebene zu definieren, die Titelkomponenten bei der Erstellung durch Inhaltsautoren haben.

### Registerkarte „Größen“ {#sizes-tab}

![Dialogfeld „Design“ der Titelkomponente](/help/email/assets/email-title-design.png)

* **Zugelassene Typen/Größen für Autoren** - Aktiviert oder deaktiviert die Überschrifttypen, die für Inhaltsautoren verfügbar sind, wenn sie die E-Mail-Titelkomponente verwenden.
* **Standardtyp/Größe** - Definiert den Überschrifttyp, der automatisch zugewiesen wird, wenn ein Inhaltsautor die E-Mail-Titelkomponente zu einer Seite hinzufügt.
* **Link deaktivieren** - Deaktiviert die Unterstützung für Links in der E-Mail-Titelkomponente, um Inhaltsautoren das Verlinken von Titeln zu untersagen.

### Registerkarte „Arten“ {#styles-tab}

Die E-Mail-Titelkomponente unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).
