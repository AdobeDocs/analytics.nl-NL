---
title: cookieDomain
description: De cookieDomain-variabele helpt het domein te bepalen waarop cookies moeten worden ingesteld.
feature: Variables
exl-id: 7e8c26b8-d1a7-49f7-9c12-45fb1633c9d7
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 1%

---

# cookieDomain

>[!IMPORTANT]
>
>Deze variabele wordt uitgeschakeld. Gebruiken [`trackingServer`](trackingserver.md) in plaats daarvan.

De `cookieDomain` De variabele bepaalt het domein waar AppMeasurement koekjes plaatst. U kunt deze variabele gebruiken om het cookiedomein uitdrukkelijk te plaatsen in plaats van het gebruiken van [`cookieDomainPeriods`](cookiedomainperiods.md) variabele.

Deze variabele hoeft alleen te worden gebruikt wanneer **beide** aan een van de volgende voorwaarden is voldaan:

* Als uw implementatie cookies van de eerste fabrikant gebruikt. Deze variabele is niet vereist bij implementaties die een [`trackingServer`](trackingserver.md) waarde die `sc.adobedc.net`.
* Als het achtervoegsel van het domein een punt bevat. Bijvoorbeeld: `example.co.uk` kan de `cookieDomain` variabele om expliciet aan te geven dat het cookiedomein `example.co.uk` en niet `co.uk`.

Slechts een klein aantal implementaties heeft voor de `cookieDomain` variabele, en zelfs dan, alternatieve variabelen zoals [`cookieDomainPeriods`](cookiedomainperiods.md) kan in plaats daarvan worden gebruikt.

## Het Domein van de cookie die SDK van het Web gebruikt

De SDK van het Web kan het correcte domein van de koekjesopslag zonder deze variabele bepalen.

## Cookie-domein met Adobe Analytics-extensie

Er is geen specifiek veld in de Adobe Analytics-extensie voor het gebruik van deze variabele. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## s.cookieDomain in AppMeasurement en de aangepaste code-editor voor de extensie Analytics

De `cookieDomain` variabele is een tekenreeks en wordt ingesteld op het domein waarop u cookies wilt opslaan.

```js
s.cookieDomain = "stats.example.com";
```
