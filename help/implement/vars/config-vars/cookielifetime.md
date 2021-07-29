---
title: cookieLifetime
description: Overschrijf de vervaldatum voor cookies die door AppMeasurement worden gemaakt.
exl-id: 2cd64301-9f12-4e77-abae-af431e4b499d
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---

# cookieLifetime

Cookies die door AppMeasurement worden ingesteld, hebben doorgaans een vervaldatum van 2 jaar. Gebruik de `cookieLifetime` variabele om de vervaldatum voor koekjes met voeten te treden die door AppMeasurement worden geplaatst.

>[!NOTE]
>
>Deze variabele is van invloed op unieke aantallen bezoekers en attributie. Wees voorzichtig wanneer u deze variabele instelt.

## Cookie Lifetime met tags in Adobe Experience Platform

Cookie Lifetime is een vervolgkeuzelijst onder de accordeon [!UICONTROL Cookies] wanneer u de Adobe Analytics-extensie configureert.

1. Meld u aan bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de gewenste eigenschap.
1. Ga naar het [!UICONTROL Extensions] lusje, dan klik [!UICONTROL Configure] knoop onder Adobe Analytics.
1. Breid [!UICONTROL Cookies] accordeon uit, die [!UICONTROL Cookie Lifetime] dropdown openbaart.

Deze vervolgkeuzelijst bevat de volgende waarden:

* **Standaard**: Cookie verloopt na twee jaar.
* **Geen**: AppMeasurement stelt geen cookies in.
* **Sessie**: De cookie verloopt aan het einde van de sessie van de bezoeker.
* **Seconden**: Het cookie verloopt nadat het opgegeven aantal seconden is verstreken. Als u deze vervolgkeuzelijst bijvoorbeeld instelt op [!UICONTROL Seconds] en `86400` in het aangepaste veld plaatst, worden cookies na precies 24 uur gedwongen te verlopen.

## s.cookieLifetime in AppMeasurement en aangepaste code-editor

De variabele `s.cookieLifetime` is een tekenreeks die de vervaldatum bepaalt van cookies die door AppMeasurement zijn ingesteld.

* Indien ingesteld op `SESSION`, verlopen cookies die zijn ingesteld door AppMeasurement nadat de browsersessie is voltooid.
* Indien ingesteld op `NONE`, probeert AppMeasurement niet om cookies in te stellen.
* Indien ingesteld op een tekenreeks met een geheel getal, verlopen cookies die door AppMeasurement zijn ingesteld, nadat het opgegeven aantal seconden is verstreken.

```js
// Expire cookies after each session
s.cookieLifetime = "SESSION";

// Expire cookies after exactly 24 hours
s.cookieLifetime = "86400";
```
