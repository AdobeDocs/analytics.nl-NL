---
description: Adobe Analytics ondersteunt classificatiemodellen op één niveau en op meerdere niveaus. Met een classificatiehiërarchie kunt u een classificatie toepassen op een classificatie.
title: Informatie over subclassificaties
feature: Classifications
exl-id: 3d22a8c0-743d-47f3-ba15-aaef1ebd4dff
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: tm+mt
source-wordcount: '644'
ht-degree: 7%

---

# Informatie over subclassificaties

Adobe Analytics ondersteunt classificatiemodellen op één niveau en die op meerdere niveaus. Met een classificatiehiërarchie kunt u een classificatie toepassen op een classificatie.

>[!NOTE]
>
>Subclassificatie heeft betrekking op de mogelijkheid classificaties van classificaties te maken. Dit is echter niet hetzelfde als een [!UICONTROL Classification Hierarchy] gebruikt om te maken [!UICONTROL Hierarchy] rapporten. Voor meer informatie over classificatiehiërarchieën raadpleegt u [Classificatiehiërarchieën](/help/admin/admin/conversion-var-admin/classification-hierarchies.md).

Bijvoorbeeld:

![](assets/single-level-popup-C.png)

Elke classificatie in dit model is onafhankelijk en komt overeen met een nieuw subrapport voor de geselecteerde rapportagevariabele. Bovendien vormt elke classificatie één gegevenskolom in het gegevensbestand, met de classificatienaam als kolomkop. Bijvoorbeeld:

| SLEUTEL | EIGENSCHAP 1 | EIGENSCHAP 2 |
|---|---|---|
| 123 | ABC | A12B |
| 456 | DEF | C3D4 |

Zie voor meer informatie over het gegevensbestand [Classificatiegegevensbestanden](/help/components/classifications/importer/c-saint-data-files.md).

Classificaties op meerdere niveaus bestaan uit ouder- en onderliggende classificaties. Bijvoorbeeld:

![](assets/Multi-Level-Class-popup.png)

**Bovenliggende classificaties:** Een ouderclassificatie is om het even welke classificatie die een bijbehorende kindclassificatie heeft. Een classificatie kan zowel een ouderclassificatie als een kindclassificatie zijn. De bovenliggende classificaties komen overeen met classificaties op één niveau.

**Onderliggende classificaties:** Een onderliggende classificatie is een classificatie die een andere classificatie heeft als de bovenliggende klasse in plaats van de variabele. Onderliggende classificaties bieden aanvullende informatie over hun ouderclassificatie. Bijvoorbeeld een [!UICONTROL Campaigns] de classificatie zou een de kindclassificatie van de Eigenaar van de Campagne kunnen hebben. [!UICONTROL Numeric] classificaties functioneren ook als metriek in classificatierapporten.

Elke classificatie, bovenliggend of onderliggend, vormt één gegevenskolom in het gegevensbestand. De kolomkop voor een onderliggende classificatie met de volgende notatie:

`<parent_name>^<child_name>`

Voor meer informatie over de indeling van het gegevensbestand raadpleegt u [Classificatiegegevensbestanden](/help/components/classifications/importer/c-saint-data-files.md).

Bijvoorbeeld:

| SLEUTEL | EIGENSCHAP 1 | Eigenschap 1^Eigenschap 1-1 | Eigenschap 1^Eigenschap 1-2 | Eigenschap 2 |
|---|---|---|---|---|
| 123 | ABC | Groen | Klein | A12B |
| 456 | DEF | Rood | Groot | C3D4 |

Hoewel het dossiermalplaatje voor een classificatie op meerdere niveaus complexer is, is de macht van classificaties op meerdere niveaus dat de afzonderlijke niveaus als afzonderlijke dossiers kunnen worden geupload. Deze benadering kan worden gebruikt om de hoeveelheid gegevens te minimaliseren die periodiek (dagelijks, wekelijks, etc.) moet worden geupload door gegevens in classificatieniveaus te groeperen die in tijd tegenover die veranderen die niet.

>[!NOTE]
>
>Als de [!UICONTROL Key] in een gegevensbestand leeg is, genereert Adobe automatisch unieke sleutels voor elke gegevensrij. Als u mogelijke bestandsbeschadiging wilt voorkomen tijdens het uploaden van een gegevensbestand met classificatiegegevens op tweede of hoger niveau, vult u elke rij van de [!UICONTROL Key] kolom met een asterisk (*).

## Voorbeelden

![](assets/sample-product-classifications.png)

>[!NOTE]
>
>Gegevens over de indeling van producten zijn beperkt tot gegevenskenmerken die rechtstreeks verband houden met het product. De gegevens zijn niet beperkt tot de wijze waarop de producten zijn gecategoriseerd of op de website worden verkocht. Gegevenselementen zoals verkoopcategorieën, browserknooppunten van sites of verkoopitems zijn geen gegevens over de productclassificatie. In plaats daarvan worden deze elementen vastgelegd in de conversievariabelen van rapporten.

Wanneer u gegevensbestanden uploadt voor deze productclassificatie, kunt u de classificatiegegevens uploaden als één bestand of als meerdere bestanden (zie hieronder). Door de kleurcode in bestand 1 en de kleurnaam in bestand 2 te scheiden, hoeven de gegevens over de kleurnaam (die mogelijk slechts een paar rijen zijn) alleen te worden bijgewerkt wanneer nieuwe kleurcodes worden gemaakt. Hiermee verwijdert u het kleurnaamveld (CODE^COLOR) uit het vaker bijgewerkte bestand 1 en verkleint u de bestandsgrootte en complexiteit bij het genereren van het gegevensbestand.

### Productclassificatie - Eén bestand {#section_E8C5E031869C449F9B636F5EB3BFEC17}

| SLEUTEL | PRODUCTNAAM | PRODUCTGEGEVENS | GENDER | GROOTTE | CODE | CODE^KLEUR |
|---|---|---|---|---|---|---|
| 410390013 | Polo-SS | Polo Shirt, korte hoes (M,01) voor heren | M | M | 01 | Steen |
| 410390014 | Polo-SS | Polo Shirt, korte hoes (L,03) voor heren | M | L | 03 | Heather |
| 410390015 | Polo-LS | Polo Shirt, lange hoes (S,23) | F | S | 23 | Aqua |

### Productclassificatie - Meerdere bestanden (bestand 1) {#section_A99F7D0F145540069BA4EEC0597FF13F}

| SLEUTEL | PRODUCTNAAM | PRODUCTGEGEVENS | GENDER | GROOTTE | CODE |
|---|---|---|---|---|---|
| 410390013 | Polo-SS | Polo Shirt, korte hoes (M,01) voor heren | M | M | 01 |
| 410390014 | Polo-SS | Polo Shirt, korte hoes (L,03) voor heren | M | L | 03 |
| 410390015 | Polo-LS | Polo Shirt, lange hoes (S,23) | F | S | 23 |

### Productclassificatie - Meerdere bestanden (bestand 2) {#section_19ED95C33B174A9687E81714568D56A3}

| SLEUTEL | CODE | CODE^KLEUR |
|---|---|---|
| * | 01 | Steen |
| * | 03 | Heather |
| * | 23 | Aqua |
