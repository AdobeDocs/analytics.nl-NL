---
description: Hiermee geeft u webpaginaverkeer weer en geeft u paginaweergaven in real-time weer. Verstrekt activeerbare gegevens om uw bedrijfsbesluiten op te baseren.
title: Real-time rapporten
feature: Real-time
exl-id: 267246ba-617f-4284-aaad-d0ace0f6a8cf
source-git-commit: b8efacacf7fca792b4a4fa41dd3f9d6ac1448578
workflow-type: tm+mt
source-wordcount: '578'
ht-degree: 0%

---

# Real-time rapporten

Hiermee geeft u webpaginaverkeer weer en geeft u paginaweergaven in real-time weer. Verstrekt activeerbare gegevens om uw bedrijfsbesluiten op te baseren.

>[!NOTE]
>
>Voor het Real-Time Report is geen aanvullende implementatie of codering vereist. Het gebruikt uw bestaande implementatie van Adobe Analytics. Om rapporten in real time te vormen, zie [Configuratie van realtime rapporten](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/realtime/t-realtime-admin.md).

Navigeer naar:

**[!UICONTROL Workspace]** > **[!UICONTROL Reports]** > **[!UICONTROL Engagement]** > **[!UICONTROL Real-Time]**.

Real-Time beantwoordt de volgende vragen: Wat is trending op mijn plaats, en waarom? Hiermee kunt u als markeerteken snel reageren op en actief de prestaties van uw marketinginhoud en -campagnes beheren. De gegevens in real time die worden gerapporteerd zijn minder dan twee minuten latent en auto-updates op een minuut-door-minuut basis.

![](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/realtime/assets/report-realtime.png)

Het dashboard bevat hoogfrequente Adobe Analytics-meetgegevens en siteanalyses om visueel verkeer en paginaweergavetrending van dynamische nieuws- en handelswebsites te melden. In real time begrijpt tendensen in uw gegevens van minuut aan minuut, binnen seconden van inzameling. Het verzamelt en stroomt gegevens in auto-bijwerkt UI, gebruikend correlatie in real time en het volgen van inhoud en wat omzetting.

Twee van de meest gangbare gebruiksscenario&#39;s zijn uitgevers die artikelen willen promoten/verwijderen als de gebruikersactiviteit verandert, en marketers die de lancering van een nieuwe productlijn willen volgen.

Als beheerder kunt u

* Maak tot 3 rapporten in real time per rapportreeks, gebruikend bestaande dimensies of classificaties en metriek. Gebruik de secundaire afmetingen om de correlatie met (of onderbreking) de primaire dimensie te bepalen.
* Voeg 3 afmetingen (of classificaties) per rapport (één primaire en twee secundaire) toe, naast 1 plaats-brede metrisch.
* Gebruik een aangepaste gebeurtenis, winkelwagentje of een andere instantie.
* U kunt maximaal 2 uur historische realtime gegevens weergeven en deze instelling wijzigen:

   * Afgelopen 15 minuten: granulariteit van 1 minuut
   * Laatste 30 minuten: 1 minuut granulariteit
   * Laatste 1 uur: 2 minuten granulariteit
   * Afgelopen 2 uur: korreligheid van 4 minuten

* Vergelijk bijvoorbeeld de waarden van vorige week met de waarden van vorig jaar (en met het totaal van vandaag).

Vergeet niet dat eVars (conversiemetriek) niet worden ondersteund, omdat er geen concept van persistentie bestaat. Hoewel u conversiemetriek kunt selecteren, werken deze alleen als ze op dezelfde pagina zijn ingesteld als de dimensie(s). Zie het waarschuwingsbericht dat is vastgelegd in [Real-Time rapporten instellen](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/realtime/t-realtime-admin.md).

De vestiging en het bekijken van rapporten in real time is beperkt tot Admins of om het even welke gebruiker in de &quot;Alle Toegang van het Rapport&quot;en &quot;Geavanceerde het Melden&quot;toestemmingsgroepen. Nochtans, in real time eerbiedigt toestemmingen. Als, bijvoorbeeld, u geen rechten hebt om opbrengst te zien, zult u geen rapport in real time kunnen bekijken dat opbrengstgegevens omvat.

## De Latentie van gegevens als resultaat van Configuratie A4T {#latency}

Nadat de integratie van A4T in Adobe Target is ingeschakeld, krijgt u in Adobe Analytics nog 5 tot 10 minuten vertraging. Door deze latentieverhoging kunnen gegevens van Analytics en Target op dezelfde hit worden opgeslagen, zodat u tests kunt onderbreken op pagina en sitesectie.

Deze toename wordt weerspiegeld in alle Adobe Analytics-services en -gereedschappen, inclusief de live stream en real-time rapportage, en is van toepassing in de volgende scenario&#39;s:

* Voor live stream, real-time rapporten en API-aanvragen en huidige gegevens voor verkeersvariabelen worden alleen hits met een aanvullende gegevens-id vertraagd.
* Voor huidige gegevens over conversiemetriek, voltooide gegevens, en gegevensvoer, worden alle klappen een extra 5-7 minuten vertraagd.

Houd er rekening mee dat de latentieverhoging begint nadat u de Identity Service hebt geïmplementeerd, zelfs als u deze integratie niet volledig hebt geïmplementeerd.
