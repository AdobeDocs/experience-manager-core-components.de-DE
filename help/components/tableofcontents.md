---
title: Inhaltsverzeichniskomponente
description: Die Inhaltsverzeichniskomponente erstellt ein Inhaltsverzeichnis, das auf den Titeln Ihres Seiteninhalts basiert und Ihren Lesern eine schnelle Navigation auf der Seite ermöglicht.
role: Architect, Developer, Admin, User
exl-id: 006adde2-ebff-4e74-8e79-325cccd43e8f
source-git-commit: dd30def59a8f037864da875ef4c831b11f766e57
workflow-type: ht
source-wordcount: '0'
ht-degree: 100%

---


# Inhaltsverzeichniskomponente {#table-of-contents-component}

Die Inhaltsverzeichniskomponente erstellt ein Inhaltsverzeichnis, das auf den Titeln Ihres Seiteninhalts basiert und Ihren Lesern eine schnelle Navigation auf der Seite ermöglicht.

{{traditional-aem}}

## Nutzung {#usage}

Die Inhaltsverzeichniskomponente bietet Website-Besuchern die Möglichkeit, schnell durch den Inhalt Ihrer Seite zu navigieren. Dazu wird ein Inhaltsverzeichnis verwendet, das anhand der Titel der Seiteninhalte effizient erstellt wird.

* Das Inhaltsverzeichnis wird Server-seitig generiert.
* Es wird vollständig vom Dispatcher zwischengespeichert, um eine schnelle Bereitstellung zu ermöglichen.
* Es funktioniert mit allen Komponenten auf der Seite, nicht nur mit den Kernkomponenten.

Der [Bearbeitungsdialog](#edit-dialog) ermöglicht es dem Autor des Inhalts, eine Reihe von Titeln zu definieren, die im Inhaltsverzeichnis verwendet werden sollen. Mithilfe des [Design-Dialogs](#design-dialog) kann der Autor der Vorlage den Standardwert für die Titel festlegen, wenn ein Inhaltsautor einer Seite eine Inhaltsverzeichniskomponente hinzufügt, sowie die im Inhaltsverzeichnis enthaltenen Titel auf der Grundlage von Klassennamen einschränken.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Inhaltsverzeichniskomponente ist v1, die mit der Version 2.20.0 der Kernkomponenten im Mai 2022 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|---|---|---|---|
| v1 | Kompatibel | Kompatibel | Kompatibel |

Weitere Informationen zu Kernkomponentenversionen und -freigaben finden Sie in den [Kernkomponentenversionen](/help/versions.md).

>[!NOTE]
>
>Auf AEM as a Cloud Service muss Ihre Administratorin oder Ihr Administrator einen Filter für die Komponente aktivieren, damit der Inhalt der Komponente gerendert werden kann.
>
>[Bitte lesen Sie die GitHub-Dokumentation der Komponente](https://adobe.com/go/aem_cmp_tech_tableofcontents_v1) für weitere Informationen.

### Technische Details {#technical-details}

Die neueste technische Dokumentation zur Inhaltsverzeichniskomponente [finden Sie auf GitHub](https://adobe.com/go/aem_cmp_tech_tableofcontents_v1).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Dialogfeld „Bearbeiten“ {#edit-dialog}

Im Bearbeitungsdialog kann der Autor des Inhalts die Bereiche der Titelebenen festlegen, die von der Inhaltskomponente als Inhaltsverzeichnis wiedergegeben werden sollen.

![Bearbeitungsdialog der Inhaltsverzeichniskomponente](/help/assets/tableofcontents-edit.png)

**Listentyp** - Diese Option definiert, ob es sich bei der Liste um eine Liste mit Aufzählungszeichen oder eine nummerierte Liste handeln soll.
* **Startstufe für Titel** - Diese Option definiert die höchste Ebene von Titeln, die die Inhaltsverzeichniskomponente rendern soll.
* **Stoppstufe für Titel** - Mit dieser Option wird die niedrigste Ebene von Titeln definiert, die die Inhaltsverzeichniskomponente rendern soll.
* **ID** - Diese Option dient zur Kontrolle der eindeutigen Kennung der Komponente in der HTML-Datei und auf der [Datenschicht](/help/developing/data-layer/overview.md).
   * Wenn Sie das Feld leer lassen, wird automatisch eine eindeutige ID generiert, die Sie über die resultierende Seite finden.
   * Sofern eine ID angegeben wird, ist vom Autor bzw. der Autorin sicherzustellen, dass diese eindeutig ist.
   * Änderungen der ID können sich auf das CSS-, JS- und Datenschicht-Tracking auswirken.

## Dialogfeld „Design“ {#design-dialog}

Mithilfe des Design-Dialogs kann der Autor der Vorlage den Standardwert für den Titelbereich der Inhaltsverzeichniskomponente festlegen und die im Inhaltsverzeichnis enthaltenen Titel auf der Grundlage von Klassennamen einschränken.

### Registerkarte „Eigenschaften“ {#properties-tab}

![Design-Dialog der Schnellsuch-Komponente](/help/assets/tableofcontents-design.png)

* **Listentyp einschränken** - Diese Option definiert den Listentyp, den die Komponente generiert. Durch Auswahl dieser Option wird die Möglichkeit des Inhaltsautors eingeschränkt, einen anderen Listentyp auszuwählen.
* **Startebene einschränken** - Diese Option definiert die höchste Titelebene, die der Inhaltsautor zum Definieren des Inhaltsverzeichnisses auswählen kann.
* **Stoppstufe einschränken** - Diese Option definiert die niedrigste Titelebene, die der Inhaltsautor zum Definieren des Inhaltsverzeichnisses auswählen kann.
* **Klassennamen einschließen** - Wenn diese Option festgelegt ist, werden nur Titel mit den angegebenen Klassennamen oder in Elementen der angegebenen Klassennamen in der Inhaltsverzeichniskomponente berücksichtigt.
   * Tippen oder klicken Sie auf das Symbol **Hinzufügen**, um einen oder mehrere Klassennamen hinzuzufügen.
   * Tippen oder klicken Sie auf das Symbol **Löschen** neben einem Klassennamen, um ihn zu löschen.
* **Klassennamen ignorieren** - Wenn diese Option festgelegt ist, werden Titel mit den angegebenen Klassennamen oder in Elementen der angegebenen Klassennamen von der Inhaltsverzeichniskomponente ignoriert.
   * Tippen oder klicken Sie auf das Symbol **Hinzufügen**, um einen oder mehrere Klassennamen hinzuzufügen.
   * Tippen oder klicken Sie auf das Symbol **Löschen** neben einem Klassennamen klicken, um ihn zu löschen.

### Registerkarte „Stile“ {#styles-tab}

Die Inhaltsverzeichniskomponente unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).

## Adobe-Client-Datenschicht {#data-layer}

Die Inhaltsverzeichniskomponente unterstützt die [Adobe-Client-Datenschicht.](/help/developing/data-layer/overview.md)
