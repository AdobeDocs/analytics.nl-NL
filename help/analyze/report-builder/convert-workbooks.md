---
title: Verouderde Report Builder-werkboeken converteren
description: Begrijp hoe u uw oudere, op Report Builder gebaseerde werkboeken kunt omzetten voor gebruik van de nieuwe Report Builder.
role: User
feature: Report Builder
type: Documentation
solution: Analytics
exl-id: ff9011b2-fc18-456f-81dc-151b9e4fccd2
source-git-commit: 504cce24babdd8aefa5f819433139671904f2e1e
workflow-type: tm+mt
source-wordcount: '681'
ht-degree: 0%

---

# Oudere Report Builder-werkboeken converteren

Als deel van de beweging aan een nieuwe functionaliteit van Report Builder, kunt u uw huidige op oudere Report Builder gebaseerde werkboeken (erfeniswerkboeken) snel omzetten om de nieuwe Report Builder [ te gebruiken gegevenssloten ](create-a-data-block.md) functionaliteit.

>[!IMPORTANT]
>
>Dupliceer elk werkboek en noem één versie anders alvorens u het erfeniswerkboek omzet. Dat zorgt ervoor dat u altijd een exemplaar van het originele erfeniswerkboek hebt, als u het nodig hebt.


>[!BEGINSHADEBOX]

