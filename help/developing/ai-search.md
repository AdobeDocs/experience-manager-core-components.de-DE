---
title: Konfigurieren der Inhaltsdatenkomponente
description: Die Inhaltsdatenkomponente bietet den Besuchern Ihrer Site eine generative KI-gestützte KI-Suche. Erfahren Sie, wie Sie diese Komponente für Ihre Inhaltsautoren aktivieren.
role: Developer, Admin
product_v2: id: c45915cf-e157-4af7-a80d-97b905bcb3a5id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: e2c1b6d3-bb7e-4fe8-8c72-f7b403298e91
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: c18d9e03-ac7d-4811-9c92-3e92ddc70ade
source-git-commit: 865622469555a773138d3ff1b54138f2b76994b0
workflow-type: tm+mt
source-wordcount: 485
ht-degree: 2%

---


# Konfigurieren der Inhaltsdatenkomponente {#configure-content-ai-search-component}

Die Inhaltsdatenkomponente bietet den Besuchern Ihrer Site eine generative KI-gestützte KI-Suche. Erfahren Sie, wie Sie diese Komponente für Ihre Inhaltsautoren aktivieren.

## Voraussetzungen {#prerequisites}

* Mindestens ein [Content Source](https://experienceleague.adobe.com/en/docs/experience-manager-content-ai/using/contentsources) wurde bereits erstellt und weist den Status **Verfügbar** auf.
* Der **AEM Content AI Client** OSGi-Konfiguration (`ContentAIClientImpl`), die sowohl in der Autoren- als auch in der Veröffentlichungsinstanz eingerichtet ist, mit gültigen API-Anmeldeinformationen und einem **Default Content Source**-Wert. Informationen zum Abrufen von Anmeldeinformationen finden [ im Dokument „Einrichten ](https://experienceleague.adobe.com/en/docs/experience-manager-content-ai/using/setup-adc-project) Adobe Developer Console-Projekts“.

## Erstellen einer Proxy-Komponente {#proxy-component}

Wie alle Kernkomponenten wird empfohlen, eine Proxy-KI-Suche für die standardmäßige Inhaltsdatenkomponente zu erstellen, die im Lieferumfang von AEM enthalten ist. Wenn Sie Ihre projektspezifischen Änderungen in der Proxy-Komponente unter `/apps` lassen, werden die Basiskomponenten unter `/libs` automatisch von Adobe aktualisiert, und Ihre Projektkomponente erbt diese Aktualisierungen automatisch. Weitere Informationen finden Sie [ den Dokumenten ](/help/get-started/using.md#aemaacs)Verwenden von Kernkomponenten[ und ](/help/developing/guidelines.md)Komponentenrichtlinien“.

## Client-Bibliotheken konfigurieren {#clientlib}

Die Inhaltsdatenkomponente folgt nicht [dem Standardmuster für das Einschließen von Client-KI-Suchen in die Kernkomponenten.](/help/developing/including-clientlibs.md) Führen Sie stattdessen die folgenden Schritte aus.

Fügen Sie der Seitenkomponente `customheaderlibs.html` (für CSS) und `customfooterlibs.html` (für JS) Ihres Projekts Folgendes hinzu:

```html
<sly data-sly-use.clientLib="/libs/granite/sightly/templates/clientlib.html"
     data-sly-call="${clientLib.css @ categories='core.wcm.components.contentaisearch.v1'}"></sly>
```

Wenn Ihr Projekt darüber hinaus einen eigenen Markenstil verwendet, fügen Sie nach diesem eine zweite Kategorie für die Client-Bibliothek Ihres Projekts hinzu.

## Verwenden der Inhaltskomponenten-KI-Suchen {#using}

Ihre Inhaltsautoren können jetzt die Inhaltskomponenten-KI-Suchen auf ihren Seiten platzieren. Weitere KI-Suchen finden Sie [ Dokument ](/help/components/ai-search.md)Inhaltsdatenkomponente“.

## Verwendung der Inhalts-KI durch die Komponente {#how-it-works}

* Standardsuchabfragen werden von derselben Abrufebene wie der Source-Index für Inhalte bereitgestellt und geben übereinstimmende Seiten, Fragmente oder Assets aus der konfigurierten Quelle zurück.
* Wenn die KI-generierte Zusammenfassung aktiviert ist, ruft die Komponente zusätzlich den generativen Endpunkt der AEM-Inhalts-KI auf, wodurch die Antwort im selben indizierten Inhalt geerdet wird, und zeigt Quellen neben der Zusammenfassung an, damit Besucher sie überprüfen können.
* Da beide Funktionen aus demselben verwalteten Source für Inhalte gelesen werden, bleiben die Ergebnisse und Zusammenfassungen mit den aktuell indizierten Inhalten konsistent. Wenn Sie die Akquise erneut ausführen (siehe [Steuern von Inhaltsquellen](https://experienceleague.adobe.com/en/docs/experience-manager-content-ai/using/contentsources)), werden beide aktualisiert.

## Nächste Schritte {#next-steps}

* [Steuern Ihrer Inhaltsquellen](https://experienceleague.adobe.com/en/docs/experience-manager-content-ai/using/contentsources) - Erstellen und verwalten Sie die Content-Source, nach der diese Komponente sucht.
* [Einrichten eines Adobe Developer Console-Projekts](https://experienceleague.adobe.com/en/docs/experience-manager-content-ai/using/setup-adc-project) - Abrufen der von der OSGi Content AI-Client-Konfiguration verwendeten Anmeldeinformationen.
* [Content AI-API-Referenz](https://developer.adobe.com/experience-cloud/experience-manager-apis/api/experimental/contentai/) - Verstehen Sie die zugrunde liegenden Endpunkte für Suchen und generative Zusammenfassungen, die diese Komponente aufruft.
