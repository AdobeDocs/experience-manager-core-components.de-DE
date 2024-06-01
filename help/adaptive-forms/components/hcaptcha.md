---
title: Captcha in AEM adaptiven Forms
description: Verbessern Sie die Formularsicherheit mit Captcha&reg; Service mühelos. Schrittweise Anleitung enthalten!
feature-set: Experience Manager Sites, Experience Manager Forms
feature: Adaptive Forms, Core Components
role: Architect, Developer, Admin, User
source-git-commit: ddfd55259f84443e6add3ced09fd319bcd9c1677
workflow-type: tm+mt
source-wordcount: '583'
ht-degree: 17%

---

# Captcha Component{#hCaptcha-component-adaptive-forms-core-component}

<span class="preview"> Diese Funktion ist im Rahmen des Programms für frühzeitige Anmeldung verfügbar. Sie können von Ihrer offiziellen E-Mail-Adresse aus an aem-forms-ea@adobe.com schreiben, um dem Early-Adopter-Programm beizutreten und den Zugriff auf diese Funktion zu beantragen. </span>

Der Captcha®-Dienst schützt Ihre Formulare vor Bots, Spam und automatisiertem Missbrauch. Es stellt eine Checkbox-Widget-Herausforderung dar und wertet die Benutzerantwort aus, um festzustellen, ob es sich um einen menschlichen oder einen Bot handelt, der mit dem Formular interagiert. Dies verhindert, dass der Benutzer fortfährt, wenn der Test fehlschlägt, und hilft, Online-Transaktionen sicher zu machen, indem Bots davon abgehalten werden, Spam oder böswillige Aktivitäten zu posten.

![hCaptcha®](/help/adaptive-forms/assets/hCaptcha-challenge.png)

## Verwendung {#usage}

Es gibt verschiedene Gründe, warum es sinnvoll ist, eine Captcha-Herausforderung in einen Formularübermittlungsprozess einzubeziehen:

- **Bot Prevention**: Dadurch wird sichergestellt, dass das Formular von einem Benutzer gesendet wird, wodurch Spam und automatisierte Übermittlungen reduziert werden.

- **Sicherheit**: Es fügt eine zusätzliche Sicherheitsebene hinzu, um die Legitimität jeder Formularübermittlung zu überprüfen und vor bösartigen Angriffen zu schützen.

- **Datenintegrität**: Indem Sie mehrere oder betrügerische Übermittlungen verhindern, können Sie die Integrität und Genauigkeit der über das Formular erfassten Daten wahren.

- **Benutzerüberprüfung**: Es überprüft die Identität des Benutzers, der das Formular sendet, und stellt sicher, dass nur authentifizierte Benutzer sensible Transaktionen abschließen können.

- **Load Management**: Dies ermöglicht die Verwaltung der Serverlast durch die Steuerung der Rate der Formularübermittlungen, wodurch eine Systemüberlastung während Zeiten mit hohem Traffic-Aufkommen verhindert wird.

## Technische Details {#technical-details}

Aktuelle Informationen zur Captcha-Komponente finden Sie in der technischen Dokumentation zu [GitHub](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/hCaptcha/v1/hCaptcha/README.md). Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Entwicklerdokumentation für Kernkomponenten](/help/developing/overview.md).

Geben Sie die Eigenschaften der Captcha-Komponente mithilfe der [Dialogfeld konfigurieren](#configure-dialog). Das Dialogfeld &quot;Konfigurieren&quot;ist Teil der Kernkomponenten, die entwickelt wurden, um das Authoring der Formulare zu erleichtern und eine effiziente Möglichkeit zur Erstellung komplexer Formulare zu bieten.

## Version und Kompatibilität {#version-and-compatibility}


Die Adaptive Forms Captcha-Komponente wird im Mai 2024 als Teil der [Kernkomponenten 3.0.20](https://github.com/adobe/aem-core-forms-components/commit/a4cb97131ffad47137a8f5f173401128a1cf3491). Hier finden Sie eine Tabelle mit allen unterstützten Versionen, AEM-Kompatibilität und Links zur entsprechenden Dokumentation:

|  |  |
|---|---|
| Komponentenversion | AEM as a Cloud Service |
| --- | --- |
| v1 | Kompatibel mit<br>[Version 2.0.4](/help/adaptive-forms/version.md) und höher | Kompatibel | Kompatibel |

Informationen zu Versionen und Freigaben der Kernkomponente finden Sie im Dokument [Kernkomponenten-Versionen](/help/adaptive-forms/version.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Sie können die Eigenschaften Ihrer Captcha-Komponente einfach mit dem Dialogfeld &quot;Konfigurieren&quot;anpassen, das über die Registerkarte &quot;Einfach&quot;und die Registerkarte &quot;Validierung&quot;verfügt, um verschiedene Eigenschaften anzupassen.

### Registerkarte „Allgemein“ {#basic-tab}

- **[!UICONTROL Name]:** Geben Sie den Namen für Ihre Captcha-Komponente an. Sie können eine Formularkomponente sowohl im Formular als auch im Regeleditor leicht mit ihrem eindeutigen Namen identifizieren.
- **[!UICONTROL Titel]:** Geben Sie den Titel Ihrer Captcha-Komponente an.
- **[!UICONTROL Konfigurationseinstellungen]:** Wählen Sie eine für Captcha® konfigurierte Cloud-Konfiguration.
- **Captcha Size:** Sie können die Anzeigegröße des Chaptcha®-Challenger-Dialogfelds auswählen. Verwenden Sie die **[!UICONTROL Kompakt]** Option zur Anzeige einer kleinen Größe und **[!UICONTROL Normal]** Option zur Anzeige eines relativ großen Chaptcha® Challenge-Dialogfelds.<!-- or **[!UICONTROL Invisible]** to validate hCaptcha&reg; without explicitly rendering the checkbox widget on the user interface. -->

  ![Registerkarte &quot;Captcha Basic&quot;](/help/adaptive-forms/assets/hcaptcha-basic.png)

### Registerkarte „Validierung“ {#validation-tab}

- **[!UICONTROL Validierungsmeldung]:** Stellen Sie eine Validierungsmeldung für Ihre Captcha-Validierung bei der Formularübermittlung bereit.
- **[!UICONTROL Überprüfungsmeldung für Skripten]** - Verwenden Sie diese Option, um eine Eingabeaufforderung einzugeben, wenn die Skriptvalidierung fehlschlägt.

  ![Registerkarte &quot;Captcha-Validierung&quot;](/help/adaptive-forms/assets/hcaptcha-validation-tab.png)

**hCaptcha® ist eine eingetragene Marke von Intuition Machines, Inc.**

**Mehr erfahren** über andere **Kapitelkomponenten** und ihre Dienste, z. B.:

- [Verwenden von Captcha in einem adaptiven Formular für Kernkomponenten](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/integrate-adaptive-forms-hCaptcha-core-components)

- [Verwenden von Captcha in einem adaptiven Formular für Foundation-Komponenten](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/add-components-to-an-adaptive-form/integrate-adaptive-forms-hcaptcha)

- [Verwenden von Turnstile CAPTCHA in einem adaptiven Formular für Foundation-Komponenten](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/add-components-to-an-adaptive-form/integrate-adaptive-forms-turnstile)

- [Verwenden von Google reCAPTCHA in einem adaptiven Formular für Foundation-Komponenten](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/captcha-adaptive-forms-core-components)

## Ähnliche Artikel {#related-articles}

{{more-like-this}}

## Siehe auch {#see-also}

{{see-also}}
