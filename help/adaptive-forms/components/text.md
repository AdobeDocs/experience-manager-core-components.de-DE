---
title: Adaptive Forms-Kernkomponente - Text
description: Verwenden oder Anpassen der Kernkomponente "Adaptiver Forms-Text".
role: Architect, Developer, Admin, User
exl-id: b8de68e4-ca0d-4ae5-9a04-104cc617f1be
source-git-commit: d2a6108f17f6e0c6b91bec84893d64a8bd48effd
workflow-type: tm+mt
source-wordcount: '812'
ht-degree: 2%

---

# Text {#text-adaptive-forms-core-component}

In einem adaptiven Formular bezieht sich Text auf den Inhalt, der im Formular angezeigt wird, damit der Benutzer ihn lesen kann. Dazu können der Text gehören, der zur Beschriftung einer Gruppe von Formularelementen verwendet wird, z. B. Textfelder, sowie alle zusätzlichen Anweisungen oder Informationen, die dem Benutzer bereitgestellt werden.

Dies kann auch dazu beitragen, die Struktur eines Formulars in logische Abschnitte zu unterteilen, was es den Benutzern erleichtert, das Formular zu verstehen und auszufüllen. Darüber hinaus kann es für Barrierefreiheitszwecke verwendet werden, um eine kurze Beschreibung des Elements anzugeben, mit dem es verknüpft ist. Ein solches Textfeld wird normalerweise in der Nähe der Formularkomponenten angezeigt, z. B. vor oder nach dem Formular.

**Beispiel**

![](/help/adaptive-forms/assets/text.png)

## Verwendung {#reasons-to-use-text-label}

Es gibt mehrere Gründe, Text in einem Formular zu verwenden:

* **Anweisungen geben**: Text kann verwendet werden, um Anweisungen zum Ausfüllen des Formulars oder dazu bereitzustellen, welche Informationen benötigt werden.

* **Kontext bereitstellen**: Text kann verwendet werden, um Kontext für das Formular bereitzustellen, z. B. um den Zweck des Formulars zu erklären oder die Organisation, die die Informationen erfasst.

* **Teilt das Formular in logische Abschnitte**: Text kann verwendet werden, um ein Formular in logische Abschnitte zu unterteilen, wodurch es für Benutzer einfacher ist, das Formular zu verstehen und auszufüllen.

* **Marken und Identität**: Text kann für Branding- und Identitätszwecke verwendet werden, z. B. zum Einschließen des Namens der Organisation in das Formular.

## Version und Kompatibilität {#version-and-compatibility}

Die Kernkomponente &quot;Adaptive Forms Accordion&quot;wurde im Februar 2023 als Teil der Kernkomponenten 2.0.4 für Cloud Service und Kernkomponenten 1.1.12 für AEM 6.5.16.0 Forms oder höher veröffentlicht. In der folgenden Tabelle finden Sie alle unterstützten Versionen, AEM Kompatibilität und Links zur entsprechenden Dokumentation:

| Komponentenversion | AEM as a Cloud Service | AEM 6.5.16.0 Forms oder höher |
|---|---|---|
| v1 | Kompatibel mit<br>[Version 2.0.4](/help/adaptive-forms/version.md) und höher | Kompatibel mit<br>[Version 1.1.12](/help/adaptive-forms/version.md) und höher, jedoch weniger als 2.0.0. |

Informationen zu Kernkomponentenversionen und -versionen finden Sie im Abschnitt [Kernkomponenten-Versionen](/help/adaptive-forms/version.md) Dokument.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technische Details {#technical-details}

Laden Sie die neuesten Informationen zur Kernkomponente &quot;Adaptives Forms-Text&quot;in der technischen Dokumentation zu [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/text/v1/text). Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie im Abschnitt [Entwicklerdokumentation für Kernkomponenten](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Im Dialogfeld &quot;Konfigurieren&quot;können Sie Ihre Texterfahrung für Besucher einfach anpassen. Sie können auch Textoptionen mit Leichtigkeit für ein nahtloses Benutzererlebnis definieren.

![Registerkarte &quot;Allgemein&quot;](/help/adaptive-forms/assets/text_properties.png)

* **Name** - Sie können eine Formularkomponente sowohl im Formular als auch im Regeleditor leicht mit ihrem eindeutigen Namen identifizieren, der Name darf jedoch keine Leerzeichen oder Sonderzeichen enthalten.

* **Bindungsverweis** - Ein Bindungsverweis ist ein Verweis auf ein Datenelement, das in einer externen Datenquelle gespeichert und in einem Formular verwendet wird. Mit der Bindungsreferenz können Sie Daten dynamisch an Formularfelder binden, sodass das Formular die aktuellsten Daten aus der Datenquelle anzeigen kann. Beispielsweise kann eine Bindungsverweis verwendet werden, um den Namen und die Adresse eines Kunden in einem Formular anzuzeigen, basierend auf der im Formular eingegebenen Kundenkennung. Die Bindungsverweis kann auch verwendet werden, um die Datenquelle mit den im Formular eingegebenen Daten zu aktualisieren. Auf diese Weise können Sie mit AEM Forms Formulare erstellen, die mit externen Datenquellen interagieren und so eine nahtlose Benutzererfahrung bei der Datenerfassung und -verwaltung bieten.
* **Komponente ausblenden** - Wählen Sie die Option, um die Komponente aus dem Formular auszublenden. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regeleditor. Dies ist nützlich, wenn Sie Informationen speichern müssen, die vom Benutzer nicht gesehen oder direkt geändert werden müssen.
* **Schreibgeschützt** - Wählen Sie die Option aus, um die Komponente nicht bearbeitbar zu machen. Der Benutzer kann den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regeleditor.


## Dialogfeld „Design“ {#design-dialog}

Das Dialogfeld &quot;Design&quot;wird verwendet, um CSS-Stile für die Textkomponente zu definieren und zu verwalten.

### Registerkarte „Arten“ {#styles-tab}

Die Registerkarte wird verwendet, um CSS-Stile für eine Komponente zu definieren und zu verwalten. Die Kernkomponente &quot;Adaptiver Forms-Text&quot;unterstützt die AEM [Stilsystem](/help/get-started/authoring.md#component-styling).

![Dialogfeld „Design“](/help/adaptive-forms/assets/reset_designdialog.png)

* **Standard-CSS-Klassen**: Sie können eine standardmäßige CSS-Klasse für die Adaptive Forms Text-Kernkomponente bereitstellen.

* **Zulässige Stile**: Sie können Stile definieren, indem Sie einen Namen und die CSS-Klasse angeben, die den Stil darstellt. Sie können beispielsweise einen Stil mit dem Namen &quot;fett Text&quot;erstellen und die CSS-Klasse &quot;font-weight: fett&quot;. Sie können diese Stile im adaptiven Forms-Editor verwenden oder auf ein adaptives Formular anwenden. Um einen Stil anzuwenden, wählen Sie im adaptiven Forms-Editor die Komponente aus, auf die Sie den Stil anwenden möchten, navigieren Sie zum Dialogfeld &quot;Eigenschaften&quot;und wählen Sie den gewünschten Stil aus dem **Stile** Dropdown-Liste. Wenn Sie die Stile aktualisieren oder ändern müssen, kehren Sie einfach zum Dialogfeld &quot;Design&quot;zurück, aktualisieren Sie die Stile auf der Registerkarte &quot;Stile&quot;und speichern Sie die Änderungen.
