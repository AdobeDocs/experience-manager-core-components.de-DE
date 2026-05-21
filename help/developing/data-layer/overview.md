---
title: Verwenden der Adobe Client-Datenschicht in Verbindung mit den Kernkomponenten
description: Verwenden der Adobe Client-Datenschicht in Verbindung mit den Kernkomponenten
feature: Core Components, Adobe Client Data Layer
role: Developer, Admin
exl-id: 55c984d3-deb7-4eda-a81d-7768791d2b46
TQID: https://experienceleague.adobe.com/CwXfehtriHzjTKA7cCwCb0HCcAWTm5I49UF3x3rrc3c
product_v2: id: c45915cf-e157-4af7-a80d-97b905bcb3a5id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: ae478996-b206-4712-9b0c-dc78a2644453id: c124fa01-25c5-42ec-adf6-21d1c114058bid: d429a63e-ade4-4117-b04e-9b996d1c94efid: f2d27a5f-0d67-4d85-8a24-86a8d8a3574b
subfeature_v2: id: a0ab86ed-7176-40e5-bccb-a2cc1295200cid: a94e5c13-4138-47ec-b9c8-e804e17aaca2id: ca9acb56-1fd9-4553-930f-d71ab7d4045did: cd14456d-a492-4b5c-8a82-1fbd4460dbd2id: f88183b7-5ea5-436c-ac46-96b53f0281ea
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 73aa5234ac63fa3be99feebce448bb6722513838
workflow-type: tm+mt
source-wordcount: 1024
ht-degree: 100%

---

# Verwenden der Adobe Client-Datenschicht in Verbindung mit den Kernkomponenten {#data-layer-core-components}

Ziel der Adobe Client-Datenschicht ist es, für beliebige Skripte anhand einer standardisierten Methode für die Bereitstellung und den Zugriff auf alle Arten von Daten den Aufwand für die Instrumentierung von Websites zu reduzieren.

Die Adobe Client-Datenschicht ist plattformunabhängig, aber für die Verwendung mit AEM vollständig in die Kernkomponenten integriert.

Wie auch die Kernkomponenten ist der Code für die Adobe Client-Datenschicht auf GitHub zusammen mit der zugehörigen Entwicklerdokumentation verfügbar. Das vorliegende Dokument gibt einen Überblick darüber, wie die Kernkomponenten mit der Datenschicht interagieren, für vollständige technische Details ist jedoch die Dokumentation auf GitHub zu konsultieren.

