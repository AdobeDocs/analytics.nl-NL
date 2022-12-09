---
title: Problemen met spikes en druppels in gegevens oplossen
description: Leer mogelijke redenen waarom u dramatische verhogingen of dalingen in trended rapporten kunt zien.
exl-id: 1a91f95e-818f-423d-9247-e0bb96bd0018
source-git-commit: dc9cd6bb45af0c992c37ffe20ea22eab67789ec5
workflow-type: tm+mt
source-wordcount: '855'
ht-degree: 0%

---

# Problemen met spikes en druppels in gegevens oplossen

Aangezien uw plaats gegevens verzamelt, zijn er vele externe factoren die gegevensinzameling of rapportering drastisch kunnen beïnvloeden. Hieronder volgt een lijst met mogelijke verklaringen waarom bepaalde variabelen of het totale verkeer drastisch stijgen of afnemen.

Terwijl u de oorzaak bepaalt en naar een resolutie toe gaat, kunt u de invloed van de gebeurtenis op de gegevens inschatten en bepalen hoe u wilt doorgaan. Zie de [overzichtspagina](overview.md) voor meer informatie .

## Verkeerdruppels

Verkeerslips worden in twee secties ingedeeld: deelgegevens en nulgegevens.

### Mogelijke oorzaken van volledig ontbrekende gegevens (rapporteringsnullen)

