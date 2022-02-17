---
title: Koppeling downloaden
description: De naam van de downloadkoppeling.
feature: Dimensions
exl-id: 078014a2-1f09-4177-9575-b44c5da25816
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 0%

---

# Koppeling downloaden

De dimensie &#39;Download link&#39; rapporteert de namen van downloadkoppelingen die op uw site zijn geïmplementeerd. Deze dimensie is waardevol als u meer wilt weten over het gedrag van bezoekers bij downloadkoppelingen, zoals:

* Bepaal de bestanden die het vaakst van uw site worden gedownload.
* Begrijp als bepaalde dossiers vaker tijdens specifieke tijdsperioden worden gedownload.
* Valideer of bezoekers verschillende bestandstypen downloaden, indien beschikbaar.

## Deze dimensie vullen met gegevens

Deze dimensie verzamelt gegevens van de [`pev2` querytekenreeks](/help/implement/validate/query-parameters.md) in afbeeldingsaanvragen voor treffers die ook `pe` querytekenreeks met de waarde van `lnk_d`. Als de `pe` queryreeks heeft een andere waarde in de hit, deze dimensie verzamelt geen gegevens.

Als u gegevens naar deze afmeting wilt verzenden gebruikend AppMeasurement, verzend een [`tl()`](/help/implement/vars/functions/tl-method.md) afbeeldingsverzoek met een koppelingstype-argument van `"d"`. Vul het argument voor de naam van de koppeling met de gewenste waarde.

## Dimension-items

Aangezien deze variabele op een douanekoord in uw implementatie gebaseerd is, bepaalt uw organisatie wat de afmetingspunten zijn. Adobe raadt u aan om koppelingen te groeperen in betekenisvolle categorieën op basis van uw rapportagebehoeften.
