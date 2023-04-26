---
title: Komponente „E-Mail-Seite“
description: Die Komponente „E-Mail-Seite“
role: Architect, Developer, Admin, User
exl-id: 17fd0f5e-2b85-41a1-abaf-8ad190a5341a
source-git-commit: c16dd8696e89f89c7b178ece11f57a565d73588b
workflow-type: ht
source-wordcount: '803'
ht-degree: 100%

---


# Komponente „E-Mail-Seite“ {#email-page-component}

Die Komponente „E-Mail-Seite“ ist eine erweiterbare Seitenkomponente, die mit dem [Vorlageneditor](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=de) zusammenarbeitet. Sie ermöglicht es, mit dem Vorlageneditor Kopfzeilen-, Fußzeilen- und Strukturkomponenten zusammenzustellen, die zur Inhalterstellung in Adobe Campaign verwendet werden können.

## Verwendung {#usage}

Die Komponente „E-Mail-Seite“ bildet die Grundlage für alle Seiten, die mit den Kernkomponenten für E-Mails entworfen wurden, sowie für bearbeitbare Vorlagen. Mithilfe der Komponente „E-Mail-Seite“ können Kopfzeilen, Fußzeilen und die Struktur der Seite unter Verwendung der anderen E-Mail-Kernkomponenten als Vorlage definiert werden.

