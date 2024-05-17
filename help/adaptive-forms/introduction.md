---
title: Introduzione ai componenti core dei moduli adattivi in AEM
description: Crea esperienze di iscrizione accattivanti (moduli) utilizzando la flessibilità dei componenti core dei moduli adattivi e forniscile con l’aiuto di Adobe Experience Manager.
role: Architect, Developer, Admin, User
exl-id: 6d0f2845-bbb8-4488-a254-b69d7a6290b1
source-git-commit: 63b4b59c43ffef10a036db3a639a6d5fa75a4e89
workflow-type: tm+mt
source-wordcount: '2215'
ht-degree: 47%

---

# Componenti core dei moduli adattivi  {#adaptive-forms-core-components-introduction}

Utilizzando i componenti core Adaptive Forms in Adobe Experience Manager, puoi creare esperienze di registrazione coinvolgenti.

## Componenti core {#overview}

In Adobe Experience Manager (AEM), i componenti sono i blocchi predefiniti utilizzati per creare pagine e moduli. Forniscono agli autori un modo semplice e potente per creare e gestire i contenuti, fornendo allo stesso tempo agli sviluppatori la flessibilità e l’estensibilità necessarie per creare componenti personalizzati. Questi sono progettati per velocizzare i tempi di sviluppo e ridurre i costi di manutenzione per siti web e moduli, per essere flessibili e possono essere facilmente personalizzati in base alle esigenze specifiche di un sito web e di un modulo.

I componenti core sono inoltre progettati per essere reattivi e supportano un’ampia gamma di dispositivi, tra cui desktop, tablet e smartphone. Inoltre, rispettano gli standard web e le best practice più recenti, rendendoli una soluzione solida e affidabile per la creazione di contenuti web.

Nel complesso, i componenti core sono uno strumento essenziale per la creazione e la gestione dei contenuti web in AEM, potente e flessibile, che consente di ridurre i tempi di sviluppo e i costi di manutenzione e offire un’ esperienza utente ottimale a coloro che visitano il sito web.

## Componenti core dei moduli adattivi

I componenti core dei moduli adattivi sono un set di 24 componenti open-source compatibili con BEM creati sulle basi dei componenti core di Web Content Management di Adobe Experience Manager. Sono progettati appositamente per la creazione di moduli adattivi, ossia moduli che si adattano al dispositivo, al browser e alle dimensioni dello schermo dell’utente.

Questi componenti possono essere utilizzati per creare esperienze eccezionali di acquisizione e registrazione dei dati fornendo un’ampia gamma di opzioni per i campi modulo, compresi campi di testo, caselle di controllo, menu a discesa e altro ancora. Includono anche funzioni quali convalida, logica condizionale e progettazione reattiva, che possono essere utilizzate per creare moduli intuitivi e facili da usare.

Inoltre, poiché questi componenti sono open-source, gli sviluppatori possono personalizzare ed estendere facilmente i componenti in base alle esigenze specifiche della propria organizzazione. Questi componenti sono basati sulla metodologia BEM, che ne garantisce la scalabilità e la manutenibilità.

![immagine del modulo adattivo](assets/sample-adaptive-form.png)

## Funzioni {#features}

