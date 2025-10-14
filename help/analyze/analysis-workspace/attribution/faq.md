---
title: Veelgestelde vraag over de toewijzing
description: Antwoorden op veelgestelde vragen over attributie.
feature: Attribution
role: User, Admin
exl-id: 8e05957a-f954-4e61-aeed-cd2bd2fe11f8
source-git-commit: 35f2812c1a1a4eed090e04d67014fcebf88a80ec
workflow-type: tm+mt
source-wordcount: '1179'
ht-degree: 1%

---

# Veelgestelde vragen

Hier volgen antwoorden op veelgestelde vragen over attributie.

+++## Wat is het **[!UICONTROL None]** lijstitem wanneer het gebruiken van attributie?

Het regelitem Geen is een catch-all-item dat alle conversies vertegenwoordigt die zonder aanraakpunten in het terugzoekvenster zijn uitgevoerd. Om het aantal omzettingen te verminderen die aan het &quot;niets&quot;lijnpunt worden toegewezen, probeer gebruikend een Venster van de Terugblik van de Douane met een langere terugzoekperiode.

+++


+++## Waarom zie ik soms data buiten mijn rapporteringsvenster wanneer het gebruiken van attributiemodellen?

Sommige op bezoek-gebaseerde metriek, zoals [&#x200B; Ingangen &#x200B;](/help/components/metrics/entries.md) of [&#x200B; Stuitpercentage &#x200B;](/help/components/metrics/bounce-rate.md), kan gegevens aan een periode vóór de het melden van het venster datariereeks kenmerken. Deze situatie is toe te schrijven aan attributiemodellen die een terugkijkvenster gebruiken, dat bepaalt hoe ver achtereigenschap zou moeten kijken om krediet voor metriek te geven. Het gemeenschappelijkste scenario is wanneer de bezoeken middernacht overspannen. Bijvoorbeeld:

1. Een gebruiker bezoekt op 7 september om 23:55 uur uw homepage.
1. Zij bezoeken verschillende pagina&#39;s, waarvan de laatste om 12.05 uur op 8 september plaatsvond.
1. Een week later voert u een dagelijks trendrapport uit met het datumbereik van 8 september tot 14 september.

De op hoogte-gebaseerde metriek, als [&#x200B; meningen van de Pagina &#x200B;](/help/components/metrics/page-views.md), zou verwachte output produceren; gegevens die elke dag van 8 september - 14 september worden gekweekt. Uit de op een bezoek gebaseerde cijfers zou echter ook blijken dat dit bezoek op 7 september heeft plaatsgevonden. De toegeschreven ingang van het bezoek vond op 7 september plaats, en het terugkijkvenster is standaard 1 september - 31 september.

In dit voorbeeld wordt altijd 0% weergegeven bij een stuitpercentage van 7 september. Deze metrische waarde wordt gedefinieerd als `Bounces divided by Entries` , een op hit gebaseerde metrische waarde die wordt gedeeld door een op bezoek gebaseerde metrische waarde. Stuiterwaarden bestaan uit één verzoek om een afbeelding, zodat ze niet meerdere dagen kunnen beslaan. Eventuele stuitingen op 7 september vonden plaats buiten het rapportagevenster, waardoor de gegarandeerde stuitsnelheid van 0% voor die dag werd veroorzaakt. Andere op hit-based metriek zou ook 0 voor 7 September in dit rapport tonen, aangezien die klappen niet binnen het rapporteringsvenster zijn.

Kijk eens naar een ander vergelijkbaar voorbeeld. Het enige verschil tussen het volgende voorbeeld en het bovenstaande voorbeeld zijn de datums:

1. Een gebruiker bezoekt op 31 augustus om 23:55 uur uw homepage.
1. Zij bezoeken verschillende pagina&#39;s, waarvan de laatste om 12.05 uur plaatsvond.
1. Een week later voert u een dagelijks vervolg rapport uit met de datumbereik 1 september - 7 september.

In dit voorbeeld worden gegevens van 31 augustus niet weergegeven met de tarieven Bounce en Bounce. Het terugzoekvenster en het rapportagevenster beginnen beide op 1 september, zodat gegevens niet vanaf 31 augustus kunnen worden toegewezen.

+++


<!-- not relevant anymore due to introduction of separation of container and lookback window 
+++## When should I use a visit, visitor, or custom attribution lookback?

The choice of attribution lookback depends on your use case. If conversions typically take longer than a single visit, a visitor or custom lookback is recommended. For longer conversion cycles, custom lookback windows are best as they are the only type that can pull in data from prior to the reporting window.

+++
-->

+++## Hoe vergelijken props en eVars wanneer het gebruiken van attributie?

Attribution wordt opnieuw berekend tijdens de runtime van het rapport, zodat er geen verschil is tussen een prop of eVar (of een andere dimensie) voor attributiemodellering. Props kunnen blijven bestaan met een terugzoekvenster of toewijzingsmodel en eVar-instellingen voor toewijzing/vervaldatum worden genegeerd.

+++


+++## Zijn attributiemodellen beschikbaar in andere analysemogelijkheden, zoals de Eigenschap van Gegevens of Data Warehouse?

Nee. Attributiemodellen gebruiken verwerking van rapporttijd, die alleen beschikbaar is in Analysis Workspace. Zie [&#x200B; de tijdverwerking van het Rapport &#x200B;](/help/components/vrs/vrs-report-time-processing.md) voor meer informatie.

+++


+++## zijn attributiemodellen slechts beschikbaar als ik een virtuele rapportreeks met toegelaten verwerking van de rapporttijd gebruik?

Attributiemodellen zijn beschikbaar buiten virtuele rapportsuites. Terwijl zij de verwerking van de rapporttijd op de achtergrond gebruiken, zijn de attributiemodellen beschikbaar aan zowel standaardrapportreeksen als virtuele rapportreeksen.

+++


+++## Welke afmetingen en metriek worden niet ondersteund?

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
* Berichten
* Afsluiten
* Pagina&#39;s niet gevonden
* Zoekopdrachten
* Bezoeken van één pagina
* Enkelvoudige toegang

+++


+++# Werkt de attributie met classificaties?

Ja, classificaties worden volledig ondersteund.

+++


+++# Werkt de attributie met gegevensbronnen?

Ja, de meeste gegevensbronnen worden ondersteund. Attributie is niet mogelijk met gegevensbronnen op overzichtsniveau omdat deze gegevensbronnen niet aan een bezoeker-id van de Analyse binden.

Transactie-id-gegevensbronnen worden op dezelfde manier behandeld als elke andere hit. De gegevensbronnen van identiteitskaart van de transactie gebruiken niet de speciale verwerking die normaal in traditionele rapportering wordt gebruikt. Met andere woorden, wanneer bij het gebruik van de verwerking van de rapporttijd, worden eVar-waarden doorgegeven van resultaten die optreden bij het tijdstempel van de hit Transactie-id. De waarden worden niet verspreid uit resultaten die vlak bij het tijdstip van de oorspronkelijke transactie zijn opgetreden.

Waar mogelijk, baseert de attributie zich op de MID kolomwaarde die binnen een gebeurtenis in de gegevensbron, eerder dan een persisted waarde wordt verzonden. Het attributiemodel wordt toegepast op de kolomwaarden MID in de gegevensbron, ter plekke. Bijvoorbeeld, wanneer u [&#x200B; Laatste attributie van de Aanraak &#x200B;](models.md) gebruikt begint het model van elke instantie van metrisch. En loopt achterwaarts in de klappen tot het model de laatste die waarde bereikt in de kolom MID wordt waargenomen.

Wanneer niet mogelijk, gebruikt de attributie de MID waarde in het *vroegere verslag* in de gegevensbron voor evaluatie. Deze eerdere record wordt mogelijk niet opeenvolgend met een tijdstempel geordend, aangezien AA geen ondersteuning biedt voor gegevens buiten de bestelling.

Omdat de records niet opeenvolgend worden geordend, kunnen de verwachte waarden van het toepassen van persistentie van invloed zijn op de hoeveelheid tijd die tussen de opgegeven tijdstempel voor de transactie-id en de oorspronkelijke transactie bestaat.

+++


+++# Werkt de attributie met de integratie van Advertising Analytics?

Metagegevensafmetingen, zoals type en trefwoord, werken met kenmerk. Metrische gegevens (zoals afbeeldingen, kosten, klikken, gemiddelde positie en gemiddelde kwaliteitsscore) gebruiken echter gegevensbronnen op overzichtsniveau en zijn daarom niet compatibel.

+++


+++# hoe werkt de attributie met marketing kanalen?

Toen de marketingkanalen voor het eerst werden geïntroduceerd, hadden ze alleen de eerste en laatste aanraakafmetingen. Expliciete eerste/laatste aanraakafmetingen zijn niet meer nodig met de huidige versie van de toewijzing. Adobe biedt algemene [!UICONTROL Marketing Channel] - en [!UICONTROL Marketing Channel Detail] -afmetingen, zodat u deze kunt gebruiken met het gewenste attributiemodel. Deze algemene afmetingen gedragen zich hetzelfde als [!UICONTROL Last Touch Channel] -afmetingen, maar worden anders gelabeld om verwarring te voorkomen bij het gebruik van marketingkanalen met een ander attributiemodel.

Aangezien de afmetingen van de marketingkanalen afhankelijk zijn van een traditionele &quot;visit&quot;-definitie (zoals gedefinieerd door hun verwerkingsregels), kan de definitie van hun &quot;visit&quot; niet worden gewijzigd met behulp van virtuele-rapportsuites.

+++


+++## Hoe werkt de attributie met multi-waardevariabelen, zoals lijstvars?

Sommige afmetingen in Analytics kunnen veelvoudige waarden op één enkele slag bevatten. Veelvoorkomende voorbeelden zijn list vars en de productvariabele.

Wanneer de attributie wordt toegepast op multi-value klappen, krijgen alle waarden in de zelfde klappers de zelfde creditering. Aangezien vele waarden dit krediet kunnen ontvangen, kan het rapporttotaal verschillend zijn dan als u elk individueel lijnpunt samenstelde. Het rapporttotaal wordt gededupliceerd, terwijl elke afzonderlijke dimensie-item de juiste creditering krijgt.

+++


+++## Hoe werkt de attributie met segmentatie?

Attributie wordt altijd uitgevoerd vóór segmentatie en segmentatie wordt uitgevoerd voordat rapportfilters worden toegepast. Dit concept is ook op virtuele rapportsuites van toepassing gebruikend segmenten.

Als u bijvoorbeeld een virtuele rapportsuite maakt met een toegepast segment &quot;Weergaveits&quot;, kunt u andere kanalen in een tabel zien met behulp van bepaalde attributiemodellen.

![&#x200B; vertoning-slechts virtuele rapportreeks &#x200B;](assets/vrs-aiq-example.png)

>[!NOTE]
>
>Als een segment klappen onderdrukt die uw metrisch bevatten, worden die metrische instanties niet toegeschreven aan enige afmeting. Nochtans, verbergt een gelijkaardig rapportfilter eenvoudig sommige afmetingspunten, zonder enige invloed op metriek die per het attributiemodel wordt verwerkt. Hierdoor kan een segment lagere waarden retourneren dan een filter met een vergelijkbare definitie.

+++
