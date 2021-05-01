---
title: Opties om het effect van browsercookiebeperkingen te beperken
description: Leer hoe u het effect van browsercookiebeperkingen kunt beperken om gegevensverzameling voor Adobe Analytics te verbeteren.
translation-type: tm+mt
source-git-commit: 07c76cea1f6fd64957fd4fd20bc5187976f3c14c
workflow-type: tm+mt
source-wordcount: '458'
ht-degree: 2%

---


# Opties om het effect van browsercookiebeperkingen te beperken

In dit document wordt uitgelegd hoe u de permanente identificatie van bezoekers in verschillende eigenschappen en oplossingen kunt behouden wanneer grote browsers preventiemaatregelen voor cookies implementeren.

Adobe Analytics vertrouwt op cookies van de eerste partij om de onsite activiteit van een bezoeker vast te leggen. Analyses vertrouwen ook op cookies van derden om de externe activiteit van een bezoeker te begrijpen, zoals activiteit op andere domeinen die u bezit. Cookies van andere bedrijven worden geblokkeerd op veel browsers en zijn grotendeels niet beschikbaar omdat Chrome binnenkort geen ondersteuning meer krijgt (momenteel gepland voor 2022). Cookies van eerste bedrijven zijn toegestaan op alle browsers, maar hebben een beperkte vervaldatum in Safari en andere browsers onder de [maatregelen van Apple voor het bijhouden van ITP](https://webkit.org/tracking-prevention). Voor meer informatie over huidige beperkingen op browser koekjes, zie &quot;[Adobe Analytics en browser koekjes](cookies.md).

Deze browserbeperkingen weerspiegelen een bredere verschuiving van anonieme tracering door derden naar expliciete uitwisseling van informatie tussen gebruikers en merken die zij vertrouwen. Ter ondersteuning van deze stap biedt Adobe klanten manieren om traditionele cookies aan te vullen met duurzame id&#39;s die via hun first-party relaties zijn verzameld.

## Customer Journey Analytics- en apparaatanalyse

[Adobe de gebruikers van de Reis van de Klant ](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html) Analytici en van de  [dwars-Apparaat ](/help/components/cda/overview.md) Analyticsallow om duurzame herkenningstekens, zoals gehakte logins, naast koekjes te omvatten:

* **Analysemogelijkheden voor** analyseprogramma&#39;s van klanten voor verschillende kanalen in Analysis Workspace via integratie met Adobe Experience Platform. Het consolideert online en off-line klantengegevens beschikbaar aan u in Experience Platform bij vraagtijd, gebruikend om het even welke identiteitskaart

* **Cross-Device** Analyticsidentificeert hoe digitale apparaten aan mensen worden toegewezen en hecht de gebruikersreis over om het even welke identiteitskaart gebruikend de Dienst van de Identiteit van Adobe Experience Platform. Hierbij wordt gebruikgemaakt van de Adobe Experience Cloud Device Co-op-grafiek, een privéapparaatgrafiek of op het veld gebaseerde stitching.

## Gegevensverzameling op de server

De server-zijinzameling verstrekt de flexibiliteit om uw eigen herkenningsteken eerder dan het steunen van browser mechanismen te verstrekken om koekjes te plaatsen.

U kunt server-zijgegevens in Analytics invoeren gebruikend of [de Invoeging API van Gegevens](https://github.com/AdobeDocs/analytics-1.4-apis/blob/master/docs/data-insertion-api/index.md) of [de Invoeging API van Bulk van Gegevens](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/bdia.md). Voor een vergelijking van twee APIs, zie &quot;[Welk hulpmiddel van Adobe Analytics zou moeten I gebruiken](https://experienceleague.adobe.com/docs/analytics/admin/admin-overview/which-analytics-tool.html).&quot;

## Meer informatie

Voor praktische stappen kan uw bedrijf overstappen van derde koekjes, zie &quot;[Klanten in een kokloze wereld met Adobe](https://business.adobe.com/solutions/cookieless.html)&quot;en diepgaand &quot;[Bezig met voorbij het derdekoekje ophalen en houden: Uw complete gids voor een wereld zonder cookies van derden](https://business.adobe.com/content/dam/www/us/en/pdfs/Adobe_Thinking_Beyond_the_Third_Party_Cookie.pdf).&quot;

>[!MORELIKETHIS]
>
>[Adobe Analytics- en browsercookies](cookies.md)
