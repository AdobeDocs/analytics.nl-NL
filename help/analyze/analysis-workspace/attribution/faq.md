---
title: Veelgestelde vragen over attributie
description: Antwoorden op veelgestelde vragen over attributie.
feature: Attribution
role: Business Practitioner, Administrator
translation-type: tm+mt
source-git-commit: 894ee7a8f761f7aa2590e06708be82e7ecfa3f6d
workflow-type: tm+mt
source-wordcount: '1030'
ht-degree: 2%

---


# Veelgestelde vragen over attributie

## Wat is het regelitem &quot;Geen&quot; wanneer u een kenmerk gebruikt?

Het regelitem Geen is een catch-all-item dat alle conversies vertegenwoordigt die zonder aanraakpunten in het terugzoekvenster zijn uitgevoerd. Om het aantal omzettingen te verminderen die aan het &quot;niets&quot;lijnpunt worden toegewezen, probeer gebruikend een Venster van de Raadpleging van de Douane met een langere raadplegingsperiode.

## Waarom zie ik soms data buiten mijn rapporteringsvenster wanneer het gebruiken van attributiemodellen?

Sommige op bezoek-gebaseerde metriek, zoals [Ingangen](/help/components/metrics/entries.md) of [Bounce Rate](/help/components/metrics/bounce-rate.md), kunnen gegevens aan een periode vóór de het rapportvenster begindatumwaaier toeschrijven. Deze situatie is toe te schrijven aan attributiemodellen die een terugkijkvenster gebruiken, dat bepaalt hoe ver achtereigenschap zou moeten kijken om krediet voor metriek te geven. Het gemeenschappelijkste scenario is wanneer de bezoeken middernacht overspannen. Bijvoorbeeld:

1. Een gebruiker bezoekt op 7 september om 23:55 uur uw homepage.
1. Zij bezoeken verschillende pagina&#39;s, waarvan de laatste om 12.05 uur op 8 september plaatsvond.
1. Een week later voert u een dagelijks trendrapport uit met het datumbereik van 8 september tot 14 september.

Metriek op basis van een hit, zoals [Paginaweergaven](/help/components/metrics/page-views.md), zou leiden tot de verwachte uitvoer; gegevens die elke dag van 8 september tot en met 14 september zijn doorgestuurd. Uit de op een bezoek gebaseerde cijfers zou echter ook blijken dat dit bezoek op 7 september heeft plaatsgevonden. De toegeschreven ingang van het bezoek vond op 7 september plaats, en het terugkijkvenster is standaard 1 september - 31 september.

In dit voorbeeld wordt altijd 0% weergegeven bij een stuitpercentage van 7 september. Deze metrische waarde wordt gedefinieerd als `Bounces divided by Entries`, een op hit gebaseerde metrische waarde gedeeld door op bezoek gebaseerde metrische waarde. Stuiterwaarden bestaan uit één verzoek om een afbeelding, zodat ze niet meerdere dagen kunnen beslaan. Eventuele stuitingen op 7 september vonden plaats buiten het rapportagevenster, waardoor de gegarandeerde stuitsnelheid van 0% voor die dag werd veroorzaakt. Andere op hit-based metriek zou ook 0 voor 7 September in dit rapport tonen, aangezien die klappen niet binnen het rapporteringsvenster zijn.

Kijk eens naar een ander vergelijkbaar voorbeeld. Het enige verschil tussen het volgende voorbeeld en het bovenstaande voorbeeld zijn de datums:

1. Een gebruiker bezoekt op 31 augustus om 23:55 uur uw homepage.
1. Zij bezoeken verschillende pagina&#39;s, waarvan de laatste om 12.05 uur plaatsvond.
1. Een week later voert u een dagelijks vervolg rapport uit met de datumbereik 1 september - 7 september.

In dit voorbeeld worden gegevens van 31 augustus niet weergegeven met de tarieven Bounce en Bounce. Het terugzoekvenster en het rapportagevenster beginnen beide op 1 september, zodat gegevens niet vanaf 31 augustus kunnen worden toegewezen.

## Wanneer moet ik een bezoek, bezoeker of aangepaste terugzoekactie voor kenmerken gebruiken?

De keuze van de terugzoekfunctie voor attributie hangt af van het gebruikte geval. Als conversies doorgaans langer duren dan één bezoek, wordt een bezoeker of aangepaste terugzoekactie aanbevolen. Voor langere conversiecycli zijn aangepaste terugzoekvensters het beste omdat dit het enige type is dat gegevens kan ophalen van vóór het rapportagevenster

## Hoe vergelijken props en eVars wanneer het gebruiken van attributie?

Attribution wordt opnieuw berekend tijdens de runtime van het rapport, zodat er geen verschil is tussen een prop of eVar (of een andere dimensie) voor attributiemodellering. Props kunnen blijven bestaan met een terugzoekvenster of een toewijzingsmodel en instellingen voor eVar-toewijzing/vervaldatum worden genegeerd.

