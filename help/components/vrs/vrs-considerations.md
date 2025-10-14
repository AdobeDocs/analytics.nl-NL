---
description: Virtuele rapportsuites en tagging met meerdere suite hebben verschillende voordelen. Leer wat het beste is voor uw organisatie.
keywords: Virtuele rapportsuite
title: Virtuele rapportreeksen en tagging met meerdere suite
feature: VRS
exl-id: 7e0a1f5b-26ac-438c-b481-33669039efe5
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '1634'
ht-degree: 0%

---

# Virtuele rapportreeksen en tagging met meerdere suite

De virtuele rapportsuites laten u gegevens van een rapportreeks bekijken die gegevens van uw digitale eigenschappen, maar met een segment permanent verzamelt.

In veel gevallen kunt u de codering met meerdere suite&#39;s vervangen door virtuele rapportsuites. Het schakelen naar virtuele rapportsuites kan de noodzaak voor [&#x200B; secundaire servervraag &#x200B;](/help/admin/tools/server-call-usage/overage-overview.md) effectief verwijderen. Uw organisatie heeft bijvoorbeeld zes verschillende websites, die elk gegevens naar hun eigen rapportsuite en een gecombineerde algemene rapportsuite verzenden. Elke plaats gaat een secundaire servervraag in; één aan de individuele reeks van het merkrapport, en een tweede aan de globale rapportreeks. In plaats daarvan, kunt u gegevens van alle plaatsen alleen naar de globale rapportreeks verzenden, dan veelvoudige virtuele rapportreeksen gebruiken om elk merk te scheiden.

Als u de tagging met meerdere suite&#39;s vervangt door een wereldwijde rapportensuite en een Virtual Report-suite, kunt u de Adobe Analytics-implementatie vereenvoudigen en het verbruik van servergesprekken verminderen. Dit wordt als een aanbevolen werkwijze aanbevolen. Er zijn echter enkele belangrijke beperkingen die in verband met Virtual Report kunnen worden overwogen. De volgende richtlijnen kunnen u helpen beslissen of het uitvoeren van virtuele rapportreeksen die op een globale rapportreeks worden voortgebouwd de juiste benadering voor u is.

## Richtsnoeren

Als u niet zeker weet of de beschreven gebruiksgevallen op u en uw organisatie van toepassing zijn, neemt u contact op met andere Adobe Analytics-beheerders of met uw Adobe-accountteam. Zij kunnen helpen uw bedrijfsbehoeften beoordelen en een aanbeveling doen.

Houd rekening met het volgende wanneer u bepaalt of u tags met meerdere suite of virtuele rapportsuites moet gebruiken:

### Segmenten publiceren naar de Adobe Experience Cloud

Het delen van segmenten naar Adobe Experience Cloud wordt niet ondersteund voor virtuele rapportsuites. Gebruikers die een segment willen delen met de Experience Cloud, moeten toegang hebben tot de bronrapportsuite.

Segmenten kunnen nog niet naar Adobe Experience Cloud worden gepubliceerd vanuit een virtuele rapportsuite voor personalisatie en doelgerichtheid. Alle gebruikers die segmenten publiceren hebben hiervoor toegang tot de bronrapportsuite nodig. U wilt bijvoorbeeld dat gebruikers alleen toegang hebben tot gegevens voor hun geografische regio&#39;s, maar dat ze segmenten van Adobe Analytics naar Adobe Experience Cloud kunnen maken en delen voor Adobe Target. In dit geval raadt Adobe aan tags toe te wijzen met meerdere suite. Als u gebruikers die toegang tot de globale rapportreeks hebben of u niet segmenten voor gebruik in andere oplossingen moet publiceren, kunnen de virtuele rapportreeksen worden gebruikt.

### Unieke (lage) grenzen

