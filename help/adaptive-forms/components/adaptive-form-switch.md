---
title: 'Componente core dei moduli adattivi: componente Interruttore'
description: Utilizzo o personalizzazione del componente core interruttore nei moduli adattivi.
role: Architect, Developer, Admin, User
exl-id: 6ff2ca76-1514-42eb-bde3-60259af2d187
source-git-commit: 6725784bd4c94d433c91d6bd65d14d03cbefd954
workflow-type: tm+mt
source-wordcount: '1922'
ht-degree: 100%

---


# Componente interruttore moduli adattivi{#switch-adaptive-forms-core-component}

Il componente Interruttore è un’interfaccia utente grafica utilizzata nei moduli che consente agli utenti di scegliere tra due opzioni. In genere si tratta di un interruttore a due stati che consente agli utenti di scegliere tra due stati, per abilitare o disabilitare una funzione, un’impostazione o una funzionalità. Il componente Interruttore è progettato per rappresentare visivamente lo stato corrente e indicare se una particolare funzione è attivata o disattivata.

Il componente Interruttore è un elemento di controllo booleano che imposta il valore su true o false. Ad esempio, viene utilizzato per attivare o disattivare una funzione, ad esempio l’audio, o per abilitare o disabilitare il Bluetooth o il WiFi.

![Esempio di componente Interruttore](/help/adaptive-forms/assets/switch-example.png)

{{traditional-aem}}

## Utilizzo {#reasons-to-use-switch}

I motivi comuni per utilizzare l’Interruttore in un modulo adattivo sono i seguenti:

- **Interazione dell’utente**: gli utenti possono interagire con il componente Interruttore facendo clic su di esso o toccandolo.

- **Stati**: il componente Interruttore presenta due stati, attivazione e disattivazione. Lo stato iniziale del componente Interruttore dipende dall’impostazione predefinita o dallo stato corrente della funzione che controlla.

- **Rappresentazione visiva**: il componente Interruttore riflette visivamente il suo stato corrente cambiando il colore o la posizione.

- **Funzionalità di controllo**: il componente Interruttore viene utilizzato per abilitare o disabilitare funzionalità specifiche in un modulo AEM. Ad esempio, consente agli utenti di attivare o disattivare una funzione.

## Versione e compatibilità {#version-and-compatibility}

Il componente core interruttore nei moduli adattivi è stato rilasciato come parte dei componenti core 2.0.64. Questa tabella mostra tutte le versioni supportate, la compatibilità con AEM e i collegamenti alla documentazione corrispondente:

|  |  |
|---|---|
| Versione del componente | AEM as a Cloud Service |
| --- | --- |
| v1 | Compatibile con <br>[versione 2.0.64](/help/adaptive-forms/version.md) e successive | Compatibile | Compatibile |

Per informazioni sulle versioni dei componenti core, consulta il documento [Versioni dei componenti core](/help/adaptive-forms/version.md).

## Dettagli tecnici {#technical-details}

Per informazioni aggiornate sul componente core interruttore per moduli adattivi, consulta la documentazione tecnica disponibile su [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/switch/v1/switch). Per ulteriori informazioni sullo sviluppo dei componenti core, consulta la [Documentazione per gli sviluppatori di componenti core](/help/developing/overview.md).

## Finestra di dialogo per la configurazione {#configure-dialog}

Puoi personalizzare facilmente l’esperienza del componente Interruttore per i visitatori tramite la finestra di dialogo Configura. Puoi anche definire le opzioni del componente Interruttore con facilità per un’esperienza di utilizzo ottimale.

### Scheda Base

![Scheda Base](/help/adaptive-forms/assets/switch-basic.png)

- **Nome**: è possibile identificare facilmente un componente modulo con il suo nome univoco sia nel modulo che nell’editor di regole, ma il nome non deve contenere spazi o caratteri speciali.

- **Titolo**: puoi identificare facilmente un componente in un modulo con il suo nome e, per impostazione predefinita, il titolo viene visualizzato accanto al componente. Se non aggiungi un titolo, il componente non viene visualizzato.
- **Consenti testo formattato per titolo**: questa funzione permette agli utenti di formattare i titoli in testo normale, incorporando opzioni come il grassetto, il corsivo, il testo sottolineato, vari font, dimensioni dei font, colori e altre opzioni per migliorare la presentazione visiva e la personalizzazione. Offre maggiore flessibilità e controllo creativo nel far risaltare i titoli all’interno di documenti, siti web o applicazioni.\
  Dopo aver selezionato la casella di controllo **Consenti testo formattato per titolo**, le opzioni di formattazione diventano visibili per applicare lo stile al titolo del componente. Per accedere a tutte le opzioni di formattazione disponibili, fai clic sulla scheda ![Icona schermo intero](/help/adaptive-forms/assets/fullscreen-icon.png).

  ![Supporto testo RTF](/help/adaptive-forms/assets/richtext-support-title.png)

