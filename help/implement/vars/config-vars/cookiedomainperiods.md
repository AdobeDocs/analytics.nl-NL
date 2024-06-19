---
title: cookieDomainPeriods
description: (Verouderd) Help AppMeasurement bepalen waar cookies moeten worden opgeslagen wanneer het domein op hoofdniveau van een website een periode bevat.
feature: Variables
exl-id: c426d6a7-4521-4d50-bb7d-1664920618d8
role: Admin, Developer
source-git-commit: 75ae77c1da1b578639609888e794e13d965ef669
workflow-type: tm+mt
source-wordcount: '351'
ht-degree: 0%

---


# cookieDomainPeriods

>[!IMPORTANT]
>Deze variabele is vervangen. Als u AppMeasurement v2.26.x of later gebruikt, of de uitbreiding van Adobe Analytics v1.9.4 of later, ontdekt de bibliotheek automatisch het domein om koekjes te plaatsen.

De `cookieDomainPeriods` De variabele hielp AppMeasurement bepalen waar te om de koekjes van Analytics te plaatsen door erop te wijzen dat het top-level domein een extra periode in het had. Deze variabele stond AppMeasurement toe om de extra periode in het top-level domein aan te passen en koekjes in de correcte plaats te plaatsen. Als het domein op hoofdniveau van uw website geen extra periode bevat, is deze variabele niet vereist.

* Voor domeinen zoals `example.co.uk` of `www.example.co.jp`stelt u deze variabele in op `"3"`.
* Voor domeinen zoals `example.nsw.gov.au`stelt u deze variabele in op `"4"`.
* Voor domeinen zoals `example.com` of `products.example.org`, deze variabele weglaten of instellen op `"2"`.

>[!TIP]
>
>Houd geen rekening met subdomeinen voor deze variabele. Niet instellen `cookieDomainPeriods` in de voorbeeld-URL `store.toys.example.com`. AppMeasurement herkent dat cookies worden opgeslagen op `example.com`, zelfs op URL&#39;s met veel subdomeinen.

Voor implementaties op AppMeasurement v2.26.x of later, [`s_ac`](https://experienceleague.adobe.com/en/docs/core-services/interface/data-collection/cookies/analytics) cookie wordt gebruikt om automatisch het juiste cookiedomein te bepalen. De bibliotheek probeert eerst een cookie te schrijven, die twee domeinperiodes omvat. Als het instellen van dit cookie mislukt, wordt het opnieuw geprobeerd, inclusief meer domeinperiodes totdat het cookie is gelukt. Deze cookie wordt direct verwijderd zodra deze is ingesteld.

## Domeinperioden cookie maken met de SDK van het web

De SDK van het Web bepaalt automatisch het correcte domein om koekjes te plaatsen.

## Domeinperiodes kopiëren met de Adobe Analytics-extensie

**[!UICONTROL Domain Periods]** is een veld onder de [!UICONTROL Cookies] accordeon bij het configureren van de Adobe Analytics-extensie.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de gewenste tageigenschap.
1. Ga naar de [!UICONTROL Extensions] en klikt u op de knop **[!UICONTROL Configure]** onder Adobe Analytics.
1. Breid uit [!UICONTROL Cookies] accordion, die de [!UICONTROL Domain Periods] veld.

Stel dit veld in op `3` alleen op topniveaudomeinen die een punt bevatten. Anders kan dit veld leeg blijven.

## Cookie-domeinperiodes in AppMeasurement en de aangepaste code-editor voor de extensie Analytics

De `cookieDomainPeriods` variabele is een tekenreeks die doorgaans wordt ingesteld op `"3"`, alleen op topniveaudomeinen die een punt bevatten. De standaardwaarde is `"2"`, die de meeste domeinen op het hoogste niveau aanpast, zoals `.com` en `.org`.

```js
// Manually set cookieDomainPeriods for domains with a period in the top-level domain, such as www.example.co.uk
s.cookieDomainPeriods = "3";
```
