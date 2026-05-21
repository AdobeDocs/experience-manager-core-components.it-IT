---
title: Progettazione reattiva dei Componenti core
description: Scopri la progettazione reattiva dei Componenti core e come può influenzare il progetto.
role: Developer, Admin, User
exl-id: c0eff174-6803-4b44-aeb1-eae3bc8a36ea
TQID: https://experienceleague.adobe.com/wUpRlK8WxDuQzmFJFWAwFZUY-1fo9qOOgbOn-GEwBok
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 73aa5234ac63fa3be99feebce448bb6722513838
workflow-type: tm+mt
source-wordcount: 178
ht-degree: 100%

---

# Progettazione reattiva dei Componenti core {#responsive-design}

Tutti i Componenti core sono progettati per essere completamente reattivi, garantendo un’esperienza fluida su tutti i dispositivi. È importante notare che alcuni componenti avanzati, come ad esempio i componenti [Carosello](/help/components/carousel.md), [Schede](/help/components/tabs.md) e [Pannello a soffietto,](/help/components/accordion.md) possono richiedere una considerazione specifica nel contesto del progetto di implementazione al fine di mantenere la reattività in tutte le condizioni.

Date le diverse modalità in cui questi componenti possono mostrare un comportamento reattivo, e nell’impegno di Adobe di mantenere i Componenti core leggeri e pronti all’uso, la responsabilità di implementare gli aspetti reattivi dettagliati è intenzionalmente lasciata al progetto.

Ad esempio, su schermi stretti il componente Schede può adattarsi suddividendo schede ampie in nuove righe, consentendo lo scorrimento verticale, trasformando schede in elenchi a discesa o adottando uno stile Pannello a soffietto. A causa del potenziale impatto sulle prestazioni che l’implementazione di tutti questi comportamenti potrebbe causare, le [clientlibs](/help/developing/including-clientlibs.md#provided) sono intese come punto di partenza per chi è addetto all’implementazione piuttosto che come soluzione esaustiva.
