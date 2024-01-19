---
description: Een deelvenster waarin de volgende of vorige dimensie-items voor een specifieke dimensie worden weergegeven.
title: Volgend of vorig deelvenster met items
feature: Panels
role: User, Admin
exl-id: 9f2f8134-2a38-42bb-b195-5e5601d33c4e
source-git-commit: d173a6c6c9751a86f4218ec842da17da14f8485b
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 0%

---

# Volgend of vorig deelvenster met items

Dit paneel bevat een aantal lijsten en visualisaties om het volgende of vorige afmetingspunt voor een specifieke afmeting gemakkelijk te identificeren. U kunt bijvoorbeeld bekijken naar welke pagina&#39;s klanten het vaakst zijn gegaan nadat ze de startpagina hebben bezocht.

## Het deelvenster openen

U hebt vanuit [!UICONTROL Reports] of binnen [!UICONTROL Workspace].

| Toegangspunt | Beschrijving |
| --- | --- |
| [!UICONTROL Reports] | <ul><li>Het deelvenster is al neergezet in een project.</li><li>De linkerspoorstaaf is samengevouwen.</li><li>Als u [!UICONTROL Next page], zijn de standaardinstellingen al toegepast, zoals [!UICONTROL Page] for [!UICONTROL Dimension]en de bovenste pagina als de [!UICONTROL Dimension Item], [!UICONTROL Next] for [!UICONTROL Direction] en [!UICONTROL Visit] for [!UICONTROL Container]. U kunt al deze instellingen wijzigen.</li></ul>![Volgende/Vorige deelvenster](assets/next-previous.png) |
| Werkruimte | Maak een nieuw project en selecteer het deelvensterpictogram in de linkerspoorstaaf. Sleep vervolgens de [!UICONTROL Next or previous item] boven de tabel voor vrije vorm. Let erop dat de [!UICONTROL Dimension] en [!UICONTROL Dimension Item] velden worden leeg gelaten. Selecteer een dimensie in de vervolgkeuzelijst. [!UICONTROL Dimension items] worden gevuld op basis van de [!UICONTROL dimension] u hebt gekozen. Het bovenste dimensie-item wordt toegevoegd, maar u kunt een ander item selecteren. De standaardwaarden zijn Next en Visitor. U kunt deze ook wijzigen.<p>![Volgende/Vorige deelvenster](assets/next-previous2.png) |

{style="table-layout:auto"}

## Deelvensterinvoer {#Input}

U kunt de [!UICONTROL Next or previous item] met deze invoerinstellingen:

| Instelling | Beschrijving |
| --- | --- |
| Segment (of andere component) dropzone | U kunt segmenten of andere componenten slepen en neerzetten om de resultaten van het deelvenster verder te filteren. |
| Dimension | De dimensie waarvoor u volgende of vorige punten wilt onderzoeken. |
| Dimension-item | Het specifieke item in het midden van uw volgende/vorige vraag. |
| Richting | Geef op of u naar de [!UICONTROL Next] of de [!UICONTROL Previous] dimensie-item. |
| Container | [!UICONTROL Visit] of [!UICONTROL Visitor] (gebrek) bepaalt het werkingsgebied van uw vraag. |

{style="table-layout:auto"}

Klikken **[!UICONTROL Build]** om het deelvenster samen te stellen.

## Deelvensteruitvoer {#output}

De [!UICONTROL Next or previous item] retourneert een uitgebreide set gegevens en visualisaties om u te helpen beter te begrijpen welke instanties specifieke dimensie-items volgen of hieraan voorafgaan.

![Uitvoer van deelvenster Volgende/Vorige](assets/next-previous-output.png)

![Uitvoer van deelvenster Volgende/Vorige](assets/next-previous-output2.png)

| Visualisatie | Beschrijving |
| --- | --- |
| Horizontale balk | Hiermee geeft u de volgende (of vorige) items weer op basis van het gekozen dimensie-item. Als u de cursor boven een afzonderlijke balk houdt, wordt het bijbehorende item in de tabel Vrije vorm gemarkeerd. |
| Samenvattingsnummer | Samenvattingsaantal op hoog niveau van alle volgende of vorige instanties van afmetingspunten voor de huidige maand (tot nu toe). |
| Vrije-vormtabel | Hiermee geeft u de volgende (of vorige) items weer op basis van het gekozen dimensie-item in een tabelindeling. Dit waren bijvoorbeeld de populairste pagina&#39;s (op voorvallen) die mensen na (of vóór) de startpagina of de werkruimtenpagina hebben weergegeven. |

{style="table-layout:auto"}
