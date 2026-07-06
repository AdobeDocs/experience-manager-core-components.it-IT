---
title: 'Componente core Forms adattivo: scelta dell’immagine'
description: Utilizzo del componente core Scelta immagine.
role: Developer, Admin, User
hide: true
source-git-commit: 0af65c80f9cc58c4ba48d5b3dc7a026820bd2833
workflow-type: tm+mt
source-wordcount: '1318'
ht-degree: 58%

---

# Campo ImageChoice modulo adattivo {#image-choice}

Il componente Scelta immagine in un modulo consente agli utenti di effettuare selezioni in base alle rappresentazioni visive, come le immagini, anziché alle opzioni basate su testo. Presenta una serie di immagini, ognuna delle quali rappresenta una scelta distinta. Gli utenti possono selezionare una o più immagini, con un feedback visivo che ne indica la selezione. Questo componente è utile per opzioni quali varianti di prodotto, risposte a sondaggi o immagini di profilo. Offre un metodo di selezione intuitivo e accattivante che migliora il coinvolgimento e la chiarezza degli utenti.

## Utilizzo

Esistono diverse funzioni chiave del componente Scelta immagine, ad esempio:

- **Rappresentazione immagine:** Gli utenti visualizzano le immagini anziché le etichette di testo o i pulsanti di scelta tradizionali. Ogni immagine corrisponde a una scelta che può essere selezionata, fornendo una rappresentazione visiva delle opzioni disponibili.

- **Immagini selezionabili:** Gli utenti possono selezionare un&#39;opzione facendo clic direttamente sull&#39;immagine. L&#39;immagine selezionata viene spesso evidenziata per indicare che è stata scelta.

- **Selezione singola o multipla:** a seconda della progettazione del componente, gli utenti possono selezionare una o più immagini.

## Versione e compatibilità {#version-and-compatibility}

Il componente Scelta immagine Forms adattivo è stato rilasciato come parte dei Componenti core 2.0.64. Di seguito è riportata una tabella che mostra tutte le versioni supportate, la compatibilità AEM e i collegamenti alla documentazione corrispondente:

| Versione del componente | AEM as a Cloud Service |
|---|---|
| v1 | Compatibile con <br>[versione 2.0.64](/help/adaptive-forms/version.md) e successive |

Per informazioni sulle versioni dei componenti core, consulta il documento [Versioni dei componenti core](/help/adaptive-forms/version.md).

## Dettagli tecnici {#technical-details}

Per informazioni aggiornate sul componente core Scelta immagine Forms adattiva, consulta la documentazione tecnica su [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/). Per ulteriori informazioni sullo sviluppo dei componenti core, consulta la [Documentazione per gli sviluppatori dei componenti core](/help/developing/overview.md).

## Finestra di dialogo per la configurazione {#configure-dialog}

Puoi personalizzare facilmente l’esperienza del componente Scelta immagine per i visitatori con la finestra di dialogo per configurazione.


### Scheda Base {#basic-tab}

![Scelta immagine scheda base](basic-tab-imagechoice.png)

- **Nome**: è possibile identificare facilmente un componente modulo con il suo nome univoco sia nel modulo che nell’editor di regole, ma il nome non deve contenere spazi o caratteri speciali.

- **Titolo** - Con il relativo Titolo, è possibile identificare facilmente un tipo di componente in un modulo adattivo e, per impostazione predefinita, il titolo viene visualizzato accanto al componente.

- **Nascondi titolo** - È possibile nascondere il titolo selezionando la casella Nascondi titolo.

- **Opzioni** - Consente di aggiungere una o più immagini e di personalizzare le proprietà di scelta dell&#39;immagine. Le proprietà di scelta dell’immagine includono Valore dati, Risorsa di riferimento immagine e Testo alt, per ciascuna immagine.

- **Riferimento di binding**: un riferimento di binding è un riferimento a un elemento dati memorizzato in un’origine dati esterna e utilizzato in un modulo. Il riferimento di binding consente di eseguire un binding dinamico dei dati ai campi del modulo, in modo che il modulo possa visualizzare i dati più aggiornati dell’origine dati.

  Ad esempio, è possibile utilizzare un riferimento di binding per visualizzare il nome e l’indirizzo di un cliente in un modulo, in base all’ID cliente immesso nel modulo. È inoltre possibile utilizzare il riferimento di binding per aggiornare l’origine dati con i dati immessi nel modulo. In questo modo, AEM Forms consente di creare moduli che interagiscono con origini dati esterne, offrendo agli utenti un’esperienza utente semplice per la raccolta e la gestione dei dati.

- **Contrassegna come elemento modulo non associato**: seleziona l’opzione per configurare un campo modulo non collegato ad alcun schema. Questa opzione consente di salvare i dati senza aggiornare l’origine dati. Consente inoltre di gestire i dati in modo personalizzato, separato dall’integrazione standard del database.

- **Tipo di dati del valore inviato**: questa opzione specifica il tipo di dati del valore inviato quando viene selezionata un’opzione. Se il **tipo di dati del valore inviato** è impostato su `Number` e si aggiungono dati stringa al **Valore dati** nella scheda **Opzioni**, nella schermata viene visualizzato il messaggio di errore `Value type mismatch`.

