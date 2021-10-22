---
title: Entwickeln von Kernkomponenten
description: Die Kernkomponenten bieten leistungsfähige und erweiterbare Basiskomponenten mit umfangreichen Funktionen, kontinuierlicher Bereitstellung, Komponentenversionierung, moderner Implementierung, schlankem Markup und JSON-Export von Inhalten.
role: Architect, Developer, Admin
exl-id: 0f79cac1-a3b0-487e-90be-0bd8263d3912
source-git-commit: 2ac16b15718128feefbe903e92f276b16fe96f69
workflow-type: ht
source-wordcount: '1583'
ht-degree: 100%

---

# Entwickeln von Kernkomponenten {#developing-core-components}

## Wann sollten die Kernkomponenten verwendet werden? {#when-to-use-the-core-components}

Da die Kernkomponenten völlig neu sind und mehrere Vorteile bieten, wird empfohlen, sie für neue AEM-Projekte zu verwenden. Bei vorhandenen Projekten sollte eine Migration Teil einer größeren Projektaufgabe sein, z. B. ein Rebranding oder eine Gesamtrefaktorierung.

Daher bietet Adobe folgende Empfehlungen:

* **Neue Projekte**
Neue Projekte sollten immer versuchen, Kernkomponenten zu verwenden. Wenn Kernkomponenten nicht direkt oder [erweitert](customizing.md) verwendet werden können, um die Projektanforderungen zu erfüllen, erstellen Sie eine benutzerdefinierte Komponente gemäß der Komponentenarchitektur, die in den Kernkomponenten festgelegt ist. Vermeiden Sie die Verwendung der [Foundation-Komponenten](/help/versions.md#foundation-component-support), sofern möglich.
* **Existierende Projekte**
Empfohlen wird, weiterhin die [Foundation-Komponenten](/help/versions.md#foundation-component-support) zu verwenden, es sei denn, es ist eine Refaktorierung von Sites oder Komponenten geplant.\
   Da sie sehr häufig von den meisten vorhandenen Projekten verwendet werden, werden die Foundation-Komponenten [weiterhin unterstützt](/help/versions.md#foundation-component-support).
* **Neue benutzerdefinierte Komponenten**
Überprüfen Sie, ob eine vorhandene [Kernkomponente angepasst werden kann](customizing.md).\
   Wenn nicht, wird empfohlen, eine neue benutzerdefinierte Komponente zu erstellen, die den [Komponentenrichtlinien](guidelines.md) folgt.
* **Vorhandene benutzerdefinierte Komponenten**
Wenn Ihre Komponenten erwartungsgemäß funktionieren, behalten Sie sie unverändert bei.
\
   Falls nicht, siehe oben „Neue benutzerdefinierte Komponenten“.

## So haben Sie Erfolg mit den Kernkomponenten {#how-to-succeed}

Die Kernkomponenten sind leistungsstark, flexibel und einfach zu verwenden und anzupassen. [Die Einhaltung einiger wichtiger Richtlinien](success.md) stellt sicher, dass Ihr Projekt mit den Kernkomponenten erfolgreich ist.

## Migration zu den Kernkomponenten

Jedes neue Projekt sollte mit Kernkomponenten implementiert werden. Bestehende Projekte verfügen jedoch meist über umfassende Implementierungen der Foundation-Komponenten.

### Migration von Foundation-Komponenten {#from-foundation}

Eine größere Arbeit an einem vorhandenen Projekt (z. B. ein Rebranding oder eine Gesamtrefaktorierung) bietet oft eine Möglichkeit, zu den Kernkomponenten zu migrieren. Um diese Migration zu erleichtern, stellt Adobe eine Reihe von Migrationswerkzeugen bereit, um die Akzeptanz der Kernkomponenten und der neuesten AEM-Technologie zu fördern.

[Die AEM-Modernisierungs-Tools](http://opensource.adobe.com/aem-modernize-tools/) ermöglichen eine einfache Konvertierung von:

* Statischen Vorlagen in bearbeitbare Vorlagen
* Design-Konfigurationen in Richtlinien
* Foundation-Komponenten in Kernkomponenten
* Klassische Benutzeroberfläche in Touch-optimierte Benutzeroberfläche

Weitere Informationen zur Verwendung dieser Werkzeuge finden Sie [in der entsprechenden Dokumentation](http://opensource.adobe.com/aem-modernize-tools/).

>[!NOTE]
>
>Die AEM-Modernisierung-Tools werden von der Community gesammelt, Adobe bietet keinerlei Unterstützung oder Garantie dafür.

## Migration mit Move zu AEM as a Cloud Service {#via-aemaacs}

Da AEM as a Cloud Service automatisch mit der neuesten Version der Kernkomponenten geliefert wird, müssen Sie beim Wechsel von einer On-Premise-AEM-Installation alle Abhängigkeiten zu den Kernkomponenten in der Datei `pom.xml` Ihres Projekts entfernen.

Ihre Proxy-Komponenten funktionieren weiterhin wie zuvor, da Proxys auf den erforderlichen Supertyp zeigen und der Supertyp-Pfad die Version enthält. Auf diese Weise ermöglicht das einfache Entfernen der Abhängigkeit, dass die Kernkomponenten in AEMaaCS genauso funktionieren, wie sie es On-Premise taten.

Wie bei jedem anderen AEMaaCS-Projekt müssen Sie auch eine Abhängigkeit zur AEM SDK-JAR-Datei hinzufügen. Dies ist nicht spezifisch für die Kernkomponenten, aber es ist erforderlich.

```xml
<dependency>
   <groupId>com.adobe.aem</groupId>
   <artifactId>aem-sdk-api</artifactId>
</dependency>
```

Weitere Informationen zu AEMaaCS-Projekten finden Sie im Dokument [Projektstruktur in AEM](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=de).

## Kernkomponentenunterstützung {#core-component-support}

Kernkomponenten sind ein integraler Bestandteil von AEM und werden ohne Mängelgewähr unterstützt, zu den gleichen Bedingungen und Konditionen, als ob sie im Rahmen des Quickstarts geliefert würden.

Wie andere AEM-Produktmerkmale lautet die allgemeine Regel: Komponenten werden zunächst als veraltet angekündigt und frühestens in der folgenden AEM-Version entfernt. Dadurch erhalten Kunden mindestens einen Versionszyklus, um zur neuen Version der Komponente zu wechseln, bevor deren Unterstützung eingestellt wird.

Die Version jeder Komponente gibt eindeutig die AEM-Versionen an, die sie unterstützt. Wenn der Support für eine Version von AEM eingestellt wird, gilt das auch für die Unterstützung der Kernkomponenten für diese Version von AEM.

Weitere Informationen zur Unterstützung von Komponentenanpassungen finden Sie auf der Seite [Anpassen von Kernkomponenten](customizing.md).


## Technische Funktionen {#technical-capabilities}

In der folgenden Tabelle finden Sie einen Überblick über die Unterschiede zwischen Kernkomponenten und Foundation-Komponenten.

Einzelheiten zu ihren Authoring-Fähigkeiten und Optionen zu ihrer Vorkonfiguration [finden Sie auf der entsprechenden Authoring-Seite](/help/get-started/authoring.md).

| **Funktion** | **Kernkomponente** | **Foundation-Komponente** |
|-----|---|---|
| Logikimplementierung | Java POJOs mit Anmerkungen zu [Sling-Modellen](https://sling.apache.org/documentation/bundles/models.html) | JSP-Code |
| Markup-Definition | [HTML Template Language](https://experienceleague.adobe.com/docs/experience-manager-htl/using/overview.html?lang=de) (HTL)-Syntax | JSP-Code |
| XSS-Bereinigung | Automatisiert durch HTL | Hauptsächlich manuell |
| CSS-Klassen-Benennung | Standardisierte Benennungskonvention basierend auf der [Block Element Modifier](https://getbem.com/) (BEM)-Notation (ab Version 2.0.0) | Benutzerdefinierte Schemata |
| Dialogfeld-Definition | [Coral 3](https://helpx.adobe.com/de/experience-manager/6-5/sites/developing/using/reference-materials/coral-ui/coralui3/index.html) | Coral 2 + Klassische Benutzeroberfläche |
| JSON-Ausgabe | [Sling Model Exporter mit Jackson-Serialisierung](https://sling.apache.org/documentation/bundles/models.html#exporter-framework-since-130) | Standard-Sling-Servlet |
| Versionierung | [Für das Modell und die HTL](guidelines.md) | Keine |
| Testing | Unit-Tests und Integrationstests | Integrationstests |
| Bereitstellung | [Über öffentliches GitHub](https://github.com/adobe/aem-core-wcm-components) | Über Quickstart |
| Lizenz | [Apache-Lizenz](https://www.apache.org/licenses/LICENSE-2.0) | Adobe-geschützt |
| Beitrag | Über Pull-Anfrage | Nicht möglich |
| Erreichbarkeit | Vollständig konform mit dem [WCAG 2.0 AA-Standard](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html?lang=de) | Nur teilweise konform mit dem [WCAG 2.0 AA-Standard](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html?lang=de) |

## Komponentenliste {#component-list}

In der folgenden Tabelle sind die verfügbaren Kernkomponenten mit Links zu ihrer API aufgeführt und es wird angegeben, welche Foundation-Komponenten sie ersetzen.

| Kernkomponente | Beschreibung | Ersetzte Foundation-Komponente(n) |
|---|---|---|
| [Seite](https://adobe.com/go/aem_cmp_tech_page_v2_de) | Responsive Seite, die mit dem Vorlageneditor arbeitet | `/libs/foundation/components/page /libs/wcm/foundation/components/page` |
| [Breadcrumb](https://adobe.com/go/aem_cmp_tech_breadcrumb_v2_de) | Navigation der Seitenhierarchie | `/libs/foundation/components/breadcrumb` |
| [Titel](https://adobe.com/go/aem_cmp_tech_title_v2_de) | H1-H6-Titel | `/libs/foundation/components/title /libs/wcm/foundation/components/title` |
| [Text](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/text/v2/text) | Rich-Text | `/libs/foundation/components/text /libs/foundation/components/table /libs/wcm/foundation/components/text` |
| [Bild](https://adobe.com/go/aem_cmp_tech_image_v2_de) | Intelligentes und entspanntes Laden der optimalen Wiedergabegröße | `/libs/foundation/components/image /libs/foundation/components/adaptiveimage /libs/foundation/components/logo /libs/foundation/components/mobileimage  /libs/foundation/components/mobilelogo /libs/wcm/foundation/components/image` |
| [Liste](https://adobe.com/go/aem_cmp_tech_list_v2_de) | Liste der Seiten | `/libs/foundation/components/list /libs/foundation/components/mobilelist /libs/wcm/foundation/components/list` |
| [Freigabe in Social Media](https://adobe.com/go/aem_cmp_tech_sharing_v1_de) | Widget zum Teilen auf Facebook und Pinterest | `-` |
| [Formular-Container](https://adobe.com/go/aem_cmp_tech_form_container_v2_de) | Responsives Formular-Absatzsystem | `/libs/foundation/components/form/start /libs/foundation/components/form/end` |
| [Formulartext](https://adobe.com/go/aem_cmp_tech_form_text_v2_de) | Texteingabefeld | `/libs/foundation/components/form/text /libs/foundation/components/form/password` |
| [Formularoptionen](https://adobe.com/go/aem_cmp_tech_form_options_v2_de) | Eingabefeld für mehrere Optionen | `/libs/foundation/components/form/checkbox /libs/foundation/components/form/radio /libs/foundation/components/form/dropdown` |
| [Ausgeblendetes Formular](https://adobe.com/go/aem_cmp_tech_form_hidden_v2_de) | Ausgeblendetes Eingabefeld | `/libs/foundation/components/form/hidden` |
| [Formularschaltfläche](https://adobe.com/go/aem_cmp_tech_form_button_v2_de) | Schaltfläche zum Absenden oder benutzerdefinierte Schaltfläche | `/libs/foundation/components/form/submit` |
| [Navigation](https://adobe.com/go/aem_cmp_tech_navigation_v1_de) | Eine Site-Navigationskomponente, die die verschachtelte Seitenhierarchie auflistet | `/libs/foundation/components/topnav /libs/foundation/components/mobiletopnav` |
| [Sprachnavigation](https://adobe.com/go/aem_cmp_tech_langnav_v1_de) | Ein Umschalter zwischen Sprachen und Ländern, der die globale Sprachstruktur auflistet | `-` |
| [Schnellsuche](https://adobe.com/go/aem_cmp_tech_search_v1_de) | Eine Suchkomponente, die die Ergebnisse als ersetzende Vorschläge in einem Dropdown-Menü anzeigt | `/libs/foundation/components/search` |
| [Teaser](https://adobe.com/go/aem_cmp_tech_teaser_v1_de) | Ermöglicht es dem Inhaltsautor, mühelos einen Teaser für weitere Inhalte zu erstellen, indem er ein Bild, einen Titel oder Rich-Text verwendet und Links zu weiteren Inhalten oder anderen Aktionen erstellt | `-` |
| [Registerkarten](https://adobe.com/go/aem_cmp_tech_tabs_v1_de) | Ermöglicht es dem Inhaltsautor, Seiteninhalte innerhalb mehrerer Registerkarten zu organisieren | `-` |
| [Karussell](https://adobe.com/go/aem_cmp_tech_carousel_v1_de) | Ermöglicht es dem Inhaltsautor, Inhalte in einem drehbaren Karussell der Folien zu organisieren | `/libs/foundation/components/carousel` |
| [Inhaltsfragment](https://adobe.com/go/aem_cmp_tech_cf_v1_de) | Ermöglicht die Anzeige eines Inhaltsfragments | `-` |
| [Inhaltsfragmentliste](https://adobe.com/go/aem_cmp_tech_cflist_v1_de) | Ermöglicht die Anzeige einer Liste mit Inhaltsfragmenten | `-` |
| [Trennzeichen](https://adobe.com/go/aem_cmp_tech_separator_v1_de) | Trennt Inhalt auf einer Seite | `-` |
| [Akkordeon](https://adobe.com/go/aem_cmp_tech_accordion_v1) | Organisieren von Inhalts-Bedienfeldern in einem ausblendbaren Accordion | `-` |
| [Container](https://adobe.com/go/aem_cmp_tech_container_v1_de) | Organisieren von Komponenten in einem Container | `-` |
| [Schaltfläche](https://adobe.com/go/aem_cmp_tech_button_v1) | Erstellen einer Schaltfläche auf einer Seite | `-` |
| [Download](https://adobe.com/go/aem_cmp_tech_download_v1) | Hinzufügen eines herunterladbaren Assets zu einer Seite | `-` |
| [Experience Fragment](https://adobe.com/go/aem_cmp_tech_xf_v1_de) | Hinzufügen eines Experience Fragment zu einer Seite | `/libs/cq/experience-fragments/editor/components/experiencefragment` |
| [Einbetten](https://adobe.com/go/aem_cmp_tech_embed_v1) | Einbetten einer externen Ressource in eine Seite | - |
| [Fortschrittsleiste](https://adobe.com/go/aem_cmp_tech_progress_v1) | Visualisierung des Fortschritts beim Erreichen eines Ziels | - |
| [PDF-Viewer](https://adobe.com/go/aem_cmp_tech_pdfviewer_v1_de) | Zeigt ein PDF-Dokument auf einer Seite an | - |

### Künftige Komponenten {#upcoming-components}

Einen Überblick über geplante Kernkomponenten finden Sie im [Projekt-Wiki auf GitHub](https://github.com/adobe/aem-core-wcm-components/wiki/home).

## Aktualisierung der Kernkomponenten {#upgrade-of-core-components}

Ein Vorteil versionierter Komponenten besteht darin, dass die Migration auf eine neue AEM-Version von der Migration auf neue Komponentenversionen getrennt werden kann. Wenn neue Komponentenversionen verfügbar sind, wird außerdem die einzelne Migration jeder Komponente zur neuen Version ermöglicht.

Die Migration zu einer neuen AEM-Version wirkt sich nicht auf die Funktionsweise der Kernkomponenten aus, sofern ihre Versionen auch die neue AEM-Version unterstützen, auf die migriert wird. An den Kernkomponenten vorgenommene Anpassungen sollten ebenfalls nicht beeinträchtigt werden, sofern sie keine [veralteten oder entfernten](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/deprecated-removed-features.html?lang=de) APIs verwenden.

Migrationen auf neue Versionen der Kernkomponenten wirken sich nicht auf die Funktionsweise der Komponente aus, aber es können ggf. neue Funktionen für Seitenautoren eingeführt werden, was möglicherweise einige Konfigurationen durch einen Vorlageneditor erfordert, falls das Standardverhalten nicht gewünscht wird. Anpassungen müssen jedoch ggf. angepasst werden. Weitere Informationen finden Sie auf der Seite [Anpassen von Kernkomponenten](customizing.md#upgrade-compatibility-of-customizations).
