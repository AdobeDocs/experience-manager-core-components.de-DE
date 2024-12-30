---
title: hCaptcha in adaptiven AEM-Formularen
description: Mit dem hCaptcha®-Dienst können Sie die Formularsicherheit optimieren. Schrittweise Anleitung enthalten!
feature-set: Experience Manager Sites, Experience Manager Forms
feature: Adaptive Forms, Core Components
role: Architect, Developer, Admin, User
exl-id: eecb38d5-711e-4dc5-bc19-498e003f37e7
source-git-commit: be25eac36cafda0ff0cb745454593640cc54ceea
workflow-type: tm+mt
source-wordcount: '583'
ht-degree: 100%

---

# hCaptcha-Komponente{#hCaptcha-component-adaptive-forms-core-component}

<span class="preview">Diese Funktion ist im Rahmen des Early-Adopter-Programms verfügbar. Sie können von Ihrer offiziellen E-Mail-Adresse aus an aem-forms-ea@adobe.com schreiben, um dem Early-Adopter-Programm beizutreten und den Zugriff auf diese Funktion zu beantragen. </span>

Der hCaptcha®-Dienst schützt Ihre Formulare vor Bots, Spam und automatisiertem Missbrauch. Er führt einen Kontrollkästchen-Widget-Test durch und ermittelt anhand der Benutzerantwort, ob ein Mensch oder ein Bot mit dem Formular interagiert. Dabei wird verhindert, dass Benutzende fortfahren, wenn der Test fehlschlägt. Dies erhöht die Sicherheit von Online-Transaktionen, indem Bots keinen Spam senden oder andere bösartige Aktivitäten durchführen können.

![hCaptcha®](/help/adaptive-forms/assets/hCaptcha-challenge.png)

## Verwendung {#usage}

Es gibt verschiedene Gründe, warum es sinnvoll ist, einen hCaptcha-Test in ein Formular einzufügen:

- **Bot-Prävention**: Der Test stellt sicher, dass das Formular von einem Menschen gesendet wird, wodurch Spam und automatisierte Übermittlungen reduziert werden.

- **Sicherheit**: Der Test bietet eine zusätzliche Sicherheitsebene, um die Legitimität jeder Formularübermittlung zu überprüfen und vor bösartigen Angriffen zu schützen.

- **Datenintegrität**: Da mehrfache oder betrügerische Übermittlungen verhindert werden, wird durch den Test die Integrität und Genauigkeit der über das Formular erfassten Daten gewahrt.

- **Benutzerüberprüfung**: Der Test überprüft die Identität der Person, die das Formular sendet, und stellt sicher, dass nur authentifizierte Benutzende sensible Transaktionen abschließen können.

- **Auslastungsverwaltung**: Der Test ermöglicht die Verwaltung der Server-Auslastung. Zu diesem Zweck wird die Rate der Formularübermittlungen gesteuert, sodass das System zu Zeiten mit hohem Traffic nicht überlastet wird.

## Technische Details {#technical-details}

Aktuelle Informationen zur hCaptcha-Komponente finden Sie in der technischen Dokumentation auf [GitHub](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/hCaptcha/v1/hCaptcha/README.md). Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Entwicklerdokumentation für Kernkomponenten](/help/developing/overview.md).

Sie können die Eigenschaften der hCaptcha-Komponente im [Dialogfeld „Konfigurieren“](#configure-dialog) festlegen. Das Dialogfeld „Konfigurieren“ ist Teil der Kernkomponenten, die erstellt wurden, um das Authoring der Formulare zu vereinfachen und eine effiziente Methode zum Erstellen komplexer Formulare bereitzustellen.

## Version und Kompatibilität {#version-and-compatibility}


Die hCaptcha-Komponente für adaptive Formulare wurde im Mai 2024 als Teil von [Version 3.0.20 der Kernkomponenten](https://github.com/adobe/aem-core-forms-components/commit/a4cb97131ffad47137a8f5f173401128a1cf3491) veröffentlicht. Hier finden Sie eine Tabelle mit allen unterstützten Versionen, AEM-Kompatibilität und Links zur entsprechenden Dokumentation:

|  |  |
|---|---|
| Komponentenversion | AEM as a Cloud Service |
| --- | --- |
| v1 | Kompatibel mit<br>[Version 2.0.4](/help/adaptive-forms/version.md) und höher | Kompatibel | Kompatibel |

Informationen zu Versionen und Freigaben der Kernkomponente finden Sie im Dokument [Kernkomponenten-Versionen](/help/adaptive-forms/version.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Sie können die Eigenschaften Ihrer hCaptcha-Komponente ganz einfach im Dialogfeld „Konfigurieren“ ändern. Dort können Sie auf den Registerkarten „Allgemein“ und „Validierung“ verschiedene Eigenschaften anpassen.

### Registerkarte „Allgemein“ {#basic-tab}

- **[!UICONTROL Name]:** Geben Sie den Namen für die hCaptcha-Komponente an. Sie können eine Formularkomponente sowohl im Formular als auch im Regeleditor leicht anhand ihres eindeutigen Namens identifizieren.
- **[!UICONTROL Titel]:** Geben Sie den Titel der hCaptcha-Komponente an.
- **[!UICONTROL Konfigurationseinstellungen]:** Wählen Sie eine für hCaptcha® konfigurierte Cloud-Konfiguration aus.
- **Captcha-Größe:** Sie können die Anzeigegröße des Dialogfelds für den hCaptcha®-Test auswählen. Verwenden Sie die Option **[!UICONTROL Kompakt]** zur Anzeige eines kleinen und die Option **[!UICONTROL Normal]** zur Anzeige eines relativ großen Dialogfelds für den hCaptcha®-Test.<!-- or **[!UICONTROL Invisible]** to validate hCaptcha&reg; without explicitly rendering the checkbox widget on the user interface. -->

  ![hCaptcha-Registerkarte „Allgemein“](/help/adaptive-forms/assets/hcaptcha-basic.png)

### Registerkarte „Validierung“ {#validation-tab}

- **[!UICONTROL Validierungsmeldung]:** Stellen Sie eine Validierungsmeldung für die Captcha-Validierung bei der Formularübermittlung bereit.
- **[!UICONTROL Skriptüberprüfungsmeldung]**: Verwenden Sie diese Option, um eine Eingabeaufforderung einzugeben, falls die Skriptüberprüfung fehlschlägt.

  ![hCaptcha-Registerkarte „Validierung“](/help/adaptive-forms/assets/hcaptcha-validation-tab.png)

**hCaptcha® ist eine eingetragene Marke von Intuition Machines, Inc.**

**Erfahren Sie mehr** über andere **Captcha-Komponenten** und ihre Dienste, z. B.:

- [Verwenden von hCaptcha in einem adaptiven Formular für Kernkomponenten](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/integrate-adaptive-forms-hcaptcha-core-components)

- [Verwenden von hCaptcha in einem adaptiven Formular für Foundation-Komponenten](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/add-components-to-an-adaptive-form/integrate-adaptive-forms-hcaptcha)

- [Verwenden von Turnstile CAPTCHA in einem adaptiven Formular für Foundation-Komponenten](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/add-components-to-an-adaptive-form/integrate-adaptive-forms-turnstile)

- [Verwenden von Google reCAPTCHA in einem adaptiven Formular für Foundation-Komponenten](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/captcha-adaptive-forms-core-components)

## Ähnliche Artikel {#related-articles}

{{more-like-this}}

## Siehe auch {#see-also}

{{see-also}}
