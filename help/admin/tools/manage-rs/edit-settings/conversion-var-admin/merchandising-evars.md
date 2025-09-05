---
title: Merchandising Vars en productzoekmethoden
description: Een diepe duik in de concepten achter het verhandelen van eVars en hoe zij gegevens verwerken en toewijzen.
feature: Admin Tools
role: Admin
exl-id: 9e1a39aa-451f-49bb-8e39-797b6bbd5499
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '5248'
ht-degree: 0%

---

# Verkoop- en productzoekmethoden

In dit zeer gedetailleerde document worden de concepten achter het verhandelen van eVars uitgelegd, die gegevens anders verwerken en toewijzen dan standaard eVars. Het legt ook uit hoe merchandising eVars verband houdt met productzoekmethoden.

## Overzicht

Het gebruiken van merchandising eVars staat u toe om het even welke succesvolle activiteit aan de waarden toe te wijzen die door eVars op a *worden gevangen per-product* niveau in plaats van a *per-bezoek/per-orde* niveau.

Hoewel de meeste websites voor de detailhandel veel manieren hebben om producten te vinden, beschouwt Adobe het volgende als de fundamentele methoden om producten te vinden die elke retailklant in Adobe Analytics zou moeten volgen:

* Trefwoorden voor intern zoeken
* Interne codes voor bijhouden van campagnes
* Categorieën voor wijzigen/bladeren
* Crossselling links

In het kader van dit document, laten wij een paar eVars aan de oplossingen als volgt in kaart brengen:

* eVar2: Trefwoorden voor intern zoeken
* eVar3: interne codes voor het bijhouden van campagnes
* eVar4: rubrieken voor winkelen/bladeren
* eVar5: Links naar andere objecten

We kunnen een extra eVar gebruiken om de prestaties van alle productzoekmethoden ten opzichte van elkaar te meten. Naast de hierboven beschreven zoekmethoden bevat de eVar andere zoekmethoden in de vergelijking, zoals koppelingen naar productdetailpagina&#39;s van externe websites.

* eVar1: Methoden voor het zoeken van producten

In plaats van het vormen van om het even welk van deze variabelen om standaard eVars te zijn, vorm hen om handelswaar te zijn Vars.

Hier ziet u een voorbeeld waarin een bezoeker besluit om de interne trefwoordzoekopdracht ‘sandalen’ te gebruiken om een product op de site te zoeken. Zo kunt u zien hoe u deze variabelen instelt. Op de pagina met zoekresultaten met trefwoorden moet u gegevens vastleggen in ten minste twee eVars:

* `eVar2` is gelijk aan het trefwoord dat is gebruikt in de zoekopdracht (&quot;sandalen&quot;)
* `eVar1` is gelijk aan de gebruikte productzoekmethode (&quot;interne zoekopdracht met trefwoorden&quot;).

Wanneer u deze twee variabelen gelijk instelt aan deze specifieke waarden, weet u dat de bezoeker de interne zoekterm voor trefwoorden &quot;sandalen&quot; gebruikt om een product te zoeken. Tegelijkertijd weet u dat de bezoeker de andere productzoekmethoden niet gebruikt om producten te zoeken (de bezoeker bladert bijvoorbeeld niet door productcategorieën op het moment dat ze een trefwoordzoekopdracht uitvoeren). Om ervoor te zorgen dat een correcte toewijzing per product plaatsvindt, zouden deze ongebruikte methodes geen krediet moeten krijgen voor het vinden van een product dat door een interne sleutelwoordonderzoek werd gevonden. Vandaar, moet u logica in de code (zoals AppMeasurement, het Web SDK van Adobe Experience Platform, etc.) opnemen die automatisch eVars verbonden aan deze andere het vinden methodes aan een waarde &quot;niet-vinden methode&quot;plaatst.

Wanneer een gebruiker bijvoorbeeld naar producten zoekt die het trefwoord &quot;sandalen&quot; gebruiken, moet de logica van de Analytics-code de variabelen op de interne pagina met zoekresultaten voor trefwoorden als volgt instellen:

* eVar2=&quot;sandalen&quot;: het trefwoord &quot;sandalen&quot; is gebruikt in de interne zoekopdracht naar trefwoorden
* eVar1=&quot;intern sleutelwoordonderzoek&quot;: de het vinden methode van het &quot;interne sleutelwoordonderzoek&quot;werd gebruikt
* eVar3=&quot;niet-interne campagne&quot;: een interne campagne is niet gebruikt om de pagina met zoekresultaten te openen
* eVar4=&quot;niet-browse&quot;: een bladercategorie is niet geopend op de pagina met zoekresultaten
* eVar5=&quot;niet-cross-sell&quot;: er is niet op de pagina met zoekresultaten op een kruiselingse link geklikt

## Verwisselende eVars-instellingen

Hier zijn de verschillende instellingen die u kunt gebruiken voor uw favoriete eVars. De volgende schermafbeelding is afkomstig uit Report Suite Manager. Ga naar [!UICONTROL Analytics] > [!UICONTROL Admin] > [!UICONTROL Report Suites] > [!UICONTROL Edit Settings] > [!UICONTROL Conversion] > [!UICONTROL Conversion Variables] > [!UICONTROL Add new] > [!UICONTROL Enable Merchandising] om het bestand te openen.

![ Merch Vars ](/help/admin/tools/manage-rs/edit-settings/conversion-var-admin/assets/merch-evars1.png)

Meer informatie over deze instellingen vindt u in de secties onder de tabel.

