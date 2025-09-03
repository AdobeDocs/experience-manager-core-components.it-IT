---
title: Componente core Moduli adattivi - Firma a mano
description: Utilizzo o personalizzazione del componente core Firma a mano per moduli adattivi.
role: Architect, Developer, Admin, User
exl-id: 608c4368-d539-4d05-a75c-c077ea822f93
source-git-commit: 006f6c844ab9e7a784dabea026867939445479e9
workflow-type: tm+mt
source-wordcount: '1761'
ht-degree: 98%

---

# Componente Firma a mano

<span>Il componente Firma scarabocchio è in fase di adozione anticipata. Puoi scrivere a `aem-forms-ea@adobe.com` dal tuo ID e-mail ufficiale per partecipare al programma early adopter e richiedere l&#39;accesso alla funzionalità.</span>

Un componente Firma a mano in un modulo adattivo è un elemento di interfaccia utente che consente agli utenti di disegnare la propria **firma** direttamente nel modulo utilizzando un mouse, uno stilo o uno schermo tattile. In questo modo è possibile acquisire accuratamente il consenso scritto a mano, le approvazioni o la verifica nei flussi di lavoro digitali.

**Esempio**

![esempio](/help/adaptive-forms/assets/scribble-signature.png){width=50%,align-center}

**Varie opzioni disponibili nella finestra Firma**

- **A:** fai clic sull’icona **Disegna** per disegnare la firma nell’area di lavoro.
- **B:** fai clic sull’icona **Cancella** per cancellare la firma nell’area di lavoro.
- **C:** fai clic sull’icona **Geolocalizzazione** per aggiungere la geolocalizzazione insieme alla firma.
- **D:** fai clic sull’icona **Tastiera** per digitare il tuo nome nell’area di lavoro.

Dopo aver selezionato l’icona **Salva** nella finestra della Firma a mano, non è possibile modificare la firma. Nel caso in cui desideri modificare la firma, è necessario ignorare quella corrente e riapporla utilizzando l’opzione Pennello/Tastiera.

>[!NOTE]
>
> Le firme vengono sempre salvate in formato PNG.

## Utilizzo {#reasons-to-use-scribble-signature}

Ci sono diversi motivi per cui è utile includere una Firma a mano in un modulo, tra cui:

- **Consenso digitale**: consente agli utenti di fornire firme legalmente valide in formato elettronico.
- **Esperienza utente migliorata**: offre un modo naturale per accedere direttamente ai dispositivi senza eseguire la scansione o il caricamento.
- **Flussi di lavoro privi di supporto cartaceo**: elimina la necessità di stampare, firmare e ripetere la scansione dei documenti.
- **Autenticazione**: funge da ulteriore livello di conferma e approvazione.
- **Precisione dei dati**: assicura la corretta acquisizione dell’input scritto a mano del firmatario in formato digitale.

## Versione e compatibilità {#version-and-compatibility}

Il componente core Firma a mano per moduli adattivi è stato rilasciato ad **agosto 2025** come parte di **Componenti core 2.24.6** per Cloud Service e versioni successive.

| Versione del componente | AEM as a Cloud Service | AEM 6.5.16.0 Forms o versioni successive |
|---|---|---|
| v1 | Compatibile con<br>[versione 2.24.6](/help/adaptive-forms/version.md) e successive | |

Per informazioni dettagliate sulle versioni, consulta [Versioni dei Componenti core](/help/adaptive-forms/version.md).

## Dettagli tecnici {#technical-details}

