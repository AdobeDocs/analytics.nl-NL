---
description: Gebruik Report Builder met Microsoft-Power BI.
title: Publiceren naar Power BI - overzicht
feature: Report Builder
role: User, Admin
exl-id: 3464c153-2db5-41af-9e83-da081ec64ad3
source-git-commit: 1ee50c6a2231795b2ad0015a79e09b7c1c74d850
workflow-type: tm+mt
source-wordcount: '957'
ht-degree: 13%

---

# Publiceren naar Power BI - overzicht

Microsoft Power BI is een suite van bedrijfsanalytische dashboards om data te analyseren en inzichten te delen. Dankzij de integratie van Adobe Analytics met Power BI kunt u de analytische data van Report Builder visualiseren in Microsoft Power BI en deze eenvoudig delen in uw organisatie.

Vroeger moest u als analist plannen dat de Report Builder-werkmappen via e-mail (of FTP) werden verspreid. Nu kunt u uw zakelijke belanghebbende gebruikers toegang geven (vanuit hun Power BI-account) tot nauwkeurige en actuele data in een webomgeving die toegankelijk is voor verschillende platforms en apparaten.

De combinatie van het rapportgenererende vermogen van Report Builder met de visualisatiefuncties van Power BI maakt informatie toegankelijker voor iedereen in uw organisatie. Met Power BI, kunt u Adobe Analytics met andere gegevensbronnen (b.v. verkooppunt, CRM) ook integreren om unieke klanteninzichten, verenigingen, en kansen te ontdekken.

![](assets/aaplusbi.png)

## Systeemvereisten {#section_0B71092D853446F38FA36447DAC0D32B}

* Adobe Report Builder 5.5 [geïnstalleerd](/help/analyze/report-builder/setup/t-install-arb.md)
* Active Microsoft-account waarmee u zich kunt aanmelden bij Power BI

## Werkmap publiceren naar Power BI {#section_21CA66229EC240D49594A9A7D3FBA687}

De geplande werkboeken zijn geformatteerde spreadsheets van Excel gevuld met gegevens van Adobe Analytics en verzonden op een regelmatig geplande basis.

**Werkmap publiceren in Report Builder**

1. In Report Builder, produceer en bewaar een werkboek.
1. Klik op de werkbalk Report Builder op **[!UICONTROL Schedule]** > **[!UICONTROL New]**.

1. In de Basis plannende Tovenaar, controleer het vakje naast **[!UICONTROL Publish Workbook to Microsoft Power BI]**.

   ![](assets/simple-schedule-wizard.png)

1. Geef uw e-mail op en verzend deze direct of geef de planningsfrequentie op (per uur, per dag, enz.).
1. Klikken **[!UICONTROL OK]** om te publiceren.
1. U wordt nu gevraagd u aan te melden bij uw Microsoft-account. Geef uw gegevens op.
1. Het werkboek van Report Builder wordt gepland en aan Power BI gepubliceerd.

   Met elke geplande instantie, en nadat Report Builder het plannen proces het werkboek met bijgewerkte gegevens van Analytics heeft verfrist, zal het werkboek aan de Power BI van Microsoft worden gepubliceerd.

**De werkboekgegevens van Report Builder weergeven in Power BI**

1. In Power BI, klik het werkboek onder het werkboek tweemaal [!UICONTROL Workbooks] -menu.

   ![](assets/workbooks-power-bi.png)

1. U kunt de werkboekdashboardgegevens nu bekijken.  ![](assets/view-data-pbi.png)

1. U kunt dan een gebied van dit werkboek vastzetten om het in om het even welk van uw dashboards van Power BI te omvatten.

## Alle opgemaakte tabellen in het werkboek publiceren als Power BI-datasettabellen {#section_7C54A54E75184DD6BAEF4ACCE241239A}

>[!NOTE]
>
>Als het werkboek een macro bevat, zal &quot;publiceren Alle Formatted Lijsten in het Werkboek als Lijsten van de Dataset van de Power BI&quot;worden onbruikbaar gemaakt.

In plaats van het invoeren van het volledige werkboek, kunt u slechts de inhoud van alle geformatteerde lijsten binnen het werkboek invoeren.

**Hoofdletters gebruiken**: U hebt een werkboek van Excel dat gegevens van veelvoudige verzoeken van Report Builder trekt en tot een summiere lijst met veel formules leidt. U kunt alleen de overzichtstabel importeren in Power BI en er een visualisatie voor maken.

**Een opgemaakte tabel in Report Builder publiceren**

1. Bij Report Builder genereert u een tabel met gegevens die een koptekstrij bevat, gevolgd door een gegevensrij.
1. Selecteer de tabel en selecteer **[!UICONTROL Format as Table]** van de [!UICONTROL Home] -menu. De tabel krijgt standaard een naam (Tabel 1, Tabel 2, enzovoort), maar u kunt de naam wijzigen op het tabblad [!UICONTROL Design]-menu.

