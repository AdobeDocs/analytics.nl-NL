---
description: Lijst met bekende beperkingen in de Adobe Analyse Workspace en de bijbehorende componenten
title: Bekende beperkingen in analysewerkruimte
translation-type: tm+mt
source-git-commit: fd4d016ffd47e74ebcd4c850f35a5471ca358366

---


# Bekende beperkingen in analysewerkruimte

Hier volgt een lijst met bekende beperkingen in de analysewerkruimte en de bijbehorende componenten:

## Tabellen

* Datumvergelijkingskolommen kunnen niet worden toegevoegd wanneer datumbereiken of metriek worden gebruikt als rijen van een tabel.
* Metrisch maken van selectie is uitgeschakeld wanneer segmenten worden gebruikt als rijen van een tabel. Bovendien moet Metrisch maken van selectie niet worden toegepast op kolommen met datumuitlijning.
* Voorwaardelijke opmaak voor splitsingsrijen kan geen aangepaste bereiken gebruiken.
* De totale rijen van de lijst kunnen niet worden getrand wanneer Berekende totalen door de rijwaarden op te tellen wordt toegepast die (typisch wordt gebruikt met Statische rijpunten) plaatsen.
* [!UICONTROL Contribution Analysis] kan [!UICONTROL daily] alleen _met de_ granulariteit worden uitgevoerd. Het kan niet worden uitgevoerd tegen [!UICONTROL hourly], [!UICONTROL weekly]etc., gegevens.

## Visualisaties

* Visualisaties die de hefboomfinanciering segmentatie, zoals [!UICONTROL Fallout], [!UICONTROL Flow], [!UICONTROL Cohort]en [!UICONTROL Histogram], niet berekende metriek als input accepteren.
* [!UICONTROL Flow]: Afmetingen in- en uitgangen, bv. [!UICONTROL Entry page], kan niet in Stroom worden gebruikt.
* [!UICONTROL Cohort]: Niet-gehele getallen kunnen niet als cohortcriteria worden gebruikt.

## Deelvensters

* Segmentvergelijking: Het [!UICONTROL Everyone Else] segment wordt niet gecreeerd als een segmentmalplaatje in de aanvankelijke dalingsstreek wordt gebruikt.

## Componenten > Segmenten

* Bepaalde maatstaven en dimensies kunnen niet worden gesegmenteerd, zoals [!UICONTROL Occurrences], [!UICONTROL Unique Visitors]enz.
* Bepaalde componenten en operatoren zijn niet beschikbaar als een segment wordt gemaakt vanuit Workspace (in tegenstelling tot het segment dat wordt gemaakt van [!UICONTROL Components > Segments]). Bijvoorbeeld, IP Adres.

## Componenten > Berekende cijfers

* Berekende meetgegevens kunnen niet worden gebruikt in bepaalde visualisaties. Zie &#39;Visualisaties&#39; hierboven.
* Berekende metriek kunnen niet in het [!UICONTROL Attribution] paneel worden gebruikt, aangezien de berekende metriek zelf afzonderlijke attributiemodellen kunnen omvatten.
* Bepaalde componenten en operatoren zijn niet beschikbaar als een berekende metrische waarde wordt gemaakt in Workspace (in tegenstelling tot het resultaat van [!UICONTROL Components > Segments]). Bijvoorbeeld, [!UICONTROL IP Address].

## Componenten > Datumbereik

* Aangepaste datumbereiken bieden geen ondersteuning voor [!UICONTROL This day last year], [!UICONTROL This day last month]enzovoort.

## Componenten > Virtuele rapporten

* Wanneer de verwerking van de rapporttijd wordt toegelaten, worden bepaalde componenten niet gesteund. Voor een volledige lijst, zie de Verwerking [van de Tijd van het](/help/components/vrs/vrs-report-time-processing.md)Rapport.

## Componenten > Rapportinstellingen

* Sommige instellingen op de [!UICONTROL Report Settings] pagina zijn niet van toepassing. De werkruimte Analyse gebruikt alleen de [!UICONTROL Language/Currency/Encoding] instellingen onderaan: [!UICONTROL Thousands separator], [!UICONTROL Scheduled Report Encoding], en [!UICONTROL CSV Separator Character].

## Attributie-IQ

* Een subset metriek wordt niet ondersteund in [!UICONTROL Attribution IQ]. Voor een volledige lijst, zie de Veelgestelde vragen van [Attributie IQ](/help/analyze/analysis-workspace/c-panels/attribution/attribution-faq.md).
