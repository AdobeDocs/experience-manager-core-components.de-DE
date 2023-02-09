---
title: Adaptive Forms-Kernkomponente - Assistent
description: Verwenden oder Anpassen der Kernkomponente des Adaptiven Forms-Assistenten
role: Architect, Developer, Admin, User
source-git-commit: 945e1793ae4e959f83960db46d2de4257916fe32
workflow-type: tm+mt
source-wordcount: '1681'
ht-degree: 1%

---


# Assistent {#wizard-adaptive-forms-core-component}

Ein Assistentenlayout in einem adaptiven Formular bezieht sich auf ein Formular, das in mehrere Schritte oder Seiten unterteilt ist, wobei der Benutzer das Formular Schritt für Schritt durchläuft. Dieses Layout wird als &quot;Assistent&quot;bezeichnet, da es den Benutzer schrittweise durch das Formular führt.

Jeder Schritt des Assistenten enthält in der Regel eine Gruppe verwandter Formularfelder und einen Navigationsmechanismus, z. B. &quot;Weiter&quot;- und &quot;Zurück&quot;-Schaltflächen, um zwischen Schritten zu wechseln. Der Benutzer kann erst mit dem nächsten Schritt fortfahren, nachdem der aktuelle Schritt abgeschlossen und alle erforderlichen Felder ausgefüllt wurden.

Das Layout des Assistenten ist für Formulare nützlich, die viele Felder oder Informationen enthalten, die erfasst werden müssen, da es das Formular in kleinere, besser verwaltbare Abschnitte unterteilt. Außerdem können Benutzer sich auf einen Satz von Feldern konzentrieren, wodurch der Formularausfüllungsprozess weniger überwältigend werden kann.

Es kann jedoch auch die Komplexität des Formulars erhöhen, da der Benutzer mehrere Seiten durchlaufen muss, um das Formular auszufüllen. Daher müssen die Formularanforderungen und die Benutzeranforderungen ausgewertet werden, bevor die Verwendung eines Assistentenlayouts beschlossen wird.

Sie können die Kernkomponente des Assistenten-Layouts in einem adaptiven Formular verwenden, um das Layout des Assistenten zu erstellen.


**Beispiel**

![](/help/adaptive-forms/assets/wizard.png)

## Verwendung {#reasons-to-use-wizard-in-an-adaptive-form}

Es gibt mehrere Gründe, warum die Verwendung eines Assistenten-Layouts in einem adaptiven Formular von Vorteil sein kann:

* **Einfachheit**: Das Aufschlüsseln eines Formulars in mehrere Schritte kann es für Benutzer einfacher machen, ein Formular zu verstehen und auszufüllen, da sie sich auf einen Satz von Feldern gleichzeitig konzentrieren können.

* **Einrichtung**: Mit einem Assistentenlayout können Sie Formulare nach Thema oder Zweck organisieren. Außerdem können zugehörige Felder gruppiert werden, was den Formularausfüllprozess logischer und effizienter machen kann.

* **Validierung**: Ein Assistentenlayout ermöglicht eine schrittweise Überprüfung, mit der Benutzer Fehler beim Ausfüllen erkennen und korrigieren können, anstatt auf das Ende des Formulars zu warten.

* **Fortschrittsanzeige**: Ein Assistentenlayout kann den Fortschritt des Formulars anzeigen, was dem Benutzer dabei hilft, zu verstehen, wie viel des Formulars noch ausgefüllt werden muss.

* **Lange Formen**: Wenn das Formular viele Felder enthält, kann es für den Benutzer überwältigend sein, sie alle gleichzeitig zu sehen, sodass es weniger einschüchternd sein kann, sie in kleinere, besser verwaltbare Abschnitte aufzuschlüsseln.

* **Vermeiden von Abbruch**: Ein Assistentenlayout kann auch dazu beitragen, den Formularabbruch zu reduzieren, da Benutzer mit höherer Wahrscheinlichkeit ein Formular ausfüllen, wenn sie den Fortschritt sehen und verstehen können, wie viel noch zu erledigen ist.

* **Mobiles Erlebnis**: Ein Assistentenlayout kann auch für Formulare von Vorteil sein, auf die auf Mobilgeräten zugegriffen wird, da es kleinere Seiten ermöglicht, die schneller geladen werden und leichter zu navigieren sind.

Insgesamt kann das Ausfüllen des Formulars durch ein Assistentenlayout für die Benutzer leichter zu handhaben und effizienter zu gestalten sein. Es ist jedoch wichtig, die Komplexität des Formulars und die Anforderungen des Benutzers zu berücksichtigen, bevor er sich für die Verwendung dieses Layouts entscheidet.

## Version und Kompatibilität {#version-and-compatibility}

Die Kernkomponente des Adaptiven Forms-Assistenten für Layout wurde im Februar 2023 als Teil der Kernkomponenten 2.0.4 veröffentlicht. Hier finden Sie eine Tabelle mit allen unterstützten Versionen, AEM Kompatibilität und Links zur entsprechenden Dokumentation:

