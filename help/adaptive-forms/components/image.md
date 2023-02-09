---
title: Adaptive Forms-Kernkomponente - Bild
description: Verwenden oder Anpassen der Adaptive Forms Image-Kernkomponente
role: Architect, Developer, Admin, User
source-git-commit: 945e1793ae4e959f83960db46d2de4257916fe32
workflow-type: tm+mt
source-wordcount: '956'
ht-degree: 2%

---


# Bild {#image-adaptive-forms-core-component}

Mit einer Bildkomponente in einem adaptiven Formular können Sie Bilder in ein Formular einfügen. Diese Bilder können verwendet werden, um das Gesamtdesign des Formulars zu verbessern, zusätzliche Informationen bereitzustellen oder als visuelle Hilfe zu dienen, um den Benutzern zu helfen, den Zweck des Formulars zu verstehen. Die Bildkomponente kann verwendet werden, um ein Logo, ein Foto oder eine Grafik im Formular hinzuzufügen.

Für die Barrierefreiheit ist es wichtig, **Alternativtext** zum Bild hinzu, um eine kurze, beschreibende Textalternative für das Bild bereitzustellen, die das Bild Benutzern beschreibt, die es nicht sehen können.


**Beispiel**

![](/help/adaptive-forms/assets/image.png)


## Verwendung {#reasons-to-use-image-in-a-form}

Es gibt verschiedene Gründe, warum es sinnvoll ist, eine Bildkomponente in ein adaptives Formular einzuschließen:

* **Branding**: Ein Bild kann verwendet werden, um das Logo oder den Namen der Organisation anzuzeigen, die das Formular erstellt hat, und so zur Erkennung und Glaubwürdigkeit der Marke beizutragen.

* **Visuelle Hilfen**: Ein Bild kann dazu beitragen, Benutzern zusätzliche Informationen bereitzustellen, indem es als visuelle Hilfe dient, um Benutzern zu helfen, den Zweck des Formulars zu verstehen.

* **Dekoration**: Ein Bild kann verwendet werden, um das Gesamtdesign des Formulars zu verbessern und es visuell ansprechender zu gestalten.

* **Anwendererlebnis**: Mit einem Bild können Sie das Formular benutzerfreundlicher gestalten, indem Sie Benutzern eine klare und intuitive Möglichkeit bieten, auf Formularfelder zuzugreifen und diese auszufüllen.

## Version und Kompatibilität {#version-and-compatibility}

Die Adaptive Forms-Bild-Kernkomponente wurde im Februar 2023 als Teil der Kernkomponenten 2.0.4 veröffentlicht. Hier finden Sie eine Tabelle mit allen unterstützten Versionen, AEM Kompatibilität und Links zur entsprechenden Dokumentation:

|  |  |
|---|---|
| Komponentenversion | AEM as a Cloud Service |
| --- | --- |
| v1 | Kompatibel mit<br>[Version 2.0.4](/help/versions.md) und höher | Kompatibel | Kompatibel |

Informationen zu Kernkomponentenversionen und -versionen finden Sie im Abschnitt [Kernkomponenten-Versionen](/help/versions.md) Dokument.


