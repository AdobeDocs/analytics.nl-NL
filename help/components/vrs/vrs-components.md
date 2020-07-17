---
description: Virtuele rapportsuites kunnen worden gebogen om components.in Analysis Workspace op te nemen en uit te sluiten.
title: Onderdeelselectie voor virtuele rapportsuites
uuid: 6c6a4071-22ad-4e8c-b1ed-140b2aa04f76
translation-type: tm+mt
source-git-commit: 4c5dd32b51693d2c0eccd4365cae1ac5a29e6d34
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 14%

---


# Onderdeelselectie voor virtuele rapportsuites

Virtuele rapportsuites kunnen worden gebogen om components.in Analysis Workspace op te nemen en uit te sluiten.

>[!NOTE]
>
>Er zijn wijzigingen aangebracht in welke componenten door beheerders en niet-beheerders kunnen worden bekeken in gecureerde Workspace-projecten en gecureerde virtuele rapportsuites (VRS&#39;s). Previously, anyone could see non-curated components by clicking **[!UICONTROL Show all Components]**. The [updated curation experience](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/curate-share/curate-projects-vrs.html) allows for more fine-grained control over which components are visible.

U kunt als volgt componentcuratie inschakelen:

1. Ga naar **[!UICONTROL Analytics]** > **[!UICONTROL Components]** > **[!UICONTROL Virtual Report Suites]** > **[!UICONTROL Create new virtual report suite]**.
1. Na het bepalen van **[!UICONTROL Settings]**, klik de **[!UICONTROL Components]** tabel.

1. Schakel het selectievakje in **[!UICONTROL Enable Customization of Virtual Report Suite Components]**:

   ![](assets/vrs-enable.png)

   >[!NOTE]
   >
   >Als de componentenaanpassing wordt toegelaten, is de virtuele rapportreeks toegankelijk **slechts in Analysis Workspace** en is niet toegankelijk in het volgende:

   * [!UICONTROL Reports & Analytics]
   * [!UICONTROL Ad Hoc Analysis]
   * [!UICONTROL Data Warehouse]
   * [!UICONTROL Report Builder]
   * [!UICONTROL Activity Map]
   * Analytics Rapportage-API

   Zodra gecontroleerd, kunt u de componenten toevoegen u in de virtuele rapportreeks zou willen worden omvat door de toepasselijke componenten van de &quot;uitgesloten componenten&quot;kolom aan de &quot;inbegrepen componenten&quot;kolom te slepen. De onderdelen die kunnen worden opgenomen en uitgesloten zijn:

   * Dimensies
   * Metrics
   * Segmenten
   * Datumbereik

   >[!NOTE]
   >
   >Het is niet nodig om gekromde componenten (segmenten, berekende metriek, datumwaaiers) te *delen* . Ze zijn altijd zichtbaar in Analysis Workspace als ze worden beheerd voor de virtuele rapportsuite, zelfs als ze niet worden gedeeld.

1. Bovendien kunt u de componenten filteren of doorzoeken en de volledige gefilterde selectie aan de inbegrepen kolom toevoegen door te klikken **[!UICONTROL Add All]**.

   ![](assets/vrs-add-all.png)

## Naam van componenten wijzigen {#section_0F7CD9F684FE4765BC00A2AFED56550E}

U kunt de vertoningsnamen van inbegrepen componenten veranderen specifiek voor de virtuele rapportreeks. Als u bijvoorbeeld de paginanaam in de virtuele rapportsuite wilt opnemen maar de naam wilt wijzigen in een meer mobiele context, kunt u deze wijzigen in App Screens. De nieuwe naam wordt weergegeven in Analysis Workspace wanneer deze virtuele rapportsuite wordt gebruikt.

![](assets/vrs-rename-component.png)

Klik in Analysis Workspace op het informatiepictogram voor een opgenomen component om de oorspronkelijke naam van de hernoemde component weer te geven:

![](assets/vrs-aw-renamed.png)

## Componentgroepen {#section_483BEC76F49E46ADAAA03F0A12E48426}

Gebruik componentengroepen om bulkcomponenttoevoegingen aan uw virtuele rapportreeks te maken. Als u bijvoorbeeld een standaardset componenten wilt importeren die specifiek zijn voor de analyse van mobiele apps, selecteert u de mobiele toepassingsgroep. Een overeenkomstige reeks afmetingen en metriek (reeds anders genoemd) wordt automatisch toegevoegd aan de virtuele inbegrepen lijst van de rapportreeks.

![](assets/vrs-comp-grp.png)

## Werking werkruimte {#section_6C32F8B642804C0097FCB14E21028D4A}

Zie Een project [](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/curate-share/curate.html)cureren en delen voor meer informatie over cursus in Analysis Workspace.
