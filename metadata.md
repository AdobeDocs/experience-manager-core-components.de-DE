---
product: Adobe Experience Manager
git-repo: https://github.com/AdobeDocs/experience-manager-cloud-manager.en
index: y
solution-title: Lernen und Support für AEM
solution-hub-url: https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/sites/home.translate.html
getting-started-title: Erste Schritte bei der Entwicklung für AEM
getting-started-url: https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/core-concepts/home.translate.html
tutorials-title: AEM-Tutorials
tutorials-url: https://docs.adobe.com/content/help/en/experience-manager-learn/cloud-service/overview.html
translation-type: ht
source-git-commit: a3085d266baf32649fda528a7f4703e133d03ab7

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

Weitere Informationen zu den Metadaten finden Sie im [internen Authoring-Handbuch.](https://docs.adobe.com/help/en/collaborative-doc-instructions/collaboration-guide/markdown/metadata.html#solution-metadata)
