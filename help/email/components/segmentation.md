---
title: E-Mail-Segmentierungskomponente
description: Die Komponente E-Mail-Segmentierung
role: Architect, Developer, Admin, User
hidefromtoc: true
index: false
source-git-commit: 8bebe3ca036557f3f7c6b8ec0e65d6d104d5ffae
workflow-type: tm+mt
source-wordcount: '1171'
ht-degree: 16%

---


# E-Mail-Segmentierungskomponente {#email-segmentation-component}

Die E-Mail-Segmentierungskomponente verwendet Variablen aus Adobe Campaign, um Inhalte basierend auf dem Empfänger des Inhalts anzuzeigen und auszublenden.

## Nutzung {#usage}

Mit der E-Mail-Segmentierungskomponente kann der Inhaltsautor Inhalte anhand von Bedingungen ausblenden und anzeigen, die von Variablen bezüglich des von Adobe Campaign bereitgestellten Empfängers erfüllt werden. Auf diese Weise sehen die Empfänger des Inhalts Inhalte basierend auf ihrer Segmentierung.

* Der Vorlagenautor kann die [Dialogfeld &quot;Design&quot;](#design-dialog) , um zu definieren, welche Komponenten als Segment hinzugefügt werden können.
* Der Inhaltsautor kann die [Dialogfeld konfigurieren](#configure-dialog) , um Komponenten als Segmente hinzuzufügen und zu konfigurieren, welche Segmente basierend auf Adobe Campaign-Variablen angezeigt werden.

Als Alternative zur Verwendung des Dialogfelds &quot;Konfigurieren&quot;kann der Inhaltsautor, sobald der Inhaltsautor die Komponente E-Mail-Segmentierung zu einer Inhaltsseite hinzugefügt hat, zusätzliche Komponenten per Drag &amp; Drop in die Komponenten für die E-Mail-Segmentierung ziehen, um neue Segmente zu erstellen.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der E-Mail-Segmentierungskomponente ist v1, die mit Version x der E-Mail-Kernkomponenten im Oktober 2022 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|
| v1 | Kompatibel | Kompatibel |

## Musterkomponentenausgabe {#sample-component-output}

Um die E-Mail-Segmentierungskomponente zu erleben und Beispiele für die Konfigurationsoptionen sowie HTML- und JSON-Ausgaben zu sehen, besuchen Sie die [Komponentenbibliothek.](https://adobe.com/go/aem_cmp_library_email_segmentation)

### Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur E-Mail-Teaser-Komponente [finden Sie auf GitHub.](https://adobe.com/go/aem_cmp_tech_email_segmentation_v1)

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler.](/help/developing/overview.md)

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Im Dialogfeld &quot;Konfigurieren&quot;kann der Inhaltsautor Segmente erstellen, umbenennen und neu anordnen sowie das aktive Segment definieren. In der Komponente E-Mail-Segmentierung ist ein Segment einfach eine andere Komponente, die basierend auf den vom Empfänger des Inhalts erfüllten Bedingungen ausgeblendet oder angezeigt wird. Sie können sie mit dem [Registerkartenkomponente &quot;Kernkomponenten&quot;](/help/components/tabs.md) In der Segmentierungskomponente wird jedoch nur der Inhalt der Registerkarte angezeigt, deren Bedingungen erfüllt sind.

### Registerkarte „Elemente“ {#items-tab}

![Registerkarte &quot;Elemente&quot;im Dialogfeld &quot;Konfigurieren&quot;der E-Mail-Segmentierungskomponente](/help/email/assets/email-segmentation-configure-items.png)

Verwenden Sie die **Segment hinzufügen** -Schaltfläche, um die Komponentenauswahl zu öffnen und auszuwählen, welche Komponente als Segment hinzugefügt werden soll. Nach dem Hinzufügen wird der Liste ein Eintrag hinzugefügt, der die folgenden Elemente enthält:

* **Symbol** - Das Symbol des Komponententyps des Segments zur einfachen Identifizierung in der Liste. Bewegen Sie den Mauszeiger darüber, um den vollständigen Komponentennamen als QuickInfo zu sehen.
* **Bedingung** - Die Bedingung, die erfüllt sein muss, damit dieses Segment dem Empfänger des Inhalts angezeigt wird.
   * Die verfügbaren Bedingungen werden im Abschnitt [Dialogfeld &quot;Design&quot;.](#design-dialog)
   * **Standard** - Definiert das Standardsegment, das angezeigt wird, wenn keine anderen Bedingungen erfüllt sind
   * **Benutzerdefiniert** - Ermöglicht es dem Autor, eine Bedingung zu definieren
      * Die Bedingungen basieren auf den Adobe Campaign-Personalisierungsvariablen
      * [Hier finden Sie Adobe Campaign Standard-Personalisierungsressourcen.](https://experienceleague.adobe.com/docs/campaign-standard/using/designing-content/personalization.html?)
      * [Hier finden Sie Adobe Campaign Classic-Personalisierungsressourcen.](https://experienceleague.adobe.com/docs/campaign-classic/using/sending-messages/personalizing-deliveries/personalization-fields.html)
* **Löschen** - Tippen oder klicken Sie, um das Segment aus der E-Mail-Segmentierungskomponente zu löschen.
* **Neu anordnen** - Tippen oder klicken und ziehen Sie, um die Segmente neu anzuordnen.

>[!TIP]
>
>Wenn der Viewport des Inhalts so reduziert wird, dass das Bearbeitungsdialogfeld im Vollbildmodus angezeigt wird, wird die **Hinzufügen** -Schaltfläche ausgeblendet. Komponenten können der E-Mail-Segmentierungskomponente weiterhin hinzugefügt werden durch [Ziehen Sie aus dem Komponenten-Browser und legen Sie die Komponente E-Mail-Segmentierung im Inhaltseditor ab.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html?lang=de#inserting-a-component)

### Registerkarte „Eigenschaften“ {#properties-tab}

![Registerkarte &quot;Eigenschaften&quot;im Dialogfeld &quot;Konfigurieren&quot;der E-Mail-Segmentierungskomponente](/help/email/assets/email-segmentation-configure-properties.png)

* **ID** - Diese Option ermöglicht die Steuerung der eindeutigen Kennung der Komponente im HTML.
   * Wenn Sie das Feld leer lassen, wird automatisch eine eindeutige ID generiert, die Sie durch Überprüfen des resultierenden Inhalts finden können.
   * Sofern eine ID angegeben wird, ist vom Autor sicherzustellen, dass diese eindeutig ist.
   * Eine Änderung der ID kann sich auf CSS auswirken.

### Registerkarte „Erreichbarkeit“ {#accessibility-tab}

![Registerkarte &quot;Barrierefreiheit&quot;im Dialogfeld &quot;Konfigurieren&quot;der E-Mail-Segmentierungskomponente](/help/email/assets/email-segmentation-configure-accessibility.png)

Auf der Registerkarte **Erreichbarkeit** können Werte für die [ARIA-Barrierefreiheits-Beschriftungen](https://www.w3.org/WAI/standards-guidelines/aria/) für die Komponente festgelegt werden.

* **Beschriftung** - Wert eines ARIA-Beschriftungs-Attributs für die Komponente

### Registerkarte „Arten“ {#styles-tab-edit}

Die E-Mail-Segmentierungskomponente unterstützt die AEM [Stilsystem.](/help/get-started/authoring.md#component-styling)

Verwenden Sie das Dropdown-Menü, um die Stile auszuwählen, die Sie auf die Komponente anwenden möchten. Die im Dialogfeld „Bearbeiten“ vorgenommenen Auswahlen haben denselben Effekt wie die in der Komponenten-Symbolleiste ausgewählten.

Stile müssen für diese Komponente im [Dialogfeld &quot;Design&quot;](#design-dialog) , damit die Registerkarte verfügbar ist.

## Bedienfeld auswählen {#select-panel}

Der Inhaltsautor kann die **Bedienfeld auswählen** in der Komponentensymbolleiste zu einem anderen Segment für die Bearbeitung wechseln und die Segmente einfach neu anordnen.

![Symbol „Bedienfeld auswählen“](/help/email/assets/select-panel-icon.png)

Nach Auswahl der **Bedienfeld auswählen** in der Komponenten-Symbolleiste werden die konfigurierten Segmente als Dropdown-Liste angezeigt.

* Die Liste wird nach der zugewiesenen Segmentanordnung geordnet und wird in der Nummerierung angezeigt.
* Der Komponententyp des Segments wird zuerst angezeigt, gefolgt von der Beschreibung des Segments in hellerer Schriftart.

![Popover „Bedienfeld auswählen“](/help/email/assets/select-panel-popover.png)

* Durch Tippen oder Klicken auf einen Eintrag in der Dropdown-Liste wird die Ansicht im Editor auf dieses Segment umgestellt.
* Die Segmente können mithilfe der Ziehpunkte an Ort und Stelle neu angeordnet werden.

>[!NOTE]
>
>Segmente werden im Seiteneditor als Registerkarten gerendert, um anzuzeigen, dass mehrere Optionen für den endgültigen Inhalt vorhanden sind. Diese Registerkarten können vom Autor im Seiteneditor nicht ausgewählt werden. Verwenden Sie das Auswahlfeld, um zwischen angezeigten Segmenten zu wechseln.

## Dialogfeld „Design“ {#design-dialog}

Im Dialogfeld &quot;Design&quot;kann der Vorlagenautor definieren, welche Komponenten der E-Mail-Segmentierungskomponente als Segmente hinzugefügt werden können, und definieren, welche benutzerdefinierten Stile dem Inhaltsautor zur Verfügung stehen.

### Registerkarte „Zugelassene Komponenten“ {#allowed-components-tab}

Die **Zugelassene Komponenten** wird verwendet, um zu definieren, welche Komponenten vom Inhaltsautor der E-Mail-Segmentierungskomponente als Segmente hinzugefügt werden können.

Die **Zugelassene Komponenten** tab funktioniert genauso wie die Registerkarte mit demselben Namen, wenn [Definieren der Richtlinie und Eigenschaften eines Layout-Containers im Vorlageneditor.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=de)

### Registerkarte „Stile“ {#styles-tab}

Die E-Mail-Segmentierungskomponente unterstützt die AEM [Stilsystem.](/help/get-started/authoring.md#component-styling)

### Registerkarte &quot;Definierte Bedingungen&quot; {#defined-conditions}

Verwenden der **Definierte Bedingungen** können Sie im Vorlagen-Editor festlegen, welche Bedingungen dem Inhaltsautor beim Erstellen von Segmenten zur Verfügung stehen.

![Registerkarte &quot;Designdialogfeld - Definierte Bedingungen&quot;](/help/email/assets/email-segmentation-design-defined-conditions.png)

Tippen oder klicken Sie auf **Hinzufügen** -Schaltfläche, um neue Bedingungen zu erstellen.

* **Name der Segmentbedingung** - Beschreibung der Bedingung
* **Segmentbedingung** - Die tatsächliche Bedingung, die basierend auf Adobe Campaign-Personalisierungsvariablen erfüllt werden muss
   * [Hier finden Sie Adobe Campaign Standard-Personalisierungsressourcen.](https://experienceleague.adobe.com/docs/campaign-standard/using/designing-content/personalization.html?)
   * [Hier finden Sie Adobe Campaign Classic-Personalisierungsressourcen.](https://experienceleague.adobe.com/docs/
* **Entfernen** - Tippen Sie auf , um auf zu klicken, um die Bedingung zu entfernen.
* **Neu anordnen** - Tippen oder klicken und ziehen Sie, um die Reihenfolge der Bedingungen neu anzuordnen.
