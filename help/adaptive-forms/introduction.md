---
title: Einführung AEM adaptiven Forms-Kernkomponenten
description: Erstellen Sie ansprechende Registrierungserlebnisse (Formulare) mit der Flexibilität der adaptiven Forms-Kernkomponenten und stellen Sie sie mit Adobe Experience Manager bereit.
role: Architect, Developer, Admin, User
source-git-commit: 781cf351ef52cbb56ff33c2674c8af591c81a30e
workflow-type: tm+mt
source-wordcount: '1069'
ht-degree: 14%

---


# Einführung in adaptive Forms-Kernkomponenten {#adaptive-forms-core-components-introduction}

Mithilfe der adaptiven Forms-Kernkomponenten in Adobe Experience Manager können Sie überzeugende Registrierungserlebnisse schaffen, indem Sie die verfügbaren Flexibilität und Anpassungsoptionen nutzen.

## Kernkomponenten  {#overview}

In Adobe Experience Manager (AEM) sind Komponenten die Bausteine, die zum Erstellen von Seiten und Formularen verwendet werden. Sie bieten Autoren eine einfache und leistungsstarke Möglichkeit, Inhalte zu erstellen und zu verwalten und bieten Entwicklern gleichzeitig die Flexibilität und Erweiterbarkeit, die zum Erstellen benutzerdefinierter Komponenten erforderlich sind.

Die Kernkomponenten sind eine Reihe vordefinierter, standardisierter WCM-Komponenten, die die Entwicklungszeit verkürzen und die Wartungskosten für Websites senken. Zu diesen Komponenten gehören Textfelder, Bilder, Videos und mehr. Sie sind flexibel und können einfach an die spezifischen Anforderungen einer Website angepasst werden.

Die Kernkomponenten sind außerdem für responsive Funktionen und unterstützen eine breite Palette von Geräten, einschließlich Desktops, Tablets und Smartphones. Sie halten sich außerdem an die neuesten Web-Standards und Best Practices und machen sie zu einer robusten und zuverlässigen Lösung für die Erstellung von Web-Inhalten.

Darüber hinaus sind die Kernkomponenten so konzipiert, dass sie nahtlos mit anderen Teilen von AEM zusammenarbeiten, sodass Autoren und Entwickler interaktive Formulare mit geringerem Aufwand und weniger Zeit erstellen können.

Insgesamt sind die Kernkomponenten ein wesentliches Tool für die Erstellung und Verwaltung von Web-Inhalten in AEM und bieten eine leistungsstarke und flexible Lösung, die dazu beiträgt, die Entwicklungszeit und die Wartungskosten zu reduzieren und den Besuchern der Website gleichzeitig ein großartiges Benutzererlebnis zu bieten.

In Adobe Experience Manager sind Komponenten die strukturellen Elemente, die den Inhalt der Seiten und Formulare ausmachen, die erstellt werden. Komponenten waren immer ein grundlegendes Element des AEM-Erlebnisses, wodurch die Seiten- und Formularerstellung einfach, aber leistungsstark für den Autor und die Entwicklung von Komponenten flexibel und erweiterbar für den Entwickler war. Die Kernkomponenten sind eine Reihe standardisierter Web Content Management (WCM)-Komponenten, um die Entwicklungszeit zu verkürzen und die Wartungskosten Ihrer Websites zu reduzieren.

## Adaptive Forms-Kernkomponenten

Die adaptiven Forms-Kernkomponenten sind eine Reihe von 24 BEM-kompatiblen Open-Source-Komponenten, die auf der Grundlage der Adobe Experience Manager WCM-Kernkomponenten erstellt wurden. Sie sind speziell für die Erstellung von Adaptive Forms entwickelt worden. Hierbei handelt es sich um Formulare, die sich an Gerät, Browser und Bildschirmgröße des Benutzers anpassen.

Diese Komponenten können verwendet werden, um außergewöhnliche Datenerfassungs- und Registrierungserlebnisse zu schaffen, indem sie eine breite Palette von Formularfeldoptionen bereitstellen, darunter Textfelder, Kontrollkästchen, Dropdownmenüs und mehr. Sie umfassen auch Funktionen wie Validierung, Bedingungslogik und responsives Design, die zum Erstellen benutzerfreundlicher und benutzerfreundlicher Formulare verwendet werden können.

Da es sich bei diesen Komponenten um Open-Source-Komponenten handelt, können Entwickler die Komponenten einfach anpassen und erweitern, um sie an die spezifischen Anforderungen ihrer Organisation anzupassen. Und diese Komponenten basieren auf der BEM-Methode, die sicherstellt, dass sie skalierbar und wartbar sind.

![](assets/sample-adaptive-form.png)

## Funktionen {#features}

