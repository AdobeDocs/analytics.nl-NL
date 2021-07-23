---
title: Referrer
description: De URL waar een bezoeker zich bevond voordat hij op uw site klikte.
exl-id: 146f0327-c73c-40f5-8cc1-584e31d163a2
source-git-commit: 562ed0e190954b7687fa79efaf5c5c54eb202af8
workflow-type: tm+mt
source-wordcount: '449'
ht-degree: 0%

---

# Referenter

De dimensie &#39;Referrer&#39; rapporteert welke URL&#39;s bezoekers hadden wanneer ze door klikten om uw site te bereiken. Deze dimensie is nuttig om te begrijpen welke specifieke URLs het meeste verkeer aan uw plaats drijft. De externe URL moet een koppeling bevatten en een bezoeker moet erop klikken om het dimensie-item weer te geven.

>[!IMPORTANT]
>
>U moet [Interne filters URL ](/help/admin/admin/internal-url-filter-admin.md) van uw rapportreeks vormen om deze afmeting te gebruiken. Als u interne URL-filters niet configureert, kunt u interne URL&#39;s opnemen of voorkomen dat externe URL&#39;s worden weergegeven.

Hetzelfde rapport kan verschillende resultaten laten zien tussen Analysis Workspace en Data Warehouse. Analysis Workspace rapporteert de referentie voor elke afzonderlijke pagina, exclusief waarden die overeenkomen met interne URL-filters. Data Warehouse rapporteert alleen de eerste referentie van het bezoek en negeert interne URL-filters.

## Deze dimensie vullen met gegevens

Deze dimensie vereist configuratie in de interface van Analytics en gegevens in beeldverzoeken.

* Binnen uw implementatie, wint deze afmeting gegevens van [`r` vraagkoord](/help/implement/validate/query-parameters.md) in beeldverzoeken terug. AppMeasurement verzamelt deze gegevens met behulp van de JavaScript-variabele `document.referrer` in de browser. U kunt de [`referrer`](/help/implement/vars/page-vars/referrer.md) veranderlijke opheffing gebruiken om het manueel te plaatsen. Als u een AppMeasurement-bibliotheek gebruikt (bijvoorbeeld via tags in Adobe Experience Platform), werkt deze dimensie buiten het vak. Als u een methode van de gegevensinzameling buiten AppMeasurement (zoals door API) gebruikt, zorg ervoor dat u `r` parameter van het vraagkoord in beeldverzoeken omvat.
* Binnen de interface van Analytics, moet u [Interne filters URL van uw rapportreeks ](/help/admin/admin/internal-url-filter-admin.md) vormen. Als u interne URL-filters niet configureert, kunt u interne URL&#39;s opnemen of voorkomen dat externe URL&#39;s worden weergegeven.

## Dimension-items

Dimension-items bevatten URL&#39;s waarop bezoekers klikken om uw site te doorlopen. Als een treffer geen verwijzingsgegevens heeft, groepeert het zich onder het afmetingspunt `"Typed/Bookmarked"`. Dit afmetingsitem betekent dat er geen verwijzingswaarde is, bijvoorbeeld dat de bezoeker het browseradres handmatig in de adresbalk heeft getypt of op een bladwijzer heeft geklikt. Het `"Typed/Bookmarked"` afmetingspunt verschijnt ook voor omleidingen die geen Analytics aanpassen. Zie [Omleidingen en aliassen](/help/technotes/redirects.md) in de gebruikershandleiding voor technische notities.

### Dimension-items met `googleusercontent.com`

De gebruikers kunnen afmetingspunten met het domein `googleusercontent.com` zien.

* **Pagina&#39;s** in cache: De spinnen van Google doorzoeken voortdurend het web en slaan kopieën van pagina&#39;s op voor het geval ze offline worden genomen. Deze in cache geplaatste pagina&#39;s zijn beschikbaar naast de meeste zoekresultaten door op de koppeling &#39;In cache&#39; te klikken. Wanneer een gebruiker op deze koppeling klikt en de inhoud bekijkt die in de cache van Google is opgeslagen, is `webcache.googleusercontent.com` een typisch dimensie-item.
* **Vertaalde pagina**&#39;s: Google biedt een robuuste en handige vertaalservice. Wanneer u een site weergeeft met deze service, komt deze van `translate.googleusercontent.com`. Dit item voor afmetingen wordt weergegeven als de gebruiker op een koppeling klikt om terug te keren naar de oorspronkelijke inhoud.
