---
title: Lokalisierungsfunktionen der Hauptkomponenten
seo-title: Lokalisierungsfunktionen der Hauptkomponenten
description: Lokalisierungsfunktionen der Hauptkomponenten
seo-description: Lokalisierungsfunktionen der Hauptkomponenten
content-type: Referenz
topic-tags: Kernkomponenten
index: y
internal: n
translation-type: tm+mt
source-git-commit: c8041e855386b7195fe32dd5dc53458f1d8270b8

---


# Lokalisierungsfunktionen der Hauptkomponenten {#localization-features-of-the-core-components}

Viele Websites erfordern, dass Inhalte in einem lokalisierten Format in mehreren Sprachen und Regionen bereitgestellt werden. Die ausgewählten Kernkomponenten verfügen über eine intelligente Referenzauflösung, um die Erstellung einer einheitlichen Vorlage für all Ihre lokalisierten Inhalte zu vereinfachen, die sich automatisch an Ihre lokalisierte Site-Struktur anpasst.

## Beispiel: Lokalisierte Seite mit Navigation und Fußzeilen {#example}

Most sites require a footer to be present across all pages. These footers are generally consistent across all content of the page. However for a localized content page, a localized version of that header or footer needs to be displayed.

Similarly a navigation component usually must be displayed across all pages. However it will need to reflect the content of the localized pages as well.

Using the localization features of the Navigation Core Component and Experience Fragment Core Component along with the editable templates of AEM, this becomes a smiple task. [](navigation.md)[](experience-fragment.md)[](https://docs.adobe.com/content/help/en/experience-manager-64/authoring/siteandpage/templates.html) The example could be further extended to use the Language Navigation Component as well.[](language-navigation.md)

## The Content Structure {#content-structure}

Alle Lokalisierungsfunktionen von AEM und seinen Core-Komponenten basieren auf einer klaren und logischen Inhaltsstruktur für Ihre lokalisierten Inhalte.

Nehmen wir an, Ihre Site wird einfach aufgerufen `my-site` und befindet sich hier:

```
/content/my-site
```

Nehmen wir auch an, dass Sie Ihre Website auf Englisch verfassen und auch auf Französisch anbieten. Wenn Sie also eine einfache Seite namens `my-page` haben, würde sie in zwei Lokalisierungszweigen in der Inhaltsstruktur Ihrer Site gefunden werden:

```
/content
\-- my-site
   +-- en
       \-- my-page
   \-- fr
       \-- my-page
```

Unter diesen Lokalisierungszweigen erstellen Sie weitere Siteseiten.

Seitenfußzeilen werden im Allgemeinen mit Erlebnisfragmenten erstellt, sodass Sie eine englische und französische Version wie Ihre Seiten benötigen. However Experience Fragments are not pages, but are rather parts of pages that can be reused across pages, so they do not live directly under `/content` as the rest of your pages. Stattdessen leben sie in ihrem eigenen Ordner, müssen aber auch lokalisiert werden, ihre Struktur muss der Lokalisierungsstruktur Ihrer Site entsprechen.

```
/content
+-- experience-fragments
   +-- en
      \-- footer
   \-- fr
      \-- footer
\-- my-site
   +-- en
      \-- my-page
   \-- fr
      \-- my-page
```

Durch die gespiegelte Lokalisierungsstruktur können die Kernkomponenten die erforderlichen lokalisierten Inhalte für eine entsprechende Seite finden.

## Page Footer - Experience Fragment {#xf-footer}

Die Komponente "Erlebnisfragment"ist sehr flexibel und eignet sich gut für eine Kopfzeile oder Fußzeile.

Da unsere hypothetische Website in Englisch und Französisch angeboten wird, müssen wir zwei Erlebnisfragmente erstellen, die beide `footer` an den zuvor beschriebenen Orten [genannt werden.](#content-structure)

![](assets/screen-shot-2019-09-09-11.08.28.png)

## Seitenvorlage {#template}

Da die Fußzeile auf jeder Seite angezeigt wird, müssen wir das Erlebnisfragment zu unserer Standardseitenvorlage hinzufügen.

Unsere Vorlage wird einfach aufgerufen `my-template` und befindet sich in unseren anderen Vorlagen:

```
/conf/my-site/settings/wcm/templates/my-template
```

Zu dieser Vorlage fügen wir die grundlegenden Komponenten hinzu, auf denen unsere Seiten basieren sollen.

* [Navigationskomponente](navigation.md)
   * The Navigation Component will appear at the top of every page.
   * In der Navigationskomponente definieren wir den Navigationsstamm und teilen die Komponente mit, wo die Navigationsstruktur der Site beginnt.
   * Basierend auf dem Navigationsstamm kann die Komponente den entsprechenden lokalisierten Inhalt automatisch finden.
* [Container-Komponente](container.md)
   * Every page will contain an editable Container Component so that authors can place additional content on the page.
* [Experience Fragment](experience-fragment.md)
   * Wir verweisen die Komponente "Expertenfragment"auf den Fragmentpfad in unserer Authoring-Sprache des Fragments, das die Fußzeile darstellt.
   * Based on that fragment's path and the structure of the experience fragments that mirrors the localized page structure, the component can find the corresponding localized content automatically.
   ![](assets/screen-shot-2019-09-09-11.20.10.png)

## Seiten {#pages}

By doing the hard work in setting up the site structure and template, the content author simply needs to add the necessary content to the pages. Thanks to the templates and the localization logic of the components, the navigation and footers will be automatically added to the page and localized.

Der Autor müsste beispielsweise nur Inhalte wie Textkomponenten zu den englischen und französischen Seiten hinzufügen (unten blau dargestellt).

Die Komponenten "Navigationskomponente"und "Erlebnisfragment"stammen aus der Seitenvorlage und wissen, dass der richtige Inhalt automatisch basierend auf der Lokalisierungsstruktur und der Position der Seite selbst angezeigt wird (unten in Weiß dargestellt).

![](assets/screen-shot-2019-09-09-11.22.14.png)

## Zusammenpassen {#fitting-it-all-together}

Im Folgenden finden Sie ein vollständiges Bild davon, wie diese einfachen, aber leistungsstarken Elemente zusammenarbeiten, um lokalisierte Seiten für Autoren bereitzustellen.

![](assets/screen-shot-2019-09-09-11.27.58.png)
