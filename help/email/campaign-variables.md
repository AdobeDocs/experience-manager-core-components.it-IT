---
title: Variabili di Campaign
description: Utilizza le variabili di Campaign come segnaposto per comporre un contenuto e-mail personalizzato.
role: Developer, Admin, User
exl-id: 124ff5bf-6612-4baf-b0ff-6b1a95b455c1
index: false
TQID: https://experienceleague.adobe.com/MB6K-S4DZbsD3puXls8w4rWi6posFFLxJRewKORMkxA
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: eb3ad9f8-54a2-45f3-abb1-d3976415a718
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: ce44533e-8ec8-4e11-a9e9-78b0fe561832
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 73aa5234ac63fa3be99feebce448bb6722513838
workflow-type: tm+mt
source-wordcount: 296
ht-degree: 100%

---

# Variabili di Campaign {#campaign-variables}

Utilizza le variabili di Campaign per comporre contenuti e-mail personalizzati. Le variabili di Campaign fungono da segnaposto per i valori di Adobe Campaign che puoi inserire nel contenuto dei messaggi e-mail. Quando il contenuto viene inviato tramite Adobe Campaign, Campaign sostituisce tali variabili con il contenuto personalizzato del destinatario.

## Utilizzo {#usage}

I componenti core E-mail rendono le variabili di Campaign facilmente accessibili tramite il pulsante di personalizzazione che si trova accanto ai campi di testo più comuni. Quando viene premuto, si apre una finestra di dialogo dalla quale è possibile selezionare un campo di personalizzazione.

L’elenco dei campi di personalizzazione disponibili è sincronizzato con l’istanza di Adobe Campaign. I campi vengono gestiti in Adobe Campaign nello schema `nms:seedMember`. Tutti i campi in `nms:seedMember` devono essere presenti anche nella tabella dei destinatari.

## Finestra di dialogo Seleziona variabile di Adobe Campaign {#dialog}

La finestra di dialogo Seleziona variabile di Adobe Campaign è disponibile in molte finestre di dialogo di modifica dei componenti core E-mail. Per utilizzarla, fai clic sull’icona **Seleziona variabile di Adobe Campaign** accanto al campo applicabile. Questa icona può assumere due forme.

![Pulsante Adobe Campaign](/help/email/assets/campaign-button.png)
![Icona Seleziona variabile di Adobe Campaign](/help/email/assets/select-adobe-campaign-variable-icon.png)

Entrambe consentono di aprire la finestra di dialogo **Seleziona variabile di Adobe Campaign**.

![Finestra di dialogo Seleziona variabile di Adobe Campaign](assets/select-campaign-variable-dialog.png)

Utilizza la vista a colonne per individuare la variabile da inserire. Quando si fa clic su un nodo in una colonna, i relativi elementi secondari vengono visualizzati in una nuova colonna a destra. In questo modo puoi navigare nella struttura del contenuto delle variabili.

Seleziona la variabile da inserire, quindi fai clic sul segno di spunta in alto a destra nella finestra di dialogo.

![Variabile di Adobe Campaign selezionata](assets/select-campaign-variable-dialog-selected.png)

La variabile viene quindi inserita nel campo della finestra di dialogo per la modifica del componente core E-mail.

![Variabile di Campaign inserita nella finestra di dialogo di modifica](assets/campaign-variable.png)

Fai clic sulla X in alto a sinistra nella finestra di dialogo in qualsiasi momento per annullare e chiudere la finestra di dialogo.
