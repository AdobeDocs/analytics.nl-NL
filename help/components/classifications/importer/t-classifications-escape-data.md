---
description: Stappen die beschrijven hoe indelingsgegevens in het classificatiebestand kunnen worden verwijderd.
title: Classificatiedata omzeilen
feature: Classifications
exl-id: 0d3a0e91-5537-43ee-bd28-9907ee6eb331
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 8%

---

# Classificatiedata omzeilen

Stappen die beschrijven hoe indelingsgegevens in het classificatiebestand kunnen worden verwijderd.

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
