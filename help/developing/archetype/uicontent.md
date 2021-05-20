---
title: ui.content-Modul des AEM-Projektarchetyps
description: ui.content-Modul des AEM-Projektarchetyps
feature: Kernkomponenten, AEM-Projektarchetyp
role: Architect, Developer, Administrator
exl-id: af019cd8-c733-4b53-bb57-321dd9451178
source-git-commit: 8ff36ca143af9496f988b1ca65475497181def1d
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 100%

---

# ui.content-Modul des AEM-Projektarchetyps {#uicontent-module}

Das Modul ui.content maven (`<src-directory>/<project>/ui.content`) umfasst Ausgangsinhalte und Konfigurationen unter `/content` und `/conf`. ui.content wird ähnlich wie ui.apps in ein AEM-Paket kompiliert. Der Hauptunterschied besteht darin, dass die in ui.content gespeicherten Knoten direkt auf der AEM-Instanz geändert werden können. Dazu gehören Seiten, DAM-Assets und bearbeitbare Vorlagen. Das Modul ui.content kann verwendet werden, um Beispielinhalte für eine saubere Instanz zu speichern und/oder um einige Basiskonfigurationen zu erstellen, die in der Quellcodeverwaltung verwaltet werden sollen.

## filter.xml {#filter}

Die `filter.xml`-Datei für das Modul ui.content befindet sich unter `<src>/<project>/ui.content/src/main/content/META-INF/vault/filter.xml` und enthält die Pfade, die mit dem Paket ui.content eingeschlossen und installiert werden. Beachten Sie, dass dem Pfad ein `mode="merge"` Attribut hinzugefügt wird. Dadurch wird sichergestellt, dass die mit einer Codebereitstellung bereitgestellten Konfigurationen nicht automatisch Inhalte oder Konfigurationen außer Kraft setzen, die direkt auf der AEM-Instanz erstellt wurden.

## ui.content/pom.xml

Das Modul ui.content verwendet, wie das Modul ui.apps, das FileVault-Paket-Plugin. Das ui.content pom (`<src>/<project>/ui.content/pom.xml`) enthält jedoch eine zusätzliche Konfigurationseigenschaft namens `acHandling` mit dem Wert `merge_preserve`. Dies ist der Fall, weil das Modul ui.content Zugriffssteuerungslisten (ACLs) enthält, die Berechtigungen sind und bestimmen, wer die Vorlagen bearbeiten kann. Damit diese ACLs in AEM importiert werden können, ist die `acHandling` Eigenschaft erforderlich.
