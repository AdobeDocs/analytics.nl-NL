---
title: Trefwoord zoeken
description: Het zoekwoord dat de bezoeker gebruikte om uw site te bereiken.
feature: Dimensions
exl-id: 5a1236a6-f94b-4679-906a-b539afe36887
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 0%

---

# Trefwoord zoeken

Het trefwoord &#39;Zoeken&#39; [dimensie](overview.md) rapporteert de zoektrefwoorden die bezoekers gebruiken om uw site te bereiken.

>[!IMPORTANT]
>
>De meeste zoekprogramma&#39;s slagen niet langer voor het trefwoord Zoeken vanwege de toenemende privacy-praktijken. Hier wordt een zoekmachine herkend door de Adobe, maar er ontbreken trefwoordgroepen onder het dimensie-item `"Keyword unavailable"`.

Een verwijzer moet aan beide volgende voorwaarden voldoen om als zoekwoord te classificeren:

* Het verwijzende domein wordt door de Adobe erkend als geldig [Zoekmachine](search-engine.md);
* De verwijzende URL bevat een parameter voor een trefwoordqueryreeks. Als de trefwoordqueryreeks bestaat, maar geen waarde bevat, wordt deze onder het dimensiepunt gegroepeerd `"Keyword unavailable"`.

Als u onderscheid wilt maken tussen betaald en natuurlijk zoeken, [Betaalde zoekdetectie](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/paid-search-detection/paid-search-detection.md) is vereist. Er zijn meerdere afmetingen beschikbaar voor zoektrefwoorden:

* **Trefwoord zoeken**: Het zoektrefwoord dat wordt gebruikt om uw site te bereiken, ongeacht of het betaald of natuurlijk is.
* **Zoeken op trefwoord - betaald**: Het zoektrefwoord dat wordt gebruikt om uw site te bereiken en dat overeenkomt met betaalde zoekdetectie.
* **Zoeken op trefwoord - natuurlijk**: Het zoekwoord dat wordt gebruikt om uw site te bereiken. Dit komt niet overeen met betaalde zoekdetectie.

## Deze dimensie vullen met gegevens

Deze dimensie verwijst naar veelvoudige raadplegingslijsten intern aan Adobe. Elke waarde is gebaseerd op de [verwijzende](referrer.md) van de hit, die afhankelijk is van [Interne URL-filters](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/internal-url-filter-admin.md). Zorg ervoor dat de verwijzingsafmeting en interne filters URL correct worden gevormd.

## Dimension-items

Items van Dimensionen bevatten zoektrefwoorden die worden gebruikt om uw site te bereiken. De `"Unspecified"` Dimensie-item is alle niet-zoekverkeer.
