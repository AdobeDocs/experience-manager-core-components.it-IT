---
title: hCaptcha nei moduli adattivi di AEM
description: Migliora la sicurezza dei moduli con il servizio hCaptcha&reg; senza sforzo. Guida dettagliata all’interno!
feature-set: Experience Manager Sites, Experience Manager Forms
feature: Adaptive Forms, Core Components
role: Architect, Developer, Admin, User
exl-id: eecb38d5-711e-4dc5-bc19-498e003f37e7
source-git-commit: be25eac36cafda0ff0cb745454593640cc54ceea
workflow-type: ht
source-wordcount: '583'
ht-degree: 100%

---

# Componente hCaptcha{#hCaptcha-component-adaptive-forms-core-component}

<span class="preview"> Questa funzione si trova nel programma per i primi utilizzatori. Per partecipare al programma per i primi utilizzatori, richiedi l’accesso alla funzionalità inviando una e-mail dal tuo account ufficiale all’indirizzo aem-forms-ea@adobe.com. </span>

Il servizio hCaptcha® protegge i moduli da bot, spam e abusi automatizzati. Pone una sfida in un widget casella di controllo e valuta la risposta dell’utente per determinare se si tratta di un essere umano o di un bot che interagisce con il modulo. Questo impedisce all’utente di procedere se il test non riesce e contribuisce a rendere sicure le transazioni online impedendo ai bot di pubblicare spam o praticare attività dannose.

![hCaptcha®](/help/adaptive-forms/assets/hCaptcha-challenge.png)

## Utilizzo {#usage}

Includere una sfida hCaptcha in un processo di invio moduli è utile per vari motivi, tra cui:

- **Prevenzione dei bot**: assicura che il modulo venga inviato da un essere umano, riducendo lo spam e gli invii automatizzati.

- **Sicurezza**: aggiunge un ulteriore livello di sicurezza, verificando la legittimità di ogni invio di moduli e proteggendo da attacchi dannosi.

- **Integrità dei dati**: impedendo invii multipli o fraudolenti, contribuisce a mantenere l’integrità e l’accuratezza dei dati raccolti tramite il modulo.

- **Verifica utente**: verifica l’identità dell’utente che invia il modulo, assicurandosi che solo gli utenti autenticati possano completare transazioni sensibili.

- **Gestione del carico**: consente di gestire il carico del server controllando la frequenza di invio dei moduli, evitando il sovraccarico del sistema durante periodi di traffico elevato.

## Dettagli tecnici {#technical-details}

Per informazioni aggiornate sul componente hCaptcha consulta la documentazione tecnica disponibile su [GitHub](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/hCaptcha/v1/hCaptcha/README.md). Per ulteriori informazioni sullo sviluppo dei componenti core, dai un’occhiata alla [documentazione sui componenti core per gli sviluppatori](/help/developing/overview.md).

Specifica le proprietà del componente hCaptcha utilizzando la [finestra di dialogo per la configurazione](#configure-dialog). La finestra di dialogo per la configurazione fa parte dei componenti core, sviluppati per semplificare la creazione dei moduli e fornire un modo efficiente per creare moduli complessi.

## Versione e compatibilità {#version-and-compatibility}


Il componente hCaptcha per moduli adattivi è stato rilasciato a maggio 2024 come parte di [Componenti core 3.0.20](https://github.com/adobe/aem-core-forms-components/commit/a4cb97131ffad47137a8f5f173401128a1cf3491). Di seguito è riportata una tabella che mostra tutte le versioni supportate, la compatibilità AEM e i collegamenti alla documentazione corrispondente:

|  |  |
|---|---|
| Versione del componente | AEM as a Cloud Service |
| --- | --- |
| v1 | Compatibile con <br>[versione 2.0.4](/help/adaptive-forms/version.md) e successive | Compatibile | Compatibile |

Per informazioni sulle versioni dei componenti core, consulta il documento [Versioni dei componenti core](/help/adaptive-forms/version.md).

## Finestra di dialogo per la configurazione {#configure-dialog}

Puoi personalizzare facilmente le proprietà del componente hCaptcha con la relativa finestra di dialogo per la configurazione, con la scheda Base e la scheda Convalida.

### Scheda Base {#basic-tab}

- **[!UICONTROL Nome]:** specificando il nome del componente hCaptcha, puoi identificare facilmente un componente modulo con il suo nome univoco sia nel modulo che nell’editor di regole.
- **[!UICONTROL Titolo]:** specifica il titolo del componente hCaptcha.
- **[!UICONTROL Impostazioni di configurazione]:** seleziona una configurazione cloud impostata per hCaptcha®.
- **Dimensione Captcha:** è possibile selezionare le dimensioni di visualizzazione della finestra di dialogo sfida hCaptcha®. Utilizza l’opzione **[!UICONTROL Compatta]** per visualizzare una dimensione ridotta e **[!UICONTROL Normale]** per visualizzare una finestra di dialogo di verifica hCaptcha® di dimensioni relativamente grandi.<!-- or **[!UICONTROL Invisible]** to validate hCaptcha&reg; without explicitly rendering the checkbox widget on the user interface. -->

  ![Scheda Base hCaptcha](/help/adaptive-forms/assets/hcaptcha-basic.png)

### Scheda Convalida {#validation-tab}

- **[!UICONTROL Messaggio di convalida]:** fornisci un messaggio per la convalida Captcha al momento dell’invio del modulo.
- **[!UICONTROL Messaggio di convalida script]**: utilizza questa opzione per immettere un messaggio di richiesta, se la convalida dello script non riesce.

  ![Scheda Convalida hCaptcha](/help/adaptive-forms/assets/hcaptcha-validation-tab.png)

**hCaptcha® è un marchio registrato di Intuition Machines, Inc.**

**Ulteriori informazioni** informazioni su altri **Componenti Captcha** e i relativi servizi, quali:

- [Utilizzo di hCaptcha in un modulo adattivo per i componenti core](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/integrate-adaptive-forms-hcaptcha-core-components)

- [Utilizzo di hCaptcha in un modulo adattivo per i componenti di base](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/add-components-to-an-adaptive-form/integrate-adaptive-forms-hcaptcha)

- [Utilizzo di CAPTCHA Turnstile in un modulo adattivo per i componenti di base](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/add-components-to-an-adaptive-form/integrate-adaptive-forms-turnstile)

- [Utilizzo di Google reCAPTCHA in un modulo adattivo per i componenti di base](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/captcha-adaptive-forms-core-components)

## Articoli correlati {#related-articles}

{{more-like-this}}

## Consulta anche {#see-also}

{{see-also}}
