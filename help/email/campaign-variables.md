---
title: Kampagnenvariablen
description: Verwenden Sie Kampagnenvariablen als Platzhalter, um personalisierte E-Mail-Inhalte zu erstellen.
role: Architect, Developer, Admin, User
exl-id: 124ff5bf-6612-4baf-b0ff-6b1a95b455c1
index: false
source-git-commit: eb77567dc32cccb81a9fc131493d11fb55b7e93b
workflow-type: ht
source-wordcount: '294'
ht-degree: 100%

---


# Kampagnenvariablen {#campaign-variables}

Verwenden Sie Kampagnenvariablen, um personalisierte E-Mail-Inhalte zu erstellen. Kampagnenvariablen dienen als Platzhalter für Adobe Campaign-Werte, die Sie in Ihren E-Mail-Inhalt einfügen können. Wenn der Inhalt über Adobe Campaign gesendet wird, ersetzt Campaign diese Variablen durch den personalisierten Inhalt des Empfängers.

## Verwendung {#usage}

Die E-Mail-Kernkomponenten machen Kampagnenvariablen über Personalisierungsschaltflächen neben allgemeinen Textfeldern leicht zugänglich. Bei gedrückter Taste wird ein Dialogfeld angezeigt, in dem Sie ein Personalisierungsfeld auswählen können.

Die Liste der verfügbaren Personalisierungsfelder wird mit Ihrer Adobe Campaign-Instanz synchronisiert. Die Felder werden in Adobe Campaign im Schema `nms:seedMember` verwaltet. Alle Felder in `nms:seedMember` müssen auch in Ihrer Empfängertabelle vorhanden sein.

## Adobe Campaign-Variablendialogfeld auswählen {#dialog}

Das Dialogfeld „Adobe Campaign-Variable auswählen“ ist in vielen Bearbeitungsdialogfeldern der E-Mail-Kernkomponenten verfügbar. Um sie zu verwenden, klicken Sie neben dem entsprechenden Feld einfach auf **Adobe Campaign-Variable auswählen**. Dieses Symbol kann zwei Formen annehmen.

![Adobe Campaign-Button](/help/email/assets/campaign-button.png)
![Symbol „Adobe Campaign-Variable auswählen“](/help/email/assets/select-adobe-campaign-variable-icon.png)

Durch Klicken auf beide Symbole wird das Dialogfeld **Adobe Campaign-Variable auswählen** angezeigt.

![Dialogfeld „Adobe Campaign-Variable auswählen“](assets/select-campaign-variable-dialog.png)

Verwenden Sie die Spaltenansicht, um die Variable zu suchen, die Sie einfügen möchten. Wenn Sie auf einen Knoten in einer Spalte klicken, werden dessen untergeordnete Elemente in einer neuen Spalte rechts angezeigt. Auf diese Weise können Sie in der Inhaltsstruktur der Variablen navigieren.

Wählen Sie die Variable aus, die Sie einfügen möchten, und klicken Sie dann oben rechts im Dialogfeld auf das Häkchen.

![Adobe Campaign-Variable ausgewählt](assets/select-campaign-variable-dialog-selected.png)

Die Variable wird dann in das Feld des Bearbeitungsdialogfelds der E-Mail-Kernkomponente eingefügt.

![In das Dialogfeld „Bearbeiten“ eingefügte Kampagnenvariable](assets/campaign-variable.png)

Klicken Sie zum Abbrechen und Schließen jederzeit auf das X oben links im Dialogfeld.
