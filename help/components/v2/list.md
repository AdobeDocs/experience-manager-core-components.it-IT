---
title: Componente Elenco (v2)
description: Il componente core Elenco consente di creare facilmente elenchi dinamici e statici.
role: Architect, Developer, Admin, User
exl-id: fa34be64-b345-45cd-baf3-571973414852
index: n
source-git-commit: 92a3ec273a5be6751c1503835b9c2e5cbd61bb9e
workflow-type: tm+mt
source-wordcount: '1012'
ht-degree: 99%

---


# Componente Elenco (v2) {#list-component}

Il componente core Elenco consente di creare facilmente elenchi dinamici e statici.

## Utilizzo {#usage}

Il componente Elenco può essere utilizzato per creare, ad esempio, un elenco dinamico di pagine secondarie o un elenco statico di elementi definiti arbitrariamente. Il tipo di elenchi disponibili e le opzioni di formattazione possono essere definiti dall’autore del modello nella [finestra di dialogo per progettazione](#design-dialog). L’editor di contenuto può scegliere tra i tipi di elenchi disponibili e come formattare gli elementi dell’elenco nella [finestra di dialogo per modifica](#edit-dialog).

## Versione e compatibilità {#version-and-compatibility}

Questo documento descrive la versione 1 del componente Elenco, originariamente introdotto con la versione 2.0.0 dei Componenti core a gennaio 2018.

>[!CAUTION]
>
>Questo documento descrive la versione 2 del componente Elenco.
>
>Per informazioni dettagliate sulla versione corrente del componente Elenco, vedi il documento [Componente Elenco](/help/components/list.md).

## Reindirizzamenti nei componenti Elenco {#redirects}

Quando una pagina presenta una destinazione di reindirizzamento (che sia verso un URL esterno o un’altra pagina AEM), un elenco che contiene i relativi link punta direttamente all’URL della destinazione di reindirizzamento.

### Esempio {#redirect-example}

* Crea una pagina A che reindirizza alla pagina B.
* Crea una pagina C che reindirizza a `https://aemcomponents.dev`
* In una pagina D, inserisci un componente elenco contenente le pagine A e C
* I rispettivi link generati puntano direttamente alle pagine B e `https://aemcomponents.dev`

## Esempio di output del componente {#sample-component-output}

Per avere un’idea del componente Elenco e vedere esempi delle opzioni di configurazione e dell’output HTML e JSON, visita la [libreria dei componenti](https://adobe.com/go/aem_cmp_library_list_it).

### Dettagli tecnici {#technical-details}

La documentazione tecnica più recente sul componente Elenco [è disponibile su GitHub](https://adobe.com/go/aem_cmp_tech_list_v2_it).

Per ulteriori informazioni sullo sviluppo di Componenti core, vedi la [documentazione per gli sviluppatori di Componenti core](/help/developing/overview.md).

## Finestra di dialogo per modifica {#edit-dialog}

La finestra di dialogo per modifica consente all’autore di contenuto di configurare l’elenco e i relativi elementi.

### Scheda Impostazioni elenco {#list-settings-tab}

L’elenco può essere creato in diversi modi.

* [Pagine secondarie](#child-pages)
* [Elenco fisso](#fixed-list)
* [Ricerca](#search-options)
* [Tag](#tags)

Indipendentemente dalla modalità di creazione dell’elenco, è sempre possibile configurare le [opzioni Ordinamento e ID](#sort-options).

![Finestra di dialogo per modifica del componente Elenco](/help/assets/v2/list-edit.png)

A seconda di come l’autore del contenuto sceglie di creare l’elenco, le opzioni di configurazione aggiuntive cambiano.

#### Pagine secondarie {#child-pages}

L’elenco può essere costituito dalle pagine secondarie della pagina corrente o di un’altra pagina.

![Opzioni per le pagine secondarie](/help/assets/v2/list-edit-child-pages.png)

* **Pagina padre**
   * Pagina da cui creare l’elenco di pagine secondarie
   * Lascia il campo vuoto per usare la pagina corrente

* **Profondità elementi secondari**
Quanti livelli della gerarchia devono essere utilizzati

#### Elenco fisso {#fixed-list}

L’elenco può essere creato utilizzando elementi fissi.

![Opzioni per elenco fisso](/help/assets/v2/list-edit-fixed-list.png)

Tocca il o fai clic sul pulsante **Aggiungi** per inserire un nuovo elemento nell’elenco.

* Inserisci il testo per l’elemento inserito nell’elenco oppure utilizza la **finestra di dialogo per selezione** per scegliere un elemento da AEM.
* Utilizza la maniglia di trascinamento per modificare la disposizione degli elementi nell’elenco.
* Utilizza l’icona cestino per eliminare elementi dall’elenco.

#### Ricerca {#search-options}

L’elenco può essere creato utilizzando i risultati di una ricerca di contenuto AEM.

![Opzioni per la ricerca](/help/assets/v2/list-edit-search.png)

* **Query di ricerca**
Stringa per la quale verrà eseguita una ricerca di testo completa per generare gli elementi dell’elenco
* **Cerca in**
Dove eseguire la ricerca
   * Utilizza la **finestra di dialogo per selezione** per scegliere la posizione in AEM
   * Se non specificata, viene utilizzata la pagina corrente

#### Tag {#tags}

L’elenco può essere creato utilizzando pagine che corrispondono a determinati tag presenti in una posizione specifica.

![Opzioni per i tag](/help/assets/v2/list-edit-tags.png)

* **Pagina padre**
La pagina da cui inizia la ricerca delle corrispondenze con i tag
   * Utilizza la **finestra di dialogo per selezione** per scegliere la posizione in AEM
   * Se non specificata, viene utilizzata la pagina corrente
* **Tag**
I tag per i quali deve esistere una corrispondenza
   * Utilizza la finestra di dialogo **Sfoglia** per selezionare i tag
* **Corrispondenza**
Consente di definire il tipo di corrispondenza da applicare a una pagina da includere nell’elenco
   * **qualsiasi tag**
   * **tutti i tag**

#### Opzioni di ordinamento {#sort-options}

Indipendentemente dalla modalità di creazione dell’elenco, è sempre possibile definire alcune opzioni di ordinamento.

![Opzioni di ordinamento](/help/assets/v2/list-edit-sort-options.png)

* **Ordina per**
Come ordinare gli elementi
   * **Titolo**
   * **Data ultima modifica**
* **Ordinamento**
L’ordine in cui devono essere disposti gli elementi
   * **crescente**
   * **decrescente**
* **Max. elementi**
Il numero massimo di elementi da visualizzare nell’elenco.
   * Lascia vuoto il campo per restituire tutti gli elementi.
* **ID**: questa opzione consente di controllare l’identificatore univoco del componente nel codice HTML e nel [livello dati](/help/developing/data-layer/overview.md).
   * Se non specificato, viene generato automaticamente un ID univoco reperibile sulla pagina risultante.
   * Se l’ID viene specificato, è responsabilità dell’autore accertarsi che sia univoco.
   * La modifica dell’ID può avere un impatto sul tracciamento di CSS, JS e livello dati.

### Scheda Impostazioni elemento {#item-settings-tab}

Utilizzando la scheda Impostazioni elemento, è possibile configurare la formattazione degli elementi dell’elenco.

![Impostazioni elemento](/help/assets/v2/list-edit-item-settings.png)

* **Collega elementi**
Collega gli elementi alla pagina corrispondente
* **Mostra descrizione**
Mostra la descrizione dell’elemento da collegare
* **Mostra data**
Mostra la data di modifica dell’elemento da collegare

## Finestra di dialogo per progettazione {#design-dialog}

La finestra di dialogo per progettazione consente all’autore del modello di definire i tipi di elenchi da consentire agli autori di contenuto e le impostazioni disponibili per gli elementi.

### Impostazioni elenco {#list-settings}

Nella scheda **Impostazioni elenco**, è possibile definire il formato della data e i tipi di elenchi da rendere disponibili nel componente per gli autori di contenuto.

![Impostazione dell’elenco nella finestra di dialogo per progettazione del componente Elenco](/help/assets/v2/list-design-list-settings.png)

* **Formato data**
Il formato da utilizzare per visualizzare la data dell’ultima modifica
* **Disabilita elementi secondari**
Disabilita il tipo di elenco secondario nel componente
* **Disabilita statico**
Disabilita il tipo di elenco statico nel componente
* **Disabilita ricerca**
Disabilita il tipo di elenco ricerca nel componente
* **Disabilita tag**
Disabilita il tipo di elenco tag nel componente

### Impostazioni elemento {#item-settings}

Nella scheda **Impostazioni elemento**, è possibile definire le opzioni di formattazione per i singoli elementi dell’elenco che devono essere disponibili nel componente per gli autori di contenuto.

![Impostazioni degli elementi nella finestra di dialogo per progettazione del componente Elenco](/help/assets/v2/list-design-item-settings.png)

* **Collega elementi**
Abilita l’opzione Collega elementi nella [finestra di dialogo per modifica](#edit-dialog)
* **Mostra descrizione**
Abilita l’opzione Mostra descrizione nella [finestra di dialogo per modifica](#edit-dialog)
* **Mostra data**
Abilita l’opzione Mostra data nella [finestra di dialogo per modifica](#edit-dialog)

### Scheda Stili {#styles-tab}

Il componente Immagine supporta il [sistema di stili](/help/get-started/authoring.md#component-styling) di AEM.

## Adobe Client Data Layer {#data-layer}

Il componente Elenco supporta [Adobe Client Data Layer.](/help/developing/data-layer/overview.md)
