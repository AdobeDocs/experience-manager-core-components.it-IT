---
title: Componente Incorpora
description: Il componente Incorpora consente di incorporare contenuto esterno in una pagina di contenuto AEM.
role: Architect, Developer, Admin, User
exl-id: 985fa304-70a3-4329-957e-76d1832a06f1
source-git-commit: dd30def59a8f037864da875ef4c831b11f766e57
workflow-type: ht
source-wordcount: '1343'
ht-degree: 100%

---


# Componente Incorpora {#embed-component}

Il componente core Incorpora consente di incorporare contenuto esterno in una pagina di contenuto AEM.

{{traditional-aem}}

## Utilizzo {#usage}

Il componente core Incorpora consente all’autore di contenuto di definire un contenuto esterno selezionato da incorporare all’interno di una pagina di contenuto AEM. Inoltre, è disponibile un’opzione per definire anche codice HTML in forma libero da incorporare.

* Le proprietà del componente possono essere definite nella [finestra di dialogo per configurazione](#configure-dialog).
* Le impostazioni predefinite del componente, quando lo si aggiunge a una pagina, possono essere definite nella [finestra di dialogo per progettazione](#design-dialog).

## Versione e compatibilità {#version-and-compatibility}

La versione corrente del componente Incorpora è la v2, introdotta con la versione 2.18.0 dei Componenti core a febbraio 2022, ed è quella descritta in questo documento.

La tabella che segue descrive tutte le versioni supportate del componente, le versioni di AEM con cui le versioni del componente sono compatibili e i collegamenti alla documentazione delle versioni precedenti.

| Versione del componente | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |---|---|---|
| v2 | - | Compatibile | Compatibile | Compatibile |
| [v1](v1/embed.md) | Compatibile | Compatibile | - | Compatibile |

Per ulteriori informazioni sulle versioni e sugli aggiornamenti dei Componenti core, vedi il documento [Versioni dei Componenti core](/help/versions.md).

## Esempio di output del componente {#sample-component-output}

Per avere un’idea del componente Incorpora e vedere esempi delle opzioni di configurazione e dell’output HTML e JSON, visita la [libreria dei componenti](https://adobe.com/go/aem_cmp_library_embed).

## Dettagli tecnici {#technical-details}

La documentazione tecnica più recente sul componente Incorpora [è disponibile su GitHub](https://adobe.com/go/aem_cmp_tech_embed_v2_it).

Per ulteriori informazioni sullo sviluppo di Componenti core, vedi la [documentazione per gli sviluppatori di Componenti core](/help/developing/overview.md).

## Finestra di dialogo per la configurazione {#configure-dialog}

La finestra di dialogo per configurazione consente all’autore di contenuto di definire la risorsa esterna da incorporare nella pagina.

### Scheda Proprietà {#properties-tab}

Scegli innanzitutto il tipo di risorsa da incorporare:

* [URL](#url)
* [Contenuto incorporabile](#embeddable)
* [HTML](#html)

Per ogni tipo di risorsa incorporabile, puoi definire un **ID**. Questa opzione consente di controllare l’identificatore univoco del componente nel codice HTML e nel [livello dati](/help/developing/data-layer/overview.md).

* Se non specificato, viene generato automaticamente un ID univoco reperibile sulla pagina risultante.
* Se l’ID viene specificato, è responsabilità dell’autore accertarsi che sia univoco.
* La modifica dell’ID può avere un impatto sul tracciamento di CSS, JS e livello dati.

#### URL {#url}

L’URL è il tipo di risorsa più facile da incorporare. È sufficiente incollare l’URL della risorsa da incorporare nel campo **URL**. Il componente tenterà di accedere alla risorsa e, se uno dei processori potrà eseguirne il rendering, visualizzerà un messaggio di conferma sotto il campo **URL**. In caso contrario, il campo verrà contrassegnato come in errore.

Il componente Incorpora viene fornito con i relativi processori per i seguenti tipi di risorse:

* Risorse conformi allo [standard oEmbed](https://oembed.com/), inclusi Facebook, Instagram, SoundCloud, Twitter e YouTube
* Pinterest

Gli sviluppatori possono aggiungere processori URL aggiuntivi [seguendo la documentazione per gli sviluppatori del componente Incorpora.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/embed/v1/embed#extending-the-embed-component)

![Opzione URL nella finestra di dialogo per la modifica del componente Incorpora](/help/assets/embed-url.png)

#### Contenuto incorporabile {#embeddable}

L’opzione Contenuto incorporabile consente un’ulteriore personalizzazione della risorsa incorporata, che può essere parametrizzata e includere informazioni aggiuntive. Un autore può scegliere tra vari tipi di contenuto affidabile preconfigurato e il componente viene fornito con YouTube incorporabile pronto per l’uso.

Il campo **Contenuto incorporabile** definisce il tipo di processore vuoi utilizzare. Nel caso di YouTube, puoi quindi definire:

* **ID del video**: l’ID del video univoco di YouTube della risorsa da incorporare
* **Larghezza**: larghezza del video incorporato
* **Altezza**: altezza del video incorporato
* **Abilita Disattiva audio**: questo parametro specifica se per impostazione predefinita il video verrà riprodotto senza audio. L’abilitazione di questa opzione aumenta le possibilità che la riproduzione automatica funzioni nei browser moderni.
* **Abilita Riproduzione automatica**: questo parametro specifica se il video iniziale si avvia automaticamente al caricamento del lettore. Questa opzione è valida solo per l’istanza Publish o quando si utilizza l’opzione **Visualizza come pubblicato** sull’istanza Autore.
* **Abilita Ciclo continuo**: nel caso di un singolo video, questo parametro specifica se il lettore deve riprodurre ripetutamente il video iniziale. Nel caso di una playlist, il lettore riproduce l’intera playlist e quindi riparte dal primo video.
* **Abilita Riproduzione in linea (iOS)**: questo parametro definisce se i video vengono riprodotti in linea (opzione abilitata) o a schermo intero (opzione disabilitata) in un lettore HTML5 su iOS.
* **Video correlati senza restrizioni**: se questa opzione è disabilitata, i video correlati proverranno dallo stesso canale del video appena riprodotto, altrimenti proverranno da qualsiasi canale.

Altre risorse incorporabili potrebbero offrire campi simili, che possono essere definiti da uno sviluppatore [seguendo la documentazione per gli sviluppatori del componente Incorpora.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/embed/v1/embed#extending-the-embed-component)

![Opzione Contenuto incorporabile nella finestra di dialogo per modifica del componente Incorpora](/help/assets/embed-embeddable.png)

>[!NOTE]
>
>Per poter essere disponibile per l’autore di pagine, l’opzione Contenuto incorporabile deve essere abilitata a livello di modello tramite la [finestra di dialogo per progettazione](#design-dialog).

#### HTML {#html}

Puoi aggiungere alla pagina codice HTML in formato libero utilizzando il componente Incorpora.

![Opzione HTML nella finestra di dialogo per la modifica del componente Incorpora](/help/assets/embed-html.png)

>[!NOTE]
>Eventuali tag non sicuri, come gli script, verranno filtrati dal codice HTML inserito e non ne verrà eseguito il rendering nella pagina risultante.

##### Sicurezza {#security}

Il markup HTML che l’autore può inserire viene filtrato a scopo di sicurezza per evitare attacchi di script tra i siti, che potrebbero, ad esempio, consentire agli autori di ottenere diritti amministrativi.

In generale, tutti gli script e gli elementi `style` nonché tutti gli attributi `on*` e `style` verranno rimossi dall’output.

Tuttavia, le regole sono più complicate, perché il componente Incorpora segue a livello globale il set di regole di filtro del framework di bonifica AntiSamy HTML di AEM, reperibile in `/libs/cq/xssprotection/config.xml`. Se necessario, uno sviluppatore può sostituire temporaneamente questa impostazione per la configurazione specifica di un progetto.

Ulteriori informazioni sulla sicurezza sono disponibili nella [documentazione sulle installazioni on-premise per gli sviluppatori di AEM](https://experienceleague.adobe.com/docs/experience-manager-65/developing/introduction/security.html?lang=it) e in [Installazioni di AEM as a Cloud Service.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/security/home.html?lang=it)

>[!NOTE]
>
>Anche se le regole del framework di bonifica AntiSamy possono essere configurate sostituendo temporaneamente `/libs/cq/xssprotection/config.xml`, queste modifiche influiscono sul comportamento di tutti gli elementi HTL e JSP e non solo su quello del componente core Incorpora.

### Scheda Stili {#styles-tab-edit}

![Scheda Stili della finestra di dialogo per modifica del componente Incorpora](/help/assets/embed-styles.png)

Il componente Incorpora supporta il [sistema di stili di AEM](/help/get-started/authoring.md#component-styling).

Utilizza il menu a discesa per selezionare gli stili da applicare al componente. Le selezioni effettuate nella finestra di dialogo di modifica hanno lo stesso effetto di quelle selezionate nella barra degli strumenti del componente.

Gli stili devono essere configurati per questo componente nella [finestra di dialogo di progettazione](#design-dialog) affinché il menu a discesa sia disponibile.

## Finestra di dialogo per progettazione {#design-dialog}

La finestra di dialogo per progettazione consente all’autore del modello di definire le opzioni disponibili per l’autore di contenuto che utilizza il componente Incorpora e le impostazioni predefinite scelte al momento dell’inserimento di questo componente.

### Scheda Tipi incorporabili {#embeddable-types-tab}

![Finestra di dialogo per progettazione del componente Incorpora](/help/assets/embed-design.png)

* **Disabilita URL**: se selezionata, disabilita l’opzione **URL** per l’autore di contenuto
* **Disabilita contenuti incorporabili**: se selezionata, disabilita l’opzione **Contenuto incorporabile** per l’autore di contenuto, indipendentemente dai processori incorporabili consentiti.
* **Disabilita HTML**: se selezionata, disabilita l’opzione **HTML** per l’autore del contenuto.
* **Contenuti incorporabili consentiti**: opzione a selezione multipla che definisce quali processori incorporabili sono disponibili per l’autore di contenuto, a condizione che sia abilitata l’opzione **Contenuto incorporabile**.

### Scheda YouTube {#youtube-tab}

![Scheda YouTube della finestra di dialogo per progettazione del componente Incorpora](/help/assets/embed-design-youtube.png)

* **Consenti la configurazione del comportamento Disattiva audio**: consente all’autore del contenuto di configurare l’opzione **Abilita Disattiva audio** nel componente quando il tipo incorporabile selezionato è YouTube
   * **Valore predefinito per Disattiva audio**: imposta automaticamente l’opzione **Abilita Disattiva audio** quando il tipo incorporabile selezionato è YouTube
* **Consenti la configurazione del comportamento Riproduzione automatica**: consente all’autore di contenuto di configurare l’opzione **Abilita riproduzione automatica** nel componente quando il tipo incorporabile selezionato è YouTube
   * **Valore predefinito per Riproduzione automatica**: se selezionata, imposta automaticamente l’opzione **Abilita Riproduzione automatica** quando il tipo incorporabile selezionato è YouTube
* **Consenti la configurazione del comportamento Ciclo continuo**: consente all’autore di contenuto di configurare l’opzione **Abilita ciclo continuo** nel componente quando il tipo incorporabile selezionato è YouTube
   * **Valore predefinito per Ciclo continuo**: imposta automaticamente l’opzione **Abilita ciclo continuo** quando il tipo incorporabile selezionato è YouTube
* **Consenti la configurazione di Riproduzione in linea (iOS)**: consente all’autore di contenuto di configurare l’opzione **Abilita riproduzione in linea (iOS)** nel componente quando il tipo incorporabile selezionato è YouTube
   * **Valore predefinito per Riproduzione in linea (iOS)**: imposta automaticamente l’opzione **Abilita riproduzione in linea (iOS)** quando il tipo incorporabile selezionato è YouTube
* **Consenti la configurazione di Video correlati**: consente all’autore di contenuto di configurare l’opzione **Video correlati senza restrizioni** nel componente quando il tipo incorporabile selezionato è YouTube
   * **Valore predefinito per Video correlati senza restrizioni**: imposta automaticamente l’opzione **Video correlati senza restrizioni** quando il tipo incorporabile selezionato è YouTube
