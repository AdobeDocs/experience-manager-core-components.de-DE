---
title: Kontextabhängige Konfigurationen von Sling und Kernkomponenten
description: Die Kernkomponenten nutzen kontextabhängige Konfigurationen von Sling für bestimmte Funktionen
role: Architect, Developer, Admin
exl-id: d35210f7-a65d-4768-ab9e-f12ec406da2d
source-git-commit: b72defe1bbe6cb286730ac3f508f7d6c14b3fc33
workflow-type: ht
source-wordcount: '174'
ht-degree: 100%

---

# Kontextabhängige Konfigurationen von Sling und Kernkomponenten {#sling-context-aware-configurations}

Kontextabhängige Konfigurationen sind eine [Funktion von Sling](https://sling.apache.org/documentation/bundles/context-aware-configuration/context-aware-configuration.html). Es handelt sich um Konfigurationen, die sich auf eine Inhaltsressource oder eine Ressourcenstruktur beziehen und von den Kernkomponenten genutzt werden, um Site-übergreifende Konfigurationen zu ermöglichen.

## Kontextabhängige Konfigurationen von Sling {#context-aware-configurations}

Ihre Site benötigt möglicherweise unterschiedliche Konfigurationen für verschiedene Site-Bereiche, z. B. wenn einige Parameter freigegeben werden, die eine Vererbung für verschachtelte Kontexte und globale Ausweichwerte erfordern. AEM nutzt kontextabhängige Sling-Konfigurationen, die dies ermöglichen.

Weitere Informationen zu Konfigurationen in AEM finden Sie in der [Dokumentation zu Konfigurationen und Konfigurations-Browser](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/configurations.html?lang=de).

## Verwendung in den Kernkomponenten {#core-components}

Eine Reihe von Kernkomponenten-Funktionen nutzen kontextabhängige Konfigurationen. Alle derartigen Konfigurationen befinden sich unter folgendem Knoten:

* `/conf/<my-site>/sling:configs/<my-configuration>`

Die einzelnen Konfigurationen hängen von der jeweiligen Komponente oder Funktion ab. Folgende Funktionen der Kernkomponenten verwenden kontextabhängige Konfigurationen:

* [Die Seitenkomponente](https://github.com/adobe/aem-core-wcm-components/tree/main/content/src/content/jcr_root/apps/core/wcm/components/page/v3/page#loading-of-context-aware-cssjs) ist beim Rendern von `link`-, `script`- und `meta`-Tags auf eine kontextabhängige Konfiguration angewiesen.
* [PDF-Viewer-Komponente](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/pdfviewer/v1/pdfviewer#context-aware-config)
* [Adobe Client-Datenschicht](/help/developing/data-layer/overview.md#installation-activation)
* [AMP-Unterstützung](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)
