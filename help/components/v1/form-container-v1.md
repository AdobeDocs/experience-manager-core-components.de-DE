---
title: Formular-Container-Komponente (v1)
description: Die Kernkomponente „Formular-Container-Komponente“ ermöglicht die Erstellung einfacher Übermittlungsformulare.
index: n
role: Architect, Developer, Admin, User
exl-id: 1e34219f-fa82-494e-82e2-1b4d63d37fea
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '609'
ht-degree: 100%

---

# Formular-Container-Komponente (v1) {#form-container-component-v1}

Die Kernkomponente „Formular-Container-Komponente“ ermöglicht die Erstellung einfacher Übermittlungsformulare.

## Nutzung {#usage}

Die Formular-Container-Komponente ermöglicht den Aufbau einfacher Formulare und Funktionen zur Informationsübermittlung, indem sie einfache WCM-Formulare unterstützt und eine verschachtelte Struktur verwendet, um zusätzliche Formularkomponenten zu ermöglichen.

Mithilfe des [Dialogfelds „Einstellungen“](#settings-dialog) kann der Inhaltseditor definieren, welche Art von Aktion durch eine Formularübermittlung ausgelöst wird, wo der gesendete Inhalt gespeichert werden soll und ob ein Workflow ausgelöst werden soll. Der Vorlagenautor kann das [Dialogfeld „Design“](#design-dialog) verwenden, um die zulässigen Komponenten und deren Zuordnungen ähnlich dem Dialogfeld „Design“ für den [Standard-Layout-Container im Vorlageneditor](https://helpx.adobe.com/de/experience-manager/6-4/sites/authoring/using/templates.html) zu definieren.

## Version und Kompatibilität {#version-and-compatibility}

In diesem Dokument wird die v1 der Formular-Container-Komponente beschrieben, die ursprünglich mit Version 1.0.0 der Kernkomponenten mit AEM 6.3 eingeführt wurde.

In der folgenden Tabelle ist die Kompatibilität von v1 der Formular-Container-Komponente aufgeführt.

| AEM-Version | Formular-Container-Komponente v1 |
|--- |--- |
| 6.3 | Kompatibel |
| 6.4 | Kompatibel |

>[!CAUTION]
>
>In diesem Dokument wird v1 der Formular-Container-Komponente beschrieben.
>
>Weitere Informationen zur aktuellen Version der Formular-Container-Komponente finden Sie im Dokument [Formular-Container-Komponente](/help/components/forms/form-container.md).

## Dialogfeld „Einstellungen“ {#settings-dialog}

Über das Dialogfeld „Einstellungen“ können Sie festlegen, welche Aktionen beim Übermitteln der Komponente durchgeführt werden.

![](/help/assets/chlimage_1.png)

Je nach ausgewähltem **Aktionstyp** werden die verfügbaren Optionen im Container geändert. Die verfügbaren Aktionstypen sind:

* [E-Mail](#mail)
* [Inhalt speichern](#store-content)
* [Bestellung übermitteln](#submit-order)
* [Auftrag aktualisieren](#update-order)

Unabhängig vom Typ gibt es [allgemeine Einstellungen](#general-settings), die für jede Aktion gelten.

### E-Mail {#mail}

Wenn das Formular gesendet wird, sendet der Mail-Aktionstyp eine E-Mail an bestimmte Empfänger.

![](/help/assets/chlimage_1-1.png)

* **Betreff** - Betreffzeile der E-Mail, die beim Übermitteln des Formulars gesendet wird
* **Von** - die Absenderadresse der E-Mail, die beim Übermitteln des Formulars gesendet wird
* **Bis** - Die Adressen der Empfänger, die eine E-Mail bei der Formularübermittlung erhalten
   * Tippen oder klicken Sie auf die Schaltfläche **Hinzufügen**, um weitere Adressen hinzuzufügen.
   * Tippen oder klicken Sie auf die Schaltfläche **Löschen**, um eine E-Mail-Adresse zu entfernen.
* **CC** - Die Adressen der Empfänger, die eine Kopie der E-Mail erhalten, die beim Übermitteln des Formulars gesendet wird
   * Tippen oder klicken Sie auf die Schaltfläche **Hinzufügen**, um weitere Adressen hinzuzufügen.
   * Tippen oder klicken Sie auf die Schaltfläche **Löschen**, um eine E-Mail-Adresse zu entfernen.

### Inhalt speichern {#store-content}

Wenn das Formular übermittelt wird, wird der Inhalt des Formulars in einem bestimmten Repository gespeichert.

![](/help/assets/chlimage_1-2.png)

* **Inhalts-Pfad** - Inhalts-Repository-Pfad, in dem der übermittelte Inhalt gespeichert wird
* **Daten anzeigen** - Tippen oder klicken Sie, um gespeicherte gesendete Daten als JSON anzuzeigen.
* **Workflow starten** - Konfigurieren Sie den Start eines Workflows mit dem gespeicherten Inhalt als Nutzlast bei Formularübermittlung.

### Bestellung übermitteln {#submit-order}

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

Das Dialogfeld „Design“ ermöglicht es dem Vorlagenautor, die zulässigen Komponenten und deren Zuordnungen für den Container ähnlich dem Dialogfeld „Design“ für den [Standard-Layout-Container im Vorlageneditor](https://helpx.adobe.com/de/experience-manager/6-4/sites/authoring/using/templates.html#main-pars_title_1754153843) zu definieren.

## Technische Details {#technical-details}

Die neueste technische Dokumentation zur Formular-Container-Komponente [finden Sie auf GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/container/v1/container).

Das gesamte Kernkomponentenprojekt kann von GitHub heruntergeladen werden.

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).
