---
description: Details voor de Adobe Analytics 1.4 API-aankondiging aan het einde van de levensduur.
title: Adobe Analytics 1.4 API EOL - Veelgestelde vragen
feature: Admin Tools
role: Admin
exl-id: 88769032-a7cd-4ca8-958f-3300a4bfe71f
source-git-commit: 73c0210ac931f3e7f823e033a3bffdc22e159ddb
workflow-type: tm+mt
source-wordcount: '534'
ht-degree: 0%

---

# Adobe Analytics 1.4 API EOL - Veelgestelde vragen

Adobe is van plan om Adobe Analytics 1.4 API op **12 augustus, 2026** terug te trekken. Na deze datum zijn ze niet meer toegankelijk. Deze aankondiging heeft rechtstreeks invloed op het volgende:

* Adobe Analytics 1.4-API&#39;s, met uitzondering van de API voor het invoegen van gegevens
* Adobe Analytics WSSE-verificatie

## 1.4 API&#39;s

[ Adobe Analytics 1.4 APIs ](https://developer.adobe.com/analytics-apis/docs/1.4/) verstrekt een brede waaier van acties, zoals het melden, classificaties, gegevensvoer, en de configuraties van de rapportreeks. Zij worden zonsondergang ten gunste van [ Adobe Analytics 2.0 APIs ](https://developer.adobe.com/analytics-apis/docs/2.0/). Met de API&#39;s van 2.0 kunt u bijna elke handeling uitvoeren die u in de gebruikersinterface Analytics kunt uitvoeren, zoals het rapporteren of beheren van componenten zoals segmenten en berekende metriek.

Adobe biedt de weg van de a [ migratie ](https://developer.adobe.com/analytics-apis/docs/2.0/guides/migration/) voor 1.4 API gebruikers aan. U kunt uw integratie migreren naar de 2.0 API&#39;s (dezelfde API&#39;s als die waarvan de Adobe Analytics-toepassing afhankelijk is) en de nieuwste functies benutten. Om het even welke mogelijkheden die in 1.4 APIs beschikbaar zijn kunnen worden verwezenlijkt gebruikend [ Adobe Analytics 2.0 APIs ](https://developer.adobe.com/analytics-apis/docs/2.0/).

## WSSE-verificatie

De authentificatie WSSE is een erfenisauthentificatieprotocol dat door Analytics 1.4 APIs wordt gesteund. Het is vervangen door de op OAuth-Gebaseerde authentificatieopties die in [ Adobe Developer Console ](https://developer.adobe.com/console/home) worden verstrekt. De projecten die authentificatie gebruiken WSSE moeten hun geloofsbrieven aan die in Adobe Developer Console provisioned bijwerken. Om dit te doen, login aan [ Adobe Developer Console ](https://developer.adobe.com/console/home) om een project voor uw Analytics 2.0 API integratie tot stand te brengen. Selecteer de verificatiemethode OAuth-gebruiker of OAuth Server-to-Server.

## Veelgestelde vragen

+++**beïnvloedt dit mijn bestaande projecten van Adobe IO voor Analytics APIs?**

Eventuele bestaande projecten die gebruikmaken van de API&#39;s voor Analytics 1.4 worden beïnvloed. Die integratie moet aan [ Adobe Analytics 2.0 APIs ](https://developer.adobe.com/analytics-apis/docs/2.0/) vóór de EOL deadline worden gemigreerd.

+++

+++**ik heb mijn geloofsbrieven van Adobe met een ander product of een toepassing gedeeld die Analytics APIs gebruikt. Hebben ze gevolgen?**

Als dat product of die toepassing uw referentie WSSE gebruikt en/of Analytics 1.4 APIs roept, wordt het beïnvloed en moet vóór de EOL termijn migreren. Neem contact op met de leverancier van het product of de toepassing voor meer informatie over de migratieplannen en de tijdlijn.

+++

+++**hoe kan ik bepalen welke API die mijn project gebruikt?**

De basis-URL die door de API-aanroepen wordt aangeroepen, bepaalt welke API-versie uw project gebruikt. De API&#39;s van Adobe Analytics 1.4 gebruiken de volgende URL&#39;s:
* `https://api.omniture.com`
* `https://api3.omniture.com`
* `https://api4.omniture.com`
* `https://api5.omniture.com`

[ Adobe Analytics 2.0 APIs ](https://developer.adobe.com/analytics-apis/docs/2.0/) gebruikt volgende URL:

* `https://analytics.adobe.io`

Als een van uw API-projecten `api*.omniture.com` gebruikt, worden de API&#39;s van Adobe Analytics 1.4 gebruikt en moet deze migreren naar de API&#39;s van 2.0.

+++

+++**doet deze eind-van-leven het gegevensinzameling?**

De Adobe Analytics 1.4 EOL heeft geen invloed op uw coderingsoplossingen, zoals Tags (voorheen Adobe Launch), Web SDK of AppMeasurement. Als u echter de 1.4-API&#39;s voor gegevensbronnen of classificaties gebruikt om uw gegevens te verbeteren, moet u deze workflows migreren naar de Adobe Analytics 2.0-API&#39;s.

De API voor het invoegen van gegevens wordt niet beïnvloed door deze aankondiging aan het einde van de levensduur. Terwijl Adobe van plan is om steun voor de Invoeging van Gegevens API voort te zetten, adviseert Adobe in plaats daarvan het gebruiken van [ Bulk API van de Invoeging van Gegevens ](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/bulk-data-insertion/).

+++

Neem contact op met uw Adobe-accountteam als u nog vragen hebt over deze aankondiging aan het einde van de levensduur die niet op deze pagina wordt beantwoord.
