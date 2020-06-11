---
title: Bezoeken
description: Een reeks paginaweergaven tijdens een sessie.
translation-type: tm+mt
source-git-commit: 0328de560185e716a3913080feda9cd078e0f206
workflow-type: tm+mt
source-wordcount: '530'
ht-degree: 1%

---


# Bezoeken

De metrische waarde &#39;Bezoekingen&#39; toont het aantal sessies voor alle bezoekers op uw site.

## Hoe deze metrische waarde wordt berekend

Een bezoek is altijd gekoppeld aan een tijdsperiode, dus u weet of u een nieuw bezoek wilt tellen als dezelfde persoon naar uw site terugkeert. Een bezoek begint wanneer de gebruiker voor het eerst op uw site arriveert. Een bezoek eindigt wanneer zij aan om het even welke volgende criteria voldoen:

* **30 minuten inactiviteit**: Bijna alle sessies eindigen op deze manier. Als er meer dan 30 minuten tussen de treffers verlopen, wordt een nieuw bezoek gestart.
* **12 uur activiteit**: Als een gebruiker voortdurend verzoeken om afbeeldingen gedurende meer dan 12 uur zonder tussenruimten van 30 minuten brandt, wordt automatisch een nieuw bezoek gestart.
* **2500 hits**: Als een gebruiker een groot aantal hits genereert zonder een nieuwe sessie te starten, wordt een nieuw bezoek geteld na 2500 afbeeldingsverzoeken.
* **100 hits in 100 seconden**: Als een bezoek uit meer dan 100 hits bestaat die in minder dan 100 seconden voorkomen, beëindigt het bezoek automatisch. Dit gedrag wijst typisch op beide activiteit, en deze beperking wordt afgedwongen om rapportprestaties te helpen verbeteren.

Een bezoek valt niet noodzakelijk samen met een browsersessie vanwege de bovenstaande criteria. Een van de meest voorkomende verschillen is de plaats waar een bezoeker naar uw site navigeert, het tabblad langer dan 30 minuten open laat en het bladeren hervat. Hoewel deze handeling technisch gezien onderdeel is van dezelfde sessie, beschouwt Adobe deze handeling als twee aparte bezoeken.

## De definitie van een bezoek wijzigen

U kunt de definitie van een bezoek wijzigen in een andere tijd dan 30 minuten.

* Voor [Virtuele rapportsuites](../vrs/vrs-about.md), kunt u de bezoekonderbreking veranderen gebruikend [!UICONTROL Visit timeout] dropdown. U kunt de time-out voor een bezoek wijzigen in een redelijke waarde.
* Voor standaardrapportreeksen kunt u contact opnemen met de klantenservice om te verzoeken dat de duur van het bezoek wordt verkort voor een bepaalde rapportsuite. De lengte van het bezoek voor standaard rapportreeksen kan niet 30 minuten overschrijden, zodat kunt u het slechts verkorten.

## Gedrag dat van invloed is op bezoeken

Als een bezoeker een van deze handelingen uitvoert, wordt een nieuw bezoek gestart:

* Wist de cache halverwege de sessie en gaat verder met bladeren door uw site
* Laat uw site langer dan 30 minuten open op een tabblad en vervolgt het bladeren
* Hiermee opent u een andere browser en navigeert u naar uw site op dezelfde computer
* Dezelfde persoon die op verschillende apparaten door uw site bladert

Als een bezoeker een van deze handelingen uitvoert, begint een nieuw bezoek **niet** zolang er minder dan 30 minuten zijn tussen opeenvolgende treffers:

* Sluit hun browser en navigeer vervolgens opnieuw naar uw site
* Start de computer opnieuw op, opent dezelfde browser en navigeert opnieuw naar uw site
* Overgangen aan een verschillend netwerk, zoals het losmaken van een getelegrafeerd netwerk dokkend post aan een draadloos netwerk
* Hiermee kunt u op meerdere tabbladen door uw site bladeren. Als een bezoeker heen en weer schakelt tussen tabs, telt elke hit als onderdeel van hetzelfde bezoek.

## Bezoeken die een datumgrens omspannen

Een bezoek telt voor elke betrokken periode. Als u bijvoorbeeld een bezoeker hebt die op maandag om 11:45 uur begint met navigeren op uw site, en vervolgens zijn laatste verzoek om een afbeelding op dinsdag om 12:10 uur verzendt, wordt een bezoek toegeschreven aan zowel maandag als dinsdag. Nochtans, wordt het totale bezoek metrisch gededupliceerd, tonend één enkel bezoek voor de waaier van de projectdatum.
