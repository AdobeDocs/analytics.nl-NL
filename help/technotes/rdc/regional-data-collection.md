---
title: Regionale dataverzameling
description: Informatie over regionale gegevensverzameling
translation-type: tm+mt
source-git-commit: 4910c19f4471e8c79516747c7e69f1cdfda54d72
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 2%

---


# Regionale dataverzameling

De Adobe Experience Cloud maakt gebruik van regionale gegevensverzameling (Regional Data Collection, RDC), zodat interactie tussen uw eindgebruikers en de Adobe Experience-cloud zo dicht mogelijk bij uw eindgebruikers plaatsvindt. Dit verbetert de prestaties van uw site/app en zorgt ervoor dat gegevens zo snel mogelijk worden verzameld om de gebruikerservaring te optimaliseren. Zodra de gegevens van uw digitale eigenschappen regionaal bij een Centrum van de Gegevensverzameling (DCC) worden verzameld, door:sturen het over een veilige verbinding aan een Centrum van de Gegevensverwerking (DPC) waar het wordt verwerkt en ter beschikking gesteld aan producten in Adobe Experience Cloud.

>[!IMPORTANT]
>
>Het China RDC (China Performance Optimization) Add-on Package is een aanrekbare add-on voor Adobe Analytics. Adobe&#39; Performance Optimization in mainland China stelt klanten in China in staat om gegevens rechtstreeks naar China edge node te verzenden in plaats van naar andere locaties wereldwijd. Hierdoor worden de laadtijden van de pagina en de gegevensnauwkeurigheid verbeterd ten opzichte van het verzenden van de gegevens naar knooppunten buiten China. Neem voor meer informatie contact op met je Adobe-verkoper.

De regionale distributiesector omvat momenteel de volgende locaties (afhankelijk van de verandering):

## Gegevensverzameling van derden en HTTP

| RDC-type | Centra voor gegevensverzameling |
|---------------------|-------------------|
| Standaard | Oregon, Virginia, Ireland, Paris, Mumbai, Singapore, Tokyo, Sydney |

Opmerking: Als uw verzoek van het beeld van de Analyse naar `adobedc`, `2o7.net` `omtrdc.net` of eindpunten wordt verzonden, dan hebt u derdegegevensinzameling. U kunt dit bepalen als u één van beide eindpunt in URL van uw verzoeken ziet.

## First-party HTTPS gegevensinzameling

| RDC-type | Centra voor gegevensverzameling |
|---------------------|-------------------|
| Algemeen (standaard) | Oregon, Virginia, Ireland, Paris, Mumbai, Singapore, Tokyo, Sydney |
| Alleen Amerika | Oregon, Virginia |
| Alleen Europa | Ierland, Parijs |
| Alleen Azië - Stille Oceaan | Mumbai, Singapore, Tokio, Sydney |

Opmerking: Experience Edge Global biedt de beste prestaties voor uw eindgebruikers.  Als u een alternatief type van BDC wilt gebruiken, gelieve de Aangepaste Zorg van de Adobe voor hulp te contacteren.

## Hoe werkt RDC?

In de volgende lijst wordt het gegevensverzamelingsproces beschreven dat door Adobe wordt gebruikt:

1. DNS lost automatisch de inzameling hostname aan het IP adres van het Centrum van de Inzameling van Gegevens dichtst bij de bezoeker op.
1. De bezoeker verzendt de gegevens naar die locatie.
1. De gegevens worden onmiddellijk via een beveiligde verbinding doorgestuurd naar het Centrum voor gegevensverwerking, waar ze worden verwerkt en ter beschikking worden gesteld van de producten in de Adobe Experience Cloud.

## Voordelen van de RDC

| Voordeel | Beschrijving |
|---------|-----------|
| Prestaties | Met de RDC zullen uw bezoekers verbinding maken met de dichtstbijzijnde DCC. Dit betekent dat de responstijden op de pagina zullen afnemen (lager is beter), wat resulteert in nauwkeuriger tracking en snellere laadtijden. |
| Redundantie | In het geval van een verstoring in communicatie met een DCC, wordt de gegevensinzameling automatisch verpletterd aan volgende dichtstbijzijnde DCC die de dienstcontinuïteit verzekeren. |
| Redundantie | In het geval van een verstoring in communicatie tussen DCC en uw DPC, bewaart de infrastructuur van Adobe RDC plaatselijk gegevens, dan door:sturen het aan DPC wanneer de mededelingen worden hersteld. |

## Revisiegeschiedenis van documentatie

| Bijwerken | Beschrijving |
|--------|---------|
| 4 februari 2020 | RDC-locaties bijwerken |
| 20 februari 2019 | Volledig herschrijven. Toegevoegde RDC-netwerkinformatie. |
