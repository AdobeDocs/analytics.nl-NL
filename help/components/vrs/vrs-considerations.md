---
description: Virtuele rapportsuites en tagging met meerdere suite hebben verschillende voordelen. Leer wat het beste is voor uw organisatie.
keywords: Virtual Report Suite,VRS
title: Virtuele rapportreeksen en tagging met meerdere suite-overwegingen
topic: Adobe Analytics
uuid: f17d3659-a5b1-4807-a01d-a1b422009a64
translation-type: tm+mt
source-git-commit: ''

---


# Virtuele rapportreeksen en tagging met meerdere suite-overwegingen

Met Virtual Report suites (VRS) kunt u gegevens weergeven uit een rapportsuite die gegevens verzamelt van uw digitale eigenschappen, maar waarbij een segment permanent wordt toegepast.

In veel gevallen kunt u de codering met meerdere suite&#39;s vervangen door virtuele rapportsuites. Het schakelen aan virtuele rapportsuites kan de noodzaak voor [secundaire servervraag](/help/admin/c-server-call-usage/overage-overview.md)effectief verwijderen. Uw organisatie heeft bijvoorbeeld zes verschillende websites, die elk gegevens naar hun eigen rapportsuite en een gecombineerde algemene rapportsuite verzenden. Elke plaats gaat een secundaire servervraag in; één voor de afzonderlijke merkrapportenreeks, en een tweede voor de globale rapportreeks. In plaats daarvan, kunt u gegevens van alle plaatsen alleen naar de globale rapportreeks verzenden, dan veelvoudige virtuele rapportreeksen gebruiken om elk merk te scheiden.

Als u de tagging met meerdere suite&#39;s vervangt door een algemene rapportsuite en VRS, kunt u de implementatie van Adobe Analytics vereenvoudigen en het verbruik van servergesprekken verminderen. Dit wordt als een aanbevolen werkwijze aanbevolen. Er zijn echter enkele belangrijke beperkingen van de vrijwillige VUT-regeling. De volgende richtlijnen kunnen u helpen beslissen of het uitvoeren van virtuele rapportreeksen die op een globale rapportreeks worden voortgebouwd de juiste benadering voor u is.

## Richtsnoeren

Als u niet zeker weet of de beschreven gebruiksgevallen op u en uw organisatie van toepassing zijn, neemt u contact op met andere Adobe Analytics-beheerders of met uw Adobe-accountmanager. Zij kunnen helpen uw bedrijfsbehoeften beoordelen en een aanbeveling doen.

Houd rekening met het volgende wanneer u bepaalt of u tags met meerdere suite of virtuele rapportsuites moet gebruiken:

### Segmenten publiceren naar de Adobe Experience Cloud

Het delen van segmenten naar Adobe Experience Cloud wordt niet ondersteund voor virtuele rapportsuites. Gebruikers die een segment willen delen met de Experience Cloud, moeten toegang hebben tot de bronrapportsuite.

Segmenten kunnen nog niet naar Adobe Experience Cloud worden gepubliceerd vanuit een virtuele rapportsuite voor personalisatie en doelversie. Alle gebruikers die segmenten publiceren hebben hiervoor toegang tot de bronrapportsuite nodig. U wilt bijvoorbeeld dat gebruikers alleen toegang hebben tot gegevens voor hun geografische regio&#39;s, maar dat ze segmenten van Adobe Analytics tot Adobe Experience Cloud kunnen maken en delen voor gebruik in Adobe Target. In dit geval raadt Adobe aan tags toe te wijzen met meerdere suite. Als u gebruikers die toegang tot de globale rapportreeks hebben of u niet segmenten voor gebruik in andere oplossingen moet publiceren, kunnen de virtuele rapportreeksen worden gebruikt.

### In real time en huidige gegevens

Realtime rapporten worden niet gesteund in virtuele rapportreeksen, omdat het gegeven wordt gesegmenteerd. De huidige gegevens worden ook niet gesteund in virtuele rapportreeksen, aangezien het geen segmentatie steunt. Beide functies zijn specifiek voor Rapporten en Analytics.

[Real-time rapporten](/help/admin/admin/realtime/t-realtime-admin.md) en [Huidige Gegevens](/help/technotes/latency.md) zijn niet beschikbaar in virtuele rapportreeksen. Dit is van invloed op gebruikers die reageren op trends die worden weergegeven in Rapporten en Analytics binnen seconden of enkele minuten na het verzamelen van gegevens. Dit kunnen bijvoorbeeld editors in een nieuwsruimte omvatten die kopregels aanpassen op basis van realtime-inhoudsverbruik. U kunt overwegen tags toe te voegen aan meerdere suite als u over belangrijke realtime gegevens beschikt die specifiek zijn voor de afzonderlijke rapportsuite. Real-time en huidige gegevens kunnen nog steeds worden gebruikt in de algemene rapportsuite.

### Unieke limieten

