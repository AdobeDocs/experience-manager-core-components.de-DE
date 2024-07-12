---
title: Unterstützung für Remote-Assets
description: Erfahren Sie, wie Sie die Bild- und Teaser-Komponenten (beides Kernkomponenten) konfigurieren, um Remote-Assets unter Verwendung von Dynamic Media mit OpenAPI zu unterstützen.
role: Architect, Developer, Admin, User
exl-id: b462c1f3-a6c8-4a2a-abf4-d08ec82d4371
source-git-commit: 36ef19d5b29fe21f86309719d1e3f6588e31a93b
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 100%

---


# Unterstützung für Remote-Assets {#remote-assets-support}

Erfahren Sie, wie Sie die Bild- und Teaser-Komponenten (beides Kernkomponenten) konfigurieren, um Remote-Assets unter Verwendung von Dynamic Media mit OpenAPI zu unterstützen.

>[!NOTE]
>
>Dynamic Media mit OpenAPI wurde früher als Next Generation Dynamic Media bezeichnet. Funktionalität und Verwendung sind identisch.

## Abrufen der neuesten AEM-Version {#latest}

Für die Unterstützung von Remote-Assets mit Dynamic Media mit OpenAPI ist Folgendes erforderlich:

* AEM 6.5 SP 18+ oder AEM as a Cloud Service
* Kernkomponenten, Version 2.23.2 oder höher

## Konfigurieren von HTTPS {#https}

Es wird allgemein empfohlen, alle Ihre Produktions-AEM-Instanzen mithilfe von HTTPS auszuführen. Ihre lokalen Entwicklungsumgebungen sind jedoch möglicherweise nicht als solche eingerichtet. Damit Remote-Assets von Dynamic Media mit OpenAPI funktionieren, ist jedoch HTTPS erforderlich.

[Verwenden Sie dieses Handbuch](https://experienceleague.adobe.com/docs/experience-manager-learn/foundation/security/use-the-ssl-wizard.html?lang=de), um HTTPS zu konfigurieren, wo immer Sie Remote-Assets verwenden möchten, einschließlich Entwicklungsumgebungen.

## Konfigurieren von OSGi {#osgi}

Der Speicherort der Remote-Assets muss in einer OSGi-Konfiguration definiert werden. Konfigurieren Sie die OSGi-Konfiguration **Next Generation Dynamic Media Config** und ersetzen Sie die Werte mit den Werten Ihrer Remote-Asset-Umgebung.

```text
imsClient="<ims-client-name>"
enabled=B"true"
imsOrg="<ims-org>@AdobeOrg"
repositoryId="<repo-id>.adobeaemcloud.com"
```

![Das OSGi-Konfigurationsfenster von Next Generation Dynamic Media](/help/assets/remote-assets-osgi.png)

Weitere Informationen zum Konfigurieren von OSGi finden Sie in den folgenden Dokumenten:

* [Konfigurieren von OSGi für Adobe Experience Manager as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/deploying/configuring-osgi.html?lang=de) für AEM as a Cloud Service
* [Konfigurieren von OSGi](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/configuring/configuring-osgi.html?lang=de) für AEM 6.5

## Überprüfen der Konfiguration {#verify}

Jetzt können Sie überprüfen, ob die Funktion für Remote-Assets mit Dynamic Media mit OpenAPI funktioniert. Dazu können Sie die WKND-Beispiel-Site und die Kernkomponenten installieren.

* [Kernkomponenten](https://github.com/adobe/aem-core-wcm-components/releases/download/core.wcm.components.reactor-2.23.2/core.wcm.components.all-2.23.2.zip), Version 2.23.2 oder höher, ist erforderlich.
* [WKND-Beispiel-Site](https://github.com/adobe/aem-guides-wknd/releases/download/aem-guides-wknd-3.2.0/aem-guides-wknd.all-3.2.0-classic.zip), Version 3.2.0 oder höher, ist erforderlich.

Sobald die Kernkomponenten- und WKND-Site installiert sind, können Sie die Funktion auf jeder beliebigen WKND-Seite testen.

1. Greifen Sie über HTTPS auf die AEM-Instanz zu.

1. Öffnen Sie eine WKND-Demoseite im Seiteneditor, z. B. `https://<host>:<httpsPort>/editor.html/content/wknd/language-masters/en/magazine/arctic-surfing.html`

1. Fügen Sie der Seite eine Bildkomponente hinzu.

1. Deaktivieren Sie im Dialogfeld „Konfigurieren“ der Komponente die Option **Vorgestelltes Bild von Seite übernehmen** auf der Registerkarte **Asset** und klicken Sie auf **Auswählen**.

1. Wenn die Konfiguration korrekt ist, wird eine Dropdown-Liste mit den Optionen **Lokal** und **Remote** angezeigt. Wählen Sie **Remote** aus.

   ![Remote- und lokale Option zur Auswahl von Bildern](/help/assets/remote-asset-selection.png)

1. Es öffnet sich ein Dialogfeld, in dem Sie sich beim Remote-Dienst authentifizieren müssen.

1. Nach der Authentifizierung wird ein Asset-Browser des Remote-Dienstes geöffnet. Wählen Sie das gewünschte Asset aus und tippen oder klicken Sie auf **Auswählen**.

   ![Auswählen eines Remote-Assets](/help/assets/remote-asset-picker.png)

Das Remote-Asset wird Ihrer lokalen AEM-Seite hinzugefügt und Sie haben überprüft, dass die Funktion korrekt konfiguriert ist.

## Verwenden von Remote-Assets {#using}

Wenn sie konfiguriert sind, können Remote-Assets mithilfe der Kernkomponenten [Bildkomponente](/help/components/image.md) und [Teaser-Komponente](/help/components/teaser.md) ausgewählt werden.
