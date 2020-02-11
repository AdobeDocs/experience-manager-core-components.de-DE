---
title: Entwickeln von Kernkomponenten
description: Die Kernkomponenten bieten leistungsfähige und erweiterbare Basiskomponenten mit umfangreichen Funktionen, kontinuierlicher Bereitstellung, Komponentenversionierung, moderner Implementierung, schlankem Markup und JSON-Export von Inhalten.
translation-type: tm+mt
source-git-commit: 5439f90faef28c72367419bb7429a3a880b65229

---


# Entwickeln von Kernkomponenten{#developing-core-components}

## Überblick {#overview}

Die Kernkomponenten bieten leistungsfähige und erweiterbare Basiskomponenten und ihre Highlights sind:

* Umfangreiche Funktionen
   * [Flexible Konfigurationsoptionen](authoring.md), um zahlreiche Anwendungsfälle abzudecken
   * [Vorkonfigurierbare Funktionen](authoring.md#pre-configuring-core-components), um festzulegen, welche Funktionen Seitenautoren zur Verfügung stehen sollen
* Kontinuierliche Bereitstellung
   * Häufige inkrementelle Verbesserungen bei der Funktionalität
   * Verfügbarkeit des [Quellcodes auf GitHub](https://github.com/adobe/aem-core-wcm-components), damit die Entwickler-Community Feedback abgeben und Beiträge hinzufügen kann
   * Installation durch [das separat veröffentlichte Inhaltspaket](https://github.com/adobe/aem-core-wcm-components/releases), sodass Komponentenaktualisierungen unabhängig von AEM-Aktualisierungen erfolgen
* [Komponentenversionierung](guidelines.md#component-versioning)
   * [Sicherstellung der Kompatibilität innerhalb einer Version](#upgrade-of-core-components), wobei die Komponenten trotzdem weiterentwickelt werden können.
   * Zulassen, dass mehrere Versionen einer Komponente in derselben Umgebung koexistieren können
* Moderne Implementierung
   * Markup definiert in [HTML Template Language](https://docs.adobe.com/content/help/en/experience-manager-htl/using/overview.html) (HTL)
   * Mit [Sling-Modellen](https://sling.apache.org/documentation/bundles/models.html) implementierte Inhaltsmodelllogik
* Schlankes Markup
   * Folgt der [Block Element Modifier](https://getbem.com/) (BEM)-Notation ab Version 2.0.0
      * Frühere Versionen folgen den [Bootstrap](https://getbootstrap.com/css/)-Benennungskonventionen
   * Erstellt entsprechend den [Richtlinien für Eingabehilfen](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html)
   * Kann für responsive und mobile Sites eingesetzt werden.
* Möglichkeit, das Inhaltsmodell für Headless-CMS-Anwendungsfälle als JSON zu serialisieren
* Barrierefrei
   * Konform mit dem [WCAG 2.0 AA-Standard](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html)

>[!CAUTION]
>
>Kernkomponenten erfordern AEM 6.3 oder höher und Java 8 sowie die Verwendung [bearbeitbarer Vorlagen](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)
>
>Kernkomponenten funktionieren weder mit der klassischen Benutzeroberfläche noch mit statischen Vorlagen.

## Überblick über die Gems-Sitzung {#gems-session-overview}

Um eine Einführung in die Kernkomponenten, die angebotenen Funktionen und ihre Nutzung in AEM zu erhalten, sehen Sie sich die AEM-Gems-Sitzung [AEM-Kernkomponenten](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/AEM-Core-Components.html)

[Gems zu Adobe Experience Manager](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/aem-index.html) ist eine Reihe technischer Vertiefungen, die von Adobe-Experten angeboten werden. Diese Reihe ergänzt die Produktdokumentation und alle anderen technischen Kanäle und ermöglicht es Entwicklern, in Kontakt zu treten und ein bestimmtes Thema zu vertiefen.

## WKND-Entwickler-Tutorial {#wknd-developer-tutorial}

Beginnen Sie mit der Entwicklung von AEM Sites mit Kernkomponenten, indem Sie [dieses Schritt-für-Schritt-Tutorial](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)

## AEM-Projektarchetyp {#aem-project-archetype}

[Der AEM-Projektarchiv](overview.md) erstellt ein Adobe Experience Manager-Minimalprojekt als Ausgangspunkt für Ihre eigenen Projekte, einschließlich eines Beispiels für benutzerdefinierte HTML-Komponenten mit SlingModels für die Logik und ordnungsgemäße Implementierung der Core-Komponenten mit dem empfohlenen Proxymuster.

## Über GitHub bereitgestellt {#delivered-over-github}

Die Kernkomponenten werden in GitHub entwickelt und durch GitHub bereitgestellt.

CODE AUF GITHUB

Den Code dieser Seite finden Sie auf GitHub

* [Öffnen Sie das Projekt aem-core-wcm-components auf GitHub](https://github.com/adobe/aem-core-wcm-components)
* Laden Sie das Projekt als [ZIP-Datei](https://github.com/adobe/aem-core-wcm-components/archive/master.zip) herunter

Öffnen Sie die Dokumentationsseite [Verwendung von Kernkomponenten](using.md), um zu erfahren, wie Sie damit in Ihrem Projekt beginnen können.

Die Verwendung der Kernkomponenten auf GitHub ermöglicht es Ihnen, häufige Aktualisierungen durchzuführen und das Feedback der AEM-Entwickler-Community zu verfolgen. Dies sollte außerdem Kunden und Partnern dabei helfen, ähnliche Muster beim Erstellen benutzerdefinierter Komponenten zu befolgen.

>[!NOTE]
>
>Um über die neuesten Änderungen an den Kernkomponenten auf dem Laufenden zu bleiben, können Sie sich das [Kernkomponenten-Repository](https://github.com/adobe/aem-core-wcm-components) auf GitHub ansehen.

## Komponentenbibliothek

Sehen Sie sich die [Komponentenbibliothek](https://adobe.com/go/aem_cmp_library) an, in der die aktuelle Version der Kernkomponenten präsentiert wird und Beispiele für deren Nutzung enthalten sind.

### Standardmäßige Kernkomponenten {#out-of-the-box}

Die Hauptkomponenten werden je nach Ausführung von AEM möglicherweise nicht automatisch installiert.

#### AEM als Cloud-Dienst {#aem-cloud-service}

Obwohl die Hauptkomponenten vollständig mit [AEM als Cloud-Dienst](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html)kompatibel sind, müssen die Hauptkomponenten manuell installiert werden und sind nicht standardmäßig verfügbar.

#### AEM On-Premise {#on-premise}

In on-premise installations, the Core Components are visible in the Quickstart when the sample content is present, because the [We.Retail reference site](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html) uses them. However, when running in production (in `nosamplecontent` runmode, without sample content enabled), the core components won&#39;t be present anymore and must be installed on the AEM instance.

>[!NOTE]
>
>In on-premise production environments, always run the Quickstart in `nosamplecontent` runmode. Um die Kernkomponenten im Ausführungsmodus `nosamplecontent` zu verwenden, befolgen Sie die Anweisungen in der Dokumentation zur [Verwendung von Kernkomponenten](using.md).

## Technische Funktionen {#technical-capabilities}

In der folgenden Tabelle finden Sie einen Überblick über die Unterschiede zwischen Kernkomponenten und Foundation-Komponenten.

Einzelheiten zu ihren Authoring-Fähigkeiten und Optionen zu ihrer Vorkonfiguration [finden Sie auf der entsprechenden Authoring-Seite](authoring.md).

| **Funktion** | **Kernkomponente** | **Foundation-Komponente** |
|-----|---|---|
| Logikimplementierung | Java POJOs mit Anmerkungen zu [Sling-Modellen](https://sling.apache.org/documentation/bundles/models.html) | JSP-Code |
| Markup-Definition | [HTML Template Language](https://docs.adobe.com/content/help/en/experience-manager-htl/using/overview.html) (HTL)-Syntax | JSP-Code |
| XSS-Bereinigung | Automatisiert durch HTL | Hauptsächlich manuell |
| CSS-Klassen-Benennung | Standardisierte Benennungskonvention basierend auf der [Block Element Modifier](https://getbem.com/) (BEM)-Notation (ab Version 2.0.0) | Benutzerdefinierte Schemata |
| Dialogfeld-Definition | [Coral 3](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/reference-materials/coral-ui/coralui3/index.html) | Coral 2 + Klassische Benutzeroberfläche |
| JSON-Ausgabe | [Sling Model Exporter mit Jackson-Serialisierung](https://sling.apache.org/documentation/bundles/models.html#exporter-framework-since-130) | Standard-Sling-Servlet |
| Versionierung | [Für das Modell und die HTL](guidelines.md) | Keine |
| Testen | Unit-Tests und Integrationstests | Integrationstests |
| Bereitstellung | [Über öffentliches GitHub](https://github.com/adobe/aem-core-wcm-components) | Über Quickstart |
| Lizenz | [Apache-Lizenz](https://www.apache.org/licenses/LICENSE-2.0) | Adobe-geschützt |
| Beitrag | Über Pull-Anfrage | Nicht möglich |
| Barrierefreiheit | Vollständig konform mit dem [WCAG 2.0 AA-Standard](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html | Nur teilweise konform mit dem [WCAG 2.0 AA-Standard](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html) |

## Komponentenliste {#component-list}

In der folgenden Tabelle sind die verfügbaren Kernkomponenten mit Links zu ihrer API aufgeführt und es wird angegeben, welche Foundation-Komponenten sie ersetzen.

| Kernkomponente | Beschreibung | Ersetzte Foundation-Komponente(n) |
|---|---|---|
| [Seite](https://adobe.com/go/aem_cmp_tech_page_v2) | Responsive Seite, die mit dem Vorlageneditor arbeitet | `/libs/foundation/components/page /libs/wcm/foundation/components/page` |
| [Breadcrumb](https://adobe.com/go/aem_cmp_tech_breadcrumb_v2) | Navigation der Seitenhierarchie | `/libs/foundation/components/breadcrumb` |
| [Titel](https://adobe.com/go/aem_cmp_tech_title_v2) | H1-H6-Titel | `/libs/foundation/components/title /libs/wcm/foundation/components/title` |
| [Text](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/text/v2/text) | Rich-Text | `/libs/foundation/components/text /libs/foundation/components/table /libs/wcm/foundation/components/text` |
| [Bild](https://adobe.com/go/aem_cmp_tech_image_v2) | Intelligentes und entspanntes Laden der optimalen Wiedergabegröße | `/libs/foundation/components/image /libs/foundation/components/adaptiveimage /libs/foundation/components/logo /libs/foundation/components/mobileimage  /libs/foundation/components/mobilelogo /libs/wcm/foundation/components/image` |
| [Liste](https://adobe.com/go/aem_cmp_tech_list_v2) | Liste der Seiten | `/libs/foundation/components/list /libs/foundation/components/mobilelist /libs/wcm/foundation/components/list` |
| [Freigabe in Social Media](https://adobe.com/go/aem_cmp_tech_sharing_v1) | Widget zum Teilen auf Facebook und Pinterest | `-` |
| [Formular-Container](https://adobe.com/go/aem_cmp_tech_form_container_v2) | Responsives Formular-Absatzsystem | `/libs/foundation/components/form/start /libs/foundation/components/form/end` |
| [Formulartext](https://adobe.com/go/aem_cmp_tech_form_text_v2) | Texteingabefeld | `/libs/foundation/components/form/text /libs/foundation/components/form/password` |
| [Formularoptionen](https://adobe.com/go/aem_cmp_tech_form_options_v2) | Eingabefeld für mehrere Optionen | `/libs/foundation/components/form/checkbox /libs/foundation/components/form/radio /libs/foundation/components/form/dropdown` |
| [Ausgeblendetes Formular](https://adobe.com/go/aem_cmp_tech_form_hidden_v2) | Ausgeblendetes Eingabefeld | `/libs/foundation/components/form/hidden` |
| [Formularschaltfläche](https://adobe.com/go/aem_cmp_tech_form_button_v2) | Schaltfläche zum Absenden oder benutzerdefinierte Schaltfläche | `/libs/foundation/components/form/submit` |
| [Navigation](https://adobe.com/go/aem_cmp_tech_navigation_v1) | Eine Site-Navigationskomponente, die die verschachtelte Seitenhierarchie auflistet | `/libs/foundation/components/topnav /libs/foundation/components/mobiletopnav` |
| [Sprachnavigation](https://adobe.com/go/aem_cmp_tech_langnav_v1) | Ein Umschalter zwischen Sprachen und Ländern, der die globale Sprachstruktur auflistet | `-` |
| [Schnellsuche](https://adobe.com/go/aem_cmp_tech_search_v1) | Eine Suchkomponente, die die Ergebnisse als ersetzende Vorschläge in einem Dropdown-Menü anzeigt | `/libs/foundation/components/search` |
| [Teaser](https://adobe.com/go/aem_cmp_tech_teaser_v1) | Ermöglicht es dem Inhaltsautor, mühelos einen Teaser für weitere Inhalte zu erstellen, indem er ein Bild, einen Titel oder Rich-Text verwendet und Links zu weiteren Inhalten oder anderen Aktionen erstellt | `-` |
| [Registerkarten](https://adobe.com/go/aem_cmp_tech_tabs_v1) | Ermöglicht es dem Inhaltsautor, Seiteninhalte innerhalb mehrerer Registerkarten zu organisieren | `-` |
| [Karussell](https://adobe.com/go/aem_cmp_tech_carousel_v1) | Ermöglicht es dem Inhaltsautor, Inhalte in einem drehbaren Karussell der Folien zu organisieren | `/libs/foundation/components/carousel` |
| [Inhaltsfragment](https://adobe.com/go/aem_cmp_tech_cf_v1) | Ermöglicht die Anzeige eines Inhaltsfragments | `-` |
| [Inhaltsfragmentliste](https://adobe.com/go/aem_cmp_tech_cflist_v1) | Ermöglicht die Anzeige einer Liste mit Inhaltsfragmenten | `-` |
| [Trennzeichen](https://adobe.com/go/aem_cmp_tech_separator_v1) | Trennt Inhalt auf einer Seite | `-` |
| [Akkordeon](https://adobe.com/go/aem_cmp_tech_accordion_v1) | Organisieren von Inhalts-Bedienfeldern in einem ausblendbaren Akkordeon | `-` |
| [Container](https://adobe.com/go/aem_cmp_tech_container_v1) | Organisieren von Komponenten in einem Container | `-` |
| [Schaltfläche](https://adobe.com/go/aem_cmp_tech_button_v1) | Erstellen einer Schaltfläche auf einer Seite | `-` |
| [Download](https://adobe.com/go/aem_cmp_tech_download_v1) | Hinzufügen eines herunterladbaren Assets zu einer Seite | `-` |
| [Experience Fragment](https://adobe.com/go/aem_cmp_tech_xf_v1) | Hinzufügen eines Experience Fragment zu einer Seite | `/libs/cq/experience-fragments/editor/components/experiencefragment` |
| [Einbetten](https://adobe.com/go/aem_cmp_tech_embed_v1) | Einbetten einer externen Ressource in eine Seite | - |

### Künftige Komponenten {#upcoming-components}

Einen Überblick über geplante Kernkomponenten finden Sie im [Projekt-Wiki auf GitHub](https://github.com/adobe/aem-core-wcm-components/wiki/home).

## Aktualisierung der Kernkomponenten {#upgrade-of-core-components}

Ein Vorteil versionierter Komponenten besteht darin, dass die Migration auf eine neue AEM-Version von der Migration auf neue Komponentenversionen getrennt werden kann. Wenn neue Komponentenversionen verfügbar sind, wird außerdem die einzelne Migration jeder Komponente zur neuen Version ermöglicht.

Die Migration zu einer neuen AEM-Version wirkt sich nicht auf die Funktionsweise der Kernkomponenten aus, sofern ihre Versionen auch die neue AEM-Version unterstützen, auf die migriert wird. An den Kernkomponenten vorgenommene Anpassungen sollten ebenfalls nicht beeinträchtigt werden, sofern sie keine [veralteten oder entfernten](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/release-notes/deprecated-removed-features.html) APIs verwenden.

Migrationen auf neue Versionen der Kernkomponenten wirken sich nicht auf die Funktionsweise der Komponente aus, aber es können ggf. neue Funktionen für Seitenautoren eingeführt werden, was möglicherweise einige Konfigurationen durch einen Vorlageneditor erfordert, falls das Standardverhalten nicht gewünscht wird. Anpassungen müssen jedoch ggf. angepasst werden. Weitere Informationen finden Sie auf der Seite [Anpassen von Kernkomponenten](customizing.md#upgrade-compatibility-of-customizations).

## Wann sollten die Kernkomponenten verwendet werden? {#when-to-use-the-core-components}

Da die Kernkomponenten völlig neu sind und mehrere Vorteile bieten, wird empfohlen, sie für neue AEM-Projekte zu verwenden. Bei vorhandenen Projekten sollte eine Migration Teil einer größeren Projektaufgabe sein, z. B. ein Rebranding oder eine Gesamtrefaktorierung.

Daher bietet Adobe folgende Empfehlungen:

* **Neue Projekte**
Neue Projekte sollten immer versuchen, Kernkomponenten zu verwenden. Wenn Kernkomponenten nicht direkt oder [erweitert](customizing.md) verwendet werden können, um die Projektanforderungen zu erfüllen, erstellen Sie eine benutzerdefinierte Komponente gemäß der Komponentenarchitektur, die in den Kernkomponenten festgelegt ist. Vermeiden Sie die Verwendung der [Foundation-Komponenten](developing.md), sofern möglich.
* **Existierende Projekte**
Empfohlen wird, weiterhin die [Foundation-Komponenten](developing.md) zu verwenden, es sei denn, es ist eine Refaktorierung von Sites oder Komponenten geplant.\
   Da sie sehr häufig von den meisten vorhandenen Projekten verwendet werden, werden die Foundation-Komponenten [weiterhin unterstützt](developing.md).
* **Neue benutzerdefinierte Komponenten**
Überprüfen Sie, ob eine vorhandene [Kernkomponente angepasst werden kann](customizing.md).\
   Wenn nicht, wird empfohlen, eine neue benutzerdefinierte Komponente zu erstellen, die den [Komponentenrichtlinien](guidelines.md) folgt.
* **Vorhandene benutzerdefinierte Komponenten**
Wenn Ihre Komponenten erwartungsgemäß funktionieren, behalten Sie sie unverändert bei.\
   Falls nicht, siehe oben „Neue benutzerdefinierte Komponenten“.

## Migration zu den Kernkomponenten

Jedes neue Projekt sollte mit Kernkomponenten implementiert werden. Bestehende Projekte verfügen jedoch meist über umfassende Implementierungen der Foundation-Komponenten.

Eine größere Arbeit an einem vorhandenen Projekt (z. B. ein Rebranding oder eine Gesamtrefaktorierung) bietet oft eine Möglichkeit, zu den Kernkomponenten zu migrieren. Um diese Migration zu erleichtern, stellt Adobe eine Reihe von Migrationswerkzeugen bereit, um die Akzeptanz der Kernkomponenten und der neuesten AEM-Technologie zu fördern.

[Die AEM-Modernisierungs-Tools](http://opensource.adobe.com/aem-modernize-tools/) ermöglichen eine einfache Konvertierung von:

* Statischen Vorlagen in bearbeitbare Vorlagen
* Designkonfigurationen in Richtlinien
* Foundation-Komponenten in Kernkomponenten
* Klassische Benutzeroberfläche in Touch-optimierte Benutzeroberfläche

Weitere Informationen zur Verwendung dieser Werkzeuge finden Sie [in der entsprechenden Dokumentation](http://opensource.adobe.com/aem-modernize-tools/).

>[!NOTE]
>
>Die AEM-Modernisierung-Tools werden von der Community gesammelt, Adobe bietet keinerlei Unterstützung oder Garantie dafür.

## Kernkomponentenunterstützung {#core-component-support}

Kernkomponenten sind ein integraler Bestandteil von AEM und werden ohne Mängelgewähr unterstützt, zu den gleichen Bedingungen und Konditionen, als ob sie im Rahmen des Quickstarts geliefert würden.

Wie andere AEM-Produktmerkmale lautet die allgemeine Regel: Komponenten werden zunächst als veraltet angekündigt und frühestens in der folgenden AEM-Version entfernt. Dadurch erhalten Kunden mindestens einen Versionszyklus, um zur neuen Version der Komponente zu wechseln, bevor deren Unterstützung eingestellt wird.

Die Version jeder Komponente gibt eindeutig die AEM-Versionen an, die sie unterstützt. Wenn der Support für eine Version von AEM eingestellt wird, gilt das auch für die Unterstützung der Kernkomponenten für diese Version von AEM.

Weitere Informationen zur Unterstützung von Komponentenanpassungen finden Sie auf der Seite [Anpassen von Kernkomponenten](customizing.md).

## Unterstützung von Foundation-Komponenten {#foundation-component-support}

Da die Foundation-Komponenten über viele AEM-Versionen hinweg als Grundlage für so viele Projekte gedient haben, werden sie in absehbarer Zukunft weiterhin unterstützt.

Der Entwicklungsschwerpunkt von Adobe wurde jedoch auf die Kernkomponenten verschoben, und neue Funktionen werden zu ihnen hinzugefügt, während [fast alle Foundation-Komponenten mit AEM 6.5 als veraltet gelten](https://docs.adobe.com/content/help/en/experience-manager-65/authoring/siteandpage/default-components-foundation.html) und jetzt nur noch Fehlerkorrekturen an den Foundation-Komponenten vorgenommen werden.

**Lesen Sie als Nächstes:**

* [Verwenden von Kernkomponenten](using.md) - Starten Sie mit Kernkomponenten in Ihrem eigenen Projekt.
* [Komponentenrichtlinien](guidelines.md) - Lernen Sie die Implementierungsmuster der Kernkomponenten kennen.
