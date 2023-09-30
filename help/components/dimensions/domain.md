---
title: Domein
description: De organisatie of ISP die de bezoeker gebruikt om tot Internet toegang te hebben.
feature: Dimensions
exl-id: 292dc256-e9e7-47be-8586-774f1c047011
source-git-commit: e32821dd3f30404166554b8437c508172e4764e5
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 1%

---

# Domein

Het domein [dimensie](overview.md) meldt de toegangspunten die bezoekers gebruiken om toegang te krijgen tot internet.

## Deze dimensie vullen met gegevens

Adobe partners met [Digitaal element](https://www.digitalelement.com/) om het domein van het toegangspunt te bepalen. Verscheidene methodes, met inbegrip van omgekeerde DNS raadpleging, worden gebruikt om het domein van het toegangspunt te bepalen. Het vereist geen configuratie, en heeft geen variabele om te bevolken.

* Voor de implementaties van AppMeasurementen, werkt deze dimensie uit de doos.
* Voor de implementaties van SDK van het Web, laat toe [!UICONTROL Network Lookup] wanneer [configureren van een gegevensstroom](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html).

## Dimension-items

Voorbeelden van dimensie-items zijn `comcast.net`, `rr.com`, `sbcglobal.net`, en `amazonaws.com`. Deze domeinen zijn toegangspunten, en niet noodzakelijk het domein dat ISP of een organisatie vertegenwoordigt.

Dimension waarden van `None` betekent dat de eigenaar van het IP van het toegangspunt adres geen domein verstrekte.
