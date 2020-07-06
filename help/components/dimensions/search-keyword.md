---
title: Trefwoord zoeken
description: Het zoekwoord dat de bezoeker gebruikte om uw site te bereiken.
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 0%

---


# Trefwoord zoeken

De dimensie &#39;sleutelwoord zoeken&#39; rapporteert de zoektrefwoorden die bezoekers gebruiken om uw site te bereiken.

>[!IMPORTANT]
>
>De meeste zoekprogramma&#39;s slagen niet langer voor het trefwoord Zoeken vanwege de toenemende privacy-praktijken. Hier wordt een zoekprogramma herkend, maar er ontbreken trefwoordgroepen onder de waarde Dimensie `"Keyword unavailable"`.

Een verwijzer moet aan beide volgende voorwaarden voldoen om als zoekwoord te classificeren:

* Het verwijzende domein wordt erkend door Adobe als geldige motor [van het](search-engine.md)Onderzoek;
* De verwijzende URL bevat een parameter voor een trefwoordqueryreeks. Als de trefwoordqueryreeks bestaat maar geen waarde bevat, wordt deze onder de waarde Dimensie gegroepeerd `"Keyword unavailable"`.

Als u betaald en natuurlijk onderzoek wilt onderscheiden, wordt de [Betaalde onderzoeksopsporing](/help/admin/admin/paid-search-detection/paid-search-detection.md) vereist. Er zijn meerdere afmetingen beschikbaar voor zoektrefwoorden:

* **Zoektrefwoord**: Het zoektrefwoord dat wordt gebruikt om uw site te bereiken, ongeacht of het betaald of natuurlijk is.
* **Zoeken op trefwoord - betaald**: Het zoektrefwoord dat wordt gebruikt om uw site te bereiken en dat overeenkomt met betaalde zoekdetectie.
* **Zoeken op trefwoord - natuurlijk**: Het zoektrefwoord dat wordt gebruikt om uw site te bereiken. Dit komt niet overeen met betaalde zoekdetectie.

## Deze dimensie vullen met gegevens

Deze dimensie verwijst naar meerdere interne opzoektabellen van Adobe. Elke waarde is gebaseerd op de [referentie](referrer.md) van de hit, die afhankelijk is van [interne URL-filters](/help/admin/admin/internal-url-filter-admin.md). Zorg ervoor dat de verwijzingsafmeting en interne filters URL correct worden gevormd.

## Dimensiewaarden

Dimensiewaarden zijn zoektrefwoorden die worden gebruikt om uw site te bereiken. De `"Unspecified"` afmetingswaarde is al verkeer niet-onderzoek.