Zie ![ VideoCheckedOut ](/help/assets/icons/VideoCheckedOut.svg) [ werkboeken ](https://video.tv.adobe.com/v/3434957?quality=12&learn=on){target="_blank"} voor een demo video omzetten.

>[!ENDSHADEBOX]


>[!NOTE]
>
>Om erfeniswerkboeken om te zetten, moet u eerste [ opstelling nieuwe Report Builder ](/help/analyze/report-builder/report-builder-setup.md) hebben.


## Een verouderde werkmap openen

Om een erfeniswerkboek te openen, kunt u:

* Open een gepland erfeniswerkboek van het **[!UICONTROL Schedule]** lusje in de [ hub van Report Builder ](report-builder-hub.md). Dit is de aangewezen methode voor geplande erfeniswerkboeken. U krijgt de optie om het programma te gebruiken dat met het erfeniswerkboek wordt geassocieerd zodra u [ het omgezette erfeniswerkboek ](#schedule-a-converted-legacy-workbook) plant.

   1. Open Excel en selecteer ![ AdobeLogoRedonWhite ](/help/assets/icons/AdobeLogoRedOnWhite.svg) **[!UICONTROL Report Builder]** van de bar van het lint van Excel.

   1. Selecteer **[!UICONTROL Login]** en meld u aan bij Report Builder.

   1. Selecteer **[!UICONTROL Schedule]** in de [ hub van Report Builder ](report-builder-hub.md).
   1. Selecteer de tab **[!UICONTROL Legacy]** . Het tabblad bevat de oudere, op Report Builder gebaseerde, geplande werkboeken.

      ![ Verouderde werkbalken ](assets/upgrade-legacy-schedule.png)

   1. Selecteer ![ SelectBox ](/help/assets/icons/SelectBox.svg) het geplande werkboek dat u van de lijst wilt omzetten, en ![ Download ](/help/assets/icons/Download.svg) selecteren. Het werkboek wordt gedownload en opent in een nieuw venster in Excel. U kunt [ het werkboek van erfenisReport Builder ](#convert-a--workbook) nu omzetten.


* Open direct een erfeniswerkboek van uw lokale computer of netwerk. Wanneer u deze methode gebruikt, wordt u niet aangeboden om het programma te gebruiken dat met het erfeniswerkboek zou kunnen worden geassocieerd. <br/> wanneer het erfeniswerkboek in Excel open is:

   1. Selecteer ![ AdobeLogoRedonWhite ](/help/assets/icons/AdobeLogoRedOnWhite.svg) **[!UICONTROL Report Builder]** van de bar van het lint van Excel.
   1. Selecteer **[!UICONTROL Login]** en meld u aan bij Report Builder.
   1. Dan [ zet het erfeniswerkboek ](#convert-a-workbook) om.


## Een verouderde werkmap omzetten

Om uw erfeniswerkboek om te zetten:

1. Zodra u een erfeniswerkboek opent, ontdekt nieuwe Report Builder als dit werkboek [ verzoeken van de erfenisReport Builder ](/help/analyze/legacy-report-builder/home.md) bevat.

   {de herinnering van het 0} verbeteringswerkboek ![](assets/upgrade-workbook.png){zoomable="yes"}

1. Als een of meer verouderde aanvragen zijn gevonden, klikt u op **[!UICONTROL Upgrade]** in het dialoogvenster **[!UICONTROL Upgrade workbook]** om het werkboek bij te werken.

   >[!NOTE]
   >
   >U moet elk verzoek afzonderlijk bijwerken. Bulkupgrade wordt niet ondersteund.


1. Er verschijnt een dialoogvenster **[!UICONTROL Warning]** dat u waarschuwt voor wijzigingen in het werkboek als u een upgrade uitvoert. Het dringt u ook aan om een steun van uw erfeniswerkboek tot stand te brengen alvorens te werk te gaan.

   ![ verbeteringswaarschuwing ](assets/upgrade-warning.png){zoomable="yes"}

1. Klik op **[!UICONTROL Proceed]** om door te gaan met de upgrade.

   Als de upgrade is gelukt, verschijnt er een **[!UICONTROL The workbook upgrade is now completed]** -melding.

   ![ volledige verbetering ](assets/upgrade-complete.png)

   * Selecteer **[!UICONTROL Close]** om het bericht te sluiten en in het werkboek met bijgewerkte verzoeken voor nieuwe Report Builder te blijven werken.

   * Selecteer **[!UICONTROL Download upgrade report]** om een nieuw werkboek van Excel te downloaden en te openen dat het resultaat van de verbetering toont. Zie hieronder voor een voorbeeld.

     ![ het werkboek van het de verbeteringsrapport van Report Builder van Excel ](assets/upgrade-report.png)

U kunt nu [ de gegevensblokken ](/help/analyze/report-builder/manage-reportbuilder.md) in het werkboek beheren. Deze gegevensblokken zijn het resultaat van de upgrade en vervangen uw oudere Report Builder-aanvragen.


## Een omgezet werkboek plannen

U hebt de optie om de planningsdetails van het erfeniswerkboek te gebruiken dat u van het **[!UICONTROL Schedule]** lusje in de hub van Report Builder hebt gedownload en geopend. Deze optie is niet beschikbaar voor oudere werkboeken met planningsdetails die u van uw lokale computer of netwerk opent.

1. Om een omgezet erfeniswerkboek met een erfenisprogramma te plannen:

   * Selecteer **[!UICONTROL Send workbook]** in de Report Builder-hub, of
   * Selecteer **[!UICONTROL Schedule workbook]** op het tabblad **[!UICONTROL Workbooks]** dat beschikbaar is op het tabblad **[!UICONTROL Schedules]** in Report Builder.

1. U wordt aangeboden om de planningsdetails van het erfeniswerkboek als standaardplanningsmontages te gebruiken.

   ![ Migreer het programma van het erfeniswerkboek ](assets/upgrade-legacy-schedule-convert.png)

   * Selecteer **[!UICONTROL Use]** om de gegevens van het oudere programma te gebruiken. De planningsdetails zijn vooraf bevolkt in [ verzend werkboek ](schedule-reportbuilder.md#schedule-a-workbook) interface.
   * Selecteer **[!UICONTROL Don't use]** om de gegevens van het verouderde schema niet te gebruiken.
   * Selecteer **[!UICONTROL Cancel]** om te annuleren.

   Selecteer **[!UICONTROL Remove legacy metadata from future use]** om de gegevens van het erfenisprogramma voor dit werkboek in de toekomst niet te gebruiken.


## Verouderde Report Builder-functies worden niet ondersteund {#unsupported}

Sommige oudere Report Builder-functionaliteit is niet meer beschikbaar in de nieuwe Report Builder

* Verzoeken in realtime.

* Rapportage van pad/uitval.

* FTP-optie voor geplande rapporten.

* Metrische gegevens van bezoekers. De volgende metriek worden omgezet in *unieke bezoekers*, alhoewel het rapporteringsresultaat geen nauwkeurige gelijke kan zijn: `visitorshourly`, `visitorsdaily`, `visitorsweekly`, `visitorsmonthly`, `visitorsquarterly`, en `visitorsyearly`. Deze conversie is ook van toepassing op `mobilevisitorshourly` , `mobilevisitorsdaily` , `mobilevisitorsweekly` , `mobilevisitorsmonthly` , `mobilevisitorsquarterly` en `mobilevisitorsyearly` .
