---
title: Bezoeken
description: Een reeks paginaweergaven in een vergadering.
feature: Metrics
exl-id: 4f78f2b5-f958-44fe-876a-83f07980beec
source-git-commit: a3a23e1d13bc10305a8cb991b73c2873a58baf63
workflow-type: tm+mt
source-wordcount: '672'
ht-degree: 0%

---

# Bezoeken

De metrische &quot;bezoeken&quot; [ ](overview.md) toont het aantal zittingen over alle bezoekers op uw plaats.

## Hoe deze metrische waarde wordt berekend

Een bezoek is altijd gekoppeld aan een tijdsperiode, dus u weet of u een nieuw bezoek wilt tellen als dezelfde persoon naar uw site terugkeert. Een bezoek begint wanneer de gebruiker voor het eerst op uw site arriveert. Een bezoek eindigt wanneer zij aan om het even welke volgende criteria voldoen:

* **30 minuten van inactiviteit**: Bijna alle zittingen beëindigen op deze manier. Als er meer dan 30 minuten tussen de treffers verlopen, wordt een nieuw bezoek gestart.
* **12 uren van activiteit**: Als een gebruiker constant beeldverzoeken zonder enige 30 minieme hiaten voor meer dan 12 uren in brand steekt, begint een nieuw bezoek automatisch.
* **2500 treffers**: Als een gebruiker een groot aantal treffers produceert zonder een nieuwe zitting te beginnen, wordt een nieuw bezoek geteld na 2500 beeldverzoeken.
* **100 hits in 100 seconden**: Als een bezoek meer dan 100 hits heeft die in de eerste 100 seconden van het bezoek voorkomen, beëindigt het bezoek automatisch. Dit gedrag wijst typisch op beide activiteit, en deze beperking wordt afgedwongen om rapportprestaties te helpen verbeteren.

Een bezoek valt niet noodzakelijk samen met een browsersessie vanwege de bovenstaande criteria. Een van de meest voorkomende verschillen is de plaats waar een bezoeker naar uw site navigeert, het tabblad langer dan 30 minuten open laat en het bladeren hervat. Hoewel deze actie technisch gezien deel uitmaakt van dezelfde sessie, beschouwt de Adobe deze actie als twee aparte bezoeken.

## Gedrag dat van invloed is op bezoeken

Als een bezoeker een van deze handelingen uitvoert, wordt een nieuw bezoek gestart:

* Hiermee verwijdert u de cookies halverwege de sessie en gaat u door met het bladeren door uw site
* Laat uw site langer dan 30 minuten open op een tabblad en vervolgt het bladeren
* Opent een andere browser en navigeert naar uw site op dezelfde computer
* Dezelfde persoon die op verschillende apparaten door uw site bladert

Als een bezoeker om het even welk van deze acties uitvoert, begint een nieuw bezoek **niet** zolang er minder dan 30 minuten tussen opeenvolgende treffers is:

* Sluit hun browser en navigeer vervolgens opnieuw naar uw site
* Start de computer opnieuw op, opent dezelfde browser en navigeert opnieuw naar uw site
* Overgangen aan een verschillend netwerk, zoals het losmaken van een getelegrafeerd netwerk dokkend post aan een draadloos netwerk
* Hiermee kunt u op meerdere tabbladen door uw site bladeren. Als een bezoeker heen en weer schakelt tussen tabs, telt elke hit als onderdeel van hetzelfde bezoek.

## De definitie van een bezoek wijzigen

U kunt de definitie van een bezoek wijzigen in een andere tijd dan 30 minuten.

* Voor [ Virtuele rapportreeksen ](../vrs/vrs-about.md), kunt u de bezoekonderbreking veranderen gebruikend de [!UICONTROL Visit timeout] drop-down lijst. U kunt de time-out voor een bezoek wijzigen in een redelijke waarde.
* Voor standaardrapportreeksen kunt u contact opnemen met de klantenservice om te verzoeken dat de duur van het bezoek wordt verkort voor een bepaalde rapportsuite. De lengte van het bezoek voor standaard rapportreeksen kan niet 30 minuten overschrijden, zodat kunt u het slechts verkorten.

## Bezoeken die een datumgrens omspannen

Een bezoek telt voor elke betrokken periode. Als u bijvoorbeeld een bezoeker hebt die op maandag om 11:45 uur begint met navigeren op uw site, en vervolgens zijn laatste verzoek om een afbeelding op dinsdag om 12:10 uur verzendt, wordt een bezoek toegeschreven aan zowel maandag als dinsdag. Nochtans, wordt het totale bezoek metrisch gededupliceerd, tonend één enkel bezoek voor de waaier van de projectdatum.

## Bezoeken op dimensie versus totale bezoeken

De bezoeken in context van een afmeting (bijvoorbeeld, [ Marketing kanaal ](../dimensions/marketing-channel.md)) tonen het aantal bezoeken dat een bepaald afmetingspunt op elk ogenblik bevatte. Items met meerdere dimensies bestaan vaak bij verschillende treffers tijdens hetzelfde bezoek. Het is doorgaans niet zinvol om te proberen om bezoeken die over dimensie-items rapporteren, samen te vatten.

## Bezoek alle bezoekers in Data Warehouse

De metrische &#39;Bezoeken - Alle Bezoekers&#39; is beschikbaar in Data Warehouse naast de &#39;Bezoekingen&#39;-meting. De metrische waarde &#39;Visits - All Visitors&#39; is vergelijkbaar met die van &#39;Visits&#39; in andere analyseprogramma&#39;s. De metrische waarde &#39;Visits&#39; in Data Warehouse sluit bezoekers uit die geen permanente cookies hebben. De Adobe beveelt aan &quot;Bezoekingen - Alle Bezoekers&quot;in Data Warehouse verzoeken te gebruiken waar bezoeken als metrisch worden gewenst.
