---
title: Veelgestelde vragen over attributie
description: Antwoorden op veelgestelde vragen over attributie.
feature: Attribution
role: User, Admin
exl-id: 8e05957a-f954-4e61-aeed-cd2bd2fe11f8
source-git-commit: 1c9f2a0f811d42c55205ee9e0431cee2f67187e7
workflow-type: tm+mt
source-wordcount: '1018'
ht-degree: 2%

---

# Veelgestelde vragen over attributie

## Wat is het regelitem &quot;Geen&quot; wanneer u een kenmerk gebruikt?

Het regelitem Geen is een catch-all-item dat alle conversies vertegenwoordigt die zonder aanraakpunten in het terugzoekvenster zijn uitgevoerd. Om het aantal omzettingen te verminderen die aan het &quot;niets&quot;lijnpunt worden toegewezen, probeer gebruikend een Venster van de Lookback van de Douane met een langere raadplegingsperiode.

## Waarom zie ik soms data buiten mijn rapporteringsvenster wanneer het gebruiken van attributiemodellen?

Sommige op bezoek-gebaseerde metriek, zoals [Berichten](/help/components/metrics/entries.md) of [Stuitsnelheid](/help/components/metrics/bounce-rate.md), kan gegevens aan een periode vóór de rapportperiode van het vensterbegin bepalen. Deze situatie is toe te schrijven aan attributiemodellen die een terugkijkvenster gebruiken, dat bepaalt hoe ver achtereigenschap zou moeten kijken om krediet voor metriek te geven. Het gemeenschappelijkste scenario is wanneer de bezoeken middernacht overspannen. Bijvoorbeeld:

1. Een gebruiker bezoekt op 7 september om 23:55 uur uw homepage.
1. Zij bezoeken verschillende pagina&#39;s, waarvan de laatste om 12.05 uur op 8 september plaatsvond.
1. Een week later voert u een dagelijks trendrapport uit met het datumbereik van 8 september tot 14 september.

Op een hoogte gebaseerde meetgegevens, zoals [Paginaweergaven](/help/components/metrics/page-views.md), de verwachte output zou produceren; gegevens die elke dag van 8 september tot en met 14 september zijn doorgestuurd. Uit de op een bezoek gebaseerde cijfers zou echter ook blijken dat dit bezoek op 7 september heeft plaatsgevonden. De toegeschreven ingang van het bezoek vond op 7 september plaats, en het terugkijkvenster is standaard 1 september - 31 september.

In dit voorbeeld wordt altijd 0% weergegeven bij een stuitpercentage van 7 september. Deze metrische waarde wordt gedefinieerd als `Bounces divided by Entries`, een op hit-Gebaseerde metrisch gedeeld door op bezoek-Gebaseerde metrisch. Stuiterwaarden bestaan uit één verzoek om een afbeelding, zodat ze niet meerdere dagen kunnen beslaan. Eventuele stuitingen op 7 september vonden plaats buiten het rapportagevenster, waardoor de gegarandeerde stuitsnelheid van 0% voor die dag werd veroorzaakt. Andere op hit-based metriek zou ook 0 voor 7 September in dit rapport tonen, aangezien die klappen niet binnen het rapporteringsvenster zijn.

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

Nee. Attributiemodellen gebruiken verwerking van rapporttijd, die alleen beschikbaar is in Analysis Workspace. Zie [Tijdverwerking rapporteren](/help/components/vrs/vrs-report-time-processing.md) voor meer informatie .

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

Ja, de meeste gegevensbronnen worden ondersteund. Attributie is niet mogelijk bij gegevensbronnen op overzichtsniveau omdat deze niet aan een bezoekersidentificatie van Analytics zijn gekoppeld.

Gegevensbronnen van de transactie-id worden op dezelfde wijze behandeld als andere treffers; ze gebruiken niet de speciale verwerking die ze normaal gebruiken in traditionele rapportage.

## Werkt attributie met de integratie van Advertising Analytics?

Metagegevensafmetingen, zoals type en trefwoord, werken met kenmerk. Metrische gegevens (zoals afbeeldingen, kosten, klikken, gemiddelde positie en gemiddelde kwaliteitsscore) gebruiken echter gegevensbronnen op overzichtsniveau en zijn daarom niet compatibel.

## Hoe werkt attributie met marketingkanalen?

Toen de marketingkanalen voor het eerst werden geïntroduceerd, hadden ze alleen de eerste en laatste aanraakafmetingen. Expliciete eerste/laatste aanraakafmetingen zijn niet meer nodig met de huidige versie van de toewijzing. Adobe verstrekt algemeen [!UICONTROL Marketing Channel] en [!UICONTROL Marketing Channel Detail] afmetingen zodat u deze kunt gebruiken met het gewenste attributiemodel. Deze algemene afmetingen gedragen zich als [!UICONTROL Last Touch Channel] de afmetingen, maar worden anders geëtiketteerd om verwarring te voorkomen wanneer het gebruiken van marketing kanalen met een verschillend attributiemodel.

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
>Als een segment klappen onderdrukt die uw metrisch bevatten, worden die metrische instanties niet toegeschreven aan om het even welke afmeting. Nochtans, verbergt een gelijkaardig rapportfilter eenvoudig sommige afmetingspunten, zonder enige invloed op metriek die per het attributiemodel wordt verwerkt. Hierdoor kan een segment lagere waarden retourneren dan een filter met een vergelijkbare definitie.
