---
title: Origineel verwijzend domein
description: Het eerste verwijzende domein waarop een bezoeker zich bevond voordat hij op uw site klikte.
feature: Dimensions
exl-id: 6b9ac662-a79a-477b-8612-7980da7cfadd
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: tm+mt
source-wordcount: '408'
ht-degree: 0%

---

# Origineel verwijzend domein

De dimensie &#39;Origineel verwijzend domein&#39; rapporteert het eerste verwijzende domein dat een bezoeker door klikte om uw plaats te bereiken. Als deze eenmaal is ingesteld, bevat deze dezelfde waarde voor de gehele levensduur van die bezoekersidentiteitskaart. Deze dimensie is nuttig om te begrijpen welke derdeplaatsen oorspronkelijk verkeer aan uw plaats drijven.

>[!IMPORTANT]
>
>U moet uw rapportreeks vormen [Interne URL-filters](/help/admin/admin/internal-url-filter-admin.md) om deze dimensie te gebruiken. Als u interne URL-filters niet configureert, kan dit interne domeinen of externe domeinen omvatten.

## Deze dimensie vullen met gegevens

Deze dimensie vereist configuratie in zowel de interface Analytics als uw implementatie.

* Binnen uw implementatie, wint deze dimensie gegevens van terug [`r` querytekenreeks](/help/implement/validate/query-parameters.md) in afbeeldingsaanvragen. AppMeturement verzamelt deze gegevens met behulp van de JavaScript-variabele `document.referrer` in de browser. Als u een AppMeasurement-bibliotheek gebruikt (bijvoorbeeld via tags in Adobe Experience Platform), werkt deze dimensie buiten het vak. Als u een methode voor gegevensverzameling buiten AppMeasurement gebruikt (bijvoorbeeld via de API), moet u de methode `r` parameter querytekenreeks in afbeeldingsaanvragen.
* Binnen de interface van Analytics, moet u uw rapportreeks vormen [Interne URL-filters](/help/admin/admin/internal-url-filter-admin.md). Als u interne URL-filters niet configureert, kan dit interne domeinen of externe domeinen omvatten.

Adobe blijft het oorspronkelijke verwijzende domein voor het leven van een bezoeker. Wanneer een bezoeker op een ander domein een koppeling verlaat en erop klikt, wordt de nieuwe waarde niet opgenomen. Als u nieuwe waarden wilt zien, raadpleegt u [Verwijzen naar domein](referring-domain.md).

## Dimension-items

Dimension-items bevatten domeinen waarop bezoekers naar uw site klikken. Als een hit geen verwijzingsgegevens heeft (ingesteld of blijvend), groepeert deze zich onder het dimensie-item `"None"`. Dit afmetingsitem betekent dat er geen verwijzingswaarde is, bijvoorbeeld dat de bezoeker het browseradres handmatig in de adresbalk heeft getypt of op een bladwijzer heeft geklikt.

## Verwijzen van domein naar oorspronkelijk verwijzend domein vergelijken

Verwijzend domein kan tussen bezoeken veranderen. Een bezoeker komt bijvoorbeeld via `google.com`, dan komt een week later naar uw site via `twitter.com`. Uiteindelijk kopen ze op uw site. Als u het verwijzingsdomein gebruikt als de dimensie met de laatste aanraakkenmerk, `twitter.com` krijgt krediet voor de aankoop. Als Origineel verwijzend domein als afmeting wordt gebruikt, `google.com` krijgt krediet voor de aankoop ongeacht attributiemodel.

Het oorspronkelijke verwijzende domein verandert nooit voor het volledige leven van een bepaalde bezoekersidentiteitskaart
