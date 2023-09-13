---
title: Kernkomponente „Fußzeile“ für adaptive Formulare
description: Verwenden oder Anpassen der Kernkomponente „Fußzeile“ für adaptive Formulare.
role: Architect, Developer, Admin, User
exl-id: c8e7d3fe-4b82-4a80-8da2-19f6cff1e3e9
source-git-commit: ad3e3bca5cb46f14e864e4704c90ac3b62779794
workflow-type: ht
source-wordcount: '843'
ht-degree: 100%

---

# Fußzeile {#footer-adaptive-forms-core-component}

Eine Fußzeilen-Komponente in einem adaptiven Formular ist ein Bereich, der normalerweise am unteren Ende eines Formulars angezeigt wird und Informationen wie einen Copyright-Hinweis, Links zu verwandten Ressourcen oder Kontaktinformationen enthält. Eine Fußzeile kann zusätzliche Informationen enthalten, z. B. das Datum der letzten Aktualisierung, was für Benutzende mit einer Behinderung von Vorteil sein kann.

**Beispiel**

![](/help/adaptive-forms/assets/footer.png)

## Verwendung {#reasons-to-use-footer}

Es gibt verschiedene Gründe, warum es sinnvoll ist, eine Fußzeilen-Komponente in ein Formular einzufügen:

* **Rechtliche Anforderungen**: Einige Formulare müssen möglicherweise einen Haftungsausschluss, einen Copyright-Hinweis oder andere rechtliche Informationen enthalten. Eine Fußzeile geeigneter Platz für diese Informationen.

* **Navigation**: Eine Fußzeile kann Links zu anderen wichtigen Seiten auf der Website bereitstellen, z. B. Datenschutzrichtlinien, Nutzungsbedingungen oder Kontaktseiten.

* **Branding**: Eine Fußzeile kann verwendet werden, um ein Logo oder andere Branding-Elemente einzufügen, wodurch die Identität der Organisation oder Website unterstrichen wird.

* **Konsistenz**: Eine Fußzeile sorgt für Konsistenz im Design und Layout des Formulars, wodurch die Navigation für Benutzende intuitiver und einfacher wird.

* **Zusätzlicher Kontext**: Eine Fußzeile kann zusätzlichen Kontext für das Formular bereitstellen, z. B. einen Text, der das Formular beschreibt, oder einen Link zu verwandten Ressourcen, wodurch das Formular informativer und benutzerfreundlicher wird.

## Version und Kompatibilität {#version-and-compatibility}

Die Kernkomponente „Akkordeon“ für adaptive Formulare wurde im Februar 2023 als Teil der Kernkomponenten 2.0.4 für Cloud Service und der Kernkomponenten 1.1.12 für AEM 6.5.16.0 Forms oder höher veröffentlicht. Hier finden Sie eine Tabelle mit allen unterstützten Versionen, AEM-Kompatibilität und Links zur entsprechenden Dokumentation:

| Komponentenversion | AEM as a Cloud Service | AEM 6.5.16.0 Forms oder höher |
|---|---|---|
| v1 | Kompatibel mit<br>[Version 2.0.4](/help/adaptive-forms/version.md) und höher | Kompatibel mit<br>[Version 1.1.12](/help/adaptive-forms/version.md) und höher (aber nur bis Version 2.0.0). |

