---
title: Registerkarten-Komponente
description: Die Registerkarten-Komponente ermöglicht die Erstellung mehrerer Registerkarten zum Anordnen von Inhalten auf einer Seite.
role: Architect, Developer, Admin, User
exl-id: 0031c5f3-447c-4932-898f-2f453801e492
source-git-commit: 6fbc781db555bc6abaed1d122a9a8756e3d53222
workflow-type: ht
source-wordcount: '1038'
ht-degree: 100%

---


# Registerkarten-Komponente {#tabs-component}

Die Kernkomponente Registerkarten-Komponente ermöglicht die Organisation von Inhalten auf mehrere Registerkarten.

## Nutzung {#usage}

Mit der Registerkarten-Komponente kann der Inhaltsautor Seiteninhalte über mehrere Registerkarten organisieren.

Im [Dialogfeld „Bearbeiten“](#edit-dialog) kann der Inhaltsautor mehrere Registerkarten definieren sowie die aktive Registerkarte festlegen. Mithilfe des [Dialogfelds „Design“](#design-dialog) kann der Vorlagenautor definieren, welche Komponenten zu Registerkarten hinzugefügt werden können, und die Stile anpassen.

>[!TIP]
>
>Verschachtelte Registerkarten-Komponenten (Registerkarten innerhalb Registerkarten) werden unterstützt.
>
>Einfache (nicht verschachtelte) Registerkarten-Komponenten können mithilfe des [Inhaltsbaums](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html?lang=de#content-tree) lokalisiert/ausgewählt werden, verschachtelte Registerkarten jedoch nicht.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Registerkarten-Komponente ist v1, die mit Version 2.2.0 der Kernkomponenten im Oktober 2018 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |--- |---|---|
| v1 | Kompatibel mit<br>[Version 2.17.4](/help/versions.md) und vorherigen | Kompatibel | Kompatibel | Kompatibel |

Weitere Informationen zu Kernkomponentenversionen und -freigaben finden Sie im Dokument [Kernkomponentenversionen](/help/versions.md).

## Musterkomponentenausgabe {#sample-component-output}

Um die Registerkarten-Komponente auszuprobieren sowie Beispiele für ihre Konfigurationsoptionen sowie HTML- und JSON-Ausgaben zu erhalten, besuchen Sie die [Komponentenbibliothek](https://adobe.com/go/aem_cmp_library_tabs_de).

### Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur Registerkarten-Komponente [finden Sie auf GitHub](https://adobe.com/go/aem_cmp_tech_tabs_v1_de).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Tiefe Verknüpfung mit einem Bedienfeld {#deep-linking}

Die Registerkarten-, [Karussell](carousel.md)- und [Akkordeon-Komponenten](accordion.md) unterstützen direkte Links zu einem Bedienfeld innerhalb der Komponente.

Gehen Sie hierfür wie folgt vor:

1. Zeigen Sie die Seite mit der Komponente über die Option **[Als veröffentlicht anzeigen](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html?lang=de#view-as-published)** im Seiteneditor an.
1. Überprüfen Sie den Inhalt der Seite und halten Sie die ID des Bedienfeldes fest.
   * Beispiel `id="accordion-86196c94d3-item-ca319dbb0b"`
1. Die ID wird der Anker, den Sie über einen Hash (`#`) an die URL anhängen können.
   * Beispiel `https://wknd.site/content/wknd/language-masters/en/magazine/western-australia.html#accordion-86196c94d3-item-ca319dbb0b`

Wird zu der URL mit der Bereichs-ID navigiert, scrollt der Browser direkt zur jeweiligen Komponente und zeigt das angegebene Bedienfeld an. Wenn das Bedienfeld so konfiguriert ist, dass es nicht standardmäßig eingeblendet wird, wird es automatisch eingeblendet.

## Registerkarte und responsives Design {#responsive-design}

Alle Kernkomponenten sind so konzipiert, dass sie vollständig responsiv sind und auf allen Geräten ein nahtloses Erlebnis bieten.

Einige erweiterte Komponenten wie die Registerkartenkomponente müssen möglicherweise im Kontext des Implementierungsprojekts besonders berücksichtigt werden, um unter allen Bedingungen Reaktionsschnelligkeit zu gewährleisten. Weitere Informationen finden Sie im Dokument [Responsives Design der Kernkomponenten](/help/responsive.md).

## Dialogfeld „Bearbeiten“ {#edit-dialog}

Im Dialogfeld „Bearbeiten“ kann der Inhaltsautor Registerkarten erstellen, umbenennen und neu anordnen sowie die aktive Registerkarte definieren.

### Registerkarte „Elemente“ {#items-tab}

![Registerkarte „Bearbeiten“ im Dialogfeld „Elemente“ der Registerkarten-Komponente](/help/assets/tabs-edit-items.png)

Verwenden Sie die Schaltfläche **Hinzufügen**, um die Komponentenauswahl zu öffnen und dort auszuwählen, welche Komponente als Registerkarte hinzugefügt werden soll. Nach dem Hinzufügen wird der Liste ein Eintrag hinzugefügt, der die folgenden Spalten enthält:

* **Symbol** - Das Symbol des Komponententyps der Registerkarte zur einfachen Identifizierung in der Liste. Bewegen Sie den Mauszeiger darüber, um den vollständigen Komponentennamen als QuickInfo zu sehen.
* **Beschreibung** - Die Beschreibung, die als Text der Registerkarte verwendet wird und standardmäßig den Namen der für die Registerkarte ausgewählten Komponente enthält.
* **Entfernen** - Tippen oder klicken Sie darauf, um die Registerkarte aus der Registerkarten-Komponente zu löschen.
* **Neu anordnen** - Tippen oder klicken Sie darauf, um die Reihenfolge der Registerkarten neu anzuordnen.

>[!TIP]
>
>Wenn der Viewport der Seite so reduziert wird, dass das Bearbeitungsdialogfeld im Vollbildmodus angezeigt wird, ist die Schaltfläche **Hinzufügen** ausgeblendet. Sie können der Registerkarten-Komponente weiterhin Komponenten hinzufügen, indem Sie sie [per Drag-and-Drop aus dem Komponenten-Browser ziehen und im Seiteneditor auf der Registerkarten-Komponente ablegen](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html?lang=de#inserting-a-component).

### Registerkarte „Eigenschaften“ {#properties-tab}

![Registerkarte „Eigenschaften“ im Dialogfeld „Bearbeiten“ der Registerkarten-Komponente](/help/assets/tabs-edit-properties.png)

* **Aktives Element** - Der Inhaltsautor kann definieren, welche Registerkarte beim Laden der Seite aktiv ist.
   * Mit der Option **Standard** wird die erste Registerkarte ausgewählt.
* **ID** – Diese Option dient zur Kontrolle der eindeutigen Kennung der Komponente in der HTML-Datei und auf der [Datenschicht](/help/developing/data-layer/overview.md).
   * Wenn Sie das Feld leer lassen, wird automatisch eine eindeutige ID generiert, die Sie über die resultierende Seite finden.
   * Sofern eine ID angegeben wird, ist vom Autor bzw. der Autorin sicherzustellen, dass diese eindeutig ist.
   * Änderungen der ID können sich auf das CSS-, JS- und Datenschicht-Tracking auswirken.

### Registerkarte „Erreichbarkeit“ {#accessibility-tab}

![Registerkarte „Barrierefreiheit“ im Dialogfeld „Bearbeiten“ der Registerkarten-Komponente](/help/assets/tabs-edit-accessibility.png)

Auf der Registerkarte **Erreichbarkeit** können Werte für die [ARIA-Barrierefreiheits-Beschriftungen](https://www.w3.org/WAI/standards-guidelines/aria/) für die Komponente festgelegt werden.

* **Beschriftung** - Wert eines ARIA-Beschriftungs-Attributs für die Komponente

## Bedienfeld auswählen {#select-panel}

Der Inhaltsautor kann in der Komponenten-Symbolleiste die Option **Bedienfeld auswählen** verwenden, um zu einem anderen Bedienfeld zu wechseln, um es zu bearbeiten und auch um die Reihenfolge der Registerkarten einfach zu ändern.

![Symbol „Bedienfeld auswählen“](/help/assets/select-panel-icon.png)

Nach Auswahl der Option **Bedienfeld auswählen** in der Komponenten-Symbolleiste werden die konfigurierten Registerkarten als Dropdown-Liste angezeigt.

* Die Liste wird im Sinne der zugewiesenen Anordnung der Registerkarten geordnet, was sich auch in der Nummerierung zeigt.
* Der Komponententyp der Registerkarte wird zuerst angezeigt, gefolgt von der Beschreibung der Registerkarte in hellerer Schriftart.

![Popover „Bedienfeld auswählen“](/help/assets/select-panel-popover.png)

* Durch Tippen oder Klicken auf einen Eintrag in der Dropdown-Liste wird die Ansicht im Editor auf diese Registerkarte verschoben.
* Die Registerkarten können direkt mithilfe der Ziehgriffe neu angeordnet werden.

>[!NOTE]
>
>Registerkarten können vom Autor im **Bearbeiten**-Modus nicht ausgewählt werden. Verwenden Sie den **[Vorschaumodus](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html?lang=de#preview-mode)** oder die Option **[Als veröffentlicht anzeigen](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html?lang=de#view-as-published)**, um so mit den Registerkarten zu interagieren, wie es ein Leser des veröffentlichten Inhalts tun würde.

## Dialogfeld „Design“ {#design-dialog}

Im Dialogfeld „Design“ kann der Vorlagenautor definieren, welche Komponenten zu der Registerkarten-Komponente als Elemente hinzugefügt werden können. Außerdem kann er festlegen, welche benutzerdefinierten Stile dem Inhaltsautor zur Verfügung stehen.

### Registerkarte „Zugelassene Komponenten“ {#allowed-components-tab}

Über die Registerkarte **Zulässige Komponenten** können Sie definieren, welche Komponenten von Inhaltsautorinnen und Inhaltsautoren als Elemente zur Registerkarten-Komponente hinzugefügt werden können.

Die Registerkarte „Zugelassene Komponenten“ funktioniert auf die gleiche Weise wie die Registerkarte desselben Namens beim [Definieren der Richtlinie und Eigenschaften eines Layout-Containers im Vorlageneditor.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=de)

### Registerkarte „Arten“ {#styles-tab}

Die Registerkarten-Komponente unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).

## Adobe Client-Datenschicht {#data-layer}

Die Registerkarten-Komponente unterstützt die [Adobe Client-Datenschicht](/help/developing/data-layer/overview.md).
