---
title: Verwenden von E-Mail-Kernkomponenten
description: Erfahren Sie mehr über die Grundlagen der Installation, Konfiguration und Verwendung der E-Mail-Kernkomponenten.
role: Architect, Developer, Admin, User
exl-id: 0e79ca8f-eb0a-4519-b1e8-a9d3b0b99987
source-git-commit: 33976c0e745ad091a142109f70541f01a31edc5b
workflow-type: tm+mt
source-wordcount: '653'
ht-degree: 96%

---


# Verwenden von E-Mail-Kernkomponenten {#using}

Erfahren Sie mehr über die Grundlagen der Installation, Konfiguration und Verwendung der E-Mail-Kernkomponenten.

## Installieren der E-Mail-Kernkomponenten {#installation}

Die E-Mail-Kernkomponenten können mit AEM 6.5 verwendet werden. Siehe den Abschnitt [Anforderungen des Einführungsdokuments für E-Mail-Kernkomponenten](introduction.md#requirements) für mehr Informationen.

### Installieren von Kernkomponenten {#core-components}

Die E-Mail-Kernkomponenten basieren auf den AEM-Kernkomponenten. Da die Kernkomponenten nicht im Lieferumfang von AEM 6.5 enthalten sind, müssen Sie zunächst die AEM Kernkomponenten installieren, bevor Sie die E-Mail-Kernkomponenten installieren.

Siehe den Abschnitt [Herunterladen und Installieren](/help/get-started/using.md#download-and-install) des Dokuments „Verwenden von Kernkomponenten“ für weitere Informationen zur Installation der Kernkomponenten.

### Installieren der E-Mail-Kernkomponenten {#email-core-components}

Nachdem die Kernkomponenten in Ihrer Instanz installiert sind, müssen Sie auch die E-Mail-Kernkomponenten installieren. Die E-Mail-Kernkomponenten sind noch nicht Teil des AEM-Projektarchetyps. Daher müssen Sie sie manuell zu Ihrem Projekt hinzufügen. Befolgen Sie zur Installation die Dokumentation unter [E-Mail-Kernkomponenten GitHub Wiki](https://github.com/adobe/aem-core-email-components/wiki/Adding-to-Existing-Project).

Sie können denselben Anweisungen folgen, wenn Sie ein vorhandenes Projekt so anpassen möchten, dass es mit den E-Mail-Kernkomponenten verwendet werden kann.

## Konfiguration {#configuration}

Nach der Installation der Kernkomponenten sollten Sie zwei wichtige Konfigurationsschritte ausführen.

### Konfigurieren von Campaign {#configure-campaign}

Sie müssen die AEM-Adobe Campaign-Integration einrichten, damit die beiden Lösungen kommunizieren können.

* Konfigurieren Ihrer Adobe Campaign-Integration
   * Adobe Campaign Classic: [Integration mit Adobe Campaign Classic](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/campaignonpremise.html?lang=de)
   * Adobe Campaign Standard: [Integration mit Adobe Campaign Standard](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/campaignstandard.html?lang=de)
* [Verknüpfen der Adobe Campaign-Integrationskonfiguration](/help/email/components/page.md#cloud-services-tab) mit der Inhaltsseite, auf der Sie die E-Mail-Kernkomponenten verwenden werden

### Hinzufügen eines AEM-Ressourcentypfilters für E-Mail-Komponenten {#aem-resource-filter}

Damit in Adobe Campaign E-Mails anhand der E-Mail-Kernkomponenten gerendert werden können, muss in Campaign ein Filter angepasst werden.

1. Melden Sie sich mit der Client-Konsole bei Adobe Campaign als Administrator an.

1. Wählen Sie **Tools** -> **Explorer** in der Menüleiste.

1. Navigieren Sie im Explorer zum Knoten **Administration** > **Plattform** > **Option**.

1. Wählen Sie die Option `AEMResourceTypeFilter` in der Liste aus.

1. Hängen Sie im Feld **Wert** `core/email/components/page/<v1>/page` an, sofern noch nicht vorhanden.

   * Ersetzen Sie `<v1>` durch die aktuelle Version [Seitenkomponente](/help/email/components/page.md) der E-Mail-Kernkomponenten, wie etwa `v1`.
   * Beachten Sie, dass Werte im Feld **Werte** kommagetrennt sein müssen.

1. Klicken Sie auf **Speichern**.

## Verwenden von E-Mail-Kernkomponenten {#using-components}

Nachdem die E-Mail-Komponenten installiert und die Integration mit Adobe Campaign konfiguriert wurde, können Sie die E-Mail-Komponenten verwenden, um E-Mail-Inhalte in AEM zu erstellen und diese Inhalte dann mithilfe von Adobe Campaign an Empfänger zu senden. Im Folgenden finden Sie eine Übersicht über den Workflow.

| Schritt | Beschreibung | Lösung |
|---|---|---|
| 1 | Autoren erstellen eine freie hierarchische Struktur von Ordnern und E-Mail-Inhalten als Seiten. | AEM |
| 2 | Autoren konfigurieren unter Verwendung des [Vorlageneditors](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=de) eine E-Mail-Kopfzeile und/oder -Fußzeile, die für alle E-Mail-Seiten, die aus dieser Seitenvorlage resultieren, verwendet werden. | AEM |
| 3 | Autoren verwenden den [Seiteneditor](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/fundamentals/editing-content.html?lang=de), um E-Mail-Inhalte mit dem Texteditor zu erstellen, in dem sie Adobe Campaign-Variablen auswählen und mithilfe der Segmentierungskomponente Informationen anzeigen können, wenn der Empfänger bestimmte Kriterien erfüllt. | AEM |
| 4 | Wenn der E-Mail-Inhalt fertig ist, wird [ein Workflow ausgeführt](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/workflows/overview.html?lang=de), um den Inhalt zu validieren und an Campaign zu senden. | AEM |
| 5 | Es wird ein Versand erstellt, in dem eine Empfängerliste definiert wird. | Campaign |
| 6 | Der in AEM erstellte Inhalt wird für den Versand ausgewählt. | Kampagne |
| 7 | Der Inhalt wird an die Empfänger gesendet. Dabei werden die Adobe Campaign-Variablen durch die personalisierten Empfängerinformationen ersetzt. | Kampagne |

Ein Beispiel für die Erstellung von E-Mail-Inhalt in AEM und den Versand in Adobe Campaign finden Sie in den folgenden Informationsmaterialien.

* AEM 6.5: [Arbeiten mit Adobe Campaign Classic und Adobe Campaign Standard](https://experienceleague.adobe.com/docs/experience-manager-65/authoring/aem-adobe-campaign/campaign.html?lang=de)
