---
title: Adobe Analytics implementeren
description: Implementeer Adobe Analytics op uw website, eigenschap of applicatie.
feature: Implementation Basics
exl-id: 2b629369-2d69-4dc6-861a-ff21a46d39e0
source-git-commit: d2c291f7db465034ffadc4a2c1caf9639caf2a1d
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 44%

---

# Adobe Analytics implementeren

![Banner](../../assets/doc_banner_implement.png)

Hier volgt een video-overzicht van Adobe Analytics:

>[!VIDEO](https://video.tv.adobe.com/v/27429/?quality=12)

Voor Adobe is code op uw site of applicatie vereist om data naar de servers voor dataverzameling van Adobe te verzenden. De volgende stappen geven aan hoe een normale implementatie werkt.

1. Wanneer een bezoeker naar uw site komt, wordt een aanvraag ingediend bij uw webserver.
2. De webserver van uw site verzendt de paginacodegegevens en de pagina wordt weergegeven in de browser.
3. De pagina wordt geladen en de Analytics JavaScript-code wordt uitgevoerd.
4. De JavaScript-code verzendt een afbeeldingsaanvraag van 1 x 1 pixel naar Adobe-gegevensverzamelingsservers. De paginadata die u in uw implementatie hebt gedefinieerd, worden verzonden als onderdeel van een querytekenreeks in deze afbeeldingsaanvraag.
5. Adobe-verzamelingsservers retourneren de gevraagde afbeelding.
6. Adobe servers parseren en slaan verzamelde gegevens op in een rapportsuite.
7. De data van de rapportsuite worden ingevuld in rapporten die u in een webbrowser kunt openen.


Adobe biedt verschillende methoden om deze code te implementeren, afhankelijk van het platform en de behoeften van uw organisatie.

* **Web SDK-extensie**: De huidige, gestandaardiseerde en aanbevolen methode voor het implementeren van Adobe Analytics. Installeer de SDK-extensie van het Web in de gegevensverzameling van Adobe Experience Platform, gebruik een loader-tag op elke pagina en verzend gegevens naar Adobe Experience Platform Edge in een voor uw organisatie geschikte indeling. Experience Edge stuurt binnenkomende gegevens door naar Adobe Analytics in de juiste indeling.
* **Web SDK**: U kunt de bibliotheken van SDK van het Web op uw plaats manueel laden als u geen Markeringen wilt gebruiken. Verwijs naar de bibliotheek van SDK van het Web op elke pagina, en verzend de gewenste het volgen vraag aan de Rand van de Ervaring van Adobe.
* **Adobe Analytics-extensie**: Installeer de extensie Adobe Analytics in Adobe Experience Platform Data Collection. Plaats een loader-tag op elke pagina en gebruik de extensie Analytics om te bepalen hoe elke variabele wordt gedefinieerd.
* **Verouderde JavaScript:** De oude handmatige methode voor de implementatie van Adobe Analytics. Omlijnt variabelen en montages die in een implementatie worden gebruikt, die voor implementaties kunnen nuttig zijn gebruikend regels met douanecode.
* **Mobile SDK:** speciale bibliotheken om data gemakkelijk vanuit uw mobiele app naar Adobe te verzenden.

## Belangrijke artikelen voor de implementatie van Analytics

* [Een bestaande Adobe Analytics-implementatie op zich nemen](/help/implement/prepare/existing-implementation.md)
* [Adobe-foutopsporing](validate/debugger.md)
* [Een tag-eigenschap maken in Experience Platform](launch/create-analytics-property.md)
* [AppMeasurement-updates](appmeasurement-updates.md)

## Meer Analytics-gebruikershandleidingen

[Analytics-gebruikershandleidingen](https://experienceleague.adobe.com/docs/analytics.html)

## Belangrijke bronnen voor Analytics

* [Contact opnemen met de klantenservice](https://experienceleague.adobe.com/?support-solution=Analytics#support)
* [Analytics-forum](https://forums.adobe.com/community/experience-cloud/analytics-cloud/analytics)
* [Bronnen voor Adobe Analytics](https://forums.adobe.com/message/10660755)
* [Experience League](https://landing.adobe.com/experience-league/)
