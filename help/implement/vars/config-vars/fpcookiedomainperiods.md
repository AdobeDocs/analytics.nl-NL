---
title: fpcookieDomainPeriods
description: Help het AppMeasurement te begrijpen welk domein cookies moeten worden opgeslagen als het domein een punt in het achtervoegsel heeft.
feature: Variables
exl-id: e994a188-1dab-4bf0-912b-cd2f6a1032e0
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 0%

---

# fpCookieDomainPeriods

De `fpCookieDomainPeriods` de variabele helpt AppMeasurement bepalen waar de koekjes van Analytics door te roepen worden geplaatst dat het domeinachtervoegsel een extra periode in het heeft. Met deze variabele kan AppMeasurement de extra periode in het domeinachtervoegsel aanpassen en cookies instellen op de juiste locatie. De waarde van [`cookieDomainPeriods`](cookiedomainperiods.md), maar het is nog steeds de beste manier om in te stellen of u een cookie-implementatie van de eerste fabrikant gebruikt.

* Voor domeinen zoals `example.com` of `www.example.com`hoeft u deze variabele niet in te stellen. Indien nodig, kunt u deze variabele instellen op `"2"`.
* Voor domeinen zoals `example.co.uk` of `www.example.co.jp`stelt u deze variabele in op `"3"`.

>[!IMPORTANT]
>
>Houd geen rekening met subdomeinen voor deze variabele. Niet instellen `fpCookieDomainPeriods` in de voorbeeld-URL `store.toys.example.com`. AppMeasurement herkent standaard dat cookies moeten worden opgeslagen op `example.com`, zelfs op URL&#39;s met veel subdomeinen.

## De periodes van het eerste partijdomein die SDK van het Web gebruiken

De SDK van het Web kan het correcte domein van de koekjesopslag zonder deze variabele bepalen.

## Domeintermijnen van de eerste partij die de uitbreiding van Adobe Analytics gebruiken

Domeintermijnen van de eerste partij is een gebied onder [!UICONTROL Cookies] accordeon bij het configureren van de Adobe Analytics-extensie.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste tageigenschap.
3. Ga naar de [!UICONTROL Extensions] en klikt u op de knop **[!UICONTROL Configure]** onder Adobe Analytics.
4. Breid uit [!UICONTROL Cookies] accordion, die de [!UICONTROL First-party Domain Periods] veld.

Stel dit veld in op `3` alleen in domeinen die een punt in zijn achtervoegsel bevatten. Anders kan dit veld leeg blijven.

## s.fpCookieDomainPeriods in AppMeasurement en de de redacteur van de de uitbreidingsdouanecode van de Analyse

De `fpCookieDomainPeriods` variabele is een tekenreeks die doorgaans wordt ingesteld op `"3"`, alleen op domeinen die een punt in het achtervoegsel bevatten. De standaardwaarde is `"2"`, waarin de meeste domeinen kunnen worden opgenomen.

```js
// Manually set fpCookieDomainPeriods for domains with a period in its suffix, such as www.example.co.uk
s.fpCookieDomainPeriods = "3";

// Detect if a URL has a domain suffix with an extra period, and set s.fpCookieDomainPeriods automatically
document.URL.indexOf(".co.") > 0 ? s.fpCookieDomainPeriods = "3" : s.fpCookieDomainPeriods = "2";
```
