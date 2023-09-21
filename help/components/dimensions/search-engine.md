---
title: Zoekmachine
description: Het zoekprogramma dat de bezoeker gebruikte om uw site te bereiken.
feature: Dimensions
exl-id: 2815f1fa-d938-4d2b-b864-c4ed834f3ed3
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 0%

---

# Zoekmachine

De zoekmachine [dimensie](overview.md) meldt de zoekmachines die bezoekers gebruiken om uw site te bereiken. Een referentie moet aan beide volgende voorwaarden voldoen om als zoekmachine te worden geclassificeerd:

* Het verwijzende domein wordt door de Adobe erkend als een geldige zoekmachine;
* De verwijzende URL bevat een parameter voor een trefwoordqueryreeks. De parameter van het vraagkoord kan leeg zijn (zoals het geval met verscheidene onderzoeksmotoren toe te schrijven aan privacypraktijken).

Als u onderscheid wilt maken tussen betaald en natuurlijk zoeken, [Betaalde zoekdetectie](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/paid-search-detection/paid-search-detection.md) is vereist. Er zijn meerdere afmetingen beschikbaar voor zoekprogramma&#39;s:

* **Zoekmachine**: Het zoekprogramma dat u gebruikt om uw site te bereiken, ongeacht of het betaald of natuurlijk is.
* **Zoekmachine - betaald**: Het zoekprogramma dat u hebt gebruikt om uw site te bereiken en waarmee de betaalde zoekfunctie is gevonden.
* **Zoekmachine - natuurlijk**: Het zoekprogramma dat u hebt gebruikt om uw site te bereiken en dat niet overeenkomt met betaalde zoekdetectie.

## Deze dimensie vullen met gegevens

Deze dimensie verwijst naar veelvoudige raadplegingslijsten intern aan Adobe. Elke waarde is gebaseerd op de [verwijzende](referrer.md) van de hit, die afhankelijk is van [Interne URL-filters](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/internal-url-filter-admin.md). Zorg ervoor dat de verwijzingsafmeting en interne filters URL correct worden gevormd.

## Dimension-items

Dimension-items bevatten zoekprogramma&#39;s die worden gebruikt om uw site te bereiken. Voorbeelden van waarden zijn `"Google"`, `"Microsoft Bing"`, en `"DuckDuckGo"`. De `"Unspecified"` Dimensie-item is alle niet-zoekverkeer.
