---
title: Entwicklung Kernkomponenten
seo-title: Entwicklung Kernkomponenten
description: Die Kernkomponenten bieten robuste und erweiterbare Basiskomponenten, die Funktionen, die kontinuierliche Bereitstellung, die Versionierung von Komponenten, die moderne Implementierung, die automatische Markierung und den JSON-Export von Inhalten bieten.
seo-description: Die Kernkomponenten bieten robuste und erweiterbare Basiskomponenten, die Funktionen, die kontinuierliche Bereitstellung, die Versionierung von Komponenten, die moderne Implementierung, die automatische Markierung und den JSON-Export von Inhalten bieten.
uuid: 88569 da 2-9 bc 8-4 e 20-9 a 71-e 5816 ace 51 ce
contentOwner: Benutzer
content-type: Referenz
topic-tags: wird entwickelt
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-new
discoiquuid: 157 a 2 ec 3-9 fca -4 path -977 a-d 93013 eeb 218
translation-type: tm+mt
source-git-commit: 632d6abb1f13667cc0457152268d50af3bfabfc4

---


# Entwicklung Kernkomponenten{#developing-core-components}

## Überblick {#overview}

Die Kernkomponenten bieten stabile und erweiterbare Basiskomponenten und ihre Highlights sind:

* Umfangreiche Funktionen
   * [Flexible Konfigurationsoptionen](authoring.md) für zahlreiche Anwendungsfälle
   * [Vorkonfigurierbare Funktionen](authoring.md#pre-configuring-core-components) zur Definition der verfügbaren Funktionen für Seitenautoren
* Kontinuierliche Bereitstellung
   * Verbesserungen bei der häufigen inkrementellen Funktionalität
   * Verfügbarkeit des [Quellcodes auf github](https://github.com/adobe/aem-core-wcm-components) , damit die Entwickler-Community Feedback abgeben und Beiträge einbringen kann
   * Installation mit [separat veröffentlichten Inhaltspaketen](https://github.com/adobe/aem-core-wcm-components/releases) für Komponentenupgrades, die unabhängig von AEM-Upgrades erfolgen
* [Komponentenversionierung](guidelines.md#component-versioning)
   * [Stellen Sie sicher, dass die Kompatibilität innerhalb einer Version erfolgt](#upgrade-of-core-components), wobei die Komponenten sich trotzdem entwickeln lassen können.
   * Zulassen, dass mehrere Versionen einer Komponente in derselben Umgebung vorhanden sind
* Moderne Implementierung
   * Markup, definiert in [HTML-Vorlagensprache](https://helpx.adobe.com/experience-manager/htl/using/overview.html) (HTL)
   * Mit [Sling Models implementierte Inhaltsmodelllogik](https://sling.apache.org/documentation/bundles/models.html)
* Schlankes Markup
   * BEM- [Notation (Block Element Modifier)](https://getbem.com/) seit Version 2.0.0
      * Frühere [Bootstrap](https://getbootstrap.com/css/) -Benennungskonventionen in früheren Versionen
   * Richtlinien [für Barrierefreiheit](https://helpx.adobe.com/experience-manager/6-5/managing/using/web-accessibility.html)
   * Verwendung für responsive und mobile Sites
* Funktion zur Serialisierung als JSON im Inhaltsmodell für CMS-Verwendungen ohne Zwischenspeicher
* Accessible
   * Konform mit [dem WCAG 2.0 AA-Standard](https://helpx.adobe.com/experience-manager/6-5/managing/using/web-accessibility.html)

>[!CAUTION]
>
>Core-Komponenten erfordern AEM 6.3 oder höher und Java 8 und erfordern die Verwendung [von bearbeitbaren Vorlagen.](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html)
>
>Core-Komponenten funktionieren nicht mit der klassischen Benutzeroberfläche und statischen Vorlagen.

## Gems Session Overview {#gems-session-overview}

Um eine Einführung in die Kernkomponenten, die angebotenen Funktionen und die Nutzung in AEM zu erhalten, sehen Sie sich die AEM Gems Session [AEM Core Components an.](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/AEM-Core-Components.html)

[Gems on Adobe Experience Manager](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/aem-index.html) ist eine Reihe von technischen Tiefstellungen von Adobe-Experten. Diese Reihe ergänzt die Produktdokumentation und alle anderen technischen Kanäle und ermöglicht es Entwicklern, Kontakt zu erhalten und ein bestimmtes Thema tief zu betrachten.

## WKND Developer Tutorial {#wknd-developer-tutorial}

Beginnen Sie mit der Entwicklung von AEM-Sites mit Kernkomponenten, indem Sie diese [schrittweise Übung befolgen.](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/getting-started.html)

## Über github bereitgestellt {#delivered-over-github}

Die Kernkomponenten werden in github entwickelt und bereitgestellt.

CODE AUF GITHUB

Den Code dieser Seite finden Sie auf GitHub

* [Projekt mit AEM-Core-wcm-components auf github öffnen](https://github.com/adobe/aem-core-wcm-components)
* Herunterladen des Projekts als [ZIP-Datei](https://github.com/adobe/aem-core-wcm-components/archive/master.zip)

Weitere Informationen [zur ersten Schritte mit dem Projekt finden Sie auf der](using.md) Dokumentation zur Kernkomponenten.

Die Verwendung der Kernkomponenten auf github ermöglicht es Ihnen, häufige Aktualisierungen durchzuführen und das Feedback der AEM-Entwicklercommunity zu überwachen. Dies sollte Kunden und Partnern dabei helfen, ähnliche Muster beim Erstellen benutzerdefinierter Komponenten zu befolgen.

>[!NOTE]
>
>Um aktuellste Änderungen an den Hauptkomponenten zu erhalten, können Sie das Repository [Kernkomponenten](https://github.com/adobe/aem-core-wcm-components) auf github ansehen.

## Komponentenbibliothek

Sehen Sie sich die [Komponentenbibliothek an](http://opensource.adobe.com/aem-core-wcm-components/library.html), in der die aktuelle Version der Kernkomponenten präsentiert wird, und zeigt Beispiele ihrer Nutzung an.

### Beispielinhaltsausführungsmodus {#sample-content-run-mode}

Die Kernkomponenten sind im Quickstart sichtbar, wenn der Beispielinhalt vorhanden ist, da [die Referenz-Website sie](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html) verwendet. Wenn jedoch die Produktion in der Produktion ausgeführt wird (im `nosamplecontent` Laufmodus ohne Beispielleistung), werden die Kernkomponenten nicht mehr angezeigt und müssen vom Entwicklungs- und/oder Betriebsteam in den AEM-Instanzen installiert werden.

>[!NOTE]
>
>Führen Sie in Produktionsumgebungen immer den Schnellstart im `nosamplecontent` Laufwerkmodus aus. To use the Core Components in `nosamplecontent` runmode, follow the instructions of the [Using Core Components](using.md) documentation page.

## Technische Funktionen {#technical-capabilities}

In der folgenden Tabelle finden Sie einen Überblick über die Unterschiede zwischen Kernkomponenten und Foundation-Komponenten.

Einzelheiten zu den Authoring-Funktionen und Optionen, die sie vorkonfigurierbar [](authoring.md)sind, finden Sie in der Authoring-Seite.

| **Funktion** | **Kernkomponente** | **Foundation Component** |
|-----|---|---|
| Logikimplementierung | Java-pojos mit [Sling Model](https://sling.apache.org/documentation/bundles/models.html) -Anmerkungen | JSP-Code |
| Markierungsdefinition | [Syntax für HTML-Vorlagensprache](https://helpx.adobe.com/experience-manager/htl/user-guide.html) (HTL) | JSP-Code |
| XSS-Bereinigung | Automatisiert nach HTL | Hauptsächlich manuell |
| CSS-Klassen benennen | Standardisierte Benennungskonvention basierend auf [dem Block-Element-Modifikator](https://getbem.com/) (BEM)-Notation (ab Version 2.0.0) | Benutzerdefinierte Schemas |
| Dialogdefinition | [Coral 3](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/reference-materials/coral-ui/coralui3/index.html) | Coral 2 + Klassische Benutzeroberfläche |
| JSON-Ausgabe | [Sling Model Exporter with Jackson serialization](https://sling.apache.org/documentation/bundles/models.html#exporter-framework-since-130) | Standard-Sling-Servlet |
| Versionierung | [Für das Modell und die HTL](guidelines.md) | Keine |
| Testen | Unit-Tests und Integrationstests | Integrationstests |
| Bereitstellung | [Über öffentliche github](https://github.com/adobe/aem-core-wcm-components) | Über Quickstart |
| Lizenz | [Apache-Lizenz](https://www.apache.org/licenses/LICENSE-2.0) | Eigentum von Adobe |
| Beitrag | Über Pull-Anfrage | Nicht möglich |
| Barrierefreiheit | Vollständig konform mit [dem WCAG 2.0 AA-Standard](https://helpx.adobe.com/experience-manager/6-5/managing/using/web-accessibility.html) | Nur teilweise konform mit [dem WCAG 2.0 AA-Standard](https://helpx.adobe.com/experience-manager/6-5/managing/using/web-accessibility.html) |

## Komponentenliste {#component-list}

In der folgenden Tabelle sind die verfügbaren Kernkomponenten aufgeführt, Links zu ihrer API verknüpft und es wird angegeben, welche Foundation-Komponenten sie ersetzen.

| Kernkomponente | Beschreibung | Foundation Component (s) ersetzt |
|---|---|---|
| [Page](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/page/v2/page) | Reaktionsfähige Seite mit Vorlageneditor | `/libs/foundation/components/page /libs/wcm/foundation/components/page` |
| [Breadcrumb](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/breadcrumb/v2/breadcrumb) | Navigation der Seitenhierarchie | `/libs/foundation/components/breadcrumb` |
| [Titel](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/title/v2/title) | H 1-H 6-Titel | `/libs/foundation/components/title /libs/wcm/foundation/components/title` |
| [Text](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/text/v2/text) | Rich Text | `/libs/foundation/components/text /libs/foundation/components/table /libs/wcm/foundation/components/text` |
| [Bild](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/image/v2/image) | Intelligentes und verzögertes Laden der optimalen Darstellungsgröße | `/libs/foundation/components/image /libs/foundation/components/adaptiveimage /libs/foundation/components/logo /libs/foundation/components/mobileimage  /libs/foundation/components/mobilelogo /libs/wcm/foundation/components/image` |
| [Liste](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/list/v2/list) | Liste der Seiten | `/libs/foundation/components/list /libs/foundation/components/mobilelist /libs/wcm/foundation/components/list` |
| [Freigabe in Social Media](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/sharing/v1/sharing) | Facebook- und Pinterest-Freigabe-Widget | `-` |
| [Formular-Container](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/container/v2/container) | Responsives Formularabsatzsystem | `/libs/foundation/components/form/start /libs/foundation/components/form/end` |
| [Formulartext](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/text/v2/text) | Texteingabefeld | `/libs/foundation/components/form/text /libs/foundation/components/form/password` |
| [Formularoptionen](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/options/v2/options) | Eingabefeld für mehrere Optionen | `/libs/foundation/components/form/checkbox /libs/foundation/components/form/radio /libs/foundation/components/form/dropdown` |
| [Ausgeblendetes Formular](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/hidden/v2/hidden) | Ausgeblendetes Eingabefeld | `/libs/foundation/components/form/hidden` |
| [Formularschaltfläche](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/button/v2/button) | Senden oder benutzerdefinierte Schaltfläche | `/libs/foundation/components/form/submit` |
| [Navigation](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/navigation/v1/navigation) | Eine Site-Navigationskomponente, die die verschachtelte Seitenhierarchie auflistet | `/libs/foundation/components/topnav /libs/foundation/components/mobiletopnav` |
| [Sprachnavigation](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/languagenavigation/v1/languagenavigation) | Sprach- und Länderumschalter, die die globale Sprachstruktur auflistet | `-` |
| [Schnellsuche](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/search/v1/search) | Eine Suchkomponente, die die Ergebnisse als ersetzende Vorschläge in einem Dropdown-Menü anzeigt | `/libs/foundation/components/search` |
| [Teaser](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/teaser/v1/teaser) | Ermöglicht es dem Inhaltsautor, einen Teaser für weitere Inhalte zu erstellen, indem Sie ein Bild, einen Titel oder einen Rich Text verwenden und Links zu weiteren Inhalten oder anderen Aktionen erstellen. | `-` |
| [Registerkarten](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/tabs/v1/tabs) | Ermöglicht es dem Inhaltsautor, Seiteninhalte innerhalb mehrerer Registerkarten zu organisieren | `-` |
| [Karussell](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/carousel/v1/carousel) | Ermöglicht dem Inhaltsautor, Inhalte in einem drehenden Karussell der Folien zu organisieren | `/libs/foundation/components/carousel` |
| [Inhaltsrahmen](https://github.com/adobe/aem-core-wcm-components/tree/master/extension/contentfragment/content/src/content/jcr_root/apps/core/wcm/extension/components/contentfragment/v1/contentfragment) | Ermöglicht die Anzeige eines Inhaltsfragments | `-` |
| [Inhaltsgliederungsliste](https://github.com/adobe/aem-core-wcm-components/tree/master/extension/contentfragment/content/src/content/jcr_root/apps/core/wcm/extension/components/contentfragmentlist/v1/contentfragmentlist) | Ermöglicht die Anzeige einer Liste mit Inhaltsfragmenten | `-` |
| [Trennzeichen](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/separator/v1/separator) | Trennt Inhalt auf einer Seite. | `-` |

### Künftige Komponenten {#upcoming-components}

Die folgenden Kernkomponenten werden aktiv bearbeitet. Sie wurden noch nicht veröffentlicht, können aber in der [Entwicklungsverzweigung in der Vorschau angezeigt](https://github.com/adobe/aem-core-wcm-components/tree/development)werden:

* Video
* Herunterladen

## Aktualisierung der Kernkomponenten {#upgrade-of-core-components}

Ein Vorteil von Komponenten mit Versionshinweisen besteht darin, die Migration auf eine neue AEM-Version von der Migration zu neuen Komponentenversionen zu trennen. Wenn neue Komponentenversionen verfügbar sind, ermöglicht es außerdem die einzelne Migration jeder Komponente zur neuen Version.

Die Migration zu einer neuen AEM-Version wirkt sich nicht auf die Funktionsweise der Core-Komponenten aus, sofern ihre Versionen auch die neue AEM-Version unterstützen, auf die migriert wird. Anpassungen an den Core-Komponenten sollten davon nicht betroffen sein, solange sie keine apis verwenden, die [nicht mehr unterstützt oder entfernt](https://helpx.adobe.com/experience-manager/6-5/release-notes/deprecated-removed-features.html)wurden.

Migrierungen in neue Versionen der Kernkomponenten wirken sich nicht auf die Funktionsweise der Komponente aus, aber neue Funktionen können ggf. auf Seitenautoren eingeführt werden, was möglicherweise einige Konfigurationen durch einen Vorlageneditor erfordert, falls das Standardverhalten nicht gewünscht wird. Anpassungen müssen jedoch ggf. angepasst werden. Weitere Informationen finden Sie auf der [Seite Anpassen Kernkomponenten](customizing.md#upgrade-compatibility-of-customizations) .

## Wann verwenden Sie die Kernkomponenten? {#when-to-use-the-core-components}

Da die Kernkomponenten völlig neu sind und mehrere Vorteile bieten, sollten Sie für neue AEM-Projekte verwendet werden. Bei vorhandenen Projekten sollte eine Migration Teil eines größeren Projekts sein, z. B. ein Rebranding oder eine Gesamtrefaktorierung.

Daher bietet Adobe folgende Empfehlungen:

* **Neue Projekte**
Neue Projekte sollten immer versuchen, Core-Komponenten zu verwenden. Wenn Core-Komponenten nicht direkt oder [erweitert](customizing.md) werden können, um die Projektanforderungen zu erfüllen, erstellen Sie eine benutzerdefinierte Komponente, die nach der Komponentenarchitektur in Kernkomponenten folgt. Vermeiden Sie die Verwendung der [Foundation-Komponenten, sofern nicht anderweitig möglich](developing.md).
* **Bestehende**Projektempfehlung
verwendet weiterhin die [Foundation-Komponenten](developing.md), es sei denn, eine Site oder Komponente refaktoriert nicht.\
   Da sie sehr häufig von den meisten vorhandenen Projekten verwendet werden, werden die Foundation-Komponenten [weiterhin unterstützt.](developing.md)
* **Neue benutzerdefinierte Komponenten**
überprüfen, wenn eine vorhandene [Core-Komponente angepasst werden kann](customizing.md).\
   Andernfalls wird empfohlen, eine neue benutzerdefinierte Komponente zu erstellen, die den [Komponentenrichtlinien folgt](guidelines.md).
* **Vorhandene benutzerdefinierte Komponenten**,
wenn Ihre Komponenten erwartungsgemäß funktionieren, behalten Sie sie unverändert bei.\
   Falls nicht, verweisen Sie auf &quot;Neue benutzerdefinierte Komponenten&quot; oben.

## Migration zu Kernkomponenten

Jedes neue Projekt sollte mit Kernkomponenten implementiert werden. Bestehende Projekte verfügen jedoch meist über umfassende Implementierungen der Foundation-Komponenten.

Eine größere Arbeit an einem vorhandenen Projekt (z. B. ein Rebranding oder eine Gesamtrefaktorierung) bietet oft eine Möglichkeit, zu den Core-Komponenten zu migrieren. Um diese Migration zu erleichtern, stellt Adobe eine Reihe von Migrationswerkzeugen bereit, um die Akzeptanz der Kernkomponenten und der neuesten AEM-Technologie zu fördern.

[Die AEM Modernisierung Tools Suite](https://github.com/adobe/aem-modernize-tools) ermöglicht die einfache Konvertierung von:

* Statische Vorlagen zu bearbeitbaren Vorlagen
* Designkonfigurationen zu Richtlinien
* Foundation-Komponenten zu Kernkomponenten
* Klassische Benutzeroberfläche für Touch-aktivierte Benutzeroberfläche

Weitere Informationen zur Nutzung dieser Werkzeuge finden Sie [in der Dokumentation](https://www.adobe.com/go/aem_modernize_tools_en).

## Core-Komponentenunterstützung {#core-component-support}

Core-Komponenten sind ein wesentlicher Bestandteil von AEM und unterstützen wie vorliegend unter denselben Bedingungen, wie sie als Teil des Quickstart bereitgestellt wurden.

Wie andere AEM-Produktmerkmale lautet die allgemeine Regel: Komponenten werden zunächst als veraltet angekündigt und am frühesten für die folgende AEM-Version entfernt. Dadurch erhalten Kunden mindestens einen Versionszyklus, um zur neuen Version der Komponente zu wechseln, bevor sie den Support abbrechen.

Die Version der einzelnen Komponenten stellt klar die von dieser Version unterstützten AEM-Versionen dar. Wenn Support-Argumente für eine Version von AEM verfügbar sind, dann wird die Unterstützung der Kernkomponenten für diese Version von AEM unterstützt.

Weitere Informationen zur Unterstützung von Komponentenanpassungen finden Sie auf der [Seite Anpassen Kernkomponenten](customizing.md) .

## Unterstützung von Foundation-Komponenten {#foundation-component-support}

Da die Foundation-Komponenten aufgrund vieler AEM-Versionen als Grundlage für so viele Projekte bereitgestellt wurden, werden sie in absehbarer Zukunft weiterhin unterstützt.

Der Entwicklungs-Schwerpunkt von Adobe wurde jedoch auf die Kernkomponenten verschoben, und neue Funktionen werden ihnen hinzugefügt, während [fast alle Foundation-Komponenten mit AEM 6.5 verworfen wurden](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/default-components-foundation.html) und es werden nur Fehlerkorrekturen an den Foundation-Komponenten vorgenommen.

**Lesen Sie als Nächstes:**

* [Verwenden Kernkomponenten](using.md) - rufen Sie die Kernkomponenten in Ihrem eigenen Projekt auf.
* [Komponentenrichtlinien](guidelines.md) - um die Implementierungsmuster der Kernkomponenten zu erfahren.
