---
title: Koppeling downloaden
description: De naam van de downloadkoppeling.
feature: Dimensions
exl-id: 078014a2-1f09-4177-9575-b44c5da25816
source-git-commit: a15d2b596c1e8b70e91efb49dd607fdbb0ceec3c
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 0%

---

# Koppeling downloaden

De &quot;verbinding van de Download&quot; [&#x200B; dimensie &#x200B;](overview.md) meldt de namen van downloadverbindingen die op uw plaats worden uitgevoerd. Deze dimensie is waardevol als u meer wilt weten over het gedrag van bezoekers bij downloadkoppelingen, zoals:

* Bepaal de bestanden die het meest van uw site worden gedownload.
* Begrijp als bepaalde dossiers vaker tijdens specifieke tijdsperioden worden gedownload.
* Valideer of bezoekers verschillende bestandstypen downloaden, indien beschikbaar.

## Deze dimensie vullen met gegevens

Deze afmeting verzamelt gegevens van [`pev2` vraagkoord &#x200B;](/help/implement/validate/query-parameters.md) in beeldverzoeken voor treffers die ook het `pe` vraagkoord met de waarde van `lnk_d` hebben. Als de queryreeks `pe` een andere waarde heeft in de hit, worden met deze dimensie geen gegevens verzameld. De maximumlengte van deze afmeting is 100 bytes.

Als u gegevens naar deze dimensie wilt verzenden met AppMeasurement, verzendt u een [`tl()`](/help/implement/vars/functions/tl-method.md) -afbeeldingsaanvraag met het argument `"d"` . Vul het argument voor de naam van de koppeling met de gewenste waarde:

```js
s.tl(true,"d","Example download link");
```

## Dimension-objecten

Aangezien deze variabele op een douanekoord in uw implementatie gebaseerd is, bepaalt uw organisatie wat de afmetingspunten zijn. Adobe raadt je aan om koppelingen te groeperen in betekenisvolle rubrieken op basis van je rapportagevereisten.
