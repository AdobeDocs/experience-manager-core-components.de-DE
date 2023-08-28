---
title: Kernkomponente für adaptive Formulare – Text
description: Verwenden oder Anpassen der Kernkomponente Adaptive Formulare Text.
role: Architect, Developer, Admin, User
exl-id: b8de68e4-ca0d-4ae5-9a04-104cc617f1be
source-git-commit: ad3e3bca5cb46f14e864e4704c90ac3b62779794
workflow-type: tm+mt
source-wordcount: '885'
ht-degree: 99%

---

# Text {#text-adaptive-forms-core-component}

In einem adaptiven Formular bezieht sich Text auf den Inhalt, der im Formular erscheint, sodass Benutzende ihn lesen können. Dazu können der Text gehören, der zur Beschriftung einer Gruppe von Formularelementen verwendet wird, z. B. Textfelder, sowie alle zusätzlichen Anweisungen oder Informationen, die Benutzenden bereitgestellt werden.

Dies kann es auch erleichtern, die Struktur eines Formulars in logische Abschnitte zu unterteilen, was es Benutzenden erleichtert, das Formular zu verstehen und auszufüllen. Darüber hinaus kann es für Barrierefreiheitszwecke verwendet werden, um eine kurze Beschreibung des Elements anzugeben, mit dem es verknüpft ist. Ein solches Textfeld wird normalerweise in der Nähe der Formularkomponenten angezeigt, z. B. vor oder nach dem Formular.

**Beispiel**

![](/help/adaptive-forms/assets/text.png)

## Verwendung {#reasons-to-use-text-label}

Es gibt mehrere Gründe, Text in einem Formular zu verwenden:

* **Anweisungen bereitstellen**: Text kann verwendet werden, um Anweisungen zu geben, wie das Formular auszufüllen ist oder welche Informationen erforderlich sind.

* **Kontext bereitstellen**: Sie können Text verwenden, um Kontext für das Formular bereitzustellen, z. B. um den Zweck des Formulars zu erklären oder die Organisation, die die Informationen erfasst.

* **Unterteilen des Formulars in logische Abschnitte**: Sie können Text verwenden, um ein Formular in logische Abschnitte zu unterteilen, wodurch es für Benutzende einfacher ist, das Formular zu verstehen und auszufüllen.

* **Branding und Identität**: Sie können Text für Branding- und Identitätszwecke verwenden, z. B. zum Einschließen des Namens der Organisation in das Formular.

## Version und Kompatibilität {#version-and-compatibility}

Die Kernkomponente „Akkordeon“ für adaptive Formulare wurde im Februar 2023 als Teil der Kernkomponenten 2.0.4 für Cloud Service und der Kernkomponenten 1.1.12 für AEM 6.5.16.0 Forms oder höher veröffentlicht. Hier finden Sie eine Tabelle mit allen unterstützten Versionen, AEM-Kompatibilität und Links zur entsprechenden Dokumentation:

| Komponentenversion | AEM as a Cloud Service | AEM 6.5.16.0 Forms oder höher |
|---|---|---|
| v1 | Kompatibel mit<br>[Version 2.0.4](/help/adaptive-forms/version.md) und höher | Kompatibel mit<br>[Version 1.1.12](/help/adaptive-forms/version.md) und höher (aber nur bis Version 2.0.0). |

