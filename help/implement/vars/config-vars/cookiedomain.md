---
title: cookieDomain
description: De cookieDomain-variabele helpt het domein te bepalen waarop cookies moeten worden ingesteld.
feature: Variables
exl-id: 7e8c26b8-d1a7-49f7-9c12-45fb1633c9d7
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: tm+mt
source-wordcount: '178'
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

## Cookie-domein met tags in Adobe Experience Platform

Er is geen specifiek gebied in de Inzameling van Gegevens UI om deze variabele te gebruiken. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## s.cookieDomain in AppMeasurement en aangepaste code-editor

De `cookieDomain` variabele is een tekenreeks en wordt ingesteld op het domein waarop u cookies wilt opslaan.

```js
s.cookieDomain = "stats.example.com";
```
