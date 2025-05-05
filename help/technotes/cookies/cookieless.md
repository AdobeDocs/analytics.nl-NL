---
title: Opties om het effect van browsercookiebeperkingen te beperken
description: Leer hoe u het effect van browsercookiebeperkingen kunt beperken om gegevensverzameling voor Adobe Analytics te verbeteren.
feature: Data Configuration and Collection
exl-id: 81cf3f0c-4871-435d-bcc9-bcff5c682f05
role: Admin
source-git-commit: 73c0210ac931f3e7f823e033a3bffdc22e159ddb
workflow-type: tm+mt
source-wordcount: '515'
ht-degree: 0%

---

# Opties om het effect van browsercookiebeperkingen te beperken

In dit document worden opties besproken voor het behouden van de permanente identificatie van bezoekers in verschillende eigenschappen en oplossingen, terwijl grote browsers preventiemaatregelen voor cookies implementeren.

Adobe Analytics vertrouwt op cookies van de eerste partij om de onsite activiteit van een bezoeker vast te leggen. Analyses vertrouwen ook op cookies van derden om de externe activiteit van een bezoeker te begrijpen, zoals activiteit op andere domeinen die u bezit. Cookies van andere bedrijven worden geblokkeerd op veel browsers en zijn grotendeels niet beschikbaar als Chrome de ondersteuning binnenkort verwijdert (momenteel gepland voor eind 2024). De koekjes van de eerste partij worden toegestaan op alle browsers maar hebben een beperkte afloop op Safari en andere browsers onder Apple [ ITP die preventie ](https://webkit.org/tracking-prevention) volgen maatregelen. Voor meer informatie over huidige beperkingen op browser koekjes, zie [ Adobe Analytics en browser koekjes ](cookies.md).

Deze browserbeperkingen weerspiegelen een bredere verschuiving van anonieme tracering door derden naar expliciete uitwisseling van informatie tussen gebruikers en merken die zij vertrouwen. Om deze stap te ondersteunen, biedt Adobe klanten manieren om traditionele cookies aan te vullen met duurzame id&#39;s die via hun first-party relaties zijn verzameld.

## Customer Journey Analytics- en Cross-Device Analytics

[ Adobe Customer Journey Analytics ](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=nl-NL) en [ dwars-Apparaat Analytics ](/help/components/cda/overview.md) staan gebruikers toe om duurzame herkenningstekens, zoals gehakt logins, naast koekjes te omvatten. Op deze manier kunt u de reis van de klant over apparaten en, in het geval van Customer Journey Analytics, over online en off-line kanalen begrijpen:

* **Customer Journey Analytics** wordt voortgebouwd op Adobe Experience Platform en verstrekt de flexibiliteit om online en off-line gegevens in Analysis Workspace te combineren, die op om het even welke gemeenschappelijke klantenidentiteitskaart wordt gebaseerd. U kunt opgeven welke id u voor een bepaalde analyse wilt gebruiken en de gegevens in Analysis Workspace bekijken. Klanten met Analytics Select, Prime en Ultimate kunnen dit product als een invoegtoepassing kopen.

* **Analytics van het Apparaat 1&rbrace; is een verhoging aan traditionele Adobe Analytics die klanten toestaat om afwisselende herkenningstekens aan bezoekers te gebruiken.** Met deze functie kunt u van een apparaatgecentreerde weergave overschakelen op een persoonlijk gecentreerde weergave. Analytics voor verschillende apparaten is beschikbaar voor Ultimate-klanten van Analytics.

## Gegevensverzameling op de server

De server-zijinzameling verstrekt de flexibiliteit om uw eigen herkenningsteken eerder dan het steunen van browser mechanismen te verstrekken om koekjes te plaatsen.

U kunt gegevens aan de server-kant van Analytics voorleggen gebruikend of de [ Invoeging API van Gegevens ](https://developer.adobe.com/analytics-apis/docs/1.4/guides/data-insertion/) of [ Bulk API van de Invoeging van Gegevens ](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/bulk-data-insertion/). API voor het invoegen van gegevens in bulk wordt aanbevolen voor nieuwe implementaties op de server. Voor een vergelijking van twee APIs, zie &quot;[ Welk hulpmiddel van Adobe Analytics ](/help/analyze/get-started/which-analytics-tool.md) zou moeten gebruiken.&quot;

## FPID (First Party Device ID) met Web SDK

Met Adobe Experience Platform Web SDK kunt u ervoor kiezen om uw eigen apparaat-id&#39;s in te stellen en te beheren in plaats van de door Adobe gegenereerde Experience Cloud-id&#39;s (ECID&#39;s). Deze worden ook wel FPID&#39;s (First-Party Device ID&#39;s) genoemd. Leer meer [ hier ](https://experienceleague.adobe.com/docs/experience-platform/edge/identity/first-party-device-ids.html?lang=nl-NL).

## Meer informatie

Voor praktische stappen kan uw zaken aan overgang weg van derdekoekjes nemen, [ verwerven en klanten in een kokloze wereld met Adobe ](https://business.adobe.com/solutions/cookieless.html) en diepgaande [ houden die voorbij het derdekoekje denken: Uw volledige gids aan een wereld zonder derdekoekjes ](https://business.adobe.com/content/dam/www/us/en/pdfs/Adobe_Thinking_Beyond_the_Third_Party_Cookie.pdf).&quot;

>[!MORELIKETHIS]
>
>[ Adobe Analytics en browser koekjes ](cookies.md)
