---
title: Abilitare e utilizzare i pattern di convalida dell’input di testo nei moduli adattativi di Adobe Experience Manager
description: Scopri come configurare i criteri dei modelli per esporre i pattern di convalida come numeri di telefono, numeri di previdenza sociale e codici postali, per poi utilizzarli nei tuoi moduli adattativi.
hide: true
exl-id: e4500666-1346-4558-861d-da9541dcef51
source-git-commit: 59064c359aea14af99675709bbddf9a933a959df
workflow-type: ht
source-wordcount: '861'
ht-degree: 100%

---

# Abilitare e utilizzare i pattern di convalida dell’input di testo nei moduli adattativi di Adobe Experience Manager

## Panoramica

Nei moduli di Adobe Experience Manager (Adobe Experience Manager), i formati di convalida specifici (come i numeri di previdenza sociale, gli indirizzi e-mail o i codici postali) dei componenti Input di testo sono controllati a livello di Criterio del modello. Questa guida spiega come:

1. Accedere all’editor modelli e configurare il criterio del componente Input di testo per esporre i pattern di convalida.
2. Creare un modulo adattivo e applicare tali pattern di convalida a un componente Input di testo.

## Prerequisiti

- Accesso a un’istanza di Adobe Experience Manager con i moduli abilitati.
- Autorizzazioni per la modifica dei modelli (solitamente fanno parte del gruppo `template-authors`).
- Autorizzazioni per creare e modificare i moduli adattativi.

## Parte 1: Abilitare i pattern di convalida nel modello

