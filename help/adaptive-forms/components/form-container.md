---
title: Componente core dei moduli adattivi - Contenitore di moduli
description: Aggiungere un modulo adattivo a una pagina web.
role: Architect, Developer, Admin, User
exl-id: 03c4cf7c-51d6-4850-a566-1c0514d52dab
source-git-commit: 86a30bc396d89340106177deb08323bfc5640e0e
workflow-type: ht
source-wordcount: '1526'
ht-degree: 100%

---

# Contenitore modulo {#form-container-adaptive-forms-core-component}

<span class="preview"> Questo articolo approfondisce la funzionalità **Bozze** <!--and **Hamburger Menu Support** -->, che è una funzione pre-release. La funzione pre-release è accessibile solo tramite il [canale pre-release](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/release-notes/prerelease.html?lang=it#new-features).</span>

I moduli consentono ai visitatori di un sito web di interagire con il sito web fornendo informazioni preziose, che possono aumentare il coinvolgimento e la soddisfazione degli utenti. Un contenitore di moduli adattivi in Adobe Experience Manager (AEM) Sites consente ai proprietari di siti web di aggiungere facilmente i moduli alle proprie pagine. Questo rende più facile la comunicazione tra i visitatori di un sito web e il proprietario o l’organizzazione del sito web, offrendo ai visitatori un modo semplificato per fornire feedback, rispondere ai sondaggi e completare altre azioni

## Utilizzo {#reasons-to-use-forms-container}

Ci sono diversi motivi per i quali viene aggiunto un modulo a un sito web:
- **Raccolta dati**: i moduli possono essere utilizzati per raccogliere dati dai visitatori di un sito web per vari scopi, come ricerche di mercato, analisi del comportamento degli utenti e altro ancora.

- **Generare lead**: un modulo può essere utilizzato per raccogliere informazioni dai potenziali clienti, ad esempio nome e indirizzo e-mail, per generare lead per attività di vendita e marketing.

- **E-commerce**: i moduli possono essere utilizzati per lo shopping online, poiché consentono ai clienti di effettuare ordini e pagamenti su un sito web.

- **Contatto**: un modulo di contatto consente ai visitatori di un sito web di raggiungere facilmente il proprietario o l’organizzazione del sito web.

- **Indagini e sondaggi**: i moduli possono essere utilizzati per raccogliere feedback e opinioni dai visitatori di un sito attraverso indagini di marketing e sondaggi.

- **Iscriversi ad eventi**: i moduli possono essere utilizzati per partecipare ad eventi, poiché consentono ai visitatori di un sito web di iscriversi ad eventi o webinar.

- **Abbonamenti**: i moduli possono essere utilizzati per sottoscrivere un abbonamento a un sito web, poiché consentono ai visitatori di iscriversi a una newsletter o ad altre comunicazioni regolari.

- **Autenticazione utente**: i moduli possono essere utilizzati per l’autenticazione degli utenti, poiché consentono ai visitatori di un sito web di creare account e di accedere a contenuti o funzionalità esclusive.

- **Aumentare il tasso di conversione**: un modulo ben progettato può aumentare il tasso di conversione rendendo più semplice per gli utenti completare un’azione desiderata, ad esempio acquistare un prodotto o iscriversi a un servizio.

## Versione e compatibilità {#version-and-compatibility}

Il componente core Pannello a soffietto moduli adattativi è stato rilasciato a febbraio 2023 come parte dei Componenti core 2.0.4 per Cloud Service e i Componenti core 1.1.12 per AEM Forms 6.5.16.0 o versioni successive. Di seguito è riportata una tabella che mostra tutte le versioni supportate, la compatibilità AEM e i collegamenti alla documentazione corrispondente:

| Versione del componente | AEM as a Cloud Service | AEM Forms 6.5.16.0 o versioni successive |
|---|---|---|
| v1 | Compatibile con <br>[versione 2.0.4](/help/adaptive-forms/version.md) e successive | Compatibile con <br>[versione 1.1.12](/help/adaptive-forms/version.md) e successive, ma precedenti a 2.0.0. |

Per informazioni sulle versioni dei componenti core, consulta il documento [Versioni dei componenti core](/help/adaptive-forms/version.md).
<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Dettagli tecnici {#technical-details}

Per informazioni aggiornate sul componente core contenitore di moduli adattivi, consulta la documentazione tecnica su [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/container/v1/container). Per ulteriori informazioni sullo sviluppo dei componenti core, consulta la [Documentazione per gli sviluppatori di componenti core](/help/developing/overview.md).

## Finestra di dialogo per la configurazione {#configure-dialog}

È possibile personalizzare facilmente l’esperienza del contenitore di moduli per i visitatori tramite la finestra di dialogo Configura. È, inoltre, possibile definire le opzioni del contenitore di moduli con facilità per un’esperienza utente perfetta.

### Scheda Base {#basic-tab}

![Scheda Base](/help/adaptive-forms/assets/formcontainer_basictab1.png)

- **Titolo** : con il relativo titolo è possibile identificare facilmente un componente in un modulo e, per impostazione predefinita, il titolo viene visualizzato sopra il componente. Se non aggiungi un titolo, al posto del testo del titolo viene visualizzato il nome del componente.

- **Servizi di precompilazione**: questa opzione consente all’utente di selezionare un servizio di precompilazione per il recupero dei dati durante il rendering del modulo adattivo. Ulteriori informazioni su [come creare e configurare un servizio di precompilazione](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/prepopulate-adaptive-form-fields.html?lang=it#aem-forms-custom-prefill-service).

- **Ruolo**: il ruolo è un attributo HTML utilizzato per specificare lo scopo di un elemento HTML per tecnologie di assistenza come le utilità per la lettura dello schermo. L’attributo ruolo viene utilizzato per fornire ulteriore contesto e significato semantico a un elemento, facilitando l’interpretazione e la lettura del contenuto da parte delle utilità per la lettura dello schermo per l’utente. Ad esempio, in AEM Forms, l’etichetta di un campo modulo potrebbe avere il ruolo di “etichetta” e il relativo campo di input potrebbe avere il ruolo di “casella di testo”. Questo permette all’assistente vocale di comprendere la relazione tra l’etichetta e il campo di input, e di leggerli in modo corretto all’utente.

- **Categoria Libreria client**: l’utente può configurare una libreria JavaScript personalizzata per un modulo adattivo. Si consiglia di mantenere solo le funzioni riutilizzabili nella libreria, che dipendono dalle librerie di terze parti jquery e underscore.js.
A volte, se sono presenti **regole di convalida complesse**, lo script di convalida esatto si trova nelle funzioni personalizzate e gli utenti chiamano tali funzioni personalizzate dall’espressione di convalida del campo. Per rendere nota e disponibile questa libreria di funzioni personalizzata durante l’esecuzione delle convalide lato server, l’utente del modulo può configurare il nome della libreria client AEM nella scheda **[!UICONTROL Base]** delle proprietà del contenitore per modulo adattivo.
L’utente può configurare una libreria JavaScript personalizzata per modulo adattivo. Si consiglia di mantenere solo le funzioni riutilizzabili nella libreria, che dipendono dalle librerie di terze parti jquery e underscore.js.

<!--
- **Enable the hamburger menu for mobile view** - Select the checkbox to integrate a hamburger menu into your form for mobile view. Represented by three horizontal lines stacked vertically, this menu provides a clear and uncluttered display for panels on smaller devices, especially on mobile devices. For more information about the hamburger menu, refer to the [Learn more about the hamburger menu](#learn-more-about-the-hamburger-menu) section. -->


### Scheda Modello dati {#data-model-tab}

![Scheda Invio](/help/adaptive-forms/assets/formcontainer_fdmtab.png)

È possibile utilizzare il modello dati modulo per collegare un modulo a un’origine dati per inviare e ricevere dati in base alle azioni degli utenti. È possibile anche collegare un modulo a uno schema JSON per ricevere i dati inviati in un formato predefinito. In base al requisito, connetti il modulo a uno schema JSON o a un modello di dati del modulo:
- Crea uno schema JSON e caricalo nell’ambiente
- Creare un modello dati modulo

### Bozze

![Scheda Invio](/help/adaptive-forms/assets/formcontainer_autosavetab.png)

- **Salvataggio automatico delle bozze**: seleziona la casella di controllo **Salvataggio automatico delle bozze** per abilitare il salvataggio dei moduli come bozze.
- **Salva preferenza**: configura **Salva preferenza** come **Salva bozze a intervalli regolari**, per salvare automaticamente il modulo dopo un intervallo di tempo specifico.
  **Salva intervallo di frequenza (secondi)**: specifica l’intervallo di tempo (in secondi) per impostare la durata di tempo che deve trascorrere tra ogni salvataggio automatico del modulo, pari all’intervallo definito.

### Scheda Invio {#submission-tab}

Gli utenti possono configurare azioni diverse per gli invii di moduli adattivi.

- **URL/percorso di reindirizzamento**: questa opzione consente agli utenti di configurare una pagina per ciascun modulo, a cui verranno reindirizzati gli utenti dei moduli dopo l’invio di un modulo adattivo. Fai clic qui per ulteriori informazioni su [come configurare le pagine di reindirizzamento](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-redirect-page.html?lang=it).

![Scheda Invio](/help/adaptive-forms/assets/formcontainer_submissiontab.png)

- **Mostra Messaggio**: questa opzione consente agli utenti di aggiungere un messaggio da visualizzare quando il modulo adattivo viene inviato correttamente. Il testo predefinito viene incluso nella finestra di dialogo e può essere modificato dall’utente. La finestra di dialogo Mostra messaggio supporta gli strumenti di formattazione RTF che consentono agli utenti di formattare il testo aggiunto.

![Scheda Mostra Messaggio](/help/adaptive-forms/assets/formconatiner_showmessage.png)

- **Azione di invio**: un’azione di invio viene attivata quando l’utente fa clic sul pulsante Invia in un modulo adattivo. Gli utenti possono selezionare azioni di Invio dall’elenco a discesa supportato come predefinito. Scopri come [configurare un’azione di invio nella scheda Invio](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html?lang=it#supporting-custom-functions-in-validation-expressions-br).

## Finestra di dialogo per la progettazione {#design-dialog}

La finestra di dialogo per la progettazione consente di definire e gestire gli stili CSS per il componente Contenitore modulo.

### Scheda Componenti Consentiti {#allowed-components-tab}

![Scheda Componente consentito della finestra di dialogo per la progettazione](/help/adaptive-forms/assets/formcontainer-allowedcomponents.png)

La scheda **Componenti consentiti** permette all’editor dei modelli di impostare i componenti che possono essere aggiunti come elementi ai pannelli nel componente nell’editor di moduli adattivi.

### Scheda Componenti predefiniti {#default-components-tab}

![Scheda Componente predefinito della finestra di dialogo per la progettazione](/help/adaptive-forms/assets/formcontainer-defaultcomponents.png)

La scheda **Componenti predefiniti** consente all’editor di modelli di specificare i componenti visibili per impostazione predefinita come elementi nel componente Contenitore modulo nell’editor moduli adattivi.

### Scheda Impostazioni reattive {#responsive-tab}

![Scheda Impostazioni reattive della finestra di dialogo per la progettazione](/help/adaptive-forms/assets/formcontainer-responsivestyle.png)

La scheda **Impostazioni reattive** consente all’editor di modelli di specificare il numero di colonne nella griglia all’interno del componente Contenitore modulo nell’editor di moduli adattivi.

### Scheda Stili {#styles-tab}

Il componente core Allegato file dei moduli adattivi supporta il [Sistema di stili](/help/get-started/authoring.md#component-styling) di AEM.

![Finestra di dialogo per la progettazione](/help/adaptive-forms/assets/formcontainer-styletab.png)

- **Classi CSS predefinite**: è possibile fornire una classe CSS predefinita per il componente core contenitore del modulo nei moduli adattivi.

- **Stili consentiti**: è possibile definire gli stili fornendo un nome e la classe CSS che rappresenta lo stile. Ad esempio, puoi creare uno stile denominato “testo in grassetto” e fornire la classe CSS “spessore carattere: grassetto”. Puoi utilizzare o applicare questi stili a un modulo adattivo nell’editor di moduli adattivi. Per applicare uno stile, nell’editor dei moduli adattivi, seleziona il componente a cui applicare lo stile, passa alla finestra di dialogo delle proprietà e seleziona lo stile desiderato dall’elenco a discesa **Stili**. Per aggiornare o modificare gli stili, è sufficiente tornare alla finestra di dialogo per la progettazione, aggiornare gli stili nella scheda Stili e salvare le modifiche.

### Scheda Proprietà personalizzate

![Finestra di dialogo Proprietà personalizzate](/help/adaptive-forms/assets/formcontainer-custompropertiestab.png)

Le proprietà personalizzate consentono di associare attributi personalizzati (coppie chiave-valore) a un componente core del modulo adattivo utilizzando il modello di modulo. Le proprietà personalizzate vengono riflesse nella sezione delle proprietà della rappresentazione headless del componente. Consentono di creare un comportamento di modulo dinamico che si adatta in base ai valori degli attributi personalizzati. Ad esempio, gli sviluppatori possono progettare diverse rappresentazioni di un componente moduli headless su piattaforme mobili, desktop o web, migliorando in modo significativo l’esperienza utente su un’ampia gamma di dispositivi.

- **Nome gruppo**: puoi fornire un nome per identificare il gruppo di proprietà personalizzate. È possibile aggiungere, eliminare o ridisporre più gruppi di proprietà personalizzate. Dopo aver aggiunto il gruppo di proprietà personalizzate, puoi visualizzare le seguenti opzioni:

   - **Coppie chiave-valore**: puoi aggiungere più nomi e valori della proprietà personalizzata facendo clic sul pulsante **Aggiungi** per ogni gruppo di proprietà personalizzate.

   - **Elimina**: tocca o fai clic per eliminare il nome e il valore della proprietà personalizzata.

   - **Ridisponi**: tocca o fai clic e trascina per ridisporre l’ordine del nome e del valore della proprietà personalizzata.

<!--
## Learn more about the hamburger menu

A hamburger menu, often referred to as a mobile menu or navigation drawer, is a popular design element in mobile user interfaces. It features three horizontal lines stacked vertically, resembling a hamburger. The design efficiently conserves screen space by hiding secondary navigation options until they are needed, especially on smaller devices such as mobile. AEM forms can be efficiently organized within the hamburger menu, enabling users to access various panels within a form without overwhelming the main interface.

Consider a scenario, where a financial institution offers an online loan application form that requires users to provide detailed information across several panels, such as personal details, financial information, loan preferences, and supporting documents. The form includes multiple panels and options that can clutter the interface, especially on mobile devices. Users need an organized way to navigate through these panels without feeling overwhelmed. The hamburger menu is implemented to enhance the user experience on mobile devices.

### Components of hamburger menu

![Hamburger Menu](/help/adaptive-forms/assets/hamburger-menu.png){width=50%, align=center}

**A. Hamburger menu**: The hamburger menu features a navigation panel that slides out or drops down when the hamburger icon is clicked or tapped. The menu displays the panel headings, and selecting a panel shifts the focus to that panel. It allows users to easily navigate between different panels.

![Hamburger Menu](/help/adaptive-forms/assets/hamburger-menu-icon.png){width=50%}

**B. Breadcrumb**: Breadcrumbs indicate the user’s current location within the form. They offer a hierarchical trail that shows the user’s navigation path and helps them understand their position in the form.

**C. Active panel**: The active panel refers to the section or part of the form that is currently being displayed. When a user selects an option from the hamburger menu, the corresponding panel becomes the active panel, showing the relevant fields and information for that section.

### Points to consider while working with the hamburger menu

- The hamburger menu displays only the names of the panels. Here are different scenarios illustrating how the panel name appears in the navigation pane of the hamburger menu based on the configuration properties of the panel:  
  
  - If you set the properties of the panel to hidden, the panel's name does not appear in the navigation pane of the hamburger menu. For example, if you configure the properties of the `Financial Information` panel as `hidden`, the panel name does not appear in the navigation pane of the hamburger menu.
    
    ![Hidden panel](/help/adaptive-forms/assets/hidden-panel.png){width=50%}

  - If you set the properties of the panel to `disabled`, its name appears in the navigation pane of the hamburger menu, but you cannot select or edit it. For example, if you configure the properties of the `Financial Information` panel as `disabled`, the panel name appears in the navigation pane, but it cannot be selected or edited. 
     
    ![Disabled panel](/help/adaptive-forms/assets/disabled-panel.png){width=50%}

  - If you hide the  title of the panel, it does not appear in the navigation pane of the hamburger menu. A blank space shows up instead, but you can navigate to the fields of the panel by clicking on that space. For example, if you hide the title of the `Financial Information` panel, the blank space appears in its place in the navigation pane of the hamburger menu. You can navigate to the fields of the panel by clicking on the blank space.
    
    ![Hidden title panel](/help/adaptive-forms/assets/hidden-title-panel.png){width=50%}

- By default, the navigation pane in the breadcrumb component supports up to three levels of navigation. However, with the custom component, you can configure the navigation hierarchy to accommodate as many levels as needed.
- When using the hamburger menu, the user can navigate between panels using arrows. However, once a panel is selected, the menu automatically closes, and focus shifts to the fields within the chosen panel.

### Advantages to use hamburger menu

- **Space efficiency**: By hiding form navigation options until needed, the hamburger menu maximizes screen space, which is especially beneficial on smaller devices.

- **Clutter reduction**: It minimizes visual clutter by consolidating various form navigation links into a single, collapsible menu.

- **Improved focus**: With fewer visible navigation elements, users can concentrate on the main content of the form without being distracted by secondary options.

- **Simplified design**: It creates a more streamlined user interface, resulting in a cleaner and more organized form layout.

- **Enhanced mobile experience**: On mobile devices, where screen space is limited, the hamburger menu offers an efficient way to access all form navigation options without overwhelming the user.

### How to enable hamburger menu for your form?

To enable hamburger menu for form, perform the following steps:

1. Open form in an edit mode.
1. Open the Content browser, and select the **[!UICONTROL Guide Container]** component of your Adaptive Form. 
1. Click the Guide Container properties ![Guide properties](/help/adaptive-forms/assets/configure_icon.png) icon. The Adaptive Form Container dialog box opens. 
1. Click the  **[!UICONTROL Basic]** tab. 
1. Select the **[!UICONTROL Add hamburger menu support]** checkbox.
1. Click **[!UICONTROL Done]**.

![Basic tab](/help/adaptive-forms/assets/formcontainer_basictab.png)
-->

## Articoli correlati {#related-articles}

{{more-like-this}}

## Consulta anche {#see-also}

{{see-also}}