---
title: Configurazioni in base al contesto di Sling e Componenti core
description: I Componenti core utilizzano le configurazioni in base al contesto di Sling per alcune funzioni
role: Architect, Developer, Admin
exl-id: d35210f7-a65d-4768-ab9e-f12ec406da2d
source-git-commit: b72defe1bbe6cb286730ac3f508f7d6c14b3fc33
workflow-type: ht
source-wordcount: '174'
ht-degree: 100%

---

# Configurazioni in base al contesto di Sling e Componenti core {#sling-context-aware-configurations}

Le configurazioni in base al contesto sono una funzione di [Sling](https://sling.apache.org/documentation/bundles/context-aware-configuration/context-aware-configuration.html). Si tratta di configurazioni correlate a una risorsa di contenuto o a una struttura di risorse e vengono utilizzate dai Componenti core per consentire configurazioni a livello di sito.

## Configurazioni in base al contesto di Sling {#context-aware-configurations}

Un sito potrebbe richiedere configurazioni diverse per le varie aree, ad esempio laddove alcuni parametri potrebbero essere condivisi e richiedere la capacità di ereditarli per contesti nidificati e valori di regresso globali. AEM utilizza le configurazioni in base contesto di Sling, in quanto offrono questa possibilità.

Per informazioni dettagliate sulle configurazioni in AEM, [vedi la documentazione sulle configurazioni e sul browser di configurazione.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/configurations.html?lang=it)

## Utilizzo nei Componenti core {#core-components}

Molte funzionalità dei Componenti core utilizzano le configurazioni in base al contesto. Tutte queste configurazioni si trovano sotto il seguente nodo:

* `/conf/<my-site>/sling:configs/<my-configuration>`

Le singole configurazioni dipendono dal componente o dalla funzione specifica. Le funzioni dei Componenti core che utilizzano le configurazioni in base al contesto includono:

* [Il componente Pagina](https://github.com/adobe/aem-core-wcm-components/tree/main/content/src/content/jcr_root/apps/core/wcm/components/page/v3/page#loading-of-context-aware-cssjs) si basa sulla configurazione che tiene conto del contesto durante il rendering dei tag `link`, `script` e `meta`.
* [Componente Visualizzatore PDF](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/pdfviewer/v1/pdfviewer#context-aware-config)
* [Adobe Client Data Layer](/help/developing/data-layer/overview.md#installation-activation)
* [Supporto AMP](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)
