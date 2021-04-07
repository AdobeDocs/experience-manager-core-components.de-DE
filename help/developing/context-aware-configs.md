---
title: Kontextabhängige Konfigurationen von Sling und Kernkomponenten
description: Die Kernkomponenten nutzen kontextabhängige Konfigurationen von Sling für bestimmte Funktionen
role: Architekt, Entwickler, Administrator
translation-type: ht
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: ht
source-wordcount: '203'
ht-degree: 100%

---


# Kontextabhängige Konfigurationen von Sling und Kernkomponenten {#sling-context-aware-configurations}

Kontextabhängige Konfigurationen sind eine [Funktion von Sling](https://sling.apache.org/documentation/bundles/context-aware-configuration/context-aware-configuration.html). Es handelt sich um Konfigurationen, die sich auf eine Inhaltsressource oder eine Ressourcenstruktur beziehen und von den Kernkomponenten genutzt werden, um Site-übergreifende Konfigurationen zu ermöglichen.

## Kontextabhängige Konfigurationen von Sling {#context-aware-configurations}

Ihre Site benötigt möglicherweise unterschiedliche Konfigurationen für verschiedene Site-Bereiche, z. B. wenn einige Parameter freigegeben werden, die eine Vererbung für verschachtelte Kontexte und globale Ausweichwerte erfordern. AEM nutzt kontextabhängige Sling-Konfigurationen, die dies ermöglichen.

Weitere Informationen zu Konfigurationen in AEM finden Sie in der [Dokumentation zu Konfigurationen und Konfigurations-Browser](https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/implementing/developing/configurations.html).

## Verwendung in den Kernkomponenten {#core-components}

Eine Reihe von Kernkomponenten-Funktionen nutzen kontextabhängige Konfigurationen. Alle derartigen Konfigurationen befinden sich unter folgendem Knoten:

* `/conf/<my-site>/sling:configs/<my-configuration>`

Die einzelnen Konfigurationen hängen von der jeweiligen Komponente oder Funktion ab. Folgende Funktionen der Kernkomponenten verwenden kontextabhängige Konfigurationen:

* [PDF-Viewer-Komponente](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/pdfviewer/v1/pdfviewer#context-aware-config)
* [Adobe Client-Datenschicht](/help/developing/data-layer/overview.md#installation-activation)
* [AMP-Unterstützung](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)
