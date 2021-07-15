---
title: Merchandising Vars en productzoekmethoden
description: Een diepe duik in de concepten achter het verhandelen van eVars en hoe zij gegevens verwerken en toewijzen.
source-git-commit: 6f98366a58c7c249c474d9f4474faa1676cdf1ea
workflow-type: tm+mt
source-wordcount: '1471'
ht-degree: 0%

---

# Verkoop- en productzoekmethoden

In dit document worden de concepten achter het verhandelen van eVars uitgelegd, die gegevens anders verwerken en toewijzen dan standaard eVars. Het legt ook uit hoe merchandising eVars verband houdt met productzoekmethoden.

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

We kunnen een extra eVar gebruiken om de prestaties van alle productzoekmethoden ten opzichte van elkaar te meten. Naast de hierboven beschreven zoekmethoden bevat de eVar andere zoekmethoden in de vergelijking, zoals koppelingen naar productdetailpagina&#39;s van externe websites.

* eVar1: Methoden voor het zoeken van producten

In plaats van het vormen van om het even welk van deze variabelen om standaard eVars te zijn, vorm hen om handelswaar te zijn Vars. Door eVars voor handelsdoeleinden te gebruiken, kunt u elke succesvolle activiteit toewijzen aan de waarden die door de eVars worden vastgelegd op een niveau *per product* in plaats van een niveau *per-visit/per-order*. In dit document wordt het verschil verduidelijkt tussen de toewijzing per product en per bestelling in de hele reeks.

Hier ziet u een voorbeeld waarin een bezoeker besluit om de interne trefwoordzoekopdracht ‘sandalen’ te gebruiken om een product op de site te zoeken. Zo kunt u zien hoe u deze variabelen instelt. Op de pagina met zoekresultaten met trefwoorden moet u gegevens vastleggen in ten minste twee eVars:

* `eVar2` is gelijk aan het trefwoord dat is gebruikt in de zoekopdracht (&quot;sandalen&quot;)
* `eVar1` is gelijk aan de gebruikte productzoekmethode (&quot;intern trefwoordzoekopdracht&quot;).

Wanneer u deze twee variabelen gelijk instelt aan deze specifieke waarden, weet u dat de bezoeker de interne zoekterm voor trefwoorden &quot;sandalen&quot; gebruikt om een product te zoeken. Tegelijkertijd weet u dat de bezoeker de andere productzoekmethoden niet gebruikt om producten te zoeken (de bezoeker bladert bijvoorbeeld niet door productcategorieën op het moment dat ze een trefwoordzoekopdracht uitvoeren). Om ervoor te zorgen dat een correcte toewijzing per product plaatsvindt, zouden deze ongebruikte methodes geen krediet moeten krijgen voor het vinden van een product dat door een interne sleutelwoordonderzoek werd gevonden. Vandaar, moet u logica in de code (zoals AppMeasurement, het Web SDK van AEP, etc.) opnemen die automatisch eVars verbonden aan deze andere het vinden methodes aan een &quot;het niet vinden methode&quot;waarde plaatst.

Wanneer een gebruiker bijvoorbeeld naar producten zoekt die het trefwoord &quot;sandalen&quot; gebruiken, moet de logica van de Analytics-code de variabelen op de interne pagina met zoekresultaten voor trefwoorden als volgt instellen:

* eVar2=&quot;sandalen&quot;: het trefwoord &quot;sandalen&quot; is gebruikt in de interne zoekopdracht met trefwoorden
* eVar1=&quot;intern sleutelwoordonderzoek&quot;: de zoekmethode &quot;intern zoeken naar trefwoorden&quot; is gebruikt
* eVar3=&quot;niet-interne campagne&quot;: een interne campagne is niet gebruikt om de pagina met zoekresultaten te openen
* eVar4=&quot;niet-browse&quot;: een bladercategorie is niet toegankelijk op de pagina met zoekresultaten
* eVar5=&quot;niet-cross-sell&quot;: Er is niet op een cross-sell-koppeling op de pagina met zoekresultaten geklikt

## Verwisselende eVars-instellingen

