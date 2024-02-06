---
description: Afhankelijk van het bekeken specifieke rapport kunnen in Adobe Analytics de rapporten Unspecified, None, Other of Unknown worden weergegeven. Over het algemeen betekent dit regelitem dat de variabele niet is gedefinieerd of anderszins niet beschikbaar is.
title: Niet opgegeven, Geen, Overige en Onbekend in rapportage
feature: Analytics Basics
exl-id: 35451239-91f3-400a-981e-8c3fbc0e4185
source-git-commit: d3d5b01fe17f88d07a748fac814d2161682837c2
workflow-type: tm+mt
source-wordcount: '515'
ht-degree: 0%

---

# &quot;Unspecified&quot;, &quot;None&quot;, &quot;Other&quot; en &quot;Unknown&quot; in reporting

Afhankelijk van het bekeken specifieke rapport, kunnen in Adobe Analytics verschillende rapporten &quot;Unspecified&quot;, &quot;Other&quot; of &quot;Unknown&quot; (Onbekend) weergeven. Over het algemeen betekent dit regelitem dat de variabele niet is gedefinieerd of anderszins niet beschikbaar is. Het volgende verstrekt een uitvoerige lijst van hoe elk rapport één van deze lijnpunten kan hebben.

## &quot;Niet gespecificeerd&quot; (of &quot;Geen&quot;) in rapportage {#reporting}

&quot;Niet gespecificeerd&quot; is een vrij algemeen lijnpunt in rapporten. Het wordt ook vaak aangeduid als &quot;Geen&quot;.

* **Een gebeurtenis wordt zonder conversievariabele geactiveerd:** Een gebruiker komt bijvoorbeeld naar uw site en koopt deze zonder eVar1-waarde. Als u orden gebruikend de afmeting eVar1 bekijkt, is er geen waarde om deze orde aan toe te schrijven. Daarom wordt deze automatisch toegewezen aan &quot;Niet gespecificeerd&quot;.
* **Niet-geclassificeerde gegevens in classificatierapporten:** Wanneer het bekijken van classificatiegegevens, om het even welke waarde die geen gegevens verbonden aan die bepaalde classificatie heeft &quot;Niet gespecificeerd&quot;terugkeert. U lost dit probleem op door de waarde van de bovenliggende variabele in te delen.
* **Uitsplitsingsrapporten waarin slechts één variabele is geactiveerd:** Wanneer u een uitsplitsing toepast op een variabele, moet elke instantie van die variabele administratief worden verwerkt. Als de tweede variabele niet werd gezien of als het van een vorige klap voorthield, is het afmetingspunt &quot;Niet gespecificeerd&quot;.
* **Niet-mobiele hits in mobiele rapporten:** Niet-mobiele treffers in mobiele rapporten worden weergegeven als &quot;Niet opgegeven&quot; (&quot;Niet mobiel&quot; in Reports and Analytics).

## &quot;Overige&quot; in de rapportage {#other}

Hoewel iets zeldzaam kan zijn in de rapportage, kan &quot;Overige&quot; voorkomen onder verschillende omstandigheden:

* **Pagina&#39;s worden buiten interne URL-filters geactiveerd:** Deze waarde is ingesteld om gegevensfraude te voorkomen, bijvoorbeeld als een andere organisatie uw broncode stort en deze op hun eigen site implementeert. U verhelpt dit probleem door ervoor te zorgen dat alle URL&#39;s die uw code bevat, overeenkomen met de interne URL-filters in de instellingen van de rapportsuite.
* **Bezoekers die een niet vaak gebruikte browser gebruiken:** In het rapport Browsertypen wordt &quot;Overige&quot; weergegeven als een uitsplitsing als bezoekers een browser gebruiken die niet populair is in de browser. Er zijn veel organisaties die browsers produceren. Alle browsers die grotere organisaties niet creeerden worden ingesloten in &quot;Andere&quot;om rapportrompen te verhinderen.

## &quot;Onbekend&quot; in rapportage {#unknown}

&quot;Onbekend&quot; kan zich onder verschillende omstandigheden voordoen:

* **Bezoekresultaten niet in de browser bij het bekijken van de Technology-rapporten:** Als een bibliotheek van het AppMeasurement niet kan bepalen als een eigenschap wordt gesteund, &quot;Onbekend&quot;wordt getoond in rapportering.
* **Segmenten gebruiken waar componenten niet toegankelijk zijn:** Zorg ervoor dat de variabelen die in een segment worden gebruikt worden toegelaten en dat de gebruikers tot hen kunnen toegang hebben. Als een gebruiker geen toegang tot een segmentcomponent heeft, of als een variabele gehandicapt is, &quot;Onbekend&quot;wordt getoond.

## Deze waarden filteren in rapportage {#filter}

In de meeste gevallen is het veilig om deze lijstitems te negeren. U kunt het zoekfilter desgewenst gebruiken om de filters te verwijderen.

Voor sommige gegevensvariabelen van het type backend wordt de waarde gebruikt `::unspecified::` in rapportering, hoewel het niet in de interface wordt getoond. Als een zoekfilter gegevens niet kan uitsluiten, probeert u deze waarde (inclusief de dubbele punten).