Informationen zu Versionen und Freigaben der Kernkomponente finden Sie im Dokument [Kernkomponenten-Versionen](/help/adaptive-forms/version.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technische Details {#technical-details}

Die neuesten Informationen zur Kernkomponente „Fußzeile“ für adaptive Formulare finden Sie in der technischen Dokumentation zu [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/footer/v1/footer). Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Entwicklerdokumentation für Kernkomponenten](/help/developing/overview.md).


## Dialogfeld „Konfigurieren“ {#configure-dialog}

Im Dialogfeld „Konfigurieren“ können Sie Ihre Fußzeile einfach anpassen. Sie können auch Optionen für Fußzeilen definieren, um das Benutzererlebnis zu verbessern.

![Registerkarte „Eigenschaften“](/help/adaptive-forms/assets/footer_propertiestab.png)

* **Dialogfeld „Bearbeiten“**
Das Dialogfeld „Bearbeiten“ bietet standardmäßige Rich-Text-Formatierungswerkzeuge, mit denen der Benutzende Text für die Fußzeile erstellen kann.

* **Fett** – Mit dieser Option wird Text fett formatiert, der zuvor markiert wurde oder nach dem Cursor eingegeben wird. `Ctrl+B` ist ein Tastaturbefehl.

* **Kursiv** – Mit dieser Option wird der Text kursiv formatiert, der zuvor markiert wurde oder nach dem Cursor eingegeben wird. `Ctrl+I` ist ein Tastaturbefehl.

![Aufzählungsoptionen](/help/adaptive-forms/assets/footer_bullet.png)


* **Aufzählungszeichen**

   * **Aufzählungssymbol** – Formatiert Text als Aufzählungsliste, der zuvor markiert wurde oder hinter dem Cursor eingefügt wird. Um eine Aufzählungsliste zu beenden, tippen oder klicken Sie erneut auf die Schaltfläche „Aufzählungszeichen“ oder geben Sie zwei Zeilenumbrüche hintereinander ein.

   * **Symbol für nummerierte Listen** – Formatiert Text als nummerierte Liste, der zuvor markiert wurde oder hinter dem Cursor eingefügt wird. Um eine nummerierte Liste zu beenden, tippen oder klicken Sie erneut auf die Schaltfläche „Nummerierte Listen“ oder geben Sie zwei Zeilenumbrüche hintereinander ein.

   * **Ausrückungssymbol** – Verringert die Einrückung von Text, der zuvor markiert wurde oder hinter dem Cursor eingefügt wird. Nur aktiv, wenn der ausgewählte Text bzw. die ausgewählte Position bereits eingerückt ist.

   * **Einrückungssymbol** – Erhöht die Einrückung von Text, der zuvor markiert wurde oder nach dem Cursor eingegeben wird.

![Hyperlink-Optionen](/help/adaptive-forms/assets/footer_link.png)

* **Hyperlink**

   * **Pfad** – Pfad eingeben
      1. Wählen Sie im Dialogfeld „Auswahl öffnen“ einen Pfad in AEM aus.
      1. Wenn der Link in AEM nicht angezeigt wird, geben Sie die absolute URL ein.
      1. Nicht-absolute Pfade werden als relativ zu AEM interpretiert.

   * **Alternativtext** – Geben Sie einen alternativen, beschreibenden Text für den Link ein.

   * **Ziel** – Link-Verhalten auswählen
      * Ziel
      * Selbe Registerkarte
      * Neue Registerkarte
      * Übergeordneter Frame
      * Top-Frame

   * **Symbol zum Aufheben einer Verknüpfung** – Mit dieser Option wird eine bereits auf den markierten Text angewendete Verknüpfung entfernt. Diese Option ist nur aktiv, wenn bereits ein Link ausgewählt ist.

   * **Absatzformat-Symbol** – Mit dieser Option können Sie eine Absatzformatierung auf den ausgewählten Text anwenden. Damit kann auch nach dem Cursor eingefügter Text formatiert werden. Mit dieser Option wird die Überschriftenebene des Titels definiert.

* **ID**: Diese Option ermöglicht es, die eindeutige Kennung der Komponente im HTML und in der Datenschicht festzulegen.

   * Wenn Sie das Feld leer lassen, wird automatisch eine eindeutige ID generiert, die Sie über die resultierende Seite finden.
   * Sofern eine ID angegeben wird, ist vom Autor bzw. der Autorin sicherzustellen, dass diese eindeutig ist.
   * Änderungen der ID können sich auf das CSS-, JS- und Datenschicht-Tracking auswirken.

## Verwandter Artikel {#related-article}

* [Erstellen eines adaptiven Formulars in einer AEM Sites-Seite oder einem Experience Fragment](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=de)

* [Erstellen eines eigenständigen adaptiven Formulars](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html?lang=de)


## Siehe auch {#see-also}

* [Akkordeon](/help/adaptive-forms/components/accordion.md)
* [Schaltfläche](/help/adaptive-forms/components/button.md)
* [Kontrollkästchen Gruppe](/help/adaptive-forms/components/checkbox-group.md)
* [Datumsauswahl](/help/adaptive-forms/components/date-picker.md)
* [Dropdown-Liste](/help/adaptive-forms/components/drop-down.md)
* [E-Mail-Eingabe](/help/adaptive-forms/components/email-input.md)
* [Formular-Container](/help/adaptive-forms/components/form-container.md)
* [Dateianhang](/help/adaptive-forms/components/file-attachment.md)
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