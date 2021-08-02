---
title: Inhaltsfragmentlisten-Komponente
description: Die Inhaltsfragmentlisten-Kernkomponente ermöglicht die Anzeige einer Liste von Inhaltsfragmenten.
role: Architect, Developer, Admin, User
exl-id: 0f2295b1-d287-4f72-8ee4-fa98c4850e53
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: ht
source-wordcount: '762'
ht-degree: 100%

---

# Inhaltsfragmentlisten-Komponente {#content-fragment-list-component}

Die Inhaltsfragmentlisten-Kernkomponente ermöglicht die Anzeige einer Liste von [Inhaltsfragmenten](https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/assets/content-fragments/content-fragments.translate.html).

## Nutzung {#usage}

Die Inhaltsfragmentlisten-Kernkomponente ermöglicht die Einbeziehung einer Liste von [Inhaltsfragmenten](https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/assets/content-fragments/content-fragments.translate.html) auf einer Seite basierend auf einem Inhaltsfragmentmodell. Dies kann besonders für die Erstellung von [Headless Content](https://helpx.adobe.com/de/experience-manager/6-5/sites/developing/user-guide.html?topic=/experience-manager/6-5/sites/developing/morehelp/headless.ug.js) nützlich sein, der leicht von anderen Programmen genutzt werden kann.

* Die Liste und ihre Eigenschaften können im [Dialogfeld „Konfigurieren“](#configure-dialog) ausgewählt werden.
* Stile können auf die Komponente im [Dialogfeld „Design“](#design-dialog) angewendet werden.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Inhaltsfragment-Komponente ist v1, die mit Version 2.4.0 der Kernkomponente im Mai 2019 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Kompatibel | Kompatibel | Kompatibel |

Weitere Informationen zu Kernkomponentenversionen und -freigaben finden Sie in den [Kernkomponentenversionen](/help/versions.md).

## Musterkomponentenausgabe {#sample-component-output}

Rufen Sie die [Komponentenbibliothek](https://adobe.com/go/aem_cmp_library_cflist_de) auf, um die Inhaltsfragmentlisten-Komponente sowie die Beispiele für ihre Konfigurationsoptionen und die HTML- und JSON-Ausgabe zu testen.

## Technische Details {#technical-details}

Die neueste technische Dokumentation zur Inhaltsfragmentlisten-Komponente [finden Sie auf GitHub](https://adobe.com/go/aem_cmp_tech_cflist_v1_de).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Über den Dialogfeld „Konfigurieren“ kann der Inhaltsautor festlegen, welche Inhaltsfragmente die Liste und die Elemente dieser Fragmente enthalten sollen.

### Registerkarte „Eigenschaften“

Auf der Registerkarte **Eigenschaften** wird festgelegt, welche Inhaltsfragmente in der Liste enthalten sind. Dies basiert hauptsächlich auf einem ausgewählten Inhaltsfragment-Modell, es stehen aber auch andere Filteroptionen zur Verfügung.

![Registerkarte „Eigenschaften“ im Dialogfeld „Bearbeiten“ der Inhaltsfragmentlisten-Komponente](/help/assets/content-fragment-list-properties.png)

* **Modell** – Pfad zum Inhaltsfragment-Modell, auf dem die Liste basiert.
   * Standardmäßig sind alle Inhaltsfragmente des Modells, das als **Modellpfad** definiert ist, in der Liste enthalten.
* **Übergeordneter Pfad** – Übergeordneter Pfad, aus dem die Liste erstellt werden soll.
   * Die auf dem ausgewählten **Modellpfad** basierenden Inhaltsfragmente werden nach den im **Übergeordneten Pfad** enthaltenen gefiltert.
      * Klicken oder tippen Sie auf die Schaltfläche **Auswahl-Dialogfeld öffnen** auf der rechten Seite des Feldes, um den Pfad anzugeben.
* **Tags** – Nur die Inhaltsfragmente mit den angegebenen Tags werden in die Liste aufgenommen.
   * Klicken oder tippen Sie auf die Schaltfläche **Auswahl-Dialogfeld öffnen** auf der rechten Seite des Feldes, um die Tags anzugeben.
   * Klicken oder tippen Sie auf das X neben den ausgewählten Tags, um sie zu entfernen.
* **Sortieren nach** – Feld des Inhaltsfragmentmodells, anhand dessen die Liste sortiert werden soll
   * Es können nur Textfelder (einschließlich numerisch, Datum und Uhrzeit) ausgewählt werden.
* **Sortierreihenfolge** – Wie die Liste anhand des Felds **Sortieren nach** sortiert wird
   * Aufsteigend oder absteigend
* **Maximale Elemente** – Maximale Anzahl der in der Liste anzuzeigenden Elemente
   * Bei keinem Wert werden alle Elemente zurückgegeben.
* **ID** – Diese Option dient zur Kontrolle der eindeutigen Kennung der Komponente in der HTML-Datei und auf der [Datenschicht](/help/developing/data-layer/overview.md).
   * Wenn Sie das Feld leer lassen, wird automatisch eine eindeutige ID generiert, die Sie über die resultierende Seite finden.
   * Sofern eine ID angegeben wird, ist vom Autor sicherzustellen, dass diese eindeutig ist.
   * Änderungen der ID können sich auf das CSS-, JS- und Datenschicht-Tracking auswirken.

>[!NOTE]
>Die Optionen **Sortieren nach**, **Sortierreihenfolge** und **Maximale Elemente** wurden mit Version 2.7.0 der Kernkomponenten eingeführt.

### Registerkarte „Elemente“

Standardmäßig werden alle Elemente des Inhaltsfragmentmodells in die Liste aufgenommen (sofern sie nicht durch das Feld **Maximale Elemente** eingeschränkt sind). Auf der Registerkarte **Elemente** können Sie nur bestimmte Elemente angeben, die einbezogen werden sollen.

![Registerkarte „Elemente“ im Dialogfeld „Bearbeiten“ der Inhaltsfragmentlisten-Komponente](/help/assets/content-fragment-list-elements.png)

* **Elemente** - Es werden nur die Elemente der Inhaltsfragmente in der angegebenen Liste angezeigt.
   * Klicken oder tippen Sie auf die Schaltfläche **Hinzufügen**, um ein neues Element hinzuzufügen..
   * Klicken oder tippen Sie auf die Schaltfläche **Löschen**, um ein ausgewähltes Element zu entfernen.
   * Ziehen Sie den Ziehgriff **Reihenfolge**, um die Reihenfolge der Elemente zu ändern.

## Dialogfeld „Design“ {#design-dialog}

Im Dialogfeld „Design“ kann der Vorlagenautor die Stile definieren, die auf die Inhaltsfragmentlisten-Komponente angewendet werden.
