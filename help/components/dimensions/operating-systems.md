---
title: Besturingssysteem
description: Het besturingssysteem van de bezoeker.
feature: Dimensions
exl-id: e3911ae0-d242-4da2-a4bc-b2f4877f9dd2
source-git-commit: 9c3e65392d6e5929ce1ecefbc460c1fd5576aed8
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---

# Besturingssysteem

Het &quot;besturingssysteem&quot; [dimensie](overview.md) toont het besturingssysteem en de versie die de bezoeker heeft gebruikt. Als u functies in uw webeigenschap hebt die OS-specifiek zijn, kunt u met deze dimensie beter begrijpen welke besturingssystemen het meest worden gebruikt.

## Deze dimensie vullen met gegevens

Deze dimensie verwijst naar een raadplegingstabel intern aan Adobe. De opzoekwaarde is gebaseerd op de `User-Agent` HTTP-header in afbeeldingsaanvragen. Adobe partners met [DeviceAtlas](https://deviceatlas.com/) om raadplegingen tussen gebruikersagent en werkend systeem te handhaven.

* Voor de implementaties van AppMeasurementen, werkt deze dimensie uit de doos.
* Voor de implementaties van SDK van het Web, laat toe [!UICONTROL Device Lookup] wanneer [configureren van een gegevensstroom](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html).

## Dimension-items

Dimension-items omvatten besturingssystemen die bezoekers gebruiken. Voorbeelden zijn `"Windows 10"`, `"OS X 10.15.7"`, en `"Android 9"`.

## Nauwkeurige versies van besturingssystemen bijhouden

Naarmate de branche zich ontwikkelt in de richting van de tips van de klant, kunnen sommige versies van besturingssystemen worden verward. Bijvoorbeeld, &quot;Vensters 10&quot;en &quot;Vensters 11&quot;kunnen allebei onder &quot;Vensters 10&quot;worden gegroepeerd als u geen high-entropy cliëntwenken verzamelt. Zie [Clienttips](/help/technotes/client-hints.md) in de TechNotes-handleiding voor meer informatie.