Voordat u verdergaat met het voorbeeld &#39;sandalen&#39;, zijn er de verschillende instellingen die u kunt gebruiken voor uw merchandising-vars.  De volgende schermafbeelding is afkomstig uit Report Suite Manager. Ga naar Analytics > Admin > Report Suites > Edit Settings > Conversion > Conversion Variables > Add new > Enable Merchandising.

![](assets/merch-evars1.png)

De secties onder de tabel bevatten meer details over deze instellingen.

| Instelling | Beschrijving |
|--- | --- |
| Naam | De naam, of de rapporteringsdimensie die de variabele moet worden geassocieerd met. Als `eVar1` bedoeld is om Methoden van het Vinden van het Product te vangen, dan zou het gebied van de Naam voor `eVar1` aan &quot;Methoden van het Vinden van het Product&quot;moeten worden geplaatst. |
| Merchandising | Het type syntaxis dat wordt gebruikt om de waarden van de eVar voor handelsdoeleinden vast te leggen |
| Toewijzing | De hulp bepaalt de waarde van de koopvaardigende eVar die krediet zou moeten ontvangen wanneer een succesvolle gebeurtenis plaatsvindt. |
| Verlopen na | Hiermee wordt bepaald wanneer bestaande bindingen van producten en eVar niet langer van kracht moeten zijn. |
| Type | Het type gegevens dat wordt verzameld in de eVar voor handelsdoeleinden |
| Merchandising Binding-gebeurtenis | De gebeurtenis(sen) die bepalen wanneer een product moet worden gebonden aan een waarde van een eVar voor handelsdoeleinden |
| Herstellen | Een trigger die alle back-endgegevens voor de eVar op dat punt opnieuw instelt |
| Merchandising inschakelen | Een vlag die aan &quot;Toegelaten&quot;moet worden geplaatst om de eVar van een standaardeVar in een eVar van de Verkoop te draaien |

### Merchandising

Deze optie is niet beschikbaar voor gewone eVars. Met de instelling [!UICONTROL Merchandising] kunt u [!UICONTROL Conversion Variable Syntax] of [!UICONTROL Product Syntax] kiezen als de methode voor het vastleggen van de waarde van de eVar.

**[!UICONTROL Conversion Variable Syntax]** betekent dat u de waarde van de eVar in een eigen variabele instelt. Met de syntaxis van omzetvariabele wordt de waarde `eVar1` van &quot;intern sleutelwoordonderzoek&quot; bijvoorbeeld als volgt ingesteld binnen de paginacode (of de code AppMeasurement, AEP Web SDK-code, enzovoort):

`s.eVar1="internal keyword search";`

Bij **[!UICONTROL Product Syntax]** wordt de eVar echter alleen ingesteld binnen de productvariabele van Adobe Analytics. De variabele Analytics products bestaat uit zes verschillende porties per product:

`s.products="[category];[productID];[quantity];[revenue];[events];[eVars]"`

* [!UICONTROL Category] is een verouderd kenmerk en wordt niet langer aanbevolen als een haalbare optie om de prestaties van de productcategorie bij te houden.  Zijn enkel bestaan toont aan waarom in de meeste implementaties van de productvariabele, één enkele puntkomma het productID gedeelte van de veranderlijke waarde voorafgaat.
* [!UICONTROL Quantity] en  [!UICONTROL Revenue] zijn nuttig wanneer een productaankoop wordt gevolgd.
* [!UICONTROL Events] is nuttig voor het opnemen van aangepaste incrementele of valutawaarden die niet als inkomsten hoeven te worden geteld (zoals verzendkosten, kortingen, enz.)

Merchandising eVars die worden gevormd om de Syntaxis van het Product te gebruiken worden geplaatst binnen het definitieve gedeelte van de productvariabele. Stel bijvoorbeeld dat een bezoeker een interne trefwoordzoekopdracht heeft gebruikt om de product-id &quot;12345&quot; te zoeken. De op productsyntaxis gebaseerde manier voor het instellen van eVar1 in dit voorbeeld ziet er als volgt uit:

`s.products=";12345;;;;eVar1=internal keyword search";`

U ziet dat er nog door puntkomma&#39;s gescheiden plaatsaanduidingen zijn voor de hoeveelheid, inkomsten en gebeurtenisgedeelten van de productvariabele.  Zonder deze placeholders, zou `eVar1` het plaatsen van intern sleutelwoordonderzoek volledig genegeerd worden.

