---
title: Introduzione ai componenti core dei moduli adattivi in AEM
description: Crea esperienze di iscrizione accattivanti (moduli) utilizzando la flessibilità dei componenti core dei moduli adattivi e forniscile con l’aiuto di Adobe Experience Manager.
role: Architect, Developer, Admin, User
exl-id: 6d0f2845-bbb8-4488-a254-b69d7a6290b1
source-git-commit: 6725784bd4c94d433c91d6bd65d14d03cbefd954
workflow-type: tm+mt
source-wordcount: '2123'
ht-degree: 100%

---


# Componenti core dei moduli adattivi  {#adaptive-forms-core-components-introduction}

Utilizzando i componenti core dei moduli adattivi in Adobe Experience Manager, puoi creare esperienze di iscrizione coinvolgenti.

{{traditional-aem}}

## Componenti core {#overview}

In Adobe Experience Manager (AEM), i componenti sono i blocchi predefiniti utilizzati per creare pagine e moduli. Forniscono agli autori un modo semplice e potente per creare e gestire i contenuti, fornendo allo stesso tempo agli sviluppatori la flessibilità e l’estensibilità necessarie per creare componenti personalizzati. Questi sono progettati per velocizzare i tempi di sviluppo e ridurre i costi di manutenzione per siti web e moduli, per essere flessibili e possono essere facilmente personalizzati in base alle esigenze specifiche di un sito web e di un modulo.

I componenti core sono inoltre progettati per essere reattivi e supportano un’ampia gamma di dispositivi, tra cui desktop, tablet e smartphone. Inoltre, rispettano gli standard web e le best practice più recenti, rendendoli una soluzione solida e affidabile per la creazione di contenuti web.

Nel complesso, i componenti core sono uno strumento essenziale per la creazione e la gestione dei contenuti web in AEM, potente e flessibile, che consente di ridurre i tempi di sviluppo e i costi di manutenzione e offire un’ esperienza utente ottimale a coloro che visitano il sito web.

## Componenti core dei moduli adattivi

I componenti core per moduli adattivi sono un set di 30 componenti open-source compatibili con BEM creati sulle basi dei componenti core WCM di Adobe Experience Manager. Sono progettati appositamente per la creazione di moduli adattivi, ossia moduli che si adattano al dispositivo, al browser e alle dimensioni dello schermo dell’utente.

Questi componenti possono essere utilizzati per creare esperienze eccezionali di acquisizione e registrazione dei dati fornendo un’ampia gamma di opzioni per i campi modulo, compresi campi di testo, caselle di controllo, menu a discesa e altro ancora. Includono anche funzioni quali convalida, logica condizionale e progettazione reattiva, che possono essere utilizzate per creare moduli intuitivi e facili da usare.

Inoltre, poiché questi componenti sono open-source, gli sviluppatori possono personalizzare ed estendere facilmente i componenti in base alle esigenze specifiche della propria organizzazione. Questi componenti sono inoltre basati sulla metodologia BEM, che garantisce la scalabilità e la manutenzione dei componenti.

![immagine del modulo adattivo](assets/sample-adaptive-form.png)

## Funzioni {#features}

