---
description: Afhankelijk van het bekeken specifieke rapport kunnen in Adobe Analytics de rapporten Unspecified, None, Other of Unknown worden weergegeven. Over het algemeen betekent dit regelitem dat de variabele niet is gedefinieerd of anderszins niet beschikbaar is.
title: Niet opgegeven, Geen, Overige en Onbekend in rapportage
feature: Analytics Basics
exl-id: 35451239-91f3-400a-981e-8c3fbc0e4185
source-git-commit: 0f5890679ea73c1bbea9f5d2939e89c6775c85da
workflow-type: tm+mt
source-wordcount: '524'
ht-degree: 0%

---

# &quot;Unspecified&quot;, &quot;None&quot;, &quot;Other&quot; en &quot;Unknown&quot; in reporting

Afhankelijk van het bekeken specifieke rapport, kunnen in Adobe Analytics verschillende rapporten &quot;Unspecified&quot;, &quot;Other&quot; of &quot;Unknown&quot; (Onbekend) weergeven. Over het algemeen betekent dit regelitem dat de variabele niet is gedefinieerd of anderszins niet beschikbaar is. Het volgende verstrekt een uitvoerige lijst van hoe elk rapport één van deze lijnpunten kan hebben.

## &quot;Niet gespecificeerd&quot; (of &quot;Geen&quot;) in rapportage {#reporting}

&quot;Niet gespecificeerd&quot; is een vrij algemeen lijnpunt in rapporten. Het wordt ook vaak aangeduid als &quot;Geen&quot;.

* **een gebeurtenisbrand zonder een omzettingsvariabele:** bijvoorbeeld, komt een gebruiker aan uw plaats en maakt een aankoop zonder om het even welke waarde eVar1. Als u orden gebruikend de afmeting eVar1 bekijkt, is er geen waarde om deze orde aan toe te schrijven. Daarom wordt deze automatisch toegewezen aan &quot;Niet gespecificeerd&quot;.
* **Niet geclassificeerde gegevens in classificatierapporten:** wanneer het bekijken van classificatiegegevens, om het even welke waarde die geen gegevens verbonden aan die bijzondere classificatie heeft keert &quot;Niet gespecificeerd terug&quot;. Om dit probleem op te lossen, moet u ervoor zorgen dat aan elk item voor de bovenliggende dimensie een classificatiewaarde is gekoppeld.
* **de rapporten van de Onderverdeling waar slechts één variabele in brand werd gestoken:** wanneer u een onderbreking op een variabele toepast, moet elke instantie van die variabele rekenschap worden gegeven. Als de tweede variabele niet werd gezien of als het van een vorige klap voorthield, is het afmetingspunt &quot;Niet gespecificeerd&quot;.
* **niet-mobiele hits in mobiele rapporten:** Om het even welke niet-mobiele klappen in mobiele rapporten zijn vermeld als &quot;Niet gespecificeerd&quot; (&quot;Niet Mobiel&quot;in Reports and Analytics).

## &quot;Overige&quot; in de rapportage {#other}

Hoewel iets zeldzaam kan zijn in de rapportage, kan &quot;Overige&quot; voorkomen onder verschillende omstandigheden:

* **de brand van Pagina&#39;s buiten interne filters URL:** Deze waarde is op zijn plaats helpen tegen gegevensfraude, zoals als een andere organisatie uw broncode steelt en het op hun eigen plaats uitvoert. U verhelpt dit probleem door ervoor te zorgen dat alle URL&#39;s die uw code bevat, overeenkomen met de interne URL-filters in de instellingen van de rapportsuite.
* **Bezoekers die gebruiken weinig gebruikte browser:** in het Browser rapport van Types, verschijnt &quot;Andere&quot;als onderbreking als de bezoekers browser gebruiken die geen populair browser type is. Er zijn veel organisaties die browsers produceren. Alle browsers die grotere organisaties niet creeerden worden ingesloten in &quot;Andere&quot;om rapportrompen te verhinderen.

## &quot;Onbekend&quot; in rapportage {#unknown}

&quot;Onbekend&quot; kan zich onder verschillende omstandigheden voordoen:

* **niet-browser klappen wanneer het bekijken van de rapporten van de Technologie:** als een bibliotheek van het AppMeasurement niet kan bepalen als een eigenschap wordt gesteund, &quot;Onbekend&quot;wordt getoond in het melden.
* **Gebruikend segmenten waar de componenten niet toegankelijk zijn:** zorg ervoor dat de variabelen in een segment worden gebruikt worden toegelaten en dat de gebruikers tot hen kunnen toegang hebben. Als een gebruiker geen toegang tot een segmentcomponent heeft, of als een variabele gehandicapt is, &quot;Onbekend&quot;wordt getoond.

## Deze waarden filteren in rapportage {#filter}

In de meeste gevallen is het veilig om deze lijstitems te negeren. U kunt het zoekfilter desgewenst gebruiken om de filters te verwijderen.

Sommige achtergrondgegevensvariabelen gebruiken de waarde `::unspecified::` in rapportage, hoewel deze niet in de interface wordt weergegeven. Als een zoekfilter gegevens niet kan uitsluiten, probeert u deze waarde (inclusief de dubbele punten).
