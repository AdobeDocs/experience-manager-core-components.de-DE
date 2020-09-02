---
title: Erweitern der Adobe Client-Datenschicht
description: Die Adobe Client-Datenschicht kann nach einigen grundlegenden Mustern erweitert werden
translation-type: tm+mt
source-git-commit: 896ed679ed3351cb309a34b38bf97fe81adc2cfe
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 0%

---


# Erweitern der Adobe Client-Datenschicht {#extending-acdl}

Sie können die Kernkomponenten mit benutzerdefinierten Dialogoptionen erweitern, mit denen Autoren von Inhalten zusätzliche Informationen zur Datenschicht eingeben können.

Um diese Felder in die Datenschicht einzuschließen, die von den Core-Komponenten bereitgestellt wird, müssen Sie das Modell der Komponente erweitern, die eigene spezifische Datenschichtmethoden implementiert.

## Beispiel: Titelkomponente {#example}

Eine Core-Komponente wie die [Title-Komponente](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/models/Title.java) erweitert die [Komponente](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/models/Title.java) , die eine `getData` Methode besitzt, die standardmäßig zurückgibt [`ComponentData`.](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/models/datalayer/ComponentData.java)

`ComponentData` serialisiert vordefinierte Felder, die Ihre Komponente implementieren kann, z. B. `getDataLayerLinkUrl` und `getDataLayerTitle` für die [`TitleImpl`.](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/internal/models/v1/TitleImpl.java)

Daher verfügt Ihr benutzerdefiniertes Sling-Modell möglicherweise über eine `getData` Methode, die ein Objekt zurückgibt, das erweitert wird, um weitere Felder zurückzugeben `ComponentData` .

Hierdurch wird dem HTML-Element Ihrer Komponente ein `data-cmp-data-layer` Attribut mit dem JSON der Daten, die in die Datenschicht eingefügt werden, hinzugefügt. An dieser Stelle können Sie Skripten implementieren, die auf diese Daten oder verwandte Ereignis hören.
