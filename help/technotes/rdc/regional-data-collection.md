---
title: Regionale dataverzameling
description: Informatie over regionale gegevensverzameling
exl-id: 295e9736-2a58-48a8-9968-5dfa33b70d95
source-git-commit: 1cf95a2bf57aacd6b0b5bdb1c3bf31d1b31339e0
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 1%

---

# Regionale dataverzameling

De Adobe Experience Cloud maakt gebruik van regionale gegevensverzameling (Regional Data Collection, RDC), zodat interactie tussen uw eindgebruikers en de Adobe Experience-cloud zo dicht mogelijk bij uw eindgebruikers plaatsvindt. Dit verbetert de prestaties van uw site/app en zorgt ervoor dat gegevens zo snel mogelijk worden verzameld om de gebruikerservaring te optimaliseren. Zodra de gegevens van uw digitale eigenschappen regionaal bij een Centrum van de Gegevensverzameling (DCC) worden verzameld, door:sturen het over een veilige verbinding aan een Centrum van de Gegevensverwerking (DPC) waar het wordt verwerkt en ter beschikking gesteld aan producten in Adobe Experience Cloud.

>[!IMPORTANT]
>
>Het China RDC (China Performance Optimization) Add-on Package is een aanrekbare add-on voor Adobe Analytics. De Optimalisering van Prestaties van Adobe in het vasteland van China laat klanten met gebruikers binnen China toe om die gegevens te hebben die rechtstreeks naar het de randknoop van China, in plaats van andere plaatsen globaal worden verzonden. Hierdoor worden de laadtijden van de pagina en de gegevensnauwkeurigheid verbeterd ten opzichte van het verzenden van de gegevens naar knooppunten buiten China. Neem voor meer informatie contact op met je Adobe-verkoper.

De regionale distributiesector omvat momenteel de volgende locaties (afhankelijk van de verandering):

## Gegevensverzameling van derden

| RDC-type | Centra voor gegevensverzameling |
|---------------------|-------------------|
| Standaard | Oregon, Virginia, Ireland, Paris, Mumbai, Singapore, Tokyo, Sydney, China* |

*China RDC vereist het China Add-on pakket. Zie de opmerking &#39;Belangrijk&#39; hierboven.

>[!NOTE]
>
>Als uw verzoek voor een analyseafbeelding naar de `adobedc`, `2o7.net` of `omtrdc.net` eindpunten, dan hebt u derdegegevensinzameling. U kunt dit bepalen als u één van beide eindpunt in URL van uw verzoeken ziet.

## Gegevensverzameling van eerste partijen

| RDC-type | Centra voor gegevensverzameling |
|---------------------|-------------------|
| Algemeen (standaard) | Oregon, Virginia, Ireland, Paris, Mumbai, Singapore, Tokyo, Sydney |
| Wereldwijd + China* | China*, Oregon, Virginia, Ireland, Paris, Mumbai, Singapore, Tokyo, Sydney |
| Alleen Amerika | Oregon, Virginia |
| Alleen Europa | Ierland, Parijs |
| Alleen Azië - Stille Oceaan | Mumbai, Singapore, Tokio, Sydney |
| Alleen China* | Peking |

*Alleen China en de RDC-typen wereldwijd + China vereisen het China Add-on-pakket. Zie de opmerking &#39;Belangrijk&#39; hierboven. Global + China zal gegevens die afkomstig zijn uit China naar onze China RDC leiden en gegevens van buiten China naar de dichtstbijzijnde RDC buiten China doorsturen.

>[!NOTE]
>
>Experience Edge Global biedt de beste prestaties voor uw eindgebruikers.  Als u een ander type van BDC wilt gebruiken, gelieve de Zorg van de Adobe van de Klant voor hulp te contacteren.

## Voordelen van de RDC

| Voordeel | Beschrijving |
| --- | --- |
| Prestaties | Met RDC maken uw bezoekers verbinding met de dichtstbijzijnde DCC. Dit zorgt voor de snelste responstijd, wat resulteert in nauwkeurigere tracking en snellere laadtijden. |
| Redundantie | In het geval van een verstoring in communicatie tussen DCC en uw DPC, bewaart de infrastructuur van RDC van Adobe gegevens plaatselijk, dan door:sturen het aan DPC wanneer de mededelingen worden hersteld. |

## Hoe werkt RDC?

In de volgende lijst wordt het gegevensverzamelingsproces beschreven dat door Adobe wordt gebruikt:

1. DNS lost automatisch de inzameling hostname aan het IP adres van het Centrum van de Inzameling van Gegevens dichtst bij de bezoeker op.
1. De bezoeker verzendt de gegevens naar die locatie.
1. De gegevens worden onmiddellijk via een beveiligde verbinding doorgestuurd naar het Centrum voor gegevensverwerking, waar ze worden verwerkt en ter beschikking worden gesteld van de producten in de Adobe Experience Cloud.
