---
title: Kontextabhängige Konfigurationen von Sling und Kernkomponenten
description: Die Kernkomponenten nutzen kontextabhängige Konfigurationen von Sling für bestimmte Funktionen
role: Developer, Admin
exl-id: d35210f7-a65d-4768-ab9e-f12ec406da2d
TQID: https://experienceleague.adobe.com/jCBeHjuqLJzIxggeZxpusUkv9ZAyE-Ktr5N-gakWK18
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 73aa5234ac63fa3be99feebce448bb6722513838
workflow-type: tm+mt
source-wordcount: 257
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
