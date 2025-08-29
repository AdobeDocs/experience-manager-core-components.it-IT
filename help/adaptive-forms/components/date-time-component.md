---
title: Componente core Forms adattivo - Data e ora
description: Utilizzo o personalizzazione del componente core Data e ora di Forms adattivo.
role: Architect, Developer, Admin, User
source-git-commit: daeabccaff39e255c111c6af2540ca4d5be0c709
workflow-type: tm+mt
source-wordcount: '1898'
ht-degree: 74%

---


# Componente data e ora

Un componente Data e ora in un modulo adattivo è un elemento dell&#39;interfaccia utente che consente agli utenti di selezionare sia **data che ora** tramite un&#39;interfaccia calendario e orologio o immettendo manualmente i valori in un formato specifico. Garantisce un input accurato e standardizzato per i casi d’uso in cui sia la data che l’ora sono essenziali.

**Esempio**

![esempio](/help/adaptive-forms/assets/date-time-picker.png)

## Utilizzo {#reasons-to-use-date-time-picker}

Ci sono diversi motivi per cui è utile includere un selettore data e ora in un modulo, tra cui:

- **Comodità**: consente agli utenti di scegliere facilmente una data e un&#39;ora senza dover digitare manualmente i valori.
- **Coerenza**: applica un formato standard per gli input di data e ora nel modulo.
- **Esperienza utente migliorata**: fornisce un&#39;interfaccia utente intuitiva con selettori di calendario e ora.
- **Pianificazione eventi**: utile nei moduli di prenotazione appuntamenti, colloqui o pianificazione riunioni.
- **Viaggi e prenotazioni**: consente agli utenti di selezionare date e ore di check-in/check-out.
- **Precisione dei dati**: riduce gli errori di input rispetto all&#39;immissione di testo libero.

## Versione e compatibilità {#version-and-compatibility}

Il componente core Data e ora Forms adattivo è stato rilasciato **agosto 2025** come parte di **Componenti core 2.24.6** per Cloud Service e versioni successive.

| Versione del componente | AEM as a Cloud Service | AEM 6.5.16.0 Forms o versioni successive |
|---|---|---|
| v1 | Compatibile con <br>[versione 2.24.6](/help/adaptive-forms/version.md) e successive | |

Per informazioni dettagliate sulle versioni, consulta [Versioni dei Componenti core](/help/adaptive-forms/version.md).

## Dettagli tecnici {#technical-details}

