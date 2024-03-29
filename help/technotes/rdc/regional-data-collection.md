---
title: Regionale dataverzameling
description: Informatie over regionale gegevensverzameling
feature: Regional Data Collection
exl-id: 295e9736-2a58-48a8-9968-5dfa33b70d95
source-git-commit: a4dd138f0f2198da66caa272dd62b46f24b578b2
workflow-type: tm+mt
source-wordcount: '482'
ht-degree: 1%

---

# Regionale dataverzameling

De Adobe Experience Cloud maakt gebruik van regionale gegevensverzameling (Regional Data Collection, RDC), zodat interactie tussen uw bezoekers en Adobe zich zo dicht mogelijk bij uw bezoekers voordoet. Zodra de gegevens regionaal bij een Centrum van de Inzameling van Gegevens (DCC, ook gekend als plaats van de Rand) worden verzameld, door:sturen het over een veilige verbinding aan een Centrum van de Verwerking van Gegevens (DPC, die ook als plaats van de Kern wordt bekend). Na verwerking zijn de gegevens beschikbaar voor producten in de Adobe Experience Cloud. Neem contact op met de klantenservice van Adobe als u uw RDC-type wilt wijzigen.

Bij het regionale gegevensverzamelingsproces worden de volgende stappen uitgevoerd:

1. DNS lost automatisch de inzameling hostname aan het IP adres van het Centrum van de Inzameling van Gegevens dichtst bij de bezoeker op.
1. De bezoeker verzendt de gegevens naar die locatie.
1. De gegevens worden onmiddellijk via een beveiligde verbinding doorgestuurd naar het Centrum voor gegevensverwerking, waar ze worden verwerkt en ter beschikking worden gesteld van de producten in de Adobe Experience Cloud.

Het gebruik van regionale gegevensverzameling biedt verschillende voordelen:

* **Prestaties**: Met RDC maken uw bezoekers verbinding met de dichtstbijzijnde DCC. Deze optimalisatie biedt de snelste responstijd, wat resulteert in nauwkeurigere tracking en snellere laadtijden.
* **Redundantie**: Als er een verstoring in communicatie tussen DCC en uw DPC is, bewaart de infrastructuur van Adobe RDC plaatselijk gegevens, dan door:sturen het aan DPC wanneer de mededelingen worden hersteld.

De regionale distributiesector omvat momenteel de volgende locaties (afhankelijk van de verandering):

## Gegevensverzameling van derden

| RDC-type | Centra voor gegevensverzameling |
| --- | --- |
| Standaard | Oregon, Virginia, Ireland, Paris, Mumbai, Singapore, Tokyo, Sydney, China* |

{style="table-layout:auto"}

*China RDC vereist het China Add-on pakket. Zie [Optimalisatie van Chinese prestaties](#china-performance-optimization) hieronder.

>[!NOTE]
>
>Als uw verzoek voor een analyseafbeelding naar de `adobedc.net`, `2o7.net` of `omtrdc.net` eindpunten, dan hebt u derdegegevensinzameling. U kunt dit bepalen als u één van beide eindpunt in URL van uw verzoeken ziet.

## Gegevensverzameling van eerste partijen

| RDC-type | Centra voor gegevensverzameling |
| --- | --- |
| Algemeen (standaard) | Oregon, Virginia, Ireland, Paris, Mumbai, Singapore, Tokyo, Sydney |
| Wereldwijd + China* | China*, Oregon, Virginia, Ireland, Paris, Mumbai, Singapore, Tokyo, Sydney |
| Alleen Amerika | Oregon, Virginia |
| Alleen Europa | Ierland, Parijs |
| Alleen Azië - Stille Oceaan | Mumbai, Singapore, Tokio, Sydney |
| Alleen China* | Peking |

{style="table-layout:auto"}

*Alleen China en de RDC-typen wereldwijd + China vereisen het China Add-on-pakket. Global + China leidt gegevens van oorsprong uit China naar Adobe RDC, terwijl ze gegevens van oorsprong uit China naar de dichtstbijzijnde RDC buiten China leiden. Zie [Optimalisatie van Chinese prestaties](#china-performance-optimization) hieronder.

## Optimalisatie van Chinese prestaties

De China RDC (China Performance Optimization) add-on package is een belastbare add-on voor Adobe Analytics. Adobe Performance Optimization in Mainland stelt klanten met gebruikers in China in staat om die gegevens rechtstreeks naar Adobe gegevensverzamelingsservers in China te laten verzenden in plaats van naar andere locaties wereldwijd. Deze optimalisatie verbetert de laadtijden van de pagina en de nauwkeurigheid van de gegevens in vergelijking met het verzenden van de gegevens naar locaties buiten China. Gegevens worden uiteindelijk overgedragen naar een van de DPC (Adobe Data Processing Centers) buiten China. Neem voor meer informatie contact op met je Adobe-verkoper.

>[!NOTE]
>
>Het China RDC-invoegpakket wordt niet ondersteund voor de [Web SDK](/help/implement/aep-edge/overview.md).

