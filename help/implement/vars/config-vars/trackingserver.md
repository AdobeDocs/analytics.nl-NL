---
title: trackingServer
description: Bepaal de locatie waarnaar verzoeken voor de afbeelding worden verzonden.
translation-type: tm+mt
source-git-commit: 09b453c1b4cd8555c5d1718759003945f5c230c5
workflow-type: tm+mt
source-wordcount: '392'
ht-degree: 2%

---


# trackingServer

Adobe verzamelt gegevens op uw site door een afbeeldingsaanvraag te ontvangen die door de bezoeker is gegenereerd. De `trackingServer` variabele bepaalt de locatie die een afbeeldingsaanvraag wordt verzonden. Als deze variabele niet correct wordt gedefinieerd, kan uw implementatie gegevensverlies ervaren.

>[!IMPORTANT]
>
>Als u deze waarde wijzigt, zoekt AppMeasurement naar cookies op een andere locatie. Het unieke aantal bezoekers kan tijdelijk in de rapportage springen, omdat bezoekerscookies op de nieuwe locatie worden ingesteld.

## Trackingserver in Adobe Experience Platform Launch

De volgende Server is een gebied onder de [!UICONTROL General] accordeon wanneer het vormen van de uitbreiding van Adobe Analytics.

1. Meld u aan bij [launch.adobe.com](https://launch.adobe.com) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Extensions] tabblad en klik vervolgens op de [!UICONTROL Configure] knop onder Adobe Analytics.
4. Breid de accordeon uit, die het [!UICONTROL General] [!UICONTROL Tracking Server] veld onthult.

Als dit veld niet wordt ingevuld, wordt standaard ingesteld op `[rsid].data.adobedc.net`.

## s.trackingServer in de aangepaste code-editor van AppMeasurement en Launch

De `s.trackingServer` variabele is een tekenreeks die de locatie bevat waar gegevens moeten worden verzonden.

## De waarde voor trackingServer bepalen

De waarde voor deze variabele is afhankelijk van het gebruik van cookies van andere bedrijven of van cookies van andere bedrijven. Adobe raadt u ten zeerste aan cookies van de eerste fabrikant te gebruiken in uw implementatie.

### Cookies van eerste bedrijven

Als u een first-party koekjesimplementatie gebruikt, is het waarschijnlijk dat iemand in uw organisatie reeds het eerste-partijkoekjesproces heeft voltooid. Zie [Eerste-partijkoekjes in de Experience Cloud](https://docs.adobe.com/content/help/en/core-services/interface/ec-cookies/cookies-first-party.html) in de de gebruikersgids van de Diensten van de Kern voor meer informatie over het first-party koekjesproces.

De individu die aanvankelijk de first-party koekjesimplementatie vormt bepaalt ook het domein en subdomain gebruikte. Bijvoorbeeld:

```js
s.trackingServer = "data.example.com";
```

### Cookies van andere bedrijven

>[!TIP]
>
>De toenemende privacy praktijken in moderne browsers maken derdekoekjes minder betrouwbaar. Adobe raadt u aan de cookie-workflow van de eerste fabrikant te volgen.

Als u een cookie-implementatie van een andere fabrikant gebruikt, `trackingServer` is de waarde voor een subdomein van `data.adobedc.net`. Bijvoorbeeld:

```js
s.trackingServer = "example.data.adobedc.net";
```

Kies een subdomein dat uniek is voor uw organisatie. Het is onwaarschijnlijk dat het wordt gekozen door een andere organisatie die Adobe Analytics gebruikt.  De aan uw organisatie toegewezen naamruimte voor bezoekers wordt aanbevolen.  Zorg ervoor dat alle implementaties in uw organisatie dezelfde trackingserver gebruiken. Het kan nuttig zijn om deze informatie in een document [van het](../../prepare/solution-design.md)oplossingsontwerp te handhaven.

Uw organisatie gebruikt mogelijk al een trackingserver van derden in de `sc.omtrdc.net` domeinen of in de `2o7.net` domeinen.  Deze werden voornamelijk gebruikt in eerdere versies van Adobe Analytics en zijn nog steeds geldig.

>[!NOTE]
>
>Gebruik geen subdomeinen die dieper zijn dan `example.data.adobedc.net`. Is bijvoorbeeld `custom.example.data.adobedc.net` geen geldige trackingserver.
