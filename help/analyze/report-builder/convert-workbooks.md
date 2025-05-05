---
title: Hoe te om uw oudere werkboeken van de Report Builder in gegevensbestanden om te zetten
description: Beschrijft hoe uw erfenisverzoeken in gegevensbestanden omzetten
role: User
feature: Report Builder
type: Documentation
solution: Analytics
exl-id: ff9011b2-fc18-456f-81dc-151b9e4fccd2
source-git-commit: 08e29da4847e8ef70bd4435949e26265d770f557
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 0%

---

# Oudere werkboeken voor Reporten Builder converteren naar databases

Als deel van de beweging aan een nieuwe technologie van de Report Builder, kunt u uw huidige oudere werkboeken in op Java-Script-Gebaseerde werkboeken snel omzetten.

>[!IMPORTANT]
>
>Dupliceer elk werkboek en noem één versie anders alvorens u het omzet. Op die manier heb je nog steeds een kopie van het originele werkboek, mocht je het nodig hebben.


>[!BEGINSHADEBOX]

Zie ![ VideoCheckedOut ](/help/assets/icons/VideoCheckedOut.svg) [ werkboeken ](https://video.tv.adobe.com/v/3446188?quality=12&learn=on&captions=dut){target="_blank"} voor een demo video omzetten.

>[!ENDSHADEBOX]



1. Opstelling de nieuwe Report Builder door [ na deze instructies ](/help/analyze/report-builder/report-builder-setup.md).

1. Open Excel en klik op het Adobe Report Builder-pictogram rechtsboven.

1. Klik op **[!UICONTROL Login]** en meld u aan bij de Report Builder.

1. De Report Builder toe:voegen-binnen ontdekt als dit werkboek [&#128279;](/help/analyze/legacy-report-builder/home.md) verzoeken van de Report Builder van de Verouderde 1&rbrace; bevat.

   {de herinnering van het 0} verbeteringswerkboek ![&#128279;](assets/upgrade_workbook.png)

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


## Verouderde functies voor Report Builder worden niet ondersteund in de nieuwe Report Builder {#unsupported}

Bij het vergelijken van de functionaliteit van verouderde Report Builder met de nieuwe Report Builder Add-in, is een deel van de oudere functionaliteit niet meer beschikbaar:

- Verzoeken in realtime

- Rapportage van pad/uitval

- FTP-optie voor geplande rapporten

- Metrische gegevens van bezoekers. De volgende meetgegevens worden allemaal omgezet in &quot;unieke bezoekers&quot;, ook al is het mogelijk dat het rapportresultaat geen exacte overeenkomst is: `visitorshourly`, `visitorsdaily`, `visitorsweekly`, `visitorsmonthly`, `visitorsquarterly` en `visitorsyearly` . Dit geldt ook voor `mobilevisitorshourly`, `mobilevisitorsdaily`, `mobilevisitorsweekly`, `mobilevisitorsmonthly`, `mobilevisitorsquarterly` en `mobilevisitorsyearly` .

## Een omgezet werkboek plannen {#schedule}

Zie [ Plan een omgezet werkboek ](/help/analyze/report-builder/schedule-reportbuilder.md) in het plannen artikel.