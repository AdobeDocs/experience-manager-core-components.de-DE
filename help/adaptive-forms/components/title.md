---
title: Adaptive Forms-Kernkomponente - Titel
description: Verwenden oder Anpassen der Kernkomponente "Adaptive Forms-Titel".
role: Architect, Developer, Admin, User
exl-id: 33eac885-8d66-4a5c-9a32-0ba11e6de293
source-git-commit: d2a6108f17f6e0c6b91bec84893d64a8bd48effd
workflow-type: tm+mt
source-wordcount: '862'
ht-degree: 14%

---

# Titel {#title-input-adaptive-forms-core-component}

In einem adaptiven Formular bezieht sich ein &quot;Titel&quot;auf den Text, der oben im Formular angezeigt wird, normalerweise unter der Kopfzeile. Der Titel wird mithilfe der Titelkomponente angegeben. Diese Komponente kann zum Formularlayout hinzugefügt werden und der Text kann entsprechend dem Zweck oder Thema des Formulars bearbeitet werden. Der Titel dient dem Benutzer als Titel oder kurze Beschreibung des Formulars und erleichtert die Unterscheidung des Formulars von anderen.

**Beispiel**

![](/help/adaptive-forms/assets/title.png)

## Verwendung {#reasons-to-use-title-in-an-adaptive-form}

Es gibt mehrere Gründe, warum es sich empfiehlt, einen Titel in einem Formular zu verwenden:

* **Klarheit**: Ein Titel identifiziert den Zweck des Formulars klar, was Benutzern hilft, zu verstehen, welche Informationen sie bereitstellen müssen.

* **Einrichtung**: Ein Titel kann dazu beitragen, Formulare nach Thema oder Zweck zu organisieren, wodurch Benutzer das benötigte Formular leichter finden können.

* **Zugänglichkeit**: Ein Titel ist ein Schlüsselelement für Benutzer mit Zugänglichkeitsanforderungen, da er von Sprachausgabeprogrammen laut ausgelesen wird, sodass Benutzer den Kontext des Formulars verstehen können.

* **Branding**: Ein Titel kann auch verwendet werden, um den Namen eines Unternehmens oder einer Organisation anzuzeigen, was dazu beiträgt, ein Gefühl von Vertrauen und Vertrautheit mit dem Benutzer zu schaffen.

* **Navigation**: Ein Titel kann auch für die Navigation durch das Formular nützlich sein, insbesondere wenn das Formular lang oder komplex ist.

* **Suchmaschinenoptimierung (SEO)**: Ein Titel im Formular hilft auch bei SEO, da Suchmaschinen den Titel verwenden, um die Relevanz einer Webseite für eine Suchabfrage zu ermitteln.

Insgesamt ist der Titel eines Formulars ein wichtiger Aspekt des Benutzererlebnisses und sollte verwendet werden, um eine klare und knappe Beschriftung für das Formular bereitzustellen, mit der Benutzer den Kontext und den Zweck des Formulars verstehen können.

## Version und Kompatibilität {#version-and-compatibility}

Die Kernkomponente &quot;Adaptive Forms Accordion&quot;wurde im Februar 2023 als Teil der Kernkomponenten 2.0.4 für Cloud Service und Kernkomponenten 1.1.12 für AEM 6.5.16.0 Forms oder höher veröffentlicht. In der folgenden Tabelle finden Sie alle unterstützten Versionen, AEM Kompatibilität und Links zur entsprechenden Dokumentation:

| Komponentenversion | AEM as a Cloud Service | AEM 6.5.16.0 Forms oder höher |
|---|---|---|
| v1 | Kompatibel mit<br>[Version 2.0.4](/help/adaptive-forms/version.md) und höher | Kompatibel mit<br>[Version 1.1.12](/help/adaptive-forms/version.md) und höher, jedoch weniger als 2.0.0. |

Informationen zu Kernkomponentenversionen und -versionen finden Sie im Abschnitt [Kernkomponenten-Versionen](/help/adaptive-forms/version.md) Dokument.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->


## Technische Details {#technical-details}

