---
description: Rollup-rapport bestaat uit geaggregeerde gegevens van meerdere groepen met kinderrapporten en geeft deze weer in een samengevatte gegevensset.
title: Rollup- en algemene rapportensuites
topic: Admin tools
uuid: c90b8e38-2c95-4318-8165-a362106b6142
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Rollup- en algemene rapportensuites

Rollup-rapport bestaat uit geaggregeerde gegevens van meerdere groepen met kinderrapporten en geeft deze weer in een samengevatte gegevensset. Deze sjablonen bieden een handige plaats voor het weergeven van samengevoegde totalen, zoals paginaweergaven, inkomsten of andere basisafmetingen. Rollups worden vaak gebruikt omdat hiervoor geen aanvullende implementatie vereist is.

## Definities van rapportsuite-typen

**Globale rapportsuite**: Implementatie is gewijzigd om afbeeldingsaanvragen in verschillende domeinen naar één algemene rapportsuite te verzenden. Als treffers ook naar individuele rapportreeksen worden verzonden, is deze praktijk genoemd als multi-suite etiketteren.

**Rollup-rapportenpakket**: Gemaakt met beheerfuncties. Neemt de som van elke metrisch aan het eind van elke dag.

* Rollups zijn vrij te gebruiken en verhogen het gebruik van serveroproepen niet.
* Rollups verschaffen totale gegevens, maar rapporteren geen afzonderlijke waarden in rapporten. Zo worden eVar1-waarden niet opgenomen, maar kan het totale totaal wel zijn.
* De gegevens worden niet gededupliceerd wanneer het combineren van gegevens over rapportreeksen.
* Rollups worden elke avond uitgevoerd.
* Wanneer u een rapportsuite toevoegt aan een bestaande rollup, worden historische gegevens niet opgenomen in de rollup.
* Alle suites van het kindrapport moeten gegevens in hen hebben om een rollup te functioneren. Als nieuwe rapportsuites in een rollup worden omvat, zorg ervoor om minstens één paginamening naar die rapportsuites te verzenden.
* Rollup-rapportreeksen zijn beperkt tot maximaal 40 kinderrapportreeksen.
* Rollup-rapportsuites zijn beperkt tot maximaal 100 gebeurtenissen.
* Gegevens in Rollup-rapportreeksen ondersteunen geen onderverdelingen of segmenten.
* Het rapport Pagina&#39;s wordt vervangen door het rapport Popular Sites, dat metriek op het kind-suite niveau rapporteert.

## Rollup versus Global Report Suites

**Secundaire serveraanroepen**: Rollups doen geen extra serveraanroepen meer dan een enkele rapportsuite verzamelt. Als uw organisatie multi-suite markering gebruikt, worden secundaire serveraanroepen gedaan voor elke extra rapportsuite die in een beeldverzoek is opgenomen.

>[!TIP] Als u slechts een globale rapportreeks met [virtuele rapportreeksen](../../components/vrs/vrs-considerations.md)gebruikt, zijn geen secundaire servervraag nodig.

**Wijzigingen** in implementatie: Rollups vereisen geen implementatiewijzigingen, terwijl voor algemene rapportsuites de id van de algemene rapportsuite in uw implementatie moet worden opgenomen.

**Dupliceren**: Globale rapportsuites dedupliceren unieke bezoekers, terwijl rollups niet. Als een gebruiker bijvoorbeeld drie van uw domeinen op dezelfde dag bezoekt, tellen de rollups drie dagelijkse unieke bezoekers. Globale rapportsuites zouden één unieke bezoeker registreren.

**Tijdschema**: Rollups worden alleen elke nacht om middernacht verwerkt, terwijl algemene rapportsuites gegevens met standaardlatentie rapporteren.

**Breedte**: Rollups hebben geen manier om te communiceren tussen rapportsuites. Globale rapportsuites kunnen krediet aan omzettingsvariabelen tussen rapportsuites, evenals het verven over rapportsuites toeschrijven.

**Historische gegevens**: Rollups kunnen historische gegevens verzamelen, terwijl globale rapportsuites alleen gegevens rapporteren vanaf het punt waarop ze zijn geïmplementeerd.

**Rapporten**: Global report suites verschaffen gegevens over alle dimensies; rollups verschaffen alleen geaggregeerde gegevens over rapporten op hoog niveau.

**Ondersteunde producten**: Rollups kunnen alleen worden gebruikt in Rapporten en Analytics. Zij worden niet gesteund in de Werkruimte van de Analyse, het Pakhuis van Gegevens, of Ad hoc Analyse. Globale rapportsuites kunnen over alle producten worden gebruikt.

**Aantal samengevoegde rapporteereeksen**: Rollups bieden alleen ondersteuning voor maximaal 40 kindrapportsuites. Algemene rapportsuites kunnen worden geïmplementeerd op elk aantal domeinen of apps die u hebt.