1. Klik op de werkbalk Report Builder op **[!UICONTROL Schedule]** > **[!UICONTROL New]**.

1. Klik in de wizard Standaard plannen op **[!UICONTROL Advanced Scheduling Options]**.
1. In de [!UICONTROL Scheduling Wizard - Advanced]over de **[!UICONTROL Publishing Options]** tabblad, schakelt u het vakje naast **[!UICONTROL Publish all Formatted Tables as Power BI dataset tables]**.

   ![](assets/advanced-schedule-wizard2.png)

1. (Optioneel) U kunt de naam van het gepubliceerde element in Power BI aanpassen. Dit kan nuttig zijn als u versioning als deel van de werkboeknaam (b.v., mijnwerkboek_v1.1.xlsx) gebruikt en u niet het versieaantal in de naam van de gepubliceerde activa van de Power BI wilt tonen. Het heeft het toegevoegde voordeel dat het gepubliceerde element niet verandert als het versienummer verandert. (Weergave [specificaties](/help/analyze/report-builder/c-publish-power-bi/specifications-limits.md) hier.)

**Tabelgegevens weergeven in Power BI**

1. Ga in Power BI naar de **[!UICONTROL Workspaces]** > **[!UICONTROL Datasets]** -menu.

   ![](assets/datasets-menu.png)

1. Selecteer de gegevensset die u hebt gepubliceerd en klik op de knop [!UICONTROL Create report] naast het pictogram. De tabellen worden weergegeven als velden.

   ![](assets/formatted-tables.png)

1. Selecteer een tabel en de bijbehorende kolommen.

   ![](assets/view-table-dataset.png)

1. Van de [!UICONTROL Visualizations] kunt u selecteren hoe u een tabel in Power BI visualiseert. U kunt er bijvoorbeeld voor kiezen uw gegevens als een lijngrafiek weer te geven:

   ![](assets/bi-line-graph.png)

1. Van hier, kunt u visualisaties van deze datasetlijst tot stand brengen.

## Alle Report Builder-aanvragen publiceren als Power BI Dataset-tabellen {#section_0C26057C7DBB4068A643FDD688F6E463}

U kunt al uw verzoeken in datasetlijsten veranderen en visualisaties bovenop hen bouwen.

>[!IMPORTANT]
>
>Als het werkboek meer dan 100 verzoeken bevat, slechts zullen de eerste 100 verzoeken aan Power BI worden gepubliceerd. Plus, voor elke verzoeken die aan Power BI worden gepubliceerd, slechts zullen de eerste 10.000 rijen van gegevens worden gepubliceerd. Hoewel deze verzoeken via planning met succes worden geleverd, is het bereik van publicatie naar Power BI beperkt.

1. In Report Builder, open of creeer een werkboek met de verzoeken van Report Builder.
1. Klik op de werkbalk Report Builder op **[!UICONTROL Schedule]** > **[!UICONTROL New]**.

1. Klik in de wizard Standaard plannen op **[!UICONTROL Advanced Scheduling Options]**.
1. In de [!UICONTROL Scheduling Wizard - Advanced]over de **[!UICONTROL Publishing Options]** tabblad, schakelt u het vakje naast **[!UICONTROL Publish all Report Builder Requests as Power BI Dataset Tables]** ![](assets/advanced-schedule-wizard2.png)

1. Klik op **[!UICONTROL OK]**.

**De aanvraaggegevens in Power BI weergeven**

Elk gepland Report Builder verzoek zal als lijst in de dataset worden gepubliceerd. Elke verzoeklijst wordt genoemd na de primaire dimensie in het verzoek en het heeft een [!UICONTROL Report Suite] en [!UICONTROL Segments] kolom.

1. Ga in Power BI naar de **[!UICONTROL Workspaces]** > **[!UICONTROL Datasets]** -menu.

1. Selecteer de aanvraag die u hebt gepubliceerd en klik op de knop [!UICONTROL Create report] naast het pictogram.

   De aanvragen worden weergegeven als tabellen in de [!UICONTROL Fields] -menu.

   ![](assets/published-requests.png)

   >[!NOTE]
   >
   >Ongeacht hoe u uw verzoek van de Report Builder om op het aantekenvel (spillay-out, douanelay-out, sommige onzichtbare kolommen) vormde worden geplaatst, zal Report Builder altijd uw verzoek in het zelfde tweedimensionale, enige formaat van de koptekstrij publiceren: Datum, Dimension, Metriek, Rapporten, Segmenten.

1. Merk ook op dat er een extra lijst geroepen is **[!UICONTROL Legend]**. Als u een verzoek uit de context van de Report Builder neemt, kan het moeilijk zijn om te herinneren wat elk verzoek voor staat. Het doel van de Legende lijst is, bijvoorbeeld, om u de naam van elk verzoek onder Lijst ID te tonen. U kunt ook de andere Legend-kolommen toevoegen voor een volledige weergave van het verzoek.

   ![](assets/legend-table.png)
