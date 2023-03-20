---
title: Adaptive Forms-Kernkomponente - Kopfzeile
description: Verwenden oder Anpassen der Kernkomponente "Adaptive Forms-Kopfzeile".
role: Architect, Developer, Admin, User
exl-id: aa18def9-0bec-4475-8dde-213860621ef5
source-git-commit: d2a6108f17f6e0c6b91bec84893d64a8bd48effd
workflow-type: tm+mt
source-wordcount: '675'
ht-degree: 6%

---

# Kopfzeile {#header-adaptive-forms-core-component}

Eine Kopfzeilenkomponente in einem adaptiven Formular ist ein Abschnitt am oberen Rand des Formulars, der normalerweise den Titel, das Logo oder den Namen des Formulars enthält. Die Kopfzeile kann auch andere Informationen enthalten, z. B. eine kurze Beschreibung des Zwecks des Formulars, den Namen der Organisation, die das Formular erstellt hat, oder Kontaktinformationen, um Hilfe zu dem Formular zu erhalten. Mit der Kopfzeile erhalten Benutzer einen Überblick über das Formular und erhalten Kontext für die Informationen, die sie ausfüllen werden. Es wird verwendet, um Benutzern zu helfen, den Zweck des Formulars zu verstehen und zu erfahren, wie es korrekt ausgefüllt werden kann.

**Beispiel**

![](/help/adaptive-forms/assets/header.png)

## Verwendung {#reasons-to-use-header}

* **Branding**: Eine Kopfzeile kann verwendet werden, um das Logo oder den Namen der Organisation anzuzeigen, die das Formular erstellt hat, und so zur Erkennung und Glaubwürdigkeit der Marke beizutragen.

* **Kontext**: Eine Kopfzeile kann eine kurze Beschreibung des Zwecks des Formulars enthalten und Benutzern dabei helfen, den Kontext zu verstehen, in dem das Formular verwendet wird.

* **Navigation**: Eine Kopfzeile kann Links oder Schaltflächen enthalten, über die Benutzer zu anderen Teilen der Website oder Anwendung navigieren können.

* **Informationen**: Ein Header kann Kontaktinformationen oder Links enthalten, um Ressourcen zu unterstützen, sodass Benutzer bei Bedarf Hilfe erhalten können.

* **Anwendererlebnis**: Mit einer Kopfzeile können Sie das Formular benutzerfreundlicher gestalten, indem Sie Benutzern eine klare und intuitive Möglichkeit bieten, auf Formularfelder zuzugreifen und sie auszufüllen.

## Version und Kompatibilität {#version-and-compatibility}

Die Kernkomponente &quot;Adaptive Forms Accordion&quot;wurde im Februar 2023 als Teil der Kernkomponenten 2.0.4 für Cloud Service und Kernkomponenten 1.1.12 für AEM 6.5.16.0 Forms oder höher veröffentlicht. In der folgenden Tabelle finden Sie alle unterstützten Versionen, AEM Kompatibilität und Links zur entsprechenden Dokumentation:

| Komponentenversion | AEM as a Cloud Service | AEM 6.5.16.0 Forms oder höher |
|---|---|---|
| v1 | Kompatibel mit<br>[Version 2.0.4](/help/adaptive-forms/version.md) und höher | Kompatibel mit<br>[Version 1.1.12](/help/adaptive-forms/version.md) und höher, jedoch weniger als 2.0.0. |

Informationen zu Kernkomponentenversionen und -versionen finden Sie im Abschnitt [Kernkomponenten-Versionen](/help/adaptive-forms/version.md) Dokument.


<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->


## Technische Details {#technical-details}

Die neuesten Informationen zur Kernkomponente &quot;Adaptive Forms-Kopfzeile&quot;finden Sie in der technischen Dokumentation zu [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/pageheader/v1/pageheader). Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie im Abschnitt [Entwicklerdokumentation für Kernkomponenten](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Im Dialogfeld &quot;Konfigurieren&quot;können Sie Ihre Kopfzeilenerfahrung für Besucher einfach anpassen. Sie können Kopfzeilenoptionen auch einfach definieren, um ein nahtloses Benutzererlebnis zu gewährleisten.

### Registerkarte &quot;Bild&quot; {#image-tab}

Dieser Teil der Kopfzeile enthält den Kopfzeilentitel und das Bild.

![ImageTab](/help/adaptive-forms/assets/header_image.png)

* **Bild-Asset** - Mit dieser Option können Sie ein Asset wie ein Bild per Drag &amp; Drop mit der Maus ablegen. Sie können auch eine Datei aus einem lokalen Dateisystem mit dem **Durchsuchen** Schaltfläche. Nach dem Hinzufügen eines Bildes werden drei Schaltflächen unten im Bild angezeigt. Nach dem Hinzufügen eines Bildes werden drei Schaltflächen unten im Bild angezeigt:
   * **Bearbeiten** - Tippen oder klicken Sie auf **Bearbeiten** , um die Ausgabeformate des Assets im Assets-Editor zu verwalten.
   * **Löschen** - Tippen oder klicken Sie auf **Löschen** , um die Auswahl des aktuell ausgewählten Bildes aufzuheben.
   * **Auswahl** - Tippen oder klicken Sie auf **Auswahl**  -Option, um ein anderes Bild aus dem Ordner Assets auszuwählen.

* **Titel** - Mit dieser Option wird die Überschrift zur Kopfzeile hinzugefügt. Der vordefinierte Text ist im Dialogfeld enthalten und kann vom Benutzer geändert werden.
* **Link zu** - Sie können die Überschrift mit dem Ordner verknüpfen, indem Sie die **Durchsuchen** Symbol.
* **Beschreibung** - Eine Beschreibung ist eine kurze Texterklärung, die zusätzliche Informationen oder Klarstellungen zum Zweck eines bestimmten Bildes bietet.
* **Größe (px)** - Es hilft bei der Anpassung der Länge und Breite des Bildes durch Vergrößern oder Verringern der Pixel.

![Registerkarte &quot;Barrierefreiheit&quot;](/help/adaptive-forms/assets/header_accessibility.png)

* **Alternativtext** - Diese Option wird verwendet, um den Text einzugeben, der eine kurze und beschreibende Textalternative für das Bild bietet, die das Bild für sehbehinderte Benutzer beschreibt.

* **Bild ist dekorativ** – Überprüfen Sie, ob das Bild von Hilfstechnologien ignoriert werden soll und daher keinen alternativen Text erfordert. Dies gilt nur für dekorative Bilder.

### Registerkarte &quot;Text&quot; {#text-tab}

In diesem Abschnitt können Sie den Text eingeben, der in die Kopfzeile eingefügt werden soll.

