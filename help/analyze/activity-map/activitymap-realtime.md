---
description: Met analyses van realtime pagina's (Live Mode) kunt u resultaten behalen met een kleine granulariteit in real-time.
title: Analyse van real-time (Live) pagina
topic: Activity map
translation-type: tm+mt
source-git-commit: 713a73a1d57d93c579e0da58e464cecab3f9d773

---


# Analyse van pagina&#39;s in realtime (Live modus)

Met analyses van realtime pagina&#39;s (Live Mode) kunt u resultaten behalen met een kleine granulariteit in real-time.

Met Activiteitenkaart worden nu de analysegegevens in stappen van 1 tot 15 minuten weergegeven om de populariteit van koppelingen te controleren op basis van microtrends voor geselecteerde pagina&#39;s. Dit is vooral belangrijk voor uitgeverijen bij het volgen van en het antwoorden op stijgende of dalende interesse in verhalen en om verkeer in real time te controleren.

Als eigenaar van site-inhoud is het voor een deel uw taak om te begrijpen wanneer u inhoud wilt promoten en verwijderen en om onze ervaring constant relevant te houden. Realtime gegevens zijn het levensbloed van deze verantwoordelijkheid. Als u begrijpt welke koppelingen en inhoud op dit moment worden doorgestuurd, kunt u snel en resoluut optreden om lezers en klanten betrokken te houden bij uw merk.

![](assets/live_mode.png)

<!-- 

Describe what you can do with the feature: - what is the data shown? why do I see trend lines everywhere? how do I choose a period in the trend? what do the overlays represent in live mode? how do you compute the gainers and losers overlays? what is the auto update mode?

 -->

Als u wilt controleren op welk element het meest wordt geklikt in Live-modus:

1. Selecteer de tijdsperiode op de de **[!UICONTROL Live Mode]** trendlijn van Toolbar die u wilt analyseren.
1. Klik op het oogpictogram op de werkbalk om de tabel Koppelingenrapport te openen.
1. Orde de de lijst door de Verbinding.

## De latentie van gegevens als resultaat van configuratie A4T

Nadat de integratie [](https://docs.adobe.com/content/help/en/target/using/integrate/a4t/a4t.html) A4T in Adobe Target is ingeschakeld, wordt er een extra vertraging van 5 tot 10 minuten waargenomen in Adobe Analytics. Door deze latentieverhoging kunnen gegevens van Analytics en Target op dezelfde hit worden opgeslagen, zodat u tests kunt onderbreken op pagina en sitesectie.

Deze toename wordt weerspiegeld in alle Adobe Analytics-services en -hulpprogramma&#39;s, inclusief de live stream en realtime rapportage, en is van toepassing in de volgende scenario&#39;s:

* Voor live stream, real-time rapporten en API-aanvragen en huidige gegevens voor verkeersvariabelen worden alleen hits met een aanvullende gegevens-id vertraagd.
* Voor huidige gegevens over conversiemetriek, voltooide gegevens, en gegevensvoer, worden alle klappen een extra 5-7 minuten vertraagd.

Houd er rekening mee dat de latentieverhoging begint nadat u de [identiteitsservice](https://marketing.adobe.com/resources/help/en_US/mcvid/)hebt geïmplementeerd, zelfs als u deze integratie niet volledig hebt geïmplementeerd.

Meer informatie [hier](/help/analyze/activity-map/activitymap-standard-live.md).