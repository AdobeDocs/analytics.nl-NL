---
title: eVar (variabel)
description: Aangepaste variabelen die u kunt gebruiken in uw implementatie.
feature: Appmeasurement Implementation
exl-id: f89457b2-4186-4276-8637-9992070e3a73
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 0%

---

# eVar

*Deze hulppagina beschrijft hoe te om eVars uit te voeren. Voor informatie over hoe eVars als afmeting werken, zie [ Vars ](/help/components/dimensions/evar.md) in de de gebruikersgids van Componenten.*

Variabelen zijn aangepaste variabelen die u kunt gebruiken zoals u dat wilt. Als u het document van het a [ oplossingsontwerp ](/help/implement/prepare/solution-design.md) hebt, beëindigen de meeste dimensies specifiek voor uw organisatie omhoog als eVars. Standaard blijven de eVars behouden na de hit waarop ze zijn ingesteld. U kunt hun vervaldatum en toewijzing onder [ variabelen van de Omzetting ](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/conversion-var-admin.md) in de reeksinstellingen van het Rapport aanpassen.

Het aantal beschikbare eVars is afhankelijk van uw contract met Adobe. Er zijn maximaal 250 eVars beschikbaar als uw contract met Adobe dit ondersteunt.

## Vars instellen in instellingen van rapportsuite

Alvorens eVars in uw implementatie te gebruiken, zorg ervoor dat u elke eVar in de montages van de rapportreeks vormt. Zie [ variabelen van de Omzetting ](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/conversion-var-admin.md) in de gids Admin.

## Vars met de Web SDK

eVars worden toegewezen aan de volgende variabelen:

* [ voorwerp XDM ](/help/implement/aep-edge/xdm-var-mapping.md): `xdm._experience.analytics.customDimensions.eVars.eVar1` aan `xdm._experience.analytics.customDimensions.eVars.eVar250`
* [ voorwerp van Gegevens ](/help/implement/aep-edge/data-var-mapping.md): `data.__adobe.analytics.eVar1` aan `data.__adobe.analytics.eVar250`; of `data.__adobe.analytics.v1` aan `data.__adobe.analytics.v250`

## Vars met de Adobe Analytics-extensie

U kunt eVars instellen tijdens het configureren van de extensie Analytics (globale variabelen) of onder regels.

1. Login aan [ de Inzameling van Gegevens van Adobe Experience Platform ](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
2. Klik op de gewenste tageigenschap.
3. Ga naar het tabblad [!UICONTROL Rules] en klik vervolgens op de gewenste regel (of maak een regel).
4. Klik onder [!UICONTROL Actions] op een bestaande [!UICONTROL Adobe Analytics - Set Variables] -actie of klik op het plusteken (+).
5. Stel de vervolgkeuzelijst [!UICONTROL Extension] in op Adobe Analytics en op [!UICONTROL Action Type] op [!UICONTROL Set Variables] .
6. Zoek de sectie [!UICONTROL eVars] .

U kunt een eVar instellen op een waarde of een gegevenselement. U kunt de waarde ook uit een andere variabele Analytics kopiëren.

## s.eVar1 - s.eVar250 in AppMeasurement en de de redacteur van de de uitbreidingsdouanecode van de Analyse

Elke eVar is een tekenreeks die aangepaste waarden bevat die specifiek zijn voor uw organisatie. De maximale lengte is 255 bytes. De waarden langer dan 255 bytes worden automatisch afgekapt wanneer ze naar Adobe worden verzonden.

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

Als er meer dan twee decimalen zijn opgegeven, wordt de eVar-teller afgerond op twee decimalen. Een eVar-teller mag geen negatieve getallen bevatten.

>[!IMPORTANT]
>
>U moet eVars eerst aan &quot;Teller&quot;in Admin Console vormen alvorens tellervariabelen te gebruiken. Zie [ variabelen van de Omzetting ](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/conversion-var-admin.md) in de gids Admin.
