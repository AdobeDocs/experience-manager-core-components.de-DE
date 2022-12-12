---
title: E-Mail-Container-Komponente
description: Die E-Mail-Container-Komponente ermöglicht die Erstellung eines Containers für mehrere zusätzliche Komponenten in Ihrem E-Mail-Inhalt.
role: Architect, Developer, Admin, User
exl-id: 3b271e95-0093-4cb1-bb83-8446ba12a821
source-git-commit: 33976c0e745ad091a142109f70541f01a31edc5b
workflow-type: tm+mt
source-wordcount: '835'
ht-degree: 100%

---


# E-Mail-Container-Komponente {#email-container-component}

Die E-Mail-Container-Komponente ermöglicht die Erstellung eines Containers für mehrere zusätzliche Komponenten in Ihrem E-Mail-Inhalt.

## Verwendung {#usage}

Die E-Mail-Container-Komponente ermöglicht die Erstellung eines Containers für verschiedene zusätzliche Komponenten in Ihrem E-Mail-Inhalt und kann dazu verwendet werden, andere Komponenten zu gruppieren und einen gemeinsamen Stil bzw. ein gemeinsames Layout anzuwenden.

* Die Eigenschaften des Containers können im [Dialogfeld „Konfigurieren“](#configure-dialog) ausgewählt werden.
* Standardwerte für die E-Mail-Container-Komponente können beim Hinzufügen zu einer Seite im [Dialogfeld „Design“](#design-dialog) konfiguriert werden.

Nachdem einer Seite eine E-Mail-Container-Komponente hinzugefügt wurde, kann ein Inhaltsautor bzw. eine Inhaltsautorin zusätzliche Komponenten per Drag-and-Drop in die Seite ziehen.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der E-Mail-Container-Komponente ist v1. Sie wurde mit dem Release X der E-Mail-Kernkomponenten im Oktober 2022 eingeführt und wird in diesem Dokument beschrieben.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|
| v1 | Kompatibel | Kompatibel |

Weitere Informationen zu E-Mail-Kernkomponentenversionen und -Releases finden Sie im Dokument [E-Mail-Kernkomponentenversionen](/help/email/versions.md).

## Muster für Komponentenausgabe {#sample-component-output}

Um die E-Mail-Container-Komponente kennenzulernen und Beispiele für ihre Konfigurationsoptionen sowie HTML- und JSON-Ausgaben zu sehen, besuchen Sie die [Komponentenbibliothek](https://adobe.com/go/aem_cmp_library_email_container).

## Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur Container-Komponente [finden Sie auf GitHub](https://adobe.com/go/aem_cmp_tech_email_container_v1).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Der Dialog „Konfigurieren“ ermöglicht es dem Inhaltsautor bzw. der Inhaltsautorin, das Container-Element sowie sein Verhalten und Aussehen im Inhalt zu definieren.

![Dialogfeld „Bearbeiten der E-Mail-Container-Komponente“](/help/email/assets/email-container-configure.png)

* **Layout** – Mit dieser Option wird das Verhalten oder das Layout-Verhalten der E-Mail-Container-Komponente definiert.
   * **Volle Breite**
   * **halb|halb**
   * **eindrittel|zweidrittel**
   * **zweidrittel|eindrittel**
   * **drittel|drittel|drittel**
* **Hintergrundfarbe** – [Je nach Konfiguration](#container-settings-tab) definierbar entweder als freie RGB-Werte oder mithilfe des Farbwählers.
* **Hintergrundbild** – Definiert [je nach Konfiguration](#container-settings-tab) eine Hintergrundfarbe für den Container.
* **ID** – Diese Option ermöglicht das Festlegen der eindeutigen Kennung der Komponente in HTML.
   * Wenn das Feld leer bleibt, wird automatisch eine eindeutige ID generiert, den Sie im resultierenden Inhalt finden.
   * Sofern eine ID angegeben wird, ist vom Autor bzw. der Autorin sicherzustellen, dass diese eindeutig ist.
   * Die Änderung der ID kann sich auf CSS auswirken.

### Registerkarte „Arten“ {#styles-tab-edit}

Die E-Mail-Container-Komponente unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).

Verwenden Sie das Dropdown-Menü, um die Stile auszuwählen, die Sie auf die Komponente anwenden möchten. Die im Dialogfeld „Bearbeiten“ vorgenommenen Auswahlen haben denselben Effekt wie die in der Komponenten-Symbolleiste ausgewählten.

Stile müssen für diese Komponente im [Dialogfeld „Design“](#design-dialog) konfiguriert werden, damit das Dropdown-Menü zur Verfügung steht.

## Dialogfeld „Design“ {#design-dialog}

Das Dialogfeld „Design“ ermöglicht dem Vorlagenautor bzw. der Vorlagenautorin zu definieren, welche Optionen dem Inhaltsautor bzw. der Inhaltsautorin, der/die die E-Mail-Container-Komponente verwendet, zur Verfügung stehen.

### Registerkarte „Zugelassene Komponenten“ {#allowed-components-tab}

Über die Registerkarte **Zugelassene Komponenten** können Sie definieren, welche Komponenten der E-Mail-Container-Komponente vom Inhaltsautor bzw. von der Inhaltsautorin als Elemente hinzugefügt werden können.

Die Registerkarte **Zugelassene Komponenten** funktioniert auf die gleiche Weise wie die gleichnamige Registerkarte beim [Definieren der Richtlinie und der Eigenschaften eines Layout-Containers im Vorlageneditor](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=de).

### Registerkarte „Standardkomponenten“ {#default-components-tab}

Die Registerkarte **Standardkomponenten** wird verwendet, um zu definieren, welche Komponente zur Komponente hinzugefügt wird, wenn ein bestimmter Medientyp im Container abgelegt wird, und funktioniert ähnlich wie [die Definition von Standardkomponenten in der Seitenvorlage](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html).

### Registerkarte „Container-Einstellungen“ {#container-settings-tab}

Die Registerkarte **Container-Einstellungen** definiert, ob der Autor bzw. die Autorin ein Hintergrundbild oder eine Hintergrundfarbe definieren kann.

![Registerkarte „Container-Einstellungen“ im Dialogfeld „Design“ der E-Mail-Container-Komponente](/help/email/assets/email-container-design-container-settings.png)

* **Hintergrundbild**
   * **Hintergrundbild aktivieren** - Wählen Sie diese Option, um dem Inhaltsautor die Möglichkeit zu bieten, ein Hintergrundbild für den Container zu definieren.
* **Hintergrundfarbe**
   * **Hintergrundfarbe aktivieren** - Wählen Sie diese Option, um dem Inhaltsautor die Möglichkeit zu bieten, eine Hintergrundfarbe für den Container zu definieren.
   * **Nur Farbfelder** - Wählen Sie diese Option, um dem Inhaltsautor nur die Auswahl aus vordefinierten Farbmustern für die Container-Hintergrundfarbe zu ermöglichen.
      * Nur verfügbar, wenn die Option **Hintergrundfarbe aktivieren** ausgewählt ist
* **Zulässige Farbfelder** - Definieren Sie vordefinierte Farben, aus denen der Inhaltsautor die Hintergrundfarbe des Containers auswählen kann
   * Verwenden Sie die Schaltfläche **Hinzufügen**, um ein vordefiniertes Farbmuster hinzuzufügen. Nach dem Hinzufügen wird der Liste ein Eintrag hinzugefügt, der die folgenden Spalten enthält:
   * **Wert** - Definieren Sie die Farbe manuell über RGB-Werte.
      * Tippen oder klicken Sie auf die Farbauswahl, um eine Farbe leichter auszuwählen, indem Sie einzelne RGB-Werte anpassen oder einen hexadezimalen Wert definieren.
   * **Löschen** - Tippen oder klicken Sie, um ein Muster zu löschen.
   * **Neu anordnen** – Tippen oder klicken und ziehen Sie, um die Farbfelder neu anzuordnen.

### Registerkarte „Arten“ {#styles-tab}

Die Komponente „E-Mail-Container“ unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).
