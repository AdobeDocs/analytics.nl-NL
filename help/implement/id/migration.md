---
title: Overwegingen voor migratie van bezoekersidentiteitsservice voor Adobe Analytics
description: Een overzicht van hoe Adobe Analytics met de Dienst van identiteitskaart van de Bezoeker omzet.
source-git-commit: f682f9c8533536e9b33f320f2a420055c6f4e397
workflow-type: tm+mt
source-wordcount: '617'
ht-degree: 0%

---

# Overwegingen voor migratie van bezoekersidentiteitsservice voor Adobe Analytics

Als uw organisatie van plan is om naar de Dienst van identiteitskaart van de Bezoeker met een bestaande implementatie van Analytics over te gaan, zijn er sommige belangrijke onderwerpen om te overwegen. Met deze overwegingen kunt u de integriteit van de bezoekersidentificatie behouden en begrijpen hoe de id-service werkt in aanwezigheid van een bestaande analytische implementatie.

>[!TIP]
>
>Deze pagina is alleen van toepassing op bestaande AppMeasurement- of Analytics-extensies en voegt de Bezoeker-id-service of -upgrade toe aan een Web SDK-implementatie. Met andere woorden, gebruikt uw implementatie een verouderde Analytics-id (`aid`) en gaat u verder naar het gebruik van een Experience Cloud-id (`mid` ). Alle implementaties van SDK van het Web gebruiken reeds Experience Cloud identiteitskaart (`mid`) door gebrek.

## Hoe de dienst van identiteitskaart van de Bezoeker met de koekjes van de bezoeker van de Verouderde Analyse omzet

Omdat AppMeasurement een eigen methode heeft om bezoekers te identificeren, hebben sommige bezoekers mogelijk verouderde Analytics-cookies wanneer een organisatie de Bezoeker-id-service implementeert. In de volgende lijst wordt beschreven hoe een bezoeker in verschillende omstandigheden wordt geïdentificeerd.

* **geen bezoekerskoekjes aanwezig**: De dienst van identiteitskaart wijst een identiteitskaart van Experience Cloud (`mid`) toe.
* **een `s_vi` koekje bestaat**: De dienst van identiteitskaart schrijft bestaande erfenisAnalytics identiteitskaart (`aid`) aan het `AMCV` koekje naast Experience Cloud identiteitskaart (`mid`). Aangezien `aid` hoger in de [&#x200B; Orde van verrichtingen &#x200B;](overview.md) is, is erfenis identiteitskaart van de Analyse identiteitskaart het bezoekersherkenningsteken tot het `AMCV` koekje verloopt of wordt ontruimd. Wanneer een respijtperiode is ingeschakeld, neemt de id-service zowel `mid` als `aid` op in de reactie.
* **A fallback koekje bestaat**: De dienst van identiteitskaart schrijft niet het fallback koekje (`fid`) aan het `AMCV` koekje. In plaats daarvan ontvangen bezoekers een Experience Cloud-id (`mid`) alsof ze een nieuwe bezoeker zijn.

## Abonnement voor service-ID van bezoeker

Als u meerdere implementaties hebt die gegevens naar dezelfde rapportsuite verzenden en u de Bezoeker-id-service op slechts enkele implementaties kunt implementeren, raadt Adobe aan een respijtperiode te configureren. Bijvoorbeeld, als de steunsectie van uw plaats door een afzonderlijke het etiketteren oplossing wordt beheerd, zou u de Dienst van identiteitskaart van de Bezoeker op de rest van uw plaats vóór de steunsectie kunnen hebben opgesteld. Zonder een respijtperiode ontvangen nieuwe bezoekers die de ondersteuningssectie bekijken een verouderde Analytics-bezoeker-id, waardoor twee aparte bezoekers worden geteld. Met een respijtperiode geeft de bezoeker-id-service zowel een Experience Cloud-id (`mid`) als een verouderde Analytics-bezoeker-id (`aid` ) uit, zodat gebieden van uw site zonder de id-service consistent blijven met het identificeren van bezoekers.

Als u de implementatie van de Bezoeker-id-service op alle gebieden van uw site coördineert, hebt u geen respijtperiode nodig. Om een respijtperiode te vormen, contacteer de [&#x200B; Zorg van de Klant van Adobe &#x200B;](https://helpx.adobe.com/nl/marketing-cloud/contact-support.html). De periodes van de SPRAAK kunnen tot 180 dagen worden gevormd, en kunnen worden vernieuwd. Adobe raadt aan de respijtperiode te beëindigen zodra uw volledige eigenschap is geconfigureerd voor gebruik van de ID-service.

## Interdomeinspatiëring

Bij sommige oudere implementaties van Analytics-bezoekers kan gebruik worden gemaakt van &#39;vriendelijke cookies van derden&#39;, waarbij twee domeinen dezelfde bezoekerscookie delen op een gemeenschappelijk domein, zoals `data.example.com` . Omdat cookies van derden die vriendelijk zijn, nog steeds cookies van derden zijn, wijzen veel moderne browsers deze af, waardoor Analytics voor de identificatie van bezoekers afhankelijk is van een fallback-id (`fid`). Als u naar de id-service gaat, kunnen alle domeinen het `AMCV` -cookie instellen in een context van een eerste partij, waardoor de betrokkenen gemakkelijker een bezoeker-id kunnen behouden.

Hoewel de Bezoeker-id-service probeert een cookie van een andere fabrikant in te stellen voor het bijhouden van meerdere domeinen (het [`demdex` cookie &#x200B;](https://experienceleague.adobe.com/nl/docs/id-service/using/intro/cookies) ), wordt dit cookie vaak afgewezen door moderne browsers. Overweeg het gebruiken van de [`appendVisitorIDsTo` &#x200B;](https://experienceleague.adobe.com/nl/docs/id-service/using/id-service-api/methods/appendvisitorid) methode om identiteitskaart van Experience Cloud van een bezoeker (`mid`) tussen domeinen over te gaan die u bezit.

## Volgen op de server

U kunt [`getMarketingCloudVisitorID` roepen &#x200B;](https://experienceleague.adobe.com/nl/docs/id-service/using/id-service-api/methods/getmcvid) om identiteitskaart van Experience Cloud (`mid`) en [`getAnalyticsVisitorID` te verkrijgen &#x200B;](https://experienceleague.adobe.com/nl/docs/id-service/using/id-service-api/methods/getanalyticsvisitorid) om erfenis identiteitskaart van de Analyse (`aid`) te verkrijgen. Adobe raadt aan beide te controleren om de logica voor de identificatie van bezoekers te behouden.
