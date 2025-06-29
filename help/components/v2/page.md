---
title: Seitenkomponente (v2)
description: Die Seitenkomponente ist eine Erweiterungskomponente für Seiten, die mit dem Vorlageneditor arbeitet und es ermöglicht, Seitenkopf-/Fußzeilen- und Strukturkomponenten mit dem Vorlageneditor zusammenzustellen.
role: Architect, Developer, Admin, User
exl-id: e85fe4db-6de4-4a84-a54c-bd07a67efed3
index: n
source-git-commit: 92a3ec273a5be6751c1503835b9c2e5cbd61bb9e
workflow-type: ht
source-wordcount: '618'
ht-degree: 100%

---


# Seitenkomponente (v2) {#page-component}

Die Seitenkomponente ist eine Erweiterungskomponente für Seiten, die mit dem [Vorlageneditor](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=de) arbeitet und es ermöglicht, Seitenkopf-/Fußzeilen- und Strukturkomponenten mit dem Vorlageneditor zusammenzustellen.

## Nutzung {#usage}

Die Seitenkomponente bildet die Grundlage aller Seiten, die mit den Kernkomponenten entworfen wurden, sowie bearbeitbarer Vorlagen. Mithilfe der Seitenkomponente können Kopfzeilen, Fußzeilen und die Struktur der Seite unter Verwendung der anderen Kernkomponenten als Vorlage definiert werden.

Im [Dialogfeld „Design“](#design-dialog) können benutzerdefinierte Client-seitige Bibliotheken für die Seite definiert werden. Im Gegensatz zu anderen Komponenten, die ein Dialogfeld „Bearbeiten“ haben, auf das direkt von der Komponente aus zugegriffen werden kann, weil die Komponente die Seite selbst ist, ist das [Dialogfeld „Bearbeiten“](#edit-dialog) der Seitenkomponente das Fenster „Seiteneigenschaften“.

## Version und Kompatibilität {#version-and-compatibility}

In diesem Dokument wird die v2 der Seitenkomponente beschrieben, die ursprünglich mit Version 2.0.0 der Kernkomponenten im Januar 2018 eingeführt wurde.

>[!CAUTION]
>
>In diesem Dokument wird die v2 der Seitenkomponente beschrieben.
>
>Weitere Informationen zur aktuellen Version der Seitenkomponente finden Sie im Dokument [Seitenkomponente](/help/components/page.md).

## Unterstützung von Progressive Web Apps {#pwa-support}

Mit Version 2.15.0 der Kernkomponenten wurde die Unterstützung für die in AEM as a Cloud Service integrierten Funktionen für [Progressive Web Apps (PWA).](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/enable-pwa.html?lang=de) eingeführt. Mit einer einfachen Konfiguration auf Website-Ebene verwandeln Sie Ihr AEM-Erlebnis in eine PWA!

### Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur Seitenkomponente [finden Sie auf GitHub](https://adobe.com/go/aem_cmp_tech_page_v2_de).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Dialogfeld „Bearbeiten“ {#edit-dialog}

Da die Komponente die gesamte Seite darstellt, befinden sich Einstellungen, die normalerweise in einem Dialogfeld „Bearbeiten“ enthalten wären, im Fenster [Seiteneigenschaften](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html?lang=de).

## Dialogfeld „Design“ {#design-dialog}

Da die Komponente die gesamte Seite darstellt, wird das Dialogfeld „Design“ über **Seiteninformationen > Seitenrichtlinien** aufgerufen, wenn Sie die Seitenvorlage bearbeiten.

![Seitenrichtlinie](/help/assets/page-policy.png)

>[!NOTE]
>
>In früheren Versionen von AEM hieß die **Seitenrichtlinie** noch **Seitendesign**.

### Registerkarte „Eigenschaften“ {#properties-tab}

Mithilfe des Fensters „Seitendesign“ können Sie die zu ladenden Client-Bibliotheken sowie die Web-Ressourcenbibliothek für die Seite definieren.

* **Client-Bibliotheken** - Damit werden Kategorien der Client-Bibliothek definiert, die geladen werden. JavaScript wird am Textende hinzugefügt und das CSS wird dem Seitenkopf hinzugefügt.
* **JavaScript-Seitenkopf der Client-Bibliotheken**
Definiert die Kategorien der JavaScript-Client-Bibliothek, die im Seitenkopf geladen werden.
   * Kategorien, die hier definiert werden und auch im Feld **Client-Bibliotheken** vorhanden sind, haben JavaScript, das anstelle am Textende in der Seitenkopfzeile geladen wird.
   * Es wird keine CSS geladen, es sei denn, die Kategorie ist ebenfalls im Feld **Client-Bibliotheken** enthalten.

* **Client-Bibliothek der Web-Ressourcen**
Die Kategorie der Client-Bibliothek, die verwendet wird, um Web-Ressourcen wie etwa Favicons zu bedienen.

* **Zur Auswahl des Hauptinhaltselements wechseln** - Wird als Barrierefreiheitsfunktion verwendet, um direkt zum Hauptinhalt der Seite zu springen.

![Dialogfeld „Design“ der Seitenkomponente](/help/assets/page-design.png)

Bibliotheken können wie folgt für die beiden Felder **Client-Bibliotheken** und **JavaScript-Seitenkopf der Client-Bibliotheken** konfiguriert werden:

* Um ein neues Feld hinzuzufügen, klicken oder tippen Sie auf die Schaltfläche **Hinzufügen** unter den Feldern.
* Um ein Feld zu entfernen, klicken oder tippen Sie neben dem Feld, das entfernt werden soll, auf das Papierkorbsymbol.
* Um die Ladereihenfolge neu anzuordnen, klicken oder tippen Sie auf den Griff neben dem Feld, das verschoben werden soll, und ziehen Sie es.

Weitere Informationen zur Verwendung clientseitiger Bibliotheken finden Sie unter [Verwendung clientseitiger Bibliotheken](https://helpx.adobe.com/de/experience-manager/6-5/sites/developing/using/clientlibs.html).

>[!CAUTION]
>
>Die Möglichkeit, Client-Bibliotheken für den Seitenkopf separat zu definieren, wurde mit Version 2.2.0 der Kernkomponenten eingeführt.

### Registerkarte „Arten“ {#styles-tab}

Die Seitenkomponente unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).

## Adobe Client-Datenschicht {#data-layer}

Die Seitenkomponente unterstützt die [Adobe Client-Datenschicht](/help/developing/data-layer/overview.md).
