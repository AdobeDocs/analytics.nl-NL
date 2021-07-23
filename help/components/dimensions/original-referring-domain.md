---
title: Origineel verwijzend domein
description: Het eerste verwijzende domein waarop een bezoeker zich bevond voordat hij op uw site klikte.
exl-id: 6b9ac662-a79a-477b-8612-7980da7cfadd
source-git-commit: 562ed0e190954b7687fa79efaf5c5c54eb202af8
workflow-type: tm+mt
source-wordcount: '408'
ht-degree: 0%

---

# Origineel verwijzend domein

De dimensie &#39;Origineel verwijzend domein&#39; rapporteert het eerste verwijzende domein dat een bezoeker door klikte om uw plaats te bereiken. Als deze eenmaal is ingesteld, bevat deze dezelfde waarde voor de gehele levensduur van die bezoekersidentiteitskaart. Deze dimensie is nuttig om te begrijpen welke derdeplaatsen oorspronkelijk verkeer aan uw plaats drijven.

>[!IMPORTANT]
>
>U moet [Interne filters URL ](/help/admin/admin/internal-url-filter-admin.md) van uw rapportreeks vormen om deze afmeting te gebruiken. Als u interne URL-filters niet configureert, kan dit interne domeinen of externe domeinen omvatten.

## Deze dimensie vullen met gegevens

Deze dimensie vereist configuratie in zowel de interface Analytics als uw implementatie.

* Binnen uw implementatie, wint deze afmeting gegevens van [`r` vraagkoord](/help/implement/validate/query-parameters.md) in beeldverzoeken terug. AppMeasurement verzamelt deze gegevens met behulp van de JavaScript-variabele `document.referrer` in de browser. Als u een AppMeasurement-bibliotheek gebruikt (bijvoorbeeld via tags in Adobe Experience Platform), werkt deze dimensie buiten het vak. Als u een methode van de gegevensinzameling buiten AppMeasurement (zoals door API) gebruikt, zorg ervoor dat u `r` parameter van het vraagkoord in beeldverzoeken omvat.
* Binnen de interface van Analytics, moet u [Interne filters URL van uw rapportreeks ](/help/admin/admin/internal-url-filter-admin.md) vormen. Als u interne URL-filters niet configureert, kan dit interne domeinen of externe domeinen omvatten.

Adobe blijft het oorspronkelijke verwijzende domein voor het leven van een bezoeker. Wanneer een bezoeker op een ander domein een koppeling verlaat en erop klikt, wordt de nieuwe waarde niet opgenomen. Als u nieuwe waarden wilt zien, zie [Verwijzend domein](referring-domain.md).

## Dimension-items

Dimension-items bevatten domeinen waarop bezoekers naar uw site klikken. Als een hit geen verwijzingsgegevens heeft (ingesteld of blijvend), groepeert deze zich onder het dimensie-item `"None"`. Dit afmetingsitem betekent dat er geen verwijzingswaarde is, bijvoorbeeld dat de bezoeker het browseradres handmatig in de adresbalk heeft getypt of op een bladwijzer heeft geklikt.

## Verwijzen van domein naar oorspronkelijk verwijzend domein vergelijken

Verwijzend domein kan tussen bezoeken veranderen. Een bezoeker arriveert bijvoorbeeld via `google.com` naar uw site en een week later komt deze via `twitter.com` aan bij uw site. Uiteindelijk kopen ze op uw site. Als `twitter.com` het verwijzingsdomein gebruikt als de dimensie met de laatste aanraakattributie, krijgt krediet voor de aankoop. Als u Origineel verwijzend domein als dimensie gebruikt, krijgt `google.com` krediet voor de aankoop ongeacht attributiemodel.

Het oorspronkelijke verwijzende domein verandert nooit voor het volledige leven van een bepaalde bezoekersidentiteitskaart
