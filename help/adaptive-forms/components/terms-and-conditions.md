---
title: Componente core dei moduli adattivi - Termini e condizioni
description: Utilizzo o personalizzazione del componente core Termini e condizioni dei moduli adattivi.
role: Architect, Developer, Admin, User
exl-id: c607d554-ad2d-4434-856d-91e174ef3149
source-git-commit: e843ccf5c030cd4f1015e3290347b5799828537a
workflow-type: tm+mt
source-wordcount: '3115'
ht-degree: 91%

---

# Componente Termini e condizioni

<span class="preview"> Questo articolo contiene informazioni su **Consenti formato Rich Text per titolo** e **Consenti formato Rich Text per opzioni**  funzioni, funzionalità precedenti al rilascio. La funzione di pre-release è accessibile solo tramite [canale preliminare](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/release-notes/prerelease.html#new-features).</span>

Per componente **Termini e condizioni** si intende una sezione all’interno di un modulo che illustra i termini, le regole e le condizioni che gli utenti devono accettare o rispettare quando utilizzano un servizio o accedono al contenuto.

Il componente **Termini e condizioni** è un componente composito costituito dai componenti Testo, Casella di controllo e Collegamento. Il componente testo contiene un titolo e una breve panoramica dello scopo e dell’ambito dei termini e delle condizioni. Include inoltre una casella di controllo utilizzata per ottenere il consenso esplicito dell’utente. Puoi anche sostituire un testo di consenso con collegamenti.

>[!NOTE]
>
> Per AEM 6.5 Forms, questo componente è stato introdotto con AEM 6.5 Forms Service Pack 19 (6.5.19.0). Per abilitare questo componente, accertati che siano installate le versioni necessarie dei componenti core di Forms e WCM. Per informazioni dettagliate sulle versioni dei componenti core dei moduli adattivi, consulta le [Versioni dei componenti core dei moduli adattivi](/help/adaptive-forms/version.md)

**Esempio**

![termini e condizioni](/help/adaptive-forms/assets/terms-and-conditions.png)

Per ulteriori informazioni sui diversi componenti del componente Termini e condizioni, consulta la sezione [Componenti secondari del componente Termini e condizioni](#sub-component).

## Utilizzo {#reasons-to-use-termsandconditions}

- **Accordo per l’utente**: il componente funge da accordo tra il fornitore di servizi e l’utente. Gli utenti devono confermare e accettare i termini prima di accedere al servizio o al contenuto.

- **Conformità legale**: garantisce la conformità legale e la tutela del fornitore di servizi delineando i diritti, le responsabilità e le responsabilità di entrambe le parti.

- **Processi di registrazione**: i moduli di registrazione o di iscrizione includono il componente **Termini e condizioni** che richiede agli utenti di accettare esplicitamente i termini prima di creare un account o utilizzare un servizio.

- **Transazioni di e-commerce**: i siti web online includono il componente **Termini e condizioni** affinché gli utenti vengano invitati ad accettare i termini e le condizioni come parte del processo di pagamento prima di effettuare acquisti online.

- **Accordi sulla sicurezza e la privacy**: il componente **Termini e condizioni** include dettagli su come i dati utente vengono raccolti, memorizzati e utilizzati, spesso integrati da un’informativa sulla privacy separata

## Versione e compatibilità {#version-and-compatibility}

Il componente core Pannello a soffietto moduli adattivi è stato rilasciato a febbraio 2023 come parte dei Componenti core 2.0.62 per Cloud Service e dei Componenti core 1.1.28 per AEM Forms 6.5.16.0 o versioni successive. Di seguito è riportata una tabella che mostra tutte le versioni supportate, la compatibilità AEM e i collegamenti alla documentazione corrispondente:

| Versione del componente | AEM as a Cloud Service | AEM Forms 6.5.16.0 o versioni successive |
|---|---|---|
| v1 | Compatibile con <br>[versione 2.0.62](/help/adaptive-forms/version.md) e successive | Compatibile con <br>[versione 1.1.28](/help/adaptive-forms/version.md) e successive, ma precedenti a 2.0.0. |

Per informazioni sulle versioni dei componenti core, consulta il documento [Versioni dei componenti core](/help/adaptive-forms/version.md).

## Dettagli tecnici {#technical-details}

Per informazioni aggiornate sul componente core Termini e condizioni per moduli adattivi, consulta la documentazione tecnica disponibile su [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/checkboxgroup/v1/checkboxgroup). Per ulteriori informazioni sullo sviluppo dei componenti core, dai un’occhiata alla [documentazione per gli sviluppatori dei componenti core](/help/developing/overview.md).

## Finestra di dialogo per la configurazione {#configure-dialog}

Puoi personalizzare facilmente l’esperienza del componente Termini e condizioni per i visitatori tramite la finestra di dialogo Configura. Puoi anche definire facilmente le opzioni dei Termini e condizioni per un’esperienza utente semplice.

### Scheda Base

![Scheda Base](/help/adaptive-forms/assets/terms-and-conditions-basic-tab.png)

- **Nome**: il nome identifica il componente in modo univoco nell’editor di regole. I caratteri speciali e gli spazi non sono consentiti nelle stringhe dei nomi.

- **Titolo**: il titolo permette di identificare facilmente un componente in un modulo e, per impostazione predefinita, il titolo viene visualizzato sopra il componente. Se non aggiungi un titolo, al posto del testo del titolo viene visualizzato il nome del componente.
- **Consenti formato Rich Text per titolo** - Questa funzione consente agli utenti di formattare i titoli di testo normale, incorporando funzioni come il grassetto, il corsivo, il testo sottolineato, vari font, dimensioni dei font, colori e opzioni aggiuntive per migliorare la presentazione visiva e la personalizzazione. Offre maggiore flessibilità e controllo creativo nel far risaltare i titoli all&#39;interno di documenti, siti Web o applicazioni.\
  Dopo aver selezionato la casella di controllo per **Consenti formato Rich Text per titolo** , le opzioni di formattazione diventano visibili per applicare lo stile al titolo del componente. Per accedere a tutte le opzioni di formattazione disponibili, puoi fare clic sul pulsante ![Icona Schermo intero](/help/adaptive-forms/assets/fullscreen-icon.png) scheda.

  ![Supporto Rich Text](/help/adaptive-forms/assets/richtext-support-title.png)

- **Mostra opzione di approvazione** : seleziona l’opzione per visualizzare la casella di controllo relativa al consenso utilizzata per ottenere il consenso esplicito dell’utente.

- **Mostra come finestra a comparsa**: seleziona l’opzione per visualizzare il componente Termini e condizioni in una finestra a comparsa.

- **Sostituisci il testo del consenso con collegamenti web**: seleziona l’opzione per sostituire un testo di consenso con un collegamento web.  Se l’opzione è deselezionata, per impostazione predefinita viene visualizzato il testo del consenso.

- **Nascondi titolo**: seleziona l’opzione per nascondere il titolo del componente.

- **Raggruppa dati dei componenti secondari all’invio del modulo (racchiudi dati nell’oggetto)**: quando questa opzione è selezionata, i dati dei relativi componenti secondari sono nidificati all’interno dell’oggetto JSON del componente principale. Tuttavia, se l’opzione non è selezionata, i dati JSON inviati hanno una struttura semplice, senza alcun oggetto per il componente principale. Ad esempio:

   - Quando l’opzione è selezionata, i dati dei componenti secondari (ad esempio, Via, Città e CAP) vengono nidificati all’interno del componente principale (Indirizzo) come oggetto JSON. In questo modo viene creata una struttura gerarchica e i dati vengono organizzati sotto il componente principale.

     Struttura dei dati inviati:

     ```JSON
     { "Address":
     
     { "Street": "123 Main Street", "City": "New York", "Zip Code": "12345" }
     
     }
     ```

   - Quando l’opzione non è selezionata, i dati JSON inviati hanno una struttura semplice senza alcun oggetto per il componente principale (Indirizzo). Tutti i dati si trovano allo stesso livello, senza alcuna organizzazione gerarchica.

     Struttura dei dati inviati:

     ```JSON
        { "Street": "123 Main Street", "City": "New York", "Zip Code": "12345" }
     ```

- **Riferimento di binding**: un riferimento di binding è un riferimento a un elemento dati memorizzato in un’origine dati esterna e utilizzato in un modulo. Il riferimento di binding consente di eseguire un binding dinamico dei dati ai campi del modulo, in modo che il modulo possa visualizzare i dati più aggiornati dell’origine dati. Ad esempio, è possibile utilizzare un riferimento di binding per visualizzare il nome e l’indirizzo di un cliente in un modulo, in base all’ID cliente immesso nel modulo. È inoltre possibile utilizzare il riferimento di binding per aggiornare l’origine dati con i dati immessi nel modulo. In questo modo, AEM Forms consente di creare moduli che interagiscono con origini dati esterne, fornendo un’esperienza utente fluida per la raccolta e la gestione dei dati.

- **Nascondi componente**: seleziona l’opzione per nascondere il componente del modulo. Il componente rimane accessibile per altri scopi, ad esempio per i calcoli nell’editor di regole. Questa funzione è utile quando devi memorizzare informazioni che non devono essere viste o modificate direttamente dall’utente.
- **Disattiva componente**: seleziona questa opzione per disabilitare il componente. Il componente disabilitato non è attivo o modificabile dall’utente finale. L’utente può visualizzare il valore del campo, ma non può modificarlo. Il componente rimane accessibile per altri scopi, ad esempio per i calcoli nell’editor di regole.
- **Sola lettura**: seleziona questa opzione per rendere il componente non modificabile. L’utente può visualizzare il valore del campo, ma non può modificarlo. Il componente rimane accessibile per altri scopi, ad esempio per i calcoli nell’editor di regole.

### Scheda Contenuto Guida {#help-content-tab}

![Scheda Contenuto Guida](/help/adaptive-forms/assets/terms-and-conditions-help-tab.png)

- **Breve descrizione**: una breve descrizione è una breve spiegazione testuale che fornisce informazioni aggiuntive o chiarimenti sullo scopo di un campo modulo specifico. Aiuta l’utente a capire quale tipo di dati deve essere immesso nel campo e può fornire linee guida o esempi per garantire che le informazioni immesse siano valide e soddisfino i criteri desiderati. Per impostazione predefinita, le descrizioni brevi rimangono nascoste. Abilita l’opzione **Mostra sempre una breve descrizione** per visualizzarla sotto il componente.

- **Mostra sempre una breve descrizione**: abilita l’opzione per visualizzare la descrizione breve sotto il componente.

- **Testo guida**: il testo guida si riferisce a informazioni o indicazioni aggiuntive fornite all’utente per aiutarlo a compilare correttamente un campo del modulo. Viene visualizzato quando l’utente fa clic sull’icona dell’aiuto (i) posta vicino al componente. Il testo guida fornisce informazioni più dettagliate rispetto all’etichetta o al testo segnaposto di un campo del modulo ed è progettato per consentire all’utente di comprendere i requisiti o i vincoli del campo. Può inoltre offrire suggerimenti o esempi per rendere più semplice e precisa la compilazione del modulo.

### Scheda Accessibilità

![Scheda Accessibilità](/help/adaptive-forms/assets/terms-and-conditions-accessibility-tab.png)

- **Testo per utilità per la lettura dello schermo**: il testo per le utilità per la lettura dello schermo si riferisce al testo aggiuntivo destinato specificamente ad essere letto da tecnologie di assistenza, come le utilità per la lettura dello schermo, utilizzate da persone ipovedenti. Questo testo fornisce una descrizione audio dello scopo del campo modulo e può includere informazioni sul titolo, la descrizione, il nome del campo ed eventuali messaggi rilevanti (testo personalizzato). Il testo dell’assistente vocale consente di garantire l’accesso al modulo da parte di qualsiasi utente, comprese le persone ipovedenti, consentendo di comprendere appieno il campo del modulo e i relativi requisiti.
- **Ruolo di HTML per l’annuncio dell’assistente vocale**: il ruolo HTML è un attributo utilizzato per specificare lo scopo di un elemento HTML per tecnologie di assistenza come le utilità per la lettura dello schermo. L’attributo ruolo viene utilizzato per fornire ulteriore contesto e significato semantico a un elemento, facilitando l’interpretazione e la lettura del contenuto da parte delle utilità per la lettura dello schermo per l’utente. Ad esempio, in AEM Forms, l’etichetta di un campo modulo potrebbe avere il ruolo di “etichetta” e il relativo campo di input potrebbe avere il ruolo di “casella di testo”. Questo permette all’assistente vocale di comprendere la relazione tra l’etichetta e il campo di input, e di leggerli in modo corretto all’utente.

## Finestra di dialogo per la progettazione {#design-dialog}

La finestra di dialogo per la progettazione consente di definire e gestire gli stili CSS per il componente Termini e condizioni.


### Scheda Stili {#styles-tab}

La scheda è utilizzata per definire e gestire gli stili CSS per un componente. Il componente core Termini e condizioni dei moduli adattivi supporta il [Sistema di stili](/help/get-started/authoring.md#component-styling) di AEM.

![Finestra di dialogo per la progettazione](/help/adaptive-forms/assets/checkbox-style.png)

- **Classi CSS predefinite**: è possibile fornire una classe CSS predefinita per il componente core Termini e condizioni nei moduli adattivi.

- **Stili consentiti**: è possibile definire gli stili fornendo un nome e la classe CSS che rappresenta lo stile. Ad esempio, puoi creare uno stile denominato “testo in grassetto” e fornire la classe CSS “spessore carattere: grassetto”. Puoi utilizzare o applicare questi stili a un modulo adattivo nell’editor di moduli adattivi. Per applicare uno stile, nell’editor dei moduli adattivi, seleziona il componente a cui applicare lo stile, passa alla finestra di dialogo delle proprietà e seleziona lo stile desiderato dall’elenco a discesa **Stili**. Per aggiornare o modificare gli stili, è sufficiente tornare alla finestra di dialogo per la progettazione, aggiornare gli stili nella scheda Stili e salvare le modifiche.

### Proprietà personalizzate

![Finestra di dialogo Proprietà personalizzate](/help/adaptive-forms/assets/checkbox-customproperties.png)

Le proprietà personalizzate consentono di associare attributi personalizzati (coppie chiave-valore) a un componente core del modulo adattivo utilizzando il modello di modulo. Le proprietà personalizzate vengono riflesse nella sezione delle proprietà della rappresentazione headless del componente. Consentono di creare un comportamento di modulo dinamico che si adatta in base ai valori degli attributi personalizzati. Ad esempio, gli sviluppatori possono progettare diverse rappresentazioni di un componente moduli headless su piattaforme mobili, desktop o web, migliorando in modo significativo l’esperienza utente su un’ampia gamma di dispositivi.

- **Nome gruppo**: puoi fornire un nome per identificare il gruppo di proprietà personalizzate. È possibile aggiungere, eliminare o ridisporre più gruppi di proprietà personalizzate. Dopo aver aggiunto il gruppo di proprietà personalizzate, puoi visualizzare le seguenti opzioni:

   - **Coppie chiave-valore**: puoi aggiungere più nomi e valori della proprietà personalizzata facendo clic sul pulsante **Aggiungi** per ogni gruppo di proprietà personalizzate.

   - **Elimina**: tocca o fai clic per eliminare il nome e il valore della proprietà personalizzata.

   - **Ridisponi**: tocca o fai clic e trascina per ridisporre l’ordine del nome e del valore della proprietà personalizzata.

## Componenti secondari del componente Termini e condizioni {#sub-component}

Il componente **Termini e condizioni** è un componente composito che comprende i seguenti componenti secondari:
- [Componente collegamento](#link)
- [Componente testo](#text)
- [Componente casella di controllo](#checkbox)

### Componente collegamento{#link}

Questo componente sostituisce un testo di consenso con uno o più collegamenti web. Viene utilizzato in uno scenario in cui l’utente intende offrire riferimenti a sezioni particolari, informazioni aggiuntive o documenti esterni. Puoi personalizzare facilmente il componente **Collegamento** singolarmente per i visitatori con la finestra di dialogo Configura.

#### Scheda Base

![Scheda Base](/help/adaptive-forms/assets/link-basic-tab.png)

- **Nome**: il nome identifica il componente in modo univoco nell’editor di regole. I caratteri speciali e gli spazi non sono consentiti nelle stringhe dei nomi.

- **Titolo**: il titolo permette di identificare facilmente un componente in un modulo e, per impostazione predefinita, il titolo viene visualizzato sopra il componente. Se non aggiungi un titolo, al posto del testo del titolo viene visualizzato il nome del componente.
- **Consenti formato Rich Text per titolo** - Questa funzione consente agli utenti di formattare i titoli utilizzando opzioni quali grassetto, corsivo, stili dei caratteri, colori e allineamento, migliorando la presentazione visiva e la personalizzazione. Offre maggiore flessibilità e controllo creativo nel far risaltare i titoli all&#39;interno di documenti, siti Web o applicazioni.\
  Dopo aver selezionato la casella di controllo per **Consenti formato Rich Text per titolo** , le opzioni di formattazione diventano visibili per applicare lo stile al titolo del componente. Per accedere a tutte le opzioni di formattazione disponibili, puoi fare clic sul pulsante ![Icona Schermo intero](/help/adaptive-forms/assets/fullscreen-icon.png) scheda.

  ![Supporto Rich Text](/help/adaptive-forms/assets/richtext-support-title.png)

- **Nascondi titolo**: seleziona l’opzione per nascondere il titolo del componente.

- **Collegamenti**: specifica il collegamento e il testo da visualizzare corrispondente al posto del testo del consenso. Puoi aggiungere più collegamenti facendo clic sul pulsante **Aggiungi**.
Una volta aggiunta una nuova opzione, è possibile eseguire le azioni seguenti:
   - **Collegamento**: questa opzione consente di immettere l’URL a cui reindirizzare quando viene selezionata un’opzione.
   - **Testo Visualizzato**: questa opzione consente di inserire il contenuto da visualizzare in un modulo adattivo.
   - **Elimina**: tocca o fai clic per eliminare l’opzione di un pulsante di scelta.
   - **Ridisponi**: tocca o fai clic e trascina per riordinare le opzioni.

  È inoltre possibile formattare le opzioni per il gruppo di caselle di controllo utilizzando **Consenti formato Rich Text per opzioni**. Dopo aver selezionato la casella di controllo per **Consenti formato Rich Text per opzioni** le opzioni di formattazione diventano visibili per formattare le opzioni del componente. Per accedere a tutte le opzioni di formattazione disponibili, puoi fare clic sul pulsante `Fullscreen` ![Icona Schermo intero](/help/adaptive-forms/assets/fullscreen-icon.png) scheda.

  ![Supporto di testo formattato per le opzioni](/help/adaptive-forms/assets/link-options.png)

- **Riferimento di binding**: un riferimento di binding è un riferimento a un elemento dati memorizzato in un’origine dati esterna e utilizzato in un modulo. Il riferimento di binding consente di eseguire un binding dinamico dei dati ai campi del modulo, in modo che il modulo possa visualizzare i dati più aggiornati dell’origine dati. Ad esempio, è possibile utilizzare un riferimento di binding per visualizzare il nome e l’indirizzo di un cliente in un modulo, in base all’ID cliente immesso nel modulo. È inoltre possibile utilizzare il riferimento di binding per aggiornare l’origine dati con i dati immessi nel modulo. In questo modo, AEM Forms consente di creare moduli che interagiscono con origini dati esterne, offrendo agli utenti un’esperienza utente semplice per la raccolta e la gestione dei dati.

- **Contrassegna come elemento modulo non associato**: seleziona l’opzione per configurare un campo modulo non collegato ad alcun schema. Questa opzione consente di salvare i dati senza aggiornare l’origine dati. Consente inoltre di gestire i dati in modo personalizzato, separato dall’integrazione standard del database.
- **Nascondi componente**: seleziona questa opzione per nascondere il componente dal modulo. Il componente rimane accessibile per altri scopi, ad esempio per i calcoli nell’editor di regole. Questa funzione è utile quando devi memorizzare informazioni che non devono essere viste o modificate direttamente dall’utente.

- **Disattiva componente**: seleziona l’opzione per disabilitare o bloccare il componente. Il componente disabilitato non è attivo o modificabile dall’utente finale. L’utente può visualizzare il valore del campo, ma non può modificarlo. Il componente rimane accessibile per altri scopi, ad esempio per i calcoli nell’editor di regole.
- **Sola lettura**: seleziona questa opzione per rendere il componente non modificabile. L’utente può visualizzare il valore del campo, ma non può modificarlo. Il componente rimane accessibile per altri scopi, ad esempio per i calcoli nell’editor di regole.

#### Scheda Convalida

![Scheda Convalida](/help/adaptive-forms/assets/link-validation-tab.png)

- **Obbligatorio**: seleziona questa opzione se desideri visualizzare il componente in un modulo adattivo. Dopo aver selezionato l’opzione, è necessario effettuare una selezione prima di procedere con l’invio di un modulo. Non è possibile selezionare **Nascondi componente** o **Disattiva componente** nella scheda **Base** quando questa opzione è selezionata.

- **Messaggio di errore**: questa opzione consente di inserire un messaggio visualizzato se la casella di controllo **Obbligatorio** è selezionata e il campo modulo viene lasciato vuoto.

- **Messaggio di convalida script**: questa opzione consente di inserire un messaggio da visualizzare in caso di mancata convalida dello script.

### Scheda Contenuto Guida {#helpcontent-tab}

![Scheda Contenuto Guida](/help/adaptive-forms/assets/link-help-tab.png)

- **Breve descrizione**: una breve descrizione è una breve spiegazione testuale che fornisce informazioni aggiuntive o chiarimenti sullo scopo di un campo modulo specifico. Aiuta l’utente a capire quale tipo di dati deve essere immesso nel campo e può fornire linee guida o esempi per garantire che le informazioni immesse siano valide e soddisfino i criteri desiderati. Per impostazione predefinita, le descrizioni brevi rimangono nascoste. Abilita l’opzione **Mostra sempre una breve descrizione** per visualizzarla sotto il componente.

- **Mostra sempre una breve descrizione**: abilita l’opzione per visualizzare la descrizione breve sotto il componente.

- **Testo guida**: il testo guida si riferisce a informazioni o indicazioni aggiuntive fornite all’utente per aiutarlo a compilare correttamente un campo del modulo. Viene visualizzato quando l’utente fa clic sull’icona dell’aiuto (i) posta vicino al componente. Il testo guida fornisce informazioni più dettagliate rispetto all’etichetta o al testo segnaposto di un campo del modulo ed è progettato per consentire all’utente di comprendere i requisiti o i vincoli del campo. Può inoltre offrire suggerimenti o esempi per rendere più semplice e precisa la compilazione del modulo.

### Scheda Accessibilità

![Scheda Accessibilità](/help/adaptive-forms/assets/link-accessibilty-tab.png)

**Testo per utilità per la lettura dello schermo**: il testo per le utilità per la lettura dello schermo si riferisce al testo aggiuntivo destinato specificamente ad essere letto da tecnologie di assistenza, come le utilità per la lettura dello schermo, utilizzate da persone ipovedenti. Questo testo fornisce una descrizione audio dello scopo del campo modulo e può includere informazioni sul titolo, la descrizione, il nome del campo ed eventuali messaggi rilevanti (testo personalizzato). Il testo dell’assistente vocale consente di garantire l’accesso al modulo da parte di qualsiasi utente, comprese le persone ipovedenti, consentendo di comprendere appieno il campo del modulo e i relativi requisiti.

### Componente testo {#text}

Il componente **Testo** mostra il contenuto di testo che fornisce informazioni agli utenti. Questo componente include i termini e le condizioni effettive, la terminologia giuridica o qualsiasi altra informazione testuale rilevante.

Puoi personalizzare facilmente il [Componente testo](/help/adaptive-forms/components/text.md) singolarmente per i visitatori con la finestra di dialogo Configura. Per definire facilmente le opzioni di testo per un’esperienza utente fluida, utilizza la [finestra di dialogo per la configurazione del componente testo](/help/adaptive-forms/components/text.md#configure-dialog).


### Componente casella di controllo {#checkbox}

Viene utilizzata una casella di controllo per ottenere il consenso o la conferma dell’utente. Funge da indicatore visivo per confermare che l’utente ha letto e accettato i termini descritti. È obbligatorio selezionare la casella di controllo per indicare il consenso dell’utente.

Puoi personalizzare facilmente il [Componente casella di controllo](/help/adaptive-forms/components/checkbox.md) singolarmente per i visitatori con la finestra di dialogo Configura. Per definire le proprietà della casella di controllo per un’esperienza utente fluida, utilizza la [finestra di dialogo per la configurazione del componente casella di controllo](/help/adaptive-forms/components/checkbox.md#configure-dialog).


## Articoli correlati {#related-articles}

{{more-like-this}}

## Consulta anche {#see-also}

{{see-also}}
