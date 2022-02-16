---
description: Elk van de bovenste vergelijkingstabellen toont een verschilscore die door verscheidene statistische tests afhankelijk van wordt berekend die wordt gemaakt; nochtans, ongeacht welke test wordt gebruikt, wordt de verschilscore getoond als waarde tussen 0 en 1.
keywords: Analysis Workspace;Segment-IQ
title: Statistische tests bij segmentvergelijking
feature: Segmentation
role: User, Admin
exl-id: b1c235ca-2eab-48d2-bf11-e8a8c4067d03
source-git-commit: 1ee50c6a2231795b2ad0015a79e09b7c1c74d850
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 2%

---

# Statistische tests bij segmentvergelijking

Elk van de bovenste vergelijkingstabellen toont een verschilscore die door verscheidene statistische tests afhankelijk van wordt berekend die wordt gemaakt; nochtans, ongeacht welke test wordt gebruikt, wordt de verschilscore getoond als waarde tussen 0 en 1.

Een score van 0 betekent dat er geen verschil is tussen de twee segmenten en een score van 1 betekent dat er een zeer groot verschil was tussen de twee segmenten. Er worden twee soorten statistische tests gebruikt om deze verschillen te genereren: Voor de Top Metrics lijst wordt een Mann-Whitney U test gebruikt, en voor de Top Dimension Items en Top Segments lijst wordt een vergelijking van het risicoverschil gebruikt.

## Beste metrische verschilscore {#section_5E8047464EB945C78543B25F8F30F17A}

In de Bovenste lijst van Metriek, gebruikt het Hulpmiddel van de Vergelijking van het Segment een twee steekproef Mann-Whitney U Test, die een nonparametric gelijkheidstest is die wordt gebruikt om de eendimensionale kansverdelingen van elke metrisch voor elk overwogen segment te vergelijken. De verschilscore in de metriekentabel is een combinatie van de p-waarde van het berekende U-statistiek (die aangeeft hoe stochastisch verschillend de twee segmenten over een bepaalde metrische waarde worden verdeeld) en de relatieve grootte van het waargenomen verschil. Een grote verschilscore (dicht bij 1) betekent dat de specifieke maatstaf een groot relatief verschil heeft en een hoog statistisch vertrouwen heeft dat de segmenten verschillend zijn.

## Items met de bovenste dimensie en de verschilscores voor de bovenste segmenten {#section_8073ADA6053B44C9A23FDC5ED4AF2AC4}

Voor het berekenen van de verschilscore op de bovenste Dimension-items en de bovenste segmentverschiltabellen wordt een algoritme voor het differentiëren van het relatieve risico gebruikt (vergelijkbaar met de risicoverhouding, hoewel een verschil wordt gebruikt in plaats van een verhouding). Een risicoverschil wordt berekend door de cumulatieve incidenties van een dimensie-item (of overlapping met een segment uit de segmenttabel) van het ene geselecteerde segment af te trekken van het andere. Een hoge verschilscore (dicht bij 1) betekent dat het specifieke dimensie-item of het tertiaire segment in een van de geselecteerde segmenten en niet in de andere segmenten een vooraanstaande positie innam.

>[!NOTE]
>
>In alle drie de tabellen is de verschilstatistiek gebaseerd op een passende steekproef van bezoekers om het proces zo snel mogelijk te laten lopen en statistisch accuraat te blijven. Hoewel de verschilscore is gebaseerd op een voorbeeld, worden de resultaten in de tabel niet gesampled. Om statistische significantie te verzekeren, steunt elke statistische test op een dynamisch toewijzingsalgoritme zodat het kleinere segment een steekproefgrootte bevat die minder dan 3% foutenmarge verstrekt. Als een segment zeer weinig bezoekers (minder dan 1.000) bevat, gebruiken wij alle beschikbare gegevens en nemen geen steekproef in het berekenen van de verschilscore.
