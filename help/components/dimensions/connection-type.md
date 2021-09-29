---
title: Verbindingstype
description: Hoe de bezoeker verbinding maakt met internet.
exl-id: 149b2353-6128-4e0c-a73a-bc5a37c66b52
source-git-commit: 82d6137bc9229bbaa997c6856690bf76c20b755c
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Verbindingstype

De dimensie &#39;Verbindingstype&#39; laat zien hoe de bezoeker verbinding heeft gemaakt met internet. Deze dimensie is handig om te bepalen hoe bezoekers verbinding maken met internet om door uw site te bladeren. U kunt dit gebruiken om site-inhoud te optimaliseren op basis van de verbindingssnelheid van bezoekers.

## Deze dimensie vullen met gegevens

Deze dimensie gebruikt een combinatie van [`ct` vraagkoord](/help/implement/validate/query-parameters.md) en Adobe server-zijlogica. Adobe gebruikt de volgende regels om de waarde ervan te bepalen:

1. Als de `ct` vraagkoord `"modem"` evenaart, plaats het afmetingspunt aan `"Modem"`. AppMeasurement verzamelt deze gegevens alleen in niet-ondersteunde Internet Explorer-browsers, waardoor dit dimensie-item ongebruikelijk wordt.
1. Controleer het IP adres van de klap en verwijs het naar een raadplegingslijst intern aan Adobe. Als het IP adres van een mobiele drager is, plaats het afmetingspunt aan `"Mobile Carrier"`.
1. Als de `ct` vraagkoord `"lan"` evenaart, plaats het afmetingspunt aan `"LAN/Wifi"`.
1. Als de hit afkomstig is van een [Gegevensbron](/help/import/c-data-sources/datasrc-home.md) of anderszins wordt beschouwd als een speciaal type hit, stelt u het dimensie-item in op `"Not specified"`.
1. Als aan geen van de bovenstaande regels wordt voldaan, standaard aan de waarde van `"LAN/Wifi"`.

## Dimension-items

Tot de Dimension-items behoren `LAN/Wifi`, `Mobile Carrier`, `Modem` en `Not Specified`.

* **`LAN/Wifi`**: De bezoeker heeft verbinding gemaakt met internet via een vaste lijn of wifi-hotspot.
* **`Mobile Carrier`**: De bezoeker heeft verbinding gemaakt met internet via een mobiele provider.
* **`Modem`**: De bezoeker heeft verbinding gemaakt met internet via een modem in een niet-ondersteunde Internet Explorer-browser.
* **`Not Specified`**: De hit heeft geen verbindingstype.
