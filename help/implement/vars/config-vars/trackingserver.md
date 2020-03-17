---
title: trackingServer
description: Bepaal de locatie waarnaar verzoeken voor de afbeelding worden verzonden.
translation-type: tm+mt
source-git-commit: 979a95ca749a3e21c4ddf48ba2d2a95672938a20

---


# trackingServer

Adobe verzamelt gegevens op uw site door een afbeeldingsaanvraag te ontvangen die door de bezoeker is gegenereerd. De `trackingServer` variabele bepaalt de locatie die een afbeeldingsaanvraag wordt verzonden. Als deze variabele niet correct wordt gedefinieerd, kan uw implementatie gegevensverlies ervaren.

> [!IMPORTANT] Als u deze waarde wijzigt, zoekt AppMeasurement naar cookies op een andere locatie. Het unieke aantal bezoekers kan tijdelijk in de rapportage springen, omdat bezoekerscookies op de nieuwe locatie worden ingesteld.

## Trackingserver in Adobe Experience Platform Launch

Trackingserver is een veld onder de [!UICONTROL General] accordeon tijdens het configureren van de extensie Adobe Analytics.

1. Meld u aan bij [launch.adobe.com](https://launch.adobe.com) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Extensions] tabblad en klik vervolgens op de [!UICONTROL Configure] knop onder Adobe Analytics.
4. Breid de accordeon uit, die het [!UICONTROL General] [!UICONTROL Tracking Server] veld onthult.

Als dit veld niet wordt ingevuld, wordt standaard ingesteld op `[rsid].112.2o7.net`.

## s.trackingServer in de aangepaste code-editor van AppMeasurement en Launch

De `s.trackingServer` variabele is een tekenreeks die de locatie bevat waar gegevens moeten worden verzonden.

> [!TIP] Sommige implementaties wijzen gegevens aan `2o7.net`. Hoewel dit een geldig domein voor gegevensverzameling is, wordt geen regionale gegevensverzameling gebruikt. Implementaties die gebruikmaken van `2o7.net` zie iets hogere responstijden voor verzoeken om afbeeldingen.

## De waarde voor trackingServer bepalen

De waarde voor deze variabele is afhankelijk van het gebruik van cookies van andere bedrijven of van cookies van andere bedrijven. Adobe raadt u ten zeerste aan cookies van de eerste fabrikant in uw implementatie te gebruiken.

### Cookies van eerste bedrijven

Als u een first-party koekjesimplementatie gebruikt, is het waarschijnlijk dat iemand in uw organisatie reeds het eerste-partijkoekjesproces heeft voltooid. Zie [First-party cookies in de Experience Cloud](https://docs.adobe.com/content/help/en/core-services/interface/ec-cookies/cookies-first-party.html) in de gebruikershandleiding voor Core Services voor meer informatie over het cookie-proces van de eerste partij.

De individu die aanvankelijk de first-party koekjesimplementatie vormt bepaalt ook het domein en subdomain gebruikte. Bijvoorbeeld:

```js
s.trackingServer = "data.example.com";
```

CNAME-records zijn meestal al ingesteld en wijzen ernaar `sc.omtrdc.net`. Het domein `2o7.net` is ook een geldige CNAME-bestemming, vooral gebruikt in eerdere versies van Adobe Analytics.

### Cookies van andere bedrijven

> [!TIP] De toenemende privacy praktijken in moderne browsers maken derdekoekjes minder betrouwbaar. Adobe raadt u aan de cookie-workflow van de eerste fabrikant te volgen.

Als u een cookie-implementatie van een andere fabrikant gebruikt, `trackingServer` is de waarde voor een subdomein van `sc.omtrdc.net`. Bijvoorbeeld:

```js
s.trackingServer = "example.sc.omtrdc.net";
```

Kies een subdomein dat uniek is voor uw organisatie en dat waarschijnlijk niet door een andere organisatie wordt gekozen die Adobe Analytics gebruikt. Zorg ervoor dat alle implementaties in uw organisatie dezelfde trackingserver gebruiken. Het kan nuttig zijn om deze informatie in een document [van het](../../prepare/solution-design.md)oplossingsontwerp te handhaven.
