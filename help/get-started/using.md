---
title: Verwenden von Kernkomponenten
description: '„Um mit Kernkomponenten in Ihrem eigenen Projekt produktiv zu werden, sind drei Schritte erforderlich: herunterladen und installieren, Proxy-Komponenten erstellen, die Kernstile laden und die Komponenten in Ihren Vorlagen zulassen.“'
translation-type: ht
source-git-commit: 78202dc777b90f795f66873921c55e21ef8a239c
workflow-type: ht
source-wordcount: '758'
ht-degree: 100%

---


# Verwenden von Kernkomponenten{#using-core-components}

Um mit Kernkomponenten in Ihrem eigenen Projekt produktiv zu werden, sind vier Schritte erforderlich, die in den folgenden Abschnitten einzeln detailliert sind:

1. [Herunterladen und installieren](#download-and-install)
1. [Proxy-Komponenten erstellen](#create-proxy-components)
1. [Laden der Kernstile](#load-the-core-styles)
1. [Komponenten aktivieren](#allow-the-components)

>[!NOTE]
>
>Alternativ kann auch das folgende mehrteilige Tutorial von Interesse sein, um zu erfahren, wie Sie mit der Projekteinrichtung, den Kernkomponenten, den bearbeitbaren Vorlagen, den Client-Bibliotheken und der Komponentenentwicklung von Grund auf neu beginnen können:\
>[Erste Schritte mit AEM Sites - WKND-Tutorial](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)

## Herunterladen und installieren {#download-and-install}

Einer der treibenden Ideen hinter den Kernkomponenten ist Flexibilität. Durch die häufigere Veröffentlichung neuer Versionen der Kernkomponenten kann Adobe bei der Bereitstellung neuer Funktionen flexibler sein. Entwickler wiederum können flexibel entscheiden, welche Komponenten sie in ihre Projekte integrieren und wie oft sie diese aktualisieren möchten.

Aus diesem Grund sind die Kernkomponenten nicht Teil des Schnellstarts, wenn Sie im Produktionsmodus (ohne Beispielinhalt) beginnen. Der erste Schritt besteht darin, [das neueste veröffentlichte Inhaltspaket von GitHub](https://github.com/adobe/aem-core-wcm-components/releases/latest) herunterzuladen und es in Ihren AEM-Umgebungen zu installieren.

Es gibt verschiedene Möglichkeiten, dies zu automatisieren, aber die einfachste Möglichkeit, ein Inhaltspaket schnell auf einer Instanz zu installieren, erfolgt über den Package Manager; siehe [Installieren von Paketen](https://docs.adobe.com/content/help/en/experience-manager-65/administering/contentmanagement/package-manager.html#installing-packages). Sobald Sie außerdem eine Veröffentlichungsinstanz ausgeführt haben, müssen Sie dieses Paket für den Herausgeber replizieren. Siehe [Replizieren von Paketen](https://docs.adobe.com/content/help/en/experience-manager-65/administering/contentmanagement/package-manager.html#replicating-packages).

## Proxy-Komponenten erstellen {#create-proxy-components}

Aus den im Abschnitt [Proxy-Komponentenmuster](/help/developing/guidelines.md#proxy-component-pattern) erläuterten Gründen dürfen Kernkomponenten nicht direkt über den Inhalt referenziert werden. Um dies zu vermeiden, gehören alle zu einer ausgeblendeten Komponentengruppe ( `.core-wcm` oder `.core-wcm-form`), was verhindert, dass sie direkt im Editor angezeigt werden.

Stattdessen müssen Site-spezifische Komponenten erstellt werden, die den gewünschten Komponentennamen und die gewünschte Gruppe definieren, die für Seitenautoren angezeigt werden sollen, und jede auf eine Kernkomponente als ihren übergeordneten Typ verweisen. Diese Site-spezifischen Komponenten werden manchmal als „Proxy-Komponenten“ bezeichnet, da sie nichts enthalten und hauptsächlich zur Definition der Version einer Komponente dienen, die für die Site verwendet werden soll. Beim Anpassen der [Kernkomponenten](/help/developing/customizing.md)spielen diese Proxy-Komponenten jedoch eine wesentliche Rolle für die Anpassung von Markup und Logik.

Für jede Kernkomponente, die für eine Site verwendet werden soll, müssen Sie also Folgendes tun:

1. Erstellen Sie eine entsprechende Proxy-Komponente im Komponentenordner der Site.

   **Beispiel**
Unter `/apps/my-site/components` Erstellen eines Titelknotens des Typs `cq:Component`

1. Verweisen Sie auf die entsprechende Kernkomponentenversion mit dem übergeordneten Typ.

   **Beispiel**
Fügen Sie folgende Eigenschaft hinzu:\
   `sling:resourceSuperType="core/wcm/components/title/v1/title"`

1. Definieren Sie die Gruppe, den Titel und optional die Beschreibung der Komponente. Diese Werte sind projektspezifisch und bestimmen, wie die Komponente Autoren offensteht.

   **Beispiel**
Fügen Sie folgende Eigenschaften hinzu:

   ```shell
   componentGroup="My Site"
   jcr:title="Title"  
   jcr:description="Section Heading"
   ```

Betrachten Sie beispielsweise die [Titelkomponente der WKND-Site](https://github.com/adobe/aem-guides-wknd/blob/master/ui.apps/src/main/content/jcr_root/apps/wknd/components/title/.content.xml). Dies ist ein gutes Beispiel für eine Proxy-Komponente, die auf diese Weise aufgebaut ist.

## Laden der Kernstile {#load-the-core-styles}

1. Erstellen Sie eine [Client-Bibliothek](https://docs.adobe.com/content/help/de-DE/experience-manager-65/developing/introduction/clientlibs.html), die alle CSS- und JS-Dateien enthält, die für Ihre Site benötigt werden, falls noch nicht geschehen.
1. Fügen Sie in der Client-Bibliothek Ihrer Site die Abhängigkeiten zu den Kernkomponenten hinzu, die möglicherweise benötigt werden. Dies geschieht durch Hinzufügen einer `embed` Eigenschaft.

   Um beispielsweise die Client-Bibliotheken aller v1 Kernkomponenten einzubeziehen, lautet die hinzuzufügende Eigenschaft:

   ```shell
   embed="[  
   core.wcm.components.image.v1,  
   core.wcm.components.list.v1,  
   core.wcm.components.breadcrumb.v1,  
   core.wcm.components.form.container.v1,  
   core.wcm.components.form.text.v1  
   ]"
   ```

Stellen Sie sicher, dass Ihre Proxy-Komponenten und Client-Bibliotheken in Ihrer AEM-Umgebung bereitgestellt wurden, bevor Sie zum nächsten Abschnitt übergehen.

## Komponenten zulassen {#allow-the-components}

Die folgenden Schritte werden im [Vorlageneditor](https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/sites/authoring/features/templates.translate.html) ausgeführt.

1. Wählen Sie im Vorlageneditor den Layout-Container aus und öffnen Sie seine Richtlinie.
1. Wählen Sie in der Liste der zulässigen Komponenten die zuvor erstellten Proxy-Komponenten aus, die unter der ihnen zugewiesenen Komponentengruppe angezeigt werden sollen. Übernehmen Sie anschließend die Änderungen.
1. Optional können sie für Komponenten, die ein Dialogfeld „Design“ haben, vorkonfiguriert werden.

Das war´s! In den aus der bearbeiteten Vorlage erstellten Seiten sollten Sie jetzt die neu erstellten Komponenten verwenden können.

**Lesen Sie als Nächstes:**

* [Anpassen der Kernkomponenten](/help/developing/customizing.md) - Erfahren Sie, wie Sie die Kernkomponenten gestalten und anpassen können.
* [Komponentenrichtlinien](/help/developing/guidelines.md) - Lernen Sie die Implementierungsmuster der Kernkomponenten kennen.
