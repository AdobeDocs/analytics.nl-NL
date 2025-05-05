---
title: Typen besturingssystemen
description: Het besturingssysteem, ongeacht de versie.
feature: Dimensions
exl-id: 0afd5261-98e8-4247-865a-1b8844c53ff4
source-git-commit: e32821dd3f30404166554b8437c508172e4764e5
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# Typen besturingssystemen

De &quot;besturingssysteemtypen&quot; [dimensie](overview.md) toont het overkoepelende OS dat de bezoeker, ongeacht specifieke versies gebruikte. Deze dimensie is handig om niet alleen te begrijpen welk besturingssysteem en welke versie het meest worden gebruikt, maar ook welk besturingssysteem bezoekers doorgaans gebruiken.

## Deze dimensie vullen met gegevens

Deze dimensie verwijst naar een raadplegingstabel intern aan Adobe. De opzoekwaarde is gebaseerd op de `User-Agent` HTTP-header in afbeeldingsaanvragen. Adobe partners met [DeviceAtlas](https://deviceatlas.com/) om raadplegingen tussen gebruikersagent en werkend systeemtype te handhaven.

* Voor de implementaties van AppMeasurementen, werkt deze dimensie uit de doos.
* Voor de implementaties van SDK van het Web, laat toe [!UICONTROL Device Lookup] wanneer [configureren van een gegevensstroom](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html?lang=nl-NL).

## Dimension-items

Dimensionen zijn onder andere het type besturingssysteem dat wordt gebruikt. Voorbeelden zijn `"Microsoft Windows"`, `"Apple Macintosh"`, `"Google Android"`, en `"Apple iOS"`.
