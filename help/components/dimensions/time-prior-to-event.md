---
title: Tijd vóór de gebeurtenis
description: De hoeveelheid tijd tussen metrisch en eerste klap van het bezoek.
feature: Dimensions
exl-id: 2586673f-d908-4b69-901a-5fafe635d0d5
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 0%

---

# Tijd vóór de gebeurtenis

De &#39;tijd voorafgaand aan de gebeurtenis&#39; [dimensie](overview.md) meldt hoeveel tijd er is verstreken tussen de eerste hit van het bezoek en de gewenste metrische waarde. Deze dimensie is handig om te bepalen hoeveel tijd het kost om een geslaagde gebeurtenis te bereiken, zoals het verzenden van een formulier of een aankoop.

## Deze dimensie vullen met gegevens

Hoewel deze dimensie technisch uit de doos voor alle implementaties werkt, werkt het best met douane en aankoopgebeurtenissen. Adobe raadt u aan aangepaste gebeurtenissen op uw site te implementeren. Als u douanegebeurtenissen uitvoert, wordt geen extra implementatie vereist voor deze dimensie.

## Dimension-items

De punten van het Dimension omvatten op tijd-gebaseerde emmers die zich van uitstrekken `"Less than 1 minute"` tot `"More than 15 hours"`. Als een bezoeker bijvoorbeeld 23 minuten had geduurd van zijn eerste hit tot een aankoop, zou hij onder de `"10 to 30 minutes"` dimensie-item. De emmers kunnen niet voor dit metrisch worden aangepast.
