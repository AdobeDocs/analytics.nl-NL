---
title: cookieLifetime
description: Overschrijf de vervaldatum voor cookies die door AppMeasurement worden gemaakt.
feature: Variables
exl-id: 2cd64301-9f12-4e77-abae-af431e4b499d
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 0%

---

# cookieLifetime

Cookies die door AppMeasurement worden ingesteld, hebben doorgaans een vervaldatum van 2 jaar. Gebruik de `cookieLifetime` variabele om de vervaldatum voor koekjes met voeten te treden die door AppMeasurement wordt geplaatst.

>[!NOTE]
>
>Deze variabele is van invloed op unieke aantallen bezoekers en attributie. Wees voorzichtig wanneer u deze variabele instelt.

## Cookie Lifetime met de SDK van het Web

De SDK van het Web biedt nog geen aanpassing aan het leven van koekjes aan die het plaatst.

## Cookie Lifetime met de Adobe Analytics-extensie

Cookie Lifetime is een vervolgkeuzelijst onder [!UICONTROL Cookies] accordeon bij het configureren van de Adobe Analytics-extensie.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de gewenste tageigenschap.
1. Ga naar de [!UICONTROL Extensions] en klikt u op de knop **[!UICONTROL Configure]** onder Adobe Analytics.
1. Breid uit [!UICONTROL Cookies] accordion, die de [!UICONTROL Cookie Lifetime] vervolgkeuzelijst.

Deze vervolgkeuzelijst bevat de volgende waarden:

* **Standaard**: Cookie verloopt na twee jaar.
* **Geen**: AppMeasurement stelt geen cookies in.
* **Sessie**: De cookie verloopt aan het einde van de sessie van de bezoeker.
* **Seconden**: Het cookie verloopt nadat het opgegeven aantal seconden is verstreken. Stel deze vervolgkeuzelijst bijvoorbeeld in op [!UICONTROL Seconds] en plaatsing `86400` in het aangepaste veld worden cookies na precies 24 uur afgedwongen.

## s.cookieLifetime in AppMeasurement en de aangepaste code-editor voor de extensie Analytics

De `s.cookieLifetime` variabele is een tekenreeks die de vervaldatum bepaalt van cookies die door AppMeasurement zijn ingesteld.

* Indien ingesteld op `SESSION`, verlopen cookies die door AppMeasurement zijn ingesteld nadat de browsersessie is voltooid.
* Indien ingesteld op `NONE`, AppMeasurement probeert niet cookies in te stellen.
* Indien ingesteld op een tekenreeks met een geheel getal, verlopen cookies die door AppMeasurement zijn ingesteld, nadat het opgegeven aantal seconden is verstreken.

```js
// Expire cookies after each session
s.cookieLifetime = "SESSION";

// Expire cookies after exactly 24 hours
s.cookieLifetime = "86400";
```