| Instelling | Beschrijving |
|--- | --- |
| Naam | De naam, of de rapporteringsdimensie die de variabele moet worden geassocieerd met. Als `eVar1` bedoeld is om methoden voor het zoeken van producten vast te leggen, moet het veld Naam voor `eVar1` worden ingesteld op &quot;Methoden voor het zoeken van producten&quot;. |
| Merchandising | Het type syntaxis dat wordt gebruikt om de eVar-waarden voor handelsdoeleinden vast te leggen |
| Toewijzing | Helps bepaalt de waarde van eVar die bij een geslaagde gebeurtenis als creditering moet worden gebruikt. |
| Verlopen na | Hiermee wordt bepaald wanneer bestaande bindingen van eVar voor producten en handelsdoeleinden niet langer van kracht moeten zijn. |
| Type | Het type gegevens dat wordt verzameld in de eVar voor handelsdoeleinden |
| Merchandising Binding-gebeurtenis | De gebeurtenis(sen) die bepalen wanneer een product moet worden gebonden aan een eVar-waarde voor handelsdoeleinden |
| Herstellen | Een trigger die alle back-endgegevens voor de eVar op dat moment opnieuw instelt |
| Merchandising inschakelen | Een markering die moet worden ingesteld op &quot;Ingeschakeld&quot; om de eVar van een standaard-eVar om te zetten in een Merchandising-eVar |

### Merchandising inschakelen

Wanneer de instelling &#39;Enable Merchandising&#39; is ingesteld op &#39;Enabled&#39;, worden alle hieronder beschreven instellingen weergegeven in Report Suite Manager. Wanneer de instelling voor Verwisselingen inschakelen is ingesteld op Uitgeschakeld, zijn alleen de standaard eVar-instellingen beschikbaar.

### Merchandising

Deze optie is niet beschikbaar voor standaard eVars. Met de instelling [!UICONTROL Merchandising] kunt u [!UICONTROL Conversion Variable Syntax] of [!UICONTROL Product Syntax] kiezen als methode voor het vastleggen van de waarde voor eVar-handelsbewerkingen.

**[!UICONTROL Conversion Variable Syntax]** betekent dat u de eVar-waarde instelt in een eigen variabele. Met de syntaxis van omzetvariabele wordt de `eVar1` -waarde van &#39;interne trefwoordzoekopdracht&#39; bijvoorbeeld als volgt ingesteld binnen de paginacode (of de AppMeasurement-code, Adobe Experience Platform Web SDK-code enzovoort):

`s.eVar1="internal keyword search";`

Met **[!UICONTROL Product Syntax]** wordt de eVar echter alleen ingesteld binnen de productvariabele van Adobe Analytics. De variabele Analytics products bestaat uit zes verschillende porties per product:

`s.products="[category];[name];[quantity];[revenue];[events];[eVars]"`

* [!UICONTROL Category] en [!UICONTROL Name] het opgegeven product identificeren.
* [!UICONTROL Quantity] en [!UICONTROL Revenue] zijn nuttig wanneer een productaankoop wordt gevolgd.
* [!UICONTROL Events] is handig voor het opnemen van aangepaste incrementele of valutawaarden die niet als inkomsten hoeven te worden geteld (zoals verzendkosten, kortingen, enz.)

Merchandising eVars die worden gevormd om de Syntaxis van het Product te gebruiken worden geplaatst binnen het definitieve gedeelte van de productvariabele. Stel dat een bezoeker een interne trefwoordzoekopdracht heeft gebruikt om de product-id &quot;12345&quot; te zoeken. De op productsyntaxis gebaseerde manier voor het instellen van eVar1 in dit voorbeeld ziet er als volgt uit:

`s.products=";12345;;;;eVar1=internal keyword search";`

U ziet dat er nog door puntkomma&#39;s gescheiden plaatsaanduidingen zijn voor de hoeveelheid, inkomsten en gebeurtenisgedeelten van de productvariabele.  Zonder deze plaatsaanduidingen wordt de instelling `eVar1` van de interne zoekopdracht met trefwoorden volledig genegeerd.

### Toewijzing

De term &quot;Toewijzing&quot; voor handelswaar is misleidend, vooral voor handelswaar die Vars gebruikt die de Syntaxis van de Variabele van de Omzetting gebruiken. Alle standaard eVars kunnen hun eigen individuele toewijzingsinstelling hebben. Nochtans, gebruiken de het verhandelen eVars met de Veranderlijke Syntaxis van de Omzetting slechts de &quot;Recentste (Laatste)&quot;toewijzingsinstelling, ongeacht wat de toewijzingsmontages in de Manager van de Reeks van het Rapport tonen.

Als u begrijpt wat deze instelling doet, begrijpt u het verschil tussen eVar-toewijzing en eVar-binding voor handelsdoeleinden. Voor handelswaar-eVars is &quot;Merchandising eVar Binding&quot; een geschiktere naam voor deze &quot;Allocation&quot;-instelling.

#### Standaard eVar-toewijzingsinstelling

Telkens wanneer een eVar met standaardsyntaxis wordt verzameld op basis van een afbeeldingsaanvraag, voegen de Adobe Analytics-verwerkingsservers gegevens in een andere databasekolom in, een zogenaamde `post_evar` -kolom. Aangezien eVars blijvend moeten zijn - ze verlopen in de meeste gevallen op een bepaald punt na de huidige hit - stellen de servers vervolgens deze `post_evar` -kolom in bij elke volgende aanvraag voor een image. Deze wordt ingesteld op de laatste waarde die wordt doorgegeven aan de overeenkomstige eVar. Voor standaard eVars, wanneer een succesgebeurtenis plaatsvindt, gebruikt Adobe Analytics de kolom `post_evar` in plaats van de gewone kolom van eVar om de eVar-waarde te bepalen die krediet voor de gebeurtenis zou moeten krijgen.

Voor standaard eVars bepaalt de Allocation-instelling of de eerste of laatste eVar-waarde die gedurende een bepaalde periode is verzameld, wordt ingevoegd in de `post_evar` -kolom. Als de Allocation-instelling voor een standaard eVar gelijk is aan &quot;Oorspronkelijke waarde (eerst)&quot;, wordt de eerste eVar-waarde die van de bezoeker wordt verzameld, ingevoegd in de `post_evar` -kolom voor alle volgende afbeeldingsaanvragen. Dit gaat door voor alle toekomstige verzoeken die van browser van deze bezoeker worden verzonden tot eVar volgens zijn &quot;Verloopt na&quot;het plaatsen verloopt.

