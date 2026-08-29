---
title: Componente Ricerca IA contenuto
description: Il componente Ricerca IA contenuto offre ai visitatori del sito una ricerca generativa basata sull’intelligenza artificiale.
role: Developer, Admin, User
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
source-git-commit: e721e8b9469646300432b87d42bfb742aaf5f3fb
workflow-type: tm+mt
source-wordcount: 805
ht-degree: 16%

---


# Componente Ricerca IA contenuto {#content-ai-search-component}

Il componente Ricerca IA contenuto offre ai visitatori del sito una ricerca generativa basata sull’intelligenza artificiale.

{{traditional-aem}}

## Utilizzo {#usage}

Il componente Ricerca IA contenuto consente ai visitatori di eseguire ricerche in un [Source contenuto](https://experienceleague.adobe.com/it/docs/experience-manager-content-ai/using/contentsources) direttamente da una pagina e, facoltativamente, di visualizzare un riepilogo dei risultati generato dall&#39;intelligenza artificiale. Combina una casella di ricerca full-text/semantica standard con un pannello di riepilogo **Mostra riepilogo generato dall&#39;intelligenza artificiale** attivato da AEM Content AI.

La [finestra di dialogo per modifica](#edit-dialog) consente all&#39;autore di contenuto di definire l&#39;ambito del contenuto della ricerca, il comportamento di ricerca e le impostazioni generative. La finestra di dialogo per progettazione non è disponibile, poiché non sono disponibili impostazioni a livello di modello.

>[!NOTE]
>
>Per utilizzare il componente Ricerca IA contenuto, è necessario avere accesso a un Source di IA per la gestione dei contenuti e l’amministratore deve aver abilitato il componente per il progetto. Per ulteriori informazioni, vedere il documento [Configurazione del componente Ricerca IA contenuto](/help/developing/ai-search.md).

## Versione e compatibilità {#version-and-compatibility}

La versione corrente del componente Ricerca IA contenuto è la v1, introdotta con la versione 2.32.0 dei Componenti core a luglio 2026, ed è quella descritta in questo documento.

La tabella che segue descrive tutte le versioni supportate del componente, le versioni di AEM con cui le versioni del componente sono compatibili e i collegamenti alla documentazione delle versioni precedenti.

| Versione del componente | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|---|---|---|---|---|
| v1 | - | - | - | In corso |

Per ulteriori informazioni sulle versioni e sugli aggiornamenti dei Componenti core, vedi il documento [Versioni dei Componenti core.](/help/versions.md)

## Esempio di output del componente {#sample-component-output}

Per avere un&#39;idea del componente Ricerca IA contenuto e vedere esempi delle opzioni di configurazione e dell&#39;output HTML e JSON, visita la [libreria dei componenti.](https://adobe.com/go/aem_cmp_library_ai_search)

## Dettagli tecnici {#technical-details}

La documentazione tecnica più recente sul componente Ricerca IA contenuto [&#x200B; è disponibile su GitHub.](https://adobe.com/go/aem_cmp_tech_ai_search_v1_it)

Per ulteriori informazioni sullo sviluppo di Componenti core, vedi la [documentazione per gli sviluppatori di Componenti core.](/help/developing/overview.md)

## Finestra di dialogo per modifica {#edit-dialog}

La finestra di dialogo per modifica consente all’autore di contenuto di definire l’ambito del contenuto della ricerca, il comportamento di ricerca e le impostazioni generative. La finestra di dialogo per progettazione non è disponibile, poiché non sono disponibili impostazioni a livello di modello.

### Scheda Ambito contenuto {#content-scope}

![Scheda Ambito contenuto della finestra di dialogo per modifica](/help/assets/content-ai-search-edit-content-scope.png)

* **ID** - Questa opzione consente di controllare l&#39;identificatore univoco del componente in HTML e nel [Data Layer.](/help/developing/data-layer/overview.md)
  * Se non specificato, viene generato automaticamente un ID univoco reperibile sulla pagina risultante.
  * Se l’ID viene specificato, è responsabilità dell’autore accertarsi che sia univoco.
  * La modifica dell’ID può avere un impatto sul tracciamento di CSS, JS e livello dati.
* **Tipo di Source contenuto** - Questo campo definisce il tipo di origine contenuto. Se si seleziona un tipo, il menu a discesa **Source dei contenuti** viene compilato con le origini corrispondenti.
  * **ACQUISIZIONE** - Valore predefinito utilizzato per le origini pubbliche con accesso anonimo indicizzate tramite una pipeline di scansiona/acquisizione
  * **AEM_AUTHOR** - Origine lato IA contenuto il cui contenuto è stato acquisito da un&#39;istanza di authoring AEM
  * **AEM_PUBLISH**: origine lato IA contenuto il cui contenuto è stato acquisito da un&#39;istanza AEM Publish
  * **PERSONALIZZATO** - Origine registrata al di fuori delle pipeline di acquisizione di AEM
* **Origini contenuto** - Definisce il Source contenuto cercato da questo componente.
  * Le voci disponibili corrispondono alle origini di contenuto già esistenti e sono **disponibili**, nonché al tipo impostato in **Content Source Type**
  * Per informazioni dettagliate, consulta il documento [Configurare e gestire le origini di IA per la gestione dei contenuti](https://experienceleague.adobe.com/it/docs/experience-manager-content-ai/using/contentsources).

### Scheda Comportamento di ricerca {#search-behavior}

![Scheda Comportamento di ricerca della finestra di dialogo per modifica](/help/assets/content-ai-search-edit-search-behavior.png)

* **Layout risultati** - Questa opzione definisce come i risultati della ricerca vengono visualizzati al visitatore.
  * **Schede** - Questa opzione visualizza i risultati in formato griglia.
  * **Elenco** - Questa opzione visualizza i risultati in un formato elenco.
* **Dimensione risultati** - Definisce il numero di risultati recuperati per richiesta di ricerca.
  * Il valore predefinito è `12`.
  * I visitatori possono caricare più risultati quando sono disponibili corrispondenze aggiuntive.
* **Testo segnaposto**: si tratta del testo visualizzato nel campo di input della ricerca vuoto prima che il visitatore entri in una query di ricerca.

### Scheda Ricerca generativa {#generative-search}

![Scheda Ricerca generativa della finestra di dialogo per modifica](/help/assets/content-ai-search-edit-generative-search.png)

* **Mostra/nascondi riepilogo generativo/a ai visitatori** - Se questa opzione non è selezionata, i visitatori non possono modificare la visualizzazione o meno del riepilogo di IA.
  * Il valore predefinito è abilitato.
* **Mostra riepilogo generativo per impostazione predefinita** - Questa opzione controlla lo stato predefinito dell&#39;interruttore rivolto al visitatore per il riepilogo generato da IA.
  * Il valore predefinito è abilitato.
* **Errore GenSearch - Fallback** - Definisce il comportamento o l&#39;errore della ricerca.
  * **Solo risultati (nascondi errore)** - Se si verifica un errore, visualizzare solo i risultati restituiti, non l&#39;errore e il pulsante non riprova. Questo è il valore predefinito.
  * **Mostra errore con nuovo tentativo** - Se si verifica un errore, visualizzare l&#39;errore con un pulsante nuovo tentativo.
  * **Mostra solo messaggio di errore** - Se si verifica un errore, visualizza solo il messaggio di errore, nessun risultato.