>[!VIDEO](https://video.tv.adobe.com/v/3480390/)

### Passaggio 1: accedere alla console dei modelli

1. Dalla schermata Home di Adobe Experience Manager, fai clic su **Strumenti** (icona a forma di martello) nella barra laterale di sinistra.
2. Passa a **Impostazioni generali > Modelli**.
3. Seleziona la cartella contenente i tuoi modelli di progetto (ad esempio, Esempi di componenti core).
4. Individua il modello specifico che desideri modificare (ad esempio, AF vuoto) e selezionalo.
5. Fai clic su **Modifica** (o apri direttamente il modello).

### Passaggio 2: accedere alla struttura dei componenti

1. Verifica di essere nella vista **Struttura** (se necessario, seleziona &quot;Struttura&quot; dal menu a discesa delle modalità in alto a destra).
2. Individua il **Contenitore di layout** principale o il contenitore specifico in cui è consentito il tuo componente di Immissione testo.
3. Fai clic sul contenitore per visualizzare l’elenco dei componenti consentiti.
4. Trova il componente **Casella di testo modulo adattivo** nell’elenco.
5. Fai clic sull’icona **Criterio** (rappresentata da un simbolo di file/cassetto) accanto al nome del componente.

### Passaggio 3: configurare il criterio del componente Immissione testo

1. Nell’editor del criterio, fai clic sulla scheda **Formati** sul lato destro della finestra.
2. Verrà visualizzato un elenco dei modelli di convalida disponibili. Seleziona le caselle relative ai formati che desideri attivare:
   - Numero di telefono
   - Numero di previdenza sociale
   - Formato alfanumerico e-mail
   - Codice postale

### Passaggio 4: definire e salvare il criterio

1. Torna alla scheda **Criteri** (oppure controlla le impostazioni a sinistra).
2. Nel campo **Titolo criterio**, immetti un nome evidente (ad esempio, `new-textinput-default-policy`).
3. Fai clic sull’icona (segno di spunta) **Fine** nell’angolo in alto a destra per salvare le modifiche.

## Parte 2: Creare un modulo e utilizzare i modelli di convalida

Ora che i modelli di convalida sono abilitati nel modello, puoi creare un modulo adattivo e applicarli ai componenti di Immissione testo.

>[!VIDEO](https://video.tv.adobe.com/v/3480391/)

### Passaggio 1: creare un modulo adattivo

1. Passa all’interfaccia **Moduli e documenti**.
2. Fai clic sul pulsante **Crea** nell’angolo in alto a destra.
3. Seleziona **Modulo adattivo** dalle opzioni a discesa.
4. Scegli il modello in cui hai abilitato i modelli di convalida (ad esempio, **Vuoto**) e fai clic su **Avanti**.
5. Nella schermata Aggiungi proprietà:
   - Inserisci un **Titolo** per il modulo (ad esempio, &quot;testPolicy&quot;). Il campo **Nome** viene popolato automaticamente in base al titolo.
   - Verifica che sia selezionata la **libreria client dei temi** corretta (ad esempio, `adaptiveform.theme.canvas3`).
6. Fai clic su **Crea**. Viene visualizzato un messaggio di operazione riuscita.
7. Fai clic su **Modifica** per aprire il modulo nell’editor.

### Passaggio 2: aggiungere un componente Immissione di testo

1. Nell’editor dei moduli, individua il browser **Componenti** nella barra laterale di sinistra.
2. Utilizza la barra di ricerca per trovare il componente **Casella di testo modulo adattivo**. Digitando &quot;testo&quot; si filtra l’elenco.
3. Fai clic e trascina il componente **Casella di testo modulo adattivo** nell’area di lavoro principale.

### Passaggio 3: configurare la formattazione dei componenti

1. Fai clic sul componente **Immissione testo** appena aggiunto per selezionarlo.
2. Fai clic sull’icona **Configura** (rappresentata da una chiave inglese) nella barra degli strumenti visualizzata sopra il componente.
3. Nella finestra di dialogo delle proprietà, passa alla scheda **Formati**.
4. Individua il menu a discesa **Tipo** e modifica la selezione in **Numero di telefono** (o in un altro formato abilitato).

### Passaggio 4: configurare la convalida dei dati

1. Nella finestra di dialogo di configurazione del componente, passa alla scheda **Convalida**.
2. Individua la sezione **Modello di convalida**.
3. Fai clic sul menu a discesa **Tipo**.
4. Seleziona **Numero di telefono** dall’elenco dei modelli di convalida. In questo modo il modulo genera un errore se l’utente immette un testo che non corrisponde a un formato numero di telefono valido.
5. Fai clic sull’icona (segno di spunta) **Fine** in alto a destra nella finestra di dialogo per salvare le modifiche.

## Verifica

Per verificare il corretto funzionamento dei modelli di convalida:

1. Mostra l’anteprima del modulo nell’editor.
2. Immetti i dati di test nel componente **Immissione testo**.
3. Conferma che:
   - I modelli di convalida abilitati sono visualizzati nelle schede Formati e Convalida del componente.
   - L’immissione non valida dà luogo a opportuni messaggi di errore.
   - L’immissione valida è accettata senza errori.

## Risoluzione dei problemi

- **Problema:** i modelli di convalida non sono visualizzati nel componente modulo.
   - **Soluzione:** verifica che i criteri del modello siano stati salvati correttamente e che stai utilizzando il modello corretto durante la creazione del modulo.

- **Problema:** impossibile accedere all’editor dei modelli.
   - **Soluzione:** verifica di disporre delle autorizzazioni necessarie per modificare i modelli (appartenenza al gruppo `template-authors`).

- **Problema:** il componente Immissione testo non convalida correttamente l’immissione.
   - **Soluzione:** ricontrolla le impostazioni del modello di convalida nella scheda Convalida del componente e assicurati che sia selezionato il modello corretto.

## Passaggi successivi

Dopo aver abilitato e utilizzato i modelli di convalida dell’immissione testo nei moduli adattativi di Adobe Experience Manager:

- Configura modelli di convalida aggiuntivi per altri tipi di dati.
- Esplora altri criteri dei componenti per personalizzare il comportamento dei moduli.
- Imposta la gestione dell’invio dei moduli e la logica di elaborazione dati.
