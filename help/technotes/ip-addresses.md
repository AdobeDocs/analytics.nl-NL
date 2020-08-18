---
title: In de Adobe Experience Cloud gebruikte IP's en domeinen
description: Als de firewall van uw organisatie IP adressen blokkeert die van Adobe afkomstig zijn, gebruik deze lijst om uw firewallmontages bij te werken.
translation-type: tm+mt
source-git-commit: b569f87dde3b9a8b323e0664d6c4d1578d410bb7
workflow-type: tm+mt
source-wordcount: '526'
ht-degree: 0%

---


# In de Adobe Experience Cloud gebruikte IP&#39;s en domeinen

Sommige firewallconfiguraties blokkeren IP adressen voortkomend uit de servers van de Adobe van de gegevensinzameling of servers verantwoordelijk voor de toegang tot van gegevens. De volgende lijst van IP adresblokken behandelt de momenteel bekende adressen betrokken in Adobe Experience Cloud. U kunt deze lijst met bereiken gebruiken om de firewallinstellingen van uw organisatie te wijzigen, zodat u toegang hebt en gegevens kunt verzenden vanuit uw organisatie.

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

## Alle Adobe IP-adresblokken

De volgende lijst behandelt alle openbare IP van Adobe Experience Cloud adressen die door Adobe worden bezeten. Deze reeksen omvatten standaard gegevensverzamelingsservers en regionale gegevensverzamelingsservers voor Adobe Analytics. Ze omvatten geen afzonderlijke AWS-hosts.

Veel van de diensten van de Adobe en de mogelijkheden delen IP blokken en waaiers, nochtans hebben sommige hun eigen ruimte. Blokken die slechts één oplossing gebruiken, worden als zodanig aangegeven.

| IP-blok (CIDR-notatie) | Notities |
| --- | --- |
| `62.210.161.0/24` | Specifiek voor Adobe Campaign |
| `63.140.32.0/19` |  |
| `66.117.16.0/20` |  |
| `66.235.128.0/19` |  |
| `67.226.212.0/23` | Specifiek voor Adobe Advertising Cloud |
| `103.202.219.0/24` | Specifiek voor Adobe Advertising Cloud |
| `130.248.0.0/16` |  |
| `172.82.192.0/18` |  |
| `185.34.188.0/22` |  |
| `185.148.48.0/24` | Specifiek voor Adobe Advertising Cloud |
| `192.243.224.0/19` |  |
| `198.98.22.0/23` | Specifiek voor Adobe Advertising Cloud |
| `205.219.231.0/24` |  |
| `208.67.40.0/22` |  |
| `208.77.136.0/22` |  |
| `208.91.168.0/21` | Specifiek voor Adobe Advertising Cloud |

## Gegevensverzameling en FTP IP-adresblokken

Als uw organisatie verkiest om specifieke IP adreswaaiers toe te staan kunt u de volgende lijst gebruiken. Alle bereiken in deze sectie zijn opgenomen in de bovenstaande tabel.

