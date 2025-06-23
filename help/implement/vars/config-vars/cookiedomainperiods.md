---
title: cookieDomainPeriods
description: (Verouderd) Help AppMeasurement te bepalen waar cookies moeten worden opgeslagen wanneer het domein op hoofdniveau van een website een punt bevat.
feature: Appmeasurement Implementation
exl-id: c426d6a7-4521-4d50-bb7d-1664920618d8
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '364'
ht-degree: 0%

---

# cookieDomainPeriods

>[!IMPORTANT]
>Deze variabele is vervangen. Als u een van de volgende methoden gebruikt:
>
>* AppMeasurement v2.26.x of hoger
>* Adobe Analytics-extensie v1.9.4 of hoger
>* Adobe Experience Cloud ID-service
>
>Deze variabele doet niets, aangezien de toepasselijke bibliotheek automatisch het domein ontdekt om koekjes te plaatsen.

Met de `cookieDomainPeriods` -variabele kon AppMeasurement bepalen waar Analytics-cookies moeten worden ingesteld door aan te geven dat het domein op het hoogste niveau een extra periode had. Met deze variabele kon AppMeasurement de extra periode in het domein op het hoogste niveau aanpassen en cookies instellen op de juiste locatie. Als het domein op hoofdniveau van uw website geen extra periode bevat, is deze variabele niet vereist.

* Voor domeinen zoals `example.co.uk` of `www.example.co.jp` stelt u deze variabele in op `"3"` .
* Voor domeinen zoals `example.nsw.gov.au`, plaats deze variabele aan `"4"`.
* Voor domeinen zoals `example.com` of `products.example.org` , laat u deze variabele weg of plaats het aan `"2"`.

>[!TIP]
>
>Houd geen rekening met subdomeinen voor deze variabele. Stel bijvoorbeeld `cookieDomainPeriods` niet in op de voorbeeld-URL `store.toys.example.com` . AppMeasurement herkent dat cookies worden opgeslagen op `example.com` , zelfs op URL&#39;s met veel subdomeinen.

Voor implementaties op AppMeasurement v2.26.x of later, wordt het [`s_ac` ](https://experienceleague.adobe.com/nl/docs/core-services/interface/data-collection/cookies/analytics) koekje gebruikt helpen automatisch het correcte koekjesdomein bepalen. De bibliotheek probeert eerst een cookie te schrijven, die twee domeinperiodes omvat. Als het instellen van dit cookie mislukt, wordt het opnieuw geprobeerd, inclusief meer domeinperiodes totdat het cookie is gelukt. Deze cookie wordt direct verwijderd zodra deze is ingesteld.

## Domeinperiodes kopiëren met gebruik van Web SDK

De Web SDK bepaalt automatisch het correcte domein om koekjes te plaatsen.

## Domeinperiodes kopiëren met de Adobe Analytics-extensie

**[!UICONTROL Domain Periods]** is een veld onder de accordeon van [!UICONTROL Cookies] wanneer u de Adobe Analytics-extensie configureert.

1. Login aan [ de Inzameling van Gegevens van Adobe Experience Platform ](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
1. Klik op de gewenste tageigenschap.
1. Ga naar de tab [!UICONTROL Extensions] en klik vervolgens op de knop **[!UICONTROL Configure]** onder Adobe Analytics.
1. Vouw de accordeon [!UICONTROL Cookies] uit, zodat het veld [!UICONTROL Domain Periods] zichtbaar wordt.

Stel dit veld in op `3` alleen op domeinen op hoofdniveau die een punt bevatten. Anders kan dit veld leeg blijven.

## Cookie-domeinperiodes in AppMeasurement en de aangepaste code-editor voor de extensie Analytics

De variabele `cookieDomainPeriods` is een tekenreeks die doorgaans op `"3"` wordt ingesteld, alleen op domeinen op hoofdniveau die een punt bevatten. De standaardwaarde is `"2"` , die geschikt is voor de meeste domeinen op het hoogste niveau, zoals `.com` en `.org` .

```js
// Manually set cookieDomainPeriods for domains with a period in the top-level domain, such as www.example.co.uk
s.cookieDomainPeriods = "3";
```
