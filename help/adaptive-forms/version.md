---
title: Kernkomponentenversionen von AEM Forms
description: AEM Kernkomponenten werden als Versionen veröffentlicht, die mehr als eine Version derselben Kernkomponenten enthalten können. In diesem Dokument wird erläutert, welche Versionen veröffentlicht werden und wie die Kompatibilität mit Kernkomponenten und AEM verstanden werden kann.
role: Architect, Developer, Admin, User
exl-id: 8146a5b1-acf6-4b54-ad6b-6e1747a137f6
source-git-commit: a567b5ad937d426abe16c34e039e19cd0b1af5b0
workflow-type: tm+mt
source-wordcount: '885'
ht-degree: 58%

---

# Kernkomponenten-Versionen {#core-components-versions}

Die aktuelle Version der Kernkomponenten 2.0.10 ist kompatibel mit [AEM as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/landing/home.html?lang=de) und die Kernkomponentenversion 1.1.12 mit [On-Premise- oder AMS-Installationen von AEM 6.5 Forms](https://experienceleague.adobe.com/docs/experience-manager-65/user-guide/home.html?lang=de).

## AEM as a Cloud Service-Versionsverlauf {#aem-as-cs-version-history}

Die nachfolgende Tabelle enthält eine Liste der Kernkomponentenversionen, die mit AEM as a Cloud Service kompatibel und auf [GitHub zusammen mit umfassenden Details zu den jeweiligen Versionen](https://github.com/adobe/aem-core-forms-components/releases) verfügbar sind.

| Version | Beschreibung | AEM as a Cloud Service | Java™ | Veröffentlichungsdatum |
|---|---|---|---|---|
| [2.0.74](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.74) | Mit dieser Version wird der Sendefehler für die Übermittlungsaktion in AEM Forms aktualisiert. | Kontinuierlich | 8, 11 | 15. November 2023 |
| [2.0.70](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.70) | In dieser Version wurde Unterstützung für die Handhabung der Seitensprache von Sites im Formularcontainer hinzugefügt. | Kontinuierlich | 8, 11 | 10. November 2023 |
| [2.0.64](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.64) | Unterstützung von Rich-Text für Beschriftungen für Radio-/Kontrollkästchen-Komponenten. Diese Version enthält auch Fehlerbehebungen für die Komponente &quot;Allgemeine Geschäftsbedingungen&quot;. | Kontinuierlich | 8, 11 | 6. November 2023 |
| [2.0.62](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.62) | Mit dieser Version wird die Komponente &quot;Allgemeine Geschäftsbedingungen&quot;unterstützt. Unterstützung für Qualifizierten Namen in Kernkomponenten hinzugefügt. | Kontinuierlich | 8, 11 | 16. Oktober 2023 |
| [2.0.60](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.60) | Diese Version enthält Fehlerbehebungen im Zusammenhang mit der Funktion, dem Assistenten und der Komponente für die Datumsauswahl für benutzerdefinierte Eigenschaften. | Kontinuierlich | 8, 11 | 12. September 2023 |
| [2.0.56](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.56) | Mit dieser Version wird Unterstützung für benutzerdefinierte Eigenschaften für alle Kernkomponenten hinzugefügt. | Kontinuierlich | 8, 11 | 12. September 2023 |
| [2.0.54](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.54) | In dieser Version wurde das Problem behoben, das bei der Lokalisierung mit der Komponente für die Datumsauswahl auftrat. | Kontinuierlich | 8, 11 | 30. August 2023 |
| [2.0.52](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.52) | Unterstützung für die Verwendung der Kontrollkästchen-Komponente in einem adaptiven Formular. | Kontinuierlich | 8, 11 | 25. August 2023 |
| [2.0.50](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.50) | Unterstützung für Formularfragmente in einem adaptiven Formular mit dieser Version hinzugefügt. | Kontinuierlich | 8, 11 | 4. August 2023 |
| [2.0.48](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.48) | Die wichtigsten Verbesserungen in dieser Version beziehen sich auf die Leistung von Lighthouse. | Kontinuierlich | 8, 11 | 25. Juli 2023 |
| [2.0.42](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.42) | Die Version beinhaltet Verbesserungen am Programmier-Ende. | Kontinuierlich | 8, 11 | 18. Juli 2023 |
| [2.0.38](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.38) | Die Barrierefreiheitsfunktion wird mit dieser Version verbessert. | Kontinuierlich | 8, 11 | 17. Juli 2023 |
| [2.0.36](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.36) | In dieser Version können Sie den benutzerdefinierten Fehler-Handler mit dem Invoke-Dienst des Regeleditors verwenden. | Kontinuierlich | 8, 11 | 3. Juli 2023 |
| [2.0.34](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.34) | Lokalisierungsunterstützung für Standard-Fehlermeldungen hinzugefügt, zusammen mit der Schaltfläche Hinzufügen/Entfernen für wiederholbare Komponenten. | Kontinuierlich | 8, 11 | 28. Juni 2023 |
| [2.0.32](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.32) | Mit dieser Version wird die Unterstützung für Captcha für Adaptive Forms hinzugefügt. | Kontinuierlich | 8, 11 | 15. Juni 2023 |
| [2.0.26](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.26) | Unterstützung für das Hinzufügen adaptiver Formulare in AEM Sites. | Kontinuierlich | 8, 11 | 7. Juni 2023 |
| [2.0.18](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.18) | Mit dieser Version wird Unterstützung für eine Wiederholbarkeit für die Accordion-Komponente. Außerdem wurde eine neue Komponente als vertikale Registerkarten hinzugefügt. | Kontinuierlich | 8, 11 | 5. Juni 2023 |
| [2.0.10](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.10) | Mit dieser Version wird die Unterstützung für eine Container-Komponente für adaptive Formulare im Editor von Sites eingeführt. | Kontinuierlich | 8, 11 | 17. März 2023 |
| [2.0.8](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.8) | Die Funktion zur Wiederholbarkeit für die Assistentenkomponente wurde in dieser Version eingeführt. | Kontinuierlich | 8, 11 | 03. März 2023 |
| [2.0.6](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.6) | In dieser Version werden mehrere Formate für die Kernkomponente „Zahleneingabe“ eingeführt. | Kontinuierlich | 8, 11 | 08. Februar 2023 |
| [2.0.4](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.6) | Die Kernkomponentenunterstützung für AEM as a Cloud Service wird in dieser Version eingeführt. | Kontinuierlich | 8, 11 | 30. Januar 2023 |

## Versionsverlauf von AEM 6.5 Forms {#aem-as-form-version-history}

Die nachfolgende Tabelle enthält eine Liste der Kernkomponentenversionen, die mit On-Premise- und AMS-Installationen von AEM 6.5 Forms kompatibel und auf [GitHub zusammen mit umfassenden Details zu den jeweiligen Versionen](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-1.1.12) verfügbar sind.

| Version | Beschreibung | AEM 6.4 | AEM 6.5 | Java™ | Veröffentlichungsdatum |
|---|---|---|---|---|---|
| [1.1.32](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-1.1.32) | In dieser Version wurden die Informationen für Paketinformationen von AEM Service Pack 6.5.18.0 aktualisiert. | - | 6.5.16.0+ | 8, 11 | 15. Oktober 2023 |
| [1.1.28](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-1.1.28) | Unterstützung von Rich-Text für Beschriftungen für Radio-/Kontrollkästchen-Komponenten. In dieser Version wird auch die Komponente &quot;Bedingungen&quot;unterstützt. | - | 6.5.16.0+ | 8, 11 | 15. Oktober 2023 |
| [1.1.26](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-1.1.26) | In dieser Version wurde die Unterstützung für die Kontrollkästchenkomponente für adaptives Formular hinzugefügt. Außerdem wurde die Leistung von Lighthouse verbessert. Der benutzerdefinierte Fehler-Handler, der den Aufrufdienst des Regeleditors verwendet, ist ebenfalls in dieser Version enthalten. | - | 6.5.16.0+ | 8, 11 | 15. Oktober 2023 |
| [1.1.24](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-1.1.24) | Lokalisierungsunterstützung für Standard-Fehlermeldungen hinzugefügt, zusammen mit der Schaltfläche Hinzufügen/Entfernen für wiederholbare Komponenten. Unterstützung für Recaptcha in Adaptive Forms hinzugefügt. | - | 6.5.16.0+ | 8, 11 | 29. Juni 2023 |
| [1.1.22](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-1.1.22) | Unterstützung für das Hinzufügen adaptiver Formulare in AEM Sites. Die Registerkarte &quot;Elemente&quot;im Dialogfeld &quot;Bearbeiten&quot;der Komponente &quot;Assistent und Vertikale Registerkarten&quot;wurde hinzugefügt. | - | 6.5.16.0+ | 8, 11 | 07. Juni 2023 |
| [1.1.12](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-1.1.12) | Die Kernkomponentenunterstützung für On-Premise- und AMS-Installationen von AEM Forms wird in dieser Version eingeführt. | - | 6.5.16.0+ | 8, 11 | 08. Februar 2023 |

## Siehe auch {#see-also}

{{see-also}}