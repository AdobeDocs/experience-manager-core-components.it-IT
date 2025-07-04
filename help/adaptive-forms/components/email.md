---
title: Componente core dei moduli adattivi - Inserimento e-mail
description: Utilizzo o personalizzazione del componente core per l’inserimento e-mail dei moduli adattivi.
role: Architect, Developer, Admin, User
exl-id: f6a2974b-991e-4cea-9ef8-0b03e8975eeb
source-git-commit: 6725784bd4c94d433c91d6bd65d14d03cbefd954
workflow-type: ht
source-wordcount: '2111'
ht-degree: 100%

---


# Componente e-mail {#Email-input-adaptive-forms-core-component}

Il componente core per l’inserimento di e-mail per moduli adattivi viene utilizzato per raccogliere gli indirizzi e-mail dagli utenti. Il campo di inserimento e-mail consente al browser di verificare che i dati immessi siano un formato di indirizzo e-mail valido. In genere è rappresentata come casella di testo e presenta convalide dei pattern per accettare solo indirizzi e-mail validi. Il campo di inseriemento e-mail può essere ulteriormente personalizzato con attributi aggiuntivi come “richiesto”, “segnaposto” e “pattern” per impostare le convalide per i dati di inserimento.

{{traditional-aem}}

**Esempio**

![esempio](/help/adaptive-forms/assets/emailid-example.png)

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion_it). -->

Ci sono diversi motivi per cui è utile includere un componente di input e-mail in un modulo adattivo, tra cui:

- **Comodità dell&#39;utente**: un campo di inseriemento e-mail facilita l’immissione dei propri indirizzi e-mail da parte degli utenti, in quanto fornisce un’indicazione chiara dei dati previsti nel campo.

- **Comunicazione personalizzata**: la raccolta degli indirizzi e-mail degli utenti tramite un modulo consente comunicazioni personalizzate, ad esempio l’invio di e-mail di conferma o newsletter.

- **Generazione di lead**: raccogliendo gli indirizzi e-mail tramite un modulo, le aziende possono creare il proprio elenco e-mail e utilizzarlo per la generazione di lead.

- **Autenticazione utente**: gli indirizzi e-mail possono essere utilizzati come mezzo di autenticazione per accedere a contenuti o servizi soggetti a restrizioni.

- **Raccolta di feedback**: un’immissione di e-mail in un modulo di feedback consente all’azienda di comunicare con l’utente per un follow-up o un chiarimento sul suo feedback.

## Versione e compatibilità {#version-and-compatibility}

Il componente core E-mail dei moduli adattivi è stato rilasciato a febbraio 2023 come parte dei Componenti core 2.0.4 per Cloud Service e dei Componenti core 1.1.12 per AEM Forms 6.5.16.0 o versioni successive. Di seguito è riportata una tabella che mostra tutte le versioni supportate, la compatibilità AEM e i collegamenti alla documentazione corrispondente:

| Versione del componente | AEM as a Cloud Service | AEM 6.5.16.0 Forms o versioni successive |
|---|---|---|
| v1 | Compatibile con <br>[versione 2.0.4](/help/adaptive-forms/version.md) e successive | Compatibile con <br>[versione 1.1.12](/help/adaptive-forms/version.md) e successive, ma precedenti a 2.0.0. |

Per informazioni sulle versioni dei componenti core, consulta il documento [Versioni dei componenti core](/help/adaptive-forms/version.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion_it). -->

## Dettagli tecnici {#technical-details}

Per informazioni aggiornate sul componente core per l’immissione di e-mail dei moduli adattivi, consulta la documentazione tecnica disponibile in [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/emailinput/v1/emailinput). Per ulteriori informazioni sullo sviluppo dei componenti core, consulta la [Documentazione per gli sviluppatori dei componenti core](/help/developing/overview.md).

## Finestra di dialogo per la configurazione {#configure-dialog}

Puoi personalizzare facilmente la tua esperienza di immissione e-mail per i visitatori tramite la finestra di dialogo Configura. Puoi anche definire le opzioni di immissione e-mail facilmente per un’esperienza utente semplice.

### Scheda Base {#basic-tab}

![Scheda Base](/help/adaptive-forms/assets/email_basictab.png)

- **Nome**: il nome identifica in modo univoco il componente nell’editor delle regole. Le stringhe di nome non consentono l’uso di caratteri e spazi speciali.

