---
description: Stappen die beschrijven hoe indelingsgegevens in het classificatiebestand kunnen worden verwijderd.
title: Classificatiedata omzeilen
feature: Classifications
exl-id: 0d3a0e91-5537-43ee-bd28-9907ee6eb331
source-git-commit: ce7f953b8f7f1f7d0616074454e4401937fcc0c7
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 8%

---

# Classificatiedata omzeilen

Classificatiegegevens verwijderen uit het classificatiebestand:

<!--Meike, please check this page against orginal. It might be missing information. -->

1. Zorg ervoor dat de indeling van het classificatiebestand v2.1 is.

   Als v2.1 wordt toegelaten, zult u een lijn gelijkend op zien:

   >[!NOTE]
   >
   >Als u de indeling v2.1 wilt opgeven, schakelt u **[!UICONTROL Quoted Output]** bij het exporteren van het bestand op het tabblad [!UICONTROL Classification Importer] pagina ( [!UICONTROL Browser Export] of [!UICONTROL FTP Export]).

1. Omring het veld met speciale tekens tussen dubbele aanhalingstekens (`"`).

Een dubbel aanhalingsteken kan in een beschermde cel verschijnen door het met twee dubbele aanhalingstekens te vervangen (`" "`). Bijvoorbeeld:

```
My String "of data"
```

Geëxpandeerd zou zijn:

```
"My String ""of data"""
```
