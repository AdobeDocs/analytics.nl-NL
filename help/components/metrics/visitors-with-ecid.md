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

De &quot;Bezoekers met identiteitskaart van Experience Cloud [&#x200B; metrisch &#x200B;](overview.md) toont het aantal unieke bezoekers die door Adobe werden geïdentificeerd gebruikend de [&#x200B; dienst van identiteitskaart van Experience Cloud &#x200B;](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=nl-NL). Dit metrisch is nuttig om met [&#x200B; Unieke bezoekers &#x200B;](unique-visitors.md) metrisch te vergelijken om de meerderheid van bezoekers aan uw plaats te verzekeren gebruikt de dienst van identiteitskaart. Als een groot deel van bezoekers de de dienstkoekjes van identiteitskaart niet gebruikt, kan het op een kwestie binnen uw implementatie wijzen.

>[!NOTE]
>
>Deze metrische waarde is vooral belangrijk voor het zuiveren als u de veelvoudige diensten van Experience Cloud, zoals Adobe Target of Adobe Audience Manager gebruikt. Segmenten die worden gedeeld door Experience Cloud-producten, omvatten geen bezoekers zonder Experience Cloud-id.

## Hoe deze metrische waarde wordt berekend

Deze metrisch is gebaseerd op [&#x200B; Unieke bezoekers &#x200B;](unique-visitors.md) metrisch, behalve omvat het slechts individuen die gebruikend het `mid` vraagkoord worden geïdentificeerd (dat op het [`s_ecid` &#x200B;](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-analytics.html?lang=nl-NL) koekje wordt gebaseerd).

## Fouten opsporen in de configuratie van Experience Cloud-id&#39;s

De metrische &#39;Bezoekers met Experience Cloud-id&#39; kan nuttig zijn bij het oplossen van problemen met de integratie in Experience Cloud of bij het identificeren van gebieden van uw site waarvoor de id-service niet is geïmplementeerd.

Sleep Bezoekers met Experience Cloud-id naast elkaar met Unieke bezoekers om ze te vergelijken:

![&#x200B; Unieke bezoekersvergelijking &#x200B;](assets/metric-mcvid1.png)

In dit voorbeeld heeft elke pagina hetzelfde aantal &#39;Unieke bezoekers&#39; als &#39;Bezoekers met een Experience Cloud-id&#39;. Het totale aantal unieke bezoekers is echter groter dan het totale aantal bezoekers met Experience Cloud-id. U kunt a [&#x200B; berekende metrisch &#x200B;](../calculated-metrics/cm-overview.md) tot stand brengen om te weten te komen welke pagina&#39;s niet de dienst van identiteitskaart plaatsen. U kunt de volgende definitie gebruiken:

![&#x200B; Berekende metrische definitie &#x200B;](assets/metric-mcvid2.png)

Door berekende metrisch aan het rapport toe te voegen, kunt u het rapport van Pagina&#39;s sorteren zodat de pagina&#39;s met het hoogste aantal bezoekers zonder MCID worden bedekt:

![&#x200B; Pagina&#39;s zonder de dienst van identiteitskaart &#x200B;](assets/metric-mcvid3.png)

Merk op dat het de afmetingspunt van &quot;Snelle meningen van het Product&quot;niet behoorlijk met de Dienst van de Identiteit wordt uitgevoerd. U kunt met de juiste teams binnen uw organisatie samenwerken om deze pagina&#39;s zo snel mogelijk bij te werken. U kunt een gelijkaardig rapport met om het even welk type van afmeting zoals [&#x200B; Browser type &#x200B;](../dimensions/browser-type.md), [&#x200B; sectie van de Plaats &#x200B;](../dimensions/site-section.md), of om het even welk [&#x200B; eVar &#x200B;](../dimensions/evar.md) construeren.
