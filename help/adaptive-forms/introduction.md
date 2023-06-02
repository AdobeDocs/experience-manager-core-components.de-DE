---
title: Einführung zu Kernkomponenten für adaptive Formulare in AEM
description: Erstellen Sie ansprechende Registrierungserlebnisse (Formulare) mit der Flexibilität der Kernkomponenten für adaptive Formulare und stellen Sie sie über Adobe Experience Manager bereit.
role: Architect, Developer, Admin, User
exl-id: 6d0f2845-bbb8-4488-a254-b69d7a6290b1
source-git-commit: 8648a8dabd1999c9d3bbb76bb4f04f16eafda650
workflow-type: tm+mt
source-wordcount: '1163'
ht-degree: 89%

---

# Einführung zu Kernkomponenten für adaptive Formulare {#adaptive-forms-core-components-introduction}

Mithilfe der Kernkomponenten für adaptive Formulare in Adobe Experience Manager können Sie überzeugende Registrierungserlebnisse schaffen, indem Sie die verfügbaren flexiblen Optionen und Anpassungsmöglichkeiten nutzen.

## Kernkomponenten  {#overview}

In Adobe Experience Manager (AEM) sind Komponenten die Bausteine, die zum Erstellen von Seiten und Formularen verwendet werden. Sie bieten Autoren und Autorinnen eine einfache und leistungsstarke Möglichkeit, Inhalte zu erstellen und zu verwalten und bieten Entwickelnden die Flexibilität und Erweiterbarkeit, die zum Erstellen benutzerdefinierter Komponenten erforderlich sind. Die Kernkomponenten sind so konzipiert, dass sie die Entwicklungszeit verkürzen und die Wartungskosten für Websites und Formulare senken, flexibel sind und einfach an die spezifischen Anforderungen einer Website und eines Formulars angepasst werden können.

Außerdem sind die Kernkomponenten responsiv und unterstützen eine breite Palette von Geräten, einschließlich Desktops, Tablets und Smartphones. Darüber hinaus entsprechen sie den neuesten Web-Standards und Best Practices und bilden eine robuste und zuverlässige Lösung für die Erstellung von Web-Inhalten.

Insgesamt sind die Kernkomponenten ein wesentliches Tool für die Erstellung und Verwaltung von Web-Inhalten in AEM und bieten eine leistungsstarke und flexible Lösung, die dazu beiträgt, die Entwicklungszeit und die Wartungskosten zu reduzieren und den Besuchern und Besucherinnen der Website ein großartiges Benutzererlebnis zu bieten.

## Kernkomponenten für adaptive Formulare

Die Kernkomponenten für adaptive Formulare bestehen aus 24 BEM-kompatiblen Open-Source-Komponenten, die auf der Grundlage der Adobe Experience Manager-WCM-Kernkomponenten basieren. Sie wurden speziell für die Erstellung von adaptiven Formularen entwickelt. Hierbei handelt es sich um Formulare, die sich an die Geräte-, Browser- und Bildschirmgröße der Benutzenden anpassen.

Diese Komponenten können verwendet werden, um außergewöhnliche Datenerfassungs- und Registrierungserlebnisse zu schaffen, indem sie eine breite Palette von Formularfeldoptionen bereitstellen, darunter Textfelder, Kontrollkästchen, Dropdown-Menüs und mehr. Sie beinhalten auch Funktionen wie Validierung, konditionelle Logik und responsives Design, die zum Erstellen benutzerfreundlicher Formulare verwendet werden können.

Da es sich bei diesen Komponenten um Open-Source-Elemente handelt, können Entwickler und Entwicklerinnen die Komponenten einfach erweitern und an die spezifischen Anforderungen ihrer Organisation anpassen. Zusätzlich basieren diese Komponenten auf der BEM-Methode, die sicherstellt, dass sie skalierbar und wartbar sind.

![](assets/sample-adaptive-form.png)

## Funktionen {#features}

