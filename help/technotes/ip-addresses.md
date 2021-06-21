---
title: IPs en domeinen die door Adobe Analytics worden gebruikt
description: Als de firewall van uw organisatie IP adressen blokkeert die van Adobe afkomstig zijn, gebruik deze lijst om uw firewallmontages bij te werken.
exl-id: e24a70e4-9ed4-4b87-8bab-4ed0aebedd1f
source-git-commit: 31fa03e0d8bba457953e10aa537d22b2d69b84c1
workflow-type: tm+mt
source-wordcount: '408'
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
| Adobe Analytics-domeinen | `adobe.com`, `adobe.net`, `adobe.io` |
| Adobe Analytics verouderd domein | `omniture.com` |
| Amazon AWS | `aaui-879784980514.s3.us-east-2.amazonaws.com` |
| Amazon CloudFront | `d30ln29764hddd.cloudfront.net` |
| Geniet | `esp.aptrinsic.com` |
| LaunchDarkly | `app.launchdarkly.com` |
| Microsoft Azure Blob-opslag | `awaascicdprodva7.blob.core.windows.net` |
| Microsoft Azure CDN | `aauicdnva7.azureedge.net` |

## Alle IP-adresblokken van Adobe Analytics Data Collection

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

Adobe Analytics gebruikt Amazon Web Services als onderdeel van het gegevensverzamelingsproces. De volgende tabel bevat AWS-hosts die zijn gereserveerd voor Adobe. Deze hosts worden **niet** opgenomen in het hierboven vermelde bereik van geaggregeerde blokken.

| Locatie | Host |
| --- | --- |
| Australië | `13.54.219.183` |
| Australië | `52.62.137.88` |
| Australië | `54.79.162.112` |
| China | `52.81.111.133` |
| China | `140.179.22.22` |
| Frankrijk | `13.36.218.177` |
| Frankrijk | `15.188.95.229` |
| Frankrijk | `15.236.176.210` |
| India | `65.0.114.116` |
| India | `65.0.115.179` |
| India | `65.0.25.111` |
| India | `3.7.24.204` |
| India | `3.108.50.194` |
| India | `3.108.177.136` |
| Ierland | `18.202.158.78` |
| Ierland | `54.72.205.114` |
| Ierland | `54.78.36.71` |
| Ierland | `54.220.133.225` |
| Ierland | `54.74.170.177` |
| Ierland | `54.195.254.128` |
| Oregon | `44.233.255.254` |
| Oregon | `44.237.54.118` |
| Oregon | `44.238.157.95` |
| Oregon | `54.212.155.93` |
| Oregon | `52.10.149.115` |
| Oregon | `52.40.172.46` |
| Singapore | `52.220.116.94` |
| Singapore | `52.76.68.91` |
| Singapore | `54.179.114.68` |
| Singapore | `54.255.88.178` |
| Singapore | `52.220.235.10` |
| Singapore | `3.1.237.132` |
| Tokyo | `18.182.161.178` |
| Tokyo | `54.168.58.167` |
| Tokyo | `54.178.61.109` |
| Tokyo | `3.113.78.189` |
| Tokyo | `13.115.137.161` |
| Tokyo | `54.178.162.114` |
| Virginia | `3.213.168.181` |
| Virginia | `3.219.249.186` |
| Virginia | `3.220.129.153` |
| Virginia | `18.206.109.10` |
| Virginia | `18.211.197.67` |
| Virginia | `34.227.41.189` |
| Virginia | `34.228.124.176` |
| Virginia | `54.90.190.103` |
| Virginia | `54.174.149.161` |
