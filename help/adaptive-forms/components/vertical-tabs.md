---
title: Kernkomponente für adaptive Formulare – Vertikale Registerkarten
description: Verwenden oder Anpassen der Kernkomponente „Vertikale Registerkarten“ für adaptive Formulare.
role: Architect, Developer, Admin, User
exl-id: d5cd1c18-6840-4f2f-a767-a69b803e6075
source-git-commit: a6c3fd98bcdcbb0d6d5697b93306adc9ef7e3fc9
workflow-type: tm+mt
source-wordcount: '2112'
ht-degree: 99%

---

# Komponente „Vertikale Registerkarten“{#vertical-tabs-adaptive-forms-core-component}

<span class="preview"> Dieser Artikel enthält Inhalte zum  **Rich-Text für Titel zulassen**  -Funktion, einer Funktion vor der Veröffentlichung. Die Vorabveröffentlichungsfunktion ist nur über unseren [Vorabveröffentlichungskanal](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/release-notes/prerelease.html?lang=de#new-features) zugänglich.</span>

Vertikale Registerkarten in adaptiven Formularen sind so aufgebaut, dass mehrere Abschnitte eines Formulars gruppiert und als separate, vertikal ausgerichtete Registerkarten angezeigt werden. Benutzende können zwischen den Registerkarten wechseln, um auf verschiedene Abschnitte des Formulars zuzugreifen. Jede Registerkarte dient als Auslöser zum Anzeigen und Ausblenden des jeweiligen Formularinhalts. Mit vertikalen Registerkarten können Sie lange Formulare in überschaubare Abschnitte organisieren und das Benutzererlebnis verbessern. Registerkarten können ein Formular für Benutzende mit Beeinträchtigungen barrierefreier gestalten, da sie mithilfe der Tastaturnavigation zwischen Abschnitten wechseln können.
Wenn Benutzende auf eine Registerkarte klicken, wird der Formularinhalt dynamisch aktualisiert und der entsprechende Abschnitt angezeigt.

>[!NOTE]
>
> Für AEM 6.5 Forms wurde diese Komponente mit AEM 6.5 Forms Service Pack 19 (6.5.19.0) eingeführt. Um diese Komponente zu aktivieren, stellen Sie sicher, dass die erforderlichen Versionen der Forms-Kernkomponenten und der WCM-Kernkomponenten installiert sind. Ausführliche Informationen zu den Versionen der Kernkomponenten für adaptive Formulare finden Sie unter [Kernkomponentenversionen für adaptive Formulare](/help/adaptive-forms/version.md)

![Beispiel](/help/adaptive-forms/assets/horizontal-example.png)

## Verwendung {#reasons-to-use-vertical-tabs}

Die häufigsten Gründe für die Verwendung vertikaler Registerkarten in einem adaptiven Formular sind:

- **Verbesserte Benutzerfreundlichkeit**: Vertikale Registerkarten erleichtern Benutzenden die Navigation durch das Formular, insbesondere wenn das Formular mehrere Abschnitte oder eine große Anzahl von Feldern enthält.

- **Platz-Management**: Vertikale Registerkarten sparen Platz auf dem Bildschirm, indem sie verwandte Formularabschnitte in Registerkarten gruppieren und jeweils nur einen Abschnitt anzeigen.

- **Bessere Organisation**: Registerkarten bieten eine klare und übersichtliche Struktur für ein Formular, sodass Benutzende das Formular besser verstehen und ausfüllen können.

- **Erhöhte Benutzerinteraktion**: Vertikale Registerkarten können ein Formular für Benutzende visuell ansprechender und interessanter gestalten, wodurch die Formularabschlussrate verbessert werden kann.

## Version und Kompatibilität {#version-and-compatibility}

Die Kernkomponente „Vertikale Registerkarten“ für adaptive Formulare wurde als Teil der Kernkomponenten 2.0.18 veröffentlicht. Hier finden Sie eine Tabelle mit allen unterstützten Versionen, Informationen zur AEM-Kompatibilität und Links zur entsprechenden Dokumentation:

|  |  |
|---|---|
| Komponentenversion | AEM as a Cloud Service |
| --- | --- |
| v1 | Kompatibel mit<br>[Version 2.0.18](/help/adaptive-forms/version.md) und höher | Kompatibel | Kompatibel |

Informationen zu Versionen und Freigaben der Kernkomponente finden Sie im Dokument [Kernkomponenten-Versionen](/help/adaptive-forms/version.md).

## Technische Details {#technical-details}

Die neuesten Informationen zur Kernkomponente „Vertikale Registerkarten“ für adaptive Formulare finden Sie in der technischen Dokumentation auf [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/verticaltabs/v1/verticaltabs). Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Entwicklerdokumentation für Kernkomponenten](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Im Dialogfeld „Konfigurieren“ können Sie die vertikalen Registerkarten einfach anpassen. Sie können auch Optionen für vertikale Registerkarten definieren, um das Benutzererlebnis zu verbessern.

### Registerkarte „Allgemein“ {#basic-tab}

![Registerkarte „Allgemein“](/help/adaptive-forms/assets/vertical-tab-basic.png)

- **Name**: Sie können eine Formularkomponente sowohl im Formular als auch im Regel-Editor leicht mit ihrem eindeutigen Namen identifizieren. Der Name darf jedoch keine Leerzeichen oder Sonderzeichen enthalten.

- **Titel**: Sie können mit dem Titel leicht eine Komponente in einem Formular identifizieren. Standardmäßig wird der Titel über der Komponente angezeigt. Wenn Sie keinen Titel hinzufügen, wird der Name der Komponente anstelle des Titeltexts angezeigt.
- **Rich-Text für Titel zulassen**: Diese Funktionen ermöglichen es Benutzenden, einfache Texttitel zu formatieren, die Funktionen wie fett, kursiv, unterstrichener Text, verschiedene Schriftarten, Schriftgrößen, Farben und zusätzliche Optionen enthalten und so die visuelle Darstellung und Anpassung zu verbessern. Sie bietet mehr Flexibilität und kreative Kontrolle bei der Hervorhebung von Titeln in Dokumenten, Websites oder Anwendungen.\
  Durch Aktivieren des Kontrollkästchens **Rich-Text für Titel zulassen** werden Formatierungsoptionen sichtbar, mit denen Sie den Titel der Komponente gestalten können. Um auf alle verfügbaren Formatierungsoptionen zuzugreifen, können Sie auf die Registerkarte ![Vollbildsymbol](/help/adaptive-forms/assets/fullscreen-icon.png) klicken.

  ![Rich-Text-Unterstützung](/help/adaptive-forms/assets/richtext-support-title.png)

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

- **Schreibgeschützt**: Wählen Sie die Option aus, um die Komponente nicht bearbeitbar zu machen. Benutzende können den Wert des Felds anzeigen, ihn jedoch nicht ändern. Die Komponente bleibt für andere Zwecke verfügbar, z. B. für Berechnungen im Regel-Editor.

### Vertikale Registerkarte – Wiederholen {#repeat-tabs-on-top}

![Registerkarte wiederholen](/help/adaptive-forms/assets/vertical-tab-repeat-vertical-tab.png)

Sie können die Wiederholungsoptionen verwenden, um die Komponente „Vertikale Registerkarten“ und ihre untergeordneten Komponenten zu duplizieren, eine minimale und maximale Wiederholungsanzahl zu definieren und die Replikation ähnlicher Abschnitte innerhalb eines Formulars zu erleichtern. Bei der Interaktion mit der Komponente „Vertikale Registerkarten“ und dem Zugriff auf ihre Einstellungen werden die folgenden Optionen angezeigt:

- **Vertikale Registerkarten wiederholbar machen**: Eine Umschalter-Funktion, mit der Benutzende die Wiederholungsfunktion aktivieren oder deaktivieren können.
- **Mindestwiederholungen**: Legt fest, wie oft die Komponente „Vertikale Registerkarten“ mindestens wiederholt werden kann. Der Wert null zeigt an, dass die Komponente „Vertikale Registerkarten“ nicht wiederholt wird. Der Standardwert ist null.
- **Maximale Wiederholungen**: Legt fest, wie oft die Komponente „Vertikale Registerkarten“ maximal wiederholt werden kann. Standardmäßig ist dieser Wert unbegrenzt.

Um wiederholbare Abschnitte innerhalb der vertikalen Registerkarten effektiv zu verwalten, folgen Sie den Schritten, die im Artikel [Erstellen von Formularen mit wiederholbaren Abschnitten](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/create-forms-repeatable-sections.html?lang=de) beschrieben sind.

### Registerkarte „Elemente“ {#items-tab}

![Registerkarte „Elemente“](/help/adaptive-forms/assets/vertical-tab-items.png)

Mit der Schalfläche **Hinzufügen** können Sie eine Komponente vom Komponentenauswahl-Fenster auswählen und als Bedienfeld hinzufügen. Nach dem Hinzufügen der Komponente werden die folgenden Optionen angezeigt:

- **Symbol**: Das Symbol identifiziert die Komponente des Bedienfelds in der Liste. Sie können den Mauszeiger über das Symbol bewegen, um den vollständigen Komponentennamen als QuickInfo anzuzeigen.
- **Beschreibung**: Die Beschreibung, die als Text des Bedienfelds verwendet wird. Standardmäßig der Name der für das Bedienfeld ausgewählten Komponente.
- **Entfernen**: Tippen oder klicken Sie, um das Bedienfeld aus der Komponente „Vertikale Registerkarten“ zu löschen.
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

Im Dialogfeld „Design“ können Vorlagenerstellende steuern, wie Elemente standardmäßig angezeigt werden. Für die Komponente „Vertikale Registerkarten“ in adaptiven Formularen können Sie folgende Einstellungen vornehmen:

- Die Kernkomponenten, die Formular-Erstellende mit dem Editor für adaptive Formulare den vertikalen Registerkarten hinzufügen können
- Einfache Namen für Stile (CSS-Klassen), die Sie im Dialogfeld „Eigenschaften“ der Komponente „Vertikale Registerkarten“ im Editor für adaptive Formulare anwenden können.

Dadurch wird das Erstellen und Anpassen von Formularen einfacher und effizienter.

### Registerkarte „Zugelassene Komponenten“ {#allowed-components-tab}

![Registerkarte „Zugelassene Komponenten“](/help/adaptive-forms/assets/tabs-allowed-component.png)

In der Registerkarte **Zugelassene Komponenten** können Vorlagen-Bearbeitende die Komponenten festlegen, die den Bedienfeldern in der Komponente „Vertikale Registerkarten“ im Editor für adaptive Formulare als Elemente hinzugefügt werden können.

### Registerkarte „Stile“ {#styles-tab}

![Registerkarte „Stile“](/help/adaptive-forms/assets/tabs-styles-tab.png)

Sie können das Dialogfeld „Design“ zum Definieren und Verwalten von CSS-Stilen für eine Komponente verwenden. Die Kernkomponente „Vertikale Registerkarten“ für adaptive Formulare unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).

