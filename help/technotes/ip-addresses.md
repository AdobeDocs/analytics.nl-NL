---
title: IPs en domeinen die door Adobe Analytics worden gebruikt
description: Als de firewall van uw organisatie IP adressen blokkeert die uit Adobe voortkomen, gebruik deze lijst om uw firewallmontages bij te werken.
feature: Data Configuration and Collection
exl-id: e24a70e4-9ed4-4b87-8bab-4ed0aebedd1f
source-git-commit: ea859717c6a40b4eeeb9eca54b95718859af9c7b
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---

# IPs en domeinen die door Adobe Analytics worden gebruikt

Sommige firewallconfiguraties blokkeren domeinen waarop Adobe Analytics voor zijn productinterface steunt. U kunt deze lijst met domeinen gebruiken om de netwerkinstellingen van uw organisatie te wijzigen en producttoegang vanuit uw organisatie toe te staan.

## Afhankelijke technologiedomeinen toestaan

Adobe Analytics gebruikt de volgende hosts om de prestaties en de productervaring te verbeteren. Adobe raadt u aan deze domeinen toe te staan via de firewall van uw organisatie voor een optimale ervaring met Adobe Analytics.

| Technologie | Domein |
| --- | --- |
| Adobe Analytics-domeinen | `adobe.com`, `adobe.net`, `adobe.io` |
| Adobe Analytics verouderd domein | `omniture.com` |
| Amazon AWS | `aaui-879784980514.s3.us-east-2.amazonaws.com` |
| Amazon CloudFront | `d30ln29764hddd.cloudfront.net` |
| Geniet | `esp.aptrinsic.com`, `esp-m.aptrinsic.com` |
| LaunchDarkly | `app.launchdarkly.com` |
| Microsoft Azure Blob-opslag | `awaascicdprodva7.blob.core.windows.net` |
| Microsoft Azure CDN | `aauicdnva7.azureedge.net` |

{style="table-layout:auto"}

## Adobe Experience Cloud IP-adresblokken

Naast de bovengenoemde domeinen, baseert Adobe Analytics zich op verscheidene IP adresblokken voor gegevensinzameling en het uitvoeren rapporten.

Zie Adobe Experience Cloud IP adressen voor de volledige lijst van IP waaiers.

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
