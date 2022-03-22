---
title: Annotaties weergeven
description: Annotaties weergeven in Workspace.
role: User, Admin
feature: Annotations
exl-id: 52b179fd-d9a4-4119-a3c6-f6a36f24f8ea
source-git-commit: 70dc0fedc6ba16cb521af7a94524a4df99200d25
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 1%

---

# Annotaties weergeven

>[!NOTE]
>
>Deze functie is momenteel in beperkte tests.

Annotaties worden iets anders weergegeven, afhankelijk van het feit of ze één dag of een datumbereik beslaan.

## Annotaties weergeven in lijngrafieken of tabellen

| Datum | Weergave |
| --- | --- |
| **Eén dag** | ![](assets/single-day.png)<p>Wanneer u de aanwijzer boven de annotatie houdt, kunt u de details van de annotatie bekijken. U kunt deze bewerken door het penpictogram te selecteren of door de annotatie te verwijderen:<p> ![](assets/hover.png) |
| **Datumbereik** | Het pictogram verandert en wanneer u de muisaanwijzer op het pictogram plaatst, wordt het datumbereik weergegeven.<p>![](assets/multi-day.png)<p>Wanneer u deze optie selecteert in het lijndiagram, worden de metagegevens van de annotatie weergegeven en kunt u deze bewerken of verwijderen:![](assets/multi-hover.png)<p>In een tabel wordt op elke datum in het datumbereik een pictogram weergegeven.<p>![](assets/multi-day-table.png) |
| **Overlappende annotaties** | Op dagen waarop meerdere annotaties zijn gekoppeld, wordt het pictogram weergegeven in een grijze kleur.<p>![](assets/grey.png)<p>Wanneer u de cursor boven het grijze pictogram houdt, worden alle overlappende annotaties weergegeven:<p>![](assets/overlap.png) |

## Annotaties weergeven in een .pdf-bestand

Aangezien u de muisaanwijzer niet boven pictogrammen in een .pdf-bestand kunt plaatsen, bevat dit bestand (na het exporteren) onder in een deelvenster notities met uitleg. Hier volgt een voorbeeld:

![](assets/ann-pdf.png)

## Annotaties met niet-trendgegevens weergeven

Soms wordt annotatie weergegeven met niet-trendgegevens, maar gekoppeld aan een specifieke dimensie. In dat geval worden ze alleen in een summiere annotatie in de rechterbenedenhoek weergegeven. Hier volgt een voorbeeld:

![](assets/non-date.png)

Het overzichtsdiagram wordt weergegeven in alle visualisatietypen in de hoek, niet alleen in niet-beheerde vrije-vormtabellen en samenvattingsnummers. Het wordt ook weergegeven in visualisaties zoals [!UICONTROL Donut], [!UICONTROL Flow],[!UICONTROL Fallout],[!UICONTROL Cohort], enzovoort.

![](assets/ann-summary.png)