| Locatie | IP-bereik (CIDR-notatie) | Notities |
| --- | --- | --- |
| Amsterdam | `66.117.28.0/23` |  |
| Dallas | `205.219.231.0/24` |  |
| Dallas | `66.235.152.0/22` |  |
| Dallas | `66.235.140.0/22` |  |
| Dallas | `63.140.32.0/21` |  |
| Dallas | `172.82.208.0/22` |  |
| SAR Hongkong van China | `66.117.24.0/22` |  |
| Londen | `66.235.156.0/24` |  |
| Londen | `66.235.148.0/23` |  |
| Londen | `66.117.16.0/23` | Specifiek voor Adobe Campaign |
| Londen | `63.140.40.0/22` |  |
| Londen | `208.67.41.0/24` |  |
| Londen | `192.243.254.0/23` |  |
| Londen | `192.243.244.0/22` |  |
| Londen | `185.34.188.0/23` |  |
| Londen | `130.248.152.0/21` |  |
| Londen | `172.82.224.0/21` |  |
| Londen | `172.82.232.0/21` |  |
| Oregon | `192.243.240.0/22` |  |
| Oregon | `192.243.232.0/21` |  |
| Oregon | `192.243.224.0/21` |  |
| Oregon | `130.248.160.0/21` |  |
| Oregon | `130.248.148.0/22` |  |
| Oregon | `172.82.192.0/21` |  |
| Oregon | `172.82.216.0/21` |  |
| Parijs | `62.210.161.0/24` | Specifiek voor Adobe Campaign |
| Parijs | `66.117.18.0/23` | Specifiek voor Adobe Campaign |
| Parijs | `208.67.40.0/24` |  |
| Singapore | `66.235.150.0/24` |  |
| Singapore | `66.235.130.0/23` |  |
| Singapore | `63.140.44.0/22` |  |
| Singapore | `208.67.43.0/24` |  |
| Singapore | `172.82.240.0/22` |  |
| Singapore | `172.82.246.0/23` |  |
| Singapore | `172.82.248.0/21` |  |
| San Jose | `66.117.20.0/24` |  |
| San Jose | `66.235.132.0/22` |  |
| San Jose | `130.248.128.0/22` |  |
| San Jose | `192.243.248.0/23` |  |
| San Jose | `172.82.200.0/22` |  |
| San Jose | `66.235.136.0/22` |  |
| San Jose | `208.91.175.0/24` |  |
| San Jose | `208.91.174.0/24` |  |
| San Jose | `208.91.169.0/24` |  |
| Sydney | `216.104.216.0/23` |  |
| Tokyo | `66.235.159.0/24` |  |
| Tokyo | `66.117.21.0/24` |  |
| Tokyo | `63.140.52.0/24` |  |
| Tokyo | `63.140.50.0/23` |  |
| Virginia | `66.235.144.0/22` |  |
| Virginia | `208.77.138.0/23` |  |
| Virginia | `208.77.136.0/23` |  |
| Virginia | `192.243.250.0/23` |  |
| Virginia | `130.248.144.0/22` |  |
| Virginia | `172.82.204.0/22` |  |
| Virginia | `172.82.212.0/22` |  |
| Virginia | Zie AWS-hosts |  |

## AWS-hosts

Sommige Adobe-mogelijkheden gebruiken Amazon Web Services om gegevens te verzamelen. De volgende tabel bevat AWS-hosts die zijn gereserveerd voor Adobe. Deze hosts zijn **niet** opgenomen in het hierboven vermelde bereik van aggregaten.

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
| Londen | `172.82.228.19` |
| Oregon | `52.42.60.49` |
| Oregon | `54.212.169.56` |
| Oregon | `54.214.170.191` |
| Singapore | `13.228.34.224` |
| Singapore | `18.136.20.161` |
| Singapore | `52.74.162.152` |
| Tokyo | `13.112.72.86` |
| Tokyo | `18.178.74.225` |
| Tokyo | `18.179.88.228` |
| Virginia | `34.234.106.101` |
| Virginia | `52.22.231.198` |
| Virginia | `54.157.65.136` |
| Virginia | `107.23.142.4` |
| Virginia | `34.192.14.184` |
| Virginia | `34.192.146.173` |
| Virginia | `34.192.229.76` |
| Virginia | `34.196.183.216` |
| Virginia | `34.196.219.120` |
| Virginia | `34.196.54.55` |
| Virginia | `34.197.179.21` |
| Virginia | `34.197.45.49` |
| Virginia | `34.197.93.163` |
| Virginia | `34.198.80.27` |
| Virginia | `34.199.102.192` |
| Virginia | `34.199.46.40` |
| Virginia | `34.199.99.62` |
| Virginia | `34.200.67.35` |
| Virginia | `34.204.146.235` |
| Virginia | `34.204.164.1` |
| Virginia | `34.204.27.249` |
| Virginia | `34.205.224.111` |
| Virginia | `34.206.69.71` |
| Virginia | `52.193.88.44` |
| Virginia | `52.200.108.250` |
| Virginia | `52.200.171.156` |
| Virginia | `52.201.49.195` |
| Virginia | `52.205.244.105` |
| Virginia | `52.207.161.156` |
| Virginia | `52.22.148.55` |
| Virginia | `52.4.155.255` |
| Virginia | `52.72.182.205` |
| Virginia | `52.72.185.111` |
| Virginia | `54.152.218.194` |
| Virginia | `54.173.37.66` |
| Virginia | `54.173.69.38` |
| Virginia | `54.236.180.248` |
| Virginia | `54.236.71.218` |
| Virginia | `54.80.103.29` |
| Virginia | `54.88.180.124` |
