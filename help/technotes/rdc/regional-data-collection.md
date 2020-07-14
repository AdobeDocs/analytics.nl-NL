---
title: Regionale dataverzameling
description: Informatie over regionale gegevensverzameling
translation-type: tm+mt
source-git-commit: 91867f379c9f3e0f4e7fdeed572a94ff798653ba
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 2%

---


# Regionale dataverzameling

De Adobe Experience Cloud maakt gebruik van Regional Data Collection (RDC), zodat interactie tussen uw eindgebruikers en de Adobe Experience Cloud zo dicht mogelijk bij uw eindgebruikers plaatsvindt. Dit verbetert de prestaties van uw site/app en zorgt ervoor dat gegevens zo snel mogelijk worden verzameld om de gebruikerservaring te optimaliseren. Zodra de gegevens van uw digitale eigenschappen regionaal bij een Centrum van de Inzameling van Gegevens (DCC) worden verzameld, door:sturen over een veilige verbinding aan een Centrum van de Gegevensverwerking (DPC) waar het wordt verwerkt en ter beschikking gesteld aan producten in de Wolk van de Ervaring van Adobe.

>[!IMPORTANT]
>
>Het China RDC (China Performance Optimization) Add-on Package is een oplaadbare invoegtoepassing voor Adobe Analytics. Neem voor meer informatie contact op met uw Adobe-vertegenwoordiger.

De regionale distributiesector omvat momenteel de volgende locaties (afhankelijk van de verandering):

## Gegevensverzameling van derden en HTTP

| Type RDC | Centra voor gegevensverzameling |
|---------------------|-------------------|
| Standaard | Oregon, Virginia, Ireland, Paris, Mumbai, Singapore, Tokyo, Sydney |

Opmerking: Als uw Analytics-verzoek voor een afbeelding naar de `2o7.net` `omtdrc.net` eindpunten of eindpunten wordt verzonden, worden gegevens van derden verzameld. U kunt dit bepalen als u één van beide eindpunt in URL van uw verzoeken ziet.

## First-party HTTPS gegevensinzameling

| Type RDC | Centra voor gegevensverzameling |
|---------------------|-------------------|
| Algemeen (standaard) | Oregon, Virginia, Ireland, Paris, Mumbai, Singapore, Tokyo, Sydney |
| Alleen Amerika | Oregon, Virginia |
| Alleen Europa | Ierland, Parijs |
| Alleen Azië - Stille Oceaan | Mumbai, Singapore, Tokio, Sydney |

Opmerking: Experience Edge Global biedt de beste prestaties voor uw eindgebruikers.  Als u een ander type RDC wilt gebruiken, neemt u contact op met de klantenservice van Adobe voor hulp.

## Hoe werkt RDC?

In de volgende lijst wordt het gegevensverzamelingsproces beschreven dat door Adobe wordt gebruikt:

1. DNS lost automatisch de inzameling hostname aan het IP adres van het Centrum van de Inzameling van Gegevens dichtst bij de bezoeker op.
1. De bezoeker verzendt de gegevens naar die locatie.
1. De gegevens worden direct via een beveiligde verbinding doorgestuurd naar het Data Processing Center, waar ze worden verwerkt en beschikbaar worden gesteld voor de producten in de Adobe Experience Cloud.

## Voordelen van de RDC

| Voordeel | Beschrijving |
|---------|-----------|
| Prestaties | Met de RDC zullen uw bezoekers verbinding maken met de dichtstbijzijnde DCC. Dit betekent dat de responstijden op de pagina zullen afnemen (lager is beter), wat resulteert in nauwkeuriger tracking en snellere laadtijden. |
| Redundantie | In het geval van een verstoring in communicatie met een DCC, wordt de gegevensinzameling automatisch verpletterd aan volgende dichtstbijzijnde DCC die de dienstcontinuïteit verzekeren. |
| Redundantie | Als de communicatie tussen de DCC en uw DPC wordt onderbroken, slaat de RDC-infrastructuur van Adobe lokale gegevens op en stuurt deze door naar de DPC wanneer de communicatie wordt hersteld. |

## Revisiegeschiedenis van documentatie

| Bijwerken | Beschrijving |
|--------|---------|
| 4 februari 2020 | RDC-locaties bijwerken |
| 20 februari 2019 | Volledig herschrijven. Toegevoegde RDC-netwerkinformatie. |
