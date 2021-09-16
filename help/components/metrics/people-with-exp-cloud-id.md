---
title: Personen met Experience Cloud-id
description: Het aantal personen in Apparaatanalyse met een Experience Cloud-id.
source-git-commit: eaf0c3b751a5fbdc70ad6bef501dbf9e8400339c
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 0%

---

# Personen met Experience Cloud-id

&#39;Personen met een Experience Cloud-id&#39; is een [Apparaatanalyse](../cda/overview.md)-meting die het aantal [Personen](people.md) toont dat door Adobe is geïdentificeerd met behulp van de [Experience Cloud-id-service](https://experienceleague.adobe.com/docs/id-service/using/home.html).

## Hoe deze metrische waarde wordt berekend

Met betrekking tot elke [Mensen](people.md) (geïdentificeerd of niet geïdentificeerd), verhoogt deze metrische verhogingen als de slag `mid` vraagkoord (die op [`s_ecid`](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-analytics.html) koekje wordt gebaseerd) bevat.

U kunt de berekende metrische `[People with ECID] ÷ [People]` tot stand brengen om het percentage bezoekers aan uw plaats te verkrijgen gebruikend de dienst van identiteitskaart.

Zie gelijkwaardige metrische [Bezoekers niet-CDA met Experience Cloud ID](visitors-with-ecid.md) voor meer informatie over belang van Experience Cloud identiteitskaart en het zuiveren van uw opstelling.
