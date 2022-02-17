---
description: Contextbewuste sessies in virtuele rapportsuites veranderen hoe Adobe Analytics mobiele bezoeken berekent. In dit artikel worden de verwerkingsimplicaties beschreven van achtergrondopdrachten en startgebeurtenissen van apps (beide ingesteld door de SDK van mobiele apparaten) voor de definitie van mobiele bezoeken.
title: Contextbewuste sessies
feature: VRS
exl-id: 5e969256-3389-434e-a989-ebfb126858ef
source-git-commit: 7a47d837eeae65f2e98123aca78029bfeb7ffe9d
workflow-type: tm+mt
source-wordcount: '1563'
ht-degree: 0%

---

# Contextbewuste sessies

Contextbewuste sessies in virtuele rapportsuites veranderen hoe Adobe Analytics bezoeken van elk apparaat berekent. In dit artikel worden ook de verwerkingsimplicaties beschreven van achtergrondopdrachten en startgebeurtenissen van apps (beide ingesteld door de SDK van mobiele apparaten) voor de definitie van mobiele bezoeken.

U kunt een bezoek op elke gewenste manier definiëren zonder de onderliggende gegevens te wijzigen, zodat deze overeenkomen met de manier waarop bezoekers met uw digitale ervaringen werken.

Hier is een video over contextbewuste sessies:

