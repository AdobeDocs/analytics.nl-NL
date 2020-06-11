---
title: Koppeling afsluiten
description: De naam van de afsluitkoppeling.
translation-type: tm+mt
source-git-commit: c9e696201d0e9ec97dcdd6ff797ca72244dcf366
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 0%

---


# Koppeling afsluiten

De dimensie &#39;Verbinding van de Uitgang&#39; meldt de namen van uitgangsverbindingen die op uw plaats worden uitgevoerd. Deze dimensie is waardevol wanneer u wilt begrijpen welke verbindingen het populairst zijn dat aan domeinen buiten uw plaats richten.

## Deze dimensie vullen met gegevens

Deze afmeting verzamelt gegevens van het [`pev2` vraagkoord](/help/implement/validate/query-parameters.md) in beeldverzoeken voor treffers die ook het `pe` vraagkoord met de waarde van `lnk_e`hebben. Als de `pe` queryreeks een andere waarde heeft in de hit, worden met deze dimensie geen gegevens verzameld.

Als u gegevens naar deze afmeting wilt verzenden gebruikend AppMeasurement:

* Vul de [`linkName`](/help/implement/vars/config-vars/linkname.md) variabele met de gewenste waarde.
* Stel de [`linkType`](/help/implement/vars/config-vars/linktype.md) variabele in op `"e"`.
* Verzend een [`tl()`](/help/implement/vars/functions/tl-method.md) afbeeldingsaanvraag.

## Dimensiewaarden

Aangezien deze variabele op een douanekoord in uw implementatie gebaseerd is, bepaalt uw organisatie wat de afmetingswaarden zijn. Adobe raadt u aan om koppelingen in betekenisvolle categorieën te groeperen op basis van uw rapportagevereisten.
