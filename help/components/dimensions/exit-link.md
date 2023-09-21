---
title: Koppeling afsluiten
description: De naam van de afsluitkoppeling.
feature: Dimensions
exl-id: 090d5fee-4b35-4be7-866c-5ef1d1c4c0a6
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 0%

---

# Koppeling afsluiten

De koppeling Afsluiten [dimensie](overview.md) rapporteert de namen van afsluitkoppelingen die op uw site zijn geïmplementeerd. Deze dimensie is waardevol wanneer u wilt begrijpen welke verbindingen het populairst zijn dat aan domeinen buiten uw plaats richten.

## Deze dimensie vullen met gegevens

Deze dimensie verzamelt gegevens van de [`pev2` querytekenreeks](/help/implement/validate/query-parameters.md) in afbeeldingsaanvragen voor treffers die ook `pe` querytekenreeks met de waarde van `lnk_e`. Als de `pe` queryreeks heeft een andere waarde in de hit, deze dimensie verzamelt geen gegevens.

Als u gegevens naar deze dimensie wilt verzenden gebruikend AppMeasurement, verzend een [`tl()`](/help/implement/vars/functions/tl-method.md) afbeeldingsverzoek met een koppelingstype-argument van `"e"`. Vul het argument voor de naam van de koppeling met de gewenste waarde.

## Dimension-items

Aangezien deze variabele op een douanekoord in uw implementatie gebaseerd is, bepaalt uw organisatie wat de afmetingspunten zijn. Adobe raadt u aan om koppelingen te groeperen in betekenisvolle categorieën op basis van uw rapportagevereisten.
