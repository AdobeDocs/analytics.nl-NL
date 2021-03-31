---
description: Met analyses van realtime pagina's (Live Mode) kunt u resultaten behalen met een kleine granulariteit in real-time.
title: Analyse van realtimepagina-analyse (Live)
feature: Activity Map
role: Bedrijfs Praktijk, Beheerder
translation-type: tm+mt
source-git-commit: 894ee7a8f761f7aa2590e06708be82e7ecfa3f6d
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 7%

---


# Analyse van pagina&#39;s in realtime (Live modus)

Met analyses van realtime pagina&#39;s (Live Mode) kunt u resultaten behalen met een kleine granulariteit in real-time.

Activity Map geeft nu analysegegevens weer in stappen van 1 minuut tot 15 minuten om de populariteit van koppelingen te controleren op basis van microtrends voor geselecteerde pagina&#39;s. Dit is vooral belangrijk voor uitgeverijen bij het volgen van en het antwoorden op stijgende of dalende interesse in verhalen en om verkeer in real time te controleren.

Als eigenaar van site-inhoud moet u begrijpen wanneer u inhoud wilt promoten en verwijderen en onze ervaring constant relevant houden. Realtime gegevens zijn het levensbloed van deze verantwoordelijkheid. Als u begrijpt welke koppelingen en inhoud op dit moment worden doorgestuurd, kunt u snel en resoluut optreden om lezers en klanten betrokken te houden bij uw merk.

![](assets/live_mode.png)

<!-- 

Describe what you can do with the feature: - what is the data shown? why do I see trend lines everywhere? how do I choose a period in the trend? what do the overlays represent in live mode? how do you compute the gainers and losers overlays? what is the auto update mode?

 -->

Als u wilt controleren op welk element het meest wordt geklikt in Live-modus:

1. Selecteer de tijdspanne op de de trendlijn **[!UICONTROL Live Mode]** van Toolbar die u wilt analyseren.
1. Klik op het oogpictogram op de werkbalk om de tabel Koppelingenrapport te openen.
1. Orde de de lijst door de Verbinding.

## De latentie van gegevens als resultaat van configuratie A4T

Nadat [A4T integration](https://docs.adobe.com/content/help/nl-NL/target/using/integrate/a4t/a4t.html) in Adobe Target wordt toegelaten, zult u extra 5-10 minuten van latentie in Adobe Analytics ervaren. Door deze latentieverhoging kunnen gegevens van Analytics en Target op dezelfde hit worden opgeslagen, zodat u tests kunt onderbreken op pagina en sitesectie.

Deze toename wordt weerspiegeld in alle Adobe Analytics-services en -gereedschappen, inclusief de live stream en real-time rapportage, en is van toepassing in de volgende scenario&#39;s:

* Voor live stream, real-time rapporten en API-aanvragen en huidige gegevens voor verkeersvariabelen worden alleen hits met een aanvullende gegevens-id vertraagd.
* Voor huidige gegevens over conversiemetriek, voltooide gegevens, en gegevensvoer, worden alle klappen een extra 5-7 minuten vertraagd.

Houd er rekening mee dat de latentieverhoging begint nadat u [Identity Service](https://docs.adobe.com/content/help/nl-NL/id-service/using/home.html) implementeert, zelfs als u deze integratie niet volledig hebt geïmplementeerd.

Meer informatie [hier](/help/analyze/activity-map/activitymap-standard-live.md).