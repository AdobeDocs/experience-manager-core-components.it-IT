---
title: Componente Ricerca rapida (v1)
description: Il componente Ricerca rapida fornisce funzionalità di ricerca in un sito web e visualizzazione dei risultati della ricerca, in modo che i visitatori possano effettuare ricerche nel sito e filtrare i risultati.
role: Developer, Admin, User
exl-id: 60a043b7-d82c-4bc1-b91a-b77f748f7bc2
index: false
TQID: https://experienceleague.adobe.com/r1iL5fuJASw8hapiIFdvwNmGTKBcQnvF55H4S26iwxA
product_v2: id: c45915cf-e157-4af7-a80d-97b905bcb3a5id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: e2c1b6d3-bb7e-4fe8-8c72-f7b403298e91
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080b
source-git-commit: 73aa5234ac63fa3be99feebce448bb6722513838
workflow-type: tm+mt
source-wordcount: 648
ht-degree: 100%

---

# Componente Ricerca rapida (v1) {#quick-search-component}

Il componente Ricerca rapida fornisce funzionalità di ricerca in un sito web e visualizzazione dei risultati della ricerca, in modo che i visitatori possano facilmente effettuare ricerche nel contenuto del sito e visualizzare i risultati.

## Utilizzo {#usage}

Il componente Ricerca rapida offre ai visitatori del sito la possibilità di cercare contenuto, visualizzare direttamente i risultati e navigare facilmente nelle pagine trovate. I nuovi risultati vengono recuperati dinamicamente mentre l’utente scorre i risultati della ricerca.

La [finestra di dialogo per modifica](#edit-dialog) consente all’autore di contenuto di definire da dove deve iniziare la ricerca nella struttura del contenuto. La [finestra di dialogo per progettazione](#design-dialog) consente all’autore del modello di impostare il valore predefinito per la posizione nella struttura del contenuto dalla quale deve iniziare la ricerca, nonché una dimensione massima del set di risultati e una lunghezza minima del termine di ricerca.

## Versione e compatibilità {#version-and-compatibility}

La versione corrente del componente Ricerca rapida e la v1, introdotta con la versione 2.0.0 dei Componenti core a gennaio 2018, ed è quella descritta in questo documento.

La tabella che segue descrive tutte le versioni supportate del componente, le versioni di AEM con cui le versioni del componente sono compatibili e i collegamenti alla documentazione delle versioni precedenti.

| Versione del componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v1 | Compatibile con la <br>[versione 2.17.4](/help/versions.md) e precedenti | Compatibile | Compatibile |

>[!CAUTION]
>
>Questo documento descrive la versione 1 del componente Ricerca rapida.
>Per informazioni dettagliate sulla versione corrente del componente Ricerca rapida, consulta il documento [Componente Ricerca rapida](/help/components/quick-search.md).

Per ulteriori informazioni sulle versioni e sugli aggiornamenti dei Componenti core, vedi il documento [Versioni dei Componenti core](/help/versions.md).

### Dettagli tecnici {#technical-details}

>[!NOTE]
>
>La protezione del componente Ricerca o di qualsiasi applicazione basata su AEM contro attacchi DOS deve essere implementata a un livello più alto, ad esempio utilizzando la proprietà `mod_security` su Dispatcher.

La documentazione tecnica più recente sul componente Ricerca rapida [è disponibile su GitHub](https://adobe.com/go/aem_cmp_tech_search_v1_it).

Per ulteriori informazioni sullo sviluppo di Componenti core, vedi la [documentazione per gli sviluppatori di Componenti core](/help/developing/overview.md).

## Finestra di dialogo per modifica {#edit-dialog}

La finestra di dialogo per modifica consente all’autore di contenuto di definire da dove deve iniziare la ricerca nella struttura del contenuto.

![Finestra di dialogo per modifica del componente Ricerca rapida](/help/assets/quick-search-edit.png)

**Pagina iniziale ricerca**: la pagina da cui avviare la ricerca. La pagina iniziale della ricerca può essere una pagina master blueprint, master lingua o normale.
* **ID**: questa opzione consente di controllare l’identificatore univoco del componente nel codice HTML e nel [livello dati.](/help/developing/data-layer/overview.md)
   * Se non specificato, viene generato automaticamente un ID univoco reperibile sulla pagina risultante.
   * Se l’ID viene specificato, è responsabilità dell’autore accertarsi che sia univoco.
   * La modifica dell’ID può avere un impatto sul tracciamento di CSS, JS e livello dati.

>[!NOTE]
>
>Se la **Pagina iniziale ricerca** non è configurata o non può essere risolta, per impostazione predefinita la ricerca rapida viene eseguita sotto la pagina corrente.

## Finestra di dialogo per progettazione {#design-dialog}

La finestra di dialogo Progettazione consente all’autore del modello di impostare il valore predefinito per la posizione nella struttura del contenuto da cui deve iniziare la ricerca, nonché la dimensione massima del set di risultati e la lunghezza minima del termine di ricerca.La finestra di dialogo per progettazione consente all’autore del modello di definire le opzioni di formattazione del testo disponibili per gli autori di contenuti.

### Scheda Proprietà {#properties-tab}

![Finestra di dialogo per progettazione del componente Ricerca rapida](/help/assets/quick-search-design.png)

* **Pagina iniziale della ricerca**
Il valore predefinito della ricerca principale quando un autore di contenuti inserisce il componente Ricerca rapida su una pagina di contenuto
* **Dimensione risultati**
Il numero massimo di risultati recuperati da una richiesta di ricerca
* **Lunghezza minima del termine di ricerca**
Lunghezza minima del termine di ricerca per iniziare la ricerca

>[!NOTE]
>
>Le opzioni **Dimensione risultati** e **Lunghezza minima termine di ricerca** possono essere impostate solo in modalità di progettazione e quindi solo a livello di modello; ciò significa che gli autori dei contenuti non possono modificare questi valori.

>[!CAUTION]
>
>Le opzioni **Dimensione risultati** e **Lunghezza minima termine di ricerca** possono avere un impatto sulle prestazioni, se impostate rispettivamente su un valore troppo alto o troppo basso.

### Scheda Stili {#styles-tab}

Il componente Ricerca rapida supporta il [sistema di stili](/help/get-started/authoring.md#component-styling) di AEM.