## Zijn toewijzingsmodellen beschikbaar in andere analysemogelijkheden, zoals gegevensfeeds of Data Warehouse?

Nee. Attributiemodellen gebruiken verwerking van rapporttijd, die alleen beschikbaar is in Analysis Workspace. Zie [Tijdverwerking rapporteren](/help/components/vrs/vrs-report-time-processing.md) voor meer informatie.

## Zijn toewijzingsmodellen alleen beschikbaar als ik een virtuele rapportsuite gebruik waarvoor verwerking van rapporttijd is ingeschakeld?

Attributiemodellen zijn beschikbaar buiten virtuele rapportsuites. Terwijl zij de verwerking van de rapporttijd op de achtergrond gebruiken, zijn de attributiemodellen beschikbaar aan zowel standaardrapportreeksen als virtuele rapportreeksen.

## Welke afmetingen en metriek worden niet gesteund?

Het deelvenster Kenmerken ondersteunt alle afmetingen. Niet-ondersteunde meetgegevens zijn:

* Alle berekende metriek
* Unieke bezoekers
* Bezoeken
* Voorvallen
* Paginaweergaven
* A4T-meetwaarden
* Metrische tijdwaarden
* Bounces
* Stuitpercentage
* Geopend
* Gesloten
* Pagina&#39;s niet gevonden
* Zoekopdrachten
* Bezoeken van één pagina
* Eenmalige toegang

## Werkt de toewijzing met classificaties?

Ja, classificaties worden volledig ondersteund.

## Werkt de toewijzing met gegevensbronnen?

Ja, de meeste gegevensbronnen worden ondersteund. Attributie is niet mogelijk bij gegevensbronnen op overzichtsniveau omdat deze niet aan een bezoekersidentificatie van Analytics zijn gekoppeld. De gegevensbronnen van identiteitskaart van de transactie worden ook gesteund, tenzij zij in een virtuele rapportreeks met toegelaten verwerking van de rapporttijd worden gebruikt.

## Werkt attributie met de integratie van Advertising Analytics?

Metagegevensafmetingen, zoals type en trefwoord, werken met kenmerk. Metrische gegevens (zoals afbeeldingen, kosten, klikken, gemiddelde positie en gemiddelde kwaliteitsscore) gebruiken echter gegevensbronnen op overzichtsniveau en zijn daarom niet compatibel.

## Hoe werkt attributie met marketingkanalen?

Toen de marketingkanalen voor het eerst werden geïntroduceerd, hadden ze alleen de eerste en laatste aanraakafmetingen. Expliciete eerste/laatste aanraakafmetingen zijn niet meer nodig met de huidige versie van de toewijzing. Adobe biedt algemene &#39;Marketing Channel&#39;- en &#39;Marketing Channel Detail&#39;-afmetingen, zodat u deze kunt gebruiken met het gewenste attributiemodel. Deze generieke afmetingen gedragen zich hetzelfde als de laatste aanraakkanaalafmetingen, maar worden anders geëtiketteerd om verwarring te voorkomen bij het gebruik van marketingkanalen met een ander toewijzingsmodel.

Aangezien de afmetingen van de marketingkanalen afhankelijk zijn van een traditionele &quot;visit&quot;-definitie (zoals gedefinieerd door hun verwerkingsregels), kan de definitie van hun &quot;visit&quot; niet worden gewijzigd met behulp van virtuele-rapportsuites.

## Hoe werkt attributie met variabelen met meerdere waarden, zoals list vars?

Sommige afmetingen in Analytics kunnen veelvoudige waarden op één enkele slag bevatten. Veelvoorkomende voorbeelden zijn list vars en de productvariabele.

Wanneer de attributie wordt toegepast op multi-value klappen, krijgen alle waarden in de zelfde klappers de zelfde creditering. Aangezien vele waarden dit krediet kunnen ontvangen, kan het rapporttotaal verschillend zijn dan als u elk individueel lijnpunt samenstelde. Het rapporttotaal wordt gededupliceerd, terwijl elke afzonderlijke dimensie-item de juiste creditering krijgt.

## Hoe werkt attributie met segmentatie?

Attributie wordt altijd uitgevoerd vóór segmentatie en segmentatie wordt uitgevoerd voordat rapportfilters worden toegepast. Dit concept is ook op virtuele rapportsuites van toepassing gebruikend segmenten.

Als u bijvoorbeeld een VRS maakt met een toegepast segment &quot;Weergaveits&quot;, kunt u andere kanalen in een tabel zien met behulp van bepaalde attributiemodellen.

![Virtuele rapportsuite met alleen weergave](assets/vrs-aiq-example.png)

>[!NOTE]
>
>Als een segment klappen onderdrukt die uw metrisch bevatten, zullen die metrische instanties niet aan om het even welke afmeting worden toegeschreven. Nochtans, zal een gelijkaardig rapportfilter eenvoudig sommige afmetingspunten verbergen, zonder enige invloed op metriek die per het attributiemodel wordt verwerkt. Hierdoor kan een segment lagere waarden retourneren dan een filter met een vergelijkbare definitie.
