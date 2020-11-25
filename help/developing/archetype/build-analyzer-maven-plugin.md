---
title: AEM come Cloud Service SDK Build Analyzer Maven Plugin
description: Documentazione per il plug-in dell'analizzatore Maven
translation-type: tm+mt
source-git-commit: e32521f35f33897cd72892de393073b01ad963f1
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 3%

---


# AEM come Cloud Service SDK Build Analyzer Maven Plugin {#maven-analyzer-plugin}

Il plugin AEM analizzatore Maven analizza la struttura dei vari progetti di pacchetti di contenuto.

Per informazioni su come includerlo in un progetto di [AEM Maven, consulta la documentazione](https://github.com/adobe/aemanalyser-maven-plugin/blob/main/aemanalyser-maven-plugin/README.md) di Analytics Maven. Il plugin è incluso in AEM Maven archetype versione 25 e superiore.

Di seguito è riportata una tabella che descrive gli analizzatori eseguiti come parte di questo passaggio. Alcuni vengono eseguiti nell’SDK locale, mentre altri vengono eseguiti solo durante la distribuzione della pipeline di Cloud Manager.

| Modulo | Funzione, esempio e risoluzione dei problemi | SDK locale | Cloud Manager |
|---|---|---|---|
| `api-regions-exportsimports` | Controlla se tutti i bundle OSGI presentano dichiarazioni Import-Package soddisfatte dalla dichiarazione Export-Package di altri pacchetti inclusi nel progetto Maven. L&#39;aspetto di un errore è il seguente: <p> </p> `[ERROR] org.acme:mybundle:0.0.1-SNAPSHOT: Bundle org.acme:mybundle:0.0.1-SNAPSHOT is importing package(s) org.acme.foo in start level 20 but no bundle is exporting these for that start level.`<p> </p>Per risolvere i problemi, consultate se il bundle che fornisce il pacchetto è incluso nella distribuzione, oppure guardate il manifesto del bundle che prevedete di esportare per determinare se è stato utilizzato il nome sbagliato o la versione errata. | Sì | Sì |
| `requirements-capabilities` | Controlla se tutte le dichiarazioni di requisiti effettuate nei bundle OSGI sono soddisfatte dalle dichiarazioni di capacità di altri bundle inclusi nel progetto Maven. L&#39;aspetto di un errore è il seguente: <p> </p> `[ERROR] org.acme:mybundle:0.0.1-SNAPSHOT: Artifact org.acme:mybundle:0.0.1-SNAPSHOT requires org.foo.bar in start level 20 but no artifact is providing a matching capability in this start level.`<p> </p> Per risolvere i problemi, controllate il manifesto del bundle che prevedete di dichiarare una capacità per determinare il motivo della sua assenza, o controllate il manifesto del bundle che richiede per verificare che il requisito in esso contenuto sia corretto. | Sì | Sì |
| `bundle-content` | Visualizza un avviso se un bundle contiene il contenuto iniziale specificato con Sling-Initial-Content, che è problematico in AEM come ambiente cluster di Cloud Service. L&#39;avviso è simile al seguente: <p> </p> `[WARNING] org.acme:mybundle:0.0.1-SNAPSHOT: Found initial content : [/]` <p> </p>Per risolvere i problemi relativi alla conversione del contenuto iniziale in istruzioni di reindirizzamento, consulta Repoinit Documentazione. | Sì | Sì |
| `bundle-resources` | Visualizza un avviso se un bundle contiene risorse specificate con l’intestazione Sling-Bundle-Resources, problema nell’AEM come ambiente cluster di Cloud Service. L&#39;avviso è simile al seguente:<p> </p> `[WARNING] org.acme:mybundle:0.0.1-SNAPSHOT: Found bundle resources : [/libs/sling/explorer!/resources/explorer]`<p> </p> Per risolvere i problemi relativi alla conversione delle risorse in istruzioni di reindirizzamento, vedere [Repoinit Documentazione](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=en#repo-init). | Sì | Sì |
| `api-regions`<p> </p>`api-regions-check-order`<p> </p>`api-regions-dependencies`<p> </p>`api-regions-duplicates` | Questi analizzatori controllano alcuni dettagli sulla configurazione delle aree API nelle funzionalità. Per i clienti, la configurazione delle aree API viene generata e non direttamente specificata da tali utenti, questi analizzatori sono attivati perché sono abilitati anche in AEMaaCS. Tuttavia, un errore prodotto da uno di questi potrebbe indicare un bug nel pacchetto di contenuto al processo di conversione del modello di feature. | Sì | Sì |
| `api-regions-crossfeature-dups` | Verifica che i bundle OSGI del cliente non abbiano dichiarazioni di pacchetto di esportazione che ignorano AEM come API pubblica  Cloud Service<p> </p>`[WARNING] org.acme:mybundle:0.0.1-SNAPSHOT: Package overlap found between region global and bundle org.acme:mybundle:0.0.1.SNAPSHOT which comes from feature: [org.acme:myproject.analyse:slingosgifeature:0.0.1-SNAPSHOT]. Both export package: com.day.util`<p> </p>Per risolvere il problema, interrompete l&#39;esportazione di un pacchetto che fa parte dell&#39;API pubblica AEM. | Sì | Sì |