>[!VIDEO](https://video.tv.adobe.com/v/23545/?quality=12)

## URL-parameter voor klantperspectief

Het proces van de gegevensinzameling van Adobe Analytics staat u toe om een parameter van het vraagkoord te plaatsen die het klantenperspectief (als &quot;cp&quot;parameter van het vraagkoord wordt aangeduid) specificeren. In dit veld wordt de status van de digitale toepassing van de eindgebruiker aangegeven. Zo kunt u zien of een hit is gegenereerd terwijl een mobiele app zich in de achtergrondstatus bevond.

## Achtergrondbewerking

Een hit op de achtergrond is een type hit dat vanuit Adobe Mobile SDK versie 4.13.6 en hoger naar Analytics wordt verzonden wanneer de toepassing een aanvraag voor bijhouden indient in een achtergrondstatus. Voorbeelden hiervan zijn:

* Gegevens verzonden tijdens een kruising met een geo-hek
* Een pushmeldingsinteractie

De volgende voorbeelden schetsen de logica die wordt gebruikt in het bepalen wanneer een bezoek voor om het even welke bezoeker begint en beëindigt wanneer de &quot;Voorkomen van AchtergrondHits van het Begin van een nieuw Bezoek&quot;het plaatsen voor een virtuele rapportreeks is of niet wordt toegelaten.

**Als &quot;Voorkomen dat de Hits van de Achtergrond een nieuw Bezoek&quot;begint niet wordt toegelaten:**

Als deze functie niet is ingeschakeld voor een virtuele rapportsuite, worden achtergrondopdrachten op dezelfde manier behandeld als elke andere hit, wat betekent dat ze nieuwe bezoeken beginnen en op dezelfde manier werken als voorgrondhits. Als een achtergrondhit bijvoorbeeld minder dan 30 minuten optreedt (de standaardsessietime-out voor een rapportsuite) voordat een set voorgrondhits wordt weergegeven, maakt de achtergrondhit deel uit van de sessie.

![](assets/nogood1.jpg)

Als de achtergrondhit meer dan 30 minuten vóór eventuele voorgrondhits optreedt, maakt de achtergrondhit een eigen bezoek voor een totaal aantal bezoeken van 2.

![](assets/nogood2.jpg)

**Als &quot;Voorkomen dat de Hits van de Achtergrond een nieuw Bezoek&quot;wordt toegelaten:**

In de volgende voorbeelden wordt het gedrag van achtergrondopdrachten getoond wanneer deze functie is ingeschakeld.

Voorbeeld 1: Een achtergrondhit treedt op in een bepaalde tijdsperiode (t) voordat een reeks voorgrondhits wordt weergegeven.

![](assets/nogoodexample1.jpg)

In dit voorbeeld, als *t* is groter dan de gevormde het bezoekonderbreking van de virtuele rapportreeks, dan wordt de achtergrondhit uitgesloten van het bezoek dat door de voorgrondhits wordt gevormd. Als de time-out van het bezoek aan de virtuele rapportsuite bijvoorbeeld is ingesteld op 15 minuten, en *t* 20 minuten lang was het bezoek van deze serie hits ( de groene omtrek toont ) geen aanleiding voor een achtergrondaanval . Dit betekent dat alle eVars die zijn ingesteld met een &quot;bezoek&quot;-vervaldatum bij een treffer op de achtergrond **niet** blijven in het volgende bezoek, en een container van het bezoekensegment zou slechts de voorgrondhits binnen het groene overzicht omvatten.

![](assets/nogoodexample1-2.jpg)

Omgekeerd, als *t* is minder dan de gevormde het bezoekonderbreking van de virtuele rapportreeks, is achtergrondhit inbegrepen als deel van het bezoek alsof het een voorgrondslag (die door het groene overzicht wordt getoond) was:

![](assets/nogoodexample1-3.jpg)

Dit betekent dat:

* Elke eVars die zijn ingesteld met de vervaldatum van het bezoek op de achtergrond blijven hun waarden behouden op de andere hits in dit bezoek.
* Om het even welke waarden die in het achtergrondoppervlak worden geplaatst zijn inbegrepen in de beoordeling van de de containercontainer van het vlekkensegment.

In beide gevallen zou het totale aantal bezoeken 1 bedragen.

Voorbeeld 2: Als een achtergrondhit optreedt na een reeks voorgrondhits, is het gedrag vergelijkbaar:

![](assets/nogoodexample2.jpg)

Als de achtergrondhit optreedt na de geconfigureerde time-out van de virtuele rapportsuite, maakt de achtergrondhit geen deel uit van een sessie (weergegeven in groen):

![](assets/nogoodexample2-1.jpg)

Evenzo, als de tijdsperiode *t* was minder dan de gevormde onderbreking van de virtuele rapportreeks, is de achtergrondhit inbegrepen in het bezoek dat door de vorige foreground wordt gevormd:

![](assets/nogoodexample2-2.jpg)

Dit betekent dat:

* Elke eVars die op de vorige voorgrondhits zijn ingesteld met de vervaldatum van het &quot;bezoek&quot;, behouden hun waarden op de achtergrond die tijdens dit bezoek werd gevonden.
* Om het even welke waarden die in het achtergrondoppervlak worden geplaatst zijn inbegrepen in de beoordeling van de de containercontainer van het vlekkensegment.

Zoals eerder zou het totale aantal bezoeken in beide gevallen 1 zijn.

Voorbeeld 3: In sommige gevallen kan een achtergrondhit ertoe leiden dat twee afzonderlijke bezoeken worden gecombineerd tot één bezoek. In het volgende scenario wordt een achtergrondhit voorafgegaan en gevolgd door een reeks voorgrondtreffelijke resultaten:

![](assets/nogoodexample3.jpg)

Indien in dit voorbeeld: *t1* en *t2* zijn allebei minder dan de virtuele rapportreeks gevormde het bezoekonderbreking, al deze klappen in één enkel bezoek zouden worden gecombineerd, zelfs als *t1* en *t2* samen zijn groter dan de time-out van het bezoek:

![](assets/nogoodexample3-1.jpg)

Indien echter *t1* en *t2* zijn groter dan de virtuele gevormde onderbreking van de rapportreeks, zouden deze klappen in twee verschillende bezoeken worden gescheiden:

![](assets/nogoodexample3-2.jpg)

Evenzo (zoals in onze vorige voorbeelden), als *t1* is kleiner dan de time-out en *t2* minder is dan de time-out die de achtergrondhit zou opnemen in het eerste bezoek:

![](assets/nogoodexample3-3.jpg)

Indien *t1* groter is dan de time-out en *t2* minder dan de time-out is, wordt de gevonden achtergrond opgenomen in het tweede bezoek:

![](assets/nogoodexample3-4.jpg)

Voorbeeld 4: In scenario&#39;s waar een reeks achtergrondklappen binnen de virtuele onderbrekingsperiode van het de verslagreeks voorkomen, vormen de klusjes een onzichtbaar &quot;achtergrondopdracht&quot;die niet op de bezoektelling telt en niet toegankelijk gebruikend een container van de bezoeksegmentatie is.

![](assets/nogoodexample4.jpg)

Hoewel dit niet als een bezoek wordt beschouwd, blijven alle eVars-sets die verlopen tijdens een bezoek hun waarden aan de andere kant behouden als de achtergrondresultaten in dit &quot;achtergrondbezoek&quot;.

Voorbeeld 5: Voor scenario&#39;s waar de veelvoudige achtergrondklappen achtereenvolgens na een reeks voorgrondklappen voorkomen, is het mogelijk (afhankelijk van onderbreking het plaatsen) dat de achtergrondklappen een bezoek langer levend houden dan de periode van de bezoekonderbreking. Als *t1* en *t2* samen waren groter dan de virtuele time-out van het rapportsuite bezoek maar individueel minder dan de time-out, dan zou het bezoek zich nog steeds uitstrekken tot beide background hits :

![](assets/nogoodexample5.jpg)

Op dezelfde manier geldt dat als een reeks achtergrondresultaten plaatsvindt voordat een reeks voorgrondgebeurtenissen plaatsvindt, dit ook gebeurt:

![](assets/nogoodexample5-1.jpg)

Achtergrondhits gedragen zich op deze manier om eventuele attributie-effecten van Vars of andere variabelen die tijdens achtergrondtreffers zijn ingesteld, te behouden. Hierdoor kunnen downstream-voorgrondconversiegebeurtenissen worden toegewezen aan handelingen die zijn uitgevoerd terwijl een app zich in de achtergrondstatus bevond. Het staat ook een container van het bezoekensegment toe om achtergrondklappen te omvatten die in een stroomafwaartse voorgrondzitting resulteerden die nuttig is om de doeltreffendheid van het duwbericht te meten.

## Metrisch gedrag bezoeken

Het aantal bezoeken is uitsluitend gebaseerd op het aantal bezoeken dat ten minste één foreground hit omvat. Dit betekent dat zwevende achtergrondopdrachten of &quot;achtergrondbezoeken&quot; niet meetellen voor de meting Visit.

## Tijd besteed per bezoek metrisch gedrag

De tijd die wordt doorgebracht wordt nog berekend op een analoge manier aan hoe het zonder achtergrondklappen gebruikend de tijd tussen klappen is. Hoewel bij een bezoek achtergrondopdrachten worden opgenomen (omdat deze direct genoeg optraden voor voorgrondhits), worden deze hits opgenomen in de berekening van de tijd die u per bezoek hebt doorgebracht, alsof het een voorgrondhit betreft.

## Instellingen voor verwerking achtergrondkleur

Omdat achtergrondhit-verwerking alleen beschikbaar is voor virtuele rapportsuites die gebruikmaken van Report Time Processing, biedt Adobe Analytics ondersteuning voor twee manieren om achtergrondresultaten te verwerken, zodat de bezoektellingen behouden blijven in de basisrapportsuite die geen gebruikmaken van Report Time Processing. Als u deze instelling wilt openen, navigeert u naar de Adobe Analytics-Admin Console en gaat u naar de instellingen van de toepasselijke basisrapportsuite. Navigeer vervolgens naar het menu &quot;Mobiel beheer&quot; en vervolgens naar het submenu &quot;Rapportering mobiele toepassing&quot;.

1. &quot;Verouderde verwerking op&quot;: Dit is het gebrek dat voor alle rapportreeksen plaatst. Het verlaten van erfenisverwerking op processen achtergronden als normale klappen in onze verwerkingspijplijn voor wat de niet-het rapportreeks van het het basisrapport van de Attributie van de Tijd van de Attributie van het Rapport betreft. Dit betekent dat om het even welke achtergrondklappen die in de reeks van het basisrapport verhogingbezoeken als normale slag verschijnen. Als u geen achtergrondopdrachten wilt verschijnen in uw reeks van het basisrapport, verander deze het plaatsen in &quot;Off&quot;.
1. &quot;Verouderde verwerking uitgeschakeld&quot;: Met erfenisverwerking voor achtergrondklappen weg, worden om het even welke achtergrondklappen die naar de reeks van het basisrapport worden verzonden genegeerd door de Reeks van het basisrapport en zijn slechts toegankelijk wanneer een virtuele rapportreeks die op deze reeks van het basisrapport wordt gecreeerd wordt gevormd om de Verwerking van de Tijd van het Rapport te gebruiken. Dit betekent dat om het even welke gegevens die door achtergrondklappen worden gevangen die naar deze reeks van het basisrapport worden verzonden slechts in een toegelaten virtuele rapportreeks van de Tijd van het Rapport van de Verwerking verschijnen.

   Deze instelling is bedoeld voor klanten die willen profiteren van de nieuwe achtergrondhit-verwerking zonder de bezoektellingen van hun basislapport te wijzigen.

In beide gevallen worden achtergrondopdrachten tegen dezelfde kosten in rekening gebracht als andere resultaten die naar Analytics worden verzonden.

## Nieuwe bezoeken starten bij elke keer dat de app wordt gestart

Naast de hitteverwerking op de achtergrond kunnen virtuele rapportsuites een nieuw bezoek afdwingen om te beginnen wanneer de mobiele SDK een app-startgebeurtenis verzendt. Als deze instelling is ingeschakeld, wordt telkens wanneer een gebeurtenis App Launch vanuit de SDK wordt verzonden, een nieuw bezoek afgedwongen, ongeacht of een open bezoek de time-out heeft bereikt. De hit met de startgebeurtenis van de app wordt opgenomen als de eerste hit tijdens het volgende bezoek en verhoogt het aantal bezoeken en maakt een aparte container voor segmentatie.
