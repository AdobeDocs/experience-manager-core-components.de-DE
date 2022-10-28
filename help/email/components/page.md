---
title: E-Mail-Seitenkomponente
description: Die Komponente "E-Mail-Seite"
role: Architect, Developer, Admin, User
hidefromtoc: true
index: false
source-git-commit: 8bebe3ca036557f3f7c6b8ec0e65d6d104d5ffae
workflow-type: tm+mt
source-wordcount: '804'
ht-degree: 40%

---


# E-Mail-Seitenkomponente {#email-page-component}

Die E-Mail-Seitenkomponente ist eine Erweiterungskomponente für Seiten, die für die Verwendung mit der [Vorlageneditor](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=de) und ermöglicht die Zusammenstellung von Seitenkopf-/Fußzeilen- und Strukturkomponenten mit dem Vorlageneditor, die auf die Erstellung von Adobe Campaign-Inhalten zugeschnitten sind.

## Nutzung {#usage}

Die E-Mail-Seitenkomponente bildet die Grundlage aller Seiten, die mit den E-Mail-Kernkomponenten und bearbeitbaren Vorlagen erstellt wurden. Mithilfe der E-Mail-Seitenkomponente können Kopf- und Fußzeilen sowie die Seitenstruktur mithilfe der anderen E-Mail-Kernkomponenten als Vorlage definiert werden.

