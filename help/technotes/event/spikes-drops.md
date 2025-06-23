---
title: Problemen met spikes en druppels in gegevens oplossen
description: Leer mogelijke redenen waarom u dramatische verhogingen of dalingen in trended rapporten kunt zien.
exl-id: 1a91f95e-818f-423d-9247-e0bb96bd0018
feature: Curate and Share, Data Configuration and Collection
source-git-commit: 29ab0cc535bd8f74b50428c11756bf8b446a23ab
workflow-type: tm+mt
source-wordcount: '853'
ht-degree: 0%

---

# Problemen met spikes en druppels in gegevens oplossen

Aangezien uw plaats gegevens verzamelt, zijn er vele externe factoren die gegevensinzameling of rapportering drastisch kunnen beïnvloeden. Hieronder volgt een lijst met mogelijke verklaringen waarom bepaalde variabelen of het totale verkeer drastisch stijgen of afnemen.

Terwijl u de oorzaak bepaalt en naar een resolutie toe gaat, kunt u de invloed van de gebeurtenis op de gegevens inschatten en bepalen hoe u wilt doorgaan. Zie de [ overzichtspagina ](overview.md) voor meer informatie.

## Verkeerstekkers

De dalingen van het verkeer zijn gecategoriseerd in twee secties: gedeeltelijke gegevens en nul gegevens.

### Mogelijke oorzaken van volledig ontbrekende gegevens (rapporteringsnullen)