* **Latentie van rapportsuite**: Een rapportsuite kan soms worden gebruikt [latentie](../latency.md) vanwege een aantal factoren. Veel latentieproblemen zijn binnen enkele uren opgelost. Als u zich zorgen maakt over een specifieke rapportsuite, neemt u contact op met de klantenservice van Adobe met de desbetreffende rapportsuite-id.
* **Implementatie verwijderen**: Soms wordt het opnieuw implementeren van Analytics over het hoofd gezien wanneer een organisatie wijzigingen aanbrengt in de implementatie of de site opnieuw structureert. Werk met ontwikkelaars in uw organisatie om de code op uw site opnieuw te implementeren.
* **Probleem met analytische interface/caching**: In zeldzame gevallen bevat het cachegeheugen van een browser ongeldige gegevens waardoor alle rapporten nullen retourneren. Wis de cookies en cache van de browser om het probleem op te lossen. Als het wissen van uw cookies/cache niet werkt, neemt u contact op met de klantenservice voor het ontbrekende rapport en het datumbereik. zij kunnen de uitgave dupliceren en aanvullende informatie verstrekken .
* **Beschikbaarheid van analysemogelijkheden**: Controleren [status.adobe.com](https://status.adobe.com/products/1173/) voor problemen met gegevensverzameling of -verwerking.

### Mogelijke oorzaken van gedeeltelijk ontbrekende gegevens of verminderd verkeer

* **Wijzigingen in implementatie**: Gebruik de [foutopsporing](/help/implement/validate/debugger.md) om te controleren of de gewenste afmetingen werken.
* **Verlaagd verwijzend verkeer**: Als een populaire banneradvertentie of hyperlink op een andere site wordt verwijderd, kan dit leiden tot een dramatische afname van het verkeer. De [Verwijzen naar domeinen](/help/components/dimensions/referring-domain.md) de dimensie van voor en na de terugval tot verder onderzoek.
* **Problemen met de prestaties van de site**: Onjuiste verdeling van verkeer via taakverdelingsmechanisme of serverproblemen die uw site hosten, kan bijdragen tot een afname van de rapportage van Analytics. Werk met het team binnen uw organisatie dat de integriteit en gezondheid van uw site beheert om mogelijke prestatieproblemen te onderzoeken.
* **Wijzigingen in de natuurlijke zoekpositie**: Verkeer kan mogelijk afnemen als een andere site uw natuurlijke zoekpositie voor sommige van uw trefwoorden verlaat. Deze daling kan vooral duidelijk zijn als uw plaats niet meer op de eerste pagina van onderzoeksresultaten is. De [Zoekprogramma&#39;s](/help/components/dimensions/search-engine.md) de dimensie van het onderzoek .
* **Wijzigingen in PPC-reclame**: Het wijzigen van advertentielijsten en beschrijvingen voor bestaande campagnes kan van invloed zijn op uw kwaliteitsscore. Over het algemeen betekent een Score van hoge kwaliteit dat het trefwoord de plaats van de trefwoorden verbetert en dat de kosten per klik lager zijn. De [Trefwoorden zoeken - betaald](/help/components/dimensions/search-keyword.md) de dimensie van het onderzoek .

## Verkeerspikes

Verkeerspikes zijn gecategoriseerd in twee secties: bijna dubbele gegevens en andere oorzaken.

### Mogelijke oorzaken van het hebben van bijna of precies verdubbeling van de verwachte gegevens

* **Meerdere verzoeken om afbeeldingen binnen een implementatie**: Als uw implementatie meer dan één [`t()`](/help/implement/vars/functions/t-method.md) methodevraag per pagina, het verdubbelt effectief alle verzamelde gegevens. Gebruik het foutopsporingsprogramma op uw site en controleer of meerdere afbeeldingsverzoeken om duplicaten af te vangen.
* **Geüploade gegevensbronbestanden dupliceren**: Als uw organisatie [Gegevensbronnen](/help/import/c-data-sources/datasrc-home.md), kan een gebruiker in uw organisatie hetzelfde bestand twee keer uploaden naar Adobe Analytics. Als u deze dubbele upload uitvoert, worden die gegevens in de rapportage verdubbeld, wat tot een scherpe verkeersstroom leidt.

### Andere potentiële oorzaken van het toegenomen verkeer

* **Spinnen of bots**: Als je een grote plotse toename van het verkeer ziet, dan is het eerste wat je moet zoeken de mogelijkheid van een spin of beide. Het identificeren van bots kan soms lastig zijn, omdat elk een eigen manier heeft om code op uw site uit te voeren. Creeer een rapport van de Data Warehouse gebruikend IP als afmeting om te zien welke adressen het meeste verkeer veroorzaken. Vervolgens kunt u beide [Bot-regels](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-rules.md) of een VISTA-regel om beide verkeer uit toekomstige rapportage te verwijderen.
* **Opgezette campagnes**: Marketing-inspanningen, zoals e-mailcampagnes of optimalisatie van zoekprogramma&#39;s, kunnen mogelijk leiden tot een toename van het verkeer op uw site. De [Code bijhouden](/help/components/dimensions/tracking-code.md) de dimensie van het onderzoek . Het kan ook helpen om contact op te nemen met uw marketingteam om ervoor te zorgen dat de piek opzettelijk was.
* **Milieu- of indirecte oorzaken**: Als een vakantie of een indirecte gebeurtenis (een significante gebeurtenis waar uw plaats een bekende middel, of resterende marketing inspanningen van andere organisaties) voorkwam, kan het verkeer op uw plaats stijgen. Het oplossen van problemen de nauwkeurige oorzaak is moeilijk, aangezien er een bijna onbeperkt aantal indirecte redenen zijn waarom het verkeer kan stijgen. Deze oorzaken echter zijn een aantal van het belangrijkste om te bepalen zodat kan uw organisatie uit hen voordeel halen en bedrijfsbesluiten dienovereenkomstig nemen. De [Pagina](/help/components/dimensions/page.md) of [Referenter](/help/components/dimensions/referrer.md) de dimensie is de meest waarschijnlijke beste plaats om in het bepalen van de bron van het verkeer te beginnen.

Neem contact op met de klantenservice van Adobe als geen van de bovenstaande redenen mogelijk een toename of afname van het verkeer op uw site tot gevolg hebben. Ze kunnen hulp bieden bij het zoeken naar de bron van de verkeerspiek of -daling. Wanneer het creëren van het incident, instrueer de agent op hoe te om een specifiek rapport te ontspannen dat duidelijk de spiek of de daling illustreert.
