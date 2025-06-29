---
title: Kernkomponente „Titel“ für adaptive Formulare
description: Verwenden oder Anpassen der Kernkomponente „Adaptive Formulare – Titel“.
role: Architect, Developer, Admin, User
exl-id: 33eac885-8d66-4a5c-9a32-0ba11e6de293
source-git-commit: 6725784bd4c94d433c91d6bd65d14d03cbefd954
workflow-type: ht
source-wordcount: '864'
ht-degree: 100%

---


# Formulartitel-Komponente{#title-input-adaptive-forms-core-component}

In einem adaptiven Formular bezieht sich ein „Titel“ auf den Text, der oben im Formular angezeigt wird, normalerweise unter der Kopfzeile. Der Titel wird mithilfe der Titelkomponente spezifiziert. Diese Komponente kann zum Formular-Layout hinzugefügt werden und ihr Text kann entsprechend dem Zweck oder Thema des Formulars bearbeitet werden. Der Titel dient Benutzenden als Bezeichnung kurze Beschreibung des Formulars und erleichtert die Unterscheidung des Formulars von anderen.

{{traditional-aem}}

**Beispiel**

![Beispiel eines Titels](/help/adaptive-forms/assets/title.png)

## Verwendung {#reasons-to-use-title-in-an-adaptive-form}

Es gibt mehrere Gründe, warum es sich empfiehlt, einen Titel in einem Formular zu verwenden:

- **Klarheit**: Ein Titel identifiziert den Zweck des Formulars, was Benutzenden hilft zu verstehen, welche Informationen sie bereitstellen müssen.

- **Ordnung**: Mit einem Titel können Formulare nach Thema oder Zweck gruppiert werden, wodurch Benutzer das benötigte Formular leichter finden können.

- **Barrierefreiheit**: Ein Titel ist ein Schlüsselelement für Benutzende mit Behinderung, da er von Sprachausgabeprogrammen laut vorgelesen wird, sodass Benutzende den Kontext des Formulars verstehen können.

- **Branding**: Ein Titel kann auch verwendet werden, um den Namen eines Unternehmens oder einer Organisation anzuzeigen, wodurch ein Gefühl von Vertrauen und Vertrautheit bei den Benutzenden geschaffen werden kann.

- **Navigation**: Ein Titel kann auch für die Navigation durch das Formular nützlich sein, insbesondere wenn das Formular lang oder komplex ist.

- **Suchmaschinen-Optimierung (SEO)**: Ein Titel im Formular hilft auch bei der SEO, da Suchmaschinen anhand des Titels die Relevanz einer Web-Seite für eine Suchabfrage ermitteln.

Insgesamt ist der Titel eines Formulars ein wichtiger Aspekt des Benutzererlebnisses und sollte verwendet werden, um eine klare und knappe Beschriftung für das Formular bereitzustellen, mit der Benutzende den Kontext und den Zweck des Formulars verstehen können.

## Version und Kompatibilität {#version-and-compatibility}

Die Kernkomponente für den Titel in adaptiven Formularen wurde im Februar 2023 als Teil der Kernkomponenten 2.0.4 für Cloud Service und der Kernkomponenten 1.1.12 für AEM 6.5.16.0 Forms oder höher veröffentlicht. Hier finden Sie eine Tabelle mit allen unterstützten Versionen, AEM-Kompatibilität und Links zur entsprechenden Dokumentation:

| Komponentenversion | AEM as a Cloud Service | AEM 6.5.16.0 Forms oder höher |
|---|---|---|
| v1 | Kompatibel mit<br>[Version 2.0.4](/help/adaptive-forms/version.md) und höher | Kompatibel mit<br>[Version 1.1.12](/help/adaptive-forms/version.md) und höher (aber nur bis Version 2.0.0). |

Informationen zu Versionen und Freigaben der Kernkomponente finden Sie im Dokument [Kernkomponenten-Versionen](/help/adaptive-forms/version.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion_de). -->


## Technische Details {#technical-details}

