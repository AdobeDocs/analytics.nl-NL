---
title: trackingServer
description: Bepaal de locatie waarnaar verzoeken voor de afbeelding worden verzonden.
feature: Variables
exl-id: bcc23286-4dd5-45ac-ac6f-7b60e95cb798
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '543'
ht-degree: 1%

---

# trackingServer

Adobe verzamelt gegevens op uw site door een afbeeldingsaanvraag te ontvangen die door de bezoeker is gegenereerd. De `trackingServer` De variabele bepaalt de locatie die een afbeeldingsaanvraag wordt verzonden. Als deze variabele niet correct wordt gedefinieerd, kan uw implementatie gegevensverlies ervaren.

>[!WARNING]
>
>Als u deze waarde wijzigt, zoekt AppMeasurement naar cookies op een andere locatie. Het unieke aantal bezoekers kan tijdelijk in de rapportage springen, omdat bezoekerscookies op de nieuwe locatie worden ingesteld.

## Het domein van de rand die de uitbreiding van SDK van het Web gebruikt

Het gebruik van Web SDK [!UICONTROL Edge domain] om zowel Tracking Server als Secure Tracking Server te verwerken. U kunt het gewenste [!UICONTROL Edge domain] waarde wanneer het vormen van de uitbreiding van SDK van het Web.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de gewenste tageigenschap.
1. Ga naar de [!UICONTROL Extensions] en klikt u op de knop **[!UICONTROL Configure]** knop onder [!UICONTROL Adobe Experience Platform Web SDK].
1. Stel het gewenste **[!UICONTROL Edge domain]** tekstveld.

Zie [De extensie Adobe Experience Platform Web SDK configureren](https://experienceleague.adobe.com/docs/experience-platform/edge/extension/web-sdk-extension-configuration.html) in de documentatie van SDK van het Web voor meer informatie.

>[!TIP]
>
>Als uw organisatie zich van een AppMeasurement of de uitbreiding van Analytics aan SDK van het Web beweegt, kan dit gebied de zelfde waarde gebruiken bevat `trackingServerSecure` (of `trackingServer`).

## Het domein van de rand voert manueel het Web SDK uit

De SDK configureren met [`edgeDomain`](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html). Het veld is een tekenreeks die het domein bepaalt waarnaar gegevens moeten worden verzonden.

```json
alloy("configure", {
  "edgeDomain": "data.example.com"
});
```

## Trackingserver met de Adobe Analytics-extensie

De volgende Server is een gebied onder het [!UICONTROL General] accordeon bij het configureren van de Adobe Analytics-extensie.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste tageigenschap.
3. Ga naar de [!UICONTROL Extensions] en klikt u op de knop **[!UICONTROL Configure]** onder Adobe Analytics.
4. Breid uit [!UICONTROL General] accordion, die de [!UICONTROL Tracking Server] veld.

Als dit veld niet wordt ingevuld, wordt standaard ingesteld op `[rsid].data.adobedc.net`.

## s.trackingServer in AppMeturement en de de coderedacteur van de de uitbreidingsuitbreiding van de Analyse

De `s.trackingServer` variable is a string that contains the location to send data.

## De waarde bepalen voor `trackingServer`

De waarde voor deze variabele is afhankelijk van het gebruik van cookies van andere bedrijven of van cookies van andere bedrijven. Adobe raadt u ten zeerste aan cookies van de eerste fabrikant te gebruiken in uw implementatie.

### Cookies van eerste bedrijven

Als u een first-party koekjesimplementatie gebruikt, is het waarschijnlijk dat iemand in uw organisatie reeds het eerste-partijkoekjesproces heeft voltooid. Zie [Eerste cookies in de Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-first-party.html) in de de gebruikersgids van de Diensten van de Kern voor meer informatie over het eerste-partijkoekjesproces.

De individu die aanvankelijk de first-party koekjesimplementatie vormt bepaalt ook het domein en subdomain gebruikte. Bijvoorbeeld:

```js
s.trackingServer = "data.example.com";
```

### Cookies van andere bedrijven

>[!TIP]
>
>De toenemende privacy praktijken in moderne browsers maken derdekoekjes minder betrouwbaar. Adobe raadt u aan de cookie-workflow van de eerste fabrikant te volgen.

Als u een cookie-implementatie van een andere fabrikant gebruikt, moet u de waarde voor `trackingServer` is een subdomein van `data.adobedc.net`. Bijvoorbeeld:

```js
s.trackingServer = "example.data.adobedc.net";
```

Kies een subdomein dat uniek is voor uw organisatie. Het is onwaarschijnlijk dat het wordt gekozen door een andere organisatie die Adobe Analytics gebruikt.  De aan uw organisatie toegewezen naamruimte voor bezoekers wordt aanbevolen.  Zorg ervoor dat alle implementaties in uw organisatie dezelfde trackingserver gebruiken. Het kan nuttig zijn deze informatie in een [document ontwerp oplossing](../../prepare/solution-design.md).

Uw organisatie gebruikt mogelijk al een trackingserver van derden in de `sc.omtrdc.net` of `2o7.net` domeinen.  Deze werden voornamelijk gebruikt in eerdere versies van Adobe Analytics en zijn nog steeds geldig.

>[!NOTE]
>
>Gebruik geen subdomeinen die dieper zijn dan `example.data.adobedc.net`. Bijvoorbeeld: `custom.example.data.adobedc.net` is geen geldige trackingserver.
