---
title: Formularcontainer-Komponente
description: Die Kernkomponente „Formularcontainer-Komponente“ ermöglicht die Erstellung einfacher Übermittlungsformulare.
role: Architektur, Entwickler, Administrator, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '961'
ht-degree: 99%

---


# Formularcontainer-Komponente {#form-container-component}

Die Kernkomponente „Formularcontainer-Komponente“ ermöglicht die Erstellung einfacher Übermittlungsformulare.

## Verwendung {#usage}

Die Formularcontainer-Komponente ermöglicht das Erstellen einfacher Informationsübermittlungsformulare und -funktionen, indem einfache WCM-Formulare unterstützt werden und eine verschachtelte Struktur verwendet wird, um zusätzliche Formularkomponenten zuzulassen.

Mithilfe des [Dialogfelds „Konfigurieren“](#configure-dialog) kann der Inhaltsbearbeiter die durch die Formularübermittlung ausgelöste Aktion definieren sowie die URL, die die Übermittlung handhaben soll, und ob ein Workflow ausgelöst werden soll. Der Vorlagenautor kann das [Dialogfeld „Design“](#design-dialog) verwenden, um die zulässigen Komponenten und deren Zuordnungen ähnlich dem Dialogfeld „Design“ für den [Standard-Layout-Container im Vorlageneditor](https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/sites/authoring/features/templates.translate.html) zu definieren.

>[!NOTE]
>
>Die Kernkomponente „Formularcontainer-Komponente“ unterstützt nur die Verwendung anderer Formularkomponenten-Kernkomponenten (Schaltfläche, Text, ausgeblendet usw.). Die Verwendung von [Foundation-Komponenten](https://docs.adobe.com/content/help/de-DE/experience-manager-65/authoring/siteandpage/default-components-foundation.html) Formularkomponenten innerhalb der Formularcontainer-Kernkomponenten (und umgekehrt) wird nicht unterstützt.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Formularcontainer-Komponente ist v2, die mit Version 2.0.0 der Kernkomponenten im Januar 2018 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v2 | Kompatibel | Kompatibel | Kompatibel |
| [v1](/help/components/v1/form-container-v1.md) | Kompatibel | Kompatibel | - |

Weitere Informationen zu Kernkomponentenversionen und -freigaben finden Sie in den [Kernkomponentenversionen](/help/versions.md).

## Musterkomponentenausgabe {#sample-component-output}

Um die Formular-Container-Komponente kennenzulernen und Beispiele für die Konfigurationsoptionen sowie HTML- und JSON-Ausgaben anzuzeigen, besuchen Sie die [Komponentenbibliothek](https://adobe.com/go/aem_cmp_library_form_container).

## Technische Details {#technical-details}

Die neueste technische Dokumentation zur Formularcontainer-Komponente [finden Sie auf GitHub](https://adobe.com/go/aem_cmp_tech_form_container_v2).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Über das Dialogfeld „Konfigurieren“ können Sie festlegen, welche Aktionen beim Senden der Komponente durchgeführt werden.

Je nach ausgewähltem **Aktionstyp** werden die verfügbaren Optionen im Container geändert. Die verfügbaren Aktionstypen sind:

* [Formulardaten posten](#post-data)
* [E-Mail](#mail)
* [Inhalt speichern](#store-content)

Unabhängig vom Typ gibt es [allgemeine Einstellungen](#general-settings), die für jede Aktion gelten.

### Formulardaten posten {#post-data}

Wenn das Formular übermittelt wird, übergibt der Aktionstyp für Formulardaten die übermittelten Daten zur Verarbeitung als JSON an einen Drittanbieter.

![Optionen zum Posten von Formulardaten im Dialogfeld „Bearbeiten“ der Formular-Container-Komponente](/help/assets/form-container-edit-post.png)

* **Endpunkt** – Der vollständig qualifizierte HTTPS-Dienst, der die Daten verarbeitet
* **Fehlermeldung** – Meldung, die angezeigt wird, wenn die Übermittlung nicht erfolgreich war

>[!TIP]
>Es gibt zusätzliche Timeout-Optionen, die ein Systemadministrator einstellen kann, um die Verarbeitung der weitergeleiteten Formulardaten zu handhaben. [Weitere Informationen finden Sie in der technischen Dokumentation zu GitHub.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/actions/rpc)

### E-Mail {#mail}

Wenn das Formular gesendet wird, sendet der Mail-Aktionstyp eine E-Mail an bestimmte Empfänger.

![E-Mail-Optionen im Dialogfeld „Bearbeiten“ der Formular-Container-Komponente ](/help/assets/form-container-edit-mail.png)

* **Betreff** - Betreffzeile der E-Mail, die beim Übermitteln des Formulars gesendet wird
* **Von** - die Absenderadresse der E-Mail, die beim Übermitteln des Formulars gesendet wird
* **An** - Die Adressen der Empfänger, die eine E-Mail bei der Formularübermittlung erhalten
   * Tippen oder klicken Sie auf die Schaltfläche **Hinzufügen**, um weitere Adressen hinzuzufügen.
   * Tippen oder klicken Sie auf die Schaltfläche **Löschen**, um eine E-Mail-Adresse zu entfernen.
* **CC** - Die Adressen der Empfänger, die eine Kopie der E-Mail erhalten, die beim Übermitteln des Formulars gesendet wird
   * Tippen oder klicken Sie auf die Schaltfläche **Hinzufügen**, um weitere Adressen hinzuzufügen.
   * Tippen oder klicken Sie auf die Schaltfläche **Löschen**, um eine E-Mail-Adresse zu entfernen.

### Inhalt speichern {#store-content}

Wenn das Formular übermittelt wird, wird der Inhalt des Formulars in einem bestimmten Repository gespeichert.

![Optionen zum Speichern von Inhalten im Dialogfeld „Bearbeiten“ des Formular-Containers](/help/assets/form-container-edit-store.png)

* **Inhalts-Pfad** - Inhalts-Repository-Pfad, in dem der übermittelte Inhalt gespeichert wird
* **Daten anzeigen** - Tippen oder klicken Sie, um gespeicherte gesendete Daten als JSON anzuzeigen.
* **Workflow starten** - Konfigurieren Sie den Start eines Workflows mit dem gespeicherten Inhalt als Nutzlast bei Formularübermittlung.

>[!NOTE]
>
>Um die Verwaltung von Benutzerdaten zu vereinfachen und die Trennung von Problemen zu erzwingen, wird im Allgemeinen nicht empfohlen, von Benutzern erstellte Inhalte im Repository zu speichern.
>
>Verwenden Sie stattdessen den Aktionstyp [Formulardaten posten](#post-data), um Benutzerinhalte an einen dedizierten Dienstleister weiterzuleiten.

### Allgemeine Einstellungen {#general-settings}

Unabhängig vom ausgewählten Aktionstyp kann eine Dankeseite immer definiert werden.

![Allgemeine Optionen im Dialogfeld „Bearbeiten“ der Formular-Container-Komponente ](/help/assets/form-container-edit-general.png)

* **Dankeseite** – Der Benutzer wird nach Abschluss der Formularübermittlung zur angegebenen Seite weitergeleitet.
   * Verwenden Sie das Dialogfeld „Auswahl“, um eine Ressource in AEM auszuwählen.
   * Wenn die Dankeseite nicht in AEM enthalten ist, geben Sie die absolute URL an. Nicht absolute URLs werden relativ zu AEM interpretiert.
   * Leer lassen, damit das Formular nach der Übermittlung wieder angezeigt wird.
* **ID** – Diese Option dient zur Kontrolle der eindeutigen Kennung der Komponente in der HTML-Datei und auf der [Datenschicht](/help/developing/data-layer/overview.md).
   * Wenn Sie das Feld leer lassen, wird automatisch eine eindeutige ID generiert, die Sie über die resultierende Seite finden.
   * Sofern eine ID angegeben wird, ist vom Autor sicherzustellen, dass diese eindeutig ist.
   * Änderungen der ID können sich auf das CSS-, JS- und Datenschicht-Tracking auswirken.

## Dialogfeld „Design“ {#design-dialog}

Das Dialogfeld „Design“ ermöglicht es dem Vorlagenautor, die zulässigen Komponenten und deren Zuordnungen für den Container ähnlich dem Dialogfeld „Design“ für den [Standard-Layout-Container im Vorlageneditor](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html) zu definieren.

### Registerkarte „Stile“ {#styles-tab}

Die Formular-Container-Komponente unterstützt das [Stilsystem](/help/get-started/authoring.md#component-styling) von AEM.
