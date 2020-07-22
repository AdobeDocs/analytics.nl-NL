---
title: Origineel verwijzend domein
description: Het eerste verwijzende domein waarop een bezoeker zich bevond voordat hij op uw site klikte.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 0%

---


# Origineel verwijzend domein

De dimensie &#39;Origineel verwijzend domein&#39; rapporteert het eerste verwijzende domein dat een bezoeker door klikte om uw plaats te bereiken. Als deze eenmaal is ingesteld, bevat deze dezelfde waarde voor de gehele levensduur van die bezoekersidentiteitskaart. Deze dimensie is nuttig om te begrijpen welke derdeplaatsen oorspronkelijk verkeer aan uw plaats drijven.

## Deze dimensie vullen met gegevens

Deze dimensie vereist configuratie in zowel de interface van Analytics als uw implementatie.

* Binnen uw implementatie, wint deze afmeting gegevens van het [`r` vraagkoord](/help/implement/validate/query-parameters.md) in beeldverzoeken terug. AppMeturement verzamelt deze gegevens met behulp van de JavaScript-variabele `document.referrer` in de browser. Als u een bibliotheek AppMeasurement gebruikt (zoals door Adobe Experience Platform Launch), werkt deze afmeting uit de doos. Als u een methode van de gegevensinzameling buiten AppMeasurement (zoals door API) gebruikt, zorg ervoor dat u de parameter van het `r` vraagkoord in beeldverzoeken omvat.
* Binnen de interface van Analytics, moet u de [Interne filters](/help/admin/admin/internal-url-filter-admin.md)van URL van uw rapportreeks vormen. Als u interne URL-filters niet configureert, kan dit interne domeinen of externe domeinen omvatten.

Adobe behoudt het oorspronkelijke verwijzende domein voor de levensduur van een bezoeker. Wanneer een bezoeker op een ander domein een koppeling verlaat en erop klikt, wordt de nieuwe waarde niet opgenomen. Zie Domein [](referring-domain.md)verwijzen als u nieuwe waarden wilt zien.

## Dimensie-items

Dimensie-items omvatten domeinen waarop bezoekers naar uw site klikken. Als een hit geen verwijzingsgegevens heeft (ingesteld of blijvend), groepeert deze zich onder het dimensie-item `"None"`. Dit afmetingsitem betekent dat er geen verwijzingswaarde is, bijvoorbeeld dat de bezoeker het browseradres handmatig in de adresbalk heeft getypt of op een bladwijzer heeft geklikt.