* Im [Dialogfeld „Design“](#design-dialog) können benutzerdefinierte Client-seitige Bibliotheken für die Seite festgelegt werden.
* Im Gegensatz zu anderen Komponenten, die das Dialogfeld „Bearbeiten“ aufweisen, auf das direkt über die Komponente zugegriffen werden kann, entspricht dem [Dialogfeld „Bearbeiten“](#edit-dialog) der Komponente „E-Mail-Seite“ das Fenster „Seiteneigenschaften“, weil die Komponente die Seite selbst ist.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Komponente „E-Mail-Seite“ ist v1. Sie wurde mit dem Release X der E-Mail-Kernkomponenten im Oktober 2022 eingeführt und wird in diesem Dokument beschrieben.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|
| v1 | Kompatibel | - |

Weitere Informationen zu Versionen und Releases der E-Mail-Kernkomponente finden Sie im Dokument [Versionen der E-Mail-Kernkomponente](/help/email/versions.md).

### Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur Seitenkomponente [finden Sie auf GitHub](https://adobe.com/go/aem_cmp_tech_email_page_v1).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Dialogfeld „Bearbeiten“ {#edit-dialog}

Da die Komponente die gesamte Seite darstellt, befinden sich Einstellungen, die normalerweise in einem Dialogfeld „Bearbeiten“ enthalten wären, im Fenster [Seiteneigenschaften](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html?lang=de).

### Registerkarte „Cloud-Services“ {#cloud-services}

Damit die E-Mail-Kernkomponenten Kampagnenvariablen und -daten abrufen können, muss die Seite mit einer Konfigeration von Adobe Campaign verknüpft sein.

![Eigenschaften der E-Mail-Seite](/help/email/assets/email-page-properties.png)

Wählen Sie unter der Überschrift **Cloud-Service-Konfiguration** in der Dropdown-Liste **Konfiguration hinzufügen**.

Wählen Sie unter der Überschrift **Adobe Campaign** die Konfiguration für Ihre Integration mit Adobe Campaign.

Weitere Informationen zum Einrichten der E-Mail-Kernkomponenten finden Sie im Dokument [Verwenden der E-Mail-Kernkomponenten](/help/email/using.md).

### Registerkarte „E-Mail“ {#email-tab}

Auf der Registerkarte „E-Mail“ werden die Eigenschaften von E-Mails definiert, die basierend auf dem Inhalt dieser Seite über Adobe Campaign gesendet werden, wie etwa der E-Mail-Betreff und der Inhalt im Plain-Text-Format.

![Eigenschaften der E-Mail-Seite](/help/email/assets/email-page-properties-email.png)

* **Betreff** – Betreff der von Adobe Campaign gesendeten E-Mail, basierend auf dieser Seite
   * Klicken Sie auf das Symbol **Adobe Campaign-Variable auswählen**, um den Dialog [Adobe Campaign-Variable auswählen](/help/email/campaign-variables.md) zu öffnen und dynamische Inhalte aus Adobe Campaign einzufügen.
* **Pre-Header**
   * Klicken Sie auf das Symbol **Adobe Campaign-Variable auswählen**, um den Dialog [Adobe Campaign-Variable auswählen](/help/email/campaign-variables.md) zu öffnen und dynamische Inhalte aus Adobe Campaign einzufügen.
* **Nur Text** – Die Textversion der von Adobe Campaign gesendeten E-Mail
   * Klicken Sie auf das Symbol **Adobe Campaign-Variable auswählen**, um den Dialog [Adobe Campaign-Variable auswählen](/help/email/campaign-variables.md) zu öffnen und dynamische Inhalte aus Adobe Campaign einzufügen.
* **Referenz-URL**

## Dialogfeld „Design“ {#design-dialog}

Da die Komponente die gesamte Seite darstellt, wird das Dialogfeld „Design“ über **Seiteninformationen > Seitenrichtlinien** aufgerufen, wenn Sie die Seitenvorlage bearbeiten.

![Seitenrichtlinie](/help/assets/page-policy.png)

### Registerkarte „Eigenschaften“ {#properties-tab}

Mithilfe des Fensters „Seitendesign“ können Sie die zu ladenden Client-Bibliotheken sowie die Web-Ressourcenbibliothek für die Seite definieren.

![Dialogfeld „Design“ der Komponente „E-Mail-Seite“](/help/email/assets/email-page-design.png)

* **Client-Bibliotheken** - Damit werden Kategorien der Client-Bibliothek definiert, die geladen werden. JavaScript wird am Textende hinzugefügt und das CSS wird dem Seitenkopf hinzugefügt.
* **JavaScript-Seitenkopf der Client-Bibliotheken** – Definiert die Kategorien der JavaScript-Client-Bibliothek, die im Seitenkopf geladen werden.
   * Kategorien, die hier definiert werden und auch im Feld **Client-Bibliotheken** vorhanden sind, haben JavaScript, das anstelle am Textende in der Seitenkopfzeile geladen wird.
   * Es wird keine CSS geladen, es sei denn, die Kategorie ist ebenfalls im Feld **Client-Bibliotheken** enthalten.
* **JavaScript-Bibliotheken asynchron laden** – Wenn diese Option aktiviert ist, werden die benutzerdefinierten JavaScript-Bibliotheken asynchron geladen.
* **Client-Bibliothek der Web-Ressourcen**
Die Kategorie der Client-Bibliothek, die verwendet wird, um Web-Ressourcen wie etwa Favicons zu bedienen.
* **Zur Auswahl des Hauptinhaltselements wechseln** - Wird als Barrierefreiheitsfunktion verwendet, um direkt zum Hauptinhalt der Seite zu springen.

Bibliotheken können für die beiden Felder **Client-Bibliotheken** und **JavaScript-Seitenkopf der Client-Bibliotheken** wie folgt konfiguriert werden:

* Um ein neues Feld hinzuzufügen, klicken oder tippen Sie auf die Schaltfläche **Hinzufügen** unter den Feldern.
* Um ein Feld zu entfernen, klicken oder tippen Sie auf das Papierkorbsymbol neben dem entsprechenden Feld.
* Um die Ladereihenfolge neu anzuordnen, klicken oder tippen Sie auf den Griff neben dem Feld, das verschoben werden soll, und ziehen Sie es.

Weitere Informationen zur Verwendung Client-seitiger Bibliotheken finden Sie unter [Verwendung Client-seitiger Bibliotheken](https://helpx.adobe.com/de/experience-manager/6-5/sites/developing/using/clientlibs.html).

### Registerkarte „Arten“ {#styles-tab}

Die Seitenkomponente unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).
