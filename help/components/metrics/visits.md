---
title: Bezoeken
description: Een reeks paginaweergaven tijdens een sessie.
feature: Metrics
exl-id: 4f78f2b5-f958-44fe-876a-83f07980beec
source-git-commit: 78cfb1f3c4d45fc983982a8da11b66f2b2c9ecbc
workflow-type: tm+mt
source-wordcount: '657'
ht-degree: 1%

---

# Bezoeken

De metrische waarde &#39;Bezoekingen&#39; toont het aantal sessies voor alle bezoekers op uw site.

## Hoe deze metrische waarde wordt berekend

Een bezoek is altijd gekoppeld aan een tijdsperiode, dus u weet of u een nieuw bezoek wilt tellen als dezelfde persoon naar uw site terugkeert. Een bezoek begint wanneer de gebruiker voor het eerst op uw site arriveert. Een bezoek eindigt wanneer zij aan om het even welke volgende criteria voldoen:

* **30 minuten inactiviteit**: Bijna alle sessies eindigen op deze manier. Als er meer dan 30 minuten tussen de treffers verlopen, wordt een nieuw bezoek gestart.
* **12 uur activiteit**: Als een gebruiker voortdurend verzoeken om afbeeldingen gedurende meer dan 12 uur zonder tussenruimten van 30 minuten brandt, wordt automatisch een nieuw bezoek gestart.
* **2500 hits**: Als een gebruiker een groot aantal hits genereert zonder een nieuwe sessie te starten, wordt een nieuw bezoek geteld na 2500 afbeeldingsverzoeken.
* **100 treffers in 100 seconden**: Als een bezoek meer dan 100 hits heeft die in de eerste 100 seconden van het bezoek optreden, eindigt het bezoek automatisch. Dit gedrag wijst typisch op beide activiteit, en deze beperking wordt afgedwongen om rapportprestaties te helpen verbeteren.

Een bezoek valt niet noodzakelijk samen met een browsersessie vanwege de bovenstaande criteria. Een van de meest voorkomende verschillen is de plaats waar een bezoeker naar uw site navigeert, het tabblad langer dan 30 minuten open laat en het bladeren hervat. Hoewel deze actie technisch deel uitmaakt van dezelfde sessie, beschouwt Adobe deze actie twee aparte bezoeken.

## Gedrag dat van invloed is op bezoeken

Als een bezoeker een van deze handelingen uitvoert, wordt een nieuw bezoek gestart:

* Wist de cache halverwege de sessie en gaat verder met bladeren door uw site
* Laat uw site langer dan 30 minuten open op een tabblad en vervolgt het bladeren
* Hiermee opent u een andere browser en navigeert u naar uw site op dezelfde computer
* Dezelfde persoon die op verschillende apparaten door uw site bladert

Als een bezoeker een van deze handelingen uitvoert, wordt tijdens een nieuw bezoek **niet** beginnen zolang er minder dan 30 minuten zijn tussen opeenvolgende treffers:

* Sluit hun browser en navigeer vervolgens opnieuw naar uw site
* Start de computer opnieuw op, opent dezelfde browser en navigeert opnieuw naar uw site
* Overgangen aan een verschillend netwerk, zoals het losmaken van een getelegrafeerd netwerk dokkend post aan een draadloos netwerk
* Hiermee kunt u op meerdere tabbladen door uw site bladeren. Als een bezoeker heen en weer schakelt tussen tabs, telt elke hit als onderdeel van hetzelfde bezoek.

## De definitie van een bezoek wijzigen

U kunt de definitie van een bezoek wijzigen in een andere tijd dan 30 minuten.

* Voor [Virtuele rapportsuites](../vrs/vrs-about.md), kunt u de time-out van het bezoek wijzigen met de opdracht [!UICONTROL Visit timeout] vervolgkeuzelijst. U kunt de time-out voor een bezoek wijzigen in een redelijke waarde.
* Voor standaardrapportreeksen kunt u contact opnemen met de klantenservice om te verzoeken dat de duur van het bezoek wordt verkort voor een bepaalde rapportsuite. De lengte van het bezoek voor standaard rapportreeksen kan niet 30 minuten overschrijden, zodat kunt u het slechts verkorten.

## Bezoeken die een datumgrens omspannen

Een bezoek telt voor elke betrokken periode. Als u bijvoorbeeld een bezoeker hebt die op maandag om 11:45 uur begint met navigeren op uw site, en vervolgens zijn laatste verzoek om een afbeelding op dinsdag om 12:10 uur verzendt, wordt een bezoek toegeschreven aan zowel maandag als dinsdag. Nochtans, wordt het totale bezoek metrisch gededupliceerd, tonend één enkel bezoek voor de waaier van de projectdatum.

## Bezoeken op dimensie versus totale bezoeken

Bezoeken in het kader van een dimensie (bijvoorbeeld [Marketingkanaal](../dimensions/marketing-channel.md)) het aantal bezoeken dat op enig moment een bepaald onderdeel van de dimensie bevatte. Items met meerdere dimensies bestaan vaak bij verschillende treffers tijdens hetzelfde bezoek. Het is doorgaans niet zinvol om te proberen om bezoeken die over dimensie-items rapporteren, samen te vatten.

## Bezoek alle bezoekers in Data Warehouse

De metrische &#39;Bezoeken - Alle Bezoekers&#39; is beschikbaar in Data Warehouse naast de &#39;Bezoekingen&#39;-meting. De metrische waarde &#39;Visits - All Visitors&#39; is vergelijkbaar met die van &#39;Visits&#39; in andere analyseprogramma&#39;s. De metrische waarde &#39;Visits&#39; in Data Warehouse sluit bezoekers uit die geen permanente cookies hebben. Adobe raadt aan &#39;Bezoekingen - Alle Bezoekers&#39; te gebruiken in Data Warehouse-aanvragen waar bezoekers als metrische waarde gewenst zijn.
