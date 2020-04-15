---
description: 'Meer informatie over '
title: Metrisch type en kenmerk
uuid: 64649698-df2a-42c3-bb31-938f766e1d1f
translation-type: tm+mt
source-git-commit: 7a791dda238b04fbee2773c60668eb45db0a1fd0

---


# Metrisch type en kenmerk

Als u het tandwielpictogram naast een metrische waarde selecteert, kunt u het metrische type en het attributiemodel opgeven.

* [Metrisch type](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/m-metric-type-alloc.md#section_34A86FB402F94E988724232283BF18B7)
* [Model kolomkenmerk](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/m-metric-type-alloc.md#section_F9690FD1943B403AB28E2FAC54EFE032)
* [Hoe Lineaire toewijzing werkt (vanaf 19 juli 2018)](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/m-metric-type-alloc.md#section_EDBB2E14A6C248C5A79C0913C02D7CA1)

## Metrisch type

![](assets/cm_type_alloc.png)

| Metrisch type | Definitie |
|---|---|
| Standaard | Deze metriek zijn de zelfde metriek die in standaard [!DNL Analytics] rapportering wordt gebruikt. Als een formule uit één enkele norm bestond, toont het identieke gegevens aan zijn niet-berekende-metrische tegenhanger. Standaardmetriek zijn handig voor het maken van berekende metriek die specifiek is voor elk afzonderlijk regelitem. Bijvoorbeeld, neemt de [Orders] / [Bezoekingen] orden voor dat specifieke lijnpunt en verdeelt het door het aantal bezoeken voor dat specifieke lijnpunt. |
| Totaal | Gebruik het totaal voor de rapportageperiode in elke post. Als een formule uit één enkel totaal metrisch bestond, toont het het zelfde totale aantal op elk lijnpunt. De totale metriek zijn nuttig om berekende metriek tot stand te brengen die met plaats totale gegevens vergelijkt. Bijvoorbeeld, tonen de [Orders] / [Totale Bezoekingen] het aandeel van orden tegen ALLE bezoeken aan uw plaats, niet alleen de bezoeken aan het specifieke lijnpunt. |

## Model kolomkenmerk

>[!IMPORTANT]
>
>In juli 2018 [!DNL Analytics] introduceerde [Attribution IQ](https://marketing.adobe.com/resources/help/en_US/analytics/analysis-workspace/attribution.html), die de manier herzag waarop toewijzingsmodellen in berekende metriek worden geëvalueerd. In het kader van deze wijziging zijn berekende maatstaven die een niet-standaard toewijzingsmodel gebruiken, gemigreerd naar nieuwe verbeterde toewijzingsmodellen:
>
>* Voor een volledige lijst van niet-gebrek attributie modellen en raadplegingsvensters die worden gesteund, zie de documentatie van [Attributie IQ](https://marketing.adobe.com/resources/help/en_US/analytics/analysis-workspace/attribution.html) .
>* De toewijzingsmodellen &quot;Marketing Channel Last Touch&quot; en &quot;Marketing Channel First Touch&quot; worden gemigreerd naar nieuwe toewijzingsmodellen &quot;Last Touch&quot; en &quot;First Touch&quot; (Opmerking: De &quot;Kanalen van de marketing&quot;zullen niet worden afgekeurd - slechts zullen de twee toewijzingsmodellen die in berekende metriek verschijnen).
>* Bovendien zullen we de manier corrigeren waarop de lineaire toewijzing wordt berekend. Voor klanten die berekende metriek met &quot;Lineaire&quot;toewijzingsmodellen gebruiken, kunnen de rapporten lichtjes veranderen om het nieuwe, gecorrigeerde attributiemodel te weerspiegelen. Deze verandering in berekende metriek zal in de Werkruimte van de Analyse, Rapporten &amp; Analyse, de Rapporterende API, de Bouwer van het Rapport, en Ad hoc Analyse worden weerspiegeld. Zie **Hoe Lineaire toewijzing werkt (vanaf 19 juli 2018**, hieronder voor meer informatie.
>



## Hoe de lineaire toewijzing werkt (vanaf 19 juli 2018)

In juli 2018 heeft Adobe de rapportage van lineaire toewijzing voor Berekende waarden gewijzigd. Deze verandering beïnvloedt de Werkruimte van de Analyse, Ad hoc Analyse, Rapporten &amp; Analyse, de Bouwer van het Rapport, de Kaart van de Activiteit, en de Rapporterende APIs. De wijziging heeft hoofdzakelijk invloed op eVars en andere dimensies die persistentie hebben. Merk op dat deze veranderingen slechts op berekende metriek van toepassing zijn en andere rapporten niet gebruikend lineaire toewijzing (zoals het rapport van Pagina&#39;s in Rapporten &amp; Analytics) beïnvloeden. Andere verslagen die gebruikmaken van lineaire allocatie zullen de bestaande lineaire toewijzingsmethode blijven gebruiken.

In het volgende voorbeeld wordt getoond hoe berekende metriek met lineaire toewijzing wordt gewijzigd in de rapportage:

|  | Hit 1 | Hit 2 | Hit 3 | Hit 4 | Actief 5 | Hit 6 | Hit 7 |
|--- |--- |--- |--- |--- |--- |--- |--- |
| Gegevens verzonden in | PROMO A | - | PROMO A | PROMO B | - | PROMO C | $10 |
| Laatste Touch Var | PROMO A | PROMO A | PROMO A | PROMO B | PROMO B | PROMO C | $10 |
| Eerste Touch Var | PROMO A | PROMO A | PROMO A | PROMO A | PROMO A | PROMO A | $10 |
| Voorbeeld | PROMO A | - | PROMO A | PROMO B | - | PROMO C | $10 |

In dit voorbeeld werden de waarden A, B, en C naar een variabele gestuurd bij hits 1, 3, 4 en 6 voordat een aankoop van 10 dollar werd gedaan bij hit 7. In de tweede rij blijven deze waarden bij alle treffers op een laatste aanraakbezoek aanwezig. De derde rij illustreert de persistentie van een eerste aanraakbezoek. Tot slot illustreert de laatste rij hoe gegevens zouden worden geregistreerd voor een eigenschap die niet persistentie heeft.

## Verschillen in hoe lineaire toewijzing werkt in Rapporten &amp; Analytics versus Werkruimte

Er zijn enkele verschillen in de manier waarop lineaire toewijzing werkt tussen deze twee gereedschappen:

* In Rapporten &amp; Analytics, (verwerkte) lineaire attributie is altijd bezoek gebaseerd, terwijl in Werkruimte, het bezoek of bezoeker kan zijn gebaseerd.
* Als in Rapporten &amp; Analytics geen waarde werd doorgegeven bij de eerste treffer van een bezoek, blijft de (initiële) waarde behouden bij het vorige bezoek. Dit is NIET het geval in Workspace (Attribution IQ). Als er geen waarde wordt doorgegeven bij de eerste aanraking van een bezoek, is Geen de beginwaarde.

## Hoe lineaire toewijzing werkte vóór juli 2018

Vóór 19 juli 2018 werd de lineaire attributie berekend nadat de eerste aanraking of laatste aanraakpersistentie al was opgetreden. Dit betekende dat voor de laatste aanraak-Var hierboven, $10 als volgt zou worden verdeeld: A = 10 * (3/6) = $5, B = 10 * (2/6) = $3,33, C = 10 * (1/6) = $1,67.

Voor de eerste aanraking hierboven, alle $10 zou aan A worden gegeven. Voor de eigenschap: A = 10 * (2/4) = $5, B = 10 * (1/4) = $2.50, en C = 10 * (1/4) = $2.50. Een overzicht geven van de lineaire toewijzing zoals deze voorheen werkte:

| Waarden | Huidige laatste aanraakbeweging | Huidige eerste aanraakbeweging | Huidige eigenschap |
|---|---|---|---|
| PROMO A | $5.00 | $10.00 | $5.00 |
| PROMO B | $3.33 | $0 | $2.50 |
| PROMO C | $1.67 | $0 | $2.50 |
| Totaal | $10.00 | $10.00 | $10.00 |

**Overzicht van de werking van lineaire toewijzing op 19 juli 2018**

Na 19 juli corrigeerden we dit gedrag in berekende metriek. In plaats van de blijvende waarden te gebruiken op basis van laatste aanraking of eerste aanraking, worden [!DNL Analytics] nu alleen de waarden gebruikt die zijn doorgegeven (de eerste rij van de bovenste tabel). Als zodanig hebben de instellingen voor dimensietoewijzing geen invloed meer op de manier waarop lineaire toewijzing wordt berekend (d.w.z. dat props en eVars op dezelfde manier worden behandeld), en de resultaten weerspiegelen wat oorspronkelijk is doorgegeven in plaats van de eerste of laatste aanraakwaarden die mogelijk hebben geduurd. In alle drie gevallen is A = 10 * (2/4) = $5, B = 10 * (1/4) = $2,50, en C = 10 * (1/4) = $2,50.

| Waarden | Nieuwe laatste Touch Var | Nieuwe eerste Touch Var | Nieuwe eigenschap |
|---|---|---|---|
| PROMO A | $5.00 | $5.00 | $5.00 |
| PROMO B | $2.50 | $2.50 | $2.50 |
| PROMO C | $2.50 | $2.50 | $2.50 |
| Totaal | $10.00 | $10.00 | $10.00 |

