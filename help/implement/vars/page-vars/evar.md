---
title: eVar (variabele)
description: Aangepaste variabelen die u kunt gebruiken in uw implementatie.
feature: Variables
exl-id: f89457b2-4186-4276-8637-9992070e3a73
role: Admin, Developer
source-git-commit: 12347957a7a51dc1f8dfb46d489b59a450c2745a
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 0%

---

# eVar

*Deze Help-pagina beschrijft hoe eVars moet worden geïmplementeerd. Voor informatie over hoe eVars als dimensie werken, zie [eVars](/help/components/dimensions/evar.md) in de gebruikershandleiding van Componenten.*

Variabelen zijn aangepaste variabelen die u kunt gebruiken zoals u dat wilt. Als u een [document ontwerp oplossing](/help/implement/prepare/solution-design.md), komen de meeste dimensies die specifiek zijn voor uw organisatie neer als eVars. Standaard blijven de eVars behouden na de hit waarop ze zijn ingesteld. U kunt de vervaldatum en de toewijzing aanpassen onder [Conversievariabelen](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/conversion-var-admin.md) in de instellingen van de rapportsuite.

Het aantal beschikbare eVars is afhankelijk van uw contract met Adobe. Er zijn maximaal 250 eVars beschikbaar als uw contract met Adobe dit ondersteunt.

## Vars instellen in instellingen van rapportsuite

Alvorens eVars in uw implementatie te gebruiken, zorg ervoor dat u elke eVar in de montages van de rapportreeks vormt. Zie [Conversievariabelen](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/conversion-var-admin.md) in de handleiding Admin.

## Vars die SDK van het Web gebruiken

eVars worden toegewezen aan de volgende variabelen:

* [XDM-object](/help/implement/aep-edge/xdm-var-mapping.md): `xdm._experience.analytics.customDimensions.eVars.eVar1` tot `xdm._experience.analytics.customDimensions.eVars.eVar250`
* [Data, object](/help/implement/aep-edge/data-var-mapping.md): `data.__adobe.analytics.eVar1` tot `data.__adobe.analytics.eVar250`; of `data.__adobe.analytics.v1` tot `data.__adobe.analytics.v250`

## Vars met de Adobe Analytics-extensie

U kunt eVars instellen tijdens het configureren van de extensie Analytics (globale variabelen) of onder regels.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste tageigenschap.
3. Ga naar de [!UICONTROL Rules] klikt u op de gewenste regel (of maakt u een regel).
4. Onder [!UICONTROL Actions], klikt u op een bestaande [!UICONTROL Adobe Analytics - Set Variables] of klik op het pictogram &#39;+&#39;.
5. Stel de [!UICONTROL Extension] vervolgkeuzelijst naar Adobe Analytics en de [!UICONTROL Action Type] tot [!UICONTROL Set Variables].
6. Zoek de [!UICONTROL eVars] sectie.

U kunt een eVar instellen op een waarde of een gegevenselement. U kunt de waarde ook uit een andere variabele Analytics kopiëren.

## s.eVar1 - s.eVar250 in AppMeasurement en de de redacteur van de de uitbreidingsdouanecode van de Analyse

Elke eVar is een tekenreeks die aangepaste waarden bevat die specifiek zijn voor uw organisatie. De maximale lengte is 255 bytes. De waarden langer dan 255 bytes worden automatisch afgebroken wanneer ze naar de Adobe worden verzonden.

```js
s.eVar1 = "Example custom value";
```

## Counter Vars

eVar-waarden bevatten doorgaans een tekenreekswaarde. Nochtans, kunt u eVars vormen om in plaats daarvan een teller te bevatten. U wilt bijvoorbeeld het aantal interne zoekopdrachten tellen dat is uitgevoerd voordat u een aankoop doet. In plaats van een tekstwaarde in te stellen, gebruikt u de volgende syntaxis:

```js
// Increment a counter eVar by 1
s.eVar1 = "+1";

// Increment a counter eVar by 12.49
s.eVar1 = "+12.49";
```

Als er meer dan twee decimalen zijn opgegeven, wordt de eVar-teller afgerond tot twee decimalen. Een eVar-teller mag geen negatieve getallen bevatten.

>[!IMPORTANT]
>
>U moet eVars aan &quot;Teller&quot;in de Admin Console eerst vormen alvorens tellervariabelen te gebruiken. Zie [Conversievariabelen](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/conversion-var-admin.md) in de handleiding Admin.
