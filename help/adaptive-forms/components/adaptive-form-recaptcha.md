---
title: Kernkomponente für adaptive Formulare – Google reCAPTCHA
description: Mit dem Google reCAPTCHA-Dienst können Sie ganz einfach mit AEM Forms die Sicherheit von Formularen verbessern. Erklärung der Eigenschaften von reCaptcha für adaptive Formulare
role: Architect, Developer, Admin, User
exl-id: 2d986b90-e596-4e8f-9a32-0ebced5461c8
source-git-commit: 6725784bd4c94d433c91d6bd65d14d03cbefd954
workflow-type: ht
source-wordcount: '0'
ht-degree: 100%

---


# Adaptives Formular – reCAPTCHA {#google-recaptcha}

CAPTCHA („Completely Automated Public Turing test to tell Computers and Humans Apart“ – „vollautomatischer öffentlicher Turing-Test zur Unterscheidung von Computern und Menschen“) ist ein Programm, das bei Online-Transaktionen eingesetzt wird, um zwischen Menschen und Bots oder automatisierten Programmen zu unterscheiden. Es stellt eine herausfordernde Aufgabe und bewertet die Benutzerantwort, um festzustellen, ob es sich um einen Menschen oder einen Bot handelt, der mit der Site interagiert. Dabei wird verhindert, dass der Benutzer fortfährt, wenn der Test fehlschlägt, wodurch Onlinetransaktionen sicherer werden, da Bots keinen Spam senden oder andere bösartige Zwecke verfolgen können.

AEM Forms as a Cloud Service unterstützt Google reCAPTCHA v2 in adaptiven Formularen. Sie können es verwenden, um eine CAPTCHA-Herausforderung bei der Formularübermittlung zu stellen

{{traditional-aem}}

## Verwendung {#reasons-to-use-google-recaptcha}


- **Spam- und Bot-Prävention**: Einer der Hauptgründe für die Verwendung von reCAPTCHA ist, zu verhindern, dass Spam-Sendungen und bösartige Bots Ihr Formular überschwemmen. Die erweiterten Algorithmen von reCAPTCHA können automatisierte Versuche beim Senden des Formulars erkennen und so sicherstellen, dass nur legitime Benutzerinnen und Benutzer mit dem Formular interagieren können.

- **Verbesserte Sicherheit**: Durch die Implementierung von reCAPTCHA fügen Sie Ihrem adaptiven Formular eine zusätzliche Sicherheitsschicht hinzu. Dies hilft, sensible Informationen zu schützen und zu verhindern, dass böswillige Menschen Schwachstellen ausnutzen.

- **Anwendererlebnis**: CAPTCHAs können zwar manchmal als Unannehmlichkeiten betrachtet werden, aber der adaptive Ansatz von reCAPTCHA bedeutet, dass den meisten Benutzerinnen und Benutzern ein optimiertes, benutzerfreundliches Erlebnis präsentiert wird, das nur eine minimale Interaktion erfordert. Dies kann dazu beitragen, ein positives Anwendererlebnis zu erhalten und gleichzeitig Bots fernzuhalten.

- **Anpassungsfähigkeit**: Der adaptive Mechanismus von reCAPTCHA analysiert das Benutzerverhalten und Interaktionen, um festzustellen, ob es sich um Menschen handelt oder nicht. Das bedeutet, dass das Niveau der Herausforderung, die der Benutzerin bzw. dem Benutzer präsentiert wird, variieren kann, je nach der Wahrscheinlichkeit, mit der es sich um einen Bot handelt. Diese Anpassungsfähigkeit reduziert die Reibung für echte Benutzerinnen und Benutzer und gewährleistet gleichzeitig eine hohe Sicherheit.

- **Geringere manuelle Moderation**: Durch eine erhebliche Reduzierung der Anzahl von Spam-Einsendungen und von Bots generierten Inhalten kann reCAPTCHA Zeit und Ressourcen sparen, die sonst für manuelle Moderation und Bereinigung ausgegeben werden müssten.

## Version und Kompatibilität {#version-and-compatibility}

Die Kernkomponente „Google reCAPTCHA“ für adaptive Formulare wurde im August 2023 als Teil der „Version“ der Kernkomponenten veröffentlicht. Hier finden Sie eine Tabelle mit allen unterstützten Versionen, AEM-Kompatibilität und Links zur entsprechenden Dokumentation:


| Komponentenversion | AEM as a Cloud Service |
|--- |--- |
| v1 | Kompatibel mit<br>[Version 2.0.4](/help/versions.md) und höher | Kompatibel | Kompatibel |

