---
title: E-Mail-Schaltflächenkomponente
description: Die Komponente E-Mail-Schaltfläche ermöglicht die Konfiguration und Anzeige eines Schaltflächenelements in Ihrem Inhalt.
role: Architect, Developer, Admin, User
exl-id: b144e8d1-1097-475d-b2eb-3353c176afb9
source-git-commit: 33976c0e745ad091a142109f70541f01a31edc5b
workflow-type: tm+mt
source-wordcount: '563'
ht-degree: 41%

---


# E-Mail-Schaltflächenkomponente {#email-button-component}

Die Komponente E-Mail-Schaltfläche ermöglicht die Konfiguration und Anzeige eines Schaltflächenelements in Ihrem Inhalt.

## Nutzung {#usage}

Die Komponente E-Mail-Schaltfläche ermöglicht die Einbeziehung einer Schaltfläche in Ihren Inhalt, die vom Inhaltsleser angeklickt werden kann und Links zu weiteren Ressourcen enthält.

* Die Eigenschaften der Schaltfläche können im [Dialogfeld &quot;Konfigurieren&quot;.](#configure-dialog)
* Stile für die E-Mail-Schaltflächenkomponente können im [Dialogfeld &quot;Design&quot;.](#design-dialog)

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der E-Mail-Schaltflächenkomponente ist v1, die mit Version x der E-Mail-Kernkomponenten im Oktober 2022 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|
| v1 | Kompatibel | Kompatibel |

Weitere Informationen zu Kernkomponentenversionen und -versionen finden Sie im Dokument . [Versionen der E-Mail-Kernkomponenten.](/help/email/versions.md)

## Musterkomponentenausgabe {#sample-component-output}

Um die E-Mail-Schaltflächenkomponente sowie Beispiele für die Konfigurationsoptionen sowie HTML- und JSON-Ausgaben zu erhalten, besuchen Sie die [Komponentenbibliothek.](https://adobe.com/go/aem_cmp_library_email_button)

## Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur E-Mail-Schaltflächenkomponente [finden Sie auf GitHub.](https://adobe.com/go/aem_cmp_tech_email_button_v1)

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler.](/help/developing/overview.md)

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Im Dialogfeld &quot;Konfigurieren&quot;kann der Inhaltsautor die Schaltfläche definieren und festlegen, wie sie sich verhält und wie sie für einen Leser Ihres Inhalts angezeigt wird.

### Registerkarte „Eigenschaften“ {#properties-tab}

![Registerkarte „Eigenschaften“ im Dialogfeld „Design“ der Schaltflächenkomponente](/help/email/assets/email-button-edit-properties.png)

* **Text** - Der Text, der auf der Schaltfläche angezeigt werden soll
   * Klicken Sie auf das Kampagnensymbol , um die [Adobe Campaign-Variable auswählen](/help/email/campaign-variables.md) zum Einfügen von dynamischen Inhalten aus Adobe Campaign.
* **Verknüpfung** - Link zu einer Inhaltsseite in AEM, einer externen Ressource oder einem Anker
   * Wählen Sie im Dialogfeld **Auswahl** einen Pfad in AEM aus.
   * Klicken Sie auf das Kampagnensymbol , um die [Adobe Campaign-Variable auswählen](/help/email/campaign-variables.md) zum Einfügen von dynamischen Inhalten aus Adobe Campaign.
* **Symbol** – Bezeichner für die Anzeige eines Symbols auf der Schaltfläche
* **ID** - Diese Option ermöglicht die Steuerung der eindeutigen Kennung der Komponente im HTML.
   * Wenn Sie das Feld leer lassen, wird automatisch eine eindeutige ID generiert, die Sie durch Überprüfen des resultierenden Inhalts finden können.
   * Sofern eine ID angegeben wird, ist vom Autor sicherzustellen, dass diese eindeutig ist.
   * Eine Änderung der ID kann sich auf CSS auswirken.
* **Link auf neuer Registerkarte öffnen** – Wenn diese Option aktiviert ist, wird der Link auf einer neuen Browser-Registerkarte geöffnet.

### Registerkarte „Erreichbarkeit“ {#accessibility-tab}

![Registerkarte „Erreichbarkeit“ im Dialogfeld „Bearbeiten“ der Schaltflächenkomponente](/help/email/assets/email-button-edit-accessibility.png)

Auf der Registerkarte **Erreichbarkeit** können Werte für die [ARIA-Barrierefreiheits-Beschriftungen](https://www.w3.org/WAI/standards-guidelines/aria/) für die Komponente festgelegt werden.

* **Beschriftung** - Wert eines ARIA-Beschriftungs-Attributs für die Komponente

### Registerkarte „Arten“ {#styles-tab-edit}

Die E-Mail-Schaltflächenkomponente unterstützt die AEM [Stilsystem.](/help/get-started/authoring.md#component-styling).

Verwenden Sie das Dropdown-Menü, um die Stile auszuwählen, die Sie auf die Komponente anwenden möchten. Die im Dialogfeld „Bearbeiten“ vorgenommenen Auswahlen haben denselben Effekt wie die in der Komponenten-Symbolleiste ausgewählten.

Stile müssen für diese Komponente im [Dialogfeld &quot;Design&quot;](#design-dialog) , damit die Registerkarte verfügbar ist.

## Dialogfeld „Design“ {#design-dialog}

### Registerkarte „Arten“ {#styles-tab}

Die E-Mail-Schaltflächenkomponente unterstützt die AEM [Stilsystem](/help/get-started/authoring.md#component-styling).
