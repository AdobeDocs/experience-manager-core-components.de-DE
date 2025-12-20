---
title: E-Mail-Segmentierungskomponente
description: Die E-Mail-Segmentierungskomponente
role: Architect, Developer, Admin, User
exl-id: 6c88b8c5-189a-40c0-ab28-04d37dc5fbac
index: false
source-git-commit: eb77567dc32cccb81a9fc131493d11fb55b7e93b
workflow-type: ht
source-wordcount: '0'
ht-degree: 100%

---


# E-Mail-Segmentierungskomponente {#email-segmentation-component}

Die E-Mail-Segmentierungskomponente verwendet Variablen von Adobe Campaign, um abhängig vom Empfänger bzw. von der Empfängerin Inhalte anzuzeigen oder auszublenden.

## Verwendung {#usage}

Mit der E-Mail-Segmentierungskomponente kann der Inhaltsautor bzw. die Inhaltsautorin Inhalte auf der Basis von Bedingungen ausblenden oder anzeigen, die von Variablen zu den von Adobe Campaign bereitgestellten Empfangenden erfüllt werden. Auf diese Weise sehen die Empfangenden Inhalte, die auf ihrer Segmentierung basieren.

* Der Vorlagenautor bzw. die Vorlagenautorin kann das [Dialogfeld „Design“](#design-dialog) verwenden, um zu definieren, welche Komponenten als Segment hinzugefügt werden können.
* Der Inhaltsautor bzw. die Inhaltsautorin kann das [Dialogfeld „Konfigurieren“](#configure-dialog) verwenden, um Komponenten als Segmente hinzuzufügen, und konfigurieren, welche Segmente basierend auf Adobe Campaign-Variablen angezeigt werden.

Als Alternative zur Verwendung des Dialogs „Konfigurieren“ kann der Inhaltsautor bzw. die Inhaltsautorin nach dem Hinzufügen der E-Mail-Segmentierungskomponente zu einer Inhaltsseite zusätzliche Komponenten per Drag-and-Drop in die E-Mail-Segmentierungskomponente ziehen, um neue Segmente zu erstellen.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der E-Mail-Segmentierungs-Komponente ist v1. Sie wurde mit dem Release X der E-Mail-Kernkomponenten im Oktober 2022 eingeführt und wird in diesem Dokument beschrieben.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|---|---|---|---|
| v1 | Kompatibel | – | – |

### Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur E-Mail-Teaser-Komponente [finden Sie auf GitHub](https://adobe.com/go/aem_cmp_tech_email_segmentation_v1_de).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Im Dialogfeld „Konfigurieren“ kann der Inhaltsautor bzw. die Inhaltsautorin Segmente erstellen, umbenennen und neu anordnen sowie das aktive Segment definieren. In der E-Mail-Segmentierungskomponente ist ein Segment einfach eine weitere Komponente, die angezeigt oder ausgeblendet wird, je nachdem ob ein Empfänger bzw. eine Empfängerin bestimmte Bedingungen erfüllt oder nicht. Sie ist vergleichbar mit der [Kernkomponenten-Registerkarte „Komponenten“](/help/components/tabs.md), nur dass in der Segmentierungskomponente wird nur der Inhalt der Registerkarte angezeigt, deren Bedingungen erfüllt werden.

### Registerkarte „Elemente“ {#items-tab}

![Registerkarte „Dialogelemente konfigurieren“ der E-Mail-Segmentierungskomponente](/help/email/assets/email-segmentation-configure-items.png)

Verwenden Sie die Schaltfläche **Segment hinzufügen**, um die Komponentenauswahl zu öffnen und dort auszuwählen, welche Komponente als Segment hinzugefügt werden soll. Nach dem Hinzufügen wird der Liste ein Eintrag hinzugefügt, der die folgenden Elemente enthält:

* **Symbol** – Das Symbol des Komponententyps des Segments zur einfachen Identifizierung in der Liste. Bewegen Sie den Mauszeiger darüber, um den vollständigen Komponentennamen als QuickInfo zu sehen.
* **Bedingung** – Die Bedingung, die erfüllt sein muss, damit dieses Segment dem Empfänger bzw. der Empfängerin des Inhalts angezeigt wird.
   * Die verfügbaren Bedingungen werden im [Dialogfeld „Design“](#design-dialog) definiert.
   * **Standard** – Definiert das Standardsegment, das angezeigt wird, wenn keine anderen Bedingungen erfüllt sind
   * **Benutzerdefiniert** – Ermöglicht dem Autor bzw. der Autorin die Definition einer Bedingung
      * Die Bedingungen basieren auf Adobe Campaign-Personalisierungsvariablen.
      * [Hier finden Sie Adobe Campaign Standard-Personalisierungsressourcen.](https://experienceleague.adobe.com/docs/campaign-standard/using/designing-content/personalization.html?lang=de)
      * [Hier finden Sie Adobe Campaign Classic-Personalisierungsressourcen.](https://experienceleague.adobe.com/docs/campaign-classic/using/sending-messages/personalizing-deliveries/personalization-fields.html?lang=de)
* **Entfernen** – Tippen oder klicken Sie darauf, um das Segment aus der E-Mail-Segmentierungskomponente zu löschen.
* **Neu anordnen** – Tippen oder klicken und ziehen Sie die Segmente, um sie neu anzuordnen.

>[!TIP]
>
>Wenn der Viewport des Inhalts so reduziert wird, dass das Bearbeitungsdialogfeld im Vollbild angezeigt wird, ist die Schaltfläche **Hinzufügen** ausgeblendet. Komponenten können der E-Mail-Segmentierungskomponente weiter hinzugefügt werden, indem [sie aus dem Komponenten-Browser gezogen und in der E-Mail-Segmentierungskomponente im Inhaltseditor abgelegt werden.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html?lang=de#inserting-a-component)

### Registerkarte „Eigenschaften“ {#properties-tab}

![Registerkarte „Eigenschaften“ im Dialogfeld „Konfigurieren“ der E-Mail Segmentierungskomponente](/help/email/assets/email-segmentation-configure-properties.png)

* **ID** – Diese Option ermöglicht das Festlegen der eindeutigen Kennung der Komponente in HTML.
   * Wenn das Feld leer bleibt, wird automatisch eine eindeutige ID generiert, den Sie im resultierenden Inhalt finden.
   * Sofern eine ID angegeben wird, ist vom Autor bzw. der Autorin sicherzustellen, dass diese eindeutig ist.
   * Die Änderung der ID kann sich auf CSS auswirken.

### Registerkarte „Erreichbarkeit“ {#accessibility-tab}

![Registerkarte „Ein-/Ausgabehilfe“ im Dialogfeld „Konfigurieren“ der E-Mail-Segmentierungkomponente](/help/email/assets/email-segmentation-configure-accessibility.png)

Auf der Registerkarte **Erreichbarkeit** können Werte für die [ARIA-Barrierefreiheits-Beschriftungen](https://www.w3.org/WAI/standards-guidelines/aria/) für die Komponente festgelegt werden.

* **Beschriftung** - Wert eines ARIA-Beschriftungs-Attributs für die Komponente

### Registerkarte „Arten“ {#styles-tab-edit}

Die E-Mail-Segmentierungskomponente unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).

Verwenden Sie das Dropdown-Menü, um die Stile auszuwählen, die Sie auf die Komponente anwenden möchten. Die im Dialogfeld „Bearbeiten“ vorgenommenen Auswahlen haben denselben Effekt wie die in der Komponenten-Symbolleiste ausgewählten.

Stile müssen für diese Komponente im [Dialogfeld „Design“](#design-dialog) konfiguriert werden, damit die Registerkarte verfügbar ist.

## Bedienfeld auswählen {#select-panel}

Der Inhaltsautor bzw. die Inhaltsautorin kann in der Komponenten-Symbolleiste die Option **Bedienfeld auswählen** verwenden, um zu einem anderen Segment zu wechseln und es zu bearbeiten oder die Reihenfolge der Segmente zu ändern.

![Symbol „Bedienfeld auswählen“](/help/email/assets/select-panel-icon.png)

Nachdem in der Komponenten-Symbolleiste die Option **Bedienfeld auswählen** ausgewählt wurde, werden die konfigurierten Registerkarten als Dropdown-Liste angezeigt.

* Die Liste ist nach der zugewiesenen Anordnung der Segmente geordnet, was sich auch in der Nummerierung zeigt.
* Der Komponententyp des Segments wird zuerst angezeigt, gefolgt von der Beschreibung des Segments in hellerer Schriftart.

![Popover „Bedienfeld auswählen“](/help/email/assets/select-panel-popover.png)

* Durch Tippen oder Klicken auf einen Eintrag in der Dropdown-Liste wechselt die Ansicht im Editor zu diesem Segment.
* Die Segmente können direkt mithilfe der Ziehgriffe neu angeordnet werden.

>[!NOTE]
>
>Segmente werden im Seiteneditor als Registerkarten gerendert, sodass ersichtlich ist, dass mehrere Optionen für den endgültigen Inhalt vorhanden sind. Diese Registerkarten können vom Autor bzw. der Autorin nicht im Seiteneditor ausgewählt werden. Verwenden Sie das Auswahlfeld, um zwischen den angezeigten Segmenten zu wechseln.

## Dialogfeld „Design“ {#design-dialog}

Im Dialogfeld „Design“ kann der Vorlagenautor bzw. die Vorlagenautorin definieren, welche Komponenten als Segmente zur E-Mail-Segmentierungskomponente hinzugefügt werden können. Außerdem kann er festlegen, welche benutzerdefinierten Stile dem Inhaltsautor bzw. der Inhaltsautorin zur Verfügung stehen.

### Registerkarte „Zugelassene Komponenten“ {#allowed-components-tab}

In der Registerkarte **Zugelassene Komponenten** können Sie definieren, welche Komponenten der Inhaltsautor bzw. die Inhaltsautorin zur E-Mail-Segmentierungskomponente hinzufügen kann.

Die Registerkarte **Zugelassene Komponenten** funktioniert auf die gleiche Weise wie die namensgleiche Registerkarte, wenn im Vorlageneditor [die Richtlinie und die Eigenschaften eines Layout-Containers definiert werden](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=de).

### Registerkarte „Arten“ {#styles-tab}

Die E-Mail-Segmentierungskomponente unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).

### Registerkarte „Definierte Bedingungen“ {#defined-conditions}

Mit der Verwendung der Registerkarte **Definierte Bedingungen** kann der Vorlagen-Editor festlegen, welche Bedingungen dem Inhaltsautor bzw. der Inhaltsautorin beim Erstellen von Segmenten zur Verfügung stehen.

![Registerkarte „Definierte Bedingungen“ des Dialogfelds „Design“](/help/email/assets/email-segmentation-design-defined-conditions.png)

Tippen oder klicken Sie auf die **Hinzufügen**-Schaltfläche, um neue Bedingungen zu erstellen.

* **Name der Segmentbedingung** – Eine Beschreibung der Bedingung
* **Segmentbedingung** – Die tatsächliche Bedingung, die basierend auf Adobe Campaign-Personalisierungsvariablen erfüllt werden muss
   * [Hier finden Sie Adobe Campaign Standard-Personalisierungsressourcen.](https://experienceleague.adobe.com/docs/campaign-standard/using/designing-content/personalization.html?lang=de)
   * [Hier finden Sie Adobe Campaign Classic-Personalisierungsressourcen.]&#x200B;(https://experienceleague.adobe.com/docs/?lang=de
* **Entfernen** – Tippen oder klicken Sie, um die Bedingung zu entfernen
* **Neu anordnen** – Tippen oder klicken und ziehen Sie die Bedingungen, um ihre Reihenfolge neu anzuordnen
