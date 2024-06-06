---
title: Componente core moduli adattivi - Selettore data
description: Utilizzo o personalizzazione del componente core del selettore data dei moduli adattivi.
role: Architect, Developer, Admin, User
exl-id: aa9402de-ca57-4c19-8d36-2dd0a78d6806
source-git-commit: b4a66a407e92398a98441c65ab588b9720777dfa
workflow-type: tm+mt
source-wordcount: '2299'
ht-degree: 93%

---

# Componente selettore data{#date-picker-adaptive-forms-core-component}

Un componente selettore di data in un modulo adattivo è un elemento dell’interfaccia utente che consente agli utenti di selezionare una data da un calendario o di inserire manualmente una data in un formato specifico. Il componente selettore di data può essere configurato in modo da avere diversi valori di formattazione, convalida e impostazione predefinita.

**Esempio**

![esempio](/help/adaptive-forms/assets/date-picker.png)

## Utilizzo {#reasons-to-use-drop-date-picker}

Ci sono diversi motivi per cui è utile includere un selettore di data in un modulo adattivo, tra cui:

- **Comodità**: un componente selettore di data consente agli utenti di selezionare facilmente una data da un calendario senza doverla inserire manualmente in un campo di testo. In questo modo è possibile risparmiare tempo e ridurre gli errori.

- **Esperienza utente**: il componente selettore di data può facilitare l’uso del modulo, fornendo agli utenti un modo chiaro e intuitivo per selezionare la data.

- **Analisi dei dati**: il componente selettore di data può essere utilizzato per raccogliere dati da varie sorgenti e analizzarli oppure per utilizzarli come input per un’ulteriore elaborazione.

- **Gestione eventi**: il componente selettore di data può essere utilizzato nei siti web di gestione eventi per selezionare la data dell’evento.

- **Prenotazione**: il componente selettore di data può essere utilizzato nei siti web di prenotazione per selezionare le date di arrivo e partenza.

- **Formato data**: il componente selettore di data può essere utilizzato per correggere il formato in cui la data viene visualizzata e inserita. Assicurati che il formato della data sia coerente in tutto il modulo per garantire un’esperienza utente coerente.

## Versione e compatibilità {#version-and-compatibility}

Il componente core Pannello a soffietto moduli adattativi è stato rilasciato a febbraio 2023 come parte dei Componenti core 2.0.4 per Cloud Service e i Componenti core 1.1.12 per AEM Forms 6.5.16.0 o versioni successive. Di seguito è riportata una tabella che mostra tutte le versioni supportate, la compatibilità AEM e i collegamenti alla documentazione corrispondente:

| Versione del componente | AEM as a Cloud Service | AEM Forms 6.5.16.0 o versioni successive |
|---|---|---|
| v1 | Compatibile con <br>[versione 2.0.4](/help/adaptive-forms/version.md) e successive | Compatibile con <br>[versione 1.1.12](/help/adaptive-forms/version.md) e successive, ma precedenti a 2.0.0. |

