---
title: cookieLifetime
description: Overschrijf de vervaldatum voor cookies die AppMeasurement maakt.
feature: Variables
exl-id: 2cd64301-9f12-4e77-abae-af431e4b499d
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 0%

---

# cookieLifetime

Cookies die door AppMeasurement worden ingesteld, hebben doorgaans een vervaldatum van 2 jaar. Gebruik de `cookieLifetime` variabele om de vervaldatum voor cookies te overschrijven die is ingesteld door AppMeasurement.

>[!NOTE]
>
>Deze variabele is van invloed op unieke aantallen bezoekers en attributie. Wees voorzichtig wanneer u deze variabele instelt.

## Cookie Lifetime met de Web SDK

De SDK van het Web biedt nog geen aanpassing aan het leven van koekjes aan die het plaatst.

## Cookie Lifetime met de Adobe Analytics-extensie

Cookie Lifetime is een vervolgkeuzelijst onder de [!UICONTROL Cookies] accordeon bij het configureren van de Adobe Analytics-extensie.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de gewenste tageigenschap.
1. Ga naar de [!UICONTROL Extensions] en klikt u op de knop **[!UICONTROL Configure]** onder Adobe Analytics.
1. Breid uit [!UICONTROL Cookies] accordion, die de [!UICONTROL Cookie Lifetime] vervolgkeuzelijst.

Deze vervolgkeuzelijst bevat de volgende waarden:

* **Standaard**: Cookie verloopt na twee jaar.
* **Geen**: AppMeasurement stelt geen cookies in.
* **Sessie**: Cookie verloopt aan het einde van de sessie van de bezoeker.
* **Seconden**: Cookie verloopt nadat het opgegeven aantal seconden is verstreken. Stel deze vervolgkeuzelijst bijvoorbeeld in op [!UICONTROL Seconds] en plaatsing `86400` in het aangepaste veld worden cookies na precies 24 uur afgedwongen.

## s.cookieLifetime in AppMeasurement en de aangepaste code-editor voor de extensie Analytics

De `s.cookieLifetime` variabele is een tekenreeks die de vervaldatum bepaalt van cookies die door het AppMeasurement worden ingesteld.

* Indien ingesteld op `SESSION`cookies die zijn ingesteld door AppMeasurement verlopen nadat de browsersessie is voltooid.
* Indien ingesteld op `NONE`AppMeasurement probeert niet cookies in te stellen.
* Indien ingesteld op een tekenreeks met een geheel getal, verlopen cookies die door het AppMeasurement zijn ingesteld nadat het opgegeven aantal seconden is verstreken.

```js
// Expire cookies after each session
s.cookieLifetime = "SESSION";

// Expire cookies after exactly 24 hours
s.cookieLifetime = "86400";
```
