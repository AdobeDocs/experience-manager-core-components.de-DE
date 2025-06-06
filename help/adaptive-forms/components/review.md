---
title: Kernkomponente „Überprüfung“ für adaptive Forms
description: Verwenden oder Anpassen der Kernkomponente „Überprüfung“ für adaptive Forms.
role: Architect, Developer, Admin, User
hide: true
hidefromtoc: true
source-git-commit: 04a685cfa2616839f4fec715847bf0821808bd59
workflow-type: tm+mt
source-wordcount: '742'
ht-degree: 14%

---


# Überprüfungskomponente

Die Überprüfungskomponente in Adaptive Forms ermöglicht es Benutzenden, die eingegebenen Informationen vor dem Absenden des Formulars zu überprüfen und zu überprüfen. Sie dient als Übersichtsseite und bietet eine schreibgeschützte Ansicht aller Felder und ihrer Werte in einem strukturierten und benutzerfreundlichen Format. Diese Funktion stellt sicher, dass Benutzer Fehler oder Auslassungen identifizieren und korrigieren können, bevor sie ihre Übermittlung abschließen, was das gesamte Formularerlebnis verbessert. Durch Klicken auf das Bearbeitungssymbol können die eingegebenen Informationen vor der Formularübermittlung geändert werden.

**Beispiel**

![Komponente überprüfen](/help/adaptive-forms/assets/review-component.png){width=50%, align=center}

## Verwendung

Im Folgenden finden Sie die Gründe für die Verwendung der Überprüfungskomponente in einem adaptiven Formular:

- **Verbesserte Datengenauigkeit**: Die Überprüfungskomponente ermöglicht es Benutzenden, alle eingegebenen Daten vor der Übermittlung zu überprüfen. Dadurch wird das Risiko von Fehlern oder Auslassungen reduziert und sichergestellt, dass die übermittelten Daten korrekt sind.
- **Verbessertes Benutzererlebnis**: Benutzer erhalten eine klare, übersichtliche Zusammenfassung aller von ihnen ausgefüllten Informationen, sodass sie darauf vertrauen können, dass das Formular vor der endgültigen Übermittlung vollständig und korrekt ist, was das Gesamterlebnis verbessert.
- **Fehlererkennung und -behebung**: Sie bietet die Möglichkeit, Informationen auf Bedienfeld- oder Feldebene zu bearbeiten, sodass Benutzende Fehler korrigieren können, ohne durch mehrere Registerkarten zurück zu navigieren. Durch Klicken auf **Bearbeiten**-Symbol neben einem Bedienfeld oder Feld können Sie problemlos zurückkehren und alle Probleme beheben.
- **Erhöhte Benutzersicherheit**: Benutzer können die eingegebenen Daten überprüfen und sich vergewissern, dass die von ihnen übermittelten Informationen korrekt sind, was zu weniger Übermittlungsfehlern und mehr Vertrauen in die Formularfunktionen führt.
- **Verhindern von unbeabsichtigten Übermittlungen**: Benutzer klicken häufig auf **Senden**, ohne alle Details zu überprüfen. Die **Überprüfungs**-Komponente gibt ihnen eine letzte Chance, ihre Daten zu überprüfen, wodurch die Wahrscheinlichkeit unbeabsichtigter Übermittlungen reduziert wird.


## Technische Details {#technical-details}

Die neuesten Informationen zur Kernkomponente „Überprüfung“ für adaptive Forms finden Sie in der technischen Dokumentation auf [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/textinput/v1/textinput). Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Entwicklerdokumentation für Kernkomponenten](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Im Dialogfeld „Konfigurieren“ können Sie das Erlebnis für Besuchende einfach anpassen, um das Benutzererlebnis zu verbessern.

![Dialogfeld „Konfigurieren](/help/adaptive-forms/assets/review-component-configure-dialog.png)

- **Name**: Sie können eine Formularkomponente sowohl im Formular als auch im Regeleditor durch ihren eindeutigen Namen identifizieren. Der Name darf keine Leerzeichen oder Sonderzeichen enthalten.

- **Titel**: Mit dem Titel können Sie eine Komponente in einem Formular leicht identifizieren. Standardmäßig wird der Titel oberhalb der Komponente angezeigt. Wenn Sie keinen Titel hinzufügen, wird der Name der Komponente anstelle des Titeltexts angezeigt.
- **Titel ausblenden**: Wählen Sie die Option aus, um den Titel der Komponente auszublenden.
- **Bearbeitungsmodusaktionen aktivieren für** - Die Optionen **Bearbeitungsmodusaktionen aktivieren für** ermöglichen es Benutzern, die eingegebenen Informationen zu ändern. Benutzer können die Informationen entweder auf Feld- oder auf Bedienfeldebene bearbeiten.
   - Wenn Benutzende die Option **Feld** auswählen, können sie während der Überprüfung einzelne Formularfelder bearbeiten.
   - Wenn Benutzende die Option **Bedienfeld** auswählen, können sie alle Felder in einem bestimmten Abschnitt (Bedienfeld) bearbeiten.
   - Wenn Benutzende die Option **Feld und Bedienfeld** auswählen, können sie auf das Bearbeitungssymbol neben einem Feld klicken, um bestimmte Informationen zu ändern, oder neben einem Bedienfeld, um alle Felder in diesem Bedienfeld zu bearbeiten.
   - Wenn Benutzende die Option **Ohne** auswählen, können sie jedes Feld oder Bedienfeld im gesamten Formular bearbeiten.

  Standardmäßig ist die Option **Bedienfeld** ausgewählt.

- **Bedienfelder verknüpfen** - Mit der Option **Bedienfelder verknüpfen** können Benutzende die Bedienfelder zur Überprüfung auswählen. Wenn Bedienfelder verknüpft sind, können Benutzende die eingegebenen Informationen der ausgewählten Bedienfelder überprüfen und vor der Übermittlung ändern.

## Anwendungsfall

Nehmen Sie ein Beispiel für ein **Kreditantragsformular** das aus vier Registerkarten besteht, auf denen jede Registerkarte spezifische Informationen über den Benutzer erfasst:

- **Persönliche Details**: Erfasst die grundlegenden persönlichen Details des Benutzers, wie Name, Geburtsdatum, Kontaktinformationen und Adresse.

- **Darlehensdetails**: Sammelt Informationen zum Darlehen, einschließlich der Art des Darlehens, des gewünschten Betrags, des Rückzahlungszeitraums und automatisch berechneter Felder wie Zinssatz und monatliches EWI.

- **Zusätzliche Dokumente**: Ermöglicht dem Benutzer das Hochladen erforderlicher Dokumente wie ID-Korrekturabzug, Adressnachweis und Einkommensnachweis. Es enthält auch ein Kontrollkästchen für die Deklaration, um die Zustimmung zu den Bedingungen zu bestätigen.

- **Formular überprüfen und senden**: Enthält eine Überprüfungskomponente, in der alle Eingaben aus den vorherigen Registerkarten zusammengefasst sind. Benutzer können ihre Daten vor dem Absenden des Formulars überprüfen und bearbeiten. Diese Registerkarte enthält auch die Schaltfläche **Senden** zum Senden des Antrags.

Das folgende Video zeigt, wie Sie die Komponente **Überprüfen** so konfigurieren, dass sie den Benutzenden die Flexibilität bietet, Informationen zu bearbeiten:

## Ähnliche Artikel {#related-articles}

{{more-like-this}}

## Siehe auch {#see-also}

{{see-also}}