Ottieni i dettagli tecnici più recenti sul componente core Firma a mano per moduli adattivi su [GitHub](https://github.com/adobe/aem-core-forms-components). Per ulteriori informazioni sullo sviluppo dei componenti core, consulta la [Documentazione per sviluppatori di componenti core](/help/developing/overview.md).

## Finestra di dialogo per la configurazione {#configure-dialog}

La finestra di dialogo per la configurazione consente di personalizzare il componente Firma a mano.

### Scheda Base {#basic-tab}

![Scheda Base](/help/adaptive-forms/assets/scribble-signature-basictab.png)

- **Nome**: il nome identifica il componente in modo univoco nell’editor di regole. I caratteri speciali e gli spazi non sono consentiti nelle stringhe dei nomi.

- **Titolo**: il titolo è una stringa che viene visualizzata nella parte superiore di un componente in un modulo adattivo. Il titolo identifica in modo univoco il componente nella struttura ad albero di un modulo adattivo. Se non aggiungi un titolo, al posto del testo del titolo viene visualizzato il nome del componente.
- **Consenti testo formattato per titolo**: questa funzione permette agli utenti di formattare i titoli in testo normale, incorporando opzioni come il grassetto, il corsivo, il testo sottolineato, vari font, dimensioni dei font, colori e altre opzioni per migliorare la presentazione visiva e la personalizzazione. Offre maggiore flessibilità e controllo creativo nel far risaltare i titoli all’interno di documenti, siti web o applicazioni.\
  Dopo aver selezionato la casella di controllo **Consenti testo formattato per titolo**, le opzioni di formattazione diventano visibili per applicare lo stile al titolo del componente. Per accedere a tutte le opzioni di formattazione disponibili, fai clic sulla scheda ![Icona schermo intero](/help/adaptive-forms/assets/fullscreen-icon.png).

  ![Supporto testo RTF](/help/adaptive-forms/assets/richtext-support-title.png)

- **Nascondi titolo**: seleziona questa opzione per nascondere il titolo del tipo di componente in un modulo adattivo.
- **Testo segnaposto**: il testo segnaposto in un componente del modulo si riferisce a un’etichetta breve o a un prompt che viene visualizzato all’interno di un campo di inserimento come suggerimento per l’utente sul tipo di informazioni che ci si aspetta venga inserito in quel campo. Il testo segnaposto scompare quando l’utente inizia a digitare nel campo e viene visualizzato nuovamente se il campo viene lasciato vuoto. Fornisce un suggerimento visivo all’utente, ma non funge da etichetta o valore permanente per il campo.

- **Riferimento di binding**: un riferimento di binding è un riferimento a un elemento dati memorizzato in un’origine dati esterna e utilizzato in un modulo. Il riferimento di binding consente di eseguire un binding dinamico dei dati ai campi del modulo, in modo che il modulo possa visualizzare i dati più aggiornati dell’origine dati. Ad esempio, è possibile utilizzare un riferimento di binding per visualizzare il nome e l’indirizzo di un cliente in un modulo, in base all’ID cliente immesso nel modulo. È inoltre possibile utilizzare il riferimento di binding per aggiornare l’origine dati con i dati immessi nel modulo. In questo modo, AEM Forms consente di creare moduli che interagiscono con origini dati esterne, offrendo agli utenti un’esperienza utente semplice per la raccolta e la gestione dei dati.

- **Contrassegna come elemento modulo non associato**: seleziona l’opzione per configurare un campo modulo non collegato ad alcun schema. Questa opzione consente di salvare i dati senza aggiornare l’origine dati. Consente inoltre di gestire i dati in modo personalizzato, separato dall’integrazione standard del database.

- **Nascondi componente**: seleziona questa opzione per nascondere il componente del modulo. Il componente rimane accessibile per altri scopi, ad esempio per i calcoli nell’editor di regole. Questa funzione è utile quando devi memorizzare informazioni che non devono essere viste o modificate direttamente dall’utente.
- **Disattiva componente**: seleziona questa opzione per disabilitare il componente. Il componente disabilitato non è attivo o modificabile dall’utente finale. L’utente può visualizzare il valore del campo, ma non può modificarlo. Il componente rimane accessibile per altri scopi, ad esempio per i calcoli nell’editor di regole.

- **Titolo finestra di dialogo per la firma**: il titolo della finestra di dialogo per la firma definisce il testo visualizzato nella parte superiore della finestra di dialogo per l’acquisizione della firma. Funge da prompt o istruzione per l’utente quando deve fornire una firma. Il testo aiuta a guidare l’utente nel processo di firma, rendendo l’interazione chiara e intuitiva.

### Scheda Convalida

![scheda convalida](/help/adaptive-forms/assets/scribble-signature-validation.png)

- **Obbligatorio**: seleziona questa opzione se desideri visualizzare il componente in un modulo adattivo. Dopo aver selezionato l’opzione, è necessario effettuare una selezione prima di procedere con l’invio di un modulo. Non è possibile selezionare **Nascondi componente** o **Disattiva componente** nella scheda **Base** quando questa opzione è selezionata.

- **Messaggio di errore**: questa opzione consente di inserire un messaggio visualizzato se la casella di controllo **Obbligatorio** è selezionata e il campo modulo viene lasciato vuoto.

- **Messaggio di convalida script**: questa opzione consente di inserire un messaggio da visualizzare in caso di mancata convalida dello script.

### Scheda Contenuto Guida {#help-content-tab}

![Scheda Contenuto Guida](/help/adaptive-forms/assets/scribble-signature-helptab.png)

- **Breve descrizione**: una breve descrizione è una breve spiegazione testuale che fornisce informazioni aggiuntive o chiarimenti sullo scopo di un campo modulo specifico. Aiuta l’utente a capire quale tipo di dati deve essere immesso nel campo e può fornire linee guida o esempi per garantire che le informazioni immesse siano valide e soddisfino i criteri desiderati. Per impostazione predefinita, le descrizioni brevi rimangono nascoste. Abilita l’opzione **Mostra sempre una breve descrizione** per visualizzarla sotto il componente.

- **Mostra sempre una breve descrizione**: abilita questa opzione per visualizzare la descrizione breve sotto il componente.

- **Testo guida**: il testo guida si riferisce a informazioni o indicazioni aggiuntive fornite all’utente per aiutarlo a compilare correttamente un campo del modulo. Viene visualizzato quando l’utente fa clic sull’icona dell’aiuto (i) posta vicino al componente. Il testo guida fornisce informazioni più dettagliate rispetto all’etichetta o al testo segnaposto di un campo del modulo ed è progettato per consentire all’utente di comprendere i requisiti o i vincoli del campo. Può inoltre offrire suggerimenti o esempi per rendere più semplice e precisa la compilazione del modulo.

### Scheda Accessibilità {#accessibility-tab}

![Scheda Accessibilità](/help/adaptive-forms/assets/scribble-signature-accessibilitytab.png)

- **Testo per utilità per la lettura dello schermo**: il testo per le utilità per la lettura dello schermo si riferisce al testo aggiuntivo destinato specificamente ad essere letto da tecnologie di assistenza, come le utilità per la lettura dello schermo, utilizzate da persone ipovedenti. Questo testo fornisce una descrizione audio dello scopo del campo modulo e può includere informazioni sul titolo, la descrizione, il nome del campo ed eventuali messaggi rilevanti (testo personalizzato). Il testo dell’assistente vocale consente di garantire l’accesso al modulo da parte di qualsiasi utente, comprese le persone ipovedenti, consentendo di comprendere appieno il campo del modulo e i relativi requisiti.
   - **Testo personalizzato**: seleziona questa opzione per utilizzare il testo personalizzato per le etichette di accessibilità ARIA. Selezionando questa opzione, viene visualizzata la finestra di dialogo Testo personalizzato. Puoi aggiungere informazioni rilevanti nella finestra di dialogo Testo personalizzato.
   - **Descrizione**: seleziona questa opzione per utilizzare la descrizione per le etichette di accessibilità ARIA.
   - **Titolo**: seleziona questa opzione per utilizzare il titolo per le etichette di accessibilità ARIA.
   - **Nome**: seleziona questa opzione per utilizzare il nome per le etichette di accessibilità ARIA.
   - **Nessuno**: seleziona questa opzione in caso tu non voglia aggiungere etichette di accessibilità ARIA.

## Finestra di dialogo per la progettazione {#design-dialog}

La finestra di dialogo per la progettazione viene utilizzata per definire e gestire gli stili CSS per il componente Firma a mano.

### Scheda Stili {#styles-tab}

La scheda è utilizzata per definire e gestire gli stili CSS per un componente. Il componente core Firma a mano per moduli adattivi supporta il [Sistema di stili](/help/get-started/authoring.md#component-styling) di AEM.

![Finestra di dialogo per la progettazione](/help/adaptive-forms/assets/checkbox-style.png)

- **Classi CSS predefinite**: è possibile fornire una classe CSS predefinita per il componente core Firma a mano per moduli adattivi.

- **Stili consentiti**: è possibile definire gli stili fornendo un nome e la classe CSS che rappresenta lo stile. Ad esempio, puoi creare uno stile denominato “testo in grassetto” e fornire la classe CSS “spessore carattere: grassetto”. Puoi utilizzare o applicare questi stili a un modulo adattivo nell’editor di moduli adattivi. Per applicare uno stile, nell’editor dei moduli adattivi, seleziona il componente a cui applicare lo stile, passa alla finestra di dialogo delle proprietà e seleziona lo stile desiderato dall’elenco a discesa **Stili**. Per aggiornare o modificare gli stili, è sufficiente tornare alla finestra di dialogo per la progettazione, aggiornare gli stili nella scheda Stili e salvare le modifiche.

### Proprietà personalizzate

![Finestra di dialogo Proprietà personalizzate](/help/adaptive-forms/assets/checkbox-customproperties.png)

Le proprietà personalizzate consentono di associare attributi personalizzati (coppie chiave-valore) a un componente core del modulo adattivo utilizzando il modello di modulo. Le proprietà personalizzate vengono riflesse nella sezione delle proprietà della rappresentazione headless del componente. Consentono di creare un comportamento di modulo dinamico che si adatta in base ai valori degli attributi personalizzati. Ad esempio, gli sviluppatori possono progettare diverse rappresentazioni di un componente moduli headless su piattaforme mobili, desktop o web, migliorando in modo significativo l’esperienza utente su un’ampia gamma di dispositivi.

- **Nome gruppo**: puoi fornire un nome per identificare il gruppo di proprietà personalizzate. È possibile aggiungere, eliminare o ridisporre più gruppi di proprietà personalizzate. Dopo aver aggiunto il gruppo di proprietà personalizzate, puoi visualizzare le seguenti opzioni:

   - **Coppie chiave-valore**: puoi aggiungere più nomi e valori della proprietà personalizzata facendo clic sul pulsante **Aggiungi** per ogni gruppo di proprietà personalizzate.

   - **Elimina**: tocca o fai clic per eliminare il nome e il valore della proprietà personalizzata.

   - **Ridisponi**: tocca o fai clic e trascina per ridisporre l’ordine del nome e del valore della proprietà personalizzata.

## Articoli correlati {#related-articles}

{{more-like-this}}

## Consulta anche {#see-also}

{{see-also}}
