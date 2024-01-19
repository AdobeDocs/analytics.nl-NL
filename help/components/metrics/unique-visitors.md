---
title: Unieke bezoekers
description: Het aantal unieke bezoeker-id's.
feature: Metrics
exl-id: 56e7bad4-4802-49ac-a0f1-ae77441fc016
source-git-commit: 93099d36a65ca2bf16fbd6342f01bfecdc8c798e
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 1%

---

# Unieke bezoekers

De &#39;Unieke bezoekers&#39; [metrisch](overview.md) toont het aantal bezoeker-id&#39;s voor het dimensie-item. Het is één van de gemeenschappelijkste metriek die bij het bepalen van verkeer wordt gebruikt, aangezien het een overzicht op hoog niveau van de populariteit van een afmetingspunt geeft. Een bezoeker kan bijvoorbeeld elke dag een maand naar uw site komen, maar hij telt nog steeds als één unieke bezoeker.

Als u [Apparaatanalyse](../cda/overview.md), wordt deze norm vervangen door de [Unieke apparaten](unique-devices.md) metrisch.

## Dagelijkse, wekelijkse, maandelijkse, driemaandelijkse en jaarlijkse unieke bezoekers

Analysis Workspace behandelt unieke bezoekers op basis van de granulariteit van het rapport. Als u bijvoorbeeld de opdracht [Dag](../dimensions/day.md) dimensie, zult u dagelijkse unieke bezoekers voor elk afmetingspunt zien. Nochtans, voor het rapporttotaal, wordt het gededupliceerde unieke bezoekers voor de de datumwaaier van de vrije lijst van de vorm.

## Hoe deze metrische waarde wordt berekend

Deze metrische waarde telt het aantal unieke bezoeker-id&#39;s voor een bepaald dimensie-item. Het gebruikt veelvoudige geavanceerde mechanismen om unieke bezoekers te identificeren, aangezien er verscheidene manieren zijn om hen te identificeren. De volgende tabel bevat een overzicht van de manier waarop een bezoeker wordt geïdentificeerd, samen met zijn prioriteit. Sommige treffers kunnen veelvoudige methodes van de bezoekersidentificatie hebben; in deze gevallen wordt de hogere prioritaire methode gebruikt.

| Volgorde gebruikt | Query-parameter (verzamelingsmethode) | presenteren als |
| --- | --- | --- |
| 1 | `vid` | De [`visitorID`](/help/implement/vars/config-vars/visitorid.md) variable is set. |
| 2 | `aid` | Bezoeker heeft een bestaande [`s_vi`](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-analytics.html) cookie. Plaats op implementaties zonder of voorafgaand aan het uitvoeren van de dienst van identiteitskaart van de Bezoeker. |
| 3 | `mid` | Bezoeker heeft een bestaande [`s_ecid`](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-analytics.html) cookie. Instellen bij implementaties met de opdracht [Adobe Experience Cloud Identity-service](https://experienceleague.adobe.com/docs/id-service/using/home.html). |
| 4 | `fid` | Bezoeker heeft een bestaande [`s_fid`](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-analytics.html) cookie, of als `aid` en `mid` kan om geen enkele reden worden ingesteld. |
| 5 | IP Adres, de Agent van de Gebruiker, IP van de Gateway Adres | Laatste middel om een unieke bezoeker te identificeren als de browser van de bezoeker geen cookies accepteert. |

>[!NOTE]
>
>Elke bezoeker-id van Analytics is gekoppeld aan een profiel op de servers van de Adobe. Deze bezoekersprofielen worden na ten minste 13 maanden inactiviteit verwijderd, ongeacht de vervaldatum van de cookie van de bezoeker.

## Gedrag dat van invloed is op het aantal unieke bezoekers

Unieke bezoekersidentificatoren worden doorgaans opgeslagen in een browsercookie. Een nieuwe unieke bezoeker wordt geteld als deze een van de volgende handelingen uitvoert:

* Wist de cache op elk gewenst moment
* Opent een andere browser op dezelfde computer. Eén unieke bezoeker wordt per browser geteld.
* Dezelfde persoon die op verschillende apparaten door uw site bladert. Een afzonderlijke unieke bezoeker wordt geteld per apparaat. U kunt [Apparaatanalyse](../cda/overview.md) om bezoekers te combineren met [Mensen](people.md) metrisch.
* Hiermee opent u een Private Browsing-sessie (zoals het tabblad Incognito van Chrome).

Een nieuwe unieke bezoeker is *niet* geteld, zolang de cookie-id behouden blijft:

* Sluit hun browser voor een langere periode
* Hiermee wordt de browser bijgewerkt naar de nieuwste versie