|  |  |
|---|---|
| Pronti per la produzione | I componenti core dei moduli adattivi sono 24 componenti WCM affidabili. |
| Compatibile con cloud | Disponibile per [AEM Forms as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/home.html?lang=it). |
| Versatili | I componenti rappresentano concetti generici con i quali gli autori di moduli possono assemblare quasi tutti i layout. |
| Configurabili | I [criteri di contenuto](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/full-stack/components-templates/templates.html?lang=it#content-policies) a livello di modello definiscono quali funzioni sono utilizzabili e quali no. |
| Accessibili | Forniscono etichette ARIA, supportano la navigazione da tastiera e testo per tecnologie di assistenza come le utilità per la lettura dello schermo. |
| Con applicazione tema | I componenti implementano il [sistema di stili](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/features/style-system.html?lang=it) e il markup segue le [convenzioni BEM CSS](https://getbem.com/). |
| Personalizzabili | Diversi modelli consentono una facile personalizzazione, dalla modficia del codice HTML al riutilizzo avanzato delle funzionalità. |
| Controllo delle versioni | I [criteri di controllo delle versioni](https://github.com/adobe/aem-core-wcm-components/wiki/Versioning-policies) garantiscono che i Componenti core non blocchino il tuo sito in fase di miglioramento di elementi che potrebbero influire su di te. |
| Open source | Se qualcosa non va come dovrebbe, suggerisci miglioramenti. |

<!-- comply with [WCAG 2.1 standard](https://www.w3.org/TR/WCAG21/), -->


## Vantaggi {#benefits}

Le esperienze di acquisizione dei dati sono fondamentali per la generazione e la registrazione dei lead e i componenti core dei moduli adattivi offrono una soluzione potente per la creazione di moduli ottimizzati per l’acquisizione dei dati. Alcuni dei motivi per utilizzare i componenti core per creare queste esperienze sui componenti di base sono:

* **[Disponibilità su GitHub](https://github.com/adobe/aem-core-forms-components)**: i componenti core dei moduli adattivi in AEM sono open-source e disponibili su GitHub, insieme a una documentazione completa. In questo modo gli sviluppatori possono comprendere più facilmente i componenti e il loro funzionamento e contribuire al loro sviluppo. Anche il sito web [aemcomponents.dev](https://www.aemcomponents.dev/) è una risorsa preziosa, in cui gli sviluppatori possono vedere i componenti in azione e accedere alla documentazione dettagliata.

* **[Modello BEM per attribuzione di stile](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/using-themes-in-core-components)**: i componenti core seguono il modello BEM (Block Element Modifier) per lo stile, una metodologia consolidata e ampiamente utilizzata per l’organizzazione dei CSS. In questo modo gli sviluppatori possono comprendere più facilmente come sono organizzati gli stili e come modificarli in base alle proprie esigenze specifiche.

* **Nessuna dipendenza dalle librerie di terze parti**: uno dei vantaggi dei componenti core è che non hanno dipendenza da librerie JavaScript di terze parti, inclusi JQuery e Underscore. Questo rende i componenti più veloci e leggeri, nonché più facili da integrare in un’implementazione AEM esistente.

* **Focus su prestazioni e accessibilità**: i componenti core sono progettati tenendo presente le prestazioni e l’accessibilità, che si riflettono nei loro punteggi Google Lighthouse e web vitals elevati. Questo rende più facile per gli sviluppatori creare pagine web accessibili e dalle prestazioni elevate, che è sempre più importante nell’attuale panorama digitale.

* **Componenti modulo nel modello e nei temi di Sites 30**: i componenti core supportano i componenti del modulo nel modello e nei temi di Sites 30, facilitando agli sviluppatori la creazione e la personalizzazione dei moduli all’interno di AEM.

* **[Stile più semplice](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/using-themes-in-core-components)**: lo stile dei componenti core è più semplice rispetto a quello delle controparti componenti di base. Il processo di creazione del tema è simile a Sites, con la possibilità di ereditare lo stesso tema/CSS dalla pagina Sites principale. Inoltre, il modello BEM per lo stile facilita la comprensione e la modifica degli stili.

* **Accessibilità**: i componenti core dei moduli adattivi supportano gli standard e le linee guida di accessibilità per garantire che i moduli possano essere utilizzati da persone con disabilità, incluse quelle che utilizzano tecnologie per l’accessibilità, come le utilità per la lettura dello schermo.

* **[Controllo delle versioni](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/add-comments-annotations-versioning-adaptive-form-core-components)**: puoi creare e gestire più versioni di moduli adattivi basati su componenti core, partecipare a discussioni collaborative tramite commenti e allegare annotazioni a componenti modulo specifici, in modo da migliorare l’esperienza complessiva di creazione del modulo.

## Componenti disponibili: un raggruppamento per tipo di componente

La versione corrente di AEM Forms contiene i seguenti componenti core: [Componenti di base](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/create-an-adaptive-form-on-forms-cs/introduction-forms-authoring#component-toolbar) e [Componenti blocco modulo (Edge Delivery Services)](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/edge-delivery/build-forms/forms-references/form-components).

| Componenti | Componenti di base | Componenti core | Componenti blocco modulo | Informazioni aggiuntive |
|------------|:---------------------:|:---------------:|:---------------------:|-----------------------|
| Blocco Adobe Sign | ✔️ | | | [L’integrazione di Adobe Sign](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/forms/integrate/services/adobe-sign-integration-adaptive-forms#adobe-acrobat-sign-for-government) è disponibile solo per i componenti di base. |
| Pannello a soffietto | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/accordion.md)</span> | | Per i componenti di base, puoi configurare il layout del pannello a soffietto nelle [proprietà dei componenti del pannello](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-layout-of-an-adaptive-form/layout-capabilities-adaptive-forms#panel-layout). |
| Frammento di modulo adattivo | ✔️ | ✔️ | | Per i componenti di base, puoi [aggiungere un frammento](https://experienceleague.adobe.com/it/docs/experience-manager-65/content/forms/adaptive-forms-basic-authoring/adaptive-form-fragments#insert-a-fragment-in-an-adaptive-form) dal Browser risorse. |
| reCAPTCHA per modulo adattivo | ✔️ | ✔️ | ✔️ | Per i componenti di base, utilizza il componente Captcha per [aggiungere Google reCaptcha a un modulo](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/add-components-to-an-adaptive-form/captcha-adaptive-forms#google-reCAPTCHA). |
| Pulsante | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/button.md)</span> | ✔️ | |
| Grafico | ✔️ | | | |
| Casella di controllo | ✔️ | ✔️ | | |
| Gruppo di caselle di selezione | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/checkbox-group.md)</span> | ✔️ | Per i componenti di base, utilizza il componente casella di controllo per aggiungere più caselle di controllo |
| Campo immissione data | ✔️ | | | Per i componenti core, utilizza il componente [Selettore data](/help/adaptive-forms/components/date-picker.md). È inoltre possibile aggiungere i componenti [casella di testo](/help/adaptive-forms/components/text-box.md) o [casella numerica](/help/adaptive-forms/components/numeric-box.md) per acquisire il giorno, il mese e l’anno. |
| Selettore data | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/date-picker.md)</span> | ✔️ | |
| Elenco a discesa | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/drop-down-list.md)</span> | ✔️ | |
| E-mail | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/email.md)</span> | ✔️ | |
| Allegato file | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/file-attachment.md)</span> | ✔️ | |
| Elenco allegato file | ✔️ | | | |
| Piè di pagina | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/footer.md)</span> | ✔️ | |
| Segnaposto Nota a piè di pagina | ✔️ | | | |
| Contenitore modulo | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/form-container.md)</span> | ✔️ | Per i componenti di base, utilizza il [componente Pannello principale](https://experienceleague.adobe.com/it/docs/experience-manager-learn/cloud-service/forms/create-first-af/configure-root-panel). |
| Titolo modulo | ✔️ | ✔️ | | Per i componenti di base, utilizza il componente titolo. |
| hCaptcha | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/hcaptcha.md)</span> |  | Per i componenti di base, è possibile [collegare i moduli adattivi con hCaptcha](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/add-components-to-an-adaptive-form/integrate-adaptive-forms-turnstile) per i moduli basati su componenti di base. |
| Intestazione | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/header.md)</span> | ✔️ | |
| Schede orizzontali | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/horizontal-tabs.md)</span> | | Per i componenti base, puoi configurare le [schede con il layout in alto (schede orizzontali)](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-layout-of-an-adaptive-form/layout-capabilities-adaptive-forms#panel-layout) nelle proprietà dei componenti del pannello. |
| Immagine | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/image.md)</span> | ✔️ | |
| Pulsante Avanti | ✔️ | ✔️ | | Utilizza il [componente procedura guidata](/help/adaptive-forms/components/wizard.md) per i pulsanti Avanti e Indietro per spostarti tra più pannelli. |
| Casella numerica | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/numeric-box.md)</span> | ✔️ | |
| Stepper numerico | ✔️ | | | |
| Pannello | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/panel.md)</span> | ✔️ | |
| Telefono | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/phone.md)</span> | ✔️ | |
| Pulsante Precedente | ✔️ | ✔️ | | Utilizza il [componente procedura guidata](/help/adaptive-forms/components/wizard.md) per i pulsanti avanti e precedente per spostarti tra più pannelli. |
| Gruppo pulsanti di scelta | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/radio-button.md)</span> | ✔️ | |
| Pulsante Ripristina | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/reset-button.md)</span> | ✔️ | |
| Rivedere |  | <span style="color:blue">[✔️](/help/adaptive-forms/components/reset-button.md)</span> |  | |
| Firma scarabocchio | ✔️ | | | |
| Separatore | ✔️ | | | Usa componente WCM [Separatore](/help/components/separator.md) |
| Pulsante Invia | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/submit-button.md)</span> | ✔️ | |
| Passaggio di riepilogo | ✔️ | | | |
| Interruttore | ✔️ | <span style="color:blue"> [✔️](/help/adaptive-forms/components/adaptive-form-switch.md) | | |
| Tabella | ✔️ | | | |
| Termini e condizioni | ✔️ | ✔️ | | |
| Testo | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/text.md)</span> | ✔️ | |
| Casella di testo | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/text-box.md)</span> | ✔️ | |
| Captcha Turnstile | ✔️ | | | [Captcha Turnstile](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/add-components-to-an-adaptive-form/integrate-adaptive-forms-turnstile) è disponibile solo per i componenti di base. |
| Schede verticali | ✔️ | ✔️ | | Per i componenti di base, puoi configurare [le schede con layout a di sinistra (schede verticali)](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-layout-of-an-adaptive-form/layout-capabilities-adaptive-forms#panel-layout) nelle proprietà dei componenti del pannello |
| Procedura guidata | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/wizard.md)</span> | ✔️ | Per i componenti base, puoi configurare il [layout della procedura guidata](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-layout-of-an-adaptive-form/layout-capabilities-adaptive-forms#panel-layout) nelle proprietà dei componenti del pannello |

<!--| Password Box | ✔️ | ✔️| ✔️ | |
| Image Choice | ✔️ | | | |
-->


>[!NOTE]
>
>
> * Oltre ai componenti elencati sopra, il Blocco moduli supporta come componenti tutti i [tipi di input HTML5](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input#input_types) e [aree testo](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/textarea) validi.
> * Hai bisogno di un componente non elencato sopra? Richiedilo inviando un’e-mail a aem-forms-ea@adobe.com dall’indirizzo ufficiale.


<!-- >
* [Accordion](/help/adaptive-forms/components/accordion.md)
* [Adaptive Form Fragment](/help/adaptive-forms/components/adaptive-form-fragment.md)
* [Adaptive Form Switch](/help/adaptive-forms/components/adaptive-form-switch.md)
* [Button](/help/adaptive-forms/components/button.md)
* [Check Box Group](/help/adaptive-forms/components/checkbox-group.md)
* [Date Picker](/help/adaptive-forms/components/date-picker.md)
* [Drop-down list](/help/adaptive-forms/components/drop-down-list.md)
* [Email](/help/adaptive-forms/components/email.md)
* [Form Container](/help/adaptive-forms/components/form-container.md)
* [File Attachment](/help/adaptive-forms/components/file-attachment.md)
* [Footer](/help/adaptive-forms/components/footer.md)
* [Header](/help/adaptive-forms/components/header.md)
* [Horizontal Tabs](/help/adaptive-forms/components/horizontal-tabs.md)
* [Image](/help/adaptive-forms/components/image.md)
* [Numeric Box](/help/adaptive-forms/components/numeric-box.md)
* [Panel](/help/adaptive-forms/components/panel.md)
* [Phone](/help/adaptive-forms/components/phone.md)
* [Radio Button](/help/adaptive-forms/components/radio-button.md)
* [Adaptive Form reCAPTCHA](/help/adaptive-forms/components/adaptive-form-recaptcha.md)
* [Reset Button](/help/adaptive-forms/components/reset-button.md)
* [Submit Button](/help/adaptive-forms/components/submit-button.md)
* [Text Box](/help/adaptive-forms/components/text-box.md)
* [Text](/help/adaptive-forms/components/text.md)
* [Form Title](/help/adaptive-forms/components/form-title.md)
* [Wizard](/help/adaptive-forms/components/wizard.md)

-->

## Editor moduli di facile utilizzo

L’editor per moduli adattivi basati su Componenti core è simile a quello già utilizzato per la creazione di pagine AEM Sites. Ecco cosa ottieni:


* **Elementi e impostazioni familiari dell’interfaccia utente**: quando configuri le proprietà per i componenti modulo, la finestra di dialogo delle proprietà ha l’aspetto di quella utilizzata per i componenti core WCM. Questo consente di trovare più rapidamente le opzioni necessarie. Come i componenti core WCM, per i componenti modulo la finestra di dialogo delle proprietà viene visualizzata al centro dell’editor con schede chiare che separano le opzioni di base e avanzate, il testo guida e le informazioni di accessibilità, il tutto in un formato a schede di facile navigazione.

* **[Editor regole](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/rule-editor-core-components)**: è possibile aggiungere funzionalità logiche e dinamiche ai moduli senza la scrittura di codice. Puoi utilizzare l’editor di regole incorporato per:
   * Mostrare o nascondere i campi in base alle scelte dell’utente
   * Attivare o disattivare un oggetto
   * Impostare un valore per un oggetto
   * Eseguire calcoli
   * Impostare la proprietà di un oggetto
   * Convalidare l’immissione di dati
   * Richiamare un servizio (richiamare funzionalità esterna)
   * Utilizzare funzioni incorporate (funzioni predefinite per le attività comuni)
   * Utilizzare funzioni personalizzate (codice personalizzato per esigenze specifiche)
   * Convalidare campi e pannelli (verificare che i dati soddisfino i requisiti)
   * Convalidare il valore di un oggetto
   * Eseguire funzioni per calcolare il valore di un oggetto
   * Richiamare un modello dati del modulo (FDM) ed eseguire un’operazione
   * Aggiungere in modo dinamico stili (modificare l’aspetto in base alle condizioni)
   * Creare altre regole (azioni a catena e logica)
   * e altro ancora!

  L’editor di regole non dispone dell’editor di codice. Puoi utilizzare [funzioni personalizzate](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/create-and-use-custom-functions) per aggiungere un codice personale all’editor di regole per esigenze specifiche.



* **Moduli precompilati**: puoi compilare automaticamente alcuni campi in un modulo con i dati esistenti quando un utente lo apre. In questo modo gli utenti possono risparmiare tempo e fatica in quanto non è necessario immettere manualmente informazioni che potrebbero essere già disponibili. L’editor dei Componenti core fornisce un servizio di precompilazione OOTB per compilare i campi del modulo con l’aiuto di un modello dati del modulo. Puoi anche creare servizi di precompilazione personalizzati per scenari più complessi.

* **[Documento di record (DoR)](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/generate-document-of-record-core-components)**: un documento di record (DoR) fa riferimento a una rappresentazione formale e stampabile dei dati inviati tramite il modulo. Funge da record permanente delle informazioni immesse da un utente, fornendo un’istantanea dei dati inviati in un formato semplice, in genere un documento PDF. Puoi utilizzare l’editor per configurare facilmente un modello personalizzato o utilizzare un modello OOTB per generare un documento di record.

* **[Modello dati modulo](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/forms/integrate/use-form-data-model/using-form-data-model)**: un modello dati di moduli adattivi (FDM) funge da ponte tra i moduli adattivi e le origini dati. In sostanza, definisce la struttura e l’organizzazione dei dati che i moduli raccolgono e con cui interagiscono. Puoi utilizzare l’editor per collegare facilmente il modulo a un modello dati modulo (FDM).

* **[Invio dei moduli](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components#:~:text=Adaptive%20Form%20Submit%20Action&text=Adobe%20recommends%20using%20Core%20Components,to%20create%20standalone%20Adaptive%20Forms.&text=A%20Submit%20Action%20lets%20you,button%20on%20an%20Adaptive%20Form)**: l’invio di un modulo si riferisce al processo con cui gli utenti completano e inviano i moduli compilati. Questo attiva una serie di azioni definite nella configurazione del modulo, che determinano l’archiviazione o l’elaborazione dei dati inviati. L’editor dei moduli adattivi offre diverse opzioni per la configurazione dell’invio dei moduli. Alcune delle azioni di invio più comuni sono:

   * [Inviare e-mail](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components#:~:text=Adaptive%20Form%20Submit%20Action&text=Adobe%20recommends%20using%20Core%20Components,to%20create%20standalone%20Adaptive%20Forms.&text=A%20Submit%20Action%20lets%20you,button%20on%20an%20Adaptive%20Form.)
   * [Richiamare un flusso Power Automate](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/forms/integrate/services/forms-microsoft-power-automate-integration)
   * [Inviare a SharePoint](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-action-sharepoint)
   * [Richiamare uno scenario Workfront Fusion](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components#:~:text=Invoke%20a%20Workfront%20Fusion)
   * [Inviare mediante il modello di dati modulo (FDM)](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/forms/integrate/use-form-data-model/using-form-data-model)
   * [Inviare ad archiviazione BLOB di Azure](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components#:~:text=Submit%20to%20Azure%20Blob%20Storage)
   * [Inviare a un endpoint REST](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-action-restpoint)
   * [Inviare a OneDrive](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components#:~:text=to%20REST%20endpoint-,Submit%20to%20OneDrive,-Invoke%20an%20AEM)
   * [Richiamare un flusso di lavoro AEM](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components#:~:text=Invoke%20an%20AEM%20Workflow)


* [Componenti core per moduli adattivi nell’Editor pagina di Sites](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page): puoi abilitare e utilizzare i componenti core per moduli adattivi nell’Editor pagina di AEM e nei frammenti di esperienza di AEM per creare direttamente un’esperienza di acquisizione dati e una pagina Sites.

  >[!VIDEO](https://video.tv.adobe.com/v/3419284?quality=12&learn=on)


<!-- 
* **Preview Forms**: You can use the editor to  simulates how the form would appear on various devices like desktops, tablets, and smartphones.
-->



## Abilitare i componenti core per moduli adattivi

Abilitando i componenti core dei moduli adattivi su AEM Forms as a Cloud Service, è possibile iniziare a creare, pubblicare e distribuire componenti core basati su moduli adattivi e moduli headless utilizzando le istanze del Cloud Service di AEM Forms su più canali. Per istruzioni dettagliate sull’abilitazione dei componenti core dei moduli adattivi, consulta [Abilita i componenti core dei moduli adattivi nell’ambiente di sviluppo locale di AEM Forms as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/setup-configure-migrate/enable-adaptive-forms-core-components.html?lang=it).

Di seguito sono riportati i requisiti dei componenti core dei moduli adattivi.

| Versione di AEM | Componente aggiuntivo per AEM Forms | Componenti core dei moduli adattivi |
|---|---|---|
| AEM as a Cloud Service | Forms: registrazione digitale | [Versione 2.0.10](version.md)+ |
| AEM 6.5 | Componente aggiuntivo Forms | [Versione 1.1.12](version.md)+ |

Se la versione dell’SDK del Cloud Service di AEM è precedente alla versione 2023.02.0, [assicurati di aver abilitato il flag `prerelease` nel tuo ambiente ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/release-notes/prerelease.html?lang=it#new-features), poiché i componenti core dei moduli adattivi facevano parte della versione prerelease precedente alla versione 2023.02.0.


## Creare componenti core basati sul modulo adattivo

Puoi eseguire le seguenti azioni in entrambi gli ambienti AEM Forms as a Cloud Service o AEM 6.5 Forms:

| Azione | Versione AEM Forms |
|--------|------------------|
| Creare un modulo adattivo indipendente | [AEM Forms as Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html?lang=it) |
| Creare un modulo adattivo nella pagina AEM Sites | [AEM 6.5 Forms](https://experienceleague.adobe.com/docs/experience-manager-65/forms/adaptive-forms-basic-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=it#create-an-adaptive-form-in-sites-editor-or-experience-fragment), [AEM Forms as Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=it#create-an-adaptive-form-in-sites-editor-or-experience-fragment) |
| Creare un modulo adattivo in Frammento di esperienza AEM | [AEM 6.5 Forms](https://experienceleague.adobe.com/docs/experience-manager-65/forms/adaptive-forms-basic-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=it#create-an-adaptive-form-in-experience-fragment), [AEM Forms as Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=it#create-an-adaptive-form-in-experience-fragment) |
| Convertire un modulo adattivo in un Frammento di esperienza | [AEM 6.5 Forms](https://experienceleague.adobe.com/docs/experience-manager-65/forms/adaptive-forms-basic-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=it#convert-an-adaptive-form-in-sites-page-to-an-experience-fragment), [AEM Forms as Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=it#convert-an-adaptive-form-in-sites-page-to-an-experience-fragment) |





<!-- >, such as  [WCAG 2.1 standard](https://www.w3.org/TR/WCAG21/), to ensure that forms can be used by people with disabilities, including those using assistive technologies such as screen readers.

*   **Alignment with AEM Sites**: The Core Components are designed to be more aligned with AEM Sites, making it easier for Sites users to adopt and use them without having to learn anything new. The components use the same front-end pipeline as Sites, making it easier to style and modify their appearance. 

<!-- Additionally, the following points further illustrate this alignment:

    *   **Authoring experience inline with Page editor**: The Core Components have an authoring experience that is inline with the Sites editor, with dialogs and other experiences similar to the Page editor. This makes it easier for Sites users to create and manage forms within the familiar context of the Sites editor.

    *   **Inline form editing in Sites editor**: The Core Components allow  inline form editing within the Sites editor, avoiding the need to switch back and forth between editors. This streamlines the authoring experience and makes it easier to create and manage forms.

    *   **Inheriting Sites features in Forms**: Forms authored within a Sites page inherit the same features as Sites. This provides a seamless and integrated experience for creating and managing forms within the context of AEM Sites 
    
    <!--including Multi Site Manager, the ability to use Sites components within a form for static content, support for scheduled publish/unpublish, form translation aligned with Sites translation, versioning, and targeting -->

## Consulta anche {#see-also}

{{see-also}}
