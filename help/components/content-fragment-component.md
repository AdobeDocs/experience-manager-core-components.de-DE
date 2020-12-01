---
title: Inhaltsfragment-Komponente
description: Die Kernkomponente „Inhaltsfragment-Komponente“ ermöglicht die Anzeige eines Inhaltsfragments.
translation-type: tm+mt
source-git-commit: c186e9ec3944d785ab0376769cf7f2307049a809
workflow-type: tm+mt
source-wordcount: '659'
ht-degree: 100%

---


# Inhaltsfragment-Komponente{#content-fragment-component}

Die Kernkomponente „Inhaltsfragment-Komponente“ ermöglicht die Anzeige eines [Inhaltsfragments](https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/assets/content-fragments/content-fragments.translate.html).

>[!NOTE]
>
>Vor Version 2.4.0 der Kernkomponenten war die Komponente „Inhaltsfragment“ als Erweiterung für die Kernkomponenten verfügbar und musste separat heruntergeladen und explizit aktiviert werden.

## Verwendung {#usage}

Die Kernkomponente „Inhaltsfragment-Komponente“ ermöglicht die Einbeziehung eines [Inhaltsfragments](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/content-fragments/content-fragments.html) auf einer Seite.

* Das Fragment und seine Eigenschaften können im [Dialogfeld „Konfigurieren“](#configure-dialog) ausgewählt werden.
* Ressourcentypen zum Verarbeiten bestimmter Bilder und Raster können im [Dialogfeld „Design“](#design-dialog) definiert werden.
* Mit der Option „Bearbeiten“ wird das ausgewählte Fragment im [Inhaltsfragment-Editor](https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/assets/content-fragments/content-fragments-variations.translate.html) geöffnet.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Inhaltsfragment-Komponente ist v1, die mit Version 1.1.0 der Kernkomponenten im Oktober 2017 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Kompatibel | Kompatibel | Kompatibel |

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

Rufen Sie die [Komponentenbibliothek](https://adobe.com/go/aem_cmp_library_cf_de) auf, um die Inhaltsfragment-Komponente sowie die Beispiele für ihre Konfigurationsoptionen und die HTML- und JSON-Ausgabe zu testen.

## Technische Details {#technical-details}

Die neueste technische Dokumentation zur Inhaltsfragment-Komponente [finden Sie auf GitHub](https://adobe.com/go/aem_cmp_tech_cf_v1_de).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Über das Dialogfeld „Konfigurieren“ kann der Inhaltsautor das gewünschte Inhaltsfragment und die zu verwendenden Elemente dieses Fragments definieren.

### Registerkarte „Eigenschaften“ {#properties-tab}

![Inhaltsfragment-Komponente](/help/assets/content-fragment-edit-properties.png)

* **Inhaltsfragment**

   * Pfad zum gewünschten Inhaltsfragment
   * Das **Dialogfeld „Auswahl“** kann zum Suchen des Fragments verwendet werden.

* **Anzeigemodus**
   * **Einzelnes Textelement** – Ermöglicht die Auswahl eines mehrzeiligen Textelements und aktiviert Optionen für die Absatzsteuerung.
   * **Mehrere Elemente** – Ermöglicht die Auswahl eines oder mehrerer Elemente des ausgewählten Inhaltsfragments
* **Element** – Die Elemente des Inhaltsfragments, die eingefügt werden sollen.
* **Variation** - Welche Variante des Inhaltsfragments zu verwenden ist (standardmäßig **Master**)

* **Absätze**

   * **Alle** - Alle Absätze anzeigen
   * **Bereich**

      * Festlegen von Bereichen der anzuzeigenden Absätze, durch ein Semikolon getrennt
      * So können Sie z. B. mit `1;3-5;7;9-*` den 1., den 3. bis 5., den 7. und den 9. bis zum letzten Absatz einbeziehen.
* **ID** – Diese Option dient zur Kontrolle der eindeutigen Kennung der Komponente in der HTML-Datei und auf der [Datenschicht](/help/developing/data-layer/overview.md).
   * Wenn Sie das Feld leer lassen, wird automatisch eine eindeutige ID generiert, die Sie über die resultierende Seite finden.
   * Sofern eine ID angegeben wird, ist vom Autor sicherzustellen, dass diese eindeutig ist.
   * Änderungen der ID können sich auf das CSS-, JS- und Datenschicht-Tracking auswirken.

### Registerkarte „Absatzsteuerung“ {#paragraph-control-tab}

Diese Registerkarte ist nicht verfügbar, wenn der Modus **Mehrere Elemente** ausgewählt ist.

![Inhaltsfragment-Komponente](/help/assets/content-fragment-edit-paragraph.png)

* **Absätze** – Ermöglicht die Auswahl aller Absätze oder eines Bereichs.
* **Überschriften als separate Absätze behandeln**

## Dialogfeld „Design“ {#design-dialog}

Das Dialogfeld „Design“ ermöglicht es dem Vorlagenautor, die Ressourcentypen zu definieren, mit denen gemischte Medienbilder und responsive Raster verarbeitet werden.

![Dialogfeld „Design“ der Inhaltsfragment-Komponente](/help/assets/content-fragment-design.png)

* **Internes responsives Raster**

   * Der Sling-Ressourcentyp, der für das interne responsive Raster verwendet wird

