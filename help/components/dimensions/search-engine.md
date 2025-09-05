---
title: Zoekmachine
description: Het zoekprogramma dat de bezoeker gebruikte om uw site te bereiken.
feature: Dimensions
exl-id: 2815f1fa-d938-4d2b-b864-c4ed834f3ed3
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 0%

---

# Zoekmachine

De &quot;motor van het Onderzoek&quot;[ dimensie ](overview.md) meldt de onderzoeksmotoren die de bezoekers gebruiken om uw plaats te bereiken. Een referentie moet aan beide volgende voorwaarden voldoen om als zoekmachine te worden geclassificeerd:

* Het verwijzende domein wordt door Adobe erkend als een geldige zoekmachine;
* De verwijzende URL bevat een parameter voor een trefwoordqueryreeks. De parameter van het vraagkoord kan leeg zijn (zoals het geval met verscheidene onderzoeksmotoren toe te schrijven aan privacypraktijken).

Als u betaald en natuurlijk onderzoek wilt onderscheiden, [ Betaalde onderzoeksopsporing ](/help/admin/tools/manage-rs/edit-settings/general/paid-search-detection/paid-search-detection.md) wordt vereist. Er zijn meerdere afmetingen beschikbaar voor zoekprogramma&#39;s:

* **motor van het Onderzoek**: De onderzoeksmotor die wordt gebruikt om uw plaats te bereiken, ongeacht als het of natuurlijk wordt betaald.
* **motor van het Onderzoek - betaald**: De onderzoeksmotor die wordt gebruikt om uw plaats te bereiken, die betaalde onderzoeksopsporing overstemde.
* **motor van het Onderzoek - natuurlijk**: De onderzoeksmotor die wordt gebruikt om uw plaats te bereiken, die betaalde onderzoeksopsporing niet aanpast.

## Deze dimensie vullen met gegevens

Deze dimensie verwijst naar meerdere opzoektabellen die intern zijn voor Adobe. Elke waarde is gebaseerd op [ verwijzer ](referrer.md) van de klap, die van [ Interne filters URL ](/help/admin/tools/manage-rs/edit-settings/general/internal-url-filter-admin.md) afhangt. Zorg ervoor dat de verwijzingsafmeting en interne filters URL correct worden gevormd.

## Dimension-objecten

Dimension-objecten bevatten zoekprogramma&#39;s waarmee je je site kunt bereiken. Voorbeelden van waarden zijn `"Google"` , `"Microsoft Bing"` en `"DuckDuckGo"` . Het `"Unspecified"` dimensie-item is allemaal niet-zoekverkeer.
