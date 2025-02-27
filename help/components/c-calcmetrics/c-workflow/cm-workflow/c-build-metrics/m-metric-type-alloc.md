---
description: Meer informatie over
title: Type en attributie metrisch
feature: Calculated Metrics
exl-id: 3fb98227-e2ef-4829-ae84-812f845470ee
source-git-commit: 75d8705170169a0ef9f1ee59b12e4bb2c3afac7a
workflow-type: tm+mt
source-wordcount: '576'
ht-degree: 0%

---

# Type en attributie metrisch {#metric-type-attribution}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_nondefaultattributionmodel"
>title="Niet-standaard toewijzingsmodel gebruiken"
>abstract="Schakel een niet-standaard attributiemodel in voor de geselecteerde metrische waarde."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attributionmodel"
>title="Model"
>abstract="Selecteer een attributiemodel voor metrisch."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_lasttouch"
>title="Laatste aanraking"
>abstract="100% van het krediet gaat naar de laatste waarde van de dimensie die een bezoeker heeft gezien."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_firsttouch"
>title="Eerste aanraking"
>abstract="100% van het krediet gaat naar de waarde van de eerste dimensie die een bezoeker ziet."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_linear"
>title="Lineair"
>abstract="De creditering wordt gelijkmatig over alle afmetingswaarden verdeeld."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_participation"
>title="Deelname"
>abstract="100% is bestemd voor elke waarde van de dimensie die een bezoeker ziet.<br/> de totalen van de Kolom zijn overdreven."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_sametouch"
>title="Zelfde aanraking"
>abstract="Er wordt alleen rekening gehouden met waarden van dimensies die zich voordoen bij dezelfde gebeurtenis als conversie."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_ushaped"
>title="U-vorm"
>abstract="40% van de kredieten voor de waarde van de eerste dimensie, 40% tot de laatste, 20% gedeeld door het midden."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_jcurve"
>title="J Curve"
>abstract="60% is bestemd voor de laatste dimensie, 20% voor de eerste, 20% voor het midden."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_inversej"
>title="Omgekeerd J"
>abstract="60% is bestemd voor de waarde van de eerste dimensie, 20% voor de laatste, 20% voor het midden."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_timedecay"
>title="Tijdverlies"
>abstract="Dimension-waarden die het dichtst bij een conversie liggen, krijgen het meeste krediet."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_custom"
>title="Aangepast"
>abstract="Definieer uw eigen op positie gebaseerde toewijzingsweging."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_algorithmic"
>title="Algorithmic"
>abstract="Krediet wordt dynamisch bepaald op basis van een statistisch algoritme."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_lookbackwindow"
>title="Venster Opzoeken"
>abstract="Deze instelling bepaalt het venster met gegevenstoewijzing dat voor elke conversie wordt toegepast."

<!-- markdownlint-enable MD034 -->

Wanneer [ bouwend een berekende metrische ](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/cm-build-metrics.md), kunt u het metrische type en het attributiemodel specificeren.

## Metrisch type

Om metrisch type te specificeren wanneer het bouwen van berekende metrisch:

1. Selecteer het tandwielpictogram naast metrisch waarvan type u wilt selecteren.

   ![](assets/cm_type_alloc.png)

1. Kies een van de volgende opties:

   | Metrisch type | Definitie |
   |---|---|
   | Standard | Deze cijfers zijn dezelfde maatstaven die worden gebruikt in de standaard [!DNL Analytics] -rapportage. Als een formule uit één enkele norm bestond, toont het identieke gegevens aan zijn niet-berekende-metrische tegenhanger. Standaardmetriek zijn handig voor het maken van berekende metriek die specifiek is voor elk afzonderlijk regelitem. Bijvoorbeeld, [ orden ] / [ bezoeken ] neemt orden voor dat specifieke lijnpunt en verdeelt het door het aantal bezoeken voor dat specifieke lijnpunt. |
   | Totaal | Totaal-generaal gebruiken voor de rapportageperiode in elke post. Als een formule uit één enkel Eindtotaal metrisch bestond, toont het het zelfde totale aantal op elk lijnpunt. Eindtotaalcijfers zijn handig voor het maken van berekende metriek die wordt vergeleken met de totale gegevens van de site. Bijvoorbeeld, [ orden ] / [ Totale Bezoeken ] toont het aandeel van orden tegen ALLE bezoeken aan uw plaats, niet alleen de bezoeken aan het specifieke lijnpunt. |

## Hoe lineaire toewijzing werkt

[ Attributie ](/help/analyze/analysis-workspace/attribution/overview.md) is hoe de toewijzingsmodellen in berekende metriek worden geëvalueerd.

Voor een volledige lijst van niet-gebrek attributiemodellen en raadplegingsvensters die worden gesteund, zie {de modellen van de Attributie en raadplegingsvensters ](/help/analyze/analysis-workspace/attribution/models.md).[

In het volgende voorbeeld wordt getoond hoe berekende metriek met lineaire toewijzingen in rapportage werkt:

| | Hit 1 | Hit 2 | Hit 3 | Hit 4 | Actief 5 | Hit 6 | Hit 7 |
|--- |--- |--- |--- |--- |--- |--- |--- |
| Gegevens verzonden in | PROMO A | - | PROMO A | PROMO B | - | PROMO C | $ 10 |
| Last Touch eVar | PROMO A | PROMO A | PROMO A | PROMO B | PROMO B | PROMO C | $ 10 |
| Eerste aanraking met eVar | PROMO A | PROMO A | PROMO A | PROMO A | PROMO A | PROMO A | $ 10 |
| Voorbeeld | PROMO A | - | PROMO A | PROMO B | - | PROMO C | $ 10 |

In dit voorbeeld werden de waarden A, B, en C naar een variabele gestuurd bij hits 1, 3, 4 en 6 voordat een aankoop van 10 dollar werd gedaan bij hit 7. In de tweede rij blijven deze waarden bij alle treffers op een laatste aanraakbezoek aanwezig. De derde rij illustreert de persistentie van een eerste aanraakbezoek. Tot slot illustreert de laatste rij hoe gegevens zouden worden geregistreerd voor een eigenschap die niet persistentie heeft.

