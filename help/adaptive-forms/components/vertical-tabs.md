---
title: Adaptive Forms-Kernkomponente - Vertikale Registerkarten
description: Verwenden oder Anpassen der Kernkomponente Adaptive Forms Vertikale Registerkarten .
role: Architect, Developer, Admin, User
exl-id: d5cd1c18-6840-4f2f-a767-a69b803e6075
source-git-commit: 4ca65f93e223fdd0b0a701ef335ed5be1fbab7fe
workflow-type: tm+mt
source-wordcount: '1904'
ht-degree: 65%

---

# Vertikale Registerkarten-Komponente{#vertical-tabs-adaptive-forms-core-component}

Vertikale Registerkarten in einem adaptiven Formular beziehen sich auf ein Entwurfsmuster, bei dem mehrere Abschnitte eines Formulars gruppiert und als separate, vertikal ausgerichtete Registerkarten angezeigt werden. Benutzende können zwischen den Registerkarten wechseln, um auf verschiedene Abschnitte des Formulars zuzugreifen. Jede Registerkarte dient als Auslöser zum Anzeigen und Ausblenden des jeweiligen Formularinhalts. Die vertikalen Registerkarten helfen, lange Formulare in überschaubare Abschnitte zu organisieren und das Benutzererlebnis zu verbessern. Registerkarten können ein Formular für Benutzende mit Behinderungen barrierefreier gestalten, da sie mithilfe der Tastaturnavigation zwischen Abschnitten wechseln können.

Wenn Benutzende auf eine Registerkarte klicken, wird der Formularinhalt dynamisch aktualisiert und der entsprechende Abschnitt wird angezeigt.

![Beispiel](/help/adaptive-forms/assets/horizontal-example.png)

## Verwendung {#reasons-to-use-vertical-tabs}

Die häufigsten Gründe für die Verwendung von vertikalen Registerkarten in einem adaptiven Formular sind:

- **Verbesserte Benutzerfreundlichkeit**: Vertikale Registerkarten erleichtern Benutzern die Navigation durch das Formular, insbesondere wenn das Formular mehrere Abschnitte oder eine große Anzahl von Feldern enthält.

- **Raummanagement**: Vertikale Registerkarten sparen Platz auf dem Bildschirm, indem sie verwandte Formularabschnitte in Registerkarten gruppieren und jeweils nur einen Abschnitt anzeigen.

- **Bessere Organisation**: Registerkarten bieten eine klare und übersichtliche Struktur für ein Formular, sodass Benutzende das Formular besser verstehen und ausfüllen können.

- **Erhöhte Benutzerinteraktion**: Vertikale Tabulatoren können ein Formular für Benutzer visueller ansprechender und ansprechender machen, wodurch die Rate der Formularabschlüsse verbessert werden kann.

## Version und Kompatibilität {#version-and-compatibility}

Die Kernkomponente &quot;Vertikale Registerkarten der adaptiven Forms&quot;wurde als Teil der Kernkomponenten 2.0.18 veröffentlicht. In der folgenden Tabelle finden Sie alle unterstützten Versionen, AEM Kompatibilität und Links zur entsprechenden Dokumentation:

|  |  |
|---|---|
| Komponentenversion | AEM as a Cloud Service |
| --- | --- |
| v1 | Kompatibel mit<br>[Version 2.0.18](/help/versions.md) und höher | Kompatibel | Kompatibel |

Informationen zu Versionen und Freigaben der Kernkomponente finden Sie im Dokument [Kernkomponenten-Versionen](/help/versions.md).

## Technische Details {#technical-details}

Die neuesten Informationen zur Kernkomponente &quot;Vertikale Registerkarten des adaptiven Forms&quot;finden Sie in der technischen Dokumentation unter [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/verticaltabs/v1/verticaltabs). Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Entwicklerdokumentation für Kernkomponenten](/help/developing/overview.md).


## Dialogfeld „Konfigurieren“ {#configure-dialog}

Im Dialogfeld Konfigurieren können Sie das Erlebnis für vertikale Registerkarten einfach für Besucher anpassen. Für ein nahtloses Benutzererlebnis können Sie auch Optionen für vertikale Registerkarten definieren.

### Registerkarte „Allgemein“ {#basic-tab}

![Registerkarte „Allgemein“](/help/adaptive-forms/assets/vertical-tab-basic.png)

