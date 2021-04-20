---
product: adobe experience manager
solution: Experience Manager Sites
type: Documentation
description: Dokumentation für die Adobe Experience Manager-Kernkomponenten
git-repo: https://git.corp.adobe.com/AdobeDocs/experience-manager-core-components.de-DE
index: y
translation-type: ht
source-git-commit: 290423c39b925ea8cf4077f31a76ecf01167f344
workflow-type: ht
source-wordcount: '113'
ht-degree: 100%

---


# Metadaten für die interne Verwendung

Die Metadaten im GitHub-Authoring-System sind hierarchisch aufgebaut und werden in den folgenden aufsteigend sortierten Präzedenzebenen definiert.

1. metadata.md
1. IHV
1. Artikel

Die in der Datei „metadata.md“ definierten Metadaten gelten für den gesamten Bericht, können jedoch auf der IHV- (ToC) und der Artikelebene überschrieben werden. Das Überschreiben der Metadaten sollte auf der niedrigstmöglichen Ebene erfolgen.

Die Metadaten im Bericht „experience-manager-core-components.en“ sind das erforderliche Minimum.

metadata.md

* `product`
* `git-repo`
* `index: y`
* `solution-title`
* `solution-hub-url`
* `getting-started-title`
* `getting-started-url`
* `tutorials-title`
* `tutorials-url`

IHVs

* `sub-product`
* `user-guide-title`

Artikel

* `title`
* `description`
* `index: n` (nur für ältere Komponentenversionen)

Weitere Informationen zu den Metadaten finden Sie im [internen Authoring-Handbuch.](https://docs.adobe.com/help/de_DE/collaborative-doc-instructions/collaboration-guide/markdown/metadata.html#solution-metadata)
