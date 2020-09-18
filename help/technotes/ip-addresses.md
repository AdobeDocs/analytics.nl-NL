---
title: IPs en domeinen die door Adobe Analytics worden gebruikt
description: Als de firewall van uw organisatie IP adressen blokkeert die van Adobe afkomstig zijn, gebruik deze lijst om uw firewallmontages bij te werken.
translation-type: tm+mt
source-git-commit: 616a6e50e08be831b05f4abdbb3d47f659046d6f
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 0%

---


# IPs en domeinen die door Adobe Analytics worden gebruikt

Sommige firewallconfiguraties blokkeren IP adressen voortkomend uit de servers van de Adobe van de gegevensinzameling of servers verantwoordelijk voor de toegang tot van gegevens. U kunt deze lijst met bereiken gebruiken om de firewallinstellingen van uw organisatie te wijzigen, zodat u toegang hebt en gegevens kunt verzenden vanuit uw organisatie.

>[!IMPORTANT]
>
>Hoewel Adobe zijn best doet om dit document huidig te houden, kan het niet de lijst van IP waaiers waarborgen het zelfde blijft. Mogelijke veranderingen omvatten de uitbreiding van het bedrijf, een Internet register vereist veranderingen in de adresruimte van Adobe IP, of een dienstverlener houdt op werkend Internet.

## Afhankelijke technologiedomeinen toestaan

Adobe Analytics gebruikt de volgende hosts om de prestaties en de productervaring te verbeteren. Adobe raadt u aan deze domeinen toe te voegen aan de lijst van gewenste personen van uw firewall voor een optimale ervaring met Adobe Analytics.

| Technologie | Domein |
| --- | --- |
| Adobe Analytics-domein | `adobe.com` |
| Adobe Analytics verouderd domein | `omniture.com` |
| Amazon AWS | `aaui-879784980514.s3.us-east-2.amazonaws.com` |
| Amazon CloudFront | `d30ln29764hddd.cloudfront.net` |
| Geniet | `esp.aptrinsic.com` |
| LaunchDarkly | `app.launchdarkly.com` |
| Microsoft Azure Blob-opslag | `awaascicdprodva7.blob.core.windows.net` |
| Microsoft Azure CDN | `aauicdnva7.azureedge.net` |

## Alle Adobe Analytics IP-adresblokken

De volgende tabel bevat alle standaardservers voor gegevensverzameling en regionale servers voor gegevensverzameling voor Adobe Analytics. Ze omvatten geen afzonderlijke AWS-hosts.

| IP-blok (CIDR-notatie) |
| --- |
| `63.140.32.0/19` |
| `66.117.16.0/20` |
| `66.235.128.0/19` |
| `130.248.0.0/16` |
| `172.82.192.0/18` |
| `185.34.188.0/22` |
| `192.243.224.0/19` |
| `205.219.231.0/24` |
| `208.67.40.0/22` |
| `208.77.136.0/22` |

## Gegevensverzameling en FTP IP-adresblokken

Als uw organisatie verkiest om specifieke IP adreswaaiers toe te staan kunt u de volgende lijst gebruiken. Alle bereiken in deze sectie zijn opgenomen in de bovenstaande tabel.

| Locatie | IP-bereik (CIDR-notatie) |
| --- | --- |
| Amsterdam | `66.117.28.0/23` |
| Dallas | `205.219.231.0/24` |
| Dallas | `66.235.152.0/22` |
| Dallas | `66.235.140.0/22` |
| Dallas | `63.140.32.0/21` |
| Dallas | `172.82.208.0/22` |
| SAR Hongkong van China | `66.117.24.0/22` |
| Londen | `66.235.156.0/24` |
| Londen | `66.235.148.0/23` |
| Londen | `63.140.40.0/22` |
| Londen | `208.67.41.0/24` |
| Londen | `192.243.254.0/23` |
| Londen | `192.243.244.0/22` |
| Londen | `185.34.188.0/23` |
| Londen | `130.248.152.0/21` |
| Londen | `172.82.224.0/21` |
| Londen | `172.82.232.0/21` |
| Oregon | `192.243.240.0/22` |
| Oregon | `192.243.232.0/21` |
| Oregon | `192.243.224.0/21` |
| Oregon | `130.248.160.0/21` |
| Oregon | `130.248.148.0/22` |
| Oregon | `172.82.192.0/21` |
| Oregon | `172.82.216.0/21` |
| Parijs | `208.67.40.0/24` |
| Singapore | `66.235.150.0/24` |
| Singapore | `66.235.130.0/23` |
| Singapore | `63.140.44.0/22` |
| Singapore | `208.67.43.0/24` |
| Singapore | `172.82.240.0/22` |
| Singapore | `172.82.246.0/23` |
| Singapore | `172.82.248.0/21` |
| San Jose | `66.117.20.0/24` |
| San Jose | `66.235.132.0/22` |
| San Jose | `130.248.128.0/22` |
| San Jose | `192.243.248.0/23` |
| San Jose | `172.82.200.0/22` |
| San Jose | `66.235.136.0/22` |
| San Jose | `208.91.175.0/24` |
| San Jose | `208.91.174.0/24` |
| San Jose | `208.91.169.0/24` |
| Sydney | `216.104.216.0/23` |
| Tokyo | `66.235.159.0/24` |
| Tokyo | `66.117.21.0/24` |
| Tokyo | `63.140.52.0/24` |
| Tokyo | `63.140.50.0/23` |
| Virginia | `66.235.144.0/22` |
| Virginia | `208.77.138.0/23` |
| Virginia | `208.77.136.0/23` |
| Virginia | `192.243.250.0/23` |
| Virginia | `130.248.144.0/22` |
| Virginia | `172.82.204.0/22` |
| Virginia | `172.82.212.0/22` |
| Virginia | Zie AWS-hosts |

## AWS-hosts

Adobe Analytics gebruikt Amazon Web Services als onderdeel van het gegevensverzamelingsproces. De volgende tabel bevat AWS-hosts die zijn gereserveerd voor Adobe. Deze hosts zijn **niet** opgenomen in het hierboven vermelde bereik van aggregaten.

| Locatie | Host |
| --- | --- |
| Australië | `13.238.77.77` |
| Australië | `52.62.21.192` |
| Australië | `54.66.152.159` |
| Frankrijk | `15.188.154.177` |
| Frankrijk | `15.236.175.233` |
| Frankrijk | `15.236.9.100` |
| India | `13.232.177.101` |
| India | `13.235.4.163` |
| India | `3.6.119.69` |
| Ierland | `52.17.94.37` |
| Ierland | `52.49.253.16` |
| Ierland | `52.51.63.15` |
| Oregon | `52.42.60.49` |
| Oregon | `54.212.169.56` |
| Oregon | `54.214.170.191` |
| Singapore | `13.228.34.224` |
| Singapore | `18.136.20.161` |
| Singapore | `52.74.162.152` |
| Tokyo | `13.112.72.86` |
| Tokyo | `18.178.74.225` |
| Tokyo | `18.179.88.228` |
| Virginia | `3.220.129.153` |
| Virginia | `18.211.197.67` |
| Virginia | `34.228.124.176` |
| Virginia | `34.234.106.101` |
| Virginia | `52.22.231.198` |
| Virginia | `54.157.65.136` |