- **Name**: Sie können eine Formularkomponente sowohl im Formular als auch im Regel-Editor leicht mit ihrem eindeutigen Namen identifizieren. Der Name darf jedoch keine Leerzeichen oder Sonderzeichen enthalten.

- **Titel**: Sie können mit dem Titel leicht eine Komponente in einem Formular identifizieren. Standardmäßig wird der Titel über der Komponente angezeigt. Wenn Sie keinen Titel hinzufügen, wird der Name der Komponente anstelle des Titeltexts angezeigt.

- **Titel ausblenden**: Wählen Sie die Option aus, um den Titel der Komponente auszublenden.

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

- **Verbindungsreferenz**: Eine Verbindungsreferenz ist ein Verweis auf ein Datenelement, das in einer externen Datenquelle gespeichert ist und in einem Formular verwendet wird. Sie können mit dem Bindungsverweis Daten dynamisch an Formularfelder binden, sodass das Formular die aktuellsten Daten aus der Datenquelle anzeigen kann. Beispielsweise kann ein Bindungsverweis verwendet werden, um den Namen und die Adresse von Kundinnen und Kunden in einem Formular anzuzeigen, basierend auf der im Formular eingegebenen Kunden-ID. Der Bindungsverweis kann auch verwendet werden, um die Datenquelle mit den im Formular eingegebenen Daten zu aktualisieren. Auf diese Weise können Sie mit AEM Forms Formulare erstellen, die mit externen Datenquellen interagieren und so ein nahtloses Benutzererlebnis bei der Datenerfassung und -verwaltung bieten.
- **Komponente ausblenden**: Wählen Sie diese Option, um die Komponente aus dem Formular auszublenden. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor. Dies ist nützlich, wenn Sie Informationen speichern müssen, die Benutzende nicht sehen oder direkt ändern müssen.
- **Komponente deaktivieren**: Wählen Sie die Option zum Deaktivieren der Komponente aus. Die deaktivierte Komponente ist nicht aktiv und Endbenutzende können sie nicht bearbeiten. Benutzende können den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor.

### Vertikale Registerkarte wiederholen {#repeat-tabs-on-top}

![Wiederholen, Registerkarte](/help/adaptive-forms/assets/vertical-tab-repeat-vertical-tab.png)

Sie können die Wiederholungsoptionen verwenden, um eine Komponente mit vertikalen Registerkarten und ihre untergeordneten Komponenten zu duplizieren, eine minimale und maximale Wiederholungsanzahl zu definieren und die Replikation ähnlicher Abschnitte innerhalb eines Formulars zu erleichtern. Bei der Interaktion mit der Komponente Vertikale Registerkarten und dem Zugriff auf ihre Einstellungen werden die folgenden Optionen angezeigt:

- **Wiederholbar machen: Vertikale Registerkarten**: Eine Umschalter-Funktion, mit der Benutzer die Wiederholungsfunktion aktivieren oder deaktivieren können.
- **Mindestwiederholungen**: Legt fest, wie oft die Komponente Vertikale Registerkarten mindestens wiederholt werden kann. Der Wert null zeigt an, dass die Komponente Vertikale Registerkarten nicht wiederholt wird. Der Standardwert ist null.
- **Maximale Wiederholungen**: Legt fest, wie oft die Komponente Vertikale Registerkarten maximal wiederholt werden kann. Standardmäßig ist dieser Wert unbegrenzt.

Um wiederholbare Abschnitte auf den vertikalen Registerkarten effektiv zu verwalten, führen Sie die Schritte aus, die im Abschnitt [Erstellen von Formularen mit wiederholbaren Abschnitten](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/create-forms-repeatable-sections.html?lang=de) Artikel.

### Registerkarte „Elemente“ {#items-tab}

![Registerkarte „Elemente“](/help/adaptive-forms/assets/vertical-tab-items.png)

Mit der Schalfläche **Hinzufügen** können Sie eine Komponente vom Komponentenauswahl-Fenster auswählen und als Bedienfeld hinzufügen. Nach dem Hinzufügen der Komponente werden die folgenden Optionen angezeigt:

- **Symbol**: Das Symbol identifiziert die Komponente des Bedienfelds in der Liste. Sie können den Mauszeiger über das Symbol bewegen, um den vollständigen Komponentennamen als QuickInfo anzuzeigen.
- **Beschreibung**: Die Beschreibung, die als Text des Bedienfelds verwendet wird. Standardmäßig der Name der für das Bedienfeld ausgewählten Komponente.
- **Löschen** - Tippen oder klicken Sie, um das Bedienfeld aus der Komponente Vertikale Registerkarten zu löschen.
- **Neu anordnen**: Tippen oder klicken und ziehen Sie, um die Reihenfolge der Bedienfelder neu anzuordnen.

