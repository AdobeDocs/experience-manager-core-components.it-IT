---
title: 'Componente core dei moduli adattivi: componente revisione'
description: Utilizzo o personalizzazione del componente core di revisione dei moduli adattivi.
role: Architect, Developer, Admin, User
hide: true
hidefromtoc: true
source-git-commit: 04a685cfa2616839f4fec715847bf0821808bd59
workflow-type: ht
source-wordcount: '742'
ht-degree: 100%

---


# Componente revisione

Il componente revisione nei moduli adattivi consente agli utenti di rivedere e verificare le informazioni immesse prima di inviare il modulo. Funge da pagina di riepilogo e fornisce una visualizzazione in sola lettura di tutti i campi e dei relativi valori in un formato strutturato e intuitivo. Questa funzione garantisce che gli utenti possano identificare e correggere eventuali errori o omissioni prima di finalizzare l’invio, migliorando l’esperienza complessiva del modulo. Facendo clic sull’icona di modifica, possono modificare le informazioni immesse prima dell’invio del modulo.

**Esempio**

![Componente di revisione](/help/adaptive-forms/assets/review-component.png){width=50%, align=center}

## Utilizzo

Esistono diversi motivi per utilizzare il componente di revisione in un modulo adattivo:

- **Miglioramento della precisione dei dati**: il componente di revisione consente agli utenti di rivedere tutti i dati immessi prima dell’invio. Ciò contribuisce a ridurre le possibilità di errori o omissioni, garantendo l’accuratezza dei dati inviati.
- **Esperienza utente migliorata**: gli utenti ottengono un riepilogo chiaro e organizzato di tutte le informazioni che hanno compilato, dando loro la certezza che il modulo è completo e accurato prima dell’invio finale, migliorando l’esperienza complessiva.
- **Rilevamento e correzione degli errori**: consente di modificare le informazioni a livello di pannello o di campo, consentendo agli utenti di correggere gli errori senza tornare indietro attraverso più schede. Facendo clic sull’icona **Modifica** accanto a un pannello o a un campo, è facile tornare indietro e risolvere eventuali problemi.
- **Maggiore fiducia dell’utente**: gli utenti possono rivedere i dati immessi, assicurandosi che le informazioni inviate siano corrette, con conseguente riduzione degli errori di invio e maggiore fiducia nelle funzionalità del modulo.
- **Impedimento di invii non intenzionali**: gli utenti spesso fanno clic su **Invia** senza rivedere tutti i dettagli. Il componente **Rivedi** offre agli utenti un’ultima possibilità di verifica dei dati, riducendo la probabilità di invii non intenzionali.


## Dettagli tecnici {#technical-details}

Puoi ottenere le informazioni più recenti sul componente core di revisione dei moduli adattivi nella documentazione tecnica su [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/textinput/v1/textinput). Per ulteriori informazioni sullo sviluppo dei componenti core, consulta la [Documentazione per gli sviluppatori dei componenti core](/help/developing/overview.md).

## Finestra di dialogo per la configurazione {#configure-dialog}

Puoi personalizzare facilmente l’esperienza per i visitatori tramite la finestra di dialogo per la configurazione, offrendo un’esperienza utente fluida.

![Finestra di dialogo per la configurazione](/help/adaptive-forms/assets/review-component-configure-dialog.png)

- **Nome**: è possibile identificare facilmente un componente modulo con il suo nome univoco sia nel modulo che nell’editor di regole, ma il nome non deve contenere spazi o caratteri speciali.

- **Titolo** : con il relativo titolo è possibile identificare facilmente un componente in un modulo e, per impostazione predefinita, il titolo viene visualizzato sopra il componente. Se non aggiungi un titolo, al posto del testo del titolo viene visualizzato il nome del componente.
- **Nascondi titolo**: seleziona l’opzione per nascondere il titolo del componente.
- **Abilita azioni modalità di modifica per**: le opzioni **Abilita azioni modalità di modifica per** consentono agli utenti di modificare le informazioni immesse. Gli utenti possono modificare le informazioni a livello di campo o di pannello.
   - Quando gli utenti selezionano l’opzione **Campo**, possono modificare singoli campi modulo durante la revisione.
   - Quando gli utenti selezionano l’opzione **Pannello**, possono modificare tutti i campi all’interno di una sezione specifica (pannello).
   - Quando gli utenti selezionano l’opzione **Campo e pannello**, possono fare clic sull’icona di modifica accanto a un campo per modificare informazioni specifiche o accanto a un pannello per modificare tutti i campi all’interno di tale pannello.
   - Quando gli utenti selezionano l’opzione **Nessuno**, possono modificare qualsiasi campo o pannello all’interno dell’intero modulo.

  Per impostazione predefinita, è selezionata l’opzione **Pannello**.

- **Collega pannelli**: l’opzione **Collega pannelli** consente agli utenti di selezionare i pannelli da rivedere. Quando i pannelli sono collegati, gli utenti possono rivedere le informazioni immesse dei pannelli selezionati e modificarle prima dell’invio.

## Caso d’uso

Prendi ad esempio un **modulo di richiesta di prestito** composto da quattro schede, in cui ogni scheda raccoglie informazioni specifiche sull’utente:

- **Dettagli personali**: raccoglie i dati personali di base dell’utente, quali nome, data di nascita, informazioni di contatto e indirizzo.

- **Dettagli prestito**: raccoglie informazioni relative al prestito, tra cui il tipo di prestito, l’importo desiderato, il periodo di rimborso e campi calcolati automaticamente come il tasso di interesse e l’EMI mensile.

- **Documenti aggiuntivi**: consente all’utente di caricare i documenti richiesti, ad esempio la bozza dell’ID, dell’indirizzo e della dichiarazione di reddito. Include inoltre una casella di controllo della dichiarazione per confermare l’accettazione dei termini.

- **Rivedi e invia modulo**: un componente di revisione riepiloga tutti gli input delle schede precedenti. Gli utenti possono verificare e modificare i propri dati prima di inviare il modulo. Questa scheda include anche il pulsante **Invia** per inviare la richiesta.

Il video seguente illustra come configurare il componente di **revisione** in modo che l’utente abbia la flessibilità di modificare le informazioni:

## Articoli correlati {#related-articles}

{{more-like-this}}

## Consulta anche {#see-also}

{{see-also}}

