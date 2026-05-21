---
title: Componente Pulsante (v1)
description: Il componente core Pulsante consente di creare e visualizzare un pulsante.
role: Developer, Admin, User
exl-id: 63af16e4-dd4d-426d-88ef-769ecd1b3175
index: false
TQID: https://experienceleague.adobe.com/te1330KgXtcUKnZTKKvYr4Uf48z9RYRKcY76tZ1oenE
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
source-wordcount: 408
ht-degree: 100%

---

# Componente Pulsante (v1) {#button-component}

Il componente core Pulsante consente di configurare e visualizzare un pulsante su una pagina.

## Utilizzo {#usage}

Il componente core Pulsante consente di includere un pulsante in una pagina.

* Le proprietà del Pulsante possono essere selezionate nella [finestra di dialogo per configurazione](#configure-dialog).
* Gli stili del componente Pulsante possono essere definiti nella [finestra di dialogo per progettazione](#design-dialog).

## Versione e compatibilità {#version-and-compatibility}

Il documento descrive la versione 1 del componente Pulsante, introdotto con la versione 2.5.0 dei componenti core a giugno 2019.

>[!CAUTION]
>
>Questo documento descrive la versione 1 del componente Pulsante.
>
>Per informazioni dettagliate sulla versione corrente del componente Pulsante, consulta il documento [Componente pulsante](/help/components/button.md).

## Esempio di output del componente {#sample-component-output}

Per avere un’idea del componente Pulsante e vedere esempi delle opzioni di configurazione e dell’output HTML e JSON, visita la [libreria dei componenti](https://adobe.com/go/aem_cmp_library_button).

## Dettagli tecnici {#technical-details}

La documentazione tecnica più recente sul componente Pulsante [è disponibile su GitHub](https://adobe.com/go/aem_cmp_tech_button_v1).

Per ulteriori informazioni sullo sviluppo di Componenti core, vedi la [documentazione per gli sviluppatori di Componenti core](/help/developing/overview.md).

## Finestra di dialogo per configurazione {#configure-dialog}

La finestra di dialogo per configurazione consente all’autore di contenuto di definire l’elemento Pulsante e il suo comportamento e aspetto nei confronti di chi visita la pagina.

### Scheda Proprietà {#properties-tab}

![Scheda Proprietà della finestra di dialogo per modifica del componente Pulsante](/help/assets/button-edit-properties.png)

* **Testo**: il testo da visualizzare sul pulsante
* **Collegamento**: il collegamento a una pagina di contenuto in AEM, una risorsa esterna o un ancoraggio
   * Utilizza la **finestra di dialogo per selezione** per scegliere un percorso all’interno di AEM.
* **Icona**: identificatore per la visualizzazione di un’icona nel pulsante
* **ID**: questa opzione consente di controllare l’identificatore univoco del componente nel codice HTML e nel [livello dati](/help/developing/data-layer/overview.md).
   * Se non specificato, viene generato automaticamente un ID univoco reperibile sulla pagina risultante.
   * Se l’ID viene specificato, è responsabilità dell’autore accertarsi che sia univoco.
   * La modifica dell’ID può avere un impatto sul tracciamento di CSS, JS e livello dati.

### Scheda Accessibilità {#accessibility-tab}

![Scheda Accessibilità della finestra di dialogo per modifica del componente Pulsante](/help/assets/button-edit-accessibility.png)

Nella scheda **Accessibilità** è possibile impostare i valori per le etichette di [accessibilità ARIA](https://www.w3.org/WAI/standards-guidelines/aria/) del componente.

* **Etichetta**: il valore di un attributo dell’etichetta ARIA del componente

## Finestra di dialogo per progettazione {#design-dialog}

### Scheda Stili {#styles-tab}

Il componente Pulsante supporta il [sistema di stili](/help/get-started/authoring.md#component-styling) di AEM.

## Adobe Client Data Layer {#data-layer}

Il componente Pulsante supporta [Adobe Client Data Layer.](/help/developing/data-layer/overview.md)