Als een standaard eVar Allocation-instelling gelijk is aan &quot;Most Recent (Last)&quot;, wordt de meest recente eVar-waarde die van de bezoeker is verzameld, in de kolom `post_evar` ingevuld voor alle volgende afbeeldingsaanvragen. De toewijzing &#39;Meest recente (laatste)&#39; houdt in dat de waarde `post_evar` telkens wordt gewijzigd wanneer de corresponderende eVar op een nieuwe waarde wordt ingesteld in een afbeeldingsaanvraag. De toewijzing &#39;Oorspronkelijke waarde (eerste)&#39; houdt in dat de kolom `post_evar` niet wordt gewijzigd in verschillende hits, ook al wordt de bijbehorende eVar in een toekomstig verzoek om een afbeelding op een andere waarde ingesteld.

#### Transchandising eVar-toewijzingsinstelling (binding)

Zoals eerder vermeld, hebben alle handelsversies van eVars met conversievariabele syntaxis alleen de toewijzing &quot;Meest recente (laatste)&quot;. De Allocation-instelling voor het verhandelen van eVars bepaalt dus niet welke waarden in de post_evar-kolom worden ingevoegd omdat een bezoeker de site blijft gebruiken. In plaats daarvan bepaalt deze instelling welke eVar-waarde aan een product wordt gekoppeld en hoe dergelijke producten hun succesgebeurtenissen terugplaatsen naar de eVar-waarden waaraan zij zijn gebonden.

Het volgende gebeurt wanneer een instelling voor het toewijzen van eVar aan handelsdoeleinden (d.w.z. binding) gelijk is aan &quot;Oorspronkelijke waarde (eerste): Alle producten die naast de kolom post_evar zijn ingesteld en die niet eerder zijn gebonden aan de corresponderende eVar van de kolom post_evar &quot;pre-processing&quot;, worden gebonden aan de waarde in de kolom post_evar.  Deze binding tussen eVar-waarde en product verandert nooit totdat de eVar verloopt volgens de instelling &#39;Verlopen na&#39; in de rapportsuite-instellingen.

Telkens wanneer een afbeeldingsaanvraag voldoet aan de criteria die een al gebonden product anders binden aan de laatst ingestelde eVar-waarde, dwingt de instelling &quot;Oorspronkelijke waarde (eerst)&quot; de servers van de Adobe Analytics-gegevensverzameling dergelijke verdere pogingen te negeren. Het tegenovergestelde gebeurt bij het verhandelen van eVars met de instelling Toewijzing (binding) gelijk aan &quot;Recentste (laatste)&quot;. Telkens wanneer een afbeeldingsaanvraag voldoet aan de criteria die een product binden aan een eVar die een product verkoopt, bindt het product zich aan (en bindt het opnieuw) de meest recente waarde die in de eVar is doorgegeven, of de waarde die (altijd) in de `post_evar` -kolom staat.

Zoals eerder vermeld, staat de handelVars u toe om succesgebeurtenissen aan de waarden van eVar op een per-productbasis in plaats van per-bezoek/per-ordebasis toe te wijzen. Dus wanneer een gebonden product een succesgebeurtenis heeft (zoals een winkelwagentje toevoegen of kopen) die eraan gekoppeld is, geeft de succesgebeurtenis zijn waardering aan zowel het product als de eVar-waarden waar het product op dat moment aan gebonden is.

### Verlopen na

Met de instelling voor verlopen van een eVar voor handelsdoeleinden kunt u kiezen

* Wanneer zowel het product als de eVar-bindingen verlopen, en

* Wanneer de kolom post_evar niet meer automatisch moet worden ingevuld nadat een eVar is doorgegeven aan een afbeeldingsaanvraag.

De vervaldatum voor een eVar kan plaatsvinden wanneer een succesgebeurtenis wordt geregistreerd of een bepaalde periode verstrijkt. Adobe Analytics staat slechts één instelling voor Expiration tegelijk toe, per eVar.

Voor de methode van het Vinden van het Product, zou de beste praktijken voor het plaatsen van een verkoop eVar vervaldatum het moeten plaatsen gelijk aan

* Of de hoeveelheid tijd die een product in een winkelwagentje van een plaats wordt gehouden alvorens de plaats automatisch het uit het karretje verwijdert (b.v. 14 dagen, 30 dagen, enz.)
* OF wanneer de aankoopgebeurtenis plaatsvindt.

In beide gevallen worden producten die een bezoeker koopt, in aanmerking genomen als bestelling/eenheid/inkomstenkrediet voor de handelswaar-eVar-waarden waaraan de producten op dat moment gebonden waren.

### Type

Met de instelling voor eVar-type bepaalt u welk type gegevens wordt ingevoegd in de eVar. In de meeste gevallen moet deze waarde gelijk zijn aan &quot;Tekst&quot;. Het gebruik van &quot;Counter&quot; voor een marketingtoepassing voor eVar is zeldzaam. Maar &#39;Counter&#39; kan worden gebruikt om succes toe te wijzen aan Counter eVar-waarden per product.  Het bespreken van oplossingen met een type van &quot;Teller&quot;is buiten het werkingsgebied van dit document.

### Merchandising Binding-gebeurtenis

Met de instelling Transchandising Binding Event kunt u opgeven onder welke voorwaarden een product moet worden gebonden aan een eVar-waarde die als handelsproduct wordt gebruikt. Deze voorwaarden zijn beperkt tot het vuren van specifieke succesgebeurtenissen of alleen eVars. Variabelen van het afvuurverkeer (bv. profielen) hebben geen invloed op handelsbanden.

Merchandising Binding Event die een product aan een waarde van eVar door meer dan één gebeurtenis plaatst kan binden. Voorbeelden:

* Via een productweergave-gebeurtenis
* Via een winkelwagentje
* Via een aankoopgebeurtenis

