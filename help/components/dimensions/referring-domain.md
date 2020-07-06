---
title: Verwijzen naar domein
description: Het overkoepelende domein waarop een bezoeker zich bevond voordat hij naar uw site klikte.
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '328'
ht-degree: 0%

---


# Verwijzen naar domein

De dimensie &#39;Verwijzend domein&#39; rapporteert welke domeinen bezoekers door klikken om uw plaats te bereiken. Deze dimensie is nuttig om te begrijpen welke derdeplaatsen het meeste verkeer aan van u drijven. Er moet een koppeling op de externe site staan en een bezoeker moet erop klikken om de waarde van de dimensie weer te geven.

>[!IMPORTANT]
>
>U moet de [Interne filters](/help/admin/admin/internal-url-filter-admin.md) van URL van uw rapportreeks vormen om deze dimensie te gebruiken. Als u interne URL-filters niet configureert, kan dit interne domeinen of externe domeinen omvatten.

## Deze dimensie vullen met gegevens

Deze dimensie vereist configuratie in de interface van Analytics en gegevens in beeldverzoeken.

* Binnen uw implementatie, wint deze afmeting gegevens van het [`r` vraagkoord](/help/implement/validate/query-parameters.md) in beeldverzoeken terug. AppMeturement verzamelt deze gegevens met behulp van de JavaScript-variabele `document.referrer` in de browser. Als u een bibliotheek AppMeasurement gebruikt (zoals door Adobe Experience Platform Launch), werkt deze afmeting uit de doos. Als u een methode van de gegevensinzameling buiten AppMeasurement (zoals door API) gebruikt, zorg ervoor dat u de parameter van het `r` vraagkoord in beeldverzoeken omvat.
* Binnen de interface van Analytics, moet u de [Interne filters](/help/admin/admin/internal-url-filter-admin.md)van URL van uw rapportreeks vormen. Als u interne URL-filters niet configureert, kan dit interne domeinen of externe domeinen omvatten.

Adobe gaat door met het verwijzen naar het domein voor een bezoek. Als een bezoeker een koppeling verlaat en doorklikt op een ander domein binnen één bezoek, wordt de nieuwe waarde bijgewerkt en blijft deze voor de rest van het bezoek bestaan. Zie [Origineel verwijzend domein](original-referring-domain.md)als u alleen de oorspronkelijke waarde wilt zien.

## Dimensiewaarden

Dimensiewaarden omvatten domeinen waarop bezoekers klikken om uw site te doorzoeken. Als een hit geen verwijzingsgegevens heeft (ingesteld of blijvend), groepeert deze zich onder de waarde van de dimensie `"Typed/Bookmarked"`. Deze afmetingswaarde betekent dat er geen verwijzingswaarde was, zoals als de bezoeker het browseradres handmatig in de adresbalk had getypt of op een bladwijzer had geklikt.
