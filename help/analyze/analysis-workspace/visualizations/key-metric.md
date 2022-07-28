---
description: Gebruik de belangrijkste metrische samenvatting visualisatie om metrische prestaties over twee chronologie te vergelijken.
title: Samenvatting van metrische sleutel
feature: Visualizations
role: User, Admin
source-git-commit: a126f51c82cf7b23f4e03134c2d870d216dadc47
workflow-type: tm+mt
source-wordcount: '586'
ht-degree: 0%

---


# Samenvatting van metrische sleutel

>[!NOTE]
>
>Deze functionaliteit is momenteel in [beperkte tests](/help/release-notes/releases.md).

De belangrijkste Metrische Summiere visualisatie laat u zien hoe belangrijke metrisch binnen één enkel tijdkader trending. Ook kunt u de metrische prestaties in twee tijdframes vergelijken. Het biedt de voordelen van meerdere visualisaties die in één visualisatie worden gecombineerd:

* **[!UICONTROL Line]** visualisaties die tonen hoe metrisch voor de primaire en vergelijkingsdatumwaaiers trendt

* **[!UICONTROL Summary percent change]** die de metrische verhoging of daling tussen primaire en vergelijkingsdatumwaaiers toont

* Huidige totale waarde ([!UICONTROL **overzichtsnummer**]) voor de metrische

## Gebruik hoofdletters

Deze visualisatie heeft betrekking op een aantal veelvoorkomende gebruiksgevallen, waaronder:

* Een analist probeert te begrijpen hoe de creatie van kansen deze maand in vergelijking met hetzelfde tijdsbestek vorig jaar eruit zag.

* Een markering die onderzoekt hoe de productie van lood voor een specifiek loodtype van deze maand in vorige maand is veranderd.

* Een uitvoerend directeur die wil begrijpen hoe nieuwe boekingen van dit kwartaal aan vorig kwartaal veranderden.

## Vorm de Belangrijkste metrische samenvatting

1. Sleep de **[!UICONTROL Key metric summary]** visualisatie van de **[!UICONTROL Visualizations]** in de linkerspoorstaaf in een paneel.

1. Vorm visualisatie door metrisch, een primaire datumwaaier, en een waaier van de vergelijkingsdatum en een segment (indien gewenst) te selecteren:

   ![](assets/key-metric-config.png)

   | Configuratie-instelling | Definitie |
   | --- | --- |
   | **[!UICONTROL Metric]** | Selecteer metrisch u wilt onderzoeken. Alle metriek worden ondersteund. |
   | **[!UICONTROL Primary date range]** | Het huidige datumbereik voor de vrije-vormtabel. |
   | **[!UICONTROL Comparison date range]** | Het datumbereik waarmee u het primaire datumbereik wilt vergelijken. |
   | **[!UICONTROL Segment (optional)]** | Elk segment waarin u specifiek geïnteresseerd bent voor deze samenvatting. |

   {style=&quot;table-layout:auto&quot;}

1. Klik op **[!UICONTROL Build]**.

## De uitvoer weergeven

![](assets/key-metric-output.png)

Opmerking:

* De **[!UICONTROL Previous period]** lijngrafiek (altijd grijs weergegeven) komt overeen met de **[!UICONTROL Comparison date range]** in de configuratiestap.

* Als er tijdens de configuratie geen vergelijkingsdatumbereik is geselecteerd of als dit bereik verborgen is in de visualisatie-instellingen (meer onder de instellingen), wordt alleen de lijngrafiek voor het primaire datumbereik weergegeven. De samenvattingswijziging wordt verborgen.

* Vanaf hier kunt u de cursor boven de lijngrafieken houden om de statistieken voor afzonderlijke dagen weer te geven:

![](assets/key-metric-output2.png)

## Visualisatie-instellingen

De Belangrijkste metrische samenvatting biedt veelvoudige flexibele montages aan om betere rapportering en communicatie van belangrijke metriek toe te laten. Instellingen zijn toegankelijk via het tandwielpictogram in de rechterbovenhoek van de visualisatie.

![](assets/key-metric-settings.png)

| Instelling | Beschrijving |
| --- | --- |
| Percentage wijziging benadrukken | Samenvattingswijziging in opvallende vetgedrukte tekst weergeven in het midden van de visualisatie |
| Nummerwaarde benadrukken | Samenvattingsnummer in opvallende, vette letters weergeven in het midden van de visualisatie |
| Legenda zichtbaar | De legenda onder aan de visualisatie weergeven of verbergen |
| Annotaties tonen | Annotaties die zijn toegevoegd door een beheerder tonen of verbergen |
| Meerdere regels tonen | Lijngrafieken onder aan het diagram weergeven of verbergen. Als de legenda is verborgen, wordt deze niet langer visueel doorverwezen naar de regels |
| Min. en max. tonen op vonklines | Minimum- en maximumwaarden tonen of verbergen in primaire diagrammen en vergelijkingslijngrafieken |
| Vergelijking tonen | Vergelijkingsgegevens tonen of verbergen. Wanneer deze optie is verborgen, worden zowel het vergelijkingsregeldiagram als de summiere wijzigingsobjecten verborgen. |
| Totaal aantal tonen | Samenvattingsnummer tonen of verbergen |
| Raw-verschil tonen | Onbewerkt verschil tonen of verbergen tussen de totale waarde van de metrische waarde in het primaire datumbereik en het secundaire datumbereik |
| Afkorting | Afkorting van numerieke waarden om gecommuniceerde inzichten te vereenvoudigen (bijvoorbeeld 20.000 -> 20K) |

## Visualisatie bewerken

Na het bouwen van visualisatie, kunt u de originele configuratie nog uitgeven.

1. Klik op het potloodpictogram in de rechterbovenhoek van de visualisatie (naast het tandwielpictogram voor instellingen).

   ![](assets/edit-icon.png)

   U wordt nu teruggezet naar de originele configuratiemening.

1. Verander metrisch, primaire datumwaaier, de waaier van de vergelijkingsdatum, of het segment zoals aangewezen.