Informationen zu Versionen und Freigaben der Kernkomponente finden Sie im Dokument [Kernkomponenten-Versionen](/help/versions.md).

## Technische Details {#technical-details}

Die neuesten Informationen zur Kernkomponente „Google reCAPTCHA“ für adaptive Formulare finden Sie in der technischen Dokumentation auf [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/recaptcha/v1/recaptcha). Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Entwicklerdokumentation für Kernkomponenten](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Sie können Ihr Google reCAPTCHA-Erlebnis für Besucherinnen und Besucher im Dialogfeld „Konfigurieren“ einfach anpassen. Sie können auch einfach Optionen für Google reCAPTCHA definieren, um ein nahtloses Anwendererlebnis zu gewährleisten.

### Registerkarte „Allgemein“ {#basic-tab}

![Registerkarte „Allgemein“](/help/adaptive-forms/assets/recaptcha-basictab.png)

- **Name**: Sie können eine Formularkomponente sowohl im Formular als auch im Regeleditor durch ihren eindeutigen Namen identifizieren. Der Name darf keine Leerzeichen oder Sonderzeichen enthalten.

- **Titel**: Mit dem Titel können Sie eine Komponente in einem Formular leicht identifizieren. Standardmäßig wird der Titel oberhalb der Komponente angezeigt. Wenn Sie keinen Titel hinzufügen, wird der Name der Komponente anstelle des Titeltexts angezeigt.

- **Rich-Text für Titel zulassen**: Diese Funktionen ermöglichen es Benutzenden, einfache Texttitel zu formatieren, die Funktionen wie fett, kursiv, unterstrichener Text, verschiedene Schriftarten, Schriftgrößen, Farben und zusätzliche Optionen enthalten und so die visuelle Darstellung und Anpassung zu verbessern. Sie bietet mehr Flexibilität und kreative Kontrolle bei der Hervorhebung von Titeln in Dokumenten, Websites oder Anwendungen.\
  Durch Aktivieren des Kontrollkästchens **„Rich-Text für Titel zulassen“ werden Formatierungsoptionen sichtbar, mit denen Sie den Titel der Komponente gestalten können. Um auf alle verfügbaren Formatierungsoptionen zuzugreifen, können Sie auf die Registerkarte ![Vollbildsymbol](/help/adaptive-forms/assets/fullscreen-icon.png) klicken.

  ![Rich-Text-Unterstützung](/help/adaptive-forms/assets/richtext-support-title.png)

- **Titel ausblenden**: Wählen Sie die Option aus, um den Titel der Komponente auszublenden.
- **Als ungebundenes Formularelement markieren**: Mit dieser Option können Sie Formularfelder konfigurieren, die mit keinem Schema verbunden sind. Mit dieser Option können Sie Daten speichern, ohne die Datenquelle zu aktualisieren. Außerdem können Sie damit Daten auf eine benutzerdefinierte Art und Weise verarbeiten, getrennt von der standardmäßigen Datenbankintegration.
- **Konfigurationseinstellungen**: Wählen Sie den Konfigurations-Container aus, der die Cloud-Konfiguration enthält, die AEM Forms mit dem reCAPTCHA-Dienst von Google verbindet.

  >[!NOTE]
  >
  > Im Artikel [Verwenden von Google reCAPTCHA in einem adaptiven Formular in AEM, das auf Kernkomponenten basiert](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/captcha-adaptive-forms-core-components) erfahren Sie, wie Sie Google reCAPTCHA für Ihre Umgebung erstellen und konfigurieren.

- **Typ**: Wählen Sie diese Option, um die Größe für reCAPTCHA auszuwählen.
   - **Normal**: Bezieht sich auf die standardmäßige, größere Version des reCAPTCHA-Widgets, die für Benutzende besser sichtbar und leichter zu nutzen sein sollte, insbesondere auf Geräten mit größeren Bildschirmen.
   - **Kompakt**: Bezieht sich auf eine kleinere Version des reCAPTCHA-Widgets. Diese Option eignet sich bei wenig Platz, z. B. auf Mobilgeräten oder in engen Layouts auf Web-Seiten.

- **Komponente ausblenden**: Wählen Sie diese Option, um die Komponente aus dem Formular auszublenden. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor. Dies ist nützlich, wenn Sie Informationen speichern müssen, die Benutzende nicht sehen oder direkt ändern müssen.

- **Komponente deaktivieren**: Wählen Sie die Option zum Deaktivieren der Komponente aus. Die deaktivierte Komponente ist nicht aktiv und Endbenutzende können sie nicht bearbeiten. Die Daten der deaktivierten Komponente werden nicht übermittelt. Die Benutzerin bzw. der Benutzer kann den Wert des Felds sehen, kann ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor.

- **Schreibgeschützt**: Wählen Sie die Option aus, um die Komponente nicht bearbeitbar zu machen. Benutzende können den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor.

### Registerkarte „Validierung“ {#validation-tab}

![Registerkarte „Validierung“](/help/adaptive-forms/assets/recaptcha-validationtab.png)

- **Fehlermeldung**: Mit dieser Option können Sie eine Nachricht eingeben, die angezeigt wird, wenn das Kontrollkästchen **Erforderlich** aktiviert ist und das Feld leer bleibt.

- **Meldung zur Skriptvalidierung**: Mit dieser Option können Sie eine Meldung eingeben, die angezeigt werden soll, wenn die Skriptvalidierung fehlschlägt.

## Dialogfeld „Design“ {#design-dialog}

Verwenden Sie das Dialogfeld „Design“, um CSS-Stile für die reCAPTCHA-Komponente zu definieren und zu verwalten.

### Registerkarte „Stile“ {#styles-design-tab}

Die reCAPTCHA-Kernkomponente in adaptiven Formularen unterstützt das [Stilsystem](/help/get-started/authoring.md#component-styling) von AEM.

![Dialogfeld „Design“](/help/adaptive-forms/assets/checkbox-style.png)

- **Standard-CSS-Klassen**: Sie können eine standardmäßige CSS-Klasse für die reCAPTCHA-Kernkomponente für adaptive Formulare bereitstellen.

- **Zulässige Stile**: Sie können Stile definieren, indem Sie den Namen und die CSS-Klasse für den Stil angeben. Sie können beispielsweise einen Stil mit dem Namen „Fettschrift“ erstellen und die CSS-Klasse „Schriftbreite: Fett“ bereitstellen. Sie können diese Stile bei einem adaptiven Formular im adaptiven Formular-Editor anwenden. Um einen Stil anzuwenden, wählen Sie im Editor für adaptive Formulare die Komponente aus, auf die Sie den Stil anwenden möchten, navigieren Sie zum Eigenschaften-Dialog und wählen Sie den gewünschten Stil aus der Dropdown-Liste **Stile**. Wenn Sie die Stile aktualisieren oder ändern müssen, kehren Sie einfach zum Dialogfeld „Design“ zurück, aktualisieren die Stile auf der Registerkarte „Stile“ und speichern die Änderungen.

### Benutzerdefinierte Eigenschaften

![Dialogfeld „Benutzerdefinierte Eigenschaften“](/help/adaptive-forms/assets/checkbox-customproperties.png)

Mit der Option „Benutzerdefinierte Eigenschaften“ können Sie mithilfe der Formularvorlage benutzerdefinierte Attribute (Schlüsselwertpaare) mit einer Kernkomponente eines adaptiven Formulars verknüpfen. Die benutzerdefinierten Eigenschaften werden im Eigenschaftenbereich der Headless-Ausgabedarstellung der Komponente angezeigt. So kann ein dynamisches Formularverhalten erzeugt werden, das sich je nach den benutzerdefinierten Attributwerten anpasst. Beispielsweise können Entwickelnde verschiedene Ausgabedarstellungen einer Headless-Formularkomponente für Mobile-, Desktop- oder Web-Plattformen entwerfen und so das Benutzererlebnis auf einer Vielzahl von Geräten erheblich verbessern.
- **Gruppenname**: Sie können einen Namen angeben, um die Gruppe der benutzerdefinierten Eigenschaften zu kennzeichnen. Sie können mehrere Gruppen benutzerdefinierter Eigenschaften hinzufügen, löschen oder neu anordnen. Nach dem Hinzufügen der Gruppe benutzerdefinierter Eigenschaften werden folgende Optionen angezeigt:

   - **Schlüssel-Wert-Paare**: Sie können mehrere Namen und Werte benutzerdefinierter Eigenschaften hinzufügen, indem Sie für jede Gruppe benutzerdefinierter Eigenschaften auf **Hinzufügen** klicken.

   - **Löschen**: Tippen oder klicken Sie auf diese Option, um den Namen und den Wert der benutzerdefinierten Eigenschaft zu löschen.

   - **Neu anordnen**: Ordnen Sie den Namen und Wert der benutzerdefinierten Eigenschaft Tippen oder Klicken und Ziehen neu an.


## Ähnliche Artikel {#related-articles}

{{more-like-this}}

## Siehe auch {#see-also}

{{see-also}}
