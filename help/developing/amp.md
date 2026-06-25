---
title: Supporto AMP per i Componenti core
description: 'I Componenti core supportano AMP: Accelerated Mobile Pages'
role: Developer, Admin
exl-id: 1fd9b6b5-0e4d-48c7-8faa-42e0d4a6bbd0
TQID: https://experienceleague.adobe.com/5v1tXLzHNRvAxy6-aJipN-ZYzsPJ1xFNc1hKmz73wic
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: e2c1b6d3-bb7e-4fe8-8c72-f7b403298e91
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: c18d9e03-ac7d-4811-9c92-3e92ddc70ade
source-git-commit: 59ca85e0f0b99ba46bb2b85f383f1fefd2b1c5fd
workflow-type: tm+mt
source-wordcount: 680
ht-degree: 76%

---


# Supporto AMP per i Componenti core {#amp-support}

A partire dalla [versione 2.11.0](/help/versions.md) dei Componenti core, è pienamente supportato [AMP: Accelerated Mobile Pages](https://developers.google.com/amp).

Questo documento offre una panoramica del supporto AMP e delle modalità di abilitazione di tale funzionalità per i siti. Tuttavia, per informazioni tecniche complete, vedi la [documentazione per gli sviluppatori GitHub.](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)

## Che cos’è AMP? {#what-is-amp}

Accelerated Mobile Pages o AMP è un framework open-source progettato originariamente da Google per ottimizzare le pagine per la navigazione mobile. Le pagine AMP vengono generalmente caricate molto più rapidamente delle pagine web standard, offrendo una migliore esperienza sui dispositivi mobili.

## AMP nei Componenti core {#amp-in-core-components}

Il supporto per AMP nei Componenti core è [completamente configurabile.](#enabling-amp) Le versioni AMP delle pagine possono essere pubblicate in via esclusiva, insieme alle versioni HTML standard, o non pubblicate affatto.

I Componenti core utilizzano `amp` come selettore Sling per eseguire il rendering di una pagina AMP. Ad esempio, `example.html` esegue il rendering della pagina normale e `example.amp.html` è la versione AMP.

I singoli progetti possono decidere se utilizzare o meno AMP. Infatti, poiché le pagine AMP e HTML standard possono essere distribuite in parallelo, un progetto può scegliere di utilizzare AMP solo su determinate pagine.

## Introduzione al supporto AMP nel progetto {#getting-started}

Sebbene il supporto AMP offra una grande flessibilità, per iniziare a utilizzarlo occorrono solo alcuni semplici passaggi:

1. [Installare i Componenti core](/help/get-started/using.md#download-and-install)
   * Per i progetti AEM as a Cloud Service, i Componenti core sono disponibili per impostazione predefinita e non è necessaria alcuna installazione aggiuntiva.
   * Per i progetti on-premise e AMS, puoi [scaricare il pacchetto di contenuti più recente per i Componenti core da GitHub](https://github.com/adobe/aem-core-wcm-components/releases/latest) e installarlo nei tuoi ambienti AEM.
   * Se il progetto on-premise o AMS utilizza una versione dei Componenti core precedente alla 2.14.0, devi installare l’estensione AMP disponibile come parte della versione su GitHub.
1. Puntare il componente `resourceSuperType` a `core/wcm/extensions/amp/components/page/v1/page`.
   * Se hai utilizzato [Archetipo progetto AEM](/help/developing/archetype/using.md) per il progetto come best practice consigliata e hai scelto [l&#39;opzione per abilitare il supporto AMP,](https://github.com/adobe/aem-project-archetype/tree/develop) l&#39;operazione è stata eseguita automaticamente.
1. [Abilita il supporto AMP](#enabling-amp) a livello di modello oppure sulle singole pagine.
1. [Distribuisci i file CSS allineati](#css-requirements) come richiesto.

### Abilitazione di AMP per le pagine {#enabling-amp}

Per abilitare AMP per una pagina, è necessario selezionare la **Modalità AMP** in [Criterio pagina.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=it#editing-a-template-page-policy-template-author-developer)

![Opzioni di Criterio pagina AMP](/help/assets/amp-policy.png)

* **Nessun AMP**: la pagina viene distribuita solo come HTML standard.
* **AMP associata**: la pagina viene distribuita sia come AMP che come HTML.
* **Solo AMP**: la pagina viene distribuita solo come AMP.

Le impostazioni AMP per una pagina possono anche essere ignorate in [Proprietà pagina](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html?lang=it) per una singola pagina.

![Proprietà pagina AMP](/help/assets/amp-page-properties.png)

* **Eredita dal modello della pagina**: questo è il valore predefinito che consente di prendere l’impostazione dal criterio del modello della pagina.
* **Nessun AMP**: la pagina viene distribuita solo come HTML standard.
* **AMP associata**: la pagina viene distribuita sia come AMP che come HTML.
* **Solo AMP**: la pagina viene distribuita solo come AMP.

Queste opzioni vengono visualizzate nell&#39;interfaccia utente solo se `resourceSuperType` è impostato correttamente per il supporto AMP. Il contenuto di esempio WKND predefinito non ha impostato `resourceSuperType` e pertanto le opzioni per AMP non sono visibili nell&#39;interfaccia utente.

### Requisiti CSS {#css-requirements}

Quando si utilizza AMP con i Componenti core, la differenza principale è che AMP richiede che tutti i [CSS siano allineati](including-clientlibs.md#inlining) nell’elemento `<head>` e ottimizzati.

Per supportare questa funzione, viene utilizzato un componente pagina personalizzato che carica solo il CSS specifico per AMP per i componenti presenti nella pagina.

>[!NOTE]
>
>A causa di limitazioni di progettazione AMP, Adobe non supporta l’uso della griglia reattiva con la versione AMP della pagina.

Per ulteriori requisiti e dettagli tecnici, vedi la [documentazione per gli sviluppatori GitHub.](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)
