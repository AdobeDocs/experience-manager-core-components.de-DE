---
title: E-Mail-Experience-Fragment-Komponente
description: Mit der E-Mail-Experience-Fragment-Komponente kann der Inhaltsautor bzw. die Inhaltsautorin eine Experience Fragment-Variation im Inhalt platzieren, während eine lokalisierte Inhaltsstruktur unterstützt wird.
role: Architect, Developer, Admin, User
exl-id: 861c1fd1-6d6d-426c-a338-a558326fe16e
index: false
source-git-commit: eb77567dc32cccb81a9fc131493d11fb55b7e93b
workflow-type: tm+mt
source-wordcount: '865'
ht-degree: 100%

---


# E-Mail-Experience-Fragment-Komponente {#email-experience-fragment-component}

Mit der E-Mail-Experience-Fragment-Komponente kann der Inhaltsautor bzw. die Inhaltsautorin eine Experience Fragment-Variation im Inhalt platzieren, während eine lokalisierte Inhaltsstruktur unterstützt wird.

## Verwendung {#usage}

Mit der E-Mail-Experience-Fragment-Komponente kann der Inhaltsautor bzw. die Inhaltsautorin aus vorhandenen Experience Fragment-Variationen auswählen und eine davon im Inhalt platzieren. Ein Experience Fragment ist eine Inhaltsgruppe, die sowohl Inhalt als auch Layout enthält und kanalübergreifend wiederverwendet werden kann.