- **Standard-CSS-Klassen**: Sie können für die Kernkomponente „Vertikale Registerkarten“ von adaptiven Formularen eine standardmäßige CSS-Klasse festlegen.

- **Zulässige Stile**: Sie können Stile definieren, indem Sie den Namen und die CSS-Klasse für den Stil angeben. Sie können beispielsweise einen Stil mit dem Namen „Fettschrift“ erstellen und die CSS-Klasse „Schriftbreite: Fett“ bereitstellen. Sie können diese Stile bei einem adaptiven Formular im adaptiven Formular-Editor anwenden. Um einen Stil anzuwenden, wählen Sie im Editor für adaptive Formulare die Komponente aus, auf die Sie den Stil anwenden möchten, navigieren Sie zum Eigenschaften-Dialog und wählen Sie den gewünschten Stil aus der Dropdown-Liste **Stile**. Wenn Sie die Stile aktualisieren oder ändern müssen, kehren Sie einfach zum Dialogfeld „Design“ zurück, aktualisieren die Stile auf der Registerkarte „Stile“ und speichern die Änderungen.

### Registerkarte „Benutzerdefinierte Eigenschaften“

![Registerkarte „Benutzerdefinierte Eigenschaften“](/help/adaptive-forms/assets/tabs-custom-properties.png)

