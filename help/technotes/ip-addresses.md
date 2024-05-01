---
title: IP adressen die door Adobe Analytics worden gebruikt
description: Als de firewall van uw organisatie IP adressen blokkeert die uit Adobe voortkomen, gebruik deze lijst om uw firewallmontages bij te werken.
feature: Data Configuration and Collection
exl-id: e24a70e4-9ed4-4b87-8bab-4ed0aebedd1f
source-git-commit: 5ac6da2eb53d2748e8838ef2c6334a771abc26c9
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 0%

---

# IP adressen die door Adobe Analytics worden gebruikt

Sommige firewallconfiguraties blokkeren IP-adressen die afkomstig zijn van gegevensverzamelingsservers of servers van de Adobe die verantwoordelijk zijn voor de toegang tot gegevens. U kunt deze lijst met bereiken gebruiken om de firewallinstellingen van uw organisatie te wijzigen, zodat u toegang hebt en gegevens kunt verzenden vanuit uw organisatie.

Alle IP adressen die door Adobe Analytics worden gebruikt maken deel uit van [IP adressen die door Adobe Experience Cloud worden gebruikt](https://experienceleague.adobe.com/en/docs/core-services/interface/data-collection/ip-addresses), met uitzondering van het China Performance Optimization Add-on-pakket.

## IP van de Optimalisering van de Prestaties van China adressen

Het China Performance Optimization-add-on-pakket is een extra betaalde service die de prestaties van AppMeasurementen voor gegevensverzameling voor bezoekers in China verbetert. Neem contact op met het accountteam van de Adobe voor meer informatie over het gebruik van deze functie.

>[!IMPORTANT]
>
>China RDC is niet beschikbaar voor Web SDK gegevensverzameling. Deze servers zijn alleen van toepassing op bibliotheken met AppMeasurementen.

De regionale servers van de gegevensinzameling in China gebruiken de volgende IP adressen:

| Locatie | Host |
| --- | --- |
| China | `52.80.168.159` |
| China | `52.80.199.104` |
| China | `54.223.199.8` |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>[IP adressen die door Adobe Experience Cloud worden gebruikt](https://experienceleague.adobe.com/en/docs/core-services/interface/data-collection/ip-addresses)
>
>[Door Adobe Analytics gebruikte domeinen](domains.md)
