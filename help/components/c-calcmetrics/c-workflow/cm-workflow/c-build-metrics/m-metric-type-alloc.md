---
description: Meer informatie over
title: Type en attributie metrisch
feature: Calculated Metrics
exl-id: 3fb98227-e2ef-4829-ae84-812f845470ee
source-git-commit: 7722a2f01ff77dfec8ce110fd04fe977f6c627c6
workflow-type: tm+mt
source-wordcount: '466'
ht-degree: 1%

---

# Type en attributie metrisch

Wanneer [bouwen van berekende metrisch](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/cm-build-metrics.md)kunt u het metrische type en het attributiemodel opgeven.

## Metrisch type

Om metrisch type te specificeren wanneer het bouwen van berekende metrisch:

1. Selecteer het tandwielpictogram naast metrisch waarvan type u wilt selecteren.

   ![](assets/cm_type_alloc.png)

1. Kies een van de volgende opties:

   | Metrisch type | Definitie |
   |---|---|
   | Standaard | Deze cijfers zijn dezelfde maatstaven die standaard worden gebruikt [!DNL Analytics] rapportage. Als een formule uit één enkele norm bestond, toont het identieke gegevens aan zijn niet-berekende-metrische tegenhanger. Standaardmetriek zijn handig voor het maken van berekende metriek die specifiek is voor elk afzonderlijk regelitem. Bijvoorbeeld: [Orders] / [Bezoeken] neemt orders voor dat specifieke lijnpunt en verdeelt het door het aantal bezoeken voor dat specifieke lijnpunt. |
   | Totaal-generaal | Totaal-generaal gebruiken voor de rapportageperiode in elke post. Als een formule uit één enkel Eindtotaal metrisch bestond, toont het het zelfde totale aantal op elk lijnpunt. Eindtotaalcijfers zijn handig voor het maken van berekende metriek die wordt vergeleken met de totale gegevens van de site. Bijvoorbeeld: [Orders] / [Totaal aantal bezoeken] geeft het aantal bestellingen tegen ALLE bezoeken aan uw site weer, niet alleen de bezoeken aan het specifieke onderdeel. |

## Hoe lineaire toewijzing werkt

[Attribution IQ](/help/analyze/analysis-workspace/attribution/overview.md) is hoe toewijzingsmodellen in berekende metriek worden geëvalueerd.

Voor een volledige lijst met ondersteunde niet-standaard toewijzingsmodellen en terugzoekvensters raadpleegt u [Attributiemodellen en terugzoekvensters](/help/analyze/analysis-workspace/attribution/models.md).

In het volgende voorbeeld wordt getoond hoe berekende metriek met lineaire toewijzingen in rapportage werkt:

|  | Hit 1 | Hit 2 | Hit 3 | Hit 4 | Actief 5 | Hit 6 | Hit 7 |
|--- |--- |--- |--- |--- |--- |--- |--- |
| Gegevens verzonden in | PROMO A | - | PROMO A | PROMO B | - | PROMO C | $10 |
| Laatste aanraking eVar | PROMO A | PROMO A | PROMO A | PROMO B | PROMO B | PROMO C | $10 |
| Eerste aanraking eVar | PROMO A | PROMO A | PROMO A | PROMO A | PROMO A | PROMO A | $10 |
| Voorbeeld | PROMO A | - | PROMO A | PROMO B | - | PROMO C | $10 |

In dit voorbeeld werden de waarden A, B, en C naar een variabele gestuurd bij hits 1, 3, 4 en 6 voordat een aankoop van 10 dollar werd gedaan bij hit 7. In de tweede rij blijven deze waarden bij alle treffers op een laatste aanraakbezoek aanwezig. De derde rij illustreert de persistentie van een eerste aanraakbezoek. Tot slot illustreert de laatste rij hoe gegevens zouden worden geregistreerd voor een eigenschap die niet persistentie heeft.

## Verschillen in hoe lineaire toewijzing werkt in Rapporten &amp; Analytics versus Werkruimte

Er zijn enkele verschillen in de manier waarop lineaire toewijzing werkt tussen deze twee gereedschappen:

* In Rapporten &amp; Analytics, (verwerkte) lineaire attributie is altijd bezoek gebaseerd, terwijl in Werkruimte, het bezoek of bezoeker kan zijn gebaseerd.
* Als in Rapporten &amp; Analytics geen waarde werd doorgegeven bij de eerste treffer van een bezoek, blijft de (initiële) waarde behouden bij het vorige bezoek. Dit is NIET het geval in Werkruimte (Attribution IQ). Als er geen waarde wordt doorgegeven bij de eerste aanraking van een bezoek, is Geen de beginwaarde.
