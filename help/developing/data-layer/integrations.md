---
title: Integrationen und die Adobe Client-Datenschicht
description: Erfahren Sie, wie die Adobe Client-Datenschicht in Ihre benutzerdefinierten Komponenten integriert werden kann und wie Sie durch Integrationen mit Adobe Analytics und Adobe Target Erkenntnisse über Ihre Website gewinnen können.
feature: Kernkomponenten, Adobe Client-Datenschicht
role: Architect, Developer, Admin
exl-id: 503dd3dc-fe95-4a17-83f5-1f0c1960993d
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 100%

---

# Integration mit der Adobe Client-Datenschicht {#integrations}

Die Adobe Client-Datenschicht reduziert Aufwand für die Instrumentierung von Websites, indem sie für jedes Skript eine standardisierte Methode für die Darstellung von und den Zugriff auf jede Art von Daten bietet.

Die Adobe Client-Datenschicht kann in Ihre benutzerdefinierten Komponenten integriert werden und Integrationen mit Adobe Analytics und Adobe Target können Ihnen dabei helfen, Erkenntnisse über Ihre Website zu gewinnen.

## Aktivieren der Datenschicht für benutzerdefinierte Komponenten {#enabling-custom-components}

So fügen Sie der Datenschicht automatisch eine benutzerdefinierte Komponente hinzu:

1. Definieren Sie die Eigenschaften des Modells für benutzerdefinierte Komponenten, das verfolgt werden soll.
1. Fügen Sie das `data-cmp-data-layer`-Attribut der HTL der benutzerdefinierten Komponente hinzu. Beispiel: `data-cmp-data-layer="${mycomponent.data.json}"`

Damit die Datenschicht jedes Mal, wenn auf ein bestimmtes Element der benutzerdefinierten Komponente geklickt wird, automatisch ein `cmp:click`-Ereignis auslöst, fügen Sie in der HTL der benutzerdefinierten Komponente das `data-cmp-clickable`-Attribut dem Element hinzu, das verfolgt werden soll.

Das `data-cmp-data-layer-enabled`-Attribut kann Client-seitig abgefragt werden, um zu prüfen, ob die Datenschicht aktiviert ist.

>[!TIP]
>
>Weitere technische Informationen zur Integration der Adobe Client-Datenschicht mit den Kernkomponenten und zur Aktivierung der Datenschicht in Ihren benutzerdefinierten Komponenten finden Sie in der Datei [`DATA_LAYER_INTEGRATION.md`](https://github.com/adobe/aem-core-wcm-components/blob/master/DATA_LAYER_INTEGRATION.md) im Repository der Kernkomponenten.

## Integration mit Adobe Analytics und Adobe Target {#analytics-target}

In Verbindung mit Adobe Analytics und Adobe Target bildet die Adobe Client-Datenschicht die Grundlage sehr leistungsfähiger und flexibler Tools, mit denen Sie Einblicke in Ihre digitalen Erlebnisse gewinnen können. Die folgenden Tutorials führen Sie durch Beispielintegrationen.

### Erfassen von Seitendaten mit Adobe Analytics {#collect-page-data}

Erfahren Sie, wie Sie die integrierten Funktionen der Adobe Client-Datenschicht mit den AEM-Kernkomponenten verwenden können, um Daten zu einer Seite in Adobe Experience Manager Sites zu erfassen. Experience Platform Launch und die Adobe Analytics-Erweiterung werden verwendet, um Regeln zum Senden von Seitendaten an Adobe Analytics zu erstellen.

[Sehen Sie sich das Tutorial hier an.](https://docs.adobe.com/content/help/de-DE/experience-manager-learn/sites/integrations/analytics/collect-data-analytics.html)

### Verfolgen geklickter Komponenten mit Adobe Analytics {#track-clicked-components}

Verwenden Sie die ereignisbasierte Adobe Client-Datenschicht mit den AEM-Kernkomponenten, um Klicks auf bestimmte Komponenten auf einer Adobe Experience Manager-Site zu verfolgen. Erfahren Sie, wie Sie Regeln in Experience Platform Launch verwenden, um Klick-Ereignisse zu überwachen, nach Komponenten zu filtern und die Daten mit einem Verfolgungs-Linkbeacon an Adobe Analytics zu senden.

[Sehen Sie sich das Tutorial hier an.](https://docs.adobe.com/content/help/de-DE/experience-manager-learn/sites/integrations/analytics/track-clicked-component.html)
