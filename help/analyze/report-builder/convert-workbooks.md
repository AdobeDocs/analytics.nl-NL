---
title: Verouderde Report Builder-werkboeken converteren
description: Leer hoe u oudere Report Builder-werkboeken kunt migreren en converteren naar de nieuwe Report Builder. Volg de stapsgewijze instructies in deze migratiegids over hoe u uw op Adobe Analytics gebaseerde werkboeken naadloos kunt converteren.
role: User
feature: Report Builder
type: Documentation
solution: Analytics
exl-id: ff9011b2-fc18-456f-81dc-151b9e4fccd2
source-git-commit: 9743d7ac2a6c7e63d7a6701e60d05683c5680d36
workflow-type: tm+mt
source-wordcount: '1096'
ht-degree: 0%

---

# Oudere Report Builder-werkboeken converteren

De nalatenschap Report Builder is in juni 2026 aan het einde van de levensduur. U moet uw werkboeken migreren van de oude Report Builder naar de nieuwe Report Builder. De nieuwe Report Builder biedt een handige manier om snel werkboeken te migreren die zijn gemaakt met de oudere Report Builder.

>[!IMPORTANT]
>
>Dupliceer elk werkboek en noem één versie anders alvorens u het erfeniswerkboek omzet. Dat zorgt ervoor dat u altijd een exemplaar van het originele erfeniswerkboek hebt, als u het nodig hebt.


>[!BEGINSHADEBOX]

