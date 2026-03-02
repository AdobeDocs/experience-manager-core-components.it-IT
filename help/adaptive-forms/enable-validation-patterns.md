---
title: Abilitare e utilizzare i modelli di convalida dell’input di testo in Adobe Experience Manager Adaptive Forms
description: Scopri come configurare i criteri dei modelli per esporre pattern di convalida come numeri di telefono, numeri di previdenza sociale e codici postali, e quindi utilizzarli nel Forms adattivo.
hide: true
hidefromtoc: true
source-git-commit: 1ac3d987337f8279e762ab5357d32bb732dea0be
workflow-type: tm+mt
source-wordcount: '861'
ht-degree: 1%

---


# Abilitare e utilizzare i modelli di convalida dell’input di testo in Adobe Experience Manager Adaptive Forms

## Panoramica

In Adobe Experience Manager (Adobe Experience Manager) Forms, formati di convalida specifici (come i numeri di previdenza sociale, gli indirizzi e-mail o i codici postali) per i componenti Input testo sono controllati a livello di Criterio modello. Questa guida spiega come:

1. Accedi all’editor di modelli e configura il criterio del componente Input di testo per esporre i modelli di convalida.
2. Crea un modulo adattivo e applica i modelli di convalida a un componente Input di testo.

## Prerequisiti

- Accesso a un’istanza di Adobe Experience Manager con Forms abilitato.
- Autorizzazioni per la modifica dei modelli (in genere fanno parte del gruppo `template-authors`).
- Autorizzazioni per creare e modificare Forms adattivo.

## Parte 1: Abilitare i modelli di convalida nel modello

