---
description: Kalenderopties in een ander model dan het Gregoriaanse model. De opties omvatten de 4-4-5, 4-5-4, en 5-4-4 kalendermodellen, die allen als normen voor de kleinhandelsindustrie worden gebruikt. Rapportage biedt ook een volledig aanpasbare kalender die u zelf kunt instellen.
title: Kalender aanpassen
feature: Admin Tools
exl-id: 2196c7b7-7183-43a8-bb91-5a1e479819d4
role: Admin
source-git-commit: d5bbba7518529befabb8815ac657336326562fd1
workflow-type: tm+mt
source-wordcount: '553'
ht-degree: 0%

---

# Kalender aanpassen

Kalenderopties in een ander model dan het Gregoriaanse model. De opties omvatten de 4-4-5, 4-5-4, en 5-4-4 kalendermodellen, die allen als normen voor de kleinhandelsindustrie worden gebruikt. Daarnaast biedt rapportage een optie voor een volledig aanpasbare kalender die u zelf kunt instellen.

**[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > Selecteer een rapportsuite > **[!UICONTROL Edit Settings]** > **[!UICONTROL General]** > **[!UICONTROL Customize Calendar]**

>[!CAUTION]
>
>Als u de kalender wijzigt, verandert de manier waarop gegevens worden verwerkt (d.w.z. de definitie van unieke wekelijkse en maandelijkse bezoekers). Wanneer de definitie van weken en maanden in een kalender verandert, worden de historische gegevens niet gewijzigd. Deze instelling heeft ook invloed op segmenten die zijn gebaseerd op datumbereiken.

U kunt de kalender gebruiken om de eerste dag van de week en het jaar te bepalen, of een verschillende detailhandelkalender stijl gebruiken. De kalenderformaten worden gebruikt voor diverse doeleinden, met inbegrip van verkoopvergelijking en voorspelde standaardisering, loonkostenanalyse, of de fysieke verordening van het inventarisaantal. De detailhandel gebruikt bijvoorbeeld de 4-5-4 boekhoudkalender om de verkoopseizoenen te ondersteunen die specifiek zijn voor de detailhandel. Elk kalenderformaat wordt hieronder beschreven.

## Kalenderbeschrijvingen aanpassen {#section_B0D224DACB914A378902A4E0E1234889}

| Kalender | Beschrijving |
|--- |--- |
| Gregoriaanse kalender | Gebruikt het traditionele kalenderformaat (Januari door December, met 30 of 31 dagen en een veranderlijk aantal weken in elke maand). |
| Gewijzigd Gregoriaans kalender | Gebruikt de Traditionele Gregoriaanse Kalender maar laat u toe om de eerste maand van het jaar en eerste dag van de week te selecteren. |
| 4-5-4 Retail Calendar | Verdeelt elke maand met het aantal weken in de maand. Januari heeft vier weken, enzovoort. De National Retail Federation gebruikt de 4-5-4-kalenderindeling. |
| Aangepaste kalender | Biedt drie indelingen op basis van het aantal weken in elke maand. Het aantal weken in elke maand hangt van de geselecteerde eerste dag van het jaar af.  Een jaar heeft 52 weken. Verdeel dat in 4 kwarten en je krijgt 13 weken per kwart. Maar er zijn drie maanden in een kwart. 13 is niet deelbaar door 3 zodat u de extra week in één van de maanden plaatst zodat het altijd verenigbaar is.<ul><li>5/4/4 betekent de eerste maand van het kwartaal de extra week heeft. 4/5/4 betekent dat de tweede maand de extra week heeft, enz. In de 5-4-4 kalender wordt de 53e week toegevoegd aan het laatste kwartaal van het jaar.</li><li>4-5-4:januari heeft vier weken, februari heeft vijf weken, maart heeft vier weken, enzovoort.</li><li>4-4-5: januari heeft vier weken, februari heeft vier weken, maart heeft vijf weken, enzovoort.</li><li>5-4-4: januari heeft vijf weken, februari heeft vier weken, maart heeft vier weken, enzovoort.</li></ul> |

>[!NOTE]
>Deze kalenderopties worden ondersteund door alle Adobe Analytics-gereedschappen (Analysis Workspace, Report Builder, Activity Map), behalve Data Warehouse. Data Warehouse ondersteunt alleen de Gregoriaanse kalender volledig. Wanneer u een niet-Gregoriaanse kalender kiest, gebruikt Data Warehouse het verwachte datumbereik van de niet-Gregoriaanse kalender, maar de uitsplitsingen van dagen/weken/maanden binnen de rijen van het rapport zijn mogelijk niet wat wordt verwacht van een niet-Gregoriaanse kalender.
