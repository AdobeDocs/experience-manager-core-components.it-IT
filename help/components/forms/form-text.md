---
title: Componente Testo Modulo
description: Il componente core Testo modulo consente l’inserimento di testo del modulo per l’invio.
role: Developer, Admin, User
exl-id: e8fa3881-51fb-4726-9654-8f93acfb7464
TQID: https://experienceleague.adobe.com/9js-R-LzxStEKmgs59UvZBz-htCWyIx-PQIjpIKJAqc
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
  - id: cc72dcf1-72e1-48cc-b434-e7c27d62d67c
source-git-commit: 73aa5234ac63fa3be99feebce448bb6722513838
workflow-type: tm+mt
source-wordcount: 581
ht-degree: 100%

---

# Componente Testo Modulo{#form-text-component}

Il componente core Testo modulo consente l’inserimento di testo del modulo per l’invio.

## Utilizzo {#usage}

Il componente Testo modulo consente l’invio di diversi tipi di testo e deve essere utilizzato insieme al componente [Contenitore modulo](form-container.md). Il tipo di convalida del testo, le etichette e i messaggi di aiuto possono essere definiti dall’editor di contenuto nella [finestra di dialogo per configurazione](#configure-dialog).

## Versione e compatibilità {#version-and-compatibility}

La versione corrente del componente Testo modulo è la v2, introdotta con la versione 2.0.0 dei Componenti core a gennaio 2018, ed è quella descritta in questo documento.

La tabella che segue descrive tutte le versioni supportate del componente, le versioni di AEM con cui le versioni del componente sono compatibili e i collegamenti alla documentazione delle versioni precedenti.

| Versione del componente | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |--- |---|---|
| v2 | Compatibile con la <br>[versione 2.17.4](/help/versions.md) e precedenti | Compatibile | Compatibile | Compatibile |
| [v1](/help/components/v1/form-text-v1.md) | Compatibile | Compatibile | - | Compatibile |

Per ulteriori informazioni sulle versioni e sugli aggiornamenti dei Componenti core, vedi il documento [Versioni dei Componenti core](/help/versions.md).

## Esempio di output del componente {#sample-component-output}

Per avere un’idea del componente Testo modulo e vedere esempi delle opzioni di configurazione e dell’output HTML e JSON, visita la [libreria dei componenti](https://adobe.com/go/aem_cmp_library_form_text_it).

### Dettagli tecnici {#technical-details}

La documentazione tecnica più recente sul componente Testo modulo [è disponibile su GitHub](https://adobe.com/go/aem_cmp_tech_form_text_v2_it).

Per ulteriori informazioni sullo sviluppo di Componenti core, vedi la [documentazione per gli sviluppatori di Componenti core](/help/developing/overview.md).

## Finestra di dialogo per configurazione {#configure-dialog}

La finestra di dialogo per configurazione consente all’autore di contenuto di definire il tipo di testo da inserire, nonché i valori e le etichette predefiniti.

### Scheda Proprietà {#properties-tab}

![Scheda Proprietà](/help/assets/form-text-edit-properties.png)

* **Vincolo**: il tipo di testo da inserire e su cui verrà effettuata la convalida
   * **Testo**
   * **Area testo**
   * **E-mail**
   * **Tel**
   * **Data**
   * **Numero**
   * **Password**
* **Righe di testo**: numero di righe da visualizzare nell’area di testo (solo se l’opzione **Vincolo** Limite è impostata su **Area testo**)
* **Etichetta**: l’etichetta che verrà visualizzata per il campo
* **Nascondi l’etichetta**: opzione necessaria se l’etichetta serve solo per scopi di accessibilità e non fornisce alcuna informazione visiva aggiuntiva relativa al campo
* **Nome elemento**: il nome del campo che viene inviato con i dati del modulo
* **Valore**: il valore predefinito inserito automaticamente nel campo
* **ID**: questa opzione consente di controllare l’identificatore univoco del componente nel codice HTML e nel [livello dati](/help/developing/data-layer/overview.md).
   * Se non specificato, viene generato automaticamente un ID univoco reperibile sulla pagina risultante.
   * Se l’ID viene specificato, è responsabilità dell’autore accertarsi che sia univoco.
   * La modifica dell’ID può avere un impatto sul tracciamento di CSS, JS e livello dati.

### Scheda Informazioni su {#about-tab}

![Scheda Informazioni su](/help/assets/form-text-edit-about.png)

* **Messaggio di aiuto**: suggerimento per l’utente per la compilazione del campo
* **Visualizza messaggio di aiuto come segnaposto**: indica se deve essere visualizzato il messaggio di aiuto nel modulo, quando il modulo è vuoto e non attivo

### Scheda Vincoli {#constraints-tab}

![Scheda Vincoli](/help/assets/form-text-edit-constraints.png)

* **Messaggio vincolo**
   * Messaggio visualizzato come descrizione comando quando si invia il modulo, se il valore non convalida il tipo scelto
   * Non visualizzato per i tipi di vincolo **Testo** e **Area testo**
* **Richiesto**: se selezionata, l’utente deve necessariamente inserire un valore prima di inviare il modulo
   * **Messaggio richiesto**: messaggio visualizzato come descrizione comando se il campo viene lasciato vuoto
* **Imposta per sola lettura**: se selezionata, l’utente non può modificare il valore del campo

## Finestra di dialogo per progettazione {#design-dialog}

### Scheda Stili {#styles-tab}

Il componente Testo modulo supporta il [sistema di stili](/help/get-started/authoring.md#component-styling) di AEM.
