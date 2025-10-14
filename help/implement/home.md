---
title: Adobe Analytics implementeren
description: Implementeer Adobe Analytics op uw website, eigenschap of applicatie.
feature: Implementation Basics
exl-id: 2b629369-2d69-4dc6-861a-ff21a46d39e0
role: Admin, Developer, Leader, User
source-git-commit: 8e701a3da6f04ccf2d7ac3abd10c6df86feb00a7
workflow-type: tm+mt
source-wordcount: '755'
ht-degree: 9%

---

# Adobe Analytics implementeren

![Banner](../../assets/doc_banner_implement.png)

Voor Adobe Analytics is code binnen uw website, mobiele app of andere applicatie vereist om data naar servers voor dataverzameling te verzenden. Er zijn verschillende methoden om deze code te implementeren, afhankelijk van het platform en de behoeften van uw organisatie.

## Implementatiemethoden voor websites

Voor uw **website**, zijn de volgende implementatiemethodes beschikbaar:

### Client-kant

* **uitbreiding van SDK van het Web**: De gestandaardiseerde en geadviseerde methode om Adobe Analytics voor nieuwe klanten uit te voeren. Voeg de **uitbreiding van SDK van het Web van Adobe Experience Platform** in de Codes van de Inzameling van de Gegevens van Adobe Experience Platform **&#x200B;**&#x200B;toe, dan plaats een ladersmarkering op elke pagina. De markering verzendt gegevens naar Adobe Experience Platform **Edge Network**, die die gegevens aan Adobe Analytics door:sturen.
  ![&#x200B; de uitbreiding van SDK van het Web &#x200B;](./assets/websdk-extension-implementation.png)
Zie [&#x200B; hoe te om Adobe Analytics uit te voeren gebruikend de uitbreiding van SDK van het Web van Adobe Experience Platform.](./aep-edge/overview.md) voor meer informatie.

* **SDK van het Web**: U kunt de bibliotheken van SDK van het Web op uw plaats manueel laden als u de Inzameling van Gegevens van Adobe Experience Platform niet wilt gebruiken. Verwijs de bibliotheek van SDK van het Web (`alloy.js`) op elke pagina, en verzend de gewenste het volgen vraag aan Adobe Experience Platform **Edge Network** in een formaat geschikt aan uw organisatie. De Edge Network stuurt die gegevens door naar Adobe Analytics.
  ![&#x200B; SDK van het Web &#x200B;](./assets/websdk-implementation.png)
Zie [&#x200B; hoe te om Adobe Analytics uit te voeren gebruikend SDK van het Web van Adobe Experience Platform &#x200B;](./aep-edge/overview.md) voor meer informatie.

* **uitbreiding van de Analyse**: Voeg de **uitbreiding van Adobe Analytics** in de Codes van de Inzameling van de Gegevens van Adobe Experience Platform **toe**, dan plaats een ladersmarkering op elke pagina. De tag verzendt de gegevens rechtstreeks naar Adobe Analytics. Gebruik deze implementatiemethode als u het gemak van tags wilt gebruiken, maar de Edge Network-infrastructuur niet wilt gebruiken.
  ![&#x200B; de uitbreiding van Adobe Analytics &#x200B;](./assets/analytics-extension-implementation.png)
Zie [&#x200B; hoe te om Adobe Analytics uit te voeren gebruikend de uitbreiding van Analytics &#x200B;](launch/overview.md) voor meer informatie.

* **Verouderde JavaScript:** De oude handmatige methode voor de implementatie van Adobe Analytics. Verwijs naar de AppMeasurement-bibliotheek (`AppMeasurement.js`) op elke pagina en stel vervolgens variabelen en instellingen in JavaScript in.
  ![&#x200B; hoe te om Adobe Analytics uit te voeren gebruikend Verouderde JavaScript &#x200B;](./assets/appmeasurement-implementation.png)
Deze implementatiemethode kan voor implementaties nuttig zijn gebruikend douanecode en is ideaal voor implementatietypen niet elders, zoals voor [&#x200B; AMP pagina&#39;s &#x200B;](other/amp.md) worden aangeboden.

De volgende beslissingsstroom kan u helpen een client-side implementatiemethode selecteren:

![&#x200B; de beslissingsboom van A voor het selecteren van een implementatiemethode, zoals die in deze sectie wordt beschreven.](./assets/decision-tree.png)


>[!TIP]
>
>Neem contact op met uw Adobe-accountteam voor advies en aanbevolen procedures voor de keuze van de implementatie op basis van uw huidige situatie.

### Server-kant

Voor het implementeren van de Adobe Analytics-server hebt u de volgende opties:

* **Edge Network API**: U voert code op de server uit die Adobe Experience Platform Edge Network API gebruikt om met Adobe Analytics door een datastream te communiceren.
  ![&#x200B; Server-kant implementatie &#x200B;](assets/edge-network-server-api.svg)
Zie [&#x200B; Adobe Analytics uitvoeren gebruikend Adobe Experience Platform Edge Network API &#x200B;](/help/implement/aep-edge/api/overview.md) voor meer informatie.

* **(Bulk) API voor het invoegen van gegevens**: u gebruikt de API&#39;s voor het invoegen van gegevens in Adobe Analytics (Bulk) om gegevens rechtstreeks in Adobe Analytics te verzamelen op de server.
  ![&#x200B; de Invoeging APIs van Gegevens &#x200B;](assets/analytics-apis.png)
Zie [&#x200B; de Invoeging API van Gegevens &#x200B;](../import/c-data-insertion-api/c-data-insertion-api.md) voor meer informatie.

## Implementatiemethoden voor mobiele apps

Voor uw **mobiele app**, zijn de volgende implementatiemethodes beschikbaar:

* **Mobiele uitbreiding van SDK**: De gestandaardiseerde en geadviseerde methode om Adobe Analytics in uw mobiele app uit te voeren. Gebruik speciale bibliotheken om gegevens vanuit uw mobiele app gemakkelijk naar Adobe te verzenden. Voeg de **Adobe Experience Platform Mobile SDK uitbreiding** in de Codes van de Inzameling van de Gegevens van Adobe Experience Platform **&#x200B;**&#x200B;toe, dan voer de Mobiele bibliotheek van SDK in uw app uit. Met de SDK kunt u bibliotheken importeren, extensies registreren en de tagconfiguratie laden. Verzend gegevens naar Adobe Experience Platform **Edge Network**; Edge dan door:sturen die gegevens aan Adobe Analytics.
  ![&#x200B; Mobiele uitbreiding van SDK &#x200B;](./assets/mobilesdk-extension.png)

  Zie [&#x200B; Adobe Analytics uitvoeren gebruikend Adobe Experience Platform Mobile SDK &#x200B;](../implement/aep-edge/mobile-sdk/overview.md) voor meer informatie.

* **uitbreiding van Analytics**: Voeg de **uitbreiding van Adobe Analytics** in de Inzameling van Gegevens van Adobe Experience Platform **Codes** toe, en voer de Mobiele bibliotheek van SDK in uw app uit. Met de SDK kunt u bibliotheken importeren, extensies registreren en de tagconfiguratie laden. Deze implementatiemethode verzendt gegevens rechtstreeks naar Adobe Analytics. Het wordt aanbevolen om het gebruiksgemak van Adobe Experience Platform Data Collection te gebruiken, maar niet om Adobe Experience Platform Edge netwerkinfrastructuur te gebruiken.
  ![&#x200B; uitbreiding Analytics &#x200B;](./assets/mobilesdk-analytics-extension.png)

  Zie [&#x200B; Adobe Analytics uitvoeren gebruikend de uitbreiding van Analytics &#x200B;](../implement/aep-edge/mobile-sdk/overview.md) voor meer informatie.


>[!CAUTION]
>
>Zie voor steun voor oudere versies van Adobe mobiele SDKs de [&#x200B; eind-van-steun aankondigingen SDKs &#x200B;](https://developer.adobe.com/client-sdks/resources/sdks-end-of-support/).

## Belangrijke artikelen voor de implementatie van Analytics

* [Een bestaande Adobe Analytics-implementatie op zich nemen](/help/implement/prepare/existing-implementation.md)
* [Adobe Debugger](validate/debugger.md)
* [Een tag-eigenschap maken in Experience Platform](launch/create-analytics-property.md)
* [AppMeasurement-updates](appmeasurement-updates.md)
* [&#x200B; Opstelling Adobe Analytics met de zelfstudie van SDK van het Web van het Platform &#x200B;](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/applications-setup/setup-analytics.html?lang=nl-NL)
* [&#x200B; voer Adobe Experience Cloud in mobiele apps leerprogramma uit &#x200B;](https://experienceleague.adobe.com/docs/platform-learn/implement-mobile-sdk/overview.html?lang=nl-NL)


## Belangrijke bronnen voor Analytics

* [Contact opnemen met de klantenservice](https://experienceleague.adobe.com/nl?support-solution=Analytics&lang=nl#support)
* [&#x200B; Gemeenschap van Adobe Analytics op Experience League &#x200B;](https://experienceleaguecommunities.adobe.com/t5/adobe-analytics/ct-p/adobe-analytics-community)
* [Bronnen voor Adobe Analytics](https://experienceleaguecommunities.adobe.com/t5/adobe-analytics-discussions/adobe-analytics-resources/m-p/276666)
* [Opmerkingen bij de laatste release](../release-notes/latest.md)