- **Titolo** : con il relativo titolo è possibile identificare facilmente un componente in un modulo e, per impostazione predefinita, il titolo viene visualizzato sopra il componente. Se non aggiungi un titolo, al posto del testo del titolo viene visualizzato il nome del componente.
- **Consenti testo formattato per titolo**: questa funzione permette agli utenti di formattare i titoli in testo normale, incorporando opzioni come il grassetto, il corsivo, il testo sottolineato, vari font, dimensioni dei font, colori e altre opzioni per migliorare la presentazione visiva e la personalizzazione. Offre maggiore flessibilità e controllo creativo nel far risaltare i titoli all’interno di documenti, siti web o applicazioni.\
  Dopo aver selezionato la casella di controllo **Consenti testo formattato per titolo**, le opzioni di formattazione diventano visibili per applicare lo stile al titolo del componente. Per accedere a tutte le opzioni di formattazione disponibili, fai clic sulla scheda ![Icona schermo intero](/help/adaptive-forms/assets/fullscreen-icon.png).

  ![Supporto testo RTF](/help/adaptive-forms/assets/richtext-support-title.png)

- **Nascondi titolo**: seleziona l’opzione per nascondere il titolo del componente.

- **Testo segnaposto**: il testo segnaposto in un componente modulo si riferisce a un’etichetta o a un prompt brevi che vengono visualizzati all’interno di un campo di inserimento come suggerimento per l’utente sul tipo di informazioni che ci si aspetta venga immesso in quel campo. Il testo segnaposto scompare quando l’utente inizia a digitare nel campo e viene visualizzato nuovamente se il campo viene lasciato vuoto. Fornisce un suggerimento visivo all’utente, ma non funge da etichetta o valore permanente per il campo.
- **Riferimento di binding**: un riferimento di binding è un riferimento a un elemento dati memorizzato in un’origine dati esterna e utilizzato in un modulo. Il riferimento di binding consente di eseguire un binding dinamico dei dati ai campi del modulo, in modo che il modulo possa visualizzare i dati più aggiornati dell’origine dati. Ad esempio, è possibile utilizzare un riferimento di binding per visualizzare il nome e l’indirizzo di un cliente in un modulo, in base all’ID cliente immesso nel modulo. È inoltre possibile utilizzare il riferimento di binding per aggiornare l’origine dati con i dati immessi nel modulo. In questo modo, AEM Forms consente di creare moduli che interagiscono con origini dati esterne, fornendo un’esperienza utente fluida per la raccolta e la gestione dei dati.
- **Contrassegna come elemento modulo non associato**: seleziona l’opzione per configurare un campo modulo non collegato ad alcun schema. Questa opzione consente di salvare i dati senza aggiornare l’origine dati. Consente inoltre di gestire i dati in modo personalizzato, separato dall’integrazione standard del database.
- **Nascondi componente**: seleziona questa opzione per nascondere il componente del modulo. Il componente rimane accessibile per altri scopi, ad esempio per i calcoli nell’editor di regole. Questa funzione è utile quando devi memorizzare informazioni che non devono essere viste o modificate direttamente dall’utente.
- **Disattiva componente**: seleziona questa opzione per disabilitare il componente. Il componente disabilitato non è attivo o modificabile dall’utente finale. L’utente può visualizzare il valore del campo, ma non può modificarlo. Il componente rimane accessibile per altri scopi, ad esempio per i calcoli nell’editor di regole.
- **Sola lettura**: seleziona questa opzione per rendere il componente non modificabile. L’utente può visualizzare il valore del campo, ma non può modificarlo. Il componente rimane accessibile per altri scopi, ad esempio per i calcoli nell’editor di regole.

- **Valore predefinito** - questa opzione consente di aggiungere un valore predefinito in un campo modulo. Se **Componente disabilitato** o **Componente di sola lettura** è selezionato, il valore predefinito viene visualizzato sullo schermo. Se l’utente non immette alcun valore nel campo modulo, questo valore viene inviato al momento dell’invio del modulo.
- **Attributo riempimento automatico**: l’opzione consente agli utenti di immettere un valore che viene popolato automaticamente nel campo del modulo in base alle informazioni memorizzate.

### Scheda Convalida {#validation-tab}

![Scheda Convalida](/help/adaptive-forms/assets/email_validationtab.png)