Standaard bindt de instelling een product aan een eVar-waarde voor handelsdoeleinden wanneer andere gebeurtenissen/eVar (handelswaar of standaard) zich in dezelfde afbeeldingsaanvraag als het product bevinden.

### Herstellen

Met de instelling Herstellen kunt u alle eVar-waarden onmiddellijk &#39;verlopen&#39; voor alle bezoekers die momenteel een `post_evar` -waarde hebben in de Adobe Analytics-back-enddatabase. Ook worden alle huidige product/eVar-bindingen verwijderd.

>[!IMPORTANT]
>Adobe raadt u niet aan de instelling Opnieuw instellen te gebruiken, tenzij u van plan bent de eVar opnieuw te starten met een volledig &#39;schone lei&#39; aan gegevens vanaf het moment dat de reset plaatsvindt.

## Welke instellingen moet u gebruiken?

Onder de vele beschikbare plaatsende combinaties, zou u zich kunnen afvragen: Welke montages zijn beste praktijken?

Als u &quot;interne sleutelwoordonderzoek&quot;aan product ID 12345 wilt binden, zou de productvariabele als volgt worden geplaatst:

`s.products=";12345;;;;eVar1=internal keyword search";`

Eventuele succesgebeurtenissen (winkelwagentjes, aankopen) die tegelijkertijd met productID 12345 worden vastgelegd, worden zowel aan product-id 12345 als aan de eVar1-waarde van &quot;interne trefwoordzoekactie&quot; toegevoegd. De enige manier waarop een andere eVar1-waarde krediet ontvangt voor succesgebeurtenissen in verband met product-id 12345 is als eVar1 later op een andere waarde binnen de productvariabele werd ingesteld (naast product-id 12345).

Bijvoorbeeld:

```js
s.products=";12345;;;;eVar1=internal campaign";
```

Met deze variabele wordt de binding van product-id 12345 gewijzigd van de eVar1-waarde van &quot;internal keyword search&quot; in de eVar1-waarde van &quot;internal campagne&quot;. Deze wijziging van de binding vindt ook plaats wanneer de eVar is geconfigureerd voor het gebruik van productsyntaxis en de instelling Toewijzing (binding) van &quot;Recentste (laatste)&quot;. Als de instelling voor Toewijzing (binding) in plaats daarvan zou worden ingesteld op &quot;Oorspronkelijke waarde (Eerste)&quot;, zou het instellen van eVar1 gelijk aan &quot;interne campagne&quot; naast product-id 12345 de product-id 12345 niet opnieuw binden aan de eVar1-waarde van &quot;interne campagne&quot;. In plaats daarvan, zou de band met de oorspronkelijk verbindende waarde blijven - &quot;interne sleutelwoordonderzoek&quot;.

### Uitdagingen van productsyntaxis

Zonder zorgvuldige planning, kunnen verscheidene kwesties uit het gebruiken van de Syntaxis van het Product voortvloeien. Laten we het hebben over het gebruik van meerdere eVars om productzoekmethoden op de website bij te houden. In dit geval moet elke individuele methode voor het vinden van het product eVar tegelijkertijd worden vastgesteld om een bepaalde methode voor het vinden van resultaten te verkrijgen, namelijk eVar-krediet (en de andere methode voor het vinden van de resultaten &quot;Vars no credit&quot;). De Syntaxis van het product kan in dergelijke scenario&#39;s worden gebruikt maar de resulterende code om op te stellen is ingewikkelder.

Als we ons oorspronkelijke &quot;sandalen&quot;-voorbeeld gebruiken en dit aanpassen aan de productsyntaxis (ervan uitgaande dat de bezoeker een product heeft gevonden met de id &quot;sandal123&quot; met de trefwoordterm &quot;sandalen&quot;), moet de resulterende productvariabele als volgt worden ingesteld:

`s.products=";sandal123;;;;eVar2=sandals|eVar1=internal search|eVar3=non-internal campaign|eVar4=non-browse|eVar5=non-cross-sell";`

Hoewel de syntaxis van de productvariabele in dit voorbeeld lang is, bindt deze elk van de eVar-waarden die worden gezien aan de product-id van &quot;sandal123&quot;. Vanaf dat moment worden eventuele succesgebeurtenissen (bijv. winkelwagentjes, aankopen) die tegelijkertijd met het product &quot;sandal123&quot; worden vastgelegd, gecrediteerd op de eVar-waarden die het laatst aan het product waren gekoppeld.  Dit codevoorbeeld laat zien of een aankoop van 1 eenheid van het product &quot;sandal123&quot; (voor $79,95) plaatsvindt nadat de bovenstaande eVars aan het product &quot;sandal123&quot; waren gebonden:

```js
s.products=";sandal123;1;79.95";
s.events="purchase";
```

De volgende waarden zouden allen 1 orde, 1 eenheid, en $79.95 van opbrengst hebben die aan hen wordt toegewezen:

* eVar2-waarde van &quot;sandalen&quot;
* eVar1-waarde van &quot;interne trefwoordzoekopdracht&quot;
* eVar3-waarde van &quot;niet-interne campagne&quot;
* eVar4-waarde van &quot;non-browse&quot;
* eVar5-waarde van &quot;niet-cross-sell&quot;

Dit is een correcte toewijzing, wat geen kwestie is. Het belangrijkste dilemma met deze aanpak is het bepalen hoe en wanneer de Vars van de Methode voor het vinden van producten moeten worden geplaatst.

In de meeste gevallen met de Syntaxis van het Product, zou de het Vinden Methode eVars van het Product op een pagina van het productdetail eerder dan op de pagina moeten worden geplaatst dat de het vinden methode eigenlijk werd gebruikt (b.v. op de pagina van het sleutelwoordonderzoek, browse pagina, de interne campagne landende pagina, enz.). Het is redelijk om aan te nemen dat een product pas echt is &quot;gevonden&quot; als een bezoeker enige interactie heeft met een product. Daarom moeten deze eVars (met productsyntaxis) niet op de pagina van de zoekmethode worden ingesteld omdat meerdere producten (gewoonlijk) op deze pagina&#39;s worden weergegeven. We willen de waarde van de zoekmethode alleen binden aan die producten waarmee de bezoeker heeft gereageerd.

