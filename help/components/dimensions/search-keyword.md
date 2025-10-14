---
title: Trefwoord zoeken
description: Het zoekwoord dat de bezoeker gebruikte om uw site te bereiken.
feature: Dimensions
exl-id: 5a1236a6-f94b-4679-906a-b539afe36887
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 0%

---

# Trefwoord zoeken

De &quot;sleutelwoord van het Onderzoek&quot;[&#x200B; dimensie &#x200B;](overview.md) meldt de onderzoekssleutelwoorden die de bezoekers gebruiken om uw plaats te bereiken.

>[!IMPORTANT]
>
>De meeste zoekprogramma&#39;s slagen niet langer voor het trefwoord Zoeken vanwege de toenemende privacy-praktijken. Dit is de locatie waar Adobe een zoekengine herkent, maar waar trefwoordgroepen ontbreken onder het dimensiemunt `"Keyword unavailable"` .

Een verwijzer moet aan beide volgende voorwaarden voldoen om als zoekwoord te classificeren:

* Het verwijzende domein wordt erkend door Adobe als geldige [&#x200B; motor van het Onderzoek &#x200B;](search-engine.md);
* De verwijzende URL bevat een parameter voor een trefwoordqueryreeks. Als de trefwoordqueryreeks bestaat maar geen waarde bevat, wordt deze onder het dimensiemunt `"Keyword unavailable"` gegroepeerd.

Als u betaald en natuurlijk onderzoek wilt onderscheiden, [&#x200B; Betaalde onderzoeksopsporing &#x200B;](/help/admin/tools/manage-rs/edit-settings/general/paid-search-detection/paid-search-detection.md) wordt vereist. Er zijn meerdere afmetingen beschikbaar voor zoektrefwoorden:

* **sleutelwoord van het Onderzoek**: Het onderzoekssleutelwoord dat wordt gebruikt om uw plaats te bereiken, ongeacht als het of natuurlijk wordt betaald.
* **het sleutelwoord van het Onderzoek - betaald**: Het onderzoekssleutelwoord dat wordt gebruikt om uw plaats te bereiken, die betaalde onderzoeksopsporing overstemde.
* **het sleutelwoord van het Onderzoek - natuurlijk**: Het onderzoekssleutelwoord dat wordt gebruikt om uw plaats te bereiken, die betaalde onderzoeksopsporing niet aanpast.

## Deze dimensie vullen met gegevens

Deze dimensie verwijst naar meerdere opzoektabellen die intern zijn voor Adobe. Elke waarde is gebaseerd op [&#x200B; verwijzer &#x200B;](referrer.md) van de klap, die van [&#x200B; Interne filters URL &#x200B;](/help/admin/tools/manage-rs/edit-settings/general/internal-url-filter-admin.md) afhangt. Zorg ervoor dat de verwijzingsafmeting en interne filters URL correct worden gevormd.

## Dimension-objecten

Dimension-objecten bevatten zoektrefwoorden die worden gebruikt om je site te bereiken. Het `"Unspecified"` dimensie-item is allemaal niet-zoekverkeer.