|  |  |
|---|---|
| Pronti per la produzione | I componenti core dei moduli adattivi sono 24 componenti WCM affidabili. |
| Compatibile con cloud | Disponibile per [AEM Forms as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/home.html?lang=it). |
| Versatili | I componenti rappresentano concetti generici con i quali gli autori di moduli possono assemblare quasi tutti i layout. |
| Configurabili | I [criteri di contenuto](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/full-stack/components-templates/templates.html?lang=it#content-policies) a livello di modello definiscono quali funzioni sono utilizzabili e quali no. |
| Accessibili | Forniscono etichette ARIA, supportano la navigazione da tastiera e testo per le tecnologie per l’accessibilità, come gli assistenti vocali. |
| Con applicazione tema | I componenti implementano il [sistema di stili](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/features/style-system.html?lang=it) e il markup segue le [convenzioni BEM CSS](https://getbem.com/). |
| Personalizzabili | Diversi modelli consentono una facile personalizzazione, dalla modficia del codice HTML al riutilizzo avanzato delle funzionalità. |
| Controllo delle versioni | I [criteri di controllo delle versioni](https://github.com/adobe/aem-core-wcm-components/wiki/Versioning-policies) garantiscono che i Componenti core non blocchino il tuo sito in fase di miglioramento di elementi che potrebbero influire su di te. |
| Open source | Se qualcosa non va come dovrebbe, suggerisci miglioramenti. |

<!-- comply with [WCAG 2.1 standard](https://www.w3.org/TR/WCAG21/), -->


## Vantaggi {#benefits}

Le esperienze di acquisizione dei dati sono fondamentali per la generazione e la registrazione dei lead e i componenti core dei moduli adattivi offrono una soluzione potente per la creazione di moduli ottimizzati per l’acquisizione dei dati. Alcuni dei motivi per utilizzare i componenti core per creare queste esperienze sui componenti di base sono:

* **[Disponibilità su GitHub](https://github.com/adobe/aem-core-forms-components)**: i componenti core Forms adattivi dell’AEM sono open-source e sono disponibili su GitHub, insieme alla relativa documentazione completa. In questo modo gli sviluppatori possono comprendere più facilmente i componenti e il loro funzionamento e contribuire al loro sviluppo. Anche il sito web [aemcomponents.dev](https://www.aemcomponents.dev/) è una risorsa preziosa, in cui gli sviluppatori possono vedere i componenti in azione e accedere alla documentazione dettagliata.

* **[Modello BEM per la creazione di stili](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/using-themes-in-core-components)**: i Componenti core seguono il modello BEM (Block Element Modifier) per lo stile, che è una metodologia consolidata e ampiamente utilizzata per organizzare i CSS. In questo modo gli sviluppatori possono comprendere più facilmente come sono organizzati gli stili e come modificarli in base alle proprie esigenze specifiche.

* **Nessuna dipendenza dalle librerie di terze parti**: uno dei vantaggi dei componenti core è che non hanno dipendenza da librerie JavaScript di terze parti, inclusi JQuery e Underscore. Questo rende i componenti più veloci e leggeri, nonché più facili da integrare in un’implementazione AEM esistente.

* **Focus su prestazioni e accessibilità**: i componenti core sono progettati tenendo presente le prestazioni e l’accessibilità, che si riflettono nei loro punteggi Google Lighthouse e web vitals elevati. Questo rende più facile per gli sviluppatori creare pagine web accessibili e dalle prestazioni elevate, che è sempre più importante nell’attuale panorama digitale.

* **Componenti modulo nel modello e nei temi di Sites 30**: i componenti core supportano i componenti del modulo nel modello e nei temi di Sites 30, facilitando agli sviluppatori la creazione e la personalizzazione dei moduli all’interno di AEM.

* **[Più semplice da personalizzare con gli stili](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/using-themes-in-core-components)**: i Componenti core hanno uno stile più semplice rispetto ai componenti di base corrispondenti. Il processo di creazione del tema è simile a Sites, con la possibilità di ereditare lo stesso tema/CSS dalla pagina Sites principale. Inoltre, il modello BEM per lo stile facilita la comprensione e la modifica degli stili.

* **Accessibilità**: i componenti core adattivi di Forms supportano gli standard e le linee guida di accessibilità per garantire che i moduli possano essere utilizzati da persone con disabilità, incluse quelle che utilizzano tecnologie per l’accessibilità, come gli assistenti vocali.

* **[Controllo delle versioni](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/add-comments-annotations-versioning-adaptive-form-core-components)**: puoi creare e gestire più versioni di un Forms adattivo basato su Componenti core, partecipare a discussioni collaborative tramite commenti e allegare annotazioni a componenti modulo specifici, in modo da migliorare l’esperienza complessiva di creazione del modulo.

## Confronto dei componenti core, dei componenti di base e dei componenti del blocco di modulo {#components}

La versione corrente dell’AEM contiene i seguenti Componenti core: [Componenti di base](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/create-an-adaptive-form-on-forms-cs/introduction-forms-authoring#component-toolbar), e [Componenti blocco modulo (Edge Delivery Services)](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/edge-delivery/build-forms/forms-references/form-components).

| Componenti | Componenti di base | Componenti core | Componenti blocco modulo | Informazioni aggiuntive |
|------------|:---------------------:|:---------------:|:---------------------:|-----------------------|
| Blocco Adobe Sign | ✔️ | | | [Integrazione con Adobe Sign](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/integrate/services/adobe-sign-integration-adaptive-forms#adobe-acrobat-sign-for-government) è disponibile solo per i componenti di base. |
| Pannello a soffietto | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/accordion.md)</span> | | Per i componenti di base, puoi configurare il layout del Pannello a soffietto in [proprietà del componente pannello](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-layout-of-an-adaptive-form/layout-capabilities-adaptive-forms#panel-layout). |
| Frammento di modulo adattivo | ✔️ | ✔️ | | Per i componenti di base, puoi: [aggiungi un frammento](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/forms/adaptive-forms-basic-authoring/adaptive-form-fragments#insert-a-fragment-in-an-adaptive-form) dal browser Risorse. |
| reCAPTCHA per modulo adattivo | ✔️ | ✔️ | ✔️ | Per i componenti Foundation, utilizza il componente Captcha per [aggiungere Google reCaptcha a un modulo](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/add-components-to-an-adaptive-form/captcha-adaptive-forms#google-reCAPTCHA). |
| Pulsante | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/button.md)</span> | ✔️ | |
| Captcha | ✔️ | | | Per i componenti Foundation, utilizza il componente Captcha per [aggiungere Google reCaptcha a un modulo](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/add-components-to-an-adaptive-form/captcha-adaptive-forms#google-reCAPTCHA). |
| Grafico | ✔️ | | | |
| Casella di controllo | ✔️ | ✔️ | | |
| Gruppo di caselle di selezione | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/checkbox-group.md)</span> | ✔️ | Per i componenti di base, utilizza il componente Casella di controllo per aggiungere più caselle di controllo |
| Campo immissione data | ✔️ | | | Per i Componenti core, utilizza [selezione data](/help/adaptive-forms/components/date-picker.md) componente. È inoltre possibile aggiungere [casella di testo](/help/adaptive-forms/components/text-box.md) o [casella numerica](/help/adaptive-forms/components/numeric-box.md) componenti per acquisire il giorno, il mese e l’anno. |
| Selettore data | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/date-picker.md)</span> | ✔️ | |
| Elenco a discesa | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/drop-down-list.md)</span> | ✔️ | |
| E-mail | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/email-input.md)</span> | ✔️ | |
| Allegato file | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/file-attachment.md)</span> | ✔️ | |
| Elenco dei file allegati | ✔️ | | | |
| Piè di pagina | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/footer.md)</span> | ✔️ | |
| Segnaposto Nota a piè di pagina | ✔️ | | | |
| Contenitore modulo | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/form-container.md)</span> | ✔️ | Per i componenti di base, utilizza [Componente pannello principale](https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/forms/create-first-af/configure-root-panel). |
| Titolo modulo | ✔️ | ✔️ | | Per i componenti di base, utilizza il componente Titolo. |
| Intestazione | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/header.md)</span> | ✔️ | |
| Schede orizzontali | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/horizontal-tabs.md)</span> | | Per i componenti di base, puoi configurare [schede nel layout superiore (schede orizzontali)](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-layout-of-an-adaptive-form/layout-capabilities-adaptive-forms#panel-layout) nelle proprietà del componente pannello. |
| Immagine | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/image.md)</span> | ✔️ | |
| Scelta dell&#39;immagine | ✔️ | | | |
| Pulsante Successivo | ✔️ | ✔️ | | Utilizza il [componente procedura guidata](/help/adaptive-forms/components/wizard.md) per spostare i pulsanti successivo e precedente tra più pannelli. |
| Casella numerica | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/numeric-box.md)</span> | ✔️ | |
| Stepper numerico | ✔️ | | | |
| Pannello | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/panel.md)</span> | ✔️ | |
| Casella password | ✔️ | | ✔️ | |
| Telefono/Telefono | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/telephone-input.md)</span> | ✔️ | |
| Pulsante Indietro | ✔️ | | | Utilizza il [componente procedura guidata](/help/adaptive-forms/components/wizard.md) per spostare i pulsanti successivo e precedente tra più pannelli. |
| Pulsante di scelta | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/radio-button.md)</span> | | |
| Gruppo pulsante di opzione | | | ✔️ | |
| Pulsante Ripristina | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/reset-button.md)</span> | ✔️ | |
| Firma a mano | ✔️ | | | |
| Separatore | ✔️ | | | |
| Pulsante Invia | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/submit-button.md)</span> | ✔️ | |
| Passaggio di riepilogo | ✔️ | | | |
| Interruttore | ✔️ | <span style="color:blue"> [✔️](/help/adaptive-forms/components/switch.md) | | |
| Tabella | ✔️ | | | |
| Termini e condizioni | ✔️ | ✔️ | | |
| Testo | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/text.md)</span> | ✔️ | |
| Casella di testo | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/text-box.md)</span> | ✔️ | |
| Titolo | ✔️ | | | Per i Componenti core, utilizza [Titolo modulo](/help/adaptive-forms/components/title.md) componente. |
| Schede verticali | ✔️ | ✔️ | | Per i componenti di base, puoi configurare [schede a sinistra (schede verticali)](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-layout-of-an-adaptive-form/layout-capabilities-adaptive-forms#panel-layout) proprietà del componente nel pannello |
| Procedura guidata | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/wizard.md)</span> | ✔️ | Per i componenti di base, puoi configurare [layout procedura guidata](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-layout-of-an-adaptive-form/layout-capabilities-adaptive-forms#panel-layout) proprietà del componente nel pannello |




>[!NOTE]
>
>
> * Oltre ai componenti elencati in precedenza, il blocco Forms supporta tutti i componenti validi [Tipi di input HTML5](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input#input_types) e [area di testo](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/textarea) come componenti.
> * Hai bisogno di un componente non elencato sopra? Richiedilo inviando un&#39;e-mail a aem-forms-ea@adobe.com dal tuo indirizzo ufficiale.


<!-- >
* [Accordion](/help/adaptive-forms/components/accordion.md)
* [Button](/help/adaptive-forms/components/button.md)
* [Check Box Group](/help/adaptive-forms/components/checkbox-group.md)
* [Date Picker](/help/adaptive-forms/components/date-picker.md)
* [Drop-down list](/help/adaptive-forms/components/drop-down-list.md)
* [Email-input](/help/adaptive-forms/components/email-input.md)
* [Form Container](/help/adaptive-forms/components/form-container.md)
* [File Attachment](/help/adaptive-forms/components/file-attachment.md)
* [Footer](/help/adaptive-forms/components/footer.md)
* [Header](/help/adaptive-forms/components/header.md)
* [Horizontal Tabs](/help/adaptive-forms/components/horizontal-tabs.md)
* [Image](/help/adaptive-forms/components/image.md)
* [Numeric Box](/help/adaptive-forms/components/numeric-box.md)
* [Panel](/help/adaptive-forms/components/panel.md)
* [Radio Button](/help/adaptive-forms/components/radio-button.md)
* [Reset Button](/help/adaptive-forms/components/reset-button.md)
* [Submit Button](/help/adaptive-forms/components/submit-button.md)
* [Telephone input](/help/adaptive-forms/components/telephone-input.md)
* [Text Box](/help/adaptive-forms/components/text-box.md)
* [Text](/help/adaptive-forms/components/text.md)
* [Title](/help/adaptive-forms/components/title.md)
* [Wizard](/help/adaptive-forms/components/wizard.md)

-->

## Editor di moduli di facile utilizzo

L’editor per Forms adattivo basato su Componenti core è simile a quello già utilizzato per la creazione di pagine AEM Sites. Ecco cosa si ottiene:


* **Elementi e impostazioni dell’interfaccia utente familiari**: quando configuri le proprietà per i componenti modulo, viene visualizzata una finestra di dialogo delle proprietà simile a quelle utilizzate per i componenti core WCM. Questo consente di trovare più rapidamente le opzioni necessarie. Come i componenti core WCM, per i componenti modulo la finestra di dialogo delle proprietà viene visualizzata al centro dell’editor con schede chiare che separano le opzioni di base e avanzate, il testo della guida e le informazioni di accessibilità, il tutto in un formato di schede per facilitarne la navigazione.

* **[Editor regole](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/rule-editor-core-components)**: è possibile aggiungere funzionalità logiche e dinamiche ai moduli senza scrivere codice. Puoi utilizzare l’editor di regole integrato per:
   * Mostrare o nascondere i campi in base alle scelte degli utenti
   * Attivare o disattivare un oggetto
   * Imposta un valore per un oggetto
   * Eseguire calcoli
   * Impostare la proprietà di un oggetto
   * Convalida immissione dati
   * Richiama un servizio (richiamare funzionalità esterne)
   * Utilizzare funzioni incorporate (funzioni predefinite per le attività comuni)
   * Utilizzare funzioni personalizzate (codice personalizzato per esigenze specifiche)
   * Convalidare campi e pannelli (verificare che i dati soddisfino i requisiti)
   * Convalidare il valore di un oggetto
   * Eseguire funzioni per calcolare il valore di un oggetto
   * Richiama un servizio FDM (Form Data Model) ed esegui un’operazione
   * Aggiunta dinamica di stili (modifica dell’aspetto in base alle condizioni)
   * Creare altre regole (azioni a catena e logica)
   * e altro ancora!

  L’editor di regole non dispone dell’editor di codice. È possibile utilizzare [funzioni personalizzate](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/create-and-use-custom-functions) per aggiungere all’editor di regole il codice per esigenze specifiche.



* **Moduli precompilati**: è possibile compilare automaticamente alcuni campi di un modulo con i dati esistenti quando un utente lo apre. In questo modo gli utenti possono risparmiare tempo e fatica, eliminando la necessità di immettere manualmente informazioni che potrebbero essere già disponibili. L’editor dei componenti core fornisce un servizio di precompilazione OOTB per compilare i campi del modulo con l’aiuto di un modello di dati del modulo. Puoi anche creare servizi di preriempimento personalizzati per scenari più complessi.

* **[Documento record (DoR)](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/generate-document-of-record-core-components)**: un documento di record (DoR) fa riferimento a una rappresentazione formale e stampabile dei dati inviati tramite il modulo. Funge da record permanente delle informazioni immesse da un utente, fornendo un’istantanea dei dati inviati in un formato semplice, in genere un documento PDF. Puoi utilizzare l’editor per configurare facilmente un modello personalizzato o un modello OOTB per generare un documento record.

* **[Modello dati modulo](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/integrate/use-form-data-model/using-form-data-model)**: un modello dati di Forms adattivo (FDM) funge da ponte tra il Forms adattivo e le origini dati. In sostanza, definisce la struttura e l’organizzazione dei dati che i moduli raccolgono e con cui interagiscono. È possibile utilizzare l’editor per collegare facilmente il modulo a un Forms Data Model (FDM).

* **[Invio modulo](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components#:~:text=Adaptive%20Form%20Submit%20Action&amp;text=Adobe%20recommends%20using%20Core%20Components,to%20create%20standalone%20Adaptive%20Forms.&amp;text=A%20Submit%20Action%20lets%20you,button%20on%20an%20Adaptive%20Form)**: l’invio di un modulo si riferisce al processo con cui gli utenti compilano e inviano i moduli compilati. Questo attiva una serie di azioni definite nella configurazione del modulo, che determinano l’archiviazione o l’elaborazione dei dati inviati. L’editor di Forms adattivo offre diverse opzioni per la configurazione dell’invio dei moduli. Alcune delle azioni di invio più comuni sono:

   * [Invia e-mail](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components#:~:text=Adaptive%20Form%20Submit%20Action&amp;text=Adobe%20recommends%20using%20Core%20Components,to%20create%20standalone%20Adaptive%20Forms.&amp;text=A%20Submit%20Action%20lets%20you,button%20on%20an%20Adaptive%20Form.)
   * [Richiama un flusso Power Automate](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/integrate/services/forms-microsoft-power-automate-integration)
   * [Invia a SharePoint](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-action-sharepoint)
   * [Richiama Workfront Fusion](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components#:~:text=Invoke%20a%20Workfront%20Fusion)
   * [Invia utilizzando il modello dati modulo (FDM)](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/integrate/use-form-data-model/using-form-data-model)
   * [Invia ad Azure Blob Storage](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components#:~:text=Submit%20to%20Azure%20Blob%20Storage)
   * [Invia all’endpoint REST](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-action-restpoint)
   * [Invia a OneDrive](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components#:~:text=to%20REST%20endpoint-,Submit%20to%20OneDrive,-Invoke%20an%20AEM)
   * [Richiama un flusso di lavoro AEM](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components#:~:text=Invoke%20an%20AEM%20Workflow)


* [Componenti core Forms adattivi nell’editor di pagine Sites](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page): puoi abilitare e utilizzare i componenti core Forms adattivi nell’Editor pagina AEM e i Frammenti esperienza AEM per creare direttamente un’esperienza di acquisizione dati e creare una pagina Sites.

  >[!VIDEO](https://video.tv.adobe.com/v/3419284?quality=12&learn=on)


<!-- 
* **Preview Forms**: You can use the editor to  simulates how the form would appear on various devices like desktops, tablets, and smartphones.
-->



## Abilita componenti core Forms adattivi

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
