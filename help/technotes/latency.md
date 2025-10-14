---
description: De volgende informatie kan helpen problemen met de latentie van de rapportsuite in analysegegevens oplossen.
keywords: ontbrekende gegevens;langzaam
title: Beschikbaarheid en latentie van gegevens
feature: Data Configuration and Collection
exl-id: fedef3ea-dde6-460f-90e3-1e661ed29b78
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '818'
ht-degree: 0%

---

# Beschikbaarheid van gegevens en latentie in Adobe Analytics

Doorgaans kunt u verwachten dat volledige gegevens in rapporten worden weergegeven twee uur nadat gegevens zijn verzameld. De volgende informatie kan helpen problemen met de latentie van de rapportsuite in analysegegevens oplossen.

## Gegevensbatchverwerking

Elke gegevensverzamelingsserver legt onbewerkte analysegegevens vast en verwerkt deze, en uploadt vervolgens gebatchgegevens op uurbasis voor rapportage. Het overdrachtsproces duurt gewoonlijk 30 minuten, zodat de normale vertraging voor verkeer dat direct optreedt nadat het vorige uploadproces is voltooid, ongeveer 90 minuten is (60 minuten totdat de volgende batch-upload plaatsvindt en 30 minuten voor bestandsoverdracht en weergave). Voor verkeer dat direct vóór een upload voorkomt, zou de gegevenslatentie kunnen zijn zo kort zoals 30 minuten (0 minuten tot de volgende partijupload voorkomt, dan 30 minuten voor dossieroverdracht en vertoning).

Indien nodig kan de Adobe Customer Care 30 minuten geüploade gegevens (in plaats van uur) uploaden voor uw meest gebruikte rapportensuites.

## Medewerkers voor latentie

De latentie is een vertraging die langer is dan de typische 2 uren het voor servers van de gegevensinzameling duurt om gegevens volledig te verwerken. Het beïnvloedt gegevensinzameling niet; de gegevens worden nog verzameld voor een werkende implementatie, ongeacht hoe latent een rapportreeks is. De ernst (hoe actueel de gegevens zijn) en de lengte (de tijd die nodig is om op te lossen) kunnen sterk variëren. Het is gewoonlijk beperkt tot één enkele rapportreeks.

Latentie wordt veroorzaakt door een van de volgende algemene categorieën:

* **Onverwachte verkeerspiek:** Dit type van latentie komt voor wanneer meer gegevens naar een rapportreeks worden verzonden dan contractueel werd begaan of verwacht. Het is de meest voorkomende oorzaak van latentie.
* **Normale hardwarekwesties:** Adobe past best-in-klassenstrategieën voor gegevenscentrumbeheer en controle, gegevensovertolligheid, en hardwarebetrouwbaarheid toe. Hardware wordt regelmatig en in combinatie met gepubliceerde onderhoudsvensters bijgewerkt. Voor noodonderhoud van defecte hardware kan een noodzakelijke en tijdelijke stopzetting van de gegevensverwerking (niet in gegevensverzameling) nodig zijn, omdat vervangende hardware online wordt gebracht. Deze tijdelijke stopzetting van de verwerking kan leiden tot opvallende latentie.
* **Abnormale gegevens:** De onnatuurlijke gegevenspatronen, zoals ongebruikelijk lange bezoeken die door een bot of een kruipper worden veroorzaakt, kunnen bepaalde verwerkingslasten tijdelijk verhogen die in latentie resulteren.

## Functies die afhankelijk zijn van latentie

Sommige mogelijkheden in de Adobe Experience Cloud worden geleverd met een aangeboren hoeveelheid latentie bovenop de standaard verwerkingstijd.

* Analytics for Target (A4T) vereist een extra wachttijd van 5 tot 10 minuten zodat verzamelde gegevens van beide platforms in dezelfde hit kunnen worden opgeslagen.
* Voor gegevens met tijdstempel is meer tijd nodig omdat deze gegevens op verschillende servers worden verwerkt. Het kan 15 minuten duren voordat treffers met een tijdstempel die zijn ontvangen op of bij real-time. De uren die met een timestamp van gisteren worden ontvangen kunnen tot 2 uren vergen. Oudere hits kunnen langer duren, elke dag tot een maximum van ongeveer 24 uur.

## Manieren om latentie te verlichten of te verhinderen

Er bestaan verschillende strategieën om latentie te voorkomen of de hersteltijd te verlagen wanneer deze zich voordoet:

* **breng Adobe op de hoogte van verwachte verkeerspikes:** Terwijl het onmogelijk is om elke verkeerspiek aan uw plaats te voorzien, kunnen er gevallen zijn waar u een significante toename van verkeer verwacht te ontvangen. Voorbeelden zijn een bijzonder succesvolle vakantieperiode, of kort na een grote campagne-push. In deze gevallen biedt Adobe uw organisatie een manier om ons op de hoogte te stellen van de verwachte toename van het verkeer, zodat we extra verwerkingsbronnen kunnen toewijzen aan uw rapportsuite. Zie [&#x200B; Plan een verkeerspiek &#x200B;](/help/admin/tools/manage-rs/edit-settings/c-traffic-management/t-traffic-schedule-spike.md) in de Admin gebruikersgids om te leren hoe te om Adobe van verhoogd verkeer op de hoogte te brengen.
* **overweegt verwerkings lading wanneer het activeren van nieuwe eigenschappen:** sommige eigenschappen zijn verwerkingsintensiever dan anderen. Hoe meer functies een rapportsuite biedt, des te moeilijker is het om van latentie te herstellen. Wanneer het toelaten van eigenschappen op een rapportreeks, houd in mening de volgende eigenschappen die de hoeveelheid te verwerken gegevens verhogen:

   * Meer dan 20 gebeurtenissen op dezelfde pagina implementeren
   * Complexe VISTA-regels
   * Meer dan 20 waarden in de productvariabele
   * Serienummering voor gebeurtenissen

* Laat IAB Bot het filtreren toe: [&#x200B; Bot het filtreren &#x200B;](/help/admin/tools/manage-rs/edit-settings/general/bot-removal/bot-removal.md) kan latentie zeer verminderen als uw rapportreeks door bots of kruiplers wordt bezocht. Het wordt geadviseerd om de IAB bot lijst te gebruiken, aangezien het door het [&#x200B; Interactieve Bureau van Advertising &#x200B;](https://www.iab.net/about_the_iab) wordt bijgewerkt en gehandhaafd. Een gebruiker kan zijn eigen beide regels aanpassen om die van IAB aan te vullen.

## Wat u moet doen met Latentie

In gevallen waarin latentie optreedt, moet u er zeker van zijn dat Adobe de verwerkingsleiding proactief controleert en alles in het werk stelt om de verwerkingstijd zo snel mogelijk weer normaal te maken. Veel latentieproblemen zijn binnen enkele uren opgelost. Als u een specifieke rapportsuite gebruikt, kan een van de ondersteunde gebruikers van uw organisatie contact opnemen met de klantenservice met de rapportsuite-id die vertraging oploopt. De Adobe-medewerker kan de latentie valideren en u op de hoogte stellen wanneer het probleem verbetert en wordt opgelost.
