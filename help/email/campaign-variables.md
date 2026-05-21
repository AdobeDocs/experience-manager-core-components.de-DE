---
title: Kampagnenvariablen
description: Verwenden Sie Kampagnenvariablen als Platzhalter, um personalisierte E-Mail-Inhalte zu erstellen.
role: Developer, Admin, User
exl-id: 124ff5bf-6612-4baf-b0ff-6b1a95b455c1
index: false
TQID: https://experienceleague.adobe.com/MB6K-S4DZbsD3puXls8w4rWi6posFFLxJRewKORMkxA
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: eb3ad9f8-54a2-45f3-abb1-d3976415a718
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: ce44533e-8ec8-4e11-a9e9-78b0fe561832
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 73aa5234ac63fa3be99feebce448bb6722513838
workflow-type: tm+mt
source-wordcount: 296
ht-degree: 100%

---

# Kampagnenvariablen {#campaign-variables}

Verwenden Sie Kampagnenvariablen, um personalisierte E-Mail-Inhalte zu erstellen. Kampagnenvariablen dienen als Platzhalter für Adobe Campaign-Werte, die Sie in Ihren E-Mail-Inhalt einfügen können. Wenn der Inhalt über Adobe Campaign gesendet wird, ersetzt Campaign diese Variablen durch den personalisierten Inhalt des Empfängers.

## Verwendung {#usage}

Die E-Mail-Kernkomponenten machen Kampagnenvariablen über Personalisierungsschaltflächen neben allgemeinen Textfeldern leicht zugänglich. Bei gedrückter Taste wird ein Dialogfeld angezeigt, in dem Sie ein Personalisierungsfeld auswählen können.

Die Liste der verfügbaren Personalisierungsfelder wird mit Ihrer Adobe Campaign-Instanz synchronisiert. Die Felder werden in Adobe Campaign im Schema `nms:seedMember` verwaltet. Alle Felder in `nms:seedMember` müssen auch in Ihrer Empfängertabelle vorhanden sein.

## Adobe Campaign-Variablendialogfeld auswählen {#dialog}

Das Dialogfeld „Adobe Campaign-Variable auswählen“ ist in vielen Bearbeitungsdialogfeldern der E-Mail-Kernkomponenten verfügbar. Um sie zu verwenden, klicken Sie neben dem entsprechenden Feld einfach auf **Adobe Campaign-Variable auswählen**. Dieses Symbol kann zwei Formen annehmen.

![Schaltfläche „Adobe Campaign“](/help/email/assets/campaign-button.png)
![Symbol „Adobe Campaign-Variable auswählen“](/help/email/assets/select-adobe-campaign-variable-icon.png)

Durch Klicken auf beide Symbole wird das Dialogfeld **Adobe Campaign-Variable auswählen** angezeigt.

![Dialogfeld „Adobe Campaign-Variable auswählen“](assets/select-campaign-variable-dialog.png)

Verwenden Sie die Spaltenansicht, um die Variable zu suchen, die Sie einfügen möchten. Wenn Sie auf einen Knoten in einer Spalte klicken, werden dessen untergeordnete Elemente in einer neuen Spalte rechts angezeigt. Auf diese Weise können Sie in der Inhaltsstruktur der Variablen navigieren.

Wählen Sie die Variable aus, die Sie einfügen möchten, und klicken Sie dann oben rechts im Dialogfeld auf das Häkchen.

![Adobe Campaign-Variable ausgewählt](assets/select-campaign-variable-dialog-selected.png)

Die Variable wird dann in das Feld des Bearbeitungsdialogfelds der E-Mail-Kernkomponente eingefügt.

![In das Dialogfeld „Bearbeiten“ eingefügte Kampagnenvariable](assets/campaign-variable.png)

Klicken Sie zum Abbrechen und Schließen jederzeit auf das X oben links im Dialogfeld.