<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technische Details {#technical-details}

Aktuelle Informationen zur Adaptive Forms Image Core-Komponente finden Sie in der technischen Dokumentation zu [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/image/v1/image). Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie im Abschnitt [Entwicklerdokumentation für Kernkomponenten](/help/developing/overview.md).


## Dialogfeld „Konfigurieren“ {#configure-dialog}

Im Dialogfeld &quot;Konfigurieren&quot;können Sie Ihre Bilderfahrung für Besucher einfach anpassen. Sie können Bildoptionen auch einfach definieren, um ein nahtloses Benutzererlebnis zu gewährleisten.

![Registerkarte „Eigenschaften“](/help/adaptive-forms/assets/image_properties.png)

* **Name** - Sie können eine Formularkomponente sowohl im Formular als auch im Regeleditor leicht mit ihrem eindeutigen Namen identifizieren, der Name darf jedoch keine Leerzeichen oder Sonderzeichen enthalten.

* **Titel** - Mit dem Titel können Sie eine Komponente in einem Formular leicht identifizieren. Standardmäßig wird der Titel über der Komponente angezeigt. Wenn Sie keinen Titel hinzufügen, wird der Name der Komponente anstelle des Titeltexts angezeigt.

* **Referenz zum Datensatzdokument** - Mit dieser Option können Sie ein Feld für ein adaptives Formular mit dem Feld Datensatzdokument verknüpfen. Wenn der Benutzer einen Wert in ein verknüpftes Feld eines adaptiven Formulars eingibt, wird dieser Wert auch im verknüpften Feld des entsprechenden Datensatzdokuments angezeigt. Beispielsweise kann eine Referenz zum Datensatzdokument verwendet werden, um den Namen und die Adresse eines Kunden in einem Datensatzdokument anzuzeigen, basierend auf der im Formular eingegebenen Kundenkennung. Auf diese Weise können Sie mit AEM Forms Datensatzdokument generieren und ein nahtloses Benutzererlebnis für die Datenerfassung und -verwaltung bieten.

* **Beschreibung** - Eine Beschreibung ist eine kurze Texterklärung, die zusätzliche Informationen oder Klarstellungen zum Zweck eines bestimmten Bildes bietet.

* **Asset hier ablegen oder nach einer hochzuladenden Datei suchen** - Mit dieser Option können Sie ein Asset wie ein Bild per Drag &amp; Drop mit der Maus ablegen. Sie können auch eine Datei aus einem lokalen Dateisystem mit dem **Durchsuchen** Schaltfläche. Nach dem Hinzufügen eines Bildes werden drei Schaltflächen unten im Bild angezeigt:
   * **Bearbeiten** - Tippen oder klicken Sie auf **Bearbeiten** , um die Ausgabeformate des Assets im Assets-Editor zu verwalten.
   * **Löschen** - Tippen oder klicken Sie auf **Löschen** , um die Auswahl des aktuell ausgewählten Bildes aufzuheben.
   * **Auswahl** - Tippen oder klicken Sie auf **Auswahl**  -Option, um ein anderes Bild aus dem Ordner Assets auszuwählen.

* **Alternativtext** - Diese Option wird verwendet, um den Text einzugeben, der eine kurze und beschreibende Textalternative für das Bild bietet, die das Bild für sehbehinderte Benutzer beschreibt.

* **Komponente ausblenden** - Wählen Sie die Option, um die Komponente aus dem Formular auszublenden. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regeleditor. Dies ist nützlich, wenn Sie Informationen speichern müssen, die vom Benutzer nicht gesehen oder direkt geändert werden müssen.

* **Schreibgeschützt** - Wählen Sie die Option aus, um die Komponente nicht bearbeitbar zu machen. Der Benutzer kann den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regeleditor.

## Dialogfeld „Design“ {#design-dialog}

Das Dialogfeld &quot;Design&quot;wird verwendet, um CSS-Stile für die Bildkomponente zu definieren und zu verwalten.

### Registerkarte „Arten“ {#styles-tab}

Das Dialogfeld &quot;Design&quot;wird zum Definieren und Verwalten von CSS-Stilen für eine Komponente verwendet. Die Kernkomponente &quot;Adaptives Forms-Bild&quot;unterstützt die AEM [Stilsystem](/help/get-started/authoring.md#component-styling).

**Standard-CSS-Klassen**: Sie können eine standardmäßige CSS-Klasse für die Adaptive Forms Image Core Component bereitstellen.

**Zulässige Stile**: Sie können Stile definieren, indem Sie einen Namen und die CSS-Klasse angeben, die den Stil darstellt. Sie können beispielsweise einen Stil mit dem Namen &quot;fett Text&quot;erstellen und die CSS-Klasse &quot;font-weight: fett&quot;. Sie können diese Stile im adaptiven Forms-Editor verwenden oder auf ein adaptives Formular anwenden. Um einen Stil anzuwenden, wählen Sie im adaptiven Forms-Editor die Komponente aus, auf die Sie den Stil anwenden möchten, navigieren Sie zum Dialogfeld &quot;Eigenschaften&quot;und wählen Sie den gewünschten Stil aus dem **Stile** Dropdown-Liste. Wenn Sie die Stile aktualisieren oder ändern müssen, kehren Sie einfach zum Dialogfeld &quot;Design&quot;zurück, aktualisieren Sie die Stile auf der Registerkarte &quot;Stile&quot;und speichern Sie die Änderungen.