---
title: Trennzeichenkomponente
description: Die Trennzeichen-Komponente erstellt einen Umbruch zwischen Komponenten auf einer Seite
translation-type: tm+mt
source-git-commit: c186e9ec3944d785ab0376769cf7f2307049a809
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 74%

---


# Trennzeichenkomponente {#separator-component}

Die Kernkomponente Trennzeichenkomponente zeigt eine horizontale Linie zum Trennen von Inhalten an.

## Nutzung {#usage}

Mit der Trennzeichenkomponente kann der Inhaltsautor einfach eine horizontale Linie als Trennlinie zwischen Inhalten erstellen, um Informationen auf einer Seite besser zu organisieren.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Trennzeichenkomponente ist v1, die mit Version 2.3.0 der Kernkomponenten im Februar 2019 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|---|
| v1 | Kompatibel | Kompatibel | Kompatibel |

## Musterkomponentenausgabe {#sample-component-output}

Um die Trennzeichenkomponente sowie Beispiele für die Konfigurationsoptionen sowie HTML- und JSON-Ausgaben zu erhalten, besuchen Sie die [Komponentenbibliothek](https://adobe.com/go/aem_cmp_library_separator).

### Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur Trennzeichenkomponente [finden Sie auf GitHub](https://adobe.com/go/aem_cmp_tech_separator_v1).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

![Dialogfeld &quot;Bearbeiten&quot;der Trennzeichenkomponente](/help/assets/separator-edit.png)

* **ID** - Diese Option ermöglicht die Steuerung des eindeutigen Bezeichners der Komponente im HTML und in der [Datenschicht](/help/developing/data-layer/overview.md).
   * Wenn Sie das Feld leer lassen, wird automatisch eine eindeutige ID generiert und Sie können die resultierende Seite überprüfen.
   * Wenn eine ID angegeben wird, muss der Autor sicherstellen, dass sie eindeutig ist.
   * Eine Änderung der ID kann sich auf die Verfolgung von CSS, JS und Datenschichten auswirken.

## Dialogfeld „Design“ {#design-dialog}

Das Dialogfeld „Design“ ermöglicht es dem Vorlagenautor, die Stile zu definieren, die auf die Trennzeichenkomponente angewendet werden.

### Registerkarte „Stile“ {#styles-tab}

Die Trennzeichenkomponente unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).
