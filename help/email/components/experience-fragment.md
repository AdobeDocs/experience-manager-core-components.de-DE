---
title: E-Mail-Experience-Fragment-Komponente
description: Mit der E-Mail-Experience-Fragment-Komponente kann der Inhaltsautor eine Experience Fragment-Variante in ihren Inhalt platzieren und dabei eine lokalisierte Inhaltsstruktur unterstützen.
role: Architect, Developer, Admin, User
exl-id: 861c1fd1-6d6d-426c-a338-a558326fe16e
source-git-commit: 33976c0e745ad091a142109f70541f01a31edc5b
workflow-type: tm+mt
source-wordcount: '927'
ht-degree: 27%

---


# E-Mail-Experience-Fragment-Komponente {#email-experience-fragment-component}

Mit der E-Mail-Experience-Fragment-Komponente kann der Inhaltsautor eine Experience Fragment-Variante in ihren Inhalt platzieren und dabei eine lokalisierte Inhaltsstruktur unterstützen.

## Nutzung {#usage}

Mit der E-Mail-Experience-Fragment-Komponente kann der Inhaltsautor aus vorhandenen Experience Fragment-Varianten auswählen und eine im Inhalt platzieren. Ein Experience Fragment ist eine Inhaltsgruppe, die sowohl Inhalt als auch Layout enthält und kanalübergreifend wiederverwendet werden kann.

