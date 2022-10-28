---
title: E-Mail-Container-Komponente
description: Die E-Mail-Container-Komponente ermöglicht die Erstellung eines Containers für mehrere zusätzliche Komponenten in Ihrem E-Mail-Inhalt.
role: Architect, Developer, Admin, User
hidefromtoc: true
index: false
source-git-commit: 8bebe3ca036557f3f7c6b8ec0e65d6d104d5ffae
workflow-type: tm+mt
source-wordcount: '835'
ht-degree: 38%

---


# E-Mail-Container-Komponente {#email-container-component}

Die E-Mail-Container-Komponente ermöglicht die Erstellung eines Containers für mehrere zusätzliche Komponenten in Ihrem E-Mail-Inhalt.

## Nutzung {#usage}

Die E-Mail-Container-Komponente ermöglicht die Erstellung eines Containers für mehrere zusätzliche Komponenten in Ihrem E-Mail-Inhalt und kann verwendet werden, um andere Komponenten zu gruppieren und einen gemeinsamen Stil oder ein gemeinsames Layout anzuwenden.

* Die Eigenschaften des Containers können im [Dialogfeld &quot;Konfigurieren&quot;.](#configure-dialog)
* Standardwerte für die E-Mail-Container-Komponente können beim Hinzufügen zu einer Seite im Abschnitt [Dialogfeld &quot;Design&quot;.](#design-dialog)

Nachdem einer Seite eine E-Mail-Container-Komponente hinzugefügt wurde, kann ein Inhaltsautor zusätzliche Komponenten per Drag &amp; Drop in die Seite ziehen.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der E-Mail-Container-Komponente ist v1, die mit Version X der E-Mail-Kernkomponenten im Oktober 2022 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|
| v1 | Kompatibel | Kompatibel |

Weitere Informationen zu E-Mail-Kernkomponentenversionen und -freigaben finden Sie im Dokument [Versionen der E-Mail-Kernkomponenten.](/help/email/versions.md)

## Musterkomponentenausgabe {#sample-component-output}

Um die E-Mail-Container-Komponente zu erleben und Beispiele für ihre Konfigurationsoptionen sowie HTML- und JSON-Ausgaben zu sehen, besuchen Sie die [Komponentenbibliothek.](https://adobe.com/go/aem_cmp_library_email_container)

## Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur Container-Komponente [finden Sie auf GitHub.](https://adobe.com/go/aem_cmp_tech_email_container_v1)

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler.](/help/developing/overview.md)

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Das Dialogfeld &quot;Konfigurieren&quot;ermöglicht es dem Inhaltsautor, das Container-Element und sein Verhalten und Aussehen in Ihrem Inhalt zu definieren.

![Dialogfeld &quot;Bearbeiten&quot;der E-Mail-Container-Komponente](/help/email/assets/email-container-configure.png)

* **Layout** - Diese Option definiert das Verhalten oder das Layout-Verhalten der E-Mail-Container-Komponente.
   * **volle Breite**
   * **half|half**
   * **one-third|two-third**
   * **two-third|one-third**
   * **third|third|third|third**
* **Hintergrundfarbe** - Definierbar entweder als freie RGB-Werte oder mithilfe der Farbauswahl, [je nach Konfiguration](#container-settings-tab).
* **Hintergrundbild** - Definiert ein Hintergrundbild für den Container, [je nach Konfiguration](#container-settings-tab)
* **ID** - Diese Option ermöglicht die Steuerung der eindeutigen Kennung der Komponente im HTML.
   * Wenn Sie das Feld leer lassen, wird automatisch eine eindeutige ID generiert, die Sie durch Überprüfen des resultierenden Inhalts finden können.
   * Sofern eine ID angegeben wird, ist vom Autor sicherzustellen, dass diese eindeutig ist.
   * Eine Änderung der ID kann sich auf CSS auswirken.

### Registerkarte „Stile“ {#styles-tab-edit}

Die E-Mail-Container-Komponente unterstützt die AEM [Stilsystem.](/help/get-started/authoring.md#component-styling)

Verwenden Sie das Dropdown-Menü, um die Stile auszuwählen, die Sie auf die Komponente anwenden möchten. Die im Dialogfeld „Bearbeiten“ vorgenommenen Auswahlen haben denselben Effekt wie die in der Komponenten-Symbolleiste ausgewählten.

Stile müssen für diese Komponente im [Dialogfeld &quot;Design&quot;](#design-dialog) , damit die Registerkarte verfügbar ist.

## Dialogfeld „Design“ {#design-dialog}

Im Dialogfeld &quot;Design&quot;kann der Vorlagenautor die Optionen definieren, die dem Inhaltsautor zur Verfügung stehen, der die E-Mail-Container-Komponente verwendet.

### Registerkarte „Zugelassene Komponenten“ {#allowed-components-tab}

Die **Zugelassene Komponenten** wird verwendet, um zu definieren, welche Komponenten der E-Mail-Container-Komponente vom Inhaltsautor als Elemente hinzugefügt werden können.

Die **Zugelassene Komponenten** tab funktioniert genauso wie die Registerkarte mit demselben Namen, wenn [Definieren der Richtlinie und Eigenschaften eines Layout-Containers im Vorlageneditor.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=de)

### Registerkarte „Standardkomponenten“ {#default-components-tab}

Die **Standardkomponenten** -Registerkarte wird verwendet, um zu definieren, welche Komponente der Komponente hinzugefügt wird, wenn ein bestimmter Asset-Typ im Container abgelegt wird, ähnlich wie bei [wie Standardkomponenten in der Seitenvorlage definiert werden.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html)

### Registerkarte &quot;Container Settings&quot; {#container-settings-tab}

Die **Container-Einstellungen** definiert, ob der Autor ein Hintergrundbild oder eine Hintergrundfarbe definieren kann.

![Registerkarte &quot;Container Settings&quot;im Dialogfeld &quot;Design&quot;der E-Mail-Container-Komponente](/help/email/assets/email-container-design-container-settings.png)

* **Hintergrundbild**
   * **Hintergrundbild aktivieren** - Wählen Sie diese Option, um dem Inhaltsautor die Möglichkeit zu bieten, ein Hintergrundbild für den Container zu definieren.
* **Hintergrundfarbe**
   * **Hintergrundfarbe aktivieren** - Wählen Sie diese Option, um dem Inhaltsautor die Möglichkeit zu bieten, eine Hintergrundfarbe für den Container zu definieren.
   * **Nur Farbmuster** - Wählen Sie diese Option, um dem Inhaltsautor nur die Auswahl aus vordefinierten Farbmustern für die Container-Hintergrundfarbe zu ermöglichen.
      * Nur verfügbar, wenn die Option **Hintergrundfarbe aktivieren** ausgewählt ist
* **Zulässige Farbfelder** - Definieren Sie vordefinierte Farben, aus denen der Inhaltsautor die Hintergrundfarbe des Containers auswählen kann
   * Verwenden Sie die Schaltfläche **Hinzufügen**, um ein vordefiniertes Farbmuster hinzuzufügen. Nach dem Hinzufügen wird der Liste ein Eintrag hinzugefügt, der die folgenden Spalten enthält:
   * **Wert** - Definieren Sie die Farbe manuell über RGB-Werte.
      * Tippen oder klicken Sie auf die Farbauswahl, um eine Farbe leichter auszuwählen, indem Sie einzelne RGB-Werte anpassen oder einen hexadezimalen Wert definieren.
   * **Löschen** - Tippen oder klicken Sie, um ein Muster zu löschen.
   * **Neu anordnen** - Tippen oder klicken und ziehen Sie, um die Muster neu anzuordnen.

### Registerkarte „Stile“ {#styles-tab}

Die E-Mail-Container-Komponente unterstützt die AEM [Stilsystem.](/help/get-started/authoring.md#component-styling)