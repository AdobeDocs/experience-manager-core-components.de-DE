---
title: Erweitern der Adobe Client-Datenschicht
description: Die Adobe Client-Datenschicht kann nach anhand von grundlegenden Mustern erweitert werden
feature: Core Components, Adobe Client Data Layer
role: Developer, Admin
exl-id: f3d5555b-4f08-49de-ab0f-dc0fb04aadf8
TQID: https://experienceleague.adobe.com/67YSpRfwNRMDgcBARHKLz51-Er6xb4vp1rXX0r0sbfE
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 73aa5234ac63fa3be99feebce448bb6722513838
workflow-type: tm+mt
source-wordcount: 289
ht-degree: 100%

---

# Erweitern der Adobe Client-Datenschicht {#extending-acdl}

Sie können die Kernkomponenten mit benutzerdefinierten Dialogoptionen erweitern, mit denen Content-Autoren zusätzliche Informationen zur Datenschicht eingeben können.

Um diese Felder in die Datenschicht einzuschließen, die von den Kernkomponenten bereitgestellt wird, müssen Sie das Modell der Komponente erweitern, das eigene spezifische Datenschichtmethoden implementiert.

## Beispiel: Titelkomponente {#example}

Eine Kernkomponente wie die [Titelkomponente](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/models/Title.java) erweitert die [Komponente](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/models/Title.java), die über eine `getData`-Methode verfügt, die standardmäßig [`ComponentData` zurückgibt.](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/models/datalayer/ComponentData.java)

`ComponentData` serialisiert vordefinierte Felder, die Ihre Komponente implementieren kann, z. B. `getDataLayerLinkUrl` und `getDataLayerTitle` für [`TitleImpl`.](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/internal/models/v1/TitleImpl.java)

Daher verfügt Ihr benutzerdefiniertes Sling-Modell möglicherweise über eine `getData`-Methode, die ein Objekt zurückgibt, das `ComponentData` so erweitert, dass weitere Felder zurückgegeben werden.

Hierdurch wird dem HTML-Element Ihrer Komponente ein `data-cmp-data-layer`-Attribut hinzugefügt mit dem JSON der Daten, die in die Datenschicht eingefügt werden. An dieser Stelle können Sie Skripte implementieren, die nach diesen Daten oder verwandten Ereignissen suchen.

>[!TIP]
>
>Um die Flexibilität der Datenschicht weiter zu untersuchen, sollten Sie sich mit den Integrationsoptionen vertraut machen, einschließlich der Aktivierung der Datenschicht für Ihre benutzerdefinierten Komponenten.
