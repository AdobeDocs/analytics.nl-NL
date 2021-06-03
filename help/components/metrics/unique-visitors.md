---
title: Unieke bezoekers
description: Het aantal unieke bezoeker-id's.
exl-id: 56e7bad4-4802-49ac-a0f1-ae77441fc016
source-git-commit: f669af03a502d8a24cea3047b96ec7cba7c59e6f
workflow-type: tm+mt
source-wordcount: '556'
ht-degree: 0%

---

# Unieke bezoekers

De metrische waarde &#39;Unieke bezoekers&#39; geeft het aantal bezoekers-id&#39;s voor het dimensie-item aan. Het is één van de gemeenschappelijkste metriek die bij het bepalen van verkeer wordt gebruikt, aangezien het een overzicht op hoog niveau van de populariteit van een afmetingspunt geeft. Een bezoeker kan bijvoorbeeld elke dag een maand naar uw site komen, maar hij telt nog steeds als één unieke bezoeker.

Als u [Apparaatanalyse](../cda/overview.md) gebruikt, wordt deze metrische waarde vervangen door [Unieke apparaten](unique-devices.md) metrisch.

## Dagelijkse, wekelijkse, maandelijkse, driemaandelijkse en jaarlijkse unieke bezoekers

Rapporten en analyses bieden opties voor unieke bezoekers per dag, week, maand, kwartaal en jaar. In plaats van één unieke bezoeker te tellen voor de volledige tijdsperiode, tellen de unieke bezoekers gebaseerd op geselecteerde metrisch. U wilt bijvoorbeeld naar dagelijkse unieke bezoekers voor uw site kijken. Als een bezoeker &#39;s ochtends en &#39;s avonds weer naar uw site komt, telt hij als één enkele unieke dagelijkse bezoeker. Als een bezoeker maandag en dinsdag weer naar uw site komt, telt hij als twee unieke bezoekers per dag.

Analysis Workspace behandelt unieke bezoekers op basis van de granulariteit van het rapport. Als u bijvoorbeeld de [Day](../dimensions/day.md)-dimensie gebruikt, ziet u dagelijks unieke bezoekers voor elk dimensie-item. Nochtans, voor het rapporttotaal, wordt het gededupliceerde unieke bezoekers voor de de datumwaaier van de vrije lijst van de vorm.

## Hoe deze metrische waarde wordt berekend

Deze metrische waarde telt het aantal unieke bezoeker-id&#39;s voor een bepaald dimensie-item. Het gebruikt veelvoudige geavanceerde mechanismen om unieke bezoekers te identificeren, aangezien er verscheidene manieren zijn om hen te identificeren. De volgende tabel bevat een overzicht van de manier waarop een bezoeker wordt geïdentificeerd, samen met zijn prioriteit. Sommige treffers kunnen veelvoudige methodes van de bezoekersidentificatie hebben; in deze gevallen wordt de methode met hogere prioriteit gebruikt .

| Volgorde gebruikt | Query-parameter (verzamelingsmethode) | presenteren als |
| --- | --- | --- |
| 1 | `vid` | De variabele [`visitorID`](/help/implement/vars/config-vars/visitorid.md) wordt ingesteld. |
| 2 | `aid` | Bezoeker heeft een bestaand [`s_vi`](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-analytics.html) cookie. Plaats op implementaties zonder of voorafgaand aan het uitvoeren van de dienst van identiteitskaart van de Bezoeker. |
| 1 | `mid` | Bezoeker heeft een bestaand [`s_ecid`](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-analytics.html) cookie. Stel deze optie in bij implementaties met de [Adobe Experience Cloud Identity-service](https://experienceleague.adobe.com/docs/id-service/using/home.html). |
| 4 | `fid` | Bezoeker heeft een bestaande [`s_fid`](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-analytics.html) cookie, of als `aid` en `mid` om welke reden dan ook niet kunnen worden ingesteld. |
| 5 | IP Adres, de Agent van de Gebruiker, IP van de Gateway Adres | Laatste middel om een unieke bezoeker te identificeren als de browser van de bezoeker geen cookies accepteert. |

>[!NOTE]
>
>Elke Analyse-bezoeker die aan een profiel op Adobe-id is gekoppeld, is gekoppeld. Deze bezoekersprofielen worden na ten minste 13 maanden inactiviteit verwijderd, ongeacht de vervaldatum van de cookie van de bezoeker.

## Gedrag dat van invloed is op het aantal unieke bezoekers

Unieke bezoekersidentificatoren worden doorgaans opgeslagen in een browsercookie. Een nieuwe unieke bezoeker wordt geteld als deze een van de volgende handelingen uitvoert:

* Wist de cache op elk gewenst moment
* Opent een andere browser op dezelfde computer. Eén unieke bezoeker wordt per browser geteld.
* Dezelfde persoon die op verschillende apparaten door uw site bladert. Een afzonderlijke unieke bezoeker wordt geteld per apparaat. U kunt [Apparaatanalyse](../cda/overview.md) gebruiken om bezoekers te combineren gebruikend [Mensen](people.md) metrisch.
* Hiermee opent u een Private Browsing-sessie (zoals het tabblad Incognito van Chrome).

Een nieuwe unieke bezoeker wordt *niet* geteld, zolang de cookie-id behouden blijft:

* Sluit hun browser voor een langere periode
* Hiermee wordt de browser bijgewerkt naar de nieuwste versie
