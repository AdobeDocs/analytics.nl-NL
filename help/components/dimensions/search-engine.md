---
title: Zoekmachine
description: Het zoekprogramma dat de bezoeker gebruikte om uw site te bereiken.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 0%

---


# Zoekmachine

De dimensie &#39;Zoekmachine&#39; rapporteert de zoekmachines die bezoekers gebruiken om uw site te bereiken. Een referentie moet aan beide volgende voorwaarden voldoen om als zoekmachine te worden geclassificeerd:

* Het verwijzende domein wordt erkend door Adobe als geldig onderzoeksintenus;
* De verwijzende URL bevat een parameter voor een trefwoordqueryreeks. De parameter van het vraagkoord kan leeg zijn (zoals het geval met verscheidene onderzoeksmotoren toe te schrijven aan privacypraktijken).

Als u betaald en natuurlijk onderzoek wilt onderscheiden, wordt de [Betaalde onderzoeksopsporing](/help/admin/admin/paid-search-detection/paid-search-detection.md) vereist. Er zijn meerdere afmetingen beschikbaar voor zoekprogramma&#39;s:

* **Zoekprogramma**: Het zoekprogramma dat u gebruikt om uw site te bereiken, ongeacht of het betaald of natuurlijk is.
* **Zoekmachine - betaald**: Het zoekprogramma dat u hebt gebruikt om uw site te bereiken en dat overeenkomt met betaalde zoekdetectie.
* **Zoekmachine - natuurlijk**: Het zoekprogramma dat u hebt gebruikt om uw site te bereiken en dat niet overeenkomt met de betaalde zoekfunctie.

## Deze dimensie vullen met gegevens

Deze dimensie verwijst naar meerdere interne opzoektabellen van Adobe. Elke waarde is gebaseerd op de [referentie](referrer.md) van de hit, die afhankelijk is van [interne URL-filters](/help/admin/admin/internal-url-filter-admin.md). Zorg ervoor dat de verwijzingsafmeting en interne filters URL correct worden gevormd.

## Dimensie-items

Dimensie-items bevatten zoekprogramma&#39;s die worden gebruikt om uw site te bereiken. Voorbeelden hiervan zijn `"Google"`, `"Microsoft Bing"`en `"DuckDuckGo"`. Het `"Unspecified"` afmetingspunt is al niet-onderzoekingsverkeer.
