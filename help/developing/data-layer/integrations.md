---
title: Integrationen und die Adobe Client-Datenschicht
description: Erfahren Sie, wie die Adobe Client Data Layer in Ihre benutzerdefinierten Komponenten integriert werden kann und wie Sie durch Integrationen mit Adobe Analytics und Adobe Target Einblicke in Ihre Website gewinnen können.
translation-type: tm+mt
source-git-commit: ea7a0e08ea1b769b400fce275c8ce7e0db6f9407
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 53%

---


# Integration mit der Adobe Client-Datenschicht {#integrations}

Die Adobe Client-Datenschicht reduziert Aufwand für die Instrumentierung von Websites, indem sie für jedes Skript eine standardisierte Methode für die Darstellung von und den Zugriff auf jede Art von Daten bietet.

Die Adobe Client Data Layer kann in Ihre benutzerdefinierten Komponenten integriert werden und Integrationen mit Adobe Analytics und Adobe Target können Ihnen dabei helfen, Einblicke in Ihre Website zu gewinnen.

## Aktivieren der Datenschicht für benutzerdefinierte Komponenten {#enabling-custom-components}

So fügen Sie der Datenschicht automatisch eine benutzerdefinierte Komponente hinzu:

1. Definieren Sie die Eigenschaften des benutzerdefinierten Komponentenmodells, das verfolgt werden muss.
1. hinzufügen das `data-cmp-data-layer` Attribut der benutzerdefinierten Komponente HTL. E.g. `data-cmp-data-layer="${mycomponent.data.json}"`.

Damit die Datenschicht jedes Mal, wenn auf ein bestimmtes Element der benutzerdefinierten Komponente geklickt wird, automatisch ein `cmp:click` Ereignis auslöst, fügen Sie das `data-cmp-clickable` Attribut dem Element hinzu, das in der benutzerdefinierten Komponente HTL verfolgt werden soll.

Das `data-cmp-data-layer-enabled` Attribut kann clientseitig abgefragt werden, um zu prüfen, ob die Datenschicht aktiviert ist.

>[!TIP]
>
>Weitere technische Informationen zur Integration der Adobe Client Data Layer mit den Core Components und zur Aktivierung der Datenschicht in Ihren benutzerdefinierten Komponenten finden Sie in der [`DATA_LAYER_INTEGRATION.md`](https://github.com/adobe/aem-core-wcm-components/blob/master/DATA_LAYER_INTEGRATION.md) Datei im Core Components Repository.

## Integration mit Adobe Analytics und Adobe Target {#analytics-target}

In Verbindung mit Adobe Analytics und Adobe Target bildet die Adobe Client-Datenschicht die Grundlage sehr leistungsfähiger und flexibler Tools, mit denen Sie Einblicke in Ihre digitalen Erlebnisse gewinnen können. Die folgenden Tutorials führen Sie durch Beispielintegrationen.

### Erfassen von Seitendaten mit Adobe Analytics {#collect-page-data}

Erfahren Sie, wie Sie die integrierten Funktionen der Adobe Client-Datenschicht mit den AEM-Kernkomponenten verwenden können, um Daten zu einer Seite in Adobe Experience Manager Sites zu erfassen. Experience Platform Launch und die Adobe Analytics-Erweiterung werden verwendet, um Regeln zum Senden von Seitendaten an Adobe Analytics zu erstellen.

[Sehen Sie sich das Tutorial hier an.](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/integrations/analytics/collect-data-analytics.html)

### Verfolgen geklickter Komponenten mit Adobe Analytics {#track-clicked-components}

Verwenden Sie die ereignisbasierte Adobe Client-Datenschicht mit den AEM-Kernkomponenten, um Klicks auf bestimmte Komponenten auf einer Adobe Experience Manager-Site zu verfolgen. Erfahren Sie, wie Sie Regeln in Experience Platform Launch verwenden, um Klick-Ereignisse zu überwachen, nach Komponenten zu filtern und die Daten mit einem Verfolgungs-Linkbeacon an Adobe Analytics zu senden.

[Sehen Sie sich das Tutorial hier an.](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/integrations/analytics/track-clicked-component.html)
