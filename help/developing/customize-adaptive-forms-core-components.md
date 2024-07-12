---
title: Anpassen von Kernkomponenten für adaptive Formulare
description: Erfahren Sie, wie Sie eine Kernkomponente für adaptive Formulare erweitern oder erstellen, um Funktionen zu implementieren, die auf Ihr Unternehmen zugeschnitten sind.
role: Architect, Developer, Admin
exl-id: f3ab12aa-d48d-47e9-a965-15052cac6f18
source-git-commit: 79cedf7099e2dc267a4cb1c25c06d4f0460367b2
workflow-type: tm+mt
source-wordcount: '562'
ht-degree: 100%

---

# Anpassen von Kernkomponenten für adaptive Formulare

Durch das Anpassen der Kernkomponenten für adaptive Formulare können Sie die vordefinierten Funktionen an Ihre spezifischen Anforderungen anpassen. Dieses Handbuch führt Sie durch den Prozess der Anpassung dieser Komponenten, um ein stärker personalisiertes Erlebnis zu schaffen.

## Voraussetzung

Bevor Sie sich mit der Anpassung der Kernkomponenten für adaptive Formulare befassen:

* Erhalten Sie Informationen zur [Architektur von Kernkomponenten](customizing.md#customizing-the-markup-customizing-the-markup) und gehen Sie die [offizielle Dokumentation zu Adobe Experience Manager-Kernkomponenten](customizing.md) durch. Diese umfangreichen Ressourcen dienen während des gesamten Anpassungsprozesses als Leitfaden für Sie.
* Einrichten der Entwicklungsumgebung – Dies gewährleistet einen reibungslosen Arbeitsablauf für Änderungen an den Kernkomponenten. Verwenden Sie beim Einrichten der Entwicklungsumgebung ein AEM-Archetyp-Projekt, das auf dem neuesten AEM-Archetyp-Projekt basiert. Je nach Umgebung haben Sie folgende Möglichkeiten:

   * [Einrichten einer lokalen Entwicklungsumgebung für Forms as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/setup-configure-migrate/setup-local-development-environment.html?lang=de).
   * [Einrichten einer lokalen Entwicklungsumgebung für AEM 6.5 Forms](https://experienceleague.adobe.com/docs/experience-manager-learn/foundation/development/set-up-a-local-aem-development-environment.html?lang=de)

## Anpassen einer Kernkomponente für adaptive Formulare

Gehen Sie wie folgt vor, um das Erscheinungsbild, das Verhalten und die Funktionalität einer Kernkomponente für adaptive Formulare zu ändern.

1. **Identifizieren und Duplizieren der Kernkomponente**

   Beim Konfigurieren der Entwicklungsumgebung haben Sie ein auf Archetypen basierendes Projekt erstellt. Identifizieren Sie im AEM-Archetyp-Projekt die spezifische Kernkomponente, die Sie anpassen möchten. Erstellen Sie nach der Identifizierung ein Duplikat der Komponente in Ihrem AEM-Archetyp-basierten Projekt. Halten Sie sie parallel zu anderen Kernkomponenten für adaptive Formulare. Dieser Schritt stellt sicher, dass Ihre Anpassungsbemühungen keine Auswirkungen auf die Originalkomponente haben, sodass Sie frei experimentieren können.

1. **Anpassen der kopierten Komponente**

   Öffnen Sie die duplizierte Komponente und nehmen Sie die erforderlichen Änderungen entsprechend Ihren Anforderungen vor:

   * **HTML-Struktur anpassen**: Passen Sie die HTML-Struktur an Ihre Design-Anforderungen an, während Sie Stilpraktiken des [BEM (Block Element Modifier)](https://github.com/adobe/aem-core-wcm-components/wiki/css-coding-conventions) für wartungsfähigen und skalierbaren Code verwenden.
   * **Titel aktualisieren**: Aktualisieren Sie die Beschriftung der Komponente, um einen klaren und beschreibenden Namen für die angepasste Version bereitzustellen. Halten Sie sich an die bereitgestellte [OOTB-Beschriftungsvorlage (vorkonfiguriert)](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/af-commons/v1/fieldTemplates/label.html?lang=de), um Konsistenz zu gewährleisten.
   * **Widget anpassen**: Passen Sie das in der Komponente verwendete Widget (Dropdown-Listen, Kontrollkästchen) an Ihren spezifischen Anwendungsfall an. Nehmen die [Beispiel-Widget-Implementierung](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/textinput/v1/textinput/textinput.html?lang=de) als Referenz.
   * **Hilfetext und Tooltips**: Personalisieren Sie den Hilfetext oder die mit der Komponente verknüpften QuickInfos, um Benutzerinnen und Benutzern Kontext und Anleitung anzubieten. Verwenden Sie die [OOTB-Hilfetextvorlage](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/af-commons/v1/fieldTemplates/questionMark.html?lang=de) als Ausgangspunkt.
   * **Datenattribute**: Schließen Sie alle erforderlichen Datenattribute in die HTML-Elemente der Komponente ein. Diese Attribute sind für das ordnungsgemäße Funktionieren der Komponente zur Laufzeit von entscheidender Bedeutung. Lesen Sie die [Dokumentation](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/textinput/v1/textinput), um die Rolle von Datenattributen in den Kernkomponenten für adaptive Formulare zu verstehen.

1. **Implementieren der Backend-Logik**

   Wenn Ihre Anpassung Backend-Logik erfordert, können Sie vorhandene Sling-Modelle erweitern. Siehe das bereitgestellte [Beispiel](https://github.com/adobe/aem-core-forms-components/blob/master/bundles/af-core/src/main/java/com/adobe/cq/forms/core/components/internal/models/v1/form/TextInputImpl.java), um die gewünschte Funktion nahtlos in Ihre angepasste Komponente zu integrieren.

1. **Konfigurieren des Dialogfelds der Komponente**

   Konfigurieren Sie das Dialogfeld, das mit Ihrer angepassten Komponente verknüpft ist. Verwenden Sie das Beispiel für ein [Komponentendialogfeld](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/textinput/v1/textinput/_cq_dialog/.content.xml), das in der Dokumentation gegeben wird, um sicherzustellen, dass Benutzerinteraktionen und -einstellungen ordnungsgemäß verwaltet werden.

1. **Bereitstellen und Testen der Komponente in Ihrer lokalen Entwicklungsumgebung**

   Verwenden Sie [Maven zum Erstellen und Bereitstellen der Komponente](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/developing/archetype/using.html?lang=de#building-and-installing) in Ihrer lokalen Entwicklungsumgebung. Nachdem die Komponente bereitgestellt wurde, erstellen Sie ein adaptives Formular, um die benutzerdefinierte Komponente zu testen.

1. **Bereitstellen der benutzerdefinierten Komponente in Ihrer Produktionsumgebung**

   Stellen Sie die Komponente nach dem Testen in Ihrer lokalen Entwicklungsumgebung in Ihren Produktionsumgebungen bereit.
