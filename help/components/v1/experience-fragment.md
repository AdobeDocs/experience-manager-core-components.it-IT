---
title: Componente Frammento esperienza (v1)
description: Il componente Frammento esperienza consente all’autore del contenuto di aggiungere a una pagina una variante del Frammento esperienza.
role: Architect, Developer, Admin, User
exl-id: 42230a7b-6feb-4535-baf9-b8fc06978d98
index: n
source-git-commit: 92a3ec273a5be6751c1503835b9c2e5cbd61bb9e
workflow-type: ht
source-wordcount: '770'
ht-degree: 100%

---


# Componente Frammento esperienza (v1) {#experience-fragment-component}

Il componente Frammento esperienza consente all’autore di contenuto di inserire una variante del Frammento esperienza in una pagina e al contempo di supportare una struttura localizzata del sito.

## Utilizzo {#usage}

Il componente Frammento esperienza consente all’autore di contenuto di selezionare tra le varianti di Frammento esperienza esistenti e inserirne una nella pagina di contenuto. Il componente Frammento esperienza supporta anche una struttura localizzata del sito.

* Le proprietà del componente possono essere definite nella [finestra di dialogo per configurazione](#configure-dialog).
* Le impostazioni predefinite del componente, quando lo si aggiunge a una pagina, possono essere definite nella [finestra di dialogo per progettazione](#design-dialog).

## Versione e compatibilità {#version-and-compatibility}

Questo documento descrive la versione 1 del componente Frammento esperienza, introdotto con la versione 2.6.0 dei componenti core a settembre 2019.

>[!CAUTION]
>
>Questo documento descrive la versione 1 del componente Frammento di esperienza.
>
>Per informazioni dettagliate sulla versione corrente del componente Frammento di esperienza, consulta il documento [Componente Frammento di esperienza](/help/components/experience-fragment.md).

## Supporto della struttura localizzata del sito {#localized-site-structure}

Il componente Frammento esperienza si adatta alle strutture localizzate dei siti ed esegue il rendering del Frammento esperienza appropriato in base alla localizzazione della pagina. A questo scopo, il Frammento esperienza deve soddisfare le seguenti condizioni.

* Il componente Frammento esperienza viene aggiunto a un modello.
* Il modello viene utilizzato per creare una nuova pagina di contenuto che fa parte di una struttura localizzata sotto `/content/<site>`.
* Il Frammento esperienza a cui si fa riferimento in una pagina di contenuto fa parte di una struttura di Frammenti esperienza localizzati sotto `/content/experience-fragments` che segue gli stessi modelli del sito sotto `/content/<site>`, incluso l’utilizzo degli stessi nomi di componenti.

In questo caso, come parte del modello, verrà eseguito il rendering del frammento con la stessa localizzazione (lingua, blueprint o Live Copy) della pagina corrente.

Questo comportamento è limitato ai componenti Frammento esperienza aggiunti ai modelli. I componenti Frammento esperienza aggiunti alle singole pagine di contenuto restituiranno esattamente le rappresentazioni dei Frammenti esperienza configurate all’interno del componente.

* Per un esempio delle funzioni di localizzazione del componente Frammento esperienza, vedi [la sezione che segue](#example).
* Per un esempio dell’interazione delle funzioni di localizzazione dei Componenti core, visita la pagina [Funzioni di localizzazione dei Componenti core](/help/get-started/localization.md).

### Esempio {#example}

Supponiamo che il contenuto sia simile al seguente:

```
/content
+-- experience-fragments
   \-- wknd
      +-- language-masters
      +-- us
         +-- en
            +-- footerTextXf
            \-- headerTextXf
         \-- es
            +-- footerTextXf
            \-- headerTextXf
      \-- ch
         +-- de
            +-- footerTextXf
            \-- headerTextXf
         +-- fr
            +-- footerTextXf
            \-- headerTextXf
         \-- it
            +-- footerTextXf
            \-- headerTextXf
+-- wknd
   +-- language-masters
   +-- us
      +-- en
      \-- es
   +-- ch
      +-- de
      +-- fr
      \-- it
+-- wknd-events
\-- wknd-shop
```

Nota come la struttura sotto `/content/experience-fragments/wknd` rispecchi la struttura di `/content/wknd`.

In questo caso, se il componente Frammento esperienza `/content/experience-fragments/wknd/us/en/footerTextXf` è inserito in un modello, per le pagine localizzate create in base a quel modello verrà automaticamente eseguito il rendering del Frammento esperienza localizzato corrispondente alla pagina localizzata.

Pertanto, se vai a una pagina di contenuto sotto `/content/wknd/ch/de` che utilizza lo stesso modello, viene eseguito il rendering di `/content/experience-fragments/wknd/ch/de/footerTextXf` invece di `/content/experience-fragments/wknd/us/en/footerTextXf`.

### Regresso {#fallback}

Il componente Frammento esperienza tenta di trovare un componente localizzato corrispondente nell’ordine seguente.

1. Prima tenta di trovare una directory principale della lingua.
1. Se non la trova, tenta di trovare un modello.
1. Se non lo trova, tenta di trovare una Live Copy.
1. Se non la trova, per impostazione predefinita viene visualizzato il Frammento esperienza configurato nel componente.

## Esempio di output del componente {#sample-component-output}

Per avere un’idea del componente Frammento esperienza e vedere esempi delle opzioni di configurazione e dell’output HTML e JSON, visita la [libreria dei componenti](https://adobe.com/go/aem_cmp_library_xf).

## Dettagli tecnici {#technical-details}

La documentazione tecnica più recente sul componente Frammento esperienza [è disponibile su GitHub](https://adobe.com/go/aem_cmp_tech_xf_v1_it).

Per ulteriori informazioni sullo sviluppo di Componenti core, vedi la [documentazione per gli sviluppatori di Componenti core](/help/developing/overview.md).

## Finestra di dialogo per configurazione {#configure-dialog}

La finestra di dialogo per configurazione consente all’autore di contenuto di selezionare la variante del Frammento di esperienza di cui eseguire il rendering sulla pagina.

![Finestra di dialogo per modifica del componente Frammento esperienza](/help/assets/experience-fragment-edit.png)

Utilizza il pulsante **Apri finestra di dialogo per selezione** per aprire il selettore di componenti e scegliere la variante del componente Frammento esperienza da aggiungere alla pagina di contenuto.

Se aggiungi il componente Frammento esperienza a un modello, noterai che verrà automaticamente localizzato, a condizione che i Frammenti esperienza siano localizzati, pertanto ciò che viene rappresentato sulla pagina può variare in base al componente esplicitamente selezionato. Per ulteriori informazioni, [vedi l’esempio precedente](#example).

Puoi anche definire un **ID**. Questa opzione consente di controllare l’identificatore univoco del componente nel codice HTML e nel [livello dati](/help/developing/data-layer/overview.md).

* Se non specificato, viene generato automaticamente un ID univoco reperibile sulla pagina risultante.
* Se l’ID viene specificato, è responsabilità dell’autore accertarsi che sia univoco.
* La modifica dell’ID può avere un impatto sul tracciamento di CSS, JS e livello dati.

## Finestra di dialogo per progettazione {#design-dialog}

La finestra di dialogo per progettazione consente all’autore del modello di definire le opzioni disponibili per l’autore di contenuto che utilizza il componente Frammento esperienza e le impostazioni predefinite scelte al momento del posizionamento del Frammento esperienza.

### Scheda Stili {#styles-tab}

Il componente Frammento esperienza supporta il [sistema di stili](/help/get-started/authoring.md#component-styling) di AEM.
