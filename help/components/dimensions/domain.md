---
title: Domein
description: De organisatie of ISP die de bezoeker gebruikt om tot Internet toegang te hebben.
feature: Dimensions
exl-id: 292dc256-e9e7-47be-8586-774f1c047011
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 1%

---

# Domein

De dimensie &#39;Domein&#39; rapporteert toegangspunten die bezoekers gebruiken om toegang te krijgen tot internet.

## Deze dimensie vullen met gegevens

Adobe partners met [Digitaal element](https://www.digitalelement.com/) om het domein van het toegangspunt te bepalen. Verscheidene methodes, met inbegrip van omgekeerde DNS raadpleging, worden gebruikt om het domein van het toegangspunt te bepalen. Het vereist geen configuratie, en heeft geen variabele om te bevolken. Het werkt uit de doos met alle implementaties AppMeasurement.

## Dimension-items

Voorbeelden van dimensie-items zijn `comcast.net`, `rr.com`, `sbcglobal.net`, en `amazonaws.com`. Merk op dat deze domeinen toegangspunten zijn, en niet noodzakelijk het domein dat ISP of organisatie vertegenwoordigt.

Dimension-waarden van `None` betekent dat de eigenaar van het IP van het toegangspunt adres geen domein verstrekte.
