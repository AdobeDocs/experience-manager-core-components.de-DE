---
title: Navigationskomponente
description: Mit der Navigationskomponente können Benutzer leicht durch eine globalisierte Site-Struktur navigieren.
translation-type: ht
source-git-commit: c186e9ec3944d785ab0376769cf7f2307049a809
workflow-type: ht
source-wordcount: '1369'
ht-degree: 100%

---


# Navigationskomponente{#navigation-component}

Mit der Navigationskomponente können Benutzer leicht durch eine globalisierte Site-Struktur navigieren.

## Verwendung {#usage}

In der Navigationskomponente wird ein Seitenbaum aufgelistet, sodass Benutzer einer Website problemlos in der Site-Struktur navigieren können.

Die Navigationskomponente kann die globale Site-Struktur Ihrer Site automatisch erkennen und [automatisch an eine lokalisierte Site anpassen.](#localized-site-structure) Darüber hinaus kann eine beliebige Site-Struktur durch die Verwendung von [Shadow-Umleitungsseiten](#shadow-structure) zur Darstellung einer anderen Struktur als Ihrer Hauptinhaltsstruktur unterstützt werden.

Das Dialogfeld [„Bearbeiten“](#edit-dialog) ermöglicht es dem Inhaltsautor, die Navigationsstammseite zusammen mit der Navigationstiefe zu definieren. Das [Dialogfeld „Design“](#design-dialog) ermöglicht es dem Vorlagenautor, Standardwerte für den Navigationsstamm und die Tiefe zu definieren.

## Unterstützung für lokalisierte Site-Strukturen {#localized-site-structure}

Webseiten werden oft in verschiedenen Sprachen für verschiedene Regionen angeboten. Normalerweise enthält jede lokalisierte Seite ein Navigationselement, das als Teil der Seitenvorlage enthalten ist. Mit der Navigationskomponente können Sie sie einmal in einer Vorlage für alle Seiten Ihrer Site platzieren. Sie wird dann, basierend auf Ihrer globalisierten Site-Struktur, automatisch an die einzelnen lokalisierten Seiten angepasst.

* Ein Beispiel dafür, wie die Lokalisierungsfunktion der Navigationskomponente funktioniert, finden Sie [unten](#example-localization).
* Ein Beispiel dafür, wie die Lokalisierungsfunktionen der Kernkomponenten zusammenarbeiten, finden Sie auf der Seite [Kernkomponenten](/help/get-started/localization.md) unter „Lokalisierungsfunktionen“.

### Beispiel {#example-localization}

Nehmen wir an, dass Ihr Inhalt wie folgt aussieht:

```
/content
+-- wknd
   +-- language-masters
      +-- de
         \-- experience
            \-- arctic-surfing-in-lofoten
      +-- en
         \-- experience
            \-- arctic-surfing-in-lofoten
      +-- es
      +-- fr
      \-- it
   +-- us
      +-- en
         \-- experience
            \-- arctic-surfing-in-lofoten
      \-- es
   \-- ch
      +-- de
         \-- experience
            \-- arctic-surfing-in-lofoten
      +-- fr
      \-- it
+-- wknd-events
\-- wknd-shop
```

Für die Site „We.Retail“ möchten Sie wahrscheinlich die Navigationskomponente auf einer Seitenvorlage als Teil der Kopfzeile platzieren. Sobald die Komponente ein Teil der Vorlage ist, können Sie den **Navigationsstamm** der Komponente auf `/content/wknd/language-masters/en` festlegen, da dort Ihr Master-Inhalt für diese Site beginnt. Eventuell möchten Sie auch die **Tiefe der Navigationsstruktur** auf `2` festlegen, da Sie wahrscheinlich nicht möchten, dass die gesamte Inhaltsstruktur durch die Komponente angezeigt wird, sondern die ersten beiden Ebenen, sodass dies als Übersicht dient.

Anhand des Wertes des **Navigationsstamms** weiß die Navigationskomponente, dass nach `/content/wknd/language-masters/en` die Navigation beginnt, und sie kann somit Navigationsoptionen generieren, indem sie die Struktur der Site auf zwei Ebenen nach unten (wie durch den Wert der **Navigationsstrukturtiefe** vorgegeben) rekursiv darstellt.

Unabhängig davon, welche lokalisierte Seite ein Benutzer ansieht, kann die Navigationskomponente die entsprechende lokalisierte Seite finden, indem sie den Speicherort der aktuellen Seite kennt, zum Stammverzeichnis zurückkehrt und sich dann zur entsprechenden Seite vorarbeitet.

Wenn ein Besucher also `/content/ch/de/experience/arctic-surfing-in-lofoten` anzeigt, kann die Komponente die Navigationsstruktur basierend auf `/content/wknd/language-masters/de` generieren. Wenn der Besucher `/content/us/en/experience/arctic-surfing-in-lofoten` anzeigt, kann die Komponente dementsprechend die Navigationsstruktur basierend auf `/content/wknd/language-masters/en` generieren.

## Unterstützung für Shadow Site-Struktur {#shadow-structure}

Manchmal ist es notwendig, ein Navigationsmenü für den Besucher zu erstellen, welches sich von der tatsächlichen Site-Struktur unterscheidet. Vielleicht soll eine Promotion bestimmte Inhalte im Menü hervorheben, indem die Liste der Inhalte neu angeordnet werden. Mithilfe von Shadow-Seiten, die einfach zu anderen Inhaltsseiten umleiten, kann die Navigationskomponente eine beliebige erforderliche Navigationsstruktur generieren.

Dazu müssen Sie Folgendes tun:

1. Erstellen Sie Shadow-Seiten als leere Seiten, die Ihre gewünschte Site-Struktur repräsentieren. Dies wird häufig als Shadow-Standortstruktur bezeichnet.
1. Legen Sie die Werte für die **Umleitung** in den Seiteneinstellungen auf diesen Seiten fest, um auf die tatsächlichen Inhaltsseiten zu verweisen.
1. Legen Sie die Option **In der Navigation ausblenden** in den Seiteneigenschaften der Shadow-Seiten fest.
1. Legen Sie den **Navigationsstammwert** der Navigationskomponente fest, um auf den Stamm der neuen Shadow-Site-Struktur zu verweisen.

Die Navigationskomponente rendert dann das Menü basierend auf der Shadow-Site-Struktur. Die von der Komponente gerenderten Links beziehen sich auf die tatsächlichen Inhaltsseiten, auf die die Shadow-Seiten umleiten, und nicht auf die Shadow-Seiten selbst. Darüber hinaus zeigt die Komponente die Namen der tatsächlichen Seiten an und hebt die aktive Seite korrekt hervor, auch wenn die Navigation auf Shadow-Seiten basiert. Die Navigationskomponente macht die Shadow-Seiten für den Besucher vollständig transparent.

>[!NOTE]
>Durch Shadow-Seiten werden Ihre Navigationsoptionen wesentlich flexibler. Beachten Sie jedoch, dass diese Struktur dann vollständig manuell verwaltet wird. Wenn Sie den Inhalt Ihren tatsächlichen Site neu anordnen oder Inhalte hinzufügen/entfernen, müssen Sie die Shadow-Struktur nach Bedarf manuell aktualisieren.

>[!NOTE]
>Beim Rendern einer Shadow-Site-Struktur werden nur die Shadow-Seiten von der Navigationslogik rekursiv dargestellt. Die Logik führt keine Rekursion der Struktur der Umleitungsziele aus.

## Version und Kompatibilität {#version-and-compatibility}

Die aktuelle Version der Navigationskomponente ist v1, die mit Version 2.0.0 der Kernkomponenten im Januar 2018 eingeführt wurde und in diesem Dokument beschrieben wird.

Die folgende Tabelle enthält alle unterstützten Versionen der Komponente, die AEM-Versionen, mit denen die Versionen der Komponente kompatibel sind, sowie Links zur Dokumentation für frühere Versionen.

| Komponentenversion | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v1 | Kompatibel | Kompatibel | Kompatibel |

Weitere Informationen zu Kernkomponentenversionen und -freigaben finden Sie in den [Kernkomponentenversionen](/help/versions.md).

## Musterkomponentenausgabe {#sample-component-output}

Um die Navigationskomponente sowie Beispiele für die Konfigurationsoptionen sowie HTML- und JSON-Ausgaben zu erhalten, besuchen Sie die [Komponentenbibliothek](https://adobe.com/go/aem_cmp_library_navigation_de).

## Technische Details {#technical-details}

Die aktuelle technische Dokumentation zur Navigationskomponente [finden Sie auf GitHub](https://adobe.com/go/aem_cmp_tech_navigation_v1_de).

Weitere Informationen zur Entwicklung von Kernkomponenten finden Sie in der [Dokumentation zu Kernkomponenten für Entwickler](/help/developing/overview.md).

>[!NOTE]
>
>Ab Version 2.1.0 der Kernkomponente unterstützt die Navigationskomponente [schema.org-Mikrodaten](https://schema.org).

## Dialogfeld „Bearbeiten“ {#edit-dialog}

Im Dialogfeld „Bearbeiten“ kann der Inhaltsautor die Stammseite für die Navigation und die Tiefe der Navigationsstruktur definieren.

### Registerkarte „Eigenschaften“ {#properties-tab}

![Registerkarte „Eigenschaften“ im Dialogfeld „Bearbeiten“ der Navigationskomponente](/help/assets/navigation-edit-properties.png)

* **Navigationsstamm** – Die Stammseite, die zum Generieren der Navigationsstruktur verwendet wird.
* **Stammebenen ausschließen** - Häufig soll der Stamm nicht in die Navigation eingeschlossen werden. Mit dieser Option können Sie festlegen, wie viele Ebenen oberhalb des Stamms Sie ausschließen möchten. Beispiel:
   * 0 = Stammebene anzeigen
   * 1 = Stammebene ausschließen
   * 2 = Stammebene und Ebene oberhalb ausschließen
   * usw.
* **Sammlung aller untergeordneten Seiten** – Sammeln Sie alle untergeordneten Seiten, die sich auf dem Navigationsstamm befinden.
* **Navigationsstrukturtiefe** – Definiert, wie viele Ebenen die Komponente in der Navigationsstruktur im Verhältnis zum Navigationsstamm anzeigen soll (nur verfügbar, wenn **Sammlung aller untergeordneten Seiten** nicht ausgewählt sind).
* **Shadowing deaktivieren** – Wenn es sich bei der Seite in der Hierarchie um einen Redirect handelt, wird anstelle der Zielseite der Name der umleitenden (Redirect)-Seite angezeigt. Weitere Informationen finden Sie unter [Unterstützung für Shadow Site-Struktur](#shadow-structure).
* **ID** – Diese Option dient zur Kontrolle der eindeutigen Kennung der Komponente in der HTML-Datei und auf der [Datenschicht](/help/developing/data-layer/overview.md).
   * Wenn Sie das Feld leer lassen, wird automatisch eine eindeutige ID generiert, die Sie über die resultierende Seite finden.
   * Sofern eine ID angegeben wird, ist vom Autor sicherzustellen, dass diese eindeutig ist.
   * Änderungen der ID können sich auf das CSS-, JS- und Datenschicht-Tracking auswirken.

### Registerkarte „Barrierefreiheit“ {#accessibility-tab}

![Registerkarte „Barrierefreiheit“ im Dialogfeld „Bearbeiten“ der Navigationskomponente](/help/assets/navigation-edit-accessibility.png)

Auf der Registerkarte **Barrierefreiheit** können Werte für die [ARIA-Barrierefreiheits-Bezeichungen](https://www.w3.org/WAI/standards-guidelines/aria/) für die Komponente festgelegt werden.

* **Bezeichnung** - Wert eines ARIA-Bezeichnungs-Attributs für die Komponente

## Dialogfeld „Design“ {#design-dialog}

Das Dialogfeld „Design“ ermöglicht es dem Vorlagenautor, die Standardwerte für die Navigationsstammseite und die Navigationstiefe festzulegen, die den Inhaltsautoren angezeigt werden.

### Registerkarte „Eigenschaften“ {#properties-tab-design}

![Dialogfeld „Design“ der Navigationskomponente](/help/assets/navigation-design.png)

* **Navigationsstamm** – Der Standardwert der Stammseite der Navigationsstruktur, die zum Generieren der Navigationsstruktur verwendet und standardmäßig verwendet wird, wenn der Inhaltsautor die Komponente der Seite hinzufügt.
* **Stammebenen ausschließen** - Häufig soll der Stamm nicht in die Navigation eingeschlossen werden. Mit dieser Option können Sie den Standard dafür festlegen, wie viele Ebenen oberhalb des Stamms Sie ausschließen möchten. Beispiel:
   * 0 = Stammebene anzeigen
   * 1 = Stammebene ausschließen
   * 2 = Stammebene und Ebene oberhalb ausschließen
   * usw.
* **Sammlung aller untergeordneten Seiten** – Der Standardwert der Option zur Sammlung aller Seiten, die sich auf dem Navigationsstamm befinden.
* **Navigationsstruktur der Tiefe** – Standardwert der Navigationsstruktur der Tiefe.
* **Shadowing deaktivieren** – Der Standardwert dafür, wann das Shadowing beim Hinzufügen einer Navigationskomponente deaktiviert werden soll

### Registerkarte „Stile“ {#styles-tab}

Die Navigationskomponente unterstützt das AEM-[Stilsystem](/help/get-started/authoring.md#component-styling).
