---
title: 'Social-Sharing-Komponente '
description: Die Kernkomponente „Social-Sharing-Komponente“ ist ein Widget zum Teilen auf Facebook und Pinterest.
role: Architect, Developer, Admin, User
exl-id: 8bd53c76-da91-479b-b416-f978682a3d43
source-git-commit: 6fbc781db555bc6abaed1d122a9a8756e3d53222
workflow-type: ht
source-wordcount: '378'
ht-degree: 100%

---

# Social-Sharing-Komponente {#social-sharing-component}

Die Kernkomponente „Social-Sharing-Komponente“ ist ein Widget zum Teilen auf Facebook und Pinterest.

>[!NOTE]
>
>Die Social-Sharing-Komponente wurde mit Kernkomponenten der [Version 2.18.0](/help/versions.md) entfernt.

## Nutzung {#usage}

Die Social-Sharing-Komponente fügt Sharing-Links für Facebook und Pinterest zur Seite hinzu. Sie wird häufig in Kopf- oder Fußzeilen von Seiten einbezogen.

Im Gegensatz zu anderen Komponenten erfolgen die Einstellungen für die Social-Sharing-Komponente durch den Vorlagenautor über [Anfangs-Seiteneigenschaften](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=de) und durch den Inhaltsautor über [Seiteneigenschaften](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html?lang=de).

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Social-Sharing-Komponente ist v1, die mit Version 1.0.0 der Kernkomponenten eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente und die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind.

| Komponentenversion | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |--- |---|---|
| v1 | Kompatibel mit<br>[Version 2.17.4](/help/versions.md) und vorherigen | Kompatibel, veraltet | Kompatibel, veraltet | Kompatibel, veraltet |

Weitere Informationen zu Kernkomponentenversionen und -freigaben finden Sie im Dokument [Kernkomponentenversionen](/help/versions.md).

### Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur Sharing-Komponente [finden Sie auf GitHub](https://adobe.com/go/aem_cmp_tech_sharing_v1_de).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Dialogfeld „Bearbeiten“ {#edit-dialog}

![Dialogfeld „Bearbeiten“ der Sharing-Komponente](/help/assets/sharing-edit.png)

* **ID** – Diese Option dient zur Kontrolle der eindeutigen Kennung der Komponente in der HTML-Datei und auf der [Datenschicht](/help/developing/data-layer/overview.md).
   * Wenn Sie das Feld leer lassen, wird automatisch eine eindeutige ID generiert, die Sie über die resultierende Seite finden.
   * Sofern eine ID angegeben wird, ist vom Autor bzw. der Autorin sicherzustellen, dass diese eindeutig ist.
   * Änderungen der ID können sich auf das CSS-, JS- und Datenschicht-Tracking auswirken.

Da das Sharing bzw. Freigeben spezielle Seiten-Kopfzeilen erfordert, muss jede Freigabe auf Seitenebene aktiviert werden. Daher sind die Bearbeitungsoptionen für die Social-Media-Komponente für den Inhaltsautor auf der Registerkarte „Freigabe“ in den [Seiteneigenschaften](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html?lang=de) verfügbar.

## Dialogfeld „Design“ {#design-dialog}

Da das Sharing bzw. Freigeben spezielle Seiten-Kopfzeilen erfordert, muss jede Freigabe auf Seitenebene aktiviert werden. Daher sind die Designoptionen für die Social-Media-Komponente für den Vorlagenautor über die [Anfangs-Seiteneigenschaften](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=de) verfügbar.
