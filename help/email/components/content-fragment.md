---
title: E-Mail-Inhaltsfragment-Komponente
description: Die E-Mail-Inhaltsfragment-Komponente ermöglicht die Anzeige eines Inhaltsfragments in Ihrem Inhalt.
role: Architect, Developer, Admin, User
exl-id: 9bc6b730-0d2a-4e5b-891c-d2f67f600bcc
source-git-commit: 91969e4956bef1a511b8d588d5290a7999bf86ec
workflow-type: ht
source-wordcount: '607'
ht-degree: 100%

---


# E-Mail-Inhaltsfragment-Komponente {#email-content-fragment-component}

Die E-Mail-Inhaltsfragment-Komponente ermöglicht die Anzeige eines [Inhaltsfragments](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/content-fragments/content-fragments.html?lang=de) in Ihrem Inhalt.

## Verwendung {#usage}

Die E-Mail-Inhaltsfragment-Komponente ermöglicht das Einfügen eines [Inhaltsfragments](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/content-fragments/content-fragments.html?lang=de) in Ihren E-Mail-Inhalt. Inhaltsfragmente sind kanalübergreifende, strukturierte Inhalte, die zentral erstellt und einfach wiederverwendet werden können.

* Das Fragment und seine Eigenschaften können im [Dialogfeld „Konfigurieren“](#configure-dialog) ausgewählt werden.
* Ressourcentypen zum Verarbeiten bestimmter Bilder und Raster können im [Dialogfeld „Design“](#design-dialog) definiert werden.
* Mit der Option „Bearbeiten“ wird das ausgewählte Fragment im [Inhaltsfragment-Editor](#edit-dialog) geöffnet und für die Verwendung mit den E-Mail-Kernkomponenten angepasst.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der E-Mail-Inhaltsfragment-Komponente ist v1. Sie wurde mit dem Release X der E-Mail-Kernkomponenten im Oktober 2022 eingeführt und wird in diesem Dokument beschrieben.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|---|---|---|---|
| v1 | Kompatibel | – | – |

Weitere Informationen zu E-Mail-Kernkomponentenversionen und -Releases finden Sie im Dokument [E-Mail-Kernkomponentenversionen](/help/email/versions.md).

## Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur E-Mail-Inhaltsfragment-Komponente [finden Sie auf GitHub](https://adobe.com/go/aem_cmp_tech_email_cf_v1).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Über das Dialogfeld „Konfigurieren“ kann der Inhaltsautor bzw. die Inhaltsautorin festlegen, welches Inhaltsfragment und welche Elemente dieses Fragments einbezogen werden sollen.

### Registerkarte „Eigenschaften“ {#properties-tab}

![E-Mail-Inhaltsfragment-Komponente](/help/email/assets/email-content-fragment-edit-properties.png)

* **Inhaltsfragment**

   * Pfad zum gewünschten Inhaltsfragment
   * Das **Dialogfeld „Auswahl“** kann zum Suchen des Fragments verwendet werden.

* **Anzeigemodus**
   * **Einzelnes Textelement** - Ermöglicht die Auswahl eines mehrzeiligen Textelements und aktiviert Optionen für die Absatzsteuerung.
* **Variation** – Welche Variante des Inhaltsfragments zu verwenden ist (standardmäßig **Master**)

* **ID** – Diese Option ermöglicht das Festlegen der eindeutigen Kennung der Komponente in HTML.
   * Wenn das Feld leer bleibt, wird automatisch eine eindeutige ID generiert, den Sie im resultierenden Inhalt finden.
   * Sofern eine ID angegeben wird, ist vom Autor bzw. der Autorin sicherzustellen, dass diese eindeutig ist.
   * Die Änderung der ID kann sich auf CSS auswirken.

### Registerkarte „Absatzsteuerung“ {#paragraph-control-tab}

![E-Mail-Inhaltsfragment-Komponente](/help/assets/content-fragment-edit-paragraph.png)

* **Absätze** – Ermöglicht die Auswahl aller Absätze oder eines Bereichs.
   * **Alle** - Alle Absätze anzeigen
   * **Bereich**
      * Festlegen von Bereichen der anzuzeigenden Absätze, durch ein Semikolon getrennt
      * Beispiel: In `1;3-5;7;9-*` soll der erste, der dritte bis fünfte, der siebte und der neunte bis zum letzten Absatz enthalten sein.
* **Überschriften als separate Absätze behandeln**

## Dialogfeld „Bearbeiten“ {#edit-dialog}

Nachdem Sie die E-Mail-Inhaltsfragment-Komponente zum Konfigurieren eines Inhaltsfragments verwendet haben, wird bei Auswahl der Komponente im Inhaltseditor eine **Bearbeiten**-Option angezeigt.

![Symbolleiste der E-Mail-Inhaltsfragment-Komponente](/help/email/assets/email-content-fragment-edit-toolbar.png)

Durch Tippen oder Klicken auf die Schaltfläche **Bearbeiten** wird der Inhaltsfragment-Editor geöffnet. Der Inhaltsfragment-Editor wurde erweitert und enthält jetzt Schaltflächen für die **Auswahl der Adobe Campaign-Variable**, um Adobe Campaign-Variablen in Inhaltsfragmente einzufügen.

![Inhaltsfragment-Editor für E-Mail](/help/email/assets/email-content-fragment-editor.png)

Weitere Informationen zum Bearbeiten und Erstellen von Inhaltsfragmenten finden Sie im Dokument [Erstellen von Fragmentinhalten](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/content-fragments/content-fragments-variations.html?lang=de).

## Dialogfeld „Design“ {#design-dialog}

Wenn eine E-Mail-Inhaltsfragment-Komponente mit einem Inhaltsfragment konfiguriert ist und Sie es im Inhaltseditor auswählen, wird in der Symbolleiste eine Schaltfläche zum Öffnen des Inhaltsfragment-Editors angezeigt.


### Registerkarte „Haupt“ {#main-tab}

![Dialogfeld „Design“ der E-Mail-Inhaltsfragment-Komponente](/help/email/assets/email-content-fragment-design.png)

* **Internes responsives Raster**

   * Der Sling-Ressourcentyp, der für das interne responsive Raster verwendet wird

### Registerkarte „Arten“ {#styles-tab}

Die E-Mail-Experience Fragment-Komponente unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).
