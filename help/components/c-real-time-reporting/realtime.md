---
description: Hiermee geeft u webpaginaverkeer weer en geeft u paginaweergaven in real-time weer. Verstrekt activeerbare gegevens om uw bedrijfsbesluiten op te baseren.
title: Overzicht van real-time rapportage
topic-fix: Reports
feature: Real-time
exl-id: 056235bc-42ea-4118-aa54-bc7666044fe3
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '600'
ht-degree: 0%

---

# Overzicht van real-time rapportage

Real-time rapporten tonen het verkeer van de Web-pagina en rangschikken paginameningen in echt - tijd. Verstrekt activeerbare gegevens om uw bedrijfsbesluiten op te baseren.

>[!NOTE]
>
>Voor het Real-Time Report is geen aanvullende implementatie of codering vereist. Het gebruikt uw bestaande implementatie van Adobe Analytics. Om rapporten in real time te vormen, zie [ Real-Time de Configuratie van Rapporten ](/help/admin/tools/manage-rs/edit-settings/realtime/t-realtime-admin.md).

## Real-time toegang tot rapporten

1. In Analysis Workspace, selecteer [!UICONTROL **Workspace**] tabel.

1. Op de linkerkant van de pagina, onder **[!UICONTROL Templates]**, uitgezochte [!UICONTROL **malplaatjes van Adobe**].

1. Selecteer [!UICONTROL **Betrokkenheid**] > **[!UICONTROL Real-Time]**.

## Real-Time rapportage begrijpen

Real-Time beantwoordt de volgende vragen: Wat is trending op mijn plaats, en waarom? Hiermee kunt u als markeerteken snel reageren op en actief de prestaties van uw marketinginhoud en -campagnes beheren. De gegevens in real time die worden gerapporteerd zijn minder dan twee minuten latent en auto-updates op een minuut-door-minuut basis.

![](/help/admin/tools/manage-rs/edit-settings/realtime/assets/report-realtime.png)

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

Vergeet niet dat eVars (conversiemetriek) niet worden ondersteund, omdat er geen concept van persistentie bestaat. Hoewel u conversiemetriek kunt selecteren, werken deze alleen als ze op dezelfde pagina zijn ingesteld als de dimensie(s). Voor meer informatie, zie het waarschuwingsbericht dat in [ Vestiging Echt - tijdRapporten ](/help/components/c-real-time-reporting/t-realtime-admin.md) wordt gevangen.

De vestiging en het bekijken van rapporten in real time is beperkt tot Admins of om het even welke gebruiker in de &quot;Alle Toegang van het Rapport&quot;en &quot;Geavanceerde het Melden&quot;toestemmingsgroepen. Nochtans, in real time eerbiedigt toestemmingen. Als, bijvoorbeeld, u geen rechten hebt om opbrengst te zien, zult u geen rapport in real time kunnen bekijken dat opbrengstgegevens omvat.

## De Latentie van gegevens als resultaat van Configuratie A4T {#latency-a4t}

Nadat de integratie A4T in Adobe [!DNL Target] is ingeschakeld, hebt u nog 5 tot 10 minuten vertraging in Adobe Analytics. Door deze latentieverhoging kunnen gegevens van Analytics en [!DNL Target] op dezelfde hit worden opgeslagen, zodat u tests kunt onderverdelen op pagina en sitesectie.

Deze toename wordt weerspiegeld in alle Adobe Analytics-services en -gereedschappen, inclusief de live stream en real-time rapportage, en is van toepassing in de volgende scenario&#39;s:

* Voor live stream, real-time rapporten en API-aanvragen, en huidige gegevens voor verkeersvariabelen, worden alleen hits met een aanvullende gegevens-id vertraagd.
* Voor huidige gegevens over conversiemetriek, voltooide gegevens, en gegevensvoer, worden alle klappen een extra 5-7 minuten vertraagd.

Houd er rekening mee dat de latentieverhoging begint nadat u de Identity Service hebt geïmplementeerd, zelfs als u deze integratie niet volledig hebt geïmplementeerd.
