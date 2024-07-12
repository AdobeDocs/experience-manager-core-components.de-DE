---
title: AEM-Projektarchetyp
description: Erfahren Sie mehr über den AEM-Projektarchetyp, der als Vorlage für AEM-basierte Anwendungen dient.
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: 58994726-9b65-4035-9d45-60b745d577bb
source-git-commit: 8940285f4c5e5870b6a135dac674f06e4c1d8b5a
workflow-type: tm+mt
source-wordcount: '527'
ht-degree: 100%

---


# AEM-Projektarchetyp {#aem-project-archetype}

Der AEM-Projektarchetyp ist eine Maven-Vorlage, anhand derer ein minimales, auf Best Practices basierendes Adobe Experience Manager(AEM)-Projekt als Ausgangspunkt für Ihre Website erstellt wird. Diese Dokumentation bietet einen Überblick über die Vorteile des Archetyps und die allgemeine Verwendung. Ausführliche technische Anweisungen und Dokumentation finden Sie im GitHub-Repository für Archetypen.

>[!TIP]
>
>Den neuesten AEM-Projektarchetyp und alle damit verbundenen technischen Details [finden Sie auf GitHub](https://github.com/adobe/aem-project-archetype).

## Gründe für die Verwendung des Archetyps {#why-use-the-archetype}

Mithilfe des AEM-Projektarchetyps können Sie auf dem Weg zum Aufbau eines AEM-Projekts mit bewährten Verfahren und nur wenigen Tastenanschlägen beginnen. Durch Verwendung des Archetyps werden alle Teile bereits vorhanden sein, sodass das resultierende Projekt minimal ist, es jedoch bereits alle [Schlüsselfunktionen](/help/developing/archetype/using.md#what-you-get) von AEM implementiert, sodass Sie nur auf dem Aufbau aufbauen und erweitern müssen.

Natürlich gibt es viele Elemente, die mit [einem erfolgreichem AEM-Projekt](/help/developing/success.md) einhergehen, aber die Verwendung des AEM-Projektarchetyps ist eine solide Grundlage und wird dringend für jedes AEM-Projekt empfohlen.

## Funktionen {#features}

* **Best Practice:** Laden Sie Ihre Website mit den neuesten empfohlenen Verfahren von Adobe.
* **Wenig Code:** Bearbeiten Sie Ihre Vorlagen, erstellen Sie Inhalte, stellen Sie Ihre CSS bereit und Ihre Website kann live geschaltet werden.
* **Cloud-fähig:** Falls gewünscht, verwenden Sie [AEM as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/landing/home.html?lang=de), um in wenigen Tagen live zu gehen und Skalierbarkeit und Wartung zu erleichtern.
* **Dispatcher:** Ein Projekt ist nur mit einer [Dispatcher-Konfiguration](https://experienceleague.adobe.com/docs/experience-manager-dispatcher/using/dispatcher.html?lang=de), die Geschwindigkeit und Sicherheit gewährleistet, abgeschlossen.
* **Mehrere Websites:** Bei Bedarf generiert der Archetyp die Inhaltsstruktur für eine [Konfigurationen mit mehreren Sprachen und Regionen](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/administering/reusing-content/msm/overview.html?lang=de).
* **Kernkomponenten:** Autoren können mit unserem vielseitigen [Satz standardisierter Komponenten](/help/introduction.md) nahezu jedes Layout erstellen.
* **Bearbeitbare Vorlagen:** Stellen Sie praktisch jede [Vorlage ohne Code](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/page-authoring/template-editor-feature-video-use.html?lang=de) zusammen und legen Sie fest, was die Autoren bearbeiten dürfen.
* **Responsives Layout:** Definieren Sie auf Vorlagen oder einzelnen Seiten, [wie die Elemente die definierten Breakpoints umfließen](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/get-started/localization.html?lang=de).
* **Kopf- und Fußzeile:** Stellen Sie sie mithilfe der [Lokalisierungsfunktionen der Komponenten](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/get-started/localization.html?lang=de) ohne Code zusammen und lokalisieren Sie sie.
* **Stilsystem:** Vermeiden Sie das Erstellen benutzerdefinierter Komponenten, indem Autoren [verschiedene Stile anwenden](https://experienceleague.adobe.com/docs/experience-manager-learn/getting-started-wknd-tutorial-develop/project-archetype/style-system.html?lang=de) können.
* **Frontend-Build:** Mit Webpack, TypeScript und SASS können Frontend-Entwickelnde [AEM-Seiten modellieren und Client-Bibliotheken erstellen](front-end.md).
* **Web-App-fähig:** Verwenden Sie für Websites, die React oder Angular verwenden, das [SPA SDK](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/hybrid/developing.html?lang=de), um die [kontextbezogene Inhaltserstellung der App](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html?lang=de) beizubehalten.
* **Commerce aktiviert:** Für Projekte, die [AEM Commerce](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/home.html?lang=de) mithilfe der [Commerce-Kernkomponenten](https://github.com/adobe/aem-core-cif-components) mit Commerce-Lösungen wie [Magento](https://magento.com/de) integrieren möchten.
* **Beispiel-Code:** Sehen Sie sich die Komponente „HelloWorld“ und die Beispielmodelle, -Servlets, -filter und -planungen an.
* **Open Source:** Wenn etwas nicht so ist, wie es sein sollte, [bringen](https://github.com/adobe/aem-core-wcm-components/blob/master/CONTRIBUTING.md) Sie Ihre Verbesserungen ein!

## Weiterführende Literatur {#further-reading}

* **[AEM-Projektarchetyp GitHub:](https://github.com/adobe/aem-project-archetype)** Vollständige Nutzung und technische Details des Archetyps
* **[Verwenden des Archetyps:](using.md)** Einen Überblick über die Verwendung des Archetyps in Ihrem Projekt und der daraus resultierenden Module
* **[Frontend-Entwicklung mit dem AEM-Projektarchetyp:](front-end.md)** Verwendung des Frontend-Moduls des Archetyps
* **Die folgenden Tutorials basieren auf diesem Archetyp:**
   * **[WKND-Site:](https://experienceleague.adobe.com/docs/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html?lang=de)** Erfahren Sie, wie Sie eine neue Website beginnen.
   * **[WKND Single Page App:](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html?lang=de)** Erfahren Sie, wie Sie eine Web-App für React oder Angular erstellen, die vollständig in AEM erstellt werden kann.
