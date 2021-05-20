---
title: Build Analyzer-Maven-Plug-in des AEM as a Cloud Service-SDK
description: Dokumentation für das lokale Build Analyzer-Maven-Plug-in
feature: Kernkomponenten, AEM-Projektarchetyp
role: Architect, Developer, Administrator
exl-id: de26b310-a294-42d6-a0db-91f6036a328c
source-git-commit: 8ff36ca143af9496f988b1ca65475497181def1d
workflow-type: tm+mt
source-wordcount: '475'
ht-degree: 100%

---

# Build Analyzer-Maven-Plug-in des AEM as a Cloud Service-SDK {#maven-analyzer-plugin}

Das Build Analyzer-Maven-Plug-in des AEM as a Cloud Service-SDK analysiert die Struktur der verschiedenen Inhaltspaketprojekte.

Informationen dazu, wie Sie das Plug-in in ein AEM-Maven-Projekt einbinden, finden Sie in der [Maven-Plug-in-Dokumentation](https://github.com/adobe/aemanalyser-maven-plugin/blob/main/aemanalyser-maven-plugin/README.md).

>[!NOTE]
>
>Es wird empfohlen, dass Sie Ihr Maven-Projekt so aktualisieren, dass es auf die neueste Version des Plug-ins im zentralen Repository von Maven verweist, das sich an folgendem Speicherort befindet: https://repo1.maven.org/maven2/com/adobe/aem/aemanalyser-maven-plugin/

Nachstehend finden Sie eine Tabelle mit den Analyzern, die im Rahmen dieses Schritts ausgeführt werden. <!-- Note that some are executed in the local SDK, while others are only executed during the Cloud Manager pipeline deployment. -->

| Modul | Funktion, Beispiel und Fehlerbehebung | Lokales SDK | Cloud Manager |
|---|---|---|---|
| `api-regions-exportsimports` | Überprüft, ob für alle OSGI-Bundles die Import-Paketdeklarationen durch die Export-Paketdeklaration anderer im Maven-Projekt enthaltener Bundles erfüllt werden. Ein Fehler würde wie folgt aussehen: <p> </p> `[ERROR] org.acme:mybundle:0.0.1-SNAPSHOT: Bundle org.acme:mybundle:0.0.1-SNAPSHOT is importing package(s) org.acme.foo in start level 20 but no bundle is exporting these for that start level.`<p> </p>Überprüfen Sie zur Fehlerbehebung, ob das Bundle, das das Paket bereitstellt, in der Implementierung enthalten ist, oder überprüfen Sie alternativ das Manifest des Bundles, das wahrscheinlich exportiert würde, um festzustellen, ob ein falscher Name oder eine falsche Version verwendet wurde. | Ja | Ja |
| `requirements-capabilities` | Überprüft, ob alle in OSGI-Bundles abgegebenen Anforderungsdeklarationen durch die Leistungsdeklarationen anderer im Maven-Projekt enthaltener Bundles erfüllt werden. Ein Fehler würde wie folgt aussehen: <p> </p> `[ERROR] org.acme:mybundle:0.0.1-SNAPSHOT: Artifact org.acme:mybundle:0.0.1-SNAPSHOT requires org.foo.bar in start level 20 but no artifact is providing a matching capability in this start level.`<p> </p> Sehen Sie sich zur Fehlerbehebung das Manifest des Bundles an, von dem Sie erwarten, dass es eine Funktion deklariert, um festzustellen, warum es fehlt, oder überprüfen Sie das Manifest des erforderlichen Bundles, um festzustellen, ob die darin enthaltenen Anforderungen korrekt sind. | Ja | Ja |
| `bundle-content` | Gibt eine Warnung aus, wenn ein Bundle anfängliche Inhalte enthält, die mit anfänglichem Sling-Inhalt angegeben wurden, was in der AEM as a Cloud Service-Cluster-Umgebung problematisch ist. Die Warnung sieht folgendermaßen aus: <p> </p> `[WARNING] org.acme:mybundle:0.0.1-SNAPSHOT: Found initial content : [/]` <p> </p>Informationen zur Fehlerbehebung beim Konvertieren des ursprünglichen Inhalts in Repoinit-Anweisungen finden Sie in der Repoinit-Dokumentation. | Ja | Ja |
| `bundle-resources` | Gibt eine Warnung aus, wenn ein Bundle Ressourcen enthält, die mit dem Sling-Bundle-Resources-Header angegeben wurden, was in der AEM as a Cloud Service-Cluster-Umgebung problematisch ist. Die Warnung sieht folgendermaßen aus:<p> </p> `[WARNING] org.acme:mybundle:0.0.1-SNAPSHOT: Found bundle resources : [/libs/sling/explorer!/resources/explorer]`<p> </p> Informationen zur Fehlerbehebung beim Konvertieren der Ressourcen in Repoinit-Anweisungen finden Sie in der [Repoinit-Dokumentation](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=de#repo-init). | Ja | Ja |
| `api-regions`<p> </p>`api-regions-check-order`<p> </p>`api-regions-dependencies`<p> </p>`api-regions-duplicates` | Diese Analyzer überprüfen einige Details im Zusammenhang mit der [Konvertierung des Inhaltspakets in Feature-Modelle](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/overview.html?lang=de#deploying), wodurch Artefakte erstellt werden, die dem Sling-Feature-Modell entsprechen. Alle Fehler sollten dem Adobe-Support gemeldet werden. | Ja | Ja |
| `api-regions-crossfeature-dups` | Überprüft, dass Kunden-OSGI-Bundles keine Export-Paketdeklarationen haben, die die öffentliche API von AEM as a Cloud Service außer Kraft setzen.<p> </p>`[WARNING] org.acme:mybundle:0.0.1-SNAPSHOT: Package overlap found between region global and bundle org.acme:mybundle:0.0.1.SNAPSHOT which comes from feature: [org.acme:myproject.analyse:slingosgifeature:0.0.1-SNAPSHOT]. Both export package: com.day.util`<p> </p>Um dieses Problem zu beheben, beenden Sie den Export eines Pakets, das Teil der öffentlichen AEM-API ist. | Ja | Ja |
| `repoinit` | Prüft die Syntax aller Repoinit-Abschnitte. | Ja | Ja |
| `bundle-nativecode` | Prüft, dass OSGI-Bundles keinen nativen Code installieren. | Ja | Ja |