- **Nascondi titolo**: seleziona l’opzione per nascondere il titolo del componente.

- **Mantieni valore stato deselezionato**: selezionando questa opzione è possibile specificare il valore da restituire quando il componente interruttore non è selezionato.
- **Opzioni**: specifica il valore dei dati e mostra il testo per ciascuna opzione.
   - **Valore dati attivato**: specifica il valore da inviare quando l’interruttore è abilitato in un modulo adattivo.
   - **Testo visualizzato attivato**: specifica il testo da visualizzare come etichetta quando l’interruttore è abilitato in un modulo adattivo.
   - **Valore dati disattivato**: specifica il valore da inviare quando l’interruttore non è abilitato in un modulo adattivo. Questa opzione è visibile solo se è attivata l’opzione **Mantieni valore stato deselezionato**.
   - **Testo visualizzato disattivato**: specifica il testo da visualizzare come etichetta quando l’interruttore non è abilitato in un modulo adattivo. Questa opzione è visibile solo se è attivata l’opzione **Mantieni valore stato deselezionato**.

  È inoltre possibile formattare le opzioni per cambiare componente utilizzando **Consenti testo formattato per opzioni**.

  ![Supporto testo RTF per le opzioni](/help/adaptive-forms/assets/switch-optipn-rich-text.png)

  Dopo aver selezionato la casella di controllo **Consenti testo formattato per opzioni** le opzioni di formattazione diventano visibili per applicare lo stile alle opzioni del componente. Per accedere a tutte le opzioni di formattazione disponibili, fai clic sulla scheda `Fullscreen` ![Icona schermo intero](/help/adaptive-forms/assets/fullscreen-icon.png).

  ![Supporto testo RTF per le opzioni](/help/adaptive-forms/assets/switch-richtext-for-display.png)

- **Riferimento di binding**: un riferimento di binding è un riferimento a un elemento dati memorizzato in un’origine dati esterna e utilizzato in un modulo. Il riferimento di binding consente di eseguire un binding dinamico dei dati ai campi del modulo, in modo che il modulo possa visualizzare i dati più aggiornati dell’origine dati. Ad esempio, è possibile utilizzare un riferimento di binding per visualizzare il nome e l’indirizzo di un cliente in un modulo, in base all’ID cliente immesso nel modulo. È inoltre possibile utilizzare il riferimento di binding per aggiornare l’origine dati con i dati immessi nel modulo. In questo modo, AEM Forms consente di creare moduli che interagiscono con origini dati esterne, offrendo agli utenti un’esperienza utente semplice per la raccolta e la gestione dei dati.
- **Contrassegna come elemento modulo non associato**: seleziona l’opzione per configurare un campo modulo non collegato ad alcun schema. Questa opzione consente di salvare i dati senza aggiornare l’origine dati. Consente inoltre di gestire i dati in modo personalizzato, separato dall’integrazione standard del database.
- **Tipo di dati del valore inviato**: questa opzione specifica il tipo di dati del valore inviato quando viene selezionata un’opzione. Se il **tipo di dati del valore inviato** è impostato su `Number` e si aggiungono dati stringa al **Valore dati** nella scheda **Opzioni**, nella schermata viene visualizzato il messaggio di errore `Value type mismatch`.
- **Nascondi componente**: seleziona questa opzione per nascondere il componente del modulo. Il componente rimane accessibile per altri scopi, ad esempio per i calcoli nell’editor di regole. Questa funzione è utile quando devi memorizzare informazioni che non devono essere viste o modificate direttamente dall’utente.

- **Disattiva componente**: seleziona l’opzione per disabilitare o bloccare il componente. Il componente disabilitato non è attivo o modificabile dall’utente finale. L’utente può visualizzare il valore del campo, ma non può modificarlo. Il componente rimane accessibile per altri scopi, ad esempio per i calcoli nell’editor di regole.

- **Valore predefinito**: questa opzione consente di aggiungere un valore predefinito in un campo del modulo. Se sono selezionati il **Componente disabilitato** o il **Componente di sola lettura**, il valore predefinito viene visualizzato sullo schermo. Se l’utente non immette alcun valore nel campo modulo, questo valore viene inviato al momento dell’invio del modulo.

### Scheda Convalida {#validation-tab}

![Scheda Convalida](/help/adaptive-forms/assets/switch-validation.png)

