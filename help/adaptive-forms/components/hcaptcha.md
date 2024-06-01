---
title: hCaptcha nel Forms adattivo dell’AEM
description: Migliora la sicurezza dei moduli con il servizio hCaptcha&reg; senza sforzo. Guida passo passo all'interno!
feature-set: Experience Manager Sites, Experience Manager Forms
feature: Adaptive Forms, Core Components
role: Architect, Developer, Admin, User
source-git-commit: ddfd55259f84443e6add3ced09fd319bcd9c1677
workflow-type: tm+mt
source-wordcount: '583'
ht-degree: 12%

---

# Componente hCaptcha{#hCaptcha-component-adaptive-forms-core-component}

<span class="preview"> Questa funzione si trova nel programma Early Adopter. Puoi scrivere a aem-forms-ea@adobe.com dal tuo ID e-mail ufficiale per partecipare al programma early adopter e richiedere l’accesso alla funzionalità. </span>

Il servizio hCaptcha® protegge i moduli da bot, spam e abusi automatizzati. Questo pone una sfida al widget casella di controllo e valuta la risposta dell’utente per determinare se si tratta di un umano o di un bot che interagisce con il modulo. Impedisce all’utente di procedere se il test non riesce e contribuisce a rendere sicure le transazioni online impedendo ai bot di pubblicare spam o attività dannose.

![Captcha®](/help/adaptive-forms/assets/hCaptcha-challenge.png)

## Utilizzo {#usage}

Ci sono diversi motivi per cui è utile includere una sfida hCaptcha in un processo di invio del modulo, questi sono:

- **Prevenzione dei bot**: assicura che il modulo venga inviato da un utente, riducendo lo spam e gli invii automatizzati.

- **Sicurezza**: aggiunge un ulteriore livello di sicurezza, verificando la legittimità di ogni invio di moduli e proteggendo contro attacchi dannosi.

- **Integrità dei dati**: impedendo invii multipli o fraudolenti, contribuisce a mantenere l’integrità e l’accuratezza dei dati raccolti tramite il modulo.

- **Verifica utente**: verifica l’identità dell’utente che invia il modulo, assicurandosi che solo gli utenti autenticati possano completare transazioni sensibili.

- **Gestione del carico**: consente di gestire il carico del server controllando la frequenza di invio dei moduli, evitando il sovraccarico del sistema durante periodi di traffico elevato.

## Dettagli tecnici {#technical-details}

Per informazioni aggiornate sul componente hCaptcha, consulta la documentazione tecnica su [GitHub](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/hCaptcha/v1/hCaptcha/README.md). Per ulteriori informazioni sullo sviluppo dei componenti core, dai un’occhiata alla [documentazione per gli sviluppatori dei componenti core](/help/developing/overview.md).

Specifica le proprietà del componente hCaptcha utilizzando [finestra di dialogo per configurazione](#configure-dialog). La finestra di dialogo per configurazione fa parte dei componenti core, creati per semplificare l’authoring dei moduli e fornire un modo efficiente per creare moduli complessi.

## Versione e compatibilità {#version-and-compatibility}


Il componente hCaptcha per Forms adattivo è stato rilasciato a maggio 2024 come parte del [Componenti core 3.0.20](https://github.com/adobe/aem-core-forms-components/commit/a4cb97131ffad47137a8f5f173401128a1cf3491). Di seguito è riportata una tabella che mostra tutte le versioni supportate, la compatibilità AEM e i collegamenti alla documentazione corrispondente:

|  |  |
|---|---|
| Versione del componente | AEM as a Cloud Service |
| --- | --- |
| v1 | Compatibile con <br>[versione 2.0.4](/help/adaptive-forms/version.md) e successive | Compatibile | Compatibile |

Per informazioni sulle versioni dei componenti core, consulta il documento [Versioni dei componenti core](/help/adaptive-forms/version.md).

## Finestra di dialogo per la configurazione {#configure-dialog}

Puoi personalizzare facilmente le proprietà del componente hCaptcha con la relativa finestra di dialogo per configurazione, con la scheda Base e la scheda Convalida, per personalizzare varie proprietà.

### Scheda Base {#basic-tab}

- **[!UICONTROL Nome]:** Specificando il nome del componente hCaptcha, puoi identificare facilmente un componente modulo con il suo nome univoco sia nel modulo che nell’editor di regole.
- **[!UICONTROL Titolo]:** Specifica il titolo del componente hCaptcha.
- **[!UICONTROL Impostazioni di configurazione]:** Seleziona una configurazione cloud configurata per hCaptcha®.
- **Dimensione Captcha:** È possibile selezionare le dimensioni di visualizzazione della finestra di dialogo sfida hCaptcha®. Utilizza il **[!UICONTROL Compatto]** per visualizzare una dimensione ridotta e il **[!UICONTROL Normale]** per visualizzare una finestra di dialogo di verifica hCaptcha® di dimensioni relativamente grandi.<!-- or **[!UICONTROL Invisible]** to validate hCaptcha&reg; without explicitly rendering the checkbox widget on the user interface. -->

  ![Scheda di base hCaptcha](/help/adaptive-forms/assets/hcaptcha-basic.png)

### Scheda Convalida {#validation-tab}

- **[!UICONTROL Messaggio di convalida]:** Fornisci un messaggio di convalida per la convalida Captcha al momento dell’invio del modulo.
- **[!UICONTROL Messaggio di convalida script]** : utilizza questa opzione per immettere un messaggio di richiesta, se la convalida dello script non riesce.

  ![Scheda di convalida hCaptcha](/help/adaptive-forms/assets/hcaptcha-validation-tab.png)

**hCaptcha® è un marchio registrato di Intuition Machines, Inc.**

**Ulteriori informazioni** informazioni su altro **Componenti Captcha** e i relativi servizi, quali:

- [Utilizzare hCaptcha in un modulo adattivo per i componenti core](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/integrate-adaptive-forms-hCaptcha-core-components)

- [Utilizzare hCaptcha in un modulo adattivo per i componenti di base](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/add-components-to-an-adaptive-form/integrate-adaptive-forms-hcaptcha)

- [Utilizzare il CAPTCHA a tornello in un modulo adattivo per i componenti di base](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/add-components-to-an-adaptive-form/integrate-adaptive-forms-turnstile)

- [Utilizzare Google reCAPTCHA in un modulo adattivo per i componenti di base](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/captcha-adaptive-forms-core-components)

## Articoli correlati {#related-articles}

{{more-like-this}}

## Consulta anche {#see-also}

{{see-also}}
