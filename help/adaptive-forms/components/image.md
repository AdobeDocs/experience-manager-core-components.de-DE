---
title: Kernkomponente „Bild“ für adaptive Formulare
description: Verwenden oder Anpassen der Kernkomponente „Bild“ für adaptive Formulare.
role: Architect, Developer, Admin, User
exl-id: 9ee42d5d-16e3-4973-8364-5bc512ebe72e
source-git-commit: be630c4d0a10ebaa679b77419b901fac818addb1
workflow-type: ht
source-wordcount: '1015'
ht-degree: 100%

---

# Bild {#image-adaptive-forms-core-component}

Mit einer Bildkomponente in einem adaptiven Formular können Sie Bilder in ein Formular einfügen. Diese Bilder können verwendet werden, um das Gesamt-Design des Formulars zu verbessern, zusätzliche Informationen bereitzustellen oder eine visuelle Hilfe zu bieten, sodass Benutzende leichter den Zweck des Formulars verstehen. Die Bildkomponente kann verwendet werden, um ein Logo, ein Foto oder eine Grafik in ein Formular einzufügen.

Für die Barrierefreiheit ist es wichtig, **Alternativtext** zum Bild anzugeben, um eine kurze, beschreibende Textalternative für das Bild bereitzustellen, die das Bild für Benutzende beschreibt, die es nicht sehen können.


**Beispiel**

![](/help/adaptive-forms/assets/image.png)


## Verwendung {#reasons-to-use-image-in-a-form}

Es gibt verschiedene Gründe, warum es sinnvoll sein kann, eine Bildkomponente zu einem adaptiven Formular hinzuzufügen:

* **Branding**: Ein Bild kann verwendet werden, um das Logo oder den Namen der Organisation anzuzeigen, die das Formular erstellt hat, und so zur Erkennung und Glaubwürdigkeit der Marke beizutragen.

* **Visuelle Hilfe**: Ein Bild kann Benutzenden zusätzliche Informationen liefern, damit sie den Zweck des Formulars leichter verstehen können.

* **Dekoration**: Ein Bild kann verwendet werden, um das Gesamtdesign des Formulars zu verbessern und es visuell ansprechender zu gestalten.

* **Benutzererlebnis**: Mit einem Bild können Sie das Formular benutzerfreundlicher gestalten, indem Sie Benutzenden eine klare und intuitive Möglichkeit bieten, auf Formularfelder zuzugreifen und diese auszufüllen.

## Version und Kompatibilität {#version-and-compatibility}

Die Kernkomponente „Akkordeon“ für adaptive Formulare wurde im Februar 2023 als Teil der Kernkomponenten 2.0.4 für Cloud Service und der Kernkomponenten 1.1.12 für AEM 6.5.16.0 Forms oder höher veröffentlicht. Hier finden Sie eine Tabelle mit allen unterstützten Versionen, AEM-Kompatibilität und Links zur entsprechenden Dokumentation:

| Komponentenversion | AEM as a Cloud Service | AEM 6.5.16.0 Forms oder höher |
|---|---|---|
| v1 | Kompatibel mit<br>[Version 2.0.4](/help/adaptive-forms/version.md) und höher | Kompatibel mit<br>[Version 1.1.12](/help/adaptive-forms/version.md) und höher (aber nur bis Version 2.0.0). |

Informationen zu Versionen und Freigaben der Kernkomponente finden Sie im Dokument [Kernkomponenten-Versionen](/help/adaptive-forms/version.md).


<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technische Details {#technical-details}

Aktuelle Informationen zur Kernkomponente „Bild“ für adaptive Formulare finden Sie in der technischen Dokumentation auf [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/image/v1/image). Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Entwicklerdokumentation für Kernkomponenten](/help/developing/overview.md).


## Dialogfeld „Konfigurieren“ {#configure-dialog}

Im Dialogfeld „Konfigurieren“ können Sie die Bildkomponente für Besuchende einfach anpassen. Sie können auch Bildoptionen definieren, um das Benutzererlebnis zu verbessern.

![Registerkarte „Eigenschaften“](/help/adaptive-forms/assets/image_properties.png)

* **Name**: Sie können eine Formularkomponente sowohl im Formular als auch im Regeleditor durch ihren eindeutigen Namen identifizieren. Der Name darf keine Leerzeichen oder Sonderzeichen enthalten.

* **Titel**: Sie können mit dem Titel leicht eine Komponente in einem Formular identifizieren. Standardmäßig wird der Titel über der Komponente angezeigt. Wenn Sie keinen Titel hinzufügen, wird der Name der Komponente anstelle des Titeltexts angezeigt.

* **Datensatzdokument Bindungsverweis**: Mit dieser Option können Sie ein Feld eines adaptiven Formulars mit dem Feld „Datensatzdokument“ verknüpfen. Wenn Benutzende einen Wert in ein verknüpftes Feld eines adaptiven Formulars eingeben, erscheint dieser Wert auch im verknüpften Feld des entsprechenden Datensatzdokuments. Sie können beispielsweise einen Bindungsverweis für ein Datensatzdokument verwenden, um den Namen und die Adresse von Erwerbenden in einem Datensatzdokument anzuzeigen, basierend auf der im Formular eingegebenen Kunden-ID. Auf diese Weise können Sie mit AEM Forms ein Datensatzdokument generieren und ein nahtloses Benutzererlebnis für die Datenerfassung und -verwaltung bieten.

