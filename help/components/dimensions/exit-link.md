---
title: Koppeling afsluiten
description: De naam van de afsluitkoppeling.
feature: Dimensions
exl-id: 090d5fee-4b35-4be7-866c-5ef1d1c4c0a6
source-git-commit: a15d2b596c1e8b70e91efb49dd607fdbb0ceec3c
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 0%

---

# Koppeling afsluiten

De &quot;verbinding van de Uitgang&quot;[ dimensie ](overview.md) meldt de namen van uitgangsverbindingen die op uw plaats worden uitgevoerd. Deze dimensie is waardevol wanneer u wilt begrijpen welke verbindingen het populairst zijn dat aan domeinen buiten uw plaats richten.

## Deze dimensie vullen met gegevens

Deze afmeting verzamelt gegevens van [`pev2` vraagkoord ](/help/implement/validate/query-parameters.md) in beeldverzoeken voor treffers die ook het `pe` vraagkoord met de waarde van `lnk_e` hebben. Als de queryreeks `pe` een andere waarde heeft in de hit, worden met deze dimensie geen gegevens verzameld. De maximumlengte van deze afmeting is 100 bytes.

Als u gegevens naar deze dimensie wilt verzenden met AppMeasurement, verzendt u een [`tl()`](/help/implement/vars/functions/tl-method.md) -afbeeldingsaanvraag met het argument `"e"` . Vul het argument voor de naam van de koppeling met de gewenste waarde.

## Dimension-objecten

Aangezien deze variabele op een douanekoord in uw implementatie gebaseerd is, bepaalt uw organisatie wat de afmetingspunten zijn. Adobe raadt je aan om koppelingen te groeperen in betekenisvolle rubrieken op basis van je rapportagevereisten.
