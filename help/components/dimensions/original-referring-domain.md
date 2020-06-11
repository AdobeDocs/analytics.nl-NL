---
title: Origineel verwijzend domein
description: Het eerste verwijzende domein waarop een bezoeker zich bevond voordat hij op uw site klikte.
translation-type: tm+mt
source-git-commit: ad206649488a1a2dead717cdfe53f4c630ba3f3b
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 0%

---


# Origineel verwijzend domein

De dimensie &#39;Origineel verwijzend domein&#39; rapporteert het eerste verwijzende domein dat een bezoeker door klikte om uw plaats te bereiken. Als deze eenmaal is ingesteld, bevat deze dezelfde waarde voor de gehele levensduur van die bezoekersidentiteitskaart. Deze dimensie is nuttig om te begrijpen welke derdeplaatsen oorspronkelijk verkeer aan uw plaats drijven.

## Deze dimensie vullen met gegevens

Deze dimensie vereist configuratie in zowel de interface Analytics als uw implementatie.

* Binnen uw implementatie, wint deze afmeting gegevens van het [`r` vraagkoord](/help/implement/validate/query-parameters.md) in beeldverzoeken terug. AppMeturement verzamelt deze gegevens met behulp van de JavaScript-variabele `document.referrer` in de browser. Als u een AppMeturement-bibliotheek gebruikt (bijvoorbeeld via Adobe Experience Platform Launch), werkt deze dimensie buiten het vak. Als u een methode van de gegevensinzameling buiten AppMeasurement (zoals door API) gebruikt, zorg ervoor dat u de parameter van het `r` vraagkoord in beeldverzoeken omvat.
* Binnen de interface van Analytics, moet u de [Interne filters](/help/admin/admin/internal-url-filter-admin.md)van URL van uw rapportreeks vormen. Als u interne URL-filters niet configureert, kan dit interne domeinen of externe domeinen omvatten.

Adobe behoudt het oorspronkelijke verwijzende domein voor de levensduur van een bezoeker. Wanneer een bezoeker op een ander domein een koppeling verlaat en erop klikt, wordt de nieuwe waarde niet opgenomen. Zie Domein [](referring-domain.md)verwijzen als u nieuwe waarden wilt zien.

## Dimensiewaarden

Dimensiewaarden omvatten domeinen waarop bezoekers klikken om uw site te doorzoeken. Als een hit geen verwijzingsgegevens heeft (ingesteld of blijvend), groepeert deze zich onder de waarde van de dimensie `"None"`. Deze afmetingswaarde betekent dat er geen verwijzingswaarde was, zoals als de bezoeker het browseradres handmatig in de adresbalk had getypt of op een bladwijzer had geklikt.