Zie ![&#x200B; VideoCheckedOut &#x200B;](/help/assets/icons/VideoCheckedOut.svg) [&#x200B; werkboeken &#x200B;](https://experienceleague.adobe.com/nl/docs/analytics-learn/tutorials/exporting/report-builder/upgrade-and-reschedule-workbooks){target="_blank"} voor een demo video omzetten.

>[!ENDSHADEBOX]


>[!NOTE]
>
>Om erfeniswerkboeken om te zetten, moet u eerste [&#x200B; opstelling nieuwe Report Builder &#x200B;](/help/analyze/report-builder/report-builder-setup.md) hebben.


## Een verouderde werkmap openen

Om een erfeniswerkboek te openen, kunt u:

* Open een gepland erfeniswerkboek van het **[!UICONTROL Schedule]** lusje in de [&#x200B; hub van Report Builder &#x200B;](report-builder-hub.md). Deze actie is de aangewezen methode voor geplande erfeniswerkboeken. U krijgt de optie om het programma te gebruiken dat met het erfeniswerkboek wordt geassocieerd zodra u [&#x200B; het omgezette erfeniswerkboek &#x200B;](#schedule-a-converted-legacy-workbook) plant.

   1. Open [!DNL Excel] en selecteer ![&#x200B; AdobeLogoRedonWhite &#x200B;](/help/assets/icons/AdobeLogoRedOnWhite.svg) **[!UICONTROL Report Builder]** van de [!DNL Excel] lintbar.

   1. Selecteer **[!UICONTROL Login]** en meld u aan bij Report Builder.

   1. Selecteer **[!UICONTROL Schedule]** in de [&#x200B; hub van Report Builder &#x200B;](report-builder-hub.md).
   1. Selecteer de tab **[!UICONTROL Legacy]** . Het tabblad bevat de oudere, op Report Builder gebaseerde, geplande werkboeken die u hebt gemaakt.

      ![&#x200B; Verouderde werkbalken &#x200B;](assets/upgrade-legacy-schedule.png)

   1. Selecteer ![&#x200B; SelectBox &#x200B;](/help/assets/icons/SelectBox.svg) het geplande werkboek dat u van de lijst wilt omzetten, en ![&#x200B; Download &#x200B;](/help/assets/icons/Download.svg) selecteren. Het werkboek wordt gedownload en in een nieuw venster in [!DNL Excel] geopend. U kunt [&#x200B; het werkboek van erfenisReport Builder &#x200B;](#convert-a--workbook) nu omzetten.


* Open direct een erfeniswerkboek van uw lokale computer of netwerk. Wanneer u deze methode gebruikt, wordt u niet aangeboden om het programma te gebruiken dat met het erfeniswerkboek zou kunnen worden geassocieerd. <br/> wanneer het erfeniswerkboek in [!DNL Excel] open is:

   1. Selecteer ![&#x200B; AdobeLogoRedOnWhite &#x200B;](/help/assets/icons/AdobeLogoRedOnWhite.svg) **[!UICONTROL Report Builder]** van de [!DNL Excel] lintbar.
   1. Selecteer **[!UICONTROL Login]** en meld u aan bij Report Builder.
   1. Dan [&#x200B; zet het erfeniswerkboek &#x200B;](#convert-a-workbook) om.


## Een verouderde werkmap omzetten

Om uw erfeniswerkboek om te zetten:

1. Zodra u een erfeniswerkboek opent, ontdekt nieuwe Report Builder als dit werkboek [&#x200B; verzoeken van de erfenisReport Builder &#x200B;](/help/analyze/legacy-report-builder/home.md) bevat.

   ![&#x200B; Schermafbeelding van het [!DNL Excel] Report Builder verbeteringsrapport dat migratieverbetering &#x200B;](assets/upgrade-workbook.png){zoomable="yes"} toont

1. Als een of meer verouderde aanvragen zijn gevonden, klikt u op **[!UICONTROL Upgrade]** in het dialoogvenster **[!UICONTROL Upgrade workbook]** om het werkboek bij te werken.

   >[!NOTE]
   >
   >U moet elk verzoek afzonderlijk bijwerken. Bulkupgrade wordt niet ondersteund.


1. Er verschijnt een dialoogvenster **[!UICONTROL Warning]** dat u waarschuwt voor wijzigingen in het werkboek als u een upgrade uitvoert. Het dringt u ook aan om een steun van uw erfeniswerkboek tot stand te brengen alvorens te werk te gaan.

   ![&#x200B; Schermafbeelding van het [!DNL Excel] Report Builder verbeteringsrapport dat migratiewaarschuwing &#x200B;](assets/upgrade-warning.png){zoomable="yes"} toont

1. Klik op **[!UICONTROL Proceed]** om door te gaan met de upgrade.

   Als de upgrade is gelukt, verschijnt er een **[!UICONTROL The workbook upgrade is now completed]** -melding.

   ![&#x200B; Schermafbeelding van het [!DNL Excel] Report Builder verbeteringsrapport dat voltooide migratie toont &#x200B;](assets/upgrade-complete.png)

   * Selecteer **[!UICONTROL Close]** om het bericht te sluiten en in het werkboek met bijgewerkte verzoeken voor nieuwe Report Builder te blijven werken.

   * Selecteer **[!UICONTROL Download upgrade report]** om een nieuw [!DNL Excel] werkboek te downloaden en te openen dat het resultaat van de verbetering toont. Zie hieronder voor een voorbeeld.

     ![&#x200B; Schermafbeelding van het [!DNL Excel] Report Builder verbeteringsrapport dat migratierapport toont &#x200B;](assets/upgrade-report.png)

U kunt nu [&#x200B; de gegevensblokken &#x200B;](/help/analyze/report-builder/manage-reportbuilder.md) in het werkboek beheren. Deze gegevensblokken zijn het resultaat van de upgrade en vervangen uw oudere Report Builder-aanvragen.


## Een omgezet werkboek plannen

U hebt de optie om de planningsdetails van het erfeniswerkboek te gebruiken dat u van het **[!UICONTROL Schedule]** lusje in de hub van Report Builder hebt gedownload en geopend. Deze optie is niet beschikbaar voor oudere werkboeken met planningsdetails die u van uw lokale computer of netwerk opent.

1. Om een omgezet erfeniswerkboek met een erfenisprogramma te plannen:

   * Selecteer **[!UICONTROL Send workbook]** in de Report Builder-hub, of
   * Selecteer **[!UICONTROL Schedule workbook]** op het tabblad **[!UICONTROL Workbooks]** dat beschikbaar is op het tabblad **[!UICONTROL Schedules]** in Report Builder.

1. U wordt aangeboden om de planningsdetails van het erfeniswerkboek als standaardplanningsmontages te gebruiken.

   ![&#x200B; Schermafbeelding van de [!DNL Excel] opties van de de erfenisplanningsmontages van Report Builder &#x200B;](assets/upgrade-legacy-schedule-convert.png)

   * Selecteer **[!UICONTROL Use]** om de gegevens van het oudere programma te gebruiken. De planningsdetails zijn vooraf bevolkt in [&#x200B; verzend werkboek &#x200B;](schedule-reportbuilder.md#schedule-a-workbook) interface.
   * Selecteer **[!UICONTROL Don't use]** om de gegevens van het verouderde schema niet te gebruiken.
   * Selecteer **[!UICONTROL Cancel]** om te annuleren.

   Selecteer **[!UICONTROL Remove legacy metadata from future use]** om de gegevens van het erfenisprogramma voor dit werkboek in de toekomst niet te gebruiken.


## Migreren vanuit Report Builder

Sommige functies van de oudere Report Builder worden niet ondersteund, gedeeltelijk ondersteund of op een andere manier geïmplementeerd in Report Builder:

* **verzoeken in real time**. Verzoeken in real time worden niet gesteund en worden verwijderd uit het omgezette erfeniswerkboek.

* **Weg/Fallout rapporterend**. De verzoeken van de val-uit worden niet gesteund en worden verwijderd uit het omgezette erfeniswerkboek.

* **[!DNL FTP]optie voor geplande rapporten**. De optie om rapporten naar een [!DNL FTP] -locatie te plannen is niet meer beschikbaar.

* **publiceer werkboek aan [!DNL Power BI] optie voor geplande rapporten**. De optie om rapporten naar [!DNL Power BI] te plannen is niet meer beschikbaar.

* **de metriek van Bezoekers**. De volgende metriek worden omgezet in *unieke bezoekers* in het omgezette erfeniswerkboek, alhoewel het rapporteringsresultaat geen nauwkeurige gelijke kan zijn: `visitorshourly`, `visitorsdaily`, `visitorsweekly`, `visitorsmonthly`, `visitorsquarterly`, en `visitorsyearly`. Deze conversie is ook van toepassing op `mobilevisitorshourly` , `mobilevisitorsdaily` , `mobilevisitorsweekly` , `mobilevisitorsmonthly` , `mobilevisitorsquarterly` en `mobilevisitorsyearly` .

* **automatische re-authentificatie**. Wanneer u een nieuw [!DNL Excel] bestand opent, moet u dit expliciet opnieuw verifiëren. Deze herverificatie is een beveiligingsfunctie van de [!DNL Office Add-ins] -functionaliteit.

* **Kopieer een aantekenvel met een groep gegevensblokken**. Ondersteuning voor de kopie van een werkblad dat meerdere gegevensblokken bevat:

   1. Selecteer het werkbladlusje in het [!DNL Excel] werkboek dat u wilt kopiëren.
   1. Selecteer in het contextmenu van de tab **[!UICONTROL Move or Copy...]**
   1. In het dialoogvenster **[!UICONTROL Move or Copy]** :
      1. Selecteer waarnaar u het gekopieerde werkblad wilt kopiëren.
      1. Zorg ervoor dat u **[!UICONTROL Create a copy]** inschakelt.
      1. Selecteer **[!UICONTROL OK]**.
   1. Vanuit het bronwerkblad:
      1. Selecteer het celbereik dat alle gegevensblokken omvat.
      1. Selecteer ![&#x200B; Exemplaar &#x200B;](/help/assets/icons/Copy.svg) **[!UICONTROL Copy data block]** van de [&#x200B; hub van Report Builder &#x200B;](/help/analyze/report-builder/report-builder-hub.md).
   1. In het doelwerkblad:
      1. Selecteer de cel waarin u het gekopieerde celbereik wilt plakken.
      1. Selecteer ![&#x200B; Deeg &#x200B;](/help/assets/icons/Paste.svg) **[!UICONTROL Paste data block]** van de [&#x200B; hub van Report Builder &#x200B;](/help/analyze/report-builder/report-builder-hub.md).

* **waaier van de Datum**. Report Builder migreert niet de opmaakopties voor het datumbereik **[!UICONTROL Show start and end period as]** die zijn toegepast op een rijlabel voor een datumbereik in de verouderde Report Builder.

* **Gemiddelde**. Report Builder migreert de geselecteerde opmaakoptie **[!UICONTROL Average options]** ( **[!UICONTROL Daily Average]** tot **[!UICONTROL Yearly Average]** ) die op metrische gegevens in de verouderde Report Builder is toegepast niet. Gebruik een berekende metrische waarde om de geselecteerde optie te vervangen.

* **prepend/stel tekst** uit. Report Builder migreert niet de **[!UICONTROL Prepend/postpend text]** die wordt toegepast op een metrische waarde in de verouderde Report Builder.

* **Subtotals**. Report Builder migreert niet de opmaakoptie **[!UICONTROL SubTotal(this request)]** die wordt toegepast op een metrische waarde in de verouderde Report Builder. Wanneer u **[!UICONTROL SubTotal(this request)]** in een aanvraag voor een verouderd werkboek hebt gebruikt, wordt de functionaliteit omgezet in **[!UICONTROL Total]** . Bijvoorbeeld: in een verouderd gegevensblok met de namen van de bovenste vijf pagina&#39;s waarin u **[!UICONTROL SubTotal(Page Views)]** hebt gebruikt om de som van de paginaweergaven voor de namen van de bovenste vijf pagina&#39;s te retourneren. Na migratie, keert het zelfde gegevensblok met top 5 paginanamen de som paginameningen voor *alle* paginanamen terug. Gebruik de berekende metriefunctionaliteit om de verouderde **[!UICONTROL SubTotal]** functionaliteit te vervangen.
