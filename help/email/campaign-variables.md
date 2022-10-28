---
title: Kampagnenvariablen
description: Verwenden Sie Kampagnenvariablen als Platzhalter, um personalisierte E-Mail-Inhalte zu erstellen.
role: Architect, Developer, Admin, User
hidefromtoc: true
index: false
source-git-commit: 8bebe3ca036557f3f7c6b8ec0e65d6d104d5ffae
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 0%

---


# Kampagnenvariablen {#campaign-variables}

Verwenden Sie Kampagnenvariablen, um personalisierte E-Mail-Inhalte zu erstellen. Kampagnenvariablen dienen als Platzhalter für Adobe Campaign-Werte, die Sie in Ihren E-Mail-Inhalt einfügen können. Wenn der Inhalt über Adobe Campaign gesendet wird, ersetzt Campaign diese Variablen durch den personalisierten Inhalt des Empfängers.

## Nutzung {#usage}

Die E-Mail-Kernkomponenten machen Kampagnenvariablen über Personalisierungsschaltflächen neben allgemeinen Textfeldern leicht zugänglich. Bei gedrückter Taste wird ein Dialogfeld angezeigt, in dem Sie ein Personalisierungsfeld auswählen können.

Die Liste der verfügbaren Personalisierungsfelder wird mit Ihrer Adobe Campaign-Instanz synchronisiert. Die Felder werden in Adobe Campaign im Schema verwaltet `nms:seedMember`. Alle Felder in `nms:seedMember` muss auch in Ihrer Empfängertabelle vorhanden sein.

## Dialogfeld &quot;Adobe Campaign-Variable auswählen&quot; {#dialog}

Das Dialogfeld Adobe Campaign-Variable auswählen ist in vielen Bearbeitungsdialogfeldern der E-Mail-Kernkomponenten verfügbar. Um sie zu verwenden, klicken Sie einfach auf **Adobe Campaign-Variable auswählen** neben dem entsprechenden Feld. Dieses Symbol kann zwei Formen annehmen.

![Adobe Campaign-Schaltfläche](/help/email/assets/campaign-button.png)
![Symbol Adobe Campaign-Variable auswählen](/help/email/assets/select-adobe-campaign-variable-icon.png)

Durch Klicken auf beide Symbole wird der **Adobe Campaign-Variable auswählen** angezeigt.

![Dialogfeld &quot;Adobe Campaign-Variable auswählen&quot;](assets/select-campaign-variable-dialog.png)

Verwenden Sie die Spaltenansicht, um die Variable zu suchen, die Sie einfügen möchten. Wenn Sie auf einen Knoten in einer Spalte klicken, werden dessen untergeordnete Elemente in einer neuen Spalte rechts angezeigt. Auf diese Weise können Sie in der Inhaltsstruktur der Variablen navigieren.

Wählen Sie die Variable aus, die Sie einfügen möchten, und klicken Sie dann oben rechts im Dialogfeld auf das Häkchen.

![Adobe Campaign-Variable ausgewählt](assets/select-campaign-variable-dialog-selected.png)

Die Variable wird dann in das Feld des Bearbeitungsdialogfelds der E-Mail-Kernkomponente eingefügt.

![In das Dialogfeld &quot;Bearbeiten&quot;eingefügte Kampagnenvariable](assets/campaign-variable.png)

Klicken Sie jederzeit auf das X oben links im Dialogfeld, um das Dialogfeld abzubrechen und zu schließen.
