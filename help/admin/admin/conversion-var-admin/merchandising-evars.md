---
title: Merchandising Vars en productzoekmethoden
description: Een diepe duik in de concepten achter het verhandelen van eVars en hoe zij gegevens verwerken en toewijzen.
source-git-commit: e7bfb56b63a9134728360c91f3c835da1952fa5a
workflow-type: tm+mt
source-wordcount: '549'
ht-degree: 0%

---

# Merchandising Vars en productzoekmethoden

In dit document worden de concepten achter het verhandelen van eVars uitgelegd, die gegevens anders verwerken en toewijzen dan standaard eVars. Het legt ook uit hoe handelswaar eVars betrekking heeft op de Methoden van het Vinden van het Product.

Hoewel de meeste websites voor de detailhandel veel manieren hebben om producten te vinden, beschouwt Adobe het volgende als de fundamentele methoden om producten te vinden die elke retailklant in Adobe Analytics moet volgen:

* Trefwoorden voor intern zoeken
* Interne codes voor bijhouden van campagnes
* Categorieën voor wijzigen/bladeren
* Crossselling links

In het kader van dit document, laten wij een paar eVars aan de oplossingen als volgt in kaart brengen:

* eVar2: Trefwoorden voor intern zoeken
* eVar3: Interne codes voor bijhouden van campagnes
* eVar4: Categorieën voor wijzigen/bladeren
* eVar5: Links voor crossverkopen

We kunnen een extra eVar gebruiken om de prestaties van alle productzoekmethoden ten opzichte van elkaar te meten. Naast de hierboven beschreven zoekmethoden zal de eVar andere zoekmethoden in de vergelijking opnemen, zoals koppelingen naar productdetailpagina&#39;s van externe websites.

* eVar1: Methoden voor het zoeken van producten

U zou om het even welk van deze variabelen niet om standaard eVars moeten vormen, maar eerder hen moeten vormen om eVars te verkopen.  Door eVars voor handelsdoeleinden te gebruiken, kunt u elke succesvolle activiteit toewijzen aan de waarden die door de eVars worden vastgelegd op een niveau *per product* in plaats van een niveau *per-visit/per-order*. Ik zal het verschil verduidelijken tussen de toewijzing per product en per bestelling gedurende de rest van dit document.

Om aan te tonen hoe deze variabelen moeten worden geplaatst, zal ik beginnen met een voorbeeld waarin een bezoeker besluit dat zij de interne sleutelwoordonderzoek &quot;zandwaardes&quot;zal gebruiken om een product op de plaats te vinden.  Op de pagina met zoekresultaten met trefwoorden moet u gegevens vastleggen in ten minste twee eVars:

* `eVar2` is gelijk aan het trefwoord dat is gebruikt in de zoekopdracht (&quot;sandalen&quot;)
* `eVar1` is gelijk aan de gebruikte methode voor het zoeken naar producten (&quot;intern zoeken naar trefwoorden&quot;).

Wanneer u deze twee variabelen gelijk instelt aan deze specifieke waarden, weet u dat de bezoeker de interne zoekterm voor trefwoorden &quot;sandalen&quot; gebruikt om een product te zoeken.
Tegelijkertijd weet u dat de bezoeker de andere productzoekmethoden niet gebruikt om producten te zoeken (de bezoeker bladert bijvoorbeeld niet door productcategorieën op het exacte moment dat hij of zij een trefwoordzoekopdracht uitvoert). Om ervoor te zorgen dat er een juiste toewijzing per product plaatsvindt, mogen deze ongebruikte methoden niet worden gebruikt om een product te vinden dat via een interne zoekopdracht met trefwoorden is gevonden.  Daarom moet u logica in de code opnemen (bijvoorbeeld AppMeasurement, AEP Web SDK, enz.) Hiermee wordt de waarde voor Vars die aan deze andere zoekmethoden zijn gekoppeld, automatisch gelijk gemaakt aan de waarde voor een &quot;niet-zoekmethode&quot;.

Wanneer een gebruiker bijvoorbeeld naar producten zoekt die het trefwoord &quot;sandalen&quot; gebruiken, moet de logica van de Analytics-code de variabelen op de interne pagina met zoekresultaten voor trefwoorden als volgt instellen:

* eVar2=&quot;sandalen&quot;: het trefwoord &quot;sandalen&quot; is gebruikt in de interne zoekopdracht met trefwoorden
* eVar1=&quot;intern sleutelwoordonderzoek&quot;: de zoekmethode &quot;intern zoeken naar trefwoorden&quot; is gebruikt
* eVar3=&quot;niet-interne campagne&quot;: een interne campagne is niet gebruikt om de pagina met zoekresultaten te openen
* eVar4=&quot;niet-browse&quot;: een bladercategorie is niet toegankelijk op de pagina met zoekresultaten
* eVar5=&quot;niet-cross-sell&quot;: er is niet op een cross-sell-koppeling op de pagina met zoekresultaten geklikt

