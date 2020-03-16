---
description: De volgende informatie kan helpen problemen met de latentie van de rapportsuite in analysegegevens oplossen.
keywords: missing data;slow
subtopic: Current data
title: Beschikbaarheid en latentie van gegevens
topic: Reports
uuid: 1f0e67e3-6cea-4af8-8b18-7ae9223df7c8
translation-type: tm+mt
source-git-commit: a4a4d9e6e2d3e3ed88b4ef66e9da3b05865a9b79

---


# Beschikbaarheid van gegevens en latentie in Adobe Analytics

Doorgaans kunt u volledige gegevens in rapporten zien 2 uur nadat gegevens zijn verzameld. De volgende informatie kan helpen problemen met de latentie van de rapportsuite in analysegegevens oplossen.

## Gegevensbatchverwerking

Elke gegevensverzamelingsserver legt onbewerkte analysegegevens vast en verwerkt deze, en uploadt vervolgens gebatchgegevens op uurbasis voor rapportage. Het overdrachtsproces duurt gewoonlijk 30 minuten, zodat de normale vertraging voor verkeer dat direct optreedt nadat het vorige uploadproces is voltooid, ongeveer 90 minuten is (60 minuten totdat de volgende batch-upload plaatsvindt en 30 minuten voor bestandsoverdracht en weergave). Voor verkeer dat direct vóór een upload voorkomt, zou de gegevenslatentie kunnen zijn zo kort zoals 30 minuten (0 minuten tot de volgende partijupload voorkomt, dan 30 minuten voor dossieroverdracht en vertoning).

Indien nodig kan de klantenservice van Adobe het uploaden van gegevens in batches van 30 minuten (in plaats van per uur) inschakelen voor uw meest gebruikte rapportsuite.

## Medewerkers voor latentie

De latentie is een vertraging die langer is dan de typische 2 uren het voor servers van de gegevensinzameling duurt om gegevens volledig te verwerken. Zij heeft geen invloed op de gegevensverzameling; gegevens worden nog verzameld voor een werkende implementatie, ongeacht hoe laat een rapportreeks is. De ernst (hoe actueel de gegevens zijn) en de lengte (de tijd die nodig is om op te lossen) kunnen sterk variëren. Het is gewoonlijk beperkt tot één enkele rapportreeks.

Latentie wordt veroorzaakt door een van de volgende algemene categorieën:

* **Onverwachte verkeerspiek:** Dit type latentie treedt op wanneer meer gegevens naar een rapportsuite worden verzonden dan contractueel is vastgelegd of verwacht. Het is de meest voorkomende oorzaak van latentie.
* **Normale hardwareproblemen:** Adobe hanteert de beste strategieën voor datacenterbeheer en -bewaking, gegevensredundantie en betrouwbaarheid van hardware. Hardware wordt regelmatig en in combinatie met gepubliceerde onderhoudsvensters bijgewerkt. Voor noodonderhoud van defecte hardware kan een noodzakelijke en tijdelijke stopzetting van de gegevensverwerking (niet in gegevensverzameling) nodig zijn, omdat vervangende hardware online wordt gebracht. Deze tijdelijke stopzetting van de verwerking kan leiden tot opvallende latentie.
* **Abnormale gegevens:** Onnatuurlijke gegevenspatronen, zoals ongebruikelijk lange bezoeken die door bot of kruipler worden veroorzaakt, kunnen bepaalde verwerkingslasten tijdelijk verhogen die in latentie resulteren.

## Functies die afhankelijk zijn van latentie

Voor sommige mogelijkheden in de Adobe Experience Cloud geldt een extra latentie bovenop de standaard verwerkingstijd.

* Analytics for Target (A4T) vereist een extra wachttijd van 5 tot 10 minuten zodat verzamelde gegevens van beide platforms in dezelfde hit kunnen worden opgeslagen.
* Voor gegevens met tijdstempel is meer tijd nodig omdat deze gegevens op verschillende servers worden verwerkt. Het kan 15 minuten duren voordat treffers met een tijdstempel die zijn ontvangen op of bij real-time. De uren die met een timestamp van gisteren worden ontvangen kunnen tot 2 uren vergen. Oudere hits kunnen langer duren, elke dag tot een maximum van ongeveer 24 uur.

## Manieren om latentie te verlichten of te verhinderen

Er bestaan verschillende strategieën om latentie te voorkomen of de hersteltijd te verlagen wanneer deze zich voordoet:

* **Adobe op de hoogte stellen van verwachte verkeersspikes:** Hoewel het onmogelijk is om elke verkeerspiek aan uw plaats te voorzien, kunnen er gevallen zijn waarin u een significante toename van verkeer verwacht te ontvangen. Voorbeelden zijn een bijzonder succesvolle vakantieperiode, of kort na een grote campagne-push. In deze gevallen biedt Adobe uw organisatie een manier om ons op de hoogte te stellen van de verwachte toename van het verkeer, zodat we extra verwerkingsbronnen kunnen toewijzen aan uw rapportsuite. Zie Een verkeersspiegel [plannen](/help/admin/c-traffic-management/t-traffic-schedule-spike.md) in de gebruikershandleiding voor Admin voor meer informatie over toegenomen verkeer.
* **Overweeg de verwerkingsbelasting wanneer u nieuwe functies activeert:** Sommige functies zijn verwerkingsintensiever dan andere. Hoe meer functies een rapportsuite biedt, des te moeilijker is het om van latentie te herstellen. Wanneer het toelaten van eigenschappen op een rapportreeks, houd in mening de volgende eigenschappen die de hoeveelheid te verwerken gegevens verhogen:

   * Meer dan 20 gebeurtenissen op dezelfde pagina implementeren
   * Complexe VISTA-regels
   * Meer dan 20 waarden in de productvariabele
   * Serienummering voor gebeurtenissen

* Filter IAB Bot inschakelen: Het filtreren [van de](/help/admin/admin/bot-removal/bot-removal.md) bott kan zeer latentie verminderen als uw rapportreeks door bots of kruiplers wordt bezocht. Aanbevolen wordt de IAB-botlijst te gebruiken, aangezien deze wordt bijgewerkt en bijgehouden door het [Interactive Advertising Bureau](https://www.iab.net/about_the_iab). Een gebruiker kan zijn eigen beide regels aanpassen om die van IAB aan te vullen.

## Wat u moet doen met Latentie

In gevallen waarin latentie optreedt, kunt u er zeker van zijn dat Adobe de verwerkingsleiding proactief controleert en alles in het werk stelt om de verwerkingstijd zo snel mogelijk weer normaal te maken. Veel latentieproblemen zijn binnen enkele uren opgelost. Als u een specifieke rapportsuite gebruikt, kan een van de ondersteunde gebruikers van uw organisatie contact opnemen met de klantenservice met de rapportsuite-id die vertraging oploopt. De vertegenwoordiger van Adobe kan de vertraging valideren en u op de hoogte stellen wanneer het probleem verbetert en wordt opgelost.
