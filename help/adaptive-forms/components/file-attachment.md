---
title: Adaptive Forms-Kernkomponente - Dateianhang
description: Verwenden oder Anpassen der Kernkomponente für adaptive Forms-Dateianlagen.
role: Architect, Developer, Admin, User
source-git-commit: 945e1793ae4e959f83960db46d2de4257916fe32
workflow-type: tm+mt
source-wordcount: '1482'
ht-degree: 1%

---


# Dateianhang {#file-attachment-adaptive-forms-core-component}

Mit einer Dateianlagenkomponente in einem adaptiven Formular können Benutzer Dateien von ihrem lokalen Computer oder Gerät auswählen und hochladen. Die Dateianlagenkomponente kann so konfiguriert werden, dass bestimmte Dateitypen, Größenbeschränkungen und mehrere Anhänge zulässig sind.

**Beispiel**

![](/help/adaptive-forms/assets/upload-image.png)


## Verwendung {#reasons-to-use-file-attachment}

Es gibt mehrere Gründe, warum es sinnvoll ist, eine Dateianlagenkomponente in ein adaptives Formular einzuschließen, darunter:

* **Zusätzliche Informationen abrufen**: Mit einer Dateianlagenkomponente können Benutzer Dokumente, Bilder, Videos oder andere Dateitypen als Teil der Formularübermittlung hochladen. Dies kann für die Sammlung zusätzlicher Informationen wie Fortsetzungen, Portfolios oder unterstützender Dokumentation nützlich sein.

* **Einfache Freigabe großer Dateien**: Die Dateianlagenkomponente ermöglicht es Benutzern, große Dateien einfach zu teilen, ohne auf externe Dateifreigabe-Dienste angewiesen zu sein.

* **Praktik**: Die Dateianlagenkomponente ermöglicht es Benutzern, Dateien von ihrem lokalen Computer hochzuladen, ohne vom Formular weg zu navigieren oder andere Tools zu verwenden.

* **Datenanalyse**: Die Dateianlagenkomponente kann verwendet werden, um Daten aus verschiedenen Quellen zu sammeln und zu analysieren oder sie als Eingabe für die weitere Verarbeitung zu verwenden.

* **Anwendererlebnis**: Die Dateianlagenkomponente kann verwendet werden, um das Formular benutzerfreundlicher zu gestalten, indem eine klare und intuitive Möglichkeit für Benutzer zum Hochladen von Dateien bereitgestellt wird.

## Version und Kompatibilität {#version-and-compatibility}

Die Kernkomponente für adaptive Forms-Dateianlagen wurde im Februar 2023 als Teil der Kernkomponenten 2.0.4 veröffentlicht. Hier finden Sie eine Tabelle mit allen unterstützten Versionen, AEM Kompatibilität und Links zur entsprechenden Dokumentation:

|  |  |
|---|---|
| Komponentenversion | AEM as a Cloud Service |
| --- | --- |
| v1 | Kompatibel mit<br>[Version 2.0.4](/help/versions.md) und höher | Kompatibel | Kompatibel |

