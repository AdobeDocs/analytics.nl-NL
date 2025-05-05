---
description: Lijst van bekende beperkingen in Adobe Analysis Workspace en de bijbehorende onderdelen
title: Bekende beperkingen in Analysis Workspace
feature: Workspace Basics
role: User, Admin
exl-id: 520e970b-1387-4f70-985b-bfe397f4a21b
source-git-commit: 2eff7656741bdba3d5d7d1f33e9261b59f8e6083
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 1%

---

# Bekende beperkingen in Analysis Workspace

Hier volgt een lijst met bekende beperkingen in Analysis Workspace en de bijbehorende componenten:

## Tabellen

* Datumvergelijkingskolommen kunnen niet worden toegevoegd wanneer datumbereiken of metriek worden gebruikt als rijen van een tabel.
* Metrisch maken van selectie is uitgeschakeld wanneer segmenten worden gebruikt als rijen van een tabel. Bovendien moet Metrisch maken van selectie niet worden toegepast op kolommen met datumuitlijning.
* Voorwaardelijke opmaak voor splitsingsrijen kan geen aangepaste bereiken gebruiken.
* De totale rijen van de lijst kunnen niet worden getrand wanneer Berekende totalen door de rijwaarden op te tellen wordt toegepast die (typisch wordt gebruikt met Statische rijpunten) plaatsen.
* [!UICONTROL Contribution Analysis] kan worden uitgevoerd op [!UICONTROL daily] granulariteit _alleen_. Het kan niet worden bestreden [!UICONTROL hourly], [!UICONTROL weekly], enz., gegevens.

## Visualisaties

* Visualisaties die segmentatie van hefboomwerking, zoals [!UICONTROL Fallout], [!UICONTROL Flow], [!UICONTROL Cohort], en [!UICONTROL Histogram], kan berekende metriek niet accepteren als invoer.
* [!UICONTROL Flow]: Afmetingen in- en uitgangen, bv. [!UICONTROL Entry page], kan niet worden gebruikt in Flow.
* [!UICONTROL Cohort]: Niet-gehele getallen kunnen niet als cohortcriteria worden gebruikt.

## Deelvensters

* Segmentvergelijking: De [!UICONTROL Everyone Else] Het segment wordt niet gecreeerd als een segmentmalplaatje in de aanvankelijke dalingsstreek wordt gebruikt.

## Componenten > Segmenten

* Bepaalde maatstaven en dimensies zijn niet segmenteerbaar, zoals [!UICONTROL Occurrences], [!UICONTROL Unique Visitors], enz.
* Adhoc-segmenten gemaakt in het dialoogvenster [dropzone van deelvenster](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/panels.html?lang=nl-NL) Dit is een type snel filter. Ze worden alleen in de linkerspoorlijn van Workspace of Segment-componentmanager weergegeven als ze openbaar worden gemaakt. Zie voor meer informatie [Snelle segmenten](/help/analyze/analysis-workspace/components/segments/quick-segments.md).

## Componenten > Berekende cijfers

* Berekende meetgegevens kunnen niet worden gebruikt in bepaalde visualisaties. Zie &#39;Visualisaties&#39; hierboven.
* Berekende metriek kan niet worden gebruikt in de [!UICONTROL Attribution] , aangezien berekende metriek zelf afzonderlijke attributiemodellen kunnen bevatten.
* Bepaalde componenten en operatoren zijn niet beschikbaar als een berekende metrische waarde wordt gemaakt in Workspace (in tegenstelling tot het resultaat [!UICONTROL Components > Segments]). Bijvoorbeeld, [!UICONTROL IP Address].

## Componenten > Datumbereik

* Aangepaste datumbereiken worden niet ondersteund [!UICONTROL This day last year], [!UICONTROL This day last month], enz.

## Componenten > Virtuele rapporten

* Wanneer de verwerking van de rapporttijd wordt toegelaten, worden bepaalde componenten niet gesteund. Zie voor een volledige lijst [Tijdverwerking rapporteren](/help/components/vrs/vrs-report-time-processing.md).

## Componenten > Alle componenten > Rapportinstellingen

* Enkele instellingen in het dialoogvenster [!UICONTROL Report Settings] is niet van toepassing. Analysis Workspace gebruikt alleen de [!UICONTROL Language/Currency/Encoding] instellingen onderaan: [!UICONTROL Thousands separator], [!UICONTROL Scheduled Report Encoding], en [!UICONTROL CSV Separator Character].

## Attributie

* Een subset van metriek wordt niet ondersteund in [!UICONTROL Attribution]. Voor een volledige lijst raadpleegt u de [Veelgestelde vragen over kenmerken](/help/analyze/analysis-workspace/attribution/faq.md).
