---
title: Integrazioni e Adobe Client Data Layer
description: Scopri come Adobe Client Data Layer può integrarsi con i componenti personalizzati e come le integrazioni con Adobe Analytics e Adobe Target possono aiutarti a ottenere insights sul tuo sito web
feature: Core Components, Adobe Client Data Layer
role: Developer, Admin
exl-id: 503dd3dc-fe95-4a17-83f5-1f0c1960993d
TQID: https://experienceleague.adobe.com/xncfOtz1FNyeH6CjQjg7cSeIonIg2mkBIPUgZvMI7Ww
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: ae478996-b206-4712-9b0c-dc78a2644453
  - id: d429a63e-ade4-4117-b04e-9b996d1c94ef
subfeature_v2:
  - id: a94e5c13-4138-47ec-b9c8-e804e17aaca2
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 73aa5234ac63fa3be99feebce448bb6722513838
workflow-type: tm+mt
source-wordcount: 424
ht-degree: 100%

---

# Integrazioni con Adobe Client Data Layer {#integrations}

Adobe Client Data Layer semplifica l’organizzazione di siti web fornendo un metodo standardizzato per visualizzare e accedere a qualsiasi tipo di dati per qualsiasi script.

Adobe Client Data Layer può integrarsi con i componenti personalizzati, e le integrazioni con Adobe Analytics e Adobe Target possono aiutarti a ottenere insight sul tuo sito web.

## Abilitazione del livello dati per componenti personalizzati {#enabling-custom-components}

Per aggiungere automaticamente un componente personalizzato al livello dati:

1. Definisci le proprietà del modello del componente personalizzato da tracciare.
1. Aggiungi l’attributo `data-cmp-data-layer` all’HTL del componente personalizzato. Ad es. `data-cmp-data-layer="${mycomponent.data.json}"`.

Per fare in modo che il livello dati attivi automaticamente un evento `cmp:click` ogni volta che si fa clic su un elemento specifico del componente personalizzato, aggiungi l’attributo `data-cmp-clickable` all’elemento da tracciare nel codice HTL del componente personalizzato.

È possibile eseguire una query sull’attributo `data-cmp-data-layer-enabled` lato client per stabilire se il livello dati è abilitato.

>[!TIP]
>
>Per ulteriori dettagli tecnici sull’integrazione di Adobe Client Data Layer con i componenti core e su come abilitare il livello dati sui componenti personalizzati, vedi il file [`DATA_LAYER_INTEGRATION.md`](https://github.com/adobe/aem-core-wcm-components/blob/master/DATA_LAYER_INTEGRATION.md) nell’archivio dei componenti core.

## Integrazione con Adobe Analytics e Adobe Target {#analytics-target}

Insieme ad Adobe Analytics e Adobe Target, Adobe Client Data Layer diventa il fondamento di uno strumento molto potente e flessibile per ottenere insight sulle tue esperienze digitali. Le seguenti esercitazioni ti guidano attraverso esempi di integrazioni.

### Raccolta dei dati di pagina con Adobe Analytics {#collect-page-data}

Scopri come utilizzare le funzioni incorporate di Adobe Client Data Layer con i componenti core di AEM per raccogliere i dati di una pagina in Adobe Experience Manager Sites. Experience Platform Launch e l’estensione Adobe Analytics verranno utilizzati per creare regole per inviare dati di pagina ad Adobe Analytics.

[Visualizza il tutorial qui.](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/integrations/analytics/collect-data-analytics.html?lang=it)

### Tracciamento dei componenti selezionati con Adobe Analytics {#track-clicked-components}

Utilizza Adobe Client Data Layer basato sugli eventi con i componenti core di AEM per tracciare i clic su componenti specifici su un sito Adobe Experience Manager. Scopri come utilizzare le regole in Experience Platform Launch per rilevare gli eventi clic, filtrarli per componente e inviare i dati ad Adobe Analytics con un beacon di tracciamento dei collegamenti.

[Visualizza il tutorial qui.](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/integrations/analytics/track-clicked-component.html?lang=it)
