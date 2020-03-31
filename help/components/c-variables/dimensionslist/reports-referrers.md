---
title: Referenties
description: Hier wordt de URL van de vorige hit weergegeven als die hit zich buiten uw site bevond.
translation-type: tm+mt
source-git-commit: f18fbd091333523cd9351bfa461a11f0c3f17bef

---


# Referenties

De dimensie &#39;Referrer&#39; toont de URL waar uw bezoekers vandaan kwamen voordat ze op uw site aankwamen. Als een bezoeker bijvoorbeeld op een koppeling klikt van `example.com/example-page.html` en op uw site arriveert, `example.com/example-page.html` is dit de referentie als deze niet als onderdeel van uw domein is gedefinieerd.

Deze dimensie vereist u om de [Interne filters](/help/admin/admin/internal-url-filter-admin.md)van URL van uw rapportreeks te vormen. Als u geen interne URL-filters configureert, beschouwt Adobe Analytics alle domeinen als intern voor uw site.

## Dimensie-eigenschappen

* Deze dimensie gebruikt standaard de meest recente toewijzing.
* Deze afmeting verloopt na bezoek door gebrek.
* Deze dimensie is onderworpen aan de unieke grens van 500 k alvorens afmetingswaarden onder (Laag-verkeer) te groeperen. Data Warehouse heeft geen unieke limiet.
* Als er geen verwijzingswaarde voor metrisch is, wordt het gegroepeerd onder `Typed/Bookmarked`.
* Deze dimensie wordt doorgaans ingesteld bij de eerste hit van het bezoek, maar kan ook worden ingesteld voor een half bezoek.

## Problemen oplossen

**V: Waarom zie ik`googleusercontent.com`als een dimensie-waarde?**

A: [Google](https://about.google/) gebruikt het domein `googleusercontent.com` voor de gehoste inhoud. Gehoste inhoud omvat:

* **Pagina&#39;s** in cache: De spinnen van Google doorzoeken voortdurend het web en slaan webpagina&#39;s op als ze offline of anderszins niet beschikbaar zijn. Deze pagina&#39;s in de cache zijn beschikbaar naast alle zoekresultaten door op de koppeling &#39;Cached&#39; op een van de zoekresultatenpagina&#39;s van Google te klikken. Wanneer een gebruiker op deze koppeling klikt, wordt de oorspronkelijke inhoud op uw site als het desbetreffende domein `googleusercontent.com` weergegeven. Deze pagina&#39;s hebben het subdomein `webcache.googleusercontent.com`.
* **Vertaalde pagina**&#39;s: Google biedt een robuuste en handige vertaalservice. Wanneer u een site weergeeft met deze service, komt deze van `googleusercontent.com`. De verwijzingsdimensie toont URL&#39;s van dit domein als de gebruiker een verbinding klikt om aan de originele inhoud terug te keren. Deze pagina&#39;s hebben het subdomein `translate.googleusercontent.com`.
