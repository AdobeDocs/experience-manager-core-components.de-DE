---
title: 'Einführung in E-Mail-Kernkomponenten '
description: Erstellen Sie ansprechende E-Mail-Inhalte unter Verwendung der flexiblen E-Mail-Kernkomponenten und versenden Sie sie mit Adobe Campaign.
role: Architect, Developer, Admin, User
exl-id: 0a411f28-bd6a-4bad-b473-6bc27c1d1055
source-git-commit: 33976c0e745ad091a142109f70541f01a31edc5b
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 99%

---


# Einführung in E-Mail-Kernkomponenten  {#email-core-components-introduction}

Erstellen Sie ansprechende E-Mail-Inhalte unter Verwendung der flexiblen E-Mail-Kernkomponenten und versenden Sie sie mit Adobe Campaign.

## Übersicht {#overview}

Die E-Mail-Kernkomponenten basieren auf derselben leistungsstarken Grundlage wie die Kernkomponenten. Sie ermöglichen eine einfache und flexible Drag-and-Drop-Erstellung von E-Mail-Inhalten, die dann mit Adobe Campaign an Ihre Zielgruppe gesendet werden können.

## Vorteile {#benefits}

E-Mails sind Teil des Markenerlebnisses und der Customer Journey. Mit den E-Mail-Kernkomponenten können Ihre Autoren bzw. Autorinnen E-Mail-Inhalte in AEM erstellen, ein konsistentes Branding-Erlebnis bieten und dadurch die Erstellung von Content beschleunigen.

* Genau wie bei der Seitenerstellung mit den Kernkomponenten können Autoren bzw. Autorinnen auch mit den E-Mail-Kernkomponenten E-Mails ohne technisches Wissen zusammenstellen und gleichzeitig sicherstellen, dass sie den Branding-Richtlinien folgen.
* Die Möglichkeit, Assets und Inhalte wiederzuverwenden, verbessert die Fähigkeit von Autoren bzw. Autorinnen, Branding-Richtlinien zu folgen und den Inhaltserstellungsprozess zu optimieren.

## Funktionen {#features}

* Die E-Mail-Kernkomponenten basieren auf den [Kernkomponenten](/help/introduction.md) und unterstützen daher auch [bearbeitbare Vorlagen](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=de) und das [Stilsystem](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/features/style-system.html?lang=de).
* Es gibt [zehn für E-Mails optimierte produktionsbereite Komponenten](#components), um E-Mail-Inhalte zu erstellen.
* Die E-Mail-Kernkomponenten bieten die Möglichkeit zur erweiterten Personalisierung, da in den meisten Dialogfeldern [Adobe Campaign-Variablen](campaign-variables.md) eingefügt werden.
* Die flexible [Segmentierungskomponente](/help/email/components/segmentation.md) ermöglicht eine erweiterte Segmentierung Ihres Inhalts.
* Die E-Mail-Kernkomponenten bieten dank [CSS Styles Inliner](https://github.com/adobe/aem-core-email-components/wiki/CSS-Styles-Inliner:-Technical-documentation), [HTML Attribute Inliner](https://github.com/adobe/aem-core-email-components/wiki/HTML-Inliner) und [HTML Sanitizer](https://github.com/adobe/aem-core-email-components/wiki/HTML-Sanitizing) eine für E-Mail optimierte HTML-Ausgabe.
* Sie können E-Mail-Inhalte an einer beliebigen Stelle unter `/content` erstellen.
* Die E-Mail-Kernkomponenten sind [Open Source](https://github.com/adobe/aem-core-email-components).

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

Siehe Dokument [Verwenden von E-Mail-Kernkomponenten](using.md) für Details zur Installation der E-Mail-Kernkomponenten.
