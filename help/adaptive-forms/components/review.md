---
title: Kernkomponente für adaptive Formulare – Überprüfungskomponente
description: Verwenden oder Anpassen der Überprüfungs-Kernkomponente für adaptive Formulare.
role: Architect, Developer, Admin, User
hide: true
hidefromtoc: true
exl-id: acd230ed-284b-4df2-98e0-a0090cd73611
source-git-commit: 6725784bd4c94d433c91d6bd65d14d03cbefd954
workflow-type: ht
source-wordcount: '0'
ht-degree: 100%

---


# Überprüfungskomponente

Die Überprüfungskomponente in adaptiven Formularen ermöglicht es Benutzenden, die eingegebenen Informationen vor dem Absenden des Formulars zu überprüfen und zu verifizieren. Sie dient als Übersichtsseite und bietet eine schreibgeschützte Ansicht aller Felder und ihrer Werte in einem strukturierten und benutzerfreundlichen Format. Diese Funktion stellt sicher, dass Benutzende Fehler oder Auslassungen identifizieren und korrigieren können, bevor sie ihre Übermittlung abschließen, was das gesamte Formularerlebnis verbessert. Durch Klicken auf das Bearbeitungssymbol können die eingegebenen Informationen vor der Formularübermittlung geändert werden.

{{traditional-aem}}

**Beispiel**

![Überprüfungskomponente](/help/adaptive-forms/assets/review-component.png){width=50%, align=center}

## Verwendung

Es folgen mehrere Gründe für die Verwendung der Überprüfungskomponente in einem adaptiven Formular:

- **Verbesserte Datengenauigkeit**: Die Überprüfungskomponente ermöglicht es Benutzenden, alle eingegebenen Daten vor der Übermittlung zu überprüfen. Dadurch wird das Risiko von Fehlern oder Auslassungen reduziert und sichergestellt, dass die übermittelten Daten korrekt sind.
- **Verbessertes Benutzererlebnis**: Benutzende erhalten eine klare, übersichtliche Zusammenfassung aller von ihnen ausgefüllten Informationen, sodass sie vor der endgültigen Übermittlung sicher sein können, dass das Formular vollständig und korrekt ist, was das Gesamterlebnis verbessert.
- **Fehlererkennung und -behebung**: Sie bietet die Möglichkeit, Informationen auf Panel- oder Feldebene zu bearbeiten, sodass Benutzende Fehler korrigieren können, ohne durch mehrere Registerkarten zurücknavigieren zu müssen. Durch Klicken auf das Symbol **Bearbeiten** neben einem Panel oder Feld kann man problemlos zurückkehren und alle Probleme beheben.
- **Erhöhte Benutzersicherheit**: Benutzende können die eingegebenen Daten überprüfen und sich vergewissern, dass die von ihnen übermittelten Informationen korrekt sind, was zu weniger Übermittlungsfehlern und mehr Vertrauen in die Formularfunktionen führt.
- **Verhindern von unbeabsichtigten Übermittlungen**: Benutzende klicken häufig auf **Senden**, ohne alle Details zu überprüfen. Die **Überprüfungskomponente** gibt ihnen eine letzte Chance, ihre Daten zu überprüfen, wodurch die Wahrscheinlichkeit unbeabsichtigter Übermittlungen reduziert wird.


## Technische Details {#technical-details}

Aktuelle Informationen zur Überprüfungs-Kernkomponente für adaptive Formulare finden Sie in der technischen Dokumentation auf [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/textinput/v1/textinput). Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Entwicklerdokumentation für Kernkomponenten](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Sie können die Eigenschaften einfach über das Dialogfeld „Konfigurieren“ anpassen, um für ein nahtloses Benutzererlebnis zu sorgen.

![Dialogfeld „Konfigurieren“](/help/adaptive-forms/assets/review-component-configure-dialog.png)

- **Name**: Sie können eine Formularkomponente sowohl im Formular als auch im Regeleditor durch ihren eindeutigen Namen identifizieren. Der Name darf keine Leerzeichen oder Sonderzeichen enthalten.

- **Titel**: Mit dem Titel können Sie eine Komponente in einem Formular leicht identifizieren. Standardmäßig wird der Titel oberhalb der Komponente angezeigt. Wenn Sie keinen Titel hinzufügen, wird der Name der Komponente anstelle des Titeltexts angezeigt.
- **Titel ausblenden**: Wählen Sie die Option aus, um den Titel der Komponente auszublenden.
- **Bearbeitungsmodusaktionen aktivieren für**: Die Optionen **Bearbeitungsmodusaktionen aktivieren für** ermöglichen es Benutzenden, die eingegebenen Informationen zu ändern. Die Benutzenden können die Informationen entweder auf Feld- oder auf Panel-Ebene bearbeiten.
   - Wenn Benutzende die Option **Feld** auswählen, können sie während der Überprüfung einzelne Formularfelder bearbeiten.
   - Wenn Benutzende die Option **Panel** auswählen, können sie alle Felder in einem bestimmten Abschnitt (Panel) bearbeiten.
   - Wenn Benutzende die Option **Feld und Panel** auswählen, können sie auf das Bearbeitungssymbol neben einem Feld klicken, um bestimmte Informationen zu ändern, oder neben einem Panel, um alle Felder in diesem Panel zu bearbeiten.
   - Wenn Benutzende die Option **Ohne** auswählen, können sie jedes Feld oder Panel im gesamten Formular bearbeiten.

  Standardmäßig ist die Option **Panel** ausgewählt.

- **Panels verknüpfen**: Mit der Option **Panels verknüpfen** können Benutzende die Panels zur Überprüfung auswählen. Wenn Panels verknüpft sind, können Benutzende die eingegebenen Informationen der ausgewählten Panels überprüfen und vor der Übermittlung ändern.

## Anwendungsfall

Nehmen Sie als Beispiel ein **Kreditantragsformular**, das aus vier Registerkarten besteht, auf denen jede Registerkarte spezifische Informationen über die Person erfasst:

- **Persönliche Details**: Erfasst die grundlegenden persönlichen Details der Person, wie etwa Name, Geburtsdatum, Kontaktinformationen und Adresse.

- **Darlehensdetails**: Sammelt Informationen zum Darlehen, einschließlich der Art des Darlehens, des gewünschten Betrags, des Rückzahlungszeitraums und automatisch berechneter Felder wie Zinssatz und monatliche Rate.

- **Zusätzliche Dokumente**: Ermöglicht den Benutzenden das Hochladen erforderlicher Dokumente wie Identitätsnachweis, Adressnachweis oder Einkommensnachweis. Es enthält auch ein Kontrollkästchen für eine Erklärung, um die Zustimmung zu den Bedingungen zu bestätigen.

- **Formular überprüfen und senden**: Enthält eine Überprüfungskomponente, in der alle Eingaben aus den vorherigen Registerkarten zusammengefasst sind. Die Benutzenden können ihre Daten vor dem Absenden des Formulars überprüfen und bearbeiten. Diese Registerkarte enthält auch die Schaltfläche **Senden** zum Senden des Antrags.

Das folgende Video zeigt, wie Sie die Komponente **Überprüfen** so konfigurieren, dass sie den Benutzenden die Flexibilität bietet, Informationen zu bearbeiten:

## Ähnliche Artikel {#related-articles}

{{more-like-this}}

## Siehe auch {#see-also}

{{see-also}}
