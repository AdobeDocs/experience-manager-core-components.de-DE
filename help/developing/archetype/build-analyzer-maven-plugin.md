---
title: AEM als Cloud Service SDK Build Analyzer Maven Plugin
description: Dokumentation für das lokale Maven Build Analyzer-Plugin
translation-type: tm+mt
source-git-commit: abb43865278f884555d1bb963686ccc561f319b5
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 3%

---


# AEM als Cloud Service SDK Build Analyzer Maven Plugin {#maven-analyzer-plugin}

Das AEM als Cloud Service SDK Build Analyzer Maven Plugin analysiert die Struktur der verschiedenen Inhaltspaketprojekte.

Informationen dazu, wie Sie es in ein AEM Maven-Projekt einbeziehen, finden Sie in der Dokumentation [zum](https://github.com/adobe/aemanalyser-maven-plugin/blob/main/aemanalyser-maven-plugin/README.md) AEM Analyzer Maven Plugin.

Nachstehend finden Sie eine Tabelle mit den Analyzern, die im Rahmen dieses Schritts ausgeführt werden. <!-- Note that some are executed in the local SDK, while others are only executed during the Cloud Manager pipeline deployment. -->

| Modul | Funktion, Beispiel und Fehlerbehebung | Lokales SDK | Cloud Manager |
|---|---|---|---|
| `api-regions-exportsimports` | Überprüft, ob alle OSGI-Pakete ihre Import-Paket-Erklärungen haben, die mit der Ausfuhrpaket-Erklärung anderer im Maven-Projekt eingeschlossener Pakete übereinstimmen. Ein Fehler würde wie folgt aussehen: <p> </p> `[ERROR] org.acme:mybundle:0.0.1-SNAPSHOT: Bundle org.acme:mybundle:0.0.1-SNAPSHOT is importing package(s) org.acme.foo in start level 20 but no bundle is exporting these for that start level.`<p> </p>Um eine Fehlerbehebung durchzuführen, prüfen Sie, ob das Paket, das das Paket bereitstellt, in der Bereitstellung enthalten ist, oder überprüfen Sie alternativ das Manifest des Pakets, das Sie voraussichtlich exportieren werden, um festzustellen, ob der falsche Name oder die falsche Version verwendet wurde. | Ja | Ja |
| `requirements-capabilities` | Überprüft, ob alle in OSGI-Bundles abgegebenen Anforderungsdeklarationen durch die Leistungsdeklarationen anderer im Maven-Projekt enthaltener Bundles erfüllt werden. Ein Fehler würde wie folgt aussehen: <p> </p> `[ERROR] org.acme:mybundle:0.0.1-SNAPSHOT: Artifact org.acme:mybundle:0.0.1-SNAPSHOT requires org.foo.bar in start level 20 but no artifact is providing a matching capability in this start level.`<p> </p> Um eine Fehlerbehebung durchzuführen, sehen Sie sich das Manifest des Pakets an, bei dem Sie erwarten würden, dass Sie eine Funktion zur Bestimmung des Fehlens des Pakets deklarieren können, oder überprüfen Sie das Manifest des erforderlichen Bundles, um zu sehen, dass die darin enthaltene Anforderung richtig ist. | Ja | Ja |
| `bundle-content` | Gibt eine Warnung aus, wenn ein Bundle anfänglichen Inhalt enthält, der mit Sling-Initial-Content angegeben wurde. Dies ist problematisch in der AEM als Cloud Service-Cluster-Umgebung. Die Warnung sieht folgendermaßen aus: <p> </p> `[WARNING] org.acme:mybundle:0.0.1-SNAPSHOT: Found initial content : [/]` <p> </p>Informationen zum Beheben von Fehlern bei der Konvertierung des ursprünglichen Inhalts in Aussagen zum Zurückweisen finden Sie in der Dokumentation zum Zurückweisen. | Ja | Ja |
| `bundle-resources` | Gibt eine Warnung aus, wenn ein Bundle Ressourcen enthält, die mit der Kopfzeile Sling-Bundle-Resources angegeben wurden. Dies ist problematisch in der AEM als Cloud Service-Cluster-Umgebung. Die Warnung sieht folgendermaßen aus:<p> </p> `[WARNING] org.acme:mybundle:0.0.1-SNAPSHOT: Found bundle resources : [/libs/sling/explorer!/resources/explorer]`<p> </p> Informationen zum Beheben von Fehlern bei der Konvertierung der Ressourcen in Aussagen zum erneuten Verweisen finden Sie unter [Dokumentation](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=en#repo-init)zum erneuten Verweisen. | Ja | Ja |
| `api-regions`<p> </p>`api-regions-check-order`<p> </p>`api-regions-dependencies`<p> </p>`api-regions-duplicates` | Diese Analysegeräte prüfen einige Details zur Einrichtung der API-Regionen in den Funktionen. Für Kunden wird die API-Regionen-Konfiguration generiert und von ihnen nicht direkt angegeben, sind diese Analysatoren aktiviert, da sie auch in AEMaaCS aktiviert sind. Ein Fehler, der von diesen verursacht wurde, deutet jedoch auf einen Fehler im Inhaltspaket hin, der den Modellkonvertierungsprozess kennzeichnet. | Ja | Ja |
| `api-regions-crossfeature-dups` | Prüft, ob die OSGI-Pakete des Kunden keine Export-Paket-Deklarationen haben, die AEM als öffentliche API des Cloud Service außer Kraft setzen<p> </p>`[WARNING] org.acme:mybundle:0.0.1-SNAPSHOT: Package overlap found between region global and bundle org.acme:mybundle:0.0.1.SNAPSHOT which comes from feature: [org.acme:myproject.analyse:slingosgifeature:0.0.1-SNAPSHOT]. Both export package: com.day.util`<p> </p>Um dieses Problem zu beheben, beenden Sie den Export eines Pakets, das Teil der öffentlichen AEM API ist. | Ja | Ja |