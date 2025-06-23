---
title: trackingServer
description: Bepaal de locatie waarnaar verzoeken voor de afbeelding worden verzonden.
feature: Appmeasurement Implementation
exl-id: bcc23286-4dd5-45ac-ac6f-7b60e95cb798
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '683'
ht-degree: 0%

---

# trackingServer

Adobe verzamelt gegevens op uw site door een afbeeldingsaanvraag te ontvangen die door de bezoeker is gegenereerd. De `trackingServer` -variabele bepaalt de locatie waar een afbeeldingsaanvraag wordt verzonden. Als deze variabele niet correct wordt gedefinieerd, kan uw implementatie gegevensverlies ervaren.

>[!WARNING]
>
>Als u deze waarde wijzigt, zoekt AppMeasurement naar cookies op een andere locatie. Het unieke aantal bezoekers kan tijdelijk in de rapportage springen, omdat bezoekerscookies op de nieuwe locatie worden ingesteld.

## Edge-domein met de extensie Web SDK

Het Web SDK gebruikt [!UICONTROL Edge domain] om zowel de het Volgen Server als Veilige het Volgen Server te behandelen. U kunt de gewenste [!UICONTROL Edge domain] -waarde instellen wanneer u de extensie Web SDK configureert.

1. Login aan [ de Inzameling van Gegevens van Adobe Experience Platform ](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
1. Klik op de gewenste tageigenschap.
1. Ga naar de tab [!UICONTROL Extensions] en klik vervolgens op de knop **[!UICONTROL Configure]** onder [!UICONTROL Adobe Experience Platform Web SDK] .
1. Stel het gewenste tekstveld in **[!UICONTROL Edge domain]** .

Zie [ de uitbreiding van SDK van het Web van Adobe Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/edge/extension/web-sdk-extension-configuration.html) in de documentatie van SDK van het Web voor meer informatie vormen.

>[!TIP]
>
>Als uw organisatie vanuit een AppMeasurement- of analytische extensie-implementatie naar de Web SDK gaat, kan voor dit veld dezelfde waarde worden gebruikt als in `trackingServerSecure` (of `trackingServer` ).

## Edge-domein handmatig implementeren van de Web SDK

Vorm SDK gebruikend [`edgeDomain` ](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html). Het veld is een tekenreeks die het domein bepaalt waarnaar gegevens moeten worden verzonden.

```json
alloy("configure", {
  "edgeDomain": "data.example.com"
});
```

## Trackingserver met de Adobe Analytics-extensie

Trackingserver is een veld onder de accordeon [!UICONTROL General] wanneer u de Adobe Analytics-extensie configureert.

1. Login aan [ de Inzameling van Gegevens van Adobe Experience Platform ](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
2. Klik op de gewenste tageigenschap.
3. Ga naar de tab [!UICONTROL Extensions] en klik vervolgens op de knop **[!UICONTROL Configure]** onder Adobe Analytics.
4. Vouw de accordeon [!UICONTROL General] uit, zodat het veld [!UICONTROL Tracking Server] zichtbaar wordt.

Als dit veld niet wordt ingevuld, wordt standaard `[rsid].data.adobedc.net` gebruikt.

## s.trackingServer in AppMeasurement en de aangepaste code-editor voor de extensie Analytics

De variabele `s.trackingServer` is een tekenreeks die de locatie bevat waar gegevens moeten worden verzonden.

## Overwegingen bij het bepalen van de waarde voor `trackingServer`

U kunt ervoor kiezen om Adobe tracking-serverdomeinen (bijvoorbeeld `adobedc.net` ) te gebruiken of u kunt een speciaal proces doorlopen om een tracingserver in te stellen die overeenkomt met uw sitedomein (bijvoorbeeld `data.mydomain.com` ), ook wel bekend als een CNAME-implementatie. Een trackingserver die overeenkomt met uw sitedomein kan voordelen hebben, afhankelijk van andere aspecten van uw implementatie. Wanneer de trackingserver niet overeenkomt met het domein van de huidige pagina, moeten cookies die door AppMeasurement zijn ingesteld, als derde worden ingesteld. Als de browser geen cookies van derden ondersteunt, kan dit probleem problemen opleveren met bepaalde analysefuncties:

- Identificatiecodes instellen: als u de Experience Cloud Identity Service gebruikt, heeft de trackingserver geen invloed op de manier waarop cookies worden ingesteld. Als u echter oude id&#39;s voor Analytics gebruikt (ook wel de `s_vi` cookie genoemd) en de verzamelingsserver niet overeenkomt met het huidige domein, moeten cookies als derde worden ingesteld. In dit geval, als derdekoekjes door browser worden geblokkeerd, plaatst de Analytics een eerste - partijreserve identiteitskaart (`s_fid`) in plaats van het standaard `s_vi` koekje.
- Koppelingen bijhouden werkt niet voor interne koppelingen.
- Activity Map werkt niet voor interne koppelingen.
- Koekjescontrole.

### Cookies van eerste bedrijven

Als u een first-party koekjesimplementatie gebruikt, is het waarschijnlijk dat iemand in uw organisatie reeds het eerste-partijkoekjesproces heeft voltooid. Zie [ Eerste partijkoekjes in Experience Cloud ](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-first-party.html) in de de gebruikersgids van de Diensten van de Kern voor meer informatie over het proces van het eerste-partijkoekje.

De individu die aanvankelijk de first-party koekjesimplementatie vormt bepaalt ook het domein en subdomain gebruikte. Bijvoorbeeld:

```js
s.trackingServer = "data.example.com";
```

### Trackingserver van derden

>[!TIP]
>
>De toenemende privacy praktijken in moderne browsers maken derdekoekjes minder betrouwbaar. Adobe raadt aan de cookie-workflow van de eerste partij te volgen.

Als u een cookie-implementatie van een andere fabrikant gebruikt, is de waarde voor `trackingServer` een subdomein van `data.adobedc.net` . Bijvoorbeeld:

```js
s.trackingServer = "example.data.adobedc.net";
```

Kies een subdomein dat uniek is voor uw organisatie. Het is onwaarschijnlijk dat het wordt gekozen door een andere organisatie die Adobe Analytics gebruikt.  De aan uw organisatie toegewezen naamruimte voor bezoekers wordt aanbevolen.  Zorg ervoor dat alle implementaties in uw organisatie dezelfde trackingserver gebruiken. Het kan nuttig zijn om deze informatie in het document van het a [ oplossingsontwerp ](../../prepare/solution-design.md) te handhaven.

Uw organisatie gebruikt mogelijk al een trackingserver van derden in de domeinen `sc.omtrdc.net` of `2o7.net` .  Deze werden voornamelijk gebruikt in eerdere versies van Adobe Analytics en zijn nog steeds geldig.

>[!NOTE]
>
>Gebruik geen subdomeinen die dieper zijn dan `example.data.adobedc.net` . `custom.example.data.adobedc.net` is bijvoorbeeld geen geldige trackingserver.
