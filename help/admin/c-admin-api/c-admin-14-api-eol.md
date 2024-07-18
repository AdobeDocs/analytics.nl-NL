---
description: Koppeling naar Adobe Analytics Admin API op github.
title: Adobe Analytics 1.4 API EOL - Veelgestelde vragen
feature: Admin Tools
role: Admin
source-git-commit: da96c049f7cfb73496416c2d8a7f4dcbc8f2303e
workflow-type: tm+mt
source-wordcount: '801'
ht-degree: 0%

---

# Adobe Analytics 1.4 API EOL - Veelgestelde vragen

## Bericht bij einde levensduur (EOL)

**wat wordt gepensioneerd?**

* Adobe Analytics 1.4-API&#39;s

* Adobe Analytics WSSE-verificatie

**wanneer wordt het gesloten?**

Deze diensten worden op 12 augustus 2026 met pensioen gegaan. Na deze datum zijn ze niet meer toegankelijk.

## 1.4 API&#39;s

**wat zijn deze diensten?**

[ Adobe Analytics 1.4 APIs ](https://developer.adobe.com/analytics-apis/docs/1.4/) is een inzameling van APIs die voor een brede waaier van acties, zoals het melden, classificaties, gegevensvoer, en de configuraties van de rapportreeks verstrekken.

**wat moet ik doen om te migreren?**

[ Adobe Analytics 2.0 APIs ](https://developer.adobe.com/analytics-apis/docs/2.0/) biedt een migratieweg voorwaarts voor 1.4 API gebruikers aan. Klanten die momenteel de 1.4-API&#39;s gebruiken, kunnen hun integratie migreren naar de 2.0-API&#39;s (dezelfde API&#39;s als waarop de Adobe Analytics-toepassing is gebaseerd) en profiteren van de nieuwste functies.

Met de API&#39;s van 2.0 kunt u bijna elke handeling uitvoeren die u in de gebruikersinterface Analytics kunt uitvoeren, zoals het rapporteren of beheren van componenten zoals segmenten en berekende metriek.

**bieden 2.0 APIs de zelfde eigenschappen aan zoals 1.4 APIs?**
Om het even welke mogelijkheden die in 1.4 APIs beschikbaar zijn kunnen worden verwezenlijkt gebruikend [ Adobe Analytics 2.0 APIs ](https://developer.adobe.com/analytics-apis/docs/2.0/). Sommige functionaliteit verstrekt de zelfde mogelijkheden zoals beschikbaar in 1.4 APIs, heeft het zelfde u toestaan om bijna om het even welke actie uit te voeren die u in het Analytische gebruikersinterface kunt uitvoeren, zoals het melden van of het beheren van componenten zoals segmenten en berekende metriek.

## WSSE-verificatie

**wat zijn deze diensten?**

De authentificatie WSSE is een erfenisauthentificatieprotocol dat door Analytics 1.4 APIs wordt gesteund. Het is vervangen door de op OAuth-Gebaseerde authentificatieopties die in [ Adobe Developer Console ](https://developer.adobe.com/console/home) worden verstrekt.

**wat moet ik doen om te migreren?**

De klanten WSSE moeten hun authentificatie bijwerken om geloofsbrieven te gebruiken die in Adobe Developer Console worden voorzien. Om dit te doen, login aan [ Adobe Developer Console ](https://developer.adobe.com/console/home) om een project voor uw Analytics 2.0 API integratie tot stand te brengen. Selecteer tussen de OAuth-gebruikersverificatiemethoden en de OAuth-serververificatiemethoden.

## Vragen

Q: **beïnvloedt dit mijn bestaande projecten van AdobeIO voor Analytics APIs?**

A: Eventuele bestaande projecten die gebruikmaken van de API&#39;s Analytics 1.4 worden beïnvloed. Die integratie moet aan [ Adobe Analytics 2.0 APIs ](https://developer.adobe.com/analytics-apis/docs/2.0/) vóór de EOL deadline worden gemigreerd.

Q: **ik heb mijn geloofsbrieven van de Adobe met een ander product of een toepassing gedeeld die Analytics APIs gebruikt. Hebben ze gevolgen?**

A: Als dat product of die toepassing uw referentie WSSE en/of Analytics 1.4 APIs gebruikt, wordt het beïnvloed en zal moeten migreren vóór de EOL termijn. Neem contact op met de leverancier van het product of de toepassing voor meer informatie over de migratieplannen en het tijdschema.

Q: **ik ben niet zeker wat Adobe Analytics API wij gebruiken.**

A: U kunt identificeren welke API u gebruikt door het adres dat in uw integratie wordt geroepen.

De API&#39;s van Adobe Analytics 1.4 worden benaderd door een van de onderstaande URL&#39;s aan te roepen:
* https://api.omniture.com
* https://api3.omniture.com
* https://api4.omniture.com
* https://api5.omniture.com

[ Adobe Analytics 2.0 APIs ](https://developer.adobe.com/analytics-apis/docs/2.0/) wordt betreden door volgende URL te roepen:
* https://analytics.adobe.io

Als u api*.omniture.com gebruikt, moet u aan [ Adobe Analytics 2.0 APIs migreren ](https://developer.adobe.com/analytics-apis/docs/2.0/).

Q: **zijn Adobe Analytics 2.0 APIs identiek aan 1.4 APIs? Zo niet, wat zijn de grootste verschillen?**

A: De API&#39;s van Adobe Analytics 2.0 zijn niet identiek aan de API&#39;s van 1.4, maar ze bieden wel vergelijkbare functies, waaronder de volgende voordelen:

* Snellere reactietijden met eenvoudigere en efficiëntere vraagmethodes, die de behoefte aan opiniepeiling elimineren

* Programmatische capaciteit voor vragen en dynamische rapportupdates

* Gegrafeerde foutafhandeling

* Flexibel functioneren om alles te bereiken wat u van Analysis Workspace kunt bereiken

* Consistentie en overeenstemming van API-aanroepen met UI-acties

* Toegang tot alle in Analysis Workspace gebruikte Attribution IQ modellen

* Toegang tot alle in Analysis Workspace gebruikte algoritmen voor anomaly-detectie

* Het vermogen om met andere producten van de Experience Cloud te integreren

* Verhoogde capaciteit voor meerdere uitsplitsingsrapporten

* Toegang tot de nieuwste analysefuncties

De [ migrerend aan Adobe Analytics 2.0 APIs ](https://developer.adobe.com/analytics-apis/docs/2.0/guides/migration/) gids bespreekt de belangrijkste verschillen tussen 1.4 en 2.0 APIs. De extra informatie is ook beschikbaar in [ Analytics 2.0 API FAQ ](https://developer.adobe.com/analytics-apis/docs/2.0/guides/faq/).

Q: **beïnvloedt deze gegevensinzameling?**

A: Adobe Analytics 1.4 EOL heeft geen invloed op uw coderingsoplossingen, zoals Tags (voorheen Adobe Launch), WebSDK of AppMeasurement.js. Als u echter de 1.4-API&#39;s voor gegevensbronnen of classificaties gebruikt om uw gegevens te verzamelen of te verbeteren, moet u deze workflows migreren naar de Adobe Analytics 2.0-API&#39;s. Gelieve te verwijzen naar de [ 2.0 API eindpuntgids ](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/) voor meer details.

Q: **wordt de Invoeging API van Gegevens beïnvloed?**

A: Nee, de API voor het invoegen van gegevens wordt niet beïnvloed door de Adobe Analytics 1.4 EOL.

Q: **wat doe ik als mijn vraag niet in dit FAQ werd beantwoord?**

A: Als je nog vragen hebt, kun je contact opnemen met een accountvertegenwoordiger van de Adobe.