* Die Eigenschaften der Komponente können im [Dialogfeld „Konfigurieren“](#configure-dialog) definiert werden.
* Standardeinstellungen für die Komponente beim Hinzufügen zum Inhalt kann im [Dialogfeld „Design“](#design-dialog) definiert werden.

Die E-Mail-Experience-Fragment-Komponente unterstützt eine lokalisierte Site-Struktur.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der E-Mail-Experience Fragment-Komponente ist v1. Sie wurde mit dem Release X der E-Mail-Kernkomponenten im Oktober 2022 eingeführt und wird in diesem Dokument beschrieben.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|---|---|---|---|
| v1 | Kompatibel | – | – |

Weitere Informationen zu E-Mail-Kernkomponentenversionen und -Releases finden Sie im Dokument [Kernkomponentenversionen](/help/email/versions.md).

## Unterstützung für lokalisierte Site-Strukturen {#localized-site-structure}

Die E-Mail-Experience-Fragment-Komponente ist an lokalisierte Inhaltsstrukturen anpassbar und gibt das richtige Experience Fragment basierend auf der Lokalisierung des Inhalts wieder. Hierfür muss das Experience Fragment die folgenden Bedingungen erfüllen:

* Die Experience Fragment-Komponente wird zu einer [Seitenvorlage](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/features/templates.html?lang=de) hinzugefügt.
* Diese Vorlage wird verwendet, um eine neue Inhaltsseite zu erstellen, die Teil einer lokalisierten Struktur unter `/content/<site>` ist.
* Das auf eine Inhaltsseite referenzierte Experience Fragment ist Teil einer lokalisierten Experience Fragment-Struktur unter `/content/experience-fragments`, die demselben Muster folgt wie die Site unter `/content/<site>`, einschließlich der gleichen Komponentennamen.

In diesem Fall wird das Fragment mit derselben Lokalisierung ([Sprache, Blueprint oder Live Copy](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/administering/reusing-content/msm-and-translation.html?lang=de)) wie die aktuelle Seite als Teil der Vorlage gerendert.

Dieses Verhalten ist auf E-Mail-Experience-Fragment-Komponenten beschränkt, die zu Vorlagen hinzugefügt werden. Experience Fragment-Komponenten, die einzelnen Inhaltsseiten hinzugefügt werden, rendern die exakten Experience Fragment-Komponenten, die in der Komponente konfiguriert wurden.

* Ein Beispiel dafür, wie die Lokalisierungsfunktion der Experience Fragment-Komponente funktioniert, finden Sie im [Abschnitt unten](#example).
* Ein Beispiel dafür, wie die Lokalisierungsfunktionen der Kernkomponenten zusammenarbeiten, finden Sie in den [Lokalisierungsfunktionen auf der Kernkomponenten-Seite](/help/get-started/localization.md).

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

Wenn die E-Mail-Experience-Fragment-Komponente `/content/experience-fragments/wknd/us/en/footerTextXf` in einer Vorlage platziert wird, rendern die lokalisierten Seiten, die basierend auf dieser Vorlage erstellt wurden, automatisch das lokalisierte Experience Fragment, welches der lokalisierten Inhaltsseite entspricht.

Wenn Sie also zu einer Inhaltsseite unter `/content/wknd/ch/de` navigieren, welche dieselbe Vorlage verwendet, wird `/content/experience-fragments/wknd/ch/de/footerTextXf` anstatt von `/content/experience-fragments/wknd/us/en/footerTextXf` gerendert.

### Notfallversorgung {#fallback}

Die Komponente E-Mail-Experience Fragment versucht, in der folgenden Reihenfolge eine entsprechende lokalisierte Komponente zu finden.

1. Zuerst wird versucht, einen Sprachstamm zu finden.
1. Wird dieser nicht gefunden, wird versucht, ein Blueprint zu finden.
1. Wenn auch dieses nicht gefunden werden, versucht sie, eine Live Copy zu finden.
1. Falls sie nicht gefunden wird, wird standardmäßig das in der Komponente konfigurierte Experience Fragment verwendet.

## Technische Details {#technical-details}

Lesen Sie die aktuellste [technische Dokumentation zur Experience Fragment-Komponente](https://www.adobe.com/go/aem_cmp_title_v1_de).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Kernkomponenten-Dokumentation für Entwickler](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Das Dialogfeld „Konfigurieren“ ermöglicht dem Inhaltsautor bzw. der Inhaltsautorin die Auswahl der Experience Fragment-Variation, die im Inhalt gerendert werden soll.

![Dialogfeld „E-Mail-Experience Fragment-Komponente bearbeiten“](/help/email/assets/email-experience-fragment-edit.png)

Verwenden Sie die Schaltfläche **Auswahldialog öffnen**, um die Komponentenauswahl zu öffnen und auszuwählen, welche Variation der Experience Fragment-Komponente zur Inhaltsseite hinzugefügt werden soll.

Wenn Sie die E-Mail-Experience-Fragment-Komponente zu einer Vorlage hinzufügen, wird sie automatisch lokalisiert, sofern die Experience Fragments lokalisiert sind. Was auf der Seite gerendert wird, kann sich daher von der Komponente unterscheiden, die Sie auswählen. Weitere Informationen finden Sie im [oben stehenden Beispiel](#example).

Sie können auch eine **ID** festlegen. Diese Option ermöglicht das Festlegen der eindeutigen Kennung der Komponente in HTM.

* Wenn das Feld leer bleibt, wird automatisch eine eindeutige ID generiert, den Sie im resultierenden Inhalt finden.
* Sofern eine ID angegeben wird, ist vom Autor bzw. der Autorin sicherzustellen, dass diese eindeutig ist.
* Die Änderung der ID kann sich auf CSS auswirken.

### Registerkarte „Arten“ {#styles-tab-edit}

Die E-Mail-Experience-Fragment-Komponente unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).

Verwenden Sie das Dropdown-Menü, um die Stile auszuwählen, die Sie auf die Komponente anwenden möchten. Die im Dialogfeld „Bearbeiten“ vorgenommenen Auswahlen haben denselben Effekt wie die in der Komponenten-Symbolleiste ausgewählten.

Stile müssen für diese Komponente im [Dialogfeld „Design“](#design-dialog) konfiguriert werden, damit das Dropdown-Menü zur Verfügung steht.

## Dialogfeld „Design“ {#design-dialog}

Über den Dialog „Design“ kann der Vorlagenautor bzw. die Vorlagenautorin die Optionen definieren, die dem Inhaltsautor bzw. der Inhaltsautorin zur Verfügung stehen, der/die die E-Mail-Experience-Fragment-Komponente verwendet. Außerdem können in diesem Dialogfenster die Standardeinstellungen beim Platzieren der E-Mail-Experience-Fragment-Komponente festgelegt werden.

### Registerkarte „Arten“ {#styles-tab}

Die E-Mail-Experience Fragment-Komponente unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).
