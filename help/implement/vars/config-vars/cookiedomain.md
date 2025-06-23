---
title: cookieDomain
description: (In ruste) Hiermee kunt u het domein bepalen waarop cookies moeten worden ingesteld.
feature: Appmeasurement Implementation
exl-id: 7e8c26b8-d1a7-49f7-9c12-45fb1633c9d7
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 0%

---

# cookieDomain

>[!IMPORTANT]
>Deze variabele wordt uitgeschakeld. Gebruik in plaats hiervan [`trackingServer`](trackingserver.md) .

De variabele `cookieDomain` bepaalt het domein waar AppMeasurement cookies instelt. U kunt deze variabele gebruiken om het cookiedomein expliciet in te stellen in plaats van de variabele [`cookieDomainPeriods`](cookiedomainperiods.md) te gebruiken.

Deze variabele moet slechts worden gebruikt wanneer **allebei** van de volgende voorwaarden wordt voldaan aan:

* Als uw implementatie cookies van de eerste fabrikant gebruikt. Deze variabele is niet vereist bij implementaties met een [`trackingServer`](trackingserver.md) -waarde die `sc.adobedc.net` bevat.
* Als het achtervoegsel van het domein een punt bevat. `example.co.uk` kan bijvoorbeeld de variabele `cookieDomain` gebruiken om expliciet aan te geven dat het cookiedomein `example.co.uk` is en niet `co.uk` .

Slechts een klein aantal implementaties heeft gebruik voor de `cookieDomain` variabele, en zelfs toen, kunnen de alternatieve variabelen zoals [`cookieDomainPeriods`](cookiedomainperiods.md) in plaats daarvan worden gebruikt.

## Cookie-domein gebruiken voor Web SDK

Web SDK kan het correcte koekjesopslagdomein zonder deze variabele bepalen.

## Cookie-domein met Adobe Analytics-extensie

Er is geen specifiek veld in de Adobe Analytics-extensie voor het gebruik van deze variabele. Gebruik de aangepaste code-editor volgens de AppMeasurement-syntaxis.

## s.cookieDomain in AppMeasurement en de aangepaste code-editor voor de extensie Analytics

De variabele `cookieDomain` is een tekenreeks en wordt ingesteld op het domein waarop u cookies wilt opslaan.

```js
s.cookieDomain = "stats.example.com";
```