### Registerkarte „Hilfe-Inhalt“ {#help-content}

![Registerkarte „Hilfe-Inhalt“](/help/adaptive-forms/assets/vertical-tab-help.png)

- **Kurzbeschreibung**: Eine Kurzbeschreibung ist eine kurze Erklärung, die zusätzliche Informationen oder Klarstellungen über den Zweck eines Formularfelds bietet. Es hilft Benutzenden zu verstehen, welcher Datentyp in das Feld eingegeben werden soll, und kann Richtlinien oder Beispiele bereitstellen, um sicherzustellen, dass die eingegebenen Informationen gültig sind und die gewünschten Kriterien erfüllen. Standardmäßig bleiben kurze Beschreibungen ausgeblendet. Aktivieren Sie die Option **Kurzbeschreibung immer anzeigen**, um sie unterhalb der Komponente anzuzeigen.

- **Kurzbeschreibung immer anzeigen**: Aktivieren Sie diese Option, um die Kurzbeschreibung unterhalb der Komponente anzuzeigen.

- **Hilfetext**: Hilfetext bezieht sich auf zusätzliche Informationen oder Anleitungen, die den Benutzenden bereitgestellt werden, um sie beim korrekten Ausfüllen eines Formularfelds zu unterstützen. Er erscheint, wenn Benutzende auf das Hilfesymbol (i) neben der Komponente klicken. Hilfetext enthält detailliertere Informationen als die Beschriftung oder der Platzhaltertext eines Formularfelds und soll den Benutzenden dabei helfen, die Anforderungen oder Einschränkungen des Felds zu verstehen. Er kann auch Vorschläge oder Beispiele anbieten, um das Ausfüllen des Formulars einfacher und genauer zu gestalten.

### Registerkarte „Barrierefreiheit“ {#accessibility}

![Registerkarte „Barrierefreiheit“](/help/adaptive-forms/assets/vertical-tab-accessibility.png)

- **Text für Bildschirmlesehilfen** – Das ist zusätzlicher Text, der von Hilfstechnologien wie etwa Bildschirmlesehilfen für sehbehinderte Personen vorgelesen wird. Dieser Text enthält eine Audiobeschreibung des Zwecks des Formularfelds und kann Informationen über den Titel, die Beschreibung, den Namen und alle relevanten Nachrichten (benutzerdefinierten Text) des Felds enthalten. Der Text der Bildschirmlesehilfe hilft sicherzustellen, dass das Formular allen Benutzenden zugänglich ist, auch Personen mit Sehschwäche, und bietet ihnen ein umfassendes Verständnis des Formularfelds und seiner Anforderungen.

- **HTML-Rolle für die Ankündigung durch die Bildschirmlesehilfe** – Die HTML-Rolle ist ein Attribut, mit dem der Zweck eines HTML-Elements für Hilfstechnologien wie Bildschirmlesehilfen spezifiziert wird. Rollenattribute werden verwendet, um für ein Element zusätzlichen Kontext und eine semantische Bedeutung bereitzustellen, wodurch es für Bildschirmlesehilfen einfacher wird, den Inhalt zu interpretieren und ihn Benutzenden mitzuteilen. In AEM Forms kann beispielsweise die Beschriftung eines Formularfelds die Rolle „Beschriftung“ haben und sein Eingabefeld die Rolle „Textfeld“. Dadurch kann die Bildschirmlesehilfe die Beziehung zwischen Beschrfitung und Eingabefeld verstehen und diese Informationen den Benutzenden korrekt mitteilen.

## Dialogfeld „Design“ {#design-dialog}

Im Dialogfeld „Design“ können Vorlagenerstellende steuern, wie Elemente standardmäßig angezeigt werden. Für die Komponente Vertikale Registerkarten des adaptiven Forms können Sie Folgendes festlegen:

- Die Kernkomponenten, die ein Formularersteller den vertikalen Registerkarten im Adaptive Forms Editor hinzufügen kann
- Einfache Namen für Stile (CSS-Klassen), die im Eigenschaftendialogfeld der Komponente Vertikale Registerkarten im Adaptive Forms-Editor angewendet werden können.

