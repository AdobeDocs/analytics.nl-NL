---
description: Veelgestelde vragen over het instellen, configureren en gebruiken van functies in Activiteitenkaart.
title: Veelgestelde vragen over activiteitenoverzicht
topic: Activity map
uuid: e4f6d4e2-55d1-4e32-bf70-a334178af370
translation-type: tm+mt
source-git-commit: 5a8ff1c81644c12f7d00ef147db197f54c48f60c

---


# Veelgestelde vragen over activiteitenoverzicht

Veelgestelde vragen over het instellen, configureren en gebruiken van functies in Activiteitenkaart.

## Implementatie en meting van toepassing

**V: Wat zijn de implementatiestappen voor het toelaten van de nieuwe Activiteitenkaart?**

A: Controleer [Activiteitenkaart inschakelen](/help/analyze/activity-map/activitymap-getting-started/activitymap-getting-started-admins/activitymap-enable.md)

**V: Hebben alle klanten van Analytics toegang tot de pagina van Activiteiten ActivityMap Enablement Admin Tools?**

A: Klanten van Adobe SiteCatalyst hebben geen toegang tot de pagina Activity Map Enablement van de beheerconsole. Alleen bedrijven die onder het contract Adobe Analytics Standard en Adobe Analytics Premium vallen, hebben toegang tot deze configuratiepagina.

**V: Kan de nieuwe code AppMeasurement via Dynamic Tag Management (DTM) worden geconfigureerd?**

