---
title: kassier
description: Hiërarchievariabelen implementeren in Adobe Analytics.
translation-type: tm+mt
source-git-commit: ''

---


# kassier

Hiërarchievariabelen zijn aangepaste variabelen waarmee u de structuur van een site kunt zien.

Deze variabele is vooral handig voor sites met meer dan drie niveaus in de sitestructuur. Een mediasite kan bijvoorbeeld 4 niveaus bevatten voor de sectie Sport: Sport, Lokale Sport, Baseball en Red Sox. Als iemand de Baseball-pagina, Sport, Lokale Sport en Baseball bezoekt, weerspiegelen alle niveaus dat bezoek.

Er zijn vijf [!UICONTROL hierarchy] variabelen beschikbaar die door de klantenservice van Adobe moeten worden ingeschakeld. Op het moment dat de hiërarchie is ingeschakeld, moet u een scheidingsteken voor de variabele en het maximumaantal niveaus voor de hiërarchie instellen. Als het scheidingsteken bijvoorbeeld een komma is, kan de sporthiërarchie als volgt worden weergegeven.

```js
s.hier1="Sports,Local Sports,Baseball"
```

Zorg ervoor dat geen van uw sectienamen het scheidingsteken heeft. Als een van uw secties bijvoorbeeld &#39;Coach Griffin, Jim&#39; heet, moet u een ander scheidingsteken kiezen dan een komma. Elke hiërarchische sectie is beperkt tot 255 bytes, terwijl de totale veranderlijke grens 255 bytes is. Nadat een scheidingsteken is gekozen (op het moment dat de hiërarchie wordt gemaakt), wordt het niet gemakkelijk gewijzigd.

Neem contact op met de klantenservice van Adobe als u het scheidingsteken voor een bestaande hiërarchie wilt wijzigen. Scheidingstekens kunnen ook uit meerdere tekens bestaan, zoals|| of /|\, die minder waarschijnlijk in een hiërarchiesectie zullen verschijnen.

## Syntaxis en mogelijke waarden

Plaats geen spatie tussen elk scheidingsteken. In de volgende voorbeeldsyntaxis, is N een aantal tussen één en vijf.

```js
s.hierN="Level 1[<delimiter>Level 2[<delimiter>Level 3[...]]]"
```

Gebruik het scheidingsteken alleen om de niveaus van de hiërarchie te scheiden. Het scheidingsteken kan een willekeurig teken of tekens zijn.

## Voorbeelden

```js
s.hier1="Toys|Boys 6+|Legos|Super Block Tub"
```

```js
s.hier4="Sports/Local Sports/Baseball"
```

## Punten, vragen en tips

* Het scheidingsteken kan niet worden gewijzigd nadat de hiërarchie is ingesteld. Neem contact op met de klantenservice van Adobe als het scheidingsteken voor uw hiërarchie moet worden gewijzigd.
* Het aantal niveaus kan niet worden gewijzigd nadat de hiërarchie is ingesteld.

> [!NOTE] Wijzigingen in hiërarchieën kunnen servicekosten tot gevolg hebben.
