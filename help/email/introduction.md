---
title: Einführung in E-Mail-Kernkomponenten
description: Erstellen Sie ansprechende E-Mail-Inhalte mithilfe der Flexibilität der E-Mail-Kernkomponenten und stellen Sie sie mit Adobe Campaign bereit.
role: Architect, Developer, Admin, User
exl-id: 0a411f28-bd6a-4bad-b473-6bc27c1d1055
source-git-commit: 33976c0e745ad091a142109f70541f01a31edc5b
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 10%

---


# Einführung in E-Mail-Kernkomponenten {#email-core-components-introduction}

Erstellen Sie ansprechende E-Mail-Inhalte mithilfe der Flexibilität der E-Mail-Kernkomponenten und stellen Sie sie mit Adobe Campaign bereit.

## Übersicht {#overview}

Die E-Mail-Kernkomponenten basieren auf derselben leistungsstarken Grundlage der Kernkomponenten. Sie ermöglichen ein einfaches und flexibles Drag-and-Drop-Authoring von E-Mail-Inhalten, die dann mithilfe von Adobe Campaign an Ihre Audience gesendet werden können.

## Vorteile {#benefits}

E-Mails sind Teil des Markenerlebnisses und der Journey von Kunden. Mit den E-Mail-Kernkomponenten können Ihre Autoren E-Mail-Inhalte aus AEM erstellen, ein konsistentes Branding-Erlebnis bieten und damit die Content-Geschwindigkeit erhöhen.

* Genau wie Authoring-Seiten mit den Kernkomponenten ermöglichen es die E-Mail-Kernkomponenten Autoren, E-Mails ohne technisches Wissen zusammenzustellen und gleichzeitig sicherzustellen, dass sie den Branding-Richtlinien entsprechen.
* Die Funktion zur Wiederverwendung von Assets und Inhalten ermutigt Autoren auch, Branding-Richtlinien zu befolgen und den Inhaltserstellungsprozess zu optimieren.

## Funktionen {#features}

* Die Kernkomponenten der E-Mail basieren auf dem [Kernkomponenten,](/help/introduction.md) und daher auch [Bearbeitbare Vorlagen](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=de) und [Stilsystem.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/features/style-system.html?lang=de)
* Es gibt [zehn für E-Mails optimierte produktionsbereite Komponenten](#components) , um E-Mail-Inhalte zu erstellen.
* Die Kernkomponenten der E-Mail bieten eine erweiterte Personalisierung durch das Einfügen von [Adobe Campaign-Variablen](campaign-variables.md) in den meisten Dialogfeldern.
* Die Flexibilität [Segmentierungskomponente](/help/email/components/segmentation.md) ermöglicht eine erweiterte Segmentierung Ihres Inhalts.
* Die Kernkomponenten der E-Mail bieten dank der [CSS-Stile in Liner,](https://github.com/adobe/aem-core-email-components/wiki/CSS-Styles-Inliner:-Technical-documentation) [das HTML-Attribut inliner,](https://github.com/adobe/aem-core-email-components/wiki/HTML-Inliner) und [HTML sanitizer.](https://github.com/adobe/aem-core-email-components/wiki/HTML-Sanitizing)
* Sie können E-Mail-Inhalte an einer beliebigen Stelle erstellen. `/content`.
* Die E-Mail-Kernkomponenten sind [Open Source.](https://github.com/adobe/aem-core-email-components)

## Voraussetzungen {#requirements}

Die E-Mail-Kernkomponenten haben die folgenden Anforderungen.

| AEM | Adobe Campaign | Kernkomponenten |
|---|---|---|
| AEM 6.5.14.0+<br>On-Premise oder AMS | Adobe Campaign Classic<br>Adobe Campaign Standard | [Version 2.21.2](/help/versions.md)+ |

>[!NOTE]
>
>Da die Adobe Campaign-Integrationen in AEM as a Cloud Service nicht unterstützt werden, werden die E-Mail-Kernkomponenten auch in AEM as a Cloud Service nicht unterstützt.

## Die E-Mail-Komponenten {#components}

Die aktuelle Version der E-Mail-Kernkomponenten enthält die folgenden Komponenten.

* [Seite  ](components/page.md)
* [Container](components/container.md)
* [Titel](components/title.md)
* [Text](components/text.md)
* [Bild](components/image.md)
* [Schaltfläche](components/button.md)
* [Teaser](components/teaser.md)
* [Experience Fragment](components/experience-fragment.md)
* [Inhaltsfragment](components/content-fragment.md)
* [Segmentierung](components/segmentation.md)

## Installation und Verwendung {#installation-usage}

Siehe [Verwenden der E-Mail-Kernkomponenten](using.md) Dokument für Details zur Installation der E-Mail-Kernkomponenten.
