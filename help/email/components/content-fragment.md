---
title: E-Mail-Inhaltsfragment-Komponente
description: Die Komponente E-Mail-Inhaltsfragment ermöglicht die Anzeige eines Inhaltsfragments in Ihrem Inhalt.
role: Architect, Developer, Admin, User
exl-id: 9bc6b730-0d2a-4e5b-891c-d2f67f600bcc
source-git-commit: 33976c0e745ad091a142109f70541f01a31edc5b
workflow-type: tm+mt
source-wordcount: '668'
ht-degree: 30%

---


# E-Mail-Inhaltsfragment-Komponente {#email-content-fragment-component}

Die Komponente E-Mail-Inhaltsfragment ermöglicht die Anzeige einer [Inhaltsfragment](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/content-fragments/content-fragments.html?lang=de) in Ihren Inhalt ein.

## Nutzung {#usage}

Die E-Mail-Inhaltsfragment-Komponente ermöglicht die Einbeziehung einer [Inhaltsfragment](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/content-fragments/content-fragments.html) in Ihren E-Mail-Inhalt. Inhaltsfragmente sind mehrkanalige strukturierte Inhalte, die zentral erstellt und einfach wiederverwendet werden können.

* Das Fragment und seine Eigenschaften können im [Dialogfeld &quot;Konfigurieren&quot;.](#configure-dialog)
* Ressourcentypen für bestimmte Bilder und Raster können im Abschnitt [Dialogfeld &quot;Design&quot;.](#design-dialog)
* Mit der Option &quot;Bearbeiten&quot;wird das ausgewählte Fragment im [Inhaltsfragment-Editor,](#edit-dialog) angepasst für die Verwendung mit den E-Mail-Kernkomponenten.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der E-Mail-Inhaltsfragment-Komponente ist v1, die mit Version X der E-Mail-Kernkomponenten im Oktober 2022 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|
| v1 | Kompatibel | Kompatibel |

Weitere Informationen zu E-Mail-Kernkomponentenversionen und -freigaben finden Sie im Dokument [Versionen der E-Mail-Kernkomponenten.](/help/email/versions.md)

## Musterkomponentenausgabe {#sample-component-output}

Um die E-Mail-Inhaltsfragment-Komponente zu erleben und Beispiele für die Konfigurationsoptionen sowie HTML- und JSON-Ausgaben zu sehen, besuchen Sie die [Komponentenbibliothek.](https://adobe.com/go/aem_cmp_library_email_cf)

## Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur E-Mail-Inhaltsfragment-Komponente [finden Sie auf GitHub.](https://adobe.com/go/aem_cmp_tech_email_cf_v1)

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler.](/help/developing/overview.md)

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Im Dialogfeld &quot;Konfigurieren&quot;kann der Inhaltsautor festlegen, welches Inhaltsfragment und welche Elemente dieses Fragments eingefügt werden sollen.

### Registerkarte „Eigenschaften“ {#properties-tab}

![E-Mail-Inhaltsfragment-Komponente](/help/email/assets/email-content-fragment-edit-properties.png)

* **Inhaltsfragment**

   * Pfad zum gewünschten Inhaltsfragment
   * Das **Dialogfeld „Auswahl“** kann zum Suchen des Fragments verwendet werden.

* **Anzeigemodus**
   * **Einzelnes Textelement** - Ermöglicht die Auswahl eines mehrzeiligen Textelements und aktiviert Optionen für die Absatzsteuerung.
* **Variation** - Welche Variante des Inhaltsfragments zu verwenden ist (standardmäßig **Master**)

* **ID** - Diese Option ermöglicht die Steuerung der eindeutigen Kennung der Komponente im HTML.
   * Wenn Sie das Feld leer lassen, wird automatisch eine eindeutige ID generiert, die Sie durch Überprüfen des resultierenden Inhalts finden können.
   * Sofern eine ID angegeben wird, ist vom Autor sicherzustellen, dass diese eindeutig ist.
   * Eine Änderung der ID kann sich auf CSS auswirken.

### Registerkarte „Absatzsteuerung“ {#paragraph-control-tab}

![E-Mail-Inhaltsfragment-Komponente](/help/assets/content-fragment-edit-paragraph.png)

* **Absätze** - Ermöglicht die Auswahl aller Absätze oder eines Bereichs.
   * **Alle** - Alle Absätze anzeigen
   * **Bereich**
      * Festlegen von Bereichen der anzuzeigenden Absätze, durch ein Semikolon getrennt
      * Beispiel `1;3-5;7;9-*` den ersten, den dritten bis fünften, den siebten und den neunten bis zum letzten Absatz aufzunehmen.
* **Überschriften als separate Absätze behandeln**

## Dialogfeld „Bearbeiten“ {#edit-dialog}

Nachdem Sie die Komponente &quot;E-Mail-Inhaltsfragment&quot;zum Konfigurieren eines Inhaltsfragments verwendet haben, wird bei Auswahl der Komponente im Inhaltseditor eine **Bearbeiten** -Option.

![Symbolleiste der Komponente &quot;E-Mail-Inhaltsfragment&quot;](/help/email/assets/email-content-fragment-edit-toolbar.png)

Tippen oder klicken Sie auf **Bearbeiten** Schaltfläche öffnet den Inhaltsfragment-Editor. Der Inhaltsfragment-Editor wurde erweitert und enthält jetzt Schaltflächen für die **Adobe Campaign-Variable auswählen** , um Adobe Campaign-Variablen in Inhaltsfragmente einzufügen.

![Inhaltsfragmenteditor für E-Mail](/help/email/assets/email-content-fragment-editor.png)

Weitere Informationen zum Bearbeiten und Bearbeiten von Inhaltsfragmenten finden Sie im Dokument [Erstellen von Fragmentinhalten.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/content-fragments/content-fragments-variations.html)

## Dialogfeld „Design“ {#design-dialog}

Wenn eine E-Mail-Inhaltsfragment-Komponente mit einem Inhaltsfragment konfiguriert ist und Sie es im Inhaltseditor auswählen, wird in der Symbolleiste eine Schaltfläche zum Öffnen des Inhaltsfragment-Editors angezeigt.


### Registerkarte „Haupt“ {#main-tab}

![Dialogfeld &quot;Design&quot;der E-Mail-Inhaltsfragment-Komponente](/help/email/assets/email-content-fragment-design.png)

* **Internes responsives Raster**

   * Der Sling-Ressourcentyp, der für das interne responsive Raster verwendet wird

### Registerkarte „Stile“ {#styles-tab}

Die E-Mail-Experience-Fragment-Komponente unterstützt die AEM [Stilsystem.](/help/get-started/authoring.md#component-styling)
