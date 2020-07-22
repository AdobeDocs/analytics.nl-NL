---
title: Aangepaste koppeling
description: De naam van de aangepaste koppeling.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---


# Aangepaste koppeling

De dimensie &#39;Aangepaste koppeling&#39; rapporteert de namen van aangepaste koppelingen die op uw site zijn geïmplementeerd. Deze dimensie is waardevol wanneer u de types van verbindingen bezoekers het meest wilt begrijpen klikt.

## Deze dimensie vullen met gegevens

Deze afmeting verzamelt gegevens van het [`pev2` vraagkoord](/help/implement/validate/query-parameters.md) in beeldverzoeken voor treffers die ook het `pe` vraagkoord met de waarde van `lnk_o`hebben. Als de `pe` queryreeks een andere waarde heeft in de hit, worden met deze dimensie geen gegevens verzameld.

Als u gegevens naar deze afmeting wilt verzenden gebruikend AppMeasurement:

* Vul de [`linkName`](/help/implement/vars/config-vars/linkname.md) variabele met de gewenste waarde.
* Stel de [`linkType`](/help/implement/vars/config-vars/linktype.md) variabele in op `"o"`.
* Verzend een [`tl()`](/help/implement/vars/functions/tl-method.md) afbeeldingsaanvraag.

## Dimensie-items

Aangezien deze variabele op een douanekoord in uw implementatie gebaseerd is, bepaalt uw organisatie wat de afmetingspunten zijn. Adobe raadt u aan om koppelingen in betekenisvolle categorieën te groeperen op basis van uw rapportagevereisten.
