---
title: Bezoekers met Experience Cloud-id
description: Het aantal unieke bezoekers dat de Adobe Experience Cloud ID-service gebruikt.
feature: Metrics
exl-id: 16c170d0-3546-4e0a-8f3c-c141b8a0e4fe
source-git-commit: 325a42c080290509309e90c9127138800d5ac496
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 0%

---

# Bezoekers met Experience Cloud-id

De &quot;Bezoekers met identiteitskaart van Experience Cloud [ metrisch ](overview.md) toont het aantal unieke bezoekers die door Adobe werden geïdentificeerd gebruikend de [ dienst van identiteitskaart van Experience Cloud ](https://experienceleague.adobe.com/docs/id-service/using/home.html). Dit metrisch is nuttig om met [ Unieke bezoekers ](unique-visitors.md) metrisch te vergelijken om de meerderheid van bezoekers aan uw plaats te verzekeren gebruikt de dienst van identiteitskaart. Als een groot deel van bezoekers de de dienstkoekjes van identiteitskaart niet gebruikt, kan het op een kwestie binnen uw implementatie wijzen.

>[!NOTE]
>
>Deze metrische waarde is vooral belangrijk voor het zuiveren als u de veelvoudige diensten van Experience Cloud, zoals Adobe Target of Adobe Audience Manager gebruikt. Segmenten die worden gedeeld door Experience Cloud-producten, omvatten geen bezoekers zonder Experience Cloud-id.

## Hoe deze metrische waarde wordt berekend

Deze metrisch is gebaseerd op [ Unieke bezoekers ](unique-visitors.md) metrisch, behalve omvat het slechts individuen die gebruikend het `mid` vraagkoord worden geïdentificeerd (dat op het [`s_ecid` ](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-analytics.html) koekje wordt gebaseerd).

## Fouten opsporen in de configuratie van Experience Cloud-id&#39;s

De metrische &#39;Bezoekers met Experience Cloud-id&#39; kan nuttig zijn bij het oplossen van problemen met de integratie in Experience Cloud of bij het identificeren van gebieden van uw site waarvoor de id-service niet is geïmplementeerd.

Sleep Bezoekers met Experience Cloud-id naast elkaar met Unieke bezoekers om ze te vergelijken:

![ Unieke bezoekersvergelijking ](assets/metric-mcvid1.png)

In dit voorbeeld heeft elke pagina hetzelfde aantal &#39;Unieke bezoekers&#39; als &#39;Bezoekers met een Experience Cloud-id&#39;. Het totale aantal unieke bezoekers is echter groter dan het totale aantal bezoekers met Experience Cloud-id. U kunt a [ berekende metrisch ](../calculated-metrics/cm-overview.md) tot stand brengen om te weten te komen welke pagina&#39;s niet de dienst van identiteitskaart plaatsen. U kunt de volgende definitie gebruiken:

![ Berekende metrische definitie ](assets/metric-mcvid2.png)

Door berekende metrisch aan het rapport toe te voegen, kunt u het rapport van Pagina&#39;s sorteren zodat de pagina&#39;s met het hoogste aantal bezoekers zonder MCID worden bedekt:

![ Pagina&#39;s zonder de dienst van identiteitskaart ](assets/metric-mcvid3.png)

Merk op dat het de afmetingspunt van &quot;Snelle meningen van het Product&quot;niet behoorlijk met de Dienst van de Identiteit wordt uitgevoerd. U kunt met de juiste teams binnen uw organisatie samenwerken om deze pagina&#39;s zo snel mogelijk bij te werken. U kunt een gelijkaardig rapport met om het even welk type van afmeting zoals [ Browser type ](../dimensions/browser-type.md), [ sectie van de Plaats ](../dimensions/site-section.md), of om het even welk [ eVar ](../dimensions/evar.md) construeren.
