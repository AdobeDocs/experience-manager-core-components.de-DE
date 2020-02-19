---
title: Inhaltsfragment-Komponente
description: Die Kernkomponente „Inhaltsfragment-Komponente“ ermöglicht die Anzeige eines Inhaltsfragments.
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# Inhaltsfragment-Komponente{#content-fragment-component}

The Core Component Content Fragment component allows for the display of a [content fragment](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/content-fragments/content-fragments.html).

>[!NOTE]
>
>Vor Version 2.4.0 der Kernkomponenten war die Komponente „Inhaltsfragment“ als Erweiterung für die Kernkomponenten verfügbar und musste separat heruntergeladen und explizit aktiviert werden.

## Nutzung {#usage}

The Core Component Content Fragment Component allows for the inclusion of a [content fragment](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/content-fragments/content-fragments.html) on a page.

* Das Fragment und seine Eigenschaften können im [Dialogfeld „Konfigurieren“](#configure-dialog) ausgewählt werden.
* Ressourcentypen zum Verarbeiten bestimmter Bilder und Raster können im [Dialogfeld „Design“](#design-dialog) definiert werden.
* Mit der Option &quot;Bearbeiten&quot;wird das ausgewählte Fragment im [Inhaltsfragmenteditor](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/content-fragments/content-fragments-variations.html)geöffnet.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Inhaltsfragment-Komponente ist v1, die mit Version 1.1.0 der Kernkomponenten im Oktober 2017 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.3 | AEM 6.4 | AEM 6.5 | AEM als Cloud Service |
|--- |--- |--- |---|---|
| v1 | Kompatibel | Kompatibel | Kompatibel | Kompatibel |

>[!NOTE]
>
>Vor Version 2.4.0 befand sich die Inhaltsfragment-Komponente im Erweiterungsordner.
>
> `apps/core/wcm/extension/components/contentfragment/v1/contentfragment`
> 
>Ab 2.4.0 wurde sie an den folgenden Speicherort verschoben.
>
>`apps/core/wcm/components/contentfragment/v1/contentfragment`
>
>Obwohl es sich bei beiden um v1 handelt, erfordert jede aus dem Erweiterungsordner verwendete Inhaltsfragment-Komponente eine Migration der zugehörigen Proxy-Komponenten, um den neuen Ressourcentyp bei der Aktualisierung auf Version 2.4.0 oder höher der Kernkomponenten zu verwenden.

Weitere Informationen zu Kernkomponentenversionen und -freigaben finden Sie in den [Kernkomponentenversionen](/help/versions.md).

## Musterkomponentenausgabe {#sample-component-output}

To experience the Content Fragment Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_cf).

## Technische Details {#technical-details}

The latest technical documentation about the Content Fragment Component [can be found on GitHub](https://adobe.com/go/aem_cmp_tech_cf_v1).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Über das Dialogfeld „Konfigurieren“ kann der Inhaltsautor das gewünschte Inhaltsfragment und die zu verwendenden Elemente dieses Fragments definieren.

![](/help/assets/chlimage_1-87.png)

* **Inhaltsfragment**

   * Pfad zum gewünschten Inhaltsfragment
   * Das **Dialogfeld „Auswahl“** kann zum Suchen des Fragments verwendet werden.

* **Element** - Das Element des Inhaltsfragments, das eingefügt werden soll
* **Variation** - Welche Variante des Inhaltsfragments zu verwenden ist (standardmäßig **Master**)

* **Absätze**

   * **Alle** - Alle Absätze anzeigen
   * **Bereich**

      * Festlegen von Bereichen der anzuzeigenden Absätze, durch ein Semikolon getrennt
      * So können Sie z. B. mit `1;3-5;7;9-*` den 1., den 3. bis 5., den 7. und den 9. bis zum letzten Absatz einbeziehen.

* **Überschriften als separate Absätze behandeln**

## Dialogfeld „Design“ {#design-dialog}

Das Dialogfeld „Design“ ermöglicht es dem Vorlagenautor, die Ressourcentypen zu definieren, mit denen gemischte Medienbilder und responsive Raster verarbeitet werden.

![](/help/assets/chlimage_1-88.png)

* **Bildtyp für gemischte Medien**

   * Ein Sling-Ressourcentyp, der für das Rendern von Bildern mit gemischten Medien verwendet wird.

* **Internes responsives Raster**

   * Der Sling-Ressourcentyp, der für das interne responsive Raster verwendet wird

