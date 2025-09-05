---
title: Origineel verwijzend domein
description: Het eerste verwijzende domein waarop een bezoeker zich bevond voordat hij op uw site klikte.
feature: Dimensions
exl-id: 6b9ac662-a79a-477b-8612-7980da7cfadd
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '408'
ht-degree: 0%

---

# Origineel verwijzend domein

De &quot;Origineel verwijzend domein&quot;[ dimensie ](overview.md) meldt het eerste verwijzende domein dat een bezoeker door klikte om uw plaats te bereiken. Als deze eenmaal is ingesteld, bevat deze dezelfde waarde voor de gehele levensduur van die bezoekersidentiteitskaart. Deze dimensie is nuttig om te begrijpen welke derdeplaatsen oorspronkelijk verkeer aan uw plaats drijven.

>[!IMPORTANT]
>
>U moet de interne filters van URL van uw rapportreeks [ vormen ](/help/admin/tools/manage-rs/edit-settings/general/internal-url-filter-admin.md) om deze afmeting te gebruiken. Als u interne URL-filters niet configureert, kan dit interne domeinen of externe domeinen omvatten.

## Deze dimensie vullen met gegevens

Deze dimensie vereist configuratie in zowel de interface Analytics als uw implementatie.

* Binnen uw implementatie, wint deze afmeting gegevens van het [`r` vraagkoord ](/help/implement/validate/query-parameters.md) in beeldverzoeken terug. AppMeasurement verzamelt deze gegevens met de JavaScript-variabele `document.referrer` in de browser. Als u een AppMeasurement-bibliotheek gebruikt (bijvoorbeeld via tags in Adobe Experience Platform), werkt deze dimensie buiten het vak. Als u buiten AppMeasurement (bijvoorbeeld via de API) een gegevensverzamelingsmethode gebruikt, moet u de parameter van de `r` querytekenreeks opnemen in afbeeldingsaanvragen.
* Binnen de interface van Analytics, moet u de interne filters van URL van uw rapportreeks [&#128279;](/help/admin/tools/manage-rs/edit-settings/general/internal-url-filter-admin.md) vormen. Als u interne URL-filters niet configureert, kan dit interne domeinen of externe domeinen omvatten.

Adobe blijft het oorspronkelijke verwijzingsdomein voor de levensduur van een bezoeker. Wanneer een bezoeker op een ander domein een koppeling verlaat en erop klikt, wordt de nieuwe waarde niet opgenomen. Als u nieuwe waarden wilt zien, zie [ Verwijzend domein ](referring-domain.md).

## Dimension-objecten

Dimension-items bevatten domeinen waarop bezoekers naar uw site klikken. Als een hit geen verwijzingsgegevens heeft (ingesteld of blijvend), groepeert deze zich onder het dimensie-item `"None"` . Dit afmetingsitem betekent dat er geen verwijzingswaarde is, bijvoorbeeld dat de bezoeker het browseradres handmatig in de adresbalk heeft getypt of op een bladwijzer heeft geklikt.

## Verwijzen van domein naar oorspronkelijk verwijzend domein vergelijken

Verwijzend domein kan tussen bezoeken veranderen. Een bezoeker arriveert bijvoorbeeld via `google.com` naar uw site en komt vervolgens een week later via `twitter.com` naar uw site. Uiteindelijk kopen ze op uw site. Als u het verwijzingsdomein gebruikt als de dimensie met de laatste aanraakkenmerk, krijgt `twitter.com` krediet voor de aankoop. Als u Origineel verwijzend domein gebruikt als de dimensie, krijgt `google.com` krediet voor de aankoop, ongeacht het attributiemodel.

Het oorspronkelijke verwijzende domein verandert nooit voor het volledige leven van een bepaalde bezoekersidentiteitskaart
