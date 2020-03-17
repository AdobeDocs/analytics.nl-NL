---
description: Met analyses van realtime pagina's (Live Mode) kunt u resultaten behalen met een kleine granulariteit in real-time.
title: Analyse van real-time (Live) pagina
topic: Activity map
uuid: a3faa9bd-73d8-48b3-be2b-f818ed7456fb
translation-type: tm+mt
source-git-commit: ''

---


# Analyse van real-time (Live) pagina

Met analyses van realtime pagina&#39;s (Live Mode) kunt u resultaten behalen met een kleine granulariteit in real-time.

Activiteitenkaart geeft nu in stappen van 1 tot 15 minuten analytische gegevens weer om de populariteit van koppelingen te controleren op basis van microtrends voor geselecteerde pagina&#39;s. Dit is vooral belangrijk voor uitgeverijen bij het volgen van en het antwoorden op stijgende of dalende interesse in verhalen en om verkeer in real time te controleren.

Als eigenaar van site-inhoud is het voor een deel uw taak om te begrijpen wanneer u inhoud wilt promoten en verwijderen en om onze ervaring constant relevant te houden. Realtime gegevens zijn het levensbloed van deze verantwoordelijkheid. Als u begrijpt welke koppelingen en inhoud op dit moment worden doorgestuurd, kunt u snel en resoluut optreden om lezers en klanten betrokken te houden bij uw merk.

![](assets/live_mode.png)

<!-- 

Describe what you can do with the feature: - what is the data shown? why do I see trend lines everywhere? how do I choose a period in the trend? what do the overlays represent in live mode? how do you compute the gainers and losers overlays? what is the auto update mode?

 -->

## De latentie van gegevens als resultaat van configuratie A4T {#section_806CE36354FC4C539A0DED9266A5C704}

Nadat de integratie van A4T in Adobe Target is ingeschakeld, duurt het nog 5 tot 10 minuten langer voordat Adobe Analytics is geïnstalleerd. Door deze latentieverhoging kunnen gegevens van Analytics en Target op dezelfde hit worden opgeslagen, zodat u tests kunt onderbreken op pagina en sitesectie.

Deze toename wordt weerspiegeld in alle Adobe Analytics-services en -hulpprogramma&#39;s, inclusief de live stream en realtime rapportage, en is van toepassing in de volgende scenario&#39;s:

* Voor live stream, real-time rapporten en API-aanvragen en huidige gegevens voor verkeersvariabelen worden alleen hits met een aanvullende gegevens-id vertraagd.
* Voor huidige gegevens over conversiemetriek, voltooide gegevens, en gegevensvoer, worden alle klappen een extra 5-7 minuten vertraagd.

Houd er rekening mee dat de latentieverhoging begint nadat u de [identiteitsservice](https://marketing.adobe.com/resources/help/en_US/mcvid/)hebt geïmplementeerd, zelfs als u deze integratie niet volledig hebt geïmplementeerd.
