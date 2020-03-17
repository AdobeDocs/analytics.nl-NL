---
title: cookieDomainPeriods
description: Help AppMeasurement weet welk domein cookies moeten worden opgeslagen als het achtervoegsel van uw domein een punt bevat.
translation-type: tm+mt
source-git-commit: ''

---


# cookieDomainPeriods

AppMeasurement bepaalt zijn koekjesplaats door het domein en domeinachtervoegsel te bekijken. Voor domeinen zoals `example.com`, plaatst AppMeturement koekjes in de correcte plaats. Voor andere domeinen, zoals `example.co.uk`AppMeasurement, kunnen cookies echter per ongeluk worden ingesteld `co.uk`. De meeste browsers weigeren cookies die op dit ongeldige domein zijn ingesteld, waardoor problemen met de identificatie van de bezoeker ontstaan.

Met de `cookieDomainPeriods` variabele kan AppMeasurement bepalen waar Analytics-cookies worden ingesteld door aan te roepen dat het domeinachtervoegsel een extra punt bevat. Met deze variabele kan AppMeasurement de extra periode in het domeinachtervoegsel aanpassen en cookies instellen op de juiste locatie.

* Voor domeinen zoals `example.com` of `www.example.com`, te hoeven deze variabele niet worden geplaatst. Indien nodig, kunt u deze variabele plaatsen aan `"2"`.
* Voor domeinen zoals `example.co.uk` of `www.example.co.jp`, plaats deze variabele aan `"3"`.

> [!IMPORTANT] Houd geen rekening met subdomeinen voor deze variabele. Stel bijvoorbeeld niet in `cookieDomainPeriods` de voorbeeld-URL `store.toys.example.com`. AppMeasurement herkent standaard dat cookies moeten worden opgeslagen op `example.com`, zelfs op URL&#39;s met veel subdomeinen.

## Domeinperioden in het starten van het Adobe Experience Platform

Domeinperioden is een veld onder de [!UICONTROL Cookies] accordeon tijdens het configureren van de extensie Adobe Analytics.

1. Meld u aan bij [launch.adobe.com](https://launch.adobe.com) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Extensions] tabblad en klik vervolgens op de [!UICONTROL Configure] knop onder Adobe Analytics.
4. Breid de accordeon uit, die het [!UICONTROL Cookies] [!UICONTROL Domain Periods] veld onthult.

Stel dit veld `3` alleen in op domeinen met een punt in het achtervoegsel. Anders kan dit veld leeg blijven.

## s.cookieDomainPeriods in AppMeasurement en Launch, aangepaste code-editor

De `cookieDomainPeriods` variabele is een tekenreeks die doorgaans wordt ingesteld op `"3"`alleen domeinen die een punt in het achtervoegsel bevatten. De standaardwaarde hiervan is `"2"`die geschikt is voor de meeste domeinen.

```js
// Manually set cookieDomainPeriods for domains with a period in its suffix, such as www.example.co.uk
s.cookieDomainPeriods = "3";

// Detect if a URL has a domain suffix with an extra period, and set s.cookieDomainPeriods automatically
document.URL.indexOf(".co.") > 0 ? s.cookieDomainPeriods = "3" : s.cookieDomainPeriods = "2";
```
