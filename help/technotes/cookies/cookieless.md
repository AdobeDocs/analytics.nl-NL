---
title: Opties om het effect van browsercookiebeperkingen te beperken
description: Leer hoe u het effect van browsercookiebeperkingen kunt beperken om gegevensverzameling voor Adobe Analytics te verbeteren.
source-git-commit: 6c354a343648162ce2951c52a70a688970e1304d
workflow-type: tm+mt
source-wordcount: '516'
ht-degree: 2%

---


# Opties om het effect van browsercookiebeperkingen te beperken

In dit document worden opties besproken voor het behouden van de permanente identificatie van bezoekers in verschillende eigenschappen en oplossingen, terwijl grote browsers preventiemaatregelen voor cookies implementeren.

Adobe Analytics vertrouwt op cookies van de eerste partij om de onsite activiteit van een bezoeker vast te leggen. Analyses vertrouwen ook op cookies van derden om de externe activiteit van een bezoeker te begrijpen, zoals activiteit op andere domeinen die u bezit. Cookies van andere bedrijven worden geblokkeerd op veel browsers en zijn grotendeels niet beschikbaar omdat Chrome binnenkort geen ondersteuning meer krijgt (momenteel gepland voor 2022). Cookies van eerste bedrijven zijn toegestaan op alle browsers, maar hebben een beperkte vervaldatum in Safari en andere browsers onder de [maatregelen van Apple voor het bijhouden van ITP](https://webkit.org/tracking-prevention). Zie [Adobe Analytics en browsercookies](cookies.md) voor meer informatie over de huidige beperkingen van browsercookies.

Deze browserbeperkingen weerspiegelen een bredere verschuiving van anonieme tracering door derden naar expliciete uitwisseling van informatie tussen gebruikers en merken die zij vertrouwen. Ter ondersteuning van deze stap biedt Adobe klanten manieren om traditionele cookies aan te vullen met duurzame id&#39;s die via hun first-party relaties zijn verzameld.

## Customer Journey Analytics- en apparaatanalyse

[Adobe de gebruikers van de Reis van de Klant ](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html) Analytici en van de  [dwars-Apparaat ](/help/components/cda/overview.md) Analyticsallow om duurzame herkenningstekens, zoals gehakte logins, naast koekjes te omvatten. Zo kunt u de reis van de klant over apparaten en, in het geval van Customer Journey Analytics, over online en off-line kanalen begrijpen:

* **De** analyse van de Reis van de klant is gebaseerd op Adobe Experience Platform en biedt de flexibiliteit om online en offline gegevens in Analysis Workspace te combineren, op basis van een gemeenschappelijke klant-id. U kunt opgeven welke id u voor een bepaalde analyse wilt gebruiken en de gegevens in Analysis Workspace bekijken. Klanten met Analytics Select, Prime en Ultimate kunnen dit als een invoegtoepassing kopen.

* **Cross-Device** Analysis en uitbreiding van traditionele Adobe Analytics waarmee klanten alternatieve id&#39;s kunnen gebruiken voor bezoekers. Met deze functie kunt u van een apparaatgecentreerde weergave overschakelen op een persoonlijk gecentreerde weergave. De Analytics Ultimate-klanten hebben toegang tot de analyse van apparaten.

## Gegevensverzameling op de server

De server-zijinzameling verstrekt de flexibiliteit om uw eigen herkenningsteken eerder dan het steunen van browser mechanismen te verstrekken om koekjes te plaatsen.

U kunt gegevens naar de analytische server verzenden met de [API voor gegevensinvoeging](https://github.com/AdobeDocs/analytics-1.4-apis/blob/master/docs/data-insertion-api/index.md) of de [API voor bulkgegevensinvoeging](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/bdia.md). API voor het invoegen van gegevens in bulk wordt aanbevolen voor nieuwe implementaties op de server. Voor een vergelijking van twee APIs, zie &quot;[Welk hulpmiddel van Adobe Analytics zou moeten I gebruiken](https://experienceleague.adobe.com/docs/analytics/admin/admin-overview/which-analytics-tool.html).&quot;

## Meer informatie

Voor praktische stappen die uw bedrijf kan nemen om over te stappen van cookies van derden, zie [Klanten in een kokloze wereld ophalen en houden met Adobe](https://business.adobe.com/solutions/cookieless.html) en de diepgaande [Dinking voorbij het cookie van derden: Uw complete gids voor een wereld zonder cookies van derden](https://business.adobe.com/content/dam/www/us/en/pdfs/Adobe_Thinking_Beyond_the_Third_Party_Cookie.pdf).&quot;

>[!MORELIKETHIS]
[Adobe Analytics- en browsercookies](cookies.md)>
>
