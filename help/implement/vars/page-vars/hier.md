---
title: kassier
description: (In ruste) Hiërarchievariabelen implementeren in Adobe Analytics.
feature: Appmeasurement Implementation
exl-id: 72bdab8f-a001-4ada-b5e2-453a8e3f24a6
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 0%

---

# kassier

>[!IMPORTANT]
>
>Deze variabele wordt gepensioneerd en geen beschikbare dimensie in Analysis Workspace. Adobe adviseert het gebruiken van [&#x200B; eVars &#x200B;](evar.md) en classificaties in plaats daarvan.

Hiërarchievariabelen zijn aangepaste variabelen waarmee u de structuur van een site kunt zien. Adobe ondersteunt maximaal vijf hiërarchische variabelen in uw implementatie.

Deze variabele is handig voor sites met meer dan drie niveaus in hun sitestructuur. Een mediasite kan bijvoorbeeld 4 niveaus bevatten voor de sectie Sport: `Sports`, `Local Sports`, `Baseball` en `Team name` . Als iemand de Baseball-pagina, Sport, Lokale Sport en Baseball bezoekt, weerspiegelen alle niveaus dat bezoek.

Alvorens hiërarchieën in uw implementatie te gebruiken, zorg ervoor dat u elke hiërarchie in de montages van de rapportreeks vormt.

## Hiërarchieën die het Web SDK gebruiken

De hiërarchieën worden [&#x200B; in kaart gebracht voor Adobe Analytics &#x200B;](/help/implement/aep-edge/xdm-var-mapping.md) onder de gebieden XDM `xdm._experience.analytics.customDimensions.hierarchies.hier1` aan `xdm._experience.analytics.customDimensions.hierarchies.hier5`.

## Hiërarchieën die de Adobe Analytics-extensie gebruiken

U kunt hiërarchieën instellen tijdens het configureren van de extensie Analytics (algemene variabelen) of onder regels.

1. Login aan [&#x200B; de Inzameling van Gegevens van Adobe Experience Platform &#x200B;](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
2. Klik op de gewenste tageigenschap.
3. Ga naar het tabblad [!UICONTROL Rules] en klik vervolgens op de gewenste regel (of maak een regel).
4. Klik onder [!UICONTROL Actions] op een bestaande [!UICONTROL Adobe Analytics - Set Variables] -actie of klik op het plusteken (+).
5. Stel de vervolgkeuzelijst [!UICONTROL Extension] in op Adobe Analytics en op [!UICONTROL Action Type] op [!UICONTROL Set Variables] .
6. Zoek de sectie [!UICONTROL Hierarchy] .

U kunt een hiërarchische waarde instellen op een statische tekenreeks of verwijzen naar een gegevenselement. U kunt ook het gewenste scheidingsteken instellen. Zorg ervoor dat het scheidingsteken dat u hier instelt, overeenkomt met het scheidingsteken dat is ingesteld in de instellingen van de rapportsuite.

## s.hier1 - s.hier5 in AppMeasurement en de aangepaste code-editor voor de extensie Analytics

Elke hiërarchie is een tekenreeks die aangepaste waarden bevat die specifiek zijn voor uw organisatie. De maximale lengte is 255 bytes. De waarden langer dan 255 bytes worden automatisch afgekapt wanneer ze naar Adobe worden verzonden.

Zorg ervoor dat geen van uw sectienamen het scheidingsteken heeft. Als een van uw secties bijvoorbeeld `Coach Griffin, Jim` wordt genoemd, kiest u een ander scheidingsteken dan een komma. De totale variabelelimiet is 255 bytes. Scheidingstekens kunnen bestaan uit meerdere tekens, zoals `||` of `/|\` , die minder vaak voorkomen in variabele waarden.

```js
s.hier1 = "Toys|Boys 6+|Legos|Super Block Tub";

s.hier3 = "Sports/Local Sports/Baseball";
```
