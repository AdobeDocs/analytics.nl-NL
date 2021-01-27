---
title: Aangepaste koppeling
description: De naam van de aangepaste koppeling.
translation-type: tm+mt
source-git-commit: 423e9b753a3b7b1e0a8e8b9748f9694d718abd18
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 0%

---


# Aangepaste koppeling

De dimensie &#39;Aangepaste koppeling&#39; rapporteert de namen van aangepaste koppelingen die op uw site zijn geïmplementeerd. Deze dimensie is waardevol wanneer u de types van verbindingen bezoekers het meest wilt begrijpen klikt.

## Deze dimensie vullen met gegevens

Deze afmeting verzamelt gegevens van [`pev2` vraagkoord](/help/implement/validate/query-parameters.md) in beeldverzoeken voor treffers die ook `pe` vraagkoord met de waarde van `lnk_o` hebben. Als de query-tekenreeks `pe` een andere waarde heeft in de hit, worden met deze dimensie geen gegevens verzameld.

Als u gegevens naar deze afmeting wilt verzenden gebruikend AppMeasurement, verzend een [`tl()`](/help/implement/vars/functions/tl-method.md) beeldverzoek met een koppelingstype argument van `"o"`. Vul het argument voor de naam van de koppeling met de gewenste waarde.

## Dimension-items

Aangezien deze variabele op een douanekoord in uw implementatie gebaseerd is, bepaalt uw organisatie wat de afmetingspunten zijn. Adobe raadt u aan om koppelingen te groeperen in betekenisvolle categorieën op basis van uw rapportagebehoeften.
