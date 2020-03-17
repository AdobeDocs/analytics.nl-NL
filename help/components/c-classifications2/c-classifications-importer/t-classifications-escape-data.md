---
description: Stappen die beschrijven hoe indelingsgegevens in het classificatiebestand kunnen worden verwijderd.
subtopic: Classifications
title: Escape-classificatiegegevens
topic: Admin tools
uuid: 724edcc5-4990-4f24-afbb-9aef301791a7
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Escape-classificatiegegevens

Stappen die beschrijven hoe indelingsgegevens in het classificatiebestand kunnen worden verwijderd.

<!--Meike, please check this page against orginal. It might be missing information. -->

1. Zorg ervoor dat de indeling van het classificatiebestand v2.1 is.

   Als v2.1 wordt toegelaten, zult u een lijn gelijkend op zien:

   >[!NOTE]
   >
   >Als u de indeling v2.1 wilt opgeven, schakelt u deze optie in **[!UICONTROL Quoted Output]** wanneer u het bestand op de [!UICONTROL Classification Importer] pagina ( [!UICONTROL Browser Export] of [!UICONTROL FTP Export]) exporteert.

1. Omring het veld met speciale tekens tussen dubbele aanhalingstekens (`"`).

Een dubbel aanhalingsteken kan in een beschermde cel verschijnen door het met twee dubbele aanhalingstekens (`" "`) te vervangen. Bijvoorbeeld:

```
My String "of data"
```

Geëxpandeerd zou zijn:

```
"My String ""of data"""
```
