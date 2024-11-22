---
title: Einführung zu Kernkomponenten für adaptive Formulare in AEM
description: Erstellen Sie ansprechende Registrierungserlebnisse (Formulare) mit der Flexibilität der Kernkomponenten für adaptive Formulare und stellen Sie sie über Adobe Experience Manager bereit.
role: Architect, Developer, Admin, User
exl-id: 6d0f2845-bbb8-4488-a254-b69d7a6290b1
source-git-commit: b37b6315312ecee0a74d8830d96a72f8a5a04e43
workflow-type: tm+mt
source-wordcount: '2215'
ht-degree: 99%

---

# Kernkomponenten für adaptive Formulare  {#adaptive-forms-core-components-introduction}

Mithilfe der Kernkomponenten für adaptive Formulare können Sie in Adobe Experience Manager überzeugende Erlebnisse bei der Registrierung schaffen.

## Kernkomponenten {#overview}

In Adobe Experience Manager (AEM) sind Komponenten die Bausteine, die zum Erstellen von Seiten und Formularen verwendet werden. Sie bieten Autoren und Autorinnen eine einfache und leistungsstarke Möglichkeit, Inhalte zu erstellen und zu verwalten und bieten Entwickelnden die Flexibilität und Erweiterbarkeit, die zum Erstellen benutzerdefinierter Komponenten erforderlich sind. Die Kernkomponenten sind so konzipiert, dass sie die Entwicklungszeit verkürzen und die Wartungskosten für Websites und Formulare senken, flexibel sind und einfach an die spezifischen Anforderungen einer Website und eines Formulars angepasst werden können.

Außerdem sind die Kernkomponenten responsiv und unterstützen eine breite Palette von Geräten, einschließlich Desktops, Tablets und Smartphones. Darüber hinaus entsprechen sie den neuesten Web-Standards und Best Practices und bilden eine robuste und zuverlässige Lösung für die Erstellung von Web-Inhalten.

Insgesamt sind die Kernkomponenten ein wesentliches Tool für die Erstellung und Verwaltung von Web-Inhalten in AEM und bieten eine leistungsstarke und flexible Lösung, die dazu beiträgt, die Entwicklungszeit und die Wartungskosten zu reduzieren und den Besuchern und Besucherinnen der Website ein großartiges Benutzererlebnis zu bieten.

## Kernkomponenten für adaptive Formulare

Die Kernkomponenten für adaptive Formulare bestehen aus 30 BEM-kompatiblen Open-Source-Komponenten, die auf der Grundlage der Adobe Experience Manager-WCM-Kernkomponenten basieren. Sie wurden speziell für die Erstellung von adaptiven Formularen entwickelt. Hierbei handelt es sich um Formulare, die sich an die Geräte-, Browser- und Bildschirmgröße der Benutzenden anpassen.

Diese Komponenten können verwendet werden, um außergewöhnliche Datenerfassungs- und Registrierungserlebnisse zu schaffen, indem sie eine breite Palette von Formularfeldoptionen bereitstellen, darunter Textfelder, Kontrollkästchen, Dropdown-Menüs und mehr. Sie beinhalten auch Funktionen wie Validierung, konditionelle Logik und responsives Design, die zum Erstellen benutzerfreundlicher Formulare verwendet werden können.

Da es sich bei diesen Komponenten um Open-Source-Elemente handelt, können Entwickler und Entwicklerinnen die Komponenten einfach erweitern und an die spezifischen Anforderungen ihrer Organisation anpassen. Zusätzlich basieren diese Komponenten auf der BEM-Methode, was sicherstellt, dass sie skalierbar und wartbar sind.

![Adaptives Formular – Bild](assets/sample-adaptive-form.png)

## Funktionen {#features}

