---
title: Koppeling downloaden
description: De naam van de downloadkoppeling.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 0%

---


# Koppeling downloaden

De dimensie &#39;Download link&#39; rapporteert de namen van downloadkoppelingen die op uw site zijn geïmplementeerd. Deze dimensie is waardevol als u meer wilt weten over het gedrag van bezoekers bij downloadkoppelingen, zoals:

* Bepaal de bestanden die het vaakst van uw site worden gedownload.
* Begrijp als bepaalde dossiers vaker tijdens specifieke tijdsperioden worden gedownload.
* Valideer of bezoekers verschillende bestandstypen downloaden, indien beschikbaar.

## Deze dimensie vullen met gegevens

Deze afmeting verzamelt gegevens van het [`pev2` vraagkoord](/help/implement/validate/query-parameters.md) in beeldverzoeken voor treffers die ook het `pe` vraagkoord met de waarde van `lnk_d`hebben. Als de `pe` queryreeks een andere waarde heeft in de hit, worden met deze dimensie geen gegevens verzameld.

Als u gegevens naar deze afmeting wilt verzenden gebruikend AppMeasurement:

* Vul de [`linkName`](/help/implement/vars/config-vars/linkname.md) variabele met de gewenste waarde.
* Stel de [`linkType`](/help/implement/vars/config-vars/linktype.md) variabele in op `"d"`.
* Verzend een [`tl()`](/help/implement/vars/functions/tl-method.md) afbeeldingsaanvraag.

## Dimensie-items

Aangezien deze variabele op een douanekoord in uw implementatie gebaseerd is, bepaalt uw organisatie wat de afmetingspunten zijn. Adobe raadt u aan om koppelingen in betekenisvolle categorieën te groeperen op basis van uw rapportagevereisten.
