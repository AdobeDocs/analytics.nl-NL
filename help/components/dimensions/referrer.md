---
title: Referrer
description: De URL waar een bezoeker zich bevond voordat hij op uw site klikte.
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 0%

---


# Referrer

De dimensie &#39;Referrer&#39; rapporteert welke URL&#39;s bezoekers hadden wanneer ze door klikten om uw site te bereiken. Deze dimensie is nuttig om te begrijpen welke specifieke URLs het meeste verkeer aan uw plaats drijft. De externe URL moet een koppeling bevatten en een bezoeker moet erop klikken om de waarde van de dimensie weer te geven.

>[!IMPORTANT]
>
>U moet de [Interne filters](/help/admin/admin/internal-url-filter-admin.md) van URL van uw rapportreeks vormen om deze dimensie te gebruiken. Als u interne URL-filters niet configureert, kunt u interne URL&#39;s opnemen of voorkomen dat externe URL&#39;s worden weergegeven.

## Deze dimensie vullen met gegevens

Deze dimensie vereist configuratie in de interface van Analytics en gegevens in beeldverzoeken.

* Binnen uw implementatie, wint deze afmeting gegevens van het [`r` vraagkoord](/help/implement/validate/query-parameters.md) in beeldverzoeken terug. AppMeturement verzamelt deze gegevens met behulp van de JavaScript-variabele `document.referrer` in de browser. Als u een bibliotheek AppMeasurement gebruikt (zoals door Adobe Experience Platform Launch), werkt deze afmeting uit de doos. Als u een methode van de gegevensinzameling buiten AppMeasurement (zoals door API) gebruikt, zorg ervoor dat u de parameter van het `r` vraagkoord in beeldverzoeken omvat.
* Binnen de interface van Analytics, moet u de [Interne filters](/help/admin/admin/internal-url-filter-admin.md)van URL van uw rapportreeks vormen. Als u interne URL-filters niet configureert, kunt u interne URL&#39;s opnemen of voorkomen dat externe URL&#39;s worden weergegeven.

## Dimensiewaarden

Dimensiewaarden zijn URL&#39;s waarop bezoekers klikken om uw site te doorzoeken. Als een treffer geen verwijzingsgegevens heeft, groepeert het zich onder de afmetingswaarde `"Typed/Bookmarked"`. Deze afmetingswaarde betekent dat er geen verwijzingswaarde was, zoals als de bezoeker het browseradres handmatig in de adresbalk had getypt of op een bladwijzer had geklikt.
