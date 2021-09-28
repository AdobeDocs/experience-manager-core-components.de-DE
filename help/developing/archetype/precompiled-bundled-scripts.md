---
title: Vorkompilierte Bundle-Skripte
description: Erfahren Sie, wie Sie Ihre Komponentenskripte über OSGi-Bundles auf Adobe Experience Manager Cloud Service bereitstellen.
source-git-commit: 56464decc8d6ae3cef68d62bfe459bceda0539ef
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 0%

---

# Vorkompilierte Bundle-Skripte

AEM as a Cloud Service unterstützt die Bereitstellung der [`ui.apps`](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html#code-packages-%2F-osgi-bundles)-Komponentenskripte als vorkompilierte gebündelte Skripte. Dadurch können Entwickler ihre Skripte zur Build-Zeit vorkompilieren und als OSGi-Pakete verpacken.

## Vorteile der Bereitstellung vorkompilierter Skripte über OSGi-Bundles

Die Bereitstellung Ihrer Skripte als vorkompilierte gebündelte Skripte bietet die folgenden Vorteile:

+ Das Kompilieren von Skripten zur Build-Zeit ermöglicht es Entwicklern, Fehler frühzeitig im Entwicklungsprozess zu erkennen
+ Java-API-Skriptabhängigkeiten werden explizit über die Bundle-Header `Import-Package` und `Export-Package` definiert
+ Vererbung (über `sling:resourceSuperType`) und Zuweisung zu anderen Ressourcentypen (z. B. über das `data-sly-resource`-Blockelement der HTL oder über das `sling:include`-JSP-Tag) können über die Metadaten des Bundles zugeordnet werden
+ Die Versionierung von Ressourcentypen kann auf ähnliche Weise erzwungen werden wie die Java-APIs

## Vorkompilierung und Package-Importe

Die [`htl-maven-plugin`](https://sling.apache.org/components/htl-maven-plugin/index.html) kann die Syntax von HTL-Skripten überprüfen, kann aber auch verwendet werden, um die HTL-Skripte in Java-Klassen zu übertragen. Diese werden dann zum Ordner `generated-sources` Ihres Maven-Projekts hinzugefügt und vom Ordner `maven-compiler-plugin` abgerufen.

[`bnd-maven-plugin`](https://github.com/bndtools/bnd/tree/master/maven/bnd-maven-plugin) kann hinzugefügt werden, um die Metadaten des OSGi-Bundles für Java-API-Importe zu generieren.

## Vererbung und Delegation

Das OSGi-Framework bietet eine leistungsstarke Möglichkeit, [Anforderungen und Funktionen](https://docs.osgi.org/specification/osgi.core/7.0.0/framework.module.html#framework.module.dependencies) zu definieren, um Verträge zwischen verschiedenen Komponenten auszudrücken. Diese werden über Metadaten beschrieben und zur Laufzeit erzwungen. Gebündelte Skripte verwenden diesen Mechanismus, um sowohl ihre Vererbungsbeziehungen (`sling:resourceSuperType`) als auch ihre Delegierung (einschließlich anderer Ressourcentypen im Rendering-Prozess) auszudrücken.

Das `bnd`-Plug-in aus dem Projekt [scriptingbundle-maven-plugin](https://sling.apache.org/components/scriptingbundle-maven-plugin/bnd.html) kann verwendet werden, um die Anforderungen und Funktionen zu extrahieren, die den Skripten entsprechen, die vom Inhaltspaket [`ui.apps`](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html#code-packages-%2F-osgi-bundles) bereitgestellt werden.

## Unterstützung AEM Projektarchetyps

Ab Version 31 kann der Projektarchetyp [AEM](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/developing/archetype/using.html) verwendet werden, um ein AEM als Cloud Service-Projekt korrekt einzurichten und vorkompilierte Skripte zu verwenden. Darüber hinaus konfiguriert der AEM Projektarchetyp das [AEM als Cloud Service-SDK Build Analyzer-Maven-Plug-in](/help/developing/archetype/build-analyzer-maven-plugin.md), um die Abhängigkeiten auf Java-Paketebene sowie auf Skriptebene zu überprüfen.
