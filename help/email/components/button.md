---
title: Componente Pulsante e-mail
description: Il componente Pulsante e-mail consente di configurare e visualizzare un pulsante nel contenuto.
role: Developer, Admin, User
exl-id: b144e8d1-1097-475d-b2eb-3353c176afb9
index: false
TQID: https://experienceleague.adobe.com/-kCXMMJi8n6DSMh97cgqruQY8pI04AkhxO2GEvwaK6s
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
source-wordcount: 527
ht-degree: 100%

---

# Componente Pulsante e-mail {#email-button-component}

Il componente Pulsante e-mail consente di configurare e visualizzare un pulsante nel contenuto.

## Utilizzo {#usage}

Il componente Pulsante e-mail consente di includere nel contenuto un pulsante su cui chi legge il contenuto può fare clic e che è collegato a risorse aggiuntive.

* Le proprietà del pulsante possono essere selezionate nella [finestra di dialogo per la configurazione.](#configure-dialog)
* Gli stili del componente Pulsante e-mail possono essere definiti nella [finestra di dialogo per la progettazione.](#design-dialog)

## Versione e compatibilità {#version-and-compatibility}

La versione corrente del componente Pulsante e-mail è la versione 1, introdotta con la versione x dei componenti core E-mail a ottobre 2022, ed è quella descritta in questo documento.

La tabella che segue descrive tutte le versioni supportate del componente, le versioni di AEM con cui le versioni del componente sono compatibili e i collegamenti alla documentazione delle versioni precedenti.

| Versione del componente | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|---|---|---|---|
| v1 | Compatibile | - | - |

Per ulteriori informazioni sulle versioni e sugli aggiornamenti dei Componenti core, consulta il documento [Versioni dei componenti core E-mail.](/help/email/versions.md)

## Dettagli tecnici {#technical-details}

La documentazione tecnica più recente sul componente Pulsante e-mail [è disponibile su GitHub.](https://adobe.com/go/aem_cmp_tech_email_button_v1)

Per ulteriori informazioni sullo sviluppo di Componenti core, vedi la [documentazione per gli sviluppatori di Componenti core.](/help/developing/overview.md)

## Finestra di dialogo per la configurazione {#configure-dialog}

La finestra di dialogo per la configurazione consente all’autore del contenuto di definire il pulsante, il suo comportamento e come si presenta a chi legge il contenuto.

### Scheda Proprietà {#properties-tab}

![Scheda Proprietà della finestra di dialogo per modifica del componente Pulsante](/help/email/assets/email-button-edit-properties.png)

* **Testo**: il testo da visualizzare sul pulsante
   * Fai clic sull’icona Campaign per aprire la finestra di dialogo [Seleziona variabile di Adobe Campaign](/help/email/campaign-variables.md) per inserire contenuto dinamico da Adobe Campaign.
* **Collegamento**: il collegamento a una pagina di contenuto in AEM, una risorsa esterna o un ancoraggio
   * Utilizza la **finestra di dialogo per selezione** per scegliere un percorso all’interno di AEM.
   * Fai clic sull’icona Campaign per aprire la finestra di dialogo [Seleziona variabile di Adobe Campaign](/help/email/campaign-variables.md) per inserire contenuto dinamico da Adobe Campaign.
* **Icona**: identificatore per la visualizzazione di un’icona nel pulsante
* **ID**: questa opzione consente di controllare l’identificatore univoco del componente nel codice HTML.
   * Se non specificato, viene generato automaticamente un ID univoco reperibile esaminando il contenuto risultante.
   * Se l’ID viene specificato, è responsabilità dell’autore accertarsi che sia univoco.
   * La modifica dell’ID può avere un impatto sulle CSS.
* **Apri il collegamento in una nuova scheda**: se questa opzione è selezionata, il collegamento verrà aperto in una nuova scheda del browser.

### Scheda Accessibilità {#accessibility-tab}

![Scheda Accessibilità della finestra di dialogo per modifica del componente Pulsante](/help/email/assets/email-button-edit-accessibility.png)

Nella scheda **Accessibilità** è possibile impostare i valori per le etichette di [accessibilità ARIA](https://www.w3.org/WAI/standards-guidelines/aria/) del componente.

* **Etichetta**: il valore di un attributo dell’etichetta ARIA del componente

### Scheda Stili {#styles-tab-edit}

Il componente Pulsante e-mail supporta il [sistema di stili](/help/get-started/authoring.md#component-styling) di AEM.

Utilizza il menu a discesa per selezionare gli stili da applicare al componente. Le selezioni effettuate nella finestra di dialogo di modifica hanno lo stesso effetto di quelle selezionate nella barra degli strumenti del componente.

Gli stili devono essere configurati per questo componente nella [finestra di dialogo per progettazione](#design-dialog) affinché la scheda sia disponibile.

## Finestra di dialogo per progettazione {#design-dialog}

### Scheda Stili {#styles-tab}

Il componente Pulsante e-mail supporta il [sistema di stili](/help/get-started/authoring.md#component-styling) di AEM.