Als u een globale rapportreeks hebt die een groot aantal plaatsen samen combineert, is het mogelijk dat u vaak in het [&#x200B; laag-verkeers &#x200B;](/help/technotes/low-traffic.md) lijnpunt loopt. Als u multi-suite markering gebruikt, is dit slechts een kwestie voor de globale rapportsuite (individuele rapportsuites zullen minder vaak weinig verkeer zien). Als u virtuele rapportsuites gebruikt, worden de unieke grenzen gedeeld, veroorzakend individuele rapportsuites ook laag-verkeer tonen. U kunt overwegen tags toe te voegen aan meerdere suite als u wilt voorkomen dat gegevens in laag verkeer worden opgenomen.

Een grote mediaorganisatie heeft bijvoorbeeld 100 wegeigenschappen. Elke eigenschap publiceert maandelijks een paar duizend nieuwsartikelen, naast het hosten van alle artikelen uit voorgaande maanden. Deze organisatie gebruikt een wereldwijde rapportensuite waar eVar1 &#39;Article Name&#39; is. In dit rapport wordt verondersteld dat er elke maand ongeveer 5 miljoen unieke artikelnamen zijn van de verschillende eigenschappen samen. Als het gebruiken van een virtueel rapportreeks, slechts zal een deel van de 5 miljoen waarden in de virtuele rapportreeks worden omvat. De overige zijn opgenomen onder laag verkeer. Als taggen met meerdere suite wordt gebruikt, kan elke afzonderlijke rapportsuite een eigen set unieke waarden zien.

De klantenservice van Adobe kan soms voor een klein aantal dimensies de unieke waardelimieten verhogen, waardoor dit probleem volledig kan worden opgelost. Raadpleeg het accountteam en de klantenservice voor meer informatie.

### Gedeelde variabelen over rapportsuites

Virtuele rapportsuites hebben niet hun eigen reeksen van afmetingen en metriek; zij erven deze van hun bronrapportreeks. De algemene rapportsuite moet alle afmetingen en meetgegevens voor alle websites vastleggen. Rapportsuites hebben momenteel maximaal 250 eVars en 1000 aangepaste gebeurtenissen.

De verschillende plaats heeft verschillende implementatiebehoeften. Sommige dimensies en gebeurtenissen kunnen tussen twee sites worden gedeeld. Een e-mailregistratie kan bijvoorbeeld dezelfde gebeurtenis op meerdere websites gebruiken en dezelfde aangepaste gebeurtenis activeren. Andere afmetingen kunnen specifiek zijn voor een site. De gebruiker kan bijvoorbeeld slechts één van uw sites in staat stellen zijn profielafbeelding te wijzigen. Deze aangepaste gebeurtenis wordt alleen geïmplementeerd op de website die deze ondersteunt.

Zorg ervoor dat het aantal unieke dimensies en metriek in één enkele globale rapportreeks kan passen. Als u vindt dat er teveel unieke dimensies of metriek zijn, herzie elke dimensie binnen elke implementatie. Er zijn waarschijnlijk overlappingen en dimensies die niet essentieel zijn voor het succes van het bedrijf. Overweeg het gebruiken van [&#x200B; classificaties &#x200B;](/help/components/classifications/classifications-overview.md) eveneens. In plaats van &#39;Productnaam&#39; op te nemen in eVar5, maakt u bijvoorbeeld een &#39;Productnaam&#39; op basis van de &#39;Productdimensie&#39;. De classificaties in een bronrapportreeks zijn automatisch beschikbaar aan om het even welke afhankelijke virtuele rapportreeksen.

>[!TIP]
>
>Met de introductie van [&#x200B; besnoeiing &#x200B;](/help/analyze/analysis-workspace/curate-share/curate.md), kunt u de naam van een bepaalde afmeting of metrisch op een per Virtuele basis van de rapportreeks veranderen.

### Segmenteringsnuances

Een virtuele rapportsuite op een fundamenteel niveau is gewoon een segment dat wordt toegepast op een rapportsuite. Bezoek- en bezoekersgerichte afmetingen kunnen leiden tot intuïtieve rapportresultaten.

U hebt bijvoorbeeld twee websites, A en B, die beide gegevens verzenden naar een algemene rapportsuite. Sommige bezoekers oversteken onvermijdelijk van site A naar site B, en deze beweging van de ene naar de andere is zichtbaar in het plakken in de algemene rapportsuite. Als u virtuele rapportsuites voor plaatsen A en B bouwt, zou een bezoek dat op plaats A begon en op plaats B beëindigde geen ingangspagina in Virtuele rapportreeks B tonen. De ingangspagina voor dit bezoek begon op plaats A, die uit de virtuele rapportreeks wordt gesegmenteerd.

### Omrekening in valuta

Virtuele rapportsuites rapporteren niet over een andere valuta dan de rapportsuite waarop ze zijn gebaseerd. Adobe Analytics staat u toe om munt om te zetten wanneer het runnen van rapporten, maar de wisselkoers is gebaseerd op de huidige dag (zelfs voor historische gegevens).

Als uw organisatie haar analyse uitvoert in één munt, is dit geen probleem. Als u echter een grote zakelijke behoefte hebt aan verschillende regionale teams die hun inkomsten in hun eigen lokale valuta moeten bekijken, kunt u overwegen om tags met meerdere suite toe te passen.

### Gegevensfeeds

Gegevensfeeds kunnen geen virtuele rapportsuites gebruiken. U kunt echter een gegevensfeed ontvangen van een algemene rapportsuite en deze vervolgens scheiden.

Met gegevensfeeds kunt u elke dag of per uur alle Adobe Analytics-gegevens exporteren op een individueel niveau. Gegevensfeeds kunnen niet vooraf worden gesegmenteerd voordat ze aan u worden geleverd, zodat u alleen een gegevensfeed voor uw algemene rapportsuite kunt ontvangen. Als uw organisatie een grote behoefte aan individuele gegevensvoer op een merk, bezit, gebied, of ander korrelig niveau heeft, denk na gebruikend multi-suite het etiketteren.

### Gegevensconnectors met partneraccounts

Bepaalde Adobe-partnerintegratie in Adobe Analytics is beperkt tot één partneraccount per rapportsuite. Sommige organisaties zouden veelvoudige partnerrekeningen voor de zelfde integratie kunnen vereisen.

Per rapportsuite is bijvoorbeeld slechts één Google DCM toegestaan. Veel bedrijven hebben meerdere DCM-accounts, waardoor verschillende merken, bedrijfseenheden en regio&#39;s hun advertenties voor beeldschermen afzonderlijk van elkaar kunnen beheren. Integraties kunnen niet worden ingesteld in virtuele-rapportsuites. Als u afhankelijke gegevensconnectors met meerdere accounts hebt, kunt u overwegen om tags toe te voegen aan meerdere suite.

### Samenvattingsgegevensbronnen

Met samenvattingsgegevensbronnen kunt u samengevoegde metriek op rapportniveau importeren in Adobe Analytics. Omdat de summiere gegevensbron uploadt samengevoegde metriek *zonder bezoekersidentiteitskaart* bevat, kunnen zij niet in [!UICONTROL Visit] en [!UICONTROL Visitor] containers worden gesegmenteerd. Aangezien de Virtuele rapportreeks gebruikend segmentatie werkt, zullen de gegevens die met summiere gegevensbronnen worden ingevoerd niet beschikbaar in virtuele rapportreeksen zijn als het segment met een Bezoek of een container van de Bezoeker wordt gebouwd.

De summiere gegevensbronnen tonen omhoog in de virtuele rapportreeks als een container van het Actief wordt gebruikt en als die container van het Actief regels heeft die worden geconditioneerd om de gegevensbroninformatie te omvatten.

>[!TIP]
>
>De volledige bronnen van verwerkingsgegevens steunen segmentatie, en kunnen in virtuele rapportreeksen worden gebruikt.

## Stappen om te volgen als u hebt besloten Virtuele rapportsuite te gebruiken

Als u ervoor kiest om secundaire servervraag ten gunste van virtuele rapportreeksen te verwijderen:

1. Creeer virtuele rapportreeksen om de gegevens in uw reeksen van het kindrapport aan te passen. Segment op een aangepaste dimensie die uw sites van elkaar onderscheidt.
   * Als u van een bestaande multi-suite geëtiketteerde implementatie migreert, vergelijk de segmenten van de virtuele rapportreeks met uw bestaande reeksen van het kindrapport. U wilt ervoor zorgen dat de gegevens vergelijkbaar zijn voordat u gebruikers naar de virtuele rapportsuite verplaatst.
   * Als beste praktijken, overweeg gebruikend [&#x200B; segment het stapelen &#x200B;](/help/components/segmentation/segmentation-workflow/seg-build.md) zodat kunt u een segment in één plaats uitgeven en het hebben op alle afhankelijke virtuele rapportsuites van toepassing zijn.
   * Gebruik raakcontainers als u virtuele rapportsuites wederzijds wilt uitsluiten.
2. Nadat u hebt bevestigd dat de virtuele rapportreeksen correct opstelling zijn, verwijder de secundaire identiteitskaart van de rapportreeks uit uw implementatie. secundaire rapportsuites verwijderen:
   * In de uitbreiding van Adobe Analytics binnen de Inzameling van Gegevens van Adobe Experience Platform, klik &quot;x&quot;naast om het even welke rapportsuites die u niet meer wilt gebruiken.
   * Zoek in verouderde JavaScript-implementaties de variabele `s.account` en verwijder de id&#39;s van de rapportsuite die u niet meer wilt gebruiken.
   * Laat in alle gevallen alleen de id van de algemene rapportensuite/bovenliggende rapportsuite staan voor het verzamelen van gegevens voor uw sites en apps.
   * Navigeer naar Beheer > Rapportagesuites en verberg secundaire rapportsuites die niet meer worden gebruikt.