Als u een globale rapportreeks hebt die een groot aantal plaatsen samen combineert, is het mogelijk dat u vaak in het [laag-verkeer](/help/technotes/low-traffic.md) lijnpunt loopt. Als u multi-suite markering gebruikt, is dit slechts een kwestie voor de globale rapportsuite (individuele rapportsuites zullen minder vaak weinig verkeer zien). Als u virtuele rapportsuites gebruikt, worden de unieke grenzen gedeeld, veroorzakend individuele rapportsuites ook laag-verkeer tonen. U kunt overwegen tags toe te voegen aan meerdere suite als u wilt voorkomen dat gegevens in laag verkeer worden opgenomen.

Een grote mediaorganisatie heeft bijvoorbeeld 100 wegeigenschappen. Elke eigenschap publiceert maandelijks een paar duizend nieuwsartikelen, naast alle artikelen uit voorgaande maanden. Deze organisatie gebruikt een globaal rapportenpakket waar eVar1 &quot;Artikelnaam&quot;is. In dit rapport zijn er elke maand ongeveer 4 miljoen unieke artikelnamen van de verschillende eigenschappen samen. Als het gebruiken van een virtueel rapportreeks, de hoogste 500.000 waarden die uit het grootste deel van het verkeer bestaan zijn inbegrepen in virtuele rapportreeksen; de overige 3,5 miljoen zijn opgenomen in het lage verkeer. Als taggen met meerdere suite&#39;s wordt gebruikt, kan elke afzonderlijke rapportsuite zijn eigen hoogste waarden van 500 k zien. De unieke limieten van de algemene rapportsuite zijn hetzelfde tussen het gebruik van tags met meerdere suite en virtuele rapportensuites.

De klantendienst van Adobe kan unieke waardemaxima voor een klein aantal dimensies verhogen, die dit probleem volledig kunnen elimineren. Raadpleeg het accountteam en de klantenservice voor meer informatie.

### Gedeelde variabelen over rapportsuites

Virtuele rapportesuites hebben hun eigen reeksen afmetingen en metriek niet; zij erven deze van hun bronrapportenreeks. De algemene rapportsuite moet alle afmetingen en meetgegevens voor alle websites vastleggen. Rapportsuites hebben momenteel maximaal 250 eVars en 1000 aangepaste gebeurtenissen.

De verschillende plaats heeft verschillende implementatiebehoeften. Sommige dimensies en gebeurtenissen kunnen tussen twee sites worden gedeeld. Een e-mailregistratie kan bijvoorbeeld dezelfde gebeurtenis op meerdere websites gebruiken en dezelfde aangepaste gebeurtenis activeren. Andere afmetingen kunnen specifiek zijn voor een site. De gebruiker kan bijvoorbeeld slechts één van uw sites in staat stellen zijn profielafbeelding te wijzigen. Deze aangepaste gebeurtenis wordt alleen geïmplementeerd op de website die deze ondersteunt.

Zorg ervoor dat het aantal unieke dimensies en metriek in één enkele globale rapportreeks kan passen. Als u vindt dat er teveel unieke dimensies of metriek zijn, herzie elke dimensie binnen elke implementatie. Er zijn waarschijnlijk overlappingen en dimensies die niet essentieel zijn voor het succes van het bedrijf. Overweeg ook [classificaties](/help/components/c-classifications2/c-classifications.md) te gebruiken. In plaats van &#39;Productnaam&#39; op te nemen in eVar5, maakt u bijvoorbeeld een &#39;Productnaam&#39; op basis van de &#39;Productdimensie&#39;. De classificaties in een bronrapportreeks zijn automatisch beschikbaar aan om het even welke afhankelijke virtuele rapportreeksen.

> [!TIP] Met de introductie van [kromming](/help/analyze/analysis-workspace/curate-share/curate-projects-vrs.md), kunt u de naam van een bepaalde afmeting of metrisch op een per-VRS basis veranderen.

### Segmenteringsnuances

Een virtuele rapportsuite op een fundamenteel niveau is gewoon een segment dat wordt toegepast op een rapportsuite. Bezoek- en bezoekersgerichte afmetingen kunnen leiden tot intuïtieve rapportresultaten.

U hebt bijvoorbeeld twee websites, A en B, die beide gegevens verzenden naar een algemene rapportsuite. Sommige bezoekers oversteken onvermijdelijk van site A naar site B, en deze beweging van de ene naar de andere is zichtbaar in het plakken in de algemene rapportsuite. Als u virtuele rapportsuites voor plaatsen A en B bouwt, zou een bezoek dat op plaats A begon en op plaats B beëindigde geen ingangspagina in VRS B tonen. De ingangspagina voor dit bezoek begon op plaats A, die uit de virtuele rapportreeks wordt gesegmenteerd.

### Omrekening in valuta

