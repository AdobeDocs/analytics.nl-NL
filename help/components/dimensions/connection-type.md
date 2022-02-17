---
title: Verbindingstype
description: Hoe de bezoeker verbinding maakt met internet.
feature: Dimensions
exl-id: 149b2353-6128-4e0c-a73a-bc5a37c66b52
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---

# Verbindingstype

De dimensie &#39;Verbindingstype&#39; laat zien hoe de bezoeker verbinding heeft gemaakt met internet. Deze dimensie is handig om te bepalen hoe bezoekers verbinding maken met internet om door uw site te bladeren. U kunt dit gebruiken om site-inhoud te optimaliseren op basis van de verbindingssnelheid van bezoekers.

## Deze dimensie vullen met gegevens

Deze dimensie gebruikt een combinatie van [`ct` querytekenreeks](/help/implement/validate/query-parameters.md) en Adobe server-side logica. Adobe gebruikt de volgende regels om de waarde ervan te bepalen:

1. Als de `ct` queryreeks is gelijk `"modem"`, stelt u het dimensie-item in op `"Modem"`. AppMeasurement verzamelt deze gegevens alleen in niet-ondersteunde Internet Explorer-browsers, waardoor dit dimensie-item ongebruikelijk wordt.
1. Controleer het IP adres van de klap en verwijs het naar een raadplegingslijst intern aan Adobe. Als het IP adres van een mobiele drager is, plaats het afmetingspunt aan `"Mobile Carrier"`.
1. Als de `ct` queryreeks is gelijk `"lan"`, stelt u het dimensie-item in op `"LAN/Wifi"`.
1. Als de treffer afkomstig is van een [Gegevensbron](/help/import/c-data-sources/datasrc-home.md) of anders beschouwd wordt als een speciaal type hit, stelt u het dimensie-item in op `"Not specified"`.
1. Als aan geen van bovenstaande regels is voldaan, wordt de waarde van `"LAN/Wifi"`.

## Dimension-items

Dimension-items bevatten `LAN/Wifi`, `Mobile Carrier`, `Modem`, en `Not Specified`.

* **`LAN/Wifi`**: De bezoeker heeft verbinding gemaakt met internet via een vaste lijn of wifi-hotspot.
* **`Mobile Carrier`**: De bezoeker heeft verbinding gemaakt met internet via een mobiele provider.
* **`Modem`**: De bezoeker heeft verbinding gemaakt met internet via een modem in een niet-ondersteunde Internet Explorer-browser.
* **`Not Specified`**: De hit heeft geen verbindingstype.
