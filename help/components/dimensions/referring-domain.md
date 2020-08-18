---
title: Verwijzen naar domein
description: Het overkoepelende domein waarop een bezoeker zich bevond voordat hij naar uw site klikte.
translation-type: tm+mt
source-git-commit: 0870ace3fea8e3ef650d2de2960006a0d655cf9f
workflow-type: tm+mt
source-wordcount: '492'
ht-degree: 0%

---


# Verwijzen naar domein

De dimensie &#39;Verwijzend domein&#39; rapporteert welke domeinen bezoekers door klikken om uw plaats te bereiken. Deze dimensie is nuttig om te begrijpen welke derdeplaatsen het meeste verkeer aan van u drijven. Er moet een koppeling bestaan op de externe site en een bezoeker moet erop klikken om het dimensie-item weer te geven.

>[!IMPORTANT]
>
>U moet de [Interne filters](/help/admin/admin/internal-url-filter-admin.md) van URL van uw rapportreeks vormen om deze dimensie te gebruiken. Als u interne URL-filters niet configureert, kan dit interne domeinen of externe domeinen omvatten.

Hetzelfde rapport kan verschillende resultaten laten zien tussen Analysis Workspace en Data Warehouse. Analysis Workspace rapporteert het verwijzende domein voor elke afzonderlijke pagina, exclusief waarden die overeenkomen met interne URL-filters. Data Warehouse rapporteert alleen het eerste verwijzende domein van het bezoek en negeert interne URL-filters.

## Deze dimensie vullen met gegevens

Deze dimensie vereist configuratie in de interface van Analytics en gegevens in beeldverzoeken.

* Binnen uw implementatie, wint deze afmeting gegevens van het [`r` vraagkoord](/help/implement/validate/query-parameters.md) in beeldverzoeken terug. AppMeturement verzamelt deze gegevens met behulp van de JavaScript-variabele `document.referrer` in de browser. Als u een AppMeasurement-bibliotheek gebruikt (bijvoorbeeld via Adobe Experience Platform Launch), werkt deze dimensie buiten het vak. Als u een methode van de gegevensinzameling buiten AppMeasurement (zoals door API) gebruikt, zorg ervoor dat u de parameter van het `r` vraagkoord in beeldverzoeken omvat.
* Binnen de interface van Analytics, moet u de [Interne filters](/help/admin/admin/internal-url-filter-admin.md)van URL van uw rapportreeks vormen. Als u interne URL-filters niet configureert, kan dit interne domeinen of externe domeinen omvatten.

Adobe blijft het verwijzen domein voor een bezoek. Als een bezoeker een koppeling verlaat en doorklikt op een ander domein binnen één bezoek, wordt de nieuwe waarde bijgewerkt en blijft deze voor de rest van het bezoek bestaan. Zie [Origineel verwijzend domein](original-referring-domain.md)als u alleen de oorspronkelijke waarde wilt zien.

## Dimension-items

Dimension-items bevatten domeinen waarop bezoekers naar uw site klikken. Als een hit geen verwijzingsgegevens heeft (ingesteld of blijvend), groepeert deze zich onder het dimensie-item `"Typed/Bookmarked"`. Dit afmetingsitem betekent dat er geen verwijzingswaarde is, bijvoorbeeld dat de bezoeker het browseradres handmatig in de adresbalk heeft getypt of op een bladwijzer heeft geklikt. Het `"Typed/Bookmarked"` dimensiepunt verschijnt ook voor omleidingen die geen Analytics aanpassen. Zie [Omleidingen en aliassen](/help/technotes/redirects.md) in de de gebruikersgids van Technotes.

### Dimension-items met `googleusercontent.com`

Gebruikers kunnen dimensie-items met het domein zien `googleusercontent.com`.

* **Pagina&#39;s** in cache: De spinnen van Google doorzoeken voortdurend het web en slaan kopieën van pagina&#39;s op voor het geval ze offline worden genomen. Deze in cache geplaatste pagina&#39;s zijn beschikbaar naast de meeste zoekresultaten door op de koppeling &#39;In cache&#39; te klikken. Wanneer een gebruiker op deze koppeling klikt en de inhoud bekijkt die in de cache van Google is opgeslagen, `googleusercontent.com` is dit het dimensie-item.
* **Vertaalde pagina**&#39;s: Google biedt een robuuste en handige vertaalservice. Wanneer u een site weergeeft met deze service, komt deze van `googleusercontent.com`. Dit item voor afmetingen wordt weergegeven als de gebruiker op een koppeling klikt om terug te keren naar de oorspronkelijke inhoud.