>[!TIP]
>
>Weitere Informationen zur Adobe Client-Datenschicht finden Sie in den Ressourcen des entsprechenden [GitHub-Repositorys.](https://github.com/adobe/adobe-client-data-layer)
>
>Weitere technische Details zur Integration der Adobe Client-Datenschicht mit den Kernkomponenten finden Sie in der Datei [`DATA_LAYER_INTEGRATION.md`](https://github.com/adobe/aem-core-wcm-components/blob/master/DATA_LAYER_INTEGRATION.md) im Kernkomponenten-Repository.

{{traditional-aem}}

## Installation und Aktivierung {#installation-activation}

Ab Version 2.9.0 der Kernkomponenten ist die Datenschicht als AEM-Client-Bibliothek in den Kernkomponenten enthalten und muss nicht installiert werden. Alle vom [AEM-Projektarchetyp ab Version 24](/help/developing/archetype/overview.md) generierten Projekte enthalten standardmäßig eine aktivierte Datenschicht.

Um die Datenschicht manuell zu aktivieren, müssen Sie eine [kontextabhängige Konfiguration](/help/developing/context-aware-configs.md) dafür erstellen:

1. Erstellen Sie die folgende Struktur unter dem Ordner `/conf/<mySite>`, wobei `<mySite>` für den Namen des Projekts für Ihre Site steht:
   * `/conf/<mySite>/sling:configs/com.adobe.cq.wcm.core.components.internal.DataLayerConfig`
   * Jeder Knoten hat einen Wert `jcr:primaryType`, der auf `nt:unstructured` eingestellt ist.
1. Fügen Sie eine boolesche Eigenschaft mit dem Namen `enabled` hinzu und legen Sie sie auf `true` fest.

   ![Position von DataLayerConfig auf der WKND-Referenz-Site](/help/assets/datalayer-contextaware-sling-config.png)

   *Position von DataLayerConfig auf der WKND-Referenz-Site*

1. Fügen Sie eine `sling:configRef`-Eigenschaft zum Knoten `jcr:content` Ihrer Site hinzu, dies unterhalb von `/content` (z. B. `/content/<mySite>/jcr:content`), und legen Sie für sie `/conf/<mySite>` fest.

1. Nach der Aktivierung können Sie diese überprüfen, indem Sie eine Seite der Site außerhalb des Editors laden, z. B. mit der Option **Als veröffentlicht anzeigen** im Editor. Überprüfen Sie die Seitenquelle. Das Tag `<body>` sollte das Attribut `data-cmp-data-layer-enabled` enthalten.

   ```html
   <body class="page basicpage" id="page-id" data-cmp-data-layer-enabled>
       <script>
         window.adobeDataLayer = window.adobeDataLayer || [];
         adobeDataLayer.push({
             page: JSON.parse("{\x22page\u002D6c5d4b9fdd\x22:{\x22xdm:language\x22:\x22en\x22,\x22repo:path\x22:\x22\/content\/wknd\/language\u002Dmasters\/en.html\x22,\x22xdm:tags\x22:[],\x22xdm:template\x22:\x22\/conf\/wknd\/settings\/wcm\/templates\/landing\u002Dpage\u002Dtemplate\x22,\x22@type\x22:\x22wknd\/components\/page\x22,\x22dc:description\x22:\x22WKND is a collective of outdoors, music, crafts, adventure sports, and travel enthusiasts that want to share our experiences, connections, and expertise with the world.\x22,\x22dc:title\x22:\x22WKND Adventures and Travel\x22,\x22repo:modifyDate\x22:\x222020\u002D09\u002D29T07:50:13Z\x22}}"),
             event:'cmp:show',
             eventInfo: {
                 path: 'page.page\u002D6c5d4b9fdd'
             }
         });
       </script>
   ```

1. Sie können auch die Entwickler-Tools des Browsers öffnen. Das JavaScript-Objekt `adobeDataLayer` sollte verfügbar sein. Geben Sie den folgenden Befehl ein, um den Status der Datenschicht der aktuellen Seite abzurufen:

   ```javascript
   window.adobeDataLayer.getState();
   ```

## Unterstützte Komponenten {#supported-components}

Die folgenden Komponenten unterstützen die Datenschicht.

* [Akkordeon](/help/components/accordion.md)
* [Breadcrumb](/help/components/breadcrumb.md)
* [Schaltfläche](/help/components/button.md)
* [Karussell](/help/components/carousel.md)
* [Inhaltsfragment](/help/components/content-fragment-component.md)
* [Bild](/help/components/image.md)
* [Sprachnavigation](/help/components/language-navigation.md)
* [Liste](/help/components/list.md)
* [Navigation](/help/components/navigation.md)
* [Seite](/help/components/page.md)
* [Fortschrittsleiste](/help/components/progress-bar.md)
* [Registerkarten](/help/components/tabs.md)
* [Teaser](/help/components/teaser.md)
* [Text](/help/components/text.md)
* [Titel](/help/components/title.md)

Siehe auch die [von den Komponenten ausgelösten Ereignisse](#events-components).

## Datenschemata der Kernkomponenten {#data-schemas}

Nachfolgend sind die Schemas aufgeführt, die die Kernkomponenten in Verbindung mit der Datenschicht verwenden.

### Komponenten-/Container-Element-Schema {#item}

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

```javascript
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

>[!NOTE]
>
>Dieses Schema ist das generische Komponentenelementschema, das als Basismuster für mehrere Kernkomponenten verwendet wird. Dies garantiert nicht, dass jede aufgelistete Komponente alle diese Felder bei jedem Element ausfüllt.

Das folgende [Ereignis](#events) ist für das Komponenten-/Container-Element-Schema relevant:

* `cmp:click`

### Seiten-Schema {#page}

Das Seiten-Schema wird von der folgenden Komponente verwendet:

* [Seite](/help/components/page.md)

Das Seiten-Schema wird wie folgt definiert:

```javascript
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

Beim Laden der Seite wird ein `cmp:show`-Ereignis ausgelöst. Dieses Ereignis wird vom Inline-JavaScript direkt unterhalb des öffnenden `<body>`-Tags ausgelöst und ist damit das früheste Ereignis in der Ereignisschlange „Datenschicht“.

### Container-Schema {#container}

Das Container-Schema wird von den folgenden Komponenten verwendet:

* [Akkordeon](/help/components/accordion.md)
* [Registerkarten](/help/components/tabs.md)
* [Karussell](/help/components/carousel.md)

Das Container-Schema wird wie folgt definiert:

```javascript
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

Die folgenden [Ereignisse](#events) sind für das Container-Schema relevant:

* `cmp:click`
* `cmp:show`
* `cmp:hide`

### Bild-Schema {#image}

Das Bild-Schema wird von der folgenden Komponente verwendet:

* [Bild](/help/components/image.md)

Das Bild-Schema wird wie folgt definiert:

```javascript
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

Das folgende [Ereignis](#events) ist für das Bild-Schema relevant:

* `cmp:click`

### Asset-Schema {#asset}

Das Asset-Schema wird innerhalb der [Bild-Komponente](/help/components/image.md) verwendet:

Das Asset-Schema wird wie folgt definiert:

```javascript
id: {
    repo:id             // asset UUID
    repo:path           // asset path
    @type               // asset resource type
    xdm:tags            // asset tags
    repo:modifyDate
}
```

Das folgende [Ereignis](#events) ist für das Asset-Schema relevant:

* `cmp:click`

### Inhaltsfragment-Schema {#content-fragment}

Das Inhaltsfragment-Schema wird von der [Inhaltsfragment-Komponente](/help/components/content-fragment-component.md) verwendet.

Das Inhaltsfragment-Schema ist wie folgt definiert:

```javascript
id: {
    @type
    repo:modifyDate
    dc:title
    dc:description
    xdm:text
    xdm:linkURL
    parentId
    elements            // array of the Content Fragment elements
}
```

Das für das Inhaltsfragment-Element verwendete Schema lautet wie folgt:

```javascript
{
    xdm:title           // title
    xdm:text            // text
}
```

## Kernkomponenten-Ereignisse {#events}

Es gibt eine Reihe von Ereignissen, die Kernkomponenten über die Datenschicht auslösen. Die Best Practice für die Interaktion mit der Datenschicht besteht darin, [einen Ereignis-Listener zu registrieren](https://github.com/adobe/adobe-client-data-layer/wiki#addeventlistener) und *dann* eine Aktion auf Grundlage des Ereignistyps und/oder der Komponente zu ergreifen, die das Ereignis ausgelöst hat. Dadurch werden potenzielle Überschneidungen mit asynchronen Skripten vermieden.

Im Folgenden finden Sie die vorkonfigurierten Ereignisse in den AEM-Kernkomponenten:

* **`cmp:click`**: Beim Klicken auf ein klickbares Element (ein Element mit einem `data-cmp-clickable`-Attribut) löst die Datenschicht ein `cmp:click`-Ereignis aus.
* **`cmp:show`** und **`cmp:hide`**: Beim Manipulieren des Akkordeon (Erweitern/Reduzieren), des Karussells (nächste/vorherige Schaltflächen) und der Registerkarten (Registerkartenauswahl) löst die Datenschicht ein `cmp:show`- bzw. ein `cmp:hide`-Ereignis aus. Ein `cmp:show`-Ereignis wird auch beim Laden der Seite ausgelöst und wird als erstes Ereignis erwartet.
* **`cmp:loaded`**: Sobald die Datenschicht mit den Kernkomponenten auf der Seite gefüllt ist, löst die Datenschicht ein `cmp:loaded`-Ereignis aus.

### Ausgelöste Ereignisse nach Komponente {#events-components}

In den folgenden Tabellen sind die standardmäßigen Kernkomponenten, die Ereignisse auslösen, zusammen mit diesen Ereignissen aufgeführt.

| Komponente | Ereignis(se) |
|---|---|
| [Akkordeon](/help/components/accordion.md) | `cmp:show` und `cmp:hide` |
| [Schaltfläche](/help/components/button.md) | `cmp:click` |
| [Breadcrumb](/help/components/breadcrumb.md) | `cmp:click` |
| [Karussell](/help/components/carousel.md) | `cmp:show` und `cmp:hide` |
| [Sprachnavigation](/help/components/language-navigation.md) | `cmp:click` |
| [Navigation](/help/components/navigation.md) | `cmp:click` |
| [Seite](/help/components/page.md) | `cmp:show` |
| [Registerkarten](/help/components/tabs.md) | `cmp:show` und `cmp:hide` |
| [Teaser](/help/components/teaser.md) | `cmp:click` |

### Ereignis-Pfadinformationen {#event-path-info}

Jedes Datenschicht-Ereignis, das von einer AEM-Kernkomponente ausgelöst wird, enthält eine Payload mit dem folgenden JSON-Objekt:

```json
eventInfo: {
    path: '<component-path>'
}
```

Bei `<component-path>` handelt es sich um den JSON-Pfad zur Komponente in der Datenschicht, die das Ereignis ausgelöst hat.  Der Wert, der über `event.eventInfo.path` verfügbar ist, ist wichtig, da er als für `adobeDataLayer.getState(<component-path>)` verwendet werden kann, das den aktuellen Status der Komponente abruft, die das Ereignis ausgelöst hat. So kann benutzerdefinierter Code auf zusätzliche Daten zugreifen und sie der Datenschicht hinzufügen.

Beispiel:

```javascript
function logEventObject(event) {
    if(event.hasOwnProperty("eventInfo") && event.eventInfo.hasOwnProperty("path")) {
        var dataObject = window.adobeDataLayer.getState(event.eventInfo.path);
        console.debug("The component that triggered this event: ");
        console.log(dataObject);
    }
}

window.adobeDataLayer = window.adobeDataLayer || [];
window.adobeDataLayer.push(function (dl) {
     dl.addEventListener("cmp:show", logEventObject);
});
```

## Tutorial

Möchten Sie mehr über die Datenschicht und die Kernkomponenten erfahren? [Sehen Sie sich dieses praxisorientierte Tutorial an.](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/integrations/adobe-client-data-layer/data-layer-overview.html?lang=de)

>[!TIP]
>
>Um die Flexibilität der Datenschicht weiter zu untersuchen, sollten Sie sich mit den Integrationsoptionen vertraut machen, einschließlich der Aktivierung der Datenschicht für Ihre benutzerdefinierten Komponenten.