>[!VIDEO](https://video.tv.adobe.com/v/3480390/)

### Passaggio 1: accedere alla console Modelli

1. Dalla schermata iniziale di Adobe Experience Manager, fai clic su **Strumenti** (icona a forma di martello) nella barra laterale a sinistra.
2. Passa a **Generale > Modelli**.
3. Seleziona la cartella contenente i modelli di progetto (ad esempio, Esempi di Componenti core).
4. Individuare il modello specifico che si desidera modificare (ad esempio, AF vuoto) e selezionarlo.
5. Fai clic su **Modifica** (o apri direttamente il modello).

### Passaggio 2: accedere alla struttura dei componenti

1. Verifica di essere nella visualizzazione **Struttura** (se necessario, seleziona &quot;Struttura&quot; dal menu a discesa della modalità in alto a destra).
2. Individua il **Contenitore di layout** principale o il contenitore specifico in cui è consentito il componente di input di testo.
3. Fai clic sul contenitore per visualizzare l’elenco dei componenti consentiti.
4. Trova il componente **Casella di testo modulo adattivo** nell&#39;elenco.
5. Fare clic sull&#39;icona **Criterio** (rappresentata da un simbolo di file/cassetto) accanto al nome del componente.

### Passaggio 3: configurare il criterio del componente Input di testo

1. Nell&#39;editor dei criteri fare clic sulla scheda **Formati** sul lato destro della finestra.
2. Verrà visualizzato un elenco dei modelli di convalida disponibili. Selezionare le caselle relative ai formati che si desidera attivare:
   - Numero di telefono
   - Numero di previdenza sociale
   - Formato alfanumerico e-mail
   - Codice postale

### Passaggio 4: definire e salvare il criterio

1. Torna alla scheda **Criteri** (oppure controlla le impostazioni a sinistra).
2. Nel campo **Titolo criterio** immettere un nome non crittografato, ad esempio `new-textinput-default-policy`.
3. Fai clic sull&#39;icona **Fine** (segno di spunta) nell&#39;angolo in alto a destra per salvare le modifiche.

## Parte 2: Creazione di una maschera e utilizzo di modelli di convalida

Ora che i modelli di convalida sono abilitati nel modello, puoi creare un modulo adattivo e applicarli ai componenti Input testo.

>[!VIDEO](https://video.tv.adobe.com/v/3480391/)

### Passaggio 1: creare un modulo adattivo

1. Passare all&#39;interfaccia **Forms e documenti**.
2. Fai clic sul pulsante **Crea** in alto a destra.
3. Seleziona **Modulo adattivo** dalle opzioni a discesa.
4. Scegli il modello in cui hai abilitato i modelli di convalida (ad esempio, **Vuoto**) e fai clic su **Successivo**.
5. Nella schermata Aggiungi proprietà:
   - Immetti un **Titolo** per il modulo (ad esempio, &quot;testPolicy&quot;). Il campo **Name** viene compilato automaticamente in base al titolo.
   - Verificare che sia selezionata la **libreria client tema** corretta (ad esempio, `adaptiveform.theme.canvas3`).
6. Fai clic su **Crea**. Viene visualizzato un messaggio di operazione riuscita.
7. Fai clic su **Modifica** per aprire il modulo nell&#39;editor.

### Passaggio 2: aggiungere un componente per l’immissione di testo

1. Nell&#39;editor dei moduli, individua il browser **Componenti** nella barra laterale a sinistra.
2. Utilizzare la barra di ricerca per trovare il componente **Casella di testo modulo adattivo**. Digitando &quot;text&quot; si filtra l’elenco.
3. Fare clic e trascinare il componente **Casella di testo modulo adattivo** nell&#39;area di lavoro principale.

### Passaggio 3: configurare la formattazione dei componenti

1. Fai clic sul componente **Input testo** appena aggiunto per selezionarlo.
2. Fai clic sull&#39;icona **Configura** (rappresentata da una chiave inglese) nella barra degli strumenti visualizzata sopra il componente.
3. Nella finestra di dialogo delle proprietà, passa alla scheda **Formati**.
4. Individua il menu a discesa **Tipo** e modifica la selezione in **Numero di telefono** (o in un altro formato abilitato).

### Passaggio 4: configurare la convalida dei dati

1. Nella finestra di dialogo di configurazione del componente, passa alla scheda **Convalida**.
2. Individuare la sezione **Pattern di convalida**.
3. Fare clic sul menu a discesa **Tipo**.
4. Selezionare **Numero di telefono** dall&#39;elenco dei modelli di convalida. In questo modo il modulo genera un errore se l&#39;utente immette testo che non corrisponde a un formato numero di telefono valido.
5. Fai clic sull&#39;icona **Fine** (segno di spunta) in alto a destra della finestra di dialogo per salvare le modifiche.

## Verifica

Per verificare il corretto funzionamento dei modelli di convalida:

1. Visualizza l’anteprima del modulo nell’editor.
2. Immettere i dati di test nel componente **Input testo**.
3. Conferma che:
   - I modelli di convalida attivati vengono visualizzati nelle schede Formati e Convalida del componente.
   - Messaggi di errore appropriati attivati da un input non valido.
   - L’input valido è accettato senza errori.

## Risoluzione dei problemi

- **Problema:** i modelli di convalida non vengono visualizzati nel componente modulo.
   - **Soluzione:** Verificare che i criteri del modello siano stati salvati correttamente e che si stia utilizzando il modello corretto durante la creazione del modulo.

- **Problema:** impossibile accedere all&#39;editor modelli.
   - **Soluzione:** Verificare di disporre delle autorizzazioni necessarie per modificare i modelli (appartenenza nel gruppo `template-authors`).

- **Problema:** il componente di immissione testo non convalida l&#39;input correttamente.
   - **Soluzione:** ricontrolla le impostazioni del modello di convalida nella scheda Convalida del componente e assicurati che sia selezionato il modello corretto.

## Passaggi successivi

Dopo aver abilitato e utilizzato i modelli di convalida dell’input di testo nel Forms adattivo di Adobe Experience Manager:

- Configurare modelli di convalida aggiuntivi per altri tipi di dati.
- Esplora altri criteri dei componenti per personalizzare il comportamento dei moduli.
- Imposta la gestione dell’invio dei moduli e la logica di elaborazione dei dati.
