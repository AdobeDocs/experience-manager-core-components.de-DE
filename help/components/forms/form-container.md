---
title: Formularcontainer-Komponente
description: Die Kernkomponente „Formularcontainer-Komponente“ ermöglicht die Erstellung einfacher Übermittlungsformulare.
translation-type: ht
source-git-commit: 95c0621f5423bfa515fe5e8b693e127ea56b4ae0

---


# Formularcontainer-Komponente {#form-container-component}

Die Kernkomponente „Formularcontainer-Komponente“ ermöglicht die Erstellung einfacher Übermittlungsformulare.

## Nutzung {#usage}

Die Formularcontainer-Komponente ermöglicht das Erstellen einfacher Informationsübermittlungsformulare und -funktionen, indem einfache WCM-Formulare unterstützt werden und eine verschachtelte Struktur verwendet wird, um zusätzliche Formularkomponenten zuzulassen.

Mithilfe des [Dialogfelds „Konfigurieren“](#configure-dialog) kann der Inhaltsbearbeiter die durch die Formularübermittlung ausgelöste Aktion definieren und festlegen, wo der gesendete Inhalt gespeichert werden soll und ob ein Workflow ausgelöst werden soll. Der Vorlagenautor kann das [Dialogfeld „Design“](#design-dialog) verwenden, um die zulässigen Komponenten und deren Zuordnungen ähnlich dem Dialogfeld „Design“ für den [Standard-Layout-Container im Vorlageneditor](https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/sites/authoring/features/templates.translate.html) zu definieren.

>[!NOTE]
>
>Die Kernkomponente „Formularcontainer-Komponente“ unterstützt nur die Verwendung anderer Formularkomponenten-Kernkomponenten (Schaltfläche, Text, ausgeblendet usw.). Die Verwendung von [Foundation-Komponenten](https://docs.adobe.com/content/help/de-DE/experience-manager-65/authoring/siteandpage/default-components-foundation.html) Formularkomponenten innerhalb der Formularcontainer-Kernkomponenten (und umgekehrt) wird nicht unterstützt.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Formularcontainer-Komponente ist v2, die mit Version 2.0.0 der Kernkomponenten im Januar 2018 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.3 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |--- |---|
| v2 | Kompatibel | Kompatibel | Kompatibel | Kompatibel |
| [v1](/help/components/v1/form-container-v1.md) | Kompatibel | Kompatibel | Kompatibel | - |

Weitere Informationen zu Kernkomponentenversionen und -freigaben finden Sie in den [Kernkomponentenversionen](/help/versions.md).

## Musterkomponentenausgabe {#sample-component-output}

Um die Formular-Container-Komponente kennenzulernen und Beispiele für die Konfigurationsoptionen sowie HTML- und JSON-Ausgaben anzuzeigen, besuchen Sie die [Komponentenbibliothek](https://adobe.com/go/aem_cmp_library_form_container_de).

## Technische Details {#technical-details}

Die neueste technische Dokumentation zur Formularcontainer-Komponente [finden Sie auf GitHub](https://adobe.com/go/aem_cmp_tech_form_container_v2_de).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Über das Dialogfeld „Konfigurieren“ können Sie festlegen, welche Aktionen beim Senden der Komponente durchgeführt werden.

![](/help/assets/screen_shot_2018-01-12at122046.png)

Je nach ausgewähltem **Aktionstyp** werden die verfügbaren Optionen im Container geändert. Die verfügbaren Aktionstypen sind:

* [E-Mail](#mail)
* [Inhalt speichern](#store-content)
* [Bestellung absenden](#submit-order)
* [Auftrag aktualisieren](#update-order)

Unabhängig vom Typ gibt es [allgemeine Einstellungen](#general-settings), die für jede Aktion gelten.

### E-Mail {#mail}

Wenn das Formular gesendet wird, sendet der Mail-Aktionstyp eine E-Mail an bestimmte Empfänger.

![](/help/assets/screen_shot_2018-01-12at122554.png)

* **Betreff**
Betreffzeile der E-Mail, die bei der Übermittlung des Formulars gesendet wird
* **Von**
die Absenderadresse der E-Mail, die bei der Übermittlung des Formulars gesendet wird
* **An**
die Adressen der Empfänger, die eine E-Mail bei der Formularübermittlung erhalten

   * Tippen oder klicken Sie auf die Schaltfläche **Hinzufügen**, um weitere Adressen hinzuzufügen.
   * Tippen oder klicken Sie auf die Schaltfläche **Löschen**, um eine E-Mail-Adresse zu entfernen.
* **CC**
Die Adressen der Empfänger, die eine Kopie der E-Mail erhalten, die bei der Formularübermittlung gesendet wird
   * Tippen oder klicken Sie auf die Schaltfläche **Hinzufügen**, um weitere Adressen hinzuzufügen.
   * Tippen oder klicken Sie auf die Schaltfläche **Löschen**, um eine E-Mail-Adresse zu entfernen.

### Inhalt speichern {#store-content}

Wenn das Formular übermittelt wird, wird der Inhalt des Formulars in einem bestimmten Repository gespeichert.

![](/help/assets/screen_shot_2018-01-12at122538.png)

* **Inhaltspfad**
Content Repository-Pfad, in dem die übermittelten Inhalte gespeichert sind.
* **Daten anzeigen**
Tippen oder Klicken, um gespeicherte gesendete Daten als JSON anzuzeigen
* **Workflow starten**
Konfigurieren, um einen Workflow mit dem gespeicherten Inhalt als Nutzlast bei der Formularübertragung zu starten.

### Bestellung absenden {#submit-order}

Wenn das Formular übermittelt wird, wird die Bestellung übermittelt.

![](/help/assets/chlimage_1-3.png)

### Auftrag aktualisieren {#update-order}

Wenn das Formular übermittelt wird, wird die Bestellung aktualisiert.

![](/help/assets/chlimage_1-4.png)

### Allgemeine Einstellungen {#general-settings}

Unabhängig vom ausgewählten Aktionstyp kann eine Dankeseite immer definiert werden.

![](/help/assets/chlimage_1-5.png)

Der Benutzer wird nach Abschluss der Formularübermittlung zur angegebenen Seite weitergeleitet.

* Verwenden Sie das Dialogfeld „Auswahl“, um eine Ressource in AEM auszuwählen.
* Wenn die Dankeseite nicht in AEM enthalten ist, geben Sie die absolute URL an. Nicht absolute URLs werden relativ zu AEM interpretiert.
* Leer lassen, damit das Formular nach der Übermittlung wieder angezeigt wird.

## Dialogfeld „Design“ {#design-dialog}

Das Dialogfeld „Design“ ermöglicht es dem Vorlagenautor, die zulässigen Komponenten und deren Zuordnungen für den Container ähnlich dem Dialogfeld „Design“ für den [Standard-Layout-Container im Vorlageneditor](https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/sites/authoring/features/templates.translate.html) zu definieren.
