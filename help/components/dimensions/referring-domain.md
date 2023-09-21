---
title: Verwijzen naar domein
description: Het overkoepelende domein waarop een bezoeker zich bevond voordat hij naar uw site klikte.
feature: Dimensions
exl-id: 9e04cb62-6526-4d84-aff7-c962c0ce42b5
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '493'
ht-degree: 0%

---

# Verwijzen naar domein

Het &#39;verwijzende domein&#39; [dimensie](overview.md) geeft aan welke domeinen bezoekers doorklikken om uw site te bereiken. Deze dimensie is nuttig om te begrijpen welke derdeplaatsen het meeste verkeer aan van u drijven. Er moet een koppeling bestaan op de externe site en een bezoeker moet erop klikken om het dimensie-item weer te geven.

>[!IMPORTANT]
>
>U moet uw rapportreeks vormen [Interne URL-filters](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/internal-url-filter-admin.md) om deze dimensie te gebruiken. Als u interne URL-filters niet configureert, kan dit interne domeinen of externe domeinen omvatten.

Hetzelfde rapport kan verschillende resultaten laten zien tussen Analysis Workspace en Data Warehouse. Analysis Workspace rapporteert het verwijzende domein voor elke afzonderlijke pagina, exclusief waarden die overeenkomen met interne URL-filters. Data Warehouse rapporteert alleen het eerste verwijzende domein van het bezoek en negeert interne URL-filters.

## Deze dimensie vullen met gegevens

Deze dimensie vereist configuratie in de interface van Analytics en gegevens in beeldverzoeken.

* Binnen uw implementatie, wint deze dimensie gegevens van terug [`r` querytekenreeks](/help/implement/validate/query-parameters.md) in afbeeldingsaanvragen. AppMeasurement verzamelt deze gegevens met de JavaScript-variabele `document.referrer` in de browser. Als u een bibliotheek met AppMeasurementen gebruikt (bijvoorbeeld via tags in Adobe Experience Platform), werkt deze dimensie buiten het vak. Als u een methode voor gegevensverzameling buiten het AppMeasurement gebruikt (bijvoorbeeld via de API), moet u de opdracht `r` parameter querytekenreeks in afbeeldingsaanvragen.
* Binnen de interface van Analytics, moet u uw rapportreeks vormen [Interne URL-filters](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/internal-url-filter-admin.md). Als u interne URL-filters niet configureert, kan dit interne domeinen of externe domeinen omvatten.

De Adobe blijft het verwijzende domein voor een bezoek. Als een bezoeker een koppeling verlaat en doorklikt op een ander domein binnen één bezoek, wordt de nieuwe waarde bijgewerkt en blijft deze voor de rest van het bezoek bestaan. Als u alleen de oorspronkelijke waarde wilt zien, raadpleegt u [Origineel verwijzend domein](original-referring-domain.md).

## Dimension-items

Items van een Dimension bevatten domeinen waarop bezoekers naar uw site klikken. Als een hit geen verwijzingsgegevens heeft (ingesteld of blijvend), groepeert deze zich onder het dimensie-item `"Typed/Bookmarked"`. Dit afmetingsitem betekent dat er geen verwijzingswaarde is, bijvoorbeeld dat de bezoeker het browseradres handmatig in de adresbalk heeft getypt of op een bladwijzer heeft geklikt. De `"Typed/Bookmarked"` Dimensie-item wordt ook weergegeven voor omleidingen die geen ruimte bieden aan Analytics. Zie [Omleiding en aliassen](/help/technotes/redirects.md) in de gebruikershandleiding voor technische notities.

### Dimension-items met `googleusercontent.com`

Gebruikers kunnen dimensie-items met het domein zien `googleusercontent.com`.

* **Pagina&#39;s in cache**: Google-spinnen doorzoeken voortdurend het web en slaan kopieën van pagina&#39;s op voor het geval ze offline worden genomen. Deze in cache geplaatste pagina&#39;s zijn beschikbaar naast de meeste zoekresultaten door op de koppeling &#39;In cache&#39; te klikken. Wanneer een gebruiker op deze koppeling klikt en de inhoud weergeeft die in Google in cache is geplaatst, `googleusercontent.com` is het dimensie-item.
* **Vertaalde pagina&#39;s**: Google biedt een robuuste en handige vertaalservice. Wanneer u een site weergeeft met deze service, komt deze van `googleusercontent.com`. Dit item voor afmetingen wordt weergegeven als de gebruiker op een koppeling klikt om terug te keren naar de oorspronkelijke inhoud.
