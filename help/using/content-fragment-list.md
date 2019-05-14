---
title: Komponente "Inhaltsfragment-Liste «
seo-title: Komponente "Inhaltsfragment-Liste «
description: 'null'
seo-description: Die Komponente "Core Component Content Fragment" ermöglicht die Anzeige einer Liste von Inhaltsfragmenten.
contentOwner: Bohnert
content-type: Referenz
topic-tags: authoring
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-new
translation-type: tm+mt
source-git-commit: d683f8110b514860bba11e08e6923be49e92652f

---


# Komponente &quot;Inhaltsfragment-Liste «{#content-fragment-list-component}

Die Komponente &quot;Core Component Content Fragment&quot; ermöglicht die Anzeige einer Liste von [Inhaltsfragmenten](https://helpx.adobe.com/experience-manager/6-5/assets/using/content-fragments.html).

## Nutzung {#usage}

Die Komponente &quot;Core Component Content Fragment List&quot; ermöglicht die Einbeziehung einer Liste von [Inhaltsfragmenten](https://helpx.adobe.com/experience-manager/6-5/assets/using/content-fragments.html) auf einer Seite basierend auf einem Content Fragmentmodell. Dies kann besonders hilfreich sein, um [headless-Inhalte](https://helpx.adobe.com/experience-manager/6-5/sites/developing/user-guide.html?topic=/experience-manager/6-5/sites/developing/morehelp/headless.ug.js) zu erstellen, die problemlos von anderen Anwendungen genutzt werden können.

* Die Liste und die zugehörigen Eigenschaften können im Dialogfeld [&quot;Konfigurieren&quot; ausgewählt](#configure-dialog)werden.
* Stile können auf die Komponente im [Design-Dialogfeld angewendet](#design-dialog)werden.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Content Fragment-Komponente ist v 1, die mit Version 2.4.0 der Kernkomponenten im Mai 2019 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |---|
| v1 | Kompatibel | Kompatibel | Kompatibel |

Weitere Informationen zu Core-Komponentenversionen und -versionen finden Sie in den Core [-Komponentenversionen](versions.md).

## Musterkomponentenausgabe {#sample-component-output}

Rufen Sie die [Komponentenbibliothek auf, um die Komponente &quot;Inhaltsfragment&quot; sowie Beispiele für die Konfigurationsoptionen sowie die HTML- und JSON-Ausgabe zu erhalten](http://opensource.adobe.com/aem-core-wcm-components/library/content-fragment-list.html).

## Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur Inhaltsfragmentlistenkomponente [finden Sie unter github](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/contentfragmentlist/v1/contentfragmentlist).

Weitere Informationen zur Entwicklung Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Komponenten](developing.md).

## Dialogfeld konfigurieren {#configure-dialog}

Über das Dialogfeld &quot;Konfigurieren&quot; kann der Inhaltsautor festlegen, welche Inhaltsfragmente die Liste und die Elemente dieser Fragmente enthalten sollen.

### Registerkarte &quot;Eigenschaften «

Auf der **Registerkarte &quot;Eigenschaften** &quot; wird festgelegt, welche Inhaltsfragmente in der Liste enthalten sind. Dies basiert hauptsächlich auf einem ausgewählten Inhaltsfragmentmodell, aber es stehen andere Filteroptionen zur Verfügung.

![](assets/screen-shot-2019-05-08-10.47.19.png)

* **Modell** - Pfad zum Inhaltsfragmentmodell, auf dem die Liste basiert.
   * Standardmäßig sind alle Inhaltsfragmente des Modells, das als **Modellpfad** definiert ist, in der Liste enthalten.
* **Übergeordneter Pfad** - Übergeordneter Pfad, aus dem die Liste erstellt werden soll.
   * Die auf dem ausgewählten **Modellpfad** basierenden Inhaltsfragmente werden auf die entsprechenden **übergeordneten Pfade gefiltert**.
   * Klicken Sie auf die Schaltfläche &quot;Auswahl **öffnen&quot;** auf der rechten Seite des Feldes, um den Pfad anzugeben.
* **Tags** - Die Liste wird nur die Inhaltsfragmente mit den angegebenen Tags enthalten.
   * Klicken Sie auf die Schaltfläche &quot;Auswahl **öffnen&quot;** auf der rechten Seite des Feldes, um die Tags anzugeben.
   * Klicken oder tippen Sie auf das X neben ausgewählten Tags, um sie zu entfernen.


### Registerkarte &quot;Elemente «

Standardmäßig werden alle Elemente des Inhaltsfragmentmodells in die Liste aufgenommen. Mit den **Elementen** können Sie nur bestimmte Elemente angeben, die einbezogen werden sollen.

![](assets/screen-shot-2019-05-08-10.47.34.png)

* **Elemente** - Es werden nur die Elemente der Inhaltsfragmente in der angegebenen Liste angezeigt.
   * Klicken oder tippen Sie auf **die Schaltfläche Hinzufügen** , um ein neues Element hinzuzufügen.
   * Klicken oder tippen Sie auf **die Schaltfläche Löschen** , um ein ausgewähltes Element zu entfernen.
   * Ziehen Sie den **Bestellpunkt** , um die Reihenfolge der Elemente zu ändern.

## Design-Dialogfeld {#design-dialog}

Im Entwurfsdialogfeld kann der Vorlagenautor die Stile definieren, die auf die Komponente &quot;Inhaltsfragment&quot; angewendet werden.