---
title: Componente core moduli adattivi - Immagine
description: Utilizzo o personalizzazione del componente core immagine dei moduli adattivi.
role: Architect, Developer, Admin, User
exl-id: 9ee42d5d-16e3-4973-8364-5bc512ebe72e
source-git-commit: 8bba79956a04020647d5d04f9fe6fa674affedf1
workflow-type: tm+mt
source-wordcount: '1058'
ht-degree: 100%

---

# Componente immagine{#image-adaptive-forms-core-component}

Un componente Immagine in un modulo adattivo consente di includere le immagini in un modulo. Queste immagini possono essere utilizzate per migliorare la struttura complessiva del modulo, fornire informazioni aggiuntive o servire come aiuto visivo per favorire la comprensione dello scopo del modulo. Il componente Immagine può essere utilizzato per aggiungere un logo, una foto o un elemento grafico nel modulo.

Per l’accessibilità, è importante specificare un **Testo alternativo** all’immagine per fornire un testo alternativo breve e descrittivo per l’immagine, la quale viene descritta agli utenti che non possono visualizzarla.

**Esempio**

![esempio](/help/adaptive-forms/assets/image.png)


## Utilizzo {#reasons-to-use-image-in-a-form}

Ci sono diversi motivi per cui è utile includere un componente Immagine in un modulo adattivo, tra cui:

- **Branding**: un’immagine può essere utilizzata per visualizzare il logo o il nome dell’organizzazione che ha creato il modulo, contribuendo a stabilire il riconoscimento e la credibilità del marchio.

- **Strumenti visivi**: un’immagine può essere utile per fornire un ulteriore livello di informazioni agli utenti, fornendo un supporto visivo per aiutarli a comprendere lo scopo del modulo.

- **Decorazione**: un’immagine può essere utilizzata per migliorare la struttura complessiva del modulo e renderlo più attraente dal punto di vista visivo.

- **Esperienza utente**: un’immagine può essere utilizzata per rendere il modulo più semplice da usare, fornendo agli utenti un modo chiaro e intuitivo di accedere e compilarne i campi.

## Versione e compatibilità {#version-and-compatibility}

Il componente core Pannello a soffietto moduli adattativi è stato rilasciato a febbraio 2023 come parte dei Componenti core 2.0.4 per Cloud Service e i Componenti core 1.1.12 per AEM Forms 6.5.16.0 o versioni successive. Di seguito è riportata una tabella che mostra tutte le versioni supportate, la compatibilità AEM e i collegamenti alla documentazione corrispondente:

| Versione del componente | AEM as a Cloud Service | AEM Forms 6.5.16.0 o versioni successive |
|---|---|---|
| v1 | Compatibile con <br>[versione 2.0.4](/help/adaptive-forms/version.md) e successive | Compatibile con <br>[versione 1.1.12](/help/adaptive-forms/version.md) e successive, ma precedenti a 2.0.0. |

Per informazioni sulle versioni dei componenti core, consulta il documento [Versioni dei componenti core](/help/adaptive-forms/version.md).


