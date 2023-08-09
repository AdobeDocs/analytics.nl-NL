---
description: Gebruik Report Builder met Microsoft-Power BI.
title: Publiceren naar Power BI - overzicht
feature: Report Builder
role: User, Admin
exl-id: 3464c153-2db5-41af-9e83-da081ec64ad3
source-git-commit: fb39f906d6c08713e4dc8211c917b2942502868e
workflow-type: tm+mt
source-wordcount: '1102'
ht-degree: 6%

---

# Publiceren naar Power BI - overzicht

Microsoft Power BI is een suite van bedrijfsanalytische dashboards om data te analyseren en inzichten te delen. Dankzij de integratie van Adobe Analytics met Power BI kunt u de analytische data van Report Builder visualiseren in Microsoft Power BI en deze eenvoudig delen in uw organisatie.

Als analist, eerder zou u Report Builder werkboekdistributie gebruikend e-mail of FTP plannen. Nu kunt u uw bedrijfs belanghebbenden toegang geven van binnen hun rekeningen, tot nauwkeurige en bijgewerkte gegevens in een Web-based milieu dat over platforms en apparaten toegankelijk is.

De combinatie van het rapportgenererende vermogen van Report Builder met de visualisatiefuncties van Power BI maakt informatie toegankelijker voor iedereen in uw organisatie. Met Power BI, kunt u Adobe Analytics met andere gegevensbronnen, bijvoorbeeld, verkooppunt, of bronnen van CRM ook integreren, om unieke klanteninzichten, verenigingen, en kansen te ontdekken.

![Diagram van het Microsoft Power BI plus het Adobe Analytics pictogram.](assets/aaplusbi.png)

## Systeemvereisten {#section_0B71092D853446F38FA36447DAC0D32B}

* Adobe Report Builder 5.5 [geïnstalleerd](/help/analyze/report-builder/setup/t-install-arb.md)
* Active Microsoft-account waarmee u zich kunt aanmelden bij Power BI

## Werkmap publiceren naar Power BI {#section_21CA66229EC240D49594A9A7D3FBA687}

De geplande werkboeken zijn geformatteerde spreadsheets van Excel die met gegevens van Adobe Analytics worden bevolkt die op een regelmatig geplande basis worden verdeeld.

**Werkmap publiceren in Report Builder**

1. In Report Builder, produceer en bewaar een werkboek.
1. Klik op de werkbalk Report Builder op **[!UICONTROL Schedule]** > **[!UICONTROL New]**.

1. In de Basis plannende Tovenaar, controleer het vakje naast **[!UICONTROL Publish Workbook to Microsoft Power BI]**.

   ![Screenshot van de Report Builder Scheduling Wizard met de optie om de Power BI Publish Workbook to Microsoft te controleren.](assets/simple-schedule-wizard.png)

1. Geef uw e-mail op en verzend deze direct of geef de planningsfrequentie op (per uur, per dag, enz.).
1. Klikken **[!UICONTROL OK]** publiceren.
1. U wordt nu gevraagd u aan te melden bij uw Microsoft-account. Geef uw gegevens op.
1. Het werkboek van Report Builder wordt gepland en aan Power BI gepubliceerd.

   Met elke geplande instantie, en nadat Report Builder het plannen proces het werkboek met bijgewerkte gegevens van Analytics heeft verfrist, zal het werkboek aan de Power BI van Microsoft worden gepubliceerd.

**De werkboekgegevens van Report Builder weergeven in Power BI**

1. In Power BI, klik het werkboek onder het werkboek tweemaal [!UICONTROL Workbooks] -menu.

   ![Screenshot van weergave van Power BI Workbooks.](assets/workbooks-power-bi.png)

1. U kunt de werkboekdashboardgegevens nu bekijken.  ![De werkboekdashboardgegevens.](assets/view-data-pbi.png)

1. U kunt dan een gebied van dit werkboek vastzetten om het in om het even welk van uw dashboards van Power BI te omvatten.

## Alle opgemaakte tabellen in het werkboek publiceren als Power BI-datasettabellen {#section_7C54A54E75184DD6BAEF4ACCE241239A}

>[!NOTE]
>
>Als het werkboek een macro bevat, zal &quot;publiceren Alle Formatted Lijsten in het Werkboek als Lijsten van de Dataset van de Power BI&quot;worden onbruikbaar gemaakt.

In plaats van het invoeren van het volledige werkboek, kunt u slechts de inhoud van alle geformatteerde lijsten binnen het werkboek invoeren.

**Hoofdletters gebruiken**: U hebt een werkboek van Excel dat gegevens van veelvoudige verzoeken van Report Builder trekt en tot een summiere lijst met vele formules leidt. U kunt alleen de overzichtstabel importeren in Power BI en er een visualisatie voor maken.

**Een opgemaakte tabel in Report Builder publiceren**

1. Bij Report Builder genereert u een tabel met gegevens die een koptekstrij bevat, gevolgd door een gegevensrij.
1. Selecteer de tabel en selecteer **[!UICONTROL Format as Table]** van de [!UICONTROL Home] -menu. De tabel krijgt standaard een naam (Tabel 1, Tabel 2, enzovoort), maar u kunt de naam wijzigen op het tabblad [!UICONTROL Design]-menu.

1. Klik op de werkbalk Report Builder op **[!UICONTROL Schedule]** > **[!UICONTROL New]**.

