---
title: Browsertype
description: De organisatie die de browser heeft gemaakt.
feature: Dimensions
exl-id: 2a88ebc6-879e-4e5b-a8e5-40a32d54ac1b
source-git-commit: e32821dd3f30404166554b8437c508172e4764e5
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 0%

---

# Browsertype

Het type Browser [dimensie](overview.md) geeft een lijst weer van de organisaties die de browser hebben gemaakt die de bezoeker gebruikt. Deze dimensie is handig wanneer u wilt zien welke overkoepelende browsers bezoekers gebruiken. Het biedt waarde over de dimensie &#39;Browsers&#39; in die zin dat het geen verschillende versies van dezelfde browser opsomt als afzonderlijke dimensie-items.

## Deze dimensie vullen met gegevens

Deze dimensie verwijst naar een raadplegingstabel intern aan Adobe. De opzoekwaarde is gebaseerd op de `User-Agent` HTTP-header in afbeeldingsaanvragen. Adobe partners met [DeviceAtlas](https://deviceatlas.com/) om raadplegingen tussen gebruikersagent en browser te handhaven.

* Voor de implementaties van AppMeasurementen, werkt deze dimensie uit de doos.
* Voor de implementaties van SDK van het Web, laat toe [!UICONTROL Device Lookup] wanneer [configureren van een gegevensstroom](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html).

## Dimension-items

Dimension-items omvatten organisaties die browsers maken. Items met een gemeenschappelijke dimensie omvatten `"Google"` (de opstellers van [!DNL Chrome]), `"Apple"` (de opstellers van [!DNL Safari]), `"Microsoft"` (de opstellers van [!DNL Edge]), en `"Mozilla"` (de opstellers van [!DNL Firefox]).