Per informazioni sulle versioni dei componenti core, consulta il documento [Versioni dei componenti core](/help/adaptive-forms/version.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Dettagli tecnici {#technical-details}

Ottieni le informazioni più recenti sul componente core del selettore data dei moduli adattivi nella documentazione tecnica su [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/datepicker/v1/datepicker). Per ulteriori informazioni sullo sviluppo dei componenti core, consulta la [Documentazione per gli sviluppatori di componenti core](/help/developing/overview.md).

## Finestra di dialogo per la configurazione {#configure-dialog}

Puoi personalizzare facilmente l’esperienza del selettore data per gli utenti tramite la finestra di dialogo Configura. Puoi anche definire le opzioni del selettore data con facilità per un’esperienza di utilizzo semplice.

### Scheda Base {#basic-tab}

![Scheda Base](/help/adaptive-forms/assets/datepicker_basictab.png)

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
- **Sola lettura**: seleziona questa opzione per rendere il componente non modificabile. L’utente può visualizzare il valore del campo, ma non può modificarlo. Il componente rimane accessibile per altri scopi, ad esempio per i calcoli nell’editor di regole.
- **Data predefinita**: questa opzione consente di aggiungere una data al campo del modulo. La data immessa viene visualizzata per impostazione predefinita nella posizione del componente. Se l’utente non immette alcuna data, questo valore viene inviato al momento dell’invio del modulo. Nel caso in cui **Componente disabilitato** o **Componente di sola lettura** sia selezionato, la data predefinita viene visualizzata sullo schermo e inviata al momento dell’inoltro del modulo.


### Scheda Convalida {#validation-tab}

![Scheda Convalida](/help/adaptive-forms/assets/datepicker_validation.png)

- **Obbligatorio**: seleziona questa opzione se desideri visualizzare il componente in un modulo adattivo. Dopo aver selezionato l’opzione, è necessario effettuare una selezione prima di procedere con l’invio di un modulo. Non è possibile selezionare **Nascondi componente** o **Disattiva componente** nella scheda **Base** quando questa opzione è selezionata.

- **Messaggio di errore**: questa opzione consente di inserire un messaggio visualizzato se la casella di controllo **Obbligatorio** è selezionata e il campo modulo viene lasciato vuoto.

- **Messaggio di convalida script**: questa opzione consente di inserire un messaggio da visualizzare in caso di errore di convalida dello script.

- **Data minima**: questa opzione consente di inserire la data minima richiesta. Se immetti una data precedente alla data specificata in Data minima, sullo schermo viene visualizzato un messaggio di errore. La finestra di dialogo **Messaggio di errore minimo** consente di aggiungere un messaggio di errore personalizzato.

- **Messaggio di errore minimo**: la finestra di dialogo **Messaggio di errore minimo** permette di aggiungere un messaggio di errore personalizzato da mostrare se si inserisce una data precedente alla data specificata nell’opzione **Data minima**.
- **Escludi data minima**: questa opzione consente di omettere la data minima in un determinato intervallo o set di date.

- **Data massima**: questa opzione consente di inserire la data massima richiesta. Se immetti una data successiva alla data specificata in Data massima, sullo schermo viene visualizzato un messaggio di errore. La finestra di dialogo **Messaggio di errore massimo** consente di aggiungere un messaggio di errore personalizzato.

- **Messaggio di errore massimo**: la finestra di dialogo **Messaggio di errore massimo** consente di aggiungere un messaggio di errore personalizzato da visualizzare, se si immette una data successiva alla data specificata nell’opzione **Data massima**.

- **Escludi data massima**: questa opzione consente di omettere la data massima in un determinato intervallo o set di date.

### Scheda Contenuto Guida {#help-content-tab}

![Scheda Contenuto Guida](/help/adaptive-forms/assets/datepicker_helptab.png)

- **Breve descrizione**: una breve descrizione è una breve spiegazione testuale che fornisce informazioni aggiuntive o chiarimenti sullo scopo di un campo modulo specifico. Aiuta l’utente a capire quale tipo di dati deve essere immesso nel campo e può fornire linee guida o esempi per garantire che le informazioni immesse siano valide e soddisfino i criteri desiderati. Per impostazione predefinita, le descrizioni brevi rimangono nascoste. Seleziona l’opzione **Mostra sempre una breve descrizione** per visualizzarla sotto il componente.

- **Mostra sempre una breve descrizione**: seleziona l’opzione per visualizzare la descrizione breve sotto il componente.

- **Testo guida**: il testo guida si riferisce a informazioni o indicazioni aggiuntive fornite all’utente per aiutarlo a compilare correttamente un campo del modulo. Viene visualizzato quando l’utente fa clic sull’icona dell’aiuto (i) posta vicino al componente. Il testo guida fornisce informazioni più dettagliate rispetto all’etichetta o al testo segnaposto di un campo del modulo ed è progettato per consentire all’utente di comprendere i requisiti o i vincoli del campo. Può inoltre offrire suggerimenti o esempi per rendere più semplice e precisa la compilazione del modulo.


### Scheda Accessibilità {#accessibility-tab}

![Scheda Accessibilità](/help/adaptive-forms/assets/datepicker_accessibilitytab.png)

- **Testo per utilità per la lettura dello schermo**: il testo per le utilità per la lettura dello schermo si riferisce al testo aggiuntivo destinato specificamente ad essere letto da tecnologie di assistenza, come le utilità per la lettura dello schermo, utilizzate da persone ipovedenti. Questo testo fornisce una descrizione audio dello scopo del campo modulo e può includere informazioni sul titolo, la descrizione, il nome del campo ed eventuali messaggi rilevanti (testo personalizzato). Il testo dell’assistente vocale consente di garantire l’accesso al modulo da parte di qualsiasi utente, comprese le persone ipovedenti, consentendo di comprendere appieno il campo del modulo e i relativi requisiti.
   - **Testo personalizzato**: seleziona questa opzione per utilizzare il testo personalizzato per le etichette di accessibilità ARIA. Selezionando questa opzione, viene visualizzata la finestra di dialogo Testo personalizzato. Puoi aggiungere informazioni rilevanti nella finestra di dialogo Testo personalizzato.
   - **Descrizione**: seleziona questa opzione per utilizzare la descrizione per le etichette di accessibilità ARIA.
   - **Titolo**: seleziona questa opzione per utilizzare il titolo per le etichette di accessibilità ARIA.
   - **Nome**: seleziona questa opzione per utilizzare il nome per le etichette di accessibilità ARIA.
   - **Nessuno**: Seleziona questa opzione se non desideri aggiungere le etichette di accessibilità ARIA.

### Scheda Formati {#format-tab}

![Scheda Formati](/help/adaptive-forms/assets/datepicker_formattab.png)

- **Formato visualizzato**: rappresenta il formato della data visualizzato dall’utente. L’opzione **Tipo** consente all’utente di selezionare il formato della data. È inoltre possibile personalizzare il formato della data utilizzando l’opzione **Personalizza** nel menu a discesa **Tipo**.

- **Modifica formato**: rappresenta un formato di data in cui l’utente può modificare la data. L’opzione **Tipo** consente all’utente di selezionare il formato della data. È inoltre possibile personalizzare il formato della data utilizzando l’opzione **Personalizza** nel menu a discesa **Tipo**.
- **Messaggio di errore Formato** - Questa opzione consente di immettere il messaggio visualizzato sullo schermo quando la data immessa non è nel formato corretto.
- **Lingua** - Questa funzione viene utilizzata per la formattazione del campo specifico. Quando un utente seleziona un’opzione di lingua dalla **Tipo** menu a discesa, il **Tag lingua IETF BCP 47** nel pannello. È possibile scegliere la lingua per la formattazione dei campi durante la traduzione di un modulo adattivo in una lingua specifica.

Il set di lingue non è visibile per impostazione predefinita, ma gli utenti possono immettere un **Tag lingua IETF BCP 47** aggiornando il criterio del modello:

1. Apri il modello corrispondente associato a un modulo adattivo nell’editor di modelli.
2. Seleziona il criterio esistente come `datepicker-default-policy` dal menu a discesa.

   ![Criterio modello selettore data](/help/adaptive-forms/assets/date-picker-template-policy.png)

3. Clic **Fine**.

   >[!NOTE]
   >
   > Per ulteriori informazioni su come tradurre un modulo adattivo in una lingua specifica, [fai clic qui](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/supporting-new-language-localization-core-components).

## Finestra di dialogo per la progettazione {#design-dialog}

La finestra di dialogo per la progettazione consente di definire e gestire gli stili CSS per il componente Selettore data.

### Scheda Stili {#styles-tab}

La scheda è utilizzata per definire e gestire gli stili CSS per un componente. Il componente core selettore data dei moduli adattivi supporta il [Sistema di stili](/help/get-started/authoring.md#component-styling) di AEM.

![Scheda Stile](/help/adaptive-forms/assets/datepicker_styletab.png)

- **Classi CSS predefinite**: è possibile fornire una classe CSS predefinita per il componente core selettore data dei moduli adattivi.

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

![Scheda formato](/help/adaptive-forms/assets/datepicker_formatpolicy.png)

<!--

## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html)

-->

## Articoli correlati {#related-articles}

{{more-like-this}}

## Consulta anche {#see-also}

{{see-also}}