A: Ja, u kunt de nieuwe code [manueel uitvoeren](https://marketing.adobe.com/resources/help/en_US/dtm/analytics_dtm.html) AppMeasurement.

**V: Wat zijn de grote veranderingen in de bibliotheek AppMeasurement v1.6?**

A: De enige verandering in AppMeasurement v1.6 is in de het volgen procesmethodologie van de verbinding van de Kaart van de Activiteit die de inzameling van de Naam van de Pagina, identiteitskaart van de Verbinding en RegionID vereist.

**V: Zal AppMeasurement op het domeinniveau eerder dan op specifieke pagina&#39;s worden uitgevoerd?**

A: AppMeasurement wordt uitgevoerd op het rapport-reeks niveau. Het rapport-reeks niveau wordt typisch geassocieerd met een domeinniveau, maar dit verschilt met elke implementatie.

**V: DTM laadt automatisch een oudere versie (1.3.4) van de bezoeker-API dan Activity Map wil (1.5.1). Is dit een probleem?**

A: Nee. De functionaliteit Activiteitenkaart is niet afhankelijk van de VisitorAPI.

## Activiteitenkaarttoepassing

<!--**Q: How does Activity Map support Single-Page Applications (SPA)?**

A: 

* Every few seconds, Activity Map scans the web page, looking for changes to the page. ActivityMap finds new content on the page without needing a new page load, but this new content is always attributed to the first pageName found when the page loaded.

* Activity Map checks to see if the visibility of links that it knows about has changed. If a change in visibility is found, then the [Links On Page](/help/analyze/activity-map/activitymap-links-report.md) table's Present column for that link updates with **[!UICONTROL Displayed]** or **[!UICONTROL Hidden]**.

* When user interaction creates new content, any new elements that are found by AppMeasurement to be a link will be added to the **[!UICONTROL Links On Page]** table. Activity Map sends a new data request that includes these new links. The new links should appear in the **[!UICONTROL Links On Page]** table when the data request is handled by the UI.-->

**V: Biedt Activity Map gegevens over &quot;weergaven&quot;?**

A: Nee, Adobe houdt de weergegeven koppelingen niet bij.

**V: Kan ik Activiteitenkaart gebruiken als ik eerder geen Visitor ClickMap op mijn website gebruikte?**

A: De oudere versie - nu gewoon ClickMap genoemd - is niet een voorwaarde voor de implementatie van de nieuwe versie. Adobe zal de oudere versie gedurende een beperkte periode blijven ondersteunen.

**V: Welke browsers en versies worden ondersteund door Activity Map?**

A: Wij ondersteunen de nieuwste versie van de vier belangrijkste browsers (Chrome, Firefox, Safari en IE).

**V: Wat zijn de standaardbedekkingsinstellingen?**

A: Door gebrek, toont de Kaart van de Activiteit ALLE verbindingen die gegevens hebben verzameld.

Als pop-updeelvensters boven op de webpagina&#39;s van de klant worden weergegeven, worden overlays die horen bij koppelingen die zich onder het pop-upvenster bevinden, mogelijk boven op het pop-upvenster weergegeven.

**V: Waarom ontbreken sommige gerangschikte itemoverlays?**

A: Sommige gerangschikte koppelingen worden mogelijk verborgen op de pagina (bijvoorbeeld submenukoppelingen). Als gevolg hiervan worden de bijbehorende koppelingsoverlays niet weergegeven. U kunt dus bedekkingsclassificaties verwachten die een aantal specifieke rankwaarden missen, omdat de rangorde voor alle koppelingen op de pagina (de huidige en de verborgen) wordt berekend.

**V: Hoe wordt de rangorde van koppelingen bepaald in het rapport Alle koppelingen?**

* In de **modus Verloop** en **Bubbel** : De rangschikking wordt bepaald door de metrische kolom. Voor verbindingen met zelfde metrische waarde, is de rang verder gebaseerd op verbinding ID alfabetische orde.
* In de modus **Gainer &amp; Loser** wordt de rangorde voornamelijk bepaald door de kolom %-verbreding. Voor koppelingen met dezelfde verbreding is de rangorde verder gebaseerd op de alfabetische volgorde van de link-id.

**V: Waarom wordt de verbinding klikgegevens niet verzameld wanneer de Kaart van de Activiteit loopt?**

A: Tijdens het gebruik van Activiteitenkaart worden koppelingsklikgegevens niet verzameld door de tag Analytics. Dit gedrag volgt het gedrag van de stop ClickMap.

**V: Hoe verhoudt de Activiteitenkaart Alle Verbindingen Rapport met Rapporten &amp; de rapportage van de Activiteitenkaart van de Analyse?**

A: Om het Alle Rapport van Verbindingen in de Kaart van de Activiteit te trekken, leiden wij tot een verdelingsverzoek als volgt: Pagina Activiteitenkaart = &quot;Bezochte pagina&quot;, uitgesplitst naar Activiteitenkaartkoppeling&amp;regio in `<list of link&regions present in the page at rendering time>`.

Om een gelijkwaardig rapport in Rapporten &amp; Analytics te krijgen, zou u aan het Rapport van de Pagina van de Kaart van de Activiteit eerst moeten navigeren. Daar, zou u voor bezochte pagename in de Kaart van de Activiteit filtreren. De bezochte Pagename wordt getoond in de linkerkolom in het paneel van de Details van de Pagina van de Activiteitenkaart onder. Zodra de pagina is gevonden, kunt u van die pagina onderbreken en de Verbindingen &amp; Gebieden van de Kaart van de Activiteit kiezen als secundaire dimensie.

Het is echter van belang op te merken dat in het verkregen rapport in O&amp;O alle koppelingen en regio&#39;s worden vermeld die voor die pagina zijn verzameld. Maar Activiteitenkaart rapporteert alleen koppelingen en regio&#39;s die momenteel op de webpagina aanwezig zijn. Dus als je een nieuwssite hebt, zal het alleen gegevens laten zien voor het nieuwsverhaal dat op dit moment aanwezig is, en niet de nieuwsverhalen die eerder op die dag aanwezig waren.

**V: Hoe werkt Activiteitenkaart met pagina&#39;s die veelvoudige markeringen bevatten die van veelvoudige rapportreeksen een lijst maken?**

A: Door gebrek, gebruikt de Kaart van de Activiteit de rapportreeks die met de eerste markering wordt geassocieerd die door de pagina wordt verzonden. U kunt een andere gelabelde rapportsuite selecteren via het tabblad Instellingen activiteitenkaart > Overige.

**V: Hoe lang wordt de Activity Map gescand op de Analytics-tag?**

A: We scannen naar de tag Analytics gedurende maximaal 20 seconden nadat de gebeurtenis Pagina voltooid is.

**V: Hoe behandelt de Kaart van de Activiteit dynamische inhoud?**

A: Activiteitenkaart controleert om de 2 seconden of er wijzigingen in de status van de webpagina zijn gevonden, zoals:

* HTML-inhoud die zichtbaar is geworden
* HTML-inhoud die verborgen is
* Nieuwe HTML-inhoud die is geïnjecteerd

Als inhoud wordt verborgen of weergegeven, wijzigt de toepassing automatisch de gewijzigde staat van de koppelingen (en dus de bedekkingen) van verborgen naar verborgen of verborgen.

Als nieuwe inhoud wordt geïnjecteerd, haalt de toepassing de bijbehorende koppelingen op, haalt de toepassing analysegegevens voor deze koppelingen op en voegt de toepassing overlays voor deze koppelingen toe.

**V: Op welke maateenheid is het rapport van de Stroom van de Pagina gebaseerd?**

A: Alle weergegeven gegevens zijn gebaseerd op paginaweergaven.

**V: Kunt u het gedrag Activiteitenkaart met verschillende typen pagina&#39;s verklaren?**

*Webpagina zonder Analytics-tag*

Onder de werkbalk wordt een waarschuwingsbericht weergegeven waarin wordt aangegeven dat er geen tag aanwezig is.

*Web-pagina met incompatibele Analytics-tag (AppMeasurement v1.5 of eerder)*

Er wordt een waarschuwingsbericht weergegeven waarin wordt aangegeven dat u de paginacode moet bijwerken naar v1.6 of meer.

*Web-pagina met compatibele Analytics-tag (AppMeasurement v1.6 of hoger), maar Activity Map-rapportage is niet ingeschakeld in Admin Tools*

Er wordt een waarschuwingsbericht weergegeven waarin wordt aangegeven dat u de beheerder moet vragen om \[Het rapport Activiteitenkaart inschakelen\](/home/analyze/activity-map/activitymap-getting-started/activitymap-getting-started-admins/activitymap-enable.md&quot;).

**V: Kan ik de gegevens van de Kaart van de Activiteit (contextData) via de[Gegevensvoer](https://docs.adobe.com/content/help/en/analytics/export/analytics-data-feed/data-feed-overview.html)van Analytics uitvoeren?**

A: Nee.

## Segmentering in activiteitenoverzicht

**V: Zijn de segmenten verbonden aan de individuele gebruikerssegmenten? Zijn de gedeelde segmenten beschikbaar in de Kaart van de Activiteit?**

A: De Kaart van de activiteit erft uw rapporterende segmenten van Analytics.

**V: Werken segmenten in de live modus?**

A: Nee, segmenten werken niet in de live modus. De functionaliteit is gelijk aan die van rapportering in real time in Rapporten &amp; Analytics.

## Virtuele rapportsuites

**V: Is de Kaart van de Activiteit compatibel met virtuele rapportsuites?**

A: Ja. Vanwege beperkingen van de virtuele rapportsuite is de actieve modus van Activiteitenkaart echter niet compatibel met virtuele rapportensuites.
