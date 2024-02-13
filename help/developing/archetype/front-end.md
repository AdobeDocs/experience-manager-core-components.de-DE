---
title: Frontend-Entwicklung mit dem AEM-Projektarchetyp
description: Erfahren Sie mehr über den optionalen, dedizierten Frontend-Build-Mechanismus des AEM-Projektarchetyps, der auf Webpack basiert.
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: 99132b49-bd06-4ac2-9348-12c0dfdfe8b2
source-git-commit: bd92a5d1884056ca7b44ea28e5817d8bde10a4d9
workflow-type: ht
source-wordcount: '654'
ht-degree: 100%

---


# Frontend-Entwicklung mit dem AEM-Projektarchetyp {#front-end}

Der AEM-Projektarchetyp enthält einen optionalen, dedizierten Frontend-Build-Mechanismus, der auf Webpack basiert. Das ui.frontend-Modul wird damit zum zentralen Speicherort für alle Frontend-Ressourcen des Projekts, einschließlich JavaScript- und CSS-Dateien. Um diese nützliche und flexible Funktion in vollem Umfang nutzen zu können, müssen Sie wissen, welchen Anteil die Frontend-Entwicklung an einem AEM-Projekt hat.

Dieses Dokument konzentriert sich auf allgemeine Nutzungsmuster des Frontend-Build-Moduls und dessen Funktionen für Sie. Detaillierte Build-Optionen und technische Anweisungen finden Sie in der Dokumentation im GitHub-Repository des Archetyps.

>[!TIP]
>
>Den neuesten AEM-Projektarchetyp und alle damit verbundenen technischen Details [finden Sie auf GitHub](https://github.com/adobe/aem-project-archetype).

## AEM-Frontend- und Backend-Entwicklung {#front-end-back-end}

In stark vereinfachten Begriffen kann davon ausgegangen werden, dass AEM-Projekte aus zwei separaten, aber miteinander verbundenen Teilen bestehen:

* Backend-Entwicklung, die die Logik von AEM unterstützt und Java-Bibliotheken, OSGi-Dienste usw. produziert
* Frontend-Entwicklung, die die Präsentation und das Verhalten der resultierenden Website steuert und JavaScript- sowie CSS-Bibliotheken erzeugt

Da sich diese beiden Entwicklungsprozesse auf verschiedene Teile des Projekts konzentrieren, kann die Backend- und Frontend-Entwicklung parallel erfolgen.

![Diagramm zum Frontend-Workflow](/help/assets/front-end-flow.png)

Jedes daraus resultierende Projekt muss jedoch die Ergebnisse beider Entwicklungsmaßnahmen nutzen, d. h. sowohl für das Backend als auch für das Frontend.

## Bestimmen des Markups {#determining-markup}

Unabhängig davon, welchen Frontend-Entwicklungs-Workflow Sie für Ihr Projekt implementieren, müssen sich die Backend-Entwickler und Frontend-Entwickler zunächst auf das Markup einigen. In der Regel definiert AEM das Markup, das von den Core-Komponenten bereitgestellt wird. [Dies kann jedoch bei Bedarf angepasst werden.](/help/developing/customizing.md#customizing-the-markup)

## Mögliche Frontend-Entwicklungs-Workflows {#possible-workflows}

Das Frontend-Build-Modul ist ein nützliches und sehr flexibles Werkzeug ohne spezielle Vorgaben dazu, wie es verwendet werden sollte. Im Folgenden finden Sie zwei Beispiele für die *mögliche* Verwendung, aber Ihre individuellen Projektanforderungen können andere Anwendungsmodelle erforderlich machen.

### Verwenden des statischen Webpack Development Servers {#using-webpack}

Mit Webpack können Sie auf Basis der statischen Ausgabe von AEM-Webseiten innerhalb des ui.frontend-Moduls formatieren und entwickeln.

1. Zeigen Sie eine Vorschau der Seite in AEM an oder geben Sie `wcmmode=disabled` in die URL ein.
1. Zeigen Sie die Seitenquelle an und speichern Sie diese als statischen HTML-Code im ui.frontend-Modul.
1. [Starten Sie Webpack](#webpack-dev-server) und beginnen Sie mit der Formatierung und Generierung des erforderlichen JavaScript- und CSS-Codes.
1. Führen Sie `npm run dev` zum Generieren der Clientlibs aus.

In diesem Workflow kann ein AEM-Entwickler die Schritte 1 und 2 ausführen sowie den statischen HTML-Code an den Front-End-Entwickler weiterleiten, der die AEM-HTML-Ausgabe zur Entwicklung nutzt.

>[!TIP]
>
>Man kann auch mit der [Komponentenbibliothek](https://adobe.com/go/aem_cmp_library_de) Beispiele der Markup-Ausgabe jeder Komponente erfassen, um auf Komponentenebene und nicht auf Seitenebene zu arbeiten.

### Verwenden von Storybook {#using-storybook}

Mit [Storybook](https://storybook.js.org) können Sie mehr atomare Frontend-Entwicklung durchführen. Obwohl Storybook nicht im AEM-Projektarchetyp enthalten ist, können Sie die Anwendung installieren und Ihre Storybook-Artefakte im ui.frontend-Modul speichern. Sobald diese für Tests in AEM bereit sind, können sie durch Ausführen von `npm run dev` als Clientlibs bereitgestellt werden.

>[!NOTE]
>
>[Storybook](https://storybook.js.org) ist nicht im AEM-Projektarchetyp enthalten. Wenn Sie das Programm verwenden möchten, müssen Sie es separat installieren.

## Überblick über Clientlibs {#clientlibs}

Das Frontend-Modul wird mithilfe einer [AEM-Clientlib bereitgestellt.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/full-stack/clientlibs.html?lang=de). Beim Ausführen des NPM-Build-Skripts wird die Anwendung gebaut und das Paket `aem-clientlib-generator` nimmt die resultierende Build-Ausgabe und wandelt sie in eine solche Clientlib um.

Eine Clientlib besteht aus den folgenden Dateien und Verzeichnissen:

* `css/`: CSS-Dateien, die im HTML-Code angefordert werden können
* `css.txt`: Teilt AEM die Reihenfolge und Namen der Dateien in `css/` mit, damit sie zusammengeführt werden können
* `js/`: JavaScript-Dateien, die im HTML-Code angefordert werden können
* `js.txt`: Teilt AEM die Reihenfolge und Namen der Dateien in `js/` mit, damit sie zusammengeführt werden können
* `resources/`: Quellzuordnungen, Nicht-Einstiegspunkt-Codeblöcke (die aus der Codeaufteilung resultieren), statische Kreativelemente (z. B. Symbole) usw.

>[!TIP]
>
>Erfahren Sie in der [AEM-Entwicklungsdokumentation](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/full-stack/clientlibs.html?lang=de) mehr darüber, wie AEM mit Clientlibs umgeht, und in der [Kernkomponenten-Dokumentation](/help/developing/including-clientlibs.md), wie Sie sie einbinden.
