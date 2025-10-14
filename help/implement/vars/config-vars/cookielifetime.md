---
title: cookieLifetime
description: Overschrijf de vervaldatum voor cookies die AppMeasurement maakt.
feature: Appmeasurement Implementation
exl-id: 2cd64301-9f12-4e77-abae-af431e4b499d
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 0%

---

# cookieLifetime

Cookies die door AppMeasurement worden ingesteld, verlopen doorgaans 2 jaar. Gebruik de variabele `cookieLifetime` om de vervaldatum te overschrijven voor cookies die door AppMeasurement zijn ingesteld.

>[!NOTE]
>
>Deze variabele is van invloed op unieke aantallen bezoekers en attributie. Wees voorzichtig wanneer u deze variabele instelt.

## Cookie Lifetime via Web SDK

De SDK van het Web biedt nog geen aanpassing aan het leven van koekjes aan die het plaatst.

## Cookie Lifetime met de Adobe Analytics-extensie

Cookie Lifetime is een vervolgkeuzelijst onder de accordeon [!UICONTROL Cookies] wanneer u de Adobe Analytics-extensie configureert.

1. Login aan [&#x200B; de Inzameling van Gegevens van Adobe Experience Platform &#x200B;](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
1. Klik op de gewenste tageigenschap.
1. Ga naar de tab [!UICONTROL Extensions] en klik vervolgens op de knop **[!UICONTROL Configure]** onder Adobe Analytics.
1. Vouw de accordeon [!UICONTROL Cookies] uit, zodat de vervolgkeuzelijst [!UICONTROL Cookie Lifetime] zichtbaar wordt.

Deze vervolgkeuzelijst bevat de volgende waarden:

* **Gebrek**: Het koekje verloopt na 2 jaar.
* **niets**: AppMeasurement plaatst geen koekjes.
* **Zitting**: De cookie verloopt aan het eind van de zitting van de bezoeker.
* **Seconden**: Het koekje verloopt nadat het gespecificeerde aantal seconden is verstreken. Als u deze vervolgkeuzelijst bijvoorbeeld instelt op [!UICONTROL Seconds] en `86400` in het aangepaste veld plaatst, worden cookies na precies 24 uur gedwongen te verlopen.

## s.cookieLifetime in AppMeasurement en de aangepaste code-editor voor de extensie Analytics

De variabele `s.cookieLifetime` is een tekenreeks die de vervaldatum bepaalt van cookies die door AppMeasurement zijn ingesteld.

* Indien ingesteld op `SESSION` , verlopen cookies die door AppMeasurement zijn ingesteld nadat de browsersessie is voltooid.
* Indien ingesteld op `NONE` , probeert AppMeasurement niet cookies in te stellen.
* Als de waarde is ingesteld op een tekenreeks met een geheel getal, verlopen cookies die door AppMeasurement zijn ingesteld nadat het opgegeven aantal seconden is verstreken.

```js
// Expire cookies after each session
s.cookieLifetime = "SESSION";

// Expire cookies after exactly 24 hours
s.cookieLifetime = "86400";
```
