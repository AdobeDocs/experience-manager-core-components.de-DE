---
title: Adaptives Formularfragment
description: Verwenden Sie Formularfragmente, um Formularsegmente oder Feldgruppen zu erstellen und sie in der gesamten adaptiven Forms wiederzuverwenden, um die Effizienz und Wiederverwendbarkeit zu verbessern.
role: Architect, Developer, Admin, User
source-git-commit: 6f83e843b95689bad2cfb31bd53c20b135d789d5
workflow-type: tm+mt
source-wordcount: '1675'
ht-degree: 67%

---


# Formularfragment-Komponente {#form-fragment-component-adaptive-forms-core-component}

Adaptive Forms bietet eine praktische Möglichkeit, Formularsegmente wie Bedienfelder oder Feldgruppen zu erstellen, damit sie in verschiedenen adaptiven Forms wiederverwendet werden können. Diese wiederverwendbaren und eigenständigen Segmente werden als [Adaptive Formularfragmente](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/adaptive-form-fragments-core-components.html).

Sie können [Fragment mehrmals zu einem Dokument hinzufügen](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/adaptive-form-fragments-core-components.html#insert-a-fragment-in-an-adaptive-form) und verwenden Datenbindungseigenschaften seiner Komponenten, um sie mit verschiedenen Datenquellen oder Schemata zu verknüpfen. Beispielsweise können Sie dasselbe Adressfragment für permanente, Kommunikations- und Abrechnungsadressen verwenden und es mit verschiedenen Feldern einer Datenquellen oder eines Schemas verbinden.

![Beispiel](/help/adaptive-forms/assets/using-multiple-fragment-af.gif)


Sie können auch die [Wiederholungsoption](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/create-forms-repeatable-sections.html?lang=de) zum Duplizieren der Formularfragmentkomponente und der zugehörigen untergeordneten Komponenten eine minimale und maximale Wiederholungsanzahl definieren und die Replikation ähnlicher Abschnitte innerhalb eines Formulars erleichtern.

>[!NOTE]
>
> Sie können [Erstellen eines adaptiven Formularfragments](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/adaptive-form-fragments-core-components.html#create-a-fragment) ein Bedienfeld in einem vorhandenen adaptiven Formular als Fragment zu speichern.

## Verwendung {#usage}

- **Wiederverwendbarkeit**: Die Möglichkeit, Formularfragmente in mehreren adaptiven Forms wiederzuverwenden, ist der Hauptvorteil der Verwendung von Formularfragmenten. Dies hilft bei der Aufrechterhaltung von Konsistenz in Design und Funktionalität, da an einem Fragment vorgenommene Änderungen in allen Instanzen übernommen werden, in denen es verwendet wird.

- **Konsistentes Benutzererlebnis**: Die Verwendung von Formularfragmenten für allgemeine Elemente, z. B. Kopf- oder Fußzeilen, stellt eine konsistente und einheitliche Benutzererfahrung sicher.

- **Einfache Wartung**: Die Änderungen oder Änderungen an einem Formularfragment werden in allen Instanzen übernommen, in denen es verwendet wird. Sie vereinfacht die Wartung und verringert die Fehlerwahrscheinlichkeit.

- **Effizienz**: Designer und Entwickler sparen Zeit, indem sie Formularfragmente nur einmal erstellen und testen. Die Formularfragmente können dann problemlos in mehrere adaptive Forms integriert werden, ohne dass redundante Arbeit erforderlich ist.

## Version und Kompatibilität {#version-and-compatibility}

Die Kernkomponente für adaptive Forms-Fragmente wurde als Teil der Kernkomponenten 2.0.50 für Cloud Service und Kernkomponenten 1.1.26 für AEM 6.5.16.0 Forms oder höher veröffentlicht. Hier finden Sie eine Tabelle mit allen unterstützten Versionen, AEM-Kompatibilität und Links zur entsprechenden Dokumentation:

| Komponentenversion | AEM as a Cloud Service | AEM 6.5.16.0 Forms oder höher |
|---|---|---|
| v1 | Kompatibel mit<br>[Version 2.0.50](/help/adaptive-forms/version.md) und höher | Kompatibel mit<br>[Version 1.1.26](/help/adaptive-forms/version.md) und höher, jedoch weniger als 2.0.0. |

Informationen zu Versionen und Freigaben der Kernkomponente finden Sie im Dokument [Kernkomponenten-Versionen](/help/adaptive-forms/version.md).

## Technische Details {#technical-details}

Die neuesten Informationen zur Kernkomponente &quot;Adaptive Forms Fragment&quot;finden Sie in der technischen Dokumentation zu [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/fragment). Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Entwicklerdokumentation für Kernkomponenten](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Im Dialogfeld &quot;Konfigurieren&quot;können Sie das Fragmenterlebnis für Besucher einfach anpassen. Sie können Fragmenteigenschaften auch einfach definieren, um ein nahtloses Benutzererlebnis zu gewährleisten.

### Registerkarte „Allgemein“ {#basic-tab}

![Registerkarte „Allgemein“](/help/adaptive-forms/assets/fragment-basictab.png)

- **Name**: Sie können eine Formularkomponente sowohl im Formular als auch im Regel-Editor leicht mit ihrem eindeutigen Namen identifizieren. Der Name darf jedoch keine Leerzeichen oder Sonderzeichen enthalten.

- **Titel**: Sie können mit dem Titel leicht eine Komponente in einem Formular identifizieren. Standardmäßig wird der Titel über der Komponente angezeigt. Wenn Sie keinen Titel hinzufügen, wird der Name der Komponente anstelle des Titeltexts angezeigt.

- **Titel ausblenden** - Wählen Sie die Option aus, um den Titel der Komponente auszublenden.

- **Daten untergeordneter Komponenten bei Formularübermittlung gruppieren (Daten in Objekt einschließen)** – Wenn die Option ausgewählt ist, werden die Daten aus den untergeordneten Komponenten innerhalb des JSON-Objekts der übergeordneten Komponente verschachtelt. Wenn jedoch die Option nicht ausgewählt ist, weisen die gesendeten JSON-Daten eine flache Struktur auf, ohne dass ein Objekt für die übergeordnete Komponente vorhanden ist. Zum Beispiel:

   - Wenn die Option ausgewählt ist, werden die Daten aus den untergeordneten Komponenten (z. B. Straße, Stadt und Postleitzahl) innerhalb der übergeordneten Komponente (Adresse) als JSON-Objekt verschachtelt. Dadurch wird eine hierarchische Struktur erstellt, und die Daten werden unter der übergeordneten Komponente angeordnet.

     Struktur der übermittelten Daten:

     ```JSON
     { "Address":
     
     { "Street": "123 Main Street", "City": "New York", "Zip Code": "12345" }
     
     }
     ```

   - Wenn die Option nicht ausgewählt ist, weisen die gesendeten JSON-Daten eine flache Struktur auf, ohne dass ein Objekt für die übergeordnete Komponente (Adresse) vorhanden ist. Alle Daten befinden sich auf derselben Ebene ohne hierarchische Organisation.


     Struktur der übermittelten Daten:

     ```JSON
        { "Street": "123 Main Street", "City": "New York", "Zip Code": "12345" }
     ```

- **Fragmentverweis** - Ein Fragmentverweis ist ein Verweis auf ein Formularfragment, das in einer externen Datenquelle gespeichert und in einem Formular verwendet wird. Mit der Fragmentreferenz können Sie das Formularfragment dynamisch an ein Formular binden.

- **Verbindungsreferenz**: Eine Verbindungsreferenz ist ein Verweis auf ein Datenelement, das in einer externen Datenquelle gespeichert ist und in einem Formular verwendet wird. Sie können mit dem Bindungsverweis Daten dynamisch an Formularfelder binden, sodass das Formular die aktuellsten Daten aus der Datenquelle anzeigen kann. Beispielsweise kann ein Bindungsverweis verwendet werden, um den Namen und die Adresse von Kundinnen und Kunden in einem Formular anzuzeigen, basierend auf der im Formular eingegebenen Kunden-ID. Der Bindungsverweis kann auch verwendet werden, um die Datenquelle mit den im Formular eingegebenen Daten zu aktualisieren. Auf diese Weise können Sie mit AEM Forms Formulare erstellen, die mit externen Datenquellen interagieren und so ein nahtloses Benutzererlebnis bei der Datenerfassung und -verwaltung bieten.

- **Komponente ausblenden**: Wählen Sie diese Option, um die Komponente aus dem Formular auszublenden. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor. Dies ist nützlich, wenn Sie Informationen speichern müssen, die Benutzende nicht sehen oder direkt ändern müssen.
- **Komponente deaktivieren**: Wählen Sie die Option zum Deaktivieren der Komponente aus. Die deaktivierte Komponente ist nicht aktiv und Endbenutzende können sie nicht bearbeiten. Benutzende können den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor.
- **Schreibgeschützt**: Wählen Sie die Option aus, um die Komponente nicht bearbeitbar zu machen. Benutzende können den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor.

### Registerkarte &quot;Fragment wiederholen&quot; {#repeat-tab}

![Registerkarte &quot;Fragment wiederholen&quot;](/help/adaptive-forms/assets/fragment-repeattab.png)

- **Fragment wiederholbar machen**: Eine Umschalter-Funktion, mit der Benutzer die Wiederholungsfunktion aktivieren oder deaktivieren können.
- **Mindestwiederholungen**: Legt fest, wie oft die Fragmentkomponente mindestens wiederholt werden kann. Der Wert null zeigt an, dass die Fragmentkomponente nicht wiederholt wird. Der Standardwert ist null.
- **Maximale Wiederholungen**: Legt fest, wie oft die Fragmentkomponente maximal wiederholt werden kann. Standardmäßig ist dieser Wert unbegrenzt.

### Registerkarte „Hilfe-Inhalt“ {#help-content}

![Registerkarte „Hilfe-Inhalt“](/help/adaptive-forms/assets/fragment-helptab.png)

- **Kurzbeschreibung**: Eine Kurzbeschreibung ist eine kurze Erklärung, die zusätzliche Informationen oder Klarstellungen über den Zweck eines Formularfelds bietet. Es hilft Benutzenden zu verstehen, welcher Datentyp in das Feld eingegeben werden soll, und kann Richtlinien oder Beispiele bereitstellen, um sicherzustellen, dass die eingegebenen Informationen gültig sind und die gewünschten Kriterien erfüllen. Standardmäßig bleiben kurze Beschreibungen ausgeblendet. Aktivieren Sie die Option **Kurzbeschreibung immer anzeigen**, um sie unterhalb der Komponente anzuzeigen.

- **Kurzbeschreibung immer anzeigen**: Aktivieren Sie diese Option, um die Kurzbeschreibung unterhalb der Komponente anzuzeigen.

- **Hilfetext**: Hilfetext bezieht sich auf zusätzliche Informationen oder Anleitungen, die den Benutzenden bereitgestellt werden, um sie beim korrekten Ausfüllen eines Formularfelds zu unterstützen. Er erscheint, wenn Benutzende auf das Hilfesymbol (i) neben der Komponente klicken. Hilfetext enthält detailliertere Informationen als die Beschriftung oder der Platzhaltertext eines Formularfelds und soll den Benutzenden dabei helfen, die Anforderungen oder Einschränkungen des Felds zu verstehen. Er kann auch Vorschläge oder Beispiele anbieten, um das Ausfüllen des Formulars einfacher und genauer zu gestalten.

### Barrierefreiheit {#accessibility}

![Registerkarte „Barrierefreiheit“](/help/adaptive-forms/assets/fragment-accessibilitytab.png)

- **Text für Bildschirmlesehilfen** – Das ist zusätzlicher Text, der von Hilfstechnologien wie etwa Bildschirmlesehilfen für sehbehinderte Personen vorgelesen wird. Dieser Text enthält eine Audiobeschreibung des Zwecks des Formularfelds und kann Informationen über den Titel, die Beschreibung, den Namen und alle relevanten Nachrichten (benutzerdefinierten Text) des Felds enthalten. Der Text der Bildschirmlesehilfe hilft sicherzustellen, dass das Formular allen Benutzenden zugänglich ist, auch Personen mit Sehschwäche, und bietet ihnen ein umfassendes Verständnis des Formularfelds und seiner Anforderungen.

## Dialogfeld „Design“ {#design-dialog}

Das Dialogfeld &quot;Design&quot;wird verwendet, um CSS-Stile für die Formularfragment-Komponente zu definieren und zu verwalten.

### Registerkarte „Stile“ {#styles-tab}

Die Kernkomponente für adaptive Formularfragmente unterstützt die AEM [Stilsystem](/help/get-started/authoring.md#component-styling).

![Dialogfeld „Design“](/help/adaptive-forms/assets/checkbox-style.png)

- **Standard-CSS-Klassen**: Sie können eine standardmäßige CSS-Klasse für die Kernkomponente &quot;Adaptives Formularfragment&quot;bereitstellen.

- **Zulässige Stile**: Sie können Stile definieren, indem Sie den Namen und die CSS-Klasse für den Stil angeben. Sie können beispielsweise einen Stil mit dem Namen „Fettschrift“ erstellen und die CSS-Klasse „Schriftbreite: Fett“ bereitstellen. Sie können diese Stile bei einem adaptiven Formular im adaptiven Formular-Editor anwenden. Um einen Stil anzuwenden, wählen Sie im Editor für adaptive Formulare die Komponente aus, auf die Sie den Stil anwenden möchten, navigieren Sie zum Eigenschaften-Dialog und wählen Sie den gewünschten Stil aus der Dropdown-Liste **Stile**. Wenn Sie die Stile aktualisieren oder ändern müssen, kehren Sie einfach zum Dialogfeld „Design“ zurück, aktualisieren die Stile auf der Registerkarte „Stile“ und speichern die Änderungen.

### Benutzerdefinierte Eigenschaften

![Dialogfeld „Benutzerdefinierte Eigenschaften“](/help/adaptive-forms/assets/checkbox-customproperties.png)

Mit benutzerdefinierten Eigenschaften können Sie benutzerdefinierte Attribute (Schlüssel-Wert-Paare) mithilfe der Formularvorlage mit einer Kernkomponente des adaptiven Formulars verknüpfen. Die benutzerdefinierten Eigenschaften werden im Eigenschaftenbereich der Headless-Ausgabedarstellung der Komponente angezeigt. So kann ein dynamisches Formularverhalten erzeugt werden, das sich je nach den benutzerdefinierten Attributwerten anpasst. Beispielsweise können Entwickelnde verschiedene Ausgabedarstellungen einer Headless-Formularkomponente für Mobile-, Desktop- oder Web-Plattformen entwerfen und so das Benutzererlebnis auf einer Vielzahl von Geräten erheblich verbessern.

- **Gruppenname**: Sie können einen Namen angeben, um die Gruppe der benutzerdefinierten Eigenschaften zu kennzeichnen. Sie können mehrere Gruppen benutzerdefinierter Eigenschaften hinzufügen, löschen oder neu anordnen. Nach dem Hinzufügen der Gruppe benutzerdefinierter Eigenschaften werden folgende Optionen angezeigt:

   - **Schlüssel-Wert-Paare**: Sie können mehrere Namen und Werte benutzerdefinierter Eigenschaften hinzufügen, indem Sie für jede Gruppe benutzerdefinierter Eigenschaften auf **Hinzufügen** klicken.

   - **Löschen**: Tippen oder klicken Sie auf diese Option, um den Namen und den Wert der benutzerdefinierten Eigenschaft zu löschen.

   - **Neu anordnen**: Tippen oder klicken und ziehen Sie, um den benutzerdefinierten Eigenschaftsnamen und den benutzerdefinierten Eigenschaftswert neu anzuordnen.

## Ähnliche Artikel {#related-articles}

{{more-like-this}}

## Siehe auch {#see-also}

{{see-also}}





