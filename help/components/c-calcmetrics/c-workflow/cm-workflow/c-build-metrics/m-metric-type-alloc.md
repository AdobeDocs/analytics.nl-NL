---
description: 'Meer informatie over '
title: Type cijfers en attributie
uuid: 64649698-df2a-42c3-bb31-938f766e1d1f
translation-type: tm+mt
source-git-commit: d0fe97b9368cbc4c9e79f9e56adf9786b58dce1a
workflow-type: tm+mt
source-wordcount: '908'
ht-degree: 6%

---


# Type cijfers en attributie

Als u het tandwielpictogram naast een metrische waarde selecteert, kunt u het metrische type en het attributiemodel opgeven.

## Metrisch type

![](assets/cm_type_alloc.png)

| Metrisch type | Definitie |
|---|---|
| Standaard | Deze metriek zijn de zelfde metriek die in standaard [!DNL Analytics] rapportering wordt gebruikt. Als een formule uit één enkele norm bestond, toont het identieke gegevens aan zijn niet-berekende-metrische tegenhanger. Standaardmetriek zijn handig voor het maken van berekende metriek die specifiek is voor elk afzonderlijk regelitem. Bijvoorbeeld, [Orders] / [Visits] neemt orden voor dat specifieke lijnpunt en verdeelt het door het aantal bezoeken voor dat specifieke lijnpunt. |
| Totaal | Gebruik het totaal voor de rapportageperiode in elke post. Als een formule uit één enkel totaal metrisch bestond, toont het het zelfde totale aantal op elk lijnpunt. De totale metriek zijn nuttig om berekende metriek tot stand te brengen die met plaats totale gegevens vergelijkt. Bijvoorbeeld [Bestellingen] / [Totaal aantal bezoeken] toont het aandeel van bestellingen tegen ALLE bezoeken aan uw plaats, niet alleen de bezoeken aan het specifieke lijnpunt. |

## Model kolomkenmerk

