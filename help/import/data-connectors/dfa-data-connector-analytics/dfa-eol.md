---
title: DFA-integratie - informatie aan het einde van de levensduur
description: Waarom is Adobe het einde van de DFA Data Connector en welke alternatieven zijn er?
translation-type: tm+mt
source-git-commit: 6669f678c1327b6af4a5b67c8033a9b7d8c9dbcf
workflow-type: tm+mt
source-wordcount: '649'
ht-degree: 0%

---


# DFA-integratie - informatie aan het einde van de levensduur

Adobe heeft onlangs [zijn plannen aangekondigd om de gegevensconnector aan het einde van de levensduur te sluiten](https://experienceleague.adobe.com/docs/analytics/import/dataconnectors/data-connectors-eol.html), een oudere toolset voor het integreren van gegevens van derden (bijvoorbeeld ESP, VOC, enz.) met Adobe Analytics.

## Waarom gaan de Verbindingen van Gegevens naar eind-van-Leven?

Het ondersteunde platform voor partnerintegratie is [Adobe Exchange](https://exchange.adobe.com/experiencecloud), dat is ontworpen om de integratie van Adobe Digital Experience-toepassingen, CXM-integratie van derden te vergemakkelijken en de verschillende gegevensvereisten van zowel clients als partners in de toekomst te ondersteunen. Vele partners die hun integratie gebruikend de Verbindingen van Gegevens hadden gebouwd hebben reeds die integratie gemigreerd aan de Uitwisseling van Adobe, met meer partners die van plan zijn dit te doen.

## Waarom gaat de DFA-integratie in het einde van de levensduur?

In [Januari 2020 kondigde Google ](https://blog.chromium.org/2020/01/building-more-private-web-path-towards.html) aan dat het in Chrome in 2022 cookies van derden geleidelijk zou elimineren. Dit volgt de industriestandaarden die Apple en Mozilla hebben ingesteld voor respectievelijk hun Safari- en Firefox-browsers. De DFA-integratie is sterk afhankelijk van cookies van derden en zal daarom ineffectief en achterhaald worden door het verwijderen van cookies van derden in de drie grote internetbrowsers. Google [heeft dit standpunt in maart 2021](https://blog.google/products/ads-commerce/a-more-privacy-first-web) versterkt door aan te kondigen dat zij geen alternatieve oplossing zullen vrijgeven.

Helaas is het onwaarschijnlijk dat Google, dat eigenaar is van de DFA-integratie, deze zal repliceren op het Adobe Exchange-platform. Daarom gaan wij verder in de veronderstelling dat, zodra de Verbindingen van Gegevens off-line gaan, de bestaande integratie zal ophouden te functioneren en geen productieve vervanging zal hebben.

Een belangrijke en aanvullende factor is het &quot;view-through&quot;-vermogen van de DFA-integratie. Zo kan Adobe Analytics gevallen bijhouden waarin een gebruiker een advertentie heeft gezien, niet heeft geklikt, maar later de website heeft bezocht. &quot;Beeld-door&quot;zijn gebaseerd op derdekoekjes, die in de loop van 2021 geleidelijk zullen worden geëlimineerd. Dit is een markt-brede kwestie, niet alleen een Adobe-kwestie. Op dit moment bestaan er geen alternatieven voor het repliceren van deze gegevens.

## Welke alternatieven bestaan er voor u?

Voor klanten die geïnteresseerd zijn in het integreren van weergave- en gegevensweergave (zonder &quot;view-through&quot;) in Adobe Analytics, hebben we momenteel de volgende opties:

* Adobe Advertising Cloud DSP-klanten kunnen gebruikmaken van [een productieve integratie met Adobe Analytics](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/integrations/ad-cloud/introduction-to-the-analytics-for-advertising-cloud-dsp-integration.html?lang=en#integrations) om weergave- en advertentiegegevens van Google naar Adobe Analytics in te stellen. Deze integratie is ons beste alternatief en zou onze aanbeveling aan klanten zijn. Met de Ad Cloud-DSP kunnen klanten online ervaringen aanbieden op alle reclamekanalen, waaronder betaalde zoekopdrachten, weergave, video en andere. Meer [hier](https://experienceleague.adobe.com/docs/advertising-cloud/dsp/introduction/dsp-about.html?lang=en#introduction). De DSP van Ad Cloud zal echter ook worden beïnvloed door het verlies van cookies van derden.
* Adobe Experience Platform en [Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-landing.html?lang=en), die mogelijkheden rond vertoning en integratie met andere gegevensbronnen verstrekken. Klanten kunnen hun weergavegegevens downloaden van hun betaalde zoekfunctie en deze gegevens uploaden naar het Experience Platform. Vervolgens brengen ze de gegevens rechtstreeks naar CJA om ze naast hun andere gegevenssets te analyseren.
* Met Adobe Consulting (Engineering Architects) kunt u een aangepaste oplossing maken voor het opnemen van weergave- en meetgegevens in Adobe Analytics. Deze oplossing is nog in ontwikkeling en alle klanten die geïnteresseerd zijn in deelname aan de bètaversie zijn welkom. Naarmate deze beschikbaar komen, worden meer details over functies, beschikbaarheid en kosten verschaft.
* U kunt uw eigen weergave- en integratiefuncties beheren met de functies Gegevensbronnen en Classificaties in Adobe Analytics. Importeer uw betaalde zoek- en weergavegegevens handmatig met Gegevensbronnen en Classificaties [zoals hier wordt beschreven](https://experienceleague.adobe.com/docs/analytics/import/use-cases/paid-search-metrics.html?lang=en#use-cases). (Opmerking: in dit document wordt verwezen naar betaalde zoekopdrachten , maar het gebruiksscenario en het gebruiksconcept zijn hetzelfde en kunnen op de weergave worden toegepast ) .

Voor extra vragen of ondersteuning kunt u contact opnemen met [Adobe Customer Care](https://helpx.adobe.com/nl/contact/enterprise-support.ec.html).