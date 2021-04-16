---
description: Stappen die beschrijven hoe indelingsgegevens in het classificatiebestand kunnen worden verwijderd.
subtopic: Classifications
title: Classificatiedata omzeilen
feature: Admin Tools
uuid: 724edcc5-4990-4f24-afbb-9aef301791a7
exl-id: 0d3a0e91-5537-43ee-bd28-9907ee6eb331
translation-type: tm+mt
source-git-commit: 78412c2588b07f47981ac0d953893db6b9e1d3c2
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 10%

---

# Classificatiedata omzeilen

Stappen die beschrijven hoe indelingsgegevens in het classificatiebestand kunnen worden verwijderd.

<!--Meike, please check this page against orginal. It might be missing information. -->

1. Zorg ervoor dat de indeling van het classificatiebestand v2.1 is.

   Als v2.1 wordt toegelaten, zult u een lijn gelijkend op zien:

   >[!NOTE]
   >
   >Als u de indeling v2.1 wilt opgeven, schakelt u **[!UICONTROL Quoted Output]** in wanneer u het bestand exporteert op de pagina [!UICONTROL Classification Importer] ( [!UICONTROL Browser Export] of [!UICONTROL FTP Export]).

1. Omring het veld met speciale tekens tussen dubbele aanhalingstekens (`"`).

Een dubbel aanhalingsteken kan in een beschermde cel verschijnen door het met twee dubbele aanhalingstekens (`" "`) te vervangen. Bijvoorbeeld:

```
My String "of data"
```

Geëxpandeerd zou zijn:

```
"My String ""of data"""
```
