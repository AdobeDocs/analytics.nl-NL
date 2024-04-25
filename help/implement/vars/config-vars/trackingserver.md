---
title: trackingServer
description: Bepaal de locatie waarnaar verzoeken voor de afbeelding worden verzonden.
feature: Variables
exl-id: bcc23286-4dd5-45ac-ac6f-7b60e95cb798
role: Admin, Developer
source-git-commit: 284f121428ce9d682b42309dd85cfd117285a7e5
workflow-type: tm+mt
source-wordcount: '683'
ht-degree: 0%

---

# trackingServer

Adobe verzamelt gegevens op uw site door een afbeeldingsaanvraag te ontvangen die door de bezoeker is gegenereerd. De `trackingServer` De variabele bepaalt de locatie die een afbeeldingsaanvraag wordt verzonden. Als deze variabele niet correct wordt gedefinieerd, kan uw implementatie gegevensverlies ervaren.

>[!WARNING]
>
>Als u deze waarde wijzigt, zoekt het AppMeasurement naar cookies op een andere locatie. Het unieke aantal bezoekers kan tijdelijk in de rapportage springen, omdat bezoekerscookies op de nieuwe locatie worden ingesteld.

## Het domein van de rand die de uitbreiding van SDK van het Web gebruikt

Het gebruik van Web SDK [!UICONTROL Edge domain] om zowel Tracking Server als Secure Tracking Server te verwerken. U kunt het gewenste [!UICONTROL Edge domain] waarde wanneer het vormen van de uitbreiding van SDK van het Web.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de gewenste tageigenschap.
1. Ga naar de [!UICONTROL Extensions] en klikt u op de knop **[!UICONTROL Configure]** knop onder [!UICONTROL Adobe Experience Platform Web SDK].
1. Stel het gewenste **[!UICONTROL Edge domain]** tekstveld.

Zie [De extensie Adobe Experience Platform Web SDK configureren](https://experienceleague.adobe.com/docs/experience-platform/edge/extension/web-sdk-extension-configuration.html) in de documentatie van SDK van het Web voor meer informatie.

>[!TIP]
>
>Als uw organisatie zich van een AppMeasurement of de de uitbreidingsimplementatie van Analytics aan SDK van het Web beweegt, kan dit gebied de zelfde waarde gebruiken bevat in `trackingServerSecure` (of `trackingServer`).

## Het domein van de rand voert manueel de SDK van het Web uit

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

## s.trackingServer in AppMeasurement en de de coderedacteur van de de uitbreidingsuitbreiding van de Analyse

De `s.trackingServer` variable is a string that contains the location to send data.

## Overwegingen bij het bepalen van de waarde voor `trackingServer`

U kunt ervoor kiezen de volgende serverdomeinen van de Adobe te gebruiken (bijvoorbeeld `adobedc.net`) of u kunt een speciaal proces doorlopen om een trackingserver in te stellen die overeenkomt met uw sitedomein (bijvoorbeeld `data.mydomain.com`), ook bekend als implementatie CNAME. Een trackingserver die overeenkomt met uw sitedomein kan voordelen hebben, afhankelijk van andere aspecten van uw implementatie. Wanneer de trackingserver niet overeenkomt met het domein van de huidige pagina, moeten cookies die door het AppMeasurement zijn ingesteld, als derde worden ingesteld. Als de browser geen cookies van derden ondersteunt, kan dit probleem problemen opleveren met bepaalde analysefuncties:

- Instellende herkenningstekens: Als u de Dienst van de Identiteit van het Experience Cloud gebruikt heeft de volgende server geen invloed op hoe de koekjes worden geplaatst. Als u echter oude id&#39;s voor Analytics gebruikt (ook wel `s_vi` cookie) en de verzamelingsserver komt niet overeen met het huidige domein, en cookies moeten dan als derde worden ingesteld. Als cookies van derden in dit geval door de browser worden geblokkeerd, stelt Analytics een fallback-id van de eerste fabrikant in (`s_fid`) in plaats van de norm `s_vi` cookie.
- Koppelingen bijhouden werkt niet voor interne koppelingen.
- Activity Map werkt niet voor interne koppelingen.
- Koekjescontrole.

### Cookies van eerste bedrijven

Als u een first-party koekjesimplementatie gebruikt, is het waarschijnlijk dat iemand in uw organisatie reeds het eerste-partijkoekjesproces heeft voltooid. Zie [Eerste cookies in het Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-first-party.html) in de de gebruikersgids van de Diensten van de Kern voor meer informatie over het eerste-partijkoekjesproces.

De individu die aanvankelijk de first-party koekjesimplementatie vormt bepaalt ook het domein en subdomain gebruikte. Bijvoorbeeld:

```js
s.trackingServer = "data.example.com";
```

### Trackingserver van derden

>[!TIP]
>
>De toenemende privacy praktijken in moderne browsers maken derdekoekjes minder betrouwbaar. Adobe raadt aan de cookie-workflow van de eerste fabrikant te volgen.

Als u een cookie-implementatie van een andere fabrikant gebruikt, moet u de waarde voor `trackingServer` is een subdomein van `data.adobedc.net`. Bijvoorbeeld:

```js
s.trackingServer = "example.data.adobedc.net";
```

Kies een subdomein dat uniek is voor uw organisatie. Het is onwaarschijnlijk dat het wordt gekozen door een andere organisatie die Adobe Analytics gebruikt.  De aan uw organisatie toegewezen naamruimte voor bezoekers wordt aanbevolen.  Zorg ervoor dat alle implementaties in uw organisatie dezelfde trackingserver gebruiken. Het kan nuttig zijn deze informatie in een [document ontwerp oplossing](../../prepare/solution-design.md).

Uw organisatie gebruikt mogelijk al een trackingserver van derden in de `sc.omtrdc.net` of `2o7.net` domeinen.  Deze werden voornamelijk gebruikt in eerdere versies van Adobe Analytics en zijn nog steeds geldig.

>[!NOTE]
>
>Gebruik geen subdomeinen die dieper zijn dan `example.data.adobedc.net`. Bijvoorbeeld: `custom.example.data.adobedc.net` is geen geldige trackingserver.