### Toewijzing

De term &quot;Toewijzing&quot; voor handelswaar is een misvatting, met name voor handelswaar die Vars verkoopt die de Syntaxis van de Variabele van de Omzetting gebruiken. Alle eVars die standaardsyntaxis gebruiken kunnen hun eigen individuele toewijzingsinstelling hebben, maar het verhandelen van eVars met de variabele syntaxis van de Omzetting gebruikt slechts een toewijzingsinstelling van &quot;Recentste (Laatste)&quot;ongeacht wat de toewijzingsinstellingen in de Manager van de Reeks van het Rapport tonen.

Om te begrijpen wat dit het plaatsen betekent dat u het verschil tussen de toewijzing van de eVar en het het verhandelen van eVar bindende eigenschappen moet begrijpen.  Voor het verhandelen van eVars kan &quot;Merchanding eVar Binding&quot; worden beschouwd als een betere naam voor deze &quot;Allocation&quot;-instelling.
Wanneer om het even welke eVar met standaardsyntaxis uit een beeldverzoek wordt verzameld, voegen de de verwerkingsservers van Adobe Analytics gegevens in een andere gegevensbestandkolom in, genoemd een post_evar kolom, naast de regelmatige eVar kolom.  Aangezien eVars blijvend moeten zijn (d.w.z. ze verlopen op een bepaald punt voorbij de huidige hit in de meeste gevallen), zullen de servers deze post_evar kolom op elk volgend beeldverzoek dan plaatsen en het plaatsen van het gelijk aan de laatste waarde die in zijn overeenkomstige eVar wordt overgegaan. Voor standaard (d.w.z. niet-Merchandising) eVars, wanneer een succesgebeurtenis plaatsvindt, gebruikt Adobe Analytics de post_evar kolom in plaats van de regelmatige eVar kolom om de eVar waarde te bepalen die krediet voor de gebeurtenis zou moeten worden verleend.
Voor standaard (d.w.z. niet-Merchandising) eVars, bepaalt het plaatsen van de Toewijzing of de eerste of laatste eVar waarde die tijdens een bepaalde periode werd verzameld in post_evar kolom zal worden opgenomen. Als de Allocation-instelling voor een standaard eVar gelijk is aan &quot;Oorspronkelijke waarde (eerst)&quot;, wordt de eerste eVar die van de bezoeker wordt verzameld, ingevoegd in de post_evar-kolom voor alle volgende afbeeldingsaanvragen.  Dit zal voor alle toekomstige verzoeken die van browser van deze bezoeker worden verzonden tot de eVar volgens zijn &quot;Verloopt na&quot;het plaatsen verloopt.\
Als de toewijzingsinstelling van een standaard eVar gelijk is aan &quot;Recentste (laatste)&quot;, wordt de meest recente eVar-waarde die van de bezoeker is verzameld, ingevuld in de kolom post_evar voor alle volgende afbeeldingsaanvragen. De toewijzing &#39;Meest recente (laatste)&#39; houdt in dat de waarde post_evar telkens wordt gewijzigd wanneer de corresponderende eVar op een nieuwe waarde wordt ingesteld in een afbeeldingsaanvraag.  De toewijzing van de &quot;Originele Waarde (Eerste)&quot;impliceert dat de post_evar kolom niet over klappen zal veranderen alhoewel zijn overeenkomstige eVar aan een verschillende waarde in een toekomstig beeldverzoek zou kunnen worden geplaatst.
Zoals eerder vermeld, hebben alle handelsversies van eVars met conversievariabele syntaxis alleen de &quot;Meest recente (laatste)&quot; toewijzing (volgens de standaarddefinitie van eVar).  Daarom moet ik uitleggen wat de &quot;Toewijzing&quot;-instelling eigenlijk betekent voor het verhandelen van eVars.  Zoals eerder geïmpliceerd, bepaalt deze het plaatsen niet welke waarden in post_evar kolom worden opgenomen aangezien een bezoeker de plaats blijft gebruiken.  In plaats daarvan bepaalt de Allocatie-instelling voor verkoopbare eVars welke eVar-waarde aan een product wordt gekoppeld en hoe deze producten worden toegewezen


