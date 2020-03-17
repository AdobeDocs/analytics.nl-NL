---
description: Afhankelijk van het bekeken specifieke rapport kunnen in verschillende rapporten in Adobe Analytics de waarden Niet opgegeven, Overige of Onbekend worden weergegeven. Over het algemeen betekent dit regelitem dat de variabele niet is gedefinieerd of anderszins niet beschikbaar is.
title: Niet opgegeven, Overige en Onbekend in rapportage
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# &quot;Unspecified&quot;, &quot;Other&quot; en &quot;Unknown&quot; in reporting

In verschillende rapporten in Adobe Analytics kunt u &quot;Unspecified&quot;, &quot;Other&quot; of &quot;Unknown&quot; (Onbekend) weergeven, afhankelijk van het bekeken specifieke rapport. Over het algemeen betekent dit regelitem dat de variabele niet is gedefinieerd of anderszins niet beschikbaar is. Het volgende verstrekt een uitvoerige lijst van hoe elk rapport één van deze lijnpunten kan hebben.

## &quot;Niet gespecificeerd&quot; in de rapportage

&quot;Niet gespecificeerd&quot; is een vrij algemeen lijnpunt in rapporten.

* **Een gebeurtenis wordt zonder conversievariabele geactiveerd:** Een gebruiker komt bijvoorbeeld naar uw site en koopt deze zonder eVar1-waarde. Als u orden gebruikend de afmeting eVar1 bekijkt, is er geen waarde om deze orde aan toe te schrijven. Daarom wordt deze automatisch toegewezen aan &quot;Niet gespecificeerd&quot;.
* **Niet-geclassificeerde gegevens in classificatierapporten:** Wanneer het bekijken van classificatiegegevens, om het even welke waarde die geen gegevens verbonden aan die bepaalde classificatie heeft &quot;Niet gespecificeerd&quot;terugkeert. U lost dit probleem op door de waarde van de bovenliggende variabele in te delen.
* **Uitsplitsingsrapporten waarin slechts één variabele is geactiveerd:** Wanneer u een uitsplitsing toepast op een variabele, moet elke instantie van die variabele administratief worden verwerkt. Als de tweede variabele niet werd gezien of als het van een vorige klap voorthield, is de afmetingswaarde &quot;Niet gespecificeerd&quot;.
* **Niet-mobiele hits in mobiele rapporten:** Niet-mobiele treffers in mobiele rapporten worden weergegeven als &quot;Niet-opgegeven&quot; (&quot;Niet-mobiel&quot; in rapporten en analyses).

## &quot;Overige&quot; in de rapportage

Hoewel iets zeldzaam kan zijn in de rapportage, kan &quot;Overige&quot; voorkomen onder verschillende omstandigheden:

* **Pagina&#39;s worden buiten interne URL-filters geactiveerd:** Deze waarde is ingesteld om gegevensfraude te voorkomen, bijvoorbeeld als een andere organisatie uw broncode stort en deze op hun eigen site implementeert. U verhelpt dit probleem door ervoor te zorgen dat alle URL&#39;s die uw code bevat, overeenkomen met de interne URL-filters in de instellingen van de rapportsuite.
* **Bezoekers die een niet vaak gebruikte browser gebruiken:** In het rapport Browsertypen wordt &quot;Overige&quot; weergegeven als een uitsplitsing als bezoekers een browser gebruiken die niet populair is in de browser. Er zijn veel organisaties die browsers produceren. Alle browsers die grotere organisaties niet creeerden worden ingesloten in &quot;Andere&quot;om rapportrompen te verhinderen.

## &quot;Onbekend&quot; in rapportage

&quot;Onbekend&quot; kan zich onder verschillende omstandigheden voordoen:

* **Bezoekresultaten niet in de browser bij het weergeven van technologierapporten:** Als een AppMeasurement-bibliotheek niet kan bepalen of een functie wordt ondersteund, wordt &quot;Onbekend&quot; weergegeven in de rapportage.
* **Segmenten gebruiken waar componenten niet toegankelijk zijn:** Zorg ervoor dat de variabelen die in een segment worden gebruikt worden toegelaten en dat de gebruikers tot hen kunnen toegang hebben. Als een gebruiker geen toegang tot een segmentcomponent heeft, of als een variabele gehandicapt is, &quot;Onbekend&quot;wordt getoond.

## Deze waarden filteren in rapportage {#section_5536E2B419D445D39C932E8F12C0070C}

In de meeste gevallen is het veilig om deze lijstitems te negeren. U kunt het zoekfilter desgewenst gebruiken om de filters te verwijderen.

Sommige achtergrondgegevensvariabelen gebruiken de waarde `::unspecified::` in het rapporteren, hoewel het niet in de interface wordt getoond. Als een zoekfilter gegevens niet kan uitsluiten, probeert u deze waarde (inclusief de dubbele punten) te gebruiken.