Virtuele rapportsuites rapporteren niet over een andere valuta dan de rapportsuite waarop ze zijn gebaseerd. Met Adobe Analytics kunt u valuta converteren tijdens het uitvoeren van rapporten, maar de wisselkoers is gebaseerd op de huidige dag (zelfs voor historische gegevens).

Als uw organisatie haar analyse uitvoert in één munt, is dit geen probleem. Als u echter een grote zakelijke behoefte hebt aan verschillende regionale teams die hun inkomsten in hun eigen lokale valuta moeten bekijken, kunt u overwegen om tags met meerdere suite toe te passen.

### Gegevensfeeds

Gegevensfeeds kunnen geen virtuele rapportsuites gebruiken. U kunt echter een gegevensfeed ontvangen van een algemene rapportsuite en deze vervolgens scheiden.

Met gegevensfeeds kunt u dagelijks of per uur alle Adobe Analytics-gegevens exporteren op een afzonderlijk niveau. Gegevensfeeds kunnen niet vooraf worden gesegmenteerd voordat ze aan u worden geleverd, zodat u alleen een gegevensfeed voor uw algemene rapportsuite kunt ontvangen. Als uw organisatie een grote behoefte aan individuele gegevensvoer op een merk, bezit, gebied, of ander korrelig niveau heeft, denk na gebruikend multi-suite het etiketteren.

### Gegevensconnectors met partneraccounts

Bepaalde Adobe-partnerintegratie in Adobe Analytics is beperkt tot één partneraccount per rapportsuite. Sommige organisaties zouden veelvoudige partnerrekeningen voor de zelfde integratie kunnen vereisen.

Zo is per rapportsuite slechts één Google DCM toegestaan. Veel bedrijven hebben meerdere DCM-accounts, waardoor verschillende merken, bedrijfseenheden en regio&#39;s hun advertenties voor schermen afzonderlijk van elkaar kunnen beheren. Integraties kunnen niet worden ingesteld in virtuele-rapportsuites. Als u afhankelijke gegevensconnectors met meerdere accounts hebt, kunt u overwegen om tags toe te voegen aan meerdere suite.

### Samenvattingsgegevensbronnen

Met behulp van samenvattingsgegevensbronnen kunt u samengevoegde metriek op rapportniveau importeren in Adobe Analytics. Aangezien samenvattingsgegevensbronuploads geaggregeerde metriek bevatten, kunnen ze niet worden gesegmenteerd. Aangezien het VRS gebruikend segmentatie werkt, zijn alle gegevens die gebruikend summiere gegevensbronnen worden ingevoerd niet beschikbaar in virtuele rapportreeksen. De summiere gegevensbronnen zijn slechts zichtbaar in de bron rapportreeks.

> [!TIP] De volledige bronnen van verwerkingsgegevens steunen segmentatie, en kunnen in virtuele rapportreeksen worden gebruikt.

## Stappen volgen als u hebt besloten VRS te gebruiken

Als u ervoor kiest om secundaire servervraag ten gunste van virtuele rapportsuites te verwijderen:

1. Creeer virtuele rapportreeksen om de gegevens in uw reeksen van het kindrapport aan te passen. Segment op een aangepaste dimensie die uw sites van elkaar onderscheidt.
   * Als u van een bestaande multi-suite geëtiketteerde implementatie migreert, vergelijk de segmenten van de virtuele rapportreeks met uw bestaande reeksen van het kindrapport. U wilt ervoor zorgen dat de gegevens vergelijkbaar zijn voordat u gebruikers naar de virtuele rapportsuite verplaatst.
   * Als beste praktijken, denk na gebruikend [segment het stapelen](/help/components/c-segmentation/c-segmentation-workflow/seg-build.md) zodat kunt u een segment in één plaats uitgeven en het hebben op alle afhankelijke virtuele rapportreeksen van toepassing zijn.
   * Gebruik raakcontainers als u virtuele rapportsuites wederzijds wilt uitsluiten.
2. Nadat u hebt bevestigd dat de virtuele rapportreeksen correct opstelling zijn, verwijder de secundaire identiteitskaart van de rapportreeks uit uw implementatie. Secundaire rapportsuites verwijderen:
   * In de Lancering van het Platform van de Ervaring van Adobe, klik &quot;x&quot;naast om het even welke rapportsuites die u niet meer wilt gebruiken.
   * Zoek in DTM de eigenschap en het hulpprogramma Analytics. Verwijder de namen van de rapportsuite-id&#39;s die u niet meer wilt gebruiken in de velden Productieaccount-id en Staging Account ID.
   * Zoek in verouderde JavaScript-implementaties de `s.account` variabele op en verwijder de id&#39;s van de rapportsuite die u niet meer wilt gebruiken.
   * Laat in alle gevallen alleen de id van de algemene rapportensuite/bovenliggende rapportsuite staan voor het verzamelen van gegevens voor uw sites en apps.
   * Navigeer naar Beheer > Rapportagesuites en verberg secundaire rapportsuites die niet meer worden gebruikt.
