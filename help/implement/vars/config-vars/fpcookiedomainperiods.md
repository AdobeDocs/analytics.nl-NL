---
title: fpcookieDomainPeriods
description: Help AppMeasurement weet welk domein cookies moeten worden opgeslagen als het achtervoegsel van uw domein een punt bevat.
feature: Variables
exl-id: e994a188-1dab-4bf0-912b-cd2f6a1032e0
source-git-commit: 10ff98f7ca4697afe5c2dae66be415c0d68c4aac
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 0%

---

# fpCookieDomainPeriods

De `fpCookieDomainPeriods` Met de variabele kan AppMeasurement bepalen waar Analytics-cookies worden ingesteld door aan te roepen dat het domeinachtervoegsel een extra periode bevat. Met deze variabele kan AppMeasurement de extra periode in het domeinachtervoegsel aanpassen en cookies instellen op de juiste locatie. Het erft de waarde van [`cookieDomainPeriods`](cookiedomainperiods.md), maar het is nog steeds de beste manier om in te stellen of u een cookie-implementatie van de eerste fabrikant gebruikt.

* Voor domeinen zoals `example.com` of `www.example.com`hoeft u deze variabele niet in te stellen. Indien nodig kunt u deze variabele instellen op `"2"`.
* Voor domeinen zoals `example.co.uk` of `www.example.co.jp`stelt u deze variabele in op `"3"`.

>[!IMPORTANT]
>
>Houd geen rekening met subdomeinen voor deze variabele. Niet instellen `fpCookieDomainPeriods` in de voorbeeld-URL `store.toys.example.com`. AppMeasurement herkent standaard dat cookies moeten worden opgeslagen op `example.com`, zelfs op URL&#39;s met veel subdomeinen.

## Domeinperioden van de eerste partij met tags in Adobe Experience Platform

Domeintermijnen van de eerste partij is een gebied onder [!UICONTROL Cookies] accordeon bij het configureren van de Adobe Analytics-extensie.

1. Aanmelden bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar de [!UICONTROL Extensions] en klikt u op de knop [!UICONTROL Configure] onder Adobe Analytics.
4. Breid uit [!UICONTROL Cookies] accordion, die de [!UICONTROL First-party Domain Periods] veld.

Stel dit veld in op `3` alleen in domeinen die een punt in zijn achtervoegsel bevatten. Anders kan dit veld leeg blijven.

## s.fpCookieDomainPeriods in AppMeasurement en de douane-code-editor

De `fpCookieDomainPeriods` variabele is een tekenreeks die doorgaans wordt ingesteld op `"3"`, alleen op domeinen die een punt in het achtervoegsel bevatten. De standaardwaarde is `"2"`, waarin de meeste domeinen passen.

```js
// Manually set fpCookieDomainPeriods for domains with a period in its suffix, such as www.example.co.uk
s.fpCookieDomainPeriods = "3";

// Detect if a URL has a domain suffix with an extra period, and set s.fpCookieDomainPeriods automatically
document.URL.indexOf(".co.") > 0 ? s.fpCookieDomainPeriods = "3" : s.fpCookieDomainPeriods = "2";
```
