---
title: cookieDomain
description: De cookieDomain-variabele helpt het domein te bepalen waarop cookies moeten worden ingesteld.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# cookieDomain

> [!IMPORTANT] Deze variabele wordt uitgeschakeld. Gebruik [`trackingServer`](trackingserver.md) in plaats hiervan.

De `cookieDomain` variabele bepaalt het domein waar AppMeturement koekjes plaatst. U kunt deze variabele gebruiken om het cookiedomein uitdrukkelijk te plaatsen in plaats van het gebruiken van de [`cookieDomainPeriods`](cookiedomainperiods.md) variabele.

Deze variabele hoeft alleen te worden gebruikt als aan **beide** voorwaarden is voldaan:

* Als uw implementatie cookies van de eerste fabrikant gebruikt. Deze variabele wordt niet vereist met implementaties die een [`trackingServer`](trackingserver.md) waarde bevatten `sc.omtrdc.net`.
* Als het achtervoegsel van het domein een punt bevat. Bijvoorbeeld, `example.co.uk` kon de `cookieDomain` variabele gebruiken om uitdrukkelijk te verklaren dat het koekjesdomein is `example.co.uk` en niet `co.uk`.

Slechts een klein aantal implementaties heeft gebruik voor de `cookieDomain` variabele, en zelfs dan, kunnen de alternatieve variabelen zoals in plaats daarvan [`cookieDomainPeriods`](cookiedomainperiods.md) worden gebruikt.

## Cookie-domein in Adobe Experience Platform Launch

Er is geen specifiek veld in Launch om deze variabele te gebruiken. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## s.cookieDomain in aangepaste code-editor voor AppMeasurement en Launch

De `cookieDomain` variabele is een tekenreeks en wordt ingesteld op het domein waarop u cookies wilt opslaan.

```js
s.cookieDomain = "stats.example.com";
```
