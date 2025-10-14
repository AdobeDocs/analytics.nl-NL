---
title: Aangepaste koppeling
description: De naam van de aangepaste koppeling.
feature: Dimensions
exl-id: c153f710-f03f-4be6-8e18-5ebf2ed80f01
source-git-commit: a15d2b596c1e8b70e91efb49dd607fdbb0ceec3c
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 0%

---

# Aangepaste koppeling

De &quot;verbinding van de Douane&quot;[&#x200B; dimensie &#x200B;](overview.md) meldt de namen van douaneverbindingen die op uw plaats worden uitgevoerd. Deze dimensie is waardevol wanneer u de types van verbindingen bezoekers het meest wilt begrijpen klikt.

## Deze dimensie vullen met gegevens

Deze afmeting verzamelt gegevens van [`pev2` vraagkoord &#x200B;](/help/implement/validate/query-parameters.md) in beeldverzoeken voor treffers die ook het `pe` vraagkoord met de waarde van `lnk_o` hebben. Als de queryreeks `pe` een andere waarde heeft in de hit, worden met deze dimensie geen gegevens verzameld. De maximumlengte van deze afmeting is 100 bytes.

Als u gegevens naar deze dimensie wilt verzenden met AppMeasurement, verzendt u een [`tl()`](/help/implement/vars/functions/tl-method.md) -afbeeldingsaanvraag met het argument `"o"` . Vul het argument voor de naam van de koppeling met de gewenste waarde.

## Dimension-objecten

Aangezien deze variabele op een douanekoord in uw implementatie gebaseerd is, bepaalt uw organisatie wat de afmetingspunten zijn. Adobe raadt je aan om koppelingen te groeperen in betekenisvolle rubrieken op basis van je rapportagevereisten.
