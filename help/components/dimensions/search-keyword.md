---
title: Trefwoord zoeken
description: Het zoekwoord dat de bezoeker gebruikte om uw site te bereiken.
feature: Dimensions
exl-id: 5a1236a6-f94b-4679-906a-b539afe36887
source-git-commit: 71ff81a0ae67c6f4cc9a8df567e27223cc63f18c
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 0%

---

# Trefwoord zoeken

De dimensie &#39;sleutelwoord zoeken&#39; rapporteert de zoektrefwoorden die bezoekers gebruiken om uw site te bereiken.

>[!IMPORTANT]
>
>De meeste zoekprogramma&#39;s slagen niet langer voor het trefwoord Zoeken vanwege de toenemende privacy-praktijken. Hits waar Adobe een onderzoeksmotor erkent maar een sleutelwoordgroepen onder het afmetingspunt mist `"Keyword unavailable"`.

Een verwijzer moet aan beide volgende voorwaarden voldoen om als zoekwoord te classificeren:

* Het verwijzende domein wordt door Adobe erkend als geldig [Zoekmachine](search-engine.md);
* De verwijzende URL bevat een parameter voor een trefwoordqueryreeks. Als de trefwoordqueryreeks bestaat, maar geen waarde bevat, wordt deze onder het dimensiepunt gegroepeerd `"Keyword unavailable"`.

Als u onderscheid wilt maken tussen betaald en natuurlijk zoeken, [Betaalde zoekdetectie](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/paid-search-detection/paid-search-detection.md) is vereist. Er zijn meerdere afmetingen beschikbaar voor zoektrefwoorden:

* **Trefwoord zoeken**: Het zoektrefwoord dat wordt gebruikt om uw site te bereiken, ongeacht of het betaald of natuurlijk is.
* **Zoeken op trefwoord - betaald**: Het zoektrefwoord dat wordt gebruikt om uw site te bereiken en dat overeenkomt met betaalde zoekdetectie.
* **Zoeken op trefwoord - natuurlijk**: Het zoektrefwoord dat wordt gebruikt om uw site te bereiken. Dit komt niet overeen met betaalde zoekdetectie.

## Deze dimensie vullen met gegevens

Deze dimensie verwijst naar veelvoudige raadplegingslijsten intern aan Adobe. Elke waarde is gebaseerd op de [referentie](referrer.md) van de hit, die afhankelijk is van [Interne URL-filters](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/internal-url-filter-admin.md). Zorg ervoor dat de verwijzingsafmeting en interne filters URL correct worden gevormd.

## Dimension-items

Dimension-items bevatten zoektrefwoorden die worden gebruikt om uw site te bereiken. De `"Unspecified"` Dimensie-item is alle niet-zoekverkeer.
