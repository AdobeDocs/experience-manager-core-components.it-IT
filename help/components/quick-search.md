---
title: Componente Ricerca rapida
description: Il componente Ricerca rapida fornisce funzionalità di ricerca in un sito web e presenta i risultati della ricerca in modo che i visitatori possano cercare nel sito e filtrare i risultati, facoltativamente utilizzando la ricerca semantica basata sull’intelligenza artificiale tramite l’interruttore Ricerca semantica.
role: Developer, Admin, User
exl-id: fc40ce1d-e69a-4a40-853e-67a37228271b
TQID: https://experienceleague.adobe.com/wU-3pacdEz9ne8b53-mKJy-XxRdyz2gu4Jvj-yFgGOw
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: e2c1b6d3-bb7e-4fe8-8c72-f7b403298e91
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
source-git-commit: f7fb04a4420a61d8a4755f2b3f09aad91b12c7eb
workflow-type: tm+mt
source-wordcount: 863
ht-degree: 46%

---


# Componente Ricerca rapida {#quick-search-component}

Il componente Ricerca rapida fornisce funzionalità di ricerca in un sito web e visualizzazione dei risultati della ricerca, in modo che i visitatori possano facilmente effettuare ricerche nel contenuto del sito e visualizzare i risultati.

{{traditional-aem}}

## Utilizzo {#usage}

Il componente Ricerca rapida offre ai visitatori del sito la possibilità di cercare contenuto, visualizzare direttamente i risultati e navigare facilmente nelle pagine trovate. I nuovi risultati vengono recuperati dinamicamente mentre l’utente scorre i risultati della ricerca.

