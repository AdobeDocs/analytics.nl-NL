---
title: Nieuwe contracten
description: Het aantal keren dat een eerste aanraakkanaal wordt ingesteld.
feature: Metrics
exl-id: a419d048-9715-4d7b-9c24-d34129755371
source-git-commit: e934de3938f013067d6bbd6b516b0444b0c9f782
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---

# Nieuwe contracten

De &quot;Nieuwe overeenkomsten&quot;[ metrische ](overview.md) toont het aantal tijden een bezoeker een marketing kanaal voor het eerst in de de betrokkenheidsperiode van die bezoeker aanpast. Deze metrische waarde is handig wanneer u een dimensie wilt vergelijken met een bezoeker die voor het eerst een verwerkingsregel voor marketingkanalen toepast.

## Hoe deze metrische waarde wordt berekend

Tijdens gegevensverwerking, loopt elke slag door [ de verwerkingsregels van het het kanaalkanaal van de Marketing ](/help/admin/tools/manage-rs/edit-settings/marketing-channels/mc-proc-rules.md). Als een hit overeenkomt met een verwerkingsregel voor marketingkanalen en de bezoeker nog geen eerste aanraakkanaal heeft, wordt een nieuwe afspraak gemaakt. Als een hit niet overeenkomt met de verwerkingsregels voor marketingkanalen of als de bezoeker al een eerste aanraakkanaal heeft, is de hit geen nieuwe afspraak.

Bezoekers kunnen meer dan één nieuwe betrokkenheid hebben als ze hun periode van betrokkenheid bij bezoekers laten verlopen.
