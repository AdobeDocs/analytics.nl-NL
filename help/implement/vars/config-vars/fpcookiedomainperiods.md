---
title: cookieDomainPeriods
description: Help AppMeasurement weet welk domein cookies moeten worden opgeslagen als het achtervoegsel van uw domein een punt bevat.
exl-id: e994a188-1dab-4bf0-912b-cd2f6a1032e0
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 0%

---

# fpCookieDomainPeriods

Met de variabele `fpCookieDomainPeriods` kan AppMeasurement bepalen waar Analytics-cookies worden ingesteld door aan te roepen dat het domeinachtervoegsel een extra periode bevat. Met deze variabele kan AppMeasurement de extra periode in het domeinachtervoegsel aanpassen en cookies instellen op de juiste locatie. Het erft de waarde van [`cookieDomainPeriods`](cookiedomainperiods.md), maar is nog een beste praktijk om te plaatsen als u een implementatie van het eerste-partijkoekje gebruikt.

* Voor domeinen zoals `example.com` of `www.example.com`, te hoeven deze variabele niet worden geplaatst. Indien nodig, kunt u deze variabele plaatsen aan `"2"`.
* Voor domeinen zoals `example.co.uk` of `www.example.co.jp`, plaats deze variabele aan `"3"`.

>[!IMPORTANT]
>
>Houd geen rekening met subdomeinen voor deze variabele. Stel bijvoorbeeld `fpCookieDomainPeriods` niet in op de voorbeeld-URL `store.toys.example.com`. AppMeasurement door gebrek erkent dat de koekjes op `example.com`, zelfs op URLs met vele subdomeinen zouden moeten worden opgeslagen.

## Domeinperioden van de eerste partij met tags in Adobe Experience Platform

De Periodes van het Domein van de eerste partij is een gebied onder [!UICONTROL Cookies] accordion wanneer het vormen van de uitbreiding van Adobe Analytics.

1. Meld u aan bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Extensions] lusje, dan klik [!UICONTROL Configure] knoop onder Adobe Analytics.
4. Vouw de accordeon [!UICONTROL Cookies] uit, zodat het veld [!UICONTROL First-party Domain Periods] zichtbaar wordt.

Stel dit veld alleen in op `3` in domeinen met een punt in het achtervoegsel. Anders kan dit veld leeg blijven.

## s.fpCookieDomainPeriods in AppMeasurement en de douane-code-editor

De `fpCookieDomainPeriods` variabele is een koord dat typisch aan `"3"`, slechts op domeinen wordt geplaatst die een periode in zijn achtervoegsel bevatten. De standaardwaarde is `"2"`, die geschikt is voor de meeste domeinen.

```js
// Manually set fpCookieDomainPeriods for domains with a period in its suffix, such as www.example.co.uk
s.fpCookieDomainPeriods = "3";

// Detect if a URL has a domain suffix with an extra period, and set s.fpCookieDomainPeriods automatically
document.URL.indexOf(".co.") > 0 ? s.fpCookieDomainPeriods = "3" : s.fpCookieDomainPeriods = "2";
```