Die neuesten Informationen zur Kernkomponente „Titel“ für adaptive Formulare finden Sie in der technischen Dokumentation auf [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/title/v1/title). Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Entwicklerdokumentation für Kernkomponenten](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Im Dialogfeld „Konfigurieren“ können Sie den Titel einfach anpassen. Sie können auch Optionen für Titel definieren, um das Benutzererlebnis zu verbessern.

![Registerkarte „Allgemein“](/help/adaptive-forms/assets/title_properties.png)

Im Dialogfeld „Bearbeiten“ kann der Inhaltsautor bzw. die Inhaltsautorin den Titeltext definieren sowie die Überschriftenebene auswählen.

- **Titel**: Mit dem Titel können Sie eine Komponente in einem Formular leicht identifizieren. Standardmäßig wird der Titel oberhalb der Komponente angezeigt. Wenn Sie keinen Titel hinzufügen, wird der Name der Komponente anstelle des Titeltexts angezeigt.
- **Typ/Größe** – Definiert die Überschriftenebene des Titels.
- **ID** – Diese Option dient zur Kontrolle der eindeutigen Kennung der Komponente in der HTML-Datei und in der Datenschicht.
   - Wenn Sie das Feld leer lassen, wird automatisch eine eindeutige ID generiert, die Sie über die resultierende Seite finden.
   - Sofern eine ID angegeben wird, ist vom Autor bzw. der Autorin sicherzustellen, dass diese eindeutig ist.
   - Änderungen der ID können sich auf das CSS-, JS- und Datenschicht-Tracking auswirken.

## Dialogfeld „Design“ {#design-dialog}

Die Registerkarte „Design“ wird verwendet, um CSS-Stile für die Formulartitel-Komponente zu definieren und zu verwalten.

### Titel

Auf der Registerkarte „Titel“ können Vorlagenautoren und -autorinnen standardmäßige und zulässige HTML-Überschriftenelemente für Formularautoren und -autorinnen festlegen:

![Registerkarte „Titel“ im Dialogfeld „Design“](/help/adaptive-forms/assets/title_heading.png)

- **Zulässige Überschriftenelemente**: Eine Liste mit mehreren Optionen, über die der Vorlagenautor bzw. die Vorlagenautorin auswählen kann, welche Überschriftenelemente der Formularautor bzw. die Formularautorin für den Titel verwenden kann.

- **Standardmäßiges Überschriftenelement**: Eine Dropdown-Liste, die das standardmäßige Überschriftenelement für die Titelkomponente festlegt.

### Registerkarte „Stile“ {#styles-tab}

Sie können die Registerkarte zum Definieren und Verwalten von CSS-Stilen für eine Komponente verwenden. Die Kernkomponente „Datumsauswahl“ in adaptiven Formularen unterstützt das [Stilsystem](/help/get-started/authoring.md#component-styling) von AEM.

![Registerkarte „Titel“ im Dialogfeld „Design“](/help/adaptive-forms/assets/title_styles.png)

- **Standard-CSS-Klassen**: Sie können eine standardmäßige CSS-Klasse für die Kernkomponente „Titel“ für adaptive Formulare bereitstellen.

- **Zulässige Stile**: Sie können Stile definieren, indem Sie den Namen und die CSS-Klasse für den Stil angeben. Sie können beispielsweise einen Stil mit dem Namen „Fettschrift“ erstellen und die CSS-Klasse „Schriftbreite: Fett“ bereitstellen. Sie können diese Stile bei einem adaptiven Formular im adaptiven Formular-Editor anwenden. Um einen Stil anzuwenden, wählen Sie im Editor für adaptive Formulare die Komponente aus, auf die Sie den Stil anwenden möchten, navigieren Sie zum Eigenschaften-Dialog und wählen Sie den gewünschten Stil aus der Dropdown-Liste **Stile**. Wenn Sie die Stile aktualisieren oder ändern müssen, kehren Sie einfach zum Dialogfeld „Design“ zurück, aktualisieren die Stile auf der Registerkarte „Stile“ und speichern die Änderungen.

### Registerkarte „Formate“ {#format-tab}

Auf der Registerkarte „Formate“ können Sie standardmäßige und benutzerdefinierte Datumsformate angeben.

![Registerkarte „Formate“](/help/adaptive-forms/assets/title_styles.png)

<!--

## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html?lang=de)

-->

## Ähnliche Artikel {#related-articles}


{{more-like-this}}

## Siehe auch {#see-also}

{{see-also}}