Bovendien kunnen bezoekers tijdens het bekijken van een pagina met zoekmethoden klikken op een koppeling die hen naar een afzonderlijke pagina met productdetails brengt of een afzonderlijk product rechtstreeks vanaf de pagina met zoekmethoden aan het winkelwagentje toevoegen. Als een bezoeker met behulp van ons zoektrefwoordvoorbeeld &quot;sandalen&quot; het product &quot;sandal123&quot; rechtstreeks vanuit een pagina met zoekresultaten met trefwoorden aan de winkelwagentje toevoegt, moet de code voor het vastleggen van de cart add-to-Cart (via de onClick-gebeurtenis van de knop Add-to-Cart, enz.) dynamisch worden gegenereerd op het moment dat de cart wordt toegevoegd of moet de code direct via de pagina worden gecodeerd tagbeheersysteem.  De code die in dergelijke gevallen moet worden afgevuurd, ziet er echter ongeveer als volgt uit:

```js
s.linkTrackVars="products,events";
s.linkTrackEvents=s.events="scAdd";
s.products=";sandal123;;;;eVar2=sandals|eVar1=internal keyword search|eVar3=non-internal campaign|eVar4=non-browse|eVar5=non-cross-sell";
s.tl(true,"o","Cart Add")
```

Deze code bindt de eVar-waarden die hierboven zijn weergegeven, correct aan het product &quot;sandal123&quot;. Als u deze waarden echter op de juiste wijze wilt instellen wanneer de gebeurtenis click plaatsvindt, moet de ontwikkelaar:

* Voeg serverlogica aan de pagina van onderzoeksresultaten toe die de waarden bepaalt die in de product het vinden methode eVars moeten worden opgenomen, en
* U kunt de volledige productvariabele samenstellen zonder syntaxisfouten.

Als een bezoeker besluit het product te &quot;vinden&quot; door op een koppeling naar de productdetailpagina te klikken, moet de ontwikkelaar ook:

* Geef de details van de productzoekmethode (zoals hierboven is weergegeven) door van de pagina met zoekmethoden naar de pagina met productdetails, en
* Maak dezelfde variabelewaarde van de productvariabele opnieuw van de items die net zijn doorgegeven vanaf de vorige pagina.

### Waar productsyntaxis nuttig is

Productsyntaxis is nog steeds handig wanneer

* Meerdere producten met dezelfde product-id&#39;s hebben tegelijkertijd te maken met en
* De eVars die aan dergelijke producten worden gebonden, moeten verschillende waarden per product-id hebben.

Veel kledingproducten hebben bijvoorbeeld &#39;Onderliggende SKU&#39;s&#39;, die de grootte, kleur, stijl en andere kenmerken aangeven. Deze kenmerken scheiden één onderliggend product van andere producten die tot hetzelfde bovenliggende product behoren. Stel dat u besluit een gemiddeld blauw t-shirt en een groot rood t-shirt te kopen. Veronderstel dat beide overhemden de ouderproduct-id van &quot;tshirt123&quot;hebben en `eVar10` is gevormd om kind SKUs te vangen. De variabelen op de pagina voor aankoopbevestiging worden als volgt ingesteld:

```js
s.events="purchase";
s.products=";tshirt123;1;20;;eVar10=tshirt123-m-blue,;tshirt123;1;20;;eVar10=tshirt123-l-red";
```

In dit geval krijgen zowel `eVar10` (childSKU) waarden van &quot;tshirt123-m-blue&quot; als &quot;tshirt123-l-red&quot; krediet voor de aankoop van hun respectievelijke instanties van product-id &quot;tshirt123&quot;.

### Uitdagingen met &quot;Recentste&quot; toewijzing

U kunt extra problemen ondervinden door de instelling Toewijzing (binding) van &quot;Meest recente (laatste)&quot; te gebruiken. In veel webbrowservaringen &quot;zoeken&quot; bezoekers een product dat ze al hebben bekeken en/of aan het winkelwagentje hebben toegevoegd. Dit gebeurt gewoonlijk tijdens een volgende bezoek of vlak voordat ze besluiten een aankoop te voltooien. Stel dat een bezoeker tijdens een bezoek aan de site het product &quot;sandal123&quot; vindt via de trefwoordzoekopdracht &quot;sandalen&quot;. Zij voegen het onmiddellijk aan het karretje van de pagina van de sleutelwoordonderzoeksresultaten toe. De code die de winkelwagentje toevoegt, wordt als volgt ingesteld:

```js
s.linkTrackVars="products,events";
s.linkTrackEvents=s.events="scAdd";
s.products=";sandal123;;;;eVar2=sandals|eVar1=internal keyword search|eVar3=non-internal campaign|eVar4=non-browse|eVar5=non-cross";
```

Als gevolg hiervan zijn alle eVar-waarden in deze afbeeldingsaanvraag gebonden aan het product &quot;sandal123&quot;.

Stel je nu voor dat de bezoeker het product niet koopt tijdens dit bezoek, maar drie dagen later terugkeert naar de site met het &quot;sandals123&quot;-product nog steeds in het winkelwagentje. De bezoeker wil meer over het product leren alvorens de aankoop te maken. Maar in plaats van het gebruiken van een sleutelwoordonderzoek om het product te vinden, doorbladert de bezoeker door de plaats. Ze eindigen in de sectie &quot;Womens > schoenen > sandalen&quot; waarin de winkels bladeren vlak voordat ze het product &quot;opnieuw vinden&quot;. Wanneer ze uiteindelijk de productdetailpagina voor het product &quot;sandal123&quot; vinden, worden de variabelen als volgt ingesteld (bij het laden van de pagina):

