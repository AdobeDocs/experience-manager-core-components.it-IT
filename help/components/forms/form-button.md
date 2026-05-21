---
title: Componente Pulsante modulo
description: Il componente core Campo nascosto modulo consente di includere un campo nascosto in un modulo.
role: Developer, Admin, User
exl-id: 1e5cff43-57db-4bfc-b2d2-23307eaf5eb3
TQID: https://experienceleague.adobe.com/GzfypWAMUQGej1-z15cKVe27SOkrovYOL5E-FsTRBkE
product_v2: id: c45915cf-e157-4af7-a80d-97b905bcb3a5id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: e2c1b6d3-bb7e-4fe8-8c72-f7b403298e91
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 73aa5234ac63fa3be99feebce448bb6722513838
workflow-type: tm+mt
source-wordcount: 416
ht-degree: 100%

---

# Componente Pulsante modulo {#form-button-component}

Il componente core Pulsante modulo consente di includere un pulsante per attivare un’azione su una pagina.

## Utilizzo {#usage}

Il componente core Pulsante modulo consente la creazione di un campo pulsante, spesso per attivare l’invio del modulo, che deve essere utilizzato insieme al componente [Contenitore modulo](form-container.md).

Le proprietà del pulsante possono essere definite tramite l’editor di contenuto nella [finestra di dialogo per configurazione](#configure-dialog).

## Versione e compatibilità {#version-and-compatibility}

La versione corrente del componente Pulsante modulo la v2, introdotta con la versione 2.0.0 dei Componenti core a gennaio 2018, ed è quella descritta in questo documento.

La tabella che segue descrive tutte le versioni supportate del componente, le versioni di AEM con cui le versioni del componente sono compatibili e i collegamenti alla documentazione delle versioni precedenti.

| Versione del componente | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |--- |---|---|
| v2 | Compatibile con la <br>[versione 2.17.4](/help/versions.md) e precedenti | Compatibile | Compatibile | Compatibile |
| [v1](/help/components/v1/form-button-v1.md) | Compatibile | Compatibile | - | Compatibile |

Per ulteriori informazioni sulle versioni e sugli aggiornamenti dei Componenti core, vedi il documento [Versioni dei Componenti core](/help/versions.md).

## Esempio di output del componente {#sample-component-output}

Per avere un’idea del componente Pulsante modulo e vedere esempi delle opzioni di configurazione e dell’output HTML e JSON, visita la [libreria dei componenti](https://adobe.com/go/aem_cmp_library_form_button_it).

### Dettagli tecnici {#technical-details}

La documentazione tecnica più recente sul componente Pulsante modulo [è disponibile su GitHub](https://adobe.com/go/aem_cmp_tech_form_button_v2_it).

Per ulteriori informazioni sullo sviluppo di Componenti core, vedi la [documentazione per gli sviluppatori di Componenti core](/help/developing/overview.md).

## Finestra di dialogo per configurazione {#configure-dialog}

La finestra di dialogo per configurazione consente all’autore di contenuto di definire i parametri del pulsante.

### Scheda Proprietà {#properties-tab}

![Finestra di dialogo per modifica del componente Pulsante modulo](/help/assets/form-button-edit.png)

* **Tipo**

   * **Pulsante**
   * **Invia**

* **Titolo**: il testo visualizzato sul pulsante

   * Se non viene specificato alcun testo, viene utilizzato automaticamente il tipo di pulsante

* **Nome**: il nome del pulsante, che viene inviato con i dati del modulo
* **Valore**: il valore del pulsante, che viene inviato con i dati del modulo

* **ID**: questa opzione consente di controllare l’identificatore univoco del componente nel codice HTML e nel [livello dati](/help/developing/data-layer/overview.md).
   * Se non specificato, viene generato automaticamente un ID univoco reperibile sulla pagina risultante.
   * Se l’ID viene specificato, è responsabilità dell’autore accertarsi che sia univoco.
   * La modifica dell’ID può avere un impatto sul tracciamento di CSS, JS e livello dati.

## Finestra di dialogo per progettazione {#design-dialog}

### Scheda Stili {#styles-tab}

Il componente Pulsante modulo supporta il [sistema di stili](/help/get-started/authoring.md#component-styling) di AEM.
