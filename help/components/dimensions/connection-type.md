---
title: Verbindingstype
description: Hoe de bezoeker verbinding maakt met internet.
feature: Dimensions
exl-id: 149b2353-6128-4e0c-a73a-bc5a37c66b52
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---

# Verbindingstype

Het type &#39;Verbinding&#39; [dimensie](overview.md) toont hoe de bezoeker verbinding heeft gemaakt met internet. Deze dimensie is handig om te bepalen hoe bezoekers verbinding maken met internet om door uw site te bladeren. U kunt dit gebruiken om site-inhoud te optimaliseren op basis van de verbindingssnelheid van bezoekers.

## Deze dimensie vullen met gegevens

Deze dimensie gebruikt een combinatie van [`ct` querytekenreeks](/help/implement/validate/query-parameters.md) en Adobe serverlogica. De Adobe gebruikt de volgende regels om zijn waarde te bepalen:

1. Als de `ct` queryreeks is gelijk aan `"modem"`, stelt u het dimensie-item in op `"Modem"`. Dit AppMeasurement verzamelt deze gegevens alleen in niet-ondersteunde Internet Explorer-browsers, waardoor dit dimensie-item ongebruikelijk wordt.
1. Controleer het IP adres van de slag en verwijs het naar een raadplegingstabel intern aan Adobe. Als het IP adres van een mobiele drager is, plaats het afmetingspunt aan `"Mobile Carrier"`.
1. Als de `ct` queryreeks is gelijk aan `"lan"`, stelt u het dimensie-item in op `"LAN/Wifi"`.
1. Als de treffer afkomstig is van een [Gegevensbron](/help/import/data-sources/overview.md) of anders beschouwd wordt als een speciaal type hit, stelt u het dimensie-item in op `"Not specified"`.
1. Als aan geen van bovenstaande regels is voldaan, wordt de waarde van `"LAN/Wifi"`.

## Dimension-items

Tot Dimension-items behoren `LAN/Wifi`, `Mobile Carrier`, `Modem`, en `Not Specified`.

* **`LAN/Wifi`**: De bezoeker heeft verbinding gemaakt met internet via een vaste lijn of wifi-hotspot.
* **`Mobile Carrier`**: De bezoeker heeft verbinding gemaakt met internet via een mobiele provider.
* **`Modem`**: De bezoeker heeft verbinding gemaakt met internet via een modem in een niet-ondersteunde Internet Explorer-browser.
* **`Not Specified`**: De hit heeft geen verbindingstype.
