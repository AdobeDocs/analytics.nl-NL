---
title: Bezoekers met Experience Cloud ID
description: Het aantal unieke bezoekers dat de Adobe Experience Cloud ID-service gebruikt.
exl-id: 16c170d0-3546-4e0a-8f3c-c141b8a0e4fe
source-git-commit: f669af03a502d8a24cea3047b96ec7cba7c59e6f
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 2%

---

# Bezoekers met Experience Cloud ID

De metrische &#39;Bezoekers met Experience Cloud-id&#39; toont het aantal unieke bezoekers dat door Adobe is geïdentificeerd met de [Experience Cloud-id-service](https://experienceleague.adobe.com/docs/id-service/using/home.html). Deze dimensie is nuttig om met [Unieke bezoekers](unique-visitors.md) metrisch te vergelijken om ervoor te zorgen de meerderheid van bezoekers aan uw plaats de dienst van identiteitskaart gebruikt. Als een groot deel van bezoekers de de dienstkoekjes van identiteitskaart niet gebruikt, kan het op een kwestie binnen uw implementatie wijzen.

>[!NOTE]
>
>Deze metrische waarde is vooral belangrijk voor het zuiveren als u de veelvoudige diensten van de Experience Cloud, zoals Adobe Target of Adobe Audience Manager gebruikt. De segmenten die over de producten van Experience Cloud worden gedeeld omvatten bezoekers zonder Experience Cloud identiteitskaart niet.

## Hoe deze metrische waarde wordt berekend

Deze metrische waarde is gebaseerd op de [Unieke bezoekers](unique-visitors.md) metrisch, behalve het omvat slechts individuen die gebruikend `mid` vraagkoord (gebaseerd op [`s_ecid`](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-analytics.html) koekje worden geïdentificeerd).

## Fouten opsporen bij het instellen van de Experience Cloud-id

De metrische waarde &#39;Bezoekers met Experience Cloud-id&#39; kan handig zijn bij het oplossen van problemen met de integratie van Experience Cloud, of bij het identificeren van gebieden van uw site die de id-service niet hebben geïmplementeerd.

Sleep Bezoekers met Experience Cloud-id naast elkaar met Unieke bezoekers om ze te vergelijken:

![Unieke vergelijking van bezoekers](assets/metric-mcvid1.png)

In dit voorbeeld heeft elke pagina hetzelfde aantal &#39;Unieke bezoekers&#39; als &#39;Bezoekers met een Experience Cloud-id&#39;. Het totale aantal unieke bezoekers is echter groter dan het totale aantal bezoekers met Experience Cloud-id. U kunt een [berekende metrisch](../c-calcmetrics/cm-overview.md) tot stand brengen om te weten te komen welke pagina&#39;s niet de dienst van identiteitskaart plaatsen. U kunt de volgende definitie gebruiken:

![Berekende metrische definitie](assets/metric-mcvid2.png)

Door berekende metrisch aan het rapport toe te voegen, kunt u het rapport van Pagina&#39;s sorteren zodat de pagina&#39;s met het hoogste aantal bezoekers zonder MCID worden bedekt:

![Pagina&#39;s zonder id-service](assets/metric-mcvid3.png)

Merk op dat het de afmetingspunt van &quot;Snelle meningen van het Product&quot;niet behoorlijk met de Dienst van de Identiteit wordt uitgevoerd. U kunt met de juiste teams binnen uw organisatie samenwerken om deze pagina&#39;s zo snel mogelijk bij te werken. U kunt een gelijkaardig rapport met om het even welk type van afmeting zoals [Browsertype](../dimensions/browser-type.md), [Sitesectie](../dimensions/site-section.md), of om het even welk [eVar](../dimensions/evar.md) construeren.
