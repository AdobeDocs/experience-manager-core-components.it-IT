---
title: Componente Pagina
description: Il componente Pagina è una pagina estensibile concepita per funzionare con l’editor di modelli e consentire l’assemblaggio di intestazione/piè di pagina e altri componenti della struttura della pagina.
role: Architect, Developer, Admin, User
exl-id: 2503e067-abed-427d-8a54-8b79e3451487
source-git-commit: dd30def59a8f037864da875ef4c831b11f766e57
workflow-type: tm+mt
source-wordcount: '695'
ht-degree: 100%

---


# Componente Pagina {#page-component}

Il componente Pagina è una pagina estensibile concepita per funzionare con l’[editor di modelli](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=it) e consentire l’assemblaggio di intestazione/piè di pagina e altri componenti della struttura della pagina.

{{traditional-aem}}

## Utilizzo {#usage}

Il componente Pagina costituisce la base di tutte le pagine progettate con i Componenti core e i modelli modificabili. Utilizzando il componente Pagina, le intestazioni, i piè di pagina e la struttura della pagina possono essere definiti in un modello utilizzando gli altri Componenti core.

Nella [finestra di dialogo per progettazione](#design-dialog) è possibile definire le librerie client della pagina. A differenza di altri componenti che hanno una finestra di dialogo per modifica accessibile direttamente dal componente, poiché il componente Pagina è la pagina stessa, la [finestra di dialogo per modifica](#edit-dialog) del componente Pagina è la finestra delle proprietà della pagina.

## Versione e compatibilità {#version-and-compatibility}

La versione corrente del componente Pagina è la v3, introdotta con la versione 2.18.0 dei Componenti core di febbraio 2022, ed è quella descritta in questo documento.

La tabella che segue descrive tutte le versioni supportate del componente, le versioni di AEM con cui le versioni del componente sono compatibili e i collegamenti alla documentazione delle versioni precedenti.

| Versione del componente | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|---|---|---|---|---|
| v3 | - | Compatibile | Compatibile | Compatibile |
| [v2](v2/page.md) | Compatibile | Compatibile | - | Compatibile |
| [v1](v1/page-v1.md) | Compatibile | Compatibile | - | Compatibile |

Per ulteriori informazioni sulle versioni e sugli aggiornamenti dei Componenti core, vedi il documento [Versioni dei Componenti core](/help/versions.md).

## Supporto di Progressive Web App {#pwa-support}

La versione 2.15.0 dei Componenti core ha introdotto il supporto delle [funzionalità Progressive Web App (PWA) incorporate in AEM as a Cloud Service.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/enable-pwa.html?lang=it)Con una semplice configurazione a livello di sito, puoi trasformare la tua esperienza AEM in un’esperienza PWA.

### Dettagli tecnici {#technical-details}

La documentazione tecnica più recente sul componente Pagina [è disponibile su GitHub](https://adobe.com/go/aem_cmp_tech_page_v3_it).

Per ulteriori informazioni sullo sviluppo di Componenti core, vedi la [documentazione per gli sviluppatori di Componenti core](/help/developing/overview.md).

## Finestra di dialogo per modifica {#edit-dialog}

Poiché il componente rappresenta l’intera pagina, le impostazioni normalmente presenti in una finestra di dialogo per modifica si trovano invece nella finestra [Proprietà della pagina](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html?lang=it).

## Finestra di dialogo per progettazione {#design-dialog}

Poiché il componente rappresenta l’intera pagina, la finestra di dialogo per progettazione è accessibile tramite **Informazioni pagina -> Criterio pagina** durante la modifica del modello della pagina.

![Criterio pagina](/help/assets/page-policy.png)

>[!NOTE]
>
>Nelle versioni precedenti di AEM, **Criterio pagina** era denominato **Progettazione pagina**.

### Scheda Proprietà {#properties-tab}

La finestra per progettazione della pagina consente di definire le librerie client da caricare e la libreria di risorse web della pagina.

* **Librerie client**: definisce le categorie di librerie client da caricare. JavaScript viene aggiunto alla fine del corpo della pagina e CSS viene aggiunto all’intestazione della pagina.
* **Intestazione pagina JavaScript per librerie client**: definisce le categorie di librerie client JavaScript da caricare nell’intestazione della pagina.
   * Le categorie definite in questo campo che sono presenti anche nel campo **Librerie client** avranno JavaScript caricato nell’intestazione invece che alla fine del corpo della pagina.
   * Non verrà caricato alcun CSS, a meno che la categoria non sia presente anche nel campo **Librerie client**.

* **Libreria client risorse web**: categoria di librerie client utilizzate per fornire risorse web come le favicons (favorite icons).

* **Selettore per passare all’elemento del contenuto principale**: utilizzato come funzione di accessibilità per passare direttamente al contenuto principale della pagina

* **Collegamenti di lingue alternative del rendering** - Se questa opzione è attivata, i collegamenti alle versioni in lingua alternativa della pagina nello stesso sito verranno aggiunti all’intestazione della pagina.

![Finestra di dialogo per progettazione del componente Pagina](/help/assets/page-design.png)

Le librerie possono essere configurate per i campi **Librerie client** e **Intestazione pagina JavaScript per librerie client**, nel modo che segue:

* Per aggiungere un nuovo campo, tocca o fai clic sul pulsante **Aggiungi** sotto ciascuno dei due campi.
* Per rimuovere un campo, tocca o fai clic sull’icona cestino accanto al campo da rimuovere.
* Per cambiare l’ordine di caricamento, tocca o fai clic e trascina la maniglia che si trova accanto al campo da spostare.

Per ulteriori informazioni sull’utilizzo delle librerie client, vedi [Utilizzo delle librerie client](https://helpx.adobe.com/it/experience-manager/6-5/sites/developing/using/clientlibs.html).

>[!CAUTION]
>
>Con la versione 2.2.0 dei Componenti core è stata introdotta la possibilità di definire separatamente le librerie client per l’intestazione della pagina.

### Scheda Stili {#styles-tab}

Il componente Pagina supporta il [sistema di stili](/help/get-started/authoring.md#component-styling) di AEM.

## Adobe Client Data Layer {#data-layer}

Il componente Pagina supporta [Adobe Client Data Layer.](/help/developing/data-layer/overview.md)
