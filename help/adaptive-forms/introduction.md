---
title: Einführung zu Kernkomponenten für adaptive Formulare in AEM
description: Erstellen Sie ansprechende Registrierungserlebnisse (Formulare) mit der Flexibilität der Kernkomponenten für adaptive Formulare und stellen Sie sie über Adobe Experience Manager bereit.
role: Architect, Developer, Admin, User
exl-id: 6d0f2845-bbb8-4488-a254-b69d7a6290b1
source-git-commit: 23ad6de410aaf4952607d9a4aa44864b0743c479
workflow-type: tm+mt
source-wordcount: '2154'
ht-degree: 57%

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

* **[Verfügbarkeit auf GitHub](https://github.com/adobe/aem-core-forms-components)**: Die AEM adaptiven Forms-Kernkomponenten sind Open-Source-Komponenten und auf GitHub verfügbar. Darüber hinaus finden Sie eine umfassende Dokumentation. Dies hilft Entwicklern, die Komponenten und ihre Funktionsweise zu verstehen, und unterstützt sie bei der Entwicklung. Die Website [aemcomponents.dev](https://www.aemcomponents.dev/) ist auch eine wertvolle Ressource, über die Entwickler die Komponenten in Verwendung sehen und auf die Dokumentation zugreifen können.

* **[BEM-Modell für die Formatierung](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/using-themes-in-core-components)**: Die Kernkomponenten folgen dem BEM-Modell (Block Element Modifier) für die Formatierung, das eine bewährte und häufig verwendete Methode für die Organisation von CSS ist. Dadurch wird es für Entwickler und Entwicklerinnen einfacher, die Organisation der Stile zu verstehen und diese an ihre spezifischen Anforderungen anzupassen.

* **Keine Abhängigkeit von Bibliotheken von Drittanbietern**: Einer der Vorteile der Kernkomponenten besteht darin, dass sie keine Abhängigkeit von JavaScript-Bibliotheken von Drittanbietern, einschließlich JQuery und Underscore, aufweisen. Dadurch können die Komponenten mit weniger Aufwand schneller erstellt und einfacher in eine vorhandene AEM-Implementierung integriert werden.

* **Fokus auf Leistung und Barrierefreiheit**: Die Kernkomponenten werden unter Berücksichtigung von Leistung und Barrierefreiheit erstellt, was sich in ihren hohen Google Lighthouse- und Web-Vitalwerten widerspiegelt. Dies erleichtert Entwicklern und Entwicklerinnen das Erstellen barrierefreier und leistungsstarker Web-Seiten, die in der heutigen digitalen Landschaft immer wichtiger werden.

* **Formularkomponenten in Sites 30-Vorlage und Designs**: Die Kernkomponenten bieten Unterstützung für Formularkomponenten in der Sites 30-Vorlage und den Designs, wodurch Entwickende Formulare in AEM einfacher erstellen und anpassen können.

* **[Einfacherer Stil](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/using-themes-in-core-components)**: Die Kernkomponenten sind einfacher zu gestalten als ihre Foundation-Komponenten-Entsprechungen. Der Design-Erstellungsprozess ähnelt jenem von Sites und bietet die Möglichkeit, das Design/die CSS der übergeordneten Sites-Seite zu übernehmen. Darüber hinaus vereinfacht das BEM-Modell die Gestaltung und Veränderung von Stilen.

* **Zugänglichkeit**: Adaptive Forms-Kernkomponenten unterstützen Barrierefreiheitsstandards und Richtlinien, um sicherzustellen, dass Formulare von Menschen mit Behinderungen verwendet werden können, einschließlich solcher, die Hilfstechnologien wie Bildschirmlesehilfen verwenden.

* **[Versionierung](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/add-comments-annotations-versioning-adaptive-form-core-components)**: Sie können mehrere Versionen eines auf Kernkomponenten basierenden adaptiven Forms erstellen und verwalten, durch Kommentare an kollaborativen Diskussionen teilnehmen und Anmerkungen an bestimmte Formularkomponenten anhängen, wodurch die gesamte Erfahrung beim Erstellen von Formularen verbessert wird.

## Vergleichen von Kernkomponenten, Foundation-Komponenten und Formularblock-Komponenten {#components}

Die aktuelle Version von AEM verfügt über die folgenden Kernkomponenten und Foundation-Komponenten.

| Komponenten | Foundation-Komponenten | Kernkomponenten | Formularblock-Komponenten | Zusätzliche Informationen |
|------------|:---------------------:|:---------------:|:---------------------:|-----------------------|
| Adobe Sign Block | ✔️ | | | Die Adobe Sign-Integration ist nur für Foundation-Komponenten verfügbar. |
| Akkordeon | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/accordion.md)</span> | | Für Foundation-Komponenten können Sie das Akkordeon-Layout in den Eigenschaften der Bedienfeldkomponenten konfigurieren |
| Adaptives Formularfragment | ✔️ | ✔️ | | Bei Foundation-Komponenten können Sie ein Fragment aus den Eigenschaften einer Bedienfeldkomponente hinzufügen. |
| Adaptives Formular – reCAPTCHA | ✔️ | ✔️ | ✔️ | Verwenden Sie für Foundation-Komponenten die Captcha-Komponente, um einem Formular Google reCaptcha hinzuzufügen. |
| Schaltfläche | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/button.md)</span> | ✔️ | |
| Captcha | ✔️ | | | Verwenden Sie für Foundation-Komponenten die Captcha-Komponente, um einem Formular Google reCaptcha hinzuzufügen. |
| Diagramm | ✔️ | | | |
| Kontrollkästchen | ✔️ | ✔️ | | |
| Kontrollkästchengruppe | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/checkbox-group.md)</span> | ✔️ | Verwenden Sie für Foundation-Komponenten das Kontrollkästchen, um mehrere Kontrollkästchen hinzuzufügen. |
| Feld zur Datumseingabe | ✔️ | | | Verwenden Sie für Kernkomponenten die Datumsauswahl oder separate Textfeldkomponenten oder numerische Feldkomponenten, um Tag, Monat und Jahr zu erfassen. |
| Datumsauswahl | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/date-picker.md)</span> | ✔️ | |
| Dropdown-Liste | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/drop-down-list.md)</span> | ✔️ | |
| E-Mail | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/email-input.md)</span> | ✔️ | |
| Dateianhang | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/file-attachment.md)</span> | ✔️ | |
| Auflistung der Dateianhänge | ✔️ | | | |
| Fußzeile | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/footer.md)</span> | ✔️ | |
| Fußnoten-Platzhalter | ✔️ | | | |
| Formular-Container | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/form-container.md)</span> | ✔️ | Verwenden Sie für Foundation-Komponenten die Komponente Stammbereich . |
| Formulartitel | ✔️ | ✔️ | | Verwenden Sie für Foundation-Komponenten die Titelkomponente . |
| Kopfzeile | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/header.md)</span> | ✔️ | |
| Horizontale Registerkarten | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/horizontal-tabs.md)</span> | | Für Foundation-Komponenten können Sie das Layout der Registerkarten oben (horizontale Registerkarten) in den Eigenschaften der Bedienfeldkomponenten konfigurieren |
| Bild | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/image.md)</span> | ✔️ | |
| Bildauswahl | ✔️ | | | |
| Schaltfläche „Weiter“ | ✔️ | ✔️ | | Verwenden Sie die Assistentenkomponente für die Schaltflächen &quot;Weiter&quot;und &quot;Zurück&quot;, um zwischen mehreren Bedienfeldern zu wechseln. |
| Numerisches Feld | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/numeric-box.md)</span> | ✔️ | |
| Numerische Schritte | ✔️ | | | |
| Bedienfeld | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/panel.md)</span> | ✔️ | |
| Kennwortfeld | ✔️ | | ✔️ | |
| Telefon/Telefon | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/telephone-input.md)</span> | ✔️ | |
| Schaltfläche „Zurück“ | ✔️ | | | Verwenden Sie die Assistentenkomponente für die Schaltflächen &quot;Weiter&quot;und &quot;Zurück&quot;, um zwischen mehreren Bedienfeldern zu wechseln. |
| Optionsschaltfläche | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/radio-button.md)</span> | | |
| Optionsfeldgruppe | | | ✔️ | |
| Schaltfläche „Zurücksetzen“ | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/reset-button.md)</span> | ✔️ | |
| Freihändige Unterschrift | ✔️ | | | |
| Seperator | ✔️ | | | |
| Schaltfläche „Absenden“ | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/submit-button.md)</span> | ✔️ | |
| Zusammenfassungsschritt | ✔️ | | | |
| Schalter | ✔️ | ✔️ | | |
| Tabelle | ✔️ | | | |
| Geschäftsbedingungen | ✔️ | ✔️ | | |
| Text | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/text.md)</span> | ✔️ | |
| Textfeld | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/text-box.md)</span> | ✔️ | |
| Titel | ✔️ | | | Verwenden Sie für Kernkomponenten die Komponente &quot;Formulartitel&quot;. |
| Vertikale Registerkarten | ✔️ | ✔️ | | Für Foundation-Komponenten können Sie das Layout der Registerkarten links (vertikale Registerkarten) in den Eigenschaften der Bedienfeldkomponenten konfigurieren |
| Assistent | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/wizard.md)</span> | ✔️ | Für Foundation-Komponenten können Sie das Assistentenlayout in den Eigenschaften der Bedienfeldkomponenten konfigurieren |




