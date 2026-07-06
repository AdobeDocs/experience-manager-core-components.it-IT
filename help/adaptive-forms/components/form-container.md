---
title: Componente core dei moduli adattivi - Contenitore di moduli
description: Aggiungere un modulo adattivo a una pagina web.
role: Developer, Admin, User
exl-id: 03c4cf7c-51d6-4850-a566-1c0514d52dab
TQID: https://experienceleague.adobe.com/kMG6SKHisAUmKhOh9AFLI8NG6w0vH7tP4XimBKAMo-I
product_v2: id: c45915cf-e157-4af7-a80d-97b905bcb3a5id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: e2c1b6d3-bb7e-4fe8-8c72-f7b403298e91
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 0af65c80f9cc58c4ba48d5b3dc7a026820bd2833
workflow-type: tm+mt
source-wordcount: 2555
ht-degree: 64%

---

# Contenitore modulo {#form-container-adaptive-forms-core-component}

<span class="preview"> In questo articolo vengono illustrate le funzionalità **Bozze** e **Supporto menu Hamburger**, che sono funzionalità precedenti al rilascio. La funzione pre-release è accessibile solo tramite il [canale pre-release](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/release-notes/prerelease.html?lang=it#new-features).</span>

I moduli consentono ai visitatori di un sito web di interagire con il sito web fornendo informazioni preziose, che possono aumentare il coinvolgimento e la soddisfazione degli utenti. Un contenitore di moduli adattivi in Adobe Experience Manager (AEM) Sites consente ai proprietari di siti web di aggiungere facilmente i moduli alle proprie pagine. Questo rende più facile la comunicazione tra i visitatori di un sito web e il proprietario o l’organizzazione del sito web, offrendo ai visitatori un modo semplificato per fornire feedback, rispondere ai sondaggi e completare altre azioni

{{traditional-aem}}

## Utilizzo {#reasons-to-use-forms-container}

Ci sono diversi motivi per i quali viene aggiunto un modulo a un sito web:
- **Raccolta dati**: i moduli possono essere utilizzati per raccogliere dati dai visitatori di un sito web per vari scopi, come ricerche di mercato, analisi del comportamento degli utenti e altro ancora.

- **Generare lead**: un modulo può essere utilizzato per raccogliere informazioni dai potenziali clienti, ad esempio nome e indirizzo e-mail, per generare lead per attività di vendita e marketing.

- **E-commerce**: i moduli possono essere utilizzati per lo shopping online, poiché consentono ai clienti di effettuare ordini e pagamenti su un sito web.

- **Contatto**: un modulo di contatto consente ai visitatori di un sito web di raggiungere facilmente il proprietario o l’organizzazione del sito web.

- **Indagini e sondaggi**: i moduli possono essere utilizzati per raccogliere feedback e opinioni dai visitatori di un sito attraverso indagini di marketing e sondaggi.

- **Iscriversi ad eventi**: i moduli possono essere utilizzati per partecipare ad eventi, poiché consentono ai visitatori di un sito web di iscriversi ad eventi o webinar.

- **Abbonamenti**: i moduli possono essere utilizzati per sottoscrivere un abbonamento a un sito web, poiché consentono ai visitatori di iscriversi a una newsletter o ad altre comunicazioni regolari.

- **Autenticazione utente**: i moduli possono essere utilizzati per l’autenticazione degli utenti, poiché consentono ai visitatori di un sito web di creare account e di accedere a contenuti o funzionalità esclusive.

- **Aumentare il tasso di conversione**: un modulo ben progettato può aumentare il tasso di conversione rendendo più semplice per gli utenti completare un’azione desiderata, ad esempio acquistare un prodotto o iscriversi a un servizio.

## Versione e compatibilità {#version-and-compatibility}

Il componente core Pannello a soffietto dei moduli adattativi è stato rilasciato a febbraio 2023 come parte dei Componenti core 2.0.4 per Cloud Service e dei Componenti core 1.1.12 per AEM Forms 6.5.16.0 o versioni successive. Di seguito è riportata una tabella che mostra tutte le versioni supportate, la compatibilità AEM e i collegamenti alla documentazione corrispondente:

| Versione del componente | AEM as a Cloud Service | AEM 6.5.16.0 Forms o versioni successive |
|---|---|---|
| v1 | Compatibile con <br>[versione 2.0.4](/help/adaptive-forms/version.md) e successive | Compatibile con <br>[versione 1.1.12](/help/adaptive-forms/version.md) e successive, ma precedenti a 2.0.0. |

Per informazioni sulle versioni dei componenti core, consulta il documento [Versioni dei componenti core](/help/adaptive-forms/version.md).
<!--
## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). 
-->

## Dettagli tecnici {#technical-details}

Per informazioni aggiornate sul componente core contenitore di moduli adattivi, consulta la documentazione tecnica su [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/container/v1/container). Per ulteriori informazioni sullo sviluppo dei componenti core, consulta la [Documentazione per gli sviluppatori dei componenti core](/help/developing/overview.md).

## Finestra di dialogo per la configurazione {#configure-dialog}

È possibile personalizzare facilmente l’esperienza del contenitore di moduli per i visitatori tramite la finestra di dialogo Configura. È, inoltre, possibile definire le opzioni del contenitore di moduli con facilità per un’esperienza utente perfetta.

### Scheda Base {#basic-tab}

![Scheda Base](/help/adaptive-forms/assets/formcontainer_basictab1.png)

- **Titolo** : con il relativo titolo è possibile identificare facilmente un componente in un modulo e, per impostazione predefinita, il titolo viene visualizzato sopra il componente. Se non aggiungi un titolo, al posto del testo del titolo viene visualizzato il nome del componente.

- **Servizi di precompilazione**: questa opzione consente all’utente di selezionare un servizio di precompilazione per il recupero dei dati durante il rendering del modulo adattivo. Ulteriori informazioni su [come creare e configurare un servizio di precompilazione](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/prepopulate-adaptive-form-fields.html?lang=it#aem-forms-custom-prefill-service).

- **Ruolo**: il ruolo è un attributo HTML utilizzato per specificare lo scopo di un elemento HTML per tecnologie di assistenza come le utilità per la lettura dello schermo. L’attributo ruolo viene utilizzato per fornire ulteriore contesto e significato semantico a un elemento, facilitando l’interpretazione e la lettura del contenuto da parte delle utilità per la lettura dello schermo per l’utente. Ad esempio, in AEM Forms, l’etichetta di un campo modulo potrebbe avere il ruolo di “etichetta” e il relativo campo di input potrebbe avere il ruolo di “casella di testo”. Questo permette all’assistente vocale di comprendere la relazione tra l’etichetta e il campo di input, e di leggerli in modo corretto all’utente.

- **Categoria Libreria client**: l’utente può configurare una libreria JavaScript personalizzata per un modulo adattivo. Si consiglia di mantenere solo le funzioni riutilizzabili nella libreria, che dipendono dalle librerie di terze parti jquery e underscore.js.A volte, se sono presenti **regole di convalida complesse**, lo script di convalida esatto si trova nelle funzioni personalizzate e gli utenti chiamano tali funzioni personalizzate dall’espressione di convalida del campo. Per rendere nota e disponibile questa libreria di funzioni personalizzata durante l’esecuzione delle convalide lato server, l’utente del modulo può configurare il nome della libreria client AEM nella scheda **[!UICONTROL Base]** delle proprietà del contenitore per modulo adattivo.L’utente può configurare una libreria JavaScript personalizzata per modulo adattivo. Si consiglia di mantenere solo le funzioni riutilizzabili nella libreria, che dipendono dalle librerie di terze parti jquery e underscore.js.

- **Abilita il menu hamburger per la visualizzazione mobile** - Seleziona la casella di controllo per integrare un menu hamburger nel modulo per la visualizzazione mobile. Rappresentato da tre linee orizzontali sovrapposte verticalmente, questo menu fornisce un display chiaro e ordinato per i pannelli su dispositivi più piccoli, in particolare sui dispositivi mobili. Per ulteriori informazioni sul menu hamburger, fare riferimento alla sezione [Ulteriori informazioni sul menu hamburger](#learn-more-about-the-hamburger-menu).


### Scheda Modello dati {#data-model-tab}

![Scheda Modello dati](/help/adaptive-forms/assets/formcontainer_fdmtab.png)

È possibile utilizzare il modello dati modulo per collegare un modulo a un’origine dati per inviare e ricevere dati in base alle azioni degli utenti. È possibile anche collegare un modulo a uno schema JSON per ricevere i dati inviati in un formato predefinito. In base al requisito, connetti il modulo a uno schema JSON o a un modello dati modulo:
- **Nessuno** - Non associare il modulo a un modello dati.
- **Schema** - Connetti il modulo a uno schema JSON caricato nell&#39;ambiente.
- **Modello dati modulo** - Connetti il modulo a un modello dati modulo per l&#39;integrazione con origini dati esterne.
- **Connettore** - Connetti il modulo a un&#39;origine dati basata su connettore.
- **Modelli di modulo** - Associa il modulo a un modello di modulo.

### Scheda Bozze {#drafts-tab}

![Scheda Bozze](/help/adaptive-forms/assets/formcontainer_autosavetab.png)

- **Salvataggio automatico delle bozze**: seleziona la casella di controllo **Salvataggio automatico delle bozze** per abilitare il salvataggio dei moduli come bozze.
- **Salva preferenza**: configura **Salva preferenza** come **Salva bozze a intervalli regolari**, per salvare automaticamente il modulo dopo un intervallo di tempo specifico.
  **Salva intervallo di frequenza (secondi)**: specifica l’intervallo di tempo (in secondi) per impostare la durata di tempo che deve trascorrere tra ogni salvataggio automatico del modulo, pari all’intervallo definito.

### Scheda Invio {#submission-tab}

Gli utenti possono configurare azioni diverse per gli invii di moduli adattivi.

- **All&#39;invio** - Scegliere **Reindirizza all&#39;URL** per inviare gli utenti del modulo a una pagina configurata dopo l&#39;invio oppure **Mostra messaggio** per visualizzare un messaggio di conferma nel modulo.

- **URL/percorso di reindirizzamento**: questa opzione consente agli utenti di configurare una pagina per ciascun modulo, a cui verranno reindirizzati gli utenti dei moduli dopo l’invio di un modulo adattivo. Fai clic qui per ulteriori informazioni su [come configurare le pagine di reindirizzamento](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-redirect-page.html?lang=it).

![Scheda Invio](/help/adaptive-forms/assets/formcontainer_submissiontab.png)

- **Mostra Messaggio**: questa opzione consente agli utenti di aggiungere un messaggio da visualizzare quando il modulo adattivo viene inviato correttamente. Il testo predefinito viene incluso nella finestra di dialogo e può essere modificato dall’utente. La finestra di dialogo Mostra messaggio supporta gli strumenti di formattazione RTF che consentono agli utenti di formattare il testo aggiunto.

![Scheda Mostra Messaggio](/help/adaptive-forms/assets/formconatiner_showmessage.png)

- **Azione di invio**: un’azione di invio viene attivata quando l’utente fa clic sul pulsante Invia in un modulo adattivo. Gli utenti possono selezionare azioni di Invio dall’elenco a discesa supportato come predefinito. Scopri come [configurare un’azione di invio nella scheda Invio](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html?lang=it#supporting-custom-functions-in-validation-expressions-br).

- **Configurazione azione** - Configura le mappature per il passaggio dei valori dei campi come parametri di richiesta della pagina di ringraziamento.

- **Abilita richiesta POST** - Selezionare questa opzione per inviare i dati del modulo utilizzando una richiesta HTTP POST.

### Scheda Documento record {#document-of-record-tab}

![Scheda Documento record](/help/adaptive-forms/assets/formcontainer_dortab.png)

Un [documento di record (DoR)](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/generate-document-of-record-core-components) è una rappresentazione formale e stampabile dei dati inviati tramite il modulo. Utilizzare la scheda **Documento record** per configurare la modalità di generazione di un documento record quando un utente invia il modulo:

- **Nessuno** - Non generare un documento di record per il modulo.
- **Associa modello modulo come modello del documento record**. Utilizzare un modello di modulo esistente come modello DoR.
- **Genera documento record** - Genera automaticamente un documento record in base ai dati del modulo inviati.
- **Escludi allegati da documento record** - Selezionare questa opzione per omettere gli allegati dal DoR generato.

## Finestra di dialogo per la progettazione {#design-dialog}

La finestra di dialogo per la progettazione consente di definire e gestire gli stili CSS per il componente Contenitore modulo.

### Scheda Componenti Consentiti {#allowed-components-tab}

![Scheda Componente consentito della finestra di dialogo per la progettazione](/help/adaptive-forms/assets/formcontainer-allowedcomponents.png)

La scheda **Componenti consentiti** permette all’editor dei modelli di impostare i componenti che possono essere aggiunti come elementi ai pannelli nel componente nell’editor di moduli adattivi.

### Scheda Componenti predefiniti {#default-components-tab}

![Scheda Componente predefinito della finestra di dialogo per la progettazione](/help/adaptive-forms/assets/formcontainer-defaultcomponents.png)

La scheda **Componenti predefiniti** consente all’editor di modelli di specificare i componenti visibili per impostazione predefinita come elementi nel componente Contenitore modulo nell’editor moduli adattivi.

### Scheda Impostazioni reattive {#responsive-tab}

![Scheda Impostazioni reattive della finestra di dialogo per la progettazione](/help/adaptive-forms/assets/formcontainer-responsivestyle.png)

La scheda **Impostazioni reattive** consente all’editor di modelli di specificare il numero di colonne nella griglia all’interno del componente Contenitore modulo nell’editor di moduli adattivi.

### Scheda Stili {#styles-tab}

Il componente core Allegato file dei moduli adattivi supporta il [Sistema di stili](/help/get-started/authoring.md#component-styling) di AEM.

![Finestra di dialogo per la progettazione](/help/adaptive-forms/assets/formcontainer-styletab.png)

- **Classi CSS predefinite**: è possibile fornire una classe CSS predefinita per il componente core contenitore del modulo nei moduli adattivi.

- **Stili consentiti**: puoi definire gli stili fornendo un nome e la classe CSS che rappresenta lo stile. Ad esempio, puoi creare uno stile denominato “testo in grassetto” e fornire la classe CSS “spessore carattere: grassetto”. Puoi utilizzare o applicare questi stili a un modulo adattivo nell’editor di moduli adattivi. Per applicare uno stile, nell’editor dei moduli adattivi, seleziona il componente a cui applicare lo stile, passa alla finestra di dialogo delle proprietà e seleziona lo stile desiderato dall’elenco a discesa **Stili**. Per aggiornare o modificare gli stili, è sufficiente tornare alla finestra di dialogo per la progettazione, aggiornare gli stili nella scheda Stili e salvare le modifiche.

### Scheda Proprietà personalizzate

![Finestra di dialogo Proprietà personalizzate](/help/adaptive-forms/assets/formcontainer-custompropertiestab.png)

Le proprietà personalizzate consentono di associare attributi personalizzati (coppie chiave-valore) a un componente core del modulo adattivo utilizzando il modello per moduli. Le proprietà personalizzate vengono riflesse nella sezione delle proprietà della rappresentazione headless del componente. Consentono di creare un comportamento di modulo dinamico che si adatta in base ai valori degli attributi personalizzati. Ad esempio, gli sviluppatori possono progettare diverse rappresentazioni di un componente moduli headless su piattaforme mobili, desktop o web, migliorando in modo significativo l’esperienza utente su un’ampia gamma di dispositivi.

- **Nome gruppo**: puoi fornire un nome per identificare il gruppo di proprietà personalizzate. È possibile aggiungere, eliminare o ridisporre più gruppi di proprietà personalizzate. Dopo aver aggiunto il gruppo di proprietà personalizzate, puoi visualizzare le seguenti opzioni:

   - **Coppie chiave-valore**: puoi aggiungere più nomi e valori della proprietà personalizzata facendo clic sul pulsante **Aggiungi** per ogni gruppo di proprietà personalizzate.

   - **Elimina**: tocca o fai clic per eliminare il nome e il valore della proprietà personalizzata.

   - **Ridisponi**: tocca o fai clic e trascina per ridisporre l’ordine del nome e del valore della proprietà personalizzata.

## Ulteriori informazioni sul menu hamburger {#learn-more-about-the-hamburger-menu}

Un menu hamburger, spesso indicato come menu mobile o cassetto di navigazione, è un elemento di design popolare nelle interfacce utente mobili. Dispone di tre linee orizzontali impilate verticalmente, che assomigliano a un hamburger. La progettazione consente di risparmiare spazio sullo schermo nascondendo le opzioni di navigazione secondaria fino a quando non sono necessarie, in particolare su dispositivi più piccoli come i dispositivi mobili. AEM forms può essere organizzato in modo efficiente all’interno del menu hamburger, consentendo agli utenti di accedere a vari pannelli all’interno di un modulo senza sovraccaricare l’interfaccia principale.

Si consideri uno scenario in cui un istituto finanziario offre un modulo di richiesta di prestito online che richiede agli utenti di fornire informazioni dettagliate su diversi pannelli, come dati personali, informazioni finanziarie, preferenze di prestito e documenti di supporto. Il modulo include più pannelli e opzioni che possono ingombrare l’interfaccia, in particolare sui dispositivi mobili. Gli utenti hanno bisogno di un modo organizzato per navigare attraverso questi pannelli senza sentirsi sopraffatti. Il menu hamburger è implementato per migliorare l’esperienza utente sui dispositivi mobili.

### Componenti del menu hamburger

![Menu Hamburger](/help/adaptive-forms/assets/hamburger-menu.png){width=50%, align=center}

**A. Menu Hamburger**: il menu hamburger presenta un pannello di navigazione che scorre o scende quando l&#39;icona dell&#39;hamburger viene selezionata o toccata. Il menu visualizza i titoli del pannello e, selezionando un pannello, lo stato attivo viene spostato su tale pannello. Consente agli utenti di navigare facilmente tra pannelli diversi.

![Menu Hamburger](/help/adaptive-forms/assets/hamburger-menu-icon.png){width=50%}

**B. Breadcrumb**: Le breadcrumb indicano la posizione corrente dell&#39;utente all&#39;interno del modulo. Offrono un percorso gerarchico che mostra il percorso di navigazione dell’utente e li aiuta a comprendere la sua posizione nel modulo.

**C. Pannello attivo**: il pannello attivo fa riferimento alla sezione o alla parte del modulo attualmente visualizzata. Quando un utente seleziona un’opzione dal menu con hamburger, il pannello corrispondente diventa il pannello attivo e mostra i campi e le informazioni pertinenti per quella sezione.

### Punti da considerare durante l&#39;utilizzo del menu hamburger

- Il menu hamburger visualizza solo i nomi dei pannelli. Di seguito sono riportati diversi scenari che illustrano come viene visualizzato il nome del pannello nel riquadro di navigazione del menu hamburger in base alle proprietà di configurazione del pannello:

   - Se si impostano le proprietà del pannello su Nascosto, il nome del pannello non viene visualizzato nel riquadro di navigazione del menu con hamburger. Se ad esempio si configurano le proprietà del pannello `Financial Information` come `hidden`, il nome del pannello non verrà visualizzato nel riquadro di spostamento del menu hamburger.

     ![Pannello nascosto](/help/adaptive-forms/assets/hidden-panel.png){width=50%}

   - Se si impostano le proprietà del pannello su `disabled`, il relativo nome verrà visualizzato nel riquadro di spostamento del menu hamburger, ma non sarà possibile selezionarlo o modificarlo. Se ad esempio si configurano le proprietà del pannello `Financial Information` come `disabled`, il nome del pannello verrà visualizzato nel riquadro di spostamento, ma non potrà essere selezionato o modificato.

     ![Pannello disabilitato](/help/adaptive-forms/assets/disabled-panel.png){width=50%}

   - Se nascondi il titolo del pannello, non viene visualizzato nel riquadro di navigazione del menu hamburger. Viene invece visualizzato uno spazio vuoto, ma puoi passare ai campi del pannello facendo clic su tale spazio. Se ad esempio si nasconde il titolo del pannello `Financial Information`, lo spazio vuoto verrà visualizzato al suo posto nel riquadro di spostamento del menu hamburger. Per passare ai campi del pannello, fai clic sullo spazio vuoto.

     ![Pannello titolo nascosto](/help/adaptive-forms/assets/hidden-title-panel.png){width=50%}

- Per impostazione predefinita, il riquadro di navigazione nel componente Breadcrumb supporta fino a tre livelli di navigazione. Tuttavia, con il componente personalizzato, puoi configurare la gerarchia di navigazione in modo da includere tutti i livelli necessari.
- Quando si utilizza il menu hamburger, l’utente può spostarsi tra i pannelli utilizzando le frecce. Tuttavia, una volta selezionato un pannello, il menu si chiude automaticamente e lo stato attivo si sposta sui campi all’interno del pannello selezionato.

<!--
### Advantages to use hamburger menu

- **Space efficiency**: By hiding form navigation options until needed, the hamburger menu maximizes screen space, which is especially beneficial on smaller devices.

- **Clutter reduction**: It minimizes visual clutter by consolidating various form navigation links into a single, collapsible menu.

- **Improved focus**: With fewer visible navigation elements, users can concentrate on the main content of the form without being distracted by secondary options.

- **Simplified design**: It creates a more streamlined user interface, resulting in a cleaner and more organized form layout.

- **Enhanced mobile experience**: On mobile devices, where screen space is limited, the hamburger menu offers an efficient way to access all form navigation options without overwhelming the user.

### How to enable hamburger menu for your form?

To enable hamburger menu for form, perform the following steps:

1. Open form in an edit mode.
1. Open the Content browser, and select the **[!UICONTROL Guide Container]** component of your Adaptive Form. 
1. Click the Guide Container properties ![Guide properties](/help/adaptive-forms/assets/configure_icon.png) icon. The Adaptive Form Container dialog box opens. 
1. Click the  **[!UICONTROL Basic]** tab. 
1. Select the **[!UICONTROL Add hamburger menu support]** checkbox.
1. Click **[!UICONTROL Done]**.

![Basic tab](/help/adaptive-forms/assets/formcontainer_basictab1.png)
-->

## Articoli correlati {#related-articles}

{{more-like-this}}

## Consulta anche {#see-also}

{{see-also}}