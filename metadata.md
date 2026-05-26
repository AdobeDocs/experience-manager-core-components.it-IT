---
product: adobe experience manager
solution: Experience Manager, Experience Manager Sites
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8id: c45915cf-e157-4af7-a80d-97b905bcb3a5
usetq: true
landing-page-name: experience-manager
landing-page-breadcrumb-title: AEM
type: Documentation
description: Documentazione dei Componenti core di Adobe Experience Manager
git-repo: https://github.com/AdobeDocs/experience-manager-core-components.en
index: true
recommendations: noDisplay
source-git-commit: 46e65d8dc8f5229e233747ffebe219734ec61adf
workflow-type: tm+mt
source-wordcount: 120
ht-degree: 1%

---


# Metadati per uso interno

I metadati nel sistema di authoring GitHub sono gerarchici e vengono definiti in base ai seguenti livelli crescenti di precedenza.

1. metadata.md
1. ToC
1. Articolo

I metadati definiti nel file metadata.md si applicano all’intero archivio, ma possono essere ignorati a livello di sommario e di articolo. Eventuali esclusioni dei metadati devono essere eseguite al livello più basso possibile.

I metadati nell’archivio experience-manager-core-components.en rappresentano il minimo richiesto.

metadata.md

* `product`
* `git-repo`
* `index: true`
* `solution-title`
* `solution-hub-url`
* `getting-started-title`
* `getting-started-url`
* `tutorials-title`
* `tutorials-url`

ToCs

* `sub-product`
* `user-guide-title`

Articolo

* `title`
* `description`
* `index: false` (solo per le versioni precedenti dei componenti)

Ulteriori informazioni sui metadati sono disponibili nella [guida all&#39;authoring interno.](https://experienceleague.adobe.com/docs/authoring-guide-exl/using/authoring/features/metadata.html#solution)