>[!NOTE]
>
>
> * Zusätzlich zu den oben aufgeführten Komponenten unterstützt der Forms-Block alle gültigen [HTML5-Eingabetypen](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input#input_types) und [textarea](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/textarea) als Komponenten.
> * Benötigen Sie eine Komponente, die oben nicht aufgeführt ist? Fordern Sie sie per E-Mail an aem-forms-ea@adobe.com von Ihrer offiziellen Adresse an.


<!-- >
* [Accordion](/help/adaptive-forms/components/accordion.md)
* [Button](/help/adaptive-forms/components/button.md)
* [Check Box Group](/help/adaptive-forms/components/checkbox-group.md)
* [Date Picker](/help/adaptive-forms/components/date-picker.md)
* [Drop-down list](/help/adaptive-forms/components/drop-down-list.md)
* [Email-input](/help/adaptive-forms/components/email-input.md)
* [Form Container](/help/adaptive-forms/components/form-container.md)
* [File Attachment](/help/adaptive-forms/components/file-attachment.md)
* [Footer](/help/adaptive-forms/components/footer.md)
* [Header](/help/adaptive-forms/components/header.md)
* [Horizontal Tabs](/help/adaptive-forms/components/horizontal-tabs.md)
* [Image](/help/adaptive-forms/components/image.md)
* [Numeric Box](/help/adaptive-forms/components/numeric-box.md)
* [Panel](/help/adaptive-forms/components/panel.md)
* [Radio Button](/help/adaptive-forms/components/radio-button.md)
* [Reset Button](/help/adaptive-forms/components/reset-button.md)
* [Submit Button](/help/adaptive-forms/components/submit-button.md)
* [Telephone input](/help/adaptive-forms/components/telephone-input.md)
* [Text Box](/help/adaptive-forms/components/text-box.md)
* [Text](/help/adaptive-forms/components/text.md)
* [Title](/help/adaptive-forms/components/title.md)
* [Wizard](/help/adaptive-forms/components/wizard.md)

-->

## Benutzerfreundlicher Forms-Editor

Der Editor für auf Kernkomponenten basierende adaptive Forms ähnelt dem Editor, den Sie bereits zum Erstellen von AEM Sites-Seiten verwenden. Hier finden Sie Folgendes:


* **Vertraute Benutzeroberflächen-Elemente und -Einstellungen**: Beim Konfigurieren von Eigenschaften für Formularkomponenten sehen Sie, dass das Dialogfeld &quot;Eigenschaften&quot;genauso aussieht wie das Dialogfeld, das Sie für WCM-Kernkomponenten verwenden. Dadurch können Sie die gewünschten Optionen schneller finden. Wie die WCM-Kernkomponenten erscheint bei Formularkomponenten das Dialogfeld &quot;Eigenschaften&quot;in der Mitte des Editors mit klaren Registerkarten, die grundlegende und erweiterte Optionen, Hilfetext und Informationen zur Barrierefreiheit voneinander trennen - alles in einem Registerkartenformat für einfache Navigation.

* **[Regeleditor](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/rule-editor-core-components)**: Sie können Ihren Formularen Logik und dynamische Funktionen hinzufügen, ohne Code zu schreiben. Mit dem integrierten Regeleditor können Sie Folgendes tun:
   * Felder basierend auf Benutzerentscheidungen ein- oder ausblenden
   * Ein Objekt aktivieren oder deaktivieren
   * Einen Wert für ein Objekt festlegen
   * Berechnungen durchführen
   * Festlegen einer Eigenschaft eines Objekts
   * Dateneingabe überprüfen
   * Aufrufen eines Dienstes (Aufrufen externer Funktionen)
   * Verwenden Sie integrierte Funktionen (vordefinierte Funktionen für häufige Aufgaben)
   * Verwenden Sie benutzerdefinierte Funktionen (Ihren eigenen Code für bestimmte Anforderungen).
   * Validieren von Feldern und Bereichen (stellen Sie sicher, dass die Daten die Anforderungen erfüllen)
   * Den Wert eines Objekts validieren
   * Funktionen zur Berechnung des Werts eines Objekts ausführen
   * Rufen Sie einen Formulardatenmodell (FDM)-Dienst auf und führen Sie einen Vorgang aus
   * Dynamisches Hinzufügen von Stilen (Ändern der Darstellung basierend auf Bedingungen)
   * Erstellen anderer Regeln (Kettenaktionen und Logik)
   * und mehr!

  Der Regeleditor verfügt nicht über den Code-Editor. Sie können [benutzerdefinierte Funktionen](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/create-and-use-custom-functions) , um Ihren eigenen Code für bestimmte Anforderungen zum Regeleditor hinzuzufügen.



* **Formulare vorbefüllen**: Sie können bestimmte Felder in einem Formular automatisch mit vorhandenen Daten füllen, wenn ein Benutzer es öffnet. Dadurch sparen Benutzer Zeit und Mühe, da die manuelle Eingabe bereits verfügbarer Informationen entfällt. Der Editor für Kernkomponenten bietet einen OOTB-Vorbefüllungs-Dienst, um Formularfelder mithilfe eines Formulardatenmodells auszufüllen. Sie können auch benutzerdefinierte Vorbefüllungs-Dienste für komplexere Szenarien erstellen.

* **[Datensatzdokument (DoR)](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/generate-document-of-record-core-components)**: Ein Datensatzdokument (DoR) bezieht sich auf eine formale, druckbare Darstellung der Daten, die über das Formular gesendet werden. Es dient als permanenter Datensatz der vom Benutzer eingegebenen Informationen und liefert eine Momentaufnahme der gesendeten Daten in einem benutzerfreundlichen Format, normalerweise ein PDF-Dokument. Sie können den Editor verwenden, um eine benutzerdefinierte Vorlage zu konfigurieren oder eine OOTB-Vorlage zu verwenden, um ein DoR zu generieren.

* **[Formulardatenmodell](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/integrate/use-form-data-model/using-form-data-model)**: Ein adaptives Forms-Datenmodell (FDM) dient als Brücke zwischen Ihrer adaptiven Forms und Ihren Datenquellen. Sie definiert im Wesentlichen die Struktur und Organisation der Daten, die Ihre Formulare erfassen und mit denen Sie interagieren. Sie können den Editor verwenden, um Ihr Formular einfach mit einem Forms-Datenmodell (FDM) zu verbinden.

* **[Formularübermittlungen](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components#:~:text=Adaptive%20Form%20Submit%20Action&amp;text=Adobe%20recommends%20using%20Core%20Components,to%20create%20standalone%20Adaptive%20Forms.&amp;text=A%20Submit%20Action%20lets%20you,button%20on%20an%20Adaptive%20Form)**: Eine Formularübermittlung bezieht sich auf den Prozess, bei dem Benutzer ihre ausgefüllten Formulare ausfüllen und senden. Dadurch wird eine Reihe von Aktionen Trigger, die in der Formularkonfiguration definiert sind und letztendlich zur Speicherung oder Verarbeitung der gesendeten Daten führen. Der adaptive Forms-Editor bietet eine Vielzahl von Optionen zum Konfigurieren von Formularübermittlungen. Einige der gängigen Sendeaktionen sind:

   * [E-Mail senden](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components#:~:text=Adaptive%20Form%20Submit%20Action&amp;text=Adobe%20recommends%20using%20Core%20Components,to%20create%20standalone%20Adaptive%20Forms.&amp;text=A%20Submit%20Action%20lets%20you,button%20on%20an%20Adaptive%20Form.)
   * [Netzautomatisierungsfluss aufrufen](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/integrate/services/forms-microsoft-power-automate-integration)
   * [An SharePoint übermitteln](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-action-sharepoint)
   * [Aufrufen einer Workfront-Fusion](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components#:~:text=Invoke%20a%20Workfront%20Fusion)
   * [Senden mit Formulardatenmodell (FDM)](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/integrate/use-form-data-model/using-form-data-model)
   * [Senden an Azure Blob Storage](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components#:~:text=Submit%20to%20Azure%20Blob%20Storage)
   * [An REST-Endpunkt übermitteln](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-action-restpoint)
   * [An OneDrive übermitteln](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components#:~:text=to%20REST%20endpoint-,Submit%20to%20OneDrive,-Invoke%20an%20AEM)
   * [AEM-Workflow aufrufen](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components#:~:text=Invoke%20an%20AEM%20Workflow)


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