Informationen zu Kernkomponentenversionen und -versionen finden Sie im Abschnitt [Kernkomponenten-Versionen](/help/versions.md) Dokument.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technische Details {#technical-details}

Die neuesten Informationen zur Kernkomponente für adaptive Forms-Dateianlagen finden Sie in der technischen Dokumentation zu [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/fileinput/v1/fileinput). Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie im Abschnitt [Entwicklerdokumentation für Kernkomponenten](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Im Dialogfeld &quot;Konfigurieren&quot;können Sie das Erlebnis für Dateianhänge für Besucher einfach anpassen. Sie können Dateianlagenoptionen auch einfach definieren, um ein nahtloses Benutzererlebnis zu gewährleisten.

### Einfache Registerkarte {#basic-tab}

![Registerkarte &quot;Allgemein&quot;](/help/adaptive-forms/assets/fileattachement_basictab.png)

* **Name** - Sie können eine Formularkomponente sowohl im Formular als auch im Regeleditor leicht mit ihrem eindeutigen Namen identifizieren, der Name darf jedoch keine Leerzeichen oder Sonderzeichen enthalten.

* **Titel** - Mit dem Titel können Sie eine Komponente in einem Formular leicht identifizieren. Standardmäßig wird der Titel über der Komponente angezeigt. Wenn Sie keinen Titel hinzufügen, wird der Name der Komponente anstelle des Titeltexts angezeigt.

* **Titel ausblenden** - Wählen Sie die Option aus, um den Titel der Komponente auszublenden.

* **Schaltflächentitel** - Diese Option wird verwendet, um die Beschriftung der Schaltfläche festzulegen, die in einem adaptiven Formular angezeigt wird.

* **Bindungsverweis** - Ein Bindungsverweis ist ein Verweis auf ein Datenelement, das in einer externen Datenquelle gespeichert und in einem Formular verwendet wird. Mit der Bindungsreferenz können Sie Daten dynamisch an Formularfelder binden, sodass das Formular die aktuellsten Daten aus der Datenquelle anzeigen kann. Beispielsweise kann eine Bindungsverweis verwendet werden, um den Namen und die Adresse eines Kunden in einem Formular anzuzeigen, basierend auf der im Formular eingegebenen Kundenkennung. Die Bindungsverweis kann auch verwendet werden, um die Datenquelle mit den im Formular eingegebenen Daten zu aktualisieren. Auf diese Weise können Sie mit AEM Forms Formulare erstellen, die mit externen Datenquellen interagieren und so eine nahtlose Benutzererfahrung bei der Datenerfassung und -verwaltung bieten.
* **Komponente ausblenden** - Wählen Sie die Option, um die Komponente aus dem Formular auszublenden. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regeleditor. Dies ist nützlich, wenn Sie Informationen speichern müssen, die vom Benutzer nicht gesehen oder direkt geändert werden müssen.
* **Komponente deaktivieren** - Wählen Sie die Option zum Deaktivieren der Komponente aus. Die deaktivierte Komponente ist vom Endbenutzer nicht aktiv oder kann nicht bearbeitet werden. Der Benutzer kann den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regeleditor.
* **Schreibgeschützt** - Wählen Sie die Option aus, um die Komponente nicht bearbeitbar zu machen. Der Benutzer kann den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regeleditor.
* **Mehrere Anlagen zulassen** - Wählen Sie diese Option aus, um mehrere Anhänge mit dem **Dateianhang** Schaltfläche.

### Registerkarte &quot;Validierung&quot; {#validation-tab}

![Registerkarte &quot;Validierung&quot;](/help/adaptive-forms/assets/fileattachment_validationtab.png)

* **Erforderlich** - Wählen Sie diese Option, wenn Sie die Komponente in einem adaptiven Formular anzeigen möchten. Sie können die **Komponente ausblenden** oder **Komponente deaktivieren**  im **Allgemein** Registerkarte angezeigt, wenn diese Option aktiviert ist.

* **Fehlermeldung** - Mit dieser Option können Sie eine Nachricht eingeben, die angezeigt wird, wenn die **Erforderlich** aktiviert ist und das Feld leer bleibt.

* **Überprüfungsmeldung für Skripten** - Mit dieser Option können Sie eine Meldung eingeben, die angezeigt werden soll, wenn die Skriptvalidierung fehlschlägt.

* **Fehlermeldung bei minimalen Dateien** - Diese Option wird verwendet, um eine Fehlermeldung einzugeben, die angezeigt wird, wenn Sie Dateien hochladen, die weniger als die angegebene Mindestanzahl von Dateien sind.

* **Fehlermeldung &quot;Maximale Dateianzahl&quot;** - Diese Option wird verwendet, um eine Fehlermeldung einzugeben, die angezeigt wird, wenn Sie Dateien hochladen, die die angegebene maximale Dateianzahl überschreiten.

* **Maximale Dateigröße (MB)** - Mit dieser Option können Sie eine maximale Dateigröße angeben. Die Dateigrößen sind in MB angegeben.

* **Fehlermeldung zur maximalen Dateigröße** - Diese Option wird verwendet, um eine Fehlermeldung einzugeben, die angezeigt wird, wenn Sie Dateien hochladen, deren Größe die in **Maximale Dateigröße (MB)** -Option.

* **Zulässige Dateitypen** - Verschiedene Arten von Dateien, die mit dem **Dateianhang** -Schaltfläche hinzugefügt. Sie können auch ein neues Dateiformat hinzufügen, indem Sie auf **Hinzufügen** Schaltfläche. Unterstützte Dateiformate sind: Audio, Video, Bild, Text oder PDF. Sie können zulässige Dateitypen auch löschen oder neu anordnen, indem Sie Folgendes verwenden:
   * **Löschen** - Tippen oder klicken Sie, um bestimmte Dateitypen zu entfernen.
   * **Neu anordnen** - Tippen oder klicken und ziehen Sie, um die Reihenfolge der zulässigen Dateitypen neu anzuordnen.

* **Fehlermeldung bezüglich Dateityp** - Mit dieser Option können Sie eine Fehlermeldung eingeben, die angezeigt wird, wenn Sie andere als die in der **Zulässige Dateitypen** -Option.

### Registerkarte &quot;Hilfe-Inhalt&quot; {#help-content-tab}

![Registerkarte &quot;Hilfe-Inhalt&quot;](/help/adaptive-forms/assets/fileattachement_helpcontenttab.png)

* **Kurzbeschreibung** - Eine kurze Beschreibung ist eine kurze Texterklärung, die zusätzliche Informationen oder Klarstellungen zum Zweck eines bestimmten Formularfelds bietet. Es hilft dem Benutzer zu verstehen, welcher Datentyp in das Feld eingegeben werden soll, und kann Richtlinien oder Beispiele bereitstellen, um sicherzustellen, dass die eingegebenen Informationen gültig sind und die gewünschten Kriterien erfüllen. Standardmäßig bleiben kurze Beschreibungen ausgeblendet. Aktivieren Sie die **Kurzbeschreibung immer anzeigen** -Option, um sie unter der Komponente anzuzeigen.

* **Kurzbeschreibung immer anzeigen** - Aktivieren Sie die Option, um die Kurzbeschreibung unter der Komponente anzuzeigen.

* **Hilfetext** - Hilfetext bezieht sich auf zusätzliche Informationen oder Anleitungen, die dem Benutzer bereitgestellt werden, um ihn beim korrekten Ausfüllen eines Formularfelds zu unterstützen. Er wird angezeigt, wenn der Benutzer auf das Hilfesymbol (i) neben der Komponente klickt. Hilfetext enthält detailliertere Informationen als die Beschriftung oder der Platzhaltertext eines Formularfelds und soll dem Benutzer dabei helfen, die Anforderungen oder Einschränkungen des Felds zu verstehen. Es kann auch Vorschläge oder Beispiele anbieten, um das Ausfüllen des Formulars zu vereinfachen und genauer zu gestalten.

![Registerkarte &quot;Barrierefreiheit&quot;](/help/adaptive-forms/assets/fileattachement_accessibilitytab.png)

* **Text für Bildschirmlesehilfen** - Text für Bildschirmlesehilfen bezieht sich auf zusätzlichen Text, der speziell für Hilfstechnologien wie Bildschirmlesehilfen vorgesehen ist, die von sehbehinderten Personen verwendet werden. Dieser Text enthält eine Audiobeschreibung des Zwecks des Formularfelds und kann Informationen über den Titel, die Beschreibung, den Namen und alle relevanten Nachrichten (benutzerdefinierten Text) des Felds enthalten. Der Text der Bildschirmlesehilfe hilft sicherzustellen, dass das Formular für alle Benutzer zugänglich ist, auch für Benutzer mit Sehbehinderungen, und bietet ihnen ein umfassendes Verständnis des Formularfelds und seiner Anforderungen.


## Dialogfeld „Design“ {#design-dialog}

Das Dialogfeld &quot;Design&quot;wird verwendet, um CSS-Stile für die Komponente &quot;Dateianlage&quot;zu definieren und zu verwalten.

### Registerkarte „Arten“ {#styles-tab}

Die Kernkomponente für adaptive Forms-Dateianlagen unterstützt die AEM [Stilsystem](/help/get-started/authoring.md#component-styling).

**Standard-CSS-Klassen**: Sie können eine standardmäßige CSS-Klasse für die Kernkomponente für adaptive Forms-Dateianlagen bereitstellen.

**Zulässige Stile**: Sie können Stile definieren, indem Sie einen Namen und die CSS-Klasse angeben, die den Stil darstellt. Sie können beispielsweise einen Stil mit dem Namen &quot;fett Text&quot;erstellen und die CSS-Klasse &quot;font-weight: fett&quot;. Sie können diese Stile im adaptiven Forms-Editor verwenden oder auf ein adaptives Formular anwenden. Um einen Stil anzuwenden, wählen Sie im adaptiven Forms-Editor die Komponente aus, auf die Sie den Stil anwenden möchten, navigieren Sie zum Dialogfeld &quot;Eigenschaften&quot;und wählen Sie den gewünschten Stil aus dem **Stile** Dropdown-Liste. Wenn Sie die Stile aktualisieren oder ändern müssen, kehren Sie einfach zum Dialogfeld &quot;Design&quot;zurück, aktualisieren Sie die Stile auf der Registerkarte &quot;Stile&quot;und speichern Sie die Änderungen.
