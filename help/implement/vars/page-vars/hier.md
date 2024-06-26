---
title: kassier
description: (In ruste) Hiërarchievariabelen implementeren in Adobe Analytics.
feature: Variables
exl-id: 72bdab8f-a001-4ada-b5e2-453a8e3f24a6
role: Admin, Developer
source-git-commit: 75ae77c1da1b578639609888e794e13d965ef669
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 0%

---

# kassier

>[!IMPORTANT]
>
>Deze variabele wordt gepensioneerd en geen beschikbare dimensie in Analysis Workspace. Adobe raadt u aan [eVars](evar.md) en classificaties.

Hiërarchievariabelen zijn aangepaste variabelen waarmee u de structuur van een site kunt zien. Adobe ondersteunt maximaal vijf hiërarchische variabelen in uw implementatie.

Deze variabele is handig voor sites met meer dan drie niveaus in hun sitestructuur. Een mediasite kan bijvoorbeeld 4 niveaus bevatten voor de sectie Sport: `Sports`, `Local Sports`, `Baseball`, en `Team name`. Als iemand de Baseball-pagina, Sport, Lokale Sport en Baseball bezoekt, weerspiegelen alle niveaus dat bezoek.

Alvorens hiërarchieën in uw implementatie te gebruiken, zorg ervoor dat u elke hiërarchie in de montages van de rapportreeks vormt.

## Hiërarchieën die SDK van het Web gebruiken

Hiërarchieën zijn [toegewezen voor Adobe Analytics](/help/implement/aep-edge/xdm-var-mapping.md) onder de XDM-velden `xdm._experience.analytics.customDimensions.hierarchies.hier1` tot `xdm._experience.analytics.customDimensions.hierarchies.hier5`.

## Hiërarchieën die de Adobe Analytics-extensie gebruiken

U kunt hiërarchieën instellen tijdens het configureren van de extensie Analytics (algemene variabelen) of onder regels.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste tageigenschap.
3. Ga naar de [!UICONTROL Rules] klikt u op de gewenste regel (of maakt u een regel).
4. Onder [!UICONTROL Actions], klikt u op een bestaande [!UICONTROL Adobe Analytics - Set Variables] of klik op het pictogram &#39;+&#39;.
5. Stel de [!UICONTROL Extension] vervolgkeuzelijst naar Adobe Analytics en de [!UICONTROL Action Type] tot [!UICONTROL Set Variables].
6. Zoek de [!UICONTROL Hierarchy] sectie.

U kunt een hiërarchische waarde instellen op een statische tekenreeks of verwijzen naar een gegevenselement. U kunt ook het gewenste scheidingsteken instellen. Zorg ervoor dat het scheidingsteken dat u hier instelt, overeenkomt met het scheidingsteken dat is ingesteld in de instellingen van de rapportsuite.

## s.hier1 - s.hier5 in AppMeasurement en de de coderedacteur van de uitbreiding van de Analyse

Elke hiërarchie is een tekenreeks die aangepaste waarden bevat die specifiek zijn voor uw organisatie. De maximale lengte is 255 bytes. De waarden langer dan 255 bytes worden automatisch afgebroken wanneer ze naar de Adobe worden verzonden.

Zorg ervoor dat geen van uw sectienamen het scheidingsteken heeft. Als bijvoorbeeld een van uw secties wordt aangeroepen `Coach Griffin, Jim`kiest u een ander scheidingsteken dan een komma. De totale variabelelimiet is 255 bytes. Scheidingstekens kunnen uit meerdere tekens bestaan, zoals `||` of `/|\`, die minder waarschijnlijk in veranderlijke waarden zullen verschijnen.

```js
s.hier1 = "Toys|Boys 6+|Legos|Super Block Tub";

s.hier3 = "Sports/Local Sports/Baseball";
```
