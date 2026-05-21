---
title: E-Mail-Button-Komponente
description: Die E-Mail-Button-Komponente ermöglicht die Konfiguration und Anzeige eines Button-Elements in Ihrem Inhalt.
role: Developer, Admin, User
exl-id: b144e8d1-1097-475d-b2eb-3353c176afb9
index: false
TQID: https://experienceleague.adobe.com/-kCXMMJi8n6DSMh97cgqruQY8pI04AkhxO2GEvwaK6s
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: e2c1b6d3-bb7e-4fe8-8c72-f7b403298e91
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: cc72dcf1-72e1-48cc-b434-e7c27d62d67c
source-git-commit: 73aa5234ac63fa3be99feebce448bb6722513838
workflow-type: tm+mt
source-wordcount: 527
ht-degree: 100%

---

# E-Mail-Button-Komponente {#email-button-component}

Die E-Mail-Button-Komponente ermöglicht die Konfiguration und Anzeige eines Button-Elements in Ihrem Inhalt.

## Verwendung {#usage}

Die E-Mail-Button-Komponente ermöglicht die Einfügung eines Buttons in Ihren Inhalt, der vom Inhaltsleser bzw. der Inhaltsleserin angeklickt werden kann und zu weiteren Ressourcen weiterleitet.

* Die Eigenschaften des Buttons können im [Dialogfeld „Konfigurieren“](#configure-dialog) ausgewählt werden.
* Stile für die E-Mail-Button-Komponente können im [Dialogfeld „Design“](#design-dialog) definiert werden.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der E-Mail-Button-Komponente ist v1. Sie wurde mit dem Release X der E-Mail-Kernkomponenten im Oktober 2022 eingeführt und wird in diesem Dokument beschrieben.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|---|---|---|---|
| v1 | Kompatibel | – | – |

Weitere Informationen zu Kernkomponentenversionen finden Sie im Dokument [E-Mail-Kernkomponentenversionen](/help/email/versions.md).

## Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur E-Mail-Button-Komponente [finden Sie auf GitHub](https://adobe.com/go/aem_cmp_tech_email_button_v1_de).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

## Dialogfeld „Konfigurieren“ {#configure-dialog}

Im Dialogfeld „Konfigurieren“ kann der Inhaltsautor bzw. die Inhaltsautorin die Schaltfläche und ihr Verhalten definieren und festlegen, wie sie dem Inhaltsleser bzw. der Inhaltsleserin dargestellt werden soll.

### Registerkarte „Eigenschaften“ {#properties-tab}

![Registerkarte „Eigenschaften“ im Dialogfeld „Design“ der Schaltflächenkomponente](/help/email/assets/email-button-edit-properties.png)

* **Text** – Der Text, der auf der Schaltfläche angezeigt werden soll
   * Klicken Sie auf das Kampagnensymbol, um das Dialogfeld [Adobe Campaign-Variable auswählen](/help/email/campaign-variables.md) zu öffnen und dynamische Inhalte aus Adobe Campaign einzufügen.
* **Verknüpfung** - Link zu einer Inhaltsseite in AEM, einer externen Ressource oder einem Anker
   * Wählen Sie im Dialogfeld **Auswahl** einen Pfad in AEM aus.
   * Klicken Sie auf das Kampagnensymbol, um das Dialogfeld [Adobe Campaign-Variable auswählen](/help/email/campaign-variables.md) zu öffnen und dynamische Inhalte aus Adobe Campaign einzufügen.
* **Symbol** – Kennung für die Darstellung eines Symbols auf der Schaltfläche
* **ID** – Diese Option ermöglicht das Festlegen der eindeutigen Kennung der Komponente in HTML.
   * Wenn das Feld leer bleibt, wird automatisch eine eindeutige ID generiert, den Sie im resultierenden Inhalt finden.
   * Sofern eine ID angegeben wird, ist vom Autor bzw. der Autorin sicherzustellen, dass diese eindeutig ist.
   * Die Änderung der ID kann sich auf CSS auswirken.
* **Link in neuer Registerkarte öffnen** – Wenn diese Option aktiviert ist, wird der Link auf einer neuen Browser-Registerkarte geöffnet.

### Registerkarte „Erreichbarkeit“ {#accessibility-tab}

![Registerkarte „Erreichbarkeit“ im Dialogfeld „Bearbeiten“ der Schaltflächenkomponente](/help/email/assets/email-button-edit-accessibility.png)

Auf der Registerkarte **Erreichbarkeit** können Werte für die [ARIA-Barrierefreiheits-Beschriftungen](https://www.w3.org/WAI/standards-guidelines/aria/) für die Komponente festgelegt werden.

* **Beschriftung** - Wert eines ARIA-Beschriftungs-Attributs für die Komponente

### Registerkarte „Arten“ {#styles-tab-edit}

Die E-Mail-Button-Komponente unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).

Verwenden Sie das Dropdown-Menü, um die Stile auszuwählen, die Sie auf die Komponente anwenden möchten. Die im Dialogfeld „Bearbeiten“ vorgenommenen Auswahlen haben denselben Effekt wie die in der Komponenten-Symbolleiste ausgewählten.

Stile müssen für diese Komponente im [Dialogfeld „Design“](#design-dialog) konfiguriert werden, damit die Registerkarte verfügbar ist.

## Dialogfeld „Design“ {#design-dialog}

### Registerkarte „Arten“ {#styles-tab}

Die E-Mail-Button-Komponente unterstützt das AEM [Stilsystem](/help/get-started/authoring.md#component-styling).
