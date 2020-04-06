---
title: cookieLifetime
description: Overschrijf de vervaldatum voor cookies die door AppMeasurement worden gemaakt.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# cookieLifetime

Cookies die door AppMeasurement worden ingesteld, hebben doorgaans een vervaldatum van 2 jaar. Gebruik de `cookieLifetime` variabele om de vervaldatum voor koekjes met voeten te treden die door AppMeasurement worden geplaatst.

>[!NOTE] Deze variabele is van invloed op unieke aantallen bezoekers en attributie. Wees voorzichtig wanneer u deze variabele instelt.

## Cookie Lifetime in Adobe Experience Platform Launch

Cookie Lifetime is een vervolgkeuzelijst onder de [!UICONTROL Cookies] accordeon wanneer u de extensie Adobe Analytics configureert.

1. Meld u aan bij [launch.adobe.com](https://launch.adobe.com) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Extensions] tabblad en klik vervolgens op de [!UICONTROL Configure] knop onder Adobe Analytics.
4. Vouw de [!UICONTROL Cookies] accordeon uit, zodat het [!UICONTROL Cookie Lifetime] vervolgkeuzemenu zichtbaar wordt.

Deze vervolgkeuzelijst bevat de volgende waarden:

* **Standaard**: Cookie verloopt na twee jaar.
* **Geen**: AppMeasurement stelt geen cookies in.
* **Sessie**: De cookie verloopt aan het einde van de sessie van de bezoeker.
* **Seconden**: Het cookie verloopt nadat het opgegeven aantal seconden is verstreken. Als u deze vervolgkeuzelijst bijvoorbeeld instelt op [!UICONTROL Seconds] en plaatst `86400` in het aangepaste veld, verlopen cookies na precies 24 uur.

## s.cookieLifetime in aangepaste code-editor voor AppMeasurement en Launch

De `s.cookieLifetime` variabele is een tekenreeks die de vervaldatum bepaalt van cookies die door AppMeasurement zijn ingesteld.

* Indien ingesteld op `SESSION`, verlopen cookies die door AppMeasurement zijn ingesteld, nadat de browsersessie is voltooid.
* Indien ingesteld op `NONE`, probeert AppMeasurement geen cookies in te stellen.
* Indien ingesteld op een tekenreeks met een geheel getal, verlopen cookies die door AppMeasurement zijn ingesteld, nadat het opgegeven aantal seconden is verstreken.

```js
// Expire cookies after each session
s.cookieLifetime = "SESSION";

// Expire cookies after exactly 24 hours
s.cookieLifetime = "86400";