|  |  |
|---|---|
| Produktionsbereit | Die Kernkomponenten für adaptive Formulare umfassen 24 zuverlässige WCM-Komponenten. |
| Cloud-fähig | Verfügbar für [AEM Forms as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/home.html?lang=de). |
| Vielseitig | Die Komponenten bieten allgemeine Konzepte, mit denen Autoren und Autorinnen von Formularen nahezu jedes beliebige Layout zusammenstellen können. |
| Konfigurierbar | Die [Inhaltsrichtlinien](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/full-stack/components-templates/templates.html?lang=de#content-policies) auf Vorlagenebene definieren, welche Funktionen verwendet oder nicht verwendet werden dürfen. |
| Barrierefrei | Sie bieten ARIA-Labels, unterstützen die Tastaturnavigation ([Bekannte Probleme](https://github.com/adobe/aem-core-wcm-components/issues?utf8=✓&amp;q=is%3Aissue+is%3Aopen+accessibility+in%3Atitle)) und Text für Hilfstechnologien wie Bildschirmlesehilfen. |
| Designbar | Die Komponenten implementieren das [Stilsystem](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/features/style-system.html?lang=de) und das Markup folgt den [BEM-CSS-Konventionen](https://getbem.com/). |
| Anpassbar | Verschiedene Muster ermöglichen eine einfache Anpassung, von der Bearbeitung des HTML-Codes bis hin zur Wiederverwendung erweiterter Funktionen. |
| Versionierung | Die [Versionierungsrichtlinie](https://github.com/adobe/aem-core-wcm-components/wiki/Versioning-policies) stellt sicher, dass die Kernkomponenten Ihre Website nicht beschädigen, wenn Funktionen verbessert werden, die sich auf Sie auswirken könnten. |
| Open Source | Wenn etwas nicht so ist, wie es sein sollte, verbessern Sie es. |

<!-- comply with [WCAG 2.1 standard](https://www.w3.org/TR/WCAG21/), -->


## Vorteile {#benefits}

Die Datenerfassung ist für die Lead-Generierung und die Registrierung von entscheidender Bedeutung, und die Kernkomponenten von Adaptive Forms bieten eine leistungsstarke Lösung für die Erstellung von Formularen, die für die Datenerfassung optimiert sind. Einige der Gründe für die Verwendung von Kernkomponenten zum Erstellen dieser Customer Experiences sind:

* **Verfügbarkeit auf GitHub und umfassende Dokumentation**: Die Kernkomponenten für adaptive Formulare in AEM sind Open-Source-Komponenten und auf GitHub verfügbar. Darüber hinaus steht eine umfassende Dokumentation bereit. Dies hilft Entwicklern, die Komponenten und ihre Funktionsweise zu verstehen, und unterstützt sie bei der Entwicklung. Die Website [aemcomponents.dev](https://www.aemcomponents.dev/) ist auch eine wertvolle Ressource, über die Entwickler die Komponenten in Verwendung sehen und auf die Dokumentation zugreifen können.

* **BEM-Modell für die Stilgestaltung**: Für die Stilgestaltung der Kernkomponenten wird das BEM-Modell (Block Element Modifier) verwendet, das eine bewährte und häufig verwendete Methode für die Organisation von CSS ist. Dadurch wird es für Entwickler und Entwicklerinnen einfacher, die Organisation der Stile zu verstehen und diese an ihre spezifischen Anforderungen anzupassen.

* **Keine Abhängigkeit von Bibliotheken von Drittanbietern**: Einer der Vorteile der Kernkomponenten besteht darin, dass sie keine Abhängigkeit von JavaScript-Bibliotheken von Drittanbietern, einschließlich JQuery und Underscore, aufweisen. Dadurch können die Komponenten mit weniger Aufwand schneller erstellt und einfacher in eine vorhandene AEM-Implementierung integriert werden.

* **Fokus auf Leistung und Barrierefreiheit**: Die Kernkomponenten werden unter Berücksichtigung von Leistung und Barrierefreiheit erstellt, was sich in ihren hohen Google Lighthouse- und Web-Vitalwerten widerspiegelt. Dies erleichtert Entwicklern und Entwicklerinnen das Erstellen barrierefreier und leistungsstarker Web-Seiten, die in der heutigen digitalen Landschaft immer wichtiger werden.

* **Formularkomponenten in Sites 30-Vorlage und Designs**: Die Kernkomponenten bieten Unterstützung für Formularkomponenten in der Sites 30-Vorlage und den Designs, wodurch Entwickende Formulare in AEM einfacher erstellen und anpassen können.

* **Einfachere Gestaltung**: Die Kernkomponenten sind einfacher zu gestalten als ihre Gegenstücke, die Foundation-Komponenten. Der Design-Erstellungsprozess ähnelt jenem von Sites und bietet die Möglichkeit, das Design/die CSS der übergeordneten Sites-Seite zu übernehmen. Darüber hinaus vereinfacht das BEM-Modell die Gestaltung und Veränderung von Stilen.

* **Barrierefreiheit**: Kernkomponenten in adaptiven Formularen unterstützen Standards und Richtlinien für die Barrierefreiheit, um sicherzustellen, dass Formulare von Menschen mit Behinderungen verwendet werden können, einschließlich solcher, die Hilfstechnologien wie Bildschirmlesehilfen verwenden

## Kernkomponenten für adaptive Formulare {#components}

Die aktuelle Version der Kernkomponenten für adaptive Formulare enthält die unten aufgelisteten Komponenten.

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
* [Text](/help/adaptive-forms/components/text.md)
* [Titel](/help/adaptive-forms/components/title.md)
* [Assistent](/help/adaptive-forms/components/wizard.md)

## Einrichten adaptiver Forms-Kernkomponenten

Durch die Aktivierung der adaptiven Forms-Kernkomponenten in AEM Forms as a Cloud Service können Sie mit der Erstellung, Veröffentlichung und Bereitstellung von Kernkomponenten-basierten adaptiven Forms- und Headless-Forms mit Ihren AEM Forms-Cloud Service-Instanzen für mehrere Kanäle beginnen. Detaillierte Anweisungen zum Aktivieren der Kernkomponenten für adaptive Formulare finden Sie unter [Aktivieren der adaptiven Forms-Kernkomponenten in der as a Cloud Service und lokalen Entwicklungsumgebung von AEM Forms](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/setup-configure-migrate/enable-adaptive-forms-core-components.html).

Die Kernkomponenten für adaptive Formulare haben die folgenden Anforderungen.

| AEM | AEM Forms-Add-on | Kernkomponenten für adaptive Formulare |
|---|---|---|
| AEM as a Cloud Service | Forms – Digitale Registrierung | [Version 2.0.10](version.md)+ |
| AEM 6.5 | Forms-Add-on | [Version 1.1.12](version.md)+ |

Wenn Ihre AEM Cloud Service SDK-Version älter als 2023.02.0 ist, [sicherstellen, dass Sie `prerelease` Markierung aktiviert in Ihrer Umgebung](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/release-notes/prerelease.html?lang=de#new-features) als Adaptive Forms-Kernkomponenten waren Teil der Vorabversion vor der Version 2023.02.0.


### Erstellen eines adaptiven Formulars basierend auf Kernkomponenten

Informationen zum Erstellen eines adaptiven Formulars in AEM Forms as a Cloud Service finden Sie unter [Erstellen eines adaptiven Formulars (Kernkomponenten)](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html?lang=de?).





<!-- >, such as  [WCAG 2.1 standard](https://www.w3.org/TR/WCAG21/), to ensure that forms can be used by people with disabilities, including those using assistive technologies such as screen readers.

*   **Alignment with AEM Sites**: The Core Components are designed to be more aligned with AEM Sites, making it easier for Sites users to adopt and use them without having to learn anything new. The components use the same front-end pipeline as Sites, making it easier to style and modify their appearance. 

<!-- Additionally, the following points further illustrate this alignment:

    *   **Authoring experience inline with Page editor**: The Core Components have an authoring experience that is inline with the Sites editor, with dialogs and other experiences similar to the Page editor. This makes it easier for Sites users to create and manage forms within the familiar context of the Sites editor.

    *   **Inline form editing in Sites editor**: The Core Components allow  inline form editing within the Sites editor, avoiding the need to switch back and forth between editors. This streamlines the authoring experience and makes it easier to create and manage forms.

    *   **Inheriting Sites features in Forms**: Forms authored within a Sites page inherit the same features as Sites. This provides a seamless and integrated experience for creating and managing forms within the context of AEM Sites 
    
    <!--including Multi Site Manager, the ability to use Sites components within a form for static content, support for scheduled publish/unpublish, form translation aligned with Sites translation, versioning, and targeting -->
