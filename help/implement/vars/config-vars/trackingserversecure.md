---
title: trackingServerSecure
description: Bepaal de locatie waar afbeeldingsaanvragen worden verzonden op HTTPS-pagina's.
feature: Variables
exl-id: d5b112f9-f3f6-43ac-8ee5-d9ad8062e380
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '408'
ht-degree: 0%

---

# trackingServerSecure

Adobe verzamelt gegevens op uw site door een afbeeldingsaanvraag te ontvangen die door de bezoeker is gegenereerd. De `trackingServerSecure` De variabele bepaalt de locatie die een afbeeldingsaanvraag via HTTPS wordt verzonden. Het bepaalt ook welke cookies van de locatiebezoeker worden opgeslagen. Als deze variabele niet correct wordt gedefinieerd, kan uw implementatie gegevensverlies ervaren.

>[!WARNING]
>
>Als u deze waarde wijzigt, zoekt het AppMeasurement naar cookies op een andere locatie. Het unieke aantal bezoekers kan tijdelijk in de rapportage springen, omdat bezoekerscookies op de nieuwe locatie worden ingesteld.

## Het domein van de rand die de uitbreiding van SDK van het Web gebruikt

Het gebruik van Web SDK [!UICONTROL Edge domain] om zowel Tracking Server als Secure Tracking Server te verwerken. U kunt het gewenste [!UICONTROL Edge domain] waarde wanneer het vormen van de uitbreiding van SDK van het Web.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de gewenste tageigenschap.
1. Ga naar de [!UICONTROL Extensions] en klikt u op de knop **[!UICONTROL Configure]** knop onder [!UICONTROL Adobe Experience Platform Web SDK].
1. Stel het gewenste **[!UICONTROL Edge domain]** tekstveld.

Zie [De extensie Adobe Experience Platform Web SDK configureren](https://experienceleague.adobe.com/docs/experience-platform/edge/extension/web-sdk-extension-configuration.html?lang=nl-NL) in de documentatie van SDK van het Web voor meer informatie.

>[!TIP]
>
>Als uw organisatie zich van een AppMeasurement of de de uitbreidingsimplementatie van Analytics aan SDK van het Web beweegt, kan dit gebied de zelfde waarde gebruiken bevat in `trackingServerSecure` (of `trackingServer`).

## Het domein van de rand voert manueel de SDK van het Web uit

De SDK configureren met [`edgeDomain`](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html?lang=nl-NL). Het veld is een tekenreeks die het domein bepaalt waarnaar gegevens moeten worden verzonden.

```json
alloy("configure", {
  "edgeDomain": "data.example.com"
});
```

## SSL-traceringsserver met de Adobe Analytics-extensie

[!UICONTROL SSL Tracking Server] is een veld onder de [!UICONTROL General] accordeon bij het configureren van de Adobe Analytics-extensie.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste tageigenschap.
3. Ga naar de [!UICONTROL Extensions] en klikt u op de knop **[!UICONTROL Configure]** onder Adobe Analytics.
4. Breid uit [!UICONTROL General] accordion, die de [!UICONTROL SSL Tracking Server] veld.

Als dit veld niet wordt ingevuld, wordt standaard de waarde in het dialoogvenster [`trackingServer`](trackingserver.md) variabele.

## s.trackingServerSecure in AppMeasurement en de aangepaste code-editor voor de extensie Analytics

De `s.trackingServerSecure` variabele is een tekenreeks die de locatie bevat waar verzoeken om afbeeldingen moeten worden verzonden. Het is bijna altijd een subdomein van uw site. De moderne privacy praktijken in browsers maken over het algemeen derde koekjes onbetrouwbaar. Als deze variabele leeg is, wordt de waarde in het dialoogvenster `s.trackingServer` variabele.

De waarde voor deze variabele is bijna altijd een domein van de eerste partij, zoals `data.example.com`. Zie [Eerste cookies in het Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-first-party.html?lang=nl-NL) in de de gebruikersgids van de Diensten van de Kern voor meer informatie over het eerste-partijkoekjesproces.

De individu die aanvankelijk de first-party koekjesimplementatie vormt bepaalt ook het domein en subdomain gebruikte. Bijvoorbeeld:

```js
s.trackingServerSecure = "data.example.com";
```

CNAME-records wijzen doorgaans naar een subdomein op `data.adobedc.net`, `sc.adobedc.net` of `2o7.net`.
