---
title: 'Componente core dei moduli adattivi: Google reCAPTCHA'
description: Migliora facilmente la sicurezza dei moduli con il servizio Google reCAPTCHA con AEM Forms. Spiegare le proprietà di reCAPTCHA per modulo adattivo
role: Architect, Developer, Admin, User
exl-id: 2d986b90-e596-4e8f-9a32-0ebced5461c8
source-git-commit: 6725784bd4c94d433c91d6bd65d14d03cbefd954
workflow-type: ht
source-wordcount: '1325'
ht-degree: 100%

---


# reCAPTCHA per modulo adattivo {#google-recaptcha}

Il CAPTCHA (Completely Automated Public Turing test to tell Computers and Humans Apart) è un programma comunemente utilizzato nelle transazioni online per distinguere tra esseri umani e programmi o bot automatizzati. Rappresenta una sfida e valuta la risposta dell’utente per determinare se si tratta di un essere umano o di un bot che interagisce con il sito. Impedisce all’utente di procedere se il test non riesce e contribuisce a rendere sicure le transazioni online impedendo ai bot di pubblicare spam o avere scopi dannosi.

AEM Forms as a Cloud Service supporta il reCAPTCHA di Google v2 nei Moduli adattivi. Puoi utilizzarlo per presentare una sfida CAPTCHA all’invio del modulo

{{traditional-aem}}

## Utilizzo {#reasons-to-use-google-recaptcha}


- **Prevenzione di spam e bot**: uno dei motivi principali per cui utilizzare un reCAPTCHA è quello di evitare che gli invii di spam e i bot dannosi invadano il modulo. Gli algoritmi avanzati di reCAPTCHA possono rilevare i tentativi automatizzati di inviare il modulo, garantendo in tal modo che solo gli utenti legittimi possano interagire con esso.

- **Sicurezza avanzata**: implementando un reCAPTCHA, aggiungi un ulteriore livello di sicurezza al modulo adattivo. In questo modo è possibile proteggere le informazioni riservate e impedire a utenti malintenzionati di sfruttare le vulnerabilità.

- **Esperienza utente**: mentre a volte i CAPTCHA possono essere considerati come un inconveniente, l’approccio adattivo di reCAPTCHA implica che alla maggior parte degli utenti viene presentata un’esperienza semplificata e intuitiva che richiede un’interazione minima. Questo può contribuire a mantenere un’esperienza utente positiva scoraggiando al contempo i bot.

- **Adattabilità**: il meccanismo adattivo di reCAPTCHA analizza il comportamento degli utenti e le interazioni per determinare se si tratta di esseri umani o meno. Ciò significa che il livello di sfida presentato all’utente può variare in base alla probabilità che si tratti di un bot. Questa adattabilità riduce gli attriti per gli utenti autentici mantenendo al contempo una sicurezza elevata.

- **Moderazione manuale ridotta**: riducendo in modo significativo il numero di invii di spam e di contenuti generati da bot, il reCAPTCHA può risparmiare tempo e risorse che altrimenti verrebbero spese per la moderazione manuale e la pulizia.

## Versione e compatibilità {#version-and-compatibility}

Il componente core reCAPTCHA di Google per moduli adattivi è stato rilasciato nell’agosto 2023 come parte della “versione” dei componenti core. Di seguito è riportata una tabella che mostra tutte le versioni supportate, la compatibilità AEM e i collegamenti alla documentazione corrispondente:


| Versione del componente | AEM as a Cloud Service |
|--- |--- |
| v1 | Compatibile con <br>[versione 2.0.4](/help/versions.md) e successive | Compatibile | Compatibile |

Per informazioni sulle versioni dei componenti core, consulta il documento [Versioni dei componenti core](/help/versions.md).

## Dettagli tecnici {#technical-details}

Per informazioni aggiornate sul componente core reCAPTCHA di Google per moduli adattivi, consulta la documentazione tecnica disponibile su [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/recaptcha/v1/recaptcha). Per ulteriori informazioni sullo sviluppo dei componenti core, consulta la [Documentazione per gli sviluppatori di componenti core](/help/developing/overview.md).

## Finestra di dialogo per la configurazione {#configure-dialog}

Puoi personalizzare facilmente l’esperienza reCAPTCHA di Google per i visitatori tramite la finestra di dialogo Configura. Puoi anche definire le opzioni reCAPTCHA di Google facilmente per un’esperienza utente semplice.

### Scheda Base {#basic-tab}

![Scheda Base](/help/adaptive-forms/assets/recaptcha-basictab.png)

