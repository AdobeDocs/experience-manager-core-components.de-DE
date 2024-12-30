---
title: Build Analyzer-Maven-Plug-in des AEM as a Cloud Service-SDK
description: Dokumentation für das lokale Build Analyzer-Maven-Plug-in
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: de26b310-a294-42d6-a0db-91f6036a328c
source-git-commit: eafbe18b13830edde3535fbb67d9ef62b7d045f3
workflow-type: tm+mt
source-wordcount: '656'
ht-degree: 100%

---

# Build Analyzer-Maven-Plug-in des AEM as a Cloud Service-SDK {#maven-analyzer-plugin}

Das Build Analyzer-Maven-Plug-in des AEM as a Cloud Service-SDK analysiert die Struktur der verschiedenen Inhaltspaketprojekte.

Informationen dazu, wie Sie das Plug-in in ein AEM-Maven-Projekt einbinden, finden Sie in der [Maven-Plug-in-Dokumentation](https://github.com/adobe/aemanalyser-maven-plugin/blob/main/aemanalyser-maven-plugin/README.md).

>[!NOTE]
>
>Es wird empfohlen, Ihr Maven-Projekt so zu aktualisieren, dass es die neueste Version des Plugins referenziert, die Sie im [zentralen Maven-Repository](https://repo1.maven.org/maven2/com/adobe/aem/aemanalyser-maven-plugin/) finden.

Das Plug-in verwendet das neueste verfügbare anstelle des im Projekt konfigurierten SDK.

Nachstehend finden Sie eine Tabelle mit den Analyzern, die im Rahmen dieses Schritts ausgeführt werden. <!-- Note that some are executed in the local SDK, while others are only executed during the Cloud Manager pipeline deployment. -->

| Modul | Funktion, Beispiel und Fehlerbehebung | Lokales SDK | Cloud Manager |
|---|---|---|---|
| `api-regions-exportsimports` | Überprüft, ob für alle OSGi-Bundles die Import-Paketdeklarationen durch die Export-Paketdeklaration anderer im Maven-Projekt enthaltener Bundles erfüllt werden. Ein Fehler würde wie folgt aussehen: <p> </p> `[ERROR] org.acme:mybundle:0.0.1-SNAPSHOT: Bundle org.acme:mybundle:0.0.1-SNAPSHOT is importing package(s) org.acme.foo in start level 20 but no bundle is exporting these for that start level.`<p> </p>Überprüfen Sie zur Fehlerbehebung, ob das Bundle, das das Paket bereitstellt, in der Implementierung enthalten ist, oder überprüfen Sie alternativ das Manifest des Bundles, das wahrscheinlich exportiert würde, um festzustellen, ob ein falscher Name oder eine falsche Version verwendet wurde. | Ja | Ja |
| `bundle-unversioned-packages` | Überprüft, ob in OSGi-Bundles eine Version mit einer Export-Package-Deklaration und ein Versionsbereich mit einer Import-Package-Deklaration angegeben sind. Ein Fehler würde wie folgt aussehen: <p> </p> `[ERROR] org.acme:mybundle:0.0.1-SNAPSHOT: Bundle org.acme:mybundle:0.0.1-SNAPSHOT is exporting package org.acme.foo without a version.`<p> </p>Stellen Sie zur Fehlerbehebung sicher, dass Sie diesem Package `package-info.java` hinzufügen, sodass die zu exportierende Version angegeben ist. | Ja | Ja |
| `requirements-capabilities` | Überprüft, ob alle in OSGi-Bundles abgegebenen Anforderungsdeklarationen durch die Leistungsdeklarationen anderer im Maven-Projekt enthaltener Bundles erfüllt werden. Ein Fehler würde wie folgt aussehen: <p> </p> `[ERROR] org.acme:mybundle:0.0.1-SNAPSHOT: Artifact org.acme:mybundle:0.0.1-SNAPSHOT requires org.foo.bar in start level 20 but no artifact is providing a matching capability in this start level.`<p> </p> Sehen Sie sich zur Fehlerbehebung das Manifest des Bundles an, von dem Sie erwarten, dass es eine Funktion deklariert, um festzustellen, warum es fehlt, oder überprüfen Sie das Manifest des erforderlichen Bundles, um festzustellen, ob die darin enthaltenen Anforderungen korrekt sind. | Ja | Ja |
| `bundle-resources` | Gibt eine Warnung aus, wenn ein Bundle Ressourcen enthält, die mit dem Sling-Bundle-Resources-Header angegeben wurden, was in der AEM as a Cloud Service-Cluster-Umgebung problematisch ist. Die Warnung sieht folgendermaßen aus:<p> </p> `[WARNING] org.acme:mybundle:0.0.1-SNAPSHOT: Found bundle resources : [/libs/sling/explorer!/resources/explorer]`<p> </p> Informationen zur Fehlerbehebung beim Konvertieren der Ressourcen in Repoinit-Anweisungen finden Sie in der [Repoinit-Dokumentation](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=de#repo-init). | Ja | Ja |
| `api-regions`<p> </p>`api-regions-check-order`<p> </p>`api-regions-dependencies`<p> </p>`api-regions-duplicates` | Diese Analyzer überprüfen einige Details im Zusammenhang mit der [Konvertierung des Inhaltspakets in Feature-Modelle](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/overview.html?lang=de#deploying), wodurch Artefakte erstellt werden, die dem Sling-Feature-Modell entsprechen. Alle Fehler sollten dem Adobe-Support gemeldet werden. | Ja | Ja |
| `api-regions-crossfeature-dups` | Überprüft, dass OSGi-Bundles der Kundschaft keine Export-Paketdeklarationen haben, die die öffentliche API von AEM as a Cloud Service außer Kraft setzen.<p> </p>`[WARNING] org.acme:mybundle:0.0.1-SNAPSHOT: Package overlap found between region global and bundle org.acme:mybundle:0.0.1.SNAPSHOT which comes from feature: [org.acme:myproject.analyse:slingosgifeature:0.0.1-SNAPSHOT]. Both export package: com.day.util`<p> </p>Um dieses Problem zu beheben, beenden Sie den Export eines Pakets, das Teil der öffentlichen AEM-API ist. | Ja | Ja |
| `repoinit` | Prüft die Syntax aller Repoinit-Abschnitte. | Ja | Ja |
| `bundle-nativecode` | Überprüft, dass OSGi-Bundles keinen nativen Code installieren. | Ja | Ja |
| `configuration-api` | Validiert wichtige OSGi-Konfigurationen. <p> </p> `Configuration org.apache.felix.webconsole.internal.servlet.OsgiManager: Configuration is not allowed (com.mysite:mysite.all:1.0.0-SNAPSHOT\|com.mysite:mysite.ui.config:1.0.0-SNAPSHOT)` | Ja | Ja |
| `region-deprecated-api` | Prüft, ob eine [veraltete API](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/deprecated-apis.html?lang=de) verwendet wird. <p> </p>`[WARNING] com.mysite:mysite.core:1.0.0-SNAPSHOT: Usage of deprecated package found : org.apache.sling.settings : Avoid these features at runtime: run modes, file system access (com.mysite:mysite.all:1.0.0-SNAPSHOT)` | Ja | Ja |
| `artifact-rules` | Prüft Abhängigkeiten wie Bundles und Inhaltspakete, um bekannte Probleme in Artefakten zu vermeiden.<p> </p>`[WARNING] [artifact-rules] com.adobe.acs:acs-aem-commons-bundle:5.0.4: Use at least version 5.0.10 (com.mysite:mysite.all:1.0.0-SNAPSHOT)` | Ja | Ja |
| `aem-env-var` | Überprüft die Verwendung von env vars gemäß dem [Handbuch zur Variablenbenennung](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/configuring-osgi.html?lang=de#variable-naming)<p> </p>`[ERROR] Configuration org.apache.felix.webconsole.internal.servlet.OsgiManager: Value for property 'port' must not use env vars prefixed with INTERNAL_ or ADOBE_ (com.mysite1:my-site-1.all:1.0.0-SNAPSHOT\|com.mysite1:my-site-1.ui.config:1.0.0-SNAPSHOT)` | Ja | Ja |
| `content-package-validation` | Führt filevault-Validatoren. Standardmäßig ist jackrabbit-docviewparser aktiviert, der nach der korrekt formatierten Inhaltssyntax von XML in Paketen sucht, die während der Bereitstellung installiert werden.<p> </p>`[main] WARN org.apache.sling.feature.analyser.task.impl.CheckContentPackages - ValidationViolation: "jackrabbit-docviewparser: Invalid XML found: The reference to entity "se" must end with the ';' delimiter.", filePath=jcr_root/apps/somename/configs/com.adobe.test.Invalid.xml, nodePath=/apps/somename/configs/com.adobe.test.Invalid`<p> </p>Um dieses Problem zu beheben, überprüfen Sie die vom Analyzer benannte Datei auf XML-Probleme. | Ja | Ja |
| `aem-provider-type` | Überprüft, ob Anwendungs-Code eine Schnittstelle/Klasse vom Typ „ProviderType“ von AEM (dem Produkt) implementiert oder erweitert; siehe [CQBP-84](https://experienceleague.adobe.com/docs/experience-manager-cloud-manager/using/how-to-use/custom-code-quality-rules.html?lang=de#product-apis-annotated-with-providertype-should-not-be-implemented-or-extended-by-customers) | Ja | Ja |
| `configurations-basic` | Überprüft OSGi-Konfigurationen auf häufige Fehler, z. B. ob der richtige Typ für die Eigenschaft „service.ranking“ angegeben wurde. | Ja | Ja |

{style="table-layout:auto"}

## Bekannte Probleme

Nachstehend finden Sie eine Liste der bekannten Probleme bei der Verwendung des Build Analyzer Maven-Plug-ins.

### Das Build Analyzer-Maven-Plug-in konnte nicht im lokalen SDK ausgeführt werden.

Wenn Sie das lokale SDK mit einer Build Analyzer-Maven-Plug-in-Version verwenden, die kleiner als `1.1.2` ist, kann die Ausführung des Plug-ins zum folgenden Fehler führen. Aktualisieren Sie in diesem Fall Ihr Projekt auf die neueste Version des Plug-ins.

```txt
[ERROR] Failed to execute goal com.adobe.aem:aemanalyser-maven-plugin:1.1.0:analyse (default-analyse) on project mysite.analyse: Execution default-analyse of goal com.adobe.aem:aemanalyser-maven-plugin:1.1.0:analyse failed: arraycopy: source index -1 out of bounds for char[65536] -> [Help 1]
```

Wenn Sie das Projekt mit dem AEM-Projektarchetyp eingerichtet haben, passen Sie die Eigenschaft im Maven-Stamm `pom.xml` wie unten beschrieben an.

```xml
   ...
   <properties>
      ...
      <aemanalyser.version>1.1.2</aemanalyser.version> <!-- Make sure to use the latest release -->
      ...
   </properties>
```
