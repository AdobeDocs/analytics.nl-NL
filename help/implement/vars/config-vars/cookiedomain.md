---
title: cookieDomain
description: De cookieDomain-variabele helpt het domein te bepalen waarop cookies moeten worden ingesteld.
exl-id: 7e8c26b8-d1a7-49f7-9c12-45fb1633c9d7
source-git-commit: 9a70d79a83d8274e17407229bab0273abbe80649
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 1%

---

# cookieDomain

>[!IMPORTANT]
>
>Deze variabele wordt uitgeschakeld. Gebruik in plaats hiervan [`trackingServer`](trackingserver.md).

De `cookieDomain` variabele bepaalt het domein waar AppMeturement koekjes plaatst. U kunt deze variabele gebruiken om het cookiedomein uitdrukkelijk te plaatsen in plaats van het gebruiken van [`cookieDomainPeriods`](cookiedomainperiods.md) variabele.

Deze variabele hoeft alleen te worden gebruikt als **beide** aan de volgende voorwaarden voldoen:

* Als uw implementatie cookies van de eerste fabrikant gebruikt. Deze variabele is niet vereist bij implementaties die een [`trackingServer`](trackingserver.md) waarde gebruiken die `sc.adobedc.net` bevat.
* Als het achtervoegsel van het domein een punt bevat. `example.co.uk` kan bijvoorbeeld de variabele `cookieDomain` gebruiken om expliciet aan te geven dat het cookiedomein `example.co.uk` is en niet `co.uk`.

Slechts een klein aantal implementaties heeft gebruik voor de `cookieDomain` variabele, en zelfs dan, kunnen de alternatieve variabelen zoals [`cookieDomainPeriods`](cookiedomainperiods.md) in plaats daarvan worden gebruikt.

## Cookie-domein met tags in Adobe Experience Platform

Er is geen specifiek gebied in de Inzameling van Gegevens UI om deze variabele te gebruiken. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## s.cookieDomain in AppMeasurement en aangepaste code-editor

De variabele `cookieDomain` is een tekenreeks en wordt ingesteld op het domein waarop u cookies wilt opslaan.

```js
s.cookieDomain = "stats.example.com";
```
