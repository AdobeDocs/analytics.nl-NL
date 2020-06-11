---
title: Bezoekers met Experience Cloud ID
description: Het aantal unieke bezoekers dat de Adobe Experience Cloud ID-service gebruikt.
translation-type: tm+mt
source-git-commit: 0328de560185e716a3913080feda9cd078e0f206
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 0%

---


# Bezoekers met Experience Cloud ID

De maatstaf &#39;Bezoekers met Experience Cloud ID&#39; toont het aantal unieke bezoekers dat door Adobe is geïdentificeerd met de [Experience Cloud ID-service](https://docs.adobe.com/content/help/en/id-service/using/home.html). Deze dimensie is handig om te vergelijken met de metrische waarde voor [Unieke bezoekers](unique-visitors.md) om ervoor te zorgen dat de meeste bezoekers van uw site de id-service gebruiken. Als een groot deel van bezoekers de de dienstkoekjes van identiteitskaart niet gebruikt, kan het op een kwestie binnen uw implementatie wijzen.

>[!NOTE] Deze maatstaf is vooral belangrijk voor foutopsporing als u werkt met meerdere Experience Cloud-services, zoals Adobe Target of Adobe Audience Manager. Segmenten die worden gedeeld door producten uit de Experience Cloud, omvatten geen bezoekers zonder de Experience Cloud-id.

## Hoe deze metrische waarde wordt berekend

Deze metrische waarde is gebaseerd op de metrische waarde voor [Unieke bezoekers](unique-visitors.md) , maar bevat alleen personen die zijn geïdentificeerd met de `mid` queryreeks (gebaseerd op het [`s_ecid`](https://docs.adobe.com/content/help/en/core-services/interface/ec-cookies/cookies-analytics.html) cookie).

## Fouten opsporen in de installatie van uw Experience Cloud ID

De metrische &#39;Bezoekers met Experience Cloud ID&#39; kan handig zijn bij het oplossen van problemen met de integratie van Experience Cloud, of bij het identificeren van gebieden van uw site waarvoor de id-service niet is geïmplementeerd.

Sleep de Bezoekers met Experience Cloud ID naast de Unieke bezoekers om ze te vergelijken:

![Unieke vergelijking van bezoekers](assets/metric-mcvid1.png)

In dit voorbeeld heeft elke pagina hetzelfde aantal &#39;Unieke bezoekers&#39; als &#39;Bezoekers met een Experience Cloud ID&#39;. Het totale aantal unieke bezoekers is echter groter dan het totale aantal bezoekers met Experience Cloud ID. U kunt een [berekende metrisch](../c-calcmetrics/cm-overview.md) tot stand brengen om te weten te komen welke pagina&#39;s de dienst van identiteitskaart niet plaatsen. U kunt de volgende definitie gebruiken:

![Berekende metrische definitie](assets/metric-mcvid2.png)

Door berekende metrisch aan het rapport toe te voegen, kunt u het rapport van Pagina&#39;s sorteren zodat de pagina&#39;s met het hoogste aantal bezoekers zonder MCID worden bedekt:

![Pagina&#39;s zonder id-service](assets/metric-mcvid3.png)

Merk op dat de waarde van de &quot;Snelle meningen van het Product&quot;dimensie niet behoorlijk met de Dienst van de Identiteit wordt uitgevoerd. U kunt met de juiste teams binnen uw organisatie samenwerken om deze pagina&#39;s zo snel mogelijk bij te werken. U kunt een gelijkaardig rapport met om het even welk type van afmeting zoals [Browser type](../dimensions/browser-type.md), de sectie [van de](../dimensions/site-section.md)Plaats, of om het even welk [eVar](../dimensions/evar.md)construeren.