- **Opzioni di visualizzazione**: consente di visualizzare il campo di scelta dell&#39;immagine in orizzontale o in verticale.

- **Valore predefinito**: questa opzione consente di aggiungere un valore predefinito (valore dati) in un campo modulo. Se è selezionato un **componente disabilitato** o un **componente di sola lettura**, sullo schermo viene visualizzato il valore predefinito. Se l’utente non immette alcun valore nel campo del modulo, tale valore viene inviato al momento dell’invio del modulo.

- **Nascondi componente**: selezionare l&#39;opzione per nascondere il componente dal modulo. Il componente rimane accessibile per altri scopi, ad esempio per i calcoli nell’editor di regole. Questa funzione è utile quando devi memorizzare informazioni che non devono essere viste o modificate direttamente dall’utente.

- **Disabilita componente**: selezionare l&#39;opzione per disabilitare o bloccare il componente. Il componente disabilitato non è attivo o modificabile dall’utente finale. L’utente può visualizzare il valore del campo, ma non può modificarlo. Il componente rimane accessibile per altri scopi, ad esempio per i calcoli nell’editor di regole.

- **Sola lettura**: questa opzione consente di aggiungere un valore predefinito (valore dati) in un campo modulo. Se è selezionato un **componente disabilitato** o un **componente di sola lettura**, sullo schermo viene visualizzato il valore predefinito. Se l’utente non immette alcun valore nel campo del modulo, tale valore viene inviato al momento dell’invio del modulo.

- **Tipo di selezione**: questa opzione consente agli utenti di selezionare una o più selezioni di campi di scelta immagine.

### Scheda Convalida {#validation-tab}

![Scelta dell&#39;immagine della scheda di convalida](validation-tab-image-choice.png)

- **Obbligatorio**: seleziona questa opzione se desideri visualizzare il componente in un modulo adattivo. Dopo aver selezionato l’opzione, è necessario effettuare una selezione prima di procedere con l’invio di un modulo. Non è possibile selezionare **Nascondi componente** o **Disabilita componente nella scheda** Base** quando questa opzione è selezionata.

- **Messaggio di errore** - Questa opzione consente di immettere un messaggio visualizzato se la casella di controllo **Obbligatorio** è selezionata e il campo di scelta dell&#39;immagine non è selezionato.

- **Messaggio di convalida script**: questa opzione consente di inserire un messaggio da visualizzare in caso di mancata convalida dello script.

### Scheda Contenuto Guida {#helpcontent-tab}

![Scelta dell&#39;immagine del contenuto della Guida](help-content-imagechoice.png)

- **Breve descrizione**: una breve descrizione è una breve spiegazione testuale che fornisce informazioni aggiuntive o chiarimenti sullo scopo di un campo modulo specifico. Aiuta l’utente a capire quale tipo di dati deve essere immesso nel campo e può fornire linee guida o esempi per garantire che le informazioni immesse siano valide e soddisfino i criteri desiderati. Per impostazione predefinita, le descrizioni brevi rimangono nascoste. Abilita l’opzione **Mostra sempre una breve descrizione** per visualizzarla sotto il componente.

- **Mostra sempre una breve descrizione**: abilita l’opzione per visualizzare la descrizione breve sotto il componente.

- **Testo guida**: il testo guida si riferisce a informazioni o indicazioni aggiuntive fornite all’utente per aiutarlo a compilare correttamente un campo del modulo. Viene visualizzato quando l’utente fa clic sull’icona dell’aiuto (i) posta vicino al componente. Il testo guida fornisce informazioni più dettagliate rispetto all’etichetta o al testo segnaposto di un campo del modulo ed è progettato per consentire all’utente di comprendere i requisiti o i vincoli del campo. Può inoltre offrire suggerimenti o esempi per rendere più semplice e precisa la compilazione del modulo.



### Scheda Accessibilità {#accessibility-tab}

![Scelta immagine di accessibilità](accessibility-imagechoice.png)

- **Testo per utilità per la lettura dello schermo**: il testo per le utilità per la lettura dello schermo indica il testo aggiuntivo destinato alla lettura da parte di tecnologie per l’accessibilità, come le utilità per la lettura dello schermo, utilizzate da persone ipovedenti. Questo testo fornisce una descrizione audio dello scopo del campo modulo e può includere informazioni sul titolo, la descrizione, il nome del campo ed eventuali messaggi rilevanti (testo personalizzato). Il testo dell’assistente vocale consente di garantire l’accesso al modulo da parte di qualsiasi utente, comprese le persone ipovedenti, consentendo di comprendere appieno il campo del modulo e i relativi requisiti.
   - **Testo personalizzato**: seleziona questa opzione per utilizzare il testo personalizzato per le etichette di accessibilità ARIA. Selezionando questa opzione, viene visualizzata la finestra di dialogo Testo personalizzato. Puoi aggiungere informazioni rilevanti nella finestra di dialogo Testo personalizzato.
   - **Titolo**: seleziona questa opzione per utilizzare il titolo per le etichette di accessibilità ARIA.

## Articoli correlati {#related-articles}

{{more-like-this}}

## Consulta anche {#see-also}

{{see-also}}


