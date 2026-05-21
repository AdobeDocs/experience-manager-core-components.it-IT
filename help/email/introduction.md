---
title: Introduzione ai Componenti core E-mail
description: Crea contenuti e-mail coinvolgenti utilizzando la flessibilità dei componenti core E-mail e distribuiscili con la potenza di Adobe Campaign.
role: Developer, Admin, User
exl-id: 0a411f28-bd6a-4bad-b473-6bc27c1d1055
index: false
TQID: https://experienceleague.adobe.com/PLDfeItW57FUgvSUO7kHgeNP8KogBwVA2AeEd-srbwg
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: ae478996-b206-4712-9b0c-dc78a2644453
  - id: d429a63e-ade4-4117-b04e-9b996d1c94ef
  - id: e2c1b6d3-bb7e-4fe8-8c72-f7b403298e91
  - id: eb3ad9f8-54a2-45f3-abb1-d3976415a718
subfeature_v2:
  - id: f86a5563-8f73-4ec0-be7d-a1782604870a
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 73aa5234ac63fa3be99feebce448bb6722513838
workflow-type: tm+mt
source-wordcount: 439
ht-degree: 100%

---

# Introduzione ai Componenti core E-mail {#email-core-components-introduction}

Crea contenuti e-mail coinvolgenti utilizzando la flessibilità dei componenti core E-mail e distribuiscili con la potenza di Adobe Campaign.

## Panoramica {#overview}

I componenti core E-mail si basano sulla stessa potente base dei componenti core. Consentono di creare in modo semplice e flessibile, mediante trascinamento, i contenuti e-mail che possono quindi essere consegnati al pubblico con le potenti funzioni di Adobe Campaign.

## Vantaggi {#benefits}

Le e-mail fanno parte della brand experience e del percorso del cliente. Con i componenti core E-mail, gli autori possono creare contenuti e-mail dall’interno di AEM, offrendo un’esperienza con branding coerente e velocizzando la creazione dei contenuti.

* Proprio come per l’authoring delle pagine con i componenti core, i componenti core E-mail consentono agli autori di assemblare le e-mail senza conoscenze tecniche, garantendo al contempo il rispetto delle linee guida di branding.
* La possibilità di riutilizzare risorse e contenuti incoraggia inoltre gli autori ad aderire alle linee guida di branding e a ottimizzare il processo di creazione dei contenuti.

## Funzioni {#features}

* I componenti core E-mail si basano sui [Componenti core](/help/introduction.md) e quindi supportano anche i [modelli modificabili](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=it) e il [sistema di stili.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/features/style-system.html?lang=it)
* Per la creazione di contenuti e-mail sono disponibili [dieci componenti pronti per la produzione e ottimizzati per e-mail](#components).
* I Componenti core E-mail consentono la personalizzazione avanzata mediante l’inserimento di [variabili Adobe Campaign](campaign-variables.md) nella maggior parte dei campi presenti nelle finestre di dialogo.
* Il [componente Segmentazione](/help/email/components/segmentation.md) è flessibile e consente la segmentazione avanzata del contenuto.
* I componenti core E-mail core forniscono un output HTML ottimale grazie alla [funzione inline per stili CSS](https://github.com/adobe/aem-core-email-components/wiki/CSS-Styles-Inliner:-Technical-documentation), alla [funzione inline per attributi HTML](https://github.com/adobe/aem-core-email-components/wiki/HTML-Inliner) e allo [strumento di pulizia HTML.](https://github.com/adobe/aem-core-email-components/wiki/HTML-Sanitizing)
* Puoi creare contenuti e-mail ovunque in `/content`.
* I componenti core E-mail sono [open source.](https://github.com/adobe/aem-core-email-components)

## Requisiti {#requirements}

Di seguito sono riportati i requisiti dei componenti core E-mail.

| AEM | Adobe Campaign | Componenti core |
|---|---|---|
| AEM 6.5.14.0+<br>on-premise o AMS | Adobe Campaign Classic<br>Adobe Campaign Standard | [Versione 2.21.2](/help/versions.md)+ |

>[!NOTE]
>
>Poiché le integrazioni Adobe Campaign non sono supportate in AEM as a Cloud Service, anche i componenti core E-mail non sono supportati in AEM as a Cloud Service.

## I componenti E-mail {#components}

La versione corrente dei componenti core E-mail include i seguenti componenti.

* [Pagina](components/page.md)
* [Contenitore](components/container.md)
* [Titolo](components/title.md)
* [Testo](components/text.md)
* [Immagine](components/image.md)
* [Pulsante](components/button.md)
* [Teaser](components/teaser.md)
* [Frammento esperienza](components/experience-fragment.md)
* [Frammento di contenuto](components/content-fragment.md)
* [Segmentazione](components/segmentation.md)

## Installazione e utilizzo {#installation-usage}

Per informazioni dettagliate sull’installazione dei componenti core E-mail, consulta il documento [Utilizzo dei componenti core E-mail](using.md).
