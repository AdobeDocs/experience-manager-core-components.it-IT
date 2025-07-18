---
title: 'Componente Condivisione '
description: Il componente core Condivisione è un widget per la condivisione su Facebook e Pinterest.
role: Architect, Developer, Admin, User
exl-id: 8bd53c76-da91-479b-b416-f978682a3d43
index: false
source-git-commit: dd30def59a8f037864da875ef4c831b11f766e57
workflow-type: ht
source-wordcount: '377'
ht-degree: 100%

---


# Componente Condivisione {#social-sharing-component}

Il componente core Condivisione è un widget per la condivisione su Facebook e Pinterest.

>[!NOTE]
>
>Il componente Condivisione social è diventato obsoleto con la [versione 2.18.0](/help/versions.md) dei Componenti core.

{{traditional-aem}}

## Utilizzo {#usage}

Il componente Condivisione aggiunge alla pagina i collegamenti a Facebook e Pinterest. Spesso il componente è incluso nelle intestazioni o nei piè di pagina.

A differenza di altri componenti, le impostazioni del componente Condivisione vengono effettuate dall’autore del modello nelle [proprietà della pagina iniziale](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=it) e dall’autore di contenuto nelle [proprietà della pagina](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html?lang=it).

## Versione e compatibilità {#version-and-compatibility}

La versione corrente del componente Condivisione è la v1, introdotta con la versione 1.0.0 dei Componenti core, ed è quella descritta in questo documento.

La tabella che segue descrive tutte le versioni supportate del componente e le versioni di AEM con cui le versioni del componente sono compatibili.

| Versione del componente | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |--- |---|---|
| v1 | Compatibile con la <br>[versione 2.17.4](/help/versions.md) e precedenti | Compatibile, obsoleto | Compatibile, obsoleto | Compatibile, obsoleto |

Per ulteriori informazioni sulle versioni e sugli aggiornamenti dei Componenti core, vedi il documento [Versioni dei Componenti core](/help/versions.md).

### Dettagli tecnici {#technical-details}

La documentazione tecnica più recente sul componente Condivisione [è disponibile su GitHub](https://adobe.com/go/aem_cmp_tech_sharing_v1_it).

Per ulteriori informazioni sullo sviluppo di Componenti core, vedi la [documentazione per gli sviluppatori di Componenti core](/help/developing/overview.md).

## Finestra di dialogo per modifica {#edit-dialog}

![Finestra di dialogo per modifica del componente Condivisione](/help/assets/sharing-edit.png)

* **ID**: questa opzione consente di controllare l’identificatore univoco del componente nel codice HTML e nel [livello dati](/help/developing/data-layer/overview.md).
   * Se non specificato, viene generato automaticamente un ID univoco reperibile sulla pagina risultante.
   * Se l’ID viene specificato, è responsabilità dell’autore accertarsi che sia univoco.
   * La modifica dell’ID può avere un impatto sul tracciamento di CSS, JS e livello dati.

Poiché la condivisione richiede speciali intestazioni di pagina, qualsiasi condivisione deve essere abilitata a livello di pagina. Pertanto, per l’autore di contenuto sono disponibili opzioni di modifica aggiuntive per il componente Condivisione nella scheda [Proprietà](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html?lang=it) della pagina.

## Finestra di dialogo per progettazione {#design-dialog}

Poiché la condivisione richiede speciali intestazioni di pagina, qualsiasi condivisione deve essere abilitata a livello di pagina. Pertanto, per l’autore del modello le opzioni di progettazione per il componente Condivisione sono disponibili nella scheda [Proprietà](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=it) della pagina iniziale.
