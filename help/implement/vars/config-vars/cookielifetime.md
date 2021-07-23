---
title: cookieLifetime
description: Overschrijf de vervaldatum voor cookies die door AppMeasurement worden gemaakt.
exl-id: 2cd64301-9f12-4e77-abae-af431e4b499d
source-git-commit: 3986084eaab81842b6ea0dbabc7bdb78e39f887a
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 0%

---

# cookieLifetime

Cookies die door AppMeasurement worden ingesteld, hebben doorgaans een vervaldatum van 2 jaar. Gebruik de `cookieLifetime` variabele om de vervaldatum voor koekjes met voeten te treden die door AppMeasurement worden geplaatst.

>[!NOTE]
>
>Deze variabele is van invloed op unieke aantallen bezoekers en attributie. Wees voorzichtig wanneer u deze variabele instelt.

## Cookie Lifetime in Adobe Experience Platform-tags

Cookie Lifetime is een vervolgkeuzelijst onder de accordeon [!UICONTROL Cookies] wanneer u de Adobe Analytics-extensie configureert.

1. Ga naar `experience.adobe.com` en meld u aan wanneer u hierom wordt gevraagd.
1. Selecteer [!UICONTROL Launch / Data Collection].
1. Klik [!UICONTROL Go to Launch / Data Collection], dan selecteer [!UICONTROL Tags].
1. Klik op de gewenste eigenschap.
1. Ga naar het [!UICONTROL Extensions] lusje, dan klik [!UICONTROL Configure] knoop onder Adobe Analytics.
1. Breid [!UICONTROL Cookies] accordeon uit, die [!UICONTROL Cookie Lifetime] dropdown openbaart.

Deze vervolgkeuzelijst bevat de volgende waarden:

* **Standaard**: Cookie verloopt na twee jaar.
* **Geen**: AppMeasurement stelt geen cookies in.
* **Sessie**: De cookie verloopt aan het einde van de sessie van de bezoeker.
* **Seconden**: Het cookie verloopt nadat het opgegeven aantal seconden is verstreken. Als u deze vervolgkeuzelijst bijvoorbeeld instelt op [!UICONTROL Seconds] en `86400` in het aangepaste veld plaatst, worden cookies na precies 24 uur gedwongen te verlopen.

## s.cookieLifetime in de redacteur van de de douanecode van AppMeturement en van de Inzameling van Gegevens

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
