---
title: cookieDomainPeriods
description: Help AppMeasurement weet welk domein cookies moeten worden opgeslagen als het achtervoegsel van uw domein een punt bevat.
feature: Variables
exl-id: c426d6a7-4521-4d50-bb7d-1664920618d8
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---

# cookieDomainPeriods

AppMeasurement bepaalt zijn koekjesplaats door het domein en domeinachtervoegsel te bekijken. Voor domeinen zoals `example.com`, AppMeasurement stelt cookies in de juiste locatie in. Voor andere domeinen, zoals `example.co.uk`, AppMeasurement kan cookies per ongeluk instellen op `co.uk`. De meeste browsers weigeren cookies die op dit ongeldige domein zijn ingesteld, wat problemen met de identificatie van de bezoeker veroorzaakt.

De `cookieDomainPeriods` Met de variabele kan AppMeasurement bepalen waar Analytics-cookies worden ingesteld door aan te roepen dat het domeinachtervoegsel een extra periode bevat. Met deze variabele kan AppMeasurement de extra periode in het domeinachtervoegsel aanpassen en cookies instellen op de juiste locatie.

* Voor domeinen zoals `example.com` of `www.example.com`hoeft u deze variabele niet in te stellen. Indien nodig kunt u deze variabele instellen op `"2"`.
* Voor domeinen zoals `example.co.uk` of `www.example.co.jp`stelt u deze variabele in op `"3"`.

>[!IMPORTANT]
>
>Houd geen rekening met subdomeinen voor deze variabele. Niet instellen `cookieDomainPeriods` in de voorbeeld-URL `store.toys.example.com`. AppMeasurement herkent standaard dat cookies moeten worden opgeslagen op `example.com`, zelfs op URL&#39;s met veel subdomeinen.

## Domeinperioden met tags in Adobe Experience Platform

Domeinperioden is een veld onder de [!UICONTROL Cookies] accordeon bij het configureren van de Adobe Analytics-extensie.

1. Aanmelden bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de gewenste eigenschap.
1. Ga naar de [!UICONTROL Extensions] en klikt u op de knop [!UICONTROL Configure] onder Adobe Analytics.
1. Breid uit [!UICONTROL Cookies] accordion, die de [!UICONTROL Domain Periods] veld.

Stel dit veld in op `3` alleen in domeinen die een punt in zijn achtervoegsel bevatten. Anders kan dit veld leeg blijven.

## s.cookieDomainPeriods in AppMeasurement en de aangepaste code-editor

De `cookieDomainPeriods` variabele is een tekenreeks die doorgaans wordt ingesteld op `"3"`, alleen op domeinen die een punt in het achtervoegsel bevatten. De standaardwaarde is `"2"`, waarin de meeste domeinen passen.

```js
// Manually set cookieDomainPeriods for domains with a period in its suffix, such as www.example.co.uk
s.cookieDomainPeriods = "3";

// Detect if a URL has a domain suffix with an extra period, and set s.cookieDomainPeriods automatically
document.URL.indexOf(".co.") > 0 ? s.cookieDomainPeriods = "3" : s.cookieDomainPeriods = "2";
```
