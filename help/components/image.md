---
title: Componente Immagine
description: Il componente core Immagine è un componente immagine adattivo.
role: Architect, Developer, Admin, User
exl-id: c5e57f4b-139f-40e7-8d79-be9a74360b63
source-git-commit: 5d2d79c96dc934efd7cccefb1a6a343813376483
workflow-type: tm+mt
source-wordcount: '1957'
ht-degree: 100%

---


# Componente Immagine {#image-component}

Il componente core Immagine è un componente immagine adattivo.

## Utilizzo {#usage}

Il componente Immagine offre all’autore del contenuto una selezione adattiva delle immagini e un comportamento reattivo con caricamento lento per il visitatore della pagina, nonché una facilità di posizionamento delle immagini.

Chi crea contenuti può utilizzare la [finestra di dialogo per la modifica](#edit-dialog) per modificare la risorsa immagine, ad esempio applicando un ritaglio o ruotando l’immagine.

Le larghezze delle immagini e le altre impostazioni possono essere definiti dall’autore del modello nella [finestra di dialogo per progettazione](#design-dialog). L’editor dei contenuti può caricare o selezionare le risorse nella [finestra di dialogo di configurazione.](#configure-dialog)

## Versione e compatibilità {#version-and-compatibility}

La versione corrente del componente Immagine è la v3, introdotta con la versione 2.18.0 dei Componenti core a febbraio 2022, ed è quella descritta in questo documento.

La tabella che segue descrive tutte le versioni supportate del componente, le versioni di AEM con cui le versioni del componente sono compatibili e i collegamenti alla documentazione delle versioni precedenti.

| Versione del componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v3 | - | Compatibile | Compatibile |
| [v2](v2/image.md) | Compatibile | Compatibile | Compatibile |
| [v1](v1/image-v1.md) | Compatibile | Compatibile | Compatibile |

Per ulteriori informazioni sulle versioni e sugli aggiornamenti dei Componenti core, vedi il documento [Versioni dei Componenti core](/help/versions.md).

## Funzioni reattive {#responsive-features}

Il componente Immagine è dotato di solide funzioni reattive pronte per l’uso. A livello di modello della pagina, si può utilizzare la [finestra di dialogo per Progettazione](#design-dialog) per definire le larghezze predefinite della risorsa immagine. Il componente Immagine carica automaticamente la larghezza corretta da visualizzare, in base alle dimensioni della finestra del browser. Quando la finestra viene ridimensionata, il componente Immagine carica dinamicamente la dimensione corretta dell’immagine. Gli sviluppatori di componenti non devono preoccuparsi di definire query multimediali personalizzate, in quanto il componente Immagine è già ottimizzato per caricare il contenuto.

Inoltre, il componente Immagine supporta il caricamento lento per posticipare il caricamento della risorsa immagine effettiva fino a quando non sarà visibile nel browser, aumentando la reattività delle pagine.

>[!TIP]
>
>Per impostazione predefinita, il componente immagine è alimentato da Adaptive Image Servlet. Per informazioni dettagliate su come funziona, consulta il documento [Adaptive Image Servlet](/help/developing/adaptive-image-servlet.md).

## Supporto di Dynamic Media {#dynamic-media}

Il componente Immagine (a partire dalla [versione 2.13.0](/help/versions.md)) supporta le risorse di [Dynamic Media](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/dynamic-media.html?lang=it). [Se abilitate,](#design-dialog) queste funzioni consentono di aggiungere risorse immagine di Dynamic Media con una semplice azione di trascinamento e rilascio della selezione oppure tramite il browser delle risorse, esattamente come faresti con qualsiasi altra immagine. Sono inoltre supportati modificatori di immagini, immagini preimpostate e ritaglio avanzato.

La tua esperienza del web costruita con i Componenti core ora si arricchisce delle molte funzionalità per le immagini offerte da Dynamic Media, efficienti, performanti, multipiattaforma e con tecnologia Sensei.

## Supporto risorse remote {#remote-assets}

Il componente Immagine (a partire dalla [versione 2.23.2](/help/versions.md)) supporta le risorse remote. [Una volta configurato](/help/developing/remote-assets.md), è possibile selezionare le risorse da un servizio remoto per il componente Immagine.

## Supporto di SVG {#svg-support}

Il componente Immagine supporta la grafica vettoriale scalabile (SVG).

* L’inserimento tramite trascinamento di una risorsa SVG da DAM e il caricamento di un file SVG da un file system locale sono supportati entrambi.
* Il file SVG originale viene inviato in streaming (le trasformazioni vengono ignorate).
* Per un’immagine SVG, le “immagini avanzate” e le “dimensioni avanzate” sono impostate su un array vuoto nel modello di immagine.

### Sicurezza {#security}

Per motivi di sicurezza, il file SVG originale non viene mai richiamato direttamente dall’editor di immagini. Viene richiamato tramite `<img src="path-to-component">`. Ciò impedisce al browser di eseguire eventuali script incorporati nel file SVG.

## Esempio di output del componente {#sample-component-output}

Per avere un’idea del componente Immagine e vedere esempi di opzioni di configurazione e dell’output HTML e JSON, visita la [libreria dei componenti](https://adobe.com/go/aem_cmp_library_image_it).

### Dettagli tecnici {#technical-details}

La documentazione tecnica più recente sul componente Immagine [è disponibile su GitHub](https://adobe.com/go/aem_cmp_tech_image_v3_it).

Per ulteriori informazioni sullo sviluppo di Componenti core, vedi la [documentazione per gli sviluppatori di Componenti core](/help/developing/overview.md).

Il componente Immagine supporta [i microdati schema.org](https://schema.org).

## Finestra di dialogo per la modifica {#edit-dialog}

La finestra di dialogo per la modifica consente a chi crea contenuti di ritagliare ed eseguire lo zoom dell’immagine.

A seconda che tu abbia o meno abilitato le funzioni di [Dynamic Media](#dynamic-media) o il [Supporto risorse remote](#remote-assets), le opzioni disponibili per la modifica delle immagini saranno diverse.

### Modifica delle risorse standard {#standard-assets}

Se stai modificando AEM Assets standard, puoi fare clic sull’icona **Modifica** nel menu di scelta rapida del componente immagine.

![Finestra di dialogo per modifica del componente Immagine](/help/assets/image-edit.png)

* Avvia ritaglio

  ![Icona Avvia ritaglio](/help/assets/image-start-crop.png)

  Selezionando questa opzione si apre un elenco a discesa per le proporzioni predefinite del ritaglio.

   * Scegli l’opzione **Rimuovi Ritaglio** per visualizzare la risorsa originale.

  Una volta selezionata un’opzione di ritaglio, utilizza le maniglie blu per dimensionare il ritaglio sull’immagine.

  ![Opzioni di ritaglio](/help/assets/image-crop-options.png)

* Ruota a destra

  ![Icona Ruota a destra](/help/assets/image-rotate-right.png)

  Utilizza questa opzione per ruotare l’immagine di 90° verso destra (in senso orario).

* Reimposta zoom

  ![Icona Reimposta zoom](/help/assets/image-reset-zoom.png)

  Se l’immagine è già stata ingrandita, utilizza questa opzione per reimpostare il livello di zoom.

* Apri cursore Zoom

  ![Icona Apri cursore zoom](/help/assets/image-zoom.png)

  Utilizza questa opzione per visualizzare un cursore che permette di controllare il livello di zoom dell’immagine.

  ![Controllo cursore dello zoom](/help/assets/image-zoom-slider.png)

L’editor locale può essere utilizzato anche per modificare l’immagine. A causa di limiti di spazio, in linea sono disponibili solo opzioni di base. Per le opzioni di modifica completa, utilizza la modalità a schermo intero.

![Opzioni di modifica diretta dell’immagine](/help/assets/image-in-place-edit.png)

>[!NOTE]
>
>Le operazioni di modifica delle immagini non sono supportate per le immagini GIF. Tutte le modifiche apportate in modalità Modifica alle immagini GIF non verranno mantenute.

### Modifica delle risorse Dynamic Media {#dynamic-media-assets}

Se le [funzionalità Dynamic Media sono abilitate,](#dynamic-media) la modifica dell’immagine stessa deve essere eseguita nella console Assets.

## Finestra di dialogo per la configurazione {#configure-dialog}

Il componente Immagine offre una finestra di dialogo di configurazione in cui l’immagine stessa è definita insieme alla relativa descrizione e alle proprietà di base.

### Scheda Risorsa {#asset-tab}

![Scheda Risorsa della finestra di dialogo per configurazione del componente Immagine](/help/assets/image-configure-asset.png)

* **Eredita immagine in primo piano dalla pagina**: Questa opzione utilizza [l’immagine in primo piano della pagina collegata](page.md) o l’immagine in primo piano della pagina corrente se l’immagine non è collegata.

* **Risorsa immagine**:se è selezionata l’opzione **Eredita immagine in primo piano dalla pagina**, viene compilata automaticamente. Deseleziona questa opzione per definire manualmente l’immagine impostando le seguenti opzioni.

   * Trascina una risorsa dal [browser Risorse](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/fundamentals/environment-tools.html?lang=it) o tocca l’opzione **Sfoglia** per caricarla da un file system locale.
   * Tocca o fai clic su **Cancella** per deselezionare l’immagine attualmente selezionata.
   * Tocca o fai clic su **Scegli** per aprire il [browser Risorse](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/fundamentals/environment-tools.html?lang=it) e seleziona un’immagine.
      * Se il [Supporto risorse remote](#remote-assets) è attivato, sono disponibili diverse opzioni per la scelta di una risorsa:
         * **Locale** sceglie la risorsa dalla libreria di risorse AEM locale.
         * **Remoto** sceglie la risorsa da una libreria Dynamic Media esterna all’istanza AEM.
   * Tocca o fai clic su **Modifica** per [gestire le rappresentazioni della risorsa](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/manage/manage-digital-assets.html?lang=it) nell’Editor risorse.

* **Testo alternativo per accessibilità**: Questo campo consente di definire una descrizione dell’immagine per gli utenti ipovedenti.

   * **Eredita testo alternativo dalla pagina**: Questa opzione utilizza la descrizione alternativa del valore della risorsa collegata dei metadati `dc:description` in DAM o nella pagina corrente se non è collegata alcuna risorsa.

* **Non fornire testo alternativo** : questa opzione contrassegna l’immagine da ignorare da parte di tecnologie di assistenza, come le utilità per la lettura dello schermo, nei casi in cui l’immagine sia puramente decorativa o in altro modo non trasmetta informazioni aggiuntive alla pagina.

### Scheda Metadati {#metadata-tab}

![Scheda Metadati della finestra di dialogo per configurazione del componente Immagine](/help/assets/image-configure-metadata.png)

* **Tipo di predefinito**: definisce i tipi di immagini preimpostate disponibili, **Predefinito immagine** o **Ritaglio avanzato**, ed è disponibile solo se [le funzioni di Dynamic Media](#dynamic-meida) sono abilitate.
   * **Predefinito immagine**: se per **Tipo di predefinito** è selezionata l’opzione **Predefinito immagine**, è disponibile l’elenco a discesa **Predefinito immagine** che consente di selezionare i predefiniti di Dynamic Media disponibili. Questa opzione è disponibile solo se per la risorsa selezionata esistono dei predefiniti.
   * **Ritaglio avanzato** : quando viene selezionato **Tipo di predefinito** di **Ritaglio avanzato**, è disponibile l’elenco a discesa **Rappresentazione** che consente di selezionare le rappresentazioni disponibili della risorsa selezionata. Questa opzione è disponibile solo se per la risorsa selezionata sono definiti rendering.
   * **Modificatori immagine**: qui si possono definire comandi Dynamic Media aggiuntivi per la gestione delle immagini, separati da `&`, indipendentemente da qualunque cosa sia selezionata per **Tipo di predefinito**.
* **Didascalia**: informazioni aggiuntive sull’immagine, per impostazione predefinita viene visualizzata sotto l’immagine.
   * **Ottieni didascalia da DAM** : se questa opzione è selezionata, come didascalia dell’immagine verrà inserito il valore dei `dc:title` metadati in DAM.
   * **Visualizza didascalia come finestra a comparsa** : se questa opzione è selezionata, la didascalia non verrà visualizzata sotto l’immagine, ma, in alcuni browser, come finestra a comparsa al passaggio del puntatore sull’immagine.
* **Collegamento**: collega l’immagine a un’altra risorsa.
   * Utilizza la finestra di dialogo per selezione per stabilire il collegamento con un’altra risorsa AEM.
   * Se non stabilisci il collegamento con un’altra risorsa AEM, immetti l’URL assoluto. Gli URL non assoluti vengono interpretati come relativi a AEM.
   * **Apri il collegamento in una nuova scheda**: questa opzione apre il collegamento in una nuova finestra del browser.
* **ID** : questa opzione consente di controllare l’identificatore univoco del componente nel codice HTML e nel [livello dati](/help/developing/data-layer/overview.md).
   * Se non specificato, viene generato automaticamente un ID univoco reperibile sulla pagina risultante.
   * Se l’ID viene specificato, è responsabilità dell’autore accertarsi che sia univoco.
   * La modifica dell’ID può avere un impatto sul tracciamento di CSS, JS e Livello dati.

>[!TIP]
>
>Le opzioni **Ritaglio avanzato** e **Predefinito immagine** si escludono a vicenda. Se un autore deve utilizzare un predefinito per immagine insieme a una rappresentazione di ritaglio avanzato, dovrà avvalersi dei **Modificatori immagine**, per aggiungere manualmente i predefiniti.

### Scheda Stili {#styles-tab-edit}

![Scheda Stili della finestra di dialogo di modifica del componente Immagine](/help/assets/image-configure-styles.png)

Il componente Immagine supporta il [sistema di stili](/help/get-started/authoring.md#component-styling) di AEM.

Utilizza il menu a discesa per selezionare gli stili da applicare al componente. Le selezioni effettuate nella finestra di dialogo di modifica hanno lo stesso effetto di quelle selezionate nella barra degli strumenti del componente.

Gli stili devono essere configurati per questo componente nella [finestra di dialogo di progettazione](#design-dialog) affinché il menu a discesa sia disponibile.

## Finestra di dialogo per la progettazione {#design-dialog}

### Scheda Principale {#main-tab}

![Scheda Principale della finestra di dialogo per progettazione del componente Immagine](/help/assets/image-design-main.png)

* **Abilita funzioni DM**: Se questa opzione è selezionata, sono disponibili [le funzioni di Dynamic Media](#dynamic-media).
   * Questa opzione viene visualizzata solo quando Dynamic Media è abilitato nell’ambiente.
* **Abilita immagini ottimizzate per il web**: quando questa opzione è selezionata, il [servizio di consegna delle immagini ottimizzate per il web](/help/developing/web-optimized-image-delivery.md) fornisce immagini in formato WebP, riducendone in media le dimensioni del 25%.
   * Questa opzione è disponibile solo in AEMaaCS.
   * Se non è selezionata o se il servizio di consegna delle immagini ottimizzate per il web non è disponibile, viene utilizzato [Adaptive Image Servlet](/help/developing/adaptive-image-servlet.md) .
* **Disattiva il caricamento lento**: se questa opzione è selezionata, il componente precarica tutte le immagini senza caricamento lento.
* **L’immagine è decorativa**: consente di definire se l’opzione dell’immagine decorativa è abilitata automaticamente quando si aggiunge il componente Immagine a una pagina.
* **Ottieni testo alternativo da DAM**: consente di definire se l’opzione per recuperare il testo alternativo dal DAM è abilitata automaticamente quando si aggiunge il componente Immagine a una pagina.
* **Ottieni didascalia da DAM**: consente di definire se l’opzione per recuperare la didascalia dal DAM è abilitata automaticamente quando si aggiunge il componente Immagine a una pagina.
* **Visualizza didascalia come nota a comparsa**: consente di definire se l’opzione per visualizzare la didascalia dell’immagine come nota a comparsa è abilitata automaticamente quando si aggiunge il componente Immagine a una pagina.
* **Larghezza di ridimensionamento**: Questo valore viene utilizzato per ridimensionare la larghezza delle immagini di base che sono risorse DAM.
   * Le proporzioni delle immagini vengono mantenute.
   * Se il valore è maggiore della larghezza effettiva dell’immagine, questo valore non avrà alcun effetto.
   * Questo valore non ha alcun effetto sulle immagini di SVG.

Puoi definire un elenco di larghezze consentite, espresse in pixel, in modo che l’immagine e il componente possano automaticamente caricare la larghezza appropriata in base alle dimensioni della finestra del browser. Questa è una parte importante delle [funzioni reattive](#responsive-features) del componente Immagine.

* **Larghezze**: consente di definire un elenco di larghezze, espresse in pixel, in modo che l’immagine e il componente possano automaticamente caricare la larghezza appropriata in base alle dimensioni della finestra del browser.
   * Tocca o fai clic sul pulsante **Aggiungi** per aggiungere un’altra dimensione.
      * Utilizza le maniglie per ridisporre l’ordine delle dimensioni.
      * Utilizza l’icona **Elimina** per rimuovere una larghezza.
   * Per impostazione predefinita, il caricamento delle immagini viene differito fino a quando non diventano visibili.
      * Seleziona l’opzione **Disattiva il caricamento lento** per caricare le immagini al caricamento della pagina.
* **Qualità JPEG**: fattore di qualità, espresso come percentuale tra 0 e 100, per immagini JPEG trasformate, ad esempio ridimensionate o ritagliate.

>[!TIP]
>
>Consulta il documento [Adaptive Image Servlet](/help/developing/adaptive-image-servlet.md) per suggerimenti su come ottimizzare la selezione delle rappresentazioni definendone con attenzione le dimensioni.

### Scheda Stili {#styles-tab}

Il componente Immagine supporta il [sistema di stili](/help/get-started/authoring.md#component-styling) di AEM.

## Adobe Client Data Layer {#data-layer}

Il componente Immagine supporta [Adobe Client Data Layer.](/help/developing/data-layer/overview.md)
