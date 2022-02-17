---
title: Personen met Experience Cloud-id
description: Het aantal personen in Apparaatanalyse met een Experience Cloud-id.
feature: Metrics
exl-id: 072e7d2b-3a08-49c6-a892-4cea2cc10159
source-git-commit: 7d5383e1ee3bee189d3dd48bc6b899f4108f7ba8
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 0%

---

# Personen met Experience Cloud-id

&#39;Personen met Experience Cloud-id&#39; is een [Apparaatanalyse](../cda/overview.md) metrisch die het aantal van toont [Mensen](people.md) die door Adobe zijn geïdentificeerd met behulp van de [Experience Cloud ID-service](https://experienceleague.adobe.com/docs/id-service/using/home.html).

## Hoe deze metrische waarde wordt berekend

Elk object in overweging nemen [Mensen](people.md) (geïdentificeerd of niet geïdentificeerd), deze metrische toename als de slag bevat `mid` queryreeks (gebaseerd op de [`s_ecid`](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-analytics.html) cookie).

U kunt de berekende metrisch creëren `[People with ECID] ÷ [People]` om het percentage bezoekers van uw site te verkrijgen met de id-service.

Zie de equivalente niet-CDA metrische waarde [Bezoekers met Experience Cloud-id](visitors-with-ecid.md) voor meer informatie over belang van Experience Cloud ID en het zuiveren van uw opstelling.