```js
s.events="prodView";
s.products=";sandal123;;;;eVar4=womens > shoes > sandals|eVar1=browse|eVar3=non-internal campaign|eVar2=non-search|eVar5=non-cross-sell";
```

Met een instelling voor Toewijzing (binding) van &quot;Recentste (laatste)&quot; bindt het product &quot;sandal123&quot; zich aan totaal andere eVar-waarden dan de oorspronkelijke waarden. Als de bezoeker vervolgens de aankoop van &quot;sandal123&quot; voltooit, wordt bovendien al het koopkrediet aan deze nieuw gebonden eVar-waarden gegeven in plaats van aan de oorspronkelijk gebonden waarden!

De vraag is: welke eVar-waarden moeten krediet krijgen voor de aankoop&quot;. Vergeet niet dat de bezoeker het product &quot;sandal123&quot; in eerste instantie heeft gevonden via een interne trefwoordzoekopdracht. Vervolgens hebben ze het rechtstreeks vanuit de pagina met zoekresultaten aan het winkelwagentje toegevoegd. Daarom moet de eVar1-waarde van &quot;interne trefwoordzoekopdracht&quot; (en de eVar2-waarde van &quot;sandalen&quot;) krediet voor de aankoop krijgen. De instellingen voor Toewijzing (binding) zijn echter ingesteld op Laatst (Laatst). Daarom krijgt de eVar1-waarde van &quot;browse&quot; (en de eVar4-waarde van &quot;womens > schoenen > sandalen&quot;) het koopkrediet. De reden hiervoor is dat het de laatste waarden waren die gebonden waren aan &quot;sandal123&quot; voordat de bezoeker de aankoop voltooide.

Een oplossing voor dit probleem is het wijzigen van de toewijzingsinstelling (binding) van de eVar voor handelsdoeleinden van &quot;Recentste (laatste)&quot; in &quot;Oorspronkelijke waarde (eerste)&quot;. Op deze manier krijgen de oorspronkelijke eVar-waarden die aan het product &quot;sandal123&quot; zijn gebonden, krediet wanneer de aankoop plaatsvindt, ongeacht hoe vaak de bezoeker het product &quot;hervindt&quot;.

Als de bezoeker een product aan het winkelwagentje toevoegt maar het nooit koopt, staat het verlopen van eVar toe dat een nieuwe waarde van de zoekmethode aan het product wordt gebonden. Het verlopen van de eVar moet gelijk zijn aan de tijd dat een product op een website in het winkelwagentje kan blijven voordat het automatisch wordt verwijderd.

### Conversievariabele-syntaxis gebruiken

Laten we terugkeren naar de vraag &quot;Productsyntaxis&quot; versus &quot;Conversion Variable Syntax&quot;. Adobe heeft een gemakkelijkere methode ontdekt voor zowel het verzamelen van de product het vinden methode die eVars verhandelen en hun waarden binden aan producten die de bezoekers hebben gevonden: Het gebruiken van de Veranderlijke Syntaxis van de Omzetting vermindert het implementatiewerk dat de ontwikkelaars van de cliënt voor verantwoordelijk zijn. Het biedt nog steeds dezelfde - of betere - informatie dan de methode van de Syntaxis van het Product. De ontwikkelaars moeten eenvoudig de plaatsingsinstructies volgen die zij werden gegeven, en de rest code kan in het Adobe AppMeasurement/Adobe Experience Platform Web SDK- dossier worden geplaatst.

Kijk bijvoorbeeld naar de aanbevolen oplossing voor het bijhouden van de interne zoekprestaties voor trefwoorden. Er wordt aangegeven dat op de pagina met zoekresultaten met trefwoorden het trefwoord waarnaar wordt gezocht met een proxy (bijvoorbeeld prop4) en een andere proxy (bijvoorbeeld prop5) door de code wordt vastgelegd. Deze profielen volgen het aantal resultaten die van het onderzoek worden getoond. Telkens wanneer een Adobe Analytics-verzoek om een afbeelding wordt gegenereerd op de pagina met zoekresultaten, werd gebruikgemaakt van de gegevenslaagobjecten (of paginacode) die door de ontwikkelaars zijn geïmplementeerd om de bovenstaande variabelen (de props) in te vullen.

Met extra logica in het AppMeasurement/Adobe Experience Platform Web SDK-bestand kunt u de resterende variabelen (de merchandising-variabelen/afmetingen) invullen die tegelijkertijd moeten worden ingesteld.\
Als een nieuwe bezoeker bijvoorbeeld een trefwoordzoekopdracht zou uitvoeren naar &quot;sandalen&quot;, die 25 resultaten heeft opgeleverd op de pagina met zoekresultaten, zou de af te vuren code (via de paginacode OF gegevenslaagvastlegging) er als volgt uitzien:

```js
s.prop4="sandals";
s.prop5="25";
```

Logica in het AppMeasurement/Analytics SDK-bestand kan dit codefragment dan automatisch omzetten in het volgende:

```js
s.prop4="sandals";
s.prop5="25";
s.eVar2="sandals";
s.eVar1="internal keyword search";
s.eVar3="non-internal campaign";
s.eVar4="non-browse";
s.eVar5="non-cross sell";
```

U hoeft zich geen zorgen te maken over het doorgeven van gegevens van pagina naar pagina en over het maken van een tamelijk grote, onhandige tekenreeks die in de productvariabele moet worden ingevoegd. In plaats daarvan, kunnen de ontwikkelaars hun gedeelte van de volgende oplossingen uitvoeren - wat in de steunen wordt opgenomen - en de rest van de implementatie aan de douanecode verlaten die door Adobe Consulting wordt verstrekt.

Zoals eerder is uitgelegd, hebben alle handelsversies van Vars die de syntaxis van de omzettingsvariabele gebruiken, de toewijzingsinstelling &quot;Meest recente (laatste)&quot;. Zodra een eVar gelijk is aan om het even welke waarde, blijft die waarde over alle verdere klappen (via post_evar kolom) voortbestaan. Deze blijft bestaan totdat een andere waarde wordt ingesteld of totdat de eVar verloopt. Daarom binden alle producten waarmee iemand communiceert nadat de eVars zijn ingesteld, als ze nog niet aan die eVars zijn gebonden, aan de waarden &quot;Recentste (laatste)&quot; die in de eVar zijn doorgegeven.