|  |  |
|---|---|
| Produktionsbereit | Die adaptiven Forms-Kernkomponenten sind 24 zuverlässige WCM-Komponenten. |
| Cloud-fähig | Verfügbar für  [AEM Forms as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/home.html). |
| Vielseitig | Die Komponenten stellen allgemeine Konzepte dar, mit denen die Forms-Autoren nahezu jedes Layout zusammenstellen können. |
| Konfigurierbar | Vorlagenebene [Content-Richtlinien](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/full-stack/components-templates/templates.html?lang=de#content-policies) definieren, welche Funktionen verwendet werden dürfen oder nicht. |
| Barrierefrei | Sie erfüllen [WCAG 2.1-Standard](https://www.w3.org/TR/WCAG21/), ARIA-Beschriftungen bereitstellen, die Tastaturnavigation unterstützen ([bekannte Probleme](https://github.com/adobe/aem-core-wcm-components/issues?utf8=✓&amp;q=is%3Aissue+is%3Aopen+accessibility+in%3Atitle)) und Text für Hilfstechnologien wie Bildschirmlesehilfen. |
| Themen-fähig | Die Komponenten implementieren das [Stilsystem](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/features/style-system.html?lang=de) und das Markup folgt den [BEM-CSS-Konventionen](http://getbem.com/). |
| Anpassbar | Verschiedene Muster ermöglichen eine einfache Anpassung, von der Anpassung des HTML-Codes bis hin zur Wiederverwendung erweiterter Funktionen. |
| Versionierung | Die [Versionierungsrichtlinie](https://github.com/adobe/aem-core-wcm-components/wiki/Versioning-policies) stellt sicher, dass die Kernkomponenten Ihre Website nicht beschädigen, wenn Funktionen verbessert werden, die sich auf Sie auswirken könnten. |
| Open Source | Wenn etwas nicht so ist, wie es sein sollte, bringen Sie Ihre Verbesserung ein. |

## Vorteile {#benefits}

Datenerfassungserlebnisse sind für die Erstellung und Registrierung von Leads von entscheidender Bedeutung. Die Kernkomponenten von Adaptive Forms bieten eine leistungsstarke Lösung zum Erstellen von Formularen, die für die Datenerfassung optimiert sind. Einige der Gründe für die Verwendung von Kernkomponenten zur Erstellung dieser Erlebnisse sind:

* **Anpassung**: Adaptive Forms-Kernkomponenten ermöglichen es Entwicklern, das Erscheinungsbild und Verhalten von Formularkomponenten wie Textfeldern, Checkboxes und Dropdownmenüs einfach anzupassen, um bestimmte Anforderungen zu erfüllen.

* **Zugänglichkeit**: Adaptive Forms-Kernkomponenten unterstützen Barrierefreiheitsstandards und -richtlinien, z. B.  [WCAG 2.1-Standard](https://www.w3.org/TR/WCAG21/), um sicherzustellen, dass Formulare von Menschen mit Behinderungen verwendet werden können, einschließlich solcher, die Hilfstechnologien wie Bildschirmlesehilfen verwenden.

* **Konsistente Formulare**: Durch die Verwendung der adaptiven Forms-Kernkomponenten können Entwickler Formulare erstellen, die ein einheitliches Erscheinungsbild aufweisen, sodass Benutzer die Formulare leichter verstehen und ausfüllen können. Dies führt zu mehr Interaktion und verbesserter Benutzerfreundlichkeit.

* **WYSIWYG-Editor**: AEM Forms bietet eine benutzerfreundliche Benutzeroberfläche und einen benutzerfreundlichen WYSIWYG-Editor, mit dem Sie diese Komponenten zum Erstellen eines adaptiven Formulars verwenden können. Sie ermöglicht es Formularautoren, Formulare zu erstellen und zu bearbeiten, ohne dass sie wissen müssen, wie sie kodieren. Es enthält auch einen visuellen Regeleditor, mit dem Sie auf einfache Weise regelbasierte Aktionen erstellen und komplexe Logik implementieren können, um das Formularverhalten zu automatisieren, ohne Code schreiben zu müssen.

* **Bedingte Logik**: Adaptive Forms-Kernkomponenten unterstützen die Verwendung von Bedingungslogik. Das bedeutet, dass das Erscheinungsbild oder Verhalten von Formularkomponenten anhand der vom Benutzer eingegebenen Werte geändert werden kann. Beispielsweise können bestimmte Felder je nach Auswahl in anderen Feldern ausgeblendet oder als Pflichtfelder festgelegt werden.

* **Datenvalidierung**: Adaptive Forms-Kernkomponenten bieten integrierte Datenvalidierungsfunktionen, mit denen Entwickler sicherstellen können, dass vom Benutzer eingegebene Daten bestimmte Kriterien wie minimale und maximale Längen, erforderliche Werte und bestimmte Formate erfüllen.

## Voraussetzungen {#requirements}

Die Kernkomponenten von Adaptive Forms haben die folgenden Anforderungen.

| AEM | AEM Forms-Add-on | Kernkomponenten |
|---|---|---|
| AEM as a Cloud Service | Forms – Digitale Registrierung | [Version 2.20.8](/help/versions.md)+ |


## Adaptive Forms-Kernkomponenten {#components}

Die aktuelle Version der adaptiven Forms-Kernkomponenten enthält die folgenden Komponenten.

* Akkordeon
* Schaltfläche
* Kontrollkästchen Gruppe
* Datumsauswahl
* Dropdown-Liste
* Email-input
* Formular-Container
* Dateianhang
* den Namen Fußzeile zu
* Kopfzeile
* Horizontale Registerkarten
* Bild
* Zahleneingabe
* Bedienfeld-Container
* Optionsfeld
* Schaltfläche „Zurücksetzen“
* Senden-Schaltfläche
* Telefoneingabe
* Texteingabe
* Text
* Titel
* Assistent