<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Dettagli tecnici {#technical-details}

Ottieni informazioni aggiornate sul componente core Immagine per moduli adattivi nella documentazione tecnica in [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/image/v1/image). Per ulteriori informazioni sullo sviluppo dei componenti core, consulta la [Documentazione per gli sviluppatori dei componenti core](/help/developing/overview.md).


## Finestra di dialogo per la configurazione {#configure-dialog}

Puoi personalizzare facilmente l’esperienza dell’immagine per i visitatori tramite la finestra di dialogo Configura. Puoi anche definire le opzioni dell’immagine con facilità per un’esperienza utente semplice.

![Scheda Proprietà](/help/adaptive-forms/assets/image_properties.png)

- **Nome**: puoi identificare facilmente un componente modulo con il suo nome univoco sia nel modulo che nell’editor di regole, ma il nome non deve contenere spazi o caratteri speciali.

- **Titolo**: con il relativo titolo è possibile identificare facilmente un componente in un modulo e, per impostazione predefinita, il titolo viene visualizzato sopra il componente. Se non aggiungi un titolo, al posto del testo del titolo viene visualizzato il nome del componente.

- **Contrassegna come elemento modulo non associato**: seleziona l’opzione per configurare un campo modulo non collegato ad alcun schema. Questa opzione consente di salvare i dati senza aggiornare l’origine dati. Consente inoltre di gestire i dati in modo personalizzato, separato dall’integrazione standard del database.

<!--   **Document of Record bind reference** - This option allows you to associate an Adaptive Form field with Document of Record field. When user enters any value in a linked field of an Adaptive Form that value also appears in the linked field of the corresponding Document of Record. For example, a Document of Record bind reference can be used to display a customer's name and address in a Document of Record, based on the customer's ID entered into the form. In this way, AEM Forms enable you to generate Document of Record and offers a seamless user experience for collecting and managing data.-->

- **Descrizione**: una descrizione è una breve spiegazione testuale che fornisce informazioni aggiuntive o chiarimenti sullo scopo di una specifica immagine.

- **Rilascia una risorsa qui o cerca un file da caricare**: questa opzione consente di rilasciare una risorsa, ad esempio un’immagine, mediante trascinamento del mouse. È inoltre possibile caricare un file da un sistema di file locale utilizzando il pulsante **Sfoglia**. Dopo l’aggiunta di un’immagine, nella sua parte inferiore vengono visualizzati tre pulsanti:
   - **Modifica**: tocca o fai clic su **Modifica** per gestire i rendering della risorsa nell’editor delle risorse.
   - **Cancella**: tocca o fai clic su **Cancella** per deselezionare l’immagine attualmente selezionata.
   - **Scegli**: tocca o fai clic sull’opzione **Scegli** per selezionare un’altra immagine dalla cartella risorse.

- **Testo alternativo**: questa opzione viene utilizzata per inserire un testo breve e descrittivo alternativo all’immagine, che descrive l’immagine per gli utenti ipovedenti.

- **Nascondi componente**: seleziona l’opzione per nascondere il componente dal modulo. Il componente rimane accessibile per altri scopi, ad esempio per i calcoli nell’editor di regole. Questa funzione è utile quando devi memorizzare informazioni che non devono essere viste o modificate direttamente dall’utente.

<!--   **Read-only** - Select the option to make the component non-editable. The user can see the value of the field but cannot modify it. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor.
-->

## Finestra di dialogo per la progettazione {#design-dialog}

La finestra di dialogo per la progettazione viene utilizzata per definire e gestire gli stili CSS per il componente Immagine.

### Scheda Stili {#styles-tab}

La scheda è utilizzata per definire e gestire gli stili CSS per un componente. Il componente core immagine dei moduli adattivi supporta il [Sistema di stili](/help/get-started/authoring.md#component-styling) di AEM.

![Finestra di dialogo per la progettazione](/help/adaptive-forms/assets/checkbox-style.png)

- **Classi CSS predefinite**: puoi fornire una classe CSS predefinita per il componente core immagine dei moduli adattivi.

- **Stili consentiti**: puoi definire gli stili fornendo un nome e la classe CSS che rappresenta lo stile. Ad esempio, puoi creare uno stile denominato “testo in grassetto” e fornire la classe CSS “spessore carattere: grassetto”. Puoi utilizzare o applicare questi stili a un modulo adattivo nell’editor di moduli adattivi. Per applicare uno stile, nell’editor dei moduli adattivi, seleziona il componente a cui applicare lo stile, passa alla finestra di dialogo delle proprietà e seleziona lo stile desiderato dall’elenco a discesa **Stili**. Per aggiornare o modificare gli stili, è sufficiente tornare alla finestra di dialogo per la progettazione, aggiornare gli stili nella scheda Stili e salvare le modifiche.

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