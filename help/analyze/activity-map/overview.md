---
description: Koppelingsactiviteit beperken met behulp van visuele overlays om de betrokkenheid van het publiek van uw webpagina's te controleren.
title: Activity Map-overzicht
feature: Activity Map
role: User, Admin
exl-id: 30a800f7-e2c8-443e-b5d4-36834ef0ba20
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '605'
ht-degree: 0%

---

# Activity Map-overzicht

Adobe Analytics Activity Map is een functie in Adobe Analytics die een visuele weergave biedt van de betrokkenheid van gebruikers bij webpagina&#39;s en mobiele apps. Marketers en analisten kunnen hiermee gebruikersinteracties zoals klikken en schuiven bijhouden en analyseren. Activity Map genereert warmtekaarten en overlayrapporten die de populairste elementen op een webpagina weergeven, zodat u uw digitale ervaringen kunt optimaliseren.

Activity Map bestaat uit verschillende belangrijke onderdelen:

* **reeks die van het Rapport** plaatst: Een rapportreeks moet Activity Map hebben toegelaten alvorens u het kunt beginnen te gebruiken. Zie [&#x200B; Activity Map die &#x200B;](/help/admin/tools/manage-rs/edit-settings/activity-map.md) meldt in de reeksinstellingen van het Rapport.
* **Implementatie**: De meeste rapportering van Activity Map is beschikbaar uit-van-de-doos. Sommige websites kunnen echter aanvullende implementatie nodig hebben om optimaal gebruik te kunnen maken van het bijhouden van koppelingen. De volgende implementatievariabelen zijn beschikbaar:
   * [`ActivityMap.linkExclusions`](/help/implement/vars/config-vars/activitymap-linkexclusions.md): filter op gegevens klikken op naam van koppeling.
   * [`ActivityMap.regionExclusions`](/help/implement/vars/config-vars/activitymap-regionexclusions.md): filter op gegevens klikken op gebiedsnaam.
   * [`ActivityMap.regionIDAttribute`](/help/implement/vars/config-vars/activitymap-regionidattribute.md): wijzig het kenmerk dat de afmetingen van het Activity Map-gebied vult.
   * [`ActivityMap.link`](/help/implement/vars/functions/activitymap-link.md): pas de logica aan die Activity Map gebruikt om de Activity Map Link-dimensie te vullen.
   * [`ActivityMap.region`](/help/implement/vars/functions/activitymap-region.md): pas de logica aan die Activity Map gebruikt om de dimensie Activity Map Region te vullen.
* **Bedekking**: Een browser uitbreiding die u toestaat om klikgegevens te zien over uw website. Zie [&#x200B; de uitbreidingsinterface van Activity Map &#x200B;](overlay/overview.md) voor meer informatie.
* **Dimensies**: Naast de bekledingsuitbreiding, verstrekt Activity Map verscheidene dimensies die u in Analysis Workspace kunt gebruiken.
   * [&#x200B; Verbinding van Activity Map &#x200B;](/help/components/dimensions/activity-map-link.md): De verbindingsnaam die werd geklikt.
   * [&#x200B; Gebied van Activity Map &#x200B;](/help/components/dimensions/activity-map-region.md): De gebiedsnaam die werd geklikt.
   * [&#x200B; de Pagina van Activity Map &#x200B;](/help/components/dimensions/activity-map-page.md): De paginanaam in de tijd dat de verbinding werd geklikt.
   * [&#x200B; Verbinding van Activity Map door Gebied &#x200B;](/help/components/dimensions/activity-map-link-by-region.md): Een samengevoegde waarde van de Verbinding van Activity Map en het Gebied van Activity Map.

## Functies en voordelen

* **Visualisatie van gebruikersovereenkomst**: Activity Map biedt een dynamische visuele vertegenwoordiging van gebruikersgedrag aan, toelatend u om precies te zien waar de gebruikers klikken. Deze visuele gegevens maken het gemakkelijker om patronen, tendensen, en gebieden van belang te identificeren. Vervolgens kunt u geïnformeerde beslissingen nemen over ontwerp, plaatsing van inhoud en doorloop van gebruikers.

* **Kaarten van de Warmte**: Activity Map produceert hittekaarten die de het klikst of interactie aangaan gebieden van een webpagina tonen. Warmtekaarten gebruiken kleurcodering om het betrokkenheidsniveau aan te geven, zodat u hotspots kunt identificeren en de aandacht kunt vestigen op gebieden met veel effect. Deze informatie kan nuttig zijn voor het optimaliseren van call-to-action-knoppen, -koppelingen, -formulieren of andere interactieve elementen.

* **de rapporten van de Bedekking**: De rapporten van de bedekking in Activity Map verstrekken gedetailleerde klikmetriek voor specifieke elementen op een webpagina. Door de doorklikpercentages en de betrokkenheidsniveaus van afzonderlijke elementen te begrijpen, kunt u uw ontwerp- en inhoudsstrategieën verfijnen om de gebruikerservaring te verbeteren.

* **de analyse van het Segment**: U kunt gebruikersgedrag analyseren dat op verschillende segmenten, zoals verkeersbronnen, demografie, of persona&#39;s wordt gebaseerd. Door de gegevens te segmenteren, kunt u waardevolle inzichten in specifieke gebruikersgroepen ontdekken, toelatend gepersonaliseerde ervaringen en gerichte marketing strategieën.

## Praktische toepassingen

* **de optimalisering van de Website**: Activity Map helpt u uw websites optimaliseren door ondermaatse elementen te identificeren, navigatie te verbeteren, en de algemene gebruikerservaring te verbeteren. Door gebruikersinteracties te analyseren, kunt u gegevensgestuurde beslissingen nemen om gebruikersstromen te stroomlijnen, formulieren te vereenvoudigen of de plaatsing van inhoud aan te passen voor een maximale impact.

* **het tariefoptimalisering van de Omzetting**: Door gebruikersbetrokkenheid en het analyseren van klikthrough tarieven te visualiseren, speelt Activity Map een cruciale rol in inspanningen CRO. U kunt hindernissen voor conversie identificeren en experimenteren met verschillende ontwerpvariaties om conversietrechter, openingspagina&#39;s en uitcheckprocessen te optimaliseren.

* **het testen A/B**: Activity Map kan met het testen A/B worden gecombineerd om het effect van ontwerp of inhoudsveranderingen te meten. Door de maatstaven voor de betrokkenheid van verschillende versies van een webpagina te vergelijken, kunt u bepalen welke variaties leiden tot een hogere betrokkenheid van gebruikers, conversietarieven of omzet.

