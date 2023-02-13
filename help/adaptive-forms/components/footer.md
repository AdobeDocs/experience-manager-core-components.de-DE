---
title: Adaptive Forms-Kernkomponente - Fußzeile
description: Verwenden oder Anpassen der Kernkomponente "Adaptive Forms-Fußzeile".
role: Architect, Developer, Admin, User
source-git-commit: b378fbd5695f82b8fc9de3a2d53a8387099ae33b
workflow-type: tm+mt
source-wordcount: '749'
ht-degree: 15%

---


# den Namen Fußzeile zu {#footer-adaptive-forms-core-component}

Eine Fußzeilenkomponente in einem adaptiven Formular ist ein Bereich, der normalerweise unten im Formular angezeigt wird und Informationen wie einen Copyright-Hinweis, Links zu verwandten Ressourcen oder Kontaktinformationen enthält. Eine Fußzeile kann zusätzliche Informationen bereitstellen, z. B. das Datum der letzten Aktualisierung, was für Benutzer mit Zugänglichkeitsanforderungen von Vorteil sein kann.

**Beispiel**

![](/help/adaptive-forms/assets/footer.png)

## Verwendung {#reasons-to-use-footer}

Es gibt verschiedene Gründe, warum es sinnvoll ist, eine Fußzeilenkomponente in ein Formular einzuschließen:

* **Rechtliche Anforderungen**: Einige Formulare müssen möglicherweise einen Haftungsausschluss, einen Copyright-Hinweis oder andere rechtliche Informationen enthalten. Eine Fußzeile ist ein bequemer Ort, um diese Informationen einzuschließen.

* **Navigation**: Eine Fußzeile kann Links zu anderen wichtigen Seiten auf der Website bereitstellen, z. B. Datenschutzrichtlinien, Nutzungsbedingungen oder Kontaktseiten.

* **Branding**: Eine Fußzeile kann verwendet werden, um ein Logo oder andere Branding-Elemente einzufügen, wodurch die Identität der Organisation oder Website gestärkt wird.

* **Konsistenz**: Eine Fußzeile sorgt für Konsistenz im Design und Layout des Formulars, wodurch die Navigation für Benutzer intuitiver und einfacher wird.

* **Zusätzlicher Kontext**: Eine Fußzeile kann zusätzlichen Kontext für das Formular bereitstellen, z. B. einen Text, der das Formular beschreibt, oder einen Link zu verwandten Ressourcen, wodurch das Formular informativer und benutzerfreundlicher wird.

## Version und Kompatibilität {#version-and-compatibility}

Die Kernkomponente &quot;Adaptive Forms-Fußzeile&quot;wurde im Februar 2023 als Teil der Kernkomponenten 2.0.4 veröffentlicht. Hier finden Sie eine Tabelle mit allen unterstützten Versionen, AEM Kompatibilität und Links zur entsprechenden Dokumentation:

|  |  |
|---|---|
| Komponentenversion | AEM as a Cloud Service |
| --- | --- |
| v1 | Kompatibel mit<br>[Version 2.0.4](/help/versions.md) und höher | Kompatibel | Kompatibel |

