---
title: Verwenden der Adobe Client-Datenschicht mit den Kernkomponenten
description: Verwenden der Adobe Client-Datenschicht mit den Kernkomponenten
translation-type: tm+mt
source-git-commit: 539a4250c954ac830731a9ecf010e129b2cf9c3a
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 3%

---


# Verwenden der Adobe Client-Datenschicht mit den Kernkomponenten {#data-layer-core-components}

Ziel der Adobe Client Data Layer ist es, den Aufwand für die Instrumentierung von Websites zu verringern, indem eine standardisierte Methode zur Offenlegung und zum Zugriff auf alle Arten von Daten für Skripten bereitgestellt wird.

Die Adobe Client-Datenschicht ist plattformunabhängig, aber vollständig in die Kernkomponenten integriert und kann mit AEM verwendet werden.

Wie die Core-Komponenten ist auch der Code für die Adobe Client-Datenschicht auf GitHub zusammen mit der Entwicklerdokumentation verfügbar. Dieses Dokument gibt einen Überblick darüber, wie die Kernkomponenten mit der Datenschicht interagieren, jedoch werden alle technischen Details der GitHub-Dokumentation zurückgestellt.

>[!TIP]
>
>Weitere Informationen zur Adobe Client-Datenschicht [finden Sie in den Ressourcen in ihrem GitHub-Repository.](https://github.com/adobe/adobe-client-data-layer)
>
>Weitere technische Details zur Integration der Adobe Client-Datenschicht mit den Core-Komponenten finden Sie in der [`DATA_LAYER_INTEGRATION.md`](https://github.com/adobe/aem-core-wcm-components/blob/master/DATA_LAYER_INTEGRATION.md) Datei im Core-Komponenten-Repository.


## Installation und Aktivierung {#installation-activation}

Ab Version 2.9.0 der Core-Komponenten wird die Datenschicht mit den Core-Komponenten als clientlib verteilt. Es ist keine Installation erforderlich.

Die Datenschicht ist jedoch nicht standardmäßig aktiviert. So aktivieren Sie die Datenschicht

1. Erstellen Sie die folgende Struktur unter dem `/conf` Knoten:
   * `/conf/<mySite>/sling:configs/com.adobe.cq.wcm.core.components.internal.DataLayerConfig`
1. Hinzufügen einer booleschen Eigenschaft mit dem Namen `enabled` und legen Sie sie auf `true`.
1. Hinzufügen Sie eine `sling:configRef` Eigenschaft auf den `jcr:content` Knoten Ihrer Site unten `/content` (z. `/content/<mySite>/jcr:content`) und legen Sie es auf `/conf/<mySite>`.

Nach der Aktivierung können Sie die Aktivierung überprüfen, indem Sie eine Seite der Site außerhalb des Editors laden. Wenn Sie die Seite überprüfen, sehen Sie, dass die Adobe Client-Datenschicht geladen wird.

## Schemas zu Hauptkomponenten {#data-schemas}

Im Folgenden finden Sie eine Liste von Schemas, die die Kernkomponenten mit der Datenschicht verwenden.

### Schema für Komponenten/Container {#item}

Das Schema Komponente/Container-Element wird in den folgenden Komponenten verwendet:

* [Breadcrumb](/help/components/breadcrumb.md)
* [Schaltfläche](/help/components/button.md)
* [Sprachnavigation](/help/components/language-navigation.md)
* [Liste](/help/components/list.md)
* [Navigation](/help/components/navigation.md)
* [Teaser](/help/components/teaser.md)
* [Text](/help/components/text.md)
* [Titel](/help/components/title.md)

Das Schema Component/Container Item wird wie folgt definiert.

```
id: {                   // component ID
    @type               // resource type
    repo:modifyDate     // last modified date
    dc:title            // title
    dc:description      // description
    xdm:text            // text
    xdm:linkURL         // link URL
    parentId            // parent component ID
}
```


### Seiten-Schema {#page}

Das Schema &quot;Seite&quot;wird von der folgenden Komponente verwendet:

* [Seite](/help/components/page.md)

Das Schema Seite wird wie folgt definiert.

```
id: {
    @type
    repo:modifyDate
    dc:title
    dc:description
    xdm:text
    xdm:linkURL
    parentId
    xdm:tags            // page tags
    repo:path           // page path
    xdm:template        // page template
    xdm:language        // page language
}
```

### Container-Schema {#container}

Das Container-Schema wird von den folgenden Komponenten verwendet:

* [Akkordeon](/help/components/accordion.md)
* [Registerkarten](/help/components/tabs.md)
* [Karussell](/help/components/carousel.md)

Das Container-Schema wird wie folgt definiert.

```
id: {
    @type
    repo:modifyDate
    dc:title
    dc:description
    xdm:text
    xdm:linkURL
    parentId
    shownItems          // array of the displayed item IDs
}
```

### Image-Schema {#image}

Das Image-Schema wird von der folgenden Komponente verwendet:

* [Image](/help/components/image.md)

Das Image-Schema wird wie folgt definiert:

```
id: {
    @type
    repo:modifyDate
    dc:title
    dc:description
    xdm:text
    xdm:linkURL
    parentId
    image               // asset detail (see below section)
}
```

### Asset-Schema {#asset}

Das Asset-Schema wird innerhalb der [Image-Komponente verwendet.](/help/components/image.md)

Das Asset-Schema ist wie folgt definiert.

```
id: {
    repo:id             // asset UUID
    repo:path           // asset path
    @type               // asset resource type
    xdm:tags            // asset tags
    repo:modifyDate
}
```

