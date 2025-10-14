---
title: Verwijzen naar domein
description: Het overkoepelende domein waarop een bezoeker zich bevond voordat hij naar uw site klikte.
feature: Dimensions
exl-id: 9e04cb62-6526-4d84-aff7-c962c0ce42b5
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '493'
ht-degree: 0%

---

# Verwijzen naar domein

De &quot;Verwijzend domein&quot; [&#x200B; dimensie &#x200B;](overview.md) meldt welke domeinbezoekers door klikken om uw plaats te bereiken. Deze dimensie is nuttig om te begrijpen welke derdeplaatsen het meeste verkeer aan van u drijven. Er moet een koppeling bestaan op de externe site en een bezoeker moet erop klikken om het dimensie-item weer te geven.

>[!IMPORTANT]
>
>U moet de interne filters van URL van uw rapportreeks [&#x200B; vormen &#x200B;](/help/admin/tools/manage-rs/edit-settings/general/internal-url-filter-admin.md) om deze afmeting te gebruiken. Als u interne URL-filters niet configureert, kan dit interne domeinen of externe domeinen omvatten.

Hetzelfde rapport kan verschillende resultaten laten zien tussen Analysis Workspace en Data Warehouse. Analysis Workspace rapporteert het verwijzende domein voor elke afzonderlijke pagina, exclusief waarden die overeenkomen met interne URL-filters. Data Warehouse rapporteert alleen het eerste verwijzende domein van het bezoek en negeert interne URL-filters.

## Deze dimensie vullen met gegevens

Deze dimensie vereist configuratie in de interface van Analytics en gegevens in beeldverzoeken.

* Binnen uw implementatie, wint deze afmeting gegevens van het [`r` vraagkoord &#x200B;](/help/implement/validate/query-parameters.md) in beeldverzoeken terug. AppMeasurement verzamelt deze gegevens met de JavaScript-variabele `document.referrer` in de browser. Als u een AppMeasurement-bibliotheek gebruikt (bijvoorbeeld via tags in Adobe Experience Platform), werkt deze dimensie buiten het vak. Als u buiten AppMeasurement (bijvoorbeeld via de API) een gegevensverzamelingsmethode gebruikt, moet u de parameter van de `r` querytekenreeks opnemen in afbeeldingsaanvragen.
* Binnen de interface van Analytics, moet u de interne filters van URL van uw rapportreeks [&#128279;](/help/admin/tools/manage-rs/edit-settings/general/internal-url-filter-admin.md) vormen. Als u interne URL-filters niet configureert, kan dit interne domeinen of externe domeinen omvatten.

Adobe blijft bij een bezoek verwijzen naar domein. Als een bezoeker een koppeling verlaat en doorklikt op een ander domein binnen één bezoek, wordt de nieuwe waarde bijgewerkt en blijft deze voor de rest van het bezoek bestaan. Als u slechts de originele waarde wilt zien, zie [&#x200B; Origineel verwijzend domein &#x200B;](original-referring-domain.md).

## Dimension-objecten

Dimension-items bevatten domeinen waarop bezoekers naar uw site klikken. Als een hit geen verwijzingsgegevens heeft (ingesteld of blijvend), groepeert deze zich onder het dimensie-item `"Typed/Bookmarked"` . Dit afmetingsitem betekent dat er geen verwijzingswaarde is, bijvoorbeeld dat de bezoeker het browseradres handmatig in de adresbalk heeft getypt of op een bladwijzer heeft geklikt. Het item voor de `"Typed/Bookmarked"` dimensie wordt ook weergegeven voor omleidingen die geen ruimte bieden voor Analytics. Zie [&#x200B; Omleiding en aliassen &#x200B;](/help/technotes/redirects.md) in de de gebruikersgids van TechNotes.

### Dimension-items met `googleusercontent.com`

Gebruikers kunnen dimensie-items zien met het domein `googleusercontent.com` .

* **Caching pagina&#39;s**: De spinnen van Google kruipen constant het Web en slaan exemplaren van pagina&#39;s op voor het geval zij offline worden genomen. Deze in cache geplaatste pagina&#39;s zijn beschikbaar naast de meeste zoekresultaten door op de koppeling &#39;In cache&#39; te klikken. Wanneer een gebruiker op deze koppeling klikt en de inhoud bekijkt die in Google in cache is geplaatst, is `googleusercontent.com` het dimensie-item.
* **Vertaalde pagina&#39;s**: Google biedt een robuuste en geschikte vertaaldienst aan. Wanneer u een site weergeeft met deze service, komt deze van `googleusercontent.com` . Dit item voor afmetingen wordt weergegeven als de gebruiker op een koppeling klikt om terug te keren naar de oorspronkelijke inhoud.
