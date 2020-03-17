---
description: Hier worden de standaardmetriek in Adobe Analytics weergegeven.
title: Metrics quick reference
topic: Metrics
uuid: 34160c96-7cb3-4e2f-9956-9ffa9d9a359e
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Metrics quick reference

Hier worden de standaardmetriek in Adobe Analytics weergegeven.

>[!NOTE]
>
>Elke metrische waarde (gebeurtenis) die hieronder niet wordt vermeld, is een [aangepaste metrische](/help/components/c-variables/c-metrics/metrics-custom.md) waarde (aangepaste gebeurtenis).

>[!IMPORTANT]
>
>De Werkruimte van de analyse onderscheidt niet meer tussen de metriek van het Verkeer en van de Omzetting. Vandaar, is het metrische type slechts relevant voor hulpmiddelen zoals Rapporten &amp; Analytics, de Diensten 1.4 van het Web, en de Bouwer van het Rapport.)

| Metrische naam | Beschrijving | Type |
|--- |--- |---|
| Gemiddelde diepte pagina | Toont gemiddeld hoe ver binnen een bezoek elke waarde in brand werd gestoken. Deze metrische waarde is nuttig om te bepalen hoe ver binnen een bezoek uw publiek een bepaalde pagina of pro-waarde bereikt. De gemiddelde Diepte van de Pagina is beschikbaar op om het even welke variabele met toegelaten kleven. | Verkeer |
| Gemiddelde tijd die op pagina wordt doorgebracht | Vertegenwoordigt de gemiddelde tijd die aan een pagina binnen een bezoek wordt doorgebracht. | Verkeer |
| Gemiddelde tijd die op de site wordt besteed | Vertegenwoordigt de gemiddelde tijd die aan een plaats binnen een bezoek wordt doorgebracht. | Verkeer |
| Stuitpercentage | Toont het percentage bezoeken die één enkele hit bevatten. De stuitsnelheid gebruikt metrische stuiterend en wordt berekend als: Bounces gedeeld door Berichten. | Conversie |
| Bounces | Een bezoek dat uit één enkele servervraag bestaat. Een bezoek van één pagina is bijvoorbeeld een stuit als een bezoeker de pagina niet zodanig verandert dat gegevens naar Adobe worden verzonden, zoals het klikken op een koppeling of het starten van een video. Als tijdens een bezoek meer dan één keer wordt bereikt, wordt een Bounce niet geteld. | Conversie |
| Campagne Click-through | Doorklikken geeft het aantal keren aan dat een trackingcode voor een bepaalde campagne is doorgegeven aan de rapportage. Wanneer een bezoeker op een partnerkoppeling klikt die is gelabeld met een van deze trackingcodes, wordt de bezoeker naar de landingspagina geleid en wordt de trackingcode vastgelegd in s.campagne. Deze gegevens worden naar de rapportage verzonden en er wordt een doorklik opgenomen. | Conversie |
| Extra winkelwagentjes | Het aantal keren dat een object aan een winkelwagentje is toegevoegd. Deze waarde is afkomstig van de gebeurtenis scAdd. | Conversie |
| Winkelwagentje openen | Het aantal keren dat een klant een winkelwagentje heeft geopend door het eerste item toe te voegen. Vindt plaats wanneer een item voor het eerst aan het winkelwagentje wordt toegevoegd. Deze waarde is afkomstig uit de gebeurtenis scOpen. | Conversie |
| Winkelwagentjes | Het aantal keren dat een artikel uit een winkelwagentje is verwijderd. Deze waarde komt uit de scRemove gebeurtenis. | Conversie |
| Houtskaarten | Het aantal keren dat een nieuw winkelwagentje werd geopend of geïnitialiseerd. | Conversie |
| Kleuraweergaven | Het aantal keren dat de inhoud van het winkelwagentje door de klant wordt bekeken. | Conversie |
| Afbeeldingen | Een gebeurtenis die plaatsvindt wanneer klanten de afhandelingsfase van een aankoop bereiken. Het betalingsstadium vindt gewoonlijk plaats vlak voordat een aankoop is voltooid, en de klant voert meestal persoonlijke gegevens in (zoals de verzend- en factureringsgegevens). U hebt controle over de gebeurtenissen op uw site die als uitchecken worden gekwalificeerd. Deze waarde is afkomstig van de gebeurtenis scCheckout. | Conversie |
| Doorklikken | Doorklikken geeft het aantal keren aan dat een trackingcode voor een bepaalde campagne is doorgegeven aan de rapportage. Wanneer een bezoeker op een partnerkoppeling klikt die is gelabeld met een van deze trackingcodes, wordt de bezoeker naar de landingspagina geleid en wordt de trackingcode vastgelegd in s.campagne. Deze gegevens worden naar de rapportage verzonden en er wordt een doorklik opgenomen. | Conversie |
| Klant (New, Return, Loyal) | Categorieën van het rapport Customer Loyalty: Nieuwe klant: Klant met 0 aankopen.  Klanten terugsturen: Klant met 1 aankoop.  Klanten van logo: Klant met meer dan 1 aankoop. | Verkeer |
| Dagelijkse terugkeerbezoeken | Hiermee geeft u het aantal bezoekers van uw website meerdere keren op een bepaalde dag weer. Een dag wordt gedefinieerd als de laatste periode van 24 uur. | Verkeer |
| Berichten | Items vertegenwoordigen het aantal keren dat een bepaalde waarde wordt vastgelegd als de eerste waarde in een bezoek. Invoer kan slechts eenmaal per bezoek plaatsvinden. Het is echter niet noodzakelijkerwijs de eerste hit wanneer de variabele niet is gedefinieerd. | Verkeer |
| Afsluiten | Het aantal keren dat een bepaalde waarde wordt vastgelegd als de laatste waarde in een bezoek. Afsluiten kan slechts eenmaal per bezoek plaatsvinden. | Verkeer |
| Instanties | Het aantal keren dat een waarde voor een variabele is ingesteld. Instanties worden voor alle raaktypen geteld, maar worden niet geteld wanneer een waarde wordt opgenomen voor een variabele op een volgende hit vanwege persistentie. | Conversie |
| Mobiele weergaven | Het aantal keren dat een pagina wordt weergegeven of een dimensie wordt ingesteld wanneer deze wordt benaderd via een mobiel apparaat. Alleen ad-hocanalyse. In plaats van metrische mobiele weergaven te gebruiken, raden we u aan het segment &quot;Bezoeken van mobiele apparaten&quot; toe te passen. | Conversie |
| Nieuwe overeenkomsten | Nieuwe afspraken zijn een meldingsmethode voor marketingkanalen waarmee nieuwe bezoekers worden geteld die komen als gevolg van een kanaal. Deze maatstaf telt ook bezoekers die de afgelopen 30 dagen niet op uw site zijn geweest. Een nieuwe betrokkenheid is een eVar die aan het begin van elk bezoek (originele toewijzing) wordt geplaatst. First-touch kanalen kunnen ook nieuwe overeenkomsten zijn, afhankelijk van de instelling die de betrokkenheid van de bezoeker afloopt. | Conversie |
| Voorval | Het aantal keren dat een specifieke waarde wordt vastgelegd, plus het aantal paginaweergaven waarvoor de opgegeven waarde behouden bleef. Met andere woorden, de voorvallen zijn de som van paginaweergaven en paginagebeurtenissen. Voorvallen zijn alleen beschikbaar in ad-hocanalyse. | Niet beschikbaar in Rapporten &amp; Analytics, de Diensten 1.4 van het Web, of de Bouwer van het Rapport |
| Orders | Het aantal bestellingen dat tijdens de geselecteerde periode op uw website is geplaatst. U kunt individuele tijdsperioden door andere metriek onderverdelen om de punten (zoals producten of campagnes) te tonen die tot de meeste orden tijdens dat tijdkader hebben bijgedragen. | Conversie |
| Paginadiepte | Het gemiddelde aantal klikken dat gebruikers nodig hebben om naar een bepaalde pagina op de website te gaan. | Verkeer |
| Pagina-gebeurtenissen | Pagina-gebeurtenissen bestaan uit aanvraaggegevens voor afbeeldingen van niet-standaard afbeeldingsaanvragen. De bronnen van niet-standaardafbeeldingsverzoeken zijn downloadkoppelingen, exit-koppelingen en het bijhouden van aangepaste koppelingen. | Verkeer |
| Paginaweergaven | Een paginaweergave wordt geteld voor elke serveraanroep die wordt verzonden. Deze metrische waarde vertegenwoordigt het totaal aantal exemplaren van de paginaweergave. De vraag van TrackLink wordt niet geteld als paginameningen en verhoogt metrisch niet de meningen van de Pagina. | Conversie |
| Padweergaven | De metrische weergave van padweergaven is gebaseerd op padgegevens, die worden bijgehouden voor alle gebruikers die blijvende cookies accepteren.  De term Padweergave wordt gebruikt om aan te geven hoe vaak een pagina is weergegeven, gezien de beperkingen van de weergegeven paden. Deze metrische waarde rapporteert het aantal paginaweergaven voor de opgegeven pagina die zich binnen het geselecteerde pad heeft voorgedaan. Deze metrische waarde is beschikbaar op het rapport van Wegen. In padweergaven kunt u zien hoe vaak een bepaalde reeks pagina&#39;s is weergegeven. | Verkeer |
| Productweergaven | Instantie van de productweergave die wordt ingesteld. Vindt plaats wanneer de pagina met productdetails wordt weergegeven. Deze waarde is afkomstig van de gebeurtenis prodView. | Conversie |
| Opnieuw laden | Wordt geteld wanneer dezelfde paginanaam tweemaal in een rij wordt geladen. Dit geeft doorgaans aan dat de pagina is vernieuwd. Merk op dat het bezoeken van de zelfde pagina tweemaal in het zelfde bezoek niet als herlading telt tenzij beide bezoeken in-a-rij voorkwamen. | Verkeer |
| Retourbezoeken | Hier wordt het aantal bezoeken weergegeven waarbij het bezoeknummer groter is dan 1. Retourbezoeken omvatten niet-gekookte bezoekers. | Conversie |
| Ontvangsten | Opbrengsten worden opgenomen op de aankoopgebeurtenis en worden gedefinieerd als het totale dollarbedrag voor de som van de bestellingen voor elk product. Deze waarde is afkomstig van de aankoopgebeurtenis. | Conversie |
| Zoekopdrachten | Zoekopdrachten zijn geen standaardmetrische gegevens. Het is altijd een aangepaste metrische waarde.  Het is de geadviseerde standaardmetrisch voor onderzoeksmotoren en sleutelwoorden. Deze metrische waarde vertegenwoordigt instanties van een klik-door, en toont de pagina die met een specifieke motor of een sleutelwoord wordt geassocieerd. De metrische gegevens van onderzoeken kunnen retroactief aan het begin van de gegevensreeks worden gerapporteerd. | Conversie |
| Enkelvoudige toegang | De enige Toegang wordt bepaald door het aantal bezoeken aan uw plaats die één enkele unieke waarde van de Naam van de Pagina bevatte. Als een gebruiker naar uw site komt en op een bijgehouden koppeling klikt, een gebeurtenis (zoals een videoweergave) activeert of de pagina opnieuw laadt, wordt het bezoek nog steeds beschouwd als een Single Access-bezoek. Zolang de waarde voor de pageName variabele niet verandert, kan om het even welk aantal verzoeken worden verzonden en het bezoek nog beschouwd als Één enkele Toegang. | Verkeer |
| Tijd besteed | Metriek die aangeeft hoeveel tijd bezoekers besteden aan een pagina, site of per bezoek. | Verkeer |
| Totaal | De totale metriek rapporteren de waarde van alle posten van de rapportlijn voor een verslagperiode. Als een filter momenteel wordt geselecteerd, zou het totaal het gefilterde totaal in plaats van het totaal van de rapportreeks kunnen vertegenwoordigen. Als geen filter wordt geselecteerd vertegenwoordigt het totaal van de rapportreeks. | De totale versie van metrisch volgt het type van metrisch basis. Bijvoorbeeld, zou `totalpageviews` Verkeer zijn omdat `pageviews` Verkeer is. |
| Unieke klant | (Uur, Dagelijks, Wekelijks, Maandelijks, Driemaandelijks, Yearly) Een unieke klant wordt één keer meegeteld voor dat tijdsbestek, maar kan niet opnieuw worden geteld, ongeacht hoe vaak de bezoeker terugkeert om een aankoop te doen. Een unieke bezoeker wordt één keer meegeteld voor het eerste bezoek in een bepaalde periode en niet opnieuw geteld tot de periode verstrijkt. Na afloop van de periode wordt de unieke bezoeker opnieuw geteld. Unieke klanten worden altijd geteld als Unieke bezoekers omdat ze de site moeten bezoeken om de aankoop te kunnen doen. | Conversie |
| Unieke bezoekers | Geeft het totale aantal unieke bezoekers voor de rapportageperiode weer (kan worden geconfigureerd voor dagelijks, wekelijks, maandelijks, driemaandelijks, jaarlijks). | Conversie |
| Eenheden | De totale eenheden die voor de geselecteerde tijdsperiode zijn besteld. Omdat er veel eenheden per bestelling zijn aangeschaft, is Eenheden een essentiële maatstaf die algemene voorraadbewegingen onthult. | Conversie |
| Bezoekers | Het aantal unieke bezoekers van uw site voor een geselecteerd uur, dag, week, maand, kwartaal of jaar. | Conversie |
| Bezoeken | Een reeks paginaweergaven in een vergadering. Metrische bezoeken worden algemeen gebruikt in rapporten die het aantal gebruikerszittingen binnen de geselecteerde tijdspanne tonen.  De meting van het bezoek wordt altijd geassocieerd met een tijdsperiode, zodat u weet of om een nieuw bezoek te tellen als de zelfde bezoeker aan uw plaats terugkeert. | Conversie |

