---
title: Verwenden der Adobe Client-Datenschicht in Verbindung mit den Kernkomponenten
description: Verwenden der Adobe Client-Datenschicht in Verbindung mit den Kernkomponenten
translation-type: ht
source-git-commit: 24a810ff634f8846881dfa0095e879476d0f16f0
workflow-type: ht
source-wordcount: '426'
ht-degree: 100%

---


# Verwenden der Adobe Client-Datenschicht in Verbindung mit den Kernkomponenten {#data-layer-core-components}

Ziel der Adobe Client-Datenschicht ist es, für beliebige Skripte anhand einer standardisierten Methode für die Bereitstellung und den Zugriff auf alle Arten von Daten den Aufwand für die Instrumentierung von Websites zu reduzieren.

Die Adobe Client-Datenschicht ist plattformunabhängig, aber für die Verwendung mit AEM vollständig in die Kernkomponenten integriert.

Wie auch die Kernkomponenten ist der Code für die Adobe Client-Datenschicht auf GitHub zusammen mit der zugehörigen Entwicklerdokumentation verfügbar. Das vorliegende Dokument gibt einen Überblick darüber, wie die Kernkomponenten mit der Datenschicht interagieren, für vollständige technische Details ist jedoch die Dokumentation auf GitHub zu konsultieren.

>[!TIP]
>
>Weitere Informationen zur Adobe Client-Datenschicht finden Sie in den Ressourcen des entsprechenden [GitHub-Repositorys](https://github.com/adobe/adobe-client-data-layer)
>
>Weitere technische Details zur Integration der Adobe Client-Datenschicht mit den Kernkomponenten finden Sie in der Datei [`DATA_LAYER_INTEGRATION.md`](https://github.com/adobe/aem-core-wcm-components/blob/master/DATA_LAYER_INTEGRATION.md) im Kernkomponenten-Repository.

## Installation und Aktivierung {#installation-activation}

Ab Version 2.9.0 der Kernkomponenten wird die Datenschicht zusammen mit den Kernkomponenten als clientlib bereitgestellt. Es ist keine Installation erforderlich.

Die Datenschicht ist jedoch nicht standardmäßig aktiviert. Gehen Sie wie folgt vor, um die Datenschicht zu aktivieren:  Sie müssen dafür eine [kontextabhängige Konfiguration](/help/developing/context-aware-configs.md) erstellen:

1. Erstellen Sie unterhalb des Knotens `/conf` die folgende Struktur:
   * `/conf/<mySite>/sling:configs/com.adobe.cq.wcm.core.components.internal.DataLayerConfig`
   * Knotentyp: `nt:unstructured`
1. Fügen Sie eine boolesche Eigenschaft mit dem Namen `enabled` hinzu und legen Sie sie auf `true` fest.
1. Fügen Sie eine `sling:configRef`-Eigenschaft zum Knoten `jcr:content` Ihrer Site hinzu, dies unterhalb von `/content` (z. B. `/content/<mySite>/jcr:content`), und legen Sie für sie `/conf/<mySite>` fest.

Sie können verifizieren, ob die Aktivierung erfolgreich war, indem Sie eine Seite der Site außerhalb des Editors laden. Durch Überprüfen der Seite können Sie feststellen, dass die Adobe Client-Datenschicht geladen wurde.

## Datenschemas der Hauptkomponenten {#data-schemas}

Nachfolgend sind die Schemas aufgeführt, die die Kernkomponenten in Verbindung mit der Datenschicht verwenden.

### Komponenten-/Container-Element-Schema{#item}

Das Komponenten-/Container-Element-Schema wird in den folgenden Komponenten verwendet:

* [Breadcrumb](/help/components/breadcrumb.md)
* [Schaltfläche](/help/components/button.md)
* [Sprachnavigation](/help/components/language-navigation.md)
* [Liste](/help/components/list.md)
* [Navigation](/help/components/navigation.md)
* [Teaser](/help/components/teaser.md)
* [Text](/help/components/text.md)
* [Titel](/help/components/title.md)

Das Komponenten-/Container-Element-Schema wird wie folgt definiert:

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

Das Seiten-Schema wird von der folgenden Komponente verwendet:

* [Seite](/help/components/page.md)

Das Seiten-Schema wird wie folgt definiert:

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

* [Accordion](/help/components/accordion.md)
* [Registerkarten](/help/components/tabs.md)
* [Karussell](/help/components/carousel.md)

Das Container-Schema wird wie folgt definiert:

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

### Bild-Schema {#image}

Das Bild-Schema wird von der folgenden Komponente verwendet:

* [Bild](/help/components/image.md)

Das Bild-Schema wird wie folgt definiert:

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

Das Asset-Schema wird innerhalb der [Bild-Komponente](/help/components/image.md) verwendet:

Das Asset-Schema wird wie folgt definiert:

```
id: {
    repo:id             // asset UUID
    repo:path           // asset path
    @type               // asset resource type
    xdm:tags            // asset tags
    repo:modifyDate
}
```

