---
title: Referrer
description: De URL waar een bezoeker zich bevond voordat hij op uw site klikte.
feature: Dimensions
exl-id: 146f0327-c73c-40f5-8cc1-584e31d163a2
source-git-commit: 71ff81a0ae67c6f4cc9a8df567e27223cc63f18c
workflow-type: tm+mt
source-wordcount: '449'
ht-degree: 0%

---

# Referenter

De dimensie &#39;Referrer&#39; rapporteert welke URL&#39;s bezoekers hadden wanneer ze door klikten om uw site te bereiken. Deze dimensie is nuttig om te begrijpen welke specifieke URLs het meeste verkeer aan uw plaats drijft. De externe URL moet een koppeling bevatten en een bezoeker moet erop klikken om het dimensie-item weer te geven.

>[!IMPORTANT]
>
>U moet uw rapportreeks vormen [Interne URL-filters](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/internal-url-filter-admin.md) om deze dimensie te gebruiken. Als u interne URL-filters niet configureert, kunt u interne URL&#39;s opnemen of voorkomen dat externe URL&#39;s worden weergegeven.

Hetzelfde rapport kan verschillende resultaten laten zien tussen Analysis Workspace en Data Warehouse. Analysis Workspace rapporteert de referentie voor elke afzonderlijke pagina, exclusief waarden die overeenkomen met interne URL-filters. Data Warehouse rapporteert alleen de eerste referentie van het bezoek en negeert interne URL-filters.

## Deze dimensie vullen met gegevens

Deze dimensie vereist configuratie in de interface van Analytics en gegevens in beeldverzoeken.

* Binnen uw implementatie, wint deze dimensie gegevens van terug [`r` querytekenreeks](/help/implement/validate/query-parameters.md) in afbeeldingsaanvragen. AppMeturement verzamelt deze gegevens met behulp van de JavaScript-variabele `document.referrer` in de browser. U kunt de [`referrer`](/help/implement/vars/page-vars/referrer.md) variabele overschrijving om deze handmatig in te stellen. Als u een AppMeasurement-bibliotheek gebruikt (bijvoorbeeld via tags in Adobe Experience Platform), werkt deze dimensie buiten het vak. Als u een methode voor gegevensverzameling buiten AppMeasurement gebruikt (bijvoorbeeld via de API), moet u de methode `r` parameter querytekenreeks in afbeeldingsaanvragen.
* Binnen de interface van Analytics, moet u uw rapportreeks vormen [Interne URL-filters](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/internal-url-filter-admin.md). Als u interne URL-filters niet configureert, kunt u interne URL&#39;s opnemen of voorkomen dat externe URL&#39;s worden weergegeven.

## Dimension-items

Dimension-items bevatten URL&#39;s waarop bezoekers klikken om uw site te doorlopen. Als een treffer geen verwijzersgegevens heeft, groepeert het zich onder het afmetingspunt `"Typed/Bookmarked"`. Dit afmetingsitem betekent dat er geen verwijzingswaarde is, bijvoorbeeld dat de bezoeker het browseradres handmatig in de adresbalk heeft getypt of op een bladwijzer heeft geklikt. De `"Typed/Bookmarked"` Dimensie-item wordt ook weergegeven voor omleidingen die geen ruimte bieden aan Analytics. Zie [Omleiding en aliassen](/help/technotes/redirects.md) in de gebruikershandleiding voor technische notities.

### Dimension-items met `googleusercontent.com`

Gebruikers kunnen dimensie-items met het domein zien `googleusercontent.com`.

* **Pagina&#39;s in cache**: Google-spinnen doorzoeken voortdurend het web en slaan kopieën van pagina&#39;s op voor het geval ze offline worden genomen. Deze in cache geplaatste pagina&#39;s zijn beschikbaar naast de meeste zoekresultaten door op de koppeling &#39;In cache&#39; te klikken. Wanneer een gebruiker op deze koppeling klikt en de inhoud weergeeft die in Google in cache is geplaatst, `webcache.googleusercontent.com` is een typisch afmetingspunt.
* **Vertaalde pagina&#39;s**: Google biedt een robuuste en handige vertaalservice. Wanneer u een site weergeeft met deze service, komt deze van `translate.googleusercontent.com`. Dit item voor afmetingen wordt weergegeven als de gebruiker op een koppeling klikt om terug te keren naar de oorspronkelijke inhoud.
