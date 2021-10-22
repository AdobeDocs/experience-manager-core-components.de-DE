---
title: Vorkompilierte Paket-Skripte
description: Erfahren Sie, wie Sie Ihre Komponentenskripte über OSGi-Pakete für Adobe Experience Manager Cloud Service bereitstellen.
exl-id: 3edc388f-01b2-45cc-bd56-f22e5a5a8624
source-git-commit: 767f83fbad11a108aab25be2b77759af3c08b864
workflow-type: ht
source-wordcount: '378'
ht-degree: 100%

---

# Vorkompilierte Paket-Skripte

AEM as a Cloud Service unterstützt die Implementierung der [`ui.apps`](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=de#code-packages-%2F-osgi-bundles)-Komponentenskripte als vorkompilierte Paket-Skripte. Dadurch können Entwickler ihre Skripte zur Build-Zeit vorkompilieren und als OSGi-Pakete verpacken.

## Vorteile der Bereitstellung vorkompilierter Skripte über OSGi-Pakete

Die Bereitstellung Ihrer Skripte als vorkompilierte gebündelte Skripte bietet die folgenden Vorteile:

+ Das Kompilieren von Skripten zur Build-Zeit ermöglicht es Entwicklern, Fehler im Entwicklungsprozess frühzeitig zu erkennen
+ Java-API-Skriptabhängigkeiten werden explizit über die Paket-Header `Import-Package` und `Export-Package` definiert
+ Vererbung (über `sling:resourceSuperType`) und Zuweisung zu anderen Ressourcentypen (z. B. über das `data-sly-resource`-Blockelement der HTL oder über das `sling:include`-JSP-Tag) können über die Metadaten des Pakets zugeordnet werden
+ Die Versionierung von Ressourcentypen kann auf ähnliche Weise erzwungen werden wie bei den Java-APIs

## Vorkompilierung und Package-Importe

Das [`htl-maven-plugin`](https://sling.apache.org/components/htl-maven-plugin/index.html) kann die Syntax von HTL-Skripten überprüfen, es kann aber auch verwendet werden, um die HTL-Skripte in Java-Klassen zu übertragen. Diese werden dann zum Ordner `generated-sources` Ihres Maven-Projekts hinzugefügt und vom `maven-compiler-plugin` abgerufen.

Das [`bnd-maven-plugin`](https://github.com/bndtools/bnd/tree/master/maven/bnd-maven-plugin) kann hinzugefügt werden, um die Metadaten des OSGi-Pakets für Java-API-Importe zu generieren.

## Vererbung und Zuweisung

Das OSGi-Framework bietet eine leistungsstarke Möglichkeit, [Anforderungen und Funktionen](https://docs.osgi.org/specification/osgi.core/7.0.0/framework.module.html#framework.module.dependencies) zu definieren, um Verträge zwischen verschiedenen Komponenten auszudrücken. Diese werden über Metadaten beschrieben und zur Laufzeit erzwungen. Gebündelte Skripte verwenden diesen Mechanismus, um sowohl ihre Vererbungsbeziehungen (`sling:resourceSuperType`) als auch ihre Zuweisung (einschließlich anderer Ressourcentypen im Rendering-Prozess) auszudrücken.

Das `bnd`-Plug-in aus dem Projekt [scriptingbundle-maven-plugin](https://sling.apache.org/components/scriptingbundle-maven-plugin/bnd.html) kann verwendet werden, um die Anforderungen und Funktionen zu extrahieren, die den Skripten entsprechen, die vom Inhaltspaket [`ui.apps`](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=de#code-packages-%2F-osgi-bundles) bereitgestellt werden.

## Unterstützung des AEM-Projektarchetyps

Ab Version 31 kann der [AEM-Projektarchetyp](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/developing/archetype/using.html?lang=de) verwendet werden, um ein AEM as a Cloud Service-Projekt korrekt einzurichten und vorkompilierte gebündelte Skripte zu verwenden. Darüber hinaus konfiguriert der AEM-Projektarchetyp das [AEM as a Cloud Service SDK Build Analyzer Maven-Plug-in](/help/developing/archetype/build-analyzer-maven-plugin.md), um die Abhängigkeiten auf Java-Paket-Ebene sowie auf Skript-Ebene zu überprüfen.
