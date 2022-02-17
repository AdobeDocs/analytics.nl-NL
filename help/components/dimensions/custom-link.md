---
title: Aangepaste koppeling
description: De naam van de aangepaste koppeling.
feature: Dimensions
exl-id: c153f710-f03f-4be6-8e18-5ebf2ed80f01
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 0%

---

# Aangepaste koppeling

De dimensie &#39;Aangepaste koppeling&#39; rapporteert de namen van aangepaste koppelingen die op uw site zijn geïmplementeerd. Deze dimensie is waardevol wanneer u de types van verbindingen bezoekers het meest wilt begrijpen klikt.

## Deze dimensie vullen met gegevens

Deze dimensie verzamelt gegevens van de [`pev2` querytekenreeks](/help/implement/validate/query-parameters.md) in afbeeldingsaanvragen voor treffers die ook `pe` querytekenreeks met de waarde van `lnk_o`. Als de `pe` queryreeks heeft een andere waarde in de hit, deze dimensie verzamelt geen gegevens.

Als u gegevens naar deze afmeting wilt verzenden gebruikend AppMeasurement, verzend een [`tl()`](/help/implement/vars/functions/tl-method.md) afbeeldingsverzoek met een koppelingstype-argument van `"o"`. Vul het argument voor de naam van de koppeling met de gewenste waarde.

## Dimension-items

Aangezien deze variabele op een douanekoord in uw implementatie gebaseerd is, bepaalt uw organisatie wat de afmetingspunten zijn. Adobe raadt u aan om koppelingen te groeperen in betekenisvolle categorieën op basis van uw rapportagebehoeften.
