---
description: Hiermee geeft u informatie weer over bezoekers, zoals het aantal bezoekers, de loyaliteit van de klant en de kenmerken van de bezoeker.
title: Bezoekersrapporten
topic: Ad hoc analysis
uuid: 3e9b41d1-d6ff-47a8-aa6b-829df1040c34
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Bezoekersrapporten

Hiermee geeft u informatie weer over bezoekers, zoals het aantal bezoekers, de loyaliteit van de klant en de kenmerken van de bezoeker.

## Geretourneerde frequentie {#concept_447A99B71E484D27A7A02888CC51FD3D}

Geeft de tijdsduur weer die verstrijkt tussen bezoeken van terugkerende bezoekers en het aantal bezoeken dat in elke tijdlengtecategorie valt. Gebruik het rapport om de gemiddelde hoeveelheid tijd te zien die de herhaalde bezoekers gaan zonder uw plaats te bezoeken, en de tendensen in herhaalde klanten gaan.

<!-- 

c_reports_return_freq.xml

 -->

Bijvoorbeeld, die de metrische Orden in dit rapport toont helpt een detailhandelsplaats de meest efficiënte tijd tussen bezoeken in het produceren van omzetting begrijpen. Gebruik deze informatie om bezoekers die een bepaalde periode hebben doorlopen zonder uw site te bezoeken, effectief op de markt te brengen.

U kunt:

* Vermeld het aantal terugkeerbezoekers en de frequentie van hun terugkeerbezoeken.
* Evalueer de aantrekkingskracht en relevantie van uw website voor bezoekers in de loop van de tijd.
* Weet hoe vastbesloten uw site is voor bezoekers en hoe vaak ze zich gedwongen voelen om terug te keren voor verdere interactie of updates.
* Bepaal de impact van de inhoud en promoties van uw website op uw bezoekers.

Dit rapport heeft standaard de volgende tijdsduur:

* Minder dan één dag
* Eén tot drie dagen
* Drie tot zeven dagen
* Zeven tot veertien dagen
* Veertien dagen tot één maand
* langer dan één maand

## Bezoek nummer {#concept_BBB614072FD74379B1A8520ACB75AE9A}

Geeft aan welke bezoeknummers van de klant op uw site het meest van invloed waren op uw succescijfers. Een bezoeker die een eerste bezoek aan uw site brengt, wordt meegeteld in het item Bezoek nummer 1 op de regel. Bezoekers die voor een tweede bezoek terugkeren naar de site, worden meegeteld in het onderdeel Bezoek nummer 2, enzovoort.

<!-- 

c_reports_visit_number.xml

 -->

U kunt dit rapport gebruiken als een uitvalrapport om te zien of bezoekers terugkeren. U kunt ook een metrische omzet toevoegen om te zien of u meer opbrengst van aanvankelijke bezoeken of verdere bezoeken produceert.

Dit rapport kan bijvoorbeeld vragen beantwoorden zoals: Hebben klanten die bij hun vierde bezoek hebben aangeschaft, meer inkomsten gegenereerd dan klanten die bij hun eerste bezoek hebben aangeschaft?

U kunt dit rapport onderverdelen door een ander rapport of een variabele om te bepalen:

* Hoeveel bezoeken neemt het typisch een gebruiker die door campagne XYZ klikte om een aankoop te maken.
* Of gebruikers in Tokio bijvoorbeeld meer bezoeken maken voordat ze een lead genereren dan gebruikers in Londen.

> [!NOTE] Als dezelfde bezoeker uw website meerdere keren in dezelfde periode bezoekt, wordt elk opgegeven bezoeknummer verhoogd voor elk bezoek.

Dit rapport is gebaseerd op de gegevens van de bezoeker-id die bij elke treffer van bezoekers worden doorgegeven aan Adobe. Terwijl deze gegevens worden ontvangen, vergelijkt Adobe deze met de gegevens van de historische bezoeker-id om te bepalen of de hit is:

* Een nieuwe bezoeker (bezoeknummer is gelijk aan 1).
* Een vorige bezoeker die doorgaat met een bezoek (bezoeknummer wordt niet verhoogd).
* Een vorige bezoeker die een nieuw bezoek brengt (het Aantal van het Bezoek wordt verhoogd met één).

