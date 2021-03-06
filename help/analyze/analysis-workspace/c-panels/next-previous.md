---
description: Een deelvenster waarin de volgende of vorige dimensie-items voor een specifieke dimensie worden weergegeven.
title: Volgend of vorig deelvenster met items
feature: Panels
role: User, Admin
source-git-commit: 4bb950350d258b8d608f6d95d37d7d860e23ed2c
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 1%

---


# Volgend of vorig deelvenster met items

De [!UICONTROL Next or previous item] deelvenster dat is gestart als een rapport in Rapporten en Analytics, onder [!UICONTROL Reports] > [!UICONTROL Most popular] > [!UICONTROL Next page/Previous page]. Het is nu ook een deelvenster Werkruimte. Dit paneel bevat een aantal lijsten en visualisaties om het volgende of vorige afmetingspunt voor een specifieke afmeting gemakkelijk te identificeren. U kunt bijvoorbeeld bekijken naar welke pagina&#39;s klanten het vaakst zijn gegaan nadat ze de startpagina hebben bezocht.

## Het deelvenster openen

U hebt vanuit [!UICONTROL Reports] of binnen [!UICONTROL Workspace].

| Toegangspunt | Beschrijving |
| --- | --- |
| [!UICONTROL Reports] | <ul><li>Het deelvenster is al neergezet in een project.</li><li>De linkerspoorstaaf is samengevouwen.</li><li>Als u [!UICONTROL Next page], zijn de standaardinstellingen al toegepast, zoals [!UICONTROL Page] for [!UICONTROL Dimension]en de bovenste pagina als de [!UICONTROL Dimension Item], [!UICONTROL Next] for [!UICONTROL Direction] en [!UICONTROL Visit] for [!UICONTROL Container]. U kunt al deze instellingen wijzigen.</li></ul>![Volgende/Vorige deelvenster](assets/next-previous.png) |
| Werkruimte | Maak een nieuw project en selecteer het deelvensterpictogram in de linkerspoorstaaf. Sleep vervolgens de [!UICONTROL Next or previous item] boven de tabel voor vrije vorm. Let erop dat de [!UICONTROL Dimension] en [!UICONTROL Dimension Item] velden worden leeg gelaten. Selecteer een dimensie in de vervolgkeuzelijst. [!UICONTROL Dimension items] worden gevuld op basis van de [!UICONTROL dimension] u hebt gekozen. Het bovenste dimensie-item wordt toegevoegd, maar u kunt een ander item selecteren. De standaardwaarden zijn Next en Visitor. U kunt deze ook wijzigen.<p>![Volgende/Vorige deelvenster](assets/next-previous2.png) |

{style=&quot;table-layout:auto&quot;}

## Deelvensterinvoer {#Input}

U kunt de [!UICONTROL Next or previous item] met deze invoerinstellingen:

| Instelling | Beschrijving |
| --- | --- |
| Segment (of andere component) dropzone | U kunt segmenten of andere componenten slepen en neerzetten om de resultaten van het deelvenster verder te filteren. |
| Dimension | De dimensie waarvoor u volgende of vorige punten wilt onderzoeken. |
| Dimension-item | Het specifieke item in het midden van uw volgende/vorige vraag. |
| Richting | Geef op of u op zoek bent naar [!UICONTROL Next] of de [!UICONTROL Previous] dimensie-item. |
| Container | [!UICONTROL Visit] of [!UICONTROL Visitor] (gebrek) bepaalt het werkingsgebied van uw vraag. |

{style=&quot;table-layout:auto&quot;}

Klikken **[!UICONTROL Build]** om het deelvenster samen te stellen.

## Deelvensteruitvoer {#output}

De [!UICONTROL Next or previous item] retourneert een uitgebreide set gegevens en visualisaties om u te helpen beter te begrijpen welke instanties specifieke dimensie-items volgen of hieraan voorafgaan.

![Uitvoer van deelvenster Volgende/Vorige](assets/next-previous-output.png)

![Uitvoer van deelvenster Volgende/Vorige](assets/next-previous-output2.png)

| Visualisatie | Beschrijving |
| --- | --- |
| Horizontale balk | Hiermee geeft u de volgende (of vorige) items weer op basis van het gekozen dimensie-item. Als u de cursor boven een afzonderlijke balk houdt, wordt het bijbehorende item in de tabel Vrije vorm gemarkeerd. |
| Samenvattingsnummer | Samenvattingsaantal op hoog niveau van alle volgende of vorige instanties van afmetingspunten voor de huidige maand (tot nu toe). |
| Vrije-vormentabel | Hiermee geeft u de volgende (of vorige) items weer op basis van het gekozen dimensie-item in een tabelindeling. Dit waren bijvoorbeeld de populairste pagina&#39;s (op voorvallen) die mensen na (of v????r) de startpagina of de werkruimtenpagina hebben weergegeven. |

{style=&quot;table-layout:auto&quot;}
