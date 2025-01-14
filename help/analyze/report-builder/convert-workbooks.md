---
title: Hoe te om uw oudere werkboeken van de Report Builder in gegevensbestanden om te zetten
description: Beschrijft hoe uw erfenisverzoeken in gegevensbestanden omzetten
role: User
feature: Report Builder
type: Documentation
solution: Analytics
source-git-commit: eedabc6295f9b918e1e00b93993680e676c216c3
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 0%

---


# Oudere werkboeken voor Reporten Builder converteren naar databases

Als deel van de beweging aan een nieuwe technologie van de Report Builder, kunt u uw huidige oudere werkboeken in op Java-Script-Gebaseerde werkboeken snel omzetten.

>[!IMPORTANT]
>
>Dupliceer elk werkboek en noem één versie anders alvorens u het omzet. Zo, hebt u nog een exemplaar van het originele werkboek als u het nodig hebt.

>[!VIDEO](https://video.tv.adobe.com/v/3434957/?quality=12&learn=on)

1. Opstelling de nieuwe Report Builder door [ na deze instructies ](/help/analyze/report-builder/report-builder-setup.md).

1. Open Excel en klik op het Adobe Report Builder-pictogram rechtsboven.

1. Klik op **[!UICONTROL Login]** en meld u aan bij de Report Builder.

1. De Report Builder toe:voegen-binnen ontdekt als dit werkboek ](/help/analyze/legacy-report-builder/home.md) verzoeken van de Report Builder van de Verouderde 1} bevat.[

   {de herinnering van het 0} verbeteringswerkboek ](assets/upgrade_workbook.png)![

1. Als één of meerdere erfenisverzoeken worden gevonden, klik **[!UICONTROL Upgrade]** om een werkboek te bevorderen.

   >[!NOTE]
   >
   >U moet elk verzoek afzonderlijk bijwerken. Bulkupgrade wordt niet ondersteund.


1. Een waarschuwing lijkt dat alarm u aan veranderingen in het werkboek als u bevordert. Het dringt u ook aan om een steun van uw erfeniswerkboek tot stand te brengen alvorens te werk te gaan.

   ![ verbeteringswaarschuwing ](assets/upgrade_warning.png)

1. Klik op **[!UICONTROL Proceed]** om door te gaan met de upgrade.

   Als de upgrade is gelukt, wordt de volgende voltooiingskennisgeving weergegeven:

   ![ volledige verbetering ](assets/upgrade_complete.png)

1. (Optioneel) Klik op **[!UICONTROL Download upgrade report]** . Dit rapport bevat de status voor elk gegevensblok dat is bijgewerkt.

U kunt [ het gegevensblok ](/help/analyze/report-builder/manage-reportbuilder.md) nu beheren.


## Verouderde functies voor Report Builder worden niet ondersteund in de nieuwe Report Builder

Bij het vergelijken van de functionaliteit van verouderde Report Builder met de nieuwe Report Builder Add-in, is een deel van de oudere functionaliteit niet meer beschikbaar:

- Verzoeken in realtime

- Rapportage van pad/uitval

- FTP-optie voor geplande rapporten

- Metrische gegevens van bezoekers. De volgende meetgegevens worden allemaal omgezet in &quot;unieke bezoekers&quot;, ook al is het mogelijk dat het rapportresultaat geen exacte overeenkomst is: `visitorshourly`, `visitorsdaily`, `visitorsweekly`, `visitorsmonthly`, `visitorsquarterly` en `visitorsyearly` . Dit geldt ook voor `mobilevisitorshourly`, `mobilevisitorsdaily`, `mobilevisitorsweekly`, `mobilevisitorsmonthly`, `mobilevisitorsquarterly` en `mobilevisitorsyearly` .
