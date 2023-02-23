---
title: IPs en domeinen die door Adobe Analytics worden gebruikt
description: Als de firewall van uw organisatie IP adressen blokkeert die van Adobe afkomstig zijn, gebruik deze lijst om uw firewallmontages bij te werken.
feature: Data Configuration and Collection
exl-id: e24a70e4-9ed4-4b87-8bab-4ed0aebedd1f
source-git-commit: d109011bcdbc6b5f37c9304e5d72f572a4245193
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 0%

---

# IPs en domeinen die door Adobe Analytics worden gebruikt

Sommige firewallconfiguraties blokkeren IP adressen voortkomend uit de servers van de Adobe van de gegevensinzameling of servers verantwoordelijk voor de toegang tot van gegevens. U kunt deze lijst met bereiken gebruiken om de firewallinstellingen van uw organisatie te wijzigen, zodat u toegang hebt en gegevens kunt verzenden vanuit uw organisatie. Deze pagina omvat zowel binnenkomende systemen (zoals gegevensinzameling) als uitgaande systemen (zoals gegevensvoer) die Adobe gebruikt.

>[!IMPORTANT]
>
>Hoewel Adobe zijn best doet om dit document huidig te houden, kan het niet garanderen dat de lijst van IP waaiers het zelfde blijft. Mogelijke veranderingen omvatten de uitbreiding van het bedrijf, een Internet register vereist veranderingen in de adresruimte van Adobe IP, of een dienstverlener houdt op werkend Internet.

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
| Microsoft Azure Blob Storage | `awaascicdprodva7.blob.core.windows.net` |
| Microsoft Azure CDN | `aauicdnva7.azureedge.net` |

## Alle Adobe Analytics IP-adresblokken

De volgende lijst behandelt alle Adobe-bezeten IP adressen die voor Adobe Analytics worden gebruikt. Zij omvatten niet alle diensten die in openbare wolken worden ontvangen.

| IP-blok (CIDR-notatie) |
| --- |
| `63.140.32.0/19` |
| `66.117.16.0/20` |
| `66.235.128.0/19` |
| `130.248.0.0/16` |
| `185.34.188.0/22` |

## Gegevensverzameling en FTP IP-adresblokken

Als uw organisatie verkiest om specifieke IP adreswaaiers toe te staan kunt u de volgende lijst gebruiken. Alle bereiken in deze sectie zijn opgenomen in de bovenstaande tabel. FTP-verbindingen voor Data Warehouse en gegevensfeeds zijn alleen afkomstig van de locaties Londen, Oregon en Singapore.

| Locatie | IP-bereik (CIDR-notatie) |
| --- | --- |
| Australië | `63.140.55.0/24` |
| Australië | `63.140.56.0/23` |
| California | `63.140.32.0/23` |
| California | `63.140.34.0/24` |
| Frankrijk | `63.140.62.0/23` |
| India | `66.117.20.0/24` |
| India | `66.117.22.0/23` |
| Japan | `130.248.130.0/23` |
| Japan | `130.248.169.0/23` |
| Japan | `63.140.50.0/23` |
| Japan | `66.117.31.0/24` |
| Londen | `66.235.156.0/24` |
| Londen | `185.34.188.0/22` |
| Oregon | `66.235.132.0/22` |
| Oregon | `130.248.150.0/24` |
| Oregon | `130.248.160.0/21` |
| Singapore | `130.248.170.0/23` |
| Singapore | `130.248.240.0/24` |
| Singapore | `63.140.44.0/22` |
| Singapore | `63.140.48.0/23` |
| Singapore | `66.117.30.0/24` |
| Virginia | `63.140.38.0/23` |
| Virginia | `63.140.54.0/24` |

## AWS-hosts

Adobe Analytics gebruikt Amazon Web Services als onderdeel van het gegevensverzamelingsproces. De volgende tabel bevat AWS IPv4-hostadressen die zijn gereserveerd voor Adobe. Deze hosts zijn **niet** opgenomen in het hierboven vermelde geaggregeerde blokbereik.

| Locatie | Host |
| --- | --- |
| China | `52.80.83.220` |
| China | `71.132.16.253` |
| China | `52.80.7.181` |
| China | `71.131.244.185` |
| China | `140.179.152.255` |
| Frankrijk | `13.37.25.97` |
| Frankrijk | `15.236.117.205` |
| Frankrijk | `15.236.125.10` |

De volgende tabel bevat AWS IPv6-adresblokken die door Adobe worden gebruikt. Deze hosts zijn **niet** opgenomen in het hierboven vermelde geaggregeerde blokbereik.

| Locatie | Host |
| --- | --- |
| Australië | `2406:da1c:406:1a00::/56` |
| Australië | `2406:da1c:ce5:b400::/56` |
| California | `2600:1f1c:366:d900::/56` |
| India | `2406:da1a:f34:6a00::/56` |
| Ierland | `2a05:d018:309:600::/56` |
| Japan | `2406:da14:b07:ab00::/56` |
| Oregon | `2600:1f14:1eb:7d00::/56` |
| Oregon | `2600:1f14:9d3:2b00::/56` |
| Singapore | `2406:da18:6e8:1e00::/56` |
| Virginia | `2600:1f18:1a20:e800::/56` |
| Virginia | `2600:1f18:4fd:6000::/56` |
| Virginia | `2600:1f18:b00:e100::/56` |
| Virginia | `2600:1f18:d1f:bd00::/56` |
