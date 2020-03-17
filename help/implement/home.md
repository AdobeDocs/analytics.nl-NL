---
title: Adobe Analytics implementeren
description: Voer Adobe Analytics op uw plaats, bezit, of toepassing uit.
translation-type: tm+mt
source-git-commit: 8a090574a6822a76366343ad5c657280bf7475eb

---


# Adobe Analytics implementeren

![Banner](../../assets/doc_banner_implement.png)

Adobe heeft code op uw site of toepassing nodig om gegevens naar de gegevensverzamelingsservers van Adobe te verzenden. De volgende stappen geven aan hoe een standaardimplementatie werkt.

1. Wanneer een bezoeker naar uw site komt, wordt een aanvraag ingediend bij uw webserver.
2. De webserver van uw site verzendt de informatie over de paginacode en de pagina wordt weergegeven in de browser.
3. De pagina wordt geladen en de JavaScript-code Analytics wordt uitgevoerd.
De JavaScript-code verzendt een Adobe-gegevensverzamelingsserver voor een afbeeldingsaanvraag. De paginagegevens die u in uw implementatie hebt gedefinieerd, worden verzonden als onderdeel van een queryreeks in deze afbeeldingsaanvraag.

4. Adobe retourneert een transparante pixelafbeelding.
5. Adobe-servers slaan verzamelde gegevens op in een *rapportsuite*.
6. De gegevens van de rapportsuite vullen de rapporten die u in Webbrowser kunt openen.

   De uitvoering van de JavaScript-code vindt snel plaats en heeft geen merkbare invloed op de laadtijden van de pagina. Op deze manier kunt u pagina&#39;s tellen die werden weergegeven wanneer een bezoeker op een pagina klikt **[!UICONTROL Reload]** **[!UICONTROL Back]** of die een pagina bereiken, omdat de JavaScript-code wordt uitgevoerd, zelfs wanneer de pagina uit de cache wordt opgehaald.

Adobe Analytics vereist code binnen uw website, mobiele app of andere toepassing om gegevens naar servers voor gegevensverzameling te verzenden. Er zijn verschillende methoden om deze code te implementeren, afhankelijk van het platform en de behoeften van uw organisatie.

* **Start** Adobe Experience Platform: De gestandaardiseerde en aanbevolen methode voor het implementeren van Adobe Analytics. Plaats een ladertag op elke pagina en gebruik de interface van Launch om te bepalen hoe elke variabele wordt gedefinieerd.
* **Dynamisch tagbeheer**: De voorganger die moet worden gestart. DTM gebruikt een gelijkaardige interface om Analytics uit te voeren, maar niet meer bijgewerkt en niet zo flexibel is. Adobe raadt u aan Launch te gebruiken voor de implementatie van Adobe Analytics.
* **Oudere JavaScript**: De historische handmatige methode voor het implementeren van Adobe Analytics. Omlijnt variabelen en montages die in een implementatie worden gebruikt, die voor de implementaties van de Lancering kunnen nuttig zijn gebruikend regels met douanecode.
* **Mobile SDK**: Speciale bibliotheken die gegevens gemakkelijk vanuit uw mobiele app naar Adobe kunnen verzenden.

## Belangrijke artikelen voor analysetransplementatie

* [Adobe Debugger](validate/debugger.md)
* [Een eigenschap maken in Launch van Experience Platform](launch/create-analytics-property.md)
* [AppMeasurement-updates](appmeasurement-updates.md)

## Meer gebruikershandleidingen voor Analytics

[Gebruikershandleidingen voor Analytics](/help/landing/home.md)

## Belangrijke bronnen voor analyse

* [Contact opnemen met de klantenservice](https://helpx.adobe.com/contact/enterprise-support.ec.html)
* [Analysereforum](https://forums.adobe.com/community/experience-cloud/analytics-cloud/analytics)
* [Bronnen voor Adobe Analytics](https://forums.adobe.com/message/10660755)
* [Experience League](https://landing.adobe.com/experience-league/)
