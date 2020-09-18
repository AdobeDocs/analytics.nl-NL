---
title: Referrer
description: De URL waar een bezoeker zich bevond voordat hij op uw site klikte.
translation-type: tm+mt
source-git-commit: dbcdabdfd53b9d65d72e6269fcd25ac7118586e7
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 0%

---


# Referrer

De dimensie &#39;Referrer&#39; rapporteert welke URL&#39;s bezoekers hadden wanneer ze door klikten om uw site te bereiken. Deze dimensie is nuttig om te begrijpen welke specifieke URLs het meeste verkeer aan uw plaats drijft. De externe URL moet een koppeling bevatten en een bezoeker moet erop klikken om het dimensie-item weer te geven.

>[!IMPORTANT]
>
>U moet de [Interne filters](/help/admin/admin/internal-url-filter-admin.md) van URL van uw rapportreeks vormen om deze dimensie te gebruiken. Als u interne URL-filters niet configureert, kunt u interne URL&#39;s opnemen of voorkomen dat externe URL&#39;s worden weergegeven.

Hetzelfde rapport kan verschillende resultaten laten zien tussen Analysis Workspace en Data Warehouse. Analysis Workspace rapporteert de referentie voor elke afzonderlijke pagina, exclusief waarden die overeenkomen met interne URL-filters. Data Warehouse rapporteert alleen de eerste referentie van het bezoek en negeert interne URL-filters.

## Deze dimensie vullen met gegevens

Deze dimensie vereist configuratie in de interface van Analytics en gegevens in beeldverzoeken.

* Binnen uw implementatie, wint deze afmeting gegevens van het [`r` vraagkoord](/help/implement/validate/query-parameters.md) in beeldverzoeken terug. AppMeturement verzamelt deze gegevens met behulp van de JavaScript-variabele `document.referrer` in de browser. U kunt de [`referrer`](/help/implement/vars/page-vars/referrer.md) variabele overschrijven gebruiken om deze handmatig in te stellen. Als u een AppMeasurement-bibliotheek gebruikt (bijvoorbeeld via Adobe Experience Platform Launch), werkt deze dimensie buiten het vak. Als u een methode van de gegevensinzameling buiten AppMeasurement (zoals door API) gebruikt, zorg ervoor dat u de parameter van het `r` vraagkoord in beeldverzoeken omvat.
* Binnen de interface van Analytics, moet u de [Interne filters](/help/admin/admin/internal-url-filter-admin.md)van URL van uw rapportreeks vormen. Als u interne URL-filters niet configureert, kunt u interne URL&#39;s opnemen of voorkomen dat externe URL&#39;s worden weergegeven.

## Dimension-items

Dimension-items bevatten URL&#39;s waarop bezoekers klikken om uw site te doorlopen. Als een treffer geen verwijzingsgegevens heeft, groepeert het zich onder het afmetingspunt `"Typed/Bookmarked"`. Dit afmetingsitem betekent dat er geen verwijzingswaarde is, bijvoorbeeld dat de bezoeker het browseradres handmatig in de adresbalk heeft getypt of op een bladwijzer heeft geklikt. Het `"Typed/Bookmarked"` dimensiepunt verschijnt ook voor omleidingen die geen Analytics aanpassen. Zie [Omleidingen en aliassen](/help/technotes/redirects.md) in de de gebruikersgids van Technotes.

### Dimension-items met `googleusercontent.com`

Gebruikers kunnen dimensie-items met het domein zien `googleusercontent.com`.

* **Pagina&#39;s** in cache: De spinnen van Google doorzoeken voortdurend het web en slaan kopieën van pagina&#39;s op voor het geval ze offline worden genomen. Deze in cache geplaatste pagina&#39;s zijn beschikbaar naast de meeste zoekresultaten door op de koppeling &#39;In cache&#39; te klikken. Wanneer een gebruiker op deze koppeling klikt en de inhoud bekijkt die in de cache van Google is opgeslagen, `webcache.googleusercontent.com` is dit een typisch dimensie-item.
* **Vertaalde pagina**&#39;s: Google biedt een robuuste en handige vertaalservice. Wanneer u een site weergeeft met deze service, komt deze van `translate.googleusercontent.com`. Dit item voor afmetingen wordt weergegeven als de gebruiker op een koppeling klikt om terug te keren naar de oorspronkelijke inhoud.
