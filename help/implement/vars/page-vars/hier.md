---
title: hier
description: Hiërarchievariabelen implementeren in Adobe Analytics.
feature: Variables
exl-id: 72bdab8f-a001-4ada-b5e2-453a8e3f24a6
source-git-commit: a71db2fac9333b70a55da91fe9a94b0cc8434b42
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 1%

---

# kassier

Hiërarchievariabelen zijn aangepaste variabelen waarmee u de structuur van een site kunt zien.

>[!TIP]
>
>Deze variabele kwam vaker voor in eerdere versies van Adobe Analytics. Adobe raadt u aan [eVars](evar.md) en classificaties.

>[!IMPORTANT]
>
>Hiërarchie wordt niet ondersteund in gegevensverzameling met XDM for Experience Edge.

Deze variabele is handig voor sites met meer dan drie niveaus in hun sitestructuur. Een mediasite kan bijvoorbeeld 4 niveaus bevatten voor de sectie Sport: `Sports`, `Local Sports`, `Baseball`, en `Team name`. Als iemand de Baseball-pagina, Sport, Lokale Sport en Baseball bezoekt, weerspiegelen alle niveaus dat bezoek.

Adobe ondersteunt maximaal vijf hiërarchische variabelen in uw implementatie. Op het moment dat de hiërarchie is ingeschakeld, bepaalt u een scheidingsteken voor de variabele en het maximumaantal niveaus voor de hiërarchie. Als het scheidingsteken bijvoorbeeld een komma is, ziet de hiërarchie er als volgt uit:

```js
s.hier1 = "Sports,Local Sports,Baseball";
```

Zorg ervoor dat geen van uw sectienamen het scheidingsteken heeft. Als bijvoorbeeld een van uw secties wordt aangeroepen `Coach Griffin, Jim`kiest u een ander scheidingsteken dan een komma. De totale variabelelimiet is 255 bytes. Scheidingstekens kunnen uit meerdere tekens bestaan, zoals `||` of `/|\`, die minder waarschijnlijk in veranderlijke waarden zullen verschijnen.

## Voorbeelden

```js
s.hier1="Toys|Boys 6+|Legos|Super Block Tub";
```

```js
s.hier4="Sports/Local Sports/Baseball";
```
