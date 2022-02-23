---
title: Handtekeningen van gewone bot
description: Herken de gemeenschappelijke herkenningstekens van bots.
feature: Bot Removal
exl-id: 57622af6-c1d3-4ef1-b3e6-10c14f04a55c
source-git-commit: f6199620033af9c8e304bd0f537d4e0b052ed64d
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 0%

---

# Handtekeningen van gewone bot

Hoewel het identificeren van bots in een gegevensset afhankelijk is van de omgeving, zijn er enkele algemene manieren om bots te identificeren.

## Het grote aantal paginaweergaven per bezoek

U kunt een rapport van de Data Warehouse met IP adres, paginameningen, en unieke bezoekers trekken. Maak vervolgens een berekening &#x200B; &#x200B; in Excel voor paginaweergaven per bezoek en sorteer deze van hoogste naar laagste. Bots hebben vaak een zeer groot aantal paginaweergaven per bezoek (honderden tot duizenden). U zult een scherpe daling zien aangezien u zich in echt verkeer beweegt.

## Geen referentie

Bots hebben doorgaans geen verwijzende URL. In segmentatie kan dit worden gefilterd als `Referring Domain equals Typed/Bookmarked`.

## Vreemde gebruikersagents

Bots gebruiken vaak aangepaste gebruikersagents die niet zijn geclassificeerd in de browserdimensie of die worden weergegeven als een `unknown` versie van een standaardbrowser. Onbekende Safari en onbekende Opera hebben een zeer grote kans om bots te zijn.

## Linux- of &quot;Niet-opgegeven&quot; besturingssystemen

We willen het grote open-source Linux-besturingssysteem niet in diskrediet brengen, maar blijkbaar willen ze het als hun besturingssysteem instellen. Wees echter voorzichtig met het uitsluiten van legitieme verkeer van Linux-gebruikers. Bots willen ook geen besturingssysteem instellen, dat kan worden gesegmenteerd als `Operating System &#x200B;equals Not Specified`.

## Paginaweergaven = Bezoekopdrachten = Unieke Bezoekers

Dit is met name op het rapport van de gebruikersagent van toepassing. Zoals u in de onderstaande schermafbeelding kunt zien, heeft de &quot;onbekende versie&quot; van deze browsers bijna hetzelfde aantal bezoekers als unieke bezoekers (en bijna hetzelfde aantal paginaweergaven). Dit kan in segmentatie worden geïsoleerd door een [!UICONTROL Include] container voor `Single Page Visits equals Enabled` of `Hit Depth is less than 2`.

![](assets/bots-browsers-unknown.png)

## Bezoek nummer 1

De bots krijgen gewoonlijk een nieuwe bezoekersidentiteitskaart telkens als zij uitvoeren, waarbij zij slechts één bezoek ooit maken en al hun verkeer zal uit een bezoekaantal van 1 bestaan.

## Lagere monitorresoluties

Moderne gebruikers beschikken over monitoren met veel hogere resolutie dan in het verleden. Hits met de volgende resoluties lijkt erg populair voor bots:

* 1024 x 768 &#x200B; &#x200B;
* 1366 x 768
* 1600 x 864
* 800 x 600
* 1600 x 1200
* Niet opgegeven
* 1024 x 667

## Land en tijdzone komen niet overeen

Er is een verschil tussen het land van oorsprong en de tijdzone. De locatie kan bijvoorbeeld de Verenigde Staten zijn, maar de tijdzone kan mij GMT zijn.

![](assets/bots-country-time-zone.png)

## Niet aangemeld

De gebruiker meldt zich op geen enkel punt in hun bezoek aan, en hun gebruikers identificeert eVars niet voortduurt van vorige bezoeken. Hoewel sommige bots kunnen worden ingesteld om te verifiëren, zijn de meesten niet zo slim.

## Geen KPI&#39;s tijdens bezoek

Bots voegen meestal geen producten toe aan een winkelwagentje of checken uit. Meestal verzenden ze geen hoofdformulieren of andere succesgebeurtenissen, maar sommige bots verzenden wel eenvoudige HTML-formulieren. &#x200B;

## Specifieke queryreeks aanwezig

Soms proberen de bots om geheime voorgeheugens te buigen of anders plaatsen te breken door misvormde URLs of URLs te raken die niet bestaan (zoals typische LAMP of WordPress admin pagina&#39;s) of door specifieke vraagkoorden toe te voegen.

## IP-adressen die afkomstig zijn van gedistribueerde computerplatforms

Webhostingservices zoals Amazon Web Services of Google Cloud kunnen als beide boerderijen worden misbruikt. Deze IP adressen zijn bij een hoog risico om bots te zijn: &#x200B;
* [Google Cloud](https://cloud.google.com/compute/): IP-adres begint met `&#x200B;35.199` of `35.194&#x200B;`
