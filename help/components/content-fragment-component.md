---
title: Inhaltsfragment-Komponente
description: Die Kernkomponente „Inhaltsfragment-Komponente“ ermöglicht die Anzeige eines Inhaltsfragments.
translation-type: tm+mt
source-git-commit: c186e9ec3944d785ab0376769cf7f2307049a809
workflow-type: tm+mt
source-wordcount: '659'
ht-degree: 78%

---


# Inhaltsfragment-Komponente{#content-fragment-component}

Die Kernkomponente „Inhaltsfragment-Komponente“ ermöglicht die Anzeige eines [Inhaltsfragments](https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/assets/content-fragments/content-fragments.translate.html).

>[!NOTE]
>
>Vor Version 2.4.0 der Kernkomponenten war die Komponente „Inhaltsfragment“ als Erweiterung für die Kernkomponenten verfügbar und musste separat heruntergeladen und explizit aktiviert werden.

## Nutzung {#usage}

Die Kernkomponente „Inhaltsfragment-Komponente“ ermöglicht die Einbeziehung eines [Inhaltsfragments](https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/assets/content-fragments/content-fragments.translate.html) auf einer Seite.

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

Rufen Sie die [Komponentenbibliothek](https://adobe.com/go/aem_cmp_library_cf) auf, um die Inhaltsfragment-Komponente sowie die Beispiele für ihre Konfigurationsoptionen und die HTML- und JSON-Ausgabe zu testen.

## Technische Details {#technical-details}

Die neueste technische Dokumentation zur Inhaltsfragment-Komponente [finden Sie auf GitHub](https://adobe.com/go/aem_cmp_tech_cf_v1).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Über das Dialogfeld „Konfigurieren“ kann der Inhaltsautor das gewünschte Inhaltsfragment und die zu verwendenden Elemente dieses Fragments definieren.

### Registerkarte „Eigenschaften“ {#properties-tab}

![Inhaltsfragment-Komponente](/help/assets/content-fragment-edit-properties.png)

* **Inhaltsfragment**

   * Pfad zum gewünschten Inhaltsfragment
   * Das **Dialogfeld „Auswahl“** kann zum Suchen des Fragments verwendet werden.

* **Anzeigemodus**
   * **EinzelTextelement** - Aktiviert die Auswahl eines mehrzeiligen Textelement und aktiviert Optionen für die Absatzkontrolle
   * **Mehrere Elemente** - Ermöglicht die Auswahl eines oder mehrerer Elemente des ausgewählten Inhaltsfragments
* **Element** - Das Element bzw. die Elemente des Inhaltsfragments, das bzw. die das
* **Variation** - Welche Variante des Inhaltsfragments zu verwenden ist (standardmäßig **Master**)

* **Absätze**

   * **Alle** - Alle Absätze anzeigen
   * **Bereich**

      * Festlegen von Bereichen der anzuzeigenden Absätze, durch ein Semikolon getrennt
      * So können Sie z. B. mit `1;3-5;7;9-*` den 1., den 3. bis 5., den 7. und den 9. bis zum letzten Absatz einbeziehen.
* **ID** - Diese Option ermöglicht die Steuerung des eindeutigen Bezeichners der Komponente im HTML und in der [Datenschicht](/help/developing/data-layer/overview.md).
   * Wenn Sie das Feld leer lassen, wird automatisch eine eindeutige ID generiert und Sie können die resultierende Seite überprüfen.
   * Wenn eine ID angegeben wird, muss der Autor sicherstellen, dass sie eindeutig ist.
   * Eine Änderung der ID kann sich auf die Verfolgung von CSS, JS und Datenschichten auswirken.

### Registerkarte &quot;Absatzsteuerung&quot; {#paragraph-control-tab}

Diese Registerkarte ist nicht verfügbar, wenn der Modus **Mehrere Elemente** ausgewählt ist.

![Inhaltsfragment-Komponente](/help/assets/content-fragment-edit-paragraph.png)

* **Absätze** - Auswahl aller Absätze oder eines Bereichs zulassen
* **Überschriften als separate Absätze behandeln**

## Dialogfeld „Design“ {#design-dialog}

Das Dialogfeld „Design“ ermöglicht es dem Vorlagenautor, die Ressourcentypen zu definieren, mit denen gemischte Medienbilder und responsive Raster verarbeitet werden.

![Design-Dialogfeld der Komponente &quot;Inhaltsfragment&quot;](/help/assets/content-fragment-design.png)

* **Internes responsives Raster**

   * Der Sling-Ressourcentyp, der für das interne responsive Raster verwendet wird