- **Obbligatorio**: seleziona questa opzione se desideri visualizzare il componente in un modulo adattivo. Dopo aver selezionato l’opzione, è necessario immettere un valore prima di procedere con l’invio di un modulo. Quando questa opzione è selezionata, non è possibile selezionare **Nascondi componente** o **Disabilita componente** nella scheda **Base**.

- **Messaggio di errore**: questa opzione consente di inserire un messaggio visualizzato se la casella di controllo **Obbligatorio** è selezionata e il campo modulo viene lasciato vuoto.

- **Messaggio di convalida script**: questa opzione consente di inserire un messaggio da visualizzare in caso di errore di convalida dello script.

- **Numero massimo di caratteri**: questa opzione consente di specificare il numero massimo di caratteri consentiti nel campo. Se immetti caratteri maggiori del valore specificato in **Numero massimo di caratteri**, sullo schermo viene visualizzato un messaggio di errore. La finestra di dialogo **Messaggio di errore relativo al numero massimo di caratteri** consente di aggiungere un messaggio di errore personalizzato.

- **Messaggio di errore relativo al numero massimo di caratteri**: la finestra di dialogo **Messaggio di errore relativo al numero massimo di caratteri** ti permette di aggiungere un messaggio di errore personalizzato se si immettono caratteri superiori al valore specificato nell’opzione **Numero massimo di caratteri**.

- **Numero minimo di caratteri**: questa opzione ti consente di specificare il numero minimo di caratteri consentiti nel campo. Se immetti caratteri inferiori al valore specificato in **Numero minimo di caratteri**, sullo schermo viene visualizzato un messaggio di errore. La finestra di dialogo **Messaggio di errore relativo al numero minimo di caratteri** ti consente di aggiungere un messaggio di errore personalizzato.

- **Messaggio di errore relativo al numero minimo di caratteri**: la finestra di dialogo **Messaggio di errore relativo al numero minimo di caratteri** ti consente di aggiungere un messaggio di errore personalizzato se si immettono caratteri inferiori al valore specificato nell’opzione **Numero minimo di caratteri**.
<br>

L’opzione **Pattern di convalida** consente di inserire un pattern per convalidare l’ID e-mail immesso. Se l’ID e-mail non viene convalidato rispetto al valore inserito nell’opzione **Pattern**, viene visualizzato il messaggio di errore.

- **Pattern**: questa opzione consente di inserire i pattern di verifica consentiti per gli indirizzi e-mail. Sono consentite anche espressioni regolari.
- **Messaggio di errore**: questa opzione consente di inserire un messaggio che viene visualizzato se l’ID e-mail non viene convalidato rispetto al valore immesso nell’opzione **Pattern**.

### Scheda Contenuto Guida {#help-content-tab}

![Scheda Contenuto Guida](/help/adaptive-forms/assets/email_helptab.png)

- **Breve descrizione**: una breve descrizione è una breve spiegazione testuale che fornisce informazioni aggiuntive o chiarimenti sullo scopo di un campo modulo specifico. Aiuta l’utente a capire quale tipo di dati deve essere immesso nel campo e può fornire linee guida o esempi per garantire che le informazioni immesse siano valide e soddisfino i criteri desiderati. Per impostazione predefinita, le descrizioni brevi rimangono nascoste. Abilita l’opzione **Mostra sempre una breve descrizione** per visualizzarla sotto il componente.

- **Mostra sempre una breve descrizione**: abilita l’opzione per visualizzare la descrizione breve sotto il componente.

- **Testo guida**: il testo guida si riferisce a informazioni o indicazioni aggiuntive fornite all’utente per aiutarlo a compilare correttamente un campo del modulo. Viene visualizzato quando l’utente fa clic sull’icona dell’aiuto (i) posta vicino al componente. Il testo guida fornisce informazioni più dettagliate rispetto all’etichetta o al testo segnaposto di un campo del modulo ed è progettato per consentire all’utente di comprendere i requisiti o i vincoli del campo. Può inoltre offrire suggerimenti o esempi per rendere più semplice e precisa la compilazione del modulo.

### Scheda Accessibilità {#accessibility-tab}

![Scheda Accessibilità](/help/adaptive-forms/assets/email_accessibilitytab.png)

