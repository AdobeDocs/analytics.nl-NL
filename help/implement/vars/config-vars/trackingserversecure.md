---
title: trackingServerSecure
description: Bepaal de locatie waar afbeeldingsaanvragen worden verzonden op HTTPS-pagina's.
exl-id: d5b112f9-f3f6-43ac-8ee5-d9ad8062e380
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 1%

---

# trackingServerSecure

Adobe verzamelt gegevens op uw site door een afbeeldingsaanvraag te ontvangen die door de bezoeker is gegenereerd. De variabele `trackingServerSecure` bepaalt de locatie die een afbeeldingsverzoek via HTTPS wordt verzonden. Het bepaalt ook welke cookies van de locatiebezoeker worden opgeslagen. Als deze variabele niet correct wordt gedefinieerd, kan uw implementatie gegevensverlies ervaren.

>[!IMPORTANT]
>
>Als u deze waarde wijzigt, zoekt AppMeasurement naar cookies op een andere locatie. Het unieke aantal bezoekers kan tijdelijk in de rapportage springen, omdat bezoekerscookies op de nieuwe locatie worden ingesteld.

## SSL-traceringsserver gebruikt tags in Adobe Experience Platform

[!UICONTROL SSL Tracking Server] is een veld onder de  [!UICONTROL General] accordeon bij het configureren van de Adobe Analytics-extensie.

1. Meld u aan bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Extensions] lusje, dan klik [!UICONTROL Configure] knoop onder Adobe Analytics.
4. Vouw de accordeon [!UICONTROL General] uit, zodat het veld [!UICONTROL SSL Tracking Server] zichtbaar wordt.

Als dit veld niet wordt ingevuld, wordt standaard de waarde in de variabele [`trackingServer`](trackingserver.md) gebruikt.

## s.trackingServerSecure in AppMeasurement en aangepaste code-editor

De variabele `s.trackingServerSecure` is een tekenreeks die de locatie bevat voor het verzenden van verzoeken om afbeeldingen. Het is bijna altijd een subdomein van uw site. De moderne privacy praktijken in browsers maken over het algemeen derde koekjes onbetrouwbaar. Als deze variabele leeg is, wordt de waarde in de variabele `s.trackingServer` gebruikt.

De waarde voor deze variabele is bijna altijd een domein van de eerste partij, zoals `data.example.com`. Zie [First-party koekjes in de Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-first-party.html) in de de gebruikersgids van de Diensten van de Kern voor meer informatie over het first-party koekjesproces.

De individu die aanvankelijk de first-party koekjesimplementatie vormt bepaalt ook het domein en subdomain gebruikte. Bijvoorbeeld:

```js
s.trackingServerSecure = "data.example.com";
```

CNAME-records verwijzen gewoonlijk naar een subdomein op `data.adobedc.net`, `sc.adobedc.net` of `2o7.net`.
