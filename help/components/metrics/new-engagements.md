---
title: Nieuwe contracten
description: Het aantal keren dat een eerste aanraakkanaal wordt ingesteld.
feature: Metrics
exl-id: a419d048-9715-4d7b-9c24-d34129755371
source-git-commit: 7d5383e1ee3bee189d3dd48bc6b899f4108f7ba8
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---

# Nieuwe contracten

De maatstaf &#39;Nieuwe overeenkomsten&#39; toont het aantal keren dat een bezoeker een marketingkanaal aanpast voor het eerst in de betrokkenheidsperiode van die bezoeker. Deze metrische waarde is handig wanneer u een dimensie wilt vergelijken met een bezoeker die voor het eerst een verwerkingsregel voor marketingkanalen toepast.

## Hoe deze metrische waarde wordt berekend

Tijdens gegevensverwerking loopt elke hit door [Verwerkingsregels voor distributiekanalen](../c-marketing-channels/c-rules.md). Als een hit overeenkomt met een verwerkingsregel voor marketingkanalen en de bezoeker nog geen eerste aanraakkanaal heeft, wordt een nieuwe afspraak gemaakt. Als een hit niet overeenkomt met de verwerkingsregels voor marketingkanalen of als de bezoeker al een eerste aanraakkanaal heeft, is de hit geen nieuwe afspraak.

Bezoekers kunnen meer dan één nieuwe betrokkenheid hebben als ze hun periode van betrokkenheid bij bezoekers laten verlopen.