Informationen zu Versionen und Freigaben der Kernkomponente finden Sie im Dokument [Kernkomponenten-Versionen](/help/adaptive-forms/version.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technische Details {#technical-details}

Aktuelle Informationen zur Text-Kernkomponente für adaptive Formulare finden Sie in der technischen Dokumentation auf [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/text/v1/text). Sie finden weitere Informationen zur Entwicklung von Kernkomponenten in der [Entwicklerdokumentation für Kernkomponenten](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Sie können Ihr Texterlebnis für Besuchende im Dialogfeld „Konfigurieren“ einfach anpassen. Sie können auch problemlos Textoptionen für ein nahtloses Benutzererlebnis definieren.

![Registerkarte „Allgemein“](/help/adaptive-forms/assets/text_properties.png)

* **Name**: Sie können eine Formularkomponente sowohl im Formular als auch im Regel-Editor leicht mit ihrem eindeutigen Namen identifizieren. Der Name darf jedoch keine Leerzeichen oder Sonderzeichen enthalten.

* **Bindungsverweis**: Bindungsverweis ist ein Verweis auf ein Datenelement, das in einer externen Datenquelle gespeichert ist und in einem Formular verwendet wird. Sie können mit dem Bindungsverweis Daten dynamisch an Formularfelder binden, sodass das Formular die aktuellsten Daten aus der Datenquelle anzeigen kann. Beispielsweise kann ein Bindungsverweis verwendet werden, um den Namen und die Adresse von Kundinnen und Kunden in einem Formular anzuzeigen, basierend auf der im Formular eingegebenen Kunden-ID. Der Bindungsverweis kann auch verwendet werden, um die Datenquelle mit den im Formular eingegebenen Daten zu aktualisieren. Auf diese Weise können Sie mit AEM Forms Formulare erstellen, die mit externen Datenquellen interagieren und so eine nahtlose Benutzererfahrung bei der Datenerfassung und Datenverwaltung bieten.
* **Komponente ausblenden**: Wählen Sie die Option, um die Komponente aus dem Formular auszublenden. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor. Dies ist nützlich, wenn Sie Informationen speichern müssen, die Benutzende nicht sehen oder direkt ändern müssen.
* **Schreibgeschützt**: Wählen Sie die Option aus, um zu verhindern, dass die Komponente bearbeitet werden kann. Benutzende können den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor.


## Dialogfeld „Design“ {#design-dialog}

Sie können das Dialogfeld „Design“ verwenden, um CSS-Stile für die Textkomponente zu definieren und verwalten.

### Registerkarte „Stile“ {#styles-tab}

Sie können die Registerkarte zum Definieren und Verwalten von CSS-Stilen für eine Komponente verwenden. Die Kernkomponente „Text“ für adaptive Formulare unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).

![Dialogfeld „Design“](/help/adaptive-forms/assets/reset_designdialog.png)

* **Standard-CSS-Klassen**: Sie können eine standardmäßige CSS-Klasse für die Text-Kernkomponente für adaptive Formulare bereitstellen.

* **Zulässige Stile**: Sie können Stile definieren, indem Sie einen Namen und die CSS-Klasse angeben, die den Stil darstellt. Sie können beispielsweise einen Stil mit dem Namen „Fettschrift“ erstellen und die CSS-Klasse „Schriftbreite: Fett“ bereitstellen. Sie können diese Stile bei einem adaptiven Formular im adaptiven Formular-Editor anwenden. Um einen Stil anzuwenden, wählen Sie im Editor für adaptive Formulare die Komponente aus, auf die Sie den Stil anwenden möchten, navigieren Sie zum Eigenschaften-Dialog und wählen Sie den gewünschten Stil aus der Dropdown-Liste **Stile**. Wenn Sie die Stile aktualisieren oder ändern müssen, kehren Sie einfach zum Dialogfeld „Design“ zurück, aktualisieren die Stile auf der Registerkarte „Stile“ und speichern die Änderungen.

## Verwandter Artikel {#related-article}

* [Erstellen eines adaptiven Formulars in einer AEM Sites-Seite oder einem Experience Fragment](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=de)

* [Erstellen eines eigenständigen adaptiven Formulars](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html?lang=de)


## Siehe auch {#see-also}

* [Akkordeon](/help/adaptive-forms/components/accordion.md)
* [Schaltfläche](/help/adaptive-forms/components/button.md)
* [Kontrollkästchen Gruppe](/help/adaptive-forms/components/checkbox-group.md)
* [Datumsauswahl](/help/adaptive-forms/components/date-picker.md)
* [Dropdown-Liste](/help/adaptive-forms/components/drop-down.md)
* [E-Mail-Eingabe](/help/adaptive-forms/components/email-input.md)
* [Formular-Container](/help/adaptive-forms/components/form-container.md)
* [Dateianhang](/help/adaptive-forms/components/file-attachment.md)
* [Fußzeile](/help/adaptive-forms/components/footer.md)
* [Kopfzeile](/help/adaptive-forms/components/header.md)
* [Horizontale Registerkarten](/help/adaptive-forms/components/horizontal-tabs.md)
* [Bild](/help/adaptive-forms/components/image.md)
* [Zahleneingabe](/help/adaptive-forms/components/number-input.md)
* [Bedienfeld-Container](/help/adaptive-forms/components/panel-container.md)
* [Optionsschaltfläche](/help/adaptive-forms/components/radio-button.md)
* [Schaltfläche „Zurücksetzen“](/help/adaptive-forms/components/reset-button.md)
* [Schaltfläche „Senden“](/help/adaptive-forms/components/submit-button.md)
* [Telefoneingabe](/help/adaptive-forms/components/telephone-input.md)
* [Texteingabe](/help/adaptive-forms/components/text-input.md)
* [Titel](/help/adaptive-forms/components/title.md)
* [Assistent](/help/adaptive-forms/components/wizard.md)