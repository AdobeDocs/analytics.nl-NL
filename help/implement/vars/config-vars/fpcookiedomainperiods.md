---
title: fpcookieDomainPeriods
description: Help AppMeasurement te begrijpen welk domein cookies moeten worden opgeslagen als voor uw domein een punt in het achtervoegsel staat.
feature: Appmeasurement Implementation
exl-id: e994a188-1dab-4bf0-912b-cd2f6a1032e0
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 0%

---

# fpCookieDomainPeriods

De `fpCookieDomainPeriods` -variabele helpt AppMeasurement te bepalen waar Analytics-cookies worden ingesteld door aan te roepen dat het domeinachtervoegsel een extra punt bevat. Met deze variabele kan AppMeasurement de extra periode in het domeinachtervoegsel aanpassen en cookies instellen op de juiste locatie. Het erft de waarde van [`cookieDomainPeriods`](cookiedomainperiods.md), maar het is nog steeds de beste manier om in te stellen als u een cookie-implementatie van de eerste partij gebruikt.

* Voor domeinen zoals `example.com` of `www.example.com` hoeft deze variabele niet te worden ingesteld. Indien nodig, kunt u deze variabele instellen op `"2"` .
* Voor domeinen zoals `example.co.uk` of `www.example.co.jp` stelt u deze variabele in op `"3"` .

>[!IMPORTANT]
>
>Houd geen rekening met subdomeinen voor deze variabele. Stel bijvoorbeeld `fpCookieDomainPeriods` niet in op de voorbeeld-URL `store.toys.example.com` . AppMeasurement herkent standaard dat cookies moeten worden opgeslagen op `example.com` , zelfs op URL&#39;s met veel subdomeinen.

## First-party domeinperiodes die de SDK van het Web gebruiken

Web SDK kan het correcte koekjesopslagdomein zonder deze variabele bepalen.

## Domeintermijnen van de eerste partij die de uitbreiding van Adobe Analytics gebruiken

Domeintermijnen van de eerste partij is een gebied onder de [!UICONTROL Cookies] accordion wanneer het vormen van de uitbreiding van Adobe Analytics.

1. Login aan [&#x200B; de Inzameling van Gegevens van Adobe Experience Platform &#x200B;](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
2. Klik op de gewenste tageigenschap.
3. Ga naar de tab [!UICONTROL Extensions] en klik vervolgens op de knop **[!UICONTROL Configure]** onder Adobe Analytics.
4. Vouw de accordeon [!UICONTROL Cookies] uit, zodat het veld [!UICONTROL First-party Domain Periods] zichtbaar wordt.

Stel dit veld in op `3` alleen in domeinen met een punt in het achtervoegsel. Anders kan dit veld leeg blijven.

## s.fpCookieDomainPeriods in AppMeasurement en de aangepaste code-editor van de extensie Analytics

De variabele `fpCookieDomainPeriods` is een tekenreeks die doorgaans wordt ingesteld op `"3"` , alleen in domeinen die een punt in het achtervoegsel bevatten. De standaardwaarde is `"2"` en dit geldt voor de meeste domeinen.

```js
// Manually set fpCookieDomainPeriods for domains with a period in its suffix, such as www.example.co.uk
s.fpCookieDomainPeriods = "3";

// Detect if a URL has a domain suffix with an extra period, and set s.fpCookieDomainPeriods automatically
document.URL.indexOf(".co.") > 0 ? s.fpCookieDomainPeriods = "3" : s.fpCookieDomainPeriods = "2";
```
