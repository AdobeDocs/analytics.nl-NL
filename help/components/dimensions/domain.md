---
title: Domein
description: De organisatie of ISP die de bezoeker gebruikt om tot Internet toegang te hebben.
translation-type: tm+mt
source-git-commit: c2d371cee2821360ab87240b1a81695798af4f9f
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 1%

---


# Domein

De dimensie &#39;Domein&#39; rapporteert toegangspunten die bezoekers gebruiken om toegang te krijgen tot internet.

## Deze dimensie vullen met gegevens

Adobe werkt samen met [Digital Element](https://www.digitalelement.com/) om het domein van het toegangspunt te bepalen. Verscheidene methodes, met inbegrip van omgekeerde DNS raadpleging, worden gebruikt om het domein van het toegangspunt te bepalen. Het vereist geen configuratie, en heeft geen variabele om te bevolken. Het werkt uit de doos met alle implementaties AppMeasurement.

## Dimension-items

Voorbeelden van dimensie-items zijn `comcast.net`, `rr.com`, `sbcglobal.net`en `amazonaws.com`. Merk op dat deze domeinen toegangspunten zijn, en niet noodzakelijk het domein dat ISP of organisatie vertegenwoordigt.

De waarden van Dimension van `None` betekenen dat de eigenaar van het IP van het toegangspunt adres geen domein verstrekte.
