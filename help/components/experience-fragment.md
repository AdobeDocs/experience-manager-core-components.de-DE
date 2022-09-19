---
title: Experience Fragment-Komponente
description: Mit der Experience Fragment-Komponente kann der Inhaltsautor einer Seite eine Experience Fragment-Variation hinzufügen.
role: Architect, Developer, Admin, User
exl-id: 103f729a-084d-4b6a-a239-d8ef8902eb95
source-git-commit: 327c239b02e0aecee878784c918bfa98d960530e
workflow-type: ht
source-wordcount: '893'
ht-degree: 100%

---

# Experience Fragment-Komponente {#experience-fragment-component}

Mit der Kernkomponente „Experience Fragment-Komponente“ kann der Inhaltsautor eine Experience Fragment-Variante auf einer Seite platzieren, während er eine lokalisierte Site-Struktur unterstützt.

## Nutzung {#usage}

Mit der Kernkomponente Experience Fragment-Komponente kann der Inhaltsautor aus vorhandenen Experience Fragment-Variationen auswählen und eine davon auf der Inhaltsseite platzieren. Die Experience Fragment-Komponente unterstützt außerdem eine lokalisierte Site-Struktur.

* Die Eigenschaften der Komponente können im [Dialogfeld „Konfigurieren“](#configure-dialog) definiert werden.
* Die Standardeinstellungen für die Komponente beim Hinzufügen zu einer Seite können im [Dialogfeld „Design“](#design-dialog) definiert werden.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Experience Fragment-Komponente ist v2. Sie wurde mit Version 2.18.0 der Kernkomponenten im Februar 2022 eingeführt und wird in diesem Dokument beschrieben.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v2 | - | Kompatibel | Kompatibel |
| [v1](v1/experience-fragment.md) | Kompatibel | Kompatibel | Kompatibel |

Weitere Informationen zu Kernkomponentenversionen und -freigaben finden Sie in den [Kernkomponentenversionen](/help/versions.md).

## Unterstützung für lokalisierte Site-Strukturen {#localized-site-structure}

Die Experience Fragment-Komponente ist an lokalisierte Site-Strukturen anpassbar und gibt das richtige Experience-Fragment basierend auf der Lokalisierung der Seite wieder. Hierfür muss das Experience Fragment die folgenden Bedingungen erfüllen:

* Die Experience Fragment-Komponente wird zu einer Vorlage hinzugefügt.
* Diese Vorlage wird verwendet, um eine neue Inhaltsseite zu erstellen, die Teil einer lokalisierten Struktur unter `/content/<site>` ist.
* Das auf einer Inhaltsseite referenzierte Experience Fragment ist Teil einer lokalisierten Experience Fragment-Struktur unter `/content/experience-fragments`; dieselben Muster wie bei der Site unter `/content/<site>` werden befolgt, einschließlich der gleichen Komponentennamen.

In diesem Fall wird das Fragment mit derselben Lokalisierung (Sprache, Blueprint oder Live Copy) wie die aktuelle Seite als Teil der Vorlage gerendert.

Dieses Verhalten ist auf Experience Fragment-Komponenten beschränkt, die zu Vorlagen hinzugefügt werden. Experience Fragment-Komponenten, die einzelnen Inhaltsseiten hinzugefügt werden, rendern die exakten Experience Fragment-Komponenten, die innerhalb der Komponente konfiguriert wurden.

* Ein Beispiel dafür, wie die Lokalisierungsfunktion der Experience Fragment-Komponente funktioniert, finden Sie [unten](#example).
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

Wenn die Experience Fragment-Komponente `/content/experience-fragments/wknd/us/en/footerTextXf` in einer Vorlage platziert wird, rendern die lokalisierten Seiten, die basierend auf dieser Vorlage erstellt wurden, automatisch das lokalisierte Experience Fragment, welches der lokalisierten Inhaltsseite entspricht.

Wenn Sie also zu einer Inhaltsseite unter `/content/wknd/ch/de` navigieren, welche dieselbe Vorlage verwendet, wird `/content/experience-fragments/wknd/ch/de/footerTextXf` anstatt von `/content/experience-fragments/wknd/us/en/footerTextXf` gerendert.

### Notfallversorgung {#fallback}

Die Experience Fragment-Komponente wird wie folgt versuchen, eine entsprechende lokalisierte Komponente zu finden.

1. Zuerst wird versucht, einen Sprachstamm zu finden.
1. Wird dieser nicht gefunden, wird versucht, ein Blueprint zu finden.
1. Wenn auch dieses nicht gefunden werden, versucht sie, eine Live Copy zu finden.
1. Falls keine Live-Copy gefunden wurde, wird standardmäßig das in der Komponente konfigurierte Experience Fragment verwendet.

## Musterkomponentenausgabe {#sample-component-output}

Rufen Sie die [Komponentenbibliothek](https://adobe.com/go/aem_cmp_library_xf) auf, um die Experience Fragment-Komponente sowie die Beispiele für ihre Konfigurationsoptionen und die HTML- und JSON-Ausgabe zu testen.

## Technische Details {#technical-details}

Die neueste technische Dokumentation zur Experience Fragment-Komponente [finden Sie auf GitHub](https://adobe.com/go/aem_cmp_tech_xf_v2_de).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Das Dialogfeld „Konfigurieren“ ermöglicht dem Inhaltsautor die Auswahl der Experience Fragment-Variante, die auf der Seite gerendert werden soll.

![Dialogfeld „Bearbeiten“ der Experience Fragment-Komponente](/help/assets/experience-fragment-edit.png)

Verwenden Sie die Schaltfläche **Auswahldialog öffnen**, um die Komponentenauswahl zu öffnen und auszuwählen, welche Variation der Experience Fragment-Komponente zur Inhaltsseite hinzugefügt werden soll.

Wenn Sie die Experience Fragment-Komponente zu einer Vorlage hinzufügen, wird sie automatisch lokalisiert, sofern die Experience Fragments lokalisiert sind. Was auf der Seite gerendert wird, kann sich daher von der Komponente unterscheiden, die Sie explizit auswählen. Weitere Informationen finden Sie im [oben stehenden Beispiel](#example).

Sie können auch eine **ID** festlegen. Diese Option dient zur Kontrolle der eindeutigen Kennung der Komponente in der HTML-Datei und auf der [Datenschicht](/help/developing/data-layer/overview.md).

* Wenn Sie das Feld leer lassen, wird automatisch eine eindeutige ID generiert, die Sie über die resultierende Seite finden.
* Sofern eine ID angegeben wird, ist vom Autor sicherzustellen, dass diese eindeutig ist.
* Änderungen der ID können sich auf das CSS-, JS- und Datenschicht-Tracking auswirken.

### Registerkarte „Arten“ {#styles-tab-edit}

![Registerkarte „Arten“ im Dialogfeld „Bearbeiten“ der Inhaltsfragmentlisten-Komponente](/help/assets/experience-fragment-edit-styles.png)

Die Experience Fragment-Komponente unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).

Verwenden Sie das Dropdown-Menü, um die Stile auszuwählen, die Sie auf die Komponente anwenden möchten. Die im Dialogfeld „Bearbeiten“ vorgenommenen Auswahlen haben denselben Effekt wie die in der Komponenten-Symbolleiste ausgewählten.

Stile müssen für diese Komponente im [Dialogfeld „Design“](#design-dialog) konfiguriert werden, damit das Dropdown-Menü verfügbar ist.

## Dialogfeld „Design“ {#design-dialog}

Über das Dialogfeld „Design“ kann der Vorlagenautor die Optionen definieren, die dem Inhaltsautor zur Verfügung stehen, der die Experience Fragment-Komponente verwendet, sowie auch die Standardeinstellungen, die beim Platzieren der Experience Fragment-Komponente festgelegt wurden.

### Registerkarte „Arten“ {#styles-tab}

Die Experience Fragment-Komponente unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).