>[!IMPORTANT]
>
>In juli 2018 heeft [!DNL Analytics] [Attribution IQ](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/panels/attribution/attribution.html) geïntroduceerd, die de manier waarop toewijzingsmodellen in berekende metriek worden geëvalueerd, heeft herzien. In het kader van deze wijziging zijn berekende maatstaven die een niet-standaard toewijzingsmodel gebruiken, gemigreerd naar nieuwe, verbeterde toewijzingsmodellen:
>
>* Raadpleeg de documentatie [Attribution IQ](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/panels/attribution/attribution.html) voor een volledige lijst met ondersteunde niet-standaard toewijzingsmodellen en terugzoekvensters.
>* De toewijzingsmodellen &quot;Marketing Channel Last Touch&quot; en &quot;Marketing Channel First Touch&quot; worden gemigreerd naar nieuwe toewijzingsmodellen &quot;Last Touch&quot; en &quot;First Touch&quot; (Opmerking: De &quot;Kanalen van de marketing&quot;zullen niet worden afgekeurd - slechts zullen de twee toewijzingsmodellen die in berekende metriek verschijnen).
>* Bovendien zullen we de manier corrigeren waarop de lineaire toewijzing wordt berekend. Voor klanten die berekende metriek met &quot;Lineaire&quot;toewijzingsmodellen gebruiken, kunnen de rapporten lichtjes veranderen om het nieuwe, gecorrigeerde attributiemodel te weerspiegelen. Deze wijziging in berekende metriek wordt weerspiegeld in Analysis Workspace, Reports &amp; Analytics, de Reporting API, en Report Builder. Zie **Hoe Lineaire toewijzing werkt (vanaf 19 juli 2018**, hieronder voor meer informatie.

>



## Hoe de lineaire toewijzing werkt (vanaf 19 juli 2018)

In juli 2018 veranderde Adobe hoe lineaire allocatie wordt gerapporteerd voor Berekende metriek. Deze wijziging is van invloed op Analysis Workspace, Rapporten en Analytics, Report Builder, Activity Map en de API&#39;s voor rapportage. De wijziging heeft hoofdzakelijk invloed op eVars en andere dimensies die persistentie hebben. Merk op dat deze veranderingen slechts op berekende metriek van toepassing zijn en andere rapporten niet gebruikend lineaire toewijzing (zoals het rapport van Pagina&#39;s in Rapporten &amp; Analytics) beïnvloeden. Andere verslagen die gebruikmaken van lineaire allocatie zullen de bestaande lineaire toewijzingsmethode blijven gebruiken.

In het volgende voorbeeld wordt getoond hoe berekende metriek met lineaire toewijzing wordt gewijzigd in de rapportage:

|  | Hit 1 | Hit 2 | Hit 3 | Hit 4 | Actief 5 | Hit 6 | Hit 7 |
|--- |--- |--- |--- |--- |--- |--- |--- |
| Gegevens verzonden in | PROMO A | - | PROMO A | PROMO B | - | PROMO C | $ 10 |
| Laatste aanraking eVar | PROMO A | PROMO A | PROMO A | PROMO B | PROMO B | PROMO C | $ 10 |
| Eerste aanraking eVar | PROMO A | PROMO A | PROMO A | PROMO A | PROMO A | PROMO A | $ 10 |
| Voorbeeld | PROMO A | - | PROMO A | PROMO B | - | PROMO C | $ 10 |

In dit voorbeeld werden de waarden A, B, en C naar een variabele gestuurd bij hits 1, 3, 4 en 6 voordat een aankoop van 10 dollar werd gedaan bij hit 7. In de tweede rij blijven deze waarden bij alle treffers op een laatste aanraakbezoek aanwezig. De derde rij illustreert de persistentie van een eerste aanraakbezoek. Tot slot illustreert de laatste rij hoe gegevens zouden worden geregistreerd voor een eigenschap die niet persistentie heeft.

## Verschillen in hoe lineaire toewijzing werkt in Rapporten &amp; Analytics versus Werkruimte

Er zijn enkele verschillen in de manier waarop lineaire toewijzing werkt tussen deze twee gereedschappen:

* In Rapporten &amp; Analytics, (verwerkte) lineaire attributie is altijd bezoek gebaseerd, terwijl in Werkruimte, het bezoek of bezoeker kan zijn gebaseerd.
* Als in Rapporten &amp; Analytics geen waarde werd doorgegeven bij de eerste treffer van een bezoek, blijft de (initiële) waarde behouden bij het vorige bezoek. Dit is NIET het geval in Werkruimte (Attribution IQ). Als er geen waarde wordt doorgegeven bij de eerste aanraking van een bezoek, is Geen de beginwaarde.

## Hoe lineaire toewijzing werkte vóór juli 2018

Vóór 19 juli 2018 werd de lineaire attributie berekend nadat de eerste aanraking of laatste aanraakpersistentie al was opgetreden. Dit betekende dat voor de laatste aanraking hierboven, $10 als volgt zou worden verdeeld: A = 10 * (3/6) = $5, B = 10 * (2/6) = $3,33, C = 10 * (1/6) = $1,67.

Voor de eerste aanraking hierboven, alle $10 zou aan A worden gegeven. Voor de eigenschap: A = 10 * (2/4) = $5, B = 10 * (1/4) = $2.50, en C = 10 * (1/4) = $2.50. Een overzicht geven van de lineaire toewijzing zoals deze voorheen werkte:

| Waarden | Huidige eVar met laatste aanraking | Huidige eVar eerste aanraking | Huidige eigenschap |
|---|---|---|---|
| PROMO A | $ 5,00 | $ 10,00 | $ 5,00 |
| PROMO B | $ 3,33 | $0 | $ 2,50 |
| PROMO C | $ 1,67 | $0 | $ 2,50 |
| Totaal | $ 10,00 | $ 10,00 | $ 10,00 |

**Overzicht van de werking van lineaire toewijzing op 19 juli 2018**

Na 19 juli corrigeerden we dit gedrag in berekende metriek. In plaats van de blijvend waarden te gebruiken op basis van laatste aanraking of eerste aanraking, gebruikt [!DNL Analytics] nu alleen de waarden die zijn doorgegeven (de eerste rij van de bovenste tabel). Als zodanig hebben de instellingen voor dimensietoewijzing geen invloed meer op de manier waarop lineaire toewijzing wordt berekend (d.w.z. dat props en eVars op dezelfde manier worden behandeld), en de resultaten weerspiegelen wat oorspronkelijk is doorgegeven in plaats van de eerste of laatste aanraakwaarden die mogelijk hebben geduurd. In alle drie gevallen is A = 10 * (2/4) = $5, B = 10 * (1/4) = $2,50, en C = 10 * (1/4) = $2,50.

| Waarden | Nieuwe eVar met laatste aanraking | Nieuwe eVar eerste aanraking | Nieuwe eigenschap |
|---|---|---|---|
| PROMO A | $ 5,00 | $ 5,00 | $ 5,00 |
| PROMO B | $ 2,50 | $ 2,50 | $ 2,50 |
| PROMO C | $ 2,50 | $ 2,50 | $ 2,50 |
| Totaal | $ 10,00 | $ 10,00 | $ 10,00 |