- **Obbligatorio**: seleziona questa opzione se desideri visualizzare il componente in un modulo adattivo. Dopo aver selezionato l’opzione, è necessario effettuare una selezione prima di procedere con l’invio di un modulo. Non è possibile selezionare **Nascondi componente** o **Disattiva componente** nella scheda **Base** quando questa opzione è selezionata.

- **Messaggio di errore**: questa opzione consente di inserire un messaggio visualizzato se la casella di controllo **Obbligatorio** è selezionata e il campo modulo viene lasciato vuoto.

- **Messaggio di convalida script**: questa opzione consente di inserire un messaggio da visualizzare in caso di mancata convalida dello script.

### Scheda Contenuto Guida {#helpcontent-tab}

![Scheda Contenuto Guida](/help/adaptive-forms/assets/switch-help.png)

- **Breve descrizione**: una breve descrizione è una breve spiegazione testuale che fornisce informazioni aggiuntive o chiarimenti sullo scopo di un campo modulo specifico. Aiuta l’utente a capire quale tipo di dati deve essere immesso nel campo e può fornire linee guida o esempi per garantire che le informazioni immesse siano valide e soddisfino i criteri desiderati. Per impostazione predefinita, le descrizioni brevi rimangono nascoste. Abilita l’opzione **Mostra sempre una breve descrizione** per visualizzarla sotto il componente.

- **Mostra sempre una breve descrizione**: abilita l’opzione per visualizzare la descrizione breve sotto il componente.

- **Testo guida**: il testo guida si riferisce a informazioni o indicazioni aggiuntive fornite all’utente per aiutarlo a compilare correttamente un campo del modulo. Viene visualizzato quando l’utente fa clic sull’icona dell’aiuto (i) posta vicino al componente. Il testo guida fornisce informazioni più dettagliate rispetto all’etichetta o al testo segnaposto di un campo del modulo ed è progettato per consentire all’utente di comprendere i requisiti o i vincoli del campo. Può inoltre offrire suggerimenti o esempi per rendere più semplice e precisa la compilazione del modulo.

### Scheda Accessibilità {#accessibility-tab}

![Scheda Accessibilità](/help/adaptive-forms/assets/switch-accessibility.png)

- **Testo per utilità per la lettura dello schermo**: il testo per le utilità per la lettura dello schermo indica il testo aggiuntivo destinato alla lettura da parte di tecnologie per l’accessibilità, come le utilità per la lettura dello schermo, utilizzate da persone ipovedenti. Questo testo fornisce una descrizione audio dello scopo del campo modulo e può includere informazioni sul titolo, la descrizione, il nome del campo ed eventuali messaggi rilevanti (testo personalizzato). Il testo dell’assistente vocale consente di garantire l’accesso al modulo da parte di qualsiasi utente, comprese le persone ipovedenti, consentendo di comprendere appieno il campo del modulo e i relativi requisiti.
   - **Testo personalizzato**: seleziona questa opzione per utilizzare il testo personalizzato per le etichette di accessibilità ARIA. Selezionando questa opzione, viene visualizzata la finestra di dialogo Testo personalizzato. Puoi aggiungere informazioni rilevanti nella finestra di dialogo Testo personalizzato.
   - **Descrizione**: seleziona questa opzione per utilizzare la descrizione per le etichette di accessibilità ARIA.
   - **Titolo**: seleziona questa opzione per utilizzare il titolo per le etichette di accessibilità ARIA.
   - **Nome**: seleziona questa opzione per utilizzare il nome per le etichette di accessibilità ARIA.
   - **Nessuno**: seleziona questa opzione in caso tu non voglia aggiungere etichette di accessibilità ARIA.

### Scheda Stili {#styles-tab}

![Scheda Stili](/help/adaptive-forms/assets/switch-styles.png)

- **Nascondi etichette**: seleziona questa opzione per nascondere le etichette del componente interruttore.

- **Mostra etichette**: seleziona questa opzione per visualizzare le etichette del componente interruttore.

## Finestra di dialogo per la progettazione {#design-dialog}

La finestra di dialogo per la progettazione viene utilizzata per definire e gestire gli stili CSS per il componente Interruttore.

### Scheda Stili {#styles-design-tab}

Il componente core interruttore per i moduli adattivi supporta il [Sistema di stili](/help/get-started/authoring.md#component-styling) di AEM.

![Finestra di dialogo per la progettazione](/help/adaptive-forms/assets/checkbox-style.png)

- **Classi CSS predefinite**: è possibile fornire una classe CSS predefinita per il componente core interruttore per i moduli adattivi.

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
