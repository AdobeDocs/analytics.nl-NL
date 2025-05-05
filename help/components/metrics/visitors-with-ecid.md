---
title: Bezoekers met Experience Cloud ID
description: Het aantal unieke bezoekers dat de Adobe Experience Cloud ID-service gebruikt.
feature: Metrics
exl-id: 16c170d0-3546-4e0a-8f3c-c141b8a0e4fe
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 2%

---

# Bezoekers met Experience Cloud ID

De &#39;Bezoekers met Experience Cloud-id&#39; [metrisch](overview.md) toont het aantal unieke bezoekers dat door Adobe met de [Experience Cloud ID-service](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=nl-NL). Deze maatstaf is handig om te vergelijken met de [Unieke bezoekers](unique-visitors.md) Nauwkeurig om ervoor te zorgen de meerderheid van bezoekers aan uw plaats de dienst van identiteitskaart gebruikt. Als een groot deel van bezoekers de de dienstkoekjes van identiteitskaart niet gebruikt, kan het op een kwestie binnen uw implementatie wijzen.

>[!NOTE]
>
>Deze metrische waarde is vooral belangrijk voor het zuiveren als u de veelvoudige diensten van het Experience Cloud, zoals Adobe Target of Adobe Audience Manager gebruikt. De segmenten die over de producten van de Experience Cloud worden gedeeld omvatten bezoekers zonder een Experience Cloud identiteitskaart.

## Hoe deze metrische waarde wordt berekend

Deze metrisch is gebaseerd op [Unieke bezoekers](unique-visitors.md) metrisch, behalve dat het alleen personen omvat die met de `mid` queryreeks (gebaseerd op de [`s_ecid`](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-analytics.html?lang=nl-NL) cookie).

## Fouten opsporen in de instellingen van uw Experience Cloud-id

De metrische waarde &#39;Bezoekers met Experience Cloud-id&#39; kan handig zijn bij de integratie van Experiencen Cloud voor probleemoplossing of bij het identificeren van gebieden van uw site die de id-service niet hebben geïmplementeerd.

Sleep Bezoekers met Experience Cloud-id naast elkaar met Unieke bezoekers om ze te vergelijken:

![Unieke vergelijking van bezoekers](assets/metric-mcvid1.png)

In dit voorbeeld heeft elke pagina hetzelfde aantal &#39;Unieke bezoekers&#39; als &#39;Bezoekers met Experience Cloud-id&#39;. Het totale aantal unieke bezoekers is echter groter dan het totale aantal bezoekers met Experience Cloud-id. U kunt een [berekend metrisch](../c-calcmetrics/cm-overview.md) om te zien welke pagina&#39;s de id-service niet instellen. U kunt de volgende definitie gebruiken:

![Berekende metrische definitie](assets/metric-mcvid2.png)

Door berekende metrisch aan het rapport toe te voegen, kunt u het rapport van Pagina&#39;s sorteren zodat de pagina&#39;s met het hoogste aantal bezoekers zonder MCID worden bedekt:

![Pagina&#39;s zonder id-service](assets/metric-mcvid3.png)

Merk op dat het de afmetingspunt van &quot;Snelle meningen van het Product&quot;niet behoorlijk met de Dienst van de Identiteit wordt uitgevoerd. U kunt met de juiste teams binnen uw organisatie samenwerken om deze pagina&#39;s zo snel mogelijk bij te werken. U kunt een gelijkaardig rapport met om het even welk type van afmeting construeren zoals [Browsertype](../dimensions/browser-type.md), [Sectie Site](../dimensions/site-section.md), of [eVar](../dimensions/evar.md).