Ottieni i dettagli tecnici più recenti sul componente core data e ora di Forms adattivo su [GitHub](https://github.com/adobe/aem-core-forms-components). Per ulteriori informazioni sullo sviluppo di Componenti core, consulta la [documentazione per gli sviluppatori di Componenti core](/help/developing/overview.md).

## Finestra di dialogo per la configurazione {#configure-dialog}

La finestra di dialogo per configurazione consente di personalizzare la data e l’ora.

### Scheda Base {#basic-tab}

![Scheda Base](/help/adaptive-forms/assets/datetime_basictab.png)

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
- **Data e ora predefinite** - Questa opzione consente di aggiungere una data e un&#39;ora al campo modulo. La data immessa viene visualizzata per impostazione predefinita nella posizione del componente. Se l&#39;utente non immette una data o un&#39;ora, questo valore viene inviato al momento dell&#39;invio del modulo. Se è selezionato **Componente disabilitato** o **Componente di sola lettura**, sullo schermo viene visualizzata la data e l&#39;ora predefinite e vengono inviate al momento dell&#39;invio del modulo.

### Scheda Convalida {#validation-tab}

![Scheda Convalida](/help/adaptive-forms/assets/datetime_validation.png)

- **Obbligatorio**: seleziona questa opzione se desideri visualizzare il componente in un modulo adattivo. Dopo aver selezionato l’opzione, è necessario effettuare una selezione prima di procedere con l’invio di un modulo. Non è possibile selezionare **Nascondi componente** o **Disattiva componente** nella scheda **Base** quando questa opzione è selezionata.

- **Messaggio di errore**: questa opzione consente di inserire un messaggio visualizzato se la casella di controllo **Obbligatorio** è selezionata e il campo modulo viene lasciato vuoto.

- **Messaggio di convalida script**: questa opzione consente di inserire un messaggio da visualizzare in caso di errore di convalida dello script.

- **Data minima**: questa opzione consente di inserire la data minima richiesta. Se si immette una data precedente a quella specificata in Data e ora minime, sullo schermo viene visualizzato un messaggio di errore. La finestra di dialogo **Messaggio di errore minimo** consente di aggiungere un messaggio di errore personalizzato.

- **Messaggio di errore minimo** - La finestra di dialogo **Messaggio di errore minimo** consente di aggiungere un messaggio di errore personalizzato da visualizzare, se si immette una data o un&#39;ora precedente alla data o all&#39;ora specificata nell&#39;opzione **Data minima**.

- **Data massima** - Questa opzione consente di immettere la data e l&#39;ora massime richieste. Se si immette una data o un&#39;ora successiva alla data o all&#39;ora specificata in Data massima, sullo schermo viene visualizzato un messaggio di errore. La finestra di dialogo **Messaggio di errore massimo** consente di aggiungere un messaggio di errore personalizzato.

- **Messaggio di errore massimo** - La finestra di dialogo **Messaggio di errore massimo** consente di aggiungere un messaggio di errore personalizzato da visualizzare, se si immette una data o un&#39;ora successiva alla data o all&#39;ora specificata nell&#39;opzione **Data massima**.

### Scheda Contenuto Guida {#help-content-tab}

![Scheda Contenuto Guida](/help/adaptive-forms/assets/datetime_helptab.png)

- **Breve descrizione**: una breve descrizione è una breve spiegazione testuale che fornisce informazioni aggiuntive o chiarimenti sullo scopo di un campo modulo specifico. Aiuta l’utente a capire quale tipo di dati deve essere immesso nel campo e può fornire linee guida o esempi per garantire che le informazioni immesse siano valide e soddisfino i criteri desiderati. Per impostazione predefinita, le descrizioni brevi rimangono nascoste. Seleziona l’opzione **Mostra sempre una breve descrizione** per visualizzarla sotto il componente.

- **Mostra sempre una breve descrizione**: seleziona l’opzione per visualizzare la descrizione breve sotto il componente.

- **Testo guida**: il testo guida si riferisce a informazioni o indicazioni aggiuntive fornite all’utente per aiutarlo a compilare correttamente un campo del modulo. Viene visualizzato quando l’utente fa clic sull’icona dell’aiuto (i) posta vicino al componente. Il testo guida fornisce informazioni più dettagliate rispetto all’etichetta o al testo segnaposto di un campo del modulo ed è progettato per consentire all’utente di comprendere i requisiti o i vincoli del campo. Può inoltre offrire suggerimenti o esempi per rendere più semplice e precisa la compilazione del modulo.


### Scheda Accessibilità {#accessibility-tab}

![Scheda Accessibilità](/help/adaptive-forms/assets/datetime_accessibilitytab.png)

- **Testo per utilità per la lettura dello schermo**: il testo per le utilità per la lettura dello schermo si riferisce al testo aggiuntivo destinato specificamente ad essere letto da tecnologie di assistenza, come le utilità per la lettura dello schermo, utilizzate da persone ipovedenti. Questo testo fornisce una descrizione audio dello scopo del campo modulo e può includere informazioni sul titolo, la descrizione, il nome del campo ed eventuali messaggi rilevanti (testo personalizzato). Il testo dell’assistente vocale consente di garantire l’accesso al modulo da parte di qualsiasi utente, comprese le persone ipovedenti, consentendo di comprendere appieno il campo del modulo e i relativi requisiti.
   - **Testo personalizzato**: seleziona questa opzione per utilizzare il testo personalizzato per le etichette di accessibilità ARIA. Selezionando questa opzione, viene visualizzata la finestra di dialogo Testo personalizzato. Puoi aggiungere informazioni rilevanti nella finestra di dialogo Testo personalizzato.
   - **Descrizione**: seleziona questa opzione per utilizzare la descrizione per le etichette di accessibilità ARIA.
   - **Titolo**: seleziona questa opzione per utilizzare il titolo per le etichette di accessibilità ARIA.
   - **Nome**: seleziona questa opzione per utilizzare il nome per le etichette di accessibilità ARIA.
   - **Nessuno**: seleziona questa opzione in caso tu non voglia aggiungere etichette di accessibilità ARIA.

<!--
### Formats Tab {#format-tab}

![Formats tab](/help/adaptive-forms/assets/datepicker_formattab.png)

-   **Display Format** - It represents the date format that is displayed to the user. The **Type** option allows the user to select the date format. You can also customize the date format using the **Custom** option in the **Type** dropdown menu.

-   **Edit Format** - It represents a date format in which the user can edit the date. The **Type** option allows the user to select the date format. You can also customize the date format using the **Custom** option in the **Type** dropdown menu.
-  **Format error message** - This option allows you to enter the message displayed on the screen when the entered date is not in the correct format.
- **Language** - This feature is used for formatting the specific field. When a user selects any language option from the **Type** drop-down menu, the **IETF BCP 47 language tag** option appears in the panel. You can choose the language for field formatting when translating an Adaptive Form into a specific language.
  
The set of languages is not visible by default, but users can input a custom **IETF BCP 47 language tag** by updating the template policy:

  1. Open the corresponding template associated with an Adaptive Form in the template editor.
  2. Select the existing policy as `datepicker-default-policy` from the drop-down menu.
   
        ![Date Picker template Policy](/help/adaptive-forms/assets/date-picker-template-policy.png)

  3. Click **Done**.

        >[!NOTE]
        >
        > For further information on how to translate an Adaptive Form to a specific locale, [click here](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/supporting-new-language-localization-core-components).
-->

## Finestra di dialogo per la progettazione {#design-dialog}

La finestra di dialogo per progettazione viene utilizzata per definire e gestire gli stili CSS per il componente Data e ora.

### Scheda Stili {#styles-tab}

La scheda è utilizzata per definire e gestire gli stili CSS per un componente. Il componente core Data e ora di Forms adattivo supporta il [sistema di stili](/help/get-started/authoring.md#component-styling) di AEM.

![Scheda Stile](/help/adaptive-forms/assets/datepicker_styletab.png)

- **Classi CSS predefinite**: è possibile fornire una classe CSS predefinita per il componente core data e ora di Forms adattivo.

- **Stili consentiti**: è possibile definire gli stili fornendo un nome e la classe CSS che rappresenta lo stile. Ad esempio, puoi creare uno stile denominato “testo in grassetto” e fornire la classe CSS “spessore carattere: grassetto”. Puoi utilizzare o applicare questi stili a un modulo adattivo nell’editor di moduli adattivi. Per applicare uno stile, nell’editor dei moduli adattivi, seleziona il componente a cui applicare lo stile, passa alla finestra di dialogo delle proprietà e seleziona lo stile desiderato dall’elenco a discesa **Stili**. Per aggiornare o modificare gli stili, è sufficiente tornare alla finestra di dialogo per la progettazione, aggiornare gli stili nella scheda Stili e salvare le modifiche.

### Proprietà personalizzate

![Finestra di dialogo Proprietà personalizzate](/help/adaptive-forms/assets/datepicker_customproperties.png)

Le proprietà personalizzate consentono di associare attributi personalizzati (coppie chiave-valore) a un componente core del modulo adattivo utilizzando il modello di modulo. Le proprietà personalizzate vengono riflesse nella sezione delle proprietà della rappresentazione headless del componente. Consentono di creare un comportamento di modulo dinamico che si adatta in base ai valori degli attributi personalizzati. Ad esempio, gli sviluppatori possono progettare diverse rappresentazioni di un componente moduli headless su piattaforme mobili, desktop o web, migliorando in modo significativo l’esperienza utente su un’ampia gamma di dispositivi.

- **Nome gruppo**: puoi fornire un nome per identificare il gruppo di proprietà personalizzate. È possibile aggiungere, eliminare o ridisporre più gruppi di proprietà personalizzate. Dopo aver aggiunto il gruppo di proprietà personalizzate, puoi visualizzare le seguenti opzioni:

   - **Coppie chiave-valore**: puoi aggiungere più nomi e valori della proprietà personalizzata facendo clic sul pulsante **Aggiungi** per ogni gruppo di proprietà personalizzate.

   - **Elimina**: tocca o fai clic per eliminare il nome e il valore della proprietà personalizzata.

   - **Ridisponi**: tocca o fai clic e trascina per ridisporre l’ordine del nome e del valore della proprietà personalizzata.

<!--
### Formats Tab {#formats-tab}

The formats tab allows you to specify default and custom date formats.

![Formattab](/help/adaptive-forms/assets/datepicker_formatpolicy.png)



## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html?lang=it)

-->

## Articoli correlati {#related-articles}

{{more-like-this}}

## Consulta anche {#see-also}

{{see-also}}