|  |  |
|---|---|
| Komponentenversion | AEM as a Cloud Service |
| --- | --- |
| v1 | Kompatibel mit<br>[Version 2.0.4](/help/versions.md) und höher | Kompatibel | Kompatibel |

Informationen zu Kernkomponentenversionen und -versionen finden Sie im Abschnitt [Kernkomponenten-Versionen](/help/versions.md) Dokument.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technische Details {#technical-details}

Laden Sie die neuesten Informationen zur Kernkomponente &quot;Adaptive Forms Title&quot;in der technischen Dokumentation zu [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/wizard/v1/wizard). Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie im Abschnitt [Entwicklerdokumentation für Kernkomponenten](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Im Dialogfeld &quot;Konfigurieren&quot;können Sie Ihre Assistentenerfahrung für Besucher einfach anpassen. Sie können außerdem problemlos Assistentenoptionen für ein nahtloses Benutzererlebnis definieren.

### Einfache Registerkarte {#basic-tab}

![Registerkarte &quot;Allgemein&quot;](/help/adaptive-forms/assets/wizard_basictab.png)

* **Name** - Sie können eine Formularkomponente sowohl im Formular als auch im Regeleditor leicht mit ihrem eindeutigen Namen identifizieren, der Name darf jedoch keine Leerzeichen oder Sonderzeichen enthalten.

* **Titel** - Mit dem Titel können Sie eine Komponente in einem Formular leicht identifizieren. Standardmäßig wird der Titel über der Komponente angezeigt.

* **Titel ausblenden** - Wählen Sie die Option aus, um den Titel der Komponente auszublenden.

* **Daten in ein Objekt einschließen** - Wählen Sie &quot;Daten in ein Objekt einschließen&quot;aus, um die Felddaten aus dem Assistenten in ein JSON-Objekt einzufügen. Wenn diese Option nicht ausgewählt ist, hat die JSON-Datei für die Übermittlungsdaten eine flache Struktur für die Felder des Assistenten.

* **Layout** - Sie können für Ihren Assistenten entweder ein festes Layout (einfach) oder ein flexibles Layout (responsives Raster) verwenden. Das einfache Layout behält alles fest an der Stelle, während das responsive Raster es Ihnen ermöglicht, die Position der Komponenten an Ihre Bedürfnisse anzupassen. Verwenden Sie beispielsweise das responsive Raster, um &quot;Vorname&quot;, &quot;Vorname&quot;und &quot;Nachname&quot;in einem Formular in einer einzigen Zeile auszurichten.

* **Bindungsverweis** - Ein Bindungsverweis ist ein Verweis auf ein Datenelement, das in einer externen Datenquelle gespeichert und in einem Formular verwendet wird. Mit der Bindungsreferenz können Sie Daten dynamisch an Formularfelder binden, sodass das Formular die aktuellsten Daten aus der Datenquelle anzeigen kann. Beispielsweise kann eine Bindungsverweis verwendet werden, um den Namen und die Adresse eines Kunden in einem Formular anzuzeigen, basierend auf der im Formular eingegebenen Kundenkennung. Die Bindungsverweis kann auch verwendet werden, um die Datenquelle mit den im Formular eingegebenen Daten zu aktualisieren. Auf diese Weise können Sie mit AEM Forms Formulare erstellen, die mit externen Datenquellen interagieren und so eine nahtlose Benutzererfahrung bei der Datenerfassung und -verwaltung bieten.

* **Komponente ausblenden** - Wählen Sie die Option, um die Komponente aus dem Formular auszublenden. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regeleditor. Dies ist nützlich, wenn Sie Informationen speichern müssen, die vom Benutzer nicht gesehen oder direkt geändert werden müssen.

* **Komponente deaktivieren** - Wählen Sie die Option zum Deaktivieren der Komponente aus. Die deaktivierte Komponente ist vom Endbenutzer nicht aktiv oder kann nicht bearbeitet werden. Der Benutzer kann den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regeleditor.

### Registerkarte &quot;Hilfe&quot; {#help-tab}

![Hilfe-Tab](/help/adaptive-forms/assets/wizard_helptab.png)

* **Kurzbeschreibung** - Eine kurze Beschreibung ist eine kurze Texterklärung, die zusätzliche Informationen oder Klarstellungen zum Zweck eines bestimmten Formularfelds bietet. Es hilft dem Benutzer zu verstehen, welcher Datentyp in das Feld eingegeben werden soll, und kann Richtlinien oder Beispiele bereitstellen, um sicherzustellen, dass die eingegebenen Informationen gültig sind und die gewünschten Kriterien erfüllen. Standardmäßig bleiben kurze Beschreibungen ausgeblendet. Aktivieren Sie die **Kurzbeschreibung immer anzeigen** -Option, um sie unter der Komponente anzuzeigen.

* **Kurzbeschreibung immer anzeigen** - Aktivieren Sie die Option, um die Kurzbeschreibung unter der Komponente anzuzeigen.

* **Hilfetext** - Hilfetext bezieht sich auf zusätzliche Informationen oder Anleitungen, die dem Benutzer bereitgestellt werden, um ihn beim korrekten Ausfüllen eines Formularfelds zu unterstützen. Er wird angezeigt, wenn der Benutzer auf das Hilfesymbol (i) neben der Komponente klickt. Hilfetext enthält detailliertere Informationen als die Beschriftung oder der Platzhaltertext eines Formularfelds und soll dem Benutzer dabei helfen, die Anforderungen oder Einschränkungen des Felds zu verstehen. Es kann auch Vorschläge oder Beispiele anbieten, um das Ausfüllen des Formulars zu vereinfachen und genauer zu gestalten.


### Registerkarte „Erreichbarkeit“ {#accessibility}

![Registerkarte &quot;Allgemein&quot;](/help/adaptive-forms/assets/wizard_accessibiltytab.png)

* **Text für Bildschirmlesehilfen** - Text für Bildschirmlesehilfen bezieht sich auf zusätzlichen Text, der speziell für Hilfstechnologien wie Bildschirmlesehilfen vorgesehen ist, die von sehbehinderten Personen verwendet werden. Dieser Text enthält eine Audiobeschreibung des Zwecks des Formularfelds und kann Informationen über den Titel, die Beschreibung, den Namen und alle relevanten Nachrichten (benutzerdefinierten Text) des Felds enthalten. Der Text der Bildschirmlesehilfe hilft sicherzustellen, dass das Formular für alle Benutzer zugänglich ist, auch für Benutzer mit Sehbehinderungen, und bietet ihnen ein umfassendes Verständnis des Formularfelds und seiner Anforderungen.

* **HTML-Rolle für die Ankündigung durch die Bildschirmlesehilfe** - Die HTML-Rolle ist ein Attribut, mit dem der Zweck eines HTML-Elements für Hilfstechnologien wie Bildschirmlesehilfen angegeben wird. Das Rollenattribut wird verwendet, um einem Element zusätzlichen Kontext und eine semantische Bedeutung zu verleihen, wodurch Bildschirmlesehilfen die Interpretation und Ankündigung des Inhalts für den Benutzer erleichtern. In AEM Forms kann beispielsweise die Beschriftung eines Formularfelds die Rolle &quot;label&quot;haben und sein Eingabefeld die Rolle &quot;textbox&quot;. Dies hilft der Bildschirmlesehilfe, die Beziehung zwischen Titel und Eingabefeld zu verstehen und sie dem Benutzer korrekt anzukündigen.


## Dialogfeld „Design“ {#design-dialog}

Im Dialogfeld &quot;Design&quot;können Vorlagenautoren steuern, wie Elemente standardmäßig angezeigt werden. Für die Komponente &quot;Adaptiver Forms-Assistent&quot;können Sie Folgendes festlegen:

* Die Kernkomponenten, die ein Formularersteller dem Assistenten im Editor für adaptive Forms hinzufügen kann
* Einfache Namen für Stile (CSS-Klassen), die im Dialogfeld &quot;Eigenschaften&quot;der Assistentenkomponente im adaptiven Forms-Editor angewendet werden können.

Dadurch wird das Erstellen und Anpassen von Formularen einfacher und effizienter.

### Registerkarte „Zugelassene Komponenten“ {#allowed-components-tab}

Die **Zugelassene Komponenten** -Tab ermöglicht es dem Vorlageneditor, die Komponenten festzulegen, die als Elemente zu den Bedienfeldern in der Assistentenkomponente im adaptiven Forms-Editor hinzugefügt werden können.

### Registerkarte „Arten“ {#styles-tab}

Das Dialogfeld &quot;Design&quot;wird zum Definieren und Verwalten von CSS-Stilen für eine Komponente verwendet. Die Kernkomponente des Adaptiven Forms-Assistenten unterstützt die AEM [Stilsystem](/help/get-started/authoring.md#component-styling).

**Standard-CSS-Klassen**: Sie können eine standardmäßige CSS-Klasse für die Assistentenkomponente bereitstellen.

**Zulässige Stile**: Sie können Stile definieren, indem Sie einen Namen und die CSS-Klasse angeben, die den Stil darstellt. Sie können beispielsweise einen Stil mit dem Namen &quot;fett Text&quot;erstellen und die CSS-Klasse &quot;font-weight: fett&quot;. Sie können diese Stile im adaptiven Forms-Editor verwenden oder auf ein adaptives Formular anwenden. Um einen Stil anzuwenden, wählen Sie im adaptiven Forms-Editor die Komponente aus, auf die Sie den Stil anwenden möchten, navigieren Sie zum Dialogfeld &quot;Eigenschaften&quot;und wählen Sie den gewünschten Stil aus dem **Stile** Dropdown-Liste. Wenn Sie die Stile aktualisieren oder ändern müssen, kehren Sie einfach zum Dialogfeld &quot;Design&quot;zurück, aktualisieren Sie die Stile auf der Registerkarte &quot;Stile&quot;und speichern Sie die Änderungen.

