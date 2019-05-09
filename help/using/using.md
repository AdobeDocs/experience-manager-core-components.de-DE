---
title: Verwenden von Kernkomponenten
seo-title: Verwenden von Kernkomponenten
description: 'null'
seo-description: '" Um mit Kernkomponenten in Ihrem eigenen Projekt vertraut zu werden, gibt es drei Schritte: herunterladen und installieren, Proxy-Komponenten erstellen, die Kernstile laden und die Komponenten in Ihren Vorlagen zulassen. «'
uuid: a 1 ef 2 acf -8226-4510-838 b-f 5 fae 196 f 9 f 1
contentOwner: Benutzer
content-type: Referenz
topic-tags: wird entwickelt
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-new
discoiquuid: 1703 a 171-830 c -477 e-a 34 f -99 caba 841 ec 4
disttype: dist5
gnavtheme: light
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 1bbec9b1f109df88964dce051a58d111bf6cafaa

---


# Verwenden von Kernkomponenten{#using-core-components}

Um mit [Kernkomponenten](developing.md) in Ihrem eigenen Projekt vertraut zu werden, gibt es vier Schritte, die in den folgenden Abschnitten einzeln detailliert sind:

1. [Herunterladen und Installieren](#download-and-install)
1. [Proxy-Komponenten erstellen](#create-proxy-components)
1. [Laden der Core-Stile](#load-the-core-styles)
1. [Komponenten aktivieren](#allow-the-components)

>[!NOTE]
>
>Alternativ dazu können die Hauptkomponenten, bearbeitbaren Vorlagen, Client-Bibliotheken und Komponentenentwicklung für allgemeine Anweisungen zur ersten Schritte mit dem Projektsetup, der bearbeitbaren Vorlage, der Client-Bibliotheken und der Komponentenentwicklung verwendet werden:\
>[Erste Schritte mit AEM Sites - WKND Tutorial](wknd-tutorial.md)

## Herunterladen und Installieren {#download-and-install}

Einer der führenden Ideen hinter den Kernkomponenten ist Flexibilität. Durch die Veröffentlichung neuer Versionen der Kernkomponenten kann Adobe bei der Bereitstellung neuer Funktionen flexibler sein. Entwickler können sich flexibel entscheiden, in welche Komponenten sie sich integrieren lassen und wie oft sie sie aktualisieren möchten.

Aus diesem Grund sind die Core-Komponenten nicht Teil des Schnellstart, wenn sie im Produktionsmodus (ohne Beispielinhalt) beginnen. Der erste Schritt besteht darin, das neueste veröffentlichte Inhaltspaket von github [herunterzuladen](https://github.com/adobe/aem-core-wcm-components/releases/latest) und es in Ihren AEM-Umgebungen zu installieren.

Es gibt verschiedene Möglichkeiten, dies zu automatisieren, aber die einfachste Möglichkeit, ein Inhaltspaket schnell auf einer Instanz zu installieren, erfolgt über den Package Manager; Siehe [Installieren von Paketen](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/package-manager.html). Sobald Sie außerdem eine Veröffentlichungsinstanz ausgeführt haben, müssen Sie dieses Paket für den Herausgeber replizieren. Siehe [Replizieren von Paketen](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/package-manager.html).

<!-- 

Comment Type: annotation
Last Modified By: ims-author-CE1E2CE451D1F0680A490D45@AdobeID
Last Modified Date: 2017-04-17T16:42:59.142-0400

Should we be promoting embedding the core-component package as an artifact in a customer application, reasoning as follows: 1) a customer application is required to leverage core components (at a minimum, proxy components must be defined) 2) a customer application must be updated to leverage new versions of core components (since it requires adjusting the sling:resourceSuperType to point at the new version of the component) It seems the only time theres an advantage to installing a release directly is if a bug-fix (non version-changing) release of core-components is cut, and it doesnt coincide with an application deployment. WDYT? For example, recommend doing this for ACS Commons which has a similar use-case (https://adobe-consulting-services.github.io/acs-aem-commons/pages/maven.html) We can of course keep the instructions for manually deploying, since some will want to do this, or the bug-fix use-case will appear.

 -->

## Proxy-Komponenten erstellen {#create-proxy-components}

Aus den im Abschnitt [Proxy Component Pattern](guidelines.md#proxy-component-pattern) erläuterten Gründen dürfen Core-Komponenten nicht direkt über den Inhalt referenziert werden. Um dies zu vermeiden, gehören alle zu einer ausgeblendeten Komponentengruppe ( `.core-wcm` oder `.core-wcm-form`), die verhindert, dass sie direkt im Editor angezeigt werden.

Stattdessen müssen site-spezifische Komponenten erstellt werden, die den gewünschten Komponentennamen und die gewünschte Gruppe definieren, die für Seitenautoren angezeigt werden sollen, und jede auf eine Core-Komponente als ihren Supertyp verweisen. Diese sitespezifischen Komponenten werden manchmal als &quot;Proxy-Komponenten&quot; bezeichnet, da sie nichts enthalten und hauptsächlich zur Definition der Version einer Komponente dienen, die für die Site verwendet werden soll. Beim Anpassen der [Kernkomponenten](customizing.md)spielen diese Proxy-Komponenten jedoch eine wesentliche Rolle für Markierung und logische Anpassung.

Für jede Core-Komponente, die für eine Site verwendet werden soll, müssen Sie Folgendes tun:

1. Erstellen Sie eine entsprechende Proxy-Komponente im Komponentenordner der Site.

   **Beispiel**
unter `/apps/my-site/components` Erstellen eines Titelknotens des Typs `cq:Component`

1. Verweisen Sie auf die entsprechende Core-Komponentenversion mit dem super-Typ.

   **Beispiel**
fügen Sie folgende Eigenschaft hinzu:\
   `sling:resourceSuperType="core/wcm/components/title/v1/title"`

1. Definieren Sie die Gruppe, den Titel und optional die Beschreibung der Komponente. Diese Werte sind projektspezifisch und bestimmen, wie die Komponente Autoren offensteht.

   **Beispiel**
Fügen Sie folgende Eigenschaften hinzu:

   ```shell
   componentGroup="My Site"
   jcr:title="Title"  
   jcr:description="Section Heading"
   ```

Betrachten Sie beispielsweise die [title-Komponente der Referenz-Website &quot;We. Retail&quot;](https://github.com/Adobe-Marketing-Cloud/aem-sample-we-retail/blob/master/ui.apps/src/main/content/jcr_root/apps/weretail/components/content/title/.content.xml). Dies ist ein gutes Beispiel für eine Proxy-Komponente, die auf diese Weise aufgebaut ist.

## Laden der Core-Stile {#load-the-core-styles}

<!-- 

Comment Type: annotation
Last Modified By: ims-author-CE1E2CE451D1F0680A490D45@AdobeID
Last Modified Date: 2017-04-17T16:57:16.414-0400

Styles is odd in that most Core Components do not have CSS; very few even have structural CSS (breadcrumbs, list) It may be more apt to title this section: Load the Core JavaScript and CSS or Load the Core Client Libraries ?

 -->

<!-- 

Comment Type: annotation
Last Modified By: ims-author-CE1E2CE451D1F0680A490D45@AdobeID
Last Modified Date: 2017-04-17T17:41:37.115-0400

This section seems to cover the "sites" clientlibs for core components; Do we need a section for ensuring the editor clientlibs are loaded in the Page Editor? Pending: https://github.com/Adobe-Marketing-Cloud/aem-core-wcm-components/issues/15

 -->

<!-- 

Comment Type: annotation
Last Modified By: cotescu
Last Modified Date: 2018-03-09T10:45:52.812-0500

Load the Core Client Libraries sounds way better

 -->

1. Erstellen Sie eine [Client-Bibliothek](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/clientlibs.html) , die alle CSS- und JS-Dateien enthält, die für Ihre Site benötigt werden, falls noch nicht geschehen.
1. Fügen Sie in der Client-Bibliothek Ihrer Site die Abhängigkeiten zu den Core-Komponenten hinzu, die möglicherweise benötigt werden. Dies geschieht durch Hinzufügen einer `embed` Eigenschaft.

   Um beispielsweise die Client-Bibliotheken aller v 1 Core Components einzubeziehen, lautet die hinzuzufügende Eigenschaft:

   ```shell
   embed="[  
   core.wcm.components.image.v1,  
   core.wcm.components.list.v1,  
   core.wcm.components.breadcrumb.v1,  
   core.wcm.components.form.container.v1,  
   core.wcm.components.form.text.v1  
   ]"
   ```

Stellen Sie sicher, dass Ihre Proxy-Komponenten und Client-Bibliotheken in Ihrer AEM-Umgebung bereitgestellt wurden, bevor Sie zum nächsten Abschnitt wechseln.

## Komponenten zulassen {#allow-the-components}

Die folgenden Schritte werden normalerweise im [Vorlagen-Editor durchgeführt](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html), für vorhandene Setups jedoch möglicherweise im Designmodus:

1. Wählen Sie im Vorlageneditor (oder im Designmodus) den Layoutcontainer (oder die parsys) aus und öffnen Sie die Richtlinie (oder Design-Konfiguration).
1. Wählen Sie in der Liste der zulässigen Komponenten die zuvor erstellten Proxy-Komponenten aus, die unter der ihnen zugewiesenen Komponentengruppe angezeigt werden sollen. Übernehmen Sie anschließend die Änderungen.
1. Optional können sie für Komponenten mit einem Design-Dialogfeld vorkonfiguriert werden.

Auf den Seiten, die aus der bearbeiteten Vorlage erstellt wurden, sollten Sie jetzt die neu erstellten Komponenten verwenden können.

**Lesen Sie als Nächstes:**

* [Anpassen der Kernkomponenten](customizing.md) - um zu erfahren, wie Sie die Kernkomponenten gestalten und anpassen können.
* [Komponentenrichtlinien](guidelines.md) - um die Implementierungsmuster der Kernkomponenten zu erfahren.