Mit der Option „Benutzerdefinierte Eigenschaften“ können Sie mithilfe der Formularvorlage benutzerdefinierte Attribute (Schlüsselwertpaare) mit einer Kernkomponente eines adaptiven Formulars verknüpfen. Die benutzerdefinierten Eigenschaften werden im Eigenschaftenbereich der Headless-Ausgabedarstellung der Komponente angezeigt. So kann ein dynamisches Formularverhalten erzeugt werden, das sich je nach den benutzerdefinierten Attributwerten anpasst. Beispielsweise können Entwickelnde verschiedene Ausgabedarstellungen einer Headless-Formularkomponente für Mobile-, Desktop- oder Web-Plattformen entwerfen und so das Benutzererlebnis auf einer Vielzahl von Geräten erheblich verbessern.

- **Gruppenname**: Sie können einen Namen angeben, um die Gruppe der benutzerdefinierten Eigenschaften zu kennzeichnen. Sie können mehrere Gruppen benutzerdefinierter Eigenschaften hinzufügen, löschen oder neu anordnen. Nach dem Hinzufügen der Gruppe benutzerdefinierter Eigenschaften werden folgende Optionen angezeigt:

   - **Schlüssel-Wert-Paare**: Sie können mehrere Namen und Werte benutzerdefinierter Eigenschaften hinzufügen, indem Sie für jede Gruppe benutzerdefinierter Eigenschaften auf **Hinzufügen** klicken.

   - **Löschen**: Tippen oder klicken Sie auf diese Option, um den Namen und den Wert der benutzerdefinierten Eigenschaft zu löschen.

   - **Neu anordnen**: Ordnen Sie den Namen und Wert der benutzerdefinierten Eigenschaft Antippen oder Klicken und Ziehen neu an.

## Ähnliche Artikel {#related-articles}

{{more-like-this}}

## Siehe auch {#see-also}

{{see-also}}
