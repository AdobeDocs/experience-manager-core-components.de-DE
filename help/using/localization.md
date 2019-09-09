---
title: Lokalisierungsfunktionen der Kernkomponenten
seo-title: Lokalisierungsfunktionen der Kernkomponenten
description: Lokalisierungsfunktionen der Kernkomponenten
seo-description: Lokalisierungsfunktionen der Kernkomponenten
content-type: Referenz
topic-tags: Kernkomponenten
index: y
internal: n
translation-type: tm+mt
source-git-commit: 4af4873edf290f93733b0997b0e7a19c6c9e26f2

---


# Lokalisierungsfunktionen der Kernkomponenten {#localization-features-of-the-core-components}

Viele Websites benötigen Inhalte, die in einem lokalisierten Format über mehrere Sprachen und Länder bereitgestellt werden sollen. Mit der Funktion für Kernkomponenten der Kernkomponenten können Sie einfach eine einheitliche Vorlage für alle lokalisierten Inhalte erstellen, die basierend auf Ihrer lokalisierten Site-Struktur automatisch angepasst werden.

## Beispiel: Lokalisierte Seite mit Navigations- und Fußzeilen {#example}

Die meisten Sites benötigen eine Fußzeile, die für alle Seiten vorhanden ist. Diese Fußzeilen sind im Allgemeinen konsistent über den gesamten Inhalt der Seite hinweg. Für eine lokalisierte Inhaltsseite muss eine lokalisierte Version dieser Kopf- oder Fußzeile angezeigt werden.

Entsprechend muss eine Navigationskomponente normalerweise auf allen Seiten angezeigt werden. Sie muss jedoch auch den Inhalt der lokalisierten Seiten widerspiegeln.

Verwenden der Lokalisierungsfunktionen der [Navigation Core Component und](navigation.md) [Experience Fragment Core Component](experience-fragment.md) zusammen mit den [bearbeitbaren Vorlagen von AEM](https://docs.adobe.com/content/help/en/experience-manager-64/authoring/siteandpage/templates.html).

## Die Inhaltsstruktur {#content-structure}

Alle Lokalisierungsfunktionen von AEM und seinen Core-Komponenten basieren auf einer klaren und logischen Inhaltsstruktur für Ihren lokalisierten Inhalt.

Nehmen wir an, Ihre Site wird einfach aufgerufen `my-site` und befindet sich hier:

```
/content/my-site
```

Nehmen wir an, Sie erstellen Ihre Site auf Englisch und bieten sie auch auf Französisch an. Wenn Sie also eine einfache Seite namens `my-page` sie in zwei Lokalisierungsverzweigungen in der Inhaltsstruktur Ihrer Site finden:

```
/content
\-- my-site
   +-- en
       \-- my-page
   \-- fr
       \-- my-page
```

Es liegt unter diesen Lokalisierungsverzweigungen, in denen Sie zusätzliche Seiten für Sites erstellen.

Seitenfußzeilen werden meist mit Erlebnisfragmenten erstellt, damit Sie eine englische und französische Version genau wie Ihre Seiten benötigen. Erlebnisfragmente sind jedoch keine Seiten, sondern dienen eher als Teil der Seiten, die wiederverwendet werden können, sodass sie nicht direkt mit `/content` den übrigen Seiten gefüllt werden. Stattdessen leben sie in ihrem eigenen Ordner, da sie jedoch auch lokalisiert werden müssen, muss ihre Struktur die Lokalisierungsstruktur Ihrer Site widerspiegeln.

```
/content
+-- experience-fragments
   +-- en
      +-- footer
   \-- fr
      +-- footer
\-- my-site
   +-- en
      \-- my-page
   \-- fr
      \-- my-page
```

Durch die gespiegelte Lokalisierungsstruktur können die Kernkomponenten den erforderlichen lokalisierten Inhalt für eine entsprechende Seite finden.

## Seitenfußzeile - Erlebnisfragment {#footer}

Die Experience Fragment-Komponente ist sehr flexibel und eignet sich gut für eine Seitenkopf- oder -fußzeile.

Da unsere hypothetische Website auf Englisch und Französisch angeboten wird, müssen wir zwei Erlebnisfragmente erstellen, die beide `footer`[an dem zuvor beschriebenen Ort aufgerufen werden.](#content-structure)

![](assets/screen-shot-2019-09-09-11.08.28.png)

## Seitenvorlage {#template}

Da die Fußzeile auf jeder Seite angezeigt wird, müssen wir das Erlebnisfragment zu unserer Standardseitenvorlage hinzufügen.

Unsere Vorlage wird einfach aufgerufen `my-template` und befindet sich mit unseren anderen Vorlagen:

```
/conf/my-site/settings/wcm/templates/my-template
```

Zu dieser Vorlage fügen wir die grundlegenden Komponenten hinzu, auf denen unsere Seiten basieren sollen.

* [Navigationskomponente](navigation.md)
   * Die Navigationskomponente wird oben auf jeder Seite angezeigt.
   * In der Navigationskomponente definieren wir den Navigationsstamm und teilen ihm mit, wo die Navigationsstruktur der Site beginnt.
   * Basierend auf dem Navigationsstamm kann die Komponente den entsprechenden lokalisierten Inhalt automatisch finden.
* Layout-Container
   * Jede Seite enthält eine editierbare Layout-Container-Komponente, damit Autoren zusätzliche Inhalte auf der Seite platzieren können.
* [Experience Fragment](experience-fragment.md)
   * Die Experteninece Fragment-Komponente verweist auf den Fragmentpfad in unserer Authoring-Sprache des Fragments, das die Fußzeile darstellt.
   * Basierend auf dem Pfad des Fragments und der Struktur der Erlebnisfragmente, die die lokalisierte Seitenstruktur reflektieren, kann die Komponente den entsprechenden lokalisierten Inhalt automatisch finden.
   ![](assets/screen-shot-2019-09-09-11.20.10.png)

## Seiten {#pages}

Wenn Sie die Site-Struktur und -vorlage einrichten, muss der Autor einfach den erforderlichen Inhalt für die Seiten hinzufügen. Aufgrund der Lokalisierungslogik der Komponenten werden die Navigations- und Fußzeilen automatisch lokalisiert.

Beispielsweise würde der Autor nur eine Textkomponente der englischen und französischen Seite hinzufügen (die in Blau dargestellt wird).

Die Komponente "Navigationskomponente und Erlebnisfragment" erkennt, dass der korrekte Inhalt basierend auf der Lokalisierungsstruktur und dem Speicherort der Seite automatisch angezeigt wird (siehe White Unten).

![](assets/screen-shot-2019-09-09-11.22.14.png)

## Alle zusammenpassen {#fitting-it-all-together}

Im Folgenden finden Sie das vollständige Bild, wie diese einfachen, aber leistungsstarken Elemente zusammenarbeiten, um lokalisierte Seiten für die Autoren bereitzustellen.

![](assets/screen-shot-2019-09-09-11.27.58.png)
