---
title: kassier
description: Hiërarchievariabelen implementeren in Adobe Analytics.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# kassier

Hiërarchievariabelen zijn aangepaste variabelen waarmee u de structuur van een site kunt zien.

>[!TIP] Deze variabele kwam vaker voor in eerdere versies van Adobe Analytics. Adobe raadt u aan [Vars](evar.md) en classificaties te gebruiken.

Deze variabele is handig voor sites met meer dan drie niveaus in hun sitestructuur. Een mediasite kan bijvoorbeeld 4 niveaus bevatten voor de sectie Sport: `Sports`, `Local Sports`, `Baseball`en `Team name`. Als iemand de Baseball-pagina, Sport, Lokale Sport en Baseball bezoekt, weerspiegelen alle niveaus dat bezoek.

Adobe ondersteunt maximaal vijf hiërarchische variabelen in uw implementatie. Op het moment dat de hiërarchie is ingeschakeld, bepaalt u een scheidingsteken voor de variabele en het maximumaantal niveaus voor de hiërarchie. Als het scheidingsteken bijvoorbeeld een komma is, ziet de hiërarchie er als volgt uit:

```js
s.hier1 = "Sports,Local Sports,Baseball";
```

Zorg ervoor dat geen van uw sectienamen het scheidingsteken heeft. Als een van uw secties bijvoorbeeld wordt aangeroepen `Coach Griffin, Jim`, kiest u een ander scheidingsteken dan een komma. De totale variabelelimiet is 255 bytes. Scheidingstekens kunnen bestaan uit meerdere tekens, zoals `||` of `/|\`, die minder vaak voorkomen in variabele waarden.

## Voorbeelden

```js
s.hier1="Toys|Boys 6+|Legos|Super Block Tub";
```

```js
s.hier4="Sports/Local Sports/Baseball";
```