Dadurch wird das Erstellen und Anpassen von Formularen einfacher und effizienter.

### Registerkarte „Zugelassene Komponenten“ {#allowed-components-tab}

![Registerkarte „Zugelassene Komponenten“](/help/adaptive-forms/assets/tabs-allowed-component.png)

Die **Zugelassene Komponenten** -Tab ermöglicht es dem Vorlageneditor, die Komponenten festzulegen, die den Bedienfeldern in der Komponente Vertikale Registerkarten im Editor für adaptive Forms als Elemente hinzugefügt werden können.

### Registerkarte „Stile“ {#styles-tab}

![Registerkarte &quot;Stile&quot;](/help/adaptive-forms/assets/tabs-styles-tab.png)

Sie können das Dialogfeld „Design“ zum Definieren und Verwalten von CSS-Stilen für eine Komponente verwenden. Die Kernkomponente &quot;Vertikale Registerkarten&quot;der adaptiven Forms unterstützt die AEM [Stilsystem](/help/get-started/authoring.md#component-styling).

- **Standard-CSS-Klassen**: Sie können eine standardmäßige CSS-Klasse für die Kernkomponente Adaptive Forms Vertikale Registerkarten bereitstellen.

- **Zulässige Stile**: Sie können Stile definieren, indem Sie den Namen und die CSS-Klasse für den Stil angeben. Sie können beispielsweise einen Stil mit dem Namen „Fettschrift“ erstellen und die CSS-Klasse „Schriftbreite: Fett“ bereitstellen. Sie können diese Stile bei einem adaptiven Formular im adaptiven Formular-Editor anwenden. Um einen Stil anzuwenden, wählen Sie im Editor für adaptive Formulare die Komponente aus, auf die Sie den Stil anwenden möchten, navigieren Sie zum Eigenschaften-Dialog und wählen Sie den gewünschten Stil aus der Dropdown-Liste **Stile**. Wenn Sie die Stile aktualisieren oder ändern müssen, kehren Sie einfach zum Dialogfeld „Design“ zurück, aktualisieren die Stile auf der Registerkarte „Stile“ und speichern die Änderungen.

### Registerkarte &quot;Benutzerdefinierte Eigenschaften&quot;

![Registerkarte &quot;Benutzerdefinierte Eigenschaften&quot;](/help/adaptive-forms/assets/tabs-custom-properties.png)

Mit benutzerdefinierten Eigenschaften können Sie benutzerdefinierte Attribute (Schlüssel-Wert-Paare) mithilfe der Formularvorlage mit einer Kernkomponente des adaptiven Formulars verknüpfen. Die benutzerdefinierten Eigenschaften werden im Abschnitt &quot;Eigenschaften&quot;der Headless-Ausgabe der Komponente angezeigt. Dies ermöglicht das Erstellen eines dynamischen Formularverhaltens, das sich basierend auf den benutzerdefinierten Attributwerten anpasst. Beispielsweise können Entwickler verschiedene Ausgabeformate einer Headless-Forms-Komponente für mobile, Desktop- oder Webplattformen entwerfen, wodurch das Benutzererlebnis auf einer Vielzahl von Geräten erheblich verbessert wird.

- **Gruppenname**: Sie können einen Namen angeben, um die benutzerdefinierte Eigenschaftsgruppe zu identifizieren. Sie können mehrere benutzerdefinierte Eigenschaftsgruppen hinzufügen, löschen oder neu anordnen. Nachdem Sie die benutzerdefinierte Eigenschaftsgruppe hinzugefügt haben, sehen Sie die folgenden Optionen:

   - **Schlüssel-Wert-Paare**: Sie können mehrere benutzerdefinierte Eigenschaftsnamen und benutzerdefinierte Eigenschaftswerte hinzufügen, indem Sie auf das **Hinzufügen** -Schaltfläche für jede benutzerdefinierte Eigenschaftsgruppe.

   - **Löschen**: Tippen oder klicken Sie auf , um den benutzerdefinierten Eigenschaftsnamen und den benutzerdefinierten Eigenschaftswert zu löschen.

   - **Neu anordnen**: Tippen oder klicken und ziehen Sie, um die Reihenfolge des benutzerdefinierten Eigenschaftsnamens und des benutzerdefinierten Eigenschaftswerts neu anzuordnen.

## Ähnliche Artikel {#related-articles}

{{more-like-this}}

## Siehe auch {#see-also}

{{see-also}}
