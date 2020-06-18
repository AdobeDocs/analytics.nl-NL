---
title: Adobe Analytics implementeren
description: Implementeer Adobe Analytics op uw website, eigenschap of applicatie.
translation-type: ht
source-git-commit: 8a090574a6822a76366343ad5c657280bf7475eb

---


# Adobe Analytics implementeren

![Banner](../../assets/doc_banner_implement.png)

Voor Adobe is code op uw site of applicatie vereist om data naar de servers voor dataverzameling van Adobe te verzenden. De volgende stappen geven aan hoe een normale implementatie werkt.

1. Wanneer een bezoeker naar uw site komt, wordt een aanvraag ingediend bij uw webserver.
2. De webserver van uw site verzendt de paginacodegegevens en de pagina wordt weergegeven in de browser.
3. De pagina wordt geladen en de Analytics JavaScript-code wordt uitgevoerd.
De JavaScript-code verzendt een afbeeldingsaanvraag voor Adobe-dataverzamelingservers. De paginadata die u in uw implementatie hebt gedefinieerd, worden verzonden als onderdeel van een querytekenreeks in deze afbeeldingsaanvraag.

4. Adobe retourneert een transparante pixelafbeelding.
5. Adobe-servers slaan verzamelde data op in een *rapportsuite*.
6. De data van de rapportsuite worden ingevuld in rapporten die u in een webbrowser kunt openen.

   Het uitvoeren van de JavaScript-code gebeurt snel en heeft geen merkbare invloed op de laadtijden van de pagina. Op deze manier kunt u de pagina&#39;s tellen die worden weergegeven wanneer een bezoeker op **[!UICONTROL Reload]** of **[!UICONTROL Back]** klikt om naar een pagina te gaan, omdat de JavaScript-code ook wordt uitgevoerd wanneer de pagina uit de cache wordt opgehaald.

Voor Adobe Analytics is code binnen uw website, mobiele app of andere applicatie vereist om data naar servers voor dataverzameling te verzenden. Er zijn verschillende methoden om deze code te implementeren, afhankelijk van het platform en de behoeften van uw organisatie.

* **Adobe Experience Platform Launch:** De gestandaardiseerde en aanbevolen methode voor de implementatie van Adobe Analytics. Plaats een ladertag op elke pagina en gebruik de interface van Launch om te bepalen hoe elke variabele wordt gedefinieerd.
* **Dynamic Tag Management:** de voorloper van Launch. DTM gebruikt een soortgelijke interface om Analytics te implementeren, maar wordt niet meer bijgewerkt en is minder flexibel. Adobe raadt u aan Launch te gebruiken voor de implementatie van Adobe Analytics.
* **Verouderde JavaScript:** De oude handmatige methode voor de implementatie van Adobe Analytics. Geeft een overzicht van de variabelen en instellingen die in een implementatie worden gebruikt, wat handig kan zijn voor Launch-implementaties waarbij regels met aangepaste code worden gebruikt.
* **Mobile SDK:** speciale bibliotheken om data gemakkelijk vanuit uw mobiele app naar Adobe te verzenden.

## Belangrijke artikelen voor de implementatie van Analytics

* [Adobe-foutopsporing](validate/debugger.md)
* [Een eigenschap maken in Experience Platform Launch](launch/create-analytics-property.md)
* [AppMeasurement-updates](appmeasurement-updates.md)

## Meer Analytics-gebruikershandleidingen

[Analytics-gebruikershandleidingen](/help/landing/home.md)

## Belangrijke bronnen voor Analytics

* [Contact opnemen met de klantenservice](https://helpx.adobe.com/nl/contact/enterprise-support.ec.html)
* [Analytics-forum](https://forums.adobe.com/community/experience-cloud/analytics-cloud/analytics)
* [Bronnen voor Adobe Analytics](https://forums.adobe.com/message/10660755)
* [Experience League](https://landing.adobe.com/experience-league/)