* Die Eigenschaften der Komponente können im [Dialogfeld „Konfigurieren“](#configure-dialog) definiert werden.
* Standardwerte für die Komponente können beim Hinzufügen zum Inhalt im [Dialogfeld &quot;Design&quot;](#design-dialog).

Die Komponente E-Mail-Experience-Fragment unterstützt eine lokalisierte Site-Struktur.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der E-Mail-Experience-Fragment-Komponente ist v1, die mit Version X der E-Mail-Kernkomponenten im Oktober 2022 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|
| v1 | Kompatibel | Kompatibel |

Weitere Informationen zu den Versionen und Versionen der E-Mail-Kernkomponenten finden Sie im Dokument . [Versionen der E-Mail-Kernkomponenten.](/help/email/versions.md)

## Unterstützung für lokalisierte Site-Strukturen {#localized-site-structure}

Die E-Mail-Experience-Fragment-Komponente ist an lokalisierte Inhaltsstrukturen angepasst und stellt das richtige Experience Fragment basierend auf der Lokalisierung des Inhalts dar. Dazu muss das Experience Fragment die folgenden Bedingungen erfüllen.

* Die E-Mail-Experience-Fragment-Komponente wird zu einem [Seitenvorlage.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/features/templates.html)
* Diese Vorlage wird verwendet, um eine neue Inhaltsseite zu erstellen, die Teil einer lokalisierten Struktur unter `/content/<site>` ist.
* Das auf einer Inhaltsseite referenzierte Experience Fragment ist Teil einer lokalisierten Experience Fragment-Struktur unten `/content/experience-fragments` , die denselben Mustern wie die unten stehende Site folgt `/content/<site>` einschließlich der Verwendung der gleichen Komponentennamen.

In diesem Fall wird das Fragment mit derselben Lokalisierung ([Sprache, Blueprint oder Live Copy](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/administering/reusing-content/msm-and-translation.html)), da die aktuelle Seite als Teil der Vorlage gerendert wird.

Dieses Verhalten ist auf E-Mail-Experience-Fragment-Komponenten beschränkt, die zu Vorlagen hinzugefügt werden. Experience Fragment-Komponenten, die einzelnen Inhaltsseiten hinzugefügt werden, rendern die exakten Experience Fragment-Ausgabeformate, die innerhalb der Komponente konfiguriert sind.

* Ein Beispiel dafür, wie die Lokalisierungsfunktionen der Experience Fragment-Komponente funktionieren, finden Sie unter [den folgenden Abschnitt](#example).
* Ein Beispiel dafür, wie die Lokalisierungsfunktionen der Kernkomponenten zusammenarbeiten, finden Sie auf der Seite [Kernkomponenten](/help/get-started/localization.md) unter „Lokalisierungsfunktionen“.

### Beispiel {#example}

Nehmen wir an, dass Ihr Inhalt wie folgt aussieht:

```
/content
+-- experience-fragments
   \-- wknd
      +-- language-masters
      +-- us
         +-- en
            +-- footerTextXf
            \-- headerTextXf
         \-- es
            +-- footerTextXf
            \-- headerTextXf
      \-- ch
         +-- de
            +-- footerTextXf
            \-- headerTextXf
         +-- fr
            +-- footerTextXf
            \-- headerTextXf
         \-- it
            +-- footerTextXf
            \-- headerTextXf
+-- wknd
   +-- language-masters
   +-- us
      +-- en
      \-- es
   +-- ch
      +-- de
      +-- fr
      \-- it
+-- wknd-events
\-- wknd-shop
```

Beachten Sie, dass sich die Struktur unter `/content/experience-fragments/wknd` auf die Struktur von `/content/wknd` auswirkt.

In diesem Fall, wenn die Komponente E-Mail-Experience-Fragment `/content/experience-fragments/wknd/us/en/footerTextXf` auf einer Vorlage platziert wird, rendern die lokalisierten Seiten, die auf dieser Vorlage erstellt werden, automatisch das lokalisierte Experience Fragment, das der lokalisierten Inhaltsseite entspricht.

Wenn Sie also zu einer Inhaltsseite unter `/content/wknd/ch/de` navigieren, welche dieselbe Vorlage verwendet, wird `/content/experience-fragments/wknd/ch/de/footerTextXf` anstatt von `/content/experience-fragments/wknd/us/en/footerTextXf` gerendert.

### Notfallversorgung {#fallback}

Die E-Mail-Experience-Fragment-Komponente versucht in der folgenden Reihenfolge, eine entsprechende lokalisierte Komponente zu finden.

1. Zuerst wird versucht, einen Sprachstamm zu finden.
1. Wird dieser nicht gefunden, wird versucht, ein Blueprint zu finden.
1. Wenn auch dieses nicht gefunden werden, versucht sie, eine Live Copy zu finden.
1. Wenn es nicht gefunden wird, wird standardmäßig das in der Komponente konfigurierte Experience Fragment verwendet.

## Musterkomponentenausgabe {#sample-component-output}

Um die E-Mail-Experience-Fragment-Komponente zu erleben und Beispiele für ihre Konfigurationsoptionen sowie HTML- und JSON-Ausgaben anzuzeigen, besuchen Sie die [Komponentenbibliothek.](https://adobe.com/go/aem_cmp_library_email_xf)

## Technische Details {#technical-details}

Die neueste technische Dokumentation zur Experience Fragment-Komponente [finden Sie auf GitHub.](https://adobe.com/go/aem_cmp_email_tech_xf_v1)

Weitere Informationen zur Entwicklung der Kernkomponenten finden Sie im [Entwicklerdokumentation für Kernkomponenten.](/help/developing/overview.md)

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Im Dialogfeld &quot;Konfigurieren&quot;kann der Inhaltsautor die Experience Fragment-Variante auswählen, die im Inhalt wiedergegeben werden soll.

![Dialogfeld &quot;Bearbeiten&quot;der E-Mail-Experience-Fragment-Komponente](/help/email/assets/email-experience-fragment-edit.png)

Verwenden Sie die **Dialogfeld &quot;Auswahl öffnen&quot;** -Schaltfläche, um die Komponentenauswahl zu öffnen und auszuwählen, welche Experience Fragment-Komponentenvariante zur Inhaltsseite hinzugefügt werden soll.

Wenn Sie die E-Mail-Experience-Fragment-Komponente zu einer Vorlage hinzufügen, wird sie automatisch lokalisiert, sofern die Experience Fragments lokalisiert sind. Was auf der Seite gerendert wird, kann sich also von der Komponente unterscheiden, die Sie explizit auswählen. Weitere Informationen finden Sie im [oben stehenden Beispiel](#example).

Sie können auch eine **ID** festlegen. Diese Option ermöglicht die Steuerung der eindeutigen Kennung der Komponente im HTM.

* Wenn Sie das Feld leer lassen, wird automatisch eine eindeutige ID generiert, die Sie durch Überprüfen des resultierenden Inhalts finden können.
* Sofern eine ID angegeben wird, ist vom Autor sicherzustellen, dass diese eindeutig ist.
* Eine Änderung der ID kann sich auf CSS auswirken.

### Registerkarte „Stile“ {#styles-tab-edit}

Die E-Mail-Experience-Fragment-Komponente unterstützt die AEM [Stilsystem.](/help/get-started/authoring.md#component-styling)

Verwenden Sie das Dropdown-Menü, um die Stile auszuwählen, die Sie auf die Komponente anwenden möchten. Die im Dialogfeld „Bearbeiten“ vorgenommenen Auswahlen haben denselben Effekt wie die in der Komponenten-Symbolleiste ausgewählten.

Stile müssen für diese Komponente im [Dialogfeld &quot;Design&quot;](#design-dialog) , damit die Registerkarte verfügbar ist.

## Dialogfeld „Design“ {#design-dialog}

Im Dialogfeld &quot;Design&quot;kann der Vorlagenautor die Optionen definieren, die dem Inhaltsautor zur Verfügung stehen, der die E-Mail-Experience-Fragment-Komponente verwendet, sowie die Standardeinstellungen, die beim Platzieren der E-Mail-Experience-Fragment-Komponente festgelegt wurden.

### Registerkarte „Stile“ {#styles-tab}

Die E-Mail-Experience-Fragment-Komponente unterstützt die AEM [Stilsystem.](/help/get-started/authoring.md#component-styling)
