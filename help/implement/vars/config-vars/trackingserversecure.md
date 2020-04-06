---
title: trackingServerSecure
description: Bepaal de locatie waar afbeeldingsaanvragen worden verzonden op HTTPS-pagina's.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# trackingServerSecure

Adobe verzamelt gegevens op uw site door een afbeeldingsaanvraag te ontvangen die door de bezoeker is gegenereerd. De `trackingServerSecure` variabele bepaalt de locatie waar een afbeeldingsaanvraag via HTTPS wordt verzonden. Het bepaalt ook welke cookies van de locatiebezoeker worden opgeslagen. Als deze variabele niet correct wordt gedefinieerd, kan uw implementatie gegevensverlies ervaren.

>[!IMPORTANT] Als u deze waarde wijzigt, zoekt AppMeasurement naar cookies op een andere locatie. Het unieke aantal bezoekers kan tijdelijk in de rapportage springen, omdat bezoekerscookies op de nieuwe locatie worden ingesteld.

## SSL-traceringsserver in Adobe Experience Platform Launch

[!UICONTROL SSL Tracking Server] is een veld onder de [!UICONTROL General] accordeon wanneer u de extensie Adobe Analytics configureert.

1. Meld u aan bij [launch.adobe.com](https://launch.adobe.com) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Extensions] tabblad en klik vervolgens op de [!UICONTROL Configure] knop onder Adobe Analytics.
4. Breid de accordeon uit, die het [!UICONTROL General] [!UICONTROL SSL Tracking Server] veld onthult.

Als dit veld niet wordt ingevuld, wordt standaard de waarde in de [`trackingServer`](trackingserver.md) variabele gebruikt.

## s.trackingServerSecure in de aangepaste code-editor van AppMeasurement en Launch

De `s.trackingServerSecure` variabele is een tekenreeks die de locatie bevat waar verzoeken om afbeeldingen moeten worden verzonden. Het is bijna altijd een subdomein van uw site. De moderne privacy praktijken in browsers maken over het algemeen derde koekjes onbetrouwbaar. Als deze variabele leeg is, wordt de waarde in de `s.trackingServer` variabele gebruikt.

De waarde voor deze variabele is bijna altijd een domein van de eerste partij, zoals `data.example.com`. Zie [First-party cookies in de Experience Cloud](https://docs.adobe.com/content/help/en/core-services/interface/ec-cookies/cookies-first-party.html) in de gebruikershandleiding voor Core Services voor meer informatie over het cookie-proces van de eerste partij.

De individu die aanvankelijk de first-party koekjesimplementatie vormt bepaalt ook het domein en subdomain gebruikte. Bijvoorbeeld:

```js
s.trackingServerSecure = "data.example.com";
```

CNAME-records wijzen doorgaans naar een subdomein op `ssl.d1.sc.omtrdc.net`.