|  |  |
|---|---|
| Produktionsbereit | Die Kernkomponenten für adaptive Formulare umfassen 24 zuverlässige WCM-Komponenten. |
| Cloud-fähig | Verfügbar für [AEM Forms as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/home.html?lang=de). |
| Vielseitig | Die Komponenten bieten allgemeine Konzepte, mit denen Autoren und Autorinnen von Formularen nahezu jedes beliebige Layout zusammenstellen können. |
| Konfigurierbar | Die [Inhaltsrichtlinien](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/full-stack/components-templates/templates.html?lang=de#content-policies) auf Vorlagenebene definieren, welche Funktionen verwendet oder nicht verwendet werden dürfen. |
| Barrierefrei | Sie bieten ARIA-Attribute, unterstützen die Tastaturnavigation und Text für Hilfstechnologien wie Bildschirmlesehilfen. |
| Designbar | Die Komponenten implementieren das [Stilsystem](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/features/style-system.html?lang=de) und das Markup folgt den [BEM-CSS-Konventionen](https://getbem.com/). |
| Anpassbar | Verschiedene Muster ermöglichen eine einfache Anpassung, von der Bearbeitung des HTML-Codes bis hin zur Wiederverwendung erweiterter Funktionen. |
| Versionierung | Die [Versionierungsrichtlinie](https://github.com/adobe/aem-core-wcm-components/wiki/Versioning-policies) stellt sicher, dass die Kernkomponenten Ihre Website nicht beschädigen, wenn Funktionen verbessert werden, die sich auf Sie auswirken könnten. |
| Open Source | Wenn etwas nicht so ist, wie es sein sollte, verbessern Sie es. |

<!-- comply with [WCAG 2.1 standard](https://www.w3.org/TR/WCAG21/), -->


## Vorteile {#benefits}

Die Datenerfassung ist für die Lead-Generierung und die Registrierung von entscheidender Bedeutung, und die Kernkomponenten von Adaptive Forms bieten eine leistungsstarke Lösung für die Erstellung von Formularen, die für die Datenerfassung optimiert sind. Einige der Gründe für die Verwendung von Kernkomponenten zum Erstellen dieser Customer Experiences sind:

* **[Verfügbarkeit auf GitHub](https://github.com/adobe/aem-core-forms-components)**: Die Kernkomponenten für adaptive Formulare in AEM sind Open-Source-Komponenten und auf GitHub verfügbar. Darüber hinaus steht eine umfassende Dokumentation bereit. Dies hilft Entwicklern, die Komponenten und ihre Funktionsweise zu verstehen, und unterstützt sie bei der Entwicklung. Die Website [aemcomponents.dev](https://www.aemcomponents.dev/) ist auch eine wertvolle Ressource, über die Entwickler die Komponenten in Verwendung sehen und auf die Dokumentation zugreifen können.

* **[BEM-Modell für die Stilgestaltung](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/using-themes-in-core-components)**: Für die Stilgestaltung der Kernkomponenten wird das BEM-Modell (Block Element Modifier) verwendet, bei dem es sich um eine bewährte und häufig verwendete Methode für die Organisation von CSS handelt. Dadurch wird es für Entwickler und Entwicklerinnen einfacher, die Organisation der Stile zu verstehen und diese an ihre spezifischen Anforderungen anzupassen.

* **Keine Abhängigkeit von Bibliotheken von Drittanbietern**: Einer der Vorteile der Kernkomponenten besteht darin, dass sie keine Abhängigkeit von JavaScript-Bibliotheken von Drittanbietern, einschließlich JQuery und Underscore, aufweisen. Dadurch können die Komponenten mit weniger Aufwand schneller erstellt und einfacher in eine vorhandene AEM-Implementierung integriert werden.

* **Fokus auf Leistung und Barrierefreiheit**: Die Kernkomponenten werden unter Berücksichtigung von Leistung und Barrierefreiheit erstellt, was sich in ihren hohen Google Lighthouse- und Web-Vitalwerten widerspiegelt. Dies erleichtert Entwicklern und Entwicklerinnen das Erstellen barrierefreier und leistungsstarker Web-Seiten, die in der heutigen digitalen Landschaft immer wichtiger werden.

* **Formularkomponenten in Sites 30-Vorlage und Designs**: Die Kernkomponenten bieten Unterstützung für Formularkomponenten in der Sites 30-Vorlage und den Designs, wodurch Entwickende Formulare in AEM einfacher erstellen und anpassen können.

* **[Einfachere Gestaltung](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/using-themes-in-core-components)**: Die Kernkomponenten sind einfacher zu gestalten als ihre Gegenstücke, die Foundation-Komponenten. Der Design-Erstellungsprozess ähnelt jenem von Sites und bietet die Möglichkeit, das Design/die CSS der übergeordneten Sites-Seite zu übernehmen. Darüber hinaus vereinfacht das BEM-Modell die Gestaltung und Veränderung von Stilen.

* **Barrierefreiheit**: Kernkomponenten in adaptiven Formularen unterstützen Standards und Richtlinien für die Barrierefreiheit, um sicherzustellen, dass Formulare von Menschen mit Behinderungen verwendet werden können, einschließlich solcher, die Hilfstechnologien wie Bildschirmlesehilfen verwenden.

* **[Versionierung](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/add-comments-annotations-versioning-adaptive-form-core-components)**: Sie können mehrere Versionen eines adaptiven Formulars auf der Basis von Kernkomponenten erstellen und verwalten, an kollaborativen Diskussionen teilnehmen, indem Sie Kommentare abgeben, und Anmerkungen zu bestimmten Formularkomponenten hinzufügen, um die Erfahrung bei der Formularerstellung insgesamt zu verbessern.

## Verfügbare Komponenten: Aufschlüsselung nach Komponententyp

Die aktuelle Version von AEM Forms enthält die folgenden Kernkomponenten: [Foundation-Komponenten](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/create-an-adaptive-form-on-forms-cs/introduction-forms-authoring#component-toolbar) und [Formularblock-Komponenten (Edge Delivery Services)](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/edge-delivery/build-forms/forms-references/form-components).

| Komponenten | Foundation-Komponenten | Kernkomponenten | Formularblock-Komponenten | Zusätzliche Informationen |
|------------|:---------------------:|:---------------:|:---------------------:|-----------------------|
| Adobe Sign Block | ✔️ | | | [Die Adobe Sign-Integration](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/forms/integrate/services/adobe-sign-integration-adaptive-forms#adobe-acrobat-sign-for-government) ist nur für Foundation-Komponenten verfügbar. |
| Akkordeon | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/accordion.md)</span> | | Für Foundation-Komponenten können Sie das Akkordeon-Layout in den [Eigenschaften der Bedienfeldkomponenten](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-layout-of-an-adaptive-form/layout-capabilities-adaptive-forms#panel-layout) konfigurieren. |
| Adaptives Formularfragment | ✔️ | ✔️ | | Für Foundation-Komponenten können Sie aus dem Asset-Browser [ein Fragment hinzufügen](https://experienceleague.adobe.com/de/docs/experience-manager-65/content/forms/adaptive-forms-basic-authoring/adaptive-form-fragments#insert-a-fragment-in-an-adaptive-form). |
| Adaptives Formular – reCAPTCHA | ✔️ | ✔️ | ✔️ | Verwenden Sie für Foundation-Komponenten die Captcha-Komponente, [um Google reCaptcha zu einem Formular hinzuzufügen](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/add-components-to-an-adaptive-form/captcha-adaptive-forms#google-reCAPTCHA). |
| Schaltfläche | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/button.md)</span> | ✔️ | |
| Diagramm | ✔️ | | | |
| Kontrollkästchen | ✔️ | ✔️ | | |
| Kontrollkästchengruppe | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/checkbox-group.md)</span> | ✔️ | Verwenden Sie für Foundation-Komponenten die Kontrollkästchen-Komponente, um mehrere Kontrollkästchen hinzuzufügen |
| Feld zur Datumseingabe | ✔️ | | | Für Kernkomponenten verwenden Sie die Komponente [Datumsauswahl](/help/adaptive-forms/components/date-picker.md). Sie können auch die separaten Komponenten [Textfeld](/help/adaptive-forms/components/text-box.md) oder [numerisches Feld](/help/adaptive-forms/components/numeric-box.md) hinzufügen, um den Tag, den Monat und das Jahr zu erfassen. |
| Datumsauswahl | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/date-picker.md)</span> | ✔️ | |
| Dropdown-Liste | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/drop-down-list.md)</span> | ✔️ | |
| E-Mail | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/email.md)</span> | ✔️ | |
| Dateianhang | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/file-attachment.md)</span> | ✔️ | |
| Auflistung der Dateianhänge | ✔️ | | | |
| Fußzeile | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/footer.md)</span> | ✔️ | |
| Fußnoten-Platzhalter | ✔️ | | | |
| Formular-Container | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/form-container.md)</span> | ✔️ | Verwenden Sie für Foundation-Komponenten die [Stamm-Bedienfeld-Komponente](https://experienceleague.adobe.com/de/docs/experience-manager-learn/cloud-service/forms/create-first-af/configure-root-panel). |
| Formulartitel | ✔️ | ✔️ | | Verwenden Sie für Foundation-Komponenten die Titelkomponente. |
| hCaptcha | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/hcaptcha.md)</span> |  | Bei Foundation-Komponenten können Sie [Ihre adaptiven Formulare mit Captcha](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/add-components-to-an-adaptive-form/integrate-adaptive-forms-turnstile.html) für auf Foundation-Komponenten basierende Formulare verbinden. |
| Kopfzeile | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/header.md)</span> | ✔️ | |
| Horizontale Registerkarten | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/horizontal-tabs.md)</span> | | Für Foundation-Komponenten können Sie das [Layout der Registerkarten oben (horizontale Registerkarten)](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-layout-of-an-adaptive-form/layout-capabilities-adaptive-forms#panel-layout) in den Eigenschaften der Bedienfeldkomponenten konfigurieren. |
| Bild | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/image.md)</span> | ✔️ | |
| Schaltfläche „Weiter“ | ✔️ | ✔️ | | Verwenden Sie die [Assistentenkomponente](/help/adaptive-forms/components/wizard.md) für die Schaltflächen „Weiter“ und „Zurück“, um zwischen mehreren Bedienfeldern zu wechseln. |
| Numerisches Feld | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/numeric-box.md)</span> | ✔️ | |
| Numerische Schritte | ✔️ | | | |
| Panel | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/panel.md)</span> | ✔️ | |
| Telefon / Mobiltelefon | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/phone.md)</span> | ✔️ | |
| Schaltfläche „Zurück“ | ✔️ | ✔️ | | Verwenden Sie die [Assistentenkomponente](/help/adaptive-forms/components/wizard.md) für die Schaltflächen „Weiter“ und „Zurück“, um zwischen mehreren Bedienfeldern zu wechseln. |
| Optionsfeldgruppe | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/radio-button.md)</span> | ✔️ | |
| Schaltfläche „Zurücksetzen“ | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/reset-button.md)</span> | ✔️ | |
| Freihändige Unterschrift | ✔️ | | | |
| Trennzeichen | ✔️ | | | Verwenden Sie die WCM-[Trennzeichenkomponente](/help/components/separator.md). |
| Schaltfläche „Senden“ | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/submit-button.md)</span> | ✔️ | |
| Zusammenfassungsschritt | ✔️ | | | |
| Schalter | ✔️ | <span style="color:blue"> [✔️](/help/adaptive-forms/components/adaptive-form-switch.md) | | |
| Tabelle | ✔️ | | | |
| Geschäftsbedingungen | ✔️ | ✔️ | | |
| Text | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/text.md)</span> | ✔️ | |
| Textfeld | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/text-box.md)</span> | ✔️ | |
| Turnstile Captcha | ✔️ | | | [Turnstile Captcha](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/add-components-to-an-adaptive-form/integrate-adaptive-forms-turnstile) ist nur für Foundation-Komponenten verfügbar. |
| Vertikale Registerkarten | ✔️ | ✔️ | | Für Foundation-Komponenten können Sie das [Layout der Registerkarten links (vertikale Registerkarten)](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-layout-of-an-adaptive-form/layout-capabilities-adaptive-forms#panel-layout) in den Eigenschaften der Bedienfeldkomponenten konfigurieren |
| Assistent | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/wizard.md)</span> | ✔️ | Für Foundation-Komponenten können Sie das [Assistenten-Layout](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-layout-of-an-adaptive-form/layout-capabilities-adaptive-forms#panel-layout) in den Eigenschaften der Bedienfeldkomponenten konfigurieren |

<!--| Password Box | ✔️ | ✔️| ✔️ | |
| Image Choice | ✔️ | | | |
-->


>[!NOTE]
>
>
> * Zusätzlich zu den oben aufgeführten Komponenten unterstützt der Formularbaustein alle gültigen [HTML5-Eingabetypen](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input#input_types) und [Textbereiche](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/textarea) als Komponenten.
> * Benötigen Sie eine Komponente, die oben nicht aufgeführt ist? Fordern Sie sie per E-Mail an aem-forms-ea@adobe.com von Ihrer offiziellen Adresse an.


<!-- >
* [Accordion](/help/adaptive-forms/components/accordion.md)
* [Adaptive Form Fragment](/help/adaptive-forms/components/adaptive-form-fragment.md)
* [Adaptive Form Switch](/help/adaptive-forms/components/adaptive-form-switch.md)
* [Button](/help/adaptive-forms/components/button.md)
* [Check Box Group](/help/adaptive-forms/components/checkbox-group.md)
* [Date Picker](/help/adaptive-forms/components/date-picker.md)
* [Drop-down list](/help/adaptive-forms/components/drop-down-list.md)
* [Email](/help/adaptive-forms/components/email.md)
* [Form Container](/help/adaptive-forms/components/form-container.md)
* [File Attachment](/help/adaptive-forms/components/file-attachment.md)
* [Footer](/help/adaptive-forms/components/footer.md)
* [Header](/help/adaptive-forms/components/header.md)
* [Horizontal Tabs](/help/adaptive-forms/components/horizontal-tabs.md)
* [Image](/help/adaptive-forms/components/image.md)
* [Numeric Box](/help/adaptive-forms/components/numeric-box.md)
* [Panel](/help/adaptive-forms/components/panel.md)
* [Phone](/help/adaptive-forms/components/phone.md)
* [Radio Button](/help/adaptive-forms/components/radio-button.md)
* [Adaptive Form reCAPTCHA](/help/adaptive-forms/components/adaptive-form-recaptcha.md)
* [Reset Button](/help/adaptive-forms/components/reset-button.md)
* [Submit Button](/help/adaptive-forms/components/submit-button.md)
* [Text Box](/help/adaptive-forms/components/text-box.md)
* [Text](/help/adaptive-forms/components/text.md)
* [Form Title](/help/adaptive-forms/components/form-title.md)
* [Wizard](/help/adaptive-forms/components/wizard.md)

-->

## Bedienfreundlicher Formular-Editor

Der Editor für adaptive Formulare, die auf Kernkomponenten basieren, ähnelt dem Editor, den Sie bereits für die Erstellung von AEM Sites-Seiten verwenden. Folgendes erhalten Sie:


* **Vertraute Benutzeroberflächen-Elemente und -Einstellungen**: Beim Konfigurieren von Eigenschaften für Formularkomponenten werden Sie feststellen, dass das Dialogfeld „Eigenschaften“ genauso aussieht wie das Dialogfeld, das Sie für WCM-Kernkomponenten verwenden. Dadurch können Sie die gewünschten Optionen schneller finden. Wie bei den WCM-Kernkomponenten wird auch bei den Formularkomponenten das Dialogfeld „Eigenschaften“ in der Mitte des Editors angezeigt, mit klaren Registerkarten, die grundlegende und erweiterte Optionen, Hilfetext und Informationen zur Barrierefreiheit voneinander trennen – alles in einem Registerkartenformat zur einfachen Navigation.

* **[Regeleditor](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/rule-editor-core-components)**: Sie können Ihren Formularen Logik und dynamische Funktionen hinzufügen, ohne Code zu schreiben. Mit dem integrierten Regeleditor können Sie Folgendes:
   * Felder basierend auf Benutzerentscheidungen ein- oder ausblenden
   * Ein Objekt aktivieren oder deaktivieren
   * Einen Wert für ein Objekt festlegen
   * Berechnungen durchführen
   * Eine Eigenschaft eines Objekts festlegen
   * Dateneingaben überprüfen
   * Einen Dienst aufrufen (externe Funktionalität aufrufen)
   * Integrierte Funktionen verwenden (vordefinierte Funktionen für häufige Aufgaben)
   * Benutzerdefinierte Funktionen verwenden (Ihren eigenen Code für bestimmte Anforderungen)
   * Felder und Bedienfelder validieren (sicherstellen, dass die Daten die Anforderungen erfüllen)
   * Den Wert eines Objekts validieren
   * Funktionen zur Berechnung des Werts eines Objekts ausführen
   * Einen Formulardatenmodelldienst aufrufen und einen Vorgang durchführen
   * Dynamische Stile hinzufügen (die Darstellung basierend auf Bedingungen ändern)
   * Andere Regeln erstellen (Kettenaktionen und Logik)
   * und mehr!

  Der Regeleditor verfügt nicht über den Code-Editor. Sie können [benutzerdefinierte Funktionen](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/create-and-use-custom-functions) verwenden, um Ihren eigenen Code für bestimmte Anforderungen zum Regeleditor hinzuzufügen.



* **Vorbefüllen von Formularen**: Sie können bestimmte Felder in einem Formular automatisch mit vorhandenen Daten füllen, wenn eine Benutzerin oder ein Benutzer es öffnet. Dadurch sparen Benutzende Zeit und Mühe, da die manuelle Eingabe bereits verfügbarer Informationen entfällt. Der Editor für Kernkomponenten bietet einen vorkonfigurierten Vorbefüllungsdienst, um Formularfelder mithilfe eines Formulardatenmodells auszufüllen. Sie können auch benutzerdefinierte Vorbefüllungsdienste für komplexere Szenarien erstellen.

* **[Datensatzdokument (DoR)](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/generate-document-of-record-core-components)**: Ein Datensatzdokument (Document of Record – DoR) bezieht sich auf eine formale, druckbare Darstellung der Daten, die über das Formular übermittelt werden. Es dient als permanenter Datensatz der von der Benutzerin oder vom Benutzer eingegebenen Informationen und liefert eine Momentaufnahme der gesendeten Daten in einem benutzerfreundlichen Format. Dies ist normalerweise ein PDF-Dokument. Sie können den Editor verwenden, um eine benutzerdefinierte Vorlage zu konfigurieren oder eine vorkonfigurierte Vorlage zu verwenden, um ein DoR zu generieren.

* **[Formulardatenmodell](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/forms/integrate/use-form-data-model/using-form-data-model)**: Ein adaptives Formulardatenmodell (Forms Date Model – FDM) dient als Brücke zwischen Ihren adaptiven Formularen und Ihren Datenquellen. Es definiert im Wesentlichen die Struktur und Organisation der Daten, die Ihre Formulare erfassen und mit denen Sie interagieren. Sie können den Editor verwenden, um Ihr Formular einfach mit einem Formulardatenmodell (FDM) zu verbinden.

* **[Formulareinreichungen](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components#:~:text=Adaptive%20Form%20Submit%20Action&amp;text=Adobe%20recommends%20using%20Core%20Components,to%20create%20standalone%20Adaptive%20Forms.&amp;text=A%20Submit%20Action%20lets%20you,button%20on%20an%20Adaptive%20Form)**: Eine Formulareinreichung bezieht sich auf den Prozess, bei dem Benutzende ihre Formulare ausfüllen und senden. Dadurch wird eine Reihe von Aktionen ausgelöst, die in der Formularkonfiguration definiert sind und letztendlich zur Speicherung oder Verarbeitung der gesendeten Daten führen. Der Editor für adaptive Formulare bietet eine Vielzahl von Optionen zum Konfigurieren von Formulareinreichungen. Einige der gängigen Sendeaktionen sind:

   * [E-Mail senden](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components#:~:text=Adaptive%20Form%20Submit%20Action&amp;text=Adobe%20recommends%20using%20Core%20Components,to%20create%20standalone%20Adaptive%20Forms.&amp;text=A%20Submit%20Action%20lets%20you,button%20on%20an%20Adaptive%20Form.)
   * [Power Automate-Fluss aufrufen](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/forms/integrate/services/forms-microsoft-power-automate-integration)
   * [An SharePoint senden](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-action-sharepoint)
   * [Workfront Fusion aufrufen](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components#:~:text=Invoke%20a%20Workfront%20Fusion)
   * [Mit Formulardatenmodell (FDM) senden](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/forms/integrate/use-form-data-model/using-form-data-model)
   * [An Azure Blob-Speicher senden](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components#:~:text=Submit%20to%20Azure%20Blob%20Storage)
   * [An REST-Endpunkt senden](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-action-restpoint)
   * [An OneDrive senden](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components#:~:text=to%20REST%20endpoint-,Submit%20to%20OneDrive,-Invoke%20an%20AEM)
   * [AEM-Workflow aufrufen](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components#:~:text=Invoke%20an%20AEM%20Workflow)


* [Kernkomponenten für adaptive Formulare im Sites-Seiteneditor](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page): Sie können Kernkomponenten für adaptive Formulare im AEM-Seiteneditor und in AEM Experience Fragments aktivieren und verwenden, um Datenerfassungserlebnisse direkt bei der Erstellung einer Sites-Seite zu erstellen.

  >[!VIDEO](https://video.tv.adobe.com/v/3419284?quality=12&learn=on)


<!-- 
* **Preview Forms**: You can use the editor to  simulates how the form would appear on various devices like desktops, tablets, and smartphones.
-->



## Aktivieren der Kernkomponenten für adaptive Formulare

Durch die Aktivierung der Kernkomponenten für adaptive Formulare in AEM Forms as a Cloud Service können Sie mit der Erstellung, Veröffentlichung und Bereitstellung von auf Kernkomponenten basierenden adaptiven Formularen und Headless-Formularen beginnen, und zwar für mehrere Kanäle mithilfe der Instanzen von AEM Forms as a Cloud Service. Detaillierte Anweisungen zum Aktivieren der Kernkomponenten für adaptive Formulare finden Sie unter [Aktivieren der Kernkomponenten für adaptive Formulare in AEM Forms as a Cloud Service und lokaler Entwicklungsumgebung](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/setup-configure-migrate/enable-adaptive-forms-core-components.html?lang=de).

Die Kernkomponenten für adaptive Formulare haben die folgenden Anforderungen.

| AEM-Version | AEM Forms-Add-on | Kernkomponenten für adaptive Formulare |
|---|---|---|
| AEM as a Cloud Service | Forms – Digitale Registrierung | [Version 2.0.10](version.md)+ |
| AEM 6.5 | Forms-Add-on | [Version 1.1.12](version.md)+ |

Wenn Ihre Version des AEM Cloud Service SDK älter als 2023.02.0 ist, [stellen Sie sicher, dass das `prerelease`-Flag in Ihrer Umgebung aktiviert ist](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/release-notes/prerelease.html?lang=de#new-features), da Kernkomponenten für adaptive Formulare Teil der Vorabversion vor der Version 2023.02.0 waren.


## Erstellen eines auf Kernkomponenten basierenden adaptiven Formulars

Sie können die folgenden Aktionen sowohl in Umgebungen von AEM Forms as a Cloud Service als auch von AEM 6.5 Forms ausführen:

| Aktion | AEM Forms-Version |
|--------|------------------|
| Erstellen eines eigenständigen adaptiven Formulars | [AEM Forms as Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html?lang=de) |
| Erstellen eines adaptiven Formulars in einer AEM Sites-Seite | [AEM 6.5 Forms](https://experienceleague.adobe.com/docs/experience-manager-65/forms/adaptive-forms-basic-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=de#create-an-adaptive-form-in-sites-editor-or-experience-fragment), [AEM Forms as Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=de#create-an-adaptive-form-in-sites-editor-or-experience-fragment) |
| Erstellen eines adaptiven Formulars in einem AEM Experience Fragment | [AEM 6.5 Forms](https://experienceleague.adobe.com/docs/experience-manager-65/forms/adaptive-forms-basic-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=de#create-an-adaptive-form-in-experience-fragment), [AEM Forms as Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=de#create-an-adaptive-form-in-experience-fragment) |
| Konvertieren eines adaptiven Formulars in ein Experience Fragment | [AEM 6.5 Forms](https://experienceleague.adobe.com/docs/experience-manager-65/forms/adaptive-forms-basic-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=de#convert-an-adaptive-form-in-sites-page-to-an-experience-fragment), [AEM Forms as Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=de#convert-an-adaptive-form-in-sites-page-to-an-experience-fragment) |





<!-- >, such as  [WCAG 2.1 standard](https://www.w3.org/TR/WCAG21/), to ensure that forms can be used by people with disabilities, including those using assistive technologies such as screen readers.

*   **Alignment with AEM Sites**: The Core Components are designed to be more aligned with AEM Sites, making it easier for Sites users to adopt and use them without having to learn anything new. The components use the same front-end pipeline as Sites, making it easier to style and modify their appearance. 

<!-- Additionally, the following points further illustrate this alignment:

    *   **Authoring experience inline with Page editor**: The Core Components have an authoring experience that is inline with the Sites editor, with dialogs and other experiences similar to the Page editor. This makes it easier for Sites users to create and manage forms within the familiar context of the Sites editor.

    *   **Inline form editing in Sites editor**: The Core Components allow  inline form editing within the Sites editor, avoiding the need to switch back and forth between editors. This streamlines the authoring experience and makes it easier to create and manage forms.

    *   **Inheriting Sites features in Forms**: Forms authored within a Sites page inherit the same features as Sites. This provides a seamless and integrated experience for creating and managing forms within the context of AEM Sites 
    
    <!--including Multi Site Manager, the ability to use Sites components within a form for static content, support for scheduled publish/unpublish, form translation aligned with Sites translation, versioning, and targeting -->

## Siehe auch {#see-also}

{{see-also}}