La [finestra di dialogo per modifica](#edit-dialog) consente all&#39;autore di contenuto di definire da dove deve iniziare la ricerca nella struttura del contenuto e, facoltativamente, di nascondere l&#39;interruttore Ricerca semantica. Utilizzando la [finestra di dialogo per progettazione](#design-dialog), l&#39;autore del modello può impostare il valore predefinito per la posizione nella struttura del contenuto da cui deve iniziare la ricerca, la dimensione massima del set di risultati, la lunghezza minima del termine di ricerca e se l&#39;opzione Ricerca semantica viene visualizzata ai visitatori per impostazione predefinita.

## Versione e compatibilità {#version-and-compatibility}

La versione corrente del componente Ricerca rapida è la v3, introdotta con la [versione 2.32.0](/help/versions.md) dei Componenti core con l’aggiunta di un interruttore di ricerca semantica opzionale, ed è quella descritta in questo documento.

La tabella che segue descrive tutte le versioni supportate del componente, le versioni di AEM con cui le versioni del componente sono compatibili e i collegamenti alla documentazione delle versioni precedenti.

| Versione del componente | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |--- |---|---|
| v3 | - | Compatibile | Compatibile | Compatibile |
| [v2](/help/components/v2/quick-search.md) | - | Compatibile | Compatibile | Compatibile |
| [v1](/help/components/v1/quick-search.md) | Compatibile con la <br>[versione 2.17.4](/help/versions.md) e precedenti | Compatibile | - | Compatibile |

Per ulteriori informazioni sulle versioni e sugli aggiornamenti dei Componenti core, vedi il documento [Versioni dei Componenti core](/help/versions.md).

### Dettagli tecnici {#technical-details}

>[!NOTE]
>
>La protezione del componente Ricerca o di qualsiasi applicazione basata su AEM contro attacchi DOS deve essere implementata a un livello più alto, ad esempio utilizzando la proprietà `mod_security` su Dispatcher.

La documentazione tecnica più recente sul componente Ricerca rapida [è disponibile su GitHub](https://adobe.com/go/aem_cmp_tech_search_v2_it).

Per ulteriori informazioni sullo sviluppo di Componenti core, vedi la [documentazione per gli sviluppatori di Componenti core](/help/developing/overview.md).

## Finestra di dialogo per modifica {#edit-dialog}

La finestra di dialogo per modifica consente all’autore di contenuto di definire da dove deve iniziare la ricerca nella struttura del contenuto e di nascondere facoltativamente l’opzione Ricerca semantica.

![Finestra di dialogo per modifica del componente Ricerca rapida](/help/assets/quick-search-edit-v3.png)

**Pagina iniziale ricerca**: la pagina da cui avviare la ricerca. La pagina iniziale della ricerca può essere una pagina master blueprint, master lingua o normale.
* **ID**: questa opzione consente di controllare l’identificatore univoco del componente nel codice HTML e nel [livello dati.](/help/developing/data-layer/overview.md)
  * Se non specificato, viene generato automaticamente un ID univoco reperibile sulla pagina risultante.
  * Se l’ID viene specificato, è responsabilità dell’autore accertarsi che sia univoco.
  * La modifica dell’ID può avere un impatto sul tracciamento di CSS, JS e livello dati.
* **Nascondi/Nascondi ricerca semantica in questa istanza** - Se questa opzione è selezionata, l&#39;opzione Ricerca semantica è nascosta, indipendentemente dalla [finestra di dialogo per progettazione](#design-dialog) configurata per la visualizzazione.
  * Lascia deselezionata questa opzione per utilizzare l’impostazione predefinita del modello.
  * Questa opzione non può forzare la visualizzazione dell&#39;interruttore su un posizionamento in cui la finestra di dialogo per progettazione la nasconde.

>[!NOTE]
>
>Se la **Pagina iniziale ricerca** non è configurata o non può essere risolta, per impostazione predefinita la ricerca rapida viene eseguita sotto la pagina corrente.

>[!NOTE]
>
>L’opzione Ricerca semantica restituisce risultati basati sull’intelligenza artificiale solo quando l’ambiente è configurato con IA per la gestione dei contenuti di AEM. Negli ambienti AEM 6.5 e AEM 6.5 LTS non configurati con IA per la gestione dei contenuti, nascondi l&#39;interruttore [utilizzando la finestra di dialogo per la progettazione](#design-dialog) in modo che ai visitatori non venga offerta una modalità di ricerca non funzionante.

## Finestra di dialogo per progettazione {#design-dialog}

Utilizzando la finestra di dialogo per progettazione, l’autore del modello può impostare il valore predefinito per la posizione nella struttura del contenuto da cui deve iniziare la ricerca, nonché una dimensione massima del set di risultati, una lunghezza minima del termine di ricerca e se l’opzione Ricerca semantica è visualizzata o meno per impostazione predefinita dai visitatori.

### Scheda Proprietà {#properties-tab}

![Finestra di dialogo per progettazione del componente Ricerca rapida](/help/assets/quick-search-design-v3.png)

* **Pagina iniziale ricerca** - Valore predefinito per la pagina iniziale della ricerca quando un autore di contenuti inserisce il componente Ricerca rapida in una pagina
* **Dimensione risultati** - Numero massimo di risultati recuperati da una richiesta di ricerca
* **Lunghezza minima termine di ricerca** - Lunghezza minima del termine di ricerca per avviare la ricerca
* **Nascondi attivazione/disattivazione ricerca semantica** - Se questa opzione è selezionata, l&#39;opzione **Ricerca semantica** descritta in [Utilizzo](#usage) non viene visualizzata ai visitatori del sito per impostazione predefinita e il componente si comporta come [il componente v2 (solo ricerca full-text).](/help/components/v2/quick-search.md)
  * Deselezionato per impostazione predefinita.
  * Gli autori dei contenuti possono inoltre ignorare questa impostazione per un singolo componente Ricerca rapida nella [finestra di dialogo per modifica.](#edit-dialog)

>[!NOTE]
>
>L’opzione Ricerca semantica restituisce risultati basati sull’intelligenza artificiale solo quando l’ambiente è configurato con IA per la gestione dei contenuti di AEM. In ambienti AEM 6.5 e AEM 6.5 LTS non configurati con IA per la gestione dei contenuti, nascondi l’interruttore utilizzando la finestra di dialogo per la progettazione in modo che ai visitatori non venga offerta una modalità di ricerca non funzionante.

>[!NOTE]
>
>Le opzioni **Dimensione risultati** e **Lunghezza minima termine di ricerca** possono essere impostate solo in modalità di progettazione e quindi solo a livello di modello, il che significa che gli autori di contenuto non possono modificare questi valori.

>[!CAUTION]
>
>Le opzioni **Dimensione risultati** e **Lunghezza minima termine di ricerca** possono avere un impatto sulle prestazioni, se impostate rispettivamente su un valore troppo alto o troppo basso.

### Scheda Stili {#styles-tab}

Il componente Ricerca rapida supporta il [sistema di stili](/help/get-started/authoring.md#component-styling) di AEM.
