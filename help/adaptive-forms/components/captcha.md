---
title: Kernkomponente für adaptive Formulare – Formular-Container
description: Ein adaptives Formular zu einer Web-Seite hinzufügen.
role: Architect, Developer, Admin, User
hide: true
hidefromtoc: true
source-git-commit: 8db061f3d6f1041336c379b34f3b6b7f03083560
workflow-type: tm+mt
source-wordcount: '723'
ht-degree: 54%

---


# Google reCPATCHA {#google-recaptcha}

CAPTCHA („Completely Automated Public Turing test to tell Computers and Humans Apart“ – „vollautomatischer öffentlicher Turing-Test zur Unterscheidung von Computern und Menschen“) ist ein Programm, das bei Onlinetransaktionen eingesetzt wird, um zwischen Menschen und Bots oder automatisierten Programmen zu unterscheiden. Es stellt eine Herausforderung dar und bewertet die Benutzerantwort, um festzustellen, ob es sich um einen Menschen oder einen Bot handelt, der mit der Site interagiert. Dabei wird verhindert, dass der Benutzer fortfährt, wenn der Test fehlschlägt, wodurch Onlinetransaktionen sicherer werden, da Bots keinen Spam senden oder andere bösartige Zwecke verfolgen können.

AEM Forms as a Cloud Service unterstützt Google reCAPTCHA v2 in Adaptive Forms. Sie können es verwenden, um eine CAPTCHA-Herausforderung bei der Formularübermittlung zu stellen.

## Verwendung {#reasons-to-use-google-recaptcha}


- **Spam und Bot Prevention**: Einer der Hauptgründe für die Verwendung von reCAPTCHA ist, zu verhindern, dass Spam-Sendungen und Bots mit bösartigen Bots Ihr Formular überschwemmen. Die erweiterten Algorithmen von reCAPTCHA können automatisierte Versuche zum Senden des Formulars erkennen und so sicherstellen, dass nur berechtigte Benutzer mit dem Formular interagieren können.

- **Verbesserte Sicherheit**: Durch die Implementierung von reCAPTCHA fügen Sie Ihrem adaptiven Formular eine zusätzliche Sicherheitsschicht hinzu. Dies hilft, sensible Informationen zu schützen und zu verhindern, dass böswillige Benutzer Schwachstellen ausnutzen.

- **Anwendererlebnis**: CAPTCHAs können zwar manchmal als Unannehmlichkeiten betrachtet werden, aber der adaptive Ansatz von reCAPTCHA bedeutet, dass den meisten Benutzern ein optimiertes, benutzerfreundliches Erlebnis präsentiert wird, das nur eine minimale Interaktion erfordert. Dies kann dazu beitragen, ein positives Benutzererlebnis zu erhalten und gleichzeitig Bots abzuschrecken.

- **Anpassungsfähigkeit**: Der adaptive Mechanismus von reCAPTCHA analysiert das Benutzerverhalten und Interaktionen, um festzustellen, ob es sich um Personen handelt. Das bedeutet, dass das Niveau der Herausforderung, die dem Benutzer präsentiert wird, je nach der Wahrscheinlichkeit, dass er ein Bot ist, variieren kann. Diese Anpassungsfähigkeit reduziert die Reibung für echte Benutzer und gewährleistet gleichzeitig eine hohe Sicherheit.

- **Geringere manuelle Moderation**: Durch eine erhebliche Reduzierung der Anzahl von Spam-Einsendungen und von Bot generierten Inhalten kann reCAPTCHA Zeit und Ressourcen sparen, die sonst für manuelle Moderation und Bereinigung ausgegeben würden.

## Version und Kompatibilität {#version-and-compatibility}

Die Kernkomponente &quot;Adaptive Forms Google reCAPTCHA&quot;wurde im August 2023 als Teil der Kernkomponentenversion veröffentlicht. Hier finden Sie eine Tabelle mit allen unterstützten Versionen, AEM-Kompatibilität und Links zur entsprechenden Dokumentation:

|  |  |
|---|---|
| Komponentenversion | AEM as a Cloud Service |
| --- | --- |
| v1 | Kompatibel mit<br>[Version 2.0.4](/help/versions.md) und höher | Kompatibel | Kompatibel |

Informationen zu Versionen und Freigaben der Kernkomponente finden Sie im Dokument [Kernkomponenten-Versionen](/help/versions.md).

## Technische Details {#technical-details}

Die neuesten Informationen zur adaptiven Forms Google-reCAPTCHA-Kernkomponente finden Sie in der technischen Dokumentation zu [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/recaptcha/v1/recaptcha). Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Entwicklerdokumentation für Kernkomponenten](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Im Dialogfeld &quot;Konfigurieren&quot;können Sie das reCAPTCHA-Erlebnis von Google einfach für Besucher anpassen. Sie können Google reCAPTCHA-Optionen auch einfach definieren, um ein nahtloses Benutzererlebnis zu gewährleisten.

### Registerkarte „Allgemein“ {#basic-tab}

- **Name**: Sie können eine Formularkomponente sowohl im Formular als auch im Regeleditor durch ihren eindeutigen Namen identifizieren. Der Name darf keine Leerzeichen oder Sonderzeichen enthalten.

- **Titel**: Sie können mit dem Titel leicht eine Komponente in einem Formular identifizieren. Standardmäßig wird der Titel über der Komponente angezeigt. Wenn Sie keinen Titel hinzufügen, wird der Name der Komponente anstelle des Titeltexts angezeigt.

- **Titel ausblenden**: Wählen Sie die Option aus, um den Titel der Komponente auszublenden.

- **Konfiguration** -

- **Typ** -

- **Komponente ausblenden**: Wählen Sie diese Option, um die Komponente aus dem Formular auszublenden. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor. Dies ist nützlich, wenn Sie Informationen speichern müssen, die Benutzende nicht sehen oder direkt ändern müssen.

- **Komponente deaktivieren**: Wählen Sie die Option zum Deaktivieren der Komponente aus. Die deaktivierte Komponente ist nicht aktiv und Endbenutzende können sie nicht bearbeiten. Die Daten der deaktivierten Komponente werden nicht übermittelt Der Benutzer kann den Wert des Felds sehen, kann ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor.

- **Schreibgeschützt**: Wählen Sie die Option aus, um die Komponente nicht bearbeitbar zu machen. Benutzende können den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor.

### Registerkarte „Validierung“ {#validation-tab}

- **Fehlermeldung**: Mit dieser Option können Sie eine Nachricht eingeben, die angezeigt wird, wenn das Kontrollkästchen **Erforderlich** aktiviert ist und das Feld leer bleibt.

