---
title: Social-Sharing-Komponente
description: Die Kernkomponente „Social-Sharing-Komponente“ ist ein Widget zum Teilen auf Facebook und Pinterest.
translation-type: tm+mt
source-git-commit: 4813748bcfa83ce7c73e81d4e4d445ecc8215d26
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 94%

---


# Social-Sharing-Komponente{#social-sharing-component}

Die Kernkomponente „Social-Sharing-Komponente“ ist ein Widget zum Teilen auf Facebook und Pinterest.

## Verwendung {#usage}

Die Social-Sharing-Komponente fügt Sharing-Links für Facebook und Pinterest zur Seite hinzu. Sie wird häufig in Kopf- oder Fußzeilen von Seiten einbezogen.

Im Gegensatz zu anderen Komponenten erfolgen die Einstellungen für die Social-Sharing-Komponente durch den Vorlagenautor über [Anfangs-Seiteneigenschaften](https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/sites/authoring/features/templates.translate.html) und durch den Inhaltsautor über [Seiteneigenschaften](https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.translate.html).

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Social Sharing-Komponente ist Version 1, die mit Version 1.0.0 der Core-Komponenten eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente und die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind.

| Komponentenversion | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v1 | Kompatibel | Kompatibel | Kompatibel |

Weitere Informationen zu Kernkomponentenversionen und -freigaben finden Sie in den [Kernkomponentenversionen](/help/versions.md).

## Musterkomponentenausgabe {#sample-component-output}

Um die Social-Sharing-Komponente kennenzulernen und Beispiele für ihre Konfigurationsoptionen sowie die HTML- und JSON-Ausgabe zu sehen, besuchen Sie die [Komponentenbibliothek](https://adobe.com/go/aem_cmp_library_sharing_de).

### Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur Sharing-Komponente [finden Sie auf GitHub](https://adobe.com/go/aem_cmp_tech_sharing_v1_de).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Dialogfeld „Bearbeiten“ {#edit-dialog}

![Dialogfeld „Bearbeiten“ der Sharing-Komponente](/help/assets/sharing-edit.png)

* **ID** – Diese Option dient zur Kontrolle der eindeutigen Kennung der Komponente in der HTML-Datei und auf der [Datenschicht](/help/developing/data-layer/overview.md).
   * Wenn Sie das Feld leer lassen, wird automatisch eine eindeutige ID generiert, die Sie über die resultierende Seite finden.
   * Sofern eine ID angegeben wird, ist vom Autor sicherzustellen, dass diese eindeutig ist.
   * Änderungen der ID können sich auf das CSS-, JS- und Datenschicht-Tracking auswirken.

Da das Sharing bzw. Freigeben spezielle Seiten-Kopfzeilen erfordert, muss jede Freigabe auf Seitenebene aktiviert werden. Daher sind die Bearbeitungsoptionen für die Social-Media-Komponente für den Inhaltsautor auf der Registerkarte „Freigabe“ in den [Seiteneigenschaften](https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.translate.html) verfügbar.

## Dialogfeld „Design“ {#design-dialog}

Da das Sharing bzw. Freigeben spezielle Seiten-Kopfzeilen erfordert, muss jede Freigabe auf Seitenebene aktiviert werden. Daher sind die Designoptionen für die Social-Media-Komponente für den Vorlagenautor über die [Anfangs-Seiteneigenschaften](https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/sites/authoring/features/templates.translate.html) verfügbar.
