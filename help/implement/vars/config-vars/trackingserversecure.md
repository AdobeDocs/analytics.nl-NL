---
title: trackingServerSecure
description: Bepaal de locatie waar afbeeldingsaanvragen worden verzonden op HTTPS-pagina's.
exl-id: d5b112f9-f3f6-43ac-8ee5-d9ad8062e380
source-git-commit: f669af03a502d8a24cea3047b96ec7cba7c59e6f
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 2%

---

# trackingServerSecure

Adobe verzamelt gegevens op uw site door een afbeeldingsaanvraag te ontvangen die door de bezoeker is gegenereerd. De variabele `trackingServerSecure` bepaalt de locatie die een afbeeldingsverzoek via HTTPS wordt verzonden. Het bepaalt ook welke cookies van de locatiebezoeker worden opgeslagen. Als deze variabele niet correct wordt gedefinieerd, kan uw implementatie gegevensverlies ervaren.

>[!IMPORTANT]
>
>Als u deze waarde wijzigt, zoekt AppMeasurement naar cookies op een andere locatie. Het unieke aantal bezoekers kan tijdelijk in de rapportage springen, omdat bezoekerscookies op de nieuwe locatie worden ingesteld.

## SSL-traceringsserver in Adobe Experience Platform Launch

[!UICONTROL SSL Tracking Server] is een veld onder de  [!UICONTROL General] accordeon bij het configureren van de Adobe Analytics-extensie.

1. Meld u met uw Adobe-id aan bij [launch.adobe.com](https://launch.adobe.com).
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Extensions] lusje, dan klik [!UICONTROL Configure] knoop onder Adobe Analytics.
4. Vouw de accordeon [!UICONTROL General] uit, zodat het veld [!UICONTROL SSL Tracking Server] zichtbaar wordt.

Als dit veld niet wordt ingevuld, wordt standaard de waarde in de variabele [`trackingServer`](trackingserver.md) gebruikt.

## s.trackingServerSecure in de aangepaste code-editor van AppMeasurement en Launch

De variabele `s.trackingServerSecure` is een tekenreeks die de locatie bevat voor het verzenden van verzoeken om afbeeldingen. Het is bijna altijd een subdomein van uw site. De moderne privacy praktijken in browsers maken over het algemeen derde koekjes onbetrouwbaar. Als deze variabele leeg is, wordt de waarde in de variabele `s.trackingServer` gebruikt.

De waarde voor deze variabele is bijna altijd een domein van de eerste partij, zoals `data.example.com`. Zie [First-party koekjes in de Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-first-party.html) in de de gebruikersgids van de Diensten van de Kern voor meer informatie over het first-party koekjesproces.

De individu die aanvankelijk de first-party koekjesimplementatie vormt bepaalt ook het domein en subdomain gebruikte. Bijvoorbeeld:

```js
s.trackingServerSecure = "data.example.com";
```

CNAME-records verwijzen gewoonlijk naar een subdomein op `data.adobedc.net`, `sc.adobedc.net` of `2o7.net`.