Informationen zu Kernkomponentenversionen und -versionen finden Sie im Abschnitt [Kernkomponenten-Versionen](/help/versions.md) Dokument.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technische Details {#technical-details}

Die neuesten Informationen zur Kernkomponente &quot;Adaptive Forms Footer&quot;finden Sie in der technischen Dokumentation zu [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/footer/v1/footer). Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie im Abschnitt [Entwicklerdokumentation für Kernkomponenten](/help/developing/overview.md).


## Dialogfeld „Konfigurieren“ {#configure-dialog}

Im Dialogfeld &quot;Konfigurieren&quot;können Sie Ihre Fußzeilenerfahrung für Besucher einfach anpassen. Sie können auch Fußzeilenoptionen für ein nahtloses Benutzererlebnis definieren.

![Registerkarte „Eigenschaften“](/help/adaptive-forms/assets/footer_propertiestab.png)

* **Dialogfeld &quot;Bearbeiten&quot;**
Das Dialogfeld &quot;Bearbeiten&quot;bietet standardmäßige Rich-Text-Formatierungswerkzeuge, mit denen der Benutzer Text für die Fußzeile erstellen kann.

* **Fett** - Bei dieser Option wird der ausgewählte Text fett formatiert oder der nach dem Cursor eingegebene Text fett formatiert. `Ctrl+B` ist ein Tastaturbefehl.

* **Kursiv** - Diese Option wendet die kursiv formatierte Formatierung auf den ausgewählten Text an oder kursiv Text, der nach dem Cursor eingegeben wird. `Ctrl+I` ist ein Tastaturbefehl.

![Aufzählungsoptionen](/help/adaptive-forms/assets/footer_bullet.png)


* **Aufzählungszeichen**

   * **Symbol &quot;Aufzählungszeichen&quot;** - Formatiert den ausgewählten Text als Liste mit Aufzählungszeichen oder beginnt mit dem Einfügen einer Liste mit Aufzählungszeichen nach dem Cursor. Um eine Liste mit Aufzählungszeichen zu beenden, tippen oder klicken Sie erneut auf die Schaltfläche Aufzählung oder geben Sie zwei Zeilenumbrüche hintereinander ein.

   * **Symbol &quot;Nummerierte Liste&quot;** - Formatiert den ausgewählten Text als nummerierte Liste oder beginnt mit dem Einfügen einer nummerierten Liste nach dem Cursor. Um eine nummerierte Liste zu beenden, tippen oder klicken Sie erneut auf die Schaltfläche Nummeriert oder geben Sie zwei Zeilenumbrüche hintereinander ein.

   * **Symbol &quot;Ausrücken&quot;** - Dadurch wird der Einzug des ausgewählten Texts oder des nach dem Cursor eingegebenen Texts verringert. Nur aktiv, wenn der ausgewählte Text bzw. die ausgewählte Position bereits eingerückt ist.

   * **Symbol &quot;Einzug&quot;** - Dadurch wird der Einzug des ausgewählten Texts oder des nach dem Cursor eingegebenen Texts erhöht.

![Hyperlink-Optionen](/help/adaptive-forms/assets/footer_link.png)

* **Hyperlink**

   * **Pfad** - Pfad eingeben
      1. Verwenden Sie das Dialogfeld Auswahl öffnen , um einen Pfad in AEM auszuwählen.
      1. Wenn der Link nicht in AEM enthalten ist, geben Sie die absolute URL ein.
      1. Nicht absolute Pfade werden als relativ zu AEM interpretiert.
   * **Alternativtext** - Geben Sie alternativen beschreibenden Text für den Link ein.

   * **Target** - Linkverhalten auswählen
      * Ziel
      * Selbe Registerkarte
      * Neue Registerkarte
      * Übergeordneter Frame
      * Top-Frame
   * **Symbol &quot;Verknüpfung aufheben&quot;** - Mit dieser Option wird ein Link entfernt, der bereits auf den ausgewählten Text angewendet wurde. Diese Option ist nur aktiv, wenn der Link bereits ausgewählt ist.

   * **Symbol &quot;Absatzformat&quot;** - Mit dieser Option können Sie Absatzformatierungen auf den ausgewählten Text anwenden. Es hilft Ihnen auch, den nach dem Cursor eingefügten Text zu formatieren. Sie definiert die Überschriftenebene des Titels.



* **ID**: Mit dieser Option können Sie die eindeutige Kennung der Komponente auf der HTML und in der Datenschicht steuern.

   * Wenn Sie das Feld leer lassen, wird automatisch * eine eindeutige ID generiert und Sie können die resultierende Seite prüfen.
   * Sofern eine ID angegeben wird, ist vom Autor bzw. der Autorin sicherzustellen, dass diese eindeutig ist.
   * Änderungen der ID können sich auf das CSS-, JS- und Datenschicht-Tracking auswirken.


