---
title: cookieDomainPeriods
description: Help AppMeasurement weet welk domein cookies moeten worden opgeslagen als het achtervoegsel van uw domein een punt bevat.
exl-id: c426d6a7-4521-4d50-bb7d-1664920618d8
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---

# cookieDomainPeriods

AppMeasurement bepaalt zijn koekjesplaats door het domein en domeinachtervoegsel te bekijken. Voor domeinen zoals `example.com`, plaatst AppMeasurement koekjes in de correcte plaats. Voor andere domeinen, zoals `example.co.uk`, kan AppMeasurement echter per ongeluk cookies instellen op `co.uk`. De meeste browsers weigeren cookies die op dit ongeldige domein zijn ingesteld, waardoor problemen met de identificatie van de bezoeker ontstaan.

Met de variabele `cookieDomainPeriods` kan AppMeasurement bepalen waar Analytics-cookies worden ingesteld door aan te roepen dat het domeinachtervoegsel een extra periode bevat. Met deze variabele kan AppMeasurement de extra periode in het domeinachtervoegsel aanpassen en cookies instellen op de juiste locatie.

* Voor domeinen zoals `example.com` of `www.example.com`, te hoeven deze variabele niet worden geplaatst. Indien nodig, kunt u deze variabele plaatsen aan `"2"`.
* Voor domeinen zoals `example.co.uk` of `www.example.co.jp`, plaats deze variabele aan `"3"`.

>[!IMPORTANT]
>
>Houd geen rekening met subdomeinen voor deze variabele. Stel bijvoorbeeld `cookieDomainPeriods` niet in op de voorbeeld-URL `store.toys.example.com`. AppMeasurement door gebrek erkent dat de koekjes op `example.com`, zelfs op URLs met vele subdomeinen zouden moeten worden opgeslagen.

## Domeinperioden met tags in Adobe Experience Platform

Domeintermijnen is een veld onder de accordeon [!UICONTROL Cookies] wanneer u de extensie Adobe Analytics configureert.

1. Meld u aan bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de gewenste eigenschap.
1. Ga naar het [!UICONTROL Extensions] lusje, dan klik [!UICONTROL Configure] knoop onder Adobe Analytics.
1. Vouw de accordeon [!UICONTROL Cookies] uit, zodat het veld [!UICONTROL Domain Periods] zichtbaar wordt.

Stel dit veld alleen in op `3` in domeinen met een punt in het achtervoegsel. Anders kan dit veld leeg blijven.

## s.cookieDomainPeriods in AppMeasurement en de aangepaste code-editor

De `cookieDomainPeriods` variabele is een koord dat typisch aan `"3"`, slechts op domeinen wordt geplaatst die een periode in zijn achtervoegsel bevatten. De standaardwaarde is `"2"`, die geschikt is voor de meeste domeinen.

```js
// Manually set cookieDomainPeriods for domains with a period in its suffix, such as www.example.co.uk
s.cookieDomainPeriods = "3";

// Detect if a URL has a domain suffix with an extra period, and set s.cookieDomainPeriods automatically
document.URL.indexOf(".co.") > 0 ? s.cookieDomainPeriods = "3" : s.cookieDomainPeriods = "2";
```