Laden Sie die neuesten Informationen zur Kernkomponente &quot;Adaptive Forms Title&quot;in der technischen Dokumentation zu [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/title/v1/title). Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie im Abschnitt [Entwicklerdokumentation für Kernkomponenten](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Im Dialogfeld &quot;Konfigurieren&quot;können Sie Ihre Titelerfahrung für Besucher einfach anpassen. Sie können auch mit Leichtigkeit Titeloptionen für ein nahtloses Benutzererlebnis definieren.

![Registerkarte &quot;Allgemein&quot;](/help/adaptive-forms/assets/title_properties.png)

Im Dialogfeld „Bearbeiten“ kann der Inhaltsautor den Titeltext definieren sowie die Überschriftenebene auswählen.

* **Titel** - Mit dem Titel können Sie eine Komponente in einem Formular leicht identifizieren. Standardmäßig wird der Titel über der Komponente angezeigt. Wenn Sie keinen Titel hinzufügen, wird der Name der Komponente anstelle des Titeltexts angezeigt.
* **Typ/Größe** - Definiert die Überschriftenebene des Titels.
* **ID** - Diese Option dient zur Kontrolle der eindeutigen Kennung der Komponente in der HTML-Datei und auf der Datenschicht.
   * Wenn Sie das Feld leer lassen, wird automatisch eine eindeutige ID generiert, die Sie über die resultierende Seite finden.
   * Sofern eine ID angegeben wird, ist vom Autor bzw. der Autorin sicherzustellen, dass diese eindeutig ist.
   * Änderungen der ID können sich auf das CSS-, JS- und Datenschicht-Tracking auswirken.

## Dialogfeld „Design“ {#design-dialog}

Die Registerkarte &quot;Design&quot;wird verwendet, um CSS-Stile für die Komponente &quot;Datumsauswahl&quot;zu definieren und zu verwalten.

### Titel

Auf der Registerkarte Titel können Vorlagenautoren standardmäßige und zulässige Überschriftenelemente für Formularautoren festlegen:

![Registerkarte &quot;Design dialog title&quot;](/help/adaptive-forms/assets/title_heading.png)

* **Zulässige Überschriftenelemente**: Eine Liste mit mehreren Optionen, über die der Vorlagenautor auswählen kann, welche Überschriftenelemente der Formularautor für den Titel verwenden kann.

* **Standardüberschriftenelement**: Eine Dropdown-Liste, die das standardmäßige Überschriftenelement für die Titelkomponente festlegt.

### Registerkarte „Arten“ {#styles-tab}

Die Registerkarte wird verwendet, um CSS-Stile für eine Komponente zu definieren und zu verwalten. Die Kernkomponente für die adaptive Forms-Datumsauswahl unterstützt die AEM [Stilsystem](/help/get-started/authoring.md#component-styling).

![Registerkarte &quot;Design dialog title&quot;](/help/adaptive-forms/assets/title_styles.png)

* **Standard-CSS-Klassen**: Sie können eine standardmäßige CSS-Klasse für die Adaptive Forms-Kernkomponente zur Datumsauswahl bereitstellen.

* **Zulässige Stile**: Sie können Stile definieren, indem Sie einen Namen und die CSS-Klasse angeben, die den Stil darstellt. Sie können beispielsweise einen Stil mit dem Namen &quot;fett Text&quot;erstellen und die CSS-Klasse &quot;font-weight: fett&quot;. Sie können diese Stile im adaptiven Forms-Editor verwenden oder auf ein adaptives Formular anwenden. Um einen Stil anzuwenden, wählen Sie im adaptiven Forms-Editor die Komponente aus, auf die Sie den Stil anwenden möchten, navigieren Sie zum Dialogfeld &quot;Eigenschaften&quot;und wählen Sie den gewünschten Stil aus dem **Stile** Dropdown-Liste. Wenn Sie die Stile aktualisieren oder ändern müssen, kehren Sie einfach zum Dialogfeld &quot;Design&quot;zurück, aktualisieren Sie die Stile auf der Registerkarte &quot;Stile&quot;und speichern Sie die Änderungen.

### Registerkarte &quot;Formate&quot; {#format-tab}

Auf der Registerkarte &quot;Formate&quot;können Sie standardmäßige und benutzerdefinierte Datumsformate angeben.

![Registerkarte &quot;Format&quot;](/help/adaptive-forms/assets/title_styles.png)


