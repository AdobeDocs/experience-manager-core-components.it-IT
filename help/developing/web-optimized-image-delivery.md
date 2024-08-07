---
title: Consegna delle immagini ottimizzate per il web
description: Scopri in che modo i componenti core possono sfruttare le funzionalità di AEM as a Cloud Service per la consegna delle immagini ottimizzate per il web, per fornire le immagini in modo più efficiente.
role: Architect, Developer, Admin, User
exl-id: 6080ab8b-f53c-4d5e-812e-16889da4d7de
source-git-commit: eb1822cb41a849695afb5125745ed5f78e3e70a4
workflow-type: tm+mt
source-wordcount: '1061'
ht-degree: 100%

---

# Consegna delle immagini ottimizzate per il web {#web-optimized-image-delivery}

Scopri in che modo i componenti core possono sfruttare le funzionalità di AEM as a Cloud Service per la consegna delle immagini ottimizzate per il web, per fornire le immagini in modo più efficiente.

## Panoramica {#overview}

La funzione di AEM as a Cloud Service per la consegna delle immagini ottimizzate per il web offre risorse immagine da DAM in [Formato WebP.](https://developers.google.com/speed/webp) WebP può ridurre la dimensione di download di un’immagine di circa il 25% in media, velocizzando così il caricamento delle pagine.

La consegna di immagini ottimizzate per il web nei componenti core è semplice da attivare e, poiché tutti i browser più comuni supportano WebP, offre all’utente finale un’esperienza trasparente. L’unica differenza che noteranno, infatti, sarà che il contenuto viene caricato più velocemente.

## Attivazione della consegna di immagini ottimizzate per il web per i componenti core {#activating}

Per abilitare la consegna di immagini ottimizzate per il web, modifica un modello di pagina e attiva semplicemente l’opzione **Abilita immagini ottimizzate per il web** nella finestra di dialogo di progettazione del [componente Immagine.](/help/components/image.md#design-dialog) Questa opzione è disponibile per le versioni v1, v2 e v3 del componente Immagine.

Se non hai familiarità con le finestre di dialogo di progettazione e i modelli di pagina AEM, [consulta questo documento.](/help/get-started/authoring.md#pre-configuring-core-components)

![Abilitazione della consegna di immagini ottimizzate per il web nella finestra di dialogo di progettazione](/help/assets/web-optimized-image-delivery.png)

Tutto qui. Le immagini vengono ora consegnate dal componente Immagine in formato WebP.

Dopo aver attivato la consegna di immagini ottimizzate per il web, potresti voler controllare la configurazione del dispatcher per verificare che non blocchi la richiesta al servizio di consegna delle immagini. Per ulteriori informazioni, consulta [questa pagina delle domande frequenti](#failure-to-deliver).

## Verifica della consegna WebP {#verifying}

La consegna delle immagini ottimizzate per il web è trasparente per il consumatore del contenuto. L’unica cosa che l’utente finale noterà è il tempo di caricamento più veloce. Pertanto, per osservare eventuali cambiamenti di comportamento effettivi, è necessario controllare il tipo di contenuto delle immagini sottoposte a rendering nel browser. Tutti i browser moderni supportano WebP. Per informazioni dettagliate sul supporto del browser, puoi consultare [questo sito](https://caniuse.com/webp).

1. In AEM, modifica una pagina basata su un modello in cui è [attivata la consegna di immagini ottimizzate per il web](#activating) per il componente Immagine.
1. Nell’Editor pagina, seleziona il pulsante **Informazioni pagina** in alto a sinistra e quindi **Visualizza come pubblicato**.
1. Apri gli strumenti di sviluppo del browser e seleziona la scheda di rete.
1. Ricarica la pagina e cerca le richieste HTTP che caricano le immagini e controlla il tipo di contenuto dell’immagine ricevuta dal browser.

## Quando la consegna delle immagini ottimizzate per il web non è disponibile {#fallback}

La consegna delle immagini ottimizzate per il web è disponibile solo in AEM as a Cloud Service. Nei casi in cui non è disponibile, ad esempio se si usa AEM 6.5 on-premise o un’istanza di sviluppo locale, la consegna delle immagini viene eseguita mediante [Adaptive Image Servlet.](/help/developing/adaptive-image-servlet.md)

Se si torna ad Adaptive Image Servlet, si modifica l’attributo `src` degli elementi `img` nella sorgente della pagina.

## Domande frequenti {#faq}

### Perché non esiste un’opzione per abilitare le immagini ottimizzate per il web nel mio ambiente? {#missing-option}

La funzione è disponibile solo in AEM as a Cloud Service. Se AEM viene eseguito on-premise o in locale, il componente Immagine utilizza come [fallback](#fallback) Adaptive Image Servlet.

### Perché il servizio non funziona con l’SDK locale? {#local-sdk}

Quando utilizzi l’SDK di AEM su `localhost`, il servizio per le immagini non è disponibile e il rendering delle immagini viene eseguito come [fallback](#fallback) da Adaptive Image Servlet.

Per utilizzare il servizio di consegna delle immagini ottimizzate per il web, implementa il progetto in un ambiente di sviluppo AEMaaCS per poter testare con precisione il funzionamento del servizio per le immagini.

### Perché il servizio non funziona per alcune immagini sulla mia pagina? {#some-images}

Il servizio per le immagini funziona solo per le risorse che si trovano in `/content/dam` e non funziona per le immagini caricate direttamente nella pagina e memorizzate in un oggetto `cq:Page`. Tali risorse verranno consegnate mediante Adaptive Image Servlet come [fallback.](#fallback)

### Perché il servizio visualizza un’immagine di qualità peggiore o limita le dimensioni delle immagini? {#quality}

Quando le risorse immagine che si trovano in `/content/dam` vengono elaborate, gli ambienti AEM as a Cloud Service generano rappresentazioni ottimizzate di dimensioni diverse. Il servizio per immagini ottimizzate per il web analizza la larghezza richiesta dal componente core Immagine, prende in considerazione l’immagine originale e tutte le rappresentazioni di dimensioni pari o inferiori a 2048 px e sceglie quelle più grandi (entro le dimensioni e i relativi limiti che il servizio per immagini è in grado di gestire, attualmente 50 MB e `12k`x`12k`) come base a cui applicare le impostazioni richieste (larghezza, ritaglio, formato, qualità, ecc.).

Per mantenere la fedeltà dell’output, il servizio per le immagini non aumenta la risoluzione delle immagini. Queste rappresentazioni definiscono la qualità migliore che il servizio per immagini sarà in grado di fornire. Poiché spesso non è possibile influenzare le dimensioni e/o le dimensioni della risorsa immagine originale, assicurati che tutte le risorse immagine abbiano una rappresentazione zoom da 2048 px e, in caso contrario, rielaborale.

### L’URL delle mie immagini termina ancora con .JPG o .PNG, non con .WEBP, e non c&#39;è un attributo SRCSET o un elemento PICTURE. Il servizio utilizza effettivamente formati web ottimizzati? {#content-negotiation}

Per fornire formati WebP, il servizio di consegna delle immagini ottimizzate per il web utilizza una tecnica chiamata “negoziazione dei contenuti”[.](https://developer.mozilla.org/en-US/docs/Web/HTTP/Content_negotiation#server-driven_content_negotiation) Questo consente di selezionare il formato di output ottimale per l’immagine in base alle funzionalità annunciate dal cliente, consentendo al servizio di consegna delle immagini di ignorare l’estensione del file.

Il vantaggio di sfruttare la negoziazione dei contenuti consiste nel fatto che i browser che non pubblicizzano il supporto per WebP riceveranno comunque il formato di file JPG o PNG senza apportare alcuna modifica necessaria nel markup della pagina. Questo offre una compatibilità ottimale per i siti esistenti e garantisce il percorso più fluido possibile per la transizione verso la consegna di immagini ottimizzate per il web.

### Posso utilizzare la consegna di immagini ottimizzate per il web con un componente personalizzato?

Sì, il servizio di consegna di immagini ottimizzate per il web può essere utilizzato con componenti personalizzati, creati [estendendo il componente Immagine,](/help/developing/customizing.md)

Di seguito è riportata un’interfaccia di servizio che può essere utilizzata per generare l’URL della risorsa.

```
com.adobe.cq.wcm.spi.AssetDelivery.getDeliveryURL(Resource resource, Map<String, Object> parameterMap)
```

>[!WARNING]
>
>L’URL diretto incorpora un’esperienza che non è generata tramite la suddetta SPI (disponibile sui siti as a Cloud Service dell’AEM) costituisce una violazione delle [condizioni di utilizzo di Media Library](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/admin/medialibrary.html?lang=it#use-media-library).

### È possibile che le immagini non vengano visualizzate dopo l’abilitazione delle immagini ottimizzate per il web? {#failure-to-deliver}

No, questo non dovrebbe mai accadere per i seguenti motivi.

* In HTML, il markup non cambia quando si abilitano le immagini ottimizzate per il web; cambia solo il valore dell’attributo `src` per l’elemento immagine.
* Se il nuovo servizio per immagini non è disponibile o non è in grado di elaborare l’immagine desiderata, l’URL generato utilizzerà come [fallback Adaptive Image Servlet.](#fallback)

Tuttavia, le regole del dispatcher possono bloccare il servizio di consegna delle immagini ottimizzate per il web. Gli URL del servizio di consegna delle immagini iniziano con `/adobe` e l’analisi dei registri del dispatcher per le richieste rifiutate come [descritto qui](https://experienceleague.adobe.com/docs/experience-manager-learn/ams/dispatcher/common-logs.html?lang=it#filter-rejects) dovrebbero aiutare a risolvere eventuali errori riscontrati durante la consegna delle immagini al browser.
