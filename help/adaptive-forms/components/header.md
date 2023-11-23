---
title: Kernkomponente für adaptive Formulare – Header
description: Verwenden oder Anpassen der Header-Kernkomponente für adaptive Formulare.
role: Architect, Developer, Admin, User
exl-id: aa18def9-0bec-4475-8dde-213860621ef5
source-git-commit: 93acf5f6f11da42a7834bbb11b15a36db1e03dc9
workflow-type: tm+mt
source-wordcount: '679'
ht-degree: 100%

---

# Header {#header-adaptive-forms-core-component}

Eine Header-Komponente in einem adaptiven Formular ist ein Abschnitt am oberen Rand des Formulars, der normalerweise den Titel, das Logo oder den Namen des Formulars enthält. Sie können Header auch für andere Informationen verwenden, z. B. eine kurze Beschreibung des Zwecks des Formulars, den Namen der Organisation, die das Formular erstellt hat, oder Kontaktinformationen, um Hilfe zu dem Formular zu erhalten. Benutzende erhalten mit dem Header einen Überblick über das Formular und erhalten Kontext für die Informationen, die sie ausfüllen werden. Er wird verwendet, um Benutzenden zu helfen, den Zweck des Formulars zu verstehen und zu erfahren, wie es korrekt ausgefüllt werden kann.

**Beispiel**

![](/help/adaptive-forms/assets/header.png)

## Verwendung {#reasons-to-use-header}

- **Branding**: Sie können den Header verwenden, um das Logo oder den Namen der Organisation anzuzeigen, die das Formular erstellt hat, und so zur Erkennung und Glaubwürdigkeit der Marke beizutragen.

- **Kontext**: Sie können in der Kopfzeile eine kurze Beschreibung des Zwecks des Formulars bereitstellen und Benutzenden dabei helfen, den Kontext zu verstehen, in dem das Formular verwendet wird.

- **Navigation**: Eine Kopfzeile kann Links oder Schaltflächen enthalten, über die Benutzende zu anderen Teilen der Website oder Anwendung navigieren können.

- **Informationen**: Ein Header kann Kontaktinformationen oder Links enthalten, um Ressourcen zu unterstützen, sodass Benutzende bei Bedarf Hilfe erhalten können.

- **Benutzererlebnis**: Sie können das Formular mit einem Header benutzerfreundlicher gestalten, indem Sie Benutzenden eine klare und intuitive Möglichkeit bieten, auf Formularfelder zuzugreifen und sie auszufüllen.

## Version und Kompatibilität {#version-and-compatibility}

Die Kernkomponente „Akkordeon“ für adaptive Formulare wurde im Februar 2023 als Teil der Kernkomponenten 2.0.4 für Cloud Service und der Kernkomponenten 1.1.12 für AEM 6.5.16.0 Forms oder höher veröffentlicht. Hier finden Sie eine Tabelle mit allen unterstützten Versionen, AEM-Kompatibilität und Links zur entsprechenden Dokumentation:

| Komponentenversion | AEM as a Cloud Service | AEM 6.5.16.0 Forms oder höher |
|---|---|---|
| v1 | Kompatibel mit<br>[Version 2.0.4](/help/adaptive-forms/version.md) und höher | Kompatibel mit<br>[Version 1.1.12](/help/adaptive-forms/version.md) und höher (aber nur bis Version 2.0.0). |

Informationen zu Versionen und Freigaben der Kernkomponente finden Sie im Dokument [Kernkomponenten-Versionen](/help/adaptive-forms/version.md).


<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->


## Technische Details {#technical-details}

Aktuelle Informationen zur Header-Kernkomponente für adaptive Formulare finden Sie in der technischen Dokumentation auf [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/pageheader/v1/pageheader). Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Entwicklerdokumentation für Kernkomponenten](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Sie können im Dialogfeld „Konfigurieren“ Ihr Header-Erlebnis für Besuchende einfach anpassen. Sie können auch einfach Header-Optionen definieren, um ein nahtloses Benutzererlebnis zu gewährleisten.

### Bild-Registerkarte {#image-tab}

Dieser Teil des Headers enthält den Header-Titel und das Bild.

![Bild-Registerkarte](/help/adaptive-forms/assets/header_image.png)

- **Bild-Asset**: Sie können mit dieser Option ein Asset wie ein Bild per Drag-and-Drop mit der Maus ablegen. Sie können auch eine Datei aus einem lokalen Dateisystem mit der Schaltfläche **Durchsuchen** hochladen. Nach dem Hinzufügen eines Bildes erscheinen unter dem Bild drei Schaltflächen. Nach dem Hinzufügen eines Bildes erscheinen unten im Bild drei Schaltflächen:
   - **Bearbeiten** – Tippen oder klicken Sie auf **Bearbeiten**, um die Wiedergabeversionen des Assets im Asset-Editor zu verwalten.
   - **Löschen** – Tippen oder klicken Sie auf **Löschen**, um die Auswahl des aktuell ausgewählten Bilds aufzuheben.
   - **Auswahl** – Tippen oder klicken Sie auf die Option **Auswahl**, um ein anderes Bild aus dem Ordner „Assets“ auszuwählen.

- **Titel** – Mit dieser Option fügen Sie die Überschrift zur Kopfzeile hinzu. Benutzende können den im Dialogfeld enthaltenen, vordefinierten Text ändern.
- **Link zu** – Sie können die Überschrift mit dem Ordner verknüpfen, indem Sie das Symbol **Durchsuchen** verwenden.
- **Beschreibung**: Eine Beschreibung ist eine kurze Texterklärung, die zusätzliche Informationen oder Klarstellungen zum Zweck eines bestimmten Bildes bietet.
- **Größe (px)** – Hiermit werden Länge und Breite des Bildes angepasst, indem die Anzahl der Pixel erhöht oder verringert wird.

![Registerkarte „Barrierefreiheit“](/help/adaptive-forms/assets/header_accessibility.png)

- **Alternativtext**: Diese Option wird verwendet, um eine kurze Textalternative für das Bild einzugeben, um es für sehbehinderte Benutzende zu beschreiben.

- **Bild ist dekorativ** – Überprüfen Sie, ob das Bild von Hilfstechnologien ignoriert werden soll und daher keinen alternativen Text erfordert. Dies gilt nur für dekorative Bilder.

### Registerkarte „Text“ {#text-tab}

Sie können in diesem Abschnitt den Text eingeben, den Sie in die Kopfzeile einfügen möchten.

<!--

## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html)

-->

## Ähnliche Artikel {#related-articles}

{{more-like-this}}

## Siehe auch {#see-also}

{{see-also}}