In ons bovenstaande voorbeeld gebruiken we de `eVar2` waarde van &quot;sandalen&quot; en de eVar1-waarde van &quot;intern zoeken naar trefwoorden&quot;, enzovoort. blijven staan op alle pagina&#39;s die worden gezien nadat de sleutelwoordzoekopdracht plaatsvond. Ze blijven bestaan totdat de eVars met andere waarden worden overschreven. Een bezoeker klikt op een koppeling naar de productdetailpagina voor de product-id &quot;sandal123&quot; op de pagina met zoekresultaten met trefwoorden.  Vervolgens wordt de product-id &quot;sandal123&quot; (als deze nog niet is gebonden) gekoppeld aan elk van de waarden in de kolommen post_evar, of aan de eVar-waarden die zijn verzameld op de vorige pagina (zoekresultaten).

Er is nog één ding om met de Veranderlijke Syntaxis van de Omzetting te heroverwegen. Het is dat bindende gebeurtenissen opstelling moeten zijn om een waarde van eVar aan een product te binden. Als u een eVar voor handelsdoeleinden (in een eigen variabele) naast een product (in de productvariabele) instelt in een Adobe Analytics-afbeeldingsaanvraag, hoeft de eVar-waarde niet noodzakelijkerwijs aan het product te worden gebonden.  In plaats daarvan bepaalt de instelling voor Merchandising Binding-gebeurtenis, die is ingesteld in Rapportbeheer, de criteria die een eVar-waarde aan een product binden

Omdat we de Product Finding Methode eVar-waarden aan producten willen binden wanneer een productinteractie plaatsvindt - wat betekent dat een product &quot;gevonden&quot; is - is het veilig om aan te nemen dat de meest voorkomende &quot;product gevonden&quot; interacties die kunnen plaatsvinden een productweergave zijn (wanneer bezoekers naar een productdetailpagina gaan) of een winkelwagentje toevoegen (wanneer bezoekers een product rechtstreeks vanaf een productzoekmethodepagina aan de winkelwagentje toevoegen).

Daarom kunnen wij deze twee gebeurtenissen (prodView, scAdd) als &quot;fundamentele&quot;handel kiezen bindende gebeurtenissen.
Dit is wat er gebeurt wanneer een van deze bindingsgebeurtenissen zich in een afbeeldingsaanvraag bevindt. Om het even welke product IDs die in het zelfde verzoek (binnen de productvariabele) bevat zijn en die niet aan een handelende eVar zijn gebonden zal aan de meest recente waarden binden die aan de handelende eVar (post_evar kolommen) worden overgegaan. Elke poging om deze producten opnieuw te binden nadat deze oorspronkelijke binding heeft plaatsgevonden, wordt genegeerd wanneer de instelling Toewijzing (binding) gelijk is aan &quot;Oorspronkelijke waarde (eerste)&quot;.

### Instellingen voor aanbevolen werkwijzen

Hier volgt een overzicht van de aanbevolen procedures. Met de beste resultaten kunnen ze de productzoekmethode eenvoudig implementeren. Adobe raadt aan dat clients elk van hun productzoekmethoden (in het algemeen) als volgt kunnen configureren:

* Merchandising Enabled: Enabled
* Merchandising [ syntaxis ]: De Veranderlijke Syntaxis van de omzetting
* Toewijzing [ bindende ]: Oorspronkelijke Waarde (eerst)
* Verlopen na: de hoeveelheid tijd die een product in een winkelwagentje blijft voordat het automatisch wordt verwijderd (bijvoorbeeld 14 dagen, 30 dagen, enz.).  Als dit niet het geval is, loopt u af na de gebeurtenis &quot;purchase&quot;
* Tekst: Tekst
* Merchandising Binding Events: Product View, Cart Add, and Purchase

## Wat doen Bindende Gebeurtenissen eigenlijk?

Wanneer een bindende gebeurtenis in de zelfde servervraag zoals de productvariabele bevat, binden de waarden van de Verkoop eVar (die de Veranderlijke Syntaxis van de Omzetting gebruiken) in hun postkolom aan de productvariabele. Gebaseerd op het vroegere voorbeeld, veronderstel dat één servervraag de volgende waarden van de Verkoop eVar bevat:

```js
s.eVar2="sandals";
s.eVar1="internal keyword search";
s.eVar3="non-internal campaign";
s.eVar4="non-browse";
s.eVar5="non-cross sell";
```

Zoals eerder uitgelegd, blijven de bovenstaande eVars na de huidige hit via hun respectievelijke post_evar kolom bestaan. Daarom transformeren Adobe-servers de bovenstaande eVars in het volgende:

```js
post_eVar2="sandals";
post_eVar1="internal keyword search";
post_eVar3="non-internal campaign";
post_eVar4="non-browse";
post_eVar5="non-cross sell";
```

Deze postkolommen worden opgeslagen in de Adobe-database en blijven na de huidige hit staan waar ze aanvankelijk waren ingesteld. Hierbij wordt ervan uitgegaan dat er geen vervaldatum of instelling van variabele plaatsvindt.  Adobe servers hebben deze post_evar waarden &quot;beschikbaar&quot;op het tijdstip dat zij om het even welke toekomstige servervraag verwerken die zowel de bindende gebeurtenis als de productvariabele bevatten.

De binding die plaatsvindt, is uitsluitend tussen deze post_evar waarden en de inhoud van de productvariabele. De bindende gebeurtenis &quot;bindt&quot;niet noodzakelijk aan of eVars of de productvariabele. Het is de &#39;katalysator&#39; die de Adobe-servers vertelt om de post_evar-waarden aan de producten te binden.

Stel dat bij een toekomstige hit de volgende variabelen worden ingesteld:

```js
s.products=";sandals123"
s.events="prodView";
```

In de kolommen post_evar zien de Adobe-verwerkingsservers dit resultaat als volgt:

```js
s.products=";sandals123";
s.events="prodView";
post_eVar2="sandals";
post_eVar1="internal keyword search";
post_eVar3="non-internal campaign";
post_eVar4="non-browse";
post_eVar5="non-cross sell";
```

Stel dat eVar1, eVar2, eVar3, eVar4 en eVar5 zo zijn geconfigureerd dat `prodView` als bindingsgebeurtenis wordt gebruikt. Als om het even welk van deze eVars niet wordt gevormd om prodView als bindende gebeurtenis te gebruiken, dan zal het binden tussen dat (misconfigured) eVar en de productvariabele niet plaatsvinden.

Binding produceert enkele zeer interessante resultaten, die in de waarde van de post_products kolom kunnen worden gezien. De binding transformeert de bovenstaande code en stelt nog een paar postkolommen in, als volgt:

```js
post_events="prodView";
post_products=";sandals123;;;;eVar2=sandals|eVar1=internal keyword search|eVar3=non-internal campaign|eVar4=non-browse|eVar5=non-cross-sell";
```

De waarde in de post_products kolom zou aan u vertrouwd kunnen zijn. Schuif omhoog in dit document en vergelijk deze post_products-waarde met de s.products-waarde zoals hieronder weergegeven. De kolom post_products is ingesteld met de syntaxis van de variabele Product.

Dit betekent dat met Binding &quot;de waarde van Conversion Variable Syntax eVar wordt gekopieerd naar de productvariabele via de productsyntaxis. Deze kopieeractie vindt alleen plaats wanneer de productvariabele en een bindingsgebeurtenis (ingesteld via de eVar-configuratie) zich in hetzelfde verzoek bevinden. Op dat moment zijn de waarden in de kolom(men) post_eVar gebonden aan het product. This Binding is represented via Product Syntax as stored in the post_products column.

## Merchandising Vars, de metrische Instanties, en Attributie

Wanneer een standaard eVar in een de servervraag van Analytics wordt verzonden, krijgt de waarde in zijn post_evar kolom altijd een Instantie die aan het wordt toegewezen. Exemplaren geven het aantal keren aan dat een eVar is ingesteld op een bepaalde waarde in een afbeeldingsaanvraag.

Stel dat `eVar10` een standaard-eVar met [!UICONTROL Last Touch] -kenmerk is. Als u `s.eVar10="hello world"` instelt op een pagina, wordt de waarde van &quot;hello world&quot; doorgegeven aan de kolom post_evar10 wanneer Adobe de hit verwerkt. De metrische waarde van de instanties is gelijk aan &quot;1&quot; voor elke individuele `eVar10` instelling van `hello world` . Onthoud dat een instantie niet altijd wordt opgenomen wanneer de kolom post_evar een waarde heeft. In plaats daarvan bepaalt de kolom post_evar welke waarde de instantie krijgt wanneer een instantie wordt geregistreerd.

Instanties voor een handelende eVar geven toewijzing aan de waarden die de eVar verzamelt. Maar dit gebeurt alleen wanneer een product dat aan de handelswaarde van eVar gebonden was, tegelijkertijd &quot;interactie&quot; had.

Als u `s.eVar1="Internal Keyword Search"` bijvoorbeeld zelf instelt, krijgt de eVar1-waarde van &quot;Intern trefwoord zoeken&quot; geen metrische waarde van Instance. Een instantie WORDT op dat punt geregistreerd. Tenzij een product echter is gebonden aan de waarde &quot;Intern trefwoord zoeken&quot; die tegelijkertijd `eVar1` is ingesteld, wordt de instantie toegewezen aan het niet-opgegeven emmertje. Met andere woorden, de `eVar1` -waarde van &quot;Intern trefwoord zoeken&quot; kan een instantie krijgen. Maar dit gebeurt alleen wanneer een product dat is gebonden aan de waarde van &quot;Intern trefwoord zoeken&quot; wordt weergegeven in de productvariabele in dezelfde afbeeldingsaanvraag.

Samengevat, zonder extra configuratie, is uit-van-de-doos Metrisch Instanties voor een het verhandelen eVar minder dan nuttig. Gelukkig, gaf Adobe [ Attributie ](/help/analyze/analysis-workspace/attribution/overview.md) vrij. Hiermee kunt u meerdere attributiemodellen toepassen op elke aangepaste metrische waarde die Adobe Analytics verzamelt. Metriek die deze attributiemodellen toepassen gebruikt niet de waarden in de post_evar kolommen of de waarden die aan om het even welk bepaald product worden gebonden. In plaats daarvan gebruiken deze meetgegevens alleen de waarden die via de afbeeldingsaanvragen zelf worden doorgegeven (of waarden die via de verwerkingsregels van Adobe Analytics worden vastgelegd). U kunt de eigenschappen in Attributie gebruiken om een correct toegeschreven instanties metrisch voor alle koopwaar te krijgen Vars die de Syntaxis van de Variabele van de Omzetting gebruiken.

![ Uitgezochte Attributie ](/help/admin/tools/manage-rs/edit-settings/conversion-var-admin/assets/attribution-select.png)

Wanneer u een exemplaar-metrische waarde toevoegt voor een eVar die een transactie aanbrengt aan een rapport, is het juiste kenmerkingsmodel het model &quot;Last Touch&quot;. De instelling voor Venster opzoeken voor het model is in dit geval niet van belang. De reden is dat een &#39;gedwongen&#39; laatste aanraakattributiemodel altijd exemplaarkredieten geeft aan elke individuele waarde die via een aanvraag wordt doorgegeven. Dit ongeacht of de eigenlijke attributie-/bindingsinstellingen van de eVar gelijk zijn aan &quot;Meest recente (laatste)&quot; of &quot;Oorspronkelijke waarde (eerste)&quot;.