- **Nome**: è possibile identificare facilmente un componente modulo con il suo nome univoco sia nel modulo che nell’editor di regole, ma il nome non deve contenere spazi o caratteri speciali.

- **Titolo** : con il relativo titolo è possibile identificare facilmente un componente in un modulo e, per impostazione predefinita, il titolo viene visualizzato sopra il componente. Se non aggiungi un titolo, al posto del testo del titolo viene visualizzato il nome del componente.

- **Consenti testo formattato per titolo**: questa funzione permette agli utenti di formattare i titoli in testo normale, incorporando opzioni come il grassetto, il corsivo, il testo sottolineato, vari font, dimensioni dei font, colori e altre opzioni per migliorare la presentazione visiva e la personalizzazione. Offre maggiore flessibilità e controllo creativo nel far risaltare i titoli all’interno di documenti, siti web o applicazioni.\
  Dopo aver selezionato la casella di controllo **Consenti testo formattato per titolo, le opzioni di formattazione diventano visibili per applicare lo stile al titolo del componente. Per accedere a tutte le opzioni di formattazione disponibili, fai clic sulla scheda ![Icona schermo intero](/help/adaptive-forms/assets/fullscreen-icon.png).

  ![Supporto testo RTF](/help/adaptive-forms/assets/richtext-support-title.png)

- **Nascondi titolo**: seleziona l’opzione per nascondere il titolo del componente.
- **Contrassegna come elemento modulo non associato**: seleziona l’opzione per configurare un campo modulo non collegato ad alcun schema. Questa opzione consente di salvare i dati senza aggiornare l’origine dati. Consente inoltre di gestire i dati in modo personalizzato, separato dall’integrazione standard del database.
- **Impostazioni di configurazione**: seleziona il contenitore di configurazione che contiene la configurazione cloud che connette AEM Forms al servizio reCAPTCHA di Google.

  >[!NOTE]
  >
  > Consulta l’articolo [Utilizzare Google reCAPTCHA in un modulo adattivo AEM basato su componenti core](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/captcha-adaptive-forms-core-components) per scoprire come creare e configurare Google reCAPTCHA per il tuo ambiente.

- **Tipo**: scegli questa opzione per selezionare le dimensioni per reCAPTCHA.
   - **Normale**: si riferisce alla versione standard e più grande del widget reCAPTCHA, che può essere più visibile e più facile con cui gli utenti di possono interagire, soprattutto sui dispositivi con schermi più grandi.
   - **Compatta**: fa riferimento a una versione più piccola del widget reCAPTCHA. Questa opzione è adatta per le situazioni in cui lo spazio è limitato, ad esempio su dispositivi mobili o in layout ristretti su pagine web.

- **Nascondi componente**: seleziona questa opzione per nascondere il componente del modulo. Il componente rimane accessibile per altri scopi, ad esempio per i calcoli nell’editor di regole. Questa funzione è utile quando devi memorizzare informazioni che non devono essere viste o modificate direttamente dall’utente.

- **Disattiva componente**: seleziona questa opzione per disabilitare il componente. Il componente disabilitato non è attivo o modificabile dall’utente finale. I dati del componente disabilitato non vengono inviati. L’utente può visualizzare il valore del campo ma non può modificarlo. Il componente rimane accessibile per altri scopi, ad esempio per i calcoli nell’editor di regole.

- **Sola lettura**: seleziona questa opzione per rendere il componente non modificabile. L’utente può visualizzare il valore del campo, ma non può modificarlo. Il componente rimane accessibile per altri scopi, ad esempio per i calcoli nell’editor di regole.

### Scheda Convalida {#validation-tab}

![Scheda Convalida](/help/adaptive-forms/assets/recaptcha-validationtab.png)

- **Messaggio di errore**: questa opzione consente di inserire un messaggio visualizzato se la casella di controllo **Obbligatorio** è selezionata e il campo modulo viene lasciato vuoto.

- **Messaggio di convalida script**: questa opzione consente di inserire un messaggio da visualizzare in caso di errore di convalida dello script.

## Finestra di dialogo per la progettazione {#design-dialog}

La finestra di dialogo per la progettazione viene utilizzata per definire e gestire gli stili CSS per il componente reCAPTCHA.

### Scheda Stili {#styles-design-tab}

Il componente core reCAPTCHA per i moduli adattivi supporta il [Sistema di stili](/help/get-started/authoring.md#component-styling) di AEM.

![Finestra di dialogo per la progettazione](/help/adaptive-forms/assets/checkbox-style.png)

- **Classi CSS predefinite**: è possibile fornire una classe CSS predefinita per il componente core reCAPTCHA per moduli adattivi.

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
