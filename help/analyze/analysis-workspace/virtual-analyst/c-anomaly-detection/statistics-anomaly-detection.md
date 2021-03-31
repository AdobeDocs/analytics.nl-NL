---
description: Gegevensinconsistenties kunnen grote problemen veroorzaken. Leer hoe u statistische anomalieën kunt identificeren met afwijkende detectietechnieken van Adobe. Ga vandaag aan de slag.
title: Statistische technieken voor anomaliedetectie
feature: AI-gereedschappen
role: Bedrijfs Praktijk, Beheerder
translation-type: tm+mt
source-git-commit: 894ee7a8f761f7aa2590e06708be82e7ecfa3f6d
workflow-type: tm+mt
source-wordcount: '797'
ht-degree: 1%

---


# Statistische technieken voor anomaliedetectie

Anomaly detection in Analysis Workspace maakt gebruik van een reeks geavanceerde statistische technieken om te bepalen of een waarneming al dan niet als abnormaal moet worden beschouwd.

Afhankelijk van de in het verslag gebruikte datum van granulariteit worden drie verschillende statistische technieken gebruikt, met name voor anomaliedetectie per uur, dag, week/maand. Elke statistische techniek wordt hieronder beschreven.

## Anomalische detectie voor dagelijkse granulariteit {#section_758ACA3C0A6B4D399563ECABFB8316FA}

Voor dagelijkse granularity- rapporten, overweegt het algoritme verscheidene belangrijke factoren om de nauwkeurigste mogelijke resultaten te leveren. Ten eerste bepaalt het algoritme welk type model moet worden toegepast op basis van beschikbare gegevens waarvan we kiezen uit een van de twee klassen - een op tijdreeksen gebaseerd model of een uitbijsteringsdetectiemodel (functionele filtering genoemd).

De modelselectie van tijdreeksen is gebaseerd op de volgende combinaties voor het type fout, trend en seizoensgebondenheid (ETS) zoals beschreven door [Hyndman et al. (2008)](https://www.springer.com/us/book/9783540719168). Specifiek, probeert het algoritme de volgende combinaties:

1. ANA (additieve fout, geen trend, additieve seizoensgebondenheid)
1. AAA (additieve fout, additieve trend, additieve seizoensgebondenheid)
1. MNM (multiplicatieve fout, geen trend, multiplicatieve seizoensgebondenheid)
1. MNA (multiplicatieve fout, geen trend, additieve seizoensgebondenheid)
1. AN (additieve fout, additieve trend, geen seizoensgebondenheid)

Het algoritme test de geschiktheid van elk van deze door één met het beste gemiddelde absolute percentagefout (MAPE) te selecteren. Als de MAPE van het beste tijdreeksmodel echter groter is dan 15%, wordt functionele filtering toegepast. Doorgaans zijn gegevens met een hoge herhalingsgraad (bv. week in week of maand in maand) het meest geschikt voor een tijdreeksmodel.

Na modelselectie past het algoritme vervolgens de resultaten aan op basis van vakantie en seizoensgebondenheid van jaar tot jaar. Voor feestdagen controleert het algoritme of een van de volgende feestdagen aanwezig is in het rapportagedatumbereik:

* Herdenkingsdag
* Juli 4
* Thanksgiving
* Zwarte vrijdag
* Cyber maandag
* 24-26 december
* Januari 1
* 31 december

Deze feestdagen werden gekozen op basis van een uitgebreide statistische analyse van vele datapunten van klanten om vast te stellen welke vakanties het meest tot het hoogste aantal trends van klanten hebben beïnvloed. Hoewel de lijst zeker niet uitputtend voor alle klanten of bedrijfscycli is, ontdekten wij dat het toepassen van deze vakanties beduidend de prestaties van het algoritme over het algemeen voor bijna alle datasets van klanten verbeterde.

Zodra het model is geselecteerd en de feestdagen zijn geïdentificeerd in de rapporteringsdatumreeks, gaat het algoritme op de volgende manier te werk:

1. De afwijkende referentieperiode samenstellen - dit omvat 35 dagen vóór het bereik van de rapportagedatum en een periode van 1 jaar vóór de matchingdatum (rekening houdend met schrikkeldagen wanneer dat vereist is en met alle van toepassing zijnde feestdagen die zich op een andere kalenderdag van het voorgaande jaar kunnen hebben voorgedaan).
1. Test of de feestdagen in de huidige periode (exclusief het voorafgaande jaar) op basis van de meest recente gegevens abnormaal zijn.
1. Als de vakantie in het huidige datumbereik afwijkend is, past u de verwachte waarde en betrouwbaarheidsinterval van de huidige vakantie aan op basis van de vakantie van het voorgaande jaar (rekening houdend met twee dagen voor en na). De correctie voor de huidige vakantie is gebaseerd op het laagste gemiddelde absolute foutenpercentage van:

   1. Additieve effecten
   1. Multiplicatieve effecten
   1. YoY verschil

U ziet de dramatische verbetering van de prestaties op kerstdag en Nieuwjaarsdag in het volgende voorbeeld:

![](assets/anomaly_statistics.png)

## Anomalydetectie voor korrelvormigheid per uur {#section_014C9E9209AF43F8A03D5D46E3B3AEE7}

Uurgegevens zijn gebaseerd op dezelfde tijdreeksalgoritmebenadering als het algoritme voor dagelijkse granulariteit. Zij is echter sterk afhankelijk van twee trendpatronen: de cyclus van 24 uur en de cyclus van weekenddagen. Om deze twee seizoenseffecten in aanmerking te nemen, bouwt het uuralgoritme twee afzonderlijke modellen voor een weekend en een weekdag volgens dezelfde hierboven beschreven aanpak.

De trainingsvensters voor trends per uur zijn gebaseerd op een terugzoekvenster van 336 uur.

## Anomalische detectie voor wekelijkse en maandelijkse granulariteit {#section_5D421576BFBC4B24A58DFCC0A6407545}

Wekelijks- en maandtrends vertonen niet dezelfde wekelijkse of dagelijkse trends die worden aangetroffen bij dagelijkse of uurmatige granulariteiten, zodat een dergelijk afzonderlijk algoritme wordt gebruikt. Voor elke week en elke maand wordt een tweestapsdetectieaanpak gebruikt, die bekend staat als de Gegeneraliseerde Extreme Studentized Deviate (GESD) test. Bij deze test wordt rekening gehouden met het maximumaantal verwachte anomalieën in combinatie met de aangepaste box-plot-aanpak (een niet-parametrische methode voor de detectie van uitbijters) om het maximumaantal uitschieters te bepalen. De twee stappen zijn:

1. Aangepaste box-plot-functie: Deze functie bepaalt het maximumaantal anomalieën op basis van de invoergegevens.
1. GESD, functie: Toegepast op de invoergegevens met de uitvoer uit stap 1.

De op vakantie- en YoY-seizoensonaliteitsanomaliedetectie zet vervolgens de gegevens van vorig jaar af van de gegevens van dit jaar en herhaalt vervolgens de gegevens opnieuw met behulp van het bovenstaande tweestappenproces om te controleren of anomalieën seizoensmatig geschikt zijn. Voor elk van deze datumgranulariteiten wordt een lookback van 15 perioden gebruikt, inclusief de geselecteerde rapporteringsdatumreeks (15 maanden of 15 weken) en een corresponderende datumbereik van 1 jaar geleden voor training.
