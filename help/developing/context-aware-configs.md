---
title: Sling Context-Aware-Konfigurationen und Kernkomponenten
description: Die Kernkomponenten nutzen kontextbezogene Sling-Konfigurationen für bestimmte Funktionen
translation-type: tm+mt
source-git-commit: 24a810ff634f8846881dfa0095e879476d0f16f0
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 12%

---


# Sling Context-Aware-Konfigurationen und Kernkomponenten {#sling-context-aware-configurations}

Kontextsensitive Konfigurationen sind eine Funktion von Sling und sind Konfigurationen, die sich auf eine Inhaltsressource oder eine Ressourcenstruktur beziehen und von den Core-Komponenten genutzt werden, um siteweite Konfigurationen zu ermöglichen.

## Sling Context-Aware-Konfigurationen {#context-aware-configurations}

Ihre Site benötigt möglicherweise unterschiedliche Konfigurationen für verschiedene Sitebereiche, z. B. wenn einige Parameter freigegeben werden, die eine Vererbung für verschachtelte Kontexte und globale Ausweichwerte erfordern. Sling-kontextabhängige Konfigurationen aktivieren dies.

Ausführliche Informationen zu kontextsensitiven Sling-Konfigurationen [finden Sie in der Apache-Dokumentation.](https://sling.apache.org/documentation/bundles/context-aware-configuration/context-aware-configuration.html)

## Use in the Core Components {#core-components}

Eine Reihe von Kernkomponenten-Funktionen nutzen kontextsensitive Konfigurationen. Alle derartigen Konfigurationen befinden sich unter dem folgenden Knoten:

* `/conf/<my-site>/sling:configs/<my-configuration>`

Die einzelnen Konfigurationen hängen von der jeweiligen Komponente oder Funktion ab. Die Kernkomponenten, die kontextsensitive Konfigurationen verwenden, umfassen folgende Funktionen:

* [PDF-Viewer-Komponente](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/pdfviewer/v1/pdfviewer#context-aware-config)
* [Adobe Client-Datenschicht](/help/developing/data-layer/overview.md#installation-activation)
* [AMP-Unterstützung](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)
