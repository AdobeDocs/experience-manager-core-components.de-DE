---
title: Einführung AEM adaptiven Forms-Kernkomponenten
description: Erstellen Sie ansprechende Registrierungserlebnisse (Formulare) mit der Flexibilität der adaptiven Forms-Kernkomponenten und stellen Sie sie mit Adobe Experience Manager bereit.
role: Architect, Developer, Admin, User
source-git-commit: 945e1793ae4e959f83960db46d2de4257916fe32
workflow-type: tm+mt
source-wordcount: '1202'
ht-degree: 12%

---


# Einführung in adaptive Forms-Kernkomponenten {#adaptive-forms-core-components-introduction}

Mithilfe der adaptiven Forms-Kernkomponenten in Adobe Experience Manager können Sie überzeugende Registrierungserlebnisse schaffen, indem Sie die verfügbaren Flexibilität und Anpassungsoptionen nutzen.

## Kernkomponenten  {#overview}

In Adobe Experience Manager (AEM) sind Komponenten die Bausteine, die zum Erstellen von Seiten und Formularen verwendet werden. Sie bieten Autoren eine einfache und leistungsstarke Möglichkeit, Inhalte zu erstellen und zu verwalten und bieten Entwicklern gleichzeitig die Flexibilität und Erweiterbarkeit, die zum Erstellen benutzerdefinierter Komponenten erforderlich sind.

Die sind so konzipiert, dass sie die Entwicklungszeit verkürzen und die Wartungskosten für Websites und Formulare senken, flexibel sein und einfach an die spezifischen Anforderungen einer Website und eines Formulars angepasst werden können.

Die Kernkomponenten sind außerdem für responsive Funktionen und unterstützen eine breite Palette von Geräten, einschließlich Desktops, Tablets und Smartphones. Sie halten sich außerdem an die neuesten Web-Standards und Best Practices und machen sie zu einer robusten und zuverlässigen Lösung für die Erstellung von Web-Inhalten.

Insgesamt sind die Kernkomponenten ein wesentliches Tool für die Erstellung und Verwaltung von Web-Inhalten in AEM und bieten eine leistungsstarke und flexible Lösung, die dazu beiträgt, die Entwicklungszeit und die Wartungskosten zu reduzieren und den Besuchern der Website gleichzeitig ein großartiges Benutzererlebnis zu bieten.

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

Datenerfassungserlebnisse sind für die Erstellung und Registrierung von Leads von entscheidender Bedeutung. Die Kernkomponenten von Adaptive Forms bieten eine leistungsstarke Lösung zum Erstellen von Formularen, die für die Datenerfassung optimiert sind. Einige der Gründe für die Verwendung von Kernkomponenten zum Erstellen dieser Erlebnisse über Foundation-Komponenten:

* **Verfügbarkeit auf GitHub und umfassende Dokumentation**: Die AEM adaptiven Forms-Kernkomponenten sind Open-Source-Komponenten und auf GitHub verfügbar. Darüber hinaus finden Sie eine umfassende Dokumentation. Dies erleichtert es Entwicklern, die Komponenten und ihre Funktionsweise zu verstehen und zu ihrer Entwicklung beizutragen. Die Website aemcomponents.dev ist ebenfalls eine wertvolle Ressource, über die Entwickler die Komponenten in Aktion sehen und auf die detaillierte Dokumentation zugreifen können.

* **BEM-Modell für die Formatierung**: Die Kernkomponenten folgen dem BEM-Modell (Block Element Modifier) für die Formatierung, das eine bewährte und häufig verwendete Methode für die Organisation von CSS ist. Dies erleichtert Entwicklern das Verständnis, wie die Stile organisiert sind und wie sie sie an ihre spezifischen Anforderungen anpassen können.

* **Keine Abhängigkeit von Bibliotheken von Drittanbietern**: Einer der Vorteile der Kernkomponenten besteht darin, dass sie keine Abhängigkeit von JavaScript-Bibliotheken von Drittanbietern haben, einschließlich JQuery und Underscore. Dadurch werden die Komponenten schneller und einfacher und können leichter in eine vorhandene AEM integriert werden.

* **Fokus auf Leistung und Zugänglichkeit**: Die Kernkomponenten werden unter Berücksichtigung von Leistung und Barrierefreiheit erstellt, was sich in ihren hohen Google Lighthouse- und Web-Vitalwerten widerspiegelt. Dies erleichtert Entwicklern das Erstellen barrierefreier und leistungsstarker Webseiten, die in der heutigen digitalen Landschaft immer wichtiger werden.

* **Formularkomponenten in Sites 30-Vorlage und Designs**: Die Kernkomponenten bieten Unterstützung für Formularkomponenten in der Sites 30-Vorlage und den Designs, wodurch Entwickler Formulare in AEM erstellen und anpassen können.

* **Einfacherer Stil**: Die Kernkomponenten sind einfacher zu gestalten als ihre Foundation-Komponenten-Entsprechungen. Der Prozess zur Designerstellung ähnelt Sites, mit der Möglichkeit, dasselbe Design/dieselbe CSS von der übergeordneten Sites-Seite zu übernehmen. Darüber hinaus erleichtert das BEM-Modell für die Formatierung das Verständnis und die Änderung der Stile.

* **Zugänglichkeit**: Adaptive Forms-Kernkomponenten unterstützen Barrierefreiheitsstandards und -richtlinien, z. B.  [WCAG 2.1-Standard](https://www.w3.org/TR/WCAG21/), um sicherzustellen, dass Formulare von Menschen mit Behinderungen verwendet werden können, einschließlich solcher, die Hilfstechnologien wie Bildschirmlesehilfen verwenden.

* **Abstimmung mit AEM Sites**: Die Kernkomponenten sind so konzipiert, dass sie besser mit AEM Sites abgestimmt sind, sodass Sites-Benutzer sie einfacher übernehmen und verwenden können, ohne etwas Neues lernen zu müssen. Die Komponenten verwenden dieselbe Front-End-Pipeline wie Sites, wodurch die Formatierung und Änderung ihres Erscheinungsbilds erleichtert wird. Außerdem wird diese Ausrichtung anhand der folgenden Punkte veranschaulicht:

   * **Inhaltserstellung inline mit dem Seiteneditor**: Die Kernkomponenten verfügen über ein Authoring-Erlebnis, das mit dem Sites-Editor mit Dialogfeldern und anderen Erlebnissen, die dem Seiten-Editor ähneln, inline ist. Dies erleichtert Sites-Benutzern das Erstellen und Verwalten von Formularen im vertrauten Kontext des Sites-Editors.

   * **Inline-Formularbearbeitung im Sites-Editor**: Die Kernkomponenten ermöglichen die Bearbeitung von Inline-Formularen im Sites-Editor, sodass ein Wechsel zwischen Editoren nicht erforderlich ist. Dadurch wird das Authoring-Erlebnis optimiert und die Erstellung und Verwaltung von Formularen vereinfacht.

   * **Vererben von Sites-Funktionen in Forms**: Forms, das auf einer Sites-Seite erstellt wurde, erbt dieselben Funktionen wie Sites. Dies bietet ein nahtloses und integriertes Erlebnis für die Erstellung und Verwaltung von Formularen im Kontext von AEM Sites

   <!--including Multi Site Manager, the ability to use Sites components within a form for static content, support for scheduled publish/unpublish, form translation aligned with Sites translation, versioning, and targeting -->



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

