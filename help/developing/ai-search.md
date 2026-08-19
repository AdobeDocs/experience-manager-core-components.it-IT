---
title: Configurazione del componente Ricerca IA contenuto
description: Il componente Ricerca IA contenuto offre ai visitatori del sito una ricerca generativa basata sull’intelligenza artificiale. Scopri come abilitare questo componente per gli autori di contenuti.
role: Developer, Admin
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
source-git-commit: 865622469555a773138d3ff1b54138f2b76994b0
workflow-type: tm+mt
source-wordcount: 485
ht-degree: 2%

---


# Configurazione del componente Ricerca IA contenuto {#configure-content-ai-search-component}

Il componente Ricerca IA contenuto offre ai visitatori del sito una ricerca generativa basata sull’intelligenza artificiale. Scopri come abilitare questo componente per gli autori di contenuti.

## Prerequisiti {#prerequisites}

* Almeno un [Source dei contenuti](https://experienceleague.adobe.com/it/docs/experience-manager-content-ai/using/contentsources) è già stato creato e con lo stato **Disponibile**.
* Configurazione OSGi del client **AEM Content AI** (`ContentAIClientImpl`) impostata sia per l&#39;authoring che per la pubblicazione, con credenziali API valide e un valore **Default Content Source**. Per informazioni su come ottenere le credenziali, vedere il documento [Configurazione di un progetto Adobe Developer Console](https://experienceleague.adobe.com/it/docs/experience-manager-content-ai/using/setup-adc-project).

## Creazione di un componente proxy {#proxy-component}

Come tutti i Componenti core, si consiglia di creare un componente proxy per il componente Ricerca IA contenuto predefinito che viene fornito con AEM. Mantenendo le modifiche specifiche del progetto nel componente proxy in `/apps`, i componenti base in `/libs` vengono aggiornati automaticamente da Adobe e il componente del progetto eredita automaticamente questi aggiornamenti. Per ulteriori informazioni, consulta i documenti [Utilizzo dei componenti core](/help/get-started/using.md#aemaacs) e [Linee guida per i componenti](/help/developing/guidelines.md).

## Configurare le librerie client {#clientlib}

Il componente Ricerca IA contenuto non segue [il modello standard per l&#39;inclusione delle librerie client nei componenti core.](/help/developing/including-clientlibs.md) Al suo posto, segui la procedura riportata di seguito.

Aggiungi quanto segue al componente pagina del progetto `customheaderlibs.html` (per CSS) e `customfooterlibs.html` (per JS):

```html
<sly data-sly-use.clientLib="/libs/granite/sightly/templates/clientlib.html"
     data-sly-call="${clientLib.css @ categories='core.wcm.components.contentaisearch.v1'}"></sly>
```

Se nel progetto è presente uno stile di marchio personalizzato, aggiungi una seconda categoria per la libreria client del progetto dopo questa.

## Utilizzo del componente Ricerca IA contenuto {#using}

Gli autori dei contenuti possono ora inserire il componente Ricerca IA contenuto nelle proprie pagine. Per ulteriori informazioni, vedere il documento [Componente Ricerca IA contenuto](/help/components/ai-search.md).

## Utilizzo di IA per la gestione dei contenuti da parte del componente {#how-it-works}

* Le query di ricerca standard sono gestite dallo stesso livello di recupero dell’indice di Content Source, che restituisce dall’origine configurata pagine, frammenti o risorse corrispondenti.
* Quando il riepilogo generato dall’intelligenza artificiale è abilitato, il componente chiama anche l’endpoint generativo di IA per l’analisi dei contenuti di AEM, basa la risposta nello stesso contenuto indicizzato e visualizza le origini insieme al riepilogo in modo che i visitatori possano verificarlo.
* Poiché entrambe le funzioni vengono lette dallo stesso Content Source gestito, i risultati e i riepiloghi rimangono coerenti con qualsiasi contenuto attualmente indicizzato. La riesecuzione dell&#39;acquisizione (vedi [Controlla le origini di contenuto](https://experienceleague.adobe.com/it/docs/experience-manager-content-ai/using/contentsources)) aggiorna entrambi.

## Passaggi successivi {#next-steps}

* [Controlla le origini di contenuto](https://experienceleague.adobe.com/it/docs/experience-manager-content-ai/using/contentsources) — crea e gestisci il Source di contenuto cercato da questo componente.
* [Configura un progetto Adobe Developer Console](https://experienceleague.adobe.com/it/docs/experience-manager-content-ai/using/setup-adc-project) - Ottieni le credenziali utilizzate dalla configurazione del client di IA per la gestione dei contenuti OSGi.
* [Riferimento API di IA per la gestione dei contenuti](https://developer.adobe.com/experience-cloud/experience-manager-apis/api/experimental/contentai/): comprendere la ricerca sottostante e gli endpoint di riepilogo generativo chiamati da questo componente.
