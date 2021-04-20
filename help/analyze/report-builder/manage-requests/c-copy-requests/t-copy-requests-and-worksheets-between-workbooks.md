---
description: Kopieer een volledig spreadsheet in een bronwerkboek aan een spreadsheet in één of meerdere doelwerkboeken.
title: Aanvragen en werkbladen kopiëren tussen werkmappen
uuid: 6b2c4259-d8cb-430e-819f-38e213dd2661
feature: Report Builder
role: Business Practitioner, Administrator
translation-type: tm+mt
source-git-commit: 894ee7a8f761f7aa2590e06708be82e7ecfa3f6d
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 4%

---


# Aanvragen en werkbladen kopiëren tussen werkmappen

Kopieer een volledig spreadsheet in een bronwerkboek aan een spreadsheet in één of meerdere doelwerkboeken.

Om dit te doen, moet u minstens twee werkboeken hebben die in het zelfde geval van Excel worden geopend: het eerste bronwerkboek bevat een spreadsheet (aantekenvel) met verzoeken in kaart gebracht aan cellen, terwijl de extra doelwerkboeken de bestemmingen zijn. Voor elk nieuw doelwerkboek, zou u aan de zelfde rapportreeks zoals het bronwerkboek moeten login alvorens u spreadsheets kunt kleven die verzoeken bevatten.
1. Klik met de rechtermuisknop op het werkblad in het bronwerkboek en selecteer **[!UICONTROL Copy Worksheet w/Requests]**.
1. In het bestemmingswerkboek, klik spreadsheet met de rechtermuisknop aan en selecteer **[!UICONTROL Paste Worksheet w/Requests]**.

   De zelfde instantie van Excel betekent dat slechts één enkel proces van Excel ( [!DNL excel.exe]) tegelijkertijd op uw computer loopt. Als u twee instanties van Excel lanceert en probeert om een aantekenvel van een werkboek in de eerste instantie van Excel aan een werkboek in de tweede instantie van Excel te kopiëren, presenteert de rapportaannemer niet de optie om een aantekenvel in het kortere wegmenu van de tweede instantie van Excel te kleven.

   Als u login aan de bron en doelwerkboeken gebruikend verschillende rapportreeksen, de enige resultaten u van de deegverrichting ziet zijn die die het formatteren van het doelwerkboek beïnvloeden. Report Builder toont een bericht verklarend dat de informatie voor de verzoeken die uit een gespecificeerde rapportreeks (in het bronwerkboek) worden afgeleid niet beschikbaar in het doelwerkboek is. Om de verzoeken te openbaren die aan het doelwerkboek worden gekleefd, moet u login aan het doelwerkboek gebruikend de zelfde rapportreeks zoals het bronwerkboek.

   U kunt één of meerdere verzoeken van een spreadsheet in één werkboek aan een spreadsheet in een ander werkboek kopiëren en kleven, zolang het tweede werkboek als een ander document in de zelfde instantie van Excel open is. De verzoeken in beide werkboeken moeten worden gecreeerd gebruikend de zelfde login van de rapportreeks.