> [!NOTE] Elke Analytics-bezoeker-id is gekoppeld aan een bezoekersprofiel op Adobe-servers. Bezoekersprofielen worden na ten minste 13 maanden inactiviteit verwijderd, ongeacht de vervaldatum van de cookie van de bezoeker.

## Loyalty van klant {#concept_991F758BAA304B7B9D48BD73BBB62FE5}

Gebruik dit rapport om te zien of uw opbrengst het meest door nieuwe klanten of door herhaalde klanten wordt beïnvloed.

<!-- 

c_reports_customerloyalty.xml

 -->

Het [!UICONTROL Customer Loyalty] rapport toont aankooppatronen van klanten die op vier categorieën loyaliteit worden gebaseerd:

* **Geen klant**: Bezoekers die nog nooit hebben gekocht
* **Nieuwe klant**: Bezoekers die één aankoop hebben gedaan
* **Klanten** terugsturen: Bezoekers die 2 aankopen hebben gedaan
* **Klanten** met logo&#39;s:bezoekers die meer dan 3 aankopen hebben gedaan

> [!NOTE] Wanneer u deze maatstaven gebruikt, worden alle bezoeken van gebruikers (of alle bezoekers) in dit rapport weergegeven, ongeacht of het bezoek (of de bezoeker) een aankoop bevatte.

De status van de loyaliteit verandert na het einde van het bezoek waar een aankoopgebeurtenis plaatsvindt. Een nieuwe klant (1 aankoop) doet bijvoorbeeld een aankoop en registreert zich vervolgens voor een nieuwsbrief na die aankoop tijdens hetzelfde bezoek. De gebeurtenis voor de registratie van nieuwsbrieven wordt nog steeds beschouwd als een interactie van de Nieuwe klant, omdat de status van de klantenservice van de bezoeker pas bij het volgende bezoek verandert.

## Bezoekerprofiel {#concept_4D829198CD144DCDA667E0651F93AFC7}

Hiermee geeft u informatie weer over het type bezoeker dat naar uw site komt. U kunt dingen als plaats van de bezoeker, het type browsers en gebruikte computerhardware, gebruikte talen, en de dienstverlener van Internet gegevens voor uw bezoekers zien.

<!-- 

c_reports_visitor_profile.xml

 -->

**[!UICONTROL Languages]**: Geeft de voorkeurstalen van uw bezoekers weer, legt de standaardbrowsertaal vast en geeft de talen weer die bezoekers het vaakst op uw site gebruiken.

**[!UICONTROL Domains]**: Maakt een lijst van de organisaties en ISPs uw bezoekers gebruiken om tot uw plaats toegang te hebben. Dit rapport verschilt van het [!UICONTROL Full Domains] rapport in zoverre dat het Volledige rapport van Domeinen het volledige ISP domein registreert, terwijl dit rapport van het secundaire domein een lijst maakt.

**[!UICONTROL Top Level Domains]**: Identificeert wereldregio&#39;s waar bezoekers vandaan komen op basis van hun oorspronkelijke domeinextensie en toont hoeveel bezoekers uit deze landen komen. Domeinen die eindigen in Commercial (.com), Network (.net), Education (.edu), Government (.gov) en Organisation (.org) zijn gewoonlijk gevestigd in de Verenigde Staten en worden afzonderlijk van de rest van de domeinen vermeld.

**[!UICONTROL Visitor ZIP/Postal Code]**: Hier worden de postcodes en de postcodes weergegeven die de klanten hebben geproduceerd die het grootste effect hadden op de gegevens over het succes van de aankoop.

## GeoSegmentation {#concept_7C1B930F90F945B49205D3855CAE1813}

<!-- 

c_reports_geosegmentation.xml

 -->

Geeft de geografische dynamiek van uw bezoekers in real-time weer, inclusief de landen, staten en steden waar ze naartoe bladeren. U kunt ook belangrijke inzichten in de technologie en voorkeuren van het publiek van uw website opdoen.