- **Testo per utilità per la lettura dello schermo**: il testo per le utilità per la lettura dello schermo si riferisce al testo aggiuntivo destinato specificamente ad essere letto da tecnologie di assistenza, come le utilità per la lettura dello schermo, utilizzate da persone ipovedenti. Questo testo fornisce una descrizione audio dello scopo del campo modulo e può includere informazioni sul titolo, la descrizione, il nome del campo ed eventuali messaggi rilevanti (testo personalizzato). Il testo dell’assistente vocale consente di garantire l’accesso al modulo da parte di qualsiasi utente, comprese le persone ipovedenti, consentendo di comprendere appieno il campo del modulo e i relativi requisiti.

   - **Testo personalizzato**: seleziona questa opzione per utilizzare il testo personalizzato per le etichette di accessibilità ARIA. Selezionando questa opzione, viene visualizzata la finestra di dialogo Testo personalizzato. Puoi aggiungere informazioni rilevanti nella finestra di dialogo Testo personalizzato.
   - **Descrizione**: seleziona questa opzione per utilizzare la descrizione per le etichette di accessibilità ARIA.
   - **Titolo**: seleziona questa opzione per utilizzare il titolo per le etichette di accessibilità ARIA.
   - **Nome**: seleziona questa opzione per utilizzare il nome per le etichette di accessibilità ARIA.
   - **Nessuno**: seleziona questa opzione in caso tu non voglia aggiungere etichette di accessibilità ARIA.

## Finestra di dialogo per la progettazione {#design-dialog}

La finestra di dialogo per la progettazione viene utilizzata per definire e gestire gli stili CSS per il componente di input e-mail.

### Scheda Stili {#styles-tab}

La scheda è utilizzata per definire e gestire gli stili CSS per un componente. Il componente core per l’inserimento e-mail dei moduli adattivi supporta il [Sistema di stili](/help/get-started/authoring.md#component-styling) di AEM.

![Scheda Stile](/help/adaptive-forms/assets/datepicker_styletab.png)

- **Classi CSS predefinite**: è possibile fornire una classe CSS predefinita per il componente core inserimento e-mail dei moduli adattivi.

- **Stili consentiti**: è possibile definire gli stili fornendo un nome e la classe CSS che rappresenta lo stile. Ad esempio, puoi creare uno stile denominato “testo in grassetto” e fornire la classe CSS “spessore carattere: grassetto”. Puoi utilizzare o applicare questi stili a un modulo adattivo nell’editor di moduli adattivi. Per applicare uno stile, nell’editor dei moduli adattivi, seleziona il componente a cui applicare lo stile, passa alla finestra di dialogo delle proprietà e seleziona lo stile desiderato dall’elenco a discesa **Stili**. Per aggiornare o modificare gli stili, è sufficiente tornare alla finestra di dialogo per la progettazione, aggiornare gli stili nella scheda Stili e salvare le modifiche.

### Proprietà personalizzate

![Finestra di dialogo Proprietà personalizzate](/help/adaptive-forms/assets/datepicker_customproperties.png)

Le proprietà personalizzate consentono di associare attributi personalizzati (coppie chiave-valore) a un componente core del modulo adattivo utilizzando il modello di modulo. Le proprietà personalizzate vengono riflesse nella sezione delle proprietà della rappresentazione headless del componente. Consentono di creare un comportamento di modulo dinamico che si adatta in base ai valori degli attributi personalizzati. Ad esempio, gli sviluppatori possono progettare diverse rappresentazioni di un componente moduli headless su piattaforme mobili, desktop o web, migliorando in modo significativo l’esperienza utente su un’ampia gamma di dispositivi.

- **Nome gruppo**: puoi fornire un nome per identificare il gruppo di proprietà personalizzate. È possibile aggiungere, eliminare o ridisporre più gruppi di proprietà personalizzate. Dopo aver aggiunto il gruppo di proprietà personalizzate, puoi visualizzare le seguenti opzioni:

   - **Coppie chiave-valore**: puoi aggiungere più nomi e valori della proprietà personalizzata facendo clic sul pulsante **Aggiungi** per ogni gruppo di proprietà personalizzate.

   - **Elimina**: tocca o fai clic per eliminare il nome e il valore della proprietà personalizzata.

   - **Ridisponi**: tocca o fai clic e trascina per ridisporre l’ordine del nome e del valore della proprietà personalizzata.

### Scheda Formati {#formats-tab}

La scheda dei formati consente di specificare i formati di data predefiniti e personalizzati.

![Scheda formato](/help/adaptive-forms/assets/emailinput_formattab.png)

<!--

## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html?lang=it)

-->

## Articoli correlati {#related-articles}

{{more-like-this}}

## Consulta anche {#see-also}

{{see-also}}