* **Beschreibung**: Eine Beschreibung ist eine kurze Texterklärung, die zusätzliche Informationen oder Klarstellungen zum Zweck eines bestimmten Bildes bietet.

* **Asset hier ablegen oder nach einer hochzuladenden Datei suchen** – Mit dieser Option können Sie ein Asset wie ein Bild per Drag-and-Drop mit der Maus ablegen. Sie können auch eine Datei aus einem lokalen Dateisystem mit der Schaltfläche **Durchsuchen** hochladen. Nach dem Hinzufügen eines Bildes erscheinen unten im Bild drei Schaltflächen:
   * **Bearbeiten** – Tippen oder klicken Sie auf **Bearbeiten**, um die Wiedergabeversionen des Assets im Asset-Editor zu verwalten.
   * **Löschen** – Tippen oder klicken Sie auf **Löschen**, um die Auswahl des aktuell ausgewählten Bilds aufzuheben.
   * **Auswahl** – Tippen oder klicken Sie auf die Option **Auswahl**, um ein anderes Bild aus dem Ordner „Assets“ auszuwählen.

* **Alternativtext**: Diese Option wird verwendet, um eine kurze Textalternative für das Bild einzugeben, um es für sehbehinderte Benutzende zu beschreiben.

* **Komponente ausblenden**: Wählen Sie diese Option, um die Komponente aus dem Formular auszublenden. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor. Dies ist nützlich, wenn Sie Informationen speichern müssen, die Benutzende nicht sehen oder direkt ändern müssen.

* **Schreibgeschützt**: Wählen Sie die Option aus, um zu verhindern, dass die Komponente bearbeitet werden kann. Benutzende können den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor.

## Dialogfeld „Design“ {#design-dialog}

Das Dialogfeld „Design“ wird verwendet, um CSS-Stile für die Bild-Komponente zu definieren und zu verwalten.

### Registerkarte „Stile“ {#styles-tab}

Sie können die Registerkarte zum Definieren und Verwalten von CSS-Stilen für eine Komponente verwenden. Die Kernkomponente „Bild“ für adaptive Formulare unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).

![Dialogfeld „Design“](/help/adaptive-forms/assets/image_designdialog.png)

**Standard-CSS-Klassen**: Sie können eine standardmäßige CSS-Klasse für die Kernkomponente „Bild“ für adaptive Formulare bereitstellen.

**Zulässige Stile**: Sie können Stile definieren, indem Sie den Namen und die CSS-Klasse für den Stil angeben. Sie können beispielsweise einen Stil mit dem Namen „Fettschrift“ erstellen und die CSS-Klasse „Schriftbreite: Fett“ bereitstellen. Sie können diese Stile bei einem adaptiven Formular im adaptiven Formular-Editor anwenden. Um einen Stil anzuwenden, wählen Sie im Editor für adaptive Formulare die Komponente aus, auf die Sie den Stil anwenden möchten, navigieren Sie zum Eigenschaften-Dialog und wählen Sie den gewünschten Stil aus der Dropdown-Liste **Stile**. Wenn Sie die Stile aktualisieren oder ändern müssen, kehren Sie einfach zum Dialogfeld „Design“ zurück, aktualisieren die Stile auf der Registerkarte „Stile“ und speichern die Änderungen.

<!--

## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html)

-->


>[!MORELIKETHIS]
>
>* [Akkordeon](/help/adaptive-forms/components/accordion.md)
>* [Schaltfläche](/help/adaptive-forms/components/button.md)
>* [Kontrollkästchengruppe](/help/adaptive-forms/components/checkbox-group.md)
>* [Datumsauswahl](/help/adaptive-forms/components/date-picker.md)
>* [Dropdown-Liste](/help/adaptive-forms/components/drop-down.md)
>* [E-Mail-Eingabe](/help/adaptive-forms/components/email-input.md)
>* [Formular-Container](/help/adaptive-forms/components/form-container.md)
>* [Dateianhang](/help/adaptive-forms/components/file-attachment.md)
>* [Fußzeile](/help/adaptive-forms/components/footer.md)
>* [Kopfzeile](/help/adaptive-forms/components/header.md)
>* [Horizontale Registerkarten](/help/adaptive-forms/components/horizontal-tabs.md)
>* [Zahleneingabe](/help/adaptive-forms/components/number-input.md)
>* [Bedienfeld-Container](/help/adaptive-forms/components/panel-container.md)
>* [Optionsschaltfläche](/help/adaptive-forms/components/radio-button.md)
>* [Zurücksetzen-Schaltfläche](/help/adaptive-forms/components/reset-button.md)
>* [Senden-Schaltfläche](/help/adaptive-forms/components/submit-button.md)
>* [Telefoneingabe](/help/adaptive-forms/components/telephone-input.md)
>* [Texteingabe](/help/adaptive-forms/components/text-input.md)
>* [Text](/help/adaptive-forms/components/text.md)
>* [Titel](/help/adaptive-forms/components/title.md)
>* [Assistent](/help/adaptive-forms/components/wizard.md)


## Siehe auch {#see-also}

{{see-also}}