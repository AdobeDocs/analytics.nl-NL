---
title: cookieDomainPeriods
description: Help AppMeasurement weet welk domein cookies moeten worden opgeslagen als het achtervoegsel van uw domein een punt bevat.
feature: Variables
exl-id: c426d6a7-4521-4d50-bb7d-1664920618d8
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '308'
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

## Domeinperiodes met de SDK van het Web

De SDK van het Web kan het correcte domein van de koekjesopslag zonder deze variabele bepalen.

## Domeinperioden die de Adobe Analytics-extensie gebruiken

Domeinperioden is een veld onder de [!UICONTROL Cookies] accordeon bij het configureren van de Adobe Analytics-extensie.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de gewenste tageigenschap.
1. Ga naar de [!UICONTROL Extensions] en klikt u op de knop **[!UICONTROL Configure]** onder Adobe Analytics.
1. Breid uit [!UICONTROL Cookies] accordion, die de [!UICONTROL Domain Periods] veld.

Stel dit veld in op `3` alleen in domeinen die een punt in zijn achtervoegsel bevatten. Anders kan dit veld leeg blijven.

## s.cookieDomainPeriods in AppMeasurement en de aangepaste code-editor van de extensie Analytics

De `cookieDomainPeriods` variabele is een tekenreeks die doorgaans wordt ingesteld op `"3"`, alleen op domeinen die een punt in het achtervoegsel bevatten. De standaardwaarde is `"2"`, waarin de meeste domeinen passen.

```js
// Manually set cookieDomainPeriods for domains with a period in its suffix, such as www.example.co.uk
s.cookieDomainPeriods = "3";

// Detect if a URL has a domain suffix with an extra period, and set s.cookieDomainPeriods automatically
document.URL.indexOf(".co.") > 0 ? s.cookieDomainPeriods = "3" : s.cookieDomainPeriods = "2";
```
