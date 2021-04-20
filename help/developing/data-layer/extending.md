---
title: Erweitern der Adobe Client-Datenschicht
description: Die Adobe Client-Datenschicht kann nach anhand von grundlegenden Mustern erweitert werden
feature: Core Components, Adobe Client Data Layer
role: Architect, Developer, Administrator
translation-type: ht
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: ht
source-wordcount: '285'
ht-degree: 100%

---


# Erweitern der Adobe Client-Datenschicht {#extending-acdl}

Sie können die Kernkomponenten mit benutzerdefinierten Dialogoptionen erweitern, mit denen Content-Autoren zusätzliche Informationen zur Datenschicht eingeben können.

Um diese Felder in die Datenschicht einzuschließen, die von den Kernkomponenten bereitgestellt wird, müssen Sie das Modell der Komponente erweitern, das eigene spezifische Datenschichtmethoden implementiert.

## Beispiel: Titelkomponente {#example}

Eine Kernomponente wie die [Titelkomponente](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/models/Title.java) erweitert die [Komponente](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/models/Title.java), die über eine `getData`-Methode verfügt, die standardmäßig [`ComponentData` zurückgibt.](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/models/datalayer/ComponentData.java)

`ComponentData` serialisiert vordefinierte Felder, die Ihre Komponente implementieren kann, z. B. `getDataLayerLinkUrl` und `getDataLayerTitle` für [`TitleImpl`.](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/internal/models/v1/TitleImpl.java)

Daher verfügt Ihr benutzerdefiniertes Sling-Modell möglicherweise über eine `getData`-Methode, die ein Objekt zurückgibt, das `ComponentData` so erweitert, dass weitere Felder zurückgegeben werden.

Hierdurch wird dem HTML-Element Ihrer Komponente ein `data-cmp-data-layer`-Attribut hinzugefügt mit dem JSON der Daten, die in die Datenschicht eingefügt werden. An dieser Stelle können Sie Skripte implementieren, die nach diesen Daten oder verwandten Ereignissen suchen.

>[!TIP]
>
>Um die Flexibilität der Datenschicht weiter zu untersuchen, sollten Sie sich mit den Integrationsoptionen vertraut machen, einschließlich der Aktivierung der Datenschicht für Ihre benutzerdefinierten Komponenten.
