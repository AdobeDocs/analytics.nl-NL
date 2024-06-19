---
title: Hiërarchie
description: (In ruste) Een aangepaste dimensie die u kunt gebruiken voor rapportage.
feature: Dimensions
exl-id: f9bd3ae1-3578-44c5-a540-ea93feac5bef
source-git-commit: 75ae77c1da1b578639609888e794e13d965ef669
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 0%

---

# Hiërarchie

>[!IMPORTANT]
>
>Deze dimensie is uitgeschakeld en niet beschikbaar [dimensie](overview.md) in Analysis Workspace. Adobe raadt u aan [eVars](evar.md) en classificaties.

De hiërarchieën zijn douanevariabelen die u kunt gebruiken hoe u zou willen. Ze blijven niet bestaan na de treffer die ze zijn ingesteld. Er zijn maximaal vijf hiërarchieën beschikbaar als uw contract met Adobe dit ondersteunt.

## Hiërarchieën vullen met gegevens

Elke hiërarchie verzamelt gegevens van de [`h1` - `h5` querytekenreeks](/help/implement/validate/query-parameters.md) in afbeeldingsaanvragen. Bijvoorbeeld de `h1` de parameter van het vraagkoord verzamelt gegevens voor Hiërarchie 1, terwijl `h4` de parameter van het vraagkoord verzamelt gegevens voor Hiërarchie 4.

AppMeasurement, dat JavaScript-variabelen compileert in een afbeeldingsaanvraag voor gegevensverzameling, gebruikt de variabelen `hier1` - `hier5`. Zie [kassier](/help/implement/vars/page-vars/hier.md) in de gebruikershandleiding Implementeren voor implementatierichtlijnen.

## Dimension-items

Aangezien de hiërarchieën douanekoorden in uw implementatie bevatten, bepaalt uw organisatie wat de afmetingspunten voor elke hiërarchie zijn. Zorg ervoor dat u het doel van elke hiërarchie en typische afmetingspunten in een registreert [document ontwerp oplossing](/help/implement/prepare/solution-design.md).
