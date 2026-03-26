---
product: adobe experience manager
solution: Experience Manager, Experience Manager Sites
landing-page-name: experience-manager
landing-page-breadcrumb-title: AEM
type: Documentation
description: Dokumentation für die Adobe Experience Manager-Kernkomponenten
git-repo: https://github.com/AdobeDocs/experience-manager-core-components.de-DE
index: true
recommendations: noDisplay
source-git-commit: 1975e060e8db5526518dcf6fc722e3623c47dda6
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 1%

---


# Metadaten für die interne Verwendung

Metadaten im GitHub-Authoring-System sind hierarchisch und werden in den folgenden zunehmenden Präzedenzfällen definiert.

1. metadata.md
1. toC
1. Artikel

Metadaten, die in der Datei „metadata.md“ definiert sind, gelten für das gesamte Repository, können jedoch auf der Inhaltsverzeichnis- und Artikelebene überschrieben werden. Jede Überschreibung der Metadaten sollte auf der niedrigstmöglichen Ebene erfolgen.

Die Metadaten im Repository „experience-manager-core-components.de“ sind das erforderliche Minimum.

metadata.md

* `product`
* `git-repo`
* `index: true`
* `solution-title`
* `solution-hub-url`
* `getting-started-title`
* `getting-started-url`
* `tutorials-title`
* `tutorials-url`

toCS

* `sub-product`
* `user-guide-title`

Artikel

* `title`
* `description`
* `index: false` (nur für frühere Versionen von Komponenten)

Weitere Informationen zu den Metadaten finden Sie im [internen Authoring-Handbuch.](https://experienceleague.adobe.com/docs/authoring-guide-exl/using/authoring/features/metadata.html#solution)
