---
title: Opties om het effect van browsercookiebeperkingen te beperken
description: Leer hoe u het effect van browsercookiebeperkingen kunt beperken om gegevensverzameling voor Adobe Analytics te verbeteren.
feature: Data Configuration and Collection
exl-id: 81cf3f0c-4871-435d-bcc9-bcff5c682f05
source-git-commit: c8faf29262b9b04fc426f4a26efaa8e51293f0ec
workflow-type: tm+mt
source-wordcount: '516'
ht-degree: 2%

---

# Opties om het effect van browsercookiebeperkingen te beperken

In dit document worden opties besproken voor het behouden van de permanente identificatie van bezoekers in verschillende eigenschappen en oplossingen, terwijl grote browsers preventiemaatregelen voor cookies implementeren.

Adobe Analytics vertrouwt op cookies van de eerste partij om de onsite activiteit van een bezoeker vast te leggen. Analyses vertrouwen ook op cookies van derden om de externe activiteit van een bezoeker te begrijpen, zoals activiteit op andere domeinen die u bezit. Cookies van andere bedrijven worden geblokkeerd op veel browsers en zijn grotendeels niet beschikbaar omdat Chrome binnenkort geen ondersteuning meer krijgt (momenteel gepland voor 2022). Cookies van eerste bedrijven zijn toegestaan op alle browsers, maar verlopen in Safari en andere browsers onder Apple beperkt [Preventie van ITP-tracking](https://webkit.org/tracking-prevention) maatregelen. Zie voor meer informatie over de huidige beperkingen van browsercookies [Adobe Analytics- en browsercookies](cookies.md).

Deze browserbeperkingen weerspiegelen een bredere verschuiving van anonieme tracering door derden naar expliciete uitwisseling van informatie tussen gebruikers en merken die zij vertrouwen. Ter ondersteuning van deze stap biedt Adobe klanten manieren om traditionele cookies aan te vullen met duurzame id&#39;s die via hun first-party relaties zijn verzameld.

## Customer Journey Analytics- en apparaatanalyse

[Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html) en [Apparaatanalyse](/help/components/cda/overview.md) staat gebruikers toe om duurzame herkenningstekens, zoals haastige logins, naast koekjes te omvatten. Zo kunt u de reis van de klant over apparaten en, in het geval van Customer Journey Analytics, over online en off-line kanalen begrijpen:

* **Customer Journey Analytics** is gebaseerd op Adobe Experience Platform en biedt de flexibiliteit om online en offline gegevens in Analysis Workspace te combineren op basis van een gemeenschappelijke klant-id. U kunt opgeven welke id u voor een bepaalde analyse wilt gebruiken en de gegevens in Analysis Workspace bekijken. Klanten met Analytics Select, Prime en Ultimate kunnen dit als een invoegtoepassing kopen.

* **Apparaatanalyse** is een uitbreiding van traditionele Adobe Analytics die klanten toestaat om alternatieve id&#39;s voor bezoekers te gebruiken. Met deze functie kunt u van een apparaatgecentreerde weergave overschakelen op een persoonlijk gecentreerde weergave. De Analytics Ultimate-klanten hebben toegang tot de analyse van apparaten.

## Gegevensverzameling op de server

De server-zijinzameling verstrekt de flexibiliteit om uw eigen herkenningsteken eerder dan het steunen van browser mechanismen te verstrekken om koekjes te plaatsen.

U kunt gegevens naar de analytische server verzenden met de [API voor gegevensinvoer](https://github.com/AdobeDocs/analytics-1.4-apis/blob/master/docs/data-insertion-api/index.md) of de [API voor het invoegen van bulkgegevens](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/bdia.md). API voor het invoegen van gegevens in bulk wordt aanbevolen voor nieuwe implementaties op de server. Voor een vergelijking van de twee API&#39;s raadpleegt u &quot;[Welke Adobe Analytics-tool ik moet gebruiken](https://experienceleague.adobe.com/docs/analytics/admin/admin-overview/which-analytics-tool.html).&quot;

## Meer informatie

Voor praktische stappen die uw bedrijf kan nemen om over te stappen van cookies van andere bedrijven, raadpleegt u [Klanten ophalen en in een koelloze wereld houden met Adobe](https://business.adobe.com/solutions/cookieless.html) en de diepgaande [Buiten het cookie van derden denken: Uw complete gids voor een wereld zonder cookies van derden](https://business.adobe.com/content/dam/www/us/en/pdfs/Adobe_Thinking_Beyond_the_Third_Party_Cookie.pdf).&quot;

>[!MORELIKETHIS]
>
>[Adobe Analytics- en browsercookies](cookies.md)
