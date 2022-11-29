---
title: Verwenden der E-Mail-Kernkomponenten
description: Erfahren Sie mehr über die grundlegende Installation, Konfiguration und Verwendung der E-Mail-Kernkomponenten.
role: Architect, Developer, Admin, User
exl-id: 0e79ca8f-eb0a-4519-b1e8-a9d3b0b99987
source-git-commit: 33976c0e745ad091a142109f70541f01a31edc5b
workflow-type: tm+mt
source-wordcount: '653'
ht-degree: 7%

---


# Verwenden der E-Mail-Kernkomponenten {#using}

Erfahren Sie mehr über die grundlegende Installation, Konfiguration und Verwendung der E-Mail-Kernkomponenten.

## Installieren der E-Mail-Kernkomponenten {#installation}

Die E-Mail-Kernkomponenten können mit AEM 6.5 verwendet werden. Siehe [Abschnitt &quot;Anforderungen&quot;des Einführungsdokuments für E-Mail-Kernkomponenten](introduction.md#requirements) für weitere Informationen.

### Installieren von Kernkomponenten {#core-components}

Die E-Mail-Kernkomponenten basieren auf den AEM Kernkomponenten. Da die Kernkomponenten nicht im Lieferumfang von AEM 6.5 enthalten sind, müssen Sie zunächst die AEM Kernkomponenten installieren, bevor Sie die E-Mail-Kernkomponenten installieren.

Siehe Abschnitt . [Herunterladen und installieren](/help/get-started/using.md#download-and-install) Abschnitt des Dokuments Verwenden von Kernkomponenten für weitere Informationen zur Installation der Kernkomponenten.

### E-Mail-Kernkomponenten installieren {#email-core-components}

Sobald die Kernkomponenten in Ihrer Instanz installiert sind, müssen Sie auch die E-Mail-Kernkomponenten installieren. Die E-Mail-Kernkomponenten sind noch nicht Teil des AEM Projektarchetyps. Daher müssen Sie sie manuell zu Ihrem Projekt hinzufügen. Befolgen Sie die Dokumentation unter [das GitHub-Wiki für E-Mail-Kernkomponenten zur Installation.](https://github.com/adobe/aem-core-email-components/wiki/Adding-to-Existing-Project)

Sie können dieselben Anweisungen befolgen, wenn Sie ein vorhandenes Projekt an die E-Mail-Kernkomponenten anpassen möchten.

## Konfiguration {#configuration}

Nach der Installation der Kernkomponenten sollten Sie zwei wichtige Konfigurationsschritte ausführen.

### Konfigurieren von Campaign {#configure-campaign}

Sie müssen die AEM-Adobe Campaign-Integration einrichten, damit die beiden Lösungen kommunizieren können.

* Konfigurieren der Adobe Campaign-Integration
   * Adobe Campaign Classic: [Integration mit Adobe Campaign Classic](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/campaignonpremise.html)
   * Adobe Campaign Standard: [Integration mit Adobe Campaign Standard](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/campaignstandard.html)
* [Verknüpfen der Adobe Campaign-Integrationskonfiguration](/help/email/components/page.md#cloud-services-tab) zur Inhaltsseite, auf der Sie die E-Mail-Kernkomponenten verwenden werden

### Hinzufügen AEM Ressourcentypfilters für E-Mail-Komponenten {#aem-resource-filter}

Damit Adobe Campaign E-Mails anhand der E-Mail-Kernkomponenten rendern kann, muss ein Filter in Campaign angepasst werden.

1. Melden Sie sich mit der Client-Konsole bei Adobe Campaign als Administrator an.

1. Wählen Sie **Tools** -> **Explorer** in der Menüleiste.

1. Navigieren Sie im Explorer zum **Administration** -> **Plattform** -> **Optionen** Knoten.

1. Wählen Sie die `AEMResourceTypeFilter` aus der Liste.

1. Im **Wert** -Feld anhängen `core/email/components/page/<v1>/page` , wenn sie noch nicht vorhanden ist.

   * Ersetzen `<v1>` mit der aktuellen Version der E-Mail-Kernkomponenten [Seitenkomponente](/help/email/components/page.md) wie `v1`.
   * Beachten Sie, dass Werte in **Werte** -Feld muss kommagetrennt sein.

1. Klicken Sie auf **Speichern**.

## Verwenden der E-Mail-Kernkomponenten {#using-components}

Nachdem die E-Mail-Komponenten installiert und die Integration mit Adobe Campaign konfiguriert wurde, können Sie die E-Mail-Komponenten verwenden, um E-Mail-Inhalte in AEM zu erstellen und diese dann mithilfe von Adobe Campaign an Empfänger zu senden. Im Folgenden finden Sie eine Übersicht über den Workflow.

| Schritt | Beschreibung | Lösung |
|---|---|---|
| 1 | Autoren erstellen eine freie hierarchische Struktur von Ordnern und E-Mail-Inhalten als Seiten. | AEM |
| 2 | Verwenden der [Vorlageneditor,](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=de) -Autoren konfigurieren eine E-Mail-Kopfzeile und/oder Fußzeile, die auf allen E-Mail-Seiten, die aus dieser Seitenvorlage resultieren, freigegeben wird. | AEM |
| 3 | Autoren verwenden die [Seiteneditor](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/fundamentals/editing-content.html) , um E-Mail-Inhalte mit dem Texteditor zu erstellen, in dem sie Adobe Campaign-Variablen auswählen und mithilfe der Segmentierungskomponente Informationen bedingt anzeigen können, wenn der Empfänger bestimmte Kriterien erfüllt. | AEM |
| 4 | Wenn der E-Mail-Inhalt abgeschlossen ist, [Ausführung eines Workflows](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/workflows/overview.html) um den Inhalt zu validieren und an Campaign zu senden. | AEM |
| 5 | Es wird ein Versand erstellt, der eine Empfängerliste enthält. | Campaign |
| 6 | Der in AEM erstellte Inhalt wird als Inhalt des Versands ausgewählt. | Kampagne |
| 7 | Der Inhalt wird an die Empfänger gesendet und ersetzt die Adobe Campaign-Variablen durch die personalisierten Empfängerinformationen. | Kampagne |

Ein Beispiel für die Erstellung von E-Mail-Inhalten in AEM und die Bereitstellung in Adobe Campaign finden Sie in den folgenden Ressourcen.

* AEM 6.5: [Arbeiten mit Adobe Campaign Classic und Adobe Campaign Standard](https://experienceleague.adobe.com/docs/experience-manager-65/authoring/aem-adobe-campaign/campaign.html)
