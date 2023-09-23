---
title: Dynamic Media-Unterstützung der nächsten Generation
description: Erfahren Sie, wie Sie die Bild- und Teaser-Kernkomponenten konfigurieren, um Remote-Dynamic Media-Assets der nächsten Generation zu unterstützen.
role: Architect, Developer, Admin, User
source-git-commit: 9b8930c2e268f52a1377906725db9a05a089e233
workflow-type: tm+mt
source-wordcount: '470'
ht-degree: 3%

---


# Dynamic Media-Unterstützung der nächsten Generation {#next-gen-dm-support}

Erfahren Sie, wie Sie die Bild- und Teaser-Kernkomponenten konfigurieren, um Remote-Dynamic Media-Assets der nächsten Generation zu unterstützen.

## Abrufen der neuesten AEM {#latest}

Die Unterstützung für Remote-Assets der nächsten Generation von Dynamic Media erfordert:

* AEM 6.5 SP 18+ oder AEM as a Cloud Service
* Kernkomponentenversion 2.23.2 oder höher

## Konfigurieren von HTTPS {#https}

Es wird allgemein empfohlen, alle Ihre Produktions-AEM-Instanzen mithilfe von HTTPs auszuführen. Ihre lokalen Entwicklungsumgebungen sind jedoch möglicherweise nicht als solche eingerichtet. Remote-Assets der nächsten Generation von Dynamic Media erfordern jedoch HTTPS, damit sie funktionieren.

[Verwenden dieses Handbuchs](https://experienceleague.adobe.com/docs/experience-manager-learn/foundation/security/use-the-ssl-wizard.html) um HTTPS zu konfigurieren, wo immer Sie Remote-Assets verwenden möchten, einschließlich Entwicklungsumgebungen.

## OSGi konfigurieren {#osgi}

Der Speicherort der Remote-Assets muss in einer OSGi-Konfiguration definiert werden. Konfigurieren Sie die **Dynamic Media-Konfiguration der nächsten Generation** OSGi-Konfiguration wie folgt konfigurieren und die Werte durch die Ihrer Remote-Asset-Umgebung ersetzen.

```text
imsClient="<ims-client-name>"
enabled=B"true"
imsOrg="<ims-org>@AdobeOrg"
repositoryId="<repo-id>.adobeaemcloud.com"
```

![Das Konfigurationsfenster der Dynamic Media-Konfiguration der nächsten Generation (OSGi)](/help/assets/remote-assets-osgi.png)

Weitere Informationen zum Konfigurieren von OSGi finden Sie in den folgenden Dokumenten:

* [Konfigurieren von OSGi für Adobe Experience Manager as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/deploying/configuring-osgi.html?lang=de) für AEM as a Cloud Service
* [Konfigurieren von OSGi](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/configuring/configuring-osgi.html?lang=de) AEM 6.5

## Konfiguration überprüfen {#verify}

Jetzt können Sie überprüfen, ob die Funktion für Remote-Assets der nächsten Generation von Dynamic Media funktioniert. Dazu können Sie die WKND-Beispiel-Site und die Kernkomponenten installieren.

* [Kernkomponenten](https://github.com/adobe/aem-core-wcm-components/releases/download/core.wcm.components.reactor-2.23.2/core.wcm.components.all-2.23.2.zip) Version 2.23.2 oder höher ist erforderlich.
* [WKND-Beispiel-Site](https://github.com/adobe/aem-guides-wknd/releases/download/aem-guides-wknd-3.2.0/aem-guides-wknd.all-3.2.0-classic.zip) Version 3.2.0 oder höher ist erforderlich.

Sobald die Kernkomponenten- und WKND-Site installiert sind, können Sie die Funktion auf jeder beliebigen WKND-Seite testen.

1. Greifen Sie über HTTPS auf die AEM-Instanz zu.

1. Öffnen Sie eine WKND-Demoseite im Seiteneditor, z. B. `https://<host>:<httpsPort>/editor.html/content/wknd/language-masters/en/magazine/arctic-surfing.html`

1. Fügen Sie der Seite eine Bildkomponente hinzu.

1. Deaktivieren Sie im Dialogfeld Konfigurieren der Komponente die Option **Eigenes Bild von Seite übernehmen** auf **Asset** Registerkarte und klicken Sie auf **Auswahl**.

1. Wenn die Konfiguration korrekt ist, wird eine Dropdown-Liste mit den Optionen angezeigt **Lokal** und **Remote**. Auswählen **Remote**.

   ![Remote- und lokale Optionen zur Auswahl von Bildern](/help/assets/remote-asset-selection.png)

1. Daraufhin wird ein Dialogfeld geöffnet, in dem Sie sich beim Remote-Dienst authentifizieren müssen.

1. Nach der Authentifizierung wird ein Asset-Browser des Remote-Dienstes geöffnet. Wählen Sie das gewünschte Asset aus und tippen oder klicken Sie auf **Auswählen**.

   ![Remote-Asset auswählen](/help/assets/remote-asset-picker.png)

Das Remote-Asset wird Ihrer lokalen AEM-Seite hinzugefügt und Sie haben überprüft, ob die Funktion korrekt konfiguriert ist.

## Verwenden von Remote-Assets {#using}

Nach der Konfiguration können Remote-Assets ausgewählt werden, in denen Sie mithilfe der Kernkomponenten Assets auswählen, z. B. im [Bildkomponente](/help/components/image.md) und [Teaser-Komponente.](/help/components/teaser.md)