* **Latentie van de Reeks van het Rapport**: Af en toe, kan een rapportreeks [ latentie ](../latency.md) toe te schrijven aan een aantal factoren ervaren. Veel latentieproblemen zijn binnen enkele uren opgelost. Als u een specifieke rapportsuite gebruikt, neemt u contact op met de klantenservice van Adobe met de desbetreffende rapportsuite-id.
* **verwijdering van de Implementatie**: Soms wanneer een organisatie implementatieveranderingen aanbrengt of hun plaats herstructureert, wordt het opnieuw uitvoeren van Analytics over het hoofd gezien. Werk met ontwikkelaars in uw organisatie om de code op uw site opnieuw te implementeren.
* **de interface van Analytics/caching kwestie**: In zeldzame gevallen, bevat het geheime voorgeheugen van browser ongeldige gegevens die alle rapporten maken nul terugkeren. Wis de cookies en cache van de browser om het probleem op te lossen. Als het wissen van uw cookies/cache niet werkt, neemt u contact op met de klantenservice met het ontbrekende rapport en het datumbereik. Ze kunnen de uitgave dupliceren en aanvullende informatie verstrekken.
* **beschikbaarheid van Analytics**: Controle [ status.adobe.com ](https://status.adobe.com/products/1173/) voor om het even welke kwesties met gegevensinzameling of verwerking.

### Mogelijke oorzaken van gedeeltelijk ontbrekende gegevens of verminderd verkeer

* **de veranderingen van de Implementatie**: Gebruik [ debugger ](/help/implement/validate/debugger.md) om te bevestigen dat de gewenste dimensies werken.
* **Verlaagd verwijzend verkeer**: Als een populaire banneradvertentie of hyperlink op een andere plaats wordt verwijderd, kan het een dramatische daling in verkeer veroorzaken. Trend de [ Verwijzende domeinen ](/help/components/dimensions/referring-domain.md) dimensie van vóór en na het daling aan onderzoek verder.
* **de prestatieskwesties van de Plaats**: De onjuiste distributie van verkeer door ladingsstabilisatoren of serverkwesties die uw plaats ontvangen kan tot een daling in Analytics bijdragen rapportering. Werk met het team binnen uw organisatie dat de integriteit en gezondheid van uw site beheert om mogelijke prestatieproblemen te onderzoeken.
* **Veranderingen in natuurlijke onderzoek rangschikt**: Het verkeer kan potentieel verminderen als een andere plaats uw natuurlijke onderzoek rangschikt voor sommige van uw sleutelwoorden verlaat. Deze daling kan vooral duidelijk zijn als uw plaats niet meer op de eerste pagina van onderzoeksresultaten is. Touw de [ motoren van het Onderzoek ](/help/components/dimensions/search-engine.md) dimensie aan onderzoek verder.
* **Veranderingen in reclame PPC**: Het veranderen van advertentietitels en beschrijvingen voor bestaande campagnes kan uw Score van de Kwaliteit beïnvloeden. Over het algemeen betekent een Score van hoge kwaliteit dat het trefwoord de plaats van de trefwoorden verbetert en dat de kosten per klik lager zijn. Touw de [ sleutelwoorden van het Onderzoek - betaalde ](/help/components/dimensions/search-keyword.md) dimensie aan onderzoek verder.

## Verkeerspikes

Verkeerspikes zijn gecategoriseerd in twee secties: bijna dubbele gegevens en andere oorzaken.

### Mogelijke oorzaken van het hebben van bijna of precies verdubbeling van de verwachte gegevens

* **Veelvoudige beeldverzoeken binnen een implementatie**: Als uw implementatie meer dan één [`t()`](/help/implement/vars/functions/t-method.md) methodevraag per pagina bevat, verdubbelt het effectief alle verzamelde gegevens. Gebruik het foutopsporingsprogramma op uw site en controleer of meerdere afbeeldingsverzoeken om duplicaten af te vangen.
* **dubbele geüploade gegevensbrondossiers**: Als uw organisatie [ Gegevensbronnen ](/help/import/data-sources/overview.md) gebruikt, kan een gebruiker in uw organisatie het zelfde dossier tweemaal aan Adobe Analytics uploaden. Als u deze dubbele upload uitvoert, worden die gegevens in de rapportage verdubbeld, wat tot een scherpe verkeersstroom leidt.

### Andere potentiële oorzaken van het toegenomen verkeer

* **Spinnen of bots**: Als u een grote plotselinge toename van verkeer ziet, is het eerste ding om te zoeken de mogelijkheid van een spin of beide. Het identificeren van bots kan soms lastig zijn, omdat elk een eigen manier heeft om code op uw site uit te voeren. Creeer een rapport van Data Warehouse gebruikend IP als afmeting om te zien welke adressen het meeste verkeer veroorzaken. U kunt of [ Bot Regels ](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-rules.md) of een regel dan gebruiken VISTA om beide verkeer van toekomstige rapportering te elimineren.
* **Gelanceerde campagnes**: De inspanningen van de marketing zoals e-mailcampagnes of de optimalisering van de onderzoeksmotor kunnen potentieel een verkeerspiek op uw plaats veroorzaken. Touw de [ het Volgen code ](/help/components/dimensions/tracking-code.md) dimensie aan onderzoek verder. Het kan ook helpen om contact op te nemen met uw marketingteam om ervoor te zorgen dat de piek opzettelijk was.
* **Milieu of indirecte oorzaken**: Als een vakantie of een indirecte gebeurtenis (een significante gebeurtenis voorkwam waar uw plaats een bekende middel, of resterende marketing inspanningen van andere organisaties) is, kan het verkeer op uw plaats stijgen. Het oplossen van problemen de nauwkeurige oorzaak is moeilijk, aangezien er een bijna onbeperkt aantal indirecte redenen zijn waarom het verkeer kan stijgen. Deze oorzaken echter zijn een aantal van het belangrijkste om te bepalen zodat kan uw organisatie uit hen voordeel halen en bedrijfsbesluiten dienovereenkomstig nemen. Het trenderen van de [ pagina ](/help/components/dimensions/page.md) of [ 3&rbrace; dimensie van de Verwijzer &lbrace;is zeer waarschijnlijk de beste plaats in het bepalen van de bron van het verkeer te beginnen.](/help/components/dimensions/referrer.md)

Neem contact op met de klantenservice van Adobe als geen van de bovenstaande redenen mogelijk een toename of afname van het verkeer op uw site tot gevolg heeft. Ze kunnen hulp bieden bij het zoeken naar de bron van de verkeerspiek of -daling. Wanneer het creëren van het incident, instrueer de agent op hoe te om een specifiek rapport te ontspannen dat duidelijk de spiek of de daling illustreert.