1. Klik in de wizard Standaard plannen op **[!UICONTROL Advanced Scheduling Options]**.
1. In de [!UICONTROL Scheduling Wizard - Advanced], over de **[!UICONTROL Publishing Options]** tabblad, schakelt u het vakje naast **[!UICONTROL Publish all Formatted Tables as Power BI dataset tables]**.

   ![Screenshot die de Plannende Tovenaar toont - Geavanceerde het Publiceren Opties met Publish alle Formatted Lijsten als Power BI datasetlijsten.](assets/advanced-schedule-wizard2.png)

1. (Optioneel) U kunt de naam van het gepubliceerde element in Power BI aanpassen. Dit kan nuttig zijn als u versioning als deel van de werkboeknaam (b.v., mijnwerkboek_v1.1.xlsx) gebruikt en u niet het versieaantal in de naam van de gepubliceerde activa van de Power BI wilt tonen. Het heeft het toegevoegde voordeel dat het gepubliceerde element niet verandert als het versienummer verandert. (Weergave [specificaties](/help/analyze/report-builder/c-publish-power-bi/specifications-limits.md) hier.)

**Tabelgegevens weergeven in Power BI**

1. Ga in Power BI naar de **[!UICONTROL Workspaces]** > **[!UICONTROL Datasets]** -menu.

   ![Screenshot met de markering van het menu Datasets van Power BI. Rapporten maken.](assets/datasets-menu.png)

1. Selecteer de gegevensset die u hebt gepubliceerd en klik op [!UICONTROL Create report] naast het pictogram. De tabellen worden weergegeven als velden.

   ![Screenshot met geselecteerde gepubliceerde dataset die de tabellen als velden vermeldt.](assets/formatted-tables.png)

1. Selecteer een tabel en de bijbehorende kolommen.

   ![Screenshot met een geselecteerde tabel met de bijbehorende kolommen](assets/view-table-dataset.png)

1. Van de [!UICONTROL Visualizations] kunt u selecteren hoe u een tabel in Power BI visualiseert. U kunt er bijvoorbeeld voor kiezen uw gegevens als een lijngrafiek weer te geven:

   ![Screenshot met het menu Visualisaties en een grafiek van de gegevenslijn.](assets/bi-line-graph.png)

1. Van hier, kunt u visualisaties van deze datasetlijst tot stand brengen.

## Alle Report Builder-aanvragen publiceren als Power BI Dataset-tabellen {#section_0C26057C7DBB4068A643FDD688F6E463}

U kunt al uw verzoeken in datasetlijsten veranderen en visualisaties bovenop hen bouwen.

>[!IMPORTANT]
>
>Als het werkboek meer dan 100 verzoeken bevat, slechts zullen de eerste 100 verzoeken aan Power BI worden gepubliceerd. Plus, voor elke verzoeken die aan Power BI worden gepubliceerd, slechts zullen de eerste 10.000 rijen van gegevens worden gepubliceerd. Hoewel deze verzoeken via planning met succes worden geleverd, is het bereik van publicatie naar Power BI beperkt.

1. In Report Builder, open of creeer een werkboek met de verzoeken van Report Builder.
1. Klik op de werkbalk Report Builder op **[!UICONTROL Schedule]** > **[!UICONTROL New]**.

1. Klik in de wizard Standaard plannen op **[!UICONTROL Advanced Scheduling Options]**.
1. In de [!UICONTROL Scheduling Wizard - Advanced], over de **[!UICONTROL Publishing Options]** tabblad, schakelt u het vakje naast **[!UICONTROL Publish all Report Builder Requests as Power BI Dataset Tables]** ![Screenshot die de Plannende Tovenaar toont die Publish alle Verzoeken van de Report Builder als optie van de Lijsten van de Dataset van de Power BI benadrukt.](assets/advanced-schedule-wizard2.png)

1. Klik op **[!UICONTROL OK]**.

**De aanvraaggegevens in Power BI weergeven**

Elk gepland Report Builder verzoek zal als lijst in de dataset worden gepubliceerd. Elke verzoeklijst wordt genoemd na de primaire dimensie in het verzoek en het heeft een [!UICONTROL Report Suite] en [!UICONTROL Segments] kolom.

1. Ga in Power BI naar de **[!UICONTROL Workspaces]** > **[!UICONTROL Datasets]** -menu.

1. Selecteer de aanvraag die u hebt gepubliceerd en klik op de knop [!UICONTROL Create report] naast het pictogram.

   De aanvragen worden weergegeven als tabellen in het dialoogvenster [!UICONTROL Fields] -menu.

   ![Screenshot met een geselecteerde aanvraag die is gepubliceerd in een tweeledige indeling voor één koptekstrij.](assets/published-requests.png)

   >[!NOTE]
   >
   >Ongeacht hoe u uw verzoek van de Report Builder om op het aantekenvel (spillay-out, douanelay-out, sommige onzichtbare kolommen) vormde worden geplaatst, zal Report Builder altijd uw verzoek in het zelfde tweedimensionale, enige formaat van de kopbalrij publiceren: Datum, Dimension, Metriek, de Reeksen van het Rapport, Segmenten.

1. Merk ook op dat er een extra lijst geroepen is **[!UICONTROL Legend]**. Als u een verzoek uit de context van de Report Builder neemt, kan het moeilijk zijn om te herinneren wat elk verzoek voor staat. Het doel van de Legende lijst is, bijvoorbeeld, om u de naam van elk verzoek onder Lijst ID te tonen. U kunt ook de andere Legend-kolommen toevoegen voor een volledige weergave van het verzoek.

   ![Screenshot met de Legend-tabel met de naam van elke aanvraag onder Tabel-id.](assets/legend-table.png)
