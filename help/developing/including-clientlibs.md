---
title: Librerie client e Componenti core
description: I Componenti core sono dotati di diverse librerie client e consentono di includerne di personalizzate.
role: Developer, Admin
exl-id: 84e7c178-247b-42a2-99bf-6d1699ecee14
TQID: https://experienceleague.adobe.com/7W848EjjUe-9AKUTVidWd2TXdAVEZ5xSWvnuD9XEuM8
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: e2c1b6d3-bb7e-4fe8-8c72-f7b403298e91
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 73aa5234ac63fa3be99feebce448bb6722513838
workflow-type: tm+mt
source-wordcount: 557
ht-degree: 100%

---

# Librerie client e Componenti core {#client-libraries}

I Componenti core sono dotati di diverse librerie client e consentono di includerne di personalizzate.

## Librerie client fornite {#provided}

I Componenti core forniscono le seguenti librerie client pronte all’uso.

* Il **sito** clientlibs fornisce il comportamento funzionale minimalista dei componenti da applicare al sito.
   * Fungono da punto di partenza per accelerare i progetti, con implementazioni favorite all’estensione e alla [personalizzazione](/help/developing/customizing.md) per ottenere l’aspetto e la funzionalità desiderati.
* Le clientlibs dell’**editor** vengono applicate alla finestra di dialogo di authoring per garantirne la funzionalità e l’aspetto previsti.
* Le clientlibs dell’**editor hook** vengono applicate al sito quando vengono caricate in modalità di modifica.
   * Contengono un codice JavaScript eseguito su eventi attivati dall’editor, facilitando l’inizializzazione della funzionalità dinamica.
* Alcuni componenti possono avere clientlibs aggiuntive specifiche progettate per l’utilizzo in situazioni particolari, ad esempio quando vengono utilizzati insieme a [Dynamic Media](/help/components/image.md#dynamic-media).

## Inclusione delle librerie client {#including}

Esistono diversi modi per includere le [librerie client](/help/developing/archetype/front-end.md#clientlibs) a seconda del caso d’uso. Di seguito sono riportati alcuni esempi di [Snippet HTL](https://experienceleague.adobe.com/docs/experience-manager-htl/using/overview.html?lang=it) per ciascuna.

### Utilizzo predefinito consigliato {#recommended-default-usage}

Se non hai tempo di capire qual è la cosa migliore nella tua situazione, includi le librerie client inserendo le seguenti righe HTL nell’elemento `head` della pagina:

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @
    categories='wknd.base', defer=true}">
    ${clientlibs.jsAndCssIncludes @ context="unsafe"}
</sly>
```

In questo modo, includerai sia CSS che JS nell’elemento `head` della pagina, ma aggiungendo anche l’attributo `defer` agli `script` JS inclusi, farai in modo che i browser attendano che il DOM (Document Object Model) sia pronto prima di eseguire gli script, ottimizzando quindi la velocità di caricamento della pagina.

### Utilizzo di base {#basic-usage}

La sintassi di base per includere sia JS che CSS di una categoria di librerie client, che genererà tutti gli elementi `link` CSS e/o `script` JS corrispondenti, è la seguente:

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.jsAndCssIncludes @ context="unsafe"}
</sly>
```

Per fare lo stesso con più categorie di librerie client contemporaneamente, è possibile fornire un array di stringhe al parametro `categories`:

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @
    categories=['wknd.base', 'cq.foundation']}">
    ${clientlibs.jsAndCssIncludes @ context="unsafe"}
</sly>
```

### Solo CSS o JS {#css-js-only}

Spesso occorre inserire le inclusioni CSS nell’elemento `head` HTML e le inclusioni JS subito prima della chiusura dell’elemento `body`.

Per includere nell’elemento `head` solo CSS e non JS, utilizza `cssIncludes`:

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.cssIncludes @ context="unsafe"}
</sly>
```

Per includere nell’elemento `body` solo JS e non CSS, utilizza `jsIncludes`:

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.jsIncludes @ context="unsafe"}
</sly>
```

### Attributi {#attributes}

Per applicare gli attributi agli elementi `link` CSS e/o agli elementi `script` JS generati, è possibile utilizzare diversi parametri:

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @
    categories='wknd.base',
    media='print',
    async=true,
    defer=true,
    onload='console.log(\'loaded: \' + this.src)',
    crossorigin='anonymous'}">
    ${clientlibs.jsAndCssIncludes @ context="unsafe"}
</sly>
```

Attributi `link` CSS che possono essere forniti a `jsAndCssIncludes` e `cssIncludes`:

* `media`: stringa Attributi `script` JS che possono essere forniti a `jsAndCssIncludes` e `jsIncludes`:
* `async`: booleano
* `defer`: booleano
* `onload`: stringa
* `crossorigin`: stringa

### Allineamento {#inlining}

In alcuni casi, per l’ottimizzazione, le e-mail o le [AMP,](amp.md) potrebbe essere necessario allineare CSS o JS nell’output HTML.

Per allineare CSS, si può utilizzare `cssInline`, nel qual caso è necessario scrivere l’elemento `style` circostante:

```html
<style type="text/css"
    data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.cssInline @ context="unsafe"}
</style>
```

Allo stesso modo, per allineare JS, si può utilizzare `jsInline`, nel qual caso è necessario scrivere l’elemento `script` circostante:

```html
<script type="text/javascript"
    data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.jsInline @ context="unsafe"}
</script>
```

### Caricamento di CSS e JavaScript in base al contesto {#context-aware-loading}

Il [componente Pagina](/help/components/page.md) supporta anche il caricamento di tag CSS, JavaScript o meta in base al contesto definiti dagli sviluppatori.

Ciò avviene attraverso la creazione di una [risorsa in base contesto](context-aware-configs.md) per `com.adobe.cq.wcm.core.components.config.HtmlPageItemsConfig`, utilizzando la seguente struttura:

```text
com.adobe.cq.wcm.core.components.config.HtmlPageItemsConfig
    - prefixPath="/some/path"
    + item01
        - element=["link"|"script"|"meta"]
        - location=["header"|"footer"]
        + attributes
            - attributeName01="attributeValue01"
            - attributeName02="attributeValue02"
            ...
    + item02
        ...
    ...
```

[Per ulteriori informazioni, consulta la documentazione tecnica del componente Pagina.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/page/v2/page#loading-of-context-aware-cssjs)
