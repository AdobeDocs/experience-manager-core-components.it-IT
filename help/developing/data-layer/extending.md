---
title: Estensione di Adobe Client Data Layer
description: Adobe Client Data Layer può essere esteso seguendo alcuni modelli di base
feature: Core Components, Adobe Client Data Layer
role: Developer, Admin
exl-id: f3d5555b-4f08-49de-ab0f-dc0fb04aadf8
TQID: https://experienceleague.adobe.com/67YSpRfwNRMDgcBARHKLz51-Er6xb4vp1rXX0r0sbfE
product_v2: id: c45915cf-e157-4af7-a80d-97b905bcb3a5id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 73aa5234ac63fa3be99feebce448bb6722513838
workflow-type: tm+mt
source-wordcount: 289
ht-degree: 100%

---

# Estensione di Adobe Client Data Layer {#extending-acdl}

È possibile estendere i componenti core tramite le opzioni della finestra di dialogo per personalizzazione, che consentono agli autori di contenuto di immettere ulteriori informazioni relative al livello dati.

Per includere questi campi nel livello dati, fornito dai componenti core, devi estendere il modello del componente che implementa i propri specifici metodi del livello dati.

## Esempio: componente Titolo {#example}

Un componente core come il [componente Titolo](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/models/Title.java) estende il [componente](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/models/Title.java) che ha un metodo `getData`, il quale per impostazione predefinita restituisce [`ComponentData`.](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/models/datalayer/ComponentData.java)

`ComponentData` serializza campi predefiniti che il componente può implementare, come `getDataLayerLinkUrl` e `getDataLayerTitle` per [`TitleImpl`.](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/internal/models/v1/TitleImpl.java)

Pertanto, il tuo modello Sling personalizzato potrebbe avere un metodo `getData` che restituisce un oggetto che estende `ComponentData` per restituire altri campi.

Per farlo, aggiungerà un attributo `data-cmp-data-layer` all’elemento HTML del componente con il JSON dei dati che verranno inseriti nel livello dati. A questo punto, puoi implementare degli script che effettuano il “listen” (ascolto) di questi dati o di eventi correlati.

>[!TIP]
>
>Per saperne di più sulla flessibilità del livello dati, vedi le opzioni di integrazione, tra cui come abilitare il livello dati per i tuoi componenti personalizzati.
