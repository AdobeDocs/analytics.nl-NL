---
title: trackingServerSecure
description: Bepaal de locatie waar afbeeldingsaanvragen worden verzonden op HTTPS-pagina's.
feature: Appmeasurement Implementation
exl-id: d5b112f9-f3f6-43ac-8ee5-d9ad8062e380
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '408'
ht-degree: 0%

---

# trackingServerSecure

Adobe verzamelt gegevens op uw site door een afbeeldingsaanvraag te ontvangen die door de bezoeker is gegenereerd. De variabele `trackingServerSecure` bepaalt de locatie waar een afbeeldingsaanvraag via HTTPS wordt verzonden. Het bepaalt ook welke cookies van de locatiebezoeker worden opgeslagen. Als deze variabele niet correct wordt gedefinieerd, kan uw implementatie gegevensverlies ervaren.

>[!WARNING]
>
>Als u deze waarde wijzigt, zoekt AppMeasurement naar cookies op een andere locatie. Het unieke aantal bezoekers kan tijdelijk in de rapportage springen, omdat bezoekerscookies op de nieuwe locatie worden ingesteld.

## Edge-domein met de extensie Web SDK

Het Web SDK gebruikt [!UICONTROL Edge domain] om zowel de het Volgen Server als Veilige het Volgen Server te behandelen. U kunt de gewenste [!UICONTROL Edge domain] -waarde instellen wanneer u de extensie Web SDK configureert.

1. Login aan [ de Inzameling van Gegevens van Adobe Experience Platform ](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
1. Klik op de gewenste tageigenschap.
1. Ga naar de tab [!UICONTROL Extensions] en klik vervolgens op de knop **[!UICONTROL Configure]** onder [!UICONTROL Adobe Experience Platform Web SDK] .
1. Stel het gewenste tekstveld in **[!UICONTROL Edge domain]** .

Zie [ de uitbreiding van SDK van het Web van Adobe Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/edge/extension/web-sdk-extension-configuration.html?lang=nl-NL) in de documentatie van SDK van het Web voor meer informatie vormen.

>[!TIP]
>
>Als uw organisatie vanuit een AppMeasurement- of analytische extensie-implementatie naar de Web SDK gaat, kan voor dit veld dezelfde waarde worden gebruikt als in `trackingServerSecure` (of `trackingServer` ).

## Edge-domein handmatig implementeren van de Web SDK

Vorm SDK gebruikend [`edgeDomain` ](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html?lang=nl-NL). Het veld is een tekenreeks die het domein bepaalt waarnaar gegevens moeten worden verzonden.

```json
alloy("configure", {
  "edgeDomain": "data.example.com"
});
```

## SSL-traceringsserver met de Adobe Analytics-extensie

[!UICONTROL SSL Tracking Server] is een veld onder de accordeon van [!UICONTROL General] wanneer u de Adobe Analytics-extensie configureert.

1. Login aan [ de Inzameling van Gegevens van Adobe Experience Platform ](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
2. Klik op de gewenste tageigenschap.
3. Ga naar de tab [!UICONTROL Extensions] en klik vervolgens op de knop **[!UICONTROL Configure]** onder Adobe Analytics.
4. Vouw de accordeon [!UICONTROL General] uit, zodat het veld [!UICONTROL SSL Tracking Server] zichtbaar wordt.

Als dit veld niet wordt ingevuld, wordt standaard de waarde in de variabele [`trackingServer`](trackingserver.md) gebruikt.

## s.trackingServerSecure in AppMeasurement en de aangepaste code-editor voor de extensie Analytics

De variabele `s.trackingServerSecure` is een tekenreeks die de locatie bevat waar verzoeken om afbeeldingen moeten worden verzonden. Het is bijna altijd een subdomein van uw site. De moderne privacy praktijken in browsers maken over het algemeen derde koekjes onbetrouwbaar. Als deze variabele leeg is, wordt de waarde in de variabele `s.trackingServer` gebruikt.

De waarde voor deze variabele is bijna altijd een domein van de eerste partij, zoals `data.example.com`. Zie [ Eerste partijkoekjes in Experience Cloud ](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-first-party.html?lang=nl-NL) in de de gebruikersgids van de Diensten van de Kern voor meer informatie over het proces van het eerste-partijkoekje.

De individu die aanvankelijk de first-party koekjesimplementatie vormt bepaalt ook het domein en subdomain gebruikte. Bijvoorbeeld:

```js
s.trackingServerSecure = "data.example.com";
```

CNAME-records verwijzen doorgaans naar een subdomein op `data.adobedc.net` , `sc.adobedc.net` of `2o7.net` .