* Verwenden der [Dialogfeld &quot;Design&quot;](#design-dialog) Für die Seite können benutzerdefinierte Client-seitige Bibliotheken definiert werden.
* Im Gegensatz zu anderen Komponenten mit einem Bearbeitungsdialogfeld, auf das direkt über die Komponente zugegriffen werden kann, da die E-Mail-Seitenkomponente die Seite selbst ist, wird die [Dialogfeld &quot;Bearbeiten&quot;](#edit-dialog) der E-Mail-Seitenkomponente ist das Fenster mit den Seiteneigenschaften.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der E-Mail-Seitenkomponente ist v1, die mit Version X der E-Mail-Kernkomponenten im Oktober 2022 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|
| v1 | Kompatibel | Kompatibel |

Weitere Informationen zu E-Mail-Kernkomponentenversionen und -freigaben finden Sie im Dokument [Versionen der E-Mail-Kernkomponenten](/help/email/versions.md)

### Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur Seitenkomponente [finden Sie auf GitHub.](https://adobe.com/go/aem_cmp_tech_email_page_v1)

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Dialogfeld „Bearbeiten“ {#edit-dialog}

Da die Komponente die gesamte Seite darstellt, befinden sich Einstellungen, die normalerweise in einem Dialogfeld „Bearbeiten“ enthalten wären, im Fenster [Seiteneigenschaften](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html?lang=de).

### Registerkarte &quot;Cloud Services&quot; {#cloud-services}

Damit die E-Mail-Kernkomponenten Kampagnenvariablen und -daten abrufen können, muss die Seite mit einer Adobe Campaign-Konfiguration verknüpft sein.

![E-Mail-Seiteneigenschaften](/help/email/assets/email-page-properties.png)

under **Cloud Service-Konfiguration** -Überschrift in der Dropdown-Auswahl **Konfiguration hinzufügen**.

under **Adobe Campaign** -Überschrift die Konfiguration für Ihre Integration mit Adobe Campaign auswählen.

Siehe Dokument . [Verwenden von E-Mail-Kernkomponenten](/help/email/using.md) Weitere Informationen zum Einrichten der E-Mail-Kernkomponenten finden Sie.

### E-Mail-Tab {#email-tab}

Im Tab E-Mail werden die Eigenschaften von E-Mails definiert, die über Adobe Campaign basierend auf dem Inhalt dieser Seite gesendet werden, z. B. E-Mail-Betreff und Nur-Text-Inhalt.

![E-Mail-Seiteneigenschaften](/help/email/assets/email-page-properties-email.png)

* **Betreff** - Betreff der von Adobe Campaign auf dieser Seite gesendeten E-Mail
   * Klicken Sie auf **Adobe Campaign-Variable auswählen** Symbol zum Öffnen [Adobe Campaign-Variable auswählen](/help/email/campaign-variables.md) zum Einfügen von dynamischen Inhalten aus Adobe Campaign.
* **Pre-Header**
   * Klicken Sie auf **Adobe Campaign-Variable auswählen** Symbol zum Öffnen [Adobe Campaign-Variable auswählen](/help/email/campaign-variables.md) zum Einfügen von dynamischen Inhalten aus Adobe Campaign.
* **Nur Text** - Die Textversion der von Adobe Campaign gesendeten E-Mail
   * Klicken Sie auf **Adobe Campaign-Variable auswählen** Symbol zum Öffnen [Adobe Campaign-Variable auswählen](/help/email/campaign-variables.md) zum Einfügen von dynamischen Inhalten aus Adobe Campaign.
* **Referenz-URL**

## Dialogfeld „Design“ {#design-dialog}

Da die Komponente die gesamte Seite darstellt, wird das Dialogfeld „Design“ über **Seiteninformationen > Seitenrichtlinien** aufgerufen, wenn Sie die Seitenvorlage bearbeiten.

![Seitenrichtlinie](/help/assets/page-policy.png)

### Registerkarte „Eigenschaften“ {#properties-tab}

Mithilfe des Fensters „Seitendesign“ können Sie die zu ladenden Client-Bibliotheken sowie die Web-Ressourcenbibliothek für die Seite definieren.

![Design-Dialogfeld der E-Mail-Seitenkomponente](/help/email/assets/email-page-design.png)

* **Client-Bibliotheken** - Damit werden Kategorien der Client-Bibliothek definiert, die geladen werden. JavaScript wird am Textende hinzugefügt und das CSS wird dem Seitenkopf hinzugefügt.
* **Seitenkopf Client-Bibliotheken JavaScript** - Dadurch werden die Kategorien der JavaScript-Client-Bibliothek definiert, die im Seitenkopf geladen werden.
   * Kategorien, die hier definiert werden und auch im Feld **Client-Bibliotheken** vorhanden sind, haben JavaScript, das anstelle am Textende in der Seitenkopfzeile geladen wird.
   * Es wird keine CSS geladen, es sei denn, die Kategorie ist ebenfalls im Feld **Client-Bibliotheken** enthalten.
* **Asynchrones Laden von JavaScript-Bibliotheken** - Wenn diese Option aktiviert ist, werden die benutzerdefinierten JavaScript-Bibliotheken asynchron geladen.
* **Client-Bibliothek der Web-Ressourcen**
Die Kategorie der Client-Bibliothek, die verwendet wird, um Web-Ressourcen wie etwa Favicons zu bedienen.
* **Zur Auswahl des Hauptinhaltselements wechseln** - Wird als Barrierefreiheitsfunktion verwendet, um direkt zum Hauptinhalt der Seite zu springen.

Bibliotheken können wie folgt für die beiden Felder **Client-Bibliotheken** und **JavaScript-Seitenkopf der Client-Bibliotheken** konfiguriert werden:

* Um ein neues Feld hinzuzufügen, klicken oder tippen Sie auf die Schaltfläche **Hinzufügen** unterhalb der Felder.
* Um ein Feld zu entfernen, klicken oder tippen Sie auf das Papierkorbsymbol neben dem Feld, das entfernt werden soll.
* Um die Ladereihenfolge neu anzuordnen, klicken oder tippen Sie auf den Griff neben dem Feld, das verschoben werden soll, und ziehen Sie es.

Weitere Informationen zur Verwendung clientseitiger Bibliotheken finden Sie unter [Verwendung clientseitiger Bibliotheken.](https://helpx.adobe.com/de/experience-manager/6-5/sites/developing/using/clientlibs.html)

### Registerkarte „Arten“ {#styles-tab}

Die Seitenkomponente unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